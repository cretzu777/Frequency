<!DOCTYPE html>  
<html lang="ro">  
<head>  
<meta charset="UTF-8"><meta name="viewport" content="width=device-width,initial-scale=1,maximum-scale=1,user-scalable=no">  
<title>Generator Stereo & Binaural</title>  
<style>  
*{box-sizing:border-box;font-family:-apple-system,sans-serif}body{margin:0;padding:14px;background:#0b1120;color:#f8fafc;display:flex;justify-content:center}  
.box{width:100%;max-width:460px;background:#1e293b;border-radius:18px;padding:18px}h1{font-size:1.2rem;text-align:center;margin:0 0 14px}  
.card{background:#0f172a;border:1px solid #334155;border-radius:12px;padding:12px;margin-bottom:12px}  
.top{display:flex;justify-content:space-between;font-size:.82rem;color:#94a3b8;margin-bottom:8px;font-weight:600}  
.grid{display:grid;grid-template-columns:1fr 1fr;gap:6px}.r{display:flex;align-items:center;gap:6px;background:#1e293b;padding:8px;border-radius:8px;border:1px solid #334155;font-size:.8rem}  
.r:has(input:checked){border-color:#38bdf8;background:rgba(56,189,248,.15)}.full{grid-column:span 2}  
.chL{border-left:4px solid #38bdf8}.chR{border-left:4px solid #a855f7}.row{display:flex;justify-content:space-between;align-items:center}  
input[type=number]{width:95px;background:#1e293b;color:#fff;border:1px solid #334155;border-radius:6px;padding:5px;font-size:1rem;font-weight:700;text-align:right}  
input[type=range]{width:100%;margin:8px 0;accent-color:#38bdf8}.chR input[type=range]{accent-color:#a855f7}  
.btns{display:grid;grid-template-columns:repeat(6,1fr);gap:4px}.btns button,.w{background:#1e293b;color:#fff;border:1px solid #334155;padding:6px 2px;border-radius:6px;font-size:.75rem;font-weight:600}  
.waves{display:grid;grid-template-columns:repeat(4,1fr);gap:5px;margin-bottom:10px}.w.on{background:#38bdf8;color:#0f172a}  
.play{width:100%;padding:14px;border:0;border-radius:12px;font-size:1rem;font-weight:700;background:#38bdf8;color:#0f172a}.play.stop{background:#ef4444;color:#fff}  
</style>  
</head>  
<body>  
<div class="box">  
<h1>Generator Stereo & Binaural</h1>  
<div class="card">  
<div class="top"><span>Mod Binaural</span><span id="df">Diferență: 0 Hz</span></div>  
<div class="grid">  
<label class="r"><input type="radio" name="m" value="none" checked onchange="cm()">None</label>  
<label class="r"><input type="radio" name="m" value="equal" onchange="cm()">Equal (+0)</label>  
<label class="r"><input type="radio" name="m" value="delta" onchange="cm()">Delta (+2)</label>  
<label class="r"><input type="radio" name="m" value="theta" onchange="cm()">Theta (+6)</label>  
<label class="r"><input type="radio" name="m" value="alpha" onchange="cm()">Alpha (+10)</label>  
<label class="r"><input type="radio" name="m" value="beta" onchange="cm()">Beta (+20)</label>  
<label class="r full"><input type="radio" name="m" value="gamma" onchange="cm()">Gamma (+40 Hz)</label>  
</div></div>  
<div class="card chL">  
<div class="row"><b style="color:#38bdf8">STÂNGA (L)</b><div><input type="number" id="iL" min="0" max="10000" step="0.1" value="200" oninput="hi('L',this.value)"> Hz</div></div>  
<input type="range" id="sL" min="0" max="10000" value="200" oninput="hi('L',this.value)">  
<div class="btns"><button onclick="st('L',-10)">-10</button><button onclick="st('L',-1)">-1</button><button onclick="st('L',-.1)">-.1</button><button onclick="st('L',.1)">+.1</button><button onclick="st('L',1)">+1</button><button onclick="st('L',10)">+10</button></div>  
</div>  
<div class="card chR">  
<div class="row"><b style="color:#a855f7">DREAPTA (R)</b><div><input type="number" id="iR" min="0" max="10000" step="0.1" value="200" oninput="hi('R',this.value)"> Hz</div></div>  
<input type="range" id="sR" min="0" max="10000" value="200" oninput="hi('R',this.value)">  
<div class="btns"><button onclick="st('R',-10)">-10</button><button onclick="st('R',-1)">-1</button><button onclick="st('R',-.1)">-.1</button><button onclick="st('R',.1)">+.1</button><button onclick="st('R',1)">+1</button><button onclick="st('R',10)">+10</button></div>  
</div>  
<div class="card">  
<div class="waves"><button class="w on" onclick="sw('sine',this)">Sinus</button><button class="w" onclick="sw('square',this)">Pătrat</button><button class="w" onclick="sw('triangle',this)">Triunghi</button><button class="w" onclick="sw('sawtooth',this)">Ferăstrău</button></div>  
<div class="top"><span>Volum Comun (L + R)</span><span id="vd">50%</span></div>  
<input type="range" id="vs" min="0" max="100" value="50" oninput="sv(this.value)">  
</div>  
<button class="play" id="pb" onclick="tg()">PORNEȘTE AUDIO STEREO</button>  
</div>  
<script>  
const OFF={none:null,equal:0,delta:2,theta:6,alpha:10,beta:20,gamma:40};  
let fL=200,fR=200,le='L',wv='sine',on=0,ctx,oL,oR,gL,gR;  
const cl=v=>Math.round(Math.min(10000,Math.max(0,parseFloat(v)||0))*10)/10;  
const gm=()=>document.querySelector('input[name="m"]:checked').value;  
function hi(c,v){le=c;v=cl(v);let o=OFF[gm()];if(c=='L'){fL=v;if(o!==null)fR=cl(fL+o)}else{fR=v;if(o!==null)fL=cl(fR+o)}up(c)}  
function st(c,d){hi(c,(c=='L'?fL:fR)+d)}  
function cm(){let o=OFF[gm()];if(o!==null){if(le=='L')fR=cl(fL+o);else fL=cl(fR+o)}up()}  
function up(a){if(a!='L')iL.value=fL;sL.value=fL;if(a!='R')iR.value=fR;sR.value=fR;df.textContent='Diferență: '+Math.round(Math.abs(fL-fR)*10)/10+' Hz';if(on&&ctx){oL.frequency.setValueAtTime(fL,ctx.currentTime);oR.frequency.setValueAtTime(fR,ctx.currentTime)}}  
function sw(t,b){wv=t;document.querySelectorAll('.w').forEach(x=>x.classList.remove('on'));b.classList.add('on');if(oL)oL.type=oR.type=t}  
function sv(v){vd.textContent=v+'%';if(ctx&&gL){gL.gain.setValueAtTime(v/100,ctx.currentTime);gR.gain.setValueAtTime(v/100,ctx.currentTime)}}  
function tg(){if(!on){ctx=ctx||new(window.AudioContext||window.webkitAudioContext)();if(ctx.state=='suspended')ctx.resume();oL=ctx.createOscillator();oR=ctx.createOscillator();gL=ctx.createGain();gR=ctx.createGain();let m=ctx.createChannelMerger(2),l=vs.value/100;oL.type=oR.type=wv;oL.frequency.setValueAtTime(fL,ctx.currentTime);oR.frequency.setValueAtTime(fR,ctx.currentTime);gL.gain.setValueAtTime(l,ctx.currentTime);gR.gain.setValueAtTime(l,ctx.currentTime);oL.connect(gL);oR.connect(gR);gL.connect(m,0,0);gR.connect(m,0,1);m.connect(ctx.destination);oL.start();oR.start();on=1;pb.textContent='OPREȘTE AUDIO';pb.classList.add('stop')}else{oL.stop();oR.stop();on=0;pb.textContent='PORNEȘTE AUDIO STEREO';pb.classList.remove('stop')}}  
</script>  
</body>  
</html>  
  
