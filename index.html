<!DOCTYPE html>
<html lang="it">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
<title>Pauper Metagame Dashboard</title>
<style>
  *{margin:0;padding:0;box-sizing:border-box}
  body{font-family:-apple-system,BlinkMacSystemFont,'Segoe UI','Inter',sans-serif;background:#0a0e27;color:#e0e6ff;padding:12px;-webkit-text-size-adjust:100%}

  /* === HEADER === */
  .header{text-align:center;margin-bottom:20px}
  .header h1{font-size:1.6rem;font-weight:800;color:#ffd700;letter-spacing:2px}
  .header p{color:#8892b0;font-size:.8rem;margin-top:2px}

  /* === STAT CARDS === */
  .stats{display:grid;grid-template-columns:repeat(3,1fr);gap:8px;margin-bottom:16px}
  .st{background:#131836;border-radius:10px;padding:12px 8px;text-align:center;border:2px solid transparent}
  .st .v{font-size:1.4rem;font-weight:800}
  .st .l{font-size:.6rem;color:#8892b0;font-weight:600;letter-spacing:.5px;margin-top:2px;text-transform:uppercase}
  .st:nth-child(1){border-color:#ffd700}.st:nth-child(1) .v{color:#ffd700}
  .st:nth-child(2){border-color:#ff6b35}.st:nth-child(2) .v{color:#ff6b35}
  .st:nth-child(3){border-color:#00d4aa}.st:nth-child(3) .v{color:#00d4aa}
  .st:nth-child(4){border-color:#667eea}.st:nth-child(4) .v{color:#667eea}
  .st:nth-child(5){border-color:#ff4757;grid-column:span 2}.st:nth-child(5) .v{color:#ff4757;font-size:1rem}

  /* === CARDS === */
  .card{background:#131836;border-radius:12px;padding:16px;border:1px solid #1e2652;margin-bottom:16px}
  .card h2{font-size:.8rem;font-weight:700;margin-bottom:12px;letter-spacing:.5px;text-transform:uppercase;color:#e0e6ff}

  /* === LEGEND === */
  .legend{display:flex;gap:12px;margin-bottom:10px;font-size:.72rem;font-weight:600;flex-wrap:wrap}
  .legend span{display:flex;align-items:center;gap:4px}
  .dot{width:10px;height:10px;border-radius:2px;display:inline-block;flex-shrink:0}

  /* === HORIZONTAL BARS === */
  .hbar-row{display:flex;align-items:center;margin-bottom:5px;gap:6px}
  .hbar-label{width:105px;text-align:right;font-size:.7rem;font-weight:700;white-space:nowrap;overflow:hidden;text-overflow:ellipsis;flex-shrink:0}
  .hbar-track{flex:1;height:22px;background:#0d1230;border-radius:3px;display:flex;overflow:hidden}
  .hbar-ch{height:100%;background:#ff6b35;display:flex;align-items:center;justify-content:center;font-size:.6rem;font-weight:700;color:#fff}
  .hbar-lg{height:100%;background:#00d4aa;display:flex;align-items:center;justify-content:center;font-size:.6rem;font-weight:700;color:#fff}
  .hbar-total{width:30px;text-align:center;font-weight:800;color:#ffd700;font-size:.8rem;flex-shrink:0}
  .hbar-pct{width:36px;text-align:right;color:#8892b0;font-size:.68rem;flex-shrink:0}

  /* === DONUT === */
  .donut-wrap{display:flex;flex-direction:column;align-items:center;gap:14px}
  .donut-legend{display:grid;grid-template-columns:1fr 1fr;gap:4px 12px;width:100%}
  .dl-item{display:flex;align-items:center;gap:5px;font-size:.72rem;font-weight:600}
  .dl-item .sw{width:10px;height:10px;border-radius:2px;flex-shrink:0}
  .dl-item .pct{color:#8892b0;font-size:.65rem;margin-left:auto}

  /* === VERTICAL BARS === */
  .vbar-wrap{display:flex;align-items:flex-end;gap:4px;height:180px;padding-top:8px;overflow-x:auto}
  .vbar-group{flex:1;min-width:34px;display:flex;flex-direction:column;align-items:center;gap:1px;height:100%;justify-content:flex-end}
  .vbar-bars{display:flex;gap:2px;align-items:flex-end;width:100%;justify-content:center}
  .vbar-bar{border-radius:2px 2px 0 0;min-width:12px}
  .vbar-val{font-size:.55rem;font-weight:700;text-align:center;margin-bottom:1px}
  .vbar-lbl{font-size:.5rem;color:#8892b0;text-align:center;margin-top:4px;line-height:1.1;word-break:break-word;max-width:40px}

  /* === TABLE === */
  .search-box{width:100%;padding:8px 10px;border-radius:8px;border:1px solid #1e2652;background:#0d1230;color:#e0e6ff;font-size:.82rem;margin-bottom:8px;outline:none;font-family:inherit}
  .search-box::placeholder{color:#4a5568}
  .search-box:focus{border-color:#667eea}
  .table-scroll{max-height:420px;overflow-y:auto;overflow-x:auto;border-radius:6px;-webkit-overflow-scrolling:touch}
  table{width:100%;border-collapse:collapse;font-size:.75rem;min-width:380px}
  thead th{text-align:left;padding:6px 6px;color:#ffd700;font-weight:700;font-size:.65rem;letter-spacing:.5px;text-transform:uppercase;border-bottom:2px solid #1e2652;cursor:pointer;user-select:none;white-space:nowrap;position:sticky;top:0;background:#131836;z-index:2}
  thead th .arrow{font-size:.55rem;margin-left:2px;opacity:.4}
  thead th.active .arrow{opacity:1}
  tbody tr{border-bottom:1px solid #0d1230}
  tbody tr:nth-child(even){background:#0d1230}
  td{padding:6px 6px}
  .c-name{font-weight:600;white-space:nowrap}
  .c-ch{color:#ff6b35;font-weight:700;text-align:center}
  .c-lg{color:#00d4aa;font-weight:700;text-align:center}
  .c-tot{color:#ffd700;font-weight:800;text-align:center}
  .c-pct{color:#8892b0;text-align:center}
  .mini-bar{height:5px;border-radius:3px;background:#1e2652;margin-top:2px;overflow:hidden;min-width:50px}
  .mini-fill{height:100%;border-radius:3px}

  .footer{text-align:center;padding:16px 0;color:#4a5568;font-size:.7rem}

  /* === DESKTOP OVERRIDES === */
  @media(min-width:768px){
    body{padding:24px;max-width:1100px;margin:0 auto}
    .header h1{font-size:2.4rem}
    .header p{font-size:.95rem}
    .stats{grid-template-columns:repeat(5,1fr)}
    .st .v{font-size:1.8rem}
    .st .l{font-size:.72rem}
    .st:nth-child(5){grid-column:span 1}
    .two-col{display:grid;grid-template-columns:1fr 1fr;gap:16px}
    .two-col .card{margin-bottom:0}
    .hbar-label{width:140px;font-size:.8rem}
    .hbar-track{height:26px}
    .hbar-ch,.hbar-lg{font-size:.7rem}
    .hbar-total{font-size:.9rem;width:36px}
    .hbar-pct{font-size:.78rem;width:42px}
    .vbar-wrap{height:240px}
    .vbar-bar{min-width:18px}
    .vbar-val{font-size:.65rem}
    .vbar-lbl{font-size:.6rem}
    .donut-wrap{flex-direction:row;gap:24px}
    .donut-legend{width:auto}
    table{font-size:.82rem}
    thead th{font-size:.72rem;padding:8px}
    td{padding:7px 8px}
  }
</style>
</head>
<body>

<div class="header">
  <h1>PAUPER METAGAME</h1>
  <p>367 entries · Challenge (160) + League (207)</p>
</div>

<div class="stats">
  <div class="st"><div class="v">367</div><div class="l">Total</div></div>
  <div class="st"><div class="v">160</div><div class="l">Challenge</div></div>
  <div class="st"><div class="v">207</div><div class="l">League</div></div>
  <div class="st"><div class="v">43</div><div class="l">Decks</div></div>
  <div class="st"><div class="v">White Aggro</div><div class="l">Top Deck</div></div>
</div>

<!-- TOP 15 -->
<div class="card">
  <h2>Top 15 Decks</h2>
  <div class="legend">
    <span><span class="dot" style="background:#ff6b35"></span>Challenge</span>
    <span><span class="dot" style="background:#00d4aa"></span>League</span>
    <span style="color:#ffd700;font-weight:800">Tot</span>
    <span style="color:#8892b0">%</span>
  </div>
  <div id="hbar"></div>
</div>

<div class="two-col">
  <!-- DONUT -->
  <div class="card">
    <h2>Meta Share — Top 8</h2>
    <div class="donut-wrap">
      <svg id="donut" width="180" height="180" viewBox="0 0 180 180"></svg>
      <div id="dleg" class="donut-legend"></div>
    </div>
  </div>

  <!-- VERTICAL BARS -->
  <div class="card">
    <h2>Challenge vs League — Top 10</h2>
    <div class="legend">
      <span><span class="dot" style="background:#ff6b35"></span>Challenge</span>
      <span><span class="dot" style="background:#00d4aa"></span>League</span>
    </div>
    <div id="vbar" class="vbar-wrap"></div>
  </div>
</div>

<!-- TABLE -->
<div class="card">
  <h2>Tutti i Deck (43)</h2>
  <input type="text" class="search-box" id="si" placeholder="Cerca un deck..." oninput="filterT()">
  <div class="table-scroll">
    <table>
      <thead><tr>
        <th onclick="srt(0)">#<span class="arrow">▼</span></th>
        <th onclick="srt(1)">Deck<span class="arrow">▼</span></th>
        <th onclick="srt(2)">Ch<span class="arrow">▼</span></th>
        <th onclick="srt(3)">Lg<span class="arrow">▼</span></th>
        <th onclick="srt(4)">Tot<span class="arrow">▼</span></th>
        <th onclick="srt(5)">%<span class="arrow">▼</span></th>
        <th style="cursor:default">Dist.</th>
      </tr></thead>
      <tbody id="tb"></tbody>
    </table>
  </div>
</div>

<div class="footer">Data: MTGO Pauper · Zero dipendenze esterne</div>

<script>
const D=[["White Aggro",11,27,38],["Elves",11,20,31],["Mono Red Madness",14,14,28],["Blue Terror",12,12,24],["Jund Wildfire",12,9,21],["Caw-Gates",7,10,17],["Grixis Affinity",1,14,15],["Mono Red Rally",8,6,14],["Gruul Ramp",7,7,14],["Tron",5,7,12],["Madness Burn",7,5,12],["Golgari Gardens",4,7,11],["Dimir Faeries",5,5,10],["Spy Combo",5,4,9],["Food Gardens",0,9,9],["Mono-Blue Faeries",4,3,7],["Dredge",4,3,7],["Gruul Ponza",2,4,6],["Familiars",2,4,6],["Dimir Terror",3,3,6],["Bogles",0,6,6],["Black Sacrifice",2,4,6],["Glintblade",1,4,5],["Dimir Control",0,5,5],["Turbo Fog",3,1,4],["Ruby Storm",0,3,3],["Jund Gardens",1,2,3],["Izzet Faeries",0,3,3],["Walls Combo",0,2,2],["Poison Storm",1,1,2],["Naya Ephemerate",1,1,2],["Izzet Terror",0,2,2],["Inside Out Combo",0,2,2],["Boros Moxite",0,2,2],["Boros Bully",0,2,2],["Walls Cascade",0,1,1],["Mardu Ephemerate",0,1,1],["Kiln Fiend",0,1,1],["Jeskai Synthesizer",0,1,1],["Jeskai Affinity",0,1,1],["Ephemerate Tron",0,1,1],["Cycle Storm",0,1,1],["Burn",0,1,1]];
const T=367,MX=38;

// HORIZONTAL BARS
!function(){
  const c=document.getElementById('hbar');
  D.slice(0,15).forEach(d=>{
    const cw=(d[1]/MX*100).toFixed(1),lw=(d[2]/MX*100).toFixed(1),pct=(d[3]/T*100).toFixed(1);
    const r=document.createElement('div');r.className='hbar-row';
    r.innerHTML=`<div class="hbar-label">${d[0]}</div><div class="hbar-track"><div class="hbar-ch" style="width:${cw}%">${d[1]>2?d[1]:''}</div><div class="hbar-lg" style="width:${lw}%">${d[2]>2?d[2]:''}</div></div><div class="hbar-total">${d[3]}</div><div class="hbar-pct">${pct}%</div>`;
    c.appendChild(r);
  });
}();

// DONUT
!function(){
  const svg=document.getElementById('donut'),leg=document.getElementById('dleg');
  const t8=D.slice(0,8),ov=T-t8.reduce((s,d)=>s+d[3],0);
  const vals=[...t8.map(d=>d[3]),ov],labels=[...t8.map(d=>d[0]),'Others (35)'];
  const cols=['#ff6b35','#00d4aa','#667eea','#ff4757','#ffa502','#a29bfe','#fd79a8','#00cec9','#636e72'];
  const cx=90,cy=90,R=80,r=48;
  let cum=0;
  vals.forEach((v,i)=>{
    const f=v/T,sA=cum*2*Math.PI-Math.PI/2;cum+=f;const eA=cum*2*Math.PI-Math.PI/2,lg=f>.5?1:0;
    const x1=cx+R*Math.cos(sA),y1=cy+R*Math.sin(sA),x2=cx+R*Math.cos(eA),y2=cy+R*Math.sin(eA);
    const x3=cx+r*Math.cos(eA),y3=cy+r*Math.sin(eA),x4=cx+r*Math.cos(sA),y4=cy+r*Math.sin(sA);
    const p=document.createElementNS('http://www.w3.org/2000/svg','path');
    p.setAttribute('d',`M${x1},${y1}A${R},${R} 0 ${lg} 1 ${x2},${y2}L${x3},${y3}A${r},${r} 0 ${lg} 0 ${x4},${y4}Z`);
    p.setAttribute('fill',cols[i]);p.setAttribute('stroke','#0a0e27');p.setAttribute('stroke-width','2');
    const tt=document.createElementNS('http://www.w3.org/2000/svg','title');
    tt.textContent=`${labels[i]}: ${v} (${(v/T*100).toFixed(1)}%)`;p.appendChild(tt);svg.appendChild(p);
    const it=document.createElement('div');it.className='dl-item';
    it.innerHTML=`<span class="sw" style="background:${cols[i]}"></span>${labels[i]}<span class="pct">${(v/T*100).toFixed(1)}%</span>`;
    leg.appendChild(it);
  });
  const ct=document.createElementNS('http://www.w3.org/2000/svg','text');
  ct.setAttribute('x',cx);ct.setAttribute('y',cy-4);ct.setAttribute('text-anchor','middle');
  ct.setAttribute('fill','#ffd700');ct.setAttribute('font-size','20');ct.setAttribute('font-weight','800');
  ct.textContent='367';svg.appendChild(ct);
  const ct2=document.createElementNS('http://www.w3.org/2000/svg','text');
  ct2.setAttribute('x',cx);ct2.setAttribute('y',cy+12);ct2.setAttribute('text-anchor','middle');
  ct2.setAttribute('fill','#8892b0');ct2.setAttribute('font-size','9');ct2.setAttribute('font-weight','600');
  ct2.textContent='ENTRIES';svg.appendChild(ct2);
}();

// VERTICAL BARS
!function(){
  const c=document.getElementById('vbar'),t10=D.slice(0,10);
  const mx=Math.max(...t10.map(d=>Math.max(d[1],d[2])));
  t10.forEach(d=>{
    const chH=(d[1]/mx*140),lgH=(d[2]/mx*140);
    // Short names for mobile
    let sn=d[0].replace('Mono Red ','M.R.').replace('Grixis ','Gx.').replace('Golgari ','Gol.');
    if(sn.length>10)sn=sn.substring(0,9)+'…';
    const g=document.createElement('div');g.className='vbar-group';
    g.innerHTML=`<div class="vbar-bars"><div><div class="vbar-val" style="color:#ff6b35">${d[1]||''}</div><div class="vbar-bar" style="height:${chH}px;background:#ff6b35;width:14px" title="Ch: ${d[1]}"></div></div><div><div class="vbar-val" style="color:#00d4aa">${d[2]}</div><div class="vbar-bar" style="height:${lgH}px;background:#00d4aa;width:14px" title="Lg: ${d[2]}"></div></div></div><div class="vbar-lbl">${sn}</div>`;
    c.appendChild(g);
  });
}();

// TABLE
let sc=4,sa=false;
function renderT(data){
  const tb=document.getElementById('tb');tb.innerHTML='';
  data.forEach((d,i)=>{
    const pct=(d[3]/T*100).toFixed(1),bw=(d[3]/MX*100).toFixed(1),cp=d[3]>0?(d[1]/d[3]*100).toFixed(1):0;
    const tr=document.createElement('tr');
    tr.innerHTML=`<td style="color:#4a5568;text-align:center;font-size:.7rem">${i+1}</td><td class="c-name">${d[0]}</td><td class="c-ch">${d[1]||'–'}</td><td class="c-lg">${d[2]}</td><td class="c-tot">${d[3]}</td><td class="c-pct">${pct}%</td><td><div class="mini-bar"><div class="mini-fill" style="width:${bw}%;background:linear-gradient(90deg,#ff6b35 ${cp}%,#00d4aa ${cp}%)"></div></div></td>`;
    tb.appendChild(tr);
  });
}
function srt(col){
  if(sc===col)sa=!sa;else{sc=col;sa=col===1}
  const s=[...D].sort((a,b)=>{let va,vb;if(col===0){va=D.indexOf(a);vb=D.indexOf(b)}else if(col===1){va=a[0];vb=b[0]}else if(col===2){va=a[1];vb=b[1]}else if(col===3){va=a[2];vb=b[2]}else{va=a[3];vb=b[3]}if(typeof va==='string')return sa?va.localeCompare(vb):vb.localeCompare(va);return sa?va-vb:vb-va});
  document.querySelectorAll('thead th').forEach((th,i)=>{th.classList.toggle('active',i===col);const a=th.querySelector('.arrow');if(a)a.textContent=(i===col&&sa)?'▲':'▼'});
  renderT(s);
}
function filterT(){renderT(D.filter(d=>d[0].toLowerCase().includes(document.getElementById('si').value.toLowerCase())))}
renderT(D);
</script>
</body>
</html>
