---
title: "Interaction Design: Multimodal Personality in Service Interfaces"
layout: single
permalink: /personality/
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

/* Comparison Table */
.matrix-table {
  width: 100%;
  border-collapse: collapse;
  margin: 20px 0 30px 0;
  font-size: 0.9em;
}
.matrix-table th {
  background-color: #f6f8fa;
  color: #24292f;
  text-align: left;
  padding: 10px 14px;
  border: 1px solid #d0d7de;
  font-weight: 600;
}
.matrix-table td {
  padding: 10px 14px;
  border: 1px solid #d0d7de;
  vertical-align: top;
  line-height: 1.45;
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

<!-- Metadata Grid -->
<div class="project-meta-grid">
  <div class="meta-item">
    <strong>My Role</strong>
    <span>Lead Interaction Designer & Experimental Researcher</span>
  </div>
  <div class="meta-item">
    <strong>Methodology & Scope</strong>
    <span>Multimodal Prototyping, Controlled Lab Experiments ($N = 255$), Factorial Study</span>
  </div>
  <div class="meta-item">
    <strong>Toolkit & Platform</strong>
    <span>SoftBank Robotics Pepper, Choregraphe, Python, SPSS, Tablet UI Design</span>
  </div>
  <div class="meta-item">
    <strong>Key Metrics</strong>
    <span>Intent to Adopt, Perceived Trust, Purchase Intent, Behavioral Recognition</span>
  </div>
</div>

## Project Overview

When automated physical agents or interactive kiosks provide customer-facing services (e.g., hospitality check-in, retail guidance, financial advising), their communication style directly dictates user trust, satisfaction, and adoption.

While prior systems relied on binary extrovert vs. introvert archetypes, this project introduced the **ambivert personality profile** to create more adaptable service interactions. By combining physical nonverbal kinetics (gestures, head nods, proxemics) with on-screen tablet UI, I designed and evaluated how multimodal behavioral profiles influence user perceptions across varying levels of task complexity and financial risk.

<div class="carousel-container">
  <div class="carousel-slides" id="robotCarousel" data-current-slide="0">
    <div class="carousel-slide">
      <img src="/files/personality1.png" alt="Pepper Robot Testing Setup">
      <p class="carousel-caption">Controlled laboratory interaction testing with the Pepper humanoid platform.</p>
    </div>
    <div class="carousel-slide">
      <img src="/files/personality2.png" alt="Participant interacting with Pepper">
      <p class="carousel-caption">Participant engaged in automated financial advisory evaluation.</p>
    </div>
    <div class="carousel-slide">
      <img src="/files/personality3.png" alt="Tablet Textual and Visual Cues">
      <p class="carousel-caption">Integrated tablet screen displaying dynamic typography and layout conditions.</p>
    </div>
  </div>
  <button class="carousel-btn prev" onclick="moveSlide(-1, 'robotCarousel')">&#10094;</button>
  <button class="carousel-btn next" onclick="moveSlide(1, 'robotCarousel')">&#10095;</button>
</div>

---

## Multimodal Design System

To establish legible personality profiles, I designed coordinated physical movements and visual tablet layouts mapped across three behavioral archetypes:

<table class="matrix-table">
  <thead>
    <tr>
      <th>Interaction Dimension</th>
      <th>Extrovert Profile</th>
      <th>Ambivert Profile (Adaptive)</th>
      <th>Introvert Profile</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>Gestural Kinetics</strong></td>
      <td>Large, expansive arm motions; rapid velocity; wide expressive head nods.</td>
      <td>Balanced, contextual gestures with moderate speed and standard nod amplitudes.</td>
      <td>Compact, subtle hand motions close to torso; slow velocity; minimal nodding.</td>
    </tr>
    <tr>
      <td><strong>Gaze & Proxemics</strong></td>
      <td>Continuous direct eye contact; leans backward to occupy physical space; closer interpersonal distance.</td>
      <td>Natural eye gaze distribution (alternating screen and user); neutral upright posture.</td>
      <td>Intermittent downward eye gaze; leans forward cautiously; maintains greater interpersonal distance.</td>
    </tr>
    <tr>
      <td><strong>Tablet UI & Typography</strong></td>
      <td>Enlarged typography; bold header styling; high-contrast visual callouts.</td>
      <td>Structured section blocks; standardized hierarchical typography and balanced spacing.</td>
      <td>Bulleted lists; compact font sizing; minimal decorative visual hierarchy.</td>
    </tr>
  </tbody>
</table>

<div style="text-align: center; margin: 30px 0;">
  <img src="/files/pepper_intervention.png" alt="Multimodal Interaction Cues on Pepper" style="max-width: 100%; height: auto; border-radius: 8px; border: 1px solid #e1e4e8;">
</div>

---

## Key Research Findings

<div class="insight-box">
  <p><strong>Risk Amplifies Personality Perception:</strong> In low-stakes routine tasks, users were relatively indifferent to personality variations. However, as task complexity and financial risk increased, user sensitivity spiked: participants strongly preferred extroverted and ambivert agents, while introvert agents triggered sharp declines in trust and purchase intent.</p>
</div>

* **Multimodal Cues Outperform Screen-Only Interfaces:** Combining gestural kinetics with on-screen tablet information significantly outperformed screen-only text across intention to use, likeability, and perceived social intelligence.
* **83% Behavioral Recognition Accuracy:** In blind evaluation trials, participants correctly classified extroverted and introverted profiles with an 83% accuracy rate, confirming the physical design parameters were distinct and legible.
* **The Ambivert Advantage:** The ambivert profile achieved the highest overall ratings for likeability and sustained intent-to-use, offering the ideal balance between approachability and professional restraint.

---

## Practical UX & Product Guidelines

<div class="guideline-card">
  <h4>1. Scale Assertiveness to Task Stakes</h4>
  <p>For high-risk, consequential user decisions (financial transactions, diagnostic intake, complex onboarding), passive or reserved UI behaviors increase user anxiety. Interfaces must use assertive, unambiguous cues (confident gaze, structured summaries) to project competence.</p>
</div>

<div class="guideline-card">
  <h4>2. Synchronize Physical Presence with Screen Layouts</h4>
  <p>Physical gestures and digital screens should never operate independently. Gestures serve as visual pointers to screen content; when physical movement and digital typography share consistent pacing, cognitive workload drops significantly.</p>
</div>

<div class="guideline-card">
  <h4>3. Default to Ambivert Archetypes in Mixed-Use Services</h4>
  <p>While extroverted behaviors command attention, continuous high-energy interactions cause user fatigue over extended sessions. An ambivert baseline provides the flexibility to remain clear without becoming overwhelming.</p>
</div>

---

## Related Publications

* **The Impacts of Social Humanoid Robot's Nonverbal Communication on Perceived Personality Traits**  
  *International Journal of Human-Computer Interaction (IJHCI 2024)* — [Paper](https://doi.org/10.1080/10447318.2023.2295696)
* **An Exploration of Multimodal Communication for Developing Extrovert, Ambivert, and Introvert Robot**  
  *ACM/IEEE International Conference on Human-Robot Interaction (HRI 2024)* — [Paper](https://doi.org/10.1145/3610978.3640567)
* **The Influence of Personality Traits in Human-Humanoid Robot Interaction**  
  *Proceedings of the Association for Information Science and Technology (ASIS&T 2022)* — [Paper](https://doi.org/10.1002/pra2.644)
* **Risk Amplifies Personality: User Perceptions of Service Robots in High and Low Stakes Financial Tasks**  
  *Under Review at IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS)*

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
