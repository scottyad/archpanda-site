---
title: "Fix Assistant"
description: "Instant DOM & A11y Remediation Inside Chrome DevTools"
layout: landing
draft: false
---

{{< rawhtml >}}

<!-- Navigation Header -->
<nav class="fa-nav">
  <div class="fa-nav-inner">
    <a href="#" class="fa-logo">
      <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round">
        <polyline points="13 2 13 9 20 9"></polyline>
        <path d="M4 22V8a2 2 0 0 1 2-2h8.5L20 11.5V20a2 2 0 0 1-2 2Z"></path>
      </svg>
      <span>Fix Assistant</span>
      <span class="fa-badge">DevTools Native</span>
    </a>
    <ul class="fa-nav-links">
      <li><a href="#features">Features</a></li>
      <li><a href="#how-it-works">How It Works</a></li>
      <li><a href="#demo">Live Demo</a></li>
      <li><a href="#pricing">Pricing</a></li>
      <li><a href="#faq">FAQ</a></li>
    </ul>
    <a href="#pricing" class="fa-cta-btn">Get Lifetime Access</a>
  </div>
</nav>

<!-- Hero Section -->
<section class="fa-hero">
  <div class="fa-hero-inner">
    <div class="fa-hero-text">
      <div class="fa-hero-badge">
        <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><polygon points="13 2 3 14 12 14 11 22 21 10 12 10 13 2"></polygon></svg>
        Instant DOM & A11y Remediation Inside Chrome DevTools
      </div>
      <h1>Stop Guessing Console Errors.<br>Fix Broken UI & Forms Directly in DevTools.</h1>
      <p class="fa-hero-sub">Fix Assistant inspects your active DOM subtree, diagnoses WCAG accessibility traps, broken form validations, and lockout defects, then generates and runs the exact fix script in real time.</p>
      <div class="fa-hero-ctas">
        <a href="#pricing" class="fa-btn-primary">Get Lifetime License — $49 <span>(One-Time)</span></a>
        <a href="#demo" class="fa-btn-secondary">
          <svg width="18" height="18" viewBox="0 0 24 24" fill="currentColor"><polygon points="5 3 19 12 5 21 5 3"></polygon></svg>
          Watch 60s Demo
        </a>
      </div>
      <p class="fa-hero-proof">
        Works on local dev servers, staging, and production · Zero vendor lock-in · Powered by Claude Haiku
      </p>
    </div>
    <div class="fa-hero-visual">
      <div class="fa-devtools-mockup">
        <div class="fa-dt-header">
          <div class="fa-dt-dots">
            <span></span><span></span><span></span>
          </div>
          <span class="fa-dt-title">Chrome DevTools — Fix Assistant</span>
        </div>
        <div class="fa-dt-body">
          <div class="fa-dt-panel fa-dt-left">
            <div class="fa-dt-panel-title">🔍 Inspector</div>
            <div class="fa-dt-tree">
              <div class="fa-dt-node fa-dt-err">&lt;form&gt;</div>
              <div class="fa-dt-node fa-dt-indent">&lt;input <span class="fa-dt-highlight">type="email"</span> /&gt;</div>
              <div class="fa-dt-node fa-dt-indent fa-dt-err">&lt;input <span class="fa-dt-highlight">disabled</span> /&gt; ⚠️</div>
              <div class="fa-dt-node fa-dt-indent">&lt;button&gt;Submit&lt;/button&gt;</div>
            </div>
            <div class="fa-dt-diagnosis">
              <strong>⚠️ Issues Found:</strong>
              <ul>
                <li>Missing <code>label</code> for email input</li>
                <li>Input is <code>disabled</code> — form lockout</li>
                <li>No <code>aria-describedby</code></li>
              </ul>
            </div>
          </div>
          <div class="fa-dt-panel fa-dt-right">
            <div class="fa-dt-panel-title">🛠️ Fix Assistant</div>
            <div class="fa-dt-script">
<pre><code>// Generated Fix Script
const email = document.querySelector('input[type="email"]');
email.setAttribute('aria-label', 'Email address');
email.removeAttribute('disabled');
email.parentElement.insertBefore(
  Object.assign(document.createElement('label'), {
    htmlFor: email.id,
    textContent: 'Email'
  }),
  email
);</code></pre>
            </div>
            <button class="fa-dt-exec">▶ Execute Fix</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- Problem vs Solution -->
<section class="fa-section fa-problem" id="problem">
  <div class="fa-section-inner">
    <h2>The Dev Pain Point</h2>
    <div class="fa-compare">
      <div class="fa-compare-card fa-compare-old">
        <h3>🔴 The Old Way</h3>
        <ul>
          <li>Open DevTools and manually inspect deeply nested DOM trees</li>
          <li>Search stack traces across multiple files</li>
          <li>Switch to Claude/ChatGPT in another tab</li>
          <li>Copy-paste HTML back and forth</li>
          <li>Manually apply edits and hope they work</li>
        </ul>
      </div>
      <div class="fa-compare-arrow">→</div>
      <div class="fa-compare-card fa-compare-new">
        <h3>🟢 The Fix Assistant Way</h3>
        <ul>
          <li>One click inside DevTools</li>
          <li>Extension reads the active DOM node automatically</li>
          <li>Diagnoses form lockout bugs and WCAG violations instantly</li>
          <li>Generates clean vanilla JS/framework patches</li>
          <li>Test the fix live with one click</li>
        </ul>
      </div>
    </div>
  </div>
</section>

<!-- Core Features Grid -->
<section class="fa-section fa-features" id="features">
  <div class="fa-section-inner">
    <h2>Core Features</h2>
    <div class="fa-features-grid">
      <div class="fa-feature-card">
        <div class="fa-feature-icon">🔧</div>
        <h3>Live Form & Validation Repair</h3>
        <p>Detects broken regex patterns, mismatched constraints, and accidental disabled lockouts before they frustrate users.</p>
      </div>
      <div class="fa-feature-card">
        <div class="fa-feature-icon">♿</div>
        <h3>Automated WCAG & A11y Auditing</h3>
        <p>Identifies missing ARIA labels, unassociated inputs, and missing alt attributes instantly as you develop.</p>
      </div>
      <div class="fa-feature-card">
        <div class="fa-feature-icon">▶️</div>
        <h3>One-Click Script Execution</h3>
        <p>Safely injects and tests generated fixes directly into the live page DOM to verify results instantly.</p>
      </div>
      <div class="fa-feature-card">
        <div class="fa-feature-icon">🌳</div>
        <h3>Subtree-Aware Context</h3>
        <p>Transmits clean, truncated DOM snippets without bloating token costs or leaking sensitive session data.</p>
      </div>
      <div class="fa-feature-card">
        <div class="fa-feature-icon">📋</div>
        <h3>Instant Diff & Patch Generation</h3>
        <p>View exact code changes to copy directly into your React, Vue, Svelte, or HTML source files.</p>
      </div>
      <div class="fa-feature-card">
        <div class="fa-feature-icon">🔑</div>
        <h3>Local & Cloud Backend Support</h3>
        <p>Powered by high-speed Claude Haiku with built-in BYOK support for custom API keys or local Ollama endpoints.</p>
      </div>
    </div>
  </div>
</section>

<!-- How It Works -->
<section class="fa-section fa-how" id="how-it-works">
  <div class="fa-section-inner">
    <h2>How It Works</h2>
    <div class="fa-steps">
      <div class="fa-step">
        <div class="fa-step-num">1</div>
        <h3>Inspect</h3>
        <p>Open Chrome DevTools (F12) and navigate to the Fix Assistant tab on any web page or local dev port.</p>
      </div>
      <div class="fa-step-arrow">→</div>
      <div class="fa-step">
        <div class="fa-step-num">2</div>
        <h3>Diagnose</h3>
        <p>Fix Assistant reads the targeted DOM node and flags broken attributes, missing labels, and logic traps.</p>
      </div>
      <div class="fa-step-arrow">→</div>
      <div class="fa-step">
        <div class="fa-step-num">3</div>
        <h3>Remediate</h3>
        <p>Click "Execute Fix" to verify the repair live in your browser, or copy the generated script into your codebase.</p>
      </div>
    </div>
  </div>
</section>

<!-- Live Demo -->
<section class="fa-section fa-demo" id="demo">
  <div class="fa-section-inner">
    <div style="text-align:center;margin-bottom:28px">
      <p class="eyebrow" style="color:#b6f36a;text-transform:uppercase;letter-spacing:.16em;font-size:12px;font-weight:800;margin:0 0 10px">Interactive Demo</p>
      <h2 style="font-size:clamp(24px,2.5vw,36px);line-height:1.15;letter-spacing:-.045em;margin:0 0 14px">Try It Before You Install</h2>
      <p style="color:#a7b5bf;margin:0;line-height:1.55;font-size:16px;max-width:640px;display:inline-block">See how Fix Assistant diagnoses a broken billing form, highlights the exact code changes, and generates a ready-to-review patch — no extension required.</p>
    </div>
    <div style="background:#151d27;border:1px solid #30404b;border-radius:16px;overflow:hidden;box-shadow:0 18px 45px #05090d44;margin-bottom:22px">
      <iframe src="/fix-assistant/demo/" style="width:100%;height:520px;border:0;display:block" title="Fix Assistant Interactive Demo" loading="lazy"></iframe>
    </div>
    <div style="text-align:center">
      <a href="/fix-assistant/demo/" target="_blank" class="fa-btn-secondary" style="display:inline-flex;align-items:center;gap:10px">
        <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M18 13v6a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h6"></path><polyline points="15 3 21 3 21 9"></polyline><line x1="10" y1="14" x2="21" y2="3"></line></svg>
        Open Demo in New Tab
      </a>
    </div>
  </div>
</section>

<!-- Pricing Table -->
<section class="fa-section fa-pricing" id="pricing">
  <div class="fa-section-inner">
    <h2>Transparent Lifetime Pricing</h2>
    <p class="fa-pricing-sub">One-time payment. No subscriptions. No surprises.</p>
    <div class="fa-pricing-grid">
      <div class="fa-pricing-card">
        <div class="fa-pricing-header">
          <h3>Haiku Starter</h3>
          <div class="fa-pricing-price">$49</div>
          <div class="fa-pricing-note">One-Time Lifetime</div>
        </div>
        <ul class="fa-pricing-features">
          <li>200 AI Audits / month</li>
          <li>Powered by Claude Haiku</li>
          <li>Form validation & A11y engine</li>
          <li>Live DOM script injection</li>
          <li>Future v1.x updates included</li>
        </ul>
        <a href="#" class="fa-pricing-cta">Buy Starter Lifetime</a>
      </div>
      <div class="fa-pricing-card fa-pricing-popular">
        <div class="fa-pricing-popular-badge">Most Popular</div>
        <div class="fa-pricing-header">
          <h3>Haiku Pro</h3>
          <div class="fa-pricing-price">$89</div>
          <div class="fa-pricing-note">One-Time Lifetime</div>
          <div class="fa-pricing-value">Best Value</div>
        </div>
        <ul class="fa-pricing-features">
          <li>500 AI Audits / month</li>
          <li>Everything in Starter</li>
          <li>Priority Claude Haiku pipeline</li>
          <li>Framework patch generator</li>
          <li>Multi-device license (3 seats)</li>
        </ul>
        <a href="#" class="fa-pricing-cta fa-pricing-cta-primary">Buy Pro Lifetime</a>
      </div>
      <div class="fa-pricing-card">
        <div class="fa-pricing-header">
          <h3>Power BYOK</h3>
          <div class="fa-pricing-price">$39</div>
          <div class="fa-pricing-note">One-Time Lifetime</div>
        </div>
        <ul class="fa-pricing-features">
          <li>Unlimited audits</li>
          <li>Bring Your Own API Key</li>
          <li>Local model support (Ollama)</li>
          <li>All features unlocked forever</li>
        </ul>
        <a href="#" class="fa-pricing-cta">Buy BYOK License</a>
      </div>
    </div>
  </div>
</section>

<!-- FAQ Section -->
<section class="fa-section fa-faq" id="faq">
  <div class="fa-section-inner">
    <h2>Frequently Asked Questions</h2>
    <div class="fa-faq-grid">
      <div class="fa-faq-card">
        <h3>How do monthly query limits work on a lifetime deal?</h3>
        <p>Your audits refresh automatically on the 1st of every month. No recurring fees ever.</p>
      </div>
      <div class="fa-faq-card">
        <h3>Does Fix Assistant send my entire webpage to an LLM?</h3>
        <p>No. It only serializes the selected element and relevant DOM subtree, keeping payloads small, fast, and private.</p>
      </div>
      <div class="fa-faq-card">
        <h3>Can I use my own API keys or local models?</h3>
        <p>Yes. The extension supports BYOK mode for Anthropic, OpenAI, and local Ollama instances.</p>
      </div>
      <div class="fa-faq-card">
        <h3>Does it work on localhost and staging sites?</h3>
        <p>Yes. Because it runs locally inside Chrome DevTools, it inspects any URL accessible in your browser.</p>
      </div>
    </div>
  </div>
</section>

<!-- Footer -->
<footer class="fa-landing-footer">
  <div class="fa-footer-inner">
    <div class="fa-footer-brand">
      <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round">
        <polyline points="13 2 13 9 20 9"></polyline>
        <path d="M4 22V8a2 2 0 0 1 2-2h8.5L20 11.5V20a2 2 0 0 1-2 2Z"></path>
      </svg>
      Fix Assistant
    </div>
    <div class="fa-footer-links">
      <a href="/privacy">Privacy Policy</a>
      <a href="/terms">Terms of Service</a>
      <a href="https://chrome.google.com/webstore">Chrome Web Store</a>
      <a href="mailto:support@fixassistant.dev">support@fixassistant.dev</a>
    </div>
    <p class="fa-footer-copy">© 2024 Fix Assistant. All rights reserved.</p>
  </div>
</footer>

{{< /rawhtml >}}
