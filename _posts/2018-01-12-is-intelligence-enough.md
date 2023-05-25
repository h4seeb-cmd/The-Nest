---
layout: post
title:  "External Featured Image"
author: sal
categories: [ Jekyll, tutorial, web development ]
image: "https://media.istockphoto.com/id/1076840920/vector/music-background.jpg?s=612x612&w=0&k=20&c=bMG2SEUYaurIHAjtRbw7bmjLsXyT7iJUvAM5HjL3G3I="
---

<!DOCTYPE html>
<html>
<head>
  <title>BeatFlow</title>
  <style>
    body {
      background-color: #45E6FF;
      margin: 0;
      padding: 0;
    }
div.container {
      background-color: #BF8AFF;
    }
.heading1 {
      font-size: 50px;
      text-align: center;
      text-decoration: underline;
      color: #ffffff;
      background-color: #FF1147;
    }
table {
      border-collapse: collapse;
      width: 100%;
    }
th, td {
      text-align: left;
      padding: 8px;
      border: 1px solid #ddd;
    }
th {
      background-color: #FF1147;
    }
.title {
      font-size: 40px;
      text-transform: uppercase;
      text-align: center;
    }
.letter {
      display: inline-block;
      animation: bubbleAnimation 1s ease-in-out infinite;
      animation-duration: 5s;
    }
@keyframes bubbleAnimation {
      0%, 100% {
        transform: translateY(0);
        color: #FF0000;
      }
      50% {
        transform: translateY(-20px);
        color: #00FF00;
      }
    }
  </style>
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/css/bootstrap.min.css" rel="stylesheet"
    integrity="sha384-EVSTQN3/azprG1Anm3QDgpJLIm9Nao0Yz1ztcQTwFspd3yD65VohhpuuCOmLASjC" crossorigin="anonymous">
  <script src="script.js"></script>
</head>
<body>
  <div class="container fullDiv">
    <h1 class="title">
      <span class="letter">🎵</span>
      <span class="letter">B</span>
      <span class="letter">E</span>
      <span class="letter">A</span>
      <span class="letter">T </span>
      <span class="letter"></span>
      <span class="letter">F</span>
      <span class="letter">L</span>
      <span class="letter">O</span>
      <span class="letter">W</span>
      <span class="letter">🎵</span>
    </h1>

<p class="heading1">◁◁ ▐ ▌ ▷▷</p>
    <img class="img-fluid" src="https://images.macrumors.com/t/hi1_a2IdFGRGMsJ0x31SdD_IcRk=/1600x/article-new/2018/05/apple-music-note.jpg">

<div class="container">
      <br>
      <div class="" style="width:100%;">
        <div class="bg-danger" style="width:100%;">
          <h1>◃◃ About Beatflow ◃◃</h1>
        </div>
        <div class="">
          <p>Listen to music anytime and anywhere with Beatflow.</p>
        </div>
        <footer class="bg-warning">
          <h5>.</h5>
        </footer>
      </div>
    </div>

<br />
    <br />

<div class="position-relative">
      <form id="musicform">
        <h4>Please enter the song name and artist:</h4>
        <div class="form-floating">
          <textarea class="form-control" placeholder="Add song name and artist here" id="input"
            style="height: 100px"></textarea>
          <label for="input">Add song name and artist here</label>
        </div>
      </form>
      <button class="btn btn-success position-absolute top-160 start-50 translate-middle" onclick="getInputForPlay()">⭒❃Submit❃⭒</button>
    </div>

<div id="result"></div>

<br />

<!-- Add a new table element to hold the playlist -->
<table id="playlist-table">
      <tr>
        <th>Playlist</th>
      </tr>
    </table>
  </div>

  <script>
    const letters = document.querySelectorAll('.letter');
    let delay = 0;

    letters.forEach(letter => {
      letter.style.animationDelay = `${delay}s`;
      delay += 0.1;
    });
  </script>
</body>
</html>













<html>
<head>
  <title>Music Notes Animation</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css">
  <style>
    body {
      margin: 0;
      padding: 0;
    }

    canvas {
      display: block;
    }
  </style>
</head>
<body>
  <canvas id="canvas"></canvas>

  <script>
    // Create the canvas
    const canvas = document.getElementById('canvas');
    const context = canvas.getContext('2d');
    canvas.width = window.innerWidth;
    canvas.height = window.innerHeight;

    // Array to store the notes
    const notes = [];

    // Function to create a new note
    function createNote() {
      const note = {
        x: Math.random() * canvas.width,
        y: canvas.height,
        speed: Math.random() * 5 + 1,
        size: Math.random() * 20 + 10,
      };

      notes.push(note);
    }

    // Function to update the animation frame
    function update() {
      context.clearRect(0, 0, canvas.width, canvas.height);

      // Create new notes at regular intervals
      if (Math.random() < 0.1) {
        createNote();
      }

      // Move and draw each note
      for (let i = 0; i < notes.length; i++) {
        const note = notes[i];
        note.y -= note.speed;

        // Display music note symbol
        context.font = note.size + 'px Arial';
        context.fillStyle = '#f00';
        context.fillText('♪', note.x, note.y);

        // Remove notes that go offscreen
        if (note.y < -note.size) {
          notes.splice(i, 1);
          i--;
        }
      }

      requestAnimationFrame(update);
    }

    // Start the animation
    update();
  </script>
</body>
</html>