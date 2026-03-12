---
layout: page
title: FM-MRS @ IROS 2026
permalink: /fm-mrs/
nav: false
nav_order: 6
description:
---

<style>
.post-title, .post-description { display: none; }
.ws-hero {
  background: linear-gradient(135deg, #1a1a2e 0%, #16213e 50%, #0f3460 100%);
  color: white;
  padding: 3rem 2rem;
  border-radius: 8px;
  margin-bottom: 2.5rem;
  text-align: center;
}
.ws-hero h1 {
  font-size: 2rem;
  font-weight: 700;
  margin-bottom: 0.5rem;
  color: white;
}
.ws-hero .subtitle {
  font-size: 1.1rem;
  color: #a8d8ea;
  margin-bottom: 1rem;
}
.ws-hero .badges span {
  display: inline-block;
  background: rgba(255,255,255,0.15);
  border: 1px solid rgba(255,255,255,0.3);
  color: white;
  padding: 0.3rem 0.9rem;
  border-radius: 20px;
  font-size: 0.9rem;
  margin: 0.25rem;
}
.ws-section {
  margin-bottom: 2.5rem;
}
.ws-section h2 {
  font-size: 1.4rem;
  font-weight: 600;
  color: #0f3460;
  border-bottom: 2px solid #0f3460;
  padding-bottom: 0.4rem;
  margin-bottom: 1.2rem;
}
.speaker-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(220px, 1fr));
  gap: 1.2rem;
}
.speaker-card {
  border: 1px solid #e0e0e0;
  border-radius: 8px;
  padding: 1.2rem;
  text-align: center;
  background: #fafafa;
  transition: box-shadow 0.2s;
}
.speaker-card:hover {
  box-shadow: 0 4px 12px rgba(0,0,0,0.1);
}
.speaker-card .speaker-name {
  font-weight: 600;
  font-size: 1rem;
  margin-bottom: 0.2rem;
}
.speaker-card .speaker-affil {
  font-size: 0.85rem;
  color: #666;
  margin-bottom: 0.5rem;
}
.speaker-card .speaker-title {
  font-size: 0.82rem;
  color: #444;
  font-style: italic;
}
.speaker-card .tbd-badge {
  display: inline-block;
  background: #f0f0f0;
  color: #999;
  padding: 0.15rem 0.6rem;
  border-radius: 10px;
  font-size: 0.8rem;
}
.person-photo {
  width: 90px;
  height: 90px;
  border-radius: 50%;
  object-fit: cover;
  object-position: top;
  margin: 0 auto 0.7rem auto;
  display: block;
  border: 2px solid #e0e0e0;
}
.tbd-photo {
  width: 90px;
  height: 90px;
  border-radius: 50%;
  background: #e8e8e8;
  margin: 0 auto 0.7rem auto;
  display: flex;
  align-items: center;
  justify-content: center;
  color: #aaa;
  font-size: 2rem;
}
.organizer-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(160px, 1fr));
  gap: 1rem;
}
.organizer-card {
  border: 1px solid #e0e0e0;
  border-radius: 8px;
  padding: 1rem;
  text-align: center;
  background: #fafafa;
}
.organizer-card .org-name {
  font-weight: 600;
  font-size: 0.95rem;
  margin-bottom: 0.2rem;
}
.organizer-card .org-affil {
  font-size: 0.82rem;
  color: #666;
}
.organizer-card .org-badge {
  display: inline-block;
  background: #0f3460;
  color: white;
  font-size: 0.72rem;
  padding: 0.1rem 0.5rem;
  border-radius: 8px;
  margin-top: 0.4rem;
}
.schedule-table {
  width: 100%;
  border-collapse: collapse;
  font-size: 0.92rem;
}
.schedule-table th {
  background: #0f3460;
  color: white;
  padding: 0.6rem 1rem;
  text-align: left;
}
.schedule-table td {
  padding: 0.6rem 1rem;
  border-bottom: 1px solid #eee;
  vertical-align: top;
}
.schedule-table tr:nth-child(even) td {
  background: #f9f9f9;
}
.schedule-table .time-col {
  white-space: nowrap;
  color: #0f3460;
  font-weight: 500;
  width: 110px;
}
.schedule-table .break-row td {
  background: #e8f0fe !important;
  color: #555;
  font-style: italic;
}
.cfp-box {
  background: #f0f5ff;
  border-left: 4px solid #0f3460;
  padding: 1.2rem 1.5rem;
  border-radius: 0 8px 8px 0;
}
</style>

<!-- Hero -->
<div class="ws-hero">
  <h1>Foundation Models in Multi-Robot Systems</h1>
  <div class="subtitle">IROS 2026 Workshop &nbsp;|&nbsp; Pittsburgh, PA, USA &nbsp;|&nbsp; Sep 27 – Oct 1, 2026</div>
  <div class="badges">
    <span>Half-day Workshop</span>
    <span>Morning Session</span>
    <span>Invited Talks &amp; Posters</span>
  </div>
</div>

<!-- Overview -->
<div class="ws-section">
  <h2>Overview</h2>
  <p>
    Foundation models, including large language models (LLMs) and vision-language models (VLMs), are rapidly transforming robotics by enabling semantic reasoning, language-guided planning, and richer perception capabilities. This workshop focuses on <strong>foundation models in multi-robot systems</strong>, exploring how large-scale pretrained models can support coordination, decision making, and mission specification across robot teams operating in complex environments.
  </p>
  <p>
    The workshop highlights emerging directions such as LLM- and VLM-driven multi-robot coordination, heterogeneous robot collaboration, language-specified missions, decentralized reasoning architectures, and reliability mechanisms including constraint checking and conformal prediction. Compared with recent workshops that primarily focus on LLM-enabled robotics, this workshop emphasizes <strong>team-level autonomy and system-level scalability</strong>, examining how foundation models can facilitate coordination, communication, and planning across multiple robots.
  </p>
  <p>
    The workshop will bring together researchers from multi-robot systems, robot learning, planning, and large-scale AI models, as well as industry practitioners developing and deploying robotic fleets. Through invited talks, lightning presentations, and interactive discussions, the workshop aims to identify key challenges, share emerging methodologies, and outline future research directions at the intersection of foundation models and multi-robot autonomy.
  </p>
</div>

<!-- Invited Speakers -->
<div class="ws-section">
  <h2>Invited Speakers</h2>
  <div class="speaker-grid">

    <div class="speaker-card">
      <img class="person-photo" src="/assets/img/IROS2026workshop/speakers/Nicholas Roy.jpeg" alt="Nicholas Roy">
      <div class="speaker-name"><a href="https://aeroastro.mit.edu/people/nicholas-roy/" target="_blank">Nicholas Roy</a></div>
      <div class="speaker-affil">MIT</div>
      <div class="speaker-title">Foundation Models and Symbol Grounding for Multirobot Systems</div>
    </div>

    <div class="speaker-card">
      <img class="person-photo" src="/assets/img/IROS2026workshop/speakers/Chuchu Fan.jpeg" alt="Chuchu Fan">
      <div class="speaker-name"><a href="https://chuchu.mit.edu/" target="_blank">Chuchu Fan</a></div>
      <div class="speaker-affil">MIT</div>
      <div class="speaker-title">LLMs and VLMs Can Solve Real-World Planning Rigorously with Formal Reasoning Tools</div>
    </div>

    <div class="speaker-card">
      <img class="person-photo" src="/assets/img/IROS2026workshop/speakers/M. Ani Hsieh.jpeg" alt="M. Ani Hsieh">
      <div class="speaker-name"><a href="https://www.seas.upenn.edu/~m.hsieh/" target="_blank">M. Ani Hsieh</a></div>
      <div class="speaker-affil">University of Pennsylvania</div>
      <div class="speaker-title">TBD</div>
    </div>

    <div class="speaker-card">
      <img class="person-photo" src="/assets/img/IROS2026workshop/speakers/Javier Alonso-Mora.jpeg" alt="Javier Alonso-Mora">
      <div class="speaker-name"><a href="https://www.autonomousrobots.nl/" target="_blank">Javier Alonso-Mora</a></div>
      <div class="speaker-affil">TU Delft</div>
      <div class="speaker-title">TBD</div>
    </div>

    <div class="speaker-card">
      <img class="person-photo" src="/assets/img/IROS2026workshop/speakers/Jiachen Li.jpeg" alt="Jiachen Li">
      <div class="speaker-name"><a href="https://jiachenli94.github.io/" target="_blank">Jiachen Li</a></div>
      <div class="speaker-affil">UC Riverside</div>
      <div class="speaker-title">Toward Safe and Efficient Coordination for Cooperative Embodied Agents</div>
    </div>

    <div class="speaker-card">
      <img class="person-photo" src="/assets/img/IROS2026workshop/speakers/Ameya Agaskar.jpeg" alt="Ameya Agaskar">
      <div class="speaker-name">Ameya Agaskar</div>
      <div class="speaker-affil">Amazon Robotics</div>
      <div class="speaker-title">DEEPFLEET: Multi-Agent Foundation Models for Mobile Robots</div>
    </div>

  </div>
</div>

<!-- Schedule -->
<div class="ws-section">
  <h2>Program Schedule</h2>
  <table class="schedule-table">
    <thead>
      <tr>
        <th>Time</th>
        <th>Session</th>
        <th>Details</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td class="time-col">8:30 – 8:35</td>
        <td>Opening Remarks</td>
        <td>Workshop overview and introduction</td>
      </tr>
      <tr>
        <td class="time-col">8:35 – 9:00</td>
        <td>Invited Talk 1</td>
        <td><strong>Nicholas Roy</strong> (MIT) &mdash; Foundation Models and Symbol Grounding for Multirobot Systems</td>
      </tr>
      <tr>
        <td class="time-col">9:00 – 9:25</td>
        <td>Invited Talk 2</td>
        <td><strong>Chuchu Fan</strong> (MIT) &mdash; LLMs and VLMs Can Solve Real-World Planning Rigorously with Formal Reasoning Tools</td>
      </tr>
      <tr>
        <td class="time-col">9:25 – 9:50</td>
        <td>Invited Talk 3</td>
        <td><strong>M. Ani Hsieh</strong> (University of Pennsylvania)</td>
      </tr>
      <tr>
        <td class="time-col">9:50 – 10:15</td>
        <td>Invited Talk 4</td>
        <td><strong>Javier Alonso-Mora</strong> (TU Delft)</td>
      </tr>
      <tr>
        <td class="time-col">10:15 – 10:30</td>
        <td>Contributed Spotlight Talks</td>
        <td>Lightning presentations from accepted submissions</td>
      </tr>
      <tr class="break-row">
        <td class="time-col">10:30 – 11:00</td>
        <td>Coffee Break</td>
        <td>Poster presentations and networking</td>
      </tr>
      <tr>
        <td class="time-col">11:00 – 11:25</td>
        <td>Invited Talk 5</td>
        <td><strong>Jiachen Li</strong> (UC Riverside) &mdash; Toward Safe and Efficient Coordination for Cooperative Embodied Agents</td>
      </tr>
      <tr>
        <td class="time-col">11:25 – 11:50</td>
        <td>Invited Talk 6</td>
        <td><strong>Ameya Agaskar</strong> (Amazon Robotics) &mdash; DEEPFLEET: Multi-Agent Foundation Models for Mobile Robots</td>
      </tr>
      <tr>
        <td class="time-col">11:50 – 12:25</td>
        <td>Panel Discussion</td>
        <td>Open Q&amp;A and discussion on future directions</td>
      </tr>
      <tr>
        <td class="time-col">12:25 – 12:30</td>
        <td>Closing Remarks</td>
        <td></td>
      </tr>
    </tbody>
  </table>
</div>

<!-- Call for Papers -->
<div class="ws-section">
  <h2>Call for Papers</h2>
  <div class="cfp-box">
    <p>We invite submissions of extended abstracts (2–4 pages) on topics including but not limited to:</p>
    <ul>
      <li>LLM- and VLM-driven multi-robot coordination and planning</li>
      <li>Language-specified missions for heterogeneous robot teams</li>
      <li>Foundation-model-based decentralized reasoning and multi-robot communication</li>
      <li>Reliability and safety of foundation models in robot teams: constraint checking, formal verification, and conformal prediction</li>
      <li>Foundation models for multi-agent decision making and task allocation</li>
      <li>Real-world deployment of foundation-model-enabled robot fleets</li>
    </ul>
    <p style="margin-bottom:0"><strong>Submission details coming soon.</strong> Accepted papers will be presented as spotlight talks and/or posters.</p>
  </div>
</div>

<!-- Organizers -->
<div class="ws-section">
  <h2>Organizers</h2>
  <div class="organizer-grid">

    <div class="organizer-card">
      <img class="person-photo" src="/assets/img/IROS2026workshop/organizers/Lifeng Zhou.jpeg" alt="Lifeng Zhou">
      <div class="org-name"><a href="https://lfzhou917.github.io/" target="_blank">Lifeng Zhou</a></div>
      <div class="org-affil">Drexel University</div>
    </div>

    <div class="organizer-card">
      <img class="person-photo" src="/assets/img/IROS2026workshop/organizers/Jiachen Li.jpeg" alt="Jiachen Li">
      <div class="org-name"><a href="https://jiachenli94.github.io/" target="_blank">Jiachen Li</a></div>
      <div class="org-affil">UC Riverside</div>
    </div>

    <div class="organizer-card">
      <img class="person-photo" src="/assets/img/IROS2026workshop/organizers/Varun Murali.jpeg" alt="Varun Murali">
      <div class="org-name"><a href="https://varunmurali1.github.io/" target="_blank">Varun Murali</a></div>
      <div class="org-affil">Texas A&amp;M University</div>
    </div>

    <div class="organizer-card">
      <img class="person-photo" src="/assets/img/IROS2026workshop/organizers/Yiannis Kantaros.jpeg" alt="Yiannis Kantaros">
      <div class="org-name"><a href="https://engineering.washu.edu/faculty/Yiannis-Kantaros.html" target="_blank">Yiannis Kantaros</a></div>
      <div class="org-affil">Washington University in St. Louis</div>
    </div>

    <div class="organizer-card">
      <img class="person-photo" src="/assets/img/IROS2026workshop/organizers/Alberto Quattrini Li.jpeg" alt="Alberto Quattrini Li">
      <div class="org-name"><a href="https://rlab.cs.dartmouth.edu/albertoq/" target="_blank">Alberto Quattrini Li</a></div>
      <div class="org-affil">Dartmouth College</div>
    </div>

    <div class="organizer-card">
      <img class="person-photo" src="/assets/img/IROS2026workshop/organizers/Lorenzo Sabattini.jpeg" alt="Lorenzo Sabattini">
      <div class="org-name"><a href="https://sites.google.com/view/lorenzosabattini" target="_blank">Lorenzo Sabattini</a></div>
      <div class="org-affil">University of Modena and Reggio Emilia</div>
    </div>

    <div class="organizer-card">
      <img class="person-photo" src="/assets/img/IROS2026workshop/organizers/Byung-Cheol Min.jpeg" alt="Byung-Cheol Min">
      <div class="org-name"><a href="https://minb.pages.iu.edu/" target="_blank">Byung-Cheol Min</a></div>
      <div class="org-affil">Indiana University Bloomington</div>
    </div>

    <div class="organizer-card">
      <img class="person-photo" src="/assets/img/IROS2026workshop/organizers/Vijay Kumar.jpeg" alt="Vijay Kumar">
      <div class="org-name"><a href="https://www.kumarrobotics.org/dr-vijay-kumar/" target="_blank">Vijay Kumar</a></div>
      <div class="org-affil">University of Pennsylvania</div>
    </div>

  </div>
</div>

<!-- Contact -->
<div class="ws-section">
  <h2>Contact</h2>
  <p>For inquiries, please contact <a href="https://lfzhou917.github.io/">Lifeng Zhou</a> at Drexel University.</p>
</div>
