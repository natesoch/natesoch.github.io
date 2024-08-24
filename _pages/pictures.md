---
layout: page
title: Pictures
permalink: /pictures/
subtitle: Here are some pictures!
---

<div class="gallery">
  <div class="gallery-item">
    <img src="/assets/img/1.jpg" alt="Description of Picture 1">
    <p>Description of Picture 1.</p>
  </div>
  <div class="gallery-item">
    <img src="/assets/img/2.jpg" alt="Description of Picture 2">
    <p>Description of Picture 2.</p>
  </div>
  <!-- Add more images here -->
</div>

<!-- Modal for expanding images -->
<div id="modal" class="modal">
  <span class="close">&times;</span>
  <img class="modal-content" id="modal-img">
  <div id="caption"></div>
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
  z-index: 100;
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

.modal-content {
  margin: auto;
  display: block;
  width: 80%;
  max-width: 700px;
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
  top: 20px;
  right: 35px;
  color: #f1f1f1;
  font-size: 40px;
  font-weight: bold;
  transition: 0.3s;
  cursor: pointer;
}

.close:hover,
.close:focus {
  color: #bbb;
  text-decoration: none;
  cursor: pointer;
}
</style>

<script>
// Get the modal
var modal = document.getElementById("modal");

// Get the image and insert it inside the modal - use its "alt" text as a caption
var modalImg = document.getElementById("modal-img");
var captionText = document.getElementById("caption");
document.querySelectorAll('.gallery-item img').forEach(function(img) {
  img.onclick = function(){
    modal.style.display = "block";
    modalImg.src = this.src;
    captionText.innerHTML = this.alt;
  }
});

// Get the <span> element that closes the modal
var span = document.getElementsByClassName("close")[0];

// When the user clicks on <span> (x), close the modal
span.onclick = function() { 
  modal.style.display = "none";
}
</script>
