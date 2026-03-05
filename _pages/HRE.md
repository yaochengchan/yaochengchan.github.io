<style>
  /* Container holds the carousel and hides overflowing images */
  .carousel-container {
    position: relative;
    width: 100%;
    max-width: 600px; /* You can adjust this width */
    margin: 0 auto;
    overflow: hidden; 
    border-radius: 8px;
    background-color: #f9f9f9;
  }

  /* Aligns all slides in a horizontal row */
  .carousel-slides {
    display: flex;
    transition: transform 0.4s ease-in-out;
  }

  /* Ensures each slide takes up exactly 100% of the container width */
  .carousel-slide {
    min-width: 100%;
    box-sizing: border-box;
    text-align: center;
  }

  /* Makes images scale correctly within the slide */
  .carousel-slide img {
    width: 100%;
    height: auto;
    display: block;
    object-fit: cover;
  }

  /* Styling for the text below the images */
  .carousel-caption {
    margin: 10px 0;
    padding: 0 15px;
    font-size: 0.9em;
    color: #333;
  }

  /* Styling for the navigation buttons */
  .carousel-btn {
    position: absolute;
    top: 45%;
    transform: translateY(-50%);
    background-color: rgba(0, 0, 0, 0.5);
    color: white;
    border: none;
    padding: 10px 15px;
    cursor: pointer;
    font-size: 18px;
    border-radius: 50%;
    z-index: 10;
  }

  .carousel-btn.prev {
    left: 10px;
  }

  .carousel-btn.next {
    right: 10px;
  }

  .carousel-btn:hover {
    background-color: rgba(0, 0, 0, 0.8);
  }
</style>
