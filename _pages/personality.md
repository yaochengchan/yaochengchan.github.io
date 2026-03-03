---
title: "Developing Extrovert, Ambivert, and Introvert Robot"
layout: single
permalink: /personality/
author_profile: true
---

My research in human-robot interaction focuses on designing and evaluating humanoid robot personalities. While most studies examine only extrovert and introvert traits, my work introduces the ambivert personality to create more adaptable robots. I use multimodal communication, specifically combining textual and gestural cues, to successfully convey these distinct personality profiles. Beyond personality design, I investigate how task context influences user perceptions of robots. My experiments show that factors like task complexity and financial risk amplify how users evaluate a robot's personality. For example, in high-stakes tasks, users strongly prefer extrovert and ambivert robots over introvert ones. Ultimately, this research provides guidelines for aligning robot behaviors with specific service demands.

<style>
  .carousel-container {
    position: relative;
    max-width: 600px;
    margin: 0 auto 30px auto;
    overflow: hidden;
    border: 1px solid #ddd;
    border-radius: 8px;
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
</style>

<div class="carousel-container">
  <div class="carousel-slides" id="robotCarousel">
    <div class="carousel-slide">
      <img src="/files/personality1.png" alt="Introvert Robot Behavior">
      <p class="carousel-caption"><em>Figure 1a: Pepper setup</em></p>
    </div>
    <div class="carousel-slide">
      <img src="/files/personality2.png" alt="Ambivert Robot Behavior">
      <p class="carousel-caption"><em>Figure 1b: A participant interacting with Pepper</em></p>
    </div>
    <div class="carousel-slide">
      <img src="/files/personality3.png" alt="Extrovert Robot Behavior">
      <p class="carousel-caption"><em>Figure 1c: Textual Cues</em></p>
    </div>
  </div>
  <button class="carousel-btn prev" onclick="moveSlide(-1)">&#10094;</button>
  <button class="carousel-btn next" onclick="moveSlide(1)">&#10095;</button>
</div>

<script>
  let currentSlide = 0;
  function moveSlide(direction) {
    const track = document.getElementById('robotCarousel');
    const totalSlides = track.children.length;
    currentSlide = (currentSlide + direction + totalSlides) % totalSlides;
    track.style.transform = `translateX(-${currentSlide * 100}%)`;
  }
</script>

<hr>

## Interventions
To evaluate the impact of personality, we manipulated the multimodal communication behaviors of the humanoid robot Pepper. This involved adjusting both physical nonverbal cues and the textual information displayed on the robot's tablet:
* **Extrovert:** The robot utilized larger and faster hand motions, along with wider head nods. It maintained frequent, direct eye contact, positioned itself closer to the user, leaned backward to utilize more space, and displayed enlarged text on its screen.
* **Ambivert:** This personality was created by balancing extroverted and introverted characteristics. The robot displayed an equal 50% mix of introvert and extrovert behavioral cues and presented textual information in structured sections with consistent font sizing.
* **Introvert:** The robot utilized smaller, slower hand motions and head nods. It exhibited less frequent eye contact by looking downward, positioned itself farther away from the user, leaned forward, and displayed information using a bulleted text format.

<div style="text-align: center; margin: 30px 0;">
  <img src="/files/pepper_intervention.png" alt="Multimodal Cues for Robot Personality" style="max-width: 100%; height: auto; border-radius: 8px;">
</div>

<hr>

<h1 style="text-align: center; margin-top: 40px; margin-bottom: 30px;">Related Publications</h1>

### The Impacts of Social Humanoid Robot's Nonverbal Communication on Perceived Personality Traits
This study investigates how nonverbal textual and gestural cues can generate a spectrum of robot personality traits, including introvert, ambivert, and extrovert profiles. We conducted empirical studies using the humanoid robot Pepper to evaluate the impact of these multimodal communication strategies on user perceptions. The results confirm that combining textual and gestural cues significantly outperforms using textual cues alone, leading to higher participant ratings for intention to use, perceived animacy, and likeability. Notably, the ambivert robot utilizing multimodal communication received the highest ratings for likeability and intentions to use.

<a href="https://doi.org/10.1080/10447318.2023.2295696" style="display: inline-block; background-color: #333; color: white; padding: 8px 15px; border-radius: 20px; text-decoration: none; font-size: 0.9em; margin-bottom: 20px;">📄 Paper</a>

### An Exploration of Multimodal Communication for Developing Extrovert, Ambivert, and Introvert Robot
This study explores how nonverbal cues can express robot personalities. It addresses a gap in the literature by integrating introvert and extrovert traits to create an ambivert robot personality. Through analyzing bodily movements and gestural behaviors such as eye contact, body orientation, and hand gestures, participants successfully discerned extroverted and introverted characteristics with an 83% correctness rate. These findings provide foundational guidelines for developing effective human-robot communication.

<a href="https://doi.org/10.1145/3610978.3640567" style="display: inline-block; background-color: #333; color: white; padding: 8px 15px; border-radius: 20px; text-decoration: none; font-size: 0.9em; margin-bottom: 20px;">📄 Paper</a>

### The Influence of Personality Traits in Human-Humanoid Robot Interaction
This research investigates how to use a humanoid robot's textual and gestural information to develop extrovert, ambivert, and introvert personality traits. We recruited 255 participants for pilot tests and lab studies to examine these traits under different levels of task complexity. The empirical results reveal that the developed gestural cues allow a humanoid robot to distinguishably convey these personalities, and the perceived traits significantly affect user intentions to interact with the robot.

<a href="https://doi.org/10.1002/pra2.644" style="display: inline-block; background-color: #333; color: white; padding: 8px 15px; border-radius: 20px; text-decoration: none; font-size: 0.9em; margin-bottom: 20px;">📄 Paper</a>

### Risk Amplifies Personality: User Perceptions of Service Robots in High and Low Stakes Financial Tasks
This study investigates the effects of robot personality by introducing the ambivert trait alongside extrovert and introvert traits. We executed lab experiments and pilot tests using the humanoid robot Pepper to explore how multimodal communication strategies shape user perceptions in a financial robo-advisor setting. The results demonstrate that extrovert and ambivert robot behaviors significantly improve user purchase intentions, perceived sociability, and service ratings in high-risk financial tasks.

<a href="#" style="display: inline-block; background-color: #333; color: white; padding: 8px 15px; border-radius: 20px; text-decoration: none; font-size: 0.9em; margin-bottom: 20px;">📄 Under Review at IROS</a>
