---
permalink: /team/
title: ""
author_profile: true
redirect_from:
  - /md/
  - /markdown.html
---

<style>

/* ── General ─────────────────────────────────────── */
.nids-section { margin: 40px 0; }
.nids-section-title {
  font-size: 1.35em;
  font-weight: 700;
  color: #1a1a1a;
  border-left: 5px solid #2a7ae2;
  padding-left: 12px;
  margin-bottom: 22px;
}

/* ── Vision banner ───────────────────────────────── */
.vision-box {
  background: #093f39;
  color: #fff;
  border-radius: 0;
  padding: 36px 40px 32px;
  margin-bottom: 36px;
  clip-path: polygon(0 0, 100% 0, 100% 88%, 97% 100%, 0 100%);
}
.vision-box h2 {
  color: #fff;
  margin: 0 0 6px 0;
  font-size: 1.6em;
  font-weight: 900;
  letter-spacing: -0.02em;
  line-height: 1;
  border: none;
}
.vision-box .vision-subtitle {
  display: inline-block;
  font-size: 0.75em;
  color: #093f39;
  background: rgba(255,255,255,0.88);
  border-radius: 3px;
  padding: 2px 10px;
  font-weight: 600;
  letter-spacing: 0.01em;
  margin-bottom: 18px;
}
.vision-box p {
  font-size: 0.91em;
  line-height: 1.8;
  color: #d4f0ec;
  margin: 0;
}

/* ── Member cards ────────────────────────────────── */
.member-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(140px, 1fr));
  gap: 16px;
  margin-bottom: 16px;
}
.member-card {
  background: #fff;
  border: 1px solid #e0e0e0;
  border-radius: 10px;
  padding: 22px 16px 16px;
  text-align: center;
  transition: box-shadow 0.2s, transform 0.2s;
}
.member-card:hover {
  box-shadow: 0 4px 18px rgba(0,0,0,0.10);
  transform: translateY(-3px);
}
.member-avatar {
  width: 80px; height: 80px;
  border-radius: 50%;
  display: flex; align-items: center; justify-content: center;
  font-size: 1.6em; font-weight: 700; color: #fff;
  margin: 0 auto 12px;
  letter-spacing: 0.5px;
}
.member-name { font-weight: 700; font-size: 0.92em; color: #1a1a1a; margin-bottom: 4px; }
.member-role { font-size: 0.78em; color: #555; margin-bottom: 3px; }
.member-year { font-size: 0.74em; color: #999; }

/* ── Alumni list ─────────────────────────────────── */
.alumni-list { list-style: none; padding: 0; margin: 0; }
.alumni-list li {
  padding: 8px 0;
  border-bottom: 1px solid #f0f0f0;
  font-size: 0.92em;
  color: #444;
}
.alumni-list li:last-child { border-bottom: none; }
.alumni-arrow { color: #2a7ae2; font-weight: 600; }

/* ── Research area cards ─────────────────────────── */
.research-grid {
  display: grid;
  grid-template-columns: 1fr;
  gap: 22px;
}
.research-card {
  background: #fff;
  border: 1px solid #e0e0e0;
  border-radius: 10px;
  overflow: hidden;
  display: flex;
  flex-direction: column;
  transition: box-shadow 0.2s, transform 0.2s;
}
@media (min-width: 600px) {
  .research-card { flex-direction: row; }
}
.research-card:hover {
  box-shadow: 0 6px 22px rgba(0,0,0,0.11);
  transform: translateY(-3px);
}
.research-figure {
  width: 100%;
  min-width: unset;
  display: flex;
  align-items: center;
  justify-content: center;
  background: #fff;
  overflow: hidden;
}
@media (min-width: 600px) {
  .research-figure {
    width: 280px;
    min-width: 280px;
  }
}
.research-figure img {
  width: 100%;
  height: auto;
  object-fit: contain;
  object-position: center;
  display: block;
}
@media (min-width: 600px) {
  .research-figure img {
    width: 280px;
    height: 100%;
  }
}
.research-figure svg { width: 100%; height: 100%; }
.research-body { padding: 16px; flex: 1; }
.research-title {
  font-size: 1em; font-weight: 700;
  color: #1a1a1a; margin-bottom: 8px;
}
.research-desc {
  font-size: 0.84em; color: #555;
  line-height: 1.55; margin-bottom: 12px;
}
.research-pubs { display: flex; flex-wrap: wrap; gap: 6px; }
.pub-tag {
  display: inline-block;
  padding: 2px 9px;
  border-radius: 10px;
  font-size: 0.72em;
  font-weight: 700;
  color: #fff;
  text-decoration: none;
}
.pub-tag:hover { opacity: 0.85; text-decoration: none; color: #fff; }
.rc-inc   .pub-tag { background: #1565c0; }
.rc-sketch .pub-tag { background: #00695c; }
.rc-malware .pub-tag { background: #c0392b; }
.rc-ai    .pub-tag { background: #e65100; }

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
    padding-left: 9px;
  }
}

/* ── Student pub highlight ───────────────────────── */
.spotlight-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
  gap: 16px;
}
.spotlight-card {
  background: #fff;
  border-left: 4px solid #2a7ae2;
  border-radius: 0 8px 8px 0;
  border-top: 1px solid #e0e0e0;
  border-right: 1px solid #e0e0e0;
  border-bottom: 1px solid #e0e0e0;
  padding: 14px 16px;
  transition: box-shadow 0.2s;
}
.spotlight-card:hover { box-shadow: 0 3px 14px rgba(0,0,0,0.09); }
.spotlight-venue {
  font-size: 0.73em; font-weight: 700;
  text-transform: uppercase; letter-spacing: 0.05em;
  color: #2a7ae2; margin-bottom: 5px;
}
.spotlight-title {
  font-size: 0.88em; font-weight: 700;
  color: #1a1a1a; margin-bottom: 5px;
  line-height: 1.4;
}
.spotlight-title a { color: inherit; text-decoration: none; }
.spotlight-title a:hover { color: #2a7ae2; }
.spotlight-authors { font-size: 0.78em; color: #777; }
</style>

<!-- ── Vision ─────────────────────────────── -->
<div class="vision-box">
  <h2>NIDS Lab</h2>
  <div class="vision-subtitle">Networked Intelligence and Distributed Security &nbsp;·&nbsp; Wayne State University</div>
  <p>Our vision is to advance the design and security of networked and distributed systems through cutting-edge research in artificial intelligence and cybersecurity. We develop innovative technologies that ensure robust, scalable, and secure knowledge convergence across various platforms - fostering safer cyber environments that promote scientific and technological progress.</p>
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

<!-- ── Research Areas ─────────────────────── -->
<div class="nids-section">
<div class="nids-section-title">Research Areas</div>
<div class="research-grid">

  <!-- Probabilistic Sketch Algorithms -->
  <div class="research-card rc-sketch">
    <div class="research-figure">
      <img src="/files/Research 1.png" alt="Probabilistic Sketch Algorithms" style="">
    </div>
    <div class="research-body">
      <div class="research-title">Probabilistic (Sketch) Algorithms</div>
      <div class="research-desc">
        We design lightweight probabilistic data structures including counting sketches and HyperLogLog for high-speed network measurement. Our work covers diffusion model-based inference for slow-and-low threat detection, noise minimization in spread estimation, and per-flow systematic sampling via sketch saturation events.
      </div>
      <div class="research-pubs">
        <a class="pub-tag tag-usenix" href="https://www.usenix.org/conference/nsdi26/presentation/mirnajafizadeh" target="_blank">NSDI 2026</a>
        <a class="pub-tag tag-dsn" href="https://ieeexplore.ieee.org/document/9833762/" target="_blank">DSN 2022</a>
        <a class="pub-tag tag-infocom" href="https://ieeexplore.ieee.org/document/9155252/" target="_blank">INFOCOM 2020</a>
      </div>
    </div>
  </div>

  <!-- Emerging Infrastructure -->
  <div class="research-card rc-inc">
    <div class="research-figure">
      <img src="/files/Research 2.png" alt="Emerging Infrastructure" style="">
    </div>
    <div class="research-body">
      <div class="research-title">Emerging Infrastructure</div>
      <div class="research-desc">
        We offload security functions directly onto programmable network hardware using P4. Our systems include a high-quality per-flow feature extractor for security-aware data planes, a distributed in-network data collection system for enhanced attack detection, a robust counting sketch for data-plane intrusion detection, and a scalable dynamic ACL enforcement mechanism.
      </div>
      <div class="research-pubs">
        <a class="pub-tag tag-ndss" href="https://www.ndss-symposium.org/ndss-paper/sketchfeature-high-quality-per-flow-feature-extractor-towards-security-aware-data-plane/" target="_blank">NDSS 2025</a>
        <a class="pub-tag tag-usenix" href="https://www.usenix.org/conference/usenixsecurity24/presentation/mirnajafizadeh" target="_blank">Security 2024</a>
        <a class="pub-tag tag-ndss" href="https://www.ndss-symposium.org/ndss-paper/a-robust-counting-sketch-for-data-plane-intrusion-detection/" target="_blank">NDSS 2023</a>
        <a class="pub-tag tag-ccs" href="https://dl.acm.org/doi/10.1145/3548606.3560606" target="_blank">CCS 2022</a>
      </div>
    </div>
  </div>

  <!-- Malware Analysis -->
  <div class="research-card rc-malware">
    <div class="research-figure">
      <img src="/files/Research 3.png" alt="Malware Analysis" style="">
    </div>
    <div class="research-body">
      <div class="research-title">Malware Analysis</div>
      <div class="research-desc">
        We study the robustness and limitations of ML-based malware detectors. Our work covers adversarial example detection in CFG-based classifiers, fine-grained hierarchical malware classification with deep learning, systematic robustness evaluation of IoT malware detectors, and exposing failures under concept drift.
      </div>
      <div class="research-pubs">
        <a class="pub-tag tag-wise"  href="https://link.springer.com/chapter/10.1007/978-981-96-0567-5_20" target="_blank">WISE 2024</a>
        <a class="pub-tag tag-raid"  href="https://dl.acm.org/doi/10.1145/3545948.3545960" target="_blank">RAID 2022</a>
        <a class="pub-tag tag-ieee"  href="https://ieeexplore.ieee.org/document/9484718/" target="_blank">TDSC 2022</a>
        <a class="pub-tag tag-ieee"  href="https://ieeexplore.ieee.org/document/9355825/" target="_blank">ICDCS 2020</a>
      </div>
    </div>
  </div>

  <!-- AI & ML Applications -->
  <div class="research-card rc-ai">
    <div class="research-figure">
      <img src="/files/Research 4.png" alt="AI & ML Applications" style="">
    </div>
    <div class="research-body">
      <div class="research-title">AI &amp; ML Applications</div>
      <div class="research-desc">
        We develop and explain AI/ML models for security and privacy. Our contributions include AttCAT, an attention-based explanation method for Transformers, DFD, an adversarial learning defense against website fingerprinting, and Seq2Seq-based untargeted code authorship evasion.
      </div>
      <div class="research-pubs">
        <a class="pub-tag tag-neurips" href="https://proceedings.neurips.cc/paper_files/paper/2022/hash/20e45668fefa793bd9f2edf19be12c4b-Abstract-Conference.html" target="_blank">NeurIPS 2022</a>
        <a class="pub-tag tag-wise" href="https://scholar.google.com/scholar?q=Untargeted+Code+Authorship+Evasion+with+Seq2Seq+Transformation" target="_blank">CSoNet 2023</a>
        <a class="pub-tag tag-infocom" href="https://ieeexplore.ieee.org/document/9155465/" target="_blank">INFOCOM 2020</a>
      </div>
    </div>
  </div>

</div>
</div>

<!-- ── Student Spotlight Publications ────────── -->
<div class="nids-section">
<div class="nids-section-title">Selected Publications</div>
<div class="spotlight-grid">

  <div class="spotlight-card">
    <div class="spotlight-venue">USENIX NSDI 2026</div>
    <div class="spotlight-title"><a href="https://www.usenix.org/conference/nsdi26/presentation/mirnajafizadeh" target="_blank">Defeating Slow-and-Low Threats via Diffusion Model-Based Generative Inference</a></div>
    <div class="spotlight-authors">Seyed Mohammad Mehdi Mirnajafizadeh, Prashant Khanduri, DaeHun Nyang, Rhongho Jang</div>
  </div>

  <div class="spotlight-card">
    <div class="spotlight-venue">ISOC NDSS 2025</div>
    <div class="spotlight-title"><a href="https://www.ndss-symposium.org/ndss-paper/sketchfeature-high-quality-per-flow-feature-extractor-towards-security-aware-data-plane/" target="_blank">SketchFeature: High-Quality Per-Flow Feature Extractor Towards Security-Aware Data Plane</a></div>
    <div class="spotlight-authors">Sian Kim, Seyed Mohammad Mehdi Mirnajafizadeh, Bara Kim, Rhongho Jang, DaeHun Nyang</div>
  </div>

  <div class="spotlight-card">
    <div class="spotlight-venue">USENIX Security 2024</div>
    <div class="spotlight-title"><a href="https://www.usenix.org/conference/usenixsecurity24/presentation/mirnajafizadeh" target="_blank">Enhancing Network Attack Detection with Distributed and In-Network Data Collection System</a></div>
    <div class="spotlight-authors">Seyed Mohammad Mehdi Mirnajafizadeh, Ashwin Raam Sethuram, David Mohaisen, DaeHun Nyang, Rhongho Jang</div>
  </div>

  <div class="spotlight-card">
    <div class="spotlight-venue">ISOC NDSS 2023</div>
    <div class="spotlight-title"><a href="https://www.ndss-symposium.org/ndss-paper/a-robust-counting-sketch-for-data-plane-intrusion-detection/" target="_blank">A Robust Counting Sketch for Data Plane Intrusion Detection</a></div>
    <div class="spotlight-authors">Sian Kim, Changhun Jung, RhongHo Jang, David Mohaisen, DaeHun Nyang</div>
  </div>

  <div class="spotlight-card">
    <div class="spotlight-venue">ACM CCS 2022</div>
    <div class="spotlight-title"><a href="https://dl.acm.org/doi/10.1145/3548606.3560606" target="_blank">A Scalable and Dynamic ACL System for In-Network Defense</a></div>
    <div class="spotlight-authors">Changhun Jung, Sian Kim, Rhongho Jang, David Mohaisen, DaeHun Nyang</div>
  </div>

</div>
</div>

<!-- ── Current Members ────────────────────── -->
<div class="nids-section">
<div class="nids-section-title">Current Members</div>
<div class="member-grid">

  <div class="member-card">
    <div class="member-avatar" style="background: linear-gradient(135deg,#1565c0,#42a5f5);">SM</div>
    <div class="member-name">Seyed Mohammad Mehdi Mirnajafizadeh</div>
    <div class="member-role">Ph.D. Student</div>
    <div class="member-year">Joined 2022</div>
  </div>

  <div class="member-card">
    <div class="member-avatar" style="background: linear-gradient(135deg,#6a1b9a,#ab47bc);">FK</div>
    <div class="member-name">Fatima Kamal Khaja</div>
    <div class="member-role">Ph.D. Student</div>
    <div class="member-year">Joined 2024</div>
  </div>

</div>
</div>

<!-- ── Alumni ─────────────────────────────── -->
<div class="nids-section">
<div class="nids-section-title">Alumni</div>
<ul class="alumni-list">
  <li>Ashwin Raam Sethuram (2024) &nbsp;<span class="alumni-arrow">→</span>&nbsp; WSU, Industrial Engineering, Ph.D. Program</li>
</ul>
</div>

