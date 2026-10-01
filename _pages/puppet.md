---
title: "Hardware Prototyping: Low-Latency Behavioral Testbed"
layout: single
permalink: /puppet/
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

/* Iteration Phase Cards */
.phase-card {
  border: 1px solid #e1e4e8;
  border-radius: 8px;
  background: #ffffff;
  padding: 22px;
  margin-bottom: 24px;
  box-shadow: 0 2px 6px rgba(0,0,0,0.03);
}
.phase-card h3 {
  margin-top: 0;
  margin-bottom: 8px;
  color: #1f2328;
}
.phase-badge {
  display: inline-block;
  font-size: 0.75em;
  font-weight: 700;
  text-transform: uppercase;
  color: #0969da;
  background: #ddf4ff;
  border: 1px solid rgba(84, 174, 255, 0.4);
  padding: 2px 8px;
  border-radius: 10px;
  margin-bottom: 10px;
}
.phase-media {
  text-align: center;
  margin: 16px 0;
}
.phase-media img {
  max-width: 100%;
  max-height: 320px;
  border-radius: 6px;
  border: 1px solid #eee;
  object-fit: contain;
}

/* Architecture Specs */
.arch-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
  gap: 16px;
  margin: 20px 0;
}
.arch-item {
  border: 1px solid #d0d7de;
  border-radius: 6px;
  padding: 14px 16px;
  background: #fafbfc;
}
.arch-item strong {
  display: block;
  font-size: 0.88em;
  color: #0969da;
  margin-bottom: 4px;
}
.arch-item p {
  margin: 0;
  font-size: 0.9em;
  line-height: 1.4;
  color: #333;
}
</style>

<!-- Metadata Grid -->
<div class="project-meta-grid">
  <div class="meta-item">
    <strong>My Role</strong>
    <span>Hardware & System Prototyping, Iterative CAD Design, User Testing</span>
  </div>
  <div class="meta-item">
    <strong>Collaboration</strong>
    <span>Carnegie Mellon University (Howie Wang & Dr. Nikolas Martelaro)</span>
  </div>
  <div class="meta-item">
    <strong>Core Toolkit</strong>
    <span>Autodesk Fusion (CAD), 3D Printing, Python, Raspberry Pi, Dynamixel Servos</span>
  </div>
  <div class="meta-item">
    <strong>Project Scope</strong>
    <span>MVP Hardware Testbed for Real-Time Teleoperation & Behavioral Simulation</span>
  </div>
</div>

## Executive Summary

Autonomous mobile systems navigating public pedestrian spaces require legible gaze and directional cues to prevent collisions and build user trust. However, developing and debugging fully autonomous computer vision and gaze-tracking algorithms directly on mobile robots in early project phases introduces significant overhead, software dependencies, and high failure rates.

To de-risk development, I co-developed an **MVP hardware puppeteering testbed**—a 2-degree-of-freedom (2-DOF) physical teleoperation rig executing real-time motor mirroring between an operator "puppet" interface and a robot head. This physical testbed enabled our team to rapidly simulate, evaluate, and iterate on complex behavioral signaling in live user studies without requiring autonomous navigation software.

<div class="insight-box">
  <p><strong>The Product Advantage:</strong> By building a lightweight Wizard-of-Oz teleoperation tool, we reduced user-testing setup time from hours of software calibration to minutes, allowing rapid prototyping of recognizable non-verbal expressions directly in front of human participants.</p>
</div>

---

## Iterative Design & Prototyping Lifecycle

The system evolved through an iterative hardware and ergonomic design process, progressing from proof-of-concept mechanics to a recognizable social interface:

<div class="phase-card">
  <span class="phase-badge">Phase 1: Proof-of-Concept & Kinematic MVP</span>
  <h3>Minimal Viable 2-DOF Mechanism</h3>
  <p>To isolate core motion variables and reduce initial complexity, the first prototype used a minimalist wooden plate mounted on a 2-DOF pan-and-tilt base rather than a digital screen or facial features.</p>
  <div class="phase-media">
    <img src="/files/prototype_wood.gif" alt="Initial wooden plate prototype executing pan-tilt mirroring">
  </div>
  <p><strong>User Pilot Findings:</strong> Early testing demonstrated that even without eyes or facial markers, participants intuitively perceived the flat plate as the robot's "face" and correctly interpreted basic directional attention and orientation cues purely through pan/tilt velocity and tilt angles.</p>
</div>

<div class="phase-card">
  <span class="phase-badge">Phase 2: CAD Design & Mechanical Integration</span>
  <h3>Custom Enclosure & Camera Housing</h3>
  <p>To enable forward orientation and integrate sensing payloads, I modeled a custom head assembly in Autodesk Fusion. The design accommodated two degrees of freedom (pan and tilt), integrated internal cable routing, and housed dual-camera fixtures while maintaining minimal payload weight on the Dynamixel actuators.</p>
  <div class="phase-media">
    <img src="/files/prototype_autodesk.png" alt="CAD model of robotic head assembly in Autodesk Fusion">
  </div>
  <p><strong>Design Consideration:</strong> Balanced torque limits and gear lash to ensure low-latency physical response without introducing jitter into subtle head movements.</p>
</div>

<div class="phase-card">
  <span class="phase-badge">Phase 3: High-Fidelity Fabrication & User Testing</span>
  <h3>3D-Printed Binocular Head Assembly</h3>
  <p>The final physical iteration utilized 3D-printed lightweight components featuring binocular eye structures inspired by industrial animation principles (e.g., Wall-E). This structural design gave the system an unmistakable forward focal vector, critical for directional gaze legibility in pedestrian trials.</p>
  <div class="phase-media">
    <img src="/files/prototype_head.gif" alt="3D printed robot head with binocular eyes executing synchronized tracking">
  </div>
  <p><strong>Validation Outcome:</strong> Remote and in-person pilot participants confirmed that synchronized real-time head tilting created a strong sense of acknowledgment. Pedestrians reported the physical movements felt responsive, approachable, and clearly indicated where the robot was "looking."</p>
</div>

---

## Technical System Architecture

The distributed architecture was engineered for low-latency synchronization and modular deployment across mobile platforms:

<div class="arch-grid">
  <div class="arch-item">
    <strong>Operator Interface (Puppet)</strong>
    <p>Handheld 2-DOF rig equipped with Dynamixel AX-12W actuators acting as physical encoders, polling joint positions in real time via USB-to-serial interfaces.</p>
  </div>
  <div class="arch-item">
    <strong>Embedded Compute</strong>
    <p>Dual Raspberry Pi microcomputers running Python scripts that package coordinate streams into lightweight timestamped JSON payloads over a local network.</p>
  </div>
  <div class="arch-item">
    <strong>Robot Actuator Unit</strong>
    <p>Target pan-and-tilt robotic head mirroring coordinates in real time. Features packet optimization and sleep timers to eliminate network latency and power draw during idle states.</p>
  </div>
</div>

---

## Key Takeaways & Impact

* **Rapid Behavioral Scoping:** Established that 2-DOF pan-and-tilt motion provides sufficient expressive bandwidth to convey directional attention, eliminating the need for expensive multi-axis facial animatronics in navigation contexts.
* **Low-Latency Wizard-of-Oz Testing:** Delivered a reliable research testbed that bypassed software bottlenecks, enabling real-time human-in-the-loop experiments for both lab settings and mobile outdoor UGV deployments.
* **Ergonomic Affordance:** Binocular physical structures provided immediate intent legibility, helping pedestrians determine the robot’s trajectory significantly faster than nondirectional planar surfaces.
