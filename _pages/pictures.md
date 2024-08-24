---
layout: page
title: pictures
permalink: /pictures/
nav: true
nav_order: 1
subtitle: Here are some pictures!
---
Here are some various pictures from trips and just from life in general. Click on an image to expand it! (please try it, it took me a while to get working)
<div class="gallery">
  <div class="gallery-item">
    <img src="/assets/img/1.jpg" alt="Description of Picture 1">
    <p>Me on a rock somewhere in Oregon.</p>
  </div>
  <div class="gallery-item">
    <img src="/assets/img/2.jpg" alt="Description of Picture 2">
    <p>On a boat in Lake Lucerne, Switzerland.</p>
  </div>
  <div class="gallery-item">
    <img src="/assets/img/3.jpg" alt="Description of Picture 3">
    <p>The Norte Dame Cathedral of Strasbourg, in Strasbourg, France.</p>
  </div>
  <div class="gallery-item">
    <img src="/assets/img/4.jpg" alt="Description of Picture 4">
    <p>On top of Dog Mountain, Washington.</p>
  </div>
  <div class="gallery-item">
    <img src="/assets/img/5.jpg" alt="Description of Picture 5">
    <p>Also Dog Mountain.</p>
  </div>
  <div class="gallery-item">
    <img src="/assets/img/6.jpg" alt="Description of Picture 6">
    <p>Village of Endelberg, Switzerland.</p>
  </div>
  <div class="gallery-item">
    <img src="/assets/img/7.jpg" alt="Description of Picture 1">
    <p>Snowy swiss alps, one of my favorite photos.</p>
  </div>
  <div class="gallery-item">
    <img src="/assets/img/8.jpg" alt="Description of Picture 2">
    <p>More mountain.</p>
  </div>
  <div class="gallery-item">
    <img src="/assets/img/9.jpg" alt="Description of Picture 3">
    <p>Atop Mt Titlis.</p>
  </div>
  <div class="gallery-item">
    <img src="/assets/img/10.jpg" alt="Description of Picture 4">
    <p>Highest suspension bridge in Europe, very cold!</p>
  </div>
  <div class="gallery-item">
    <img src="/assets/img/11.jpg" alt="Description of Picture 5">
    <p>Lake Lucerne.</p>
  </div>
  <div class="gallery-item">
    <img src="/assets/img/12.jpg" alt="Description of Picture 6">
    <p>Lucerne.</p>
  </div>
  <!-- Add more images here -->
</div>

<!-- Modal for expanding images -->
<div id="modal" class="modal">
  <span class="close">&times;</span>
  <img class="modal-content" id="modal-img">
</div>

<style>
.gallery {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 10px;
  margin-top: 20px;
}

.gallery-item {
  text-align: center;
}

.gallery-item img {
  width: 100%;
  cursor: pointer;
  transition: transform 0.2s;
}

.gallery-item img:hover {
  transform: scale(1.05);
}

.modal {
  display: none;
  position: fixed;
  z-index: 9999; /* Ensure the modal is above the header */
  padding-top: 60px;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  overflow: auto;
  background-color: rgba(0, 0, 0, 0.9);
  align-items: center;
  justify-content: center;
}

.close {
  position: absolute;
  top: 80px; /* Position the close button lower, below the header */
  right: 20px;
  color: #f1f1f1;
  font-size: 40px;
  font-weight: bold;
  transition: 0.3s;
  cursor: pointer;
  z-index: 10000; /* Ensure the close button is on top of everything */
}

.close:hover,
.close:focus {
  color: #bbb;
  text-decoration: none;
  cursor: pointer;
}

.modal-content {
  margin: auto;
  display: block;
  width: 80%;
  max-width: 700px;
  position: relative;
}


.modal-content, .close {
  animation-name: zoom;
  animation-duration: 0.6s;
}

@keyframes zoom {
  from {transform: scale(0)} 
  to {transform: scale(1)}
}

.close {
  position: absolute;
  top: 10px;
  right: 10px; /* Position closer to the corner of the image */
  color: #f1f1f1;
  font-size: 40px;
  font-weight: bold;
  transition: 0.3s;
  cursor: pointer;
  z-index: 101; /* Ensure the X is on top */
}

.close:hover,
.close:focus {
  color: #bbb;
  text-decoration: none;
  cursor: pointer;
}

.modal-content {
  position: relative;
}
</style>

<script>
// Get the modal
var modal = document.getElementById("modal");

// Get the image and insert it inside the modal - use its "alt" text as a caption
var modalImg = document.getElementById("modal-img");
document.querySelectorAll('.gallery-item img').forEach(function(img) {
  img.onclick = function(){
    modal.style.display = "block";
    modalImg.src = this.src;
  }
});

// Get the <span> element that closes the modal
var span = document.getElementsByClassName("close")[0];

// When the user clicks on <span> (x), close the modal
span.onclick = function() { 
  modal.style.display = "none";
}
</script>
