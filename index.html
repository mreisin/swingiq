<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <meta name="apple-mobile-web-app-capable" content="yes">
    <meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
    <meta name="apple-mobile-web-app-title" content="SwingIQ">
    <title>SwingIQ</title>
    <script src="https://cdn.jsdelivr.net/npm/@tensorflow/tfjs@4.17.0/dist/tf.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/@tensorflow-models/pose-detection@2.1.3/dist/pose-detection.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/chart.js@4.4.1/dist/chart.umd.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/marked@12.0.0/marked.min.js"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=DM+Sans:ital,opsz,wght@0,9..40,300;0,9..40,500;0,9..40,700;1,9..40,400&family=JetBrains+Mono:wght@400;600&display=swap');
        :root{--bg:#0a0c0f;--s1:rgba(255,255,255,0.04);--s2:rgba(255,255,255,0.08);--brd:rgba(255,255,255,0.07);--g:#34d399;--gd:rgba(52,211,153,0.12);--y:#fbbf24;--yd:rgba(251,191,36,0.12);--r:#f87171;--rd:rgba(248,113,113,0.12);--t:#d1d5db;--td:#6b7280;--tb:#f9fafb;--blue:#60a5fa;--purple:#a78bfa;--mono:'JetBrains Mono',monospace}
        *{margin:0;padding:0;box-sizing:border-box;-webkit-tap-highlight-color:transparent}
        body{font-family:'DM Sans',-apple-system,sans-serif;background:var(--bg);color:var(--t);min-height:100dvh;overflow-x:hidden}
        .hidden{display:none!important}
        .fade{animation:fade .4s ease}@keyframes fade{from{opacity:0;transform:translateY(6px)}to{opacity:1}}
        .pulse{animation:pls 2s ease-in-out infinite}@keyframes pls{0%,100%{opacity:1}50%{opacity:.4}}
        input,select,textarea{font-family:'DM Sans';background:rgba(0,0,0,.5);border:1px solid var(--brd);border-radius:12px;padding:12px 16px;color:var(--tb);font-size:16px;width:100%;outline:none}
        input:focus,select:focus{border-color:var(--g)}select{-webkit-appearance:none}
        .btn{display:flex;align-items:center;justify-content:center;gap:8px;width:100%;padding:14px;border:none;border-radius:14px;font-family:'DM Sans';font-size:16px;font-weight:700;cursor:pointer;transition:all .15s}
        .btn-g{background:var(--g);color:#000}.btn-g:disabled{background:#1a1f2e;color:#4b5563;cursor:not-allowed}
        .btn-o{background:transparent;color:var(--td);border:1px solid var(--brd)}
        .btn-s{padding:8px 14px;font-size:13px;width:auto;border-radius:10px}
        .btn-r{background:var(--rd);color:var(--r);border:1px solid rgba(248,113,113,.15)}

        /* Layout */
        .hdr{position:sticky;top:0;z-index:50;padding:12px 16px;background:rgba(10,12,15,.88);backdrop-filter:blur(20px);border-bottom:1px solid var(--brd)}
        .hdr-in{max-width:480px;margin:0 auto;display:flex;align-items:center;justify-content:space-between}
        .logo{font-weight:700;font-size:17px;color:var(--tb)}
        .tabs{display:flex;gap:2px}.tab{padding:6px 14px;border-radius:8px;font-size:13px;font-weight:500;color:var(--td);cursor:pointer;border:none;background:none}.tab.on{background:var(--gd);color:var(--g)}
        .wrap{padding:0 16px;max-width:480px;margin:0 auto;width:100%}
        .card{background:var(--s1);border:1px solid var(--brd);border-radius:16px;padding:20px;margin-bottom:12px}
        .lbl{font-size:11px;color:var(--td);text-transform:uppercase;letter-spacing:.6px;margin-bottom:10px}

        /* Upload */
        .uzone{border:2px dashed rgba(255,255,255,.1);border-radius:16px;padding:36px 20px;text-align:center;cursor:pointer;transition:all .2s}
        .uzone:active{border-color:var(--g);background:var(--gd)}

        /* Verdict badges */
        .verdict{display:inline-flex;align-items:center;gap:6px;padding:6px 12px;border-radius:20px;font-size:13px;font-weight:600;margin:3px}
        .v-good{background:var(--gd);color:var(--g)}.v-warn{background:var(--yd);color:var(--y)}.v-bad{background:var(--rd);color:var(--r)}

        /* Swing cards */
        .sw-card{display:flex;align-items:center;gap:12px;padding:12px;border-radius:14px;background:var(--s1);border:1px solid var(--brd);margin-bottom:8px}
        .sw-card img{width:65px;height:85px;object-fit:cover;border-radius:8px;flex-shrink:0;cursor:pointer}
        .sw-info{flex:1;min-width:0}.sw-acts{display:flex;gap:6px;flex-shrink:0}

        /* Position thumbs */
        .pos-row{display:flex;gap:10px;overflow-x:auto;padding-bottom:4px}
        .pos-th{flex-shrink:0;width:100px;border-radius:12px;overflow:hidden;border:2px solid transparent;cursor:pointer}.pos-th.on{border-color:var(--g)}
        .pos-th img{width:100%;height:130px;object-fit:cover;display:block}
        .pos-th-i{padding:6px 8px;background:rgba(0,0,0,.6);font-size:11px}

        /* Coaching */
        .coach h2{font-size:16px;font-weight:700;margin:18px 0 8px;color:var(--g)}
        .coach h3{font-size:14px;font-weight:600;margin-top:12px;color:var(--tb)}
        .coach p{margin:6px 0;line-height:1.55;font-size:14px}.coach strong{color:var(--tb)}
        .coach ul,.coach ol{padding-left:18px;margin:6px 0}.coach li{margin:4px 0;font-size:14px;line-height:1.5}

        /* Launch grid */
        .lm-g{display:grid;grid-template-columns:1fr 1fr;gap:10px}
        .lm-f label{display:block;font-size:11px;color:var(--td);margin-bottom:4px}
        .lm-f input{padding:10px 12px;font-size:14px;border-radius:10px}

        /* Overlay */
        .overlay{position:fixed;inset:0;z-index:100;background:rgba(10,12,15,.96);display:flex;align-items:center;justify-content:center;flex-direction:column;gap:16px;padding:40px;text-align:center}
        .pbar{width:100%;max-width:260px;height:4px;background:#1f2937;border-radius:2px;overflow:hidden}
        .pfill{height:100%;background:var(--g);border-radius:2px;transition:width .5s}

        /* Voice toggle */
        .vtog{display:inline-flex;align-items:center;gap:5px;padding:4px 10px;border-radius:20px;font-size:12px;font-weight:600;cursor:pointer}
        .von{background:var(--gd);color:var(--g)}.voff{background:var(--s1);color:var(--td)}

        /* Camera controls */
        .cam-ctrl{position:absolute;top:10px;right:10px;display:flex;gap:6px;z-index:10}
        .cam-btn{width:36px;height:36px;border-radius:50%;background:rgba(0,0,0,.6);border:none;color:#fff;font-size:16px;cursor:pointer;backdrop-filter:blur(8px)}

        /* Live container */
        .live-wrap{position:relative;border-radius:14px;overflow:hidden;background:#111}

        .mono{font-family:var(--mono)}
        .processing-canvas{display:none}

        /* Plain English panel */
        .eng-panel{padding:16px;border-radius:14px;background:linear-gradient(135deg,rgba(52,211,153,.06),rgba(96,165,250,.06));border:1px solid var(--brd)}
        .eng-line{display:flex;align-items:flex-start;gap:10px;padding:8px 0;font-size:14px;line-height:1.5}
        .eng-icon{flex-shrink:0;font-size:16px;margin-top:1px}
        .eng-fix{color:var(--blue);font-weight:500}
    </style>
</head>
<body>

<!-- ===== SETUP ===== -->
<div id="setupScreen" style="min-height:100dvh;display:flex;align-items:center;justify-content:center;padding:24px;background:radial-gradient(ellipse at 50% 0%,rgba(52,211,153,.05) 0%,transparent 60%)">
    <div style="width:100%;max-width:340px;text-align:center">
        <div style="font-size:48px;margin-bottom:8px">🏌️</div>
        <div style="font-size:28px;font-weight:700;color:var(--tb)">SwingIQ</div>
        <div style="color:var(--td);font-size:14px;margin:4px 0 28px">Your Personal Swing Coach</div>
        <div id="setupStep">
            <p style="font-size:13px;color:var(--td);margin-bottom:16px">Enter your Claude API key<br><span style="font-size:12px">Get one at <strong style="color:var(--g)">console.anthropic.com</strong></span></p>
            <input id="apiKeyInput" type="password" placeholder="sk-ant-..." autocomplete="off" style="margin-bottom:10px;font-family:var(--mono);font-size:14px">
            <input id="setupPw" type="password" placeholder="Set an app password" autocomplete="new-password" style="margin-bottom:14px">
            <button class="btn btn-g" onclick="saveSetup()">Get Started</button>
            <p id="setupErr" class="hidden" style="color:var(--r);font-size:13px;margin-top:10px"></p>
        </div>
        <div id="loginStep" class="hidden">
            <input id="loginPw" type="password" placeholder="Password" autocomplete="current-password" style="margin-bottom:14px" onkeydown="if(event.key==='Enter')doLogin()">
            <button class="btn btn-g" onclick="doLogin()">Unlock</button>
            <p id="loginErr" class="hidden" style="color:var(--r);font-size:13px;margin-top:10px">Wrong password</p>
            <button class="btn btn-o" style="margin-top:10px;font-size:13px" onclick="if(confirm('Erase all data?')){localStorage.removeItem('swingiq');location.reload()}">Reset App</button>
        </div>
    </div>
</div>

<!-- ===== MAIN ===== -->
<div id="mainApp" class="hidden" style="min-height:100dvh;display:flex;flex-direction:column">
    <div class="hdr"><div class="hdr-in">
        <div class="logo">🏌️ SwingIQ</div>
        <div class="tabs">
            <button class="tab on" data-t="analyze" onclick="goTab('analyze')">Analyze</button>
            <button class="tab" data-t="history" onclick="goTab('history')">History</button>
            <button class="tab" data-t="progress" onclick="goTab('progress')">Progress</button>
        </div>
    </div></div>

    <!-- ===== ANALYZE ===== -->
    <div id="analyzeTab" class="wrap fade" style="padding-top:16px;padding-bottom:100px">

        <!-- Mode -->
        <div style="display:flex;gap:8px;margin-bottom:12px">
            <button id="mUpload" class="btn btn-s" style="flex:1;background:var(--gd);color:var(--g)" onclick="setMode('upload')">📁 Upload</button>
            <button id="mLive" class="btn btn-s" style="flex:1" onclick="setMode('live')">🎙️ Live</button>
        </div>

        <!-- UPLOAD MODE -->
        <div id="uploadMode">
            <div class="card">
                <div class="lbl">Club</div>
                <select id="club"><option>Driver</option><option>3-Wood</option><option>5-Wood</option><option>3-Hybrid</option><option>4-Hybrid</option><option>4-Iron</option><option>5-Iron</option><option>6-Iron</option><option>7-Iron</option><option>8-Iron</option><option>9-Iron</option><option>Pitching Wedge</option><option>Gap Wedge</option><option>Sand Wedge</option><option>Lob Wedge</option></select>
            </div>
            <div class="card">
                <div class="lbl">Swing Video</div>
                <div class="uzone" id="uzone" onclick="document.getElementById('vidIn').click()">
                    <div style="font-size:32px;margin-bottom:6px">📱</div>
                    <div style="font-weight:600;font-size:15px">Record or Choose Video</div>
                    <div style="font-size:12px;color:var(--td);margin-top:4px">Multi-swing videos supported</div>
                </div>
                <input type="file" id="vidIn" accept="video/*" style="display:none" onchange="handleVid(this)">
                <div id="vidPrev" class="hidden" style="margin-top:12px">
                    <video id="prevVid" style="width:100%;border-radius:12px" controls playsinline></video>
                    <div style="display:flex;justify-content:space-between;align-items:center;margin-top:6px">
                        <span id="vName" style="font-size:12px;color:var(--td);overflow:hidden;text-overflow:ellipsis;white-space:nowrap;max-width:200px"></span>
                        <button onclick="clearVid()" style="background:none;border:none;color:var(--r);font-size:13px;cursor:pointer">Remove</button>
                    </div>
                </div>
            </div>
            <div class="card">
                <div style="display:flex;justify-content:space-between;align-items:center;cursor:pointer" onclick="toggleLM()">
                    <div class="lbl" style="margin-bottom:0">📊 Launch Data</div>
                    <span id="lmIcon" style="font-size:12px;color:var(--td)">＋</span>
                </div>
                <div id="lmSec" class="hidden" style="margin-top:14px">
                    <div class="lm-g">
                        <div class="lm-f"><label>Ball Speed</label><input type="number" id="lmBS" step=".1" placeholder="165 mph"></div>
                        <div class="lm-f"><label>Club Speed</label><input type="number" id="lmCS" step=".1" placeholder="112 mph"></div>
                        <div class="lm-f"><label>Launch Angle</label><input type="number" id="lmLA" step=".1" placeholder="12.5°"></div>
                        <div class="lm-f"><label>Spin Rate</label><input type="number" id="lmSR" step="1" placeholder="2400 rpm"></div>
                        <div class="lm-f"><label>Carry</label><input type="number" id="lmCY" step=".1" placeholder="275 yds"></div>
                        <div class="lm-f"><label>Smash Factor</label><input type="number" id="lmSF" step=".01" placeholder="1.47"></div>
                        <div class="lm-f"><label>Total Dist</label><input type="number" id="lmTD" step=".1" placeholder="295 yds"></div>
                        <div class="lm-f"><label>Attack Angle</label><input type="number" id="lmAA" step=".1" placeholder="-1.5°"></div>
                    </div>
                </div>
            </div>
            <button class="btn btn-g" id="goBtn" onclick="runAnalysis()" disabled>🔍 Analyze Swing(s)</button>
        </div>

        <!-- LIVE MODE -->
        <div id="liveMode" class="hidden">
            <div class="card" style="padding:12px">
                <div style="display:flex;justify-content:space-between;align-items:center;margin-bottom:10px">
                    <select id="liveClub" style="width:auto;padding:6px 12px;font-size:13px;border-radius:8px"><option>Driver</option><option>7-Iron</option><option>9-Iron</option><option>Pitching Wedge</option></select>
                    <div class="vtog von" id="vTog" onclick="toggleVoice()">🔊 Voice On</div>
                </div>
                <div class="live-wrap">
                    <video id="liveVid" style="width:100%;display:block" autoplay playsinline muted></video>
                    <div class="cam-ctrl">
                        <button class="cam-btn" onclick="flipCamera()" title="Flip camera">🔄</button>
                    </div>
                </div>
                <div style="display:flex;gap:8px;margin-top:10px">
                    <button class="btn btn-g btn-s" id="liveBtn" onclick="toggleLive()" style="flex:1">▶ Start Practice</button>
                </div>
                <div id="liveStat" style="margin-top:10px;font-size:13px;color:var(--td);text-align:center">Set up phone, press Start, then swing.</div>
                <div id="liveCount" class="hidden mono" style="text-align:center;margin-top:6px;font-size:22px;font-weight:700;color:var(--g)">0 swings</div>
            </div>
            <div id="liveCards" style="margin-top:12px"></div>
        </div>

        <!-- MULTI-SWING RESULTS -->
        <div id="msr" class="hidden fade" style="margin-top:16px">
            <div class="card">
                <div style="display:flex;justify-content:space-between;align-items:center;margin-bottom:12px">
                    <div class="lbl" style="margin-bottom:0">Detected Swings</div>
                    <span id="swCnt" class="mono" style="font-size:13px;color:var(--g)"></span>
                </div>
                <div id="swList"></div>
                <div style="display:flex;gap:8px;margin-top:12px">
                    <button class="btn btn-g btn-s" style="flex:1" onclick="saveAll()">✓ Save All</button>
                    <button class="btn btn-o btn-s" style="flex:1" onclick="discAll()">✕ Discard All</button>
                </div>
            </div>
            <div id="batchSec" class="hidden">
                <button class="btn btn-g" id="batchBtn" onclick="runBatch()">🤖 Get Session Coaching</button>
                <div id="batchRes" class="hidden card" style="margin-top:12px">
                    <div class="lbl">🤖 Session Coaching</div>
                    <div id="batchTxt" class="coach"></div>
                </div>
            </div>
        </div>

        <!-- SINGLE SWING DETAIL -->
        <div id="swDetail" class="hidden fade" style="margin-top:12px">
            <div class="card">
                <div style="display:flex;justify-content:space-between;align-items:center;margin-bottom:16px">
                    <button class="btn btn-o btn-s" onclick="$('swDetail').classList.add('hidden')">← Back</button>
                    <span id="dLabel" class="mono" style="font-weight:700"></span>
                </div>

                <!-- Plain English Summary -->
                <div id="engPanel" class="eng-panel" style="margin-bottom:16px"></div>

                <!-- Positions -->
                <div class="lbl">Key Positions</div>
                <div class="pos-row" id="dPosRow" style="margin-bottom:12px"></div>

                <!-- Selected position canvas -->
                <div id="dPosCard" class="hidden" style="margin-bottom:12px">
                    <canvas id="dCanvas" style="width:100%;border-radius:12px"></canvas>
                    <div id="dVerdicts" style="margin-top:10px;display:flex;flex-wrap:wrap;gap:4px"></div>
                    <details style="margin-top:10px">
                        <summary style="font-size:12px;color:var(--td);cursor:pointer">📐 Technical Details</summary>
                        <div id="dAngles" style="margin-top:8px;font-size:12px"></div>
                    </details>
                </div>
            </div>
        </div>
    </div>

    <!-- ===== HISTORY ===== -->
    <div id="historyTab" class="wrap hidden fade" style="padding-top:16px;padding-bottom:40px">
        <div style="display:flex;justify-content:space-between;align-items:center;margin-bottom:16px">
            <div style="font-size:18px;font-weight:700">History</div>
            <select id="hFilt" onchange="renderHist()" style="width:auto;padding:6px 12px;font-size:13px;border-radius:8px"><option value="">All</option><option>Driver</option><option>7-Iron</option></select>
        </div>
        <div id="hList"></div>
    </div>

    <!-- ===== PROGRESS ===== -->
    <div id="progressTab" class="wrap hidden fade" style="padding-top:16px;padding-bottom:40px">
        <div style="display:flex;justify-content:space-between;align-items:center;margin-bottom:16px">
            <div style="font-size:18px;font-weight:700">Progress</div>
            <select id="pFilt" onchange="renderProg()" style="width:auto;padding:6px 12px;font-size:13px;border-radius:8px"><option value="">All</option><option>Driver</option><option>7-Iron</option></select>
        </div>
        <div class="card"><div class="lbl">Swing Score</div><canvas id="pSc" height="180"></canvas></div>
        <div class="card"><div class="lbl">Handicap</div><canvas id="pHc" height="180"></canvas></div>
        <div class="card"><div class="lbl">Launch Trends</div><canvas id="pLm" height="220"></canvas></div>
    </div>
</div>

<!-- Overlay -->
<div id="ovl" class="overlay hidden">
    <div class="pulse" style="font-size:56px">🏌️</div>
    <div style="font-weight:700;font-size:18px;color:var(--tb)" id="ovlTitle">Analyzing your swing(s)</div>
    <div id="ovlStep" style="font-size:14px;color:var(--td)">Preparing...</div>
    <div class="pbar"><div id="ovlFill" class="pfill" style="width:0%"></div></div>
</div>

<canvas id="fCvs" class="processing-canvas"></canvas>
<canvas id="aCvs" class="processing-canvas"></canvas>
<canvas id="lCvs" class="processing-canvas"></canvas>

<script>
const $=id=>document.getElementById(id);
const POS=['Address','Takeaway','Top','Downswing','Impact','Follow-Through'];
const SK='swingiq';
const KP={NOSE:0,L_SH:5,R_SH:6,L_EL:7,R_EL:8,L_WR:9,R_WR:10,L_HI:11,R_HI:12,L_KN:13,R_KN:14,L_AN:15,R_AN:16};

// Ideal ranges + plain English verdicts
const IDEALS={
    Address:{spine:[28,38],knee_l:[140,160]},
    Takeaway:{spine:[28,38],l_arm:[160,180]},
    Top:{spine:[25,40],l_arm:[155,180],hip_rot:[30,50]},
    Downswing:{spine:[28,42],hip_rot:[20,45]},
    Impact:{spine:[28,42],l_arm:[155,180]},
    'Follow-Through':{spine:[15,35]}
};
const VERDICTS={
    spine:{good:'Spine angle looks solid',warn_lo:'Standing too tall — bend more from the hips',warn_hi:'Too hunched over — straighten up a bit',bad_lo:'Way too upright — need more forward tilt',bad_hi:'Way too bent over — you\'ll lose power and balance'},
    l_arm:{good:'Left arm nice and straight',warn:'Left arm breaking down slightly',bad:'Left arm collapsed — focus on keeping it extended'},
    knee_l:{good:'Good knee flex',warn_lo:'Legs too straight — add some athletic flex',warn_hi:'Knees too bent — you\'re squatting',bad_lo:'Locked knees — soften them',bad_hi:'Way too deep — stand taller'},
    hip_rot:{good:'Great hip rotation',warn_lo:'Hips not rotating enough — turn more',warn_hi:'Over-rotating hips',bad_lo:'Hips are stuck — they need to fire first',bad_hi:'Hips spinning out — slow them down'}
};
const POS_W={Address:1,Takeaway:.8,Top:1.2,Downswing:1.3,Impact:1.5,'Follow-Through':.7};

let state=load();
let vidFile=null,detector=null,dSwings=[],voiceOn=true,liveOn=false,liveStream=null,liveCnt=0,liveInt=null,prevGray=null,mBase=0,cooldown=false;
let facingMode='environment';

function load(){try{const r=localStorage.getItem(SK);return r?JSON.parse(r):{key:'',pw:'',sessions:[]}}catch{return{key:'',pw:'',sessions:[]}}}
function save(){try{localStorage.setItem(SK,JSON.stringify(state))}catch{}}

// ===== SETUP =====
(function(){if(state.key&&state.pw){$('setupStep').classList.add('hidden');$('loginStep').classList.remove('hidden')}if(state.in)showApp()})();
function saveSetup(){const k=$('apiKeyInput').value.trim(),p=$('setupPw').value;if(!k.startsWith('sk-ant-'))return sErr('API key should start with sk-ant-');if(p.length<4)return sErr('Password must be 4+ characters');state.key=k;state.pw=p;state.in=true;save();showApp()}
function doLogin(){if($('loginPw').value===state.pw){state.in=true;save();showApp()}else $('loginErr').classList.remove('hidden')}
function sErr(m){$('setupErr').textContent=m;$('setupErr').classList.remove('hidden')}
function showApp(){$('setupScreen').classList.add('hidden');$('mainApp').classList.remove('hidden');initDetector()}

// ===== TABS =====
function goTab(t){['analyze','history','progress'].forEach(x=>{$(x+'Tab').classList.toggle('hidden',x!==t);document.querySelector(`.tab[data-t="${x}"]`).classList.toggle('on',x===t)});if(t==='history')renderHist();if(t==='progress')renderProg()}

// ===== MODE =====
function setMode(m){$('uploadMode').classList.toggle('hidden',m!=='upload');$('liveMode').classList.toggle('hidden',m!=='live');$('mUpload').style.background=m==='upload'?'var(--gd)':'transparent';$('mUpload').style.color=m==='upload'?'var(--g)':'var(--td)';$('mLive').style.background=m==='live'?'var(--gd)':'transparent';$('mLive').style.color=m==='live'?'var(--g)':'var(--td)';if(m==='live')initCam();else stopLive()}

// ===== VIDEO =====
function handleVid(inp){const f=inp.files[0];if(!f)return;vidFile=f;$('uzone').classList.add('hidden');$('vidPrev').classList.remove('hidden');$('vName').textContent=f.name;$('prevVid').src=URL.createObjectURL(f);$('goBtn').disabled=false}
function clearVid(){vidFile=null;$('uzone').classList.remove('hidden');$('vidPrev').classList.add('hidden');$('vidIn').value='';$('goBtn').disabled=true}
function toggleLM(){$('lmSec').classList.toggle('hidden');$('lmIcon').textContent=$('lmSec').classList.contains('hidden')?'＋':'－'}

// ===== VOICE =====
function speak(t){if(!voiceOn)return;try{const u=new SpeechSynthesisUtterance(t);u.rate=1.05;u.lang='en-US';speechSynthesis.speak(u)}catch{}}
function toggleVoice(){voiceOn=!voiceOn;$('vTog').className='vtog '+(voiceOn?'von':'voff');$('vTog').innerHTML=voiceOn?'🔊 Voice On':'🔇 Off'}

// ===== CAMERA =====
async function initCam(){try{if(liveStream)liveStream.getTracks().forEach(t=>t.stop());liveStream=await navigator.mediaDevices.getUserMedia({video:{facingMode,width:{ideal:1280},height:{ideal:720}},audio:false});$('liveVid').srcObject=liveStream}catch(e){$('liveStat').textContent='Camera denied. Check Settings → Safari → Camera.'}}
function flipCamera(){facingMode=facingMode==='environment'?'user':'environment';initCam()}

// ===== DETECTOR =====
async function initDetector(){try{detector=await poseDetection.createDetector(poseDetection.SupportedModels.MoveNet,{modelType:poseDetection.movenet.modelType.SINGLEPOSE_THUNDER});console.log('Detector ready')}catch(e){console.error(e)}}

// ===== ANALYSIS PIPELINE =====
async function runAnalysis(){
    if(!vidFile||!detector)return;
    $('ovl').classList.remove('hidden');prog('Loading video...',5);
    try{
        prog('Scanning for swings...',10);
        const swings=await detectSwings(vidFile);
        if(!swings.length)throw new Error('No swings found. Try a clearer video with more motion.');
        dSwings=[];
        for(let i=0;i<swings.length;i++){
            prog(`Analyzing swing ${i+1}/${swings.length}...`,10+((i/swings.length)*80));
            const r=await analyzeFrames(swings[i]);r.idx=i+1;r.st='pending';dSwings.push(r);
        }
        prog('Done!',100);setTimeout(()=>{$('ovl').classList.add('hidden');showSwings()},400);
    }catch(e){$('ovl').classList.add('hidden');alert(e.message);console.error(e)}
}
function prog(s,p){$('ovlStep').textContent=s;$('ovlFill').style.width=p+'%'}

// ===== SWING DETECTION =====
async function detectSwings(file){
    return new Promise((res,rej)=>{
        const v=document.createElement('video');v.muted=true;v.playsInline=true;v.preload='auto';
        v.onloadedmetadata=async()=>{
            const dur=v.duration;if(dur<.5){rej(new Error('Too short'));return}
            const c=$('fCvs'),cx=c.getContext('2d');
            const n=Math.min(150,Math.floor(dur*15));
            const mp=[],sf=[];
            for(let i=0;i<n;i++){const t=(i/n)*dur;try{const d=await seek(v,c,cx,t);sf.push({t,d});mp.push(i>0?{t,m:motion(sf[i-1].d,d,c.width,c.height)}:{t,m:0})}catch{mp.push({t,m:0})}}
            const wins=findPeaks(mp,dur);
            const all=[];
            for(const w of wins){const kt=keyTimes(mp,w.s,w.p,w.e);const frames=[];for(const t of kt){try{const d=await seek(v,c,cx,t);frames.push({t,imageData:d,width:c.width,height:c.height})}catch{}}if(frames.length>=4)all.push(frames)}
            URL.revokeObjectURL(v.src);res(all);
        };
        v.onerror=()=>rej(new Error('Cannot load video'));v.src=URL.createObjectURL(file);
    });
}
function seek(v,c,cx,t){return new Promise((res,rej)=>{v.currentTime=t;v.onseeked=()=>{c.width=v.videoWidth;c.height=v.videoHeight;cx.drawImage(v,0,0);res(cx.getImageData(0,0,c.width,c.height))};setTimeout(()=>rej('timeout'),5000)})}
function motion(a,b,w,h){let d=0;const s=8;for(let i=0;i<a.data.length;i+=s*4)d+=(Math.abs(a.data[i]-b.data[i])+Math.abs(a.data[i+1]-b.data[i+1])+Math.abs(a.data[i+2]-b.data[i+2]))/3;return d/(a.data.length/(s*4))}
function smooth(a,r){return a.map((_,i)=>{let s=0,c=0;for(let j=Math.max(0,i-r);j<=Math.min(a.length-1,i+r);j++){s+=a[j];c++}return s/c})}

function findPeaks(mp,dur){
    const ms=mp.map(x=>x.m),ts=mp.map(x=>x.t),sm=smooth(ms,3),mx=Math.max(...sm);
    if(mx<1)return[];const th=mx*.25;
    const pks=[];
    for(let i=3;i<sm.length-3;i++){if(sm[i]>th&&sm[i]>=sm[i-1]&&sm[i]>=sm[i+1]&&sm[i]>=sm[i-2])pks.push(i)}
    const gap=Math.max(4,Math.floor(mp.length/dur*.8)),merged=[];
    for(const p of pks){if(!merged.length||p-merged[merged.length-1]>gap)merged.push(p);else if(sm[p]>sm[merged[merged.length-1]])merged[merged.length-1]=p}
    return merged.map(pk=>{let s=pk;while(s>0&&sm[s]>th*.2)s--;s=Math.max(0,s-3);let e=pk;while(e<sm.length-1&&sm[e]>th*.2)e++;e=Math.min(sm.length-1,e+3);return{s,p:pk,e}});
}

function keyTimes(mp,si,pi,ei){
    const ts=mp.map(x=>x.t),sm=smooth(mp.map(x=>x.m),3);
    let ti=Math.floor((si+pi)/2),mv=Infinity;
    for(let i=Math.max(si,si+Math.floor((pi-si)*.25));i<pi-1;i++){if(sm[i]<mv){mv=sm[i];ti=i}}
    const ai=Math.max(0,si),tki=ai+Math.round((ti-ai)*.4),di=ti+Math.round((pi-ti)*.5),fi=Math.min(mp.length-1,pi+Math.round((ei-pi)*.5));
    let idx=[ai,tki,ti,di,pi,fi];
    for(let i=1;i<idx.length;i++){if(idx[i]<=idx[i-1])idx[i]=Math.min(idx[i-1]+1,mp.length-1)}
    return idx.map(i=>ts[Math.min(i,ts.length-1)]);
}

// ===== POSE ANALYSIS =====
async function analyzeFrames(frames){
    const results=[];
    for(let i=0;i<frames.length;i++)results.push(await analyzePos(frames[i],POS[i]||'Pos '+(i+1)));
    return{positions:results,score:calcScore(results),club:$('club').value,launch:getLM(),date:new Date().toISOString()};
}

async function analyzePos(frame,pos){
    const c=$('fCvs'),cx=c.getContext('2d');c.width=frame.width;c.height=frame.height;cx.putImageData(frame.imageData,0,0);
    let kps=null;try{const p=await detector.estimatePoses(c);if(p.length)kps=p[0].keypoints}catch{}
    const ang=kps?calcAngles(kps,frame.width,frame.height):{};
    const sc=scorePos(ang,pos);
    const eng=getVerdicts(ang,sc,pos);
    const ac=$('aCvs');ac.width=frame.width;ac.height=frame.height;
    const ax=ac.getContext('2d');ax.putImageData(frame.imageData,0,0);
    if(kps)drawVisual(ax,kps,ang,sc,pos,frame.width,frame.height);
    drawHdr(ax,pos,posScore(sc),frame.width);
    return{position:pos,angles:ang,scores:sc,verdicts:eng,pscore:posScore(sc),img:ac.toDataURL('image/jpeg',.85),hasPose:!!kps};
}

function pt(kps,i){const k=kps[i];return{x:k.x,y:k.y}}
function angB(a,b,c){const ba={x:a.x-b.x,y:a.y-b.y},bc={x:c.x-b.x,y:c.y-b.y};const d=ba.x*bc.x+ba.y*bc.y,m=Math.sqrt(ba.x**2+ba.y**2)*Math.sqrt(bc.x**2+bc.y**2);return m===0?0:Math.acos(Math.max(-1,Math.min(1,d/m)))*57.2958}
function angV(a,b){return Math.atan2(Math.abs(b.x-a.x),Math.abs(b.y-a.y))*57.2958}
function rnd(v){return Math.round(v*10)/10}

function calcAngles(kps,w,h){
    const ls=pt(kps,KP.L_SH),rs=pt(kps,KP.R_SH),lh=pt(kps,KP.L_HI),rh=pt(kps,KP.R_HI);
    const lk=pt(kps,KP.L_KN),rk=pt(kps,KP.R_KN),la=pt(kps,KP.L_AN),ra=pt(kps,KP.R_AN);
    const le=pt(kps,KP.L_EL),re=pt(kps,KP.R_EL),lw=pt(kps,KP.L_WR),rw=pt(kps,KP.R_WR);
    const mh={x:(lh.x+rh.x)/2,y:(lh.y+rh.y)/2},ms={x:(ls.x+rs.x)/2,y:(ls.y+rs.y)/2};
    const a={};
    a.spine=rnd(angV(mh,ms));a.knee_l=rnd(angB(lh,lk,la));a.knee_r=rnd(angB(rh,rk,ra));
    a.l_arm=rnd(angB(ls,le,lw));a.r_arm=rnd(angB(rs,re,rw));
    const sw=Math.abs(ls.x-rs.x),hw=Math.abs(lh.x-rh.x);
    if(hw>0)a.hip_rot=rnd(Math.max(0,(1-hw/Math.max(sw,1))*90));
    a.sh_tilt=rnd(Math.abs(Math.atan2(rs.y-ls.y,rs.x-ls.x)*57.2958));
    return a;
}

function scorePos(ang,pos){
    const ideal=IDEALS[pos]||{};const sc={};
    const map={spine:'spine',l_arm:'l_arm',knee_l:'knee_l',hip_rot:'hip_rot'};
    for(const[ak,ik]of Object.entries(map)){
        if(!ideal[ik]||ang[ak]==null)continue;
        const[lo,hi]=ideal[ik],v=ang[ak];let dev=0;if(v<lo)dev=lo-v;else if(v>hi)dev=v-hi;
        const s=Math.max(0,Math.round(100-dev*5));
        sc[ak]={s,st:dev===0?'good':dev<=5?'warn':'bad',v,r:[lo,hi],dev:rnd(dev),dir:v<lo?'lo':'hi'};
    }
    return sc;
}

function posScore(sc){const v=Object.values(sc);return v.length?Math.round(v.reduce((a,x)=>a+x.s,0)/v.length):75}

function getVerdicts(ang,scores,pos){
    const lines=[];
    for(const[k,s]of Object.entries(scores)){
        const vd=VERDICTS[k];if(!vd)continue;
        if(s.st==='good')lines.push({icon:'✅',text:vd.good,type:'good'});
        else if(s.st==='warn')lines.push({icon:'⚠️',text:vd['warn_'+s.dir]||vd.warn||'Slightly off',type:'warn',fix:`Aim for ${s.r[0]}–${s.r[1]}°`});
        else lines.push({icon:'🔴',text:vd['bad_'+s.dir]||vd.bad||'Needs work',type:'bad',fix:`Target: ${s.r[0]}–${s.r[1]}°`});
    }
    return lines;
}

// ===== VISUAL DRAWING (AMG-style) =====
function drawVisual(cx,kps,ang,scores,pos,w,h){
    const ls=pt(kps,KP.L_SH),rs=pt(kps,KP.R_SH),lh=pt(kps,KP.L_HI),rh=pt(kps,KP.R_HI);
    const lk=pt(kps,KP.L_KN),rk=pt(kps,KP.R_KN),la=pt(kps,KP.L_AN),ra=pt(kps,KP.R_AN);
    const le=pt(kps,KP.L_EL),re=pt(kps,KP.R_EL),lw=pt(kps,KP.L_WR),rw=pt(kps,KP.R_WR);
    const nose=pt(kps,KP.NOSE);
    const mh={x:(lh.x+rh.x)/2,y:(lh.y+rh.y)/2},ms={x:(ls.x+rs.x)/2,y:(ls.y+rs.y)/2};
    const lw2=Math.max(2,w/250),dot=Math.max(4,w/140);

    // === IDEAL ZONE OVERLAYS ===

    // Spine angle zone (green translucent wedge from hips)
    const spSc=scores.spine?.st||'good';const spCol=sCol(spSc);
    // Draw ideal spine zone as a wedge
    const ideal=IDEALS[pos];
    if(ideal?.spine){
        const[lo,hi]=ideal.spine;const dist=Math.sqrt((ms.x-mh.x)**2+(ms.y-mh.y)**2)*1.2;
        cx.save();cx.translate(mh.x,mh.y);
        cx.fillStyle='rgba(52,211,153,0.08)';
        cx.beginPath();cx.moveTo(0,0);
        cx.lineTo(-Math.sin(lo*Math.PI/180)*dist,-Math.cos(lo*Math.PI/180)*dist);
        cx.lineTo(-Math.sin(hi*Math.PI/180)*dist,-Math.cos(hi*Math.PI/180)*dist);
        cx.closePath();cx.fill();
        // Zone borders
        cx.strokeStyle='rgba(52,211,153,0.3)';cx.lineWidth=1;cx.setLineDash([4,4]);
        cx.beginPath();cx.moveTo(0,0);cx.lineTo(-Math.sin(lo*Math.PI/180)*dist,-Math.cos(lo*Math.PI/180)*dist);cx.stroke();
        cx.beginPath();cx.moveTo(0,0);cx.lineTo(-Math.sin(hi*Math.PI/180)*dist,-Math.cos(hi*Math.PI/180)*dist);cx.stroke();
        cx.setLineDash([]);cx.restore();
    }

    // Swing plane line for Downswing/Impact
    if(pos==='Downswing'||pos==='Impact'||pos==='Top'){
        const handMid={x:(lw.x+rw.x)/2,y:(lw.y+rw.y)/2};
        // Ideal plane from ball area through hands
        cx.save();
        cx.strokeStyle='rgba(52,211,153,0.4)';cx.lineWidth=Math.max(2,w/200);cx.setLineDash([8,6]);
        const extX=handMid.x+(handMid.x-ms.x)*3,extY=handMid.y+(handMid.y-ms.y)*3;
        cx.beginPath();cx.moveTo(ms.x-(handMid.x-ms.x),ms.y-(handMid.y-ms.y));cx.lineTo(extX,extY);cx.stroke();
        cx.setLineDash([]);

        // "Slot" zone — a shaded area where hands should be on downswing
        if(pos==='Downswing'){
            cx.fillStyle='rgba(52,211,153,0.06)';
            const cx1=ms.x,cy1=ms.y;
            const r=Math.sqrt((handMid.x-ms.x)**2+(handMid.y-ms.y)**2)*1.3;
            cx.beginPath();
            cx.moveTo(cx1,cy1);
            const a1=Math.atan2(rh.y-ms.y,rh.x-ms.x);
            const a2=a1+0.4;
            cx.arc(cx1,cy1,r,a1,a2);cx.closePath();cx.fill();

            // Label "THE SLOT"
            const slotX=ms.x+Math.cos(a1+.2)*r*.6,slotY=ms.y+Math.sin(a1+.2)*r*.6;
            const fs=Math.max(10,w/45);
            cx.font=`bold ${fs}px 'DM Sans'`;cx.fillStyle='rgba(52,211,153,0.5)';
            cx.fillText('THE SLOT',slotX-30,slotY);
        }
        cx.restore();
    }

    // === SKELETON ===
    const pairs=[[ls,rs],[lh,rh],[ls,lh],[rs,rh],[ls,le],[le,lw],[rs,re],[re,rw],[lh,lk],[lk,la],[rh,rk],[rk,ra],[ls,nose],[rs,nose]];
    cx.strokeStyle='rgba(255,255,255,0.25)';cx.lineWidth=Math.max(1.5,w/350);
    for(const[a,b]of pairs){cx.beginPath();cx.moveTo(a.x,a.y);cx.lineTo(b.x,b.y);cx.stroke()}

    // === JOINTS (color-coded) ===
    const joints=[ls,rs,lh,rh,lk,rk,la,ra,le,re,lw,rw,nose];
    for(const j of joints){cx.fillStyle='rgba(255,255,255,0.9)';cx.beginPath();cx.arc(j.x,j.y,dot*.7,0,Math.PI*2);cx.fill();cx.strokeStyle='rgba(52,211,153,0.6)';cx.lineWidth=1.5;cx.stroke()}

    // === SPINE LINE (colored by score) ===
    cx.strokeStyle=spCol;cx.lineWidth=Math.max(3,w/180);
    const dx=ms.x-mh.x,dy=ms.y-mh.y;
    cx.beginPath();cx.moveTo(mh.x-dx*.2,mh.y-dy*.2);cx.lineTo(ms.x+dx*.25,ms.y+dy*.25);cx.stroke();

    // === LEFT ARM LINE (colored) ===
    const armSt=scores.l_arm?.st||'good';
    cx.strokeStyle=sCol(armSt);cx.lineWidth=Math.max(2.5,w/220);
    cx.beginPath();cx.moveTo(ls.x,ls.y);cx.lineTo(le.x,le.y);cx.lineTo(lw.x,lw.y);cx.stroke();

    // === SIMPLE LABELS (not numbers, just status) ===
    const fs=Math.max(12,w/40);
    if(scores.spine){
        const txt=scores.spine.st==='good'?'✓ Spine':scores.spine.st==='warn'?'⚠ Spine':'✗ Spine';
        drawBadge(cx,txt,mh.x+20,mh.y-20,spCol,fs,w);
    }
    if(scores.l_arm){
        const txt=scores.l_arm.st==='good'?'✓ Arm':scores.l_arm.st==='warn'?'⚠ Arm':'✗ Arm';
        drawBadge(cx,txt,le.x-50,le.y-15,sCol(armSt),fs,w);
    }
    if(scores.knee_l){
        const kSt=scores.knee_l.st;
        const txt=kSt==='good'?'✓ Knees':kSt==='warn'?'⚠ Knees':'✗ Knees';
        drawBadge(cx,txt,lk.x-40,lk.y+20,sCol(kSt),fs,w);
    }
    if(scores.hip_rot){
        const hSt=scores.hip_rot.st;
        const txt=hSt==='good'?'✓ Hips':hSt==='warn'?'⚠ Hips':'✗ Hips';
        drawBadge(cx,txt,mh.x-60,mh.y+25,sCol(hSt),fs,w);
    }
}

function drawBadge(cx,text,x,y,color,fs,fw){
    cx.font=`600 ${fs}px 'DM Sans'`;const tm=cx.measureText(text);
    x=Math.max(5,Math.min(x,fw-tm.width-16));
    cx.fillStyle='rgba(0,0,0,0.7)';
    const bx=x-6,by=y-fs-2,bw=tm.width+12,bh=fs+8;
    cx.beginPath();cx.roundRect?cx.roundRect(bx,by,bw,bh,6):cx.fillRect(bx,by,bw,bh);cx.fill();
    cx.fillStyle=color;cx.fillText(text,x,y);
}

function drawHdr(cx,pos,sc,w){
    const h=Math.max(34,w/12);cx.fillStyle='rgba(0,0,0,0.7)';cx.fillRect(0,0,w,h);
    cx.font=`bold ${h*.48}px 'DM Sans'`;cx.fillStyle='#fff';cx.fillText(pos,10,h*.66);
    const c=sc>=75?'#34d399':sc>=50?'#fbbf24':'#f87171';const t=`${sc}/100`;cx.fillStyle=c;cx.fillText(t,w-cx.measureText(t).width-10,h*.66);
}

function sCol(s){return s==='good'?'#34d399':s==='warn'?'#fbbf24':'#f87171'}

function calcScore(results){
    let ws=0,wt=0;const ps={};
    for(const r of results){const s=r.pscore;ps[r.position]=s;const w=POS_W[r.position]||1;ws+=s*w;wt+=w}
    const sc=wt>0?Math.round(ws/wt):0;
    let hc;if(sc>=90)hc=Math.max(-2,(100-sc)*.5-2);else if(sc>=80)hc=(90-sc)*.5;else if(sc>=70)hc=5+(80-sc)*.5;else if(sc>=60)hc=10+(70-sc)*.5;else if(sc>=50)hc=15+(60-sc)*.5;else if(sc>=40)hc=20+(50-sc)*.5;else hc=25+(40-sc)*.5;
    let g;if(sc>=90)g='Tour-caliber mechanics';else if(sc>=80)g='Strong fundamentals';else if(sc>=70)g='Solid — minor tweaks needed';else if(sc>=60)g='Good foundation to build on';else if(sc>=50)g='Key fixes will help a lot';else g='Focus on fundamentals first';
    return{score:sc,handicap:rnd(hc),grade:g,ps};
}

// ===== SHOW MULTI-SWING RESULTS =====
function showSwings(){
    $('msr').classList.remove('hidden');$('swDetail').classList.add('hidden');
    $('swCnt').textContent=dSwings.length+' swing'+(dSwings.length!==1?'s':'');
    renderSL();speak(`Found ${dSwings.length} swings.`);
}
function renderSL(){
    const l=$('swList');l.innerHTML='';
    dSwings.forEach((sw,i)=>{
        if(sw.st==='discarded')return;
        const sc=sw.score.score,col=sc>=75?'var(--g)':sc>=50?'var(--y)':'var(--r)';
        const img=sw.positions.find(p=>p.position==='Impact')?.img||sw.positions[0]?.img||'';
        const saved=sw.st==='saved';
        // Get top verdict
        const topV=sw.positions.flatMap(p=>p.verdicts).find(v=>v.type!=='good');
        const verdict=topV?topV.text:'Looking good!';
        const d=document.createElement('div');d.className='sw-card';
        d.innerHTML=`${img?`<img src="${img}" onclick="viewSw(${i})">`:''}
            <div class="sw-info" onclick="viewSw(${i})" style="cursor:pointer">
                <div style="font-weight:600">Swing ${sw.idx}</div>
                <div class="mono" style="color:${col};font-size:18px;font-weight:700">${sc}<span style="font-size:12px;color:var(--td)"> / 100</span></div>
                <div style="font-size:12px;color:var(--td);margin-top:2px">${verdict.substring(0,45)}</div>
            </div>
            <div class="sw-acts">
                <button class="btn btn-s ${saved?'btn-g':'btn-o'}" onclick="togSave(${i})" style="font-size:18px;padding:8px 12px">${saved?'✓':'+'}</button>
                <button class="btn btn-s btn-r" onclick="disc(${i})" style="font-size:18px;padding:8px 12px">✕</button>
            </div>`;
        l.appendChild(d);
    });
    const cnt=dSwings.filter(s=>s.st==='saved').length;
    $('batchSec').classList.toggle('hidden',cnt===0);
    if(cnt)$('batchBtn').textContent=`🤖 Get Coaching for ${cnt} Swing${cnt>1?'s':''}`;
}
function togSave(i){dSwings[i].st=dSwings[i].st==='saved'?'pending':'saved';renderSL()}
function disc(i){dSwings[i].st='discarded';renderSL()}
function saveAll(){dSwings.forEach(s=>{if(s.st!=='discarded')s.st='saved'});renderSL()}
function discAll(){if(confirm('Discard all?')){dSwings.forEach(s=>s.st='discarded');renderSL()}}

function viewSw(i){
    const sw=dSwings[i];$('swDetail').classList.remove('hidden');
    $('dLabel').textContent='Swing '+sw.idx;

    // Plain English panel
    const ep=$('engPanel');
    const allV=sw.positions.flatMap(p=>p.verdicts.map(v=>({...v,pos:p.position})));
    const goods=allV.filter(v=>v.type==='good'),issues=allV.filter(v=>v.type!=='good');
    let html=`<div style="font-weight:700;margin-bottom:10px;font-size:15px">Score: <span class="mono" style="color:${sw.score.score>=70?'var(--g)':'var(--y)'}">${sw.score.score}/100</span> · HC: ${sw.score.handicap}</div>`;
    if(issues.length){html+='<div style="font-size:12px;color:var(--td);margin-bottom:6px">THINGS TO WORK ON</div>';issues.forEach(v=>{html+=`<div class="eng-line"><div class="eng-icon">${v.icon}</div><div><strong>${v.pos}:</strong> ${v.text}${v.fix?`<br><span class="eng-fix">→ ${v.fix}</span>`:''}</div></div>`})}
    if(goods.length){html+=`<div style="font-size:12px;color:var(--td);margin:10px 0 6px">WHAT'S WORKING</div>`;goods.forEach(v=>{html+=`<div class="eng-line"><div class="eng-icon">✅</div><div>${v.pos}: ${v.text}</div></div>`})}
    ep.innerHTML=html;

    // Position thumbs
    const row=$('dPosRow');row.innerHTML='';
    sw.positions.forEach((p,j)=>{
        const ps=posScore(p.scores),pc=ps>=75?'var(--g)':ps>=50?'var(--y)':'var(--r)';
        const d=document.createElement('div');d.className='pos-th'+(j===0?' on':'');
        d.innerHTML=`<img src="${p.img}"><div class="pos-th-i"><span style="font-weight:500">${p.position}</span> <span class="mono" style="color:${pc};float:right">${ps}</span></div>`;
        d.onclick=()=>{row.querySelectorAll('.pos-th').forEach(t=>t.classList.remove('on'));d.classList.add('on');showPD(p)};
        row.appendChild(d);
    });
    if(sw.positions.length)showPD(sw.positions[0]);
    $('swDetail').scrollIntoView({behavior:'smooth'});
}

function showPD(p){
    $('dPosCard').classList.remove('hidden');
    const cv=$('dCanvas'),img=new Image();
    img.onload=()=>{cv.width=img.width;cv.height=img.height;cv.style.height='auto';cv.getContext('2d').drawImage(img,0,0)};
    img.src=p.img;
    // Verdict badges
    const vd=$('dVerdicts');vd.innerHTML='';
    p.verdicts.forEach(v=>{vd.innerHTML+=`<span class="verdict v-${v.type}">${v.icon} ${v.text.split('—')[0].trim()}</span>`});
    // Technical details
    const ad=$('dAngles');ad.innerHTML='';
    for(const[k,v]of Object.entries(p.angles)){if(k.startsWith('head_')||k==='hip_center_x')continue;const s=p.scores[k];const col=s?sCol(s.st):'var(--td)';ad.innerHTML+=`<div style="display:flex;justify-content:space-between;padding:4px 0;border-bottom:1px solid var(--brd)"><span>${k.replace(/_/g,' ')}</span><span class="mono" style="color:${col}">${v}°${s?` (${s.r[0]}-${s.r[1]}°)`:''}</span></div>`}
}

// ===== BATCH COACHING =====
async function runBatch(){
    const saved=dSwings.filter(s=>s.st==='saved');if(!saved.length)return;
    $('batchBtn').disabled=true;$('batchBtn').textContent='🤖 Analyzing...';
    try{
        const txt=await callClaude(saved);
        saved.forEach(sw=>{state.sessions.unshift({id:Date.now()+Math.random()*999,date:sw.date,club:sw.club,swingScore:sw.score,positions:sw.positions.map(p=>({position:p.position,angles:p.angles,scores:p.scores,imageData:p.img})),coaching:txt,launchData:sw.launch,notes:''})});
        if(state.sessions.length>500)state.sessions=state.sessions.slice(0,500);save();
        $('batchRes').classList.remove('hidden');
        try{$('batchTxt').innerHTML=marked.parse(txt)}catch{$('batchTxt').innerHTML=txt.replace(/\n/g,'<br>')}
        $('batchBtn').textContent='✓ Done — Swings Saved';speak('Coaching complete.');
        $('batchRes').scrollIntoView({behavior:'smooth'});
    }catch(e){$('batchBtn').disabled=false;$('batchBtn').textContent='🤖 Retry';alert(e.message)}
}

async function callClaude(swings){
    const content=[];
    let o=`## Session: ${swings.length} swings with ${swings[0].club}\n\nScores: ${swings.map(s=>`Swing ${s.idx}: ${s.score.score}`).join(', ')}\n`;
    content.push({type:'text',text:o});
    const sorted=[...swings].sort((a,b)=>b.score.score-a.score.score);
    const sample=[sorted[0]];if(sorted.length>1)sample.push(sorted[sorted.length-1]);if(sorted.length>2)sample.push(sorted[Math.floor(sorted.length/2)]);
    for(const sw of sample){
        content.push({type:'text',text:`\n### Swing ${sw.idx} (${sw.score.score}/100):`});
        for(const p of sw.positions){if(p.img){content.push({type:'image',source:{type:'base64',media_type:'image/jpeg',data:p.img.split(',')[1]}})}
            let t=`**${p.position}:** `;for(const[k,v]of Object.entries(p.angles)){if(!k.startsWith('head'))t+=`${k}: ${v}° `}content.push({type:'text',text:t})}
    }
    if(swings[0].launch){let t='\n### Launch Data:\n';for(const[k,v]of Object.entries(swings[0].launch))t+=`${k}: ${v}\n`;content.push({type:'text',text:t})}
    content.push({type:'text',text:'\nGive a complete session analysis. Focus on patterns, consistency, fatigue. Plain English — no jargon. Severity-rank issues. Top 3 priorities with drills.'});

    const r=await fetch('https://api.anthropic.com/v1/messages',{method:'POST',headers:{'Content-Type':'application/json','x-api-key':state.key,'anthropic-version':'2023-06-01','anthropic-dangerous-direct-browser-access':'true'},
        body:JSON.stringify({model:'claude-sonnet-4-20250514',max_tokens:4000,system:'You are SwingIQ, an expert golf coach. Analyze this practice session. Use PLAIN ENGLISH — no technical jargon unless explaining. Be specific, actionable, encouraging. Format with headers and bullet points. Include: session overview, what\'s working, severity-ranked issues (1-10), top 3 priorities with drills, and what made the best swing work.',messages:[{role:'user',content}]})});
    if(!r.ok){const e=await r.json().catch(()=>({}));throw new Error(e.error?.message||'API error '+r.status)}
    return(await r.json()).content.map(b=>b.text||'').join('\n');
}

// ===== LIVE PRACTICE =====
function toggleLive(){if(liveOn)stopLive();else startLive()}
function startLive(){
    if(!liveStream||!detector){alert('Camera or detector not ready');return}
    liveOn=true;liveCnt=0;prevGray=null;mBase=0;
    $('liveBtn').textContent='⏹ Stop';$('liveBtn').style.background='var(--r)';
    $('liveCount').classList.remove('hidden');$('liveCount').textContent='0 swings';
    $('liveStat').textContent='Swing when ready...';speak('Ready. Swing when you want.');
    const vid=$('liveVid'),c=$('lCvs'),cx=c.getContext('2d');
    liveInt=setInterval(()=>{
        if(!liveOn)return;c.width=vid.videoWidth||640;c.height=vid.videoHeight||480;cx.drawImage(vid,0,0);
        const g=gray(cx.getImageData(0,0,c.width,c.height));
        if(prevGray){let m=0;const s=16;for(let i=0;i<g.length;i+=s)m+=Math.abs(g[i]-prevGray[i]);m/=(g.length/s);
            if(!mBase)mBase=m*1.5+2;
            if(m>mBase*3&&!cooldown){cooldown=true;setTimeout(()=>{cx.drawImage(vid,0,0);liveAnalyze(cx.getImageData(0,0,c.width,c.height),c.width,c.height);cooldown=false},800)}
            mBase=mBase*.98+m*.02;
        }prevGray=g;
    },100);
}
function gray(d){const g=new Uint8Array(d.width*d.height);for(let i=0;i<g.length;i++){const j=i*4;g[i]=(d.data[j]*.3+d.data[j+1]*.59+d.data[j+2]*.11)|0}return g}
async function liveAnalyze(fd,w,h){
    liveCnt++;$('liveCount').textContent=liveCnt+' swing'+(liveCnt>1?'s':'');
    const c=$('fCvs');c.width=w;c.height=h;c.getContext('2d').putImageData(fd,0,0);
    try{
        const poses=await detector.estimatePoses(c);if(!poses.length)return speak('Couldn\'t see you. Try again.');
        const ang=calcAngles(poses[0].keypoints,w,h),sc=scorePos(ang,'Impact'),vd=getVerdicts(ang,sc,'Impact');
        // Voice: plain English
        const issues=vd.filter(v=>v.type!=='good');
        let msg=`Swing ${liveCnt}. `;
        if(!issues.length)msg+='That looked good! ';
        else issues.forEach(v=>{msg+=v.text+'. '});
        speak(msg);
        // Card
        const ac=$('aCvs');ac.width=w;ac.height=h;const ax=ac.getContext('2d');ax.putImageData(fd,0,0);
        drawVisual(ax,poses[0].keypoints,ang,sc,'Impact',w,h);drawHdr(ax,'Swing '+liveCnt,posScore(sc),w);
        const card=document.createElement('div');card.className='sw-card fade';
        card.innerHTML=`<img src="${ac.toDataURL('image/jpeg',.7)}"><div class="sw-info"><div style="font-weight:600">Swing ${liveCnt}</div><div style="font-size:12px;color:var(--td)">${issues.length?issues[0].text:'Looking good!'}</div></div>`;
        $('liveCards').insertBefore(card,$('liveCards').firstChild);
    }catch(e){console.error(e)}
}
function stopLive(){liveOn=false;if(liveInt){clearInterval(liveInt);liveInt=null}$('liveBtn').textContent='▶ Start';$('liveBtn').style.background='';$('liveStat').textContent='Session complete.';if(liveCnt)speak(`Done. ${liveCnt} swings.`)}

// ===== LAUNCH DATA =====
function getLM(){const f={ball_speed:'lmBS',club_speed:'lmCS',launch_angle:'lmLA',spin_rate:'lmSR',carry:'lmCY',smash_factor:'lmSF',total_distance:'lmTD',attack_angle:'lmAA'};const d={};for(const[k,id]of Object.entries(f)){const v=$(id).value;if(v)d[k]=parseFloat(v)}return Object.keys(d).length?d:null}

// ===== HISTORY =====
function renderHist(){
    const f=$('hFilt').value;let s=state.sessions;if(f)s=s.filter(x=>x.club===f);
    $('hList').innerHTML=s.length?s.map(x=>{const d=new Date(x.date).toLocaleDateString('en-US',{month:'short',day:'numeric'});const sc=x.swingScore?.score??'--';const col=sc>=75?'var(--g)':sc>=50?'var(--y)':'var(--r)';
        return`<div class="card" style="display:flex;justify-content:space-between;align-items:center;padding:16px;cursor:pointer"><div><div style="font-weight:600">${x.club}</div><div style="font-size:12px;color:var(--td)">${d}</div></div><div style="text-align:right"><div class="mono" style="color:${col};font-size:20px;font-weight:700">${sc}</div><div style="font-size:12px;color:var(--td)">HC: ${x.swingScore?.handicap??'--'}</div></div></div>`}).join(''):'<p style="text-align:center;color:var(--td);padding:40px">No sessions yet.</p>';
}

// ===== PROGRESS =====
let cS,cH,cL;
function renderProg(){
    const f=$('pFilt').value;let s=[...state.sessions].reverse();if(f)s=s.filter(x=>x.club===f);if(!s.length)return;
    const lb=s.map(x=>new Date(x.date).toLocaleDateString('en-US',{month:'short',day:'numeric'}));
    const o={responsive:true,plugins:{legend:{display:false}},scales:{x:{ticks:{color:'#6b7280',font:{size:10}},grid:{color:'rgba(255,255,255,.04)'}},y:{ticks:{color:'#6b7280'},grid:{color:'rgba(255,255,255,.04)'}}}};
    if(cS)cS.destroy();cS=new Chart($('pSc'),{type:'line',data:{labels:lb,datasets:[{data:s.map(x=>x.swingScore?.score),borderColor:'#34d399',backgroundColor:'rgba(52,211,153,.06)',fill:true,tension:.3,pointRadius:3}]},options:{...o,scales:{...o.scales,y:{...o.scales.y,min:0,max:100}}}});
    if(cH)cH.destroy();cH=new Chart($('pHc'),{type:'line',data:{labels:lb,datasets:[{data:s.map(x=>x.swingScore?.handicap),borderColor:'#fbbf24',backgroundColor:'rgba(251,191,36,.06)',fill:true,tension:.3,pointRadius:3}]},options:o});
    if(cL)cL.destroy();const cs={ball_speed:'#f87171',club_speed:'#60a5fa',carry:'#34d399'};const dl={ball_speed:'Ball Spd',club_speed:'Club Spd',carry:'Carry'};const ds=[];
    for(const[k,c]of Object.entries(cs)){const v=s.map(x=>x.launchData?.[k]??null);if(v.some(x=>x!=null))ds.push({label:dl[k],data:v,borderColor:c,tension:.3,pointRadius:2,spanGaps:true})}
    cL=new Chart($('pLm'),{type:'line',data:{labels:lb,datasets:ds},options:{...o,plugins:{legend:{display:true,labels:{color:'#6b7280',font:{size:10}}}}}});
}
</script>
</body>
</html>
