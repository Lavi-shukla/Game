# Game<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Simple Space Game</title>
<style>
  canvas {
    background: black;
    display: block;
    margin: 0 auto;
  }
</style>
</head>
<body>
<canvas id="gameCanvas" width="480" height="320"></canvas>
<script>
  const canvas = document.getElementById('gameCanvas');
  const ctx = canvas.getContext('2d');

  let shipX = canvas.width / 2 - 15;
  const shipWidth = 30;
  const shipHeight = 15;
  const shipSpeed = 5;

  let rightPressed = false;
  let leftPressed = false;

  let bullets = [];

  document.addEventListener("keydown", keyDownHandler, false);
  document.addEventListener("keyup", keyUpHandler, false);

  function keyDownHandler(e) {
    if(e.key === "Right" || e.key === "ArrowRight") {
      rightPressed =
      
