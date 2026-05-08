<!DOCTYPE html>
<html lang="so">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Imtixaanka Daraasaadka Soomaalida</title>
<style>
  * { box-sizing: border-box; margin: 0; padding: 0; }
  body { font-family: sans-serif; background: #f0f4f8; min-height: 100vh; display: flex; align-items: center; justify-content: center; padding: 16px; }
  .card { background: #fff; border-radius: 16px; padding: 24px; max-width: 480px; width: 100%; box-shadow: 0 4px 20px rgba(0,0,0,0.1); }
  h2 { color: #1a5276; text-align: center; margin-bottom: 8px; }
  .subtitle { text-align: center; color: #555; margin-bottom: 20px; font-size: 14px; }
  .btn { width: 100%; padding: 13px; border: none; border-radius: 10px; font-size: 15px; font-weight: bold; cursor: pointer; margin-top: 8px; }
  .btn-green { background: #27ae60; color: #fff; }
  .btn-blue { background: #1a5276; color: #fff; }
  .btn-orange { background: #f39c12; color: #fff; }
  .filter-btn { width: 100%; padding: 12px 16px; border-radius: 8px; font-size: 15px; cursor: pointer; text-align: left; margin-bottom: 8px; }
  .question-box { background: #eaf2ff; border-radius: 10px; padding: 16px; margin-bottom: 18px; font-size: 16px; font-weight: bold; color: #1a5276; }
  .opt { width: 100%; padding: 12px 14px; border-radius: 8px; font-size: 14px; cursor: pointer; text-align: left; margin-bottom: 8px; border: 2px solid #ddd; background: #f8f9fa; }
  .opt.selected { background: #d6eaf8; border-color: #1a5276; font-weight: bold; }
  .opt.correct { background: #d5f5e3; border-color: #27ae60; color: #1e8449; }
  .opt.wrong { background: #fadbd8; border-color: #e74c3c; color: #c0392b; }
  .feedback { margin-top: 12px; padding: 10px 14px; border-radius: 8px; font-weight: bold; font-size: 14px; }
  .fb-ok { background: #d5f5e3; color: #1e8449; }
  .fb-err { background: #fadbd8; color: #c0392b; }
  .topbar { display: flex; justify-content: space-between; margin-bottom: 12px; font-size: 13px; }
  .grade { font-size: 64px; font-weight: bold; margin: 16px 0; }
  .score-txt { font-size: 22px; margin-bottom: 8px; }
  .pct { font-size: 18px; font-weight: bold; margin-bottom: 20px; }
  .result-list { background: #f8f9fa; border-radius: 10px; padding: 16px; margin-bottom: 20px; text-align: left; max-height: 280px; overflow-y: auto; }
  .result-item { padding: 6px 0; border-bottom: 1px solid #eee; font-size: 13px; }
  .row { display: flex; gap: 10px; }
  .half { flex: 1; }
  #menu, #quiz, #result { display: none; }
</style>
</head>
<body>
<div class="card">

  <!-- MENU -->
  <div id="menu">
    <h2>📚 Imtixaanka Daraasaadka Soomaalida</h2>
    <p class="subtitle">Dooro cutubka aad rabto</p>
    <div id="filter-btns"></div>
    <button class="btn btn-green" onclick="startQuiz()">Bilow Imtixaanka ▶</button>
  </div>

  <!-- QUIZ -->
  <div id="quiz">
    <div class="topbar">
      <span id="cutub-label" style="color:#888"></span>
      <span id="progress" style="color:#1a5276;font-weight:bold"></span>
    </div>
    <div class="question-box" id="qtext"></div>
    <div id="options"></div>
    <div class="row" style="margin-top:18px">
      <button class="btn btn-orange half" id="btn-check" onclick="checkAnswer()" style="display:none">Hubi Jawaabta</button>
      <button class="btn btn-blue half" id="btn-next" onclick="nextQuestion()" style="display:none">Xigta ▶</button>
    </div>
    <div class="feedback" id="feedback" style="display:none"></div>
  </div>

  <!-- RESULT -->
  <div id="result" style="text-align:center">
    <h2>🎓 Natiijadaada</h2>
    <div class="grade" id="grade-letter"></div>
    <div class="score-txt" id="score-txt"></div>
    <div class="pct" id="pct-txt"></div>
    <div class="result-list" id="result-list"></div>
    <button class="btn btn-blue" onclick="goMenu()">🔄 Dib u Bilow</button>
  </div>

</div>

<script>
const allQ = [
  {q:"Meeqa qeybood oo waaweyn ayaa dhulka qowmiyadda Soomaalidu u qeybsan tahay?",opts:["3 qeybood","2 qeybood","5 qeybood","4 qeybood"],ans:1,cutub:"Cutubka 1aad"},
  {q:"Xagga dhirirka, dhulka Soomaalidu degto waxaa uu ku yaallaa inta u dhaxeysa xarriiqmaha ballaca ee kee?",opts:["3aad ilaa 12aad","1aad ilaa 10aad","5aad ilaa 15aad","2aad ilaa 10aad"],ans:0,cutub:"Cutubka 1aad"},
  {q:"Jasiiradda ugu weyn ee Soomaaliya waa ayo?",opts:["Cabdul Kori","Baajuunta","Soqodra","Sacdudiin"],ans:2,cutub:"Cutubka 1aad"},
  {q:"Bedka dhulka qowmiyadda Soomaalidu degto waxaa lagu qiyaasaa meeqa km²?",opts:["500,000 km²","637,657 km²","1,000,000 km²","800,000 km²"],ans:2,cutub:"Cutubka 1aad"},
  {q:"Dhulka qowmiyadda Soomaalidu waxaa uu xudduud la leeyahay immisa dal?",opts:["2 dal","4 dal","3 dal","5 dal"],ans:2,cutub:"Cutubka 1aad"},
  {q:"Marinka 'Baab Al-Mandab' wuxuu ku yaallaa cirifka waqooyi ee dalka xee?",opts:["Eritrea","Jabbuuti","Yemen","Kenya"],ans:1,cutub:"Cutubka 1aad"},
  {q:"Gubanku waa dhulka ku yaalla meesha?",opts:["Koofurta dalka","Dhuldeexeedka Waqooyi u dhexeeya Gacanka Cadmeed iyo buuralleyda goolis","Bartamaha dalka","Galbeedka dalka"],ans:1,cutub:"Cutubka 1aad"},
  {q:"Xudduudka Soomaaliya iyo Kenya waa meeqa km?",opts:["1600 km","58 km","682 km","500 km"],ans:2,cutub:"Cutubka 1aad"},
  {q:"Jinsiga 'Xaamiga' waxaa uu ku noolaan jiray hareeraha dhulka loo yaqaan?",opts:["Jasiiradda Carabta","Qawqaaz","Waqooyiga Afrika","Webiga Neylka"],ans:1,cutub:"Cutubka 2aad"},
  {q:"Afka Soomaaliga wuxuu kamid yahay qoysaska afafka la isku yiraahdo?",opts:["Saamiitiga","Baantuuga","Bahda Kushiitiga","Laatiinka"],ans:2,cutub:"Cutubka 2aad"},
  {q:"Sanadkii 1972kii, farta Soomaaliga la soo saaray waxay ka koobnayd meeqa xaraf oo shibbanayaal ah?",opts:["18 xaraf","22 xaraf","26 xaraf","30 xaraf"],ans:1,cutub:"Cutubka 2aad"},
  {q:"Qaamuuska u horreeyay ee 'Soomaali-English' waxaa soo saaray?",opts:["Deyvid Soolti","Rv. Delarajaas","Cismaan Yuusuf Keenidiid","Enderveski"],ans:1,cutub:"Cutubka 2aad"},
  {q:"Afguriyada afka Soomaaliga iskucelceliska isu ekaashahoodu waa meeqa?",opts:["30-40%","50-60%","60-80%","80-90%"],ans:2,cutub:"Cutubka 2aad"},
  {q:"Farta cusub ee Soomaaliga oo aan Carabi iyo Laatiin midna aheyn ee ugu horreysey waxaa soo saaray?",opts:["Sheekh Nuur","Cismaan Yuusuf Keenidiid","Xusen Sheekh Axmed Kaddare","Shire Jaamac"],ans:1,cutub:"Cutubka 2aad"},
  {q:"Afka Soomaaliga waxaa ku hadla qiyaas ahaan meeqa qof?",opts:["10 malyuun","20 malyuun","35 malyuun","50 malyuun"],ans:2,cutub:"Cutubka 2aad"},
  {q:"Qaybta 1aad ee afguriyada afka Soomaaliga waxaa la yiraahdaa?",opts:["Maay","Maxaatiri","Maadhati","Digil"],ans:1,cutub:"Cutubka 2aad"},
  {q:"Erayga 'Suugaan' Soomaalidu marka hore waxaa lagu aqoon jiray?",opts:["Gabayga","Xoogaa caleen ah oo degaan gaar ah ku yaalla","Heesta","Masafada"],ans:1,cutub:"Cutubka 3aad"},
  {q:"Astaamaha guud ee suugaanta Soomaalida waxaa kamid ah?",opts:["Jiibta, Jaanta, Orka","Xarafraaca, Miisaanka, Luuqda","Sacabka, Durbaan, Alalaaska","Gabayga, Masafada, Heesta"],ans:1,cutub:"Cutubka 3aad"},
  {q:"Hoyga suugaanta Soomaalida waa?",opts:["Magaalada","Miyiga","Xeebta","Buuraleyda"],ans:1,cutub:"Cutubka 3aad"},
  {q:"Masafada waxaa sida badan tiriya?",opts:["Dhallinyarada","Dumarku","Culumada diinta","Odayaasha"],ans:2,cutub:"Cutubka 3aad"},
  {q:"Farqiga u dhexeeya hidde iyo dhaxaldhaqameed, hidduhu?",opts:["Nolosha laga kasbadaa","Waa wax lugu dhasho (abuuris Eebbe)","Meel kasta laga kasbi karaa","Waa baaba'aa muddo ka dib"],ans:1,cutub:"Cutubka 3aad"},
  {q:"Akademiyada cilmiga, fanka iyo suugaanta Soomaalida waxay diiwaangelisay ilaa meeqa laamood?",opts:["100 laamood","200 laamood","300 laamood","500 laamood"],ans:2,cutub:"Cutubka 3aad"},
  {q:"Unugga ugu hooseeya ee bulshada Soomaalida waa?",opts:["Jilib","Reer","Qoys","Beel"],ans:2,cutub:"Cutubka 4aad"},
  {q:"Qaabdhismeedka isbaheysiga waa qaab ku dhisan?",opts:["Abtirsiinta kaliya","Dhib iyo dheef wadaag","Xeer qabiil","Xiriir degaan"],ans:1,cutub:"Cutubka 4aad"},
  {q:"Soomaalidu 'Seddex baa qabiil lagu yahay', maxaa kamid ah?",opts:["Nin qumman quweyntiisa","Nin hodanka ah","Nin caalimka ah","Nin geesiga ah"],ans:0,cutub:"Cutubka 4aad"},
  {q:"Magacyada madaxdhaqameedka bulshada Soomaalida waxaa kamid ah?",opts:["Wasiir, Madaxweyne","Ugaas, Boqor, Suldaan","Xildhibaan, Gudoomiye","Amiir, Khaliif"],ans:1,cutub:"Cutubka 4aad"},
];

const cutubs = ["Dhammaan","Cutubka 1aad","Cutubka 2aad","Cutubka 3aad","Cutubka 4aad"];
let selFilter = "Dhammaan", questions = [], cur = 0, selOpt = null, answers = [], checked = false;

function goMenu() {
  document.getElementById('menu').style.display='block';
  document.getElementById('quiz').style.display='none';
  document.getElementById('result').style.display='none';
  renderFilters();
}

function renderFilters() {
  const c = document.getElementById('filter-btns');
  c.innerHTML = '';
  cutubs.forEach(f => {
    const b = document.createElement('button');
    b.className = 'filter-btn';
    b.textContent = f;
    b.style.border = f===selFilter ? '2px solid #1a5276' : '2px solid #ddd';
    b.style.background = f===selFilter ? '#1a5276' : '#f8f9fa';
    b.style.color = f===selFilter ? '#fff' : '#333';
    b.style.fontWeight = f===selFilter ? 'bold' : 'normal';
    b.onclick = () => { selFilter = f; renderFilters(); };
    c.appendChild(b);
  });
}

function shuffle(a) { return [...a].sort(()=>Math.random()-0.5); }

function startQuiz() {
  let pool = selFilter==='Dhammaan' ? allQ : allQ.filter(q=>q.cutub===selFilter);
  questions = shuffle(pool);
  cur = 0; selOpt = null; answers = []; checked = false;
  document.getElementById('menu').style.display='none';
  document.getElementById('quiz').style.display='block';
  document.getElementById('result').style.display='none';
  renderQ();
}

function renderQ() {
  const q = questions[cur];
  document.getElementById('cutub-label').textContent = q.cutub;
  document.getElementById('progress').textContent = (cur+1)+' / '+questions.length;
  document.getElementById('qtext').textContent = q.q;
  const od = document.getElementById('options');
  od.innerHTML = '';
  q.opts.forEach((o,i) => {
    const b = document.createElement('button');
    b.className = 'opt';
    b.textContent = String.fromCharCode(65+i)+'. '+o;
    b.onclick = () => selectOpt(i);
    b.id = 'opt-'+i;
    od.appendChild(b);
  });
  selOpt = null; checked = false;
  document.getElementById('feedback').style.display='none';
  document.getElementById('btn-check').style.display='none';
  document.getElementById('btn-next').style.display='none';
}

function selectOpt(i) {
  if (checked) return;
  selOpt = i;
  document.querySelectorAll('.opt').forEach((b,j) => {
    b.classList.toggle('selected', j===i);
  });
  document.getElementById('btn-check').style.display='block';
}

function checkAnswer() {
  if (selOpt===null || checked) return;
  checked = true;
  const q = questions[cur];
  document.querySelectorAll('.opt').forEach((b,i) => {
    if (i===q.ans) b.classList.add('correct');
    else if (i===selOpt) b.classList.add('wrong');
    b.classList.remove('selected');
  });
  const fb = document.getElementById('feedback');
  fb.style.display='block';
  if (selOpt===q.ans) { fb.className='feedback fb-ok'; fb.textContent='✅ Saxsaxay!'; }
  else { fb.className='feedback fb-err'; fb.textContent='❌ Jawaabta saxda ah waa: '+q.opts[q.ans]; }
  document.getElementById('btn-check').style.display='none';
  document.getElementById('btn-next').style.display='block';
  document.getElementById('btn-next').textContent = cur+1<questions.length ? 'Xigta ▶' : 'Natiijada Fiiri ✓';
}

function nextQuestion() {
  answers.push({q:questions[cur], chosen:selOpt});
  if (cur+1<questions.length) { cur++; renderQ(); }
  else showResult();
}

function showResult() {
  document.getElementById('quiz').style.display='none';
  document.getElementById('result').style.display='block';
  const score = answers.filter(a=>a.chosen===a.q.ans).length;
  const pct = Math.round(score/answers.length*100);
  const grade = pct>=80?'A':pct>=70?'B':pct>=60?'C':pct>=50?'D':'F';
  const gc = pct>=80?'#27ae60':pct>=60?'#f39c12':'#e74c3c';
  const gl = document.getElementById('grade-letter');
  gl.textContent = grade; gl.style.color = gc;
  document.getElementById('score-txt').textContent = score+' / '+answers.length+' Su\'aal';
  const pt = document.getElementById('pct-txt');
  pt.textContent = pct+'%'; pt.style.color = gc;
  const rl = document.getElementById('result-list');
  rl.innerHTML = answers.map(a=>`<div class="result-item" style="color:${a.chosen===a.q.ans?'#27ae60':'#e74c3c'}">${a.chosen===a.q.ans?'✅':'❌'} ${a.q.q.substring(0,55)}...</div>`).join('');
}

goMenu();
</script>
</body>
</html>
