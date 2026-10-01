---
title: "Method Validation: Simulation vs. Real-World Field Testing"
layout: single
permalink: /vid2real/
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
    <span>Co-Author, Framework Methodology, Experimental Validation</span>
  </div>
  <div class="meta-item">
    <strong>Core Methodologies</strong>
    <span>Within/Between-Subjects Design, Statistical Power Analysis, Mixed-Methods</span>
  </div>
  <div class="meta-item">
    <strong>Toolkit</strong>
    <span>G*Power, SPSS, R, Qualtrics, Statistical Modeling (ANOVA/LMM)</span>
  </div>
  <div class="meta-item">
    <strong>Primary Impact</strong>
    <span>Empirical framework aligning low-cost digital simulations with physical field trials</span>
  </div>
</div>

## Executive Summary

A fundamental challenge across User Experience Research and product validation is balancing **study velocity against ecological validity**. Running physical, in-situ evaluations of embodied systems (e.g., autonomous machines, hardware interfaces, spatial computing) is time-intensive, technically complex, and costly. Conversely, lightweight online video studies and digital prototypes are fast and scalable, but frequently suffer from artificial lab bias and questionable real-world transferability.

To solve this trade-off, our team developed and empirically evaluated the **Vid2Real HRI Framework**—a structured research methodology that aligns video-based experimental designs with specific real-world field settings. By calibrating online simulation conditions against live Wizard-of-Oz deployments, this framework enables teams to use rapid video prototypes to reliably de-risk interaction designs and accurately forecast real-world human behavior.

<div class="insight-box">
  <p><strong>The Core Research Insight:</strong> Video simulations provide high statistical power for isolating subjective perceptual differences (e.g., social intelligence, perceived warmth) and estimating accurate sample sizes. However, they systematically overestimate user attention compared to live, distracting field environments. Vid2Real provides the blueprint to bridge this gap.</p>
</div>

---

## The Vid2Real Framework Pipeline

The framework establishes a circular, commensurable research workflow between digital testing and in-situ physical deployment:

<table class="matrix-table">
  <thead>
    <tr>
      <th>Stage</th>
      <th>Operational Focus</th>
      <th>Key Deliverable</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>1. Real-World Alignment</strong></td>
      <td>Define the target field scenario (physical location, pedestrian flow, potential edge cases) before recording video assets.</td>
      <td>Hypothetical field study protocol and scenario constraints.</td>
    </tr>
    <tr>
      <td><strong>2. Commensurable Video Study</strong></td>
      <td>Record high-fidelity video stimuli from standardized user vantages (e.g., encounterer vs. bystander perspectives) matching the field site.</td>
      <td>Scalable online evaluation isolating specific behavioral variables.</td>
    </tr>
    <tr>
      <td><strong>3. Statistical Calibration & Power Sizing</strong></td>
      <td>Analyze effect sizes and variance from online cohorts to calculate exact sample sizes needed for physical trials.</td>
      <td>G*Power calculations preventing underpowered, costly field experiments.</td>
    </tr>
    <tr>
      <td><strong>4. In-Situ Validation (In Vivo)</strong></td>
      <td>Execute targeted physical deployment testing only the highest-signal conditions identified during digital simulation.</td>
      <td>Empirically validated design guidelines and verified behavioral transfer.</td>
    </tr>
  </tbody>
</table>

---

## Experimental Validation: Video vs. Real-World Encounters

To validate the framework, we conducted a dual-modality study testing pedestrian reactions to an autonomous mobile platform utilizing baseline gaits versus expressive body language and verbal signaling:

* **Online Video Evaluation ($N = 128+$):** Conducted a controlled between-subjects evaluation measuring perceived social intelligence, animacy, and compliance intentions. The data confirmed significant effect sizes for expressive movements, providing the statistical parameters needed to power a live study ($Power = 0.95$).
* **Physical Deployment Validation:** Deployed the physical platform in an active campus corridor testing the top-performing conditions. We observed direct alignment in directional user sentiment between modalities, while uncovering critical real-world attentional dynamics that video simulations missed.

---

## Practical UX Research Guidelines

<div class="guideline-card">
  <h4>1. Use Video Prototypes for Rapid Condition Pruning</h4>
  <p>Never test untested multi-arm variations directly in costly field trials. Use commensurable video simulations to eliminate weak interface variants and narrow down to the 2–3 highest-performing conditions.</p>
</div>

<div class="guideline-card">
  <h4>2. Calculate Real-World Sample Sizes from Simulation Variance</h4>
  <p>Field studies in shared spaces almost always require between-subject designs due to order effects and participant exhaustion. Vid2Real uses variance measured in low-cost online studies to precisely calculate the minimum sample size required for physical field statistical power.</p>
</div>

<div class="guideline-card">
  <h4>3. Standardize Camera Vantages to Match Real-World Gaze Vectors</h4>
  <p>How an interaction is recorded dictates user evaluation. First-person encounter vantages predict personal discomfort and proximity boundaries, whereas third-person observer vantages artificially inflate sociability ratings.</p>
</div>

---

## Related Publications & Resources

* **Vid2Real HRI: Align Video-Based HRI Study Designs with Real-World Settings**  
  *33rd IEEE International Conference on Robot and Human Interactive Communication (RO-MAN 2024)* — [Paper](https://arxiv.org/abs/2403.15798)
* **Community Embedded Robotics: Vid2Real Online Video Dataset**  
  *Texas Data Repository (2024)* — [Open Dataset](https://vid2real.github.io/vid2realHRI)
* **Shaping Perceptions of Robots With Video Vantages**  
  *ACM/IEEE International Conference on Human-Robot Interaction (HRI 2025)* — [Paper](https://doi.org/10.1109/HRI61500.2025.10974252)
