<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Happy Birthday, Phol!</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      padding: 0;
      font-family: Arial, sans-serif;
      background: linear-gradient(to bottom right, #fbe4e6, #cce5ff);
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
      padding: 20px;
    }

    .intro {
      transition: opacity 0.6s ease, visibility 0.6s ease;
    }

    .hidden {
      opacity: 0;
      visibility: hidden;
      position: absolute;
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
      opacity: 0;
      transition: opacity 0.8s ease;
      display: flex;
      flex-direction: column;
      align-items: center;
      width: 100%;
      max-width: 500px;
    }

    .video-container.show {
      opacity: 1;
    }

    video {
      width: 100%;
      border-radius: 12px;
      box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2);
    }

    .next-link {
      margin-top: 20px;
      display: none;
      flex-direction: column;
      align-items: center;
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

    /* Responsive tweaks */
    @media (max-width: 600px) {
      h1 {
        font-size: 1.5rem;
      }

      button {
        font-size: 14px;
        padding: 10px 16px;
      }

      .next-link p,
      .next-link a {
        font-size: 14px;
      }
    }
  </style>
</head>
<body>

  <div class="intro" id="intro">
    <h1>Happy birthday, Phol. Please click this</h1>
    <button id="revealBtn">Click me 🎉</button>
  </div>

  <div class="video-container" id="videoContainer">
    <video id="bdayVideo" controls autoplay>
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
    const intro = document.getElementById('intro');
    const videoContainer = document.getElementById('videoContainer');
    const nextLink = document.getElementById('nextLink');

    revealBtn.addEventListener('click', () => {
      intro.classList.add('hidden');
      videoContainer.classList.add('show');

      setTimeout(() => {
        nextLink.style.display = 'flex';
      }, 2000);
    });
  </script>

</body>
</html>
