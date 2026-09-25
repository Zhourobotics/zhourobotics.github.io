---
layout: page
title: FM-MRS @ IROS 2026
permalink: /fm-mrs/
nav: true
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
  /* auto-fit: 5 speakers sit on one row on a wide screen and reflow on narrow
     ones. A fixed 4 columns would leave a lone card stranded on a second row. */
  grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
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
.paper-list {
  padding-left: 1.4rem;
  margin: 0;
}
.paper-list li {
  margin-bottom: 0.9rem;
}
.paper-list .paper-title {
  display: block;
  font-weight: 600;
  line-height: 1.35;
}
.paper-list .paper-authors {
  display: block;
  font-size: 0.86rem;
  color: #666;
  margin-top: 0.15rem;
}
.cfp-box {
  background: #f0f5ff;
  border-left: 4px solid #0f3460;
  padding: 1.2rem 1.5rem;
  border-radius: 0 8px 8px 0;
}

/* Dark-mode contrast fixes. This page uses hardcoded light backgrounds, but in
   dark mode the theme switches body text to a light color -> light-on-light.
   These overrides only apply in dark mode; light mode is unchanged. */
html[data-theme='dark'] .ws-section h2 {
  color: #a8d8ea;                /* navy heading is unreadable on the dark page bg */
}
/* The theme pins color directly on p/li/strong/div (_base.scss), so inheritance
   from the box is not enough — the inner elements must be targeted explicitly. */
html[data-theme='dark'] .cfp-box p,
html[data-theme='dark'] .cfp-box li,
html[data-theme='dark'] .cfp-box strong {
  color: #1a1a1a;                /* keep dark text on the light CFP box */
}
html[data-theme='dark'] .cfp-box a {
  color: #1565c0;               /* readable blue link on the light box (not cyan) */
}
html[data-theme='dark'] .speaker-card .speaker-name,
html[data-theme='dark'] .organizer-card .org-name {
  color: #1a1a1a;                /* unlinked names are divs -> theme paints them light grey on the light cards */
}
html[data-theme='dark'] .speaker-card .speaker-name a,
html[data-theme='dark'] .organizer-card .org-name a {
  color: #1565c0;               /* linked names: readable blue instead of cyan on the light cards */
}
html[data-theme='dark'] .paper-list .paper-authors {
  color: #9aa7b4;              /* #666 on the dark page bg is unreadable */
}
html[data-theme='dark'] .schedule-table td {
  background: #f9f9f9;
  color: #1a1a1a;                /* light bg + dark text for all rows */
}
html[data-theme='dark'] .schedule-table td strong {
  color: #1a1a1a;                /* speaker names are <strong>, pinned light by the theme */
}
html[data-theme='dark'] .schedule-table tr:nth-child(even) td {
  background: #efefef;
}
</style>

<!-- Hero -->
<div class="ws-hero">
  <h1>Foundation Models in Multi-Robot Systems</h1>
  <div class="subtitle">IROS 2026 Workshop &nbsp;|&nbsp; Rooms 301 &amp; 302, Pittsburgh, PA, USA &nbsp;|&nbsp; Sunday, Sep 27, 2026 &nbsp;|&nbsp; 8:30 AM – 12:30 PM</div>
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
      <img class="person-photo" src="/assets/img/IROS2026workshop/speakers/Chuchu Fan.jpeg" alt="Chuchu Fan">
      <div class="speaker-name"><a href="https://chuchu.mit.edu/" target="_blank">Chuchu Fan</a></div>
      <div class="speaker-affil">MIT</div>
      <div class="speaker-title">LLMs and VLMs Can Solve Real-World Planning Rigorously with Formal Reasoning Tools</div>
    </div>

    <div class="speaker-card">
      <img class="person-photo" src="/assets/img/IROS2026workshop/speakers/M. Ani Hsieh.jpeg" alt="M. Ani Hsieh">
      <div class="speaker-name"><a href="https://www.grasp.upenn.edu/people/ani-hsieh/" target="_blank">M. Ani Hsieh</a></div>
      <div class="speaker-affil">University of Pennsylvania</div>
      <div class="speaker-title">Physics Foundation Models for Multi-Robot Autonomy: From Team-Level Sensing to Guaranteed-Safe Motion</div>
    </div>

    <div class="speaker-card">
      <img class="person-photo" src="/assets/img/IROS2026workshop/speakers/Javier Alonso-Mora.jpeg" alt="Javier Alonso-Mora">
      <div class="speaker-name"><a href="https://www.autonomousrobots.nl/" target="_blank">Javier Alonso-Mora</a></div>
      <div class="speaker-affil">TU Delft</div>
      <div class="speaker-title">Foundation Models for Planner Adaptation and Open-World Perception</div>
    </div>

    <div class="speaker-card">
      <img class="person-photo" src="/assets/img/IROS2026workshop/speakers/Jiachen Li.jpeg" alt="Jiachen Li">
      <div class="speaker-name"><a href="https://jiachenli94.github.io/" target="_blank">Jiachen Li</a></div>
      <div class="speaker-affil">Georgia Tech</div>
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
        <td class="time-col">8:30 – 8:40</td>
        <td>Opening Remarks</td>
        <td>Workshop overview and introduction</td>
      </tr>
      <tr>
        <td class="time-col">8:40 – 9:05</td>
        <td>Invited Talk 1</td>
        <td><strong>Chuchu Fan</strong> (MIT) &mdash; LLMs and VLMs Can Solve Real-World Planning Rigorously with Formal Reasoning Tools</td>
      </tr>
      <tr>
        <td class="time-col">9:05 – 9:30</td>
        <td>Invited Talk 2</td>
        <td><strong>M. Ani Hsieh</strong> (University of Pennsylvania) &mdash; Physics Foundation Models for Multi-Robot Autonomy: From Team-Level Sensing to Guaranteed-Safe Motion</td>
      </tr>
      <tr>
        <td class="time-col">9:30 – 9:55</td>
        <td>Invited Talk 3</td>
        <td><strong>Javier Alonso-Mora</strong> (TU Delft) &mdash; Foundation Models for Planner Adaptation and Open-World Perception</td>
      </tr>
      <tr>
        <td class="time-col">9:55 – 10:15</td>
        <td>Contributed Spotlight Talks</td>
        <td>Lightning talks from the ten accepted papers</td>
      </tr>
      <tr class="break-row">
        <td class="time-col">10:15 – 11:15</td>
        <td>Coffee Break &amp; Poster Session</td>
        <td>Poster presentations and networking</td>
      </tr>
      <tr>
        <td class="time-col">11:15 – 11:35</td>
        <td>Invited Talk 4</td>
        <td><strong>Jiachen Li</strong> (Georgia Tech) &mdash; Toward Safe and Efficient Coordination for Cooperative Embodied Agents</td>
      </tr>
      <tr>
        <td class="time-col">11:35 – 11:55</td>
        <td>Invited Talk 5</td>
        <td><strong>Ameya Agaskar</strong> (Amazon Robotics) &mdash; DEEPFLEET: Multi-Agent Foundation Models for Mobile Robots</td>
      </tr>
      <tr>
        <td class="time-col">11:55 – 12:20</td>
        <td>Panel Discussion</td>
        <td>Open Q&amp;A and discussion on future directions</td>
      </tr>
      <tr>
        <td class="time-col">12:20 – 12:25</td>
        <td>Community Announcement</td>
        <td><strong>Giuseppe Loianno</strong> (UC Berkeley) and <strong>Francesco Blasi</strong> (ASPIRE) &mdash; A2RL Multi-Agent Drone Racing Challenge</td>
      </tr>
      <tr>
        <td class="time-col">12:25 – 12:30</td>
        <td>Closing Remarks</td>
        <td></td>
      </tr>
    </tbody>
  </table>
</div>

<!-- Accepted Papers -->
<div class="ws-section">
  <h2>Accepted Papers</h2>
  <p>Ten papers were accepted to the workshop. Each is presented as a 2-minute lightning talk during the Contributed Spotlight session, followed by a poster during the coffee break. Papers are available on <a href="https://openreview.net/group?id=IEEE.org/IROS/2026/Workshop/FM-MRS" target="_blank">OpenReview</a>.</p>
  <ol class="paper-list">
      <li>
        <span class="paper-title">Risk-Bounded Language-to-Task Allocation: A Conformal Prediction Framework for Heterogeneous Robot Teams</span>
        <span class="paper-authors">Shivum Telang</span>
      </li>
      <li>
        <span class="paper-title">Physical Agentic AI: An Architecture for Orchestrating a Robot Crew with LLMs</span>
        <span class="paper-authors">Xinyuan Liu, Eren Sadikoglu, Riana Chatterjee, Ransalu Senanayake</span>
      </li>
      <li>
        <span class="paper-title">Evaluating Social Reasoning in Embodied Vision-Language Models</span>
        <span class="paper-authors">Daniel Weiner, Raj Korpan</span>
      </li>
      <li>
        <span class="paper-title">LLM-Guided Adaptive Auction Coordination for Multi-Autonomous Trucks Under Non-Nominal Logistics Yard Conditions</span>
        <span class="paper-authors">Seongju Jang, Jiayi Qiu, Meng Xu, SangHyun Lee</span>
      </li>
      <li>
        <span class="paper-title">Multi-Robot Formation Coordination with Verified Agentic LLM Planning</span>
        <span class="paper-authors">Jinyuan Zhang, Yuwei Wu, Guangyao Shi, Jonathan Diller, Gaurav S. Sukhatme, Vijay Kumar</span>
      </li>
      <li>
        <span class="paper-title">PIP-LLM: Integrating PDDL-Integer Programming with LLMs for Coordinating Multi-Robot Teams Using Natural Language</span>
        <span class="paper-authors">Guangyao Shi</span>
      </li>
      <li>
        <span class="paper-title">NeuroMesh: A Unified Neural Inference Framework for Decentralized Multi-Robot Collaboration</span>
        <span class="paper-authors">Yang Zhou, Yash Shetye, Long Quang, Devon Super, Jesse Milzman, Manohari Goarin, Aditya Azad, Devang Sunil Dhake, Jeffrey Mao, Carlos Nieto-Granda, Giuseppe Loianno</span>
      </li>
      <li>
        <span class="paper-title">TriPlane-WAM: A Multi-Robot World Action Model with Shared Tri-Plane Workspace</span>
        <span class="paper-authors">Guoning Wu, Zijian Cai, Yuhang Zhang, Ying Liu, Yongbin Zheng</span>
      </li>
      <li>
        <span class="paper-title">Interactive Grounding for Multi-Robot Coordination using Affordance-Based Hypergraphs</span>
        <span class="paper-authors">Noah Boehme, Geoffrey Hollinger</span>
      </li>
      <li>
        <span class="paper-title">Verifier-Mediated Multi-LLM Coordination for Multi-Robot Path Planning</span>
        <span class="paper-authors">Vivek Khatana, Zijian Song, Naira Hovakimyan, Petros G. Voulgaris</span>
      </li>
  </ol>
</div>

<!-- Call for Papers -->
<div class="ws-section">
  <h2>Call for Papers</h2>
  <div class="cfp-box">
    <p>We invite submissions of extended abstracts (2–4 pages, including references) on topics including but not limited to:</p>
    <ul>
      <li>LLM- and VLM-driven multi-robot coordination and planning</li>
      <li>Language-specified missions for heterogeneous robot teams</li>
      <li>Foundation-model-based decentralized reasoning and multi-robot communication</li>
      <li>Reliability and safety of foundation models in robot teams: constraint checking, formal verification, and conformal prediction</li>
      <li>Foundation models for multi-agent decision making and task allocation</li>
      <li>Real-world deployment of foundation-model-enabled robot fleets</li>
    </ul>
    <p style="margin-bottom:0">Accepted papers are presented as a <strong>2-minute lightning talk</strong> followed by a <strong>poster presentation</strong> during the coffee break session.</p>
    <p><strong>Submit your paper via <a href="https://openreview.net/group?id=IEEE.org/IROS/2026/Workshop/FM-MRS" target="_blank">OpenReview</a>.</strong></p>
    <p>Please prepare your submission in the standard IEEE conference format. You can find the right template using the <a href="https://template-selector.ieee.org/secure/templateSelector/publicationType" target="_blank">IEEE template selector</a>.</p>
    <p style="margin-bottom:0"><strong>Submissions are now closed.</strong> The deadline was August 23, 2026.</p>
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
      <img class="person-photo" src="/assets/img/IROS2026workshop/organizers/Peihan Li.jpeg" alt="Peihan Li">
      <div class="org-name"><a href="https://scholar.google.com/citations?user=Qg7-Gr0AAAAJ&hl=en" target="_blank">Peihan Li</a></div>
      <div class="org-affil">Drexel University</div>
    </div>

    <div class="organizer-card">
      <img class="person-photo" src="/assets/img/IROS2026workshop/organizers/Jiachen Li.jpeg" alt="Jiachen Li">
      <div class="org-name"><a href="https://jiachenli94.github.io/" target="_blank">Jiachen Li</a></div>
      <div class="org-affil">Georgia Tech</div>
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
      <img class="person-photo" src="/assets/img/IROS2026workshop/organizers/Pratap_Tokekar.jpeg" alt="Pratap Tokekar">
      <div class="org-name"><a href="https://scholar.google.com/citations?user=FKAovywAAAAJ&hl=en" target="_blank">Pratap Tokekar</a></div>
      <div class="org-affil">University of Maryland</div>
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
  <p>For inquiries, please contact Lifeng Zhou (lz457#drexel.edu) and Peihan Li (pl525#drexel.edu) at Drexel University.</p>
</div>
