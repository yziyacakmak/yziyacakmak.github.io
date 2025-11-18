---
layout: about
title: about
permalink: /
subtitle:

profile:
  align: right
  image: prof_pic.jpg
  image_circular: false # crops the image to make it circular
  more_info: >
    <p>A nice day in Washington D.C.</p>
    <p>
      <a href="https://github.com/yziyacakmak" target="_blank"><i class="fab fa-github"></i> GitHub</a><br>
      <a href="mailto:yusufzcakmakl@gmail.com"><i class="fas fa-envelope"></i> Contact Me</a>
    </p>
    <style>
      body {
          font-family: 'Inter', sans-serif;
          background-color: #1a1a1a;
          color: #fff;
          display: flex;
          flex-direction: column;
          align-items: center;
          justify-content: center;
          min-height: 100vh;
          margin: 0;
      }
      a {
          color: #fff;
          text-decoration: none;
          font-size: 18px;
          margin: 8px;
      }
      a:hover {
          color: #5F65AC;
          text-decoration: underline;
      }
      .social-links {
          display: flex;
          gap: 20px;
          margin-bottom: 20px;
          flex-wrap: wrap;
          justify-content: center;
      }
      .surprise-button {
          padding: 12px 24px;
          background: #5F65AC;
          color: #fff;
          border-radius: 8px;
          cursor: pointer;
          font-size: 15px;
          border: none;
          transition: transform 0.2s ease, background-color 0.2s ease;
          margin-bottom: 20px;
      }
      .surprise-button:hover {
          transform: scale(1.05);
          background-color: #4b4fa0;
      }

      #catEasterEgg {
          position: fixed;
          top: 50%;
          left: 50%;
          transform: translate(-50%, -50%) scale(0.8);
          background: #5F65AC;
          padding: 20px;
          border-radius: 12px;
          display: none;
          text-align: center;
          z-index: 1000;
          color: #fff;
          box-shadow: 0 8px 24px rgba(0,0,0,0.3);
          transition: all 0.3s ease;
          opacity: 0;
      }

      #catEasterEgg.show {
          display: block;
          opacity: 1;
          transform: translate(-50%, -50%) scale(1);
      }

      #catEasterEgg img {
          max-width: 300px;
          border-radius: 8px;
          margin-top: 10px;
      }

      #catEasterEgg p {
          margin: 0;
          font-size: 16px;
      }
    </style>
    <button class="surprise-button" id="surpriseTrigger">Click for a surprise! 🎁</button>
    <div id="catEasterEgg">
      <p>You found a secret cat! 🐱</p>
      <img src="https://thecatapi.com/api/images/get?format=src&type=gif">
    </div>
    <script>
      const surpriseTrigger = document.getElementById('surpriseTrigger');
      const catEgg = document.getElementById('catEasterEgg');

      surpriseTrigger.onclick = function(e) {
          e.stopPropagation();
          catEgg.classList.add('show');

          // Refresh GIF to get a new random cat
          const img = catEgg.querySelector('img');
          img.src = `https://thecatapi.com/api/images/get?format=src&type=gif&timestamp=${new Date().getTime()}`;
      }

      window.onclick = function(e) {
          if (catEgg.classList.contains('show') && !catEgg.contains(e.target) && e.target !== surpriseTrigger) {
              catEgg.classList.remove('show');
          }
      }
    </script>



selected_papers: false # includes a list of papers marked as "selected={true}"
social: false # includes social icons at the bottom of the page

announcements:
  enabled: false # includes a list of news items
  scrollable: true # adds a vertical scroll bar if there are more than 3 news items
  limit: 5 # leave blank to include all the news in the `_news` folder

latest_posts:
  enabled: false
  scrollable: true # adds a vertical scroll bar if there are more than 3 new posts items
  limit: 3 # leave blank to include all the blog posts
---

I am a software engineer at Saykal Electronics, specializing in user interface design and development for automotive embedded systems. Recently, I've grown interested in building high-performance web applications using modern technologies like WebAssembly, particularly exploring how these approaches deliver native-like speed. I see this shift as an opportunity to make application deployment and updates significantly more efficient. I'm also passionate about automotive cybersecurity and secure software update mechanisms.

Beyond my day-to-day work, I enjoy diving into the technical depths of C# programming, studying topics like garbage collection internals and source generators. When I'm not coding, I'm an enthusiast of Turkish classical music and play the [ney](https://en.wikipedia.org/wiki/Ney) as a hobby.



