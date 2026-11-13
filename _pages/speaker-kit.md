---
permalink: /speaker-kit/
title: "Speaker Kit"
author_profile: true
---

Organizers: feel free to use anything on this page for agendas, websites and announcements — no need to ask.

<style>
.photo-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
  gap: 1em;
  align-items: start;
}
.photo-grid img {
  width: 100%;
  aspect-ratio: 4 / 3;
  object-fit: cover;
  display: block;
  border-radius: 4px;
}
.copy-bio {
  display: inline-block;
  margin-top: 0.4em;
  padding: 0.15em 0.65em;
  font-size: 0.8em;
  line-height: 1.5;
  color: inherit;
  background: transparent;
  border: 1px solid currentColor;
  border-radius: 4px;
  cursor: pointer;
  opacity: 0.7;
}
.copy-bio:hover,
.copy-bio:focus { opacity: 1; }
</style>

## Name & title
**Mr. Thi Nguyen Dinh** — Senior Solutions Architect, Generative AI & Agentic Systems
*(Pronunciation: "Tee")* · Please use **Mr.**

## Bio — 1 sentence (for MC)
<div id="bio-1sentence" class="bio-text" markdown="0">Thi Nguyen Dinh is a Senior Solutions Architect and AWS Vietnam's GenAI Champion, with 20 years in software and a focus on taking agentic AI from prototype to production.</div>
<button type="button" class="copy-bio" data-target="bio-1sentence">Copy</button>

## Bio — 50 words (for agenda)
<div id="bio-50words" class="bio-text" markdown="0">Thi Nguyen Dinh is a Senior Solutions Architect and AWS Vietnam's GenAI Champion for the past two years. With 20 years in software — from startup co-founder to principal engineer — he helps companies build agentic AI in production. He has delivered 100+ talks and authored an open-source GenAI repo with 380+ stars.</div>
<button type="button" class="copy-bio" data-target="bio-50words">Copy</button>

## Bio — 150 words (for website)
<div id="bio-150words" class="bio-text" markdown="0">
<p>Thi Nguyen Dinh is a Senior Solutions Architect focused on generative AI and agentic systems, and has been recognized as AWS Vietnam's GenAI Champion for the past two years. Over 20 years in software, he has worked as a developer, co-founded a startup at 24, led engineering teams, and served as a technical architect for fintech and payments platforms.</p>

<p>Today he helps startups and enterprises take agentic AI from prototype to production — covering architecture, evaluation, security and isolation, and cost and latency optimization — and modernize business-critical workloads such as core banking and SAP. His work is featured in public AWS case studies with Katalon and TymeX.</p>

<p>Thi has delivered 100+ talks and workshops, judged and mentored hackathons including Agentic AI Build Week (3,300+ builders, 60+ countries), and maintains AWS-First-GenAI-Journey, an open-source collection of 24 GenAI reference apps with 380+ stars.</p>
</div>
<button type="button" class="copy-bio" data-target="bio-150words">Copy</button>

## Photos (high resolution)
Click any photo to open the full-resolution version.

<div class="photo-grid">
  <a href="/images/profile.jpg"><img src="/images/profile.jpg" alt="Thi Nguyen Dinh — profile"></a>
  <a href="/images/bio-photo-1.jpg"><img src="/images/bio-photo-1.jpg" alt="Thi Nguyen Dinh — bio photo 1"></a>
  <a href="/images/bio-photo-2.jpg"><img src="/images/bio-photo-2.jpg" alt="Thi Nguyen Dinh — bio photo 2"></a>
</div>

Downloads: [profile.jpg](/images/profile.jpg) · [bio-photo-1.jpg](/images/bio-photo-1.jpg) · [bio-photo-2.jpg](/images/bio-photo-2.jpg) · [Event photos](/talks/)

## Talk topics
- Agentic AI in production: from prototype to multi-tenant platform
- Securing and isolating AI agents (per-session isolation, compliance)
- Governing AI coding tools at enterprise scale
- Context engineering and evaluation for LLM applications
- Modernizing core banking and SAP on the cloud

## Formats
Keynote · technical deep-dive · hands-on workshop · panel · hackathon judge/mentor
Languages: English, Vietnamese

## Contact
[LinkedIn](https://www.linkedin.com/in/ndthi/) · [ndthi@amazon.com](mailto:ndthi@amazon.com)

<script>
(function () {
  function fallbackCopy(text, done) {
    var ta = document.createElement('textarea');
    ta.value = text;
    ta.style.position = 'fixed';
    ta.style.left = '-9999px';
    document.body.appendChild(ta);
    ta.focus();
    ta.select();
    try { document.execCommand('copy'); done(true); } catch (e) { done(false); }
    document.body.removeChild(ta);
  }

  function flash(btn, ok) {
    var original = btn.getAttribute('data-label') || btn.textContent;
    btn.setAttribute('data-label', original);
    btn.textContent = ok ? 'Copied!' : 'Press Ctrl+C';
    setTimeout(function () { btn.textContent = original; }, 1500);
  }

  document.addEventListener('DOMContentLoaded', function () {
    document.querySelectorAll('.copy-bio').forEach(function (btn) {
      btn.addEventListener('click', function () {
        var target = document.getElementById(btn.getAttribute('data-target'));
        if (!target) { return; }
        var text = target.innerText.replace(/\n{3,}/g, '\n\n').trim();
        if (navigator.clipboard && navigator.clipboard.writeText) {
          navigator.clipboard.writeText(text).then(
            function () { flash(btn, true); },
            function () { fallbackCopy(text, function (ok) { flash(btn, ok); }); }
          );
        } else {
          fallbackCopy(text, function (ok) { flash(btn, ok); });
        }
      });
    });
  });
})();
</script>
