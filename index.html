<!doctype html><html><head><meta charset=utf8><meta name=viewport content="width=device-width,initial-scale=1,viewport-fit=cover"><style>:root{color-scheme:light;box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}html{scroll-padding-top:env(safe-area-inset-top,0px)}body{margin:0;padding:0;font:14px -apple-system,BlinkMacSystemFont,sans-serif;background:#fff;color:#000}img{max-width:100%}[hidden]:not([hidden=until-found i]){display:none!important}</style></head><body>
<title>Faster</title>
<meta name="description" content="A desert speed-flyer. Hit boost to Mach 12, skim the dunes, shoot spider walkers.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Chakra+Petch:ital,wght@0,500;0,600;0,700;1,700&display=swap">
<style>
/* Layout: full-bleed 3D view, HUD pinned to edges, title/game-over sheets anchored bottom-left. */
:root {
  --ink: #f4efe6;
  --ink-dim: #b9b2a6;
  --slate: rgba(22, 28, 40, 0.82);
  --cyan: #4fd8ff;
  --amber: #ffa43a;
  --red: #ff4a3a;
  --off: #566070;
  --night: #0c0d10;
  --font: 'Chakra Petch', 'Rajdhani', ui-monospace, system-ui, sans-serif;
  color-scheme: dark;
}
html, body { height: 100%; }
body {
  margin: 0; background: var(--night); color: var(--ink); font-family: var(--font);
  overflow: hidden; overscroll-behavior: none; touch-action: none; user-select: none; -webkit-user-select: none;
}
#app { position: relative; width: 100%; height: 100%; overflow: hidden; background: var(--night); }
#c { position: absolute; inset: 0; width: 100%; height: 100%; display: block; }

#hud { position: absolute; inset: 0; pointer-events: none; }
#pill {
  position: absolute; top: 10px; left: 50%; transform: translateX(-50%);
  display: flex; align-items: center; gap: 12px; padding: 6px 12px; border-radius: 5px;
  background: var(--slate); font-size: 13px; font-weight: 600; letter-spacing: .06em; font-variant-numeric: tabular-nums;
  white-space: nowrap;
}
#pill .lbl { font-size: 9px; color: var(--ink-dim); letter-spacing: .14em; }
#pill b { font-weight: 700; font-size: 15px; }
.pips { display: flex; gap: 5px; }
.pip { width: 8px; height: 8px; transform: rotate(45deg); background: var(--off); }
.pip.cyan { background: var(--cyan); }
.pip.amber { background: var(--amber); }
.kills { display: flex; align-items: center; gap: 5px; color: var(--red); }
.kills svg { width: 10px; height: 10px; fill: var(--red); }

#warn {
  position: absolute; top: 56px; left: 50%; width: 34px; height: 34px; margin-left: -17px; opacity: 0;
}
#warn.on { animation: blink .5s steps(2, jump-none) infinite; }
#warn svg { width: 100%; height: 100%; filter: drop-shadow(0 0 6px rgba(255,164,58,.7)); }
@keyframes blink { 0% { opacity: 1; } 100% { opacity: .15; } }

#mach {
  position: absolute; left: 0; right: 0; top: 30%; text-align: center; opacity: 0;
  font-size: clamp(22px, 5vw, 34px); font-weight: 600; letter-spacing: .12em; text-shadow: 0 0 14px rgba(255,255,255,.55), 0 1px 0 rgba(0,0,0,.25);
}
#mach.show { animation: machin 1.8s ease-out; }
@keyframes machin {
  0% { opacity: 0; transform: scale(.94); }
  12% { opacity: 1; transform: scale(1); }
  70% { opacity: .9; }
  100% { opacity: 0; transform: scale(1.04); }
}

#lock { position: absolute; left: 0; top: 0; width: 46px; height: 46px; margin: -23px 0 0 -23px; display: none; color: var(--amber); }
#lock i { position: absolute; width: 10px; height: 10px; border: 0 solid currentColor; }
#lock i:nth-child(1) { left: 0; top: 0; border-width: 2px 0 0 2px; }
#lock i:nth-child(2) { right: 0; top: 0; border-width: 2px 2px 0 0; }
#lock i:nth-child(3) { left: 0; bottom: 0; border-width: 0 0 2px 2px; }
#lock i:nth-child(4) { right: 0; bottom: 0; border-width: 0 2px 2px 0; }
#lock span { position: absolute; left: 50%; top: 100%; transform: translateX(-50%); margin-top: 3px; font-size: 10px; font-weight: 600; letter-spacing: .08em; white-space: nowrap; }

#toast {
  position: absolute; left: 0; right: 0; top: 36%; text-align: center; font-size: 12px; font-weight: 600; letter-spacing: .18em; color: var(--amber); opacity: 0;
}
#toast.show { animation: toast 1.2s ease-out; }
@keyframes toast { 0% { opacity: 0; transform: translateY(6px); } 15% { opacity: 1; transform: none; } 75% { opacity: 1; } 100% { opacity: 0; transform: translateY(-6px); } }

#gauge {
  position: absolute; left: max(16px, env(safe-area-inset-left, 0px)); bottom: 16px; display: grid; grid-template-columns: auto auto; gap: 2px 12px;
  font-size: 10px; letter-spacing: .16em; color: var(--ink-dim); font-weight: 600;
}
#gauge b { color: var(--ink); font-size: 16px; letter-spacing: .04em; font-variant-numeric: tabular-nums; text-align: right; }
#vig { position: absolute; inset: 0; opacity: 0; background: radial-gradient(ellipse at center, rgba(255,40,20,0) 40%, rgba(255,40,20,.55) 100%); }

#touch { position: absolute; inset: 0; pointer-events: none; display: none; }
#touch.live { display: block; }
#stick { position: absolute; width: 110px; height: 110px; margin: -55px 0 0 -55px; border: 2px solid rgba(255,255,255,.35); border-radius: 50%; display: none; }
#stick i { position: absolute; left: 50%; top: 50%; width: 44px; height: 44px; margin: -22px 0 0 -22px; border-radius: 50%; background: rgba(255,255,255,.35); }
.btn {
  position: absolute; pointer-events: auto; border-radius: 50%; display: grid; place-items: center; font-family: var(--font); font-weight: 700; letter-spacing: .1em; font-size: 12px;
  color: var(--ink); background: rgba(22,28,40,.55); border: 2px solid rgba(255,255,255,.4); touch-action: none;
}
.btn.down { background: rgba(255,164,58,.55); }
#bFire { right: max(24px, env(safe-area-inset-right, 0px)); bottom: 164px; width: 72px; height: 72px; border-color: var(--red); }
#bBoost { right: max(16px, env(safe-area-inset-right, 0px)); bottom: 28px; width: 120px; height: 120px; font-size: 17px; border-color: var(--cyan); border-width: 3px; box-shadow: 0 0 18px rgba(79,216,255,.35); }
.btn.on { background: rgba(79,216,255,.5); box-shadow: 0 0 34px rgba(79,216,255,.9); color: #fff; }
#bBrake { right: calc(max(16px, env(safe-area-inset-right, 0px)) + 134px); bottom: 28px; width: 56px; height: 56px; font-size: 10px; }
#touch.nobtn .btn { display: none; }
#gear { position: absolute; z-index: 5; top: 8px; right: max(12px, env(safe-area-inset-right, 0px)); width: 40px; height: 40px; border: 0; border-radius: 5px; background: var(--slate); color: var(--ink); display: grid; place-items: center; cursor: pointer; }
#gear svg { width: 20px; height: 20px; stroke: currentColor; fill: none; stroke-width: 2; stroke-linecap: round; }
#gear:focus-visible, .go:focus-visible, .row input:focus-visible { outline: 3px solid var(--ink); outline-offset: 2px; }
#settings { z-index: 6; background: rgba(10,12,18,.9); justify-content: center; }
#settings .panel { display: flex; flex-direction: column; gap: 6px; max-width: 420px; }
.row { display: flex; align-items: center; justify-content: space-between; gap: 16px; padding: 14px 0; border-bottom: 1px solid rgba(255,255,255,.12); font-size: 15px; font-weight: 600; letter-spacing: .06em; }
.row small { display: block; margin-top: 3px; font-size: 11px; font-weight: 500; letter-spacing: .02em; color: var(--ink-dim); line-height: 1.35; }
.row input { appearance: none; -webkit-appearance: none; flex: none; width: 46px; height: 26px; border-radius: 13px; background: var(--off); position: relative; cursor: pointer; transition: background .15s; margin: 0; }
.row input::after { content: ''; position: absolute; top: 3px; left: 3px; width: 20px; height: 20px; border-radius: 50%; background: var(--ink); transition: transform .15s; }
.row input:checked { background: var(--cyan); }
.row input:checked::after { transform: translateX(20px); }
#fx { position: absolute; inset: 0; width: 100%; height: 100%; }
#svig { position: absolute; inset: 0; opacity: 0; background: radial-gradient(ellipse at center, rgba(8,14,30,0) 35%, rgba(8,14,30,.75) 100%); }
#flash { position: absolute; inset: 0; opacity: 0; background: radial-gradient(circle at center, rgba(255,255,255,.9), rgba(160,220,255,.55) 60%, rgba(160,220,255,0)); }

.screen {
  position: absolute; inset: 0; display: flex; flex-direction: column; justify-content: flex-end; gap: 14px;
  padding: 24px max(20px, env(safe-area-inset-right, 0px)) max(24px, env(safe-area-inset-bottom, 0px)) max(20px, env(safe-area-inset-left, 0px));
  background: linear-gradient(to top, rgba(10,12,18,.94) 0%, rgba(10,12,18,.7) 45%, rgba(10,12,18,0) 80%);
}
.screen[hidden] { display: none; }
.eyebrow { font-size: 11px; letter-spacing: .28em; color: var(--amber); font-weight: 600; }
h1, h2 { margin: 0; font-style: italic; font-weight: 700; line-height: .9; text-transform: uppercase; text-wrap: balance; }
h1 { font-size: clamp(64px, 20vw, 132px); letter-spacing: .02em; }
h2 { font-size: clamp(44px, 13vw, 84px); }
.tag { margin: 0; font-size: 15px; color: var(--ink-dim); max-width: 34ch; line-height: 1.4; }
.keys { display: grid; grid-template-columns: repeat(auto-fit, minmax(140px, 1fr)); gap: 8px 20px; max-width: 520px; font-size: 12px; color: var(--ink-dim); }
.keys div { min-width: 0; line-height: 1.35; }
.keys kbd { font-family: var(--font); font-weight: 700; color: var(--ink); }
.go {
  align-self: flex-start; font-family: var(--font); font-weight: 700; font-size: 18px; letter-spacing: .2em; padding: 14px 30px; border: 0; border-radius: 4px;
  background: var(--amber); color: #1a1208; cursor: pointer; pointer-events: auto;
}
.go:hover { background: #ffb85c; }
.go:focus-visible { outline: 3px solid var(--ink); outline-offset: 3px; }
.stats { display: grid; grid-template-columns: repeat(2, minmax(0, 120px)); gap: 10px 28px; font-size: 10px; letter-spacing: .16em; color: var(--ink-dim); font-weight: 600; }
.stats b { display: block; font-size: 24px; color: var(--ink); letter-spacing: .02em; font-variant-numeric: tabular-nums; }
@media (prefers-reduced-motion: reduce) { #mach.show, #toast.show, #warn.on { animation-duration: .01s; } }
</style>

<div id="app">
  <canvas id="c"></canvas>
  <div id="hud">
    <div id="svig"></div>
    <canvas id="fx"></canvas>
    <div id="flash"></div>
    <div id="pill" aria-label="Status">
      <span class="lbl">LIFE</span><b id="lives">4</b>
      <span class="pips"><i class="pip cyan"></i><i class="pip cyan"></i><i class="pip cyan"></i></span>
      <span class="kills"><svg viewBox="0 0 10 10"><path d="M5 9 L0 1 H10 Z"/></svg><b id="kills">0</b></span>
    </div>
    <div id="warn"><svg viewBox="0 0 34 34"><path d="M17 3 L32 30 H2 Z" fill="#ffa43a"/><rect x="15.6" y="12" width="2.8" height="10" fill="#3a2108"/><rect x="15.6" y="24" width="2.8" height="2.8" fill="#3a2108"/></svg></div>
    <div id="mach"></div>
    <div id="toast"></div>
    <div id="lock"><i></i><i></i><i></i><i></i><span id="lockd"></span></div>
    <div id="gauge"><span>MACH</span><b id="gm">2.0</b><span>ALT</span><b id="ga">90</b><span>SCORE</span><b id="gs">0</b></div>
    <div id="vig"></div>
  </div>
  <div id="touch">
    <div id="stick"><i></i></div>
    <div class="btn" id="bBoost">BOOST</div>
    <div class="btn" id="bFire">FIRE</div>
    <div class="btn" id="bBrake">BRAKE</div>
  </div>

  <button id="gear" aria-label="Settings"><svg viewBox="0 0 24 24"><path d="M4 6h10M18 6h2M4 12h4M12 12h8M4 18h12M20 18h0"/><circle cx="16" cy="6" r="2"/><circle cx="10" cy="12" r="2"/><circle cx="18" cy="18" r="2"/></svg></button>

  <div class="screen" id="title">
    <div class="eyebrow">DESERT SPEED RUN</div>
    <h1>Faster</h1>
    <p class="tag">Games never felt fast enough. Hold the throttle, stay low, outrun everything that shoots back.</p>
    <div class="keys">
      <div><kbd>Mouse</kbd> or <kbd>WASD</kbd> steer</div>
      <div><kbd>Shift</kbd> or the BOOST button to go Mach 12</div>
      <div><kbd>Space</kbd> or click to fire</div>
      <div><kbd>Q</kbd> brake</div>
      <div><kbd>Touch</kbd> drag left side to steer, hold the buttons</div>
    </div>
    <button class="go" id="launch">LAUNCH</button>
  </div>

  <div class="screen" id="settings" hidden>
    <div class="panel">
      <div class="eyebrow">SETTINGS</div>
      <label class="row"><span>On-screen buttons<small>Off: hold the right side of the screen to fire, double-tap it to toggle boost.</small></span><input type="checkbox" id="sButtons"></label>
      <label class="row"><span>Speed lines<small>Radial streaks and edge darkening at high Mach.</small></span><input type="checkbox" id="sFx"></label>
      <label class="row"><span>Sound</span><input type="checkbox" id="sSound"></label>
      <button class="go" id="sClose" style="margin-top:16px">RESUME</button>
    </div>
  </div>

  <div class="screen" id="over" hidden>
    <div class="eyebrow">SORTIE ENDED</div>
    <h2>Shot down</h2>
    <div class="stats">
      <div>SCORE<b id="oScore">0</b></div>
      <div>BEST<b id="oBest">0</b></div>
      <div>KILLS<b id="oKills">0</b></div>
      <div>TOP SPEED<b id="oMach">0</b></div>
    </div>
    <button class="go" id="again">FLY AGAIN</button>
  </div>
</div>

<script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
<script>
(() => {
'use strict';
const T = window.THREE;
const V3 = T.Vector3;
const MACH = 100;                // world units per second at Mach 1
const CELL = 700, RAD = 4;       // terrain chunk size / load radius
const START = new V3(0, 90, 0);
const clamp = (v, a, b) => Math.max(a, Math.min(b, v));
const lerp = (a, b, t) => a + (b - a) * t;
const rnd = (a, b) => a + Math.random() * (b - a);

/* ---------- DOM ---------- */
const $ = id => document.getElementById(id);
const app = $('app'), canvas = $('c');
const el = {
  lives: $('lives'), kills: $('kills'), pips: Array.from(document.querySelectorAll('.pip')),
  mach: $('mach'), warn: $('warn'), lock: $('lock'), lockd: $('lockd'), toast: $('toast'),
  gm: $('gm'), ga: $('ga'), gs: $('gs'), vig: $('vig'), title: $('title'), over: $('over'), touch: $('touch'),
  stick: $('stick'),
};
const settings = { buttons: true, fx: true, sound: true }, tfire = { id: -1, last: 0 };
try { Object.assign(settings, JSON.parse(localStorage.getItem('faster-settings') || '{}')); } catch (e) { /* defaults */ }
let paused = false;
let best = 0;
try { best = parseInt(localStorage.getItem('faster-best') || '0', 10) || 0; } catch (e) { best = 0; }

/* ---------- renderer / scene ---------- */
const renderer = new T.WebGLRenderer({ canvas, antialias: true, powerPreference: 'high-performance' });
renderer.setPixelRatio(Math.min(window.devicePixelRatio || 1, 2));
const scene = new T.Scene();
const HORIZON = 0xeddcc2;
scene.fog = new T.Fog(HORIZON, 400, 3000);
const camera = new T.PerspectiveCamera(72, 1, 0.5, 9000);
let baseFov = 72;

scene.add(new T.HemisphereLight(0xcfe0ff, 0xc99a6a, 0.62));
const sun = new T.DirectionalLight(0xfff1d6, 0.8);
const sunDir = new V3(-0.5, 0.7, 0.35).normalize();
sun.position.copy(sunDir).multiplyScalar(500);
scene.add(sun);

// sky dome
const sky = new T.Mesh(
  new T.SphereGeometry(4000, 24, 16),
  new T.ShaderMaterial({
    side: T.BackSide, depthWrite: false, fog: false,
    uniforms: {
      top: { value: new T.Color(0x3a72c2) }, mid: { value: new T.Color(0x9cc0e8) },
      hor: { value: new T.Color(HORIZON) }, sunDir: { value: sunDir },
    },
    vertexShader: 'varying vec3 vDir; void main(){ vDir = normalize(position); gl_Position = projectionMatrix * modelViewMatrix * vec4(position,1.0); }',
    fragmentShader: 'uniform vec3 top; uniform vec3 mid; uniform vec3 hor; uniform vec3 sunDir; varying vec3 vDir;' +
      'void main(){ float h = clamp(vDir.y, -0.2, 1.0); vec3 c = mix(hor, mid, smoothstep(0.0, 0.22, h));' +
      'c = mix(c, top, smoothstep(0.18, 0.85, h)); float s = max(dot(normalize(vDir), sunDir), 0.0);' +
      'c += vec3(1.0,0.85,0.6) * pow(s, 18.0) * 0.45 + vec3(1.0,0.92,0.75) * pow(s, 300.0) * 1.4; gl_FragColor = vec4(c, 1.0); }',
  })
);
sky.renderOrder = -10; sky.frustumCulled = false;
scene.add(sky);

// sand ground
function sandTexture() {
  const s = 256, c = document.createElement('canvas'); c.width = c.height = s;
  const g = c.getContext('2d');
  g.fillStyle = '#d9a164'; g.fillRect(0, 0, s, s);
  const dot = (x, y, r, col) => {
    g.fillStyle = col;
    for (let ox = -1; ox <= 1; ox++) for (let oy = -1; oy <= 1; oy++) { g.beginPath(); g.arc(x + ox * s, y + oy * s, r, 0, 6.2832); g.fill(); }
  };
  for (let i = 0; i < 700; i++) dot(Math.random() * s, Math.random() * s, rnd(2, 9), 'rgba(' + (Math.random() < .5 ? '236,190,130' : '190,134,82') + ',0.10)');
  for (let i = 0; i < 900; i++) dot(Math.random() * s, Math.random() * s, rnd(.5, 1.6), 'rgba(120,76,44,0.35)');
  for (let i = 0; i < 400; i++) dot(Math.random() * s, Math.random() * s, rnd(.5, 1.4), 'rgba(250,220,170,0.35)');
  const t = new T.CanvasTexture(c);
  t.wrapS = t.wrapT = T.RepeatWrapping; t.anisotropy = 8;
  return t;
}
const TILE = 50, GSIZE = 7000;
const gtex = sandTexture(); gtex.repeat.set(GSIZE / TILE, GSIZE / TILE);
const ground = new T.Mesh(new T.PlaneGeometry(GSIZE, GSIZE), new T.MeshLambertMaterial({ map: gtex }));
ground.rotation.x = -Math.PI / 2;
scene.add(ground);

// clouds
function cloudTexture() {
  const c = document.createElement('canvas'); c.width = 256; c.height = 128;
  const g = c.getContext('2d');
  for (let i = 0; i < 26; i++) {
    const x = rnd(40, 216), y = rnd(46, 88), r = rnd(18, 44);
    const gr = g.createRadialGradient(x, y, 0, x, y, r);
    gr.addColorStop(0, 'rgba(255,255,255,0.55)'); gr.addColorStop(1, 'rgba(255,255,255,0)');
    g.fillStyle = gr; g.fillRect(0, 0, 256, 128);
  }
  return new T.CanvasTexture(c);
}
const clouds = [];
{
  const ct = cloudTexture();
  for (let i = 0; i < 16; i++) {
    const s = new T.Sprite(new T.SpriteMaterial({ map: ct, fog: false, transparent: true, depthWrite: false, opacity: rnd(.7, 1) }));
    s.scale.set(rnd(800, 1500), rnd(280, 460), 1);
    s.position.set(rnd(-3000, 3000), rnd(450, 900), rnd(-3000, 3000));
    scene.add(s); clouds.push(s);
  }
}

/* ---------- particles (sprite pools) ---------- */
function glowTexture() {
  const c = document.createElement('canvas'); c.width = c.height = 64;
  const g = c.getContext('2d'), gr = g.createRadialGradient(32, 32, 0, 32, 32, 32);
  gr.addColorStop(0, 'rgba(255,255,255,1)'); gr.addColorStop(.35, 'rgba(255,255,255,.6)'); gr.addColorStop(1, 'rgba(255,255,255,0)');
  g.fillStyle = gr; g.fillRect(0, 0, 64, 64);
  return new T.CanvasTexture(c);
}
const glowTex = glowTexture();
function makePool(n, additive) {
  const items = [];
  for (let i = 0; i < n; i++) {
    const m = new T.SpriteMaterial({ map: glowTex, transparent: true, depthWrite: false, blending: additive ? T.AdditiveBlending : T.NormalBlending, opacity: 0 });
    const s = new T.Sprite(m); s.visible = false; scene.add(s);
    items.push({ s, on: false, life: 0, max: 1, vel: new V3(), s0: 1, s1: 1, c0: new T.Color(), c1: new T.Color(), o: 1, drag: 0 });
  }
  return { items, next: 0 };
}
const fireP = makePool(140, true), smokeP = makePool(110, false);
function emit(pool, pos, vel, life, s0, s1, c0, c1, o, drag) {
  let it = null;
  for (let k = 0; k < pool.items.length; k++) { const c = pool.items[(pool.next + k) % pool.items.length]; if (!c.on) { it = c; pool.next = (pool.next + k + 1) % pool.items.length; break; } }
  if (!it) { it = pool.items[pool.next]; pool.next = (pool.next + 1) % pool.items.length; }
  it.on = true; it.life = it.max = life; it.s.position.copy(pos); it.vel.copy(vel); it.s0 = s0; it.s1 = s1;
  it.c0.set(c0); it.c1.set(c1); it.o = o; it.drag = drag || 0; it.s.visible = true;
}
function updatePool(pool, dt) {
  for (const it of pool.items) {
    if (!it.on) continue;
    it.life -= dt;
    if (it.life <= 0) { it.on = false; it.s.visible = false; continue; }
    const t = 1 - it.life / it.max;
    it.s.position.addScaledVector(it.vel, dt);
    if (it.drag) it.vel.multiplyScalar(Math.max(0, 1 - it.drag * dt));
    const sc = lerp(it.s0, it.s1, t); it.s.scale.set(sc, sc, 1);
    it.s.material.color.copy(it.c0).lerp(it.c1, t);
    it.s.material.opacity = it.o * (1 - t);
  }
}
const tv = new V3(), tv2 = new V3(), tv3 = new V3();
function randDir(out) { out.set(rnd(-1, 1), rnd(-.3, 1), rnd(-1, 1)); if (out.lengthSq() < 1e-4) out.set(0, 1, 0); return out.normalize(); }
function explosion(pos, size) {
  const v = new V3();
  for (let i = 0; i < 16; i++) emit(fireP, pos, randDir(v).multiplyScalar(size * rnd(2, 7)), rnd(.5, .95), size * .8, size * 3.4, 0xffe08a, 0xff3a10, .95, 1.5);
  for (let i = 0; i < 10; i++) { randDir(v); v.y = Math.abs(v.y) + .4; emit(smokeP, pos, v.multiplyScalar(size * rnd(1, 3)), rnd(1.6, 2.8), size * 1.6, size * 5.5, 0x3a3532, 0x6a625a, .7, 1.1); }
  emit(fireP, pos, tv.set(0, 0, 0), .22, size * 1.5, size * 8, 0xffffff, 0xffc060, 1, 0);
  const d = pos.distanceTo(P.pos);
  shake = Math.max(shake, clamp(size * 18 / (d + 30), 0, 1.2));
  sfx('boom', clamp(1 - d / 2200, .15, 1));
}
function puff(pos, size) { emit(fireP, pos, tv.set(0, 0, 0), .25, size * .6, size * 2, 0xffe9b0, 0xff6a20, .9, 0); }

/* ---------- audio ---------- */
const A = { ctx: null };
function audioInit() {
  if (A.ctx) { if (A.ctx.state === 'suspended') A.ctx.resume(); return; }
  try {
    const ctx = new (window.AudioContext || window.webkitAudioContext)(); A.ctx = ctx;
    const len = ctx.sampleRate * 2, buf = ctx.createBuffer(1, len, ctx.sampleRate), d = buf.getChannelData(0);
    let last = 0;
    for (let i = 0; i < len; i++) { last = (last + 0.02 * (Math.random() * 2 - 1)) / 1.02; d[i] = clamp(last * 3.5, -1, 1); }
    A.buf = buf;
    const src = ctx.createBufferSource(); src.buffer = buf; src.loop = true;
    A.f = ctx.createBiquadFilter(); A.f.type = 'lowpass'; A.f.frequency.value = 300;
    A.g = ctx.createGain(); A.g.gain.value = 0;
    src.connect(A.f); A.f.connect(A.g); A.g.connect(ctx.destination); src.start();
    A.o = ctx.createOscillator(); A.o.type = 'sawtooth'; A.o.frequency.value = 50;
    const og = ctx.createGain(); og.gain.value = 0.05; A.o.connect(og); og.connect(A.f); A.o.start();
  } catch (e) { A.ctx = null; }
}
function audioUpdate(frac, on) {
  if (!A.ctx) return;
  const t = A.ctx.currentTime;
  A.f.frequency.setTargetAtTime(250 + frac * 3400, t, .1);
  A.g.gain.setTargetAtTime(!settings.sound ? 0 : (on ? .22 + frac * .4 : 0.05), t, .15);
  A.o.frequency.setTargetAtTime(45 + frac * 95, t, .1);
}
function sfx(kind, vol) {
  if (!A.ctx || !settings.sound) return;
  const ctx = A.ctx, t = ctx.currentTime, v = vol == null ? 1 : vol;
  try {
    if (kind === 'beep') {
      const o = ctx.createOscillator(), g = ctx.createGain(); o.type = 'square'; o.frequency.value = 900;
      g.gain.setValueAtTime(.04, t); g.gain.exponentialRampToValueAtTime(.001, t + .09);
      o.connect(g); g.connect(ctx.destination); o.start(t); o.stop(t + .1); return;
    }
    const s = ctx.createBufferSource(), f = ctx.createBiquadFilter(), g = ctx.createGain();
    s.buffer = A.buf;
    if (kind === 'shot') {
      s.playbackRate.value = 3; f.type = 'bandpass'; f.frequency.value = 1800;
      g.gain.setValueAtTime(.16 * v, t); g.gain.exponentialRampToValueAtTime(.001, t + .07);
      s.connect(f); f.connect(g); g.connect(ctx.destination); s.start(t, Math.random() * 1.5); s.stop(t + .08);
    } else if (kind === 'whoosh') {
      s.playbackRate.value = 1.5; f.type = 'bandpass'; f.Q.value = 1.2; f.frequency.setValueAtTime(300, t); f.frequency.exponentialRampToValueAtTime(4000, t + .5);
      g.gain.setValueAtTime(.001, t); g.gain.exponentialRampToValueAtTime(.9 * v, t + .18); g.gain.exponentialRampToValueAtTime(.001, t + .8);
      s.connect(f); f.connect(g); g.connect(ctx.destination); s.start(t, Math.random()); s.stop(t + .85);
    } else if (kind === 'hit') {
      f.type = 'bandpass'; f.frequency.value = 700;
      g.gain.setValueAtTime(.5 * v, t); g.gain.exponentialRampToValueAtTime(.001, t + .25);
      s.connect(f); f.connect(g); g.connect(ctx.destination); s.start(t, Math.random() * 1.5); s.stop(t + .3);
    } else {
      f.type = 'lowpass'; f.frequency.setValueAtTime(900, t); f.frequency.exponentialRampToValueAtTime(70, t + 1);
      g.gain.setValueAtTime(.9 * v, t); g.gain.exponentialRampToValueAtTime(.001, t + 1.1);
      s.connect(f); f.connect(g); g.connect(ctx.destination); s.start(t, Math.random() * .8); s.stop(t + 1.2);
    }
  } catch (e) { /* audio is optional */ }
}

/* ---------- player ship ---------- */
const flameGeo = new T.ConeGeometry(1, 1, 10, 1, true);
flameGeo.translate(0, .5, 0); flameGeo.rotateX(Math.PI / 2);   // base at origin, tip toward +Z (backward)
function flameMat(col, op) { return new T.MeshBasicMaterial({ color: col, transparent: true, opacity: op, blending: T.AdditiveBlending, depthWrite: false, side: T.DoubleSide }); }
const shipG = new T.Group(), flames = [];
{
  const body = new T.MeshStandardMaterial({ color: 0xd0763a, roughness: .55, metalness: .3, flatShading: true });
  const dark = new T.MeshStandardMaterial({ color: 0x2c2f36, roughness: .5, metalness: .6, flatShading: true });
  const blue = new T.MeshStandardMaterial({ color: 0x2f6fd0, roughness: .4, metalness: .2, emissive: 0x0a2a66 });
  const pods = [[0, .75], [-.9, -.5], [.9, -.5]];
  for (const [x, y] of pods) {
    const cyl = new T.Mesh(new T.CylinderGeometry(.6, .6, 5.2, 10), body); cyl.rotation.x = Math.PI / 2; cyl.position.set(x, y, 0);
    const nose = new T.Mesh(new T.ConeGeometry(.6, 1.9, 10), dark); nose.rotation.x = -Math.PI / 2; nose.position.set(x, y, -3.5);
    const ring = new T.Mesh(new T.CylinderGeometry(.66, .66, .5, 10), blue); ring.rotation.x = Math.PI / 2; ring.position.set(x, y, 1.5);
    const noz = new T.Mesh(new T.CylinderGeometry(.5, .64, .7, 10), dark); noz.rotation.x = Math.PI / 2; noz.position.set(x, y, 2.85);
    shipG.add(cyl, nose, ring, noz);
    const inner = new T.Mesh(flameGeo, flameMat(0xfff2c8, .95)), outer = new T.Mesh(flameGeo, flameMat(0xff8a2a, .7)), trail = new T.Mesh(flameGeo, flameMat(0xe08cff, .32));
    for (const m of [inner, outer, trail]) { m.position.set(x, y, 3.2); shipG.add(m); }
    flames.push({ inner, outer, trail });
  }
  for (const sx of [-1, 1]) {
    const w = new T.Mesh(new T.BoxGeometry(3.6, .12, 1.8), dark); w.position.set(sx * 2.3, -.1, 1); w.rotation.y = sx * .35; shipG.add(w);
  }
  const fin = new T.Mesh(new T.BoxGeometry(.12, 1.7, 1.8), dark); fin.position.set(0, 1.7, 1.8); shipG.add(fin);
}
shipG.rotation.order = 'YXZ';
scene.add(shipG);

/* ---------- speed streaks ---------- */
const NS = 520;
const streakPos = new Float32Array(NS * 6), streakW = [];
for (let i = 0; i < NS; i++) streakW.push({ p: new V3(0, -9999, 0), k: rnd(.5, 1) });
const streakGeo = new T.BufferGeometry();
streakGeo.setAttribute('position', new T.BufferAttribute(streakPos, 3));
const streakMat = new T.LineBasicMaterial({ color: 0xffffff, transparent: true, opacity: 0, blending: T.AdditiveBlending, depthWrite: false, fog: false });
const streaks = new T.LineSegments(streakGeo, streakMat); streaks.frustumCulled = false; scene.add(streaks);

/* ---------- terrain chunks ---------- */
const rockGeo = new T.DodecahedronGeometry(1, 0);
const rockMat = new T.MeshStandardMaterial({ color: 0x8a4b2e, roughness: 1, flatShading: true });
const mesaMat = new T.MeshStandardMaterial({ vertexColors: true, roughness: 1, flatShading: true });
const cells = new Map(), mesas = [], enemies = [];
function mulberry(a) { return function () { a |= 0; a = a + 0x6D2B79F5 | 0; let t = Math.imul(a ^ a >>> 15, 1 | a); t = t + Math.imul(t ^ t >>> 7, 61 | t) ^ t; return ((t ^ t >>> 14) >>> 0) / 4294967296; }; }
function makeMesa(rBot, rTop, h, seed) {
  const geo = new T.CylinderGeometry(rTop, rBot, h, 10, 6, false);
  geo.translate(0, h / 2, 0);
  const pos = geo.attributes.position, col = new Float32Array(pos.count * 3), c0 = new T.Color(0x6e301c), c1 = new T.Color(0xcc6c3c), c = new T.Color();
  for (let i = 0; i < pos.count; i++) {
    const x = pos.getX(i), y = pos.getY(i), z = pos.getZ(i), ang = Math.atan2(z, x);
    const n = 1 + Math.sin(ang * 3 + y * .05 + seed) * .13 + Math.sin(ang * 7 + y * .11 + seed * 2) * .07;
    pos.setX(i, x * n); pos.setZ(i, z * n);
    const f = y / h, band = Math.sin(y * .16 + seed) * .06;
    c.copy(c0).lerp(c1, clamp(f * .9 + band, 0, 1));
    col[i * 3] = c.r; col[i * 3 + 1] = c.g; col[i * 3 + 2] = c.b;
  }
  geo.setAttribute('color', new T.BufferAttribute(col, 3));
  geo.computeVertexNormals();
  return geo;
}
function createCell(cx, cz, early) {
  const r = mulberry(((cx * 73856093) ^ (cz * 19349663)) >>> 0);
  const g = new T.Group(), cell = { cx, cz, g, mesas: [], enemies: [], geos: [], inst: null };
  const ox = cx * CELL, oz = cz * CELL, dStart = Math.hypot(ox + CELL / 2 - START.x, oz + CELL / 2 - START.z);
  const addMesa = (x, z, rb, rt, h) => {
    if (Math.abs(x) < 260 && z < 0) return;   // keep the launch lane clear
    const geo = makeMesa(rb, rt, h, r() * 10), m = new T.Mesh(geo, mesaMat); m.position.set(x, 0, z); g.add(m);
    const e = { x, z, rb, rt, h }; mesas.push(e); cell.mesas.push(e); cell.geos.push(geo);
  };
  if (r() < .55 && dStart > 650) {
    const x = ox + rnd0(r, 120, CELL - 120), z = oz + rnd0(r, 120, CELL - 120), rb = rnd0(r, 45, 140), h = rnd0(r, 70, 250);
    addMesa(x, z, rb, rb * rnd0(r, .55, .85), h);
    const n = Math.floor(r() * 3);
    for (let i = 0; i < n; i++) {
      const a = r() * 6.28, d = rb * rnd0(r, 1.1, 1.8), rb2 = rnd0(r, 14, 34);
      addMesa(x + Math.cos(a) * d, z + Math.sin(a) * d, rb2, rb2 * .7, rnd0(r, 20, 70));
    }
  }
  const NR = 46, inst = new T.InstancedMesh(rockGeo, rockMat, NR), m4 = new T.Matrix4(), q = new T.Quaternion(), e = new T.Euler(), sc = new V3(), p = new V3();
  for (let i = 0; i < NR; i++) {
    const big = i < 6, s = big ? rnd0(r, 3, 9) : rnd0(r, .5, 2.6);
    e.set(r() * 3, r() * 3, r() * 3); q.setFromEuler(e);
    sc.set(s, s * rnd0(r, .5, .9), s * rnd0(r, .8, 1.3)); p.set(ox + r() * CELL, s * .3, oz + r() * CELL);
    m4.compose(p, q, sc); inst.setMatrixAt(i, m4);
  }
  inst.frustumCulled = false; g.add(inst); cell.inst = inst;
  const wr = r(), ramp = Math.min(1, game.t / 120);
  if (!early && dStart > 900 && wr < .12 + .1 * ramp && game.mode === 'play') {
    const w = spawnWalker(ox + rnd0(r, 60, CELL - 60), oz + rnd0(r, 60, CELL - 60)); w.cell = cell; cell.enemies.push(w);
  }
  scene.add(g); cells.set(cx + ',' + cz, cell);
}
function rnd0(r, a, b) { return a + r() * (b - a); }
function removeCell(key) {
  const c = cells.get(key); if (!c) return;
  scene.remove(c.g);
  for (const g of c.geos) g.dispose();
  c.inst.dispose();
  for (const m of c.mesas) { const i = mesas.indexOf(m); if (i >= 0) mesas.splice(i, 1); }
  for (const w of c.enemies.slice()) if (w.alive) killEnemy(w, true);
  cells.delete(key);
}
function updateCells(all) {
  const pcx = Math.floor(P.pos.x / CELL), pcz = Math.floor(P.pos.z / CELL);
  let made = 0;
  for (let dx = -RAD; dx <= RAD; dx++) for (let dz = -RAD; dz <= RAD; dz++) {
    const k = (pcx + dx) + ',' + (pcz + dz);
    if (!cells.has(k)) { if (!all && made >= 5) continue; createCell(pcx + dx, pcz + dz, all); made++; }
  }
  for (const [k, c] of cells) if (Math.abs(c.cx - pcx) > RAD + 1 || Math.abs(c.cz - pcz) > RAD + 1) removeCell(k);
}

/* ---------- enemies ---------- */
function limb(a, b, rad, mat) {
  const d = tv.copy(b).sub(a), len = d.length(), m = new T.Mesh(new T.CylinderGeometry(rad, rad * .7, 1, 5), mat);
  m.position.copy(a).addScaledVector(d, .5); m.scale.y = len; m.quaternion.setFromUnitVectors(new V3(0, 1, 0), d.normalize());
  return m;
}
const walkerMat = new T.MeshStandardMaterial({ color: 0x23201f, roughness: .6, metalness: .5, flatShading: true });
const coreMat = new T.MeshBasicMaterial({ color: 0xff5a1a });
const walkerGeo = { body: new T.SphereGeometry(3.4, 8, 6) };
function walkerModel() {
  const g = new T.Group(), body = new T.Mesh(walkerGeo.body, walkerMat);
  body.scale.set(1.3, .8, 1.3); body.position.y = 13; g.add(body);
  const core = new T.Mesh(new T.SphereGeometry(1.5, 8, 6), coreMat); core.position.set(0, 12.6, 2.8); g.add(core);
  for (const sx of [-1, 1]) for (const sz of [-1, 1]) {
    const hip = new V3(sx * 2.4, 12.5, sz * 2.4), knee = new V3(sx * 8, 16, sz * 8), foot = new V3(sx * 11, 0, sz * 11);
    g.add(limb(hip, knee, .45, walkerMat), limb(knee, foot, .4, walkerMat));
  }
  return { g, core };
}
function spawnWalker(x, z) {
  const m = walkerModel(); m.g.position.set(x, 0, z); scene.add(m.g);
  const w = { type: 'walker', alive: true, pos: new V3(x, 8, z), vel: new V3(), hp: 6, hp0: 6, rad: 13, mesh: m.g, core: m.core, cd: rnd(2, 4), smoke: 0, cell: null };
  enemies.push(w); return w;
}
const droneBody = new T.MeshStandardMaterial({ color: 0x3a3d46, roughness: .5, metalness: .5, flatShading: true });
function spawnDrone() {
  const g = new T.Group();
  g.add(new T.Mesh(new T.BoxGeometry(1.3, .8, 4.6), droneBody));
  for (const sx of [-1, 1]) { const w = new T.Mesh(new T.BoxGeometry(4.2, .12, 1.4), droneBody); w.position.set(sx * 2.4, 0, .6); w.rotation.y = -sx * .4; g.add(w); }
  const glow = new T.Mesh(flameGeo, flameMat(0xff7a2a, .9)); glow.position.z = -2.2; glow.rotation.y = Math.PI; glow.scale.set(.5, .5, 4); g.add(glow);
  const f = P.f.clone(); f.y = 0; if (f.lengthSq() < .01) f.set(0, 0, -1); f.normalize();
  const side = new V3(-f.z, 0, f.x), pos = P.pos.clone().addScaledVector(f, rnd(2300, 2900)).addScaledVector(side, rnd(-700, 700));
  pos.y = rnd(50, 200); g.position.copy(pos); scene.add(g);
  const d = { type: 'drone', alive: true, pos, vel: f.clone().multiplyScalar(-300), hp: 3, hp0: 3, rad: 7, mesh: g, mode: 'attack', timer: 0, evade: new V3(), cd: rnd(.5, 1.5), burst: 0, burstT: 0 };
  enemies.push(d); return d;
}
function killEnemy(e, silent) {
  if (!e.alive) return;
  e.alive = false; scene.remove(e.mesh);
  if (e.cell) { const i = e.cell.enemies.indexOf(e); if (i >= 0) e.cell.enemies.splice(i, 1); }
  const i = enemies.indexOf(e); if (i >= 0) enemies.splice(i, 1);
  if (silent) return;
  explosion(e.pos, e.type === 'walker' ? 9 : 5);
  const pts = e.type === 'walker' ? 150 : 100;
  game.score += pts; game.kills++;
  toast((e.type === 'walker' ? 'WALKER DOWN' : 'DRONE DOWN') + '  +' + pts);
}

// projectiles
const bulletGeo = new T.BoxGeometry(.28, .28, 10);
const pBullets = [], eBullets = [], missiles = [];
const pbMat = new T.MeshBasicMaterial({ color: 0xffa040, blending: T.AdditiveBlending, transparent: true, depthWrite: false });
const ebMat = new T.MeshBasicMaterial({ color: 0xff3a7a, blending: T.AdditiveBlending, transparent: true, depthWrite: false });
for (let i = 0; i < 70; i++) { const m = new T.Mesh(bulletGeo, pbMat); m.visible = false; scene.add(m); pBullets.push({ m, on: false, life: 0, vel: new V3(), prev: new V3() }); }
for (let i = 0; i < 40; i++) { const m = new T.Mesh(bulletGeo, ebMat); m.visible = false; m.scale.set(1.4, 1.4, 1); scene.add(m); eBullets.push({ m, on: false, life: 0, vel: new V3() }); }
const missileGeo = new T.SphereGeometry(1.3, 8, 6), missileMat = new T.MeshBasicMaterial({ color: 0xffb060 });
function spawnMissile(from, dir) {
  const m = new T.Mesh(missileGeo, missileMat); m.position.copy(from); scene.add(m);
  missiles.push({ m, pos: m.position, dir: dir.clone().normalize(), speed: 160, life: 8, hp: 1, rad: 5, trailT: 0 });
}
function segHitsSphere(p0, p1, c, r) {
  tv3.copy(p1).sub(p0);
  const l2 = tv3.lengthSq(), t = l2 > 0 ? clamp(tv2.copy(c).sub(p0).dot(tv3) / l2, 0, 1) : 0;
  tv2.copy(p0).addScaledVector(tv3, t);
  return tv2.distanceToSquared(c) < r * r;
}

/* ---------- game state ---------- */
const game = { mode: 'title', t: 0, score: 0, kills: 0, lives: 4, topMach: 0, droneT: 5, machShown: 0, overT: 0, warnBeep: 0 };
const P = {
  pos: START.clone(), yaw: 0, pitch: 0, roll: 0, speed: 3 * MACH, f: new V3(0, 0, -1), vel: new V3(),
  hull: 3, invuln: 0, dead: 0, fireCd: 0, gunSide: 1, dustT: 0,
};
const camF = new V3(0, 0, -1);
let shake = 0, fov = 72, flashV = 0, cockpitT = 0;

function forwardFrom(yaw, pitch, out) { const cp = Math.cos(pitch); return out.set(-Math.sin(yaw) * cp, Math.sin(pitch), -Math.cos(yaw) * cp); }

function resetGame() {
  for (const e of enemies.slice()) killEnemy(e, true);
  for (const k of Array.from(cells.keys())) removeCell(k);
  for (const l of [pBullets, eBullets]) for (const b of l) { b.on = false; b.m.visible = false; }
  for (const m of missiles) scene.remove(m.m);
  missiles.length = 0;
  for (const pool of [fireP, smokeP]) for (const it of pool.items) { it.on = false; it.s.visible = false; }
  game.t = 0; game.score = 0; game.kills = 0; game.lives = 4; game.topMach = 0; game.droneT = 6; game.machShown = 0;
  P.pos.copy(START); P.yaw = 0; P.pitch = 0; P.roll = 0; P.speed = 3 * MACH; P.hull = 3; P.invuln = 2; P.dead = 0; P.fireCd = 0;
  forwardFrom(0, 0, P.f); camF.copy(P.f);
  shipG.visible = true;
}
function toast(msg) { el.toast.textContent = msg; el.toast.classList.remove('show'); void el.toast.offsetWidth; el.toast.classList.add('show'); }
function hurt(n) {
  if (P.invuln > 0 || P.dead > 0 || game.mode !== 'play') return;
  P.hull -= n; P.invuln = 1.3; flashV = 1; shake = Math.max(shake, .8); sfx('hit');
  if (P.hull <= 0) die();
}
function die() {
  if (P.dead > 0) return;
  explosion(P.pos, 12); P.dead = 2; P.hull = 0; game.lives--; shipG.visible = false;
}
function respawn() {
  P.hull = 3; P.invuln = 2.5; P.pos.y = 320; P.pitch = -.12; P.roll = 0; P.speed = 3 * MACH; boostLatch = false; $('bBoost').classList.remove('on'); shipG.visible = true;
  camF.copy(forwardFrom(P.yaw, P.pitch, P.f));
  for (const m of missiles) scene.remove(m.m);
  missiles.length = 0;
}
function endGame() {
  game.mode = 'over'; P.pos.y = 320; P.pitch = -.1; P.invuln = 0; P.speed = 4 * MACH;
  const final = Math.floor(game.score);
  if (final > best) { best = final; try { localStorage.setItem('faster-best', String(best)); } catch (e) { /* no storage */ } }
  $('oScore').textContent = final.toLocaleString(); $('oBest').textContent = best.toLocaleString();
  $('oKills').textContent = game.kills; $('oMach').textContent = 'M ' + game.topMach.toFixed(1);
  el.over.hidden = false; el.touch.classList.remove('live');
}
function startGame() {
  audioInit(); resetGame(); updateCells(true); mouse.on = false; mouse.x = mouse.y = 0;
  game.mode = 'play'; el.title.hidden = true; el.over.hidden = true; el.touch.classList.add('live');
  toast('GO'); showMach(3); game.machShown = 3; boostLatch = false; $('bBoost').classList.remove('on');
}

/* ---------- input ---------- */
const keys = {};
const inp = { ix: 0, iy: 0, fire: false, boost: false, brake: false };
const mouse = { x: 0, y: 0, on: false }, stick = { id: -1, ox: 0, oy: 0, x: 0, y: 0 }, btn = { fire: false, boost: false, brake: false }, mfire = { v: false };
const dz = v => Math.abs(v) < .1 ? 0 : clamp((v - Math.sign(v) * .1) / .9, -1, 1);
addEventListener('keydown', e => {
  keys[e.code] = true;
  if (e.code === 'Enter' && game.mode !== 'play') startGame();
  if (['Space', 'ArrowUp', 'ArrowDown', 'ArrowLeft', 'ArrowRight'].includes(e.code)) e.preventDefault();
});
addEventListener('keyup', e => { keys[e.code] = false; });
addEventListener('blur', () => { for (const k in keys) keys[k] = false; });
app.addEventListener('pointermove', e => {
  if (e.pointerType === 'mouse') {
    if (e.target.closest && e.target.closest('.screen')) { mouse.on = false; return; }
    const r = app.getBoundingClientRect();
    if (e.target.closest && (e.target.closest('.btn') || e.target.closest('#gear'))) { mouse.x = 0; mouse.y = 0; }
    else { mouse.x = ((e.clientX - r.left) / r.width - .5) * 2; mouse.y = -(((e.clientY - r.top) / r.height) - .5) * 2; }
    mouse.on = true;
  } else if (e.pointerId === stick.id) {
    let dx = (e.clientX - stick.ox) / 55, dy = (e.clientY - stick.oy) / 55; const l = Math.hypot(dx, dy);
    if (l > 1) { dx /= l; dy /= l; }
    stick.x = dx; stick.y = -dy;
    el.stick.firstElementChild.style.transform = 'translate(' + dx * 40 + 'px,' + dy * 40 + 'px)';
  }
});
app.addEventListener('pointerdown', e => {
  if (e.target.closest('.btn') || e.target.closest('.screen') || e.target.closest('#gear')) return;
  if (e.pointerType === 'mouse') { if (e.button === 0) mfire.v = true; return; }
  document.body.classList.add('touch');
  const r = app.getBoundingClientRect();
  if (stick.id < 0 && e.clientX - r.left < r.width * .62) {
    stick.id = e.pointerId; stick.ox = e.clientX; stick.oy = e.clientY; stick.x = stick.y = 0;
    const s = el.stick; s.style.display = 'block'; s.style.left = (e.clientX - r.left) + 'px'; s.style.top = (e.clientY - r.top) + 'px';
    s.firstElementChild.style.transform = '';
  } else if (!settings.buttons && game.mode === 'play' && tfire.id < 0 && e.clientX - r.left >= r.width * .62) {
    tfire.id = e.pointerId; btn.fire = true;
    const n = performance.now();
    if (n - tfire.last < 320) { boostLatch = !boostLatch; $('bBoost').classList.toggle('on', boostLatch); }
    tfire.last = n;
  }
});
function endPointer(e) {
  if (e.pointerType === 'mouse') { mfire.v = false; return; }
  if (e.pointerId === tfire.id) { tfire.id = -1; btn.fire = false; }
  if (e.pointerId === stick.id) { stick.id = -1; stick.x = stick.y = 0; el.stick.style.display = 'none'; }
}
addEventListener('pointerup', endPointer); addEventListener('pointercancel', endPointer);
let boostLatch = false, prevBoost = false;
for (const [id, name] of [['bFire', 'fire'], ['bBoost', 'boost'], ['bBrake', 'brake']]) {
  const b = $(id);
  if (name === 'boost') { b.addEventListener('pointerdown', e => { e.preventDefault(); boostLatch = !boostLatch; b.classList.toggle('on', boostLatch); }); continue; }
  b.addEventListener('pointerdown', e => { e.preventDefault(); b.setPointerCapture(e.pointerId); btn[name] = true; b.classList.add('down'); document.body.classList.add('touch'); });
  const up = () => { btn[name] = false; b.classList.remove('down'); };
  b.addEventListener('pointerup', up); b.addEventListener('pointercancel', up); b.addEventListener('lostpointercapture', up);
}
app.addEventListener('contextmenu', e => e.preventDefault());
if (window.matchMedia && matchMedia('(pointer: coarse)').matches) document.body.classList.add('touch');
function applySettings() {
  el.touch.classList.toggle('nobtn', !settings.buttons);
  $('sButtons').checked = settings.buttons; $('sFx').checked = settings.fx; $('sSound').checked = settings.sound;
  if (!settings.fx) { $('svig').style.opacity = 0; }
  try { localStorage.setItem('faster-settings', JSON.stringify(settings)); } catch (e) { /* no storage */ }
}
function setPaused(v) {
  paused = v && game.mode === 'play'; $('settings').hidden = !v;
  if (!v) last = performance.now();
  if (v) { stick.id = -1; stick.x = stick.y = 0; el.stick.style.display = 'none'; }
}
for (const [id, key] of [['sButtons', 'buttons'], ['sFx', 'fx'], ['sSound', 'sound']]) $(id).addEventListener('change', e => { settings[key] = e.target.checked; applySettings(); });
$('gear').addEventListener('click', () => setPaused($('settings').hidden));
$('sClose').addEventListener('click', () => setPaused(false));
addEventListener('keydown', e => { if (e.code === 'Escape') setPaused($('settings').hidden); });
applySettings();
$('launch').addEventListener('click', startGame); $('again').addEventListener('click', startGame);

function readInput() {
  let kx = (keys.ArrowRight || keys.KeyD ? 1 : 0) - (keys.ArrowLeft || keys.KeyA ? 1 : 0);
  let ky = (keys.ArrowUp || keys.KeyW ? 1 : 0) - (keys.ArrowDown || keys.KeyS ? 1 : 0);
  let ix = kx, iy = ky;
  if (!kx && !ky) {
    if (stick.id >= 0) { ix = stick.x; iy = stick.y; } else if (mouse.on) { ix = dz(mouse.x * 1.5); iy = dz(mouse.y * 1.5); }
  }
  inp.ix = ix; inp.iy = iy;
  inp.fire = !!(keys.Space || keys.KeyF || mfire.v || btn.fire);
  inp.boost = !!(keys.ShiftLeft || keys.ShiftRight || boostLatch);
  inp.brake = !!(keys.KeyQ || keys.ControlLeft || btn.brake);
  if (inp.brake && boostLatch) { boostLatch = false; $('bBoost').classList.remove('on'); }
}

/* ---------- targeting / firing ---------- */
function bestTarget() {
  let best = null, bs = 1e9;
  const cands = enemies.concat(missiles);
  for (const t of cands) {
    const pos = t.pos; if (t.alive === false) continue;
    tv.copy(pos).sub(P.pos); const d = tv.length(); if (d > 2600 || d < 15) continue;
    const ang = Math.acos(clamp(tv.dot(P.f) / d, -1, 1)); if (ang > .42) continue;
    const s = ang * 900 + d * .15 + (t.type === 'walker' || t.type === 'drone' ? 0 : 120);
    if (s < bs) { bs = s; best = { t, d, ang }; }
  }
  return best;
}
function firePlayer(target) {
  const b = pBullets.find(x => !x.on); if (!b) return;
  const spd = 1500 + P.speed;
  const dir = tv.copy(P.f);
  if (target && target.ang < .17) {
    const t = target.t, tt = target.d / spd;
    tv2.copy(t.pos); if (t.vel) tv2.addScaledVector(t.vel, tt); else if (t.dir) tv2.addScaledVector(tv3.copy(t.dir), t.speed * tt);
    tv2.sub(P.pos).normalize(); dir.copy(tv2);
  }
  P.gunSide *= -1;
  const side = tv2.set(-P.f.z, 0, P.f.x).normalize().multiplyScalar(P.gunSide * 1.1);
  b.m.position.copy(P.pos).add(side).addScaledVector(P.f, -1); b.prev.copy(b.m.position);
  b.vel.copy(dir).multiplyScalar(spd); b.life = 1.6; b.on = true; b.m.visible = true; b.m.lookAt(tv3.copy(b.m.position).add(dir));
  sfx('shot', .6);
}

/* ---------- boost / speed FX ---------- */
let kick = 0, flashFx = 0, sf = 0;
function boostKick() {
  if (game.mode !== 'play') return;
  P.speed = Math.min(13 * MACH, P.speed + 1.2 * MACH);
  kick = 1; flashFx = 1; shake = Math.max(shake, .7); sfx('whoosh');
  const right = new V3(-P.f.z, 0, P.f.x).normalize(), up = new V3().crossVectors(right, P.f).normalize(), p = new V3(), v = new V3();
  for (let i = 0; i < 30; i++) {
    const a = i / 30 * 6.2832, c = Math.cos(a), sn = Math.sin(a);
    p.copy(P.pos).addScaledVector(right, c * 5).addScaledVector(up, sn * 5).addScaledVector(P.f, -2);
    v.copy(P.f).multiplyScalar(-P.speed * .3).addScaledVector(right, c * 70).addScaledVector(up, sn * 70);
    emit(fireP, p, v, .55, 6, 2, 0xbfe8ff, 0xffffff, .85, .6);
  }
}
const fxc = $('fx'), fxg = fxc.getContext('2d'), fxLines = [];
for (let i = 0; i < 80; i++) fxLines.push({ a: rnd(0, 6.283), r: rnd(.3, 1), l: rnd(.08, .3), v: rnd(.7, 1.5) });
function drawFx(dt) {
  const w = fxc.width, h = fxc.height;
  fxg.clearRect(0, 0, w, h);
  if (sf < .03 || !settings.fx) return;
  const cx = w / 2, cy = h * .46, R = Math.hypot(w, h) / 2, sc = w / Math.max(1, app.clientWidth);
  fxg.lineCap = 'round';
  for (const L of fxLines) {
    L.r += dt * L.v * (.6 + sf * 2.6);
    if (L.r > 1.05) { L.r = rnd(.28, .42); L.a = rnd(0, 6.283); L.l = rnd(.08, .3); }
    const r0 = L.r * R, r1 = (L.r + L.l * (.3 + sf * 1.2)) * R, al = Math.min(1, (L.r - .28) * 2) * sf * .6, c = Math.cos(L.a), sn = Math.sin(L.a);
    fxg.strokeStyle = 'rgba(215,238,255,' + al.toFixed(3) + ')'; fxg.lineWidth = (1 + L.r * 2.6) * sc;
    fxg.beginPath(); fxg.moveTo(cx + c * r0, cy + sn * r0); fxg.lineTo(cx + c * r1, cy + sn * r1); fxg.stroke();
  }
}
const coneMat = new T.MeshBasicMaterial({ color: 0xaee4ff, transparent: true, opacity: 0, blending: T.AdditiveBlending, depthWrite: false, side: T.DoubleSide });
const coneGeo = new T.ConeGeometry(1, 1, 20, 1, true); coneGeo.rotateX(-Math.PI / 2); coneGeo.translate(0, 0, .5);
const cone = new T.Mesh(coneGeo, coneMat); cone.position.z = -5; cone.scale.set(6, 6, 24); shipG.add(cone);

/* ---------- per-frame updates ---------- */
function updatePlayer(dt) {
  if (P.dead > 0) {
    P.dead -= dt;
    if (P.dead <= 0) { if (game.lives <= 0) endGame(); else respawn(); }
    return;
  }
  const play = game.mode === 'play';
  let ix = play ? inp.ix : Math.sin(game.t * .35) * .25, iy = play ? inp.iy : Math.sin(game.t * .5) * .06;
  const mach = P.speed / MACH, rate = 2.1 / (1 + mach * .1);
  P.yaw -= ix * rate * dt;
  P.pitch += iy * rate * .85 * dt;
  if (!iy) P.pitch *= 1 - .35 * dt;
  P.pitch = clamp(P.pitch, -1.2, 1.2);
  P.roll += (-ix * .95 - P.roll) * Math.min(1, dt * 5);
  const boost = play && inp.boost, brake = play && inp.brake;
  const target = boost ? 12 * MACH : (brake ? 1.5 * MACH : (play ? 3 : 4) * MACH);
  if (boost && !prevBoost) boostKick();
  prevBoost = boost;
  if (P.speed < target) P.speed = Math.min(target, P.speed + (boost ? 260 : 220) * dt);
  else P.speed = Math.max(target, P.speed - (brake ? 420 : 150) * dt);
  forwardFrom(P.yaw, P.pitch, P.f);
  P.speed = clamp(P.speed - P.f.y * 90 * dt, 1.2 * MACH, 13 * MACH);
  P.vel.copy(P.f).multiplyScalar(P.speed);
  P.pos.addScaledVector(P.vel, dt);
  if (P.pos.y > 700) P.pitch -= (P.pos.y - 700) * .004 * dt;
  if (P.invuln > 0) { P.invuln -= dt; shipG.visible = P.invuln <= 0 || Math.floor(P.invuln * 12) % 2 === 0; } else shipG.visible = true;
  if (!play) return;
  // ground
  if (P.pos.y < 2.2) {
    if (P.f.y < -.2) { if (P.invuln <= 0 || P.f.y < -.35) { P.pos.y = 2.2; die(); return; } }
    P.pos.y = 2.2; if (P.pitch < 0) P.pitch *= 1 - Math.min(1, dt * 6);
  }
  // mesas
  for (const m of mesas) {
    const dx = P.pos.x - m.x, dzz = P.pos.z - m.z;
    if (P.pos.y > m.h + 3) continue;
    const rr = (lerp(m.rb, m.rt, clamp(P.pos.y / m.h, 0, 1)) * .88) + 3;
    if (dx * dx + dzz * dzz < rr * rr) { die(); return; }
  }
  // dust when skimming
  if (P.pos.y < 16) {
    P.dustT -= dt;
    if (P.dustT <= 0) {
      P.dustT = .035;
      tv.set(P.pos.x, 1.5, P.pos.z).addScaledVector(P.f, 6); tv2.set(rnd(-6, 6), rnd(2, 10), rnd(-6, 6));
      emit(smokeP, tv, tv2, .9, 5, 20 + mach * 2, 0xd9b27c, 0xeedbb4, .5, 1);
    }
  }
  // guns
  P.fireCd -= dt;
  if (inp.fire && P.fireCd <= 0) { firePlayer(bestTarget()); P.fireCd = 1 / 14; }
  game.score += dt * mach * 2.5;
  game.topMach = Math.max(game.topMach, mach);
}

function updateCamera(dt) {
  const mach = P.speed / MACH, f = forwardFrom(P.yaw, P.pitch, tv3);
  if (P.dead <= 0) camF.lerp(f, 1 - Math.exp(-dt * 6)).normalize();
  const dist = 14 + mach * 1.5 + kick * 6, h = 3.2 + mach * .2;
  camera.position.copy(P.pos).addScaledVector(camF, -dist); camera.position.y += h;
  sf = clamp((mach - 3) / 9, 0, 1);
  const s = shake * .15 + sf * sf * .22;
  camera.position.x += rnd(-s, s); camera.position.y += rnd(-s, s);
  if (camera.position.y < 1.5) camera.position.y = 1.5;
  tv.copy(P.pos).addScaledVector(camF, 40); camera.lookAt(tv); camera.rotateZ(P.roll * .3);
  kick = Math.max(0, kick - dt * 1.4); flashFx = Math.max(0, flashFx - dt * 3);
  fov += (baseFov + sf * 40 + kick * 16 - fov) * Math.min(1, dt * 4);
  if (Math.abs(camera.fov - fov) > .05) { camera.fov = fov; camera.updateProjectionMatrix(); }
  shake = Math.max(0, shake - dt * 2.2);
  shipG.position.copy(P.pos); shipG.rotation.set(P.pitch, P.yaw, P.roll);
  // flames
  for (const fl of flames) {
    const j = rnd(.88, 1.12);
    fl.inner.scale.set(.38, .38, (2.4 + mach * .45) * j); fl.outer.scale.set(.62, .62, (4 + mach * .9) * j); fl.trail.scale.set(.36, .36, (14 + mach * 7) * j);
  }
  coneMat.opacity += ((prevBoost && game.mode === 'play' ? .1 + sf * .22 : 0) - coneMat.opacity) * Math.min(1, dt * 6); cone.scale.set(5 + sf * 3, 5 + sf * 3, 20 + sf * 24);
  // environment follows camera
  sky.position.copy(camera.position);
  ground.position.set(Math.round(P.pos.x / TILE) * TILE, 0, Math.round(P.pos.z / TILE) * TILE);
  for (const c of clouds) {
    const dx = c.position.x - P.pos.x, dzz = c.position.z - P.pos.z;
    if (dx * dx + dzz * dzz > 3600 * 3600) { const a = rnd(0, 6.283), d = rnd(2200, 3400); c.position.set(P.pos.x + Math.cos(a) * d, rnd(450, 900), P.pos.z + Math.sin(a) * d); }
  }
}

function updateStreaks() {
  const len = P.speed * .05, f = P.f;
  const right = tv.set(-f.z, 0, f.x).normalize(), up = tv2.crossVectors(right, f).normalize();
  streakMat.opacity = clamp(sf * 1.5, 0, .8);
  for (let i = 0; i < NS; i++) {
    const s = streakW[i], rel = tv3.copy(s.p).sub(P.pos), along = rel.dot(f);
    if (along < -30 || along > 700 || rel.lengthSq() > 750 * 750) {
      const a = rnd(0, 6.283), r = rnd(12, 120), d = rnd(60, 680);
      s.p.copy(P.pos).addScaledVector(f, d).addScaledVector(right, Math.cos(a) * r).addScaledVector(up, Math.sin(a) * r);
    }
    const o = i * 6, l = len * s.k;
    streakPos[o] = s.p.x; streakPos[o + 1] = s.p.y; streakPos[o + 2] = s.p.z;
    streakPos[o + 3] = s.p.x - f.x * l; streakPos[o + 4] = s.p.y - f.y * l; streakPos[o + 5] = s.p.z - f.z * l;
  }
  streakGeo.attributes.position.needsUpdate = true;
}

function updateEnemies(dt) {
  game.t += dt;
  if (game.mode !== 'play' || P.dead > 0) { return; }
  // drone spawning
  game.droneT -= dt;
  const maxD = Math.min(4, 1 + Math.floor(game.t / 50));
  if (game.droneT <= 0) { if (enemies.filter(e => e.type === 'drone').length < maxD) spawnDrone(); game.droneT = rnd(5, 9); }
  for (const e of enemies.slice()) {
    if (!e.alive) continue;
    const to = tv.copy(P.pos).sub(e.pos), dist = to.length();
    if (e.type === 'walker') {
      e.mesh.rotation.y = Math.atan2(to.x, to.z);
      e.core.scale.setScalar(1 + Math.sin(game.t * 8) * .2);
      e.cd -= dt;
      if (e.cd <= 0 && dist < 2400 && dist > 300 && missiles.length < 4) {
        e.cd = rnd(3.5, 6);
        spawnMissile(tv2.set(e.pos.x, 18, e.pos.z), tv3.set(0, 1, 0).addScaledVector(to, 1 / dist));
      }
      if (e.hp < e.hp0) { e.smoke -= dt; if (e.smoke <= 0) { e.smoke = .1; emit(smokeP, tv2.set(e.pos.x, 16, e.pos.z), tv3.set(rnd(-2, 2), rnd(14, 24), rnd(-2, 2)), 2.2, 4, 14, 0x2a2624, 0x5a524a, .65, .3); } }
    } else {
      const dir = tv2.copy(e.vel).normalize();
      let want = tv3;
      if (e.mode === 'attack') { want.copy(to).divideScalar(dist); if (dist < 520) { e.mode = 'evade'; e.timer = rnd(1.8, 3); e.evade.set(rnd(-1, 1), rnd(-.2, .6), rnd(-1, 1)).normalize(); } }
      else { want.copy(e.evade); e.timer -= dt; if (e.timer <= 0) e.mode = 'attack'; }
      dir.lerp(want, Math.min(1, dt * 1.7)).normalize();
      if (e.pos.y < 40 && dir.y < .15) dir.y = .15;
      if (e.pos.y > 400 && dir.y > -.1) dir.y = -.1;
      e.vel.copy(dir).multiplyScalar(300); e.pos.addScaledVector(e.vel, dt);
      e.mesh.position.copy(e.pos); e.mesh.lookAt(tv.copy(e.pos).add(e.vel));
      // burst fire
      e.cd -= dt;
      if (e.burst > 0) { e.burstT -= dt; if (e.burstT <= 0) { e.burstT = .09; e.burst--; shootEnemy(e); } }
      else if (e.mode === 'attack' && e.cd <= 0 && dist < 1500 && dir.dot(want) > .96) { e.burst = 3; e.burstT = 0; e.cd = rnd(1.6, 2.6); }
      if (dist > 5200) killEnemy(e, true);
    }
    // ram
    if (e.alive && dist < e.rad + 4) { killEnemy(e); hurt(1); }
  }
  // enemy missiles
  for (let i = missiles.length - 1; i >= 0; i--) {
    const m = missiles[i];
    m.life -= dt; m.speed = Math.min(430, m.speed + 320 * dt);
    const to = tv.copy(P.pos).sub(m.pos), d = to.length(); to.divideScalar(d || 1);
    const ang = Math.acos(clamp(m.dir.dot(to), -1, 1)), step = Math.min(ang, 1.5 * dt);
    if (ang > 1e-3) { tv2.crossVectors(m.dir, to); if (tv2.lengthSq() > 1e-8) m.dir.applyAxisAngle(tv2.normalize(), step); }
    m.pos.addScaledVector(m.dir, m.speed * dt);
    m.trailT -= dt; if (m.trailT <= 0) { m.trailT = .035; emit(smokeP, m.pos, tv3.set(0, 0, 0), 1.2, 2.5, 7, 0xeee8e0, 0xb0a89c, .6, 0); emit(fireP, m.pos, tv3, .15, 3, 1, 0xffc070, 0xff5a10, .9, 0); }
    if (d < m.rad + 5) { explosion(m.pos, 5); scene.remove(m.m); missiles.splice(i, 1); hurt(1); continue; }
    if (m.life <= 0 || m.pos.y < 0) { puff(m.pos, 5); scene.remove(m.m); missiles.splice(i, 1); }
  }
  // enemy bullets
  for (const b of eBullets) {
    if (!b.on) continue;
    b.life -= dt; b.m.position.addScaledVector(b.vel, dt);
    if (b.m.position.distanceTo(P.pos) < 6) { b.on = false; b.m.visible = false; hurt(1); continue; }
    if (b.life <= 0) { b.on = false; b.m.visible = false; }
  }
}
function shootEnemy(e) {
  const b = eBullets.find(x => !x.on); if (!b) return;
  const spd = 1100, t = e.pos.distanceTo(P.pos) / spd;
  const dir = tv2.copy(P.pos).addScaledVector(P.vel, t * .8).sub(e.pos).normalize();
  b.m.position.copy(e.pos); b.vel.copy(dir).multiplyScalar(spd); b.life = 2.2; b.on = true; b.m.visible = true; b.m.lookAt(tv3.copy(b.m.position).add(dir));
  sfx('shot', .25);
}

function updateBullets(dt) {
  for (const b of pBullets) {
    if (!b.on) continue;
    b.prev.copy(b.m.position); b.m.position.addScaledVector(b.vel, dt); b.life -= dt;
    let hit = false;
    for (const e of enemies) {
      if (!e.alive) continue;
      if (segHitsSphere(b.prev, b.m.position, e.pos, e.rad + 2)) {
        e.hp--; hit = true; puff(b.m.position, 4);
        if (e.hp <= 0) killEnemy(e);
        break;
      }
    }
    if (!hit) for (let i = missiles.length - 1; i >= 0; i--) {
      const m = missiles[i];
      if (segHitsSphere(b.prev, b.m.position, m.pos, m.rad + 3)) { explosion(m.pos, 4); scene.remove(m.m); missiles.splice(i, 1); game.score += 25; hit = true; break; }
    }
    if (!hit && b.m.position.y < 0) { hit = true; emit(smokeP, b.m.position, tv.set(0, 8, 0), .8, 4, 12, 0xd9b27c, 0xeedbb4, .5, 1); }
    if (!hit) for (const m of mesas) {
      if (b.m.position.y < m.h) { const dx = b.m.position.x - m.x, dzz = b.m.position.z - m.z, r = lerp(m.rb, m.rt, b.m.position.y / m.h) * .9; if (dx * dx + dzz * dzz < r * r) { hit = true; puff(b.m.position, 5); break; } }
    }
    if (hit || b.life <= 0) { b.on = false; b.m.visible = false; }
  }
}

/* ---------- HUD ---------- */
let hud = { lives: -1, kills: -1, hull: -1, gm: '', ga: '', gs: '' };
function showMach(n) { el.mach.textContent = 'MACH ' + n; el.mach.classList.remove('show'); void el.mach.offsetWidth; el.mach.classList.add('show'); }
function updateHud(dt) {
  if (hud.lives !== game.lives) { hud.lives = game.lives; el.lives.textContent = Math.max(0, game.lives); }
  if (hud.kills !== game.kills) { hud.kills = game.kills; el.kills.textContent = game.kills; }
  const h = Math.max(0, P.hull);
  if (hud.hull !== h) { hud.hull = h; el.pips.forEach((p, i) => { p.className = 'pip ' + (i < h ? (h === 1 ? 'amber' : 'cyan') : ''); }); }
  const mach = P.speed / MACH, gm = mach.toFixed(1), ga = String(Math.max(0, Math.round(P.pos.y))), gs = String(Math.floor(game.score));
  if (hud.gm !== gm) { hud.gm = gm; el.gm.textContent = gm; }
  if (hud.ga !== ga) { hud.ga = ga; el.ga.textContent = ga; }
  if (hud.gs !== gs) { hud.gs = gs; el.gs.textContent = Number(gs).toLocaleString(); }
  if (game.mode === 'play') {
    const mi = Math.floor(mach + .02);
    if (mi > game.machShown && mi >= 3) showMach(mi);
    game.machShown = mi;
  }
  // warning
  const threat = game.mode === 'play' && P.dead <= 0 && (missiles.some(m => m.pos.distanceTo(P.pos) < 2600) || eBullets.some(b => b.on));
  el.warn.classList.toggle('on', threat);
  if (threat) { game.warnBeep -= dt; if (game.warnBeep <= 0) { game.warnBeep = .5; sfx('beep'); } }
  // lock reticle
  const tgt = game.mode === 'play' && P.dead <= 0 ? bestTarget() : null;
  if (tgt) {
    tv.copy(tgt.t.pos).project(camera);
    if (tv.z < 1 && Math.abs(tv.x) < 1.05 && Math.abs(tv.y) < 1.05) {
      const w = app.clientWidth, hh = app.clientHeight;
      el.lock.style.display = 'block'; el.lock.style.transform = 'translate(' + ((tv.x * .5 + .5) * w).toFixed(1) + 'px,' + ((-tv.y * .5 + .5) * hh).toFixed(1) + 'px)';
      el.lockd.textContent = Math.round(tgt.d).toLocaleString() + ' M';
      el.lock.style.color = tgt.t.type ? '#ffa43a' : '#ff6a4a';
    } else el.lock.style.display = 'none';
  } else el.lock.style.display = 'none';
  flashV = Math.max(0, flashV - dt * 1.6); el.vig.style.opacity = flashV.toFixed(2);
}

/* ---------- loop ---------- */
function resize() {
  const w = app.clientWidth || 1, h = app.clientHeight || 1;
  const dpr = Math.min(window.devicePixelRatio || 1, 1.5); fxc.width = Math.round(w * dpr); fxc.height = Math.round(h * dpr);
  renderer.setSize(w, h, false); camera.aspect = w / h; baseFov = w / h < .8 ? 84 : 72; camera.updateProjectionMatrix();
}
addEventListener('resize', resize); resize();

resetGame(); P.invuln = 0; updateCells(true);
let last = performance.now();
function frame(now) {
  const dt = Math.min(.05, (now - last) / 1000); last = now;
  if (paused) { renderer.render(scene, camera); requestAnimationFrame(frame); return; }
  readInput();
  updatePlayer(dt);
  updateCamera(dt);
  updateCells(false);
  updateStreaks();
  updateEnemies(dt);
  updateBullets(dt);
  updatePool(fireP, dt); updatePool(smokeP, dt);
  updateHud(dt);
  audioUpdate(clamp((P.speed / MACH - 1) / 11, 0, 1), game.mode === 'play' && P.dead <= 0);
  drawFx(dt);
  $('svig').style.opacity = settings.fx ? (sf * .8).toFixed(2) : 0; $('flash').style.opacity = (flashFx * .55).toFixed(2);
  renderer.render(scene, camera);
  requestAnimationFrame(frame);
}
requestAnimationFrame(frame);
})();
</script>

</body></html>
