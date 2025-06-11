<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Happy Birthday, Phol!</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: Arial, sans-serif;
      background: linear-gradient(to bottom right, #fbe4e6, #cce5ff);
      height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
    }

    h1 {
      font-size: 2rem;
      margin-bottom: 20px;
      color: #333;
    }

    button {
      background-color: #ff82a9;
      color: white;
      border: none;
      padding: 12px 20px;
      border-radius: 10px;
      font-size: 16px;
      cursor: pointer;
      transition: background-color 0.3s ease;
    }

    button:hover {
      background-color: #ff5d90;
    }

    .video-container {
      display: none;
      margin-top: 30px;
    }

    video {
      border-radius: 12px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.2);
    }

    .next-link {
      margin-top: 20px;
      display: none;
    }

    .next-link p {
      font-size: 16px;
      color: #444;
      margin-bottom: 10px;
    }

    .next-link a {
      font-weight: bold;
      color: #0066cc;
      text-decoration: underline;
      font-size: 16px;
    }
  </style>
</head>
<body>

  <h1>Happy birthday, Phol. Please click this</h1>
  <button id="revealBtn">Click me 🎉</button>

  <div class="video-container" id="videoContainer">
    <video id="bdayVideo" width="480" controls autoplay>
      <source src="phol-video.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>

    <div class="next-link" id="nextLink">
      <p>pls click this too</p>
      <a href="https://postimg.cc/5QJHL5jh" target="_blank">Click here</a>
    </div>
  </div>

  <script>
    const revealBtn = document.getElementById('revealBtn');
    const videoContainer = document.getElementById('videoContainer');
    const nextLink = document.getElementById('nextLink');

    revealBtn.addEventListener('click', () => {
      videoContainer.style.display = 'block';
      revealBtn.style.display = 'none';

      setTimeout(() => {
        nextLink.style.display = 'block';
      }, 2000); // show "pls click this too" after 2 seconds
    });
  </script>

</body>
</html>
