
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Idee Infotech – Letter Generator</title>
<style>
:root{--bg:#f4f6fb;--card:#fff;--text:#1b2437;--muted:#5b6578;--line:#d9dfec;--brand:#1d4ed8;--brand2:#0f2a6b;box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}
@media (prefers-color-scheme:dark){:root:not([data-theme="light"]){--bg:#0f1420;--card:#192033;--text:#e8ecf6;--muted:#9aa5bd;--line:#2c3650;--brand:#5b8cff}}
:root[data-theme="dark"]{--bg:#0f1420;--card:#192033;--text:#e8ecf6;--muted:#9aa5bd;--line:#2c3650;--brand:#5b8cff}
html{scroll-padding-top:env(safe-area-inset-top,0px)}
*{box-sizing:border-box}
body{margin:0;background:var(--bg);color:var(--text);font-family:'Segoe UI',system-ui,-apple-system,Arial,sans-serif}
.wrap{max-width:1280px;margin:0 auto;padding:16px;display:grid;grid-template-columns:380px 1fr;gap:20px}
@media(max-width:900px){.wrap{grid-template-columns:1fr}}
.panel{background:var(--card);border:1px solid var(--line);border-radius:12px;padding:16px}
h1{font-size:18px;margin:0 0 12px}
.tabs{display:flex;gap:6px;margin-bottom:12px;flex-wrap:wrap}
.tab{flex:1;padding:8px 6px;border:1px solid var(--line);background:transparent;color:var(--text);border-radius:8px;cursor:pointer;font-size:13px}
.tab.on{background:var(--brand);color:#fff;border-color:var(--brand)}
label{display:block;font-size:12px;color:var(--muted);margin:10px 0 3px}
input,textarea,select{width:100%;padding:8px 10px;border:1px solid var(--line);border-radius:8px;background:var(--bg);color:var(--text);font:inherit;font-size:14px}
.row{display:grid;grid-template-columns:1fr 1fr;gap:8px}
.btns{display:flex;gap:8px;margin-top:16px;flex-wrap:wrap}
button.p{flex:1;padding:10px;border:0;border-radius:8px;background:var(--brand);color:#fff;font-size:14px;cursor:pointer}
button.s{padding:10px 14px;border:1px solid var(--line);border-radius:8px;background:transparent;color:var(--text);cursor:pointer;font-size:14px}
button:disabled{opacity:.45;cursor:not-allowed}
.note{font-size:12px;color:var(--muted);margin-top:10px}
.pv{overflow-x:auto}
.paper{width:794px;height:1122px;background:#fff;color:#1b2437;display:flex;flex-direction:column;margin:0 auto;box-shadow:0 2px 14px rgba(0,0,0,.18);font-family:'Segoe UI',Arial,sans-serif}
.hd{background:#0f2a6b;color:#fff;padding:26px 44px 18px;border-bottom:6px solid #1d4ed8}
.hd .n{font-size:30px;font-weight:700;letter-spacing:1px}
.hd .t{font-size:12px;opacity:.85;margin-top:2px;letter-spacing:2px;text-transform:uppercase}
.bd{padding:30px 44px;flex:1;font-size:14px;line-height:1.65}
.meta{display:flex;justify-content:space-between;margin-bottom:18px;font-size:13px}
.sub{font-weight:700;text-decoration:underline;margin:16px 0}
.bd p{margin:0 0 12px}
.bd table{border-collapse:collapse;margin:10px 0 14px;width:100%}
.bd td{border:1px solid #c9d1e3;padding:6px 10px;font-size:13px}
.bd td:first-child{background:#eef2fb;width:34%;font-weight:600}
.sig{margin-top:34px}
.ft{background:#0f2a6b;color:#fff;padding:14px 44px;font-size:12px;display:flex;justify-content:space-between;gap:14px;border-top:4px solid #1d4ed8}
</style>
</head>
<body>
<div class="wrap">
<div class="panel">
<h1>Letter Generator</h1>
<div class="tabs" id="tabs">
<button class="tab on" data-t="call">Call Letter</button>
<button class="tab" data-t="conf">Confirmation</button>
<button class="tab" data-t="join">Joining Letter</button>
</div>
<label>Candidate name</label><input id="name" value="">
<label>Address</label><textarea id="addr" rows="2"></textarea>
<div class="row"><div><label>Phone</label><input id="phone"></div><div><label>Email</label><input id="mail"></div></div>
<label>Position</label><select id="pos"><option value="">— Select position —</option><option>Digital Marketing Executive</option><option>SEO Executive</option><option>Social Media Manager</option><option>Performance Marketing (Ads) Executive</option><option>Content Writer</option><option>Graphic Designer</option><option>UI/UX Designer</option><option>Video Editor</option><option>Motion Graphics Artist</option><option>Photographer / Videographer</option><option>Web Developer</option><option>Business Development Executive</option><option>Telecaller / Tele-sales</option><option>Client Relationship Executive</option><option>HR Executive</option><option>Accounts Executive</option><option>Office Administrator</option><option>Intern – Digital Marketing</option><option>Other</option></select><input id="pos2" placeholder="Type position" style="display:none;margin-top:6px"><label>Letter date</label><input id="date" type="date">
<div id="f-call">
<div class="row"><div><label>Interview date</label><input id="idate" type="date"></div><div><label>Time</label><input id="itime" type="time" value="10:00"></div></div>
<label>Interview mode</label><select id="imode"><option>Offline</option><option>Online</option></select>
<div id="m-off"><label>Venue</label><input id="venue"></div>
<div id="m-on" style="display:none"><div class="row"><div><label>Platform</label><select id="plat"><option>Google Meet</option><option>Zoom</option><option>Microsoft Teams</option><option>WhatsApp Video Call</option></select></div><div><label>Meeting link / ID</label><input id="link"></div></div></div>
<label>Documents to bring</label><input id="docs" value="Resume, ID proof, education certificates, passport-size photo">
</div>
<div id="f-conf" style="display:none">
<div class="row"><div><label>Salary (monthly)</label><input id="sal"></div><div><label>Joining date</label><input id="jdate" type="date"></div></div>
<label>Reply by (date)</label><input id="rdate" type="date">
</div>
<div id="f-join" style="display:none">
<div class="row"><div><label>Date of joining</label><input id="jdate2" type="date"></div><div><label>Salary (monthly)</label><input id="sal2"></div></div>
<div class="row"><div><label>Probation (months)</label><input id="prob" value="3"></div><div><label>Reporting to</label><input id="rep"></div></div>
<label>Working hours</label><input id="hours" value="9:30 AM to 6:30 PM, Monday to Saturday">
</div>
<hr style="border:0;border-top:1px solid var(--line);margin:14px 0 0">
<label>Company address (footer)</label><input id="caddr" value="Salem, Tamil Nadu">
<div class="row"><div><label>Signatory name</label><input id="sname"></div><div><label>Designation</label><input id="sdes" value="Authorised Signatory"></div></div>
<div class="btns">
<button class="p" id="go">Submit &amp; Generate</button>
<button class="s" id="pdf" disabled>Download PDF</button>
</div>
<div class="note" id="msg">Fill the details and press Submit to see the letter.</div>
</div>
<div class="pv"><div class="paper" id="paper"></div></div>
</div>
<script src="https://cdnjs.cloudflare.com/ajax/libs/html2pdf.js/0.10.1/html2pdf.bundle.min.js"></script>
<script>
var type='call',$=function(i){return document.getElementById(i)};
var CO={n:'IDEE INFOTECH',mail:'ideeinfotech@gmail.com',ph:'7810010572'};
function esc(s){return String(s==null?'':s).replace(/[&<>]/g,function(c){return{'&':'&amp;','<':'&lt;','>':'&gt;'}[c]})}
function fd(v){if(!v)return '________';var d=new Date(v+'T00:00:00');return d.toLocaleDateString('en-GB',{day:'2-digit',month:'long',year:'numeric'})}
function ft(v){if(!v)return '';var p=v.split(':'),h=+p[0];return (h%12||12)+':'+p[1]+(h>=12?' PM':' AM')}
function v(i){return esc($(i).value.trim())||'________'}
function ref(){var k={call:'CL',conf:'CF',join:'JL'}[type],d=new Date();return 'IDEE/'+k+'/'+d.getFullYear()+'/'+String(d.getMonth()+1).padStart(2,'0')+String(d.getDate()).padStart(2,'0')+'/'+(Math.floor(Math.random()*900)+100)}
var R=ref();
function getPos(){return $('pos').value==='Other'?$('pos2').value:$('pos').value}
function isOn(){return $('imode').value==='Online'}
function modeRows(){return isOn()?[['Platform',v('plat')],['Meeting link / ID',v('link')]]:[['Venue',v('venue')]]}
function tbl(rows){return '<table>'+rows.map(function(r){return '<tr><td>'+r[0]+'</td><td>'+r[1]+'</td></tr>'}).join('')+'</table>'}
function body(){
var nm=v('name'),pos=esc(getPos().trim())||'________',t='';
if(type==='call'){
t='<div class="sub">Subject: Call letter for interview – '+pos+'</div><p>Dear '+nm+',</p><p>Thank you for applying for the position of <b>'+pos+'</b> at Idee Infotech. After reviewing your profile, we are pleased to invite you for an interview. The details are given below:</p>'+tbl([['Date',fd($('idate').value)],['Time',ft($('itime').value)||'________'],['Mode',v('imode')]].concat(modeRows(),[['Position',pos]]))+'<p>'+(isOn()?'Please be online 10 minutes early and keep the following documents ready: ':'Please bring the following documents: ')+v('docs')+'.</p><p>Kindly confirm your attendance by replying to this letter or calling us on '+CO.ph+'.</p><p>We look forward to meeting you.</p>';
}else if(type==='conf'){
t='<div class="sub">Subject: Confirmation of selection – '+pos+'</div><p>Dear '+nm+',</p><p>We are pleased to inform you that you have been selected for the position of <b>'+pos+'</b> at Idee Infotech, following your interview with us.</p>'+tbl([['Position',pos],['Monthly salary',v('sal')],['Date of joining',fd($('jdate').value)],['Reply by',fd($('rdate').value)]])+'<p>Please confirm your acceptance by the date mentioned above. A formal joining letter will be issued on your joining.</p><p>Congratulations, and we look forward to welcoming you to our team.</p>';
}else{
t='<div class="sub">Subject: Joining letter – '+pos+'</div><p>Dear '+nm+',</p><p>With reference to your acceptance, we are pleased to confirm your appointment as <b>'+pos+'</b> at Idee Infotech on the following terms:</p>'+tbl([['Date of joining',fd($('jdate2').value)],['Monthly salary',v('sal2')],['Probation period',v('prob')+' month(s)'],['Reporting to',v('rep')],['Working hours',v('hours')]])+'<p>You are requested to report on the date of joining with your original documents for verification. You are expected to follow the policies and code of conduct of the company.</p><p>We wish you a successful career with us.</p>';
}
return t}
function render(){
var name=$('name').value.trim();
$('paper').innerHTML='<div class="hd"><div class="n">'+CO.n+'</div><div class="t">Digital Marketing Solutions</div></div><div class="bd"><div class="meta"><div>Ref: '+R+'</div><div>Date: '+fd($('date').value)+'</div></div><div><b>'+(v('name'))+'</b><br>'+v('addr').replace(/\n/g,'<br>')+'<br>Ph: '+v('phone')+' | '+v('mail')+'</div>'+body()+'<div class="sig">Yours sincerely,<br><br><br><b>'+v('sname')+'</b><br>'+v('sdes')+'<br>Idee Infotech</div></div><div class="ft"><div>'+esc($('caddr').value)+'</div><div>'+CO.mail+' | '+CO.ph+'</div></div>';
}
$('date').value=new Date().toISOString().slice(0,10);
document.querySelectorAll('.tab').forEach(function(b){b.onclick=function(){
document.querySelectorAll('.tab').forEach(function(x){x.classList.remove('on')});b.classList.add('on');
type=b.dataset.t;['call','conf','join'].forEach(function(k){$('f-'+k).style.display=k===type?'':'none'});
R=ref();render();$('pdf').disabled=false}});
$('go').onclick=async function(){R=ref();render();$('pdf').disabled=false;var ok=await saveRec();$('msg').textContent=ok?'Letter generated and details saved. Now download the PDF.':'Letter generated, but could not be saved to Records (sign in to claude.ai to enable saving).'};
$('pdf').onclick=async function(){
var fn=(['Call-Letter','Confirmation-Letter','Joining-Letter'][['call','conf','join'].indexOf(type)])+'-'+($('name').value.trim().replace(/\s+/g,'-')||'Candidate')+'.pdf';
$('msg').textContent='Preparing PDF…';
try{
var blob=await html2pdf().set({margin:0,image:{type:'jpeg',quality:.97},html2canvas:{scale:2,useCORS:true},jsPDF:{unit:'px',format:[794,1122],orientation:'portrait',hotfixes:['px_scaling']}}).from($('paper')).outputPdf('blob');
var dl=null;try{dl=await claude.use('downloads')}catch(e){}
if(dl){await dl.save({filename:fn,data:blob});$('msg').textContent='PDF ready.'}
else{$('msg').textContent='Download is not available here. Opening print dialog – choose "Save as PDF".';window.print()}
}catch(e){$('msg').textContent=(e&&e.code==='declined')?'Download cancelled.':'Could not create the PDF. Try again.'}};
var DB=null,ROWS=[];
if(window.claude&&claude.use){claude.use('db').then(function(d){DB=d;}).catch(function(){})}
function getRec(){
var j=type==='conf'?$('jdate').value:type==='join'?$('jdate2').value:'';
var s=type==='conf'?$('sal').value:type==='join'?$('sal2').value:'';
var ts=Date.now();
return{ts:ts,ref:R,type:{call:'Call Letter',conf:'Confirmation Letter',join:'Joining Letter'}[type],letterDate:$('date').value,name:$('name').value.trim(),phone:$('phone').value.trim(),email:$('mail').value.trim(),address:$('addr').value.trim(),position:getPos().trim(),interviewDate:type==='call'?$('idate').value:'',interviewTime:type==='call'?$('itime').value:'',mode:type==='call'?$('imode').value:'',platform:type==='call'&&isOn()?$('plat').value:'',meetingLink:type==='call'&&isOn()?$('link').value.trim():'',venue:type==='call'&&!isOn()?$('venue').value.trim():'',salary:s.trim(),joiningDate:j,replyBy:type==='conf'?$('rdate').value:'',probationMonths:type==='join'?$('prob').value:'',reportingTo:type==='join'?$('rep').value.trim():'',signatory:$('sname').value.trim()}}
async function saveRec(){if(!DB)return false;try{var r=getRec();await DB.collection('letters').doc('r'+r.ts).set(r);return true}catch(e){return false}}
$('pos').onchange=function(){$('pos2').style.display=$('pos').value==='Other'?'':'none'};
$('imode').onchange=function(){$('m-off').style.display=isOn()?'none':'';$('m-on').style.display=isOn()?'':'none'};
render();
</script>
</body>
</html>
