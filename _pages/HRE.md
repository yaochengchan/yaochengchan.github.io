---
layout: single
title: "Deployment & Human Reaction: Evaluating Autonomous Signaling in Shared Spaces"
permalink: /HRE/
author_profile: true
classes: wide
---

<style>
/* Metadata Grid */
.project-meta-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 16px;
  background: #f6f8fa;
  border: 1px solid #d0d7de;
  border-radius: 8px;
  padding: 18px 20px;
  margin-bottom: 30px;
}
.meta-item strong {
  display: block;
  font-size: 0.8em;
  text-transform: uppercase;
  letter-spacing: 0.5px;
  color: #57606a;
  margin-bottom: 4px;
}
.meta-item span {
  font-size: 0.95em;
  color: #24292f;
  line-height: 1.4;
}

/* Callout Box */
.insight-box {
  background: #f0f7ff;
  border-left: 4px solid #0969da;
  padding: 16px 20px;
  border-radius: 0 8px 8px 0;
  margin: 24px 0;
}
.insight-box p {
  margin: 0;
  font-size: 0.95em;
  line-height: 1.5;
  color: #1f2328;
}

/* Carousel Styling */
.carousel-container {
  position: relative;
  max-width: 650px;
  margin: 20px auto 25px auto;
  overflow: hidden;
  border: 1px solid #d0d7de;
  border-radius: 8px;
  background-color: #fafbfc;
}
.carousel-slides {
  display: flex;
  transition: transform 0.4s ease-in-out;
}
.carousel-slide {
  min-width: 100%;
  box-sizing: border-box;
}
.carousel-slide img {
  width: 100%;
  height: 320px;
  object-fit: contain;
  background-color: #fafbfc;
  display: block;
}
.carousel-caption {
  text-align: center;
  padding: 10px 14px;
  font-size: 0.85em;
  color: #57606a;
  background-color: #ffffff;
  border-top: 1px solid #eaeef2;
  margin: 0;
}
.carousel-btn {
  position: absolute;
  top: 45%;
  background-color: rgba(0, 0, 0, 0.55);
  color: white;
  border: none;
  padding: 10px 14px;
  cursor: pointer;
  font-size: 16px;
  border-radius: 4px;
  user-select: none;
  z-index: 10;
}
.carousel-btn:hover {
  background-color: rgba(0, 0, 0, 0.8);
}
.carousel-btn.prev { left: 10px; }
.carousel-btn.next { right: 10px; }

/* Guideline Cards */
.guideline-card {
  border: 1px solid #e1e4e8;
  border-radius: 8px;
  padding: 16px 20px;
  margin-bottom: 14px;
  background: #ffffff;
}
.guideline-card h4 {
  margin: 0 0 6px 0;
  color: #0969da;
}
.guideline-card p {
  margin: 0;
  font-size: 0.92em;
  line-height: 1.5;
  color: #333;
}
</style>

<!-- Section 1: Executive Metadata Grid -->
<div class="project-meta-grid">
  <div class="meta-item">
    <strong>My Role</strong>
    <span>Lead Researcher & Experimental Designer (End-to-End Study Execution)</span>
  </div>
  <div class="meta-item">
    <strong>Methodology</strong>
    <span>Mixed-Methods, Controlled Video Studies, Field Deployments, Grounded Theory</span>
  </div>
  <div class="meta-item">
    <strong>Key Tools</strong>
    <span>SPSS, Python, Qualtrics, Clearpath Husky UGV, Boston Dynamics Spot</span>
  </div>
  <div class="meta-item">
    <strong>Impact & Outcome</strong>
    <span>Empirical design framework identifying human perceptual bottlenecks in autonomous public signaling</span>
  </div>
</div>

## Project Overview

When autonomous robots operate in pedestrian environments (sidewalks, hallways, building lobbies), they share physical space with everyday bystanders who have no prior training or expectation of meeting a machine. 

To prevent collisions, navigational hesitation, and public discomfort, autonomous systems need clear communicative signaling. This research evaluated how different visual and behavioral modalities, ranging from anthropomorphic eye gaze to explicit physical indicators, shape human perception, trust, and behavioral compliance during incidental encounters.

<div style="text-align: center; margin: 25px 0;">
  <img src="/files/HRE_theme.png" alt="Incidental Human Robot Encounter Core Framework" style="max-width: 100%; height: auto; border-radius: 8px; border: 1px solid #e1e4e8;">
</div>

---

## The Research Question & Challenges

1. **Intent Legibility:** Which signaling modalities (gaze, light patterns, arrow pointers) most effectively communicate directional navigation intent to pedestrians?
2. **Controlled vs. In-Situ Validity:** Do behavioral benefits observed in controlled video evaluations hold true when pedestrians encounter a live robot in a busy, distracting public corridor?
3. **Contextual Legibility:** How do physical cues of human oversight (such as handlers, joysticks, or service vests) affect public comfort and perceived safety?

---

## Study Design & Methodology

A multi-phase mixed-methods approach bridged controlled laboratory testing with physical field deployments:

* **Phase 1: Controlled Online Video Evaluations:** Tested five distinct signaling interventions (Puppet System, Nao Gestures, Arrow Pointers, LED Strips, Animated Eyes) using standardized scales, including the Perceived Social Intelligence (PSI) scale, to isolate perceptual baseline differences.
* **Phase 2: In-Situ Public Field Deployment:** Deployed a Clearpath Husky mobile platform in an active university hallway with scheduled pedestrian participants to measure real-time proxemics, avoidance maneuvers, and immediate perceptual responses.
* **Phase 3: Qualitative Investigation & Thematic Analysis:** Conducted post-encounter semi-structured interviews analyzed via Grounded Theory and hybrid thematic coding to uncover the underlying cognitive models bystanders construct when interpreting autonomous machines.

---

## Evaluated Interventions

### 1. Directional Signaling Modalities (Clearpath Husky Platform)
We evaluated communicative mechanisms designed to signal navigation trajectory and acknowledge oncoming pedestrian traffic:

<div class="carousel-container">
  <div class="carousel-slides" id="huskyCarousel" data-current-slide="0">
    <div class="carousel-slide">
      <img src="/files/img_phase1.png" alt="Husky Signaling Modalities">
      <p class="carousel-caption">Five signaling modalities tested: Robotic Puppeteering, Humanoid Nao gestures, Arrow Pointers, LED Strips, and Animated Eyes.</p>
    </div>
    <div class="carousel-slide">
      <img src="/files/img_phase2.png" alt="Husky Hallway Field Test Setup">
      <p class="carousel-caption">Real-world experimental setup in an active public pedestrian corridor.</p>
    </div>
  </div>
  <button class="carousel-btn prev" onclick="moveSlide(-1, 'huskyCarousel')">&#10094;</button>
  <button class="carousel-btn next" onclick="moveSlide(1, 'huskyCarousel')">&#10095;</button>
</div>

### 2. Expressive Non-Verbal Movement (Boston Dynamics Spot)
Investigated whether non-functional, canine-inspired gaits (tail wagging, play bows, sit-and-wait) could mitigate intimidation and increase public approachability compared to standard mechanical locomotion.

<div class="carousel-container">
  <div class="carousel-slides" id="spotGaitCarousel" data-current-slide="0">
    <div class="carousel-slide">
      <img src="/files/BL1.png" alt="Spot Wagging Gait">
      <p class="carousel-caption">Gait modification: Expressive tail-wagging motion</p>
    </div>
    <div class="carousel-slide">
      <img src="/files/BL2.png" alt="Spot Play Bow">
      <p class="carousel-caption">Play bow and seated waiting posture</p>
    </div>
    <div class="carousel-slide">
      <img src="/files/BL3.png" alt="Spot Spin Gait">
      <p class="carousel-caption">Rotational gestures and expressive avoidance loops</p>
    </div>
  </div>
  <button class="carousel-btn prev" onclick="moveSlide(-1, 'spotGaitCarousel')">&#10094;</button>
  <button class="carousel-btn next" onclick="moveSlide(1, 'spotGaitCarousel')">&#10095;</button>
</div>

### 3. Visual Indicators of Supervision & Human Control
Tested how physical visual cues (handler presence, leash attachment, remote joystick, service vest) alter public comfort in shared public corridors.

<div class="carousel-container">
  <div class="carousel-slides" id="spotLeashCarousel" data-current-slide="0">
    <div class="carousel-slide">
      <img src="/files/autonomous.png" alt="Fully Autonomous Mode">
      <p class="carousel-caption">Baseline: Unassisted autonomous operation</p>
    </div>
    <div class="carousel-slide">
      <img src="/files/controller.png" alt="Handler with Controller">
      <p class="carousel-caption">Handler utilizing visible joystick controller</p>
    </div>
    <div class="carousel-slide">
      <img src="/files/companion.png" alt="Passive Human Companion">
      <p class="carousel-caption">Passive human companion walking alongside platform</p>
    </div>
    <div class="carousel-slide">
      <img src="/files/leash.png" alt="Handler with Physical Leash">
      <p class="carousel-caption">Physical tether/leash setup</p>
    </div>
    <div class="carousel-slide">
      <img src="/files/servicevest.png" alt="Service Vest Setup">
      <p class="carousel-caption">Service vest indicator</p>
    </div>
  </div>
  <button class="carousel-btn prev" onclick="moveSlide(-1, 'spotLeashCarousel')">&#10094;</button>
  <button class="carousel-btn next" onclick="moveSlide(1, 'spotLeashCarousel')">&#10095;</button>
</div>

---

## Key Research Findings

<div class="insight-box">
  <p><strong>The Real-World Perceptual Bottleneck:</strong> In controlled video evaluations, subtle anthropomorphic cues (like robotic eye gaze) significantly elevated perceived social intelligence and buffered against negative ratings during behavioral failures. However, during live field deployment in busy hallways, pedestrian attentional bandwidth was consumed by personal navigation and environmental distractions, causing subtle gaze cues to be overlooked entirely.</p>
</div>

* **Subtle Cues Fail in High-Distraction Environments:** While retrospective video analysis proved participants could decode eye gaze when prompted, in-situ pedestrians failed to notice it in real time. Signaling must be placed within primary forward sightlines and feature high luminance or explicit physical indicators.
* **Expressive Gaits Significantly Improve Perceived Warmth:** Canine-inspired movements produced statistically significant increases in perceived animacy and approachability on the Godspeed questionnaire, mitigating the intimidating impression of raw mechanical quadrupeds.
* **Visual Familiarity Mitigates Perceived Risk:** Visual cues mimicking familiar mental models (such as a handler walking with a leash or service vest) immediately resolved the bystander's primary implicit question: <em>"What is this robot doing here, and who is responsible for it?"</em>

---

## Actionable Design Guidelines for Public Systems

<div class="guideline-card">
  <h4>1. Prioritize High-Salience Forward Signaling over Micro-Interactions</h4>
  <p>Subtle anthropomorphic cues (eye gaze, minor tilts) work well in focused, stationary 1-on-1 interactions. In mobile navigation through shared public corridors, signals must use high-contrast, peripheral-friendly visual modalities (e.g., floor projections, bright light strips) to overcome real-world cognitive distractions.</p>
</div>

<div class="guideline-card">
  <h4>2. Anchor System Roles to Established Mental Models</h4>
  <p>Bystander hesitation stems from role ambiguity. Incorporating clear physical indicators of role and human oversight (service badging, status lighting, clear supervision cues) reduces hesitation and builds immediate public trust.</p>
</div>

<div class="guideline-card">
  <h4>3. Validate Beyond Controlled Digital Simulations</h4>
  <p>Lab studies and unmoderated video tests often produce false positives for subtle interaction cues because participants are focused solely on the screen. Physical, in-situ field validation is required to catch environmental edge cases and realistic attentional limitations.</p>
</div>

---

## Related Publications

* **Perceived Social Intelligence in Autonomous Robots: Evaluating Communicative Behaviors in Social Navigation Tasks**  
  *Ph.D. Dissertation, The University of Texas at Austin (May 2026)*
* **A Field Observation of Incidental Human-Robot Encounters in Public**  
  *ACM/IEEE International Conference on Human-Robot Interaction (HRI 2025)* — [Paper](https://doi.org/10.1109/HRI61500.2025.10973844)
* **Shaping Perceptions of Robots With Video Vantages**  
  *ACM/IEEE International Conference on Human-Robot Interaction (HRI 2025)* — [Paper](https://doi.org/10.1109/HRI61500.2025.10974252)
* **Influencing Incidental Human-Robot Encounters: Expressive Movement Improves Pedestrians' Impressions of a Quadruped Service Robot**  
  *arXiv Preprint (2023)* — [Paper](https://arxiv.org/abs/2311.04454)
* **Understanding Reactions in Human-Robot Encounters with Autonomous Quadruped Robots**  
  *Proceedings of the Association for Information Science and Technology (ASIS&T 2023)* — [Paper](https://doi.org/10.1002/pra2.771)
* **"What's That Robot Doing Here?": Perceptions Of Incidental Encounters With Autonomous Quadruped Robots**  
  *ACM International Conference on Human-Agent Interaction (HAI 2023)* — [Paper](https://doi.org/10.1145/3597512.3599707)

<script>
function moveSlide(direction, carouselId) {
  var track = document.getElementById(carouselId);
  if (!track) return;
  var totalSlides = track.children.length;
  var currentIndex = parseInt(track.getAttribute('data-current-slide')) || 0;
  currentIndex = (currentIndex + direction + totalSlides) % totalSlides;
  track.setAttribute('data-current-slide', currentIndex);
  track.style.transform = "translateX(-" + (currentIndex * 100) + "%)";
}
</script>
