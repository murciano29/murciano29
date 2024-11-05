- 👋 Hi, I’m @murciano29
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
murciano29/murciano29 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
---><html><head><base href="." /><meta charset="UTF-8" /><meta name="viewport" content="width=device-width, initial-scale=1.0" />
<meta name="mobile-web-app-capable" content="yes" />
<meta name="apple-mobile-web-app-capable" content="yes" />
<meta name="apple-mobile-web-app-status-bar-style" content="black-translucent" />
<meta name="theme-color" content="#4a90e2" />
<title>Fortune Cookie App</title>
<link rel="manifest" href="data:application/json;base64,ewogICJuYW1lIjogIkZvcnR1bmUgQ29va2llIEFwcCIsCiAgInNob3J0X25hbWUiOiAiRm9ydHVuZSIsCiAgInN0YXJ0X3VybCI6ICIuIiwKICAiZGlzcGxheSI6ICJzdGFuZGFsb25lIiwKICAiYmFja2dyb3VuZF9jb2xvciI6ICIjNGE5MGUyIiwKICAidGhlbWVfY29sb3IiOiAiIzRhOTBlMiIsCiAgImljb25zIjogW3sKICAgICJzcmMiOiAiZGF0YTppbWFnZS9zdmcreG1sLCUzQ3N2ZyB4bWxucz0naHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmcnIHZpZXdCb3g9JzAgMCAxMDAgMTAwJyUzRSUzQ3BhdGggZD0nTTUwLDEwIEM3MCwxMCA4NSwyNSA4NSw0NSBDODUsNjUgNzAsODAgNTAsODAgQzMwLDgwIDE1LDY1IDE1LDQ1IEMxNSwyNSAzMCwxMCA1MCwxMCcgZmlsbD0nJTIzZmZhNTAyJy8lM0UlM0Mvc3ZnJTNFIiwKICAgICJzaXplcyI6ICIxNDR4MTQ0IiwKICAgICJ0eXBlIjogImltYWdlL3N2ZyIKICB9XQp9" />
<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Arial', sans-serif;
    background: linear-gradient(135deg, #4a90e2, #6351ce);
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    color: white;
}

.container {
    padding: 20px;
    text-align: center;
    max-width: 400px;
    width: 100%;
    margin-top: 60px;
}

.counter {
    font-size: 3rem;
    margin: 40px 0;
}

.cookie {
    width: 200px;
    height: 200px;
    margin: 30px auto;
    cursor: pointer;
    transition: transform 0.3s ease;
    filter: drop-shadow(0 0 10px rgba(0,0,0,0.3));
}

.cookie:hover {
    transform: scale(1.1);
}

.button {
    background: #ffa502;
    color: white;
    border: none;
    padding: 15px 30px;
    border-radius: 25px;
    font-size: 1.1rem;
    cursor: pointer;
    transition: background 0.3s ease;
    margin: 20px 0;
}

.button:hover {
    background: #ff9f00;
}

.nav-bar {
    position: fixed;
    bottom: 0;
    width: 100%;
    background: rgba(255, 255, 255, 0.1);
    backdrop-filter: blur(10px);
    padding: 15px;
    display: flex;
    justify-content: space-around;
    border-top: 1px solid rgba(255, 255, 255, 0.1);
}

.nav-item {
    color: white;
    text-decoration: none;
    font-size: 1.2rem;
}

.sparkle {
    position: absolute;
    pointer-events: none;
}

.modal {
    display: none;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0.5);
    justify-content: center;
    align-items: center;
    z-index: 1000;
}

.modal-content {
    background: white;
    padding: 20px;
    border-radius: 10px;
    width: 90%;
    max-width: 300px;
    text-align: center;
}

.modal-content input {
    width: 100%;
    padding: 10px;
    margin: 10px 0;
    border: 1px solid #ccc;
    border-radius: 5px;
}

.modal-content button {
    background: #ffa502;
    color: white;
    border: none;
    padding: 10px 20px;
    border-radius: 5px;
    cursor: pointer;
    margin: 5px;
}

.modal-content h2 {
    color: #333;
    margin-bottom: 15px;
}

.username-display {
    position: fixed;
    top: 20px;
    left: 50%;
    transform: translateX(-50%);
    background: rgba(255, 255, 255, 0.1);
    backdrop-filter: blur(5px);
    padding: 10px 20px;
    border-radius: 20px;
    display: flex;
    align-items: center;
    gap: 8px;
    font-size: 1.2rem;
    z-index: 100;
}

.username-display .emoji {
    font-size: 1.4rem;
}

@media (hover: none) {
    .cookie:hover {
        transform: none;
    }
    
    .button:hover {
        background: #ffa502;
    }
}

@supports (-webkit-touch-callout: none) {
    .container {
        padding-bottom: 100px;
    }
    
    .nav-bar {
        padding-bottom: calc(15px + env(safe-area-inset-bottom));
    }
}

.no-select {
    -webkit-touch-callout: none;
    -webkit-user-select: none;
    -khtml-user-select: none;
    -moz-user-select: none;
    -ms-user-select: none;
    user-select: none;
    -webkit-tap-highlight-color: transparent;
}
</style>
</head>
<body class="no-select">
    <div id="usernameDisplay" class="username-display" style="display: none">
        <span class="emoji">😊</span>
        <span id="usernameText"></span>
    </div>

    <div class="container">
        <div class="counter">2,214</div>
        
        <svg class="cookie" viewBox="0 0 100 100">
            <path d="M50,10 
                     C70,10 85,25 85,45 
                     C85,65 70,80 50,80 
                     C30,80 15,65 15,45 
                     C15,25 30,10 50,10" 
                  fill="#ffa502"/>
            <path d="M40,45 L60,45" 
                  stroke="white" 
                  stroke-width="2"/>
        </svg>

        <button class="button">GET A PREDICTION</button>
    </div>

    <div class="modal" id="usernameModal">
        <div class="modal-content">
            <h2>Change Username</h2>
            <input type="text" id="usernameInput" placeholder="Enter new username">
            <button onclick="saveUsername()">Save</button>
            <button onclick="closeModal()">Cancel</button>
        </div>
    </div>

    <nav class="nav-bar">
        <a href="javascript:void(0)" class="nav-item" onclick="showUsernameModal()">🏠</a>
        <a href="javascript:void(0)" class="nav-item">📊</a>
        <a href="javascript:void(0)" class="nav-item">📤</a>
        <a href="javascript:void(0)" class="nav-item">👤</a>
    </nav>

<script>
const cookie = document.querySelector('.cookie');
const button = document.querySelector('.button');
const counter = document.querySelector('.counter');
const modal = document.getElementById('usernameModal');
let count = 2214;

function createSparkle() {
    const sparkle = document.createElement('div');
    sparkle.className = 'sparkle';
    sparkle.style.left = Math.random() * window.innerWidth + 'px';
    sparkle.style.top = Math.random() * window.innerHeight + 'px';
    sparkle.style.transform = `scale(${Math.random()})`;
    sparkle.innerHTML = '✨';
    document.body.appendChild(sparkle);
    
    setTimeout(() => sparkle.remove(), 1000);
}

function animateCookie() {
    cookie.style.transform = 'scale(0.9)';
    setTimeout(() => {
        cookie.style.transform = 'scale(1)';
    }, 150);
    
    for(let i = 0; i < 5; i++) {
        setTimeout(createSparkle, i * 100);
    }
    
    count++;
    counter.textContent = count.toLocaleString();
}

function showUsernameModal() {
    modal.style.display = 'flex';
}

function closeModal() {
    modal.style.display = 'none';
}

function saveUsername() {
    const username = document.getElementById('usernameInput').value;
    if (username.trim() !== '') {
        localStorage.setItem('username', username);
        updateUsernameDisplay(username);
        closeModal();
    }
}

function updateUsernameDisplay(username) {
    const display = document.getElementById('usernameDisplay');
    const usernameText = document.getElementById('usernameText');
    usernameText.textContent = username;
    display.style.display = 'flex';
}

// Load username on page load
window.addEventListener('load', () => {
    const savedUsername = localStorage.getItem('username');
    if (savedUsername) {
        updateUsernameDisplay(savedUsername);
    }
});

button.addEventListener('click', animateCookie);
cookie.addEventListener('click', animateCookie);

// Add touch events for mobile
cookie.addEventListener('touchstart', (e) => {
    e.preventDefault();
    animateCookie();
});

button.addEventListener('touchstart', (e) => {
    e.preventDefault();
    animateCookie();
});

// Simple animation loop for the cookie
function animate() {
    requestAnimationFrame(animate);
    const time = Date.now() / 1000;
    const scale = 1 + Math.sin(time) * 0.03;
    if (!cookie.style.transform.includes('scale(0.9)')) {
        cookie.style.transform = `scale(${scale})`;
    }
}

// Close modal when clicking outside
modal.addEventListener('click', (e) => {
    if (e.target === modal) {
        closeModal();
    }
});

// Prevent double-tap zoom on mobile
document.addEventListener('touchend', (e) => {
    e.preventDefault();
    e.target.click();
}, false);

// Handle iOS PWA status bar
if (window.navigator.standalone) {
    document.body.style.paddingTop = '20px';
}

// Prevent scrolling when modal is open
modal.addEventListener('touchmove', (e) => {
    e.preventDefault();
}, { passive: false });

// Add passive event listeners for better scrolling performance
document.addEventListener('touchstart', () => {}, { passive: true });
document.addEventListener('touchmove', () => {}, { passive: true });

// Handle visibility change for mobile browsers
document.addEventListener('visibilitychange', () => {
    if (document.visibilityState === 'visible') {
        requestAnimationFrame(animate);
    }
});

animate();
</script>
</body></html>
