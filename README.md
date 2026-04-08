<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>الخطة التشغيلية 2026 | بلدية الخرج</title>
<link href="https://fonts.googleapis.com/css2?family=Tajawal:wght@300;400;500;700;800;900&display=swap" rel="stylesheet">
<script src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/4.4.0/chart.umd.min.js"></script>
<style>
:root{
  --g900:#0a3d22;--g800:#0f4a2b;--g700:#1a6b4a;--g600:#2d8a5e;
  --g400:#4caf80;--g200:#c3e9d4;--g100:#e8f5ee;--g050:#f4faf7;
  --gold:#c9a227;--gold-bg:#fffbeb;
  --white:#fff;--text:#1a2e25;--muted:#6b8a7a;--border:#d4e8da;
  --shadow:0 2px 12px rgba(10,61,34,.09);
  --danger:#c53030;--warn:#d69e2e;--ok:#276749;
  --sidebar:268px;--r:14px;--rs:8px;
}
*{margin:0;padding:0;box-sizing:border-box;}
body{font-family:'Tajawal',sans-serif;background:var(--g050);color:var(--text);font-size:14px;}

/* ── LOGIN ── */
#login-page{min-height:100vh;display:flex;align-items:center;justify-content:center;
  background:linear-gradient(145deg,var(--g900),#0d4030 60%,#0a3525);position:relative;overflow:hidden;}
.lp-grid{position:absolute;inset:0;background-image:
  repeating-linear-gradient(0deg,rgba(255,255,255,.025) 0,rgba(255,255,255,.025) 1px,transparent 1px,transparent 55px),
  repeating-linear-gradient(90deg,rgba(255,255,255,.025) 0,rgba(255,255,255,.025) 1px,transparent 1px,transparent 55px);}
.lp-glow{position:absolute;width:600px;height:600px;border-radius:50%;
  background:radial-gradient(circle,rgba(45,138,94,.25),transparent 65%);top:-200px;right:-150px;}
.lp-glow2{position:absolute;width:400px;height:400px;border-radius:50%;
  background:radial-gradient(circle,rgba(201,162,39,.12),transparent 65%);bottom:-100px;left:-100px;}
.login-box{width:430px;position:relative;z-index:1;animation:riseUp .6s cubic-bezier(.34,1.56,.64,1);}
@keyframes riseUp{from{opacity:0;transform:translateY(40px)}to{opacity:1;transform:translateY(0)}}
.login-brand{text-align:center;margin-bottom:1.8rem;color:#fff;}
.lb-seal{width:76px;height:76px;margin:0 auto 1rem;border-radius:50%;
  background:linear-gradient(135deg,var(--g700),var(--g600));border:2px solid rgba(201,162,39,.45);
  display:flex;align-items:center;justify-content:center;font-size:2rem;
  box-shadow:0 0 40px rgba(76,175,128,.2);}
.login-brand h1{font-size:1.65rem;font-weight:900;}
.login-brand p{font-size:.82rem;opacity:.5;margin-top:3px;}
.login-card{background:#fff;border-radius:20px;padding:2.2rem;box-shadow:0 50px 100px rgba(0,0,0,.45);}
.login-card h2{text-align:center;font-size:1rem;color:var(--g900);font-weight:700;
  margin-bottom:1.7rem;padding-bottom:.9rem;border-bottom:1px solid var(--border);}
.field{margin-bottom:1rem;}
.field label{display:block;font-size:.78rem;color:var(--muted);margin-bottom:5px;font-weight:600;}
.field input,.field select{width:100%;padding:.72rem 1rem;border:1.5px solid var(--border);
  border-radius:var(--rs);font-family:inherit;font-size:.93rem;color:var(--text);background:var(--g050);transition:all .2s;}
.field input:focus,.field select:focus{outline:none;border-color:var(--g700);background:#fff;box-shadow:0 0 0 3px rgba(26,107,74,.1);}
.btn-login{width:100%;padding:.85rem;margin-top:.4rem;
  background:linear-gradient(135deg,var(--g700),var(--g600));color:#fff;border:none;
  border-radius:var(--rs);font-family:inherit;font-size:1rem;font-weight:800;cursor:pointer;transition:all .3s;}
.btn-login:hover{transform:translateY(-2px);box-shadow:0 10px 25px rgba(26,107,74,.4);}
.login-err{display:none;background:#fff5f5;border:1px solid #fed7d7;color:var(--danger);
  padding:.6rem 1rem;border-radius:var(--rs);font-size:.83rem;text-align:center;margin-top:.7rem;}
.login-hint{margin-top:1.1rem;padding:.75rem .9rem;background:var(--g100);
  border-radius:var(--rs);font-size:.75rem;color:var(--muted);line-height:1.7;}
.login-hint strong{color:var(--g700);display:block;margin-bottom:.2rem;}
code{background:#fff;padding:1px 6px;border-radius:4px;font-family:monospace;color:var(--g900);}

/* ── APP ── */
#app{display:none;min-height:100vh;}
.sidebar{position:fixed;right:0;top:0;width:var(--sidebar);height:100vh;
  background:var(--g900);color:#fff;display:flex;flex-direction:column;z-index:200;overflow-y:auto;}
.sidebar::before{content:'';position:absolute;inset:0;pointer-events:none;
  background-image:repeating-linear-gradient(45deg,rgba(255,255,255,.018) 0,rgba(255,255,255,.018) 1px,transparent 1px,transparent 22px);}
.sb-head{padding:1.3rem 1.1rem;border-bottom:1px solid rgba(255,255,255,.07);text-align:center;position:relative;}
.sb-logo{width:50px;height:50px;margin:0 auto .6rem;border-radius:50%;
  background:linear-gradient(135deg,var(--g700),var(--g600));border:1.5px solid rgba(201,162,39,.35);
  display:flex;align-items:center;justify-content:center;font-size:1.5rem;}
.sb-head h2{font-size:.83rem;font-weight:800;}
.sb-head p{font-size:.68rem;opacity:.45;margin-top:2px;}
.sb-user{padding:.8rem 1.1rem;background:rgba(255,255,255,.06);
  display:flex;align-items:center;gap:.6rem;border-bottom:1px solid rgba(255,255,255,.06);}
.sb-av{width:32px;height:32px;background:var(--g700);border-radius:50%;
  display:flex;align-items:center;justify-content:center;font-size:.95rem;flex-shrink:0;}
.sb-name{font-size:.8rem;font-weight:700;}
.sb-role{font-size:.68rem;opacity:.45;}
.sb-nav{padding:.6rem 0;flex:1;}
.nav-lbl{font-size:.62rem;letter-spacing:1px;opacity:.35;padding:.5rem 1.1rem .2rem;text-transform:uppercase;}
.nav-item{display:flex;align-items:center;gap:.6rem;padding:.6rem 1.1rem;
  cursor:pointer;font-size:.8rem;border-right:3px solid transparent;transition:all .15s;}
.nav-item:hover{background:rgba(255,255,255,.07);}
.nav-item.active{background:rgba(76,175,128,.15);border-right-color:var(--g400);font-weight:700;}
.nav-item .ni{font-size:.95rem;width:20px;text-align:center;flex-shrink:0;}
.nav-badge{margin-right:auto;background:rgba(201,162,39,.22);color:var(--gold);
  font-size:.62rem;font-weight:700;padding:2px 6px;border-radius:10px;}
.sb-foot{padding:.9rem 1.1rem;border-top:1px solid rgba(255,255,255,.07);}
.btn-logout{width:100%;padding:.55rem;background:rgba(255,255,255,.07);
  border:1px solid rgba(255,255,255,.1);color:rgba(255,255,255,.65);
  border-radius:var(--rs);cursor:pointer;font-family:inherit;font-size:.8rem;transition:all .2s;}
.btn-logout:hover{background:rgba(255,255,255,.12);color:#fff;}

.main{margin-right:var(--sidebar);min-height:100vh;}
.topbar{background:#fff;border-bottom:1px solid var(--border);padding:.85rem 1.8rem;
  display:flex;align-items:center;justify-content:space-between;position:sticky;top:0;z-index:100;}
.topbar h1{font-size:1.1rem;font-weight:800;color:var(--g900);}
.tb-right{display:flex;align-items:center;gap:.6rem;}
.period-pill{display:flex;align-items:center;gap:.3rem;background:var(--g100);
  border:1px solid var(--border);border-radius:20px;padding:.3rem .8rem;font-size:.8rem;}
.period-pill select{border:none;background:transparent;font-family:inherit;
  font-size:.8rem;color:var(--g700);font-weight:700;cursor:pointer;}
.tb-btn{padding:.35rem .8rem;border:1px solid var(--border);border-radius:20px;
  background:#fff;cursor:pointer;font-family:inherit;font-size:.77rem;
  color:var(--muted);transition:all .2s;}
.tb-btn:hover{background:var(--g100);color:var(--g700);border-color:var(--g600);}
.tb-btn.active{background:var(--g700);color:#fff;border-color:var(--g700);}
.content{padding:1.6rem 1.8rem;}

/* VIEW MODE TABS */
.view-tabs{display:flex;gap:.4rem;background:var(--g100);border-radius:20px;padding:3px;
  border:1px solid var(--border);margin-left:.5rem;}
.vtab{padding:.3rem .75rem;border-radius:16px;cursor:pointer;font-size:.77rem;
  font-weight:600;color:var(--muted);transition:all .2s;border:none;background:transparent;font-family:inherit;}
.vtab.on{background:var(--g700);color:#fff;}

/* STATS */
.stats-row{display:grid;grid-template-columns:repeat(4,1fr);gap:.9rem;margin-bottom:1.6rem;}
.stat-card{background:#fff;border-radius:var(--r);padding:1.2rem 1.3rem;
  box-shadow:var(--shadow);border:1px solid var(--border);
  position:relative;overflow:hidden;cursor:pointer;transition:all .2s;}
.stat-card::before{content:'';position:absolute;top:0;left:0;right:0;height:3px;background:var(--sc,var(--g700));}
.stat-card:hover{transform:translateY(-2px);box-shadow:0 8px 20px rgba(10,61,34,.13);}
.stat-card .si{font-size:1.6rem;margin-bottom:.5rem;}
.stat-card .sv{font-size:1.9rem;font-weight:900;color:var(--g900);line-height:1;}
.stat-card .sl{font-size:.74rem;color:var(--muted);margin-top:.25rem;}
.stat-card .sc-hint{font-size:.68rem;color:var(--g600);margin-top:.3rem;opacity:.8;}

.sec-title{font-size:.95rem;font-weight:800;color:var(--g900);
  margin-bottom:.9rem;display:flex;align-items:center;gap:.5rem;}
.sec-title::before{content:'';width:4px;height:16px;
  background:linear-gradient(180deg,var(--g700),var(--g400));border-radius:2px;}

/* DEPT CARDS */
.dept-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(248px,1fr));gap:.9rem;margin-bottom:1.8rem;}
.dept-card{background:#fff;border-radius:var(--r);padding:1.3rem;
  box-shadow:var(--shadow);border:1px solid var(--border);cursor:pointer;transition:all .22s;position:relative;}
.dept-card:hover{transform:translateY(-3px);box-shadow:0 14px 32px rgba(10,61,34,.13);border-color:var(--g600);}
.dept-card .di{font-size:1.9rem;margin-bottom:.7rem;}
.dept-card .dn{font-size:.88rem;font-weight:700;color:var(--g900);margin-bottom:.25rem;}
.dept-card .dc{font-size:.74rem;color:var(--muted);margin-bottom:.9rem;}
.perf-row{display:flex;align-items:center;gap:.5rem;}
.perf-bar{flex:1;height:6px;background:#e2e8f0;border-radius:3px;overflow:hidden;}
.perf-fill{height:100%;border-radius:3px;transition:width .6s ease;}
.perf-pct{font-size:.75rem;font-weight:700;min-width:38px;}

/* DEADLINE BADGE on dept card */
.dl-badge{position:absolute;top:.8rem;left:.8rem;padding:2px 8px;border-radius:10px;
  font-size:.68rem;font-weight:700;display:flex;align-items:center;gap:3px;}
.dl-ok{background:#f0fff4;color:var(--ok);}
.dl-warn{background:#fffbeb;color:var(--warn);}
.dl-over{background:#fff5f5;color:var(--danger);animation:pulse 1.5s infinite;}
@keyframes pulse{0%,100%{opacity:1}50%{opacity:.6}}

/* CHARTS */
.charts-row{display:grid;grid-template-columns:1fr 2fr;gap:.9rem;margin-bottom:1.6rem;}
.chart-card{background:#fff;border-radius:var(--r);padding:1.3rem;box-shadow:var(--shadow);border:1px solid var(--border);}
.chart-card h3{font-size:.87rem;font-weight:700;color:var(--g900);margin-bottom:.9rem;
  padding-bottom:.65rem;border-bottom:1px solid var(--border);}

/* DEPT HERO */
.dept-hero{background:linear-gradient(135deg,var(--g900),var(--g700));
  color:#fff;border-radius:var(--r);padding:1.4rem 1.7rem;margin-bottom:1.4rem;
  display:flex;align-items:center;gap:1rem;position:relative;overflow:hidden;}
.dept-hero::after{content:'';position:absolute;inset:0;
  background-image:repeating-linear-gradient(-45deg,rgba(255,255,255,.025) 0,rgba(255,255,255,.025) 1px,transparent 1px,transparent 18px);}
.dh-icon{font-size:2.4rem;flex-shrink:0;position:relative;z-index:1;}
.dh-text{position:relative;z-index:1;}
.dh-text h2{font-size:1.15rem;font-weight:800;}
.dh-text p{font-size:.79rem;opacity:.65;margin-top:2px;}
.dh-stat{margin-right:auto;position:relative;z-index:1;text-align:center;}
.dh-stat .dsv{font-size:2rem;font-weight:900;color:var(--gold);}
.dh-stat .dsl{font-size:.72rem;opacity:.6;}

/* DEPT DEADLINE DISPLAY */
.dept-dl-strip{display:flex;align-items:center;justify-content:space-between;
  background:#fff;border-radius:var(--rs);padding:.6rem 1rem;
  margin-bottom:1.2rem;border:1px solid var(--border);box-shadow:var(--shadow);}
.dl-info{display:flex;align-items:center;gap:.6rem;font-size:.8rem;}
.dl-countdown{font-size:.85rem;font-weight:700;}
.dl-countdown.green{color:var(--ok);}
.dl-countdown.yellow{color:var(--warn);}
.dl-countdown.red{color:var(--danger);}

/* SUMMARY ROW */
.summary-row{display:grid;grid-template-columns:repeat(3,1fr);gap:.9rem;margin-bottom:1.4rem;}
.sum-card{background:#fff;border-radius:var(--r);padding:1rem 1.2rem;
  box-shadow:var(--shadow);border:1px solid var(--border);display:flex;align-items:center;gap:.8rem;}
.sum-card .sc-icon{font-size:1.5rem;}
.sum-card .sc-v{font-size:1.5rem;font-weight:900;color:var(--g900);}
.sum-card .sc-l{font-size:.74rem;color:var(--muted);}

/* PERIOD VIEW SWITCHER (dept) */
.period-view-bar{display:flex;align-items:center;justify-content:space-between;margin-bottom:1rem;}
.period-view-tabs{display:flex;gap:.3rem;background:#fff;border-radius:20px;
  padding:3px;border:1px solid var(--border);box-shadow:var(--shadow);}
.pvtab{padding:.3rem .85rem;border-radius:16px;cursor:pointer;font-size:.78rem;
  font-weight:600;color:var(--muted);transition:all .2s;border:none;background:transparent;font-family:inherit;}
.pvtab.on{background:var(--g700);color:#fff;}

/* KPI CARD */
.kpi-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(340px,1fr));gap:1rem;}
.kpi-card{background:#fff;border-radius:var(--r);box-shadow:var(--shadow);
  border:1px solid var(--border);overflow:hidden;display:flex;flex-direction:column;}
.kpi-head{padding:1rem 1.1rem .8rem;border-bottom:1px solid var(--border);}
.kpi-name-row{display:flex;align-items:flex-start;gap:.5rem;margin-bottom:.6rem;}
.kstatus{width:10px;height:10px;border-radius:50%;flex-shrink:0;margin-top:4px;}
.s-green{background:#38a169;box-shadow:0 0 0 3px rgba(56,161,105,.15);}
.s-yellow{background:#d69e2e;box-shadow:0 0 0 3px rgba(214,158,46,.15);}
.s-red{background:#e53e3e;box-shadow:0 0 0 3px rgba(229,62,62,.15);}
.s-gray{background:#a0aec0;}
.kpi-name{font-size:.87rem;font-weight:700;color:var(--text);line-height:1.45;flex:1;}
.kpi-actions{display:flex;gap:.3rem;align-items:center;}
.kpi-edit-btn{width:26px;height:26px;border-radius:6px;border:1px solid var(--border);
  background:var(--g050);cursor:pointer;display:flex;align-items:center;justify-content:center;
  font-size:.8rem;transition:all .2s;flex-shrink:0;}
.kpi-edit-btn:hover{background:var(--g100);border-color:var(--g700);}

.kpi-big-num{font-size:2.4rem;font-weight:900;color:var(--g900);line-height:1;margin-bottom:.35rem;}
.kpi-big-num .ku{font-size:.9rem;font-weight:400;color:var(--muted);}
.kpi-big-num.no-data{font-size:1rem;color:#a0aec0;font-weight:500;}
.tag-row{display:flex;gap:.4rem;flex-wrap:wrap;margin-bottom:.7rem;}
.tag{display:inline-block;padding:2px 8px;border-radius:12px;font-size:.7rem;font-weight:600;}
.tm{background:#ebf8ff;color:#2b6cb0;}.tq{background:#f0f0ff;color:#553c9a;}
.ty{background:#f0fff4;color:#276749;}
.tt{background:var(--g100);color:var(--g700);}.tl{background:#fff5f5;color:var(--danger);}
.tn{background:var(--gold-bg);color:#92681a;}
.kpi-prog{height:8px;background:#edf2f7;border-radius:4px;overflow:hidden;margin-bottom:.2rem;}
.kpi-prog-fill{height:100%;border-radius:4px;transition:width .7s ease;}
.kpi-prog-lbl{display:flex;justify-content:space-between;font-size:.68rem;color:var(--muted);}
.kpi-formula{padding:.5rem .8rem;background:var(--g050);
  border-top:1px dashed var(--border);font-size:.72rem;color:var(--muted);line-height:1.5;}
.kpi-formula strong{color:var(--g700);}

/* INPUTS */
.kpi-inputs{padding:.9rem 1.1rem;border-top:1px solid var(--border);background:var(--g050);}
.inp-period{font-size:.73rem;font-weight:700;color:var(--g700);margin-bottom:.6rem;}
.inp-grid{display:grid;gap:.5rem;margin-bottom:.6rem;}
.inp-grid.two{grid-template-columns:1fr 1fr;}
.inp-grid.one{grid-template-columns:1fr;}
.inp-group{display:flex;flex-direction:column;gap:3px;}
.inp-group label{font-size:.7rem;color:var(--muted);font-weight:500;}
.inp-group input{padding:.5rem .7rem;border:1.5px solid var(--border);
  border-radius:var(--rs);font-family:inherit;font-size:.95rem;
  text-align:center;color:var(--text);background:#fff;font-weight:700;transition:border-color .2s;}
.inp-group input:focus{outline:none;border-color:var(--g700);box-shadow:0 0 0 2px rgba(26,107,74,.08);}
.inp-group input::placeholder{font-size:.8rem;font-weight:400;color:#c0c8c4;}
.calc-box{background:#fff;border:1.5px solid var(--g200);border-radius:var(--rs);
  padding:.5rem .8rem;margin-bottom:.6rem;display:flex;align-items:center;justify-content:space-between;}
.calc-box .cl{font-size:.72rem;color:var(--muted);}
.calc-box .cv{font-size:1.25rem;font-weight:900;}
.cv-g{color:var(--ok);}.cv-y{color:var(--warn);}.cv-r{color:var(--danger);}.cv-x{color:var(--muted);}
.save-row{display:flex;gap:.5rem;}
.btn-save{flex:1;padding:.52rem;background:var(--g700);color:#fff;border:none;
  border-radius:var(--rs);cursor:pointer;font-family:inherit;font-size:.82rem;font-weight:700;transition:all .2s;}
.btn-save:hover{background:var(--g800);}
.btn-sm{padding:.52rem .8rem;background:#fff;color:var(--muted);
  border:1.5px solid var(--border);border-radius:var(--rs);cursor:pointer;
  font-family:inherit;font-size:.78rem;transition:all .2s;white-space:nowrap;}
.btn-sm:hover{border-color:var(--g700);color:var(--g700);}

/* FILE ATTACH */
.attach-strip{border-top:1px solid var(--border);padding:.6rem 1.1rem;background:#fff;}
.attach-header{display:flex;align-items:center;justify-content:space-between;margin-bottom:.4rem;}
.attach-header span{font-size:.72rem;color:var(--muted);font-weight:600;}
.attach-btn{display:inline-flex;align-items:center;gap:.3rem;padding:.3rem .7rem;
  background:var(--g050);border:1.5px dashed var(--border);border-radius:6px;
  cursor:pointer;font-size:.75rem;color:var(--g700);font-weight:600;transition:all .2s;}
.attach-btn:hover{background:var(--g100);border-color:var(--g700);}
.attach-list{display:flex;flex-direction:column;gap:.3rem;}
.attach-file{display:flex;align-items:center;justify-content:space-between;
  padding:.35rem .6rem;background:var(--g050);border-radius:6px;border:1px solid var(--border);}
.attach-file .af-name{font-size:.73rem;color:var(--g700);font-weight:600;cursor:pointer;text-decoration:underline;}
.attach-file .af-del{cursor:pointer;color:var(--danger);font-size:.8rem;background:none;border:none;}

/* TABLE */
.tbl-wrap{background:#fff;border-radius:var(--r);border:1px solid var(--border);
  box-shadow:var(--shadow);overflow:hidden;margin-bottom:1.5rem;}
.tbl{width:100%;border-collapse:collapse;font-size:.8rem;}
.tbl th{background:var(--g100);color:var(--g700);padding:.65rem .9rem;
  text-align:right;font-weight:700;border-bottom:1.5px solid var(--border);}
.tbl td{padding:.6rem .9rem;border-bottom:1px solid var(--border);}
.tbl tbody tr:hover td{background:var(--g050);}
.tbl tbody tr:last-child td{border-bottom:none;}

/* SETTINGS PAGE */
.settings-section{background:#fff;border-radius:var(--r);padding:1.4rem;
  box-shadow:var(--shadow);border:1px solid var(--border);margin-bottom:1.2rem;}
.settings-section h3{font-size:.9rem;font-weight:700;color:var(--g900);
  margin-bottom:1rem;padding-bottom:.6rem;border-bottom:1px solid var(--border);}
.settings-row{display:grid;grid-template-columns:repeat(auto-fill,minmax(280px,1fr));gap:.8rem;}
.settings-item{background:var(--g050);border-radius:var(--rs);padding:.8rem;border:1px solid var(--border);}
.settings-item .si-name{font-size:.8rem;font-weight:700;color:var(--g900);margin-bottom:.6rem;}
.settings-item .si-fields{display:grid;grid-template-columns:1fr 1fr;gap:.4rem;}
.settings-item label{font-size:.68rem;color:var(--muted);display:block;margin-bottom:2px;}
.settings-item input,.settings-item select{width:100%;padding:.38rem .5rem;
  border:1.5px solid var(--border);border-radius:5px;font-family:inherit;font-size:.82rem;
  color:var(--text);background:#fff;transition:border-color .2s;}
.settings-item input:focus,.settings-item select:focus{outline:none;border-color:var(--g700);}
.btn-settings-save{margin-top:1rem;padding:.6rem 1.4rem;background:var(--g700);color:#fff;
  border:none;border-radius:var(--rs);cursor:pointer;font-family:inherit;
  font-size:.85rem;font-weight:700;transition:all .2s;}
.btn-settings-save:hover{background:var(--g800);}

/* DEADLINE SETTINGS */
.dl-settings-row{display:grid;grid-template-columns:repeat(auto-fill,minmax(260px,1fr));gap:.8rem;}
.dl-item{background:var(--g050);border-radius:var(--rs);padding:.8rem;border:1px solid var(--border);}
.dl-item h4{font-size:.8rem;font-weight:700;margin-bottom:.6rem;color:var(--g900);}
.dl-fields{display:grid;grid-template-columns:1fr 1fr;gap:.4rem;}
.dl-fields label{font-size:.68rem;color:var(--muted);}
.dl-fields input,.dl-fields select{width:100%;padding:.38rem .5rem;border:1.5px solid var(--border);
  border-radius:5px;font-family:inherit;font-size:.82rem;background:#fff;}
.dl-fields input:focus,.dl-fields select:focus{outline:none;border-color:var(--g700);}

/* MODAL */
.modal-overlay{display:none;position:fixed;inset:0;background:rgba(0,0,0,.55);
  z-index:500;align-items:center;justify-content:center;}
.modal-overlay.open{display:flex;}
.modal{background:#fff;border-radius:18px;width:700px;max-width:96vw;
  max-height:90vh;overflow-y:auto;box-shadow:0 50px 100px rgba(0,0,0,.35);
  animation:popIn .28s ease;}
.modal.sm{width:460px;}
@keyframes popIn{from{opacity:0;transform:scale(.9)}to{opacity:1;transform:scale(1)}}
.modal-header{padding:1.2rem 1.5rem;border-bottom:1px solid var(--border);
  display:flex;justify-content:space-between;align-items:center;
  position:sticky;top:0;background:#fff;border-radius:18px 18px 0 0;z-index:1;}
.modal-header h2{font-size:.97rem;color:var(--g900);line-height:1.45;flex:1;font-weight:800;}
.btn-close{width:29px;height:29px;border-radius:50%;border:none;background:var(--g100);
  cursor:pointer;font-size:1rem;display:flex;align-items:center;justify-content:center;
  flex-shrink:0;margin-right:.7rem;transition:background .2s;}
.btn-close:hover{background:var(--border);}
.modal-body{padding:1.3rem 1.5rem;}
.info-grid{display:grid;grid-template-columns:1fr 1fr;gap:.6rem;margin-bottom:1.1rem;}
.info-item{background:var(--g050);border-radius:8px;padding:.65rem .85rem;}
.info-item .il{font-size:.69rem;color:var(--muted);margin-bottom:2px;}
.info-item .iv{font-size:.87rem;font-weight:700;color:var(--g900);}
.formula-box{background:var(--g050);border:1px solid var(--border);border-radius:8px;
  padding:.8rem 1rem;margin-bottom:1.1rem;font-size:.78rem;color:var(--muted);line-height:1.6;}
.formula-box strong{color:var(--g700);}
.hist-title{font-size:.83rem;font-weight:700;color:var(--g900);margin-bottom:.65rem;}
.modal-ch-wrap{height:175px;margin-bottom:1.1rem;}
.hist-tbl{width:100%;border-collapse:collapse;font-size:.8rem;}
.hist-tbl th{background:var(--g100);color:var(--g700);padding:.5rem .8rem;
  text-align:right;font-weight:700;border-bottom:1.5px solid var(--border);}
.hist-tbl td{padding:.5rem .8rem;border-bottom:1px solid var(--border);}
.hist-tbl tr:last-child td{border-bottom:none;}
.hist-tbl tr:hover td{background:var(--g050);}

/* EDIT KPI MODAL */
.edit-field{margin-bottom:.8rem;}
.edit-field label{display:block;font-size:.78rem;color:var(--muted);margin-bottom:4px;font-weight:600;}
.edit-field input,.edit-field select{width:100%;padding:.62rem .8rem;border:1.5px solid var(--border);
  border-radius:var(--rs);font-family:inherit;font-size:.88rem;color:var(--text);background:var(--g050);transition:all .2s;}
.edit-field input:focus,.edit-field select:focus{outline:none;border-color:var(--g700);background:#fff;}

/* STAT MODAL */
.stat-modal-list{display:flex;flex-direction:column;gap:.5rem;}
.stat-modal-item{display:flex;align-items:center;justify-content:space-between;
  padding:.6rem .9rem;background:var(--g050);border-radius:8px;border:1px solid var(--border);}
.stat-modal-item .smi-dept{font-size:.8rem;font-weight:700;color:var(--g900);}
.stat-modal-item .smi-kpi{font-size:.73rem;color:var(--muted);margin-top:1px;}
.stat-modal-item .smi-val{font-size:.95rem;font-weight:900;}
.smi-green{color:var(--ok);}
.smi-yellow{color:var(--warn);}
.smi-red{color:var(--danger);}
.smi-gray{color:var(--muted);}

/* ANNUAL VIEW */
.annual-kpi-wrap{background:#fff;border-radius:var(--r);padding:1.2rem;
  box-shadow:var(--shadow);border:1px solid var(--border);margin-bottom:1rem;}
.annual-kpi-name{font-size:.88rem;font-weight:700;color:var(--g900);margin-bottom:.8rem;}
.annual-months-grid{display:grid;grid-template-columns:repeat(6,1fr);gap:.3rem;}
.amcell{background:var(--g050);border-radius:6px;padding:.4rem .3rem;text-align:center;border:1px solid var(--border);}
.amcell .am-lbl{font-size:.6rem;color:var(--muted);}
.amcell .am-val{font-size:.82rem;font-weight:700;color:var(--g900);}
.amcell.green{background:#f0fff4;border-color:#9ae6b4;}
.amcell.yellow{background:#fffbeb;border-color:#faf089;}
.amcell.red{background:#fff5f5;border-color:#fed7d7;}
.amcell.gray{background:var(--g050);}

/* NOTIF */
.notif{position:fixed;bottom:2rem;left:2rem;background:var(--g700);color:#fff;
  padding:.75rem 1.3rem;border-radius:12px;font-size:.86rem;font-weight:600;
  box-shadow:0 8px 24px rgba(0,0,0,.2);z-index:1000;
  transform:translateY(80px);opacity:0;transition:all .35s cubic-bezier(.34,1.56,.64,1);}
.notif.show{transform:translateY(0);opacity:1;}
</style>
</head>
<body>

<!-- LOGIN -->
<div id="login-page">
  <div class="lp-grid"></div><div class="lp-glow"></div><div class="lp-glow2"></div>
  <div class="login-box">
    <div class="login-brand">
      <div class="lb-seal">🏛️</div>
      <h1>بلدية الخرج</h1><p>منظومة الخطة التشغيلية 2026م</p>
    </div>
    <div class="login-card">
      <h2>🔐 تسجيل الدخول</h2>
      <div class="field"><label>الجهة / الوكالة</label>
        <select id="user-sel">
          <option value="">-- اختر --</option>
          <option value="admin">مدير النظام — إدارة الجودة</option>
          <option value="branches">وكالة الفروع والمراكز</option>
          <option value="urban">وكالة التعمير والتنمية الحضرية</option>
          <option value="compliance">وكالة الامتثال والاستدامة البيئية</option>
          <option value="projects">وكالة المشاريع</option>
          <option value="investment">وكالة الاستثمار والتخصيص</option>
          <option value="services">وكالة الخدمات المؤسسية</option>
          <option value="emergency">الإدارة العامة للطوارئ والكوارث</option>
          <option value="excellence">وكالة التميز المؤسسي والتحول الرقمي</option>
          <option value="communication">الإدارة العامة للاتصال المؤسسي</option>
          <option value="safety">الإدارة العامة للأمن والسلامة</option>
          <option value="executive">المكتب التنفيذي</option>
        </select>
      </div>
      <div class="field"><label>كلمة المرور</label>
        <input type="password" id="pass-in" placeholder="أدخل كلمة المرور">
      </div>
      <button class="btn-login" onclick="doLogin()">دخول ←</button>
      <div class="login-err" id="login-err">⚠ بيانات الدخول غير صحيحة</div>
      <div class="login-hint">
        <strong>🔑 بيانات تجريبية</strong>
        المدير: <code>admin2026</code> &nbsp;|&nbsp; الوكالات: <code>[id]2026</code> مثال: <code>branches2026</code>
      </div>
    </div>
  </div>
</div>

<!-- APP -->
<div id="app">
  <aside class="sidebar">
    <div class="sb-head"><div class="sb-logo">🏛️</div><h2>بلدية الخرج</h2><p>الخطة التشغيلية 2026م</p></div>
    <div class="sb-user">
      <div class="sb-av" id="sb-av">👤</div>
      <div><div class="sb-name" id="sb-name">-</div><div class="sb-role" id="sb-role">-</div></div>
    </div>
    <nav class="sb-nav" id="sb-nav"></nav>
    <div class="sb-foot"><button class="btn-logout" onclick="doLogout()">⬅ تسجيل الخروج</button></div>
  </aside>
  <main class="main">
    <header class="topbar">
      <h1 id="pg-title">لوحة التحكم</h1>
      <div class="tb-right">
        <div class="view-tabs">
          <button class="vtab on" onclick="setViewMode('m',this)">شهري</button>
          <button class="vtab" onclick="setViewMode('q',this)">ربع سنوي</button>
          <button class="vtab" onclick="setViewMode('y',this)">سنوي</button>
        </div>
        <div class="period-pill">📅<select id="period-sel" onchange="onPeriodChange()"></select></div>
        <button class="tb-btn" onclick="window.print()">🖨️ طباعة</button>
        <button class="tb-btn" onclick="seedDemo()">📊 بيانات تجريبية</button>
      </div>
    </header>
    <div class="content" id="content"></div>
  </main>
</div>

<!-- MODAL OVERLAY -->
<div class="modal-overlay" id="modal-ov" onclick="if(event.target===this)closeModal()">
  <div class="modal" id="modal">
    <div class="modal-header"><h2 id="modal-title">-</h2><button class="btn-close" onclick="closeModal()">✕</button></div>
    <div class="modal-body" id="modal-body"></div>
  </div>
</div>

<div class="notif" id="notif">✅ تم الحفظ</div>

<script>
// ═══════════════ CONSTANTS ═══════════════
const Mo=['يناير','فبراير','مارس','أبريل','مايو','يونيو','يوليو','أغسطس','سبتمبر','أكتوبر','نوفمبر','ديسمبر'];
const Qr=['الربع الأول','الربع الثاني','الربع الثالث','الربع الرابع'];

const USERS={
  admin:       {name:'مدير النظام',       icon:'👨‍💼',role:'إدارة الجودة',              pass:'admin2026',        isAdmin:true},
  branches:    {name:'وكالة الفروع',      icon:'🏘️', role:'وكالة الفروع والمراكز',     pass:'branches2026',     isAdmin:false},
  urban:       {name:'وكالة التعمير',     icon:'🏗️', role:'وكالة التعمير',             pass:'urban2026',        isAdmin:false},
  compliance:  {name:'وكالة الامتثال',    icon:'🌿', role:'وكالة الامتثال',            pass:'compliance2026',   isAdmin:false},
  projects:    {name:'وكالة المشاريع',    icon:'🔧', role:'وكالة المشاريع',            pass:'projects2026',     isAdmin:false},
  investment:  {name:'وكالة الاستثمار',   icon:'💰', role:'وكالة الاستثمار',           pass:'investment2026',   isAdmin:false},
  services:    {name:'وكالة الخدمات',     icon:'📋', role:'وكالة الخدمات المؤسسية',    pass:'services2026',     isAdmin:false},
  emergency:   {name:'إدارة الطوارئ',     icon:'🚨', role:'الطوارئ والكوارث',          pass:'emergency2026',    isAdmin:false},
  excellence:  {name:'وكالة التميز',      icon:'💡', role:'التميز والتحول الرقمي',     pass:'excellence2026',   isAdmin:false},
  communication:{name:'إدارة الاتصال',   icon:'📢', role:'الاتصال المؤسسي',           pass:'communication2026',isAdmin:false},
  safety:      {name:'إدارة الأمن',      icon:'🛡️', role:'الأمن والسلامة',            pass:'safety2026',       isAdmin:false},
  executive:   {name:'المكتب التنفيذي',  icon:'🏢', role:'المكتب التنفيذي',           pass:'executive2026',    isAdmin:false},
};

// Base KPI definitions — p: 'm'=monthly, 'q'=quarterly
const BASE_DEPTS=[
{id:'branches',name:'وكالة الفروع والمراكز',icon:'🏘️',kpis:[
  {id:'nasifa', name:'نسبة جولات الرقابة — فرع الناصفة', target:80,p:'m',num:'عدد الجولات المنفذة',   den:'عدد الجولات المخططة',  src:'تقرير العمليات الرقابية',f:'الجولات المنفذة ÷ الجولات المخططة × 100'},
  {id:'uyun',   name:'نسبة جولات الرقابة — فرع العيون',  target:80,p:'m',num:'عدد الجولات المنفذة',   den:'عدد الجولات المخططة',  src:'تقرير العمليات الرقابية',f:'الجولات المنفذة ÷ الجولات المخططة × 100'},
  {id:'yamamah',name:'نسبة جولات الرقابة — فرع اليمامة',target:80,p:'m',num:'عدد الجولات المنفذة',   den:'عدد الجولات المخططة',  src:'تقرير العمليات الرقابية',f:'الجولات المنفذة ÷ الجولات المخططة × 100'},
  {id:'tuwaiq', name:'نسبة جولات الرقابة — فرع طويق',   target:80,p:'m',num:'عدد الجولات المنفذة',   den:'عدد الجولات المخططة',  src:'تقرير العمليات الرقابية',f:'الجولات المنفذة ÷ الجولات المخططة × 100'},
  {id:'saih',   name:'نسبة جولات الرقابة — فرع السيح',  target:80,p:'m',num:'عدد الجولات المنفذة',   den:'عدد الجولات المخططة',  src:'تقرير العمليات الرقابية',f:'الجولات المنفذة ÷ الجولات المخططة × 100'},
]},
{id:'urban',name:'وكالة التعمير والتنمية الحضرية',icon:'🏗️',kpis:[
  {id:'tech_lic',  name:'نسبة طلبات التراخيص الفنية المنجزة',                  target:100,p:'m',num:'عدد التراخيص المنجزة',      den:'إجمالي طلبات التراخيص',  src:'أنظمة الأمانة',          f:'التراخيص المنجزة ÷ إجمالي الطلبات × 100'},
  {id:'comp_cert', name:'نسبة طلبات شهادات إتمام البناء المنجزة',              target:100,p:'m',num:'عدد الشهادات المنجزة',      den:'إجمالي طلبات الشهادات',  src:'أنظمة الأمانة',          f:'الشهادات المنجزة ÷ إجمالي الطلبات × 100'},
  {id:'tech_tour', name:'نسبة جولات الرقابة الفنية المنجزة',                   target:80, p:'m',num:'عدد الجولات المنفذة',       den:'عدد الجولات المخططة',    src:'تقرير العمليات الرقابية',f:'الجولات المنفذة ÷ الجولات المخططة × 100'},
  {id:'land_tour', name:'نسبة جولات رقابة الأراضي المنجزة',                    target:80, p:'m',num:'عدد الجولات المنفذة',       den:'عدد الجولات المخططة',    src:'تقرير العمليات الرقابية',f:'الجولات المنفذة ÷ الجولات المخططة × 100'},
  {id:'survey',    name:'نسبة تنفيذ طلبات المساحة',                            target:100,p:'m',num:'عدد الطلبات المنجزة',       den:'إجمالي الطلبات',          src:'تقرير',                  f:'الطلبات المنجزة ÷ إجمالي الطلبات × 100'},
  {id:'land_plan', name:'نسبة مخططات تقسيمات الأراضي في الوقت المحدد (60 يوم)',target:null,p:'q',num:'الطلبات المنجزة < 60 يوم',den:'إجمالي الطلبات المنجزة',  src:'تقرير',                  f:'الطلبات < 60 يوم ÷ إجمالي الطلبات × 100'},
]},
{id:'compliance',name:'وكالة الامتثال والاستدامة البيئية',icon:'🌿',kpis:[
  {id:'prof_lic',   name:'نسبة طلبات التراخيص المهنية المنجزة',               target:100,p:'m',num:'عدد التراخيص المنجزة',       den:'إجمالي طلبات التراخيص',    src:'نظام بلدي',              f:'التراخيص المنجزة ÷ إجمالي الطلبات × 100'},
  {id:'health_cert',name:'نسبة طلبات الشهادات الصحية المنجزة',                target:100,p:'m',num:'عدد الشهادات المنجزة',       den:'إجمالي طلبات الشهادات',    src:'نظام بلدي',              f:'الشهادات المنجزة ÷ إجمالي الطلبات × 100'},
  {id:'health_tour',name:'نسبة جولات الرقابة الصحية المنجزة',                 target:80, p:'m',num:'عدد الجولات المنفذة',        den:'عدد الجولات المخططة',      src:'تقرير العمليات الرقابية',f:'الجولات المنفذة ÷ الجولات المخططة × 100'},
  {id:'clean_tour', name:'نسبة جولات مراقبي النظافة المنجزة',                 target:80, p:'m',num:'عدد الجولات المنفذة',        den:'عدد الجولات المخططة',      src:'تقرير العمليات الرقابية',f:'الجولات المنفذة ÷ الجولات المخططة × 100'},
  {id:'road_clean', name:'نسبة نظافة الطرق',                                  target:null,p:'m',num:'مسافة الطرق المكنوسة (كم)', den:'إجمالي الطرق المستهدفة (كم)',src:'تقرير',                f:'مسافة الطرق المكنوسة ÷ الطرق المستهدفة × 100'},
  {id:'sidewalks',  name:'نسبة الأرصفة والممرات المغسولة',                    target:null,p:'m',num:'مساحة الأرصفة المغسولة (م²)',den:'الأرصفة المستهدفة (م²)',   src:'تقرير',                  f:'الأرصفة المغسولة ÷ الأرصفة المستهدفة × 100'},
  {id:'stray_dogs', name:'نسبة السيطرة على انتشار الكلاب الضالة',             target:null,p:'m',num:'المواقع المسيطر عليها',      den:'إجمالي مواقع الانتشار',    src:'تقرير',                  f:'المواقع المسيطر عليها ÷ إجمالي مواقع الانتشار × 100'},
]},
{id:'projects',name:'وكالة المشاريع',icon:'🔧',kpis:[
  {id:'proj_comp', name:'نسبة الإنجاز في المشاريع',                            target:null,p:'q',num:'المراحل المنجزة',              den:'إجمالي المراحل المخططة',  src:'تقرير',f:'المراحل المنجزة ÷ المراحل المخططة × 100'},
  {id:'road_maint',name:'نسبة تنفيذ الصيانة الوقائية للطرق',                   target:null,p:'q',num:'عدد الطرق المصانة',            den:'إجمالي المخطط له',        src:'تقرير',f:'الطرق المصانة ÷ إجمالي المخطط له × 100'},
  {id:'potholes',  name:'نسبة معالجة الحفر والهبوط',                           target:null,p:'q',num:'الحفر والهبوط المعالجة',       den:'إجمالي المرصود',          src:'تقرير',f:'الحفر المعالجة ÷ إجمالي المرصود × 100'},
  {id:'lighting',  name:'نسبة الإنارة المصانة',                                target:null,p:'q',num:'عدد الإنارات المصانة',         den:'إجمالي المرصود',          src:'تقرير',f:'الإنارات المصانة ÷ إجمالي المرصود × 100'},
  {id:'drainage',  name:'نسبة صيانة شبكات تصريف الأمطار ومجاري السيول',       target:null,p:'q',num:'عدد الشبكات المصانة',          den:'إجمالي المخطط له',        src:'تقرير',f:'الشبكات المصانة ÷ إجمالي المخطط له × 100'},
  {id:'green',     name:'نسبة زيادة المسطحات الخضراء بالمحافظة',               target:null,p:'q',num:'المساحة المزروعة (م²)',        den:'المستهدف زراعتها (م²)',   src:'تقرير',f:'المزروعة ÷ المستهدفة × 100'},
  {id:'trees',     name:'نسبة زيادة التشجير بالمحافظة',                        target:null,p:'q',num:'عدد الأشجار المزروعة',         den:'الأشجار المستهدفة',       src:'تقرير',f:'الأشجار المزروعة ÷ الأشجار المستهدفة × 100'},
]},
{id:'investment',name:'وكالة الاستثمار والتخصيص',icon:'💰',kpis:[
  {id:'inv_rev',name:'نسبة النمو بالإيرادات الاستثمارية',target:null,p:'q',num:'إيرادات الفترة الحالية (ريال)',den:'إيرادات نفس الفترة من العام الماضي (ريال)',src:'أنظمة الأمانة',f:'إيرادات الفترة ÷ إيرادات نفس الفترة العام الماضي × 100'},
]},
{id:'services',name:'وكالة الخدمات المؤسسية',icon:'📋',kpis:[
  {id:'revenues',    name:'نسبة الإيرادات المحصلة',                            target:null,p:'m',num:'مبالغ الإيرادات المحصلة (ريال)',   den:'مبالغ الفواتير المصدرة (ريال)',      src:'أنظمة الأمانة',f:'الإيرادات المحصلة ÷ الفواتير المصدرة × 100'},
  {id:'budget_plan', name:'نسبة الالتزام بخطة الصرف من الميزانية المعتمدة',   target:null,p:'q',num:'إجمالي الصرف الفعلي (ريال)',       den:'الميزانية المعتمدة (ريال)',           src:'تقرير',         f:'الصرف الفعلي ÷ الميزانية المعتمدة × 100'},
  {id:'budget_spend',name:'نسبة الصرف في الميزانية',                           target:null,p:'q',num:'الصرف خلال الفترة (ريال)',         den:'إجمالي الميزانية (ريال)',             src:'تقرير',         f:'الصرف خلال الفترة ÷ إجمالي الميزانية × 100'},
  {id:'equipment',   name:'نسبة المعدات التي تعمل',                            target:null,p:'q',num:'عدد المعدات التي تعمل',            den:'إجمالي معدات البلدية',               src:'تقرير',         f:'المعدات التي تعمل ÷ إجمالي المعدات × 100'},
  {id:'volunteers',  name:'عدد المتطوعين',                                     target:null,p:'q',num:'عدد المتطوعين المشاركين',          den:null,isCount:true,                    src:'تقرير',         f:'مجموع المتطوعين المشاركين خلال الفترة'},
  {id:'training',    name:'نسبة تنفيذ خطط الدورات التدريبية',                 target:null,p:'q',num:'عدد الدورات المقامة',              den:'إجمالي الدورات المستهدفة',           src:'تقرير',         f:'الدورات المقامة ÷ الدورات المستهدفة × 100'},
  {id:'workshops',   name:'نسبة تنفيذ خطط ورش العمل',                         target:null,p:'q',num:'عدد ورش العمل المقامة',            den:'إجمالي ورش العمل المستهدفة',         src:'تقرير',         f:'ورش العمل المقامة ÷ الورش المستهدفة × 100'},
]},
{id:'emergency',name:'الإدارة العامة للطوارئ والكوارث',icon:'🚨',kpis:[
  {id:'rep_done',    name:'نسبة تنفيذ البلاغات',                               target:100,p:'m',            num:'عدد البلاغات المنفذة',  den:'إجمالي البلاغات الواردة', src:'نظام 940',f:'البلاغات المنفذة ÷ إجمالي البلاغات الواردة × 100'},
  {id:'rep_comply',  name:'نسبة الامتثال بالبلاغات',                           target:100,p:'m',            num:'عدد البلاغات الممتثلة', den:'إجمالي البلاغات',         src:'نظام 940',f:'البلاغات الممتثلة ÷ إجمالي البلاغات × 100'},
  {id:'rep_satisfy', name:'نسبة الرضا على تنفيذ البلاغات',                    target:95, p:'m',            num:'عدد المقيمين براضي',    den:'إجمالي المقيمين',         src:'نظام 940',f:'المقيمون براضي ÷ إجمالي المقيمين × 100'},
  {id:'clean_rep',   name:'نسبة بلاغات النظافة (الهدف < 15%)',                 target:15, p:'m',lower:true, num:'عدد بلاغات النظافة',   den:'إجمالي البلاغات',         src:'نظام 940',f:'بلاغات النظافة ÷ إجمالي البلاغات × 100'},
  {id:'light_rep',   name:'نسبة بلاغات الإنارة (الهدف < 15%)',                 target:15, p:'m',lower:true, num:'عدد بلاغات الإنارة',   den:'إجمالي البلاغات',         src:'نظام 940',f:'بلاغات الإنارة ÷ إجمالي البلاغات × 100'},
]},
{id:'excellence',name:'وكالة التميز المؤسسي والتحول الرقمي',icon:'💡',kpis:[
  {id:'dev_eff',  name:'نسبة كفاءة وجاهزية الأجهزة', target:null,p:'m',num:'الأجهزة التي تعمل بشكل جيد',den:'إجمالي الأجهزة (جيد + تحتاج صيانة)',src:'تقرير',f:'الأجهزة الجيدة ÷ إجمالي الأجهزة × 100'},
  {id:'tech_supp',name:'نسبة تنفيذ الدعم الفني',      target:null,p:'m',num:'طلبات الدعم المنجزة',          den:'إجمالي طلبات الدعم الفني',          src:'تقرير',f:'الطلبات المنجزة ÷ إجمالي الطلبات × 100'},
]},
{id:'communication',name:'الإدارة العامة للاتصال المؤسسي',icon:'📢',kpis:[
  {id:'events',name:'نسبة تنفيذ الفعاليات المخطط لها',target:null,p:'q',num:'عدد الفعاليات المنفذة',den:'الفعاليات المستهدف تنفيذها',src:'تقرير',f:'الفعاليات المنفذة ÷ الفعاليات المستهدفة × 100'},
]},
{id:'safety',name:'الإدارة العامة للأمن والسلامة',icon:'🛡️',kpis:[
  {id:'cameras',name:'نسبة جاهزية كاميرات المراقبة بالمرافق العامة',target:100,p:'m',num:'عدد الكاميرات التي تعمل بشكل جيد',den:'إجمالي الكاميرات',src:'تقرير',f:'الكاميرات الجيدة ÷ إجمالي الكاميرات × 100'},
]},
{id:'executive',name:'المكتب التنفيذي',icon:'🏢',kpis:[
  {id:'urgent',    name:'نسبة إنجاز المعاملات العاجلة',                        target:100,p:'m',num:'عدد المعاملات العاجلة المنجزة', den:'إجمالي المعاملات العاجلة', src:'تقرير',f:'المنجزة ÷ إجمالي المعاملات × 100'},
  {id:'guest_apts',name:'نسبة إغلاق مواعيد خدمة الضيف',                      target:100,p:'m',num:'عدد المواعيد المغلقة',          den:'إجمالي المواعيد',         src:'تقرير',f:'المواعيد المغلقة ÷ إجمالي المواعيد × 100'},
  {id:'tasks',     name:'نسبة التزام الوكالات والإدارات بتنفيذ جدول المهام',   target:100,p:'m',num:'عدد المهام المنجزة',            den:'إجمالي المهام',           src:'تقرير',f:'المهام المنجزة ÷ إجمالي المهام × 100'},
]},
];

// ═══════════════ STATE ═══════════════
const ST={user:null,page:'',deptId:null,month:new Date().getMonth()+1,
  quarter:Math.ceil((new Date().getMonth()+1)/3),year:2026,ch:{},viewMode:'m'};

// ═══════════════ STORAGE ═══════════════
function gd(key='kpi26'){try{return JSON.parse(localStorage.getItem(key)||'{}');}catch{return {};}}
function sd(data,key='kpi26'){localStorage.setItem(key,JSON.stringify(data));}

// KPI data (num,den,pct)
function gKey(di,ki,per){return`${di}::${ki}::${ST.year}::${per}`;}
function getR(di,ki,per){return gd()[gKey(di,ki,per)]||null;}
function setR(di,ki,per,obj){const d=gd();d[gKey(di,ki,per)]=obj;sd(d);}
function getPct(di,ki,per){const r=getR(di,ki,per);return r?r.pct:null;}
function allPcts(di,ki,isM){
  if(isM)return Mo.map((_,i)=>getPct(di,ki,`M${i+1}`));
  return[1,2,3,4].map(q=>getPct(di,ki,`Q${q}`));
}

// Settings overrides (target, period per KPI)
function getSettings(){return gd('kpi26_settings');}
function saveSettings(s){sd(s,'kpi26_settings');}
function getKpiSetting(di,ki){return(getSettings()[`${di}::${ki}`])||{};}
function setKpiSetting(di,ki,obj){const s=getSettings();s[`${di}::${ki}`]=obj;saveSettings(s);}

// File attachments
function getFiles(){return gd('kpi26_files');}
function saveFiles(f){sd(f,'kpi26_files');}
function getKpiFiles(di,ki,per){return(getFiles()[`${di}::${ki}::${per}`])||[];}
function addKpiFile(di,ki,per,fileObj){
  const f=getFiles();const k=`${di}::${ki}::${per}`;
  if(!f[k])f[k]=[];f[k].push(fileObj);saveFiles(f);
}
function delKpiFile(di,ki,per,idx){
  const f=getFiles();const k=`${di}::${ki}::${per}`;
  if(f[k])f[k].splice(idx,1);saveFiles(f);
}

// Deadline settings
function getDlSettings(){return gd('kpi26_deadlines');}
function saveDlSettings(d){sd(d,'kpi26_deadlines');}
function getDeptDl(id){return(getDlSettings()[id])||{type:'m',days:5};}

// ═══════════════ KPI RESOLUTION (apply overrides) ═══════════════
function getDepts(){
  const settings=getSettings();
  return BASE_DEPTS.map(dept=>({
    ...dept,
    kpis:dept.kpis.map(kpi=>{
      const ov=settings[`${dept.id}::${kpi.id}`]||{};
      return{...kpi,
        target:ov.target!==undefined?ov.target:kpi.target,
        p:ov.p||kpi.p,
      };
    })
  }));
}

// ═══════════════ HELPERS ═══════════════
function DEPTS(){return getDepts();}
function findDept(id){return getDepts().find(d=>d.id===id);}

function cp(kpi){return kpi.p==='m'?`M${ST.month}`:`Q${ST.quarter}`;}
function cpForMode(kpi){
  if(ST.viewMode==='m')return kpi.p==='m'?`M${ST.month}`:`Q${ST.quarter}`;
  if(ST.viewMode==='q')return`Q${ST.quarter}`;
  return null; // annual = aggregate
}

function sts(v,tgt,low){
  if(v===null||v===undefined)return'gray';
  if(!tgt&&tgt!==0)return'gray';
  const p=low?(tgt/Math.max(v,.01))*100:(v/tgt)*100;
  return p>=90?'green':p>=70?'yellow':'red';
}
function ppct(v,tgt,low){
  if(v===null||v===undefined)return 0;
  if(!tgt&&tgt!==0)return Math.min(v,100);
  return low?Math.min(100,(tgt/Math.max(v,.01))*100):Math.min(100,(v/tgt)*100);
}
function pc(s){return{green:'#38a169',yellow:'#d69e2e',red:'#e53e3e',gray:'#a0aec0'}[s];}

function annualAvg(di,ki,kpi){
  if(kpi.p==='m'){const vs=Mo.map((_,i)=>getPct(di,ki,`M${i+1}`)).filter(v=>v!==null);return vs.length?parseFloat((vs.reduce((a,b)=>a+b,0)/vs.length).toFixed(1)):null;}
  else{const vs=[1,2,3,4].map(q=>getPct(di,ki,`Q${q}`)).filter(v=>v!==null);return vs.length?parseFloat((vs.reduce((a,b)=>a+b,0)/vs.length).toFixed(1)):null;}
}

function plbl(kpi){
  if(ST.viewMode==='y')return'السنوي '+ST.year;
  return kpi.p==='m'?Mo[ST.month-1]+' '+ST.year:Qr[ST.quarter-1]+' '+ST.year;
}

function dperf(id){
  const dept=findDept(id);if(!dept)return null;
  let t=0,c=0;
  dept.kpis.forEach(k=>{
    const v=ST.viewMode==='y'?annualAvg(id,k.id,k):getPct(id,k.id,cp(k));
    if(v!==null&&k.target){const p=k.lower?Math.min(100,(k.target/Math.max(v,.01))*100):Math.min(100,(v/k.target)*100);t+=p;c++;}
  });
  return c?Math.round(t/c):null;
}

function gstats(){
  let total=0,met=0,notMet=0,noData=0;
  const metList=[],notList=[],noList=[];
  getDepts().forEach(d=>d.kpis.forEach(k=>{
    total++;
    const v=ST.viewMode==='y'?annualAvg(d.id,k.id,k):getPct(d.id,k.id,cp(k));
    const item={dept:d,kpi:k,val:v};
    if(v===null){noData++;noList.push(item);return;}
    if(!k.target&&k.target!==0){noData++;noList.push(item);return;}
    const p=k.lower?(k.target/Math.max(v,.01))*100:(v/k.target)*100;
    if(p>=80){met++;metList.push(item);}else{notMet++;notList.push(item);}
  }));
  return{total,met,notMet,noData,metList,notList,noList};
}

// ═══════════════ DEADLINE CALC ═══════════════
function calcDeadline(deptId){
  const dl=getDeptDl(deptId);
  const now=new Date();
  let refDate;
  if(dl.type==='m'){
    // deadline = days after end of current month
    const lastDay=new Date(now.getFullYear(),now.getMonth()+1,0);
    refDate=new Date(lastDay);refDate.setDate(refDate.getDate()+parseInt(dl.days||5));
  }else if(dl.type==='w'){
    // weekly — days from last Sunday
    const lastSun=new Date(now);lastSun.setDate(now.getDate()-now.getDay());
    refDate=new Date(lastSun);refDate.setDate(refDate.getDate()+parseInt(dl.days||2));
  }else{
    // quarterly
    const qEnd=new Date(now.getFullYear(),ST.quarter*3,0);
    refDate=new Date(qEnd);refDate.setDate(refDate.getDate()+parseInt(dl.days||10));
  }
  const diff=Math.ceil((refDate-now)/(1000*60*60*24));
  return{days:diff,refDate};
}

function dlBadge(deptId){
  const{days}=calcDeadline(deptId);
  if(days<0)return`<div class="dl-badge dl-over">🔴 متأخر ${Math.abs(days)} يوم</div>`;
  if(days<=2)return`<div class="dl-badge dl-warn">🟡 ${days} أيام متبقية</div>`;
  return`<div class="dl-badge dl-ok">✅ ${days} يوم</div>`;
}

// ═══════════════ AUTH ═══════════════
function doLogin(){
  const uid=document.getElementById('user-sel').value;
  const pw=document.getElementById('pass-in').value;
  const err=document.getElementById('login-err');
  if(!uid||!USERS[uid]||USERS[uid].pass!==pw){err.style.display='block';return;}
  err.style.display='none';ST.user=uid;
  document.getElementById('login-page').style.display='none';
  document.getElementById('app').style.display='block';
  const u=USERS[uid];
  document.getElementById('sb-av').textContent=u.icon;
  document.getElementById('sb-name').textContent=u.name;
  document.getElementById('sb-role').textContent=u.role;
  buildSB();buildPer();
  u.isAdmin?nav('admin'):(ST.deptId=uid,nav('dept::'+uid));
}
function doLogout(){
  ST.user=null;
  document.getElementById('app').style.display='none';
  document.getElementById('login-page').style.display='flex';
  document.getElementById('pass-in').value='';
}

// ═══════════════ SIDEBAR ═══════════════
function buildSB(){
  const u=USERS[ST.user];let h='';
  if(u.isAdmin){
    h+=`<div class="nav-lbl">الرئيسية</div>
      ${ni('admin','📊','لوحة التحكم')}
      ${ni('settings','⚙️','إعدادات المؤشرات')}
      ${ni('deadlines','⏱️','إعدادات المواعيد')}`;
    h+=`<div class="nav-lbl">الوكالات والإدارات</div>`;
    getDepts().forEach(d=>h+=ni('dept::'+d.id,d.icon,d.name,d.kpis.length+' مؤشر'));
  }else{
    const dept=findDept(ST.user);
    if(dept)h+=`<div class="nav-lbl">مؤشراتي</div>${ni('dept::'+dept.id,dept.icon,'مؤشرات الأداء',dept.kpis.length+' مؤشر')}`;
  }
  document.getElementById('sb-nav').innerHTML=h;
}
function ni(page,icon,lbl,badge=''){
  const b=badge?`<span class="nav-badge">${badge}</span>`:'';
  return`<div class="nav-item" id="nav-${page.replace('::','-')}" onclick="nav('${page}')"><span class="ni">${icon}</span><span style="flex:1">${lbl}</span>${b}</div>`;
}
function setAct(page){
  document.querySelectorAll('.nav-item').forEach(e=>e.classList.remove('active'));
  const e=document.getElementById('nav-'+page.replace('::','-'));
  if(e)e.classList.add('active');
}

// ═══════════════ PERIOD ═══════════════
function buildPer(){
  const s=document.getElementById('period-sel');
  let h=`<optgroup label="شهري">`;
  Mo.forEach((m,i)=>h+=`<option value="M${i+1}" ${ST.month===i+1?'selected':''}>${m} ${ST.year}</option>`);
  h+=`</optgroup><optgroup label="ربع سنوي">`;
  Qr.forEach((q,i)=>h+=`<option value="Q${i+1}">${q} ${ST.year}</option>`);
  h+=`</optgroup>`;
  s.innerHTML=h;
}
function onPeriodChange(){
  const v=document.getElementById('period-sel').value;
  v.startsWith('M')?ST.month=parseInt(v.slice(1)):ST.quarter=parseInt(v.slice(1));
  render();
}
function setViewMode(mode,btn){
  ST.viewMode=mode;
  document.querySelectorAll('.vtab').forEach(b=>b.classList.remove('on'));
  btn.classList.add('on');
  render();
}

// ═══════════════ NAVIGATION ═══════════════
function nav(page){ST.page=page;setAct(page);dch();render();}
function render(){
  dch();
  if(ST.page==='admin')rAdmin();
  else if(ST.page==='settings')rSettings();
  else if(ST.page==='deadlines')rDeadlines();
  else if(ST.page.startsWith('dept::'))rDept(ST.page.split('::')[1]);
}
function dch(){Object.values(ST.ch).forEach(c=>{try{c.destroy();}catch{}});ST.ch={};}

// ═══════════════ ADMIN ═══════════════
function rAdmin(){
  document.getElementById('pg-title').textContent='لوحة التحكم الرئيسية';
  const s=gstats();
  let h=`<div class="stats-row">
    <div class="stat-card" style="--sc:#1a6b4a" onclick="openStatModal('all')">
      <div class="si">📊</div><div class="sv">${s.total}</div><div class="sl">إجمالي مؤشرات الأداء</div>
      <div class="sc-hint">اضغط لعرض التفاصيل ▾</div></div>
    <div class="stat-card" style="--sc:#38a169" onclick="openStatModal('met')">
      <div class="si">✅</div><div class="sv">${s.met}</div><div class="sl">تحقق المستهدف</div>
      <div class="sc-hint">اضغط لعرض الوكالات ▾</div></div>
    <div class="stat-card" style="--sc:#e53e3e" onclick="openStatModal('not')">
      <div class="si">⚠️</div><div class="sv">${s.notMet}</div><div class="sl">دون المستهدف</div>
      <div class="sc-hint">اضغط لعرض التفاصيل ▾</div></div>
    <div class="stat-card" style="--sc:#a0aec0" onclick="openStatModal('no')">
      <div class="si">📋</div><div class="sv">${s.noData}</div><div class="sl">بلا بيانات</div>
      <div class="sc-hint">اضغط لعرض التفاصيل ▾</div></div>
  </div>
  <div class="charts-row">
    <div class="chart-card"><h3>📈 الأداء العام</h3><div style="height:190px"><canvas id="dnt"></canvas></div></div>
    <div class="chart-card"><h3>🏢 أداء الوكالات والإدارات</h3><div style="height:190px"><canvas id="brc"></canvas></div></div>
  </div>
  <div class="sec-title">الوكالات والإدارات</div>
  <div class="dept-grid">`;
  getDepts().forEach(d=>{
    const p=dperf(d.id);
    const col=p===null?'#a0aec0':p>=80?'#38a169':p>=60?'#d69e2e':'#e53e3e';
    h+=`<div class="dept-card" onclick="nav('dept::${d.id}')">
      ${dlBadge(d.id)}
      <div class="di">${d.icon}</div><div class="dn">${d.name}</div>
      <div class="dc">${d.kpis.length} مؤشر أداء</div>
      <div class="perf-row">
        <div class="perf-bar"><div class="perf-fill" style="width:${p||0}%;background:${col}"></div></div>
        <div class="perf-pct" style="color:${col}">${p===null?'—':p+'%'}</div>
      </div>
    </div>`;
  });
  h+=`</div>
  <div class="sec-title" style="margin-top:1.2rem">قائمة جميع المؤشرات</div>
  <div class="tbl-wrap"><table class="tbl"><thead><tr>
    <th>الوكالة</th><th>المؤشر</th><th>المستهدف</th><th>الدورة</th><th>القيمة</th><th>الحالة</th>
  </tr></thead><tbody>`;
  getDepts().forEach(d=>d.kpis.forEach(k=>{
    const v=ST.viewMode==='y'?annualAvg(d.id,k.id,k):getPct(d.id,k.id,cp(k));
    const s2=sts(v,k.target,k.lower);
    const dot={green:'🟢',yellow:'🟡',red:'🔴',gray:'⚪'}[s2];
    const tgt=k.target?(k.lower?'< '+k.target+'%':k.target+'%'):'—';
    const val=v!==null?(k.isCount?v:v.toFixed(1)+'%'):'—';
    const pr=k.p==='m'?`<span class="tag tm">شهري</span>`:`<span class="tag tq">ربع سنوي</span>`;
    h+=`<tr><td>${d.icon} ${d.name}</td><td>${k.name}</td><td>${tgt}</td><td>${pr}</td><td><strong>${val}</strong></td><td>${dot}</td></tr>`;
  }));
  h+=`</tbody></table></div>`;
  document.getElementById('content').innerHTML=h;
  setTimeout(()=>{bDnt(s);bBar();},50);
}

function bDnt(s){
  const ctx=document.getElementById('dnt');if(!ctx)return;
  ST.ch.dnt=new Chart(ctx,{type:'doughnut',data:{
    labels:['يحقق الهدف','دون الهدف','بلا بيانات'],
    datasets:[{data:[s.met,s.notMet,s.noData],backgroundColor:['#38a169','#e53e3e','#e2e8f0'],borderWidth:0,hoverOffset:5}]
  },options:{responsive:true,maintainAspectRatio:false,cutout:'68%',
    plugins:{legend:{position:'bottom',labels:{font:{family:'Tajawal',size:10},boxWidth:11,padding:9}}}}});
}
function bBar(){
  const ctx=document.getElementById('brc');if(!ctx)return;
  const data=getDepts().map(d=>dperf(d.id)||0);
  ST.ch.bar=new Chart(ctx,{type:'bar',
    data:{labels:getDepts().map(d=>d.icon+' '+d.name.slice(0,13)),
          datasets:[{data,backgroundColor:data.map(v=>v>=80?'rgba(56,161,105,.75)':v>=60?'rgba(214,158,46,.75)':v>0?'rgba(229,62,62,.75)':'rgba(160,174,192,.5)'),borderRadius:5,borderSkipped:false}]},
    options:{responsive:true,maintainAspectRatio:false,indexAxis:'y',
      scales:{x:{min:0,max:100,ticks:{callback:v=>v+'%',font:{family:'Tajawal',size:9}},grid:{color:'#f5f5f5'}},y:{ticks:{font:{family:'Tajawal',size:9}}}},
      plugins:{legend:{display:false},tooltip:{callbacks:{label:c=>c.raw+'%'}}}}});
}

// ═══════════════ STAT MODAL ═══════════════
function openStatModal(type){
  const s=gstats();
  const titles={all:'📊 جميع مؤشرات الأداء',met:'✅ المؤشرات التي حققت المستهدف',not:'⚠️ المؤشرات دون المستهدف',no:'📋 المؤشرات بلا بيانات'};
  const list=type==='all'?[...s.metList,...s.notList,...s.noList]:type==='met'?s.metList:type==='not'?s.notList:s.noList;
  document.getElementById('modal-title').textContent=titles[type];
  document.getElementById('modal').classList.remove('sm');

  // Group by dept
  const byDept={};
  list.forEach(item=>{
    const dn=item.dept.name;
    if(!byDept[dn])byDept[dn]={icon:item.dept.icon,id:item.dept.id,items:[]};
    byDept[dn].items.push(item);
  });

  let h=`<div style="margin-bottom:.8rem;font-size:.8rem;color:var(--muted)">إجمالي: ${list.length} مؤشر</div>`;
  Object.keys(byDept).forEach(dName=>{
    const g=byDept[dName];
    h+=`<div style="margin-bottom:1rem">
      <div style="font-size:.78rem;font-weight:800;color:var(--g700);margin-bottom:.4rem;padding:.3rem .6rem;background:var(--g100);border-radius:6px">${g.icon} ${dName}</div>
      <div class="stat-modal-list">`;
    g.items.forEach(item=>{
      const v=item.val;
      const s2=sts(v,item.kpi.target,item.kpi.lower);
      const vcls={green:'smi-green',yellow:'smi-yellow',red:'smi-red',gray:'smi-gray'}[s2];
      const vTxt=v!==null?(item.kpi.isCount?v:v.toFixed(1)+'%'):'—';
      const dot={green:'🟢',yellow:'🟡',red:'🔴',gray:'⚪'}[s2];
      h+=`<div class="stat-modal-item">
        <div><div class="smi-dept">${item.kpi.name}</div>
          <div class="smi-kpi">الهدف: ${item.kpi.target!==null&&item.kpi.target!==undefined?(item.kpi.lower?'< '+item.kpi.target+'%':item.kpi.target+'%'):'—'}</div>
        </div>
        <div style="text-align:left;display:flex;align-items:center;gap:.4rem">
          <span class="smi-val ${vcls}">${vTxt}</span><span>${dot}</span>
        </div>
      </div>`;
    });
    h+=`</div></div>`;
  });
  if(!list.length)h+='<p style="text-align:center;color:var(--muted);padding:2rem">لا توجد بيانات في هذه الفئة</p>';
  document.getElementById('modal-body').innerHTML=h;
  document.getElementById('modal-ov').classList.add('open');
}

// ═══════════════ SETTINGS ═══════════════
function rSettings(){
  document.getElementById('pg-title').textContent='⚙️ إعدادات مؤشرات الأداء';
  let h='';
  getDepts().forEach(dept=>{
    h+=`<div class="settings-section">
      <h3>${dept.icon} ${dept.name}</h3>
      <div class="settings-row">`;
    dept.kpis.forEach(kpi=>{
      const ov=getKpiSetting(dept.id,kpi.id);
      const curTgt=ov.target!==undefined?ov.target:kpi.target;
      const curP=ov.p||kpi.p;
      h+=`<div class="settings-item">
        <div class="si-name">${kpi.name}</div>
        <div class="si-fields">
          <div>
            <label>المستهدف</label>
            <input type="number" min="0" max="200" id="tgt_${dept.id}_${kpi.id}" value="${curTgt!==null&&curTgt!==undefined?curTgt:''}" placeholder="قيد التحديد">
          </div>
          <div>
            <label>دورة الحصر</label>
            <select id="per_${dept.id}_${kpi.id}">
              <option value="m" ${curP==='m'?'selected':''}>شهري</option>
              <option value="q" ${curP==='q'?'selected':''}>ربع سنوي</option>
            </select>
          </div>
        </div>
      </div>`;
    });
    h+=`</div>
      <button class="btn-settings-save" onclick="saveSettingsDept('${dept.id}')">💾 حفظ إعدادات ${dept.name}</button>
    </div>`;
  });
  document.getElementById('content').innerHTML=h;
}

function saveSettingsDept(deptId){
  const dept=BASE_DEPTS.find(d=>d.id===deptId);if(!dept)return;
  dept.kpis.forEach(kpi=>{
    const tEl=document.getElementById(`tgt_${deptId}_${kpi.id}`);
    const pEl=document.getElementById(`per_${deptId}_${kpi.id}`);
    if(!tEl||!pEl)return;
    const tval=tEl.value.trim();
    setKpiSetting(deptId,kpi.id,{
      target:tval===''?null:parseFloat(tval),
      p:pEl.value
    });
  });
  showN('✅ تم حفظ إعدادات '+dept.name);
  buildSB();
}

// ═══════════════ DEADLINES ═══════════════
function rDeadlines(){
  document.getElementById('pg-title').textContent='⏱️ إعدادات مواعيد إدخال البيانات';
  let h=`<div class="settings-section">
    <h3>ضبط مهلة الإدخال لكل وكالة / إدارة</h3>
    <p style="font-size:.78rem;color:var(--muted);margin-bottom:1rem">
      يحدد المدير المهلة المسموحة لإدخال البيانات بعد نهاية الفترة. عند تجاوز المهلة تظهر تنبيه أحمر على الوكالة.
    </p>
    <div class="dl-settings-row">`;
  getDepts().forEach(d=>{
    const dl=getDeptDl(d.id);
    h+=`<div class="dl-item">
      <h4>${d.icon} ${d.name}</h4>
      <div class="dl-fields">
        <div>
          <label>نوع الدورة</label>
          <select id="dlt_${d.id}">
            <option value="m" ${dl.type==='m'?'selected':''}>شهري</option>
            <option value="w" ${dl.type==='w'?'selected':''}>أسبوعي</option>
            <option value="q" ${dl.type==='q'?'selected':''}>ربع سنوي</option>
          </select>
        </div>
        <div>
          <label>مهلة الإدخال (أيام)</label>
          <input type="number" min="1" max="30" id="dld_${d.id}" value="${dl.days||5}" placeholder="5">
        </div>
      </div>
    </div>`;
  });
  h+=`</div>
    <button class="btn-settings-save" onclick="saveAllDeadlines()" style="margin-top:1.2rem">💾 حفظ جميع المواعيد</button>
  </div>
  <div class="settings-section">
    <h3>📊 حالة المواعيد الحالية</h3>
    <table class="tbl" style="font-size:.82rem">
      <thead><tr><th>الوكالة / الإدارة</th><th>نوع الدورة</th><th>المهلة</th><th>الأيام المتبقية</th><th>الحالة</th></tr></thead>
      <tbody>`;
  getDepts().forEach(d=>{
    const dl=getDeptDl(d.id);
    const{days}=calcDeadline(d.id);
    const typeMap={m:'شهري',w:'أسبوعي',q:'ربع سنوي'};
    const cls=days<0?'smi-red':days<=2?'smi-yellow':'smi-green';
    const status=days<0?`متأخر ${Math.abs(days)} يوم`:days<=2?`${days} أيام 🟡`:`${days} يوم ✅`;
    h+=`<tr><td>${d.icon} ${d.name}</td><td>${typeMap[dl.type]||'شهري'}</td><td>${dl.days||5} أيام</td>
      <td class="${cls}" style="font-weight:700">${days}</td><td>${status}</td></tr>`;
  });
  h+=`</tbody></table></div>`;
  document.getElementById('content').innerHTML=h;
}

function saveAllDeadlines(){
  const d=getDlSettings();
  getDepts().forEach(dept=>{
    const t=document.getElementById(`dlt_${dept.id}`)?.value||'m';
    const ds=document.getElementById(`dld_${dept.id}`)?.value||'5';
    d[dept.id]={type:t,days:parseInt(ds)};
  });
  saveDlSettings(d);showN('✅ تم حفظ جميع المواعيد بنجاح');rDeadlines();
}

// ═══════════════ DEPT VIEW ═══════════════
function rDept(id){
  const dept=findDept(id);if(!dept)return;
  document.getElementById('pg-title').textContent=dept.name;
  const perf=dperf(id);
  const isAdmin=USERS[ST.user]?.isAdmin;
  const met=dept.kpis.filter(k=>{const v=ST.viewMode==='y'?annualAvg(id,k.id,k):getPct(id,k.id,cp(k));return v!==null&&k.target&&(k.lower?(k.target/Math.max(v,.01))*100:(v/k.target)*100)>=80;}).length;
  const hasData=dept.kpis.filter(k=>(ST.viewMode==='y'?annualAvg(id,k.id,k):getPct(id,k.id,cp(k)))!==null).length;
  const{days}=calcDeadline(id);
  const dlCls=days<0?'red':days<=2?'yellow':'green';
  const dlMsg=days<0?`⏰ تجاوز المهلة بـ ${Math.abs(days)} يوم`:days<=2?`⚡ تبقى ${days} أيام للإدخال`:`✅ تبقى ${days} يوم للإدخال`;

  let h=`<div class="dept-hero">
    <div class="dh-icon">${dept.icon}</div>
    <div class="dh-text"><h2>${dept.name}</h2><p>${dept.kpis.length} مؤشر أداء · الخطة التشغيلية 2026م</p></div>
    <div class="dh-stat"><div class="dsv">${perf!==null?perf+'%':'—'}</div><div class="dsl">متوسط الأداء</div></div>
  </div>
  <div class="dept-dl-strip">
    <div class="dl-info">⏱️ <strong>موعد الإدخال:</strong> &nbsp;<span class="dl-countdown ${dlCls}">${dlMsg}</span></div>
    <div style="font-size:.72rem;color:var(--muted)">آخر تحديث: ${new Date().toLocaleDateString('ar-SA')}</div>
  </div>
  <div class="summary-row">
    <div class="sum-card"><div class="sc-icon">📋</div><div><div class="sc-v">${dept.kpis.length}</div><div class="sc-l">إجمالي المؤشرات</div></div></div>
    <div class="sum-card"><div class="sc-icon">✅</div><div><div class="sc-v" style="color:#38a169">${met}</div><div class="sc-l">تحقق المستهدف</div></div></div>
    <div class="sum-card"><div class="sc-icon">📊</div><div><div class="sc-v" style="color:var(--g700)">${hasData}</div><div class="sc-l">مُدخل بيانات</div></div></div>
  </div>`;

  // Annual view — grid cells
  if(ST.viewMode==='y'){
    h+=`<div class="sec-title">عرض البيانات السنوية — ${ST.year}</div>`;
    dept.kpis.forEach(k=>{
      const isM=k.p==='m';
      const labels=isM?Mo:Qr;
      const vals=isM?Mo.map((_,i)=>getPct(id,k.id,`M${i+1}`)):[1,2,3,4].map(q=>getPct(id,k.id,`Q${q}`));
      const avg=annualAvg(id,k.id,k);
      const s2=sts(avg,k.target,k.lower);
      h+=`<div class="annual-kpi-wrap">
        <div style="display:flex;justify-content:space-between;align-items:center">
          <div class="annual-kpi-name">${k.name}</div>
          <div style="font-size:1.4rem;font-weight:900;color:${pc(s2)}">${avg!==null?avg.toFixed(1)+'%':'—'} <span style="font-size:.7rem;color:var(--muted)">متوسط</span></div>
        </div>
        <div class="annual-months-grid">`;
      labels.forEach((lbl,i)=>{
        const v=vals[i];const s3=sts(v,k.target,k.lower);
        h+=`<div class="amcell ${s3}">
          <div class="am-lbl">${lbl.slice(0,4)}</div>
          <div class="am-val">${v!==null?v.toFixed(1)+'%':'—'}</div>
        </div>`;
      });
      h+=`</div></div>`;
    });
  } else {
    // Monthly/Quarterly trend chart
    const monthlyK=dept.kpis.filter(k=>k.p==='m').slice(0,4);
    if(monthlyK.length){
      h+=`<div class="chart-card" style="margin-bottom:1.2rem">
        <h3>📈 منحنى الأداء الشهري</h3>
        <div style="height:170px"><canvas id="trd"></canvas></div>
      </div>`;
    }
    h+=`<div class="period-view-bar"><div class="sec-title" style="margin-bottom:0">مؤشرات الأداء — ${plbl(dept.kpis[0]||{p:'m'})}</div></div>`;
    h+=`<div class="kpi-grid">`;
    dept.kpis.forEach(k=>h+=kpiCard(k,id,isAdmin));
    h+=`</div>`;
  }

  document.getElementById('content').innerHTML=h;
  if(ST.viewMode!=='y'){
    const monthlyK=dept.kpis.filter(k=>k.p==='m').slice(0,4);
    if(monthlyK.length)setTimeout(()=>bTrd(dept,monthlyK),50);
  }
}

function bTrd(dept,kpis){
  const ctx=document.getElementById('trd');if(!ctx)return;
  const cols=['#1a6b4a','#2196F3','#e53e3e','#d69e2e'];
  const ds=kpis.map((k,i)=>({
    label:k.name.length>22?k.name.slice(0,22)+'…':k.name,
    data:allPcts(dept.id,k.id,true),
    borderColor:cols[i],backgroundColor:cols[i]+'18',fill:false,tension:.35,pointRadius:3,borderWidth:2,
  }));
  ST.ch.trd=new Chart(ctx,{type:'line',data:{labels:Mo,datasets:ds},
    options:{responsive:true,maintainAspectRatio:false,
      scales:{x:{ticks:{font:{family:'Tajawal',size:9}},grid:{display:false}},
              y:{min:0,max:100,ticks:{callback:v=>v+'%',font:{family:'Tajawal',size:9}},grid:{color:'#f5f5f5'}}},
      plugins:{legend:{position:'bottom',labels:{font:{family:'Tajawal',size:9},boxWidth:10,padding:7}}}}});
}

// ═══════════════ KPI CARD ═══════════════
function kpiCard(kpi,di,isAdmin){
  const per=cp(kpi);
  const rec=getR(di,kpi.id,per);
  const v=rec?rec.pct:null;
  const s=sts(v,kpi.target,kpi.lower);
  const prog=ppct(v,kpi.target,kpi.lower);
  const col=pc(s);
  const uid=`${di}_${kpi.id}`;
  const files=getKpiFiles(di,kpi.id,per);

  const vhtml=v===null
    ?`<div class="kpi-big-num no-data">أدخل الأرقام أدناه لحساب المؤشر</div>`
    :`<div class="kpi-big-num">${kpi.isCount?v:v.toFixed(1)}<span class="ku">${kpi.isCount?'':'%'}</span></div>`;

  const tgtTag=kpi.target!==null&&kpi.target!==undefined
    ?(kpi.lower?`<span class="tag tl">الهدف: أقل من ${kpi.target}%</span>`:`<span class="tag tt">الهدف: ${kpi.target}${kpi.isCount?'':'%'}</span>`)
    :`<span class="tag tn">هدف قيد التحديد</span>`;
  const perTag=kpi.p==='m'?`<span class="tag tm">شهري</span>`:`<span class="tag tq">ربع سنوي</span>`;

  const numV=rec&&rec.num!==null?rec.num:'';
  const denV=rec&&rec.den!==null?rec.den:'';
  const calcDisp=v!==null?'flex':'none';
  const calcVal=v!==null?(kpi.isCount?v:v.toFixed(1)+(kpi.isCount?'':'%')):'—';
  const calcCls=s==='green'?'cv-g':s==='yellow'?'cv-y':s==='red'?'cv-r':'cv-x';

  const editBtn=isAdmin?`<button class="kpi-edit-btn" onclick="openEditKpi('${di}','${kpi.id}')" title="تعديل الهدف والدورة">⚙️</button>`:'';

  let inpHtml=kpi.isCount
    ?`<div class="inp-grid one">
        <div class="inp-group"><label>${kpi.num}</label>
          <input type="number" min="0" id="num_${uid}" value="${numV}" placeholder="0"
            oninput="liveCalc('${uid}','count')">
        </div>
      </div>`
    :`<div class="inp-grid two">
        <div class="inp-group"><label>البسط — ${kpi.num}</label>
          <input type="number" min="0" id="num_${uid}" value="${numV}" placeholder="0"
            oninput="liveCalc('${uid}','ratio')">
        </div>
        <div class="inp-group"><label>المقام — ${kpi.den}</label>
          <input type="number" min="0" id="den_${uid}" value="${denV}" placeholder="0"
            oninput="liveCalc('${uid}','ratio')">
        </div>
      </div>`;

  // Files list
  let filesHtml='';
  if(files.length){
    filesHtml=files.map((f,i)=>`
      <div class="attach-file">
        <span class="af-name" onclick="downloadFile('${di}','${kpi.id}','${per}',${i})">${f.name}</span>
        <button class="af-del" onclick="deleteFile('${di}','${kpi.id}','${per}',${i})">🗑</button>
      </div>`).join('');
  }

  return`<div class="kpi-card">
    <div class="kpi-head">
      <div class="kpi-name-row">
        <div class="kstatus s-${s}"></div>
        <div class="kpi-name">${kpi.name}</div>
        <div class="kpi-actions">${editBtn}</div>
      </div>
      ${vhtml}
      <div class="tag-row">${tgtTag}${perTag}</div>
      <div class="kpi-prog"><div class="kpi-prog-fill" style="width:${prog}%;background:${col}"></div></div>
      <div class="kpi-prog-lbl"><span>0</span><span>${kpi.target&&!kpi.lower?'الهدف '+kpi.target+'%':''}</span><span>100%</span></div>
    </div>
    <div class="kpi-formula"><strong>📐 الحساب:</strong> ${kpi.f}</div>
    <div class="kpi-inputs">
      <div class="inp-period">📅 إدخال بيانات — ${plbl(kpi)}</div>
      ${inpHtml}
      <div class="calc-box" id="cb_${uid}" style="display:${calcDisp}">
        <span class="cl">النتيجة المحسوبة</span>
        <span class="cv ${calcCls}" id="cv_${uid}">${calcVal}</span>
      </div>
      <div class="save-row">
        <button class="btn-save" onclick="saveKpi('${uid}','${di}','${kpi.id}','${per}','${kpi.isCount?'c':'r'}')">💾 حفظ</button>
        <button class="btn-sm" onclick="openModal_hist('${di}','${kpi.id}')">📈 السجل</button>
      </div>
    </div>
    <div class="attach-strip">
      <div class="attach-header">
        <span>📎 المرفقات (${files.length})</span>
        <label class="attach-btn">
          ➕ إرفاق تقرير
          <input type="file" style="display:none" accept=".pdf,.xlsx,.xls,.docx,.doc,.png,.jpg"
            onchange="handleFileUpload(event,'${di}','${kpi.id}','${per}')">
        </label>
      </div>
      <div class="attach-list">${filesHtml}</div>
    </div>
  </div>`;
}

// ═══════════════ LIVE CALC ═══════════════
function liveCalc(uid,type){
  const cb=document.getElementById('cb_'+uid);
  const cv=document.getElementById('cv_'+uid);
  if(!cb||!cv)return;
  const n=parseFloat(document.getElementById('num_'+uid)?.value)||0;
  if(type==='count'){cb.style.display='flex';cv.textContent=n;cv.className='cv cv-g';return;}
  const d=parseFloat(document.getElementById('den_'+uid)?.value)||0;
  if(!d){cb.style.display='none';return;}
  const pct=(n/d)*100;
  cb.style.display='flex';
  cv.textContent=pct.toFixed(1)+'%';
  cv.className='cv '+(pct>=90?'cv-g':pct>=70?'cv-y':'cv-r');
}

// ═══════════════ SAVE ═══════════════
function saveKpi(uid,di,ki,period,type){
  const n=parseFloat(document.getElementById('num_'+uid)?.value);
  if(isNaN(n)||n<0){showN('⚠ أدخل قيمة صحيحة');return;}
  let obj;
  if(type==='c'){obj={num:n,den:null,pct:n};}
  else{
    const dv=parseFloat(document.getElementById('den_'+uid)?.value)||0;
    if(!dv){showN('⚠ المقام يجب أن يكون أكبر من صفر');return;}
    obj={num:n,den:dv,pct:parseFloat(((n/dv)*100).toFixed(2))};
  }
  setR(di,ki,period,obj);
  showN('✅ تم الحفظ بنجاح');render();
}

// ═══════════════ EDIT KPI MODAL ═══════════════
function openEditKpi(di,ki){
  const dept=findDept(di);const kpi=dept?.kpis.find(k=>k.id===ki);if(!kpi)return;
  const ov=getKpiSetting(di,ki);
  const curTgt=ov.target!==undefined?ov.target:kpi.target;
  const curP=ov.p||kpi.p;
  document.getElementById('modal-title').textContent='⚙️ تعديل مؤشر: '+kpi.name;
  document.getElementById('modal').classList.add('sm');
  document.getElementById('modal-body').innerHTML=`
    <div class="edit-field"><label>المستهدف</label>
      <input type="number" min="0" max="200" id="ek-tgt" value="${curTgt!==null&&curTgt!==undefined?curTgt:''}" placeholder="قيد التحديد">
    </div>
    <div class="edit-field"><label>دورة الحصر</label>
      <select id="ek-per">
        <option value="m" ${curP==='m'?'selected':''}>شهري</option>
        <option value="q" ${curP==='q'?'selected':''}>ربع سنوي</option>
      </select>
    </div>
    <div class="edit-field"><label>مصدر البيانات</label>
      <input type="text" id="ek-src" value="${kpi.src}" placeholder="مصدر البيانات">
    </div>
    <button class="btn-settings-save" style="width:100%" onclick="saveEditKpi('${di}','${ki}')">💾 حفظ التعديلات</button>`;
  document.getElementById('modal-ov').classList.add('open');
}

function saveEditKpi(di,ki){
  const tEl=document.getElementById('ek-tgt');
  const pEl=document.getElementById('ek-per');
  const tval=tEl.value.trim();
  setKpiSetting(di,ki,{target:tval===''?null:parseFloat(tval),p:pEl.value});
  closeModal();showN('✅ تم تعديل المؤشر بنجاح');buildSB();render();
}

// ═══════════════ HIST MODAL ═══════════════
function openModal_hist(di,ki){
  const dept=findDept(di);const kpi=dept?.kpis.find(k=>k.id===ki);if(!kpi)return;
  document.getElementById('modal-title').textContent='📈 '+kpi.name;
  document.getElementById('modal').classList.remove('sm');
  const isM=kpi.p==='m';
  const pers=isM?Mo.map((m,i)=>({lbl:m,key:`M${i+1}`})):Qr.map((q,i)=>({lbl:q,key:`Q${i+1}`}));
  const recs=pers.map(p=>getR(di,ki,p.key));
  const vals=recs.map(r=>r?r.pct:null);
  const tgt=kpi.target!==null&&kpi.target!==undefined?(kpi.lower?'أقل من '+kpi.target+'%':kpi.target+'%'):'قيد التحديد';

  let rows='';
  pers.forEach((p,i)=>{
    const r=recs[i];const v=r?r.pct:null;
    const s2=sts(v,kpi.target,kpi.lower);
    const dot={green:'🟢',yellow:'🟡',red:'🔴',gray:'⚪'}[s2];
    const files=getKpiFiles(di,ki,p.key);
    const fIcon=files.length?`📎 ${files.length}`:'—';
    rows+=`<tr>
      <td>${p.lbl} ${ST.year}</td>
      <td>${r&&r.num!==null?r.num:'—'}</td>
      <td>${kpi.isCount?'—':(r&&r.den!==null?r.den:'—')}</td>
      <td><strong>${v!==null?(kpi.isCount?v:v.toFixed(1)+'%'):'—'}</strong></td>
      <td>${dot}</td>
      <td style="color:var(--g700)">${fIcon}</td>
    </tr>`;
  });

  document.getElementById('modal-body').innerHTML=`
  <div class="info-grid">
    <div class="info-item"><div class="il">المستهدف</div><div class="iv">${tgt}</div></div>
    <div class="info-item"><div class="il">دورة الحصر</div><div class="iv">${isM?'شهري':'ربع سنوي'}</div></div>
    <div class="info-item"><div class="il">مصدر البيانات</div><div class="iv">${kpi.src}</div></div>
    <div class="info-item"><div class="il">الوكالة</div><div class="iv">${dept.icon} ${dept.name}</div></div>
  </div>
  <div class="formula-box"><strong>📐 طريقة الحساب:</strong><br>${kpi.f}</div>
  <div class="hist-title">📊 السجل التاريخي — ${ST.year}</div>
  <div class="modal-ch-wrap"><canvas id="mch"></canvas></div>
  <table class="hist-tbl"><thead><tr>
    <th>الفترة</th><th>${kpi.num}</th><th>${kpi.isCount?'—':(kpi.den||'المقام')}</th><th>النتيجة</th><th>الحالة</th><th>المرفقات</th>
  </tr></thead><tbody>${rows}</tbody></table>`;

  document.getElementById('modal-ov').classList.add('open');
  setTimeout(()=>{
    const ctx=document.getElementById('mch');if(!ctx)return;
    ST.ch.modal=new Chart(ctx,{type:'bar',
      data:{labels:pers.map(p=>p.lbl),datasets:[{data:vals.map(v=>v??0),
        backgroundColor:vals.map(v=>{const s2=sts(v,kpi.target,kpi.lower);return{green:'rgba(56,161,105,.7)',yellow:'rgba(214,158,46,.7)',red:'rgba(229,62,62,.7)',gray:'rgba(160,174,192,.5)'}[s2];}),borderRadius:5}]},
      options:{responsive:true,maintainAspectRatio:false,
        scales:{x:{ticks:{font:{family:'Tajawal',size:9}},grid:{display:false}},
                y:{min:0,ticks:{callback:v=>kpi.isCount?v:v+'%',font:{family:'Tajawal',size:9}},grid:{color:'#f5f5f5'}}},
        plugins:{legend:{display:false}}}});
  },50);
}

function closeModal(){
  document.getElementById('modal-ov').classList.remove('open');
  if(ST.ch.modal){try{ST.ch.modal.destroy();}catch{}delete ST.ch.modal;}
}

// ═══════════════ FILE HANDLING ═══════════════
function handleFileUpload(e,di,ki,per){
  const file=e.target.files[0];if(!file)return;
  if(file.size>3*1024*1024){showN('⚠ حجم الملف يجب أن يكون أقل من 3MB');return;}
  const reader=new FileReader();
  reader.onload=function(ev){
    addKpiFile(di,ki,per,{name:file.name,type:file.type,data:ev.target.result,date:new Date().toLocaleDateString('ar-SA')});
    showN('📎 تم إرفاق الملف: '+file.name);render();
  };
  reader.readAsDataURL(file);
}

function downloadFile(di,ki,per,idx){
  const files=getKpiFiles(di,ki,per);
  const f=files[idx];if(!f)return;
  const a=document.createElement('a');
  a.href=f.data;a.download=f.name;a.click();
}

function deleteFile(di,ki,per,idx){
  if(!confirm('حذف هذا الملف؟'))return;
  delKpiFile(di,ki,per,idx);showN('🗑 تم حذف الملف');render();
}

// ═══════════════ NOTIF ═══════════════
let nt;
function showN(msg){const e=document.getElementById('notif');e.textContent=msg;e.classList.add('show');clearTimeout(nt);nt=setTimeout(()=>e.classList.remove('show'),2800);}

// ═══════════════ DEMO ═══════════════
function seedDemo(){
  if(!confirm('تعبئة بيانات تجريبية؟ سيتم استبدال البيانات الحالية.'))return;
  const d=gd();
  getDepts().forEach(dept=>dept.kpis.forEach(k=>{
    const pers=k.p==='m'?Mo.map((_,i)=>`M${i+1}`):[1,2,3,4].map(q=>`Q${q}`);
    pers.forEach(p=>{
      const key=gKey(dept.id,k.id,p);
      if(k.isCount){const n=Math.floor(Math.random()*80+20);d[key]={num:n,den:null,pct:n};}
      else{
        const den=Math.floor(Math.random()*80+40);
        let num=k.lower?Math.floor(Math.random()*den*.25):Math.floor(den*(Math.random()*.25+.7));
        num=Math.min(num,den);
        d[key]={num,den,pct:parseFloat(((num/den)*100).toFixed(2))};
      }
    });
  }));
  sd(d);showN('📊 تم تعبئة البيانات التجريبية');render();
}

// ═══════════════ INIT ═══════════════
document.addEventListener('DOMContentLoaded',()=>{
  document.getElementById('pass-in').addEventListener('keydown',e=>{if(e.key==='Enter')doLogin();});
});
</script>
</body>
</html>
