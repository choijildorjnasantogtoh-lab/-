<!-- Scripts -->
<script>
/* === SETTINGS === */
const PROMO_CODE = 'VIPBet247';
const AFFILIATE_URL = 'https://refpa3665.com/L?tag=d_4194631m_66329c_&site=4194631&ad=66329';
const HARD_END = new Date('2025-12-31T23:59:59');

/* === TRANSLATIONS === */
const translations = {
  mn: { /* ...монгол контент... */ },
  en: {
    title: "🏆 Register at Melbet and Get a 100% BONUS!",
    subtitle: "Welcome offer for international players – sports betting and casino games! 🎰⚽",
    promoCode: "🎁 Make your first deposit and receive an equal bonus amount (up to $10,000). In other words, your account balance will double!",
    promoText: "👉 Use the <strong>VIPBet247</strong> code during registration to claim your bonus!",
    telegramText: "📲 Join our Telegram channel! Melbet registration guides and updates!",
    featuresTitle: "🎮 Melbet Features",
    features: [
      "🎰 <strong>5,000+</strong> Casino games (Slots, Table Games)",
      "🃏 <strong>600+</strong> Live dealer casino games",
      "⚽ Betting on <strong>40+</strong> sports",
      "🏀 <strong>~200</strong> live sports events daily",
      "♠️ Online poker, virtual sports, and more"
    ],
    howToTitle: "📲 How to Register?",
    howTo: [
      "Click the official <a href=\"https://refpa3665.com/L?tag=d_4194631m_66329c_&site=4194631&ad=66329\" target=\"_blank\" rel=\"noopener noreferrer nofollow\">Melbet link</a> below.",
      "Sign up as a new user (via email, phone number, or one-click registration).",
      "Enter <strong>VIPBet247</strong> in the <strong>Promo Code</strong> field.",
      "Make your first deposit (minimum $1) to double your balance up to $10,000 with a 100% bonus!"
    ],
    examplesTitle: "📊 Bonus Examples:",
    examples: "• Deposit $1 → Total $2<br>• Deposit $5 → Total $10<br>• Deposit $100 → Total $200<br>• Deposit $1,000 → Total $2,000",
    registerButton: "👉 Register at Melbet",
    copyButton: "Copy Promo Code",
    calculatorTitle: "💰 Bonus Calculator",
    calculateButton: "Calculate",
    telegramButton: "Join Telegram",
    promoTimer: "Time left for promo code:",
    disclaimer: "<p><strong>Responsible Gaming Notice:</strong> For users aged 18+. Gamble responsibly within your means. Bonus terms: 5x wagering (accumulator, 1.40+ odds, 3+ events), 30-day validity. See details at <a href=\"https://melbet.com/en/information/rules\" target=\"_blank\" rel=\"noopener noreferrer\">Melbet Terms</a>.</p><p>© 2025 Melbet. All rights reserved.</p>",
    copyMessage: "PROMO CODE VIPBet247 copied! Use it during registration.",
    copyError: "Could not copy: Please copy VIPBet247 manually.",
    expired: "Expired! Restarting in 7 days...",
    timerUnits: { days: "d", hours: "h", minutes: "m", seconds: "s" },
    calculator: {
      deposit: "Deposit ($)",
      bonus: "Bonus",
      total: "Total",
      calculateButton: "Calculate",
      invalid: "Please enter at least $1 and max $10,000 (no negatives)."
    }
  },
  ru: { /* ...орос контент... */ },
  vi: { /* ...вьетнам контент... */ }
};

/* === LANGUAGE DETECTION & CHANGE (ALWAYS DEFAULT TO MN IF NOT EXIST) === */
function changeLanguage(lang) {
  if (!translations[lang]) lang = 'mn';
  const t = translations[lang];
  document.getElementById('title').innerHTML = t.title;
  document.getElementById('subtitle').innerHTML = t.subtitle;
  document.getElementById('promo-code-text').innerHTML = t.promoCode;
  document.getElementById('promo-note').innerHTML = t.promoText;
  document.getElementById('promo-display').textContent = PROMO_CODE;
  document.getElementById('calculator-title').innerHTML = t.calculatorTitle;
  document.getElementById('calculate-button').textContent = t.calculator.calculateButton;
  document.getElementById('copy-btn').textContent = t.copyButton;
  document.querySelectorAll('.register-button').forEach(btn => btn.textContent = t.registerButton);
  document.getElementById('promo-timer').innerHTML = `${t.promoTimer} <div id="countdown" class="mt-2" aria-live="polite"></div>`;

  // features
  const featuresList = document.getElementById('features');
  featuresList.innerHTML = '';
  (t.features || []).forEach(f => {
    const li = document.createElement('li');
    li.innerHTML = f;
    featuresList.appendChild(li);
  });

  // how-to
  const howList = document.getElementById('how-to');
  howList.innerHTML = '';
  (t.howTo || []).forEach(step => {
    const li = document.createElement('li');
    li.innerHTML = step;
    howList.appendChild(li);
  });

  // examples
  document.getElementById('examples').innerHTML = t.examples || '';

  // disclaimer
  document.getElementById('disclaimer').innerHTML = t.disclaimer || document.getElementById('disclaimer').innerHTML;

  // language button label and aria-selected
  const selectedLabel = document.querySelector(`#language-list li[data-value="${lang}"]`);
  if (selectedLabel) {
    document.getElementById('language-button').innerHTML = `🌐 ${selectedLabel.textContent}`;
  } else {
    document.getElementById('language-button').innerHTML = `🌐 ${lang}`;
  }
  document.querySelectorAll('#language-list li').forEach(item => {
    item.setAttribute('aria-selected', item.getAttribute('data-value') === lang);
  });

  document.documentElement.lang = lang;
  localStorage.setItem('preferredLanguage', lang);
  startCountdown();
}

/* ... Таны бусад функцууд хэвээр ... */

</script># -
