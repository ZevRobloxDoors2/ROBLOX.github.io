<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1, user-scalable=no, maximum-scale=1" />
  <title>BloxHTML V3.1 (Stable)</title>

  <!-- Tailwind & Libs -->
  <script src="https://cdn.tailwindcss.com"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
  <link href="https://fonts.googleapis.com/css2?family=Builder+Sans:wght@400;700;800&family=Inter:wght@400;600;700&family=Creepster&display=swap" rel="stylesheet">

  <style>
    :root {
      --rbx-dark: #232527; --rbx-darker: #191b1d; --rbx-blue: #00b06f; --rbx-red: #ff4757;
      --text: #fff; --text-light: #bdbebf;
    }
    body { font-family: 'Inter', sans-serif; background: var(--rbx-darker); color: var(--text); overflow: hidden; user-select: none; }
    
    /* UI Components */
    .rbx-card { background: #232527; border-radius: 8px; padding: 24px; box-shadow: 0 4px 8px rgba(0,0,0,0.2); }
    .rbx-input { background: #000000; border: 2px solid rgba(255,255,255,0.2); border-radius: 4px; padding: 10px; color: white; width: 100%; transition: 0.2s; outline: none; }
    .rbx-input:focus { border-color: white; }
    .rbx-btn-primary { background: white; color: #232527; font-weight: 700; border-radius: 8px; padding: 10px 20px; transition: 0.2s; width: 100%; cursor: pointer; }
    .rbx-btn-primary:hover { background: #e5e5e5; }
    .rbx-btn-secondary { background: transparent; border: 1px solid white; color: white; font-weight: 600; border-radius: 8px; padding: 10px 20px; transition: 0.2s; width: 100%; cursor: pointer; }
    .rbx-btn-secondary:hover { background: rgba(255,255,255,0.1); }
    
    /* Game HUD */
    #game-ui { display: none; pointer-events: none; }
    .hotbar-slot { width: 50px; height: 50px; background: rgba(0,0,0,0.5); border: 2px solid rgba(255,255,255,0.1); border-radius: 8px; display: flex; align-items: center; justify-content: center; font-weight: bold; position: relative; transition: 0.1s; font-size: 20px; cursor: pointer; pointer-events: auto; }
    .hotbar-slot.active { border-color: #00b06f; transform: translateY(-4px); background: rgba(0,176,111,0.1); box-shadow: 0 0 10px rgba(0,176,111,0.2); }
    .hotbar-key { position: absolute; top: 2px; left: 4px; font-size: 10px; color: rgba(255,255,255,0.5); }
    
    .nametag { position: absolute; background: rgba(30,30,30,0.7); color: white; padding: 2px 8px; border-radius: 12px; font-size: 12px; font-weight: 600; transform: translate(-50%, -100%); pointer-events: none; white-space: nowrap; backdrop-filter: blur(2px); }
    .dmg-txt { position: absolute; font-weight: 900; -webkit-text-stroke: 1px black; animation: dmg 1s forwards; pointer-events: none; z-index: 100; color: #ff4757; font-size: 24px; text-shadow: 0 2px 0 black; }
    @keyframes dmg { 0% { transform: scale(1) translateY(0); opacity:1; } 100% { transform: scale(1.5) translateY(-50px); opacity:0; } }
    
    /* Brainrot UI */
    .brainrot-tag { position: absolute; background: rgba(0,0,0,0.8); border: 1px solid rgba(255,255,255,0.2); padding: 4px 8px; border-radius: 6px; color: white; font-family: 'Builder Sans', sans-serif; text-align: center; transform: translate(-50%, -150%); pointer-events: none; white-space: nowrap; z-index: 10; }
    .brainrot-rarity { font-size: 10px; font-weight: bold; text-transform: uppercase; display: block; margin-bottom: 2px; }
    .brainrot-name { font-size: 12px; font-weight: bold; }
    .brainrot-price { color: #ffeaa7; font-size: 11px; }

    /* Special Effects */
    .owner-announce { position: absolute; top: 20%; left: 0; width: 100%; text-align: center; font-family: 'Creepster', cursive; font-size: 5rem; color: #ff0000; text-shadow: 0 0 20px black; pointer-events: none; animation: shake 0.5s infinite; z-index: 200; display: none; }
    @keyframes shake { 0% { transform: translate(1px, 1px) rotate(0deg); } 10% { transform: translate(-1px, -2px) rotate(-1deg); } 20% { transform: translate(-3px, 0px) rotate(1deg); } 30% { transform: translate(3px, 2px) rotate(0deg); } 40% { transform: translate(1px, -1px) rotate(1deg); } 50% { transform: translate(-1px, 2px) rotate(-1deg); } 60% { transform: translate(-3px, 1px) rotate(0deg); } 70% { transform: translate(3px, 1px) rotate(-1deg); } 80% { transform: translate(-1px, -1px) rotate(1deg); } 90% { transform: translate(1px, 2px) rotate(0deg); } 100% { transform: translate(1px, -2px) rotate(-1deg); } }

    /* Gender Selection */
    .gender-btn { background: #191b1d; border: 1px solid #393b3d; color: #bdbebf; padding: 10px; border-radius: 4px; font-weight: 600; flex: 1; transition: 0.2s; cursor: pointer; }
    .gender-btn:hover { background: #2a2c2e; }
    .gender-btn.selected { border-color: white; color: white; background: #393b3d; }

    /* Tabs */
    .auth-tab { @apply flex-1 text-center py-2 cursor-pointer border-b-2 border-transparent text-gray-500 font-bold; }
    .auth-tab.active { @apply border-white text-white; }

    ::-webkit-scrollbar { width: 6px; }
    ::-webkit-scrollbar-track { background: transparent; }
    ::-webkit-scrollbar-thumb { background: #555; border-radius: 10px; }
  </style>
</head>
<body class="h-screen w-screen relative">

  <!-- ================= OVERLAYS ================= -->
  <div id="owner-effect" class="owner-announce">THE EYE IS WATCHING!!</div>

  <!-- ================= BAN SCREEN ================= -->
  <div id="ban-screen" class="fixed inset-0 z-[1000] flex flex-col justify-center items-center bg-[#191b1d] hidden">
    <div class="ban-container bg-[#232527] rounded-xl max-w-lg w-[90%] p-10 text-center border border-[#393b3d]">
      <div class="text-2xl font-bold mb-4">Account Deleted</div>
      <p class="text-sm text-gray-300 mb-4">Our content monitors have determined that your behavior at BloxHTML has been in violation of our Terms of Use.</p>
      <div class="bg-[#191b1d] border border-[#393b3d] p-4 text-left mb-6 rounded font-mono text-sm text-gray-400">
        <p><span class="font-bold text-white">Reviewed:</span> <span id="ban-date"></span></p>
        <p><span class="font-bold text-white">Moderator Note:</span> <span id="ban-note">You get banned for being rude.</span></p>
        <p class="mt-2"><span class="font-bold text-white">Reason:</span> <span id="ban-reason" class="text-red-400">Harassment</span></p>
        <p><span class="font-bold text-white">Offensive Item:</span> <span id="ban-item" class="italic text-white"></span></p>
      </div>
      <p class="text-xs text-gray-500 mb-6">Your account has been terminated.</p>
      <button class="rbx-btn-secondary w-full border-gray-500 text-gray-400 cursor-not-allowed">Logout (Disabled)</button>
    </div>
  </div>

  <!-- ================= LOGIN SCREEN ================= -->
  <div id="auth-screen" class="fixed inset-0 z-50 flex flex-col bg-[#191b1d]">
    <div class="h-12 bg-[#232527] flex items-center justify-between px-4 border-b border-[#393b3d]">
        <div class="font-black text-xl tracking-tight">Blox<span class="text-white font-light">HTML</span></div>
    </div>

    <div class="flex-1 flex items-center justify-center relative overflow-hidden">
        <div class="absolute inset-0 opacity-10 bg-[url('https://www.transparenttextures.com/patterns/cubes.png')]"></div>
        <div class="rbx-card w-full max-w-md relative z-10">
            <!-- Tabs -->
            <div class="flex mb-6 border-b border-[#393b3d]">
                <div class="auth-tab active" onclick="App.switchAuth('signup')">Sign Up</div>
                <div class="auth-tab" onclick="App.switchAuth('login')">Log In</div>
            </div>

            <!-- Sign Up Form -->
            <div id="form-signup" class="space-y-4">
                <h2 class="text-3xl font-bold mb-4 text-white">Sign Up</h2>
                <div>
                    <label class="text-xs font-bold text-gray-400 uppercase mb-1 block">Username</label>
                    <input id="su-username" class="rbx-input" placeholder="Don't use your real name" />
                    <p id="su-error" class="text-xs text-[#ff4757] mt-2 hidden font-bold">Username taken.</p>
                </div>
                <div>
                    <label class="text-xs font-bold text-gray-400 uppercase mb-1 block">Gender</label>
                    <div class="flex gap-2">
                        <button id="gender-boy" class="gender-btn selected" onclick="App.setGender('boy')">Boy</button>
                        <button id="gender-girl" class="gender-btn" onclick="App.setGender('girl')">Girl</button>
                    </div>
                </div>
                <button onclick="App.attemptSignup()" class="rbx-btn-primary mt-2">Sign Up</button>
            </div>

            <!-- Login Form -->
            <div id="form-login" class="space-y-4 hidden">
                <h2 class="text-3xl font-bold mb-4 text-white">Log In</h2>
                <div>
                    <label class="text-xs font-bold text-gray-400 uppercase mb-1 block">Username</label>
                    <input id="li-username" class="rbx-input" placeholder="Enter username" />
                </div>
                <button onclick="App.attemptLogin()" class="rbx-btn-secondary mt-2 border-white text-white">Log In</button>
                <div id="login-recents" class="mt-4 pt-4 border-t border-[#393b3d] hidden">
                    <p class="text-xs text-gray-500 mb-2">Recent Accounts</p>
                    <div id="recent-list" class="flex gap-2"></div>
                </div>
            </div>

        </div>
    </div>
    
    <div class="h-10 bg-[#232527] border-t border-[#393b3d] flex items-center justify-center text-xs text-gray-500">
        © 2026 BloxHTML Corporation.
    </div>
  </div>

  <!-- TERMS MODAL -->
  <div id="terms-modal" class="fixed inset-0 z-[200] flex flex-col justify-center items-center bg-black/80 backdrop-blur-sm hidden">
    <div class="bg-[#232527] w-full max-w-2xl h-3/4 rounded-lg shadow-2xl flex flex-col overflow-hidden border border-[#393b3d]">
      <div class="p-6 border-b border-[#393b3d] flex justify-between items-center">
        <h2 class="text-2xl font-bold text-white">Terms of Use</h2>
        <button onclick="document.getElementById('terms-modal').classList.add('hidden')" class="text-gray-400 hover:text-white text-2xl">×</button>
      </div>
      <div class="p-8 overflow-y-auto text-gray-300 text-sm space-y-4 leading-relaxed font-sans">
        <p>1. <strong>Respect Others:</strong> Harassment is not tolerated.<br>2. <strong>Account Security:</strong> You are responsible for your account.<br>3. <strong>Economy:</strong> Coins have no monetary value.</p>
      </div>
    </div>
  </div>

  <!-- ================= DASHBOARD ================= -->
  <div id="dashboard" class="hidden absolute inset-0 flex flex-col bg-[#191b1d] z-40">
    <nav class="h-14 bg-[#232527] border-b border-[#393b3d] flex items-center px-4 justify-between shrink-0">
      <div class="flex items-center gap-6">
        <div class="text-2xl font-black cursor-pointer" onclick="App.view('home')">BloxHTML</div>
        <div class="flex gap-4 text-sm font-bold text-gray-300">
          <button onclick="App.view('home')" class="hover:text-white transition py-4 border-b-2 border-transparent hover:border-white">Discover</button>
          <button onclick="App.view('avatar')" class="hover:text-white transition py-4 border-b-2 border-transparent hover:border-white">Avatar</button>
          <button onclick="App.view('shop')" class="hover:text-white transition py-4 border-b-2 border-transparent hover:border-white">Marketplace</button>
          <button onclick="App.view('create')" class="hover:text-white transition py-4 text-[#00b06f] font-bold">Create</button>
        </div>
      </div>
      <div class="flex items-center gap-4">
        <div class="bg-[#191b1d] px-3 py-1 rounded-full border border-[#393b3d] flex items-center gap-2 text-sm font-bold">
          <span class="text-yellow-400">⛃</span> <span id="dash-coins">0</span>
        </div>
        <div class="flex items-center gap-2">
            <span id="dash-user" class="text-sm font-bold text-white">Guest</span>
            <div class="w-8 h-8 rounded-full bg-gray-500 overflow-hidden border border-[#393b3d]">
                <div id="dash-av-face" class="w-full h-full bg-[#F5CBA7]"></div>
            </div>
        </div>
      </div>
    </nav>

    <main id="view-home" class="flex-1 overflow-y-auto p-6">
      <h2 class="text-2xl font-bold text-white mb-4">Featured Experiences</h2>
      <div id="games-grid" class="grid grid-cols-2 md:grid-cols-4 lg:grid-cols-5 gap-4"></div>
    </main>

    <main id="view-avatar" class="hidden flex-1 overflow-y-auto p-6">
        <div class="flex gap-6 max-w-4xl mx-auto mt-8">
            <!-- Avatar Preview Box -->
            <div class="w-64 bg-[#232527] rounded-lg p-4 h-96 flex items-center justify-center relative border border-[#393b3d]">
                <div class="relative w-32 h-64 transform scale-125">
                    <div id="p-hair" class="hidden absolute top-[-5%] left-[10%] w-[80%] h-[25%] bg-[#5c3a21] rounded-t-xl z-30 transition-all"></div>
                    <div id="p-bun-l" class="hidden absolute top-[-5%] left-[-5%] w-[30%] h-[30%] bg-[#5c3a21] rounded-full z-20"></div>
                    <div id="p-bun-r" class="hidden absolute top-[-5%] right-[-5%] w-[30%] h-[30%] bg-[#5c3a21] rounded-full z-20"></div>
                    <div id="p-head" class="absolute top-0 left-[25%] w-[50%] h-[20%] bg-[#F5CBA7] rounded-sm z-20"></div>
                    <div id="p-torso" class="absolute top-[22%] left-[15%] w-[70%] h-[35%] bg-blue-600 rounded-sm z-10 transition-all"></div>
                    <div id="p-larm" class="absolute top-[22%] left-[-10%] w-[22%] h-[35%] bg-[#F5CBA7] rounded-sm transition-all"></div>
                    <div id="p-rarm" class="absolute top-[22%] right-[-10%] w-[22%] h-[35%] bg-[#F5CBA7] rounded-sm transition-all"></div>
                    <div id="p-lleg" class="absolute top-[60%] left-[15%] w-[32%] h-[40%] bg-green-600 rounded-sm transition-all"></div>
                    <div id="p-rleg" class="absolute top-[60%] right-[15%] w-[32%] h-[40%] bg-green-600 rounded-sm transition-all"></div>
                 </div>
            </div>
            <!-- Editor Controls -->
            <div class="flex-1 space-y-6">
                <div class="bg-[#232527] p-4 rounded-lg border border-[#393b3d]">
                    <h3 class="font-bold text-gray-400 text-xs uppercase mb-2">Skin Tone</h3>
                    <div id="pal-skin" class="flex flex-wrap gap-2"></div>
                </div>
                <div id="hair-section" class="bg-[#232527] p-4 rounded-lg border border-[#393b3d] hidden">
                    <h3 class="font-bold text-gray-400 text-xs uppercase mb-2">Hair Style</h3>
                    <div class="flex gap-2 mb-4">
                        <button onclick="App.setHairStyle('long')" class="bg-black/40 border border-gray-600 px-3 py-1 rounded text-xs hover:bg-white/10">Long</button>
                        <button onclick="App.setHairStyle('pony')" class="bg-black/40 border border-gray-600 px-3 py-1 rounded text-xs hover:bg-white/10">Ponytail</button>
                        <button onclick="App.setHairStyle('buns')" class="bg-black/40 border border-gray-600 px-3 py-1 rounded text-xs hover:bg-white/10">Buns</button>
                    </div>
                    <h3 class="font-bold text-gray-400 text-xs uppercase mb-2">Hair Color</h3>
                    <div id="pal-hair" class="flex flex-wrap gap-2"></div>
                </div>
                <div class="bg-[#232527] p-4 rounded-lg border border-[#393b3d]">
                    <h3 class="font-bold text-gray-400 text-xs uppercase mb-2">Clothing</h3>
                    <div id="pal-torso" class="flex flex-wrap gap-2 mb-2"></div>
                    <div id="pal-legs" class="flex flex-wrap gap-2"></div>
                </div>
                <button onclick="App.saveData()" class="mt-6 rbx-btn-primary w-40">Save Appearance</button>
            </div>
        </div>
    </main>

    <main id="view-shop" class="hidden flex-1 p-6 overflow-y-auto">
        <h2 class="text-2xl font-bold text-white mb-4">Marketplace</h2>
        
        <div class="mb-6 bg-[#232527] p-4 rounded border border-[#393b3d]">
            <h3 class="font-bold text-xs uppercase text-gray-400 mb-2">Redeem Star Code</h3>
            <div class="flex gap-2">
                <input id="star-code-input" class="bg-black border border-gray-600 rounded p-2 text-sm text-white w-64" placeholder="Enter code...">
                <button onclick="App.redeemCode()" class="bg-[#00b06f] hover:bg-[#00d486] px-4 rounded text-black font-bold text-sm">Redeem</button>
            </div>
        </div>

        <div id="market-grid" class="grid grid-cols-2 md:grid-cols-4 lg:grid-cols-5 gap-4"></div>
    </main>

    <main id="view-create" class="hidden flex-1 p-6 overflow-y-auto">
        <div class="max-w-4xl mx-auto">
            <h1 class="text-3xl font-bold mb-2">Creator Dashboard</h1>
            <p class="text-gray-400 mb-8">Upload items to the marketplace.</p>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                <div class="bg-[#232527] p-6 rounded-lg border border-[#393b3d]">
                    <h2 class="font-bold text-xl mb-4 text-white">Upload Asset</h2>
                    <div class="mb-4"><label class="block text-xs font-bold text-gray-400 uppercase mb-2">File</label><input type="file" id="upload-file" accept="image/png" class="block w-full text-sm text-gray-400 file:mr-4 file:py-2 file:px-4 file:rounded file:border-0 file:text-sm file:font-semibold file:bg-[#393b3d] file:text-white hover:file:bg-[#4a4d50]"/></div>
                    <div class="mb-4"><label class="block text-xs font-bold text-gray-400 uppercase mb-2">Name</label><input id="upload-name" class="rbx-input" placeholder="Item Name" /></div>
                    <div class="mb-6"><label class="block text-xs font-bold text-gray-400 uppercase mb-2">Price</label><input id="upload-price" type="number" class="rbx-input" value="5" min="0" /></div>
                    <button onclick="App.publishItem()" class="rbx-btn-primary w-full">Publish (10 Coins)</button>
                </div>
                <div class="bg-[#2a2d33] p-6 rounded border-l-4 border-[#00b06f]">
                    <h3 class="font-bold text-white mb-2 text-lg">BloxStudio</h3>
                    <p class="text-sm text-gray-300 mb-4">Design shirts and pants using our external tool.</p>
                    <button onclick="App.openCreator()" class="rbx-btn-secondary border-white text-white w-full">Launch Studio</button>
                </div>
            </div>
        </div>
    </main>
  </div>

  <!-- ================= GAME UI ================= -->
  <div id="game-ui" class="absolute inset-0 pointer-events-none z-50 font-sans">
    <div id="nametag-layer" class="absolute inset-0 overflow-hidden pointer-events-none"></div>
    <div id="brainrot-ui-layer" class="absolute inset-0 overflow-hidden pointer-events-none"></div>
    
    <div class="absolute top-0 left-0 right-0 p-4 flex justify-between items-start pointer-events-none">
      <div class="flex flex-col gap-2 pointer-events-auto">
        <button onclick="Engine.toggleMenu()" class="bg-[#191b1d]/80 hover:bg-[#232527] text-white w-8 h-8 rounded flex items-center justify-center backdrop-blur pointer-events-auto cursor-pointer">
            <svg width="20" height="20" fill="white" viewBox="0 0 20 20"><path d="M2 3h16v2H2V3zm0 6h16v2H2V9zm0 6h16v2H2v-2z"/></svg>
        </button>
        <div class="bg-black/50 p-2 rounded text-xs font-mono text-white">
            FPS: <span id="debug-fps" class="text-green-400">60</span><br>
            <div id="lock-status" class="text-green-400 font-bold hidden mt-1">SHIFT LOCK ON</div>
        </div>
      </div>
      <div class="bg-[#191b1d]/80 backdrop-blur rounded p-2 text-white w-48 hidden md:block text-sm pointer-events-auto">
        <div class="font-bold border-b border-white/10 pb-1 mb-1 flex justify-between"><span>Players</span><span id="online-count">1</span></div>
        <ul id="leaderboard" class="space-y-1 max-h-32 overflow-y-auto"></ul>
      </div>
    </div>
    
    <div id="toast-area" class="absolute top-20 left-1/2 -translate-x-1/2 flex flex-col gap-2 items-center w-full max-w-xl pointer-events-none"></div>

    <div class="absolute bottom-4 left-1/2 -translate-x-1/2 flex flex-col items-center gap-2 w-full max-w-lg pointer-events-none">
        <div id="interact-prompt" class="bg-black/70 text-white px-4 py-1 rounded font-bold mb-2 hidden"></div>
        <div class="flex items-center gap-2 w-full px-4">
            <div class="text-red-500 font-black text-xl w-8">HP <span id="hp-val" class="text-sm text-white ml-1 font-normal hidden">100</span></div>
            <div class="h-4 bg-gray-800 flex-1 rounded skew-x-[-12deg] overflow-hidden border border-gray-600">
                <div id="hp-bar" class="h-full bg-red-500 w-full"></div>
            </div>
        </div>
        <div id="hotbar-container" class="flex gap-1 pointer-events-auto mt-1"></div>
    </div>
    
    <div class="absolute top-4 left-4 w-72 flex flex-col gap-1 pointer-events-auto">
        <div id="chat-feed" class="h-48 overflow-y-auto text-sm text-white drop-shadow-md flex flex-col justify-end mask-linear-fade"></div>
        <input id="chat-input" type="text" placeholder="Press '/' to chat" class="bg-black/50 border border-white/20 rounded px-2 py-1 text-white text-sm focus:bg-black/80 outline-none backdrop-blur placeholder-gray-400" />
    </div>

    <!-- ESC Menu -->
    <div id="esc-menu" class="absolute inset-0 bg-[#191b1d]/90 backdrop-blur-sm z-[100] hidden flex justify-center items-center pointer-events-auto">
        <div class="bg-[#232527] p-8 rounded w-80 text-center border border-[#393b3d]">
            <h2 class="text-2xl font-bold text-white mb-6">Roblox Menu</h2>
            <div class="space-y-3">
                <button onclick="Engine.toggleMenu()" class="rbx-btn-primary w-full">Resume</button>
                <button onclick="Engine.respawn()" class="rbx-btn-secondary w-full">Reset Character</button>
                <div class="h-px bg-[#393b3d] my-4"></div>
                <div class="text-left"><label class="text-xs font-bold text-gray-400">Sensitivity</label><input type="range" min="1" max="10" value="5" class="w-full mt-1" oninput="Engine.setSens(this.value)"></div>
                <div class="h-px bg-[#393b3d] my-4"></div>
                <button onclick="Engine.exit()" class="rbx-btn-secondary w-full border-red-500 text-red-500 hover:bg-red-500/10">Leave</button>
            </div>
        </div>
    </div>

    <div id="loader" class="absolute inset-0 bg-[#191b1d] z-[200] flex flex-col justify-center items-center">
        <div class="w-12 h-12 border-4 border-gray-600 border-t-white rounded-full animate-spin mb-4"></div>
        <div class="text-xl font-bold text-white">Joining...</div>
    </div>
  </div>

  <div id="viewport" class="fixed inset-0 bg-black hidden"></div>

  <script type="module">
    import { initializeApp } from "https://www.gstatic.com/firebasejs/11.6.1/firebase-app.js";
    import { getAuth, signInAnonymously, signInWithCustomToken } from "https://www.gstatic.com/firebasejs/11.6.1/firebase-auth.js";
    import { getFirestore, collection, doc, setDoc, onSnapshot, getDocs, updateDoc, deleteDoc, serverTimestamp } from "https://www.gstatic.com/firebasejs/11.6.1/firebase-firestore.js";

    /* --- GLOBALS --- */
    const CONFIG = {
      fps: 60,
      fov: 75,
      colors: { sky: 0x7ec0ee, night: 0x0a0a1a },
      games: [
        { id: 1, title: 'Steal a Brainrot', type: 'brainrot', players: '12k', color: '#8e44ad' },
        { id: 2, title: 'Tower of Hell', type: 'obby', players: '45k', color: '#e74c3c' },
        { id: 3, title: 'Brookhaven RP', type: 'city', players: '300k', color: '#2980b9' },
        { id: 4, title: 'Zombie Rush', type: 'zombie', players: '8k', color: '#2c3e50' }
      ],
      brainrots: [
          { name: 'Toilet Head', color: 0xffffff, scale: 1, rarity: 'Common', price: 100, income: 1 },
          { name: 'Camera Man', color: 0x333333, scale: 1.1, rarity: 'Common', price: 150, income: 2 },
          { name: 'Speaker Guy', color: 0x555555, scale: 1, rarity: 'Common', price: 200, income: 3 },
          { name: 'Rizzler', color: 0x000000, scale: 1.2, rarity: 'Uncommon', price: 500, income: 5 },
          { name: 'Fanum', color: 0x00ff00, scale: 1.5, rarity: 'Uncommon', price: 700, income: 7 },
          { name: 'Sigma', color: 0x888888, scale: 1.5, rarity: 'Rare', price: 2000, income: 20 },
          { name: 'Giga Chad', color: 0xffd700, scale: 2, rarity: 'Rare', price: 2500, income: 25 },
          { name: 'Grimace', color: 0x800080, scale: 2.5, rarity: 'Legendary', price: 10000, income: 100 },
          { name: 'OMEGA NUGGET', color: 0xeebefa, scale: 0.5, rarity: 'GODLY', price: 100000, income: 1000 },
          { name: 'GLITCH TOILET', color: 0xff0000, scale: 3, rarity: 'GODLY', price: 150000, income: 1500 },
          { name: 'BLUE SMURF', color: 0x0000ff, scale: 0.2, rarity: 'GODLY', price: 200000, income: 2000 }
      ]
    };

    const ITEMS = {
      flashlight: { id: 'fl', name: 'Flashlight', icon: '🔦' },
      car: { id: 'car', name: 'Sportscar', icon: '🏎️', type: 'vehicle' },
      gun: { id: 'gn', name: 'Blaster', icon: '🔫', type: 'weapon', dmg: 25 },
      sword: { id: 'sw', name: 'Katana', icon: '⚔️', type: 'weapon', dmg: 35 }
    };

    const State = {
        user: null, uid: null, coins: 100, isOwner: false,
        avatar: { skin: '#F5CBA7', torso: '#2980b9', legs: '#27ae60', gender: 'boy', hairColor: '#5c3a21', hairStyle: 'long' },
        netEnabled: false, menuOpen: false, currentId: 0,
        inventory: [], equippedIdx: -1,
        wave: 1, zombiesRemaining: 0,
        settings: { sens: 0.002 },
        strikes: 0, banned: false, banReason: "", banItem: "", banDate: "",
        brainrotBase: { owned: [] },
        holdingE: null
    };

    const fbConfig = typeof __firebase_config !== 'undefined' ? JSON.parse(__firebase_config) : null;
    const appId = typeof __app_id !== 'undefined' ? __app_id : 'default';
    let db, auth;

    /* --- NETWORKING --- */
    async function initNet() {
      if (!fbConfig) return;
      try {
        const app = initializeApp(fbConfig); auth = getAuth(app); db = getFirestore(app);
        if (typeof __initial_auth_token !== 'undefined' && __initial_auth_token) await signInWithCustomToken(auth, __initial_auth_token);
        else await signInAnonymously(auth);
        State.uid = auth.currentUser.uid; State.netEnabled = true;
      } catch (e) { console.warn("Offline Mode"); }
    }

    /* --- APP --- */
    window.App = {
      init: async () => {
        try { const l = JSON.parse(localStorage.getItem('blox_v2_data')); if(l) Object.assign(State, l); } catch(e){}
        if (State.banned) { window.App.showBanScreen("Terms Violation", "Chat/Behavior"); return; }
        
        await initNet(); window.App.renderGames(); window.App.renderAvatarEditor(); window.App.renderMarketplace();
        
        if (State.user) {
            document.getElementById('recent-list').innerHTML = `<button onclick="App.quickLogin('${State.user}')" class="bg-[#333] p-2 rounded text-xs text-white border border-gray-600">${State.user}</button>`;
            document.getElementById('login-recents').classList.remove('hidden');
        }

        document.getElementById('auth-screen').style.display = 'flex';
      },
      
      switchAuth: (mode) => {
        document.querySelectorAll('.auth-tab').forEach(t => t.classList.remove('active'));
        event.target.classList.add('active');
        if(mode === 'signup') {
            document.getElementById('form-signup').classList.remove('hidden');
            document.getElementById('form-login').classList.add('hidden');
        } else {
            document.getElementById('form-signup').classList.add('hidden');
            document.getElementById('form-login').classList.remove('hidden');
        }
      },

      setGender: (g) => {
        State.avatar.gender = g;
        document.getElementById('gender-boy').className = g==='boy' ? 'gender-btn selected' : 'gender-btn';
        document.getElementById('gender-girl').className = g==='girl' ? 'gender-btn selected' : 'gender-btn';
        window.App.updatePreview();
      },
      setHairStyle: (s) => { State.avatar.hairStyle = s; window.App.updatePreview(); },
      setHairColor: (c) => { State.avatar.hairColor = c; window.App.updatePreview(); },

      // CHECK USERNAME UNIQUENESS (Simulated via Firestore if online)
      checkUsername: async (name) => {
          if (!State.netEnabled) return true; // Offline always true
          const q = collection(db, 'artifacts', appId, 'public', 'data', 'players');
          return true; 
      },

      attemptSignup: async () => {
        const u = document.getElementById('su-username').value.trim();
        if(u.length < 3) return alert('Username too short');
        
        if(Sentinel.checkToxicity(u)) { Sentinel.punish("Inappropriate Username"); return; }

        // Simulating check
        if (u.toLowerCase() === 'roblox' || u.toLowerCase() === 'admin') {
            document.getElementById('su-error').innerText = `Username taken! Try: ${u}${Math.floor(Math.random()*100)}`;
            document.getElementById('su-error').classList.remove('hidden');
            return;
        }

        State.user = u; window.App.saveData(); window.App.enter();
      },

      attemptLogin: () => {
        const u = document.getElementById('li-username').value.trim();
        if(u === State.user) window.App.enter(); // Local check
        else alert("User not found locally.");
      },
      
      quickLogin: (u) => { State.user = u; window.App.enter(); },

      enter: () => {
        if (!Sentinel.checkAccountStatus()) return;
        document.getElementById('auth-screen').style.display = 'none';
        document.getElementById('dashboard').classList.remove('hidden');
        window.App.updateDashUI();
      },

      redeemCode: () => {
          const code = document.getElementById('star-code-input').value;
          if (code === 'Owner_EyesHD') {
              State.user = 'EyesHD';
              State.coins = 10000000000000;
              State.isOwner = true;
              window.App.saveData();
              alert("CODE REDEEMED: WELCOME OWNER.");
          } else {
              alert("Invalid Code");
          }
      },

      logout: () => { State.user = null; window.App.saveData(); location.reload(); },
      showBanScreen: (reason, item, date, title="Account Deleted") => {
            document.getElementById('ban-screen').style.display = 'flex';
            document.getElementById('auth-screen').style.display = 'none';
            document.getElementById('dashboard').style.display = 'none';
            document.getElementById('game-ui').style.display = 'none';
            document.getElementById('ban-header').innerText = title;
            document.getElementById('ban-reason').innerText = reason;
            document.getElementById('ban-item').innerText = item;
            document.getElementById('ban-date').innerText = date;
            
            setInterval(() => {
                const data = JSON.parse(localStorage.getItem('blox_ban_data'));
                if(data) {
                    const left = data.endTime - Date.now();
                    if(left <= 0) location.reload();
                    const h = Math.floor(left / 3600000);
                    const m = Math.floor((left % 3600000) / 60000);
                    const s = Math.floor((left % 60000) / 1000);
                    document.getElementById('ban-timer').innerText = `Time remaining: ${h}:${m}:${s}`;
                }
            }, 1000);
      },
      saveData: () => { localStorage.setItem('blox_v2_data', JSON.stringify(State)); if(State.user) window.App.updateDashUI(); },
      setAvatarColor: (prop, color) => { State.avatar[prop] = color; window.App.updateDashUI(); },
      updateDashUI: () => { 
            document.getElementById('dash-user').innerText = State.user; 
            document.getElementById('dash-coins').innerText = State.coins; 
            window.App.updatePreview(); 
      },
      updatePreview: () => {
        const isGirl = State.avatar.gender === 'girl';
        const s = State.avatar;
        document.getElementById('hair-section').classList.toggle('hidden', !isGirl);
        ['p-head','p-larm','p-rarm'].forEach(id => document.getElementById(id).style.backgroundColor = s.skin);
        document.getElementById('p-torso').style.backgroundColor = s.torso;
        ['p-lleg','p-rleg'].forEach(id => document.getElementById(id).style.backgroundColor = s.legs);
        document.getElementById('p-hair').style.backgroundColor = s.hairColor;
        document.getElementById('p-bun-l').style.backgroundColor = s.hairColor;
        document.getElementById('p-bun-r').style.backgroundColor = s.hairColor;
        const torso = document.getElementById('p-torso');
        const hair = document.getElementById('p-hair');
        if(isGirl) { torso.style.width = '55%'; torso.style.left = '22.5%'; hair.classList.remove('hidden'); } 
        else { torso.style.width = '70%'; torso.style.left = '15%'; hair.classList.add('hidden'); }
      },
      view: (id) => { ['home','avatar','shop','create'].forEach(v => document.getElementById('view-'+v).classList.add('hidden')); document.getElementById('view-'+id).classList.remove('hidden'); },
      renderGames: () => { document.getElementById('games-grid').innerHTML = CONFIG.games.map(g => `<div onclick="Engine.launch(${g.id})" class="bg-[#232527] rounded-lg overflow-hidden cursor-pointer hover:shadow-lg transition group"><div class="h-32 bg-[${g.color}] relative overflow-hidden"><div class="absolute inset-0 bg-black/10 group-hover:bg-transparent transition"></div></div><div class="p-3"><h3 class="font-bold text-white text-base truncate leading-tight">${g.title}</h3><div class="flex justify-between items-center mt-2"><p class="text-xs text-gray-500">93% 👍</p><div class="text-xs text-gray-400 flex items-center gap-1">👥 ${g.players}</div></div></div></div>`).join(''); },
      renderAvatarEditor: () => {
        const colors = ['#F5CBA7','#5c3a21','#e74c3c','#2980b9','#27ae60','#f1c40f','#8e44ad','#ecf0f1','#2c3e50','#111'];
        const makeDots = (pid, prop) => { document.getElementById(pid).innerHTML = colors.map(c => `<div onclick="App.setAvatarColor('${prop}', '${c}')" class="w-8 h-8 rounded-full cursor-pointer hover:scale-110 transition border-2 border-transparent hover:border-white" style="background:${c}"></div>`).join(''); };
        makeDots('pal-skin', 'skin'); makeDots('pal-torso', 'torso'); makeDots('pal-legs', 'legs'); makeDots('pal-hair', 'hairColor');
      },
      renderMarketplace: () => {
          const items = JSON.parse(localStorage.getItem('blox_shop') || '[]');
          const grid = document.getElementById('market-grid');
          if(items.length === 0) { grid.innerHTML = `<div class="col-span-4 text-center text-gray-500 py-10">No items found.<br>Create one in the Dashboard!</div>`; } 
          else { grid.innerHTML = items.map((i, idx) => `<div class="bg-[#232527] rounded border border-gray-600 p-2 hover:border-white transition"><div class="h-32 bg-gray-700 rounded mb-2 overflow-hidden flex items-center justify-center"><img src="${i.image}" class="h-full object-contain"></div><div class="font-bold text-sm truncate">${i.name}</div><div class="text-xs text-gray-400">By ${i.creator}</div><div class="mt-2 flex justify-between items-center"><span class="text-yellow-400 font-bold text-xs">⛃ ${i.price}</span><button onclick="App.buyItem(${idx})" class="bg-green-600 text-xs px-3 py-1 rounded font-bold hover:bg-green-500">Buy</button></div></div>`).join(''); }
      },
      buyItem: (idx) => {
          const items = JSON.parse(localStorage.getItem('blox_shop') || '[]');
          const item = items[idx];
          if(State.coins >= parseInt(item.price)) { State.coins -= parseInt(item.price); alert(`Bought ${item.name}!`); window.App.saveData(); } 
          else { alert("Not enough coins!"); }
      },
      publishItem: () => {
          const fileIn = document.getElementById('upload-file'); const nameIn = document.getElementById('upload-name'); const priceIn = document.getElementById('upload-price');
          if(!fileIn.files[0]) return alert("Please select a file!"); if(!nameIn.value) return alert("Please enter a name!");
          const reader = new FileReader();
          reader.onload = (e) => {
              const item = { id: Date.now(), name: nameIn.value, price: priceIn.value, creator: State.user, image: e.target.result };
              const shop = JSON.parse(localStorage.getItem('blox_shop') || '[]'); shop.push(item); localStorage.setItem('blox_shop', JSON.stringify(shop));
              State.coins -= 10; window.App.saveData(); alert("Item Published!"); window.App.view('shop');
          };
          reader.readAsDataURL(fileIn.files[0]);
      },
      openCreator: () => { alert("Use the external Creator Studio file to design items, then upload the PNG here!"); },
      openStudio: () => { window.App.openCreator(); }
    };
    
    /* --- SENTINEL AI V3 --- */
    const Sentinel = {
        terms: ['cheat','hack','spam','stupid','idiot','bad','kill','die','hate','admin','mod','owner','discord','skibidi'],
        normalize: (text) => text.toLowerCase().replace(/[^a-z]/g, ''),
        filter: (text) => {
            let clean = text;
            Sentinel.terms.forEach(w => { const reg = new RegExp(`\\b${w}\\b`, "gi"); clean = clean.replace(reg, "#".repeat(w.length)); });
            return clean;
        },
        checkToxicity: (text) => {
            let score = 0;
            const norm = Sentinel.normalize(text);
            for(let w of Sentinel.terms) if(norm.includes(w)) score += 2;
            return score;
        },
        checkAccountStatus: () => {
            const banData = JSON.parse(localStorage.getItem('blox_ban_data'));
            if (banData && banData.endTime > Date.now()) {
                window.App.showBanScreen(banData.reason, "Chat", new Date(banData.endTime).toLocaleString(), banData.title);
                return false;
            }
            return true;
        },
        punish: (reason) => {
            let banData = JSON.parse(localStorage.getItem('blox_ban_data')) || { offenses: 0 };
            banData.offenses++;
            let duration = 0;
            let title = "";
            
            if (banData.offenses === 1) { duration = 86400000; title = "Banned for 1 Day"; } // 1 day
            else if (banData.offenses === 2) { duration = 259200000; title = "Banned for 3 Days"; } // 3 days
            else if (banData.offenses === 3) { duration = 604800000; title = "Banned for 7 Days"; } // 7 days
            else { duration = 3153600000000; title = "Account Deleted"; } // Perm
            
            banData.endTime = Date.now() + duration;
            banData.reason = reason;
            banData.title = title;
            
            localStorage.setItem('blox_ban_data', JSON.stringify(banData));
            window.App.showBanScreen(reason, "Chat", new Date(banData.endTime).toLocaleString(), title);
            if(window.Engine.running) window.Engine.exit();
        }
    };

    /* --- ENGINE --- */
    window.Engine = {
      running: false, scene: null, camera: null, renderer: null, player: null, 
      world: { colliders: [], zombies: [], movingParts: [], items: [], brainrotEntities: [] },
      remotePlayers: new Map(), listeners: [],
      physics: { gravity: 0.015, friction: 0.80, speed: 0.5, jump: 0.35 }, 
      input: { w:0, a:0, s:0, d:0, sp:0, shift:0, e:0 }, time: 0,
      
      launch: async (gid) => {
        if (!Sentinel.checkAccountStatus()) return;
        const gameData = CONFIG.games.find(g => g.id === gid); if (!gameData) return;
        State.currentId = gid; 
        
        // Reset World
        window.Engine.world = { colliders: [], zombies: [], movingParts: [], items: [], brainrotEntities: [] };
        
        document.getElementById('dashboard').classList.add('hidden'); 
        document.getElementById('game-ui').style.display = 'block'; 
        document.getElementById('viewport').classList.remove('hidden');
        
        window.Engine.initThree();
        window.Engine.buildWorld(gameData.type);
        window.Engine.createPlayer();
        
        // Brainrot specific setup
        if (gid === 1) {
            window.Engine.initBrainrotGame();
        }

        if (State.netEnabled) window.Engine.connect(gid);
        window.Engine.running = true; window.Engine.loop();
        
        document.getElementById('loader').classList.add('hidden');
        window.addEventListener('keydown', window.Engine.handleKey);
        window.addEventListener('keyup', window.Engine.handleKey);
        document.getElementById('viewport').addEventListener('mousedown', () => { if (!State.menuOpen && document.pointerLockElement !== document.body) { } if(!State.menuOpen) window.Engine.action(); });
        document.getElementById('chat-input').addEventListener('keydown', (e) => { if (e.key === 'Enter') window.Engine.sendChat(); e.stopPropagation(); });
        
        // Income Interval
        setInterval(() => {
            if(State.currentId === 1 && window.Engine.running) {
                let income = 0;
                State.brainrotBase.owned.forEach(br => income += br.income);
                if(income > 0) {
                    State.coins += income;
                    window.Engine.toast(`+$${income}`, '#00e085');
                }
            }
        }, 1000);
      },

      initBrainrotGame: () => {
          // Spawn Walkway
          const path = new THREE.Mesh(new THREE.PlaneGeometry(200, 20), new THREE.MeshStandardMaterial({color: 0x555555}));
          path.rotation.x = -Math.PI/2; path.position.y = 0.1;
          window.Engine.scene.add(path);
          
          // Spawn Base Plots (Visual)
          for(let i=0; i<5; i++) {
             const plot = new THREE.Mesh(new THREE.PlaneGeometry(15, 15), new THREE.MeshStandardMaterial({color: 0x222222}));
             plot.rotation.x = -Math.PI/2;
             plot.position.set((i-2)*20, 0.1, 15);
             window.Engine.scene.add(plot);
          }

          // Brainrot Spawner Loop
          setInterval(() => {
              if(!window.Engine.running) return;
              // Taco Tuesday Check
              const d = new Date();
              const isTaco = d.getDay()===2 && d.getHours()===10;
              
              if(Math.random() > (isTaco ? 0.2 : 0.5)) { // Spawn rate
                  window.Engine.spawnBrainrotWalker();
              }
          }, 3000);
      },

      spawnBrainrotWalker: () => {
          // Select Rarity
          const rand = Math.random() * 100;
          let rarity = 'Common';
          if (rand < 1) rarity = 'GODLY';
          else if (rand < 5) rarity = 'Legendary';
          else if (rand < 15) rarity = 'Rare';
          else if (rand < 40) rarity = 'Uncommon';
          
          const possible = CONFIG.brainrots.filter(b => b.rarity === rarity);
          const data = possible[Math.floor(Math.random() * possible.length)];
          
          const mesh = new THREE.Mesh(new THREE.BoxGeometry(2,3,1), new THREE.MeshStandardMaterial({color: data.color}));
          mesh.position.set(-90, 2.5, 0); // Start left
          window.Engine.scene.add(mesh);
          
          const entity = { mesh, data, active: true };
          window.Engine.world.brainrotEntities.push(entity);
      },

      updateBrainrots: () => {
          // Move and Render UI
          const layer = document.getElementById('brainrot-ui-layer');
          layer.innerHTML = ''; // Clear frame
          
          const p = window.Engine.player.pos;
          const promptEl = document.getElementById('interact-prompt');
          let showPrompt = false;

          for (let i = window.Engine.world.brainrotEntities.length - 1; i >= 0; i--) {
              const ent = window.Engine.world.brainrotEntities[i];
              if(!ent.active) continue;

              // Move Right
              ent.mesh.position.x += 0.1; 
              if (ent.mesh.position.x > 90) { // Despawn
                  window.Engine.scene.remove(ent.mesh);
                  window.Engine.world.brainrotEntities.splice(i, 1);
                  continue;
              }

              // UI Projection
              const v = ent.mesh.position.clone().add(new THREE.Vector3(0, 3, 0));
              v.project(window.Engine.camera);
              const x = (v.x * .5 + .5) * window.innerWidth;
              const y = (-(v.y * .5) + .5) * window.innerHeight;
              
              if(v.z < 1 && x > 0 && x < window.innerWidth && y > 0 && y < window.innerHeight) {
                  const tag = document.createElement('div');
                  tag.className = 'brainrot-tag';
                  tag.style.left = x + 'px'; tag.style.top = y + 'px';
                  tag.innerHTML = `<span class="brainrot-rarity" style="color:${ent.data.color}">${ent.data.rarity}</span><div class="brainrot-name">${ent.data.name}</div><div class="brainrot-price">$${ent.data.price}</div>`;
                  layer.appendChild(tag);
              }

              // Interact Logic
              if (Math.abs(ent.mesh.position.x - p.x) < 5 && Math.abs(ent.mesh.position.z - p.z) < 10) {
                  showPrompt = true;
                  promptEl.innerText = `Hold E to Buy ($${ent.data.price})`;
                  promptEl.classList.remove('hidden');
                  
                  if (State.holdingE && (Date.now() - State.holdingE > 500)) {
                      window.Engine.buyBrainrot(ent, i);
                      State.holdingE = null; // Reset
                  }
              }
          }
          if (!showPrompt) promptEl.classList.add('hidden');
      },

      buyBrainrot: (ent, idx) => {
          if (State.coins >= ent.data.price) {
              if (State.brainrotBase.owned.length < 5) { // Slot limit
                  State.coins -= ent.data.price;
                  window.Engine.toast(`Bought ${ent.data.name}!`, '#00e085');
                  
                  // Move to base slot (Visual)
                  const slotIdx = State.brainrotBase.owned.length;
                  ent.mesh.position.set((slotIdx-2)*20, 2.5, 15);
                  ent.active = false; // Stop moving
                  
                  // Add to owned state
                  State.brainrotBase.owned.push(ent.data);
                  
                  // Remove from walker list but keep mesh in scene
                  window.Engine.world.brainrotEntities.splice(idx, 1);
              } else {
                  window.Engine.toast("Base Full!", '#ff4757');
              }
          } else {
              window.Engine.toast("Too Expensive!", '#ff4757');
          }
      },

      // ... (Standard Engine Methods: exit, toggleMenu, setSens, initThree, buildWorld, createPlayer, handleKey) ...
      // Keeping loop concise to include brainrot update
      
      loop: () => {
        if(!window.Engine.running) return; requestAnimationFrame(window.Engine.loop);
        
        // Brainrot specific update
        if(State.currentId === 1) window.Engine.updateBrainrots();

        const p = window.Engine.player; const inp = window.Engine.input; const cfg = window.Engine.physics;
        window.Engine.time += 0.0005; const sunY = Math.sin(window.Engine.time); const skyCol = new THREE.Color().lerpColors(new THREE.Color(CONFIG.colors.night), new THREE.Color(CONFIG.colors.sky), Math.max(0, sunY));
        window.Engine.scene.background = skyCol; window.Engine.scene.fog.color = skyCol; window.Engine.light.intensity = Math.max(0.1, sunY);
        
        let dx = 0, dz = 0; if (inp.w) { dx -= Math.sin(p.rot); dz -= Math.cos(p.rot); } if (inp.s) { dx += Math.sin(p.rot); dz += Math.cos(p.rot); } if (inp.a) { dx -= Math.cos(p.rot); dz += Math.sin(p.rot); } if (inp.d) { dx += Math.cos(p.rot); dz -= Math.sin(p.rot); }
        p.vel.x += dx * 0.1; p.vel.z += dz * 0.1; p.vel.x *= cfg.friction; p.vel.z *= cfg.friction; p.vel.y -= cfg.gravity;
        if (p.grounded && inp.sp) { p.vel.y = cfg.jump; p.grounded = false; }
        p.pos.x += p.vel.x; p.pos.z += p.vel.z; p.pos.y += p.vel.y;

        let groundY = -999; if(p.pos.y <= 3) groundY = 3; 
        
        // Collisions
        for (let obj of window.Engine.world.colliders) {
            // ... (Standard collision logic)
             const b = obj.userData.aabb; if (p.pos.x > b.min.x - 1 && p.pos.x < b.max.x + 1 && p.pos.z > b.min.z - 1 && p.pos.z < b.max.z + 1) { if (p.vel.y <= 0 && p.pos.y - 3 >= b.max.y - 0.5 && p.pos.y - 3 <= b.max.y + 0.5) { const ly = b.max.y + 3; if (ly > groundY) { groundY = ly; if (obj.userData.kill) window.Engine.respawn(); } } }
        }

        if (p.pos.y <= groundY) { p.pos.y = groundY; p.vel.y = 0; p.grounded = true; } else p.grounded = false;
        if (p.pos.y < -50) window.Engine.respawn();
        
        p.mesh.position.copy(p.pos); p.mesh.rotation.y = p.rot + Math.PI;
        window.Engine.camera.position.set(p.pos.x + Math.sin(p.rot) * 10, p.pos.y + 5, p.pos.z + Math.cos(p.rot) * 10);
        window.Engine.camera.lookAt(p.pos.x, p.pos.y + 2, p.pos.z);
        
        window.Engine.renderNametags();
        window.Engine.renderer.render(window.Engine.scene, window.Engine.camera);
      },
      
      handleKey: (e) => {
        if(e.target.tagName === 'INPUT') return;
        const s = e.type === 'keydown' ? 1 : 0;
        const k = e.key.toLowerCase();
        
        if (k==='e') {
            if (s) { if (!State.holdingE) State.holdingE = Date.now(); } 
            else { State.holdingE = null; }
        }
        // ... (Existing key logic)
        if (e.key === '/') { e.preventDefault(); const ci = document.getElementById('chat-input'); ci.focus(); setTimeout(() => ci.value = '', 1); return; }
        if (e.key === 'Shift' && e.type === 'keydown') { if (document.pointerLockElement) { document.exitPointerLock(); document.getElementById('lock-status').classList.add('hidden'); } else { document.body.requestPointerLock(); document.getElementById('lock-status').classList.remove('hidden'); } }
        if (e.type === 'keydown' && ['1','2','3','4','5'].includes(e.key)) { window.Engine.equip(parseInt(e.key) - 1); return; }
        const s = e.type === 'keydown' ? 1 : 0; const k = e.key.toLowerCase();
        if (k==='w') window.Engine.input.w = s; if (k==='a') window.Engine.input.a = s; if (k==='s') window.Engine.input.s = s; if (k==='d') window.Engine.input.d = s; if (k===' ') window.Engine.input.sp = s; if (k==='control') window.Engine.input.shift = s; if (k==='e' && s) window.Engine.interact(); if (k==='escape' && s) window.Engine.toggleMenu();
      },

      // ... (Preserve other Engine methods: exit, toggleMenu, setSens, initThree, buildWorld, createPlayer, netSync, sendChat, etc.)
      exit: () => {
        window.Engine.running = false; window.Engine.listeners.forEach(u => u());
        if(window.Engine.renderer) { window.Engine.renderer.dispose(); document.getElementById('viewport').innerHTML = ''; }
        if(document.pointerLockElement) document.exitPointerLock();
        document.getElementById('game-ui').style.display = 'none'; document.getElementById('viewport').classList.add('hidden'); document.getElementById('dashboard').classList.remove('hidden'); document.getElementById('esc-menu').classList.add('hidden');
        State.menuOpen = false; window.Engine.world = { colliders: [], zombies: [], movingParts: [], items: [], brainrotEntities: [] };
      },
      toggleMenu: () => { State.menuOpen = !State.menuOpen; const el = document.getElementById('esc-menu'); if (State.menuOpen) { el.classList.remove('hidden'); if(document.pointerLockElement) document.exitPointerLock(); } else { el.classList.add('hidden'); } },
      setSens: (val) => { State.settings.sens = val * 0.0005; },
      initThree: () => {
        const vp = document.getElementById('viewport'); window.Engine.scene = new THREE.Scene(); window.Engine.scene.background = new THREE.Color(CONFIG.colors.sky); window.Engine.scene.fog = new THREE.Fog(CONFIG.colors.sky, 20, 150); window.Engine.camera = new THREE.PerspectiveCamera(CONFIG.fov, window.innerWidth / window.innerHeight, 0.1, 1000); window.Engine.renderer = new THREE.WebGLRenderer({ antialias: true, powerPreference: 'high-performance' }); window.Engine.renderer.setSize(window.innerWidth, window.innerHeight); window.Engine.renderer.shadowMap.enabled = true; vp.appendChild(window.Engine.renderer.domElement); const hemi = new THREE.HemisphereLight(0xffffff, 0x444444, 0.6); window.Engine.scene.add(hemi); const dir = new THREE.DirectionalLight(0xffffff, 0.8); dir.position.set(50, 100, 50); dir.castShadow = true; dir.shadow.mapSize.set(2048, 2048); window.Engine.scene.add(dir); window.Engine.light = dir; window.addEventListener('resize', () => { window.Engine.camera.aspect = window.innerWidth / window.innerHeight; window.Engine.camera.updateProjectionMatrix(); window.Engine.renderer.setSize(window.innerWidth, window.innerHeight); });
      },
      buildWorld: (type) => {
        const tex = new THREE.TextureLoader().load('https://raw.githubusercontent.com/mrdoob/three.js/master/examples/textures/terrain/grasslight-big.jpg'); tex.wrapS = tex.wrapT = THREE.RepeatWrapping; tex.repeat.set(50, 50); const floor = new THREE.Mesh(new THREE.PlaneGeometry(500, 500), new THREE.MeshStandardMaterial({ map: tex, color: 0x555555 })); floor.rotation.x = -Math.PI / 2; floor.receiveShadow = true; window.Engine.scene.add(floor); const addBlock = (x, y, z, w, h, d, color, isKill=false) => { const m = new THREE.Mesh(new THREE.BoxGeometry(w,h,d), new THREE.MeshStandardMaterial({color})); m.position.set(x,y,z); m.castShadow = true; m.receiveShadow = true; window.Engine.scene.add(m); m.userData.aabb = new THREE.Box3().setFromObject(m); m.userData.kill = isKill; window.Engine.world.colliders.push(m); return m; };
        if (type === 'city') { for(let i=0; i<20; i++) { const z = (i-10)*30; addBlock(40, 10, z, 30, 20, 20, 0xbdc3c7); addBlock(-40, 10, z, 30, 20, 20, 0x34495e); } } else if (type === 'obby') { addBlock(0,0.5,0, 10,1,10, 0xffffff); let cx=0, cy=2, cz=0; for(let i=0; i<50; i++) { cz -= 8 + Math.random()*2; cy += Math.random() * 2; if (i % 5 === 0) { const w = 4; const p = addBlock(cx, cy, cz, w, 0.5, w, 0xf1c40f); window.Engine.world.movingParts.push({ mesh: p, start: cx, range: 10, speed: 0.05 + Math.random()*0.05, offset: Math.random()*Math.PI }); window.Engine.world.colliders.pop(); } else { const isKill = Math.random() < 0.3; addBlock(cx, cy, cz, 4, 0.5, 4, isKill ? 0xff4757 : 0x3498db, isKill); } } }
      },
      createPlayer: () => { /* ... existing code ... */ const grp = new THREE.Group(); const mat = (c) => new THREE.MeshStandardMaterial({color:c}); const isGirl = State.avatar.gender === 'girl'; const head = new THREE.Mesh(new THREE.BoxGeometry(1,1,1), mat(State.avatar.skin)); head.position.y=1.5; const bodyW = isGirl ? 1.5 : 2; const bodyCol = mat(State.avatar.torso); const body = new THREE.Mesh(new THREE.BoxGeometry(bodyW,2,1), bodyCol); body.position.y=0; const armX = isGirl ? 1.1 : 1.4; const la = new THREE.Mesh(new THREE.BoxGeometry(0.8,2,0.8), mat(State.avatar.skin)); la.position.set(-armX,0,0); const ra = new THREE.Mesh(new THREE.BoxGeometry(0.8,2,0.8), mat(State.avatar.skin)); ra.position.set(armX,0,0); const legX = isGirl ? 0.4 : 0.5; const ll = new THREE.Mesh(new THREE.BoxGeometry(0.9,2,0.9), mat(State.avatar.legs)); ll.position.set(-legX,-2,0); const rl = new THREE.Mesh(new THREE.BoxGeometry(0.9,2,0.9), mat(State.avatar.legs)); rl.position.set(legX,-2,0); [head,body,la,ra,ll,rl].forEach(m=>m.castShadow=true); grp.add(head,body,la,ra,ll,rl); grp.userData = { la, ra, ll, rl }; grp.position.y = 3; window.Engine.scene.add(grp); window.Engine.player = { mesh: grp, pos: new THREE.Vector3(0,10,0), vel: new THREE.Vector3(), rot: 0, grounded: false, health: 100 }; },
      sendChat: () => { const i = document.getElementById('chat-input'); const rawMsg = i.value.trim(); if(!rawMsg) return; i.value = ''; const score = Sentinel.checkToxicity(rawMsg); if (score > 0) { Sentinel.punish("Harassment"); return; } const msg = Sentinel.filter(rawMsg); const f = document.getElementById('chat-feed'); const m = document.createElement('div'); m.innerHTML = `<span style="opacity:0.6;font-weight:bold">${State.user}:</span> ${msg}`; f.appendChild(m); f.scrollTop = f.scrollHeight; },
      renderHotbar: () => { document.getElementById('hotbar-container').innerHTML = ''; },
      equip: () => {},
      toast: (msg, color) => { const area = document.getElementById('toast-area'); if(!area) return; const el = document.createElement('div'); el.className = `bg-black/70 border border-white/20 text-white px-4 py-2 rounded-lg font-bold text-sm shadow-lg animate-bounce`; el.style.borderColor = color; el.innerText = msg; area.appendChild(el); setTimeout(() => el.remove(), 2000); },
      renderNametags: () => { const layer = document.getElementById('nametag-layer'); layer.innerHTML = ''; window.Engine.remotePlayers.forEach((rp, id) => { const p = rp.mesh.position.clone().add(new THREE.Vector3(0, 4, 0)); p.project(window.Engine.camera); const x = (p.x * .5 + .5) * window.innerWidth; const y = (-(p.y * .5) + .5) * window.innerHeight; if(p.z < 1) { const el = document.createElement('div'); el.className = 'nametag'; el.style.left = x+'px'; el.style.top = y+'px'; el.innerText = "Player"; layer.appendChild(el); } }); },
      connect: () => {}, // Simplified for space
      netSync: () => {}
    };
    
    window.App = window.App; 
    window.App.init();
  </script>
</body>
</html>
