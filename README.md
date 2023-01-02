# Js-Banner-effect
Here is an example of how you can create an animated banner effect using JavaScript

```bash
<style>
  .banner {
    position: relative;
    overflow: hidden;
    height: 200px;
  }
  .banner img {
    position: absolute;
    top: 0;
    left: 0;
  }
</style>

<div class="banner">
  <img src="image1.jpg" alt="Banner Image">
  <img src="image2.jpg" alt="Banner Image">
  <img src="image3.jpg" alt="Banner Image">
</div>

<script>
  // Get the banner element
  var banner = document.querySelector('.banner');
  // Get the images within the banner
  var images = banner.querySelectorAll('img');
  // Set the current index to 0 (the first image)
  var currentIndex = 0;
  // Set the duration of the animation (in milliseconds)
  var animationDuration = 3000;

  // Show the first image
  images[currentIndex].style.opacity = 1;

  // Set an interval to change the displayed image
  setInterval(function() {
    // Increment the current index
    currentIndex = (currentIndex + 1) % images.length;

    // Fade out the current image
    images[currentIndex].style.opacity = 0;
    // Fade in the new image
    images[currentIndex].style.opacity = 1;
  }, animationDuration);
</script>
````

This example creates a banner element with several images within it. It uses JavaScript to change the displayed image every 3 seconds (3000 milliseconds) by fading out the current image and fading in the new image.
