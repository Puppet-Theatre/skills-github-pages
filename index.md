  PUPPET THEATRE @import url('https://fonts.googleapis.com/css2?family=Space+Mono:wght@400;700&display=swap'); \* { margin: 0; padding: 0; box-sizing: border-box; } body { font-family: 'Space Mono', monospace; background-color: white; color: black; cursor: default; } .container { width: 100%; max-width: 100vw; height: 100vh; display: grid; grid-template-columns: 1fr 1fr; grid-template-rows: auto 1fr auto; grid-template-areas: "header header" "left-content right-content" "footer footer"; } header { grid-area: header; padding: 1rem; border-bottom: 1px solid black; display: flex; justify-content: space-between; align-items: center; position: relative; } .logo { font-size: 1.5rem; font-weight: bold; text-transform: uppercase; letter-spacing: 2px; } .menu-toggle { font-size: 1rem; text-decoration: underline; cursor: pointer; user-select: none; } .left-content { grid-area: left-content; padding: 2rem; border-right: 1px solid black; overflow-y: auto; } .featured-image { width: 100%; height: 50vh; background-color: #f0f0f0; margin-bottom: 1rem; position: relative; overflow: hidden; } .featured-image img { width: 100%; height: 100%; object-fit: cover; } .right-content { grid-area: right-content; padding: 2rem; overflow-y: auto; } .article-list { display: flex; flex-direction: column; gap: 2rem; } .article-item { border-top: 1px solid black; padding-top: 1rem; } .article-meta { display: flex; justify-content: space-between; margin-bottom: 0.5rem; font-size: 0.8rem; } .article-title { font-size: 1.2rem; margin-bottom: 0.5rem; cursor: pointer; } .article-excerpt { margin-bottom: 1rem; line-height: 1.4; } .read-more { font-size: 0.8rem; text-decoration: underline; cursor: pointer; } footer { grid-area: footer; padding: 1rem; border-top: 1px solid black; display: flex; justify-content: space-between; font-size: 0.8rem; } .footer-links { display: flex; gap: 1rem; } .footer-link { text-decoration: underline; cursor: pointer; } .menu { position: fixed; top: 0; left: 0; width: 100vw; height: 100vh; background-color: black; color: white; display: flex; flex-direction: column; justify-content: center; align-items: center; gap: 2rem; z-index: 10; transition: transform 0.3s ease; transform: translateY(-100%); } .menu.active { transform: translateY(0); } .menu-close { position: absolute; top: 1rem; right: 1rem; font-size: 1rem; cursor: pointer; } .menu-item { font-size: 2rem; cursor: pointer; transition: transform 0.2s ease; } .menu-item:hover { transform: scale(1.1); } .cursor-follower { position: fixed; width: 20px; height: 20px; border-radius: 50%; background-color: rgba(0, 0, 0, 0.5); mix-blend-mode: difference; pointer-events: none; z-index: 9999; transition: transform 0.1s ease; display: none; } @media (max-width: 768px) { .container { grid-template-columns: 1fr; grid-template-areas: "header" "left-content" "right-content" "footer"; } .left-content { border-right: none; border-bottom: 1px solid black; } } /\* Animations \*/ @keyframes fadeIn { from { opacity: 0; } to { opacity: 1; } } .fade-in { animation: fadeIn 1s ease forwards; } .marquee { position: fixed; bottom: 0; left: 0; width: 100%; background-color: black; color: white; padding: 0.5rem 0; white-space: nowrap; overflow: hidden; } .marquee-content { display: inline-block; animation: marquee 15s linear infinite; } @keyframes marquee { 0% { transform: translateX(100%); } 100% { transform: translateX(-100%); } } .puppets-dance { position: fixed; top: 50%; left: 50%; transform: translate(-50%, -50%); width: 100vw; height: 100vh; pointer-events: none; z-index: -1; opacity: 0.1; } .puppet { position: absolute; font-size: 4rem; animation: dance 20s infinite alternate; } @keyframes dance { 0% { transform: translate(0, 0) rotate(0deg); } 25% { transform: translate(100px, 50px) rotate(10deg); } 50% { transform: translate(-50px, 100px) rotate(-20deg); } 75% { transform: translate(-100px, -50px) rotate(15deg); } 100% { transform: translate(50px, -100px) rotate(-5deg); } }

PUPPET THEATRE

MENU

Notes for Ethical Fiction
=========================

Why are you doing that? How can we stop doing that.

By Georgina Montesquieu January 2025

Don’t memorialise the banal. Easy to forget, writing, that there are people, reading, who cannot tease substance out from style. If you allow this to happen you will make the world worse and poorer with each keystroke. Trust that disaffected writers have stripped the vein of its treasure entirely.

On the despondency of so much current literary fiction, and some ways to make it out of that trap.

Read more

By Kuhle Wampe December 2025

THE PURPOSE OF PUPPET THEATRE
-----------------------------

Wilders, Le Pen, Orban, the AFD, the FPO, Meloni, Milei, Farage, Trump and Yoon Suk Yeol. There is a single dominant trend across much of the world: the clamour has obscured the buckling of opposition to the far right.

[Read full article](articles/Editors_comment.html)

By Elena Petrova Spring 2025

AGAINST PUNK
------------

The purpose of the live setting for guitar music is as experiential, as ontological, as it is aesthetic. Otherwise, a vinyl record, or a Spotify playlist, would be indistinguishable from it. On a studio recording the muddy sonics of bigger rooms and the inevitable technical errors of live performance are ironed out in the process known as production. The word used for this process is telling.

Read more

By Smudge Wilcock Spring 2025

NEIGHBOURS
----------

This house is changing. She's mapped the contours

Read more

© 2025 PUPPET THEATRE Magazine

Subscribe

Archive

Contact

✕

CURRENT ISSUE

ARCHIVE

FEATURES

INTERVIEWS

EVENTS

SUBSCRIBE

ABOUT

PUPPET THEATRE MAGAZINE — MAY 2025 ISSUE — ROSS THURBER — DONA FERENTES — QUENTIN TARANTINO — IQUITA GAUDIER-MUYS — MAY 2025 ISSUE —

🎭

🎪

🎨

🎯

// Menu toggle functionality const menuToggle = document.getElementById('menuToggle'); const menu = document.getElementById('menu'); const menuClose = document.getElementById('menuClose'); menuToggle.addEventListener('click', () => { menu.classList.add('active'); }); menuClose.addEventListener('click', () => { menu.classList.remove('active'); }); // Custom cursor const cursorFollower = document.querySelector('.cursor-follower'); document.addEventListener('mousemove', (e) => { cursorFollower.style.display = 'block'; cursorFollower.style.transform = \`translate(${e.clientX - 10}px, ${e.clientY - 10}px)\`; }); // Hover effect for menu items and article titles const menuItems = document.querySelectorAll('.menu-item'); const articleTitles = document.querySelectorAll('.article-title'); \[...menuItems, ...articleTitles\].forEach(item => { item.addEventListener('mouseenter', () => { cursorFollower.style.transform = \`translate(${parseFloat(cursorFollower.style.transform.split('(')\[1\]) - 5}px, ${parseFloat(cursorFollower.style.transform.split(',')\[1\]) - 5}px) scale(2)\`; }); item.addEventListener('mouseleave', () => { cursorFollower.style.transform = \`translate(${parseFloat(cursorFollower.style.transform.split('(')\[1\]) - 5}px, ${parseFloat(cursorFollower.style.transform.split(',')\[1\]) - 5}px) scale(1)\`; }); }); // Randomized element positions on load document.addEventListener('DOMContentLoaded', () => { const articleItems = document.querySelectorAll('.article-item'); articleItems.forEach((item, index) => { item.style.opacity = '0'; setTimeout(() => { item.classList.add('fade-in'); }, 300 \* index); }); }); // Make puppets move independently const puppets = document.querySelectorAll('.puppet'); puppets.forEach((puppet, index) => { puppet.style.animationDelay = \`${index \* 2}s\`; });
