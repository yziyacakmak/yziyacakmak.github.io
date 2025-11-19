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
      <a href="https://www.linkedin.com/in/yziyacakmak" target="_blank"><i class="fab fa-linkedin"></i> LinkedIn </a><br>
      <a href="https://github.com/yziyacakmak" target="_blank"><i class="fab fa-github"></i> GitHub</a><br>
      <a href="mailto:yusufzcakmak@gmail.com"><i class="fas fa-envelope"></i> Contact Me</a>

    </p>
    <style>
      .profile a {
          text-decoration: none;
          font-size: 18px;
          margin: 8px;
      }
      .profile a:hover {
          color: #5F65AC;
          text-decoration: underline;
      }
      .profile .surprise-button {
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
      .profile .surprise-button:hover {
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
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 10px;
        text-align: center;
        z-index: 1000;
        color: #fff;
        box-shadow: 0 8px 24px rgba(0,0,0,0.3);
        transition: all 0.3s ease;
        opacity: 0;
        pointer-events: none;
      }

      #catEasterEgg.show {
          opacity: 1;
          transform: translate(-50%, -50%) scale(1);
          pointer-events: auto;
      }

      #catEasterEgg img {
        max-width: 300px;
        border-radius: 8px;
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

I am a software engineer at Saykal Electronics, specializing in user interface design and development for automotive embedded systems. Recently, I've grown interested in building high-performance web applications using WebAssembly, particularly exploring how these approaches deliver native-like speed. I see this shift as an opportunity to make application deployment and updates significantly more efficient. I'm also passionate about automotive cybersecurity and secure software update mechanisms.

Beyond my day-to-day work, I enjoy diving into the technical depths of C# programming, studying topics like garbage collection internals and source generators. When I'm not coding, I'm an enthusiast of Turkish classical music and play the [ney](https://en.wikipedia.org/wiki/Ney) as a hobby.



