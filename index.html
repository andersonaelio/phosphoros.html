<!-- Assessoria — painel de gestão de influenciadores (protótipo SaaS) -->
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Assessoria · Painel</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,400;9..144,500;9..144,600;9..144,700&family=Hanken+Grotesk:wght@400;500;600;700&display=swap" rel="stylesheet">
<script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2"></script>
<style>
  :root{
    --bg:#F6F1E9; --paper:#FFFDF9; --ink:#211C17; --ink-soft:#5C5247;
    --line:#E4DBCD; --line-2:#EFE8DC;
    --coral:#D85A3A; --coral-deep:#B8431F; --coral-soft:#F6E2D8;
    --sage:#5B6B4F; --sage-soft:#E5EADD;
    --gold:#C29A3B; --plum:#7A4A63;
    --shadow:0 1px 2px rgba(33,28,23,.04), 0 8px 28px -16px rgba(33,28,23,.22);
  }
  *{box-sizing:border-box}
  html,body{margin:0}
  body{
    background:
      radial-gradient(120% 80% at 100% 0%, #FBEFE6 0%, transparent 55%),
      radial-gradient(90% 70% at 0% 100%, #EEF0E6 0%, transparent 50%),
      var(--bg);
    color:var(--ink); font-family:"Hanken Grotesk",sans-serif;
    font-size:15px; line-height:1.5; -webkit-font-smoothing:antialiased;
    min-height:100vh;
  }
  .wrap{max-width:1180px; margin:0 auto; padding:22px 22px 80px}
  /* ---------- top bar ---------- */
  header.top{display:flex; align-items:center; justify-content:space-between; gap:16px; flex-wrap:wrap; margin-bottom:6px}
  .brand{display:flex; align-items:baseline; gap:12px}
  .brand h1{font-family:"Fraunces",serif; font-weight:600; font-size:30px; letter-spacing:-.01em; margin:0}
  .brand .dot{color:var(--coral)}
  .brand small{color:var(--ink-soft); font-size:12.5px; letter-spacing:.16em; text-transform:uppercase}
  .save-pill{font-size:11.5px; color:var(--sage); background:var(--sage-soft); padding:5px 11px; border-radius:999px; font-weight:600; letter-spacing:.02em}
  .save-pill.warn{color:#8a5a00; background:#f6ecd2}
  /* ---------- nav ---------- */
  nav.tabs{display:flex; gap:4px; margin:18px 0 22px; border-bottom:1.5px solid var(--line); flex-wrap:wrap}
  nav.tabs button{
    appearance:none; border:0; background:none; font:inherit; cursor:pointer;
    padding:11px 16px; color:var(--ink-soft); font-weight:600; border-radius:10px 10px 0 0;
    position:relative; transition:color .15s; font-size:14.5px;
  }
  nav.tabs button:hover{color:var(--ink)}
  nav.tabs button.active{color:var(--coral-deep)}
  nav.tabs button.active::after{content:""; position:absolute; left:14px; right:14px; bottom:-1.5px; height:2.5px; background:var(--coral); border-radius:3px}
  /* ---------- generic ---------- */
  .card{background:var(--paper); border:1px solid var(--line); border-radius:16px; box-shadow:var(--shadow)}
  .muted{color:var(--ink-soft)}
  h2.sec{font-family:"Fraunces",serif; font-weight:600; font-size:21px; margin:0 0 2px}
  button.btn{appearance:none; cursor:pointer; font:inherit; font-weight:600; border-radius:10px; padding:9px 15px; border:1px solid var(--coral); background:var(--coral); color:#fff; transition:.15s; font-size:13.5px}
  button.btn:hover{background:var(--coral-deep); border-color:var(--coral-deep)}
  button.ghost{background:none; color:var(--ink); border:1px solid var(--line)}
  button.ghost:hover{background:#fff; border-color:var(--ink-soft)}
  input,select,textarea{font:inherit; color:var(--ink); background:var(--paper); border:1px solid var(--line); border-radius:9px; padding:8px 10px; width:100%}
  input:focus,select:focus,textarea:focus{outline:none; border-color:var(--coral); box-shadow:0 0 0 3px var(--coral-soft)}
  label.fld{display:block; font-size:12px; font-weight:600; color:var(--ink-soft); margin:0 0 4px; letter-spacing:.02em}
  .grid-form{display:grid; grid-template-columns:1fr 1fr; gap:13px}
  /* ---------- dashboard ---------- */
  .stat-row{display:grid; grid-template-columns:repeat(4,1fr); gap:14px}
  .stat{padding:16px 18px}
  .stat .k{font-family:"Fraunces",serif; font-size:30px; font-weight:600; line-height:1}
  .stat .l{font-size:12px; color:var(--ink-soft); margin-top:6px; letter-spacing:.04em; text-transform:uppercase}
  .stat .sub{font-size:12px; color:var(--coral-deep); margin-top:3px; font-weight:600}
  .two{display:grid; grid-template-columns:1.3fr 1fr; gap:14px; margin-top:14px}
  .bar-item{display:flex; align-items:center; gap:10px; margin:9px 0}
  .bar-item .name{width:120px; font-size:13px; font-weight:600; flex-shrink:0; text-transform:capitalize}
  .bar-track{flex:1; height:9px; background:var(--line-2); border-radius:99px; overflow:hidden}
  .bar-fill{height:100%; border-radius:99px}
  .bar-item .val{width:54px; text-align:right; font-size:12.5px; color:var(--ink-soft); font-variant-numeric:tabular-nums}
  .pad{padding:18px 20px}
  /* ---------- tier badges ---------- */
  .tier{display:inline-flex; align-items:center; gap:5px; font-size:11px; font-weight:700; padding:3px 9px; border-radius:99px; letter-spacing:.03em; white-space:nowrap}
  .tier::before{content:""; width:6px; height:6px; border-radius:99px; background:currentColor}
  .t-nano{color:#6b6256; background:#EEE8DC}
  .t-micro{color:var(--sage); background:var(--sage-soft)}
  .t-macro{color:var(--coral-deep); background:var(--coral-soft)}
  .t-mega{color:var(--plum); background:#F1E3EB}
  /* ---------- table ---------- */
  .toolbar{display:flex; gap:10px; flex-wrap:wrap; align-items:center; margin-bottom:14px}
  .toolbar .search{flex:1; min-width:180px; position:relative}
  .toolbar .search input{padding-left:32px}
  .toolbar .search svg{position:absolute; left:10px; top:9px; opacity:.45}
  .toolbar select{width:auto; min-width:130px}
  table{width:100%; border-collapse:collapse; font-size:13.5px}
  thead th{text-align:left; font-size:11px; letter-spacing:.06em; text-transform:uppercase; color:var(--ink-soft); font-weight:700; padding:10px 12px; border-bottom:1.5px solid var(--line); cursor:pointer; user-select:none; white-space:nowrap}
  thead th .arr{opacity:.4; font-size:10px}
  tbody td{padding:11px 12px; border-bottom:1px solid var(--line-2); vertical-align:middle}
  tbody tr:hover{background:#FCF7EF}
  .handle{font-weight:700}
  .handle a{color:var(--coral-deep); text-decoration:none}
  .handle a:hover{text-decoration:underline}
  .num{font-variant-numeric:tabular-nums; font-weight:600}
  .niche-chip{display:inline-block; font-size:11.5px; background:var(--line-2); color:var(--ink-soft); padding:2px 8px; border-radius:7px; margin:1px 2px 1px 0}
  .rowbtns{display:flex; gap:6px; opacity:0; transition:.15s}
  tr:hover .rowbtns{opacity:1}
  .iconbtn{appearance:none; border:1px solid var(--line); background:#fff; border-radius:8px; width:28px; height:28px; cursor:pointer; display:grid; place-items:center; padding:0}
  .iconbtn:hover{border-color:var(--coral); color:var(--coral-deep)}
  .empty{padding:40px; text-align:center; color:var(--ink-soft)}
  .bchip{display:inline-flex; align-items:center; gap:5px; font-size:11.5px; font-weight:700; padding:3px 9px; border-radius:99px; white-space:nowrap}
  .bchip::before{content:""; width:6px; height:6px; border-radius:99px; background:currentColor}
  .contact-btn{appearance:none; cursor:pointer; font:inherit; font-size:12.5px; font-weight:600; border:1px solid var(--sage); color:var(--sage); background:var(--sage-soft); border-radius:8px; padding:6px 11px; white-space:nowrap; display:inline-flex; align-items:center; gap:5px}
  .contact-btn:hover{background:var(--sage); color:#fff}
  .pop{position:fixed; z-index:60; background:var(--paper); border:1px solid var(--line); border-radius:13px; box-shadow:0 22px 55px -18px rgba(33,28,23,.45); padding:6px; min-width:182px; animation:popin .12s ease}
  @keyframes popin{from{opacity:0; transform:translateY(-4px)}to{opacity:1; transform:none}}
  .pop a,.pop button{display:flex; align-items:center; gap:9px; width:100%; text-align:left; padding:9px 11px; border-radius:9px; font:inherit; font-size:13.5px; color:var(--ink); text-decoration:none; background:none; border:0; cursor:pointer}
  .pop a:hover,.pop button:hover{background:var(--coral-soft); color:var(--coral-deep)}
  .pop .hd{font-size:11px; text-transform:uppercase; letter-spacing:.06em; color:var(--ink-soft); padding:7px 11px 5px; font-weight:700; pointer-events:none}
  .pop .pop-hint{font-size:11px; color:var(--ink-soft); padding:7px 11px; line-height:1.35}
  .due{font-size:12.5px; font-weight:600; font-variant-numeric:tabular-nums; white-space:nowrap}
  .due-ok{color:var(--ink)}
  .due-soon{color:var(--gold)}
  .due-late{color:var(--coral-deep); font-weight:700}
  .agenda-row{display:flex; align-items:center; gap:11px; padding:9px 0; border-bottom:1px solid var(--line-2); font-size:13.5px}
  .agenda-row:last-child{border-bottom:0}
  .agenda-tag{font-size:10.5px; font-weight:700; letter-spacing:.04em; text-transform:uppercase; padding:3px 8px; border-radius:7px; flex-shrink:0}
  .tg-e{color:#3A6B8C; background:#e1ebf2}
  .tg-p{color:var(--coral-deep); background:var(--coral-soft)}
  .chk-grid{display:grid; grid-template-columns:1fr 1fr; gap:4px 12px; max-height:170px; overflow:auto; border:1px solid var(--line); border-radius:10px; padding:10px 12px}
  .chk{display:flex; align-items:center; gap:7px; font-size:13px; font-weight:500}
  .chk input{width:auto}
  .inf-grid{display:grid; grid-template-columns:repeat(auto-fill,minmax(300px,1fr)); gap:16px}
  .inf-card{background:var(--paper); border:1px solid var(--line); border-radius:16px; box-shadow:var(--shadow); padding:20px; display:flex; flex-direction:column; gap:14px; transition:transform .18s, box-shadow .18s, border-color .18s}
  .inf-card:hover{border-color:var(--coral); transform:translateY(-2px); box-shadow:0 12px 32px -16px rgba(33,28,23,.32)}
  .av-lg{width:46px; height:46px; font-size:19px}
  .inf-top{display:flex; align-items:center; gap:12px}
  .inf-handle{font-weight:700; color:var(--coral-deep); text-decoration:none; font-size:15.5px; display:block; overflow:hidden; text-overflow:ellipsis; white-space:nowrap}
  .inf-handle:hover{text-decoration:underline}
  .inf-meta{font-size:12.5px; color:var(--ink-soft); margin-top:2px}
  .inf-rowbtns{display:flex; gap:6px; flex-shrink:0}
  .inf-stat{display:flex; align-items:baseline; justify-content:space-between; gap:10px; padding-bottom:14px; border-bottom:1px solid var(--line-2)}
  .inf-foll{font-family:"Fraunces",serif; font-size:26px; font-weight:600; line-height:1}
  .inf-niches{display:flex; flex-wrap:wrap; gap:4px; min-height:22px}
  .inf-foot{display:flex; align-items:center; justify-content:space-between; gap:10px; margin-top:auto}
  /* ---------- modal ---------- */
  .scrim{position:fixed; inset:0; background:rgba(33,28,23,.42); backdrop-filter:blur(2px); display:none; align-items:center; justify-content:center; z-index:50; padding:18px}
  .scrim.on{display:flex}
  .modal{background:var(--paper); border-radius:18px; max-width:560px; width:100%; max-height:90vh; overflow:auto; box-shadow:0 30px 70px -20px rgba(33,28,23,.5)}
  .modal-h{padding:18px 22px; border-bottom:1px solid var(--line); display:flex; justify-content:space-between; align-items:center; position:sticky; top:0; background:var(--paper)}
  .modal-h h3{font-family:"Fraunces",serif; margin:0; font-size:19px; font-weight:600}
  .modal-b{padding:20px 22px}
  .modal-f{padding:14px 22px; border-top:1px solid var(--line); display:flex; justify-content:flex-end; gap:10px; position:sticky; bottom:0; background:var(--paper)}
  /* ---------- matcher ---------- */
  .match-grid{display:grid; grid-template-columns:300px 1fr; gap:16px}
  .roster-card{display:flex; align-items:center; gap:12px; padding:11px 14px; border:1px solid var(--line); border-radius:12px; margin-bottom:9px}
  .roster-card:hover{border-color:var(--coral)}
  .av{width:36px; height:36px; border-radius:50%; background:linear-gradient(135deg,var(--coral),var(--gold)); display:grid; place-items:center; color:#fff; font-weight:700; font-size:14px; flex-shrink:0; font-family:"Fraunces",serif}
  .pill-stat{display:flex; gap:20px; padding:14px 18px; background:var(--coral-soft); border-radius:12px; margin-bottom:14px; flex-wrap:wrap}
  .pill-stat .k{font-family:"Fraunces",serif; font-size:22px; font-weight:600}
  .pill-stat .l{font-size:11px; text-transform:uppercase; letter-spacing:.05em; color:var(--coral-deep)}
  .link{color:var(--coral-deep); cursor:pointer; font-weight:600; background:none; border:0; font:inherit; padding:0}
  .link:hover{text-decoration:underline}
  @media(max-width:760px){
    .stat-row{grid-template-columns:1fr 1fr}
    .two,.match-grid{grid-template-columns:1fr}
    .grid-form{grid-template-columns:1fr}
    .hide-sm{display:none}
  }
  .gate{min-height:100vh; display:flex; align-items:center; justify-content:center; padding:22px}
  .gate-card{width:100%; max-width:380px; padding:30px 28px}
  .au-msg{font-size:12.5px; color:var(--sage); margin-top:10px; min-height:16px; line-height:1.4}
  .au-msg.err{color:var(--coral-deep)}
</style>

<div id="gate" class="gate" style="display:none"></div>

<div id="appwrap" class="wrap" style="display:none">
  <header class="top">
    <div class="brand">
      <h1>Assessoria<span class="dot">.</span></h1>
      <small>Painel de talentos</small>
    </div>
    <div style="display:flex;align-items:center;gap:10px;flex-wrap:wrap">
      <span id="savePill" class="save-pill">salvo</span>
      <span id="wsBox" class="bchip" style="color:var(--sage);background:var(--sage-soft);border:1px solid var(--sage)"></span>
      <button class="iconbtn" title="Convidar sócia" onclick="showInvite()" style="width:auto;padding:0 10px;font-size:12.5px;font-weight:600">Convidar</button>
      <span id="userBox" class="muted" style="font-size:12.5px"></span>
      <button class="iconbtn" title="Sair" onclick="logout()" style="width:auto;padding:0 10px;font-size:12.5px;font-weight:600">Sair</button>
    </div>
  </header>

  <nav class="tabs" id="tabs">
    <button data-tab="painel" class="active">Painel</button>
    <button data-tab="influ">Influenciadores</button>
    <button data-tab="marcas">Marcas</button>
    <button data-tab="camp">Campanhas</button>
    <button data-tab="match">Match</button>
  </nav>

  <section id="view"></section>
</div>

<!-- modal host -->
<div class="scrim" id="scrim"><div class="modal" id="modal"></div></div>

<script>
/* ============================ estado ============================ */
/* ============================================================
   Conexão com o Supabase.
   BUILTIN_* = conexão fixa do site (preenchida 1x pelo dono).
   A chave "publishable/anon" PODE ser pública — é protegida pelo RLS.
   Com elas preenchidas, o usuário final NÃO vê nada de chave:
   só faz login com e-mail e senha.
   ============================================================ */
const BUILTIN_URL = "https://efskrnrpqgtgkaiulrpb.supabase.co";   // <- dono cola a Project URL aqui
const BUILTIN_KEY = "sb_publishable_BHuFybhaK0yANvm_NcOEJw_3vAsmnAI";   // <- dono cola a chave publishable aqui
function normUrl(u){ u=(u||'').trim(); try{ return new URL(u).origin; }catch(e){ return u.replace(/\/+$/,''); } }
let SUPABASE_URL = normUrl(BUILTIN_URL) || localStorage.getItem('sb_url') || "";
let SUPABASE_KEY = BUILTIN_KEY || localStorage.getItem('sb_key') || "";

let DB={ influencers:[], brands:[], campaigns:[], rates:{reel:50, story:20} };
let sb=null, rtTimer=null, booted=false;
let WS=null, WSNAME='', WSCODE='';   // agência (workspace) atual

function seed(){
  const raw=[
    ["@mariannasdf",14000,"Millennials","REC","Moda e lifestyle"],
    ["@mariaoucarolina",5000,"","REC","Moda"],
    ["@dborahmendess",20000,"Gen Z","","Beauty e lifestyle"],
    ["@ayanelemoss",4000,"Gen Z","REC","Modelo"],
    ["@robertamirandaag",11000,"","REC","Provador, lifestyle e saúde"],
    ["@claracvd",100000,"Gen Z","REC","Beauty e lifestyle"],
    ["@leticiaboo_",10000,"Gen Z","REC","Maternidade e beauty"],
    ["@claravida",120000,"Gen Z","REC","Lifestyle"],
    ["@julianalatache",140000,"","REC","Maternidade e moda"],
    ["@mjuliameireles",65000,"Gen Z","REC","Moda e lifestyle"],
    ["@tataobana_",71000,"Gen Z","REC","Moda e lifestyle"],
    ["@meduardapontual",55000,"Gen Z","REC","Moda e lifestyle"],
    ["@camiccarv",13000,"","REC","Lifestyle"],
    ["@deb.rocha",150000,"","JP","Perfumes e dicas"],
    ["@dudarlucena",25000,"","Caruaru","Beauty e lifestyle"],
    ["@milenaxlopez",30000,"Gen Z","RJ","Beauty"],
    ["@daily_cidrack",30000,"","","Beauty"],
    ["@malicemacdowell",120000,"Millennials","REC","Maternidade"],
    ["@lecarossiter",40000,"Millennials","","Dicas e gastronomia"],
    ["@cucaamorim",350000,"Millennials","REC","Maternidade e Beauty"],
  ];
  DB.influencers = raw.map((r,i)=>({
    id:'i'+(i+1), ig:r[0], tiktok:"", followers:r[1], gen:r[2],
    loc:r[3], niche:r[4], engaj:null, status:"ativo", notas:"",
    brand:"", phone:"", email:""
  }));
  DB.brands=[
    {id:'b1', name:"RN", contato:"", canal:"", niche:"Moda, Maternidade", status:"Ativa", ultimoContato:"2026-05-20", notas:"Respondeu — topou campanha de inverno"},
    {id:'b2', name:"Marca exemplo", contato:"", canal:"", niche:"Beauty", status:"Prospect", ultimoContato:"", notas:""}
  ];
  const ju=DB.influencers.find(x=>x.ig==="@julianalatache"); if(ju) ju.brand="RN";
  DB.campaigns=[
    {id:'c1', titulo:"Coleção Inverno", brand:"RN", influs:[ju?ju.id:''].filter(Boolean),
     valor:4000, entrega:"2026-06-10", pagamento:"2026-06-25", status:"A produzir", notas:"2 reels + 3 stories"}
  ];
}

/* ===== camada de dados (Supabase) ===== */
function configOk(){ return SUPABASE_URL.startsWith('http') && SUPABASE_KEY.length>20; }
function flash(t,warn){ const p=document.getElementById('savePill'); if(!p)return; p.textContent=t; p.className='save-pill'+(warn?' warn':''); }
async function sbLoadAll(){
  const [inf,br,ca,st]=await Promise.all([
    sb.from('influencers').select('id,data').eq('workspace_id',WS),
    sb.from('brands').select('id,data').eq('workspace_id',WS),
    sb.from('campaigns').select('id,data').eq('workspace_id',WS),
    sb.from('settings').select('key,data').eq('workspace_id',WS).eq('key','rates')
  ]);
  DB.influencers=(inf.data||[]).map(r=>({...r.data,id:r.id}));
  DB.brands=(br.data||[]).map(r=>({...r.data,id:r.id}));
  DB.campaigns=(ca.data||[]).map(r=>({...r.data,id:r.id}));
  DB.rates=(st.data&&st.data[0]&&st.data[0].data)||{reel:50,story:20};
}
async function sbUpsert(table,rec){ const {id,...rest}=rec; const {error}=await sb.from(table).upsert({id,workspace_id:WS,data:rest}); flash(error?'erro ao salvar':'salvo ✓', !!error); if(error)console.error(error); }
async function sbDelete(table,id){ const {error}=await sb.from(table).delete().eq('id',id).eq('workspace_id',WS); if(error){flash('erro ao remover',1);console.error(error);} }
async function sbRates(r){ const {error}=await sb.from('settings').upsert({workspace_id:WS,key:'rates',data:r}); flash(error?'erro':'salvo ✓', !!error); }
async function loadExample(){
  if(!confirm('Carregar o casting de exemplo nesta agência? Você pode editar/apagar depois.'))return;
  seed();
  for(const r of DB.influencers) await sbUpsert('influencers',r);
  for(const r of DB.brands) await sbUpsert('brands',r);
  for(const r of DB.campaigns) await sbUpsert('campaigns',r);
  await sbRates(DB.rates); render();
}
async function resetExample(){ await loadExample(); }

/* ===== sincronização ao vivo (opcional) ===== */
function subscribeRealtime(){
  ['influencers','brands','campaigns','settings'].forEach(t=>{
    sb.channel('rt-'+t).on('postgres_changes',{event:'*',schema:'public',table:t},scheduleSync).subscribe();
  });
}
function scheduleSync(){ clearTimeout(rtTimer); rtTimer=setTimeout(async()=>{ if(WS){ await sbLoadAll(); render(); } },350); }

/* ===== login + agência (workspace) ===== */
async function boot(){
  if(!configOk()){ showSetup(); return; }
  sb=supabase.createClient(SUPABASE_URL,SUPABASE_KEY);
  sb.auth.onAuthStateChange((_e,session)=>{ session?afterLogin():showLogin(); });
  const {data:{session}}=await sb.auth.getSession();
  session?afterLogin():showLogin();
}
async function afterLogin(){
  const {data:mem}=await sb.from('members').select('workspace_id, workspaces(name,invite_code)').limit(1);
  if(!mem || !mem.length){ showOnboard(); return; }
  WS=mem[0].workspace_id;
  WSNAME=mem[0].workspaces?mem[0].workspaces.name:'';
  WSCODE=mem[0].workspaces?mem[0].workspaces.invite_code:'';
  document.getElementById('gate').style.display='none';
  document.getElementById('appwrap').style.display='';
  try{ const u=(await sb.auth.getUser()).data.user; const ub=document.getElementById('userBox'); if(ub) ub.textContent=u?u.email:''; }catch(e){}
  const wb=document.getElementById('wsBox'); if(wb) wb.textContent=WSNAME;
  await sbLoadAll(); render();
  if(!booted){ subscribeRealtime(); booted=true; }
}
function showOnboard(){
  const a=document.getElementById('appwrap'); if(a)a.style.display='none';
  const g=document.getElementById('gate'); g.style.display='';
  g.innerHTML=`<div class="gate-card card">
    <div class="brand" style="justify-content:center;margin-bottom:4px"><h1>Assessoria<span class="dot">.</span></h1></div>
    <p class="muted" style="text-align:center;margin:0 0 18px;font-size:13.5px">Bem-vinda! Como você quer começar?</p>
    <label class="fld">Criar a sua agência</label>
    <input id="ob_name" placeholder="Nome da sua agência">
    <button class="btn" style="width:100%;margin-top:9px" onclick="doCreateWs()">Criar agência</button>
    <div style="text-align:center;margin:16px 0;color:var(--ink-soft);font-size:12px">— ou —</div>
    <label class="fld">Entrar numa agência por convite</label>
    <input id="ob_code" placeholder="Código de convite">
    <button class="btn ghost" style="width:100%;margin-top:9px" onclick="doJoinWs()">Entrar com código</button>
    <div id="ob_msg" class="au-msg"></div>
    <div style="text-align:center;margin-top:14px"><button class="link" style="font-size:12px" onclick="logout()">Sair</button></div>
  </div>`;
}
async function doCreateWs(){
  const name=document.getElementById('ob_name').value.trim();
  const msg=document.getElementById('ob_msg');
  if(!name){ msg.textContent='Dê um nome pra sua agência.'; msg.className='au-msg err'; return; }
  msg.textContent='Criando…'; msg.className='au-msg';
  const {error}=await sb.rpc('create_workspace',{p_name:name});
  if(error){ msg.textContent=error.message; msg.className='au-msg err'; return; }
  afterLogin();
}
async function doJoinWs(){
  const code=document.getElementById('ob_code').value.trim();
  const msg=document.getElementById('ob_msg');
  if(!code){ msg.textContent='Cole o código de convite.'; msg.className='au-msg err'; return; }
  msg.textContent='Entrando…'; msg.className='au-msg';
  const {error}=await sb.rpc('join_workspace',{p_code:code});
  if(error){ msg.textContent='Código inválido.'; msg.className='au-msg err'; return; }
  afterLogin();
}
function showInvite(){ alert('Código de convite da agência "'+WSNAME+'":\n\n'+WSCODE+'\n\nMande esse código pra sua sócia. Ela cria a conta dela e usa "Entrar com código" pra cair na mesma agência.'); }
function showLogin(){
  const a=document.getElementById('appwrap'); if(a)a.style.display='none';
  const g=document.getElementById('gate'); g.style.display='';
  g.innerHTML=`<div class="gate-card card">
    <div class="brand" style="justify-content:center;margin-bottom:4px"><h1>Assessoria<span class="dot">.</span></h1></div>
    <p class="muted" style="text-align:center;margin:0 0 18px;font-size:13.5px">Entre para acessar o painel da agência</p>
    <label class="fld">E-mail</label><input id="au_e" type="email" placeholder="voce@email.com">
    <label class="fld" style="margin-top:11px">Senha</label><input id="au_p" type="password" placeholder="mínimo 6 caracteres">
    <div id="au_msg" class="au-msg"></div>
    <button class="btn" style="width:100%;margin-top:14px" onclick="doAuth('in')">Entrar</button>
    <button class="btn ghost" style="width:100%;margin-top:9px" onclick="doAuth('up')">Criar conta</button>
    ${configIsBuiltin()?'':'<div style="text-align:center;margin-top:14px"><button class="link" style="font-size:12px" onclick="reconfig()">Reconfigurar conexão</button></div>'}
  </div>`;
}
function configIsBuiltin(){ return !!(normUrl(BUILTIN_URL) && BUILTIN_KEY); }
async function doAuth(mode){
  const em=document.getElementById('au_e').value.trim();
  const pw=document.getElementById('au_p').value;
  const msg=document.getElementById('au_msg');
  if(!em||!pw){ msg.textContent='Preencha e-mail e senha.'; msg.className='au-msg err'; return; }
  msg.textContent='Aguarde…'; msg.className='au-msg';
  const {error}= mode==='in'
    ? await sb.auth.signInWithPassword({email:em,password:pw})
    : await sb.auth.signUp({email:em,password:pw});
  if(error){ msg.textContent=error.message; msg.className='au-msg err'; }
  else if(mode==='up'){ msg.textContent='Conta criada! Se pedir confirmação por e-mail, confirme e depois entre.'; msg.className='au-msg'; }
}
async function logout(){ WS=null; WSNAME=''; booted=false; await sb.auth.signOut(); }
function reconfig(){ localStorage.removeItem('sb_url'); localStorage.removeItem('sb_key'); SUPABASE_URL=''; SUPABASE_KEY=''; sb=null; booted=false; WS=null; showSetup(); }
function showSetup(){
  const a=document.getElementById('appwrap'); if(a)a.style.display='none';
  const g=document.getElementById('gate'); g.style.display='';
  g.innerHTML=`<div class="gate-card card">
    <div class="brand" style="justify-content:center;margin-bottom:4px"><h1>Assessoria<span class="dot">.</span></h1></div>
    <p class="muted" style="text-align:center;margin:0 0 16px;font-size:13.5px">Conexão do app (só o dono faz isto)</p>
    <label class="fld">URL do projeto</label><input id="cf_u" placeholder="https://xxxxx.supabase.co" value="${SUPABASE_URL||''}">
    <label class="fld" style="margin-top:11px">Chave publishable / anon</label><input id="cf_k" placeholder="sb_publishable_... ou eyJ..." value="${SUPABASE_KEY||''}">
    <div id="cf_msg" class="au-msg"></div>
    <button class="btn" style="width:100%;margin-top:14px" onclick="saveSetup()">Conectar</button>
    <p class="muted" style="font-size:11.5px;margin-top:14px;line-height:1.5">A URL está em Supabase → Project Settings → Data API. A chave está em API Keys (use a <b>Publishable</b>). Pode colar a URL com barra no final que eu ajusto sozinho.</p>
  </div>`;
}
function saveSetup(){
  const u=normUrl(document.getElementById('cf_u').value);
  const k=document.getElementById('cf_k').value.trim();
  const msg=document.getElementById('cf_msg');
  if(!u.startsWith('http')||!u.includes('.supabase.')){ msg.textContent='A URL parece incorreta. Deve ser algo como https://xxxxx.supabase.co'; msg.className='au-msg err'; return; }
  if(k.length<20){ msg.textContent='A chave parece curta demais. Copie a chave Publishable/anon completa.'; msg.className='au-msg err'; return; }
  localStorage.setItem('sb_url',u); localStorage.setItem('sb_key',k);
  SUPABASE_URL=u; SUPABASE_KEY=k; boot();
}

/* ============================ helpers ============================ */
const LOCS={REC:"Recife",JP:"João Pessoa",RJ:"Rio de Janeiro",Caruaru:"Caruaru"};
const uid=p=>p+Math.random().toString(36).slice(2,8);
function tierOf(f){ if(f<10000)return["nano","t-nano"]; if(f<100000)return["micro","t-micro"]; if(f<1000000)return["macro","t-macro"]; return["mega","t-mega"]; }
function fmtN(n){ if(n>=1000000)return (n/1000000).toFixed(n%1000000?1:0)+"M"; if(n>=1000)return (n/1000).toFixed(n%1000?1:0)+"k"; return ""+n; }
function fmtMoney(n){ return "R$ "+Math.round(n).toLocaleString("pt-BR"); }
function nicheTags(s){ return (s||"").split(/,|\be\b/i).map(x=>x.trim()).filter(Boolean); }
function reelValue(f){ return f/1000*DB.rates.reel; }
function storyValue(f){ return f/1000*DB.rates.story; }
function esc(s){ return (s||"").replace(/[&<>"]/g,c=>({"&":"&amp;","<":"&lt;",">":"&gt;",'"':"&quot;"}[c])); }
const BRANDPAL=['#D85A3A','#5B6B4F','#7A4A63','#C29A3B','#3A6B8C','#9B5524','#4F7A6B','#A03A52'];
function brandColor(name){ let h=0; for(const ch of name)h=(h*31+ch.charCodeAt(0))>>>0; return BRANDPAL[h%BRANDPAL.length]; }
function brandChip(name){ if(!name)return '<span class="muted">—</span>'; const c=brandColor(name); return `<span class="bchip" style="color:${c};background:${c}1a;border:1px solid ${c}40">${esc(name)}</span>`; }
const TODAY=new Date(); TODAY.setHours(0,0,0,0);
function fmtDate(iso){ if(!iso)return '—'; const[y,m,d]=iso.split('-'); return `${d}/${m}`; }
function daysUntil(iso){ if(!iso)return null; const t=new Date(iso+'T00:00:00'); return Math.round((t-TODAY)/864e5); }
function dueChip(iso,label){ if(!iso)return '<span class="muted">—</span>'; const d=daysUntil(iso); let cl='due-ok',tag=''; if(d<0){cl='due-late';tag=` · ${label} atrasado`;} else if(d<=3){cl='due-soon';tag=` · em ${d}d`;} return `<span class="due ${cl}">${fmtDate(iso)}${tag}</span>`; }
const BRAND_STATUS={"Prospect":"#8a7f6d","Contatado":"#3A6B8C","Respondeu":"#C29A3B","Ativa":"#5B6B4F","Sem retorno":"#9b8e7a","Pausada":"#A03A52"};
const CAMP_STATUS={"A produzir":"#C29A3B","Conteúdo entregue":"#3A6B8C","Aguardando pagamento":"#D85A3A","Pago":"#5B6B4F"};
function statusChip(s,map){ const c=map[s]||"#888"; return `<span class="bchip" style="color:${c};background:${c}1a;border:1px solid ${c}40">${esc(s||'—')}</span>`; }

/* ============================ router ============================ */
let TAB='painel';
document.getElementById('tabs').addEventListener('click',e=>{
  const b=e.target.closest('button[data-tab]'); if(!b)return;
  TAB=b.dataset.tab;
  [...document.querySelectorAll('#tabs button')].forEach(x=>x.classList.toggle('active',x===b));
  render();
});
function render(){
  const v=document.getElementById('view');
  if(TAB==='painel')v.innerHTML=viewPainel();
  if(TAB==='influ'){v.innerHTML=viewInflu(); wireInflu();}
  if(TAB==='marcas'){v.innerHTML=viewMarcas(); wireMarcas();}
  if(TAB==='camp'){v.innerHTML=viewCamp();}
  if(TAB==='match'){v.innerHTML=viewMatch(); wireMatch();}
}

/* ============================ PAINEL ============================ */
function viewPainel(){
  const inf=DB.influencers;
  const total=inf.length;
  const reach=inf.reduce((a,b)=>a+(+b.followers||0),0);
  const avg=total?reach/total:0;
  const eng=inf.filter(i=>i.engaj!=null);
  const avgEng=eng.length?eng.reduce((a,b)=>a+(+b.engaj),0)/eng.length:null;

  // por tier
  const tiers={nano:0,micro:0,macro:0,mega:0};
  inf.forEach(i=>{ tiers[tierOf(+i.followers)[0]]++; });
  const tierColors={nano:'#b6ab97',micro:'var(--sage)',macro:'var(--coral)',mega:'var(--plum)'};

  // por nicho (tag primária)
  const nm={};
  inf.forEach(i=>nicheTags(i.niche).forEach(t=>{const k=t.toLowerCase(); nm[k]=(nm[k]||0)+1;}));
  const niches=Object.entries(nm).sort((a,b)=>b[1]-a[1]).slice(0,6);
  const maxN=Math.max(1,...niches.map(n=>n[1]));

  // valor estimado do roster (1 reel cada)
  const rosterReel=inf.reduce((a,b)=>a+reelValue(+b.followers),0);

  return `
  <div class="stat-row">
    <div class="card stat"><div class="k">${total}</div><div class="l">Influenciadores</div></div>
    <div class="card stat"><div class="k">${fmtN(reach)}</div><div class="l">Alcance somado</div><div class="sub">média ${fmtN(Math.round(avg))}/perfil</div></div>
    <div class="card stat"><div class="k">${avgEng!=null?avgEng.toFixed(1)+'%':'—'}</div><div class="l">Engajamento médio</div><div class="sub">${eng.length}/${total} preenchidos</div></div>
    <div class="card stat"><div class="k" style="font-size:23px">${fmtMoney(rosterReel)}</div><div class="l">Valor estimado · 1 reel cada</div></div>
  </div>

  <div class="two">
    <div class="card pad">
      <h2 class="sec">Nichos do casting</h2>
      <p class="muted" style="margin:0 0 14px;font-size:13px">Distribuição automática por tag de nicho</p>
      ${niches.map(([n,c])=>`
        <div class="bar-item">
          <div class="name">${esc(n)}</div>
          <div class="bar-track"><div class="bar-fill" style="width:${c/maxN*100}%;background:var(--coral)"></div></div>
          <div class="val">${c}</div>
        </div>`).join('')||'<p class="muted">Sem dados.</p>'}
    </div>

    <div class="card pad">
      <h2 class="sec">Por porte</h2>
      <p class="muted" style="margin:0 0 14px;font-size:13px">Classificação automática pelo nº de seguidores</p>
      ${Object.entries(tiers).map(([t,c])=>`
        <div class="bar-item">
          <div class="name">${t}</div>
          <div class="bar-track"><div class="bar-fill" style="width:${c/Math.max(1,total)*100}%;background:${tierColors[t]}"></div></div>
          <div class="val">${c}</div>
        </div>`).join('')}
    </div>
  </div>

  <div class="two" style="grid-template-columns:1fr 1fr">
    <div class="card pad">
      <h2 class="sec">Tabela de preços</h2>
      <p class="muted" style="margin:0 0 14px;font-size:13px">Base do cálculo automático de valor (por 1.000 seguidores)</p>
      <div class="grid-form">
        <div><label class="fld">Reel · R$ / 1k</label><input type="number" id="rateReel" value="${DB.rates.reel}"></div>
        <div><label class="fld">Story · R$ / 1k</label><input type="number" id="rateStory" value="${DB.rates.story}"></div>
      </div>
      <p class="muted" style="font-size:12px;margin-top:12px">Ex.: um perfil de 100k → reel ${fmtMoney(reelValue(100000))}, story ${fmtMoney(storyValue(100000))}. Ajuste pros valores reais da sua agência.</p>
    </div>
    <div class="card pad">
      <h2 class="sec">Dados</h2>
      <p class="muted" style="margin:0 0 14px;font-size:13px">Seu casting fica salvo automaticamente no navegador.</p>
      <div style="display:flex;gap:10px;flex-wrap:wrap">
        <button class="btn ghost" onclick="exportCsv()">Exportar CSV</button>
        <button class="btn ghost" onclick="resetExample()">Carregar dados de exemplo</button>
      </div>
    </div>
  </div>`;
}
let ratesTimer;
document.addEventListener('input',e=>{
  if(e.target.id==='rateReel'){DB.rates.reel=+e.target.value||0; queueRates();}
  if(e.target.id==='rateStory'){DB.rates.story=+e.target.value||0; queueRates();}
});
function queueRates(){ clearTimeout(ratesTimer); ratesTimer=setTimeout(()=>sbRates(DB.rates),500); }

/* ============================ INFLUENCIADORES ============================ */
let fState={q:'',niche:'all',tier:'all',sort:'followers',dir:-1};
function viewInflu(){
  const allNiches=[...new Set(DB.influencers.flatMap(i=>nicheTags(i.niche).map(t=>t.toLowerCase())))].sort();
  let rows=DB.influencers.filter(i=>{
    const q=fState.q.toLowerCase();
    const hit=!q || (i.ig+i.niche+i.loc+i.gen+(i.brand||'')).toLowerCase().includes(q);
    const nN=fState.niche==='all'||nicheTags(i.niche).map(t=>t.toLowerCase()).includes(fState.niche);
    const tN=fState.tier==='all'||tierOf(+i.followers)[0]===fState.tier;
    return hit&&nN&&tN;
  });
  rows.sort((a,b)=>{
    let x=a[fState.sort],y=b[fState.sort];
    if(fState.sort==='followers'){x=+x;y=+y;} else {x=(''+x).toLowerCase();y=(''+y).toLowerCase();}
    return x<y?-fState.dir:x>y?fState.dir:0;
  });
  return `
  <div class="toolbar">
    <div class="search">
      <svg width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="11" cy="11" r="7"/><path d="m21 21-4.3-4.3"/></svg>
      <input id="fq" placeholder="Buscar perfil, nicho, cidade…" value="${esc(fState.q)}">
    </div>
    <select id="fniche">
      <option value="all">Todos os nichos</option>
      ${allNiches.map(n=>`<option value="${n}" ${fState.niche===n?'selected':''}>${esc(n)}</option>`).join('')}
    </select>
    <select id="ftier">
      ${['all','nano','micro','macro','mega'].map(t=>`<option value="${t}" ${fState.tier===t?'selected':''}>${t==='all'?'Todos os portes':t}</option>`).join('')}
    </select>
    <select id="fsort">
      ${[['followers:-1','Mais seguidores'],['followers:1','Menos seguidores'],['ig:1','A–Z'],['brand:1','Por marca']].map(([v,l])=>`<option value="${v}" ${fState.sort+':'+fState.dir===v?'selected':''}>${l}</option>`).join('')}
    </select>
    <button class="btn" onclick="openInflu()">+ Novo</button>
  </div>

  <div class="inf-grid">
    ${rows.length?rows.map(i=>{
      const[t,cl]=tierOf(+i.followers);
      const init=esc((i.ig.replace('@','')[0]||'?').toUpperCase());
      const meta=[LOCS[i.loc]||i.loc||'', i.gen||''].filter(Boolean).join(' · ')||'sem local';
      return `<div class="inf-card">
        <div class="inf-top">
          <div class="av av-lg">${init}</div>
          <div style="flex:1;min-width:0">
            <a class="inf-handle" href="https://instagram.com/${i.ig.replace('@','')}" target="_blank" rel="noopener">${esc(i.ig)}</a>
            <div class="inf-meta">${esc(meta)}</div>
          </div>
          <div class="inf-rowbtns">
            <button class="iconbtn" title="Editar" onclick="openInflu('${i.id}')">✎</button>
            <button class="iconbtn" title="Remover" onclick="delInflu('${i.id}')">🗑</button>
          </div>
        </div>
        <div class="inf-stat">
          <div><span class="inf-foll">${fmtN(+i.followers)}</span> <span class="muted" style="font-size:12.5px">seguidores</span></div>
          <span class="tier ${cl}">${t}</span>
        </div>
        <div class="inf-line">${i.brand?brandChip(i.brand):'<span class="muted" style="font-size:12.5px">sem marca conectada</span>'}</div>
        <div class="inf-niches">${nicheTags(i.niche).map(n=>`<span class="niche-chip">${esc(n)}</span>`).join('')||'<span class="muted">—</span>'}</div>
        <div class="inf-foot">
          <button class="contact-btn" onclick="contactMenu('${i.id}',event)">✉ Contato</button>
          <span class="muted" style="font-size:12px">reel ~ ${fmtMoney(reelValue(+i.followers))}</span>
        </div>
      </div>`;
    }).join(''):`<div class="card empty" style="grid-column:1/-1">Nenhum perfil encontrado.</div>`}
  </div>
  <p class="muted" style="font-size:12.5px;margin-top:14px">${rows.length} de ${DB.influencers.length} perfis · porte e valor calculados automaticamente</p>`;
}
function wireInflu(){
  const q=document.getElementById('fq');
  q.oninput=()=>{fState.q=q.value; const p=q.selectionStart; render(); const nq=document.getElementById('fq'); nq.focus(); nq.setSelectionRange(p,p);};
  document.getElementById('fniche').onchange=e=>{fState.niche=e.target.value; render();};
  document.getElementById('ftier').onchange=e=>{fState.tier=e.target.value; render();};
  document.getElementById('fsort').onchange=e=>{const[s,d]=e.target.value.split(':'); fState.sort=s; fState.dir=+d; render();};
}
async function delInflu(id){ if(!confirm('Remover este perfil?'))return; DB.influencers=DB.influencers.filter(i=>i.id!==id); render(); await sbDelete('influencers',id); }
function openInflu(id){
  const i = id?DB.influencers.find(x=>x.id===id):{ig:'',tiktok:'',followers:'',gen:'',loc:'',niche:'',engaj:'',status:'ativo',notas:'',brand:'',phone:'',email:''};
  modal(`
    <div class="modal-h"><h3>${id?'Editar perfil':'Novo perfil'}</h3><button class="iconbtn" onclick="closeModal()">✕</button></div>
    <div class="modal-b">
      <div class="grid-form">
        <div><label class="fld">Instagram</label><input id="m_ig" value="${esc(i.ig)}" placeholder="@usuario"></div>
        <div><label class="fld">TikTok</label><input id="m_tt" value="${esc(i.tiktok)}" placeholder="@usuario"></div>
        <div><label class="fld">Seguidores</label><input id="m_f" type="number" value="${i.followers}" placeholder="ex: 50000"></div>
        <div><label class="fld">Engajamento (%)</label><input id="m_e" type="number" step="0.1" value="${i.engaj??''}" placeholder="opcional"></div>
        <div><label class="fld">Geração</label><select id="m_g">
          ${['','Gen Z','Millennials','Gen X'].map(g=>`<option ${i.gen===g?'selected':''}>${g}</option>`).join('')}
        </select></div>
        <div><label class="fld">Local</label><input id="m_l" value="${esc(i.loc)}" placeholder="REC, JP, RJ…"></div>
        <div><label class="fld">Marca conectada</label><input id="m_br" list="brandlist" value="${esc(i.brand||'')}" placeholder="ex: RN"><datalist id="brandlist">${DB.brands.map(b=>`<option value="${esc(b.name)}">`).join('')}</datalist></div>
        <div><label class="fld">WhatsApp</label><input id="m_ph" value="${esc(i.phone||'')}" placeholder="ex: 5581999998888"></div>
        <div><label class="fld">E-mail</label><input id="m_em" value="${esc(i.email||'')}" placeholder="opcional"></div>
        <div style="grid-column:1/3"><label class="fld">Nicho</label><input id="m_n" value="${esc(i.niche)}" placeholder="Moda e lifestyle"></div>
        <div style="grid-column:1/3"><label class="fld">Notas</label><textarea id="m_nt" rows="2">${esc(i.notas)}</textarea></div>
      </div>
    </div>
    <div class="modal-f">
      <button class="btn ghost" onclick="closeModal()">Cancelar</button>
      <button class="btn" onclick="saveInflu('${id||''}')">Salvar</button>
    </div>`);
}
async function saveInflu(id){
  const g=k=>document.getElementById(k).value;
  const rec={ ig:g('m_ig')||'@', tiktok:g('m_tt'), followers:+g('m_f')||0, engaj:g('m_e')===''?null:+g('m_e'),
    gen:g('m_g'), loc:g('m_l'), niche:g('m_n'), notas:g('m_nt'), status:'ativo',
    brand:g('m_br'), phone:g('m_ph'), email:g('m_em') };
  if(id){ rec.id=id; Object.assign(DB.influencers.find(x=>x.id===id),rec); }
  else { rec.id=uid('i'); DB.influencers.push(rec); }
  closeModal(); render(); await sbUpsert('influencers',rec);
}

/* ============================ MARCAS ============================ */
let bFilter='all';
function viewMarcas(){
  const counts={}; Object.keys(BRAND_STATUS).forEach(s=>counts[s]=0);
  DB.brands.forEach(b=>{ if(counts[b.status]!=null)counts[b.status]++; });
  let list=DB.brands.filter(b=>bFilter==='all'||b.status===bFilter);
  return `
  <div class="toolbar">
    <h2 class="sec" style="flex:1">Marcas · funil de contato</h2>
    <select id="bfilter">
      <option value="all" ${bFilter==='all'?'selected':''}>Todos os status</option>
      ${Object.keys(BRAND_STATUS).map(s=>`<option value="${s}" ${bFilter===s?'selected':''}>${s} (${counts[s]})</option>`).join('')}
    </select>
    <button class="btn" onclick="openBrand()">+ Nova marca</button>
  </div>
  <div class="card" style="overflow:hidden"><div style="overflow-x:auto"><table>
    <thead><tr><th>Marca</th><th>Status</th><th class="hide-sm">Contato</th><th class="hide-sm">Últ. contato</th><th>Conectados</th><th class="hide-sm">Retorno / notas</th><th></th></tr></thead>
    <tbody>${list.length?list.map(b=>{
      const conn=DB.influencers.filter(x=>(x.brand||'').toLowerCase()===b.name.toLowerCase());
      return `<tr>
      <td class="handle">${brandChip(b.name)}<div class="muted" style="font-size:11.5px;margin-top:2px">${nicheTags(b.niche).map(t=>esc(t)).join(' · ')}</div></td>
      <td>${statusChip(b.status,BRAND_STATUS)}</td>
      <td class="hide-sm">${b.contato||b.canal?`${esc(b.contato||'')}${b.canal?`<div class="muted" style="font-size:12px">${esc(b.canal)}</div>`:''}`:'<span class="muted">—</span>'}</td>
      <td class="hide-sm">${b.ultimoContato?fmtDate(b.ultimoContato):'<span class="muted">—</span>'}</td>
      <td>${conn.length?conn.map(c=>`<span class="niche-chip">${esc(c.ig)}</span>`).join(''):'<span class="muted">nenhum</span>'}</td>
      <td class="hide-sm muted">${esc(b.notas)}</td>
      <td><div class="rowbtns">
        <button class="iconbtn" onclick="openBrand('${b.id}')">✎</button>
        <button class="iconbtn" onclick="delBrand('${b.id}')">🗑</button>
      </div></td></tr>`;}).join(''):`<tr><td colspan="7" class="empty">Nenhuma marca neste status.</td></tr>`}
    </tbody></table></div></div>`;
}
function wireMarcas(){ const f=document.getElementById('bfilter'); if(f)f.onchange=e=>{bFilter=e.target.value; render();}; }
async function delBrand(id){ if(!confirm('Remover marca?'))return; DB.brands=DB.brands.filter(b=>b.id!==id); render(); await sbDelete('brands',id); }
function openBrand(id){
  const b=id?DB.brands.find(x=>x.id===id):{name:'',niche:'',notas:'',contato:'',canal:'',status:'Prospect',ultimoContato:''};
  modal(`
    <div class="modal-h"><h3>${id?'Editar marca':'Nova marca'}</h3><button class="iconbtn" onclick="closeModal()">✕</button></div>
    <div class="modal-b"><div class="grid-form">
      <div><label class="fld">Nome da marca</label><input id="b_n" value="${esc(b.name)}"></div>
      <div><label class="fld">Status</label><select id="b_st">${Object.keys(BRAND_STATUS).map(s=>`<option ${b.status===s?'selected':''}>${s}</option>`).join('')}</select></div>
      <div><label class="fld">Pessoa de contato</label><input id="b_ct" value="${esc(b.contato||'')}" placeholder="ex: Marina (marketing)"></div>
      <div><label class="fld">Canal (e-mail/zap/@)</label><input id="b_cn" value="${esc(b.canal||'')}" placeholder="email ou telefone"></div>
      <div><label class="fld">Último contato</label><input id="b_dt" type="date" value="${b.ultimoContato||''}"></div>
      <div><label class="fld">Nicho de interesse</label><input id="b_ni" value="${esc(b.niche)}" placeholder="Beauty, Maternidade…"></div>
      <div style="grid-column:1/3"><label class="fld">Retorno / notas</label><textarea id="b_nt" rows="2" placeholder="o que a marca respondeu, próximo passo…">${esc(b.notas)}</textarea></div>
    </div></div>
    <div class="modal-f"><button class="btn ghost" onclick="closeModal()">Cancelar</button><button class="btn" onclick="saveBrand('${id||''}')">Salvar</button></div>`);
}
async function saveBrand(id){
  const g=k=>document.getElementById(k).value;
  const rec={name:g('b_n'),status:g('b_st'),contato:g('b_ct'),canal:g('b_cn'),ultimoContato:g('b_dt'),niche:g('b_ni'),notas:g('b_nt')};
  if(id){rec.id=id; Object.assign(DB.brands.find(x=>x.id===id),rec);} else{rec.id=uid('b'); DB.brands.push(rec);}
  closeModal(); render(); await sbUpsert('brands',rec);
}

/* ============================ CAMPANHAS (controle de prazos) ============================ */
function campCost(c){ return DB.influencers.filter(i=>(c.influs||[]).includes(i.id)).reduce((a,b)=>a+reelValue(+b.followers),0); }
function viewCamp(){
  const cs=DB.campaigns.slice();
  const aReceber=cs.filter(c=>c.status!=='Pago').reduce((a,b)=>a+(+b.valor||0),0);
  // agenda: próximos eventos
  const ev=[];
  cs.forEach(c=>{
    if(c.entrega && c.status!=='Conteúdo entregue' && c.status!=='Pago') ev.push({t:'Entrega',iso:c.entrega,c});
    if(c.pagamento && c.status!=='Pago') ev.push({t:'Pagamento',iso:c.pagamento,c});
  });
  ev.sort((a,b)=>(a.iso||'').localeCompare(b.iso||''));
  const next=ev.slice(0,4);

  const byDate=cs.sort((a,b)=>(a.entrega||'9').localeCompare(b.entrega||'9'));
  return `
  <div class="stat-row" style="grid-template-columns:repeat(3,1fr)">
    <div class="card stat"><div class="k">${cs.length}</div><div class="l">Campanhas</div></div>
    <div class="card stat"><div class="k" style="font-size:23px">${fmtMoney(aReceber)}</div><div class="l">A receber</div></div>
    <div class="card stat"><div class="k">${next.length?fmtDate(next[0].iso):'—'}</div><div class="l">Próximo prazo</div>${next.length?`<div class="sub">${next[0].t.toLowerCase()} · ${esc(next[0].c.brand||'')}</div>`:''}</div>
  </div>

  ${next.length?`<div class="card pad" style="margin-top:14px">
    <h2 class="sec">Agenda</h2>
    <p class="muted" style="margin:0 0 12px;font-size:13px">Próximas entregas e pagamentos, em ordem</p>
    ${next.map(e=>`<div class="agenda-row">
      <span class="agenda-tag ${e.t==='Entrega'?'tg-e':'tg-p'}">${e.t}</span>
      <span style="flex:1">${esc(e.c.titulo||'(sem título)')} · ${brandChip(e.c.brand)}</span>
      ${dueChip(e.iso, e.t==='Entrega'?'entrega':'pagamento')}
    </div>`).join('')}
  </div>`:''}

  <div class="toolbar" style="margin-top:16px"><h2 class="sec" style="flex:1">Campanhas</h2><button class="btn" onclick="openCamp()">+ Nova campanha</button></div>
  <div class="card" style="overflow:hidden"><div style="overflow-x:auto"><table>
    <thead><tr><th>Campanha</th><th>Marca</th><th class="hide-sm">Influenciadores</th><th>Valor</th><th>Entrega</th><th>Pagamento</th><th>Status</th><th></th></tr></thead>
    <tbody>${cs.length?byDate.map(c=>{
      const who=DB.influencers.filter(i=>(c.influs||[]).includes(i.id));
      return `<tr>
      <td class="handle">${esc(c.titulo||'(sem título)')}</td>
      <td>${brandChip(c.brand)}</td>
      <td class="hide-sm">${who.length?who.map(w=>`<span class="niche-chip">${esc(w.ig)}</span>`).join(''):'<span class="muted">—</span>'}</td>
      <td class="num">${c.valor?fmtMoney(+c.valor):'<span class="muted">—</span>'}</td>
      <td>${c.status==='Conteúdo entregue'||c.status==='Pago'?`<span class="muted">${fmtDate(c.entrega)} ✓</span>`:dueChip(c.entrega,'entrega')}</td>
      <td>${c.status==='Pago'?`<span class="muted">${fmtDate(c.pagamento)} ✓</span>`:dueChip(c.pagamento,'pagamento')}</td>
      <td>${statusChip(c.status,CAMP_STATUS)}</td>
      <td><div class="rowbtns">
        <button class="iconbtn" onclick="openCamp('${c.id}')">✎</button>
        <button class="iconbtn" onclick="delCamp('${c.id}')">🗑</button>
      </div></td></tr>`;}).join(''):`<tr><td colspan="8" class="empty">Nenhuma campanha ainda. Crie a primeira com o botão acima.</td></tr>`}
    </tbody></table></div></div>`;
}
async function delCamp(id){ if(!confirm('Remover campanha?'))return; DB.campaigns=DB.campaigns.filter(c=>c.id!==id); render(); await sbDelete('campaigns',id); }
function openCamp(id){
  const c=id?DB.campaigns.find(x=>x.id===id):{titulo:'',brand:'',influs:[],valor:'',entrega:'',pagamento:'',status:'A produzir',notas:''};
  const sel=new Set(c.influs||[]);
  modal(`
    <div class="modal-h"><h3>${id?'Editar campanha':'Nova campanha'}</h3><button class="iconbtn" onclick="closeModal()">✕</button></div>
    <div class="modal-b"><div class="grid-form">
      <div style="grid-column:1/3"><label class="fld">Título da campanha</label><input id="k_t" value="${esc(c.titulo)}" placeholder="ex: Coleção Inverno"></div>
      <div><label class="fld">Marca</label><input id="k_b" list="brandlist2" value="${esc(c.brand)}" placeholder="ex: RN"><datalist id="brandlist2">${DB.brands.map(b=>`<option value="${esc(b.name)}">`).join('')}</datalist></div>
      <div><label class="fld">Status</label><select id="k_s">${Object.keys(CAMP_STATUS).map(s=>`<option ${c.status===s?'selected':''}>${s}</option>`).join('')}</select></div>
      <div><label class="fld">Valor (R$)</label><input id="k_v" type="number" value="${c.valor}" placeholder="ex: 4000"></div>
      <div></div>
      <div><label class="fld">Data de entrega</label><input id="k_e" type="date" value="${c.entrega||''}"></div>
      <div><label class="fld">Data de pagamento</label><input id="k_p" type="date" value="${c.pagamento||''}"></div>
      <div style="grid-column:1/3"><label class="fld">Influenciadores</label>
        <div class="chk-grid">${DB.influencers.map(i=>`<label class="chk"><input type="checkbox" value="${i.id}" ${sel.has(i.id)?'checked':''}> ${esc(i.ig)}</label>`).join('')}</div>
      </div>
      <div style="grid-column:1/3"><label class="fld">Notas (entregáveis, briefing…)</label><textarea id="k_nt" rows="2">${esc(c.notas)}</textarea></div>
    </div></div>
    <div class="modal-f"><button class="btn ghost" onclick="closeModal()">Cancelar</button><button class="btn" onclick="saveCamp('${id||''}')">Salvar</button></div>`);
}
async function saveCamp(id){
  const g=k=>document.getElementById(k).value;
  const influs=[...document.querySelectorAll('.chk-grid input:checked')].map(x=>x.value);
  const rec={titulo:g('k_t'),brand:g('k_b'),status:g('k_s'),valor:+g('k_v')||0,entrega:g('k_e'),pagamento:g('k_p'),influs,notas:g('k_nt')};
  if(id){rec.id=id; Object.assign(DB.campaigns.find(x=>x.id===id),rec);} else{rec.id=uid('c'); DB.campaigns.push(rec);}
  closeModal(); render(); await sbUpsert('campaigns',rec);
}

/* ============================ MATCH (busca de casting) ============================ */
let mState={niche:'',tier:'all',loc:'',budget:'',selected:new Set()};
function viewMatch(){
  return `
  <h2 class="sec" style="margin-bottom:14px">Match inteligente de campanha</h2>
  <div class="match-grid">
    <div class="card pad">
      <label class="fld">Nicho da campanha</label>
      <input id="c_niche" value="${esc(mState.niche)}" placeholder="ex: maternidade">
      <label class="fld" style="margin-top:13px">Porte</label>
      <select id="c_tier">${['all','nano','micro','macro','mega'].map(t=>`<option value="${t}" ${mState.tier===t?'selected':''}>${t==='all'?'Qualquer':t}</option>`).join('')}</select>
      <label class="fld" style="margin-top:13px">Local</label>
      <input id="c_loc" value="${esc(mState.loc)}" placeholder="ex: REC (opcional)">
      <label class="fld" style="margin-top:13px">Orçamento (R$)</label>
      <input id="c_budget" type="number" value="${mState.budget}" placeholder="opcional">
      <p class="muted" style="font-size:12px;margin-top:14px">Marque os perfis ao lado pra montar o casting da proposta. O total é calculado na hora (1 reel por perfil).</p>
    </div>
    <div>${matchResults()}</div>
  </div>`;
}
function matchResults(){
  let list=DB.influencers.filter(i=>{
    const nN=!mState.niche||nicheTags(i.niche).some(t=>t.toLowerCase().includes(mState.niche.toLowerCase()));
    const tN=mState.tier==='all'||tierOf(+i.followers)[0]===mState.tier;
    const lN=!mState.loc||(''+i.loc).toLowerCase().includes(mState.loc.toLowerCase());
    return nN&&tN&&lN;
  }).sort((a,b)=>b.followers-a.followers);

  const sel=DB.influencers.filter(i=>mState.selected.has(i.id));
  const totReach=sel.reduce((a,b)=>a+(+b.followers),0);
  const totCost=sel.reduce((a,b)=>a+reelValue(+b.followers),0);
  const over=mState.budget&&totCost>+mState.budget;

  return `
  ${sel.length?`<div class="pill-stat">
    <div><div class="k">${sel.length}</div><div class="l">no casting</div></div>
    <div><div class="k">${fmtN(totReach)}</div><div class="l">alcance</div></div>
    <div><div class="k" style="${over?'color:var(--coral-deep)':''}">${fmtMoney(totCost)}</div><div class="l">custo est.${over?' · acima do orçamento':''}</div></div>
  </div>`:''}
  ${list.length?list.map(i=>{
    const[t,cl]=tierOf(+i.followers); const on=mState.selected.has(i.id);
    return `<div class="roster-card" style="${on?'border-color:var(--coral);background:var(--coral-soft)':''}">
      <div class="av">${esc(i.ig.replace('@','')[0]||'?').toUpperCase()}</div>
      <div style="flex:1;min-width:0">
        <div class="handle">${esc(i.ig)} <span class="tier ${cl}">${t}</span></div>
        <div class="muted" style="font-size:12.5px">${fmtN(+i.followers)} seg · ${esc(i.niche)||'—'} · ${esc(i.loc)||'—'}</div>
      </div>
      <div style="text-align:right">
        <div class="num">${fmtMoney(reelValue(+i.followers))}</div>
        <button class="link" onclick="toggleSel('${i.id}')">${on?'remover':'+ casting'}</button>
      </div>
    </div>`;
  }).join(''):`<div class="card empty">Nenhum perfil bate com esses filtros.</div>`}`;
}
function toggleSel(id){ mState.selected.has(id)?mState.selected.delete(id):mState.selected.add(id); document.querySelector('.match-grid > div:last-child').innerHTML=matchResults(); }
function wireMatch(){
  const map={c_niche:'niche',c_loc:'loc',c_budget:'budget'};
  Object.entries(map).forEach(([id,k])=>{
    const el=document.getElementById(id);
    el.oninput=()=>{mState[k]=el.value; const p=el.selectionStart; document.querySelector('.match-grid > div:last-child').innerHTML=matchResults();};
  });
  document.getElementById('c_tier').onchange=e=>{mState.tier=e.target.value; document.querySelector('.match-grid > div:last-child').innerHTML=matchResults();};
}

/* ============================ modal infra ============================ */
function modal(html){ document.getElementById('modal').innerHTML=html; document.getElementById('scrim').classList.add('on'); }
function closeModal(){ document.getElementById('scrim').classList.remove('on'); }
document.getElementById('scrim').addEventListener('click',e=>{ if(e.target.id==='scrim')closeModal(); });

/* ============================ contato rápido ============================ */
function contactMenu(id,ev){
  ev.stopPropagation(); closePop();
  const i=DB.influencers.find(x=>x.id===id); if(!i)return;
  const user=i.ig.replace('@','');
  const rows=[`<div class="hd">${esc(i.ig)}</div>`];
  rows.push(`<a href="https://ig.me/m/${encodeURIComponent(user)}" target="_blank" rel="noopener">💬 Direct (Instagram)</a>`);
  if(i.phone) rows.push(`<a href="https://wa.me/${i.phone.replace(/\D/g,'')}" target="_blank" rel="noopener">🟢 WhatsApp</a>`);
  if(i.email) rows.push(`<a href="mailto:${esc(i.email)}">✉ E-mail</a>`);
  rows.push(`<a href="https://instagram.com/${encodeURIComponent(user)}" target="_blank" rel="noopener">↗ Abrir perfil</a>`);
  rows.push(`<button onclick="if(navigator.clipboard)navigator.clipboard.writeText('${i.ig}');this.textContent='@ copiado ✓'">⧉ Copiar @</button>`);
  if(!i.phone&&!i.email) rows.push(`<div class="pop-hint">Adicione WhatsApp/e-mail no perfil pra liberar mais canais</div>`);
  const pop=document.createElement('div'); pop.className='pop'; pop.id='pop'; pop.innerHTML=rows.join('');
  document.body.appendChild(pop);
  const r=ev.currentTarget.getBoundingClientRect();
  let top=r.bottom+6, left=r.left;
  if(left+pop.offsetWidth>innerWidth-10) left=innerWidth-pop.offsetWidth-10;
  if(top+pop.offsetHeight>innerHeight-10) top=r.top-pop.offsetHeight-6;
  pop.style.top=Math.max(8,top)+'px'; pop.style.left=Math.max(8,left)+'px';
}
function closePop(){ const p=document.getElementById('pop'); if(p)p.remove(); }
document.addEventListener('click',e=>{ if(!e.target.closest('#pop')&&!e.target.closest('.contact-btn'))closePop(); });
window.addEventListener('scroll',closePop,true);

/* ============================ export ============================ */
function exportCsv(){
  const head=['instagram','tiktok','seguidores','porte','geracao','local','nicho','engajamento','reel_estimado'];
  const lines=DB.influencers.map(i=>[i.ig,i.tiktok,i.followers,tierOf(+i.followers)[0],i.gen,i.loc,i.niche,i.engaj??'',Math.round(reelValue(+i.followers))]
    .map(c=>`"${(''+c).replace(/"/g,'""')}"`).join(','));
  const blob=new Blob(['\ufeff'+[head.join(','),...lines].join('\n')],{type:'text/csv'});
  const a=document.createElement('a'); a.href=URL.createObjectURL(blob); a.download='casting_assessoria.csv'; a.click();
}

boot();
</script>
