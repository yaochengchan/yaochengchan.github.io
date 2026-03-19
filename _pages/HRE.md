---
layout: archive
title: "Incidental Human-Robot Encounter"
permalink: /HRE/
author_profile: true
---

<style>
.carousel-container {
  position: relative;
  max-width: 600px;
  margin: 0 auto 30px auto;
  overflow: hidden;
  border: 1px solid #ddd;
  border-radius: 8px;
  background-color: #f9f9f9;
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
  height: 300px;
  object-fit: contain;
  background-color: #f9f9f9;
  display: block;
}
.carousel-caption {
  text-align: center;
  padding: 10px;
  font-size: 0.85em;
  color: #555;
  background-color: #fff;
  border-top: 1px solid #eee;
  margin: 0;
}
.carousel-btn {
  position: absolute;
  top: 40%;
  background-color: rgba(0, 0, 0, 0.5);
  color: white;
  border: none;
  padding: 10px 15px;
  cursor: pointer;
  font-size: 18px;
  border-radius: 4px;
  user-select: none;
  z-index: 10;
}
.carousel-btn:hover {
  background-color: rgba(0, 0, 0, 0.8);
}
.carousel-btn.prev {
  left: 10px;
}
.carousel-btn.next {
  right: 10px;
}

/* New styles for the side-by-side video row */
.video-row {
  display: flex;
  justify-content: space-between;
  gap: 15px;
  margin-top: 20px;
  margin-bottom: 30px;
}
.video-item {
  flex: 1;
  text-align: center;
}
.video-item iframe {
  width: 100%;
  aspect-ratio: 16 / 9;
  border-radius: 8px;
  background-color: #000;
}
.video-caption {
  font-size: 0.85em;
  color: #555;
  margin-top: 5px;
}

/* Stack videos on smaller screens */
@media (max-width: 768px) {
  .video-row {
    flex-direction: column;
  }
}
</style>

An incidental human-robot encounter occurs when a person unexpectedly shares a physical space with an autonomous robot during their routine activities. Unlike planned interactions where a user actively operates or collaborates with a machine, these encounters typically involve everyday bystanders in public settings, such as pedestrians walking past a service robot on a sidewalk.

Because these individuals usually have no prior training or expectation of meeting the robot, they must quickly interpret its movements and communication signals to understand its intent and figure out how to navigate around it. Evaluating these brief, unscripted events helps researchers understand how a robot's design, body language, and verbal cues affect public perception, perceived social intelligence, and overall acceptance in shared spaces.

<div style="text-align: center; margin: 30px 0;">
  <img src="/files/HRE_theme.png" alt="HRE" style="max-width: 100%; height: auto; border-radius: 8px;">
</div>

<hr>

<h2>Design Interventions for Public Encounters</h2>
<p>To improve how bystanders experience incidental encounters, I design and run tests on several behavioral and physical design modifications on autonomous service robots. These interventions are designed to increase a robot's perceived social intelligence and help pedestrians understand the robot's purpose in a shared space.</p>

<ul>
  <li style="margin-bottom: 30px;">
    <strong>Communicative Behaviors (Clearpath Robotics Husky):</strong> We evaluated communicative behaviors, such as animated robotic eyes, to signal a robot's intent during social navigation.
    <br><br>
   
  <div class="carousel-container">
    <div class="carousel-slides" id="huskyCarousel" data-current-slide="0">
        <div class="carousel-slide">
          <img src="/files/img_phase1.png" alt="Husky Gaze Cues">
          <p class="carousel-caption"><em>Figure 1a: Five distinct communicative behaviors tested for trajectory signaling: Puppet System, Nao, Arrow Pointers, LED Light, and Robotic Eyes.</em></p>
        </div>
        <div class="carousel-slide">
          <img src="/files/img_phase2.png" alt="Husky Field Test">
          <p class="carousel-caption"><em>Figure 1b: Field experiment setup in a busy environment</em></p>
        </div>
      </div>
      <button class="carousel-btn prev" onclick="moveSlide(-1, 'huskyCarousel')">&#10094;</button>
      <button class="carousel-btn next" onclick="moveSlide(1, 'huskyCarousel')">&#10095;</button>
    </div>

  <div class="video-row">
      <div class="video-item">
        <iframe src="https://drive.google.com/file/d/1uaHbn1BnCQtOKbGpFXFM-LvyVTSwxLb0/preview" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
        <p class="video-caption"><em>Video 1: Puppet System as communicative behavior</em></p>
      </div>
      <div class="video-item">
        <iframe src="https://drive.google.com/file/d/10L-wJ57eg5ja0sg_sc_wvJ9mYwA0ual_/preview" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
        <p class="video-caption"><em>Video 2: Huamnoid Nao as communcative behavior</em></p>
      </div>
      <div class="video-item">
        <iframe src="https://drive.google.com/file/d/1B2i5129QsfhOPv9bdreND4LBUJBhHepo/preview" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
        <p class="video-caption"><em>Video 3: Robotic Eyes as communicative behavior</em></p>
      </div>
    </div>

   <br>
    A three-phase mixed-methods investigation evaluated how robot communicative behaviors affect pedestrians during social navigation, using the Perceived Social Intelligence scale to measure results. Online video studies showed that anthropomorphic features, like animated robotic eyes, improved perceived social competence and protected against negative ratings during behavioral failures, such as obstructing a photographer's view. However, live field experiments in a public hallway yielded different results. Real-world distractions caused pedestrians to frequently miss these subtle gaze cues during brief encounters, resulting in no significant difference in their evaluations. Retrospective video reviews confirmed the cues were legible but overlooked in the moment, indicating that robot communication designs need high visibility and explicit signals to be noticed in active public spaces.
  </li>
   
  <li style="margin-bottom: 30px;">
    <strong>Expressive Body Language (Boston Dynamics Spot):</strong> We modified the standard walking motion of a quadruped robot to include non-functional, canine-inspired movements such as tail wagging, play bows, and spinning.
    <br><br>
     
  <div class="carousel-container">
      <div class="carousel-slides" id="spotGaitCarousel" data-current-slide="0">
        <div class="carousel-slide">
          <img src="/files/BL1.png" alt="Spot Mechanical Gait">
          <p class="carousel-caption"><em>Figure 2a: Wagging</em></p>
        </div>
        <div class="carousel-slide">
          <img src="/files/BL2.png" alt="Spot Expressive Gait">
          <p class="carousel-caption"><em>Figure 2b: Play bow and Sit</em></p>
        </div>
        <div class="carousel-slide">
          <img src="/files/BL3.png" alt="Spot Expressive Gait">
          <p class="carousel-caption"><em>Figure 2c: Walk in circle and spin</em></p>
        </div>
      </div>
      <button class="carousel-btn prev" onclick="moveSlide(-1, 'spotGaitCarousel')">&#10094;</button>
      <button class="carousel-btn next" onclick="moveSlide(1, 'spotGaitCarousel')">&#10095;</button>
    </div>

   <br>
    Our results demonstrate that participants viewed the quadruped performing these expressive movements as more friendly, responsive, doglike, and conscious compared to a robot using a standard mechanical gait. Specifically, the body language interventions produced significantly higher ratings in perceived animacy and cynomorphism (dog-like traits).
  </li>
   
  <li style="margin-bottom: 30px;">
    <strong>Visual Indicators of Control (Boston Dynamics Spot):</strong> We tested how physical additions and human presence affect public perception. We evaluated conditions featuring a human handler utilizing a joystick, a leash, or a service vest. 
    <br><br>
     
   <div class="carousel-container">
      <div class="carousel-slides" id="spotLeashCarousel" data-current-slide="0">
        <div class="carousel-slide">
          <img src="/files/autonomous.png" alt="Spot with Leash">
          <p class="carousel-caption"><em>Figure 3a: Autonomous mode</em></p>
        </div>
        <div class="carousel-slide">
          <img src="/files/controller.png" alt="Pedestrian Reaction">
          <p class="carousel-caption"><em>Figure 3b: Joystick</em></p>
        </div>
        <div class="carousel-slide">
          <img src="/files/companion.png" alt="Pedestrian Reaction">
          <p class="carousel-caption"><em>Figure 3c: Companion</em></p>
        </div>
        <div class="carousel-slide">
          <img src="/files/leash.png" alt="Pedestrian Reaction">
          <p class="carousel-caption"><em>Figure 3d: Companion with a dog leash</em></p>
        </div>
        <div class="carousel-slide">
          <img src="/files/servicevest.png" alt="Pedestrian Reaction">
          <p class="carousel-caption"><em>Figure 3e: Companion with a service vest</em></p>
        </div>
      </div>
      <button class="carousel-btn prev" onclick="moveSlide(-1, 'spotLeashCarousel')">&#10094;</button>
      <button class="carousel-btn next" onclick="moveSlide(1, 'spotLeashCarousel')">&#10095;</button>
    </div>
     
   <br>
    While standardized survey metrics showed minimal changes, in-depth interviews revealed that these visual indicators of control provided a strong sense of familiarity by mimicking a standard human-dog pairing. This familiarity led to higher perceived safety. Ultimately, these visual cues helped bystanders quickly answer the implicit question of what the robot was doing in their environment.
  </li>
</ul>

<hr>

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

<h1 style="text-align: center; margin-top: 40px; margin-bottom: 30px;">Related Publications</h1>

### Perceived Social Intelligence in Autonomous Robots: Evaluating Communicative Behaviors in Social Navigation Tasks
This dissertation addresses the challenge of integrating autonomous robots into public spaces by investigating how communicative behaviors influence pedestrians' perceived social intelligence of robots during social navigation. Through a three-phase mixed-methods investigation, the research evaluated interventions ranging from abstract signals to anthropomorphic behaviors across both video-based and real-world settings. While anthropomorphic features like animated robotic eyes enhanced perceived sociability in controlled studies, live field experiments revealed that environmental distractions and attentional constraints often render subtle social signals unnoticeable during brief encounters. This work concludes that robot design must prioritize high visibility to ensure signals are effectively perceived in active environments.

<a href="#" style="display: inline-block; background-color: #333; color: white; padding: 8px 15px; border-radius: 20px; text-decoration: none; font-size: 0.9em; margin-bottom: 20px;">📄 Dissertation (May 2026)</a>

### A Field Observation of Incidental Human-Robot Encounters in Public
This field observation explores how pedestrians react to an autonomous quadruped robot seeking assistance to enter a building. By focusing on incidental encounters, this work broadens the scope of human-robot interaction to include non-users who simply happen to be in the shared space. The findings provide insights into how robot behaviors can be designed to integrate more smoothly into human environments and highlight new directions for real-world observational research.

<a href="https://doi.org/10.1109/HRI61500.2025.10973844" style="display: inline-block; background-color: #333; color: white; padding: 8px 15px; border-radius: 20px; text-decoration: none; font-size: 0.9em; margin-bottom: 20px;">📄 Paper</a>

### Shaping Perceptions of Robots With Video Vantages
This study investigates the role of video vantages, specifically "Encounterer" and "Observer" perspectives, in shaping how people perceive a robot's social intelligence. Using videos of robots employing gaze cues while navigating hallways, the results indicate that the Observer vantage consistently yields higher perceived social intelligence ratings. These findings highlight how the chosen vantage impacts the interpretation of robot behaviors, emphasizing the need for careful design in video-based studies to ensure generalizable real-world insights.

<a href="https://doi.org/10.1109/HRI61500.2025.10974252" style="display: inline-block; background-color: #333; color: white; padding: 8px 15px; border-radius: 20px; text-decoration: none; font-size: 0.9em; margin-bottom: 20px;">📄 Paper</a>

### Influencing Incidental Human-Robot Encounters: Expressive movement improves pedestrians' impressions of a quadruped service robot
This experiment tests the impact of robot body language, defined as non-functional modifications to movement, on incidental pedestrian encounters in a real-world setting. The results demonstrate that canine-inspired expressive movements positively influenced participants' perceptions compared to the robot's stock walking motion. These positive effects were visible across all categories of the Godspeed questionnaire, suggesting that expressive body language is a practical and promising design space for improving service robot encounters.

<a href="https://arxiv.org/abs/2311.04454" style="display: inline-block; background-color: #333; color: white; padding: 8px 15px; border-radius: 20px; text-decoration: none; font-size: 0.9em; margin-bottom: 20px;">📄 Paper</a>

### Understanding Reactions in Human-Robot Encounters with Autonomous Quadruped Robots
This research applies Grounded Theory methodologies to understand human reactions during encounters with an autonomous quadruped robot. Based on observations and interviews, the study finds that a person's reaction can be explained by their familiarity, certainty, and confidence, alongside their understanding of the robot's role. By providing an emerging theory, this work helps explain the complexity of these interactions and assists hypothesis generation for future deployments of mobile service robots.

<a href="https://doi.org/10.1002/pra2.771" style="display: inline-block; background-color: #333; color: white; padding: 8px 15px; border-radius: 20px; text-decoration: none; font-size: 0.9em; margin-bottom: 20px;">📄 Paper</a>

### "What's That Robot Doing Here?": Perceptions Of Incidental Encounters With Autonomous Quadruped Robots
This research investigates how pedestrians perceive incidental encounters with autonomous quadruped robots. Through a pilot study and a revised study involving semi-structured interviews, we hypothesized that visual indicators of human control, such as a leash, would impact human perceptions. The interview data suggested that human presence elicited positive reactions, whereas traditional survey instruments focused on robot characteristics yielded insignificant results. Ultimately, this work suggests that these encounters are characterized by a person's ability to answer the implicit question, "what is that robot doing here?".

<a href="https://doi.org/10.1145/3597512.3599707" style="display: inline-block; background-color: #333; color: white; padding: 8px 15px; border-radius: 20px; text-decoration: none; font-size: 0.9em; margin-bottom: 20px;">📄 Paper</a>
