---
layout: single
permalink: /
title: ""
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

<style>

/* ── Hero banner ─────────────────────────────────── */
.hero-banner {
  background: #093f39;
  border-radius: 0;
  padding: 22px 32px 20px;
  color: #fff;
  margin-bottom: 24px;
  position: relative;
  clip-path: polygon(0 0, 100% 0, 100% 88%, 97% 100%, 0 100%);
}
.hero-name {
  font-size: 2em;
  font-weight: 900;
  letter-spacing: -0.02em;
  margin-bottom: 10px;
  line-height: 1;
}
.hero-title {
  display: inline-block;
  font-size: 0.75em;
  color: #093f39;
  background: rgba(255,255,255,0.88);
  border-radius: 3px;
  padding: 2px 10px;
  margin-bottom: 5px;
  font-weight: 600;
  letter-spacing: 0.01em;
}
.hero-title-wrap {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  gap: 4px;
  margin-bottom: 16px;
}
.hero-bio {
  font-size: 0.86em;
  line-height: 1.6;
  color: rgba(255,255,255,0.88);
  max-width: 680px;
  margin-bottom: 14px;
}
.hero-interests-label {
  font-size: 0.7em;
  font-weight: 700;
  letter-spacing: 0.12em;
  text-transform: uppercase;
  color: rgba(255,255,255,0.55);
  margin-bottom: 6px;
}
.hero-tags {
  display: flex; flex-wrap: wrap; gap: 6px;
}
.hero-tag {
  background: rgba(255,255,255,0.12);
  border: 1px solid rgba(255,255,255,0.35);
  border-radius: 2px;
  padding: 3px 10px;
  font-size: 0.74em;
  font-weight: 600;
  color: #fff;
  letter-spacing: 0.02em;
}

/* ── Stats row ───────────────────────────────────── */
.stats-row {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
  gap: 14px;
  margin-bottom: 32px;
}
.stat-card {
  background: #fff;
  border: 1px solid #e0e0e0;
  border-radius: 10px;
  padding: 18px 14px;
  text-align: center;
  transition: box-shadow 0.2s, transform 0.2s;
}
.stat-card:hover {
  box-shadow: 0 4px 16px rgba(0,0,0,0.09);
  transform: translateY(-2px);
}
.stat-number {
  font-size: 1.9em;
  font-weight: 800;
  color: #093f39;
  line-height: 1;
  margin-bottom: 5px;
}
.stat-label {
  font-size: 0.76em;
  color: #666;
  line-height: 1.3;
}

/* ── Section title ───────────────────────────────── */
.about-section { margin-bottom: 32px; }
.about-section-title {
  font-size: 1.15em;
  font-weight: 700;
  color: #1a1a1a;
  border-left: 5px solid #093f39;
  padding-left: 12px;
  margin-bottom: 16px;
}

/* ── News feed ───────────────────────────────────── */
.news-feed { list-style: none; padding: 0; margin: 0; }
.news-item {
  display: flex;
  gap: 10px;
  padding: 5px 10px;
  margin-bottom: 3px;
  background: #fff;
  border: 1px solid #e8e8e8;
  border-left: 3px solid #093f39;
  border-radius: 4px;
  font-size: 0.70em;
  line-height: 1.3;
  align-items: center;
}
.news-date {
  white-space: nowrap;
  font-weight: 700;
  color: #093f39;
  font-size: 0.72em;
  min-width: 62px;
  background: #f0f7f5;
  border-radius: 3px;
  padding: 2px 6px;
  text-align: center;
}
.news-text { color: #333; flex: 1; }
.news-badge {
  display: inline-block;
  background: #fff3cd;
  border: 1px solid #ffc107;
  color: #856404;
  border-radius: 4px;
  font-size: 0.75em;
  font-weight: 700;
  padding: 2px 7px;
  margin-right: 4px;
  white-space: nowrap;
  vertical-align: middle;
}
.news-badge.award { background: #fff0f0; border-color: #e53935; color: #b71c1c; }
.news-badge.grant { background: #e8f5e9; border-color: #43a047; color: #1b5e20; }
.news-venue {
  font-weight: 700;
  color: #1565c0;
}

/* ── Sponsor bar ─────────────────────────────────── */
.sponsor-bar {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  gap: 20px;
  margin-bottom: 28px;
  padding: 14px 20px;
  background: #fff;
  border: 1px solid #e8e8e8;
  border-radius: 6px;
  box-shadow: 0 1px 4px rgba(0,0,0,0.05);
}
.sponsor-bar .sponsor-label {
  font-size: 0.68em;
  color: #aaa;
  font-weight: 700;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  white-space: nowrap;
}
.sponsor-bar a {
  opacity: 0.85;
  transition: opacity 0.2s;
  text-decoration: none;
}
.sponsor-bar a:hover { opacity: 1; }
.sponsor-bar img {
  height: 60px;
  object-fit: contain;
  display: block;
}
.sponsor-item {
  display: flex;
  align-items: center;
  gap: 10px;
}
.sponsor-name {
  display: none;
  font-size: 1.05em;
  color: #111;
  font-weight: 700;
  line-height: 1.2;
  white-space: nowrap;
}
@media (max-width: 599px) {
  .sponsor-bar {
    flex-direction: column;
    align-items: flex-start;
    text-align: left;
    gap: 14px;
    padding: 16px;
  }
  .sponsor-bar img {
    height: 50px;
    max-width: 100%;
  }
  .sponsor-item {
    flex-direction: row;
    align-items: center;
    gap: 12px;
  }
  .sponsor-name {
    display: block;
    text-align: left;
  }
  .sponsor-item:last-child {
    padding-left: 36px;
  }
}
</style>

<!-- Hero -->
<div class="hero-banner">
  <div class="hero-name">Rhongho Jang</div>
  <div class="hero-title-wrap">
    <span class="hero-title">Assistant Professor · Department of Computer Science · Wayne State University</span>
    <span class="hero-title">Adjunct Assistant Professor · AI and Data Science (AIDaS) Institute</span>
  </div>
  <div class="hero-bio">
    I received dual Ph.D. degrees in Computer Science (2020), advised by <a href="https://www.cs.ucf.edu/~mohaisen/" target="_blank" style="color:#a8e6df;font-weight:600;">Dr. David Mohaisen</a> (University of Central Florida) and <a href="https://pure.ewha.ac.kr/en/persons/daehun-nyang" target="_blank" style="color:#a8e6df;font-weight:600;">Dr. DaeHun Nyang</a> (Ewha Womans University), and completed a research internship at the USC Information Sciences Institute (ISI) in 2019.
    I'm directing the <a href="/team/" style="color:#a8e6df;font-weight:600;">NIDS Lab</a> (Networked Intelligence and Distributed Security), where we build next-generation systems that narrow the deployment gap between programmable hardware and AI.
  </div>
  <div class="hero-interests-label">Research Interests</div>
  <div class="hero-tags">
    <span class="hero-tag">Emerging Infrastructure</span>
    <span class="hero-tag">Network Intelligence</span>
    <span class="hero-tag">System Resiliency</span>
<span class="hero-tag">Applied AI</span>
  </div>
</div>


<!-- Sponsors -->
<div class="sponsor-bar">
  <span class="sponsor-label">Supported by</span>
  <a href="https://www.nsf.gov" target="_blank" class="sponsor-item">
    <img src="/files/NSF_Official_logo_High_Res_1200ppi.png" alt="NSF" style="width:60px;">
    <span class="sponsor-name">National Science Foundation</span>
  </a>
  <a href="https://engineering.wayne.edu/computer-science" target="_blank" class="sponsor-item">
    <img src="/files/computer_science_anderson_horz_561.jpg" alt="WSU CS">
  </a>
</div>

<!-- News -->
<div class="about-section">
<div class="about-section-title">Recent News</div>
<ul class="news-feed">

  <li class="news-item">
    <span class="news-date">Mar 2026</span>
    <span class="news-text">Mehdi will join <strong><span style="color:#4285F4">G</span><span style="color:#EA4335">o</span><span style="color:#FBBC05">o</span><span style="color:#4285F4">g</span><span style="color:#34A853">l</span><span style="color:#EA4335">e</span></strong> for a summer internship!</span>
  </li>

  <li class="news-item">
    <span class="news-date">Dec 2025</span>
    <span class="news-text">Low-and-slow threat detection paper accepted in <span class="news-venue">USENIX NSDI 2026</span>. Congrats to Mehdi!</span>
  </li>

  <li class="news-item">
    <span class="news-date">Oct 2025</span>
    <span class="news-text">Mehdi is selected as a <strong>Distinguished AE Reviewer</strong> for USENIX Security, congrats!</span>
  </li>

  <li class="news-item">
    <span class="news-date">Sep 2025</span>
    <span class="news-text">Malware concept drift paper to appear in <span class="news-venue">Computing</span>.</span>
  </li>

  <li class="news-item">
    <span class="news-date">Apr 2025</span>
    <span class="news-text">🏅 Mehdi received <strong>Michael Conrad Award ($1,000)</strong> for <span class="news-venue">USENIX Security 2024</span> paper, congrats!</span>
  </li>

  <li class="news-item">
    <span class="news-date">Feb 2025</span>
    <span class="news-text">"SketchFeature" in-network defense paper to be presented at <span class="news-venue">ISOC NDSS 2025</span>.</span>
  </li>

  <li class="news-item">
    <span class="news-date">Dec 2024</span>
    <span class="news-text">🏆 <strong>Best Paper Award</strong> at WISE 2024 for malware concept drift research.</span>
  </li>

  <li class="news-item">
    <span class="news-date">Aug 2024</span>
    <span class="news-text">Mehdi's first paper as lead author to be presented at <span class="news-venue">USENIX Security 2024</span>.</span>
  </li>

  <li class="news-item">
    <span class="news-date">Aug 2023</span>
    <span class="news-text"><span class="news-badge grant">Grant</span> Received <strong>NSF travel grant</strong> (PI) for IEEE CNS 2022.</span>
  </li>

  <li class="news-item">
    <span class="news-date">Apr 2023</span>
    <span class="news-text">Hospital website security paper accepted in <span class="news-venue">IEEE ICCCN 2023</span>.</span>
  </li>

  <li class="news-item">
    <span class="news-date">Feb 2023</span>
    <span class="news-text">In-network traffic measurement paper to be presented at <span class="news-venue">ISOC NDSS 2023</span>.</span>
  </li>

  <li class="news-item">
    <span class="news-date">Sep 2022</span>
    <span class="news-text">Transformer explainability paper accepted in <span class="news-venue">NeurIPS 2022</span>.</span>
  </li>

  <li class="news-item">
    <span class="news-date">Aug 2022</span>
    <span class="news-text"><span class="news-badge grant">Grant</span> Received <strong>NSF HCC grant</strong> (Co-PI) for AI for social goods.</span>
  </li>

  <li class="news-item">
    <span class="news-date">Jul 2022</span>
    <span class="news-text">In-network ACL defense paper to appear at <span class="news-venue">ACM CCS 2022</span>.</span>
  </li>

  <li class="news-item news-old">
    <span class="news-date">Jun 2022</span>
    <span class="news-text">Malware detection system analysis paper accepted in <span class="news-venue">RAID 2022</span>.</span>
  </li>

  <li class="news-item news-old">
    <span class="news-date">Mar 2022</span>
    <span class="news-text">Flow spread estimation algorithm paper accepted in <span class="news-venue">IEEE DSN 2022</span>.</span>
  </li>

  <li class="news-item news-old">
    <span class="news-date">Aug 2021</span>
    <span class="news-text">DNS resolver behavioral analysis paper accepted in <span class="news-venue">IEEE/ACM ToN</span>.</span>
  </li>

  <li class="news-item news-old">
    <span class="news-date">Jan 2021</span>
    <span class="news-text">🏆 <strong>Best Fast Abstract Award</strong> for IoT malware defense at <span class="news-venue">IEEE DSN 2021</span>.</span>
  </li>

  <li class="news-item news-old">
    <span class="news-date">Jul 2020</span>
    <span class="news-text">Two papers (Security/Privacy) accepted in <span class="news-venue">IEEE INFOCOM 2020</span>.</span>
  </li>

  <li class="news-item news-old">
    <span class="news-date">Mar 2020</span>
    <span class="news-text">Malware adversarial learning paper accepted in <span class="news-venue">IEEE ICDCS 2020</span>.</span>
  </li>

</ul>
<div style="text-align:center;margin-top:6px;">
  <button id="news-toggle" onclick="toggleNews()" style="background:none;border:1px solid #093f39;color:#093f39;font-size:0.72em;font-weight:600;padding:3px 14px;border-radius:3px;cursor:pointer;">Show more</button>
</div>
</div>

<script>
function toggleNews() {
  var items = document.querySelectorAll('.news-old');
  var btn = document.getElementById('news-toggle');
  var hidden = items[0].style.display === 'none' || items[0].style.display === '';
  items.forEach(function(el) { el.style.display = hidden ? 'flex' : 'none'; });
  btn.textContent = hidden ? 'Show less' : 'Show more';
}
document.querySelectorAll('.news-old').forEach(function(el) { el.style.display = 'none'; });
</script>
