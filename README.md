# Valentine
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Will You Be My Valentine?</title>
<style>
  body {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background: pink;
    font-family: Arial, sans-serif;
  }
  #question {
    font-size: 2em;
    margin-bottom: 30px;
    text-align: center;
  }
  .btn {
    padding: 15px 30px;
    font-size: 1.2em;
    margin: 10px;
    cursor: pointer;
    border: none;
    border-radius: 10px;
  }
  #yes { background: #ff4d4d; color: white; }
  #no { background: #4d4dff; color: white; position: relative; }
</style>
</head>
<body>

<div id="question">Will you be my Valentine? 💘</div>
<button id="yes" class="btn">Yes!</button>
<button id="no" class="btn">No...</button>

<script>
const noBtn = document.getElementById("no");

noBtn.addEventListener("mouseover", function() {
  // Random X and Y positions inside the window
  const x = Math.random() * (window.innerWidth - noBtn.clientWidth);
  const y = Math.random() * (window.innerHeight - noBtn.clientHeight);
  noBtn.style.position = "absolute";
  noBtn.style.left = x + "px";
  noBtn.style.top = y + "px";
});

document.getElementById("yes").addEventListener("click", function() {
  alert("Yay! 💖 I knew you’d say Yes!");
});
</script>

</body>
</html>
