<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Essenceloved</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700;900&family=Nunito:wght@400;600;700;800&display=swap" rel="stylesheet">
<style>

/* ── VARIABLES ── */
:root {
  --accent: #FF6B6B;
  --green:  #6BCB77;
  --blue:   #4D96FF;
  --purple: #C77DFF;
  --yellow: #FFD93D;
  --bg:     #FFF8F0;
  --white:  #FFFFFF;
  --text:   #2D2D2D;
  --gray:   #999;
  --border: #EEE;
  --radius: 16px;
  --shadow: 0 2px 16px rgba(0,0,0,0.08);
}

/* ── RESET & BASE ── */
* { margin:0; padding:0; box-sizing:border-box; }
body { font-family:'Nunito',sans-serif; background:var(--bg); color:var(--text); height:100vh; overflow:hidden; display:flex; flex-direction:column; }
button { cursor:pointer; font-family:inherit; border:none; }
input, textarea, select { font-family:inherit; }

/* ── LAYOUT ORDER (top→bottom): header, strip, pages, nav ── */
#header  { order:0; flex-shrink:0; height:50px; display:flex; align-items:center; justify-content:space-between; padding:0 16px; background:rgba(255,255,255,0.95); backdrop-filter:blur(10px); border-bottom:1px solid var(--border); z-index:30; }
#strip   { order:1; flex-shrink:0; height:82px; display:flex; flex-direction:column; justify-content:center; padding:8px 14px; background:rgba(255,255,255,0.95); backdrop-filter:blur(8px); border-bottom:1px solid var(--border); z-index:20; }
#pages   { order:2; flex:1; overflow:hidden; }
#botnav  { order:3; flex-shrink:0; height:56px; display:flex; align-items:center; justify-content:space-around; padding:0 6px; background:rgba(255,255,255,0.95); backdrop-filter:blur(10px); border-top:1px solid var(--border); z-index:30; }

/* ── HEADER ── */
#app-name { font-family:'Playfair Display',serif; font-size:20px; font-weight:900; }
#app-name span { color:var(--accent); }
#user-pill { font-size:12px; font-weight:800; color:var(--gray); padding:3px 10px; background:var(--bg); border-radius:20px; border:1.5px solid var(--border); display:none; }
#header-date { font-size:11px; color:var(--gray); font-weight:700; }

/* ── TASK STRIP ── */
.strip-top  { display:flex; align-items:center; justify-content:space-between; margin-bottom:6px; }
.strip-lbl  { font-size:10px; font-weight:800; letter-spacing:1px; text-transform:uppercase; color:var(--gray); }
.strip-add  { font-size:12px; font-weight:800; color:var(--accent); background:none; }
.strip-row  { display:flex; gap:8px; overflow-x:auto; scrollbar-width:none; padding-bottom:2px; overflow-y:visible; }
.strip-row::-webkit-scrollbar { display:none; }

/* Strip task pill */
.strip-wrap { position:relative; flex-shrink:0; }
.s-pill {
  display:flex; align-items:center; gap:6px;
  background:var(--bg); border-radius:30px; padding:5px 10px 5px 6px;
  border:2px solid transparent; cursor:pointer; transition:border-color 0.2s; white-space:nowrap;
}
.s-pill:hover { border-color:var(--accent); }
.s-dot  { width:16px; height:16px; border-radius:50%; border:2px solid var(--accent); display:flex; align-items:center; justify-content:center; font-size:9px; color:white; flex-shrink:0; }
.s-txt  { font-size:13px; font-weight:700; }
.s-tag  { font-size:10px; font-weight:800; padding:1px 6px; border-radius:20px; }
.s-prog { font-size:10px; font-weight:800; color:var(--gray); background:rgba(0,0,0,0.06); padding:1px 6px; border-radius:20px; }
.s-arr  { font-size:11px; color:var(--gray); background:none; padding:0 2px; transition:transform 0.2s; }
.s-arr.open { transform:rotate(180deg); }
.s-thumb { width:18px; height:18px; border-radius:4px; object-fit:cover; }

/* Tags */
.tag-personal { background:#f0e0ff; color:var(--purple); }
.tag-work     { background:#dceeff; color:var(--blue);   }
.tag-health   { background:#d9f7dc; color:#3aaa52;       }

/* Sub-task dropdown — fixed position, rendered outside scroll container */
.sub-drop {
  display:none; position:fixed;
  background:white; border-radius:14px; padding:10px 12px;
  box-shadow:0 8px 28px rgba(0,0,0,0.18); z-index:500; min-width:220px; max-width:300px;
}
.sub-drop.open { display:block; }
.sub-drop-ttl { font-size:10px; font-weight:800; letter-spacing:1px; text-transform:uppercase; color:var(--gray); margin-bottom:8px; }
.sub-item { display:flex; align-items:center; gap:8px; padding:7px 8px; border-radius:8px; cursor:pointer; }
.sub-item:hover { background:var(--bg); }
.sub-item.done { opacity:0.45; }
.sub-item.done .si-txt { text-decoration:line-through; }
.si-chk { width:17px; height:17px; border-radius:4px; border:2px solid var(--accent); display:flex; align-items:center; justify-content:center; font-size:9px; color:white; flex-shrink:0; }
.sub-item.done .si-chk { background:var(--accent); }
.si-txt { font-size:13px; font-weight:600; flex:1; }
.prog-bg  { height:4px; border-radius:4px; background:var(--border); overflow:hidden; margin-top:8px; }
.prog-bar { height:100%; border-radius:4px; background:var(--accent); transition:width 0.3s; }
.prog-lbl { font-size:10px; font-weight:800; color:var(--gray); text-align:right; margin-top:3px; }

/* Inline add row inside dropdown */
.dd-add-row {
  display:flex; gap:6px; margin-top:10px;
  border-top:1px solid var(--border); padding-top:8px;
}
.dd-add-inp {
  flex:1; padding:6px 10px; border-radius:8px;
  border:2px solid var(--border); font-size:13px;
  font-family:inherit; outline:none; background:var(--bg);
}
.dd-add-inp:focus { border-color:var(--accent); }
.dd-add-btn {
  padding:6px 12px; border-radius:8px;
  background:var(--accent); color:white;
  font-size:14px; font-weight:800; border:none; cursor:pointer;
}
.dd-add-btn:hover { opacity:0.85; }

/* ── PAGES ── */
.page { display:none; height:100%; overflow-y:auto; padding:16px; padding-bottom:82px; }
.page.active { display:block; }
.pg-hdr { display:flex; align-items:center; justify-content:space-between; margin-bottom:16px; }
.pg-ttl { font-family:'Playfair Display',serif; font-size:24px; font-weight:900; }

/* ── BOTTOM NAV ── */
.ntab { display:flex; flex-direction:column; align-items:center; gap:1px; padding:6px 8px; border-radius:12px; background:transparent; font-size:10px; font-weight:800; color:var(--gray); min-width:46px; }
.ntab .ni { font-size:19px; line-height:1; }
.ntab:hover { color:var(--accent); }
.ntab.active { color:var(--accent); background:rgba(255,107,107,0.08); }

/* ── CARDS ── */
.card { background:rgba(255,255,255,0.92); border-radius:var(--radius); padding:16px; box-shadow:var(--shadow); margin-bottom:14px; background-size:cover; background-position:center; position:relative; overflow:hidden; }
.card.has-img::before { content:''; position:absolute; inset:0; background:rgba(255,255,255,0.6); backdrop-filter:blur(3px); border-radius:var(--radius); pointer-events:none; }
.card > * { position:relative; z-index:1; }

/* ── BUTTONS ── */
.btn { padding:9px 15px; border-radius:11px; border:none; font-size:13px; font-weight:700; transition:all 0.15s; cursor:pointer; }
.btn:hover { opacity:0.85; transform:translateY(-1px); }
.btn-a { background:var(--accent); color:white; }
.btn-p { background:var(--purple); color:white; }
.btn-y { background:var(--yellow); color:var(--text); }
.btn-g { background:var(--green);  color:white; }
.btn-x { background:var(--border); color:var(--gray); }

/* ── HOME ── */
.greet-h { font-family:'Playfair Display',serif; font-size:23px; font-weight:900; margin-bottom:3px; }
.greet-s { font-size:12px; color:var(--gray); font-weight:600; margin-bottom:16px; }
.add-trig { display:flex; align-items:center; justify-content:center; gap:8px; width:100%; padding:12px; border-radius:13px; border:2px dashed var(--border); background:rgba(255,255,255,0.7); font-size:13px; font-weight:700; color:var(--gray); cursor:pointer; margin-bottom:18px; transition:all 0.2s; }
.add-trig:hover { border-color:var(--accent); color:var(--accent); }
.sec-ttl { font-size:10px; font-weight:800; letter-spacing:1.3px; text-transform:uppercase; color:var(--gray); margin-bottom:9px; }
.feed-card { background:white; border-radius:var(--radius); box-shadow:var(--shadow); overflow:hidden; margin-bottom:14px; }
.fc-body  { padding:13px 14px; }
.fc-row   { display:flex; align-items:center; gap:10px; background:var(--bg); border-radius:11px; padding:10px 12px; }
.fc-chk   { width:20px; height:20px; border-radius:5px; border:2px solid var(--accent); display:flex; align-items:center; justify-content:center; font-size:10px; color:white; flex-shrink:0; }
.fc-txt   { flex:1; font-size:14px; font-weight:700; }
.fc-tag   { font-size:10px; font-weight:800; padding:2px 7px; border-radius:20px; }
.media-prev { margin-top:8px; border-radius:9px; overflow:hidden; }
.media-prev img, .media-prev video { width:100%; max-height:150px; object-fit:cover; display:block; }
.done-lbl { font-size:10px; font-weight:800; color:var(--green); text-transform:uppercase; letter-spacing:0.8px; margin:6px 0 3px; }
.note-card { border-radius:var(--radius); padding:15px; min-height:120px; cursor:pointer; box-shadow:var(--shadow); position:relative; transition:transform 0.2s; overflow:hidden; background-size:cover; background-position:center; }
.note-card.has-img::before { content:''; position:absolute; inset:0; background:rgba(255,255,255,0.55); backdrop-filter:blur(3px); border-radius:var(--radius); pointer-events:none; }
.note-card > * { position:relative; z-index:1; }
.note-card:hover { transform:translateY(-3px); }
.n-ttl { font-family:'Playfair Display',serif; font-size:16px; font-weight:700; margin-bottom:6px; }
.n-bod { font-size:12px; line-height:1.6; }
.n-dt  { position:absolute; bottom:9px; right:11px; font-size:10px; opacity:0.5; font-weight:700; }
.nc0 { background:linear-gradient(135deg,#fff3cc,#ffd93d); }
.nc1 { background:linear-gradient(135deg,#d9f7dc,#6bcb77); }
.nc2 { background:linear-gradient(135deg,#e8d5ff,#c77dff); }
.nc3 { background:linear-gradient(135deg,#ffd5d5,#ff6b6b); }
.nc4 { background:linear-gradient(135deg,#d5eeff,#4d96ff); }
.nc5 { background:linear-gradient(135deg,#ffe8d6,#ffaa70); }
.no-item { background:white; border-radius:var(--radius); padding:16px; text-align:center; color:var(--gray); font-size:13px; font-weight:700; box-shadow:var(--shadow); }

/* ── GALLERY ── */
.drop-zone { border:3px dashed var(--border); border-radius:var(--radius); padding:28px; text-align:center; cursor:pointer; color:var(--gray); margin-bottom:13px; transition:all 0.2s; }
.drop-zone:hover { border-color:var(--purple); color:var(--purple); background:#faf5ff; }
.photo-grid { display:grid; grid-template-columns:repeat(auto-fill,minmax(130px,1fr)); gap:10px; }
.photo-wrap { border-radius:13px; overflow:hidden; aspect-ratio:1; position:relative; box-shadow:var(--shadow); }
.photo-wrap img { width:100%; height:100%; object-fit:cover; display:block; }
.photo-nm { position:absolute; bottom:0; left:0; right:0; background:rgba(0,0,0,0.42); color:white; font-size:11px; font-weight:700; padding:4px 8px; opacity:0; transition:opacity 0.2s; }
.photo-wrap:hover .photo-nm { opacity:1; }

/* ── NOTES ── */
.notes-grid { display:grid; grid-template-columns:repeat(auto-fill,minmax(185px,1fr)); gap:12px; }

/* ── CALENDAR ── */
.cal-layout { display:grid; grid-template-columns:1fr 240px; gap:12px; }
.cal-nav { display:flex; align-items:center; gap:10px; margin-bottom:10px; }
.cal-mo  { font-family:'Playfair Display',serif; font-size:18px; font-weight:700; }
.cal-arr { background:var(--bg); border:2px solid var(--border); border-radius:8px; width:30px; height:30px; display:flex; align-items:center; justify-content:center; font-size:14px; }
.cal-arr:hover { background:var(--accent); border-color:var(--accent); color:white; }
.cal-grid { display:grid; grid-template-columns:repeat(7,1fr); gap:2px; }
.dn { text-align:center; font-size:9px; font-weight:800; text-transform:uppercase; color:var(--gray); padding:5px 0; }
.dc { aspect-ratio:1; border-radius:7px; border:none; background:transparent; font-size:12px; font-weight:700; color:var(--text); position:relative; }
.dc:hover:not(.om) { background:var(--bg); }
.dc.om { color:#ccc; }
.dc.td { background:var(--accent); color:white; }
.dc.sl:not(.td) { background:var(--bg); border:2px solid var(--accent); color:var(--accent); }
.dc.he::after { content:''; position:absolute; bottom:2px; left:50%; transform:translateX(-50%); width:4px; height:4px; border-radius:50%; background:var(--green); }
.dc.td.he::after { background:white; }
.ev-box   { background:white; border-radius:var(--radius); padding:14px; box-shadow:var(--shadow); }
.ev-ttl   { font-family:'Playfair Display',serif; font-size:15px; font-weight:700; margin-bottom:10px; }
.ev-row   { display:flex; gap:8px; padding:8px; border-radius:8px; background:var(--bg); margin-bottom:6px; }
.ev-dot   { width:8px; height:8px; border-radius:50%; margin-top:4px; flex-shrink:0; }
.ev-nm    { font-size:13px; font-weight:700; }
.ev-tm    { font-size:11px; color:var(--gray); }
.ev-form  { display:flex; flex-direction:column; gap:6px; margin-top:10px; }
.ev-form input { padding:8px 11px; border-radius:8px; border:2px solid var(--border); font-size:13px; outline:none; background:var(--bg); }
.ev-form input:focus { border-color:var(--green); }
.no-ev { font-size:12px; color:var(--gray); font-weight:600; }

/* ── COMPLETED ── */
.done-card { background:white; border-radius:var(--radius); padding:13px 15px; box-shadow:var(--shadow); margin-bottom:10px; border-left:4px solid var(--green); }
.done-card .dc-top { display:flex; align-items:center; gap:9px; margin-bottom:5px; }
.dc-txt  { flex:1; font-size:14px; font-weight:700; text-decoration:line-through; color:var(--gray); }
.dc-dt   { font-size:11px; color:var(--gray); font-weight:700; margin-bottom:5px; }
.dc-subs { display:flex; flex-wrap:wrap; gap:5px; margin-bottom:5px; }
.dc-sub  { font-size:11px; font-weight:700; padding:2px 8px; background:var(--bg); border-radius:20px; color:var(--gray); }
.dc-med  { border-radius:8px; overflow:hidden; margin-bottom:6px; }
.dc-med img, .dc-med video { width:100%; max-height:130px; object-fit:cover; display:block; border-radius:8px; }
.restore-btn { background:none; border:2px solid var(--border); border-radius:7px; padding:3px 9px; font-size:11px; font-weight:800; color:var(--gray); cursor:pointer; }
.restore-btn:hover { border-color:var(--accent); color:var(--accent); }

/* ── SETTINGS ── */
.sett-sec { margin-bottom:22px; }
.sett-sec-ttl { font-size:10px; font-weight:800; letter-spacing:1.5px; text-transform:uppercase; color:var(--gray); margin-bottom:10px; padding-bottom:5px; border-bottom:1px solid var(--border); }
.sett-row { display:flex; align-items:center; gap:11px; background:white; border-radius:13px; padding:11px 13px; margin-bottom:7px; box-shadow:0 1px 6px rgba(0,0,0,0.05); }
.sett-ico { font-size:20px; width:34px; text-align:center; flex-shrink:0; }
.sett-lbl { font-size:13px; font-weight:700; }
.sett-sub { font-size:11px; color:var(--gray); margin-top:1px; }
.sett-right { display:flex; align-items:center; gap:7px; flex-shrink:0; margin-left:auto; }
.s-inp  { border:2px solid var(--border); border-radius:8px; padding:6px 9px; font-size:13px; font-weight:700; width:130px; outline:none; background:var(--bg); }
.s-inp:focus  { border-color:var(--accent); }
.s-sel  { padding:7px 10px; border-radius:8px; border:2px solid var(--border); font-size:13px; font-weight:700; background:var(--bg); outline:none; cursor:pointer; }
.s-sel:focus  { border-color:var(--accent); }
.e-btn  { width:32px; height:32px; border-radius:8px; background:var(--bg); border:2px solid var(--border); font-size:16px; display:flex; align-items:center; justify-content:center; cursor:pointer; }
.e-btn:hover  { border-color:var(--accent); }
.clr-btn { width:26px; height:26px; border-radius:50%; background:rgba(255,107,107,0.1); border:none; font-size:13px; color:var(--accent); display:flex; align-items:center; justify-content:center; cursor:pointer; }
.up-btn  { display:flex; align-items:center; gap:5px; padding:5px 10px; border-radius:8px; background:var(--bg); border:2px solid var(--border); font-size:12px; font-weight:700; color:var(--gray); cursor:pointer; }
.up-btn:hover { border-color:var(--purple); color:var(--purple); }
.s-img-prev { width:32px; height:32px; border-radius:7px; border:2px solid var(--border); object-fit:cover; }
/* Toggle */
.tog { position:relative; display:inline-block; width:44px; height:24px; }
.tog input { opacity:0; width:0; height:0; }
.tog-sl { position:absolute; inset:0; background:#ccc; border-radius:24px; cursor:pointer; transition:0.3s; }
.tog-sl::before { content:''; position:absolute; width:18px; height:18px; left:3px; bottom:3px; background:white; border-radius:50%; transition:0.3s; }
.tog input:checked + .tog-sl { background:var(--accent); }
.tog input:checked + .tog-sl::before { transform:translateX(20px); }
/* Color wheel */
.cw-row { display:flex; align-items:center; gap:9px; flex-wrap:wrap; padding-left:45px; margin-top:4px; }
.cw     { width:42px; height:42px; border-radius:50%; border:3px solid var(--border); padding:2px; background:none; cursor:pointer; -webkit-appearance:none; appearance:none; }
.cw::-webkit-color-swatch-wrapper { padding:0; border-radius:50%; }
.cw::-webkit-color-swatch { border:none; border-radius:50%; }
.chip   { width:34px; height:34px; border-radius:9px; border:2px solid var(--border); flex-shrink:0; }
.hex-inp { width:86px; padding:6px 9px; border-radius:8px; border:2px solid var(--border); font-size:12px; font-weight:700; outline:none; background:var(--bg); text-transform:uppercase; }
.hex-inp:focus { border-color:var(--accent); }
.qsw { display:flex; gap:4px; flex-wrap:wrap; }
.qs  { width:20px; height:20px; border-radius:50%; cursor:pointer; border:2px solid transparent; }
.qs:hover { border-color:var(--text); transform:scale(1.15); }
/* Export items */
.exp-item { display:flex; align-items:center; gap:9px; padding:9px 12px; border-radius:11px; background:white; border:2px solid var(--border); margin-bottom:6px; cursor:pointer; transition:border-color 0.2s; }
.exp-item:hover { border-color:var(--accent); }
.exp-item.sel   { border-color:var(--accent); background:rgba(255,107,107,0.05); }
.exp-item.sel .exp-chk { background:var(--accent); border-color:var(--accent); color:white; }
.exp-chk { width:18px; height:18px; border-radius:5px; border:2px solid var(--border); display:flex; align-items:center; justify-content:center; font-size:10px; flex-shrink:0; }
.exp-ico { font-size:17px; flex-shrink:0; }
.exp-txt { flex:1; font-size:13px; font-weight:700; }
.exp-typ { font-size:10px; font-weight:800; padding:2px 6px; border-radius:20px; background:var(--bg); color:var(--gray); }
/* Subtask builder */
.sb-row { display:flex; gap:6px; margin-bottom:6px; }
.sb-row input { flex:1; padding:7px 11px; border-radius:9px; border:2px solid var(--border); font-size:13px; outline:none; background:var(--bg); }
.sb-row input:focus { border-color:var(--accent); }
.sb-row button { padding:7px 12px; border-radius:9px; background:var(--accent); color:white; font-size:13px; font-weight:700; }
.sb-list { display:flex; flex-direction:column; gap:4px; max-height:110px; overflow-y:auto; }
.sb-item { display:flex; align-items:center; gap:7px; padding:6px 9px; border-radius:7px; background:var(--bg); font-size:13px; font-weight:600; }
.sb-del  { background:none; border:none; color:var(--gray); font-size:13px; cursor:pointer; margin-left:auto; }
.sb-del:hover { color:var(--accent); }

/* ── MODALS ── */
.modal-bg { display:none; position:fixed; inset:0; background:rgba(0,0,0,0.42); z-index:100; align-items:center; justify-content:center; backdrop-filter:blur(4px); }
.modal-bg.open { display:flex; }
.modal-box { background:white; border-radius:20px; padding:22px; width:420px; max-width:92vw; box-shadow:0 20px 50px rgba(0,0,0,0.15); }
.m-ttl { font-family:'Playfair Display',serif; font-size:18px; font-weight:900; margin-bottom:12px; }
.m-inp { width:100%; padding:10px 13px; border-radius:10px; border:2px solid var(--border); font-size:14px; outline:none; margin-bottom:9px; background:var(--bg); }
.m-inp:focus { border-color:var(--accent); }
.m-sel { width:100%; padding:9px 12px; border-radius:10px; border:2px solid var(--border); font-size:13px; font-weight:700; background:var(--bg); outline:none; margin-bottom:9px; }
.m-ta  { width:100%; border:none; outline:none; font-size:14px; line-height:1.7; height:130px; resize:none; color:var(--text); }
.m-hr  { border:none; border-top:1px solid var(--border); margin-bottom:10px; }
.m-foot { display:flex; justify-content:flex-end; gap:8px; margin-top:10px; }
.m-foot-c { display:flex; justify-content:center; gap:8px; margin-top:10px; }
.att-btn { display:flex; align-items:center; gap:7px; padding:9px 12px; border-radius:10px; border:2px dashed var(--border); background:var(--bg); font-size:13px; font-weight:700; color:var(--gray); cursor:pointer; width:100%; margin-bottom:9px; }
.att-btn:hover { border-color:var(--purple); color:var(--purple); }
.med-wrap { position:relative; margin-bottom:9px; border-radius:10px; overflow:hidden; }
.med-wrap img, .med-wrap video { width:100%; max-height:140px; object-fit:cover; display:block; border-radius:10px; }
.med-rm  { position:absolute; top:5px; right:5px; background:rgba(0,0,0,0.55); color:white; border:none; border-radius:50%; width:22px; height:22px; font-size:11px; display:flex; align-items:center; justify-content:center; cursor:pointer; }
.med-badge { position:absolute; bottom:5px; left:7px; background:rgba(0,0,0,0.55); color:white; font-size:10px; font-weight:700; padding:2px 7px; border-radius:20px; }

/* ── 30-MIN POPUP ── */
#remind { display:none; position:fixed; inset:0; z-index:200; align-items:center; justify-content:center; background:rgba(0,0,0,0.35); backdrop-filter:blur(5px); }
#remind.open { display:flex; }
.rem-box { background:white; border-radius:22px; padding:24px; width:340px; max-width:92vw; box-shadow:0 20px 50px rgba(0,0,0,0.16); text-align:center; position:relative; overflow:hidden; }
.conf-area { position:absolute; inset:0; pointer-events:none; overflow:hidden; border-radius:22px; }
.conf-p { position:absolute; width:8px; height:8px; border-radius:2px; animation:cf 1.8s ease-in forwards; opacity:0; }
@keyframes cf { 0%{transform:translateY(-20px) rotate(0deg);opacity:1} 100%{transform:translateY(340px) rotate(540deg);opacity:0} }
.rem-em { font-size:42px; margin-bottom:6px; }
.rem-ttl { font-family:'Playfair Display',serif; font-size:19px; font-weight:900; margin-bottom:3px; }
.rem-sub { font-size:12px; color:var(--gray); margin-bottom:12px; font-weight:600; }
.rem-score { font-size:12px; color:var(--gray); font-weight:700; margin-bottom:8px; }
.rem-list { text-align:left; margin-bottom:12px; max-height:190px; overflow-y:auto; }
.rem-item { display:flex; align-items:center; gap:8px; padding:8px 10px; border-radius:10px; background:var(--bg); margin-bottom:5px; cursor:pointer; border:2px solid transparent; }
.rem-item:hover { border-color:var(--accent); }
.rem-chk { width:18px; height:18px; border-radius:5px; border:2px solid var(--accent); display:flex; align-items:center; justify-content:center; font-size:9px; color:white; flex-shrink:0; }
.rem-txt { flex:1; font-size:13px; font-weight:600; }
.rem-foot { display:flex; gap:8px; justify-content:center; }

/* ── EMOJI PICKER ── */
#epick { display:none; position:fixed; z-index:300; background:white; border-radius:14px; padding:12px; box-shadow:0 8px 36px rgba(0,0,0,0.16); width:270px; max-height:210px; overflow-y:auto; }
#epick.open { display:block; }
.ep-grid { display:grid; grid-template-columns:repeat(8,1fr); gap:3px; }
.ep { font-size:21px; cursor:pointer; text-align:center; padding:3px; border-radius:5px; }
.ep:hover { background:var(--bg); }

/* ── DARK MODE ── */
body.dm {
  --bg:#1A1A2E; --white:#22223B; --text:#F0EBE3; --gray:#888; --border:#333355; --shadow:0 2px 16px rgba(0,0,0,0.35);
}
body.dm .feed-card, body.dm .card, body.dm .ev-box, body.dm .modal-box, body.dm .rem-box,
body.dm .sett-row, body.dm .note-card, body.dm .done-card, body.dm .sub-drop { background:#22223B; color:#F0EBE3; }
body.dm #header, body.dm #strip, body.dm #botnav { background:rgba(26,26,46,0.96); }
body.dm .ntab { color:#888; }
body.dm .ntab.active { color:var(--accent); }
body.dm .s-pill, body.dm .fc-row, body.dm .rem-item, body.dm .ev-row, body.dm .add-trig { background:#2D2D4E; }
body.dm .exp-item { background:#2D2D4E; border-color:#333355; }
body.dm input, body.dm textarea, body.dm select { background:#2D2D4E; color:#F0EBE3; border-color:#333355; }
body.dm .btn-x { background:#2D2D4E; color:#888; }

/* Edit button on strip pill */
.s-edit {
  background: none; border: none; font-size: 13px; cursor: pointer;
  padding: 0 2px; opacity: 0; transition: opacity 0.15s; flex-shrink: 0;
}
.s-pill:hover .s-edit { opacity: 1; }

/* Sub-task checklist in modal */
.sb-chk {
  width: 18px; height: 18px; border-radius: 5px; border: 2px solid var(--accent);
  display: flex; align-items: center; justify-content: center;
  font-size: 10px; color: white; flex-shrink: 0; cursor: pointer;
  transition: background 0.15s;
}
.sb-chk-done { background: var(--accent); }
.sb-edit-inp {
  flex: 1; border: none; outline: none; background: transparent;
  font-size: 13px; font-weight: 600; font-family: inherit; color: var(--text);
  padding: 0 4px;
}
.sb-done-txt { text-decoration: line-through; opacity: 0.5; }

/* ── RESPONSIVE ── */
@media (max-width:600px) {
  .cal-layout { grid-template-columns:1fr; }
  .ntab { min-width:40px; padding:5px 5px; }
  .s-inp { width:100px; }
}

</style>
</head>
<body>

<!-- HEADER -->
<div id="header">
  <div style="display:flex;align-items:baseline;gap:9px">
    <span id="app-name">Essence<span>loved</span> 🌸</span>
    <span id="user-pill"></span>
  </div>
  <span id="header-date"></span>
</div>

<!-- TASK STRIP -->
<div id="strip">
  <div class="strip-top">
    <span class="strip-lbl" id="strip-lbl-el">📋 Today's Tasks</span>
    <button class="strip-add" onclick="openTaskModal()">+ Add</button>
  </div>
  <div class="strip-row" id="strip-row"></div>
</div>

<!-- PAGES -->
<div id="pages">

  <!-- HOME -->
  <div class="page active" id="page-home">
    <div class="greet-h" id="greet-h"></div>
    <div class="greet-s" id="greet-s"></div>
    <button class="add-trig" onclick="openTaskModal()">
      <span id="add-icon">✏️</span> <span id="add-lbl">New Task — add a photo, GIF or video</span>
    </button>
    <div class="sec-ttl" id="ft-lbl">📋 Latest Task</div>
    <div id="feed-task"></div>
    <div class="sec-ttl" id="fn-lbl" style="margin-top:14px">📝 Latest Note</div>
    <div id="feed-note"></div>
    <div class="sec-ttl" id="fp-lbl" style="margin-top:14px">📸 Latest Photo</div>
    <div id="feed-photo"></div>
  </div>

  <!-- GALLERY -->
  <div class="page" id="page-gallery">
    <div class="pg-hdr">
      <div class="pg-ttl" id="gallery-ttl">Gallery</div>
      <button class="btn btn-p" onclick="document.getElementById('ph-inp').click()">+ Upload</button>
    </div>
    <input type="file" id="ph-inp" accept="image/*" multiple style="display:none" onchange="loadPhotos(event)">
    <div class="drop-zone" onclick="document.getElementById('ph-inp').click()">
      <div style="font-size:32px;margin-bottom:5px">📷</div>
      <div style="font-weight:700">Tap to upload photos</div>
    </div>
    <div class="photo-grid" id="photo-grid">
      <div style="grid-column:1/-1;text-align:center;color:var(--gray);font-weight:700;padding:16px">No photos yet 🌸</div>
    </div>
  </div>

  <!-- NOTES -->
  <div class="page" id="page-notes">
    <div class="pg-hdr">
      <div class="pg-ttl" id="notes-ttl">Notes &amp; Journal</div>
      <button class="btn btn-y" onclick="openNote(null)">+ New Note</button>
    </div>
    <div class="notes-grid" id="notes-grid"></div>
  </div>

  <!-- CALENDAR -->
  <div class="page" id="page-calendar">
    <div class="pg-hdr"><div class="pg-ttl" id="cal-ttl">Calendar</div></div>
    <div class="cal-layout">
      <div class="card" id="c-cal">
        <div class="cal-nav">
          <button class="cal-arr" onclick="moveCal(-1)">&#8249;</button>
          <div class="cal-mo" id="cal-lbl"></div>
          <button class="cal-arr" onclick="moveCal(1)">&#8250;</button>
        </div>
        <div class="cal-grid" id="cal-grid"></div>
      </div>
      <div class="ev-box" id="c-ev">
        <div class="ev-ttl" id="ev-hd">Events</div>
        <div id="ev-list"></div>
        <div class="ev-form">
          <input type="text" id="ev-inp" placeholder="Event name…">
          <input type="time" id="ev-time">
          <button class="btn btn-g" onclick="addEvent()">Add Event</button>
        </div>
      </div>
    </div>
  </div>

  <!-- COMPLETED -->
  <div class="page" id="page-completed">
    <div class="pg-hdr">
      <div class="pg-ttl">🏆 Completed</div>
      <button class="btn btn-x" style="font-size:12px;padding:7px 12px" onclick="clearCompleted()">Clear All</button>
    </div>
    <div id="done-list"></div>
  </div>

  <!-- SETTINGS -->\n  <div class=\"page\" id=\"page-settings\">\n    <div class=\"pg-hdr\">
      <div class=\"pg-ttl\">⚙️ Settings</div>
      <div style=\"display:flex;gap:8px\">
        <button class=\"btn btn-x\" style=\"font-size:12px;padding:7px 12px\" onclick=\"revertSettings()\">↩ Revert</button>
        <button class=\"btn btn-a\" style=\"font-size:12px;padding:7px 12px\" onclick=\"saveSettings()\">💾 Save</button>
      </div>
    </div>
    <div id=\"save-banner\" style=\"display:none;background:#d9f7dc;color:#2a7a3b;font-size:13px;font-weight:700;padding:10px 14px;border-radius:11px;margin-bottom:14px;text-align:center\"></div>

    <div class="sett-sec">
      <div class="sett-sec-ttl">🏷️ Identity</div>
      <div class="sett-row">
        <div class="sett-ico">👤</div>
        <div><div class="sett-lbl">Your Name</div><div class="sett-sub">Shown next to app name</div></div>
        <div class="sett-right"><input class="s-inp" id="s-name" placeholder="e.g. Sarah" oninput="applyS()"></div>
      </div>
      <div class="sett-row">
        <div class="sett-ico">💬</div>
        <div><div class="sett-lbl">Greeting</div><div class="sett-sub">Home page welcome text</div></div>
        <div class="sett-right"><input class="s-inp" id="s-greet" value="Good morning" oninput="applyS()"></div>
      </div>
    </div>

    <div class="sett-sec">
      <div class="sett-sec-ttl">🎨 Theme</div>
      <div class="sett-row">
        <div class="sett-ico">🌙</div>
        <div><div class="sett-lbl">Dark Mode</div></div>
        <div class="sett-right"><label class="tog"><input type="checkbox" id="s-dm" onchange="applyDM(this.checked)"><span class="tog-sl"></span></label></div>
      </div>
      <div class="sett-row" style="flex-direction:column;align-items:flex-start;gap:10px">
        <div style="display:flex;align-items:center;gap:10px;width:100%">
          <div class="sett-ico">🎨</div>
          <div><div class="sett-lbl">Accent Colour</div><div class="sett-sub">Buttons, tabs, checkboxes</div></div>
        </div>
        <div class="cw-row">
          <input type="color" class="cw" id="acc-w" value="#FF6B6B" oninput="setAccent(this.value)">
          <div class="chip" id="acc-chip" style="background:#FF6B6B"></div>
          <input type="text" class="hex-inp" id="acc-hex" value="#FF6B6B" maxlength="7" oninput="if(/^#[0-9A-Fa-f]{6}$/.test(this.value)){setAccent(this.value);document.getElementById('acc-w').value=this.value;}">
          <div class="qsw" id="acc-qs"></div>
        </div>
      </div>
      <div class="sett-row" style="flex-direction:column;align-items:flex-start;gap:10px">
        <div style="display:flex;align-items:center;gap:10px;width:100%">
          <div class="sett-ico">🌑</div>
          <div style="flex:1"><div class="sett-lbl">Shadow Colour</div><div class="sett-sub">Card drop shadows</div></div>
          <label class="tog"><input type="checkbox" id="s-sh-on" checked onchange="applyShadow()"><span class="tog-sl"></span></label>
        </div>
        <div class="cw-row">
          <input type="color" class="cw" id="sh-w" value="#000000" oninput="setShadow(this.value)">
          <div class="chip" id="sh-chip" style="background:#000000"></div>
          <input type="text" class="hex-inp" id="sh-hex" value="#000000" maxlength="7" oninput="if(/^#[0-9A-Fa-f]{6}$/.test(this.value)){setShadow(this.value);document.getElementById('sh-w').value=this.value;}">
          <div class="qsw" id="sh-qs"></div>
        </div>
        <div style="display:flex;align-items:center;gap:8px;width:100%;padding-left:45px">
          <span style="font-size:11px;font-weight:700;color:var(--gray)">Intensity</span>
          <input type="range" id="sh-op" min="0" max="40" value="8" oninput="applyShadow()" style="flex:1;accent-color:var(--accent)">
          <span id="sh-pct" style="font-size:11px;font-weight:700;color:var(--gray);width:28px;text-align:right">8%</span>
        </div>
      </div>
      <div class="sett-row">
        <div class="sett-ico">🅰️</div>
        <div><div class="sett-lbl">Font</div></div>
        <div class="sett-right">
          <select class="s-sel" id="s-font" onchange="applyS()">
            <option value="Nunito">Nunito</option>
            <option value="Georgia">Georgia</option>
            <option value="Courier New">Courier New</option>
            <option value="Trebuchet MS">Trebuchet</option>
            <option value="Palatino">Palatino</option>
          </select>
        </div>
      </div>
      <div class="sett-row">
        <div class="sett-ico">🖼️</div>
        <div><div class="sett-lbl">Wallpaper</div><div class="sett-sub">Full background image</div></div>
        <div class="sett-right">
          <div id="wp-prev" style="width:32px;height:32px;border-radius:7px;border:2px solid var(--border);background:var(--bg);display:flex;align-items:center;justify-content:center;font-size:16px;overflow:hidden">🌅</div>
          <button class="up-btn" onclick="triggerImg('wp')">📁 Upload</button>
          <button class="clr-btn" onclick="clearImg('wp')">✕</button>
        </div>
      </div>
    </div>

    <div class="sett-sec">
      <div class="sett-sec-ttl">✏️ Labels &amp; Icons</div>
      <div id="lbl-rows"></div>
    </div>

    <div class="sett-sec">
      <div class="sett-sec-ttl">🖼️ Section Images</div>
      <div id="img-rows"></div>
    </div>

    <div class="sett-sec">
      <div class="sett-sec-ttl">🧭 Nav Labels</div>
      <div id="nav-rows"></div>
    </div>

    <div class="sett-sec">
      <div class="sett-sec-ttl">⏰ Reminder Timing</div>
      <div class="sett-row">
        <div class="sett-ico">🔔</div>
        <div><div class="sett-lbl">Check-in Frequency</div></div>
        <div class="sett-right">
          <select class="s-sel" id="s-freq" onchange="applyFreq()">
            <option value="0">No reminders</option>
            <option value="30" selected>Every 30 min</option>
            <option value="60">Every 1 hour</option>
            <option value="120">Every 2 hours</option>
          </select>
        </div>
      </div>
      <div class="sett-row">
        <div class="sett-ico">👁️</div>
        <div><div class="sett-lbl">Preview Reminder</div></div>
        <div class="sett-right"><button class="btn btn-a" style="font-size:12px;padding:6px 12px" onclick="openRemind()">Show Now</button></div>
      </div>
    </div>

    <div class="sett-sec">
      <div class="sett-sec-ttl">📤 Export &amp; Share</div>
      <div class="sett-row" style="flex-direction:column;align-items:flex-start;gap:10px">
        <div style="display:flex;align-items:center;justify-content:space-between;width:100%">
          <div><div class="sett-lbl">Select Posts to Export</div></div>
          <div style="display:flex;gap:6px">
            <button class="btn btn-x" style="font-size:11px;padding:5px 10px" onclick="selAll()">All</button>
            <button class="btn btn-x" style="font-size:11px;padding:5px 10px" onclick="deselAll()">None</button>
          </div>
        </div>
        <div id="exp-list" style="width:100%"></div>
        <div style="display:flex;gap:8px;width:100%;flex-wrap:wrap">
          <button class="btn btn-a" style="flex:1;min-width:110px" onclick="expEmail()">📧 Email</button>
          <button class="btn btn-p" style="flex:1;min-width:110px" onclick="expFile()">💾 Save File</button>
        </div>
        <div id="exp-status" style="font-size:12px;color:var(--gray);font-weight:700;width:100%;text-align:center;min-height:16px"></div>
      </div>
    </div>

  </div>

</div><!-- /pages -->

<!-- BOTTOM NAV -->
<div id="botnav">
  <button class="ntab active" id="nb-home"      onclick="goPage('home',this)">     <span class="ni" id="ni-home">🏠</span>     <span id="nl-home">Home</span></button>
  <button class="ntab"        id="nb-gallery"   onclick="goPage('gallery',this)">  <span class="ni" id="ni-gallery">📸</span>  <span id="nl-gallery">Gallery</span></button>
  <button class="ntab"        id="nb-notes"     onclick="goPage('notes',this)">    <span class="ni" id="ni-notes">📝</span>    <span id="nl-notes">Notes</span></button>
  <button class="ntab"        id="nb-calendar"  onclick="goPage('calendar',this)"> <span class="ni" id="ni-calendar">📅</span> <span id="nl-calendar">Cal</span></button>
  <button class="ntab"        id="nb-completed" onclick="goPage('completed',this)"><span class="ni" id="ni-completed">🏆</span><span id="nl-completed">Done</span></button>
  <button class="ntab"        id="nb-settings"  onclick="goPage('settings',this)"> <span class="ni" id="ni-settings">⚙️</span> <span id="nl-settings">Settings</span></button>
</div>

<!-- TASK MODAL -->
<!-- TASK MODAL (create + edit) -->
<div class="modal-bg" id="task-modal">
  <div class="modal-box">
    <div class="m-ttl">✏️ New Task</div>
    <!-- title row with editable task name + delete button -->
    <div style="display:flex;align-items:center;gap:8px;margin-bottom:10px">
      <input class="m-inp" type="text" id="tm-txt" placeholder="Task name…" style="margin-bottom:0;flex:1">
      <button id="tm-del-btn" class="btn btn-x" style="padding:8px 11px;font-size:12px;display:none" onclick="deleteTask()">🗑️</button>
    </div>

    <select class="m-sel" id="tm-tag">
      <option value="personal">🙋 Personal</option>
      <option value="work">💼 Work</option>
      <option value="health">💪 Health</option>
    </select>

    <!-- Checklist (sub-tasks) — live editable -->
    <div style="font-size:11px;font-weight:800;letter-spacing:1px;text-transform:uppercase;color:var(--gray);margin-bottom:7px">📋 Checklist</div>
    <div id="sb-list" class="sb-list"></div>
    <div class="sb-row">
      <input type="text" id="sb-inp" placeholder="Add checklist item…" onkeydown="if(event.key==='Enter'){event.preventDefault();addSub();}">
      <button onclick="addSub()">+ Add</button>
    </div>

    <!-- Media -->
    <button class="att-btn" onclick="document.getElementById('tm-file').click()" style="margin-top:8px">
      🖼️ <span id="tm-att-lbl">Attach photo, GIF or video</span>
    </button>
    <input type="file" id="tm-file" accept="image/*,video/*,.gif" style="display:none" onchange="prevMedia(event,'tm')">
    <div id="tm-med-wrap" class="med-wrap" style="display:none">
      <div id="tm-med-slot"></div>
      <button class="med-rm" onclick="rmMedia('tm')">✕</button>
      <div class="med-badge" id="tm-badge"></div>
    </div>

    <div class="m-foot">
      <button class="btn btn-x" onclick="closeModal('task-modal')">Cancel</button>
      <button class="btn btn-a" id="tm-save-btn" onclick="saveTask()">Add Task</button>
    </div>
  </div>
</div>

<!-- COMPLETE MODAL -->
<div class="modal-bg" id="comp-modal">
  <div class="modal-box" style="text-align:center">
    <div style="font-size:40px;margin-bottom:6px">🎉</div>
    <div class="m-ttl" style="text-align:center">Task Complete!</div>
    <div style="font-size:13px;color:var(--gray);margin-bottom:14px">Add a photo, GIF or video to celebrate 🌟</div>
    <button class="att-btn" style="justify-content:center" onclick="document.getElementById('cm-file').click()">
      📎 <span id="cm-att-lbl">Attach celebration media (optional)</span>
    </button>
    <input type="file" id="cm-file" accept="image/*,video/*,.gif" style="display:none" onchange="prevMedia(event,'cm')">
    <div id="cm-med-wrap" class="med-wrap" style="display:none">
      <div id="cm-med-slot"></div>
      <button class="med-rm" onclick="rmMedia('cm')">✕</button>
    </div>
    <div class="m-foot-c">
      <button class="btn btn-x" onclick="closeComp(false)">Skip</button>
      <button class="btn btn-g" onclick="closeComp(true)">Save 🎊</button>
    </div>
  </div>
</div>

<!-- NOTE MODAL -->
<div class="modal-bg" id="note-modal">
  <div class="modal-box">
    <div class="m-ttl" id="note-modal-ttl">📝 New Note</div>
    <input class="m-inp" type="text" id="note-ttl-inp" placeholder="Note title…">
    <hr class="m-hr">
    <textarea class="m-ta" id="note-bod-inp" placeholder="Write here…"></textarea>
    <div class="m-foot">
      <button class="btn btn-x" onclick="closeModal('note-modal')">Cancel</button>
      <button class="btn btn-y" onclick="saveNote()">Save</button>
    </div>
  </div>
</div>

<!-- 30-MIN POPUP -->
<div id="remind">
  <div class="rem-box">
    <div class="conf-area" id="conf-area"></div>
    <div class="rem-em" id="rem-em">⏰</div>
    <div class="rem-ttl" id="rem-ttl">Task Check-in!</div>
    <div class="rem-sub">Tap a task to view its sub-tasks 🎉</div>
    <div class="rem-score" id="rem-score"></div>
    <div class="rem-list" id="rem-list"></div>
    <div class="rem-foot">
      <button class="btn btn-x" onclick="closeRemind()">Later</button>
      <button class="btn btn-a" onclick="closeRemind()">Done! 🎉</button>
    </div>
  </div>
</div>

<!-- EMOJI PICKER -->
<div id="epick"><div class="ep-grid" id="ep-grid"></div></div>

<!-- Hidden file inputs -->
<input type="file" id="sett-file" accept="image/*" style="display:none">

<script>

/* ═══════════════════════════
   DATA
═══════════════════════════ */
var tasks = [
  { id:1, text:'Morning meditation', tag:'health',   media:null, doneMedia:null, completedAt:null,
    subs:[{id:11,text:'Eye rest',done:false},{id:12,text:'Meditation',done:false},{id:13,text:'Coffee',done:false}] },
  { id:2, text:'Review weekly goals', tag:'personal', media:null, doneMedia:null, completedAt:null, subs:[] },
  { id:3, text:'Team standup',         tag:'work',     media:null, doneMedia:null, completedAt:null,
    subs:[{id:31,text:'Check agenda',done:false},{id:32,text:'Share updates',done:false}] },
  { id:4, text:'Go for a 30 min walk', tag:'health',  media:null, doneMedia:null, completedAt:null, subs:[] }
];
var doneTasks = [];
var photos    = [];
var notes     = [
  { id:1, title:'My Goals 🌟',   body:'Dream big, start small, act now.',      color:0, date:'Mar 15' },
  { id:2, title:'Gratitude Log', body:'Grateful for family and morning coffee.', color:1, date:'Mar 17' },
  { id:3, title:'Ideas 💡',      body:'Redecorate. Pottery. Weekend trip!',      color:2, date:'Mar 18' }
];
var calEvs = {
  '2026-3-19':[{name:'Doctor Appointment',time:'10:00'},{name:'Lunch with Sarah',time:'13:00'}],
  '2026-3-22':[{name:'Weekend hike',time:'08:00'}],
  '2026-3-25':[{name:'Birthday party 🎂',time:'19:00'}]
};
var calY=2026, calM=2, selD=19, noteEditId=null, noteColorIdx=3;
var completingId=null, tmMedia=null, cmMedia=null;
var tmSubs=[];
var remTimer=null;
var expSel={};

/* Settings state */
var S = {
  username:'', greeting:'Good morning', font:'Nunito',
  accent:'#FF6B6B', shadowColor:'#000000', dm:false, remMins:30,
  wallpaper:null, sectionImgs:{},
  labels:{
    'strip':       {icon:'📋',text:"Today's Tasks"},
    'feed-task':   {icon:'📋',text:'Latest Task'},
    'feed-note':   {icon:'📝',text:'Latest Note'},
    'feed-photo':  {icon:'📸',text:'Latest Photo'},
    'add-task':    {icon:'✏️',text:'New Task — add a photo, GIF or video'},
    'gallery':     {icon:'🖼️',text:'Gallery'},
    'notes':       {icon:'📖',text:'Notes & Journal'},
    'calendar':    {icon:'📅',text:'Calendar'}
  },
  navLabels:{
    home:{icon:'🏠',text:'Home'}, gallery:{icon:'📸',text:'Gallery'},
    notes:{icon:'📝',text:'Notes'}, calendar:{icon:'📅',text:'Cal'},
    completed:{icon:'🏆',text:'Done'}, settings:{icon:'⚙️',text:'Settings'}
  }
};

/* ── DEFAULTS (used by Revert) ── */
var DEFAULTS = {
  username:'', greeting:'Good morning', font:'Nunito',
  accent:'#FF6B6B', shadowColor:'#000000', dm:false, remMins:30,
  wallpaper:null, sectionImgs:{},
  labels:{
    'strip':      {icon:'📋',text:"Today's Tasks"},
    'feed-task':  {icon:'📋',text:'Latest Task'},
    'feed-note':  {icon:'📝',text:'Latest Note'},
    'feed-photo': {icon:'📸',text:'Latest Photo'},
    'add-task':   {icon:'✏️',text:'New Task — add a photo, GIF or video'},
    'gallery':    {icon:'🖼️',text:'Gallery'},
    'notes':      {icon:'📖',text:'Notes & Journal'},
    'calendar':   {icon:'📅',text:'Calendar'}
  },
  navLabels:{
    home:{icon:'🏠',text:'Home'}, gallery:{icon:'📸',text:'Gallery'},
    notes:{icon:'📝',text:'Notes'}, calendar:{icon:'📅',text:'Cal'},
    completed:{icon:'🏆',text:'Done'}, settings:{icon:'⚙️',text:'Settings'}
  }
};

/* ── SAVE to localStorage ── */
function saveSettings() {
  try {
    /* Don't store image data urls — they're too large for localStorage.
       Store everything except wallpaper and sectionImgs blobs. */
    var toSave = {
      username:    S.username,
      greeting:    S.greeting,
      font:        S.font,
      accent:      S.accent,
      shadowColor: S.shadowColor,
      dm:          S.dm,
      remMins:     S.remMins,
      labels:      S.labels,
      navLabels:   S.navLabels
    };
    localStorage.setItem('essenceloved_settings', JSON.stringify(toSave));
    showBanner('✅ Settings saved!', '#d9f7dc', '#2a7a3b');
  } catch(e) {
    showBanner('⚠️ Could not save — storage may be unavailable.', '#ffd5d5', '#8b0000');
  }
}

/* ── REVERT to factory defaults ── */
function revertSettings() {
  if (!confirm('Reset all settings to original defaults?')) return;
  /* Deep-copy DEFAULTS into S */
  S.username    = DEFAULTS.username;
  S.greeting    = DEFAULTS.greeting;
  S.font        = DEFAULTS.font;
  S.accent      = DEFAULTS.accent;
  S.shadowColor = DEFAULTS.shadowColor;
  S.dm          = DEFAULTS.dm;
  S.remMins     = DEFAULTS.remMins;
  S.wallpaper   = DEFAULTS.wallpaper;
  S.sectionImgs = {};
  S.labels      = JSON.parse(JSON.stringify(DEFAULTS.labels));
  S.navLabels   = JSON.parse(JSON.stringify(DEFAULTS.navLabels));

  /* Clear saved data */
  try { localStorage.removeItem('essenceloved_settings'); } catch(e){}

  /* Re-apply everything */
  applyS();
  applyDM(false);
  setAccent(S.accent);
  setShadow(S.shadowColor);
  applyLabels();
  applyNavLabels();

  /* Remove any section images from DOM */
  var imgIds = ['c-cal','c-ev','strip'];
  imgIds.forEach(function(id){
    var el = document.getElementById(id);
    if (el) { el.style.backgroundImage=''; el.classList.remove('has-img'); }
  });

  /* Rebuild settings UI if visible */
  var sf = document.getElementById('s-freq');
  if (sf) sf.value = '30';
  buildSettingsUI();

  showBanner('↩ Settings reverted to defaults.', '#fff3cc', '#7a5c00');
}

/* ── LOAD from localStorage on startup ── */
function loadSettings() {
  try {
    var raw = localStorage.getItem('essenceloved_settings');
    if (!raw) return;
    var saved = JSON.parse(raw);
    if (saved.username    !== undefined) S.username    = saved.username;
    if (saved.greeting    !== undefined) S.greeting    = saved.greeting;
    if (saved.font        !== undefined) S.font        = saved.font;
    if (saved.accent      !== undefined) S.accent      = saved.accent;
    if (saved.shadowColor !== undefined) S.shadowColor = saved.shadowColor;
    if (saved.dm          !== undefined) S.dm          = saved.dm;
    if (saved.remMins     !== undefined) S.remMins     = saved.remMins;
    if (saved.labels)    S.labels    = saved.labels;
    if (saved.navLabels) S.navLabels = saved.navLabels;
  } catch(e) { /* ignore parse errors */ }
}

/* ── Banner helper ── */
function showBanner(msg, bg, color) {
  var el = document.getElementById('save-banner');
  if (!el) return;
  el.textContent = msg;
  el.style.background = bg;
  el.style.color = color;
  el.style.display = 'block';
  clearTimeout(showBanner._t);
  showBanner._t = setTimeout(function(){ el.style.display='none'; }, 3000);
}

var IMG_TARGETS = [
  {id:'c-cal',label:'Calendar Card'},
  {id:'c-ev', label:'Events Card'},
  {id:'strip',label:'Task Strip'}
];
var LBL_DEFS = [
  {id:'strip',title:'Task Strip'},       {id:'feed-task',title:'Home: Tasks'},
  {id:'feed-note',title:'Home: Notes'},  {id:'feed-photo',title:'Home: Photos'},
  {id:'add-task',title:'Add Task Button'},{id:'gallery',title:'Gallery Title'},
  {id:'notes',title:'Notes Title'},      {id:'calendar',title:'Calendar Title'}
];
var NAV_DEFS = ['home','gallery','notes','calendar','completed','settings'];
var MONTHS=['January','February','March','April','May','June','July','August','September','October','November','December'];
var WDAYS=['Sun','Mon','Tue','Wed','Thu','Fri','Sat'];
var DOT=['var(--accent)','var(--purple)','var(--green)','var(--blue)','var(--yellow)'];
var CONF_CLR=['#FF6B6B','#FFD93D','#6BCB77','#4D96FF','#C77DFF','#FF9F43'];
var QS_ACC=['#FF6B6B','#4D96FF','#6BCB77','#C77DFF','#FF9F43','#FFD93D','#EF476F','#118AB2','#06D6A0','#2D2D2D'];
var QS_SH=['#000000','#1A1A2E','#FF6B6B','#4D96FF','#6BCB77','#C77DFF','#8B4513','#2F4F4F','#4B0082','#696969'];
var EMOJIS='🌸🌺🌻🌹🌷💐🍀🌿🦋🐝🌈⭐🌟✨💫🎀🎁🎉🎊🏆🥇💎💡📌📋📝📸📅🏠❤️🧡💛💚💙💜🌙☀️🌊🔥💧🍎🍓🍒🥑🍋🧁🎂☕🏃🧘💪🎵🎶📚✏️🖊️📖🎮🗓️'.split('').filter(function(c){return c.charCodeAt(0)>127;});

/* ═══════════════════════════
   INIT
═══════════════════════════ */
(function init(){
  var h = new Date().getHours();
  var g = h<12?'Good morning':h<17?'Good afternoon':'Good evening';

  /* Load any previously saved settings first */
  loadSettings();

  /* If no saved greeting, use time-based default */
  if (!S.greeting || S.greeting === 'Good morning' && !localStorage.getItem('essenceloved_settings')) {
    S.greeting = g;
  }
  document.getElementById('s-greet').value = S.greeting;

  document.getElementById('header-date').textContent =
    new Date().toLocaleDateString('en-US',{month:'short',day:'numeric'});
  document.getElementById('greet-s').textContent =
    new Date().toLocaleDateString('en-US',{weekday:'long',month:'long',day:'numeric',year:'numeric'});

  applyS();
  /* Apply colour and dark mode from loaded/default state */
  setAccent(S.accent);
  setShadow(S.shadowColor);
  if (S.dm) applyDM(true);
  /* Force labels onto all pages on first load */
  applyLabels();
  applyNavLabels();
  renderStrip(); renderFeed(); renderNotes(); renderGallery(); renderCalendar(); renderDone();

  remTimer = setInterval(openRemind, 30*60*1000);
  setTimeout(openRemind, 5000);
})();

/* ═══════════════════════════
   NAVIGATION
═══════════════════════════ */
function goPage(name, btn) {
  document.querySelectorAll('.page').forEach(function(p){ p.classList.remove('active'); });
  document.getElementById('page-' + name).classList.add('active');
  document.querySelectorAll('.ntab').forEach(function(b){ b.classList.remove('active'); });
  btn.classList.add('active');

  /* Always re-apply labels so page titles stay in sync */
  applyLabels();
  applyNavLabels();

  if (name === 'settings') {
    /* Sync input fields to current S state before building */
    var sn = document.getElementById('s-name');
    var sg = document.getElementById('s-greet');
    var sf = document.getElementById('s-font');
    if (sn) sn.value = S.username;
    if (sg) sg.value = S.greeting;
    if (sf) sf.value = S.font;
    buildSettingsUI();
  }
}

/* ═══════════════════════════
   TASKS
═══════════════════════════ */
/* ─── track whether we're editing an existing task ─── */
var editingTaskId = null;

function openTaskModal() {
  editingTaskId = null;
  tmMedia = null; tmSubs = [];
  document.getElementById('tm-txt').value = '';
  document.getElementById('tm-tag').value = 'personal';
  document.getElementById('tm-att-lbl').textContent = 'Attach photo, GIF or video';
  document.getElementById('tm-med-wrap').style.display = 'none';
  document.getElementById('tm-med-slot').innerHTML = '';
  document.getElementById('tm-del-btn').style.display = 'none';
  document.getElementById('tm-save-btn').textContent = 'Add Task';
  document.querySelector('#task-modal .m-ttl') && (document.querySelector('#task-modal .m-ttl').textContent = '✏️ New Task');
  renderSbList();
  document.getElementById('sb-inp').value = '';
  openModal('task-modal');
  setTimeout(function(){ document.getElementById('tm-txt').focus(); }, 80);
}

function editTask(id) {
  var t = tasks.find(function(x){ return x.id === id; });
  if (!t) return;
  editingTaskId = id;
  tmSubs = t.subs.map(function(s){ return Object.assign({}, s); }); /* copy */
  tmMedia = t.media;

  document.getElementById('tm-txt').value = t.text;
  document.getElementById('tm-tag').value = t.tag;
  document.getElementById('tm-del-btn').style.display = 'inline-flex';
  document.getElementById('tm-save-btn').textContent = 'Save Changes';

  /* show existing media if any */
  if (t.media) {
    document.getElementById('tm-att-lbl').textContent = t.media.name || 'Attached';
    document.getElementById('tm-med-slot').innerHTML = t.media.type === 'video'
      ? '<video src="'+t.media.url+'" controls style="width:100%;max-height:140px;border-radius:9px"></video>'
      : '<img src="'+t.media.url+'" style="width:100%;max-height:140px;object-fit:cover;border-radius:9px">';
    document.getElementById('tm-med-wrap').style.display = 'block';
  } else {
    document.getElementById('tm-att-lbl').textContent = 'Attach photo, GIF or video';
    document.getElementById('tm-med-wrap').style.display = 'none';
    document.getElementById('tm-med-slot').innerHTML = '';
  }

  renderSbList();
  document.getElementById('sb-inp').value = '';
  openModal('task-modal');
  setTimeout(function(){ document.getElementById('tm-txt').focus(); }, 80);
}

function deleteTask() {
  if (!editingTaskId) return;
  if (!confirm('Delete this task?')) return;
  tasks = tasks.filter(function(x){ return x.id !== editingTaskId; });
  closeModal('task-modal');
  editingTaskId = null;
  renderStrip(); renderFeed();
}

/* ─── sub-task list in modal ─── */
function renderSbList() {
  document.getElementById('sb-list').innerHTML = tmSubs.map(function(s, i) {
    return '<div class="sb-item">'+
      /* checkbox — toggles done state while editing */
      '<div class="sb-chk'+(s.done?' sb-chk-done':'')+'" onclick="toggleTmSub('+s.id+')">'+
        (s.done ? '✓' : '') +
      '</div>'+
      /* editable text */
      '<input class="sb-edit-inp'+(s.done?' sb-done-txt':'')+'" value="'+s.text+'" '+
        'onchange="tmSubs['+i+'].text=this.value" '+
        'onkeydown="if(event.key===\'Enter\'){event.preventDefault();document.getElementById(\'sb-inp\').focus();}">'+
      /* delete */
      '<button class="sb-del" onclick="rmSub('+s.id+')">✕</button>'+
      '</div>';
  }).join('');
}

function toggleTmSub(sid) {
  var s = tmSubs.find(function(x){ return x.id === sid; });
  if (s) s.done = !s.done;
  renderSbList();
}

function addSub() {
  var inp = document.getElementById('sb-inp'), t = inp.value.trim();
  if (!t) return;
  tmSubs.push({ id: Date.now() + (Math.random()*1000|0), text: t, done: false });
  inp.value = '';
  renderSbList();
  inp.focus();
}

function rmSub(sid) {
  tmSubs = tmSubs.filter(function(s){ return s.id !== sid; });
  renderSbList();
}

function saveTask() {
  var text = document.getElementById('tm-txt').value.trim();
  if (!text) return;
  var tag  = document.getElementById('tm-tag').value;

  if (editingTaskId) {
    /* update existing */
    var t = tasks.find(function(x){ return x.id === editingTaskId; });
    if (t) {
      t.text  = text;
      t.tag   = tag;
      t.media = tmMedia;
      t.subs  = tmSubs.slice();
      /* if all subs now done, trigger complete flow */
      var allDone = t.subs.length > 0 && t.subs.every(function(s){ return s.done; });
      closeModal('task-modal');
      editingTaskId = null;
      if (allDone) { startComp(t.id); } else { renderStrip(); renderFeed(); }
    }
  } else {
    /* create new */
    tasks.unshift({ id: Date.now(), text: text, tag: tag,
      media: tmMedia, doneMedia: null, completedAt: null, subs: tmSubs.slice() });
    closeModal('task-modal');
    editingTaskId = null;
    renderStrip(); renderFeed();
  }
}

function toggleSub(tid, sid) {
  var t = tasks.find(function(x){ return x.id === tid; });
  if (!t) return;
  var s = t.subs.find(function(x){ return x.id === sid; });
  if (s) s.done = !s.done;

  var allDone = t.subs.length > 0 && t.subs.every(function(x){ return x.done; });
  if (allDone) {
    /* close dropdown then trigger complete flow */
    var dd = document.getElementById('floating-dd');
    if (dd) dd.classList.remove('open');
    openDDTaskId = null;
    startComp(tid);
  } else {
    renderStrip();
    /* re-render dropdown if still open for this task */
    if (openDDTaskId === tid) renderDD(tid);
  }
}

var openDDTaskId = null;

function toggleDD(tid) {
  var dd = document.getElementById('floating-dd');
  if (!dd) return;

  if (openDDTaskId === tid && dd.classList.contains('open')) {
    dd.classList.remove('open');
    var oldArr = document.getElementById('arr-' + openDDTaskId);
    if (oldArr) oldArr.classList.remove('open');
    openDDTaskId = null;
    return;
  }

  if (openDDTaskId) {
    var prevArr = document.getElementById('arr-' + openDDTaskId);
    if (prevArr) prevArr.classList.remove('open');
  }

  openDDTaskId = tid;
  var arr = document.getElementById('arr-' + tid);
  if (arr) arr.classList.add('open');

  renderDD(tid);

  var pill = document.getElementById('pill-' + tid);
  if (pill) {
    var r = pill.getBoundingClientRect();
    dd.style.top  = (r.bottom + 6) + 'px';
    dd.style.left = Math.min(r.left, window.innerWidth - 240) + 'px';
  }

  dd.classList.add('open');
}

function renderDD(tid) {
  var t  = tasks.find(function(x){ return x.id === tid; });
  var dd = document.getElementById('floating-dd');
  if (!t || !dd) return;
  var dc  = t.subs.filter(function(s){ return s.done; }).length;
  var pct = t.subs.length ? Math.round(dc / t.subs.length * 100) : 0;

  var subsHtml = t.subs.length
    ? t.subs.map(function(s) {
        return '<div class="sub-item' + (s.done ? ' done' : '') + '" onclick="toggleSub(' + tid + ',' + s.id + ')">' +
          '<div class="si-chk">' + (s.done ? '✓' : '') + '</div>' +
          '<span class="si-txt">' + s.text + '</span>' +
          '</div>';
      }).join('')
    : '<div style="font-size:12px;color:var(--gray);padding:4px 2px">No items yet — add one below!</div>';

  var progressHtml = t.subs.length
    ? '<div class="prog-bg"><div class="prog-bar" style="width:' + pct + '%"></div></div>' +
      '<div class="prog-lbl">' + dc + ' / ' + t.subs.length + ' done</div>'
    : '';

  dd.innerHTML =
    '<div class="sub-drop-ttl">📋 ' + t.text + '</div>' +
    subsHtml +
    progressHtml +
    /* inline add row */
    '<div class="dd-add-row">' +
      '<input class="dd-add-inp" id="dd-add-inp-' + tid + '" placeholder="Add item…" ' +
        'onkeydown="if(event.key===\'Enter\'){event.preventDefault();ddAddItem(' + tid + ')}">' +
      '<button class="dd-add-btn" onclick="ddAddItem(' + tid + ')">+</button>' +
    '</div>';

  /* focus the input after a short delay */
  setTimeout(function() {
    var inp = document.getElementById('dd-add-inp-' + tid);
    if (inp) inp.focus();
  }, 50);
}

function ddAddItem(tid) {
  var inp = document.getElementById('dd-add-inp-' + tid);
  if (!inp) return;
  var text = inp.value.trim();
  if (!text) return;
  var t = tasks.find(function(x){ return x.id === tid; });
  if (!t) return;
  t.subs.push({ id: Date.now() + (Math.random() * 1000 | 0), text: text, done: false });
  inp.value = '';
  renderStrip();
  renderDD(tid); /* re-render dropdown with new item */
  /* re-focus the input */
  setTimeout(function() {
    var newInp = document.getElementById('dd-add-inp-' + tid);
    if (newInp) newInp.focus();
  }, 30);
}

document.addEventListener('click', function(e) {
  if (!e.target.closest('.strip-wrap') && !e.target.closest('#floating-dd')) {
    var dd = document.getElementById('floating-dd');
    if (dd) dd.classList.remove('open');
    if (openDDTaskId) {
      var arr = document.getElementById('arr-' + openDDTaskId);
      if (arr) arr.classList.remove('open');
      openDDTaskId = null;
    }
  }
});

function startComp(id) {
  completingId=id; cmMedia=null;
  document.getElementById('cm-att-lbl').textContent='Attach celebration media (optional)';
  document.getElementById('cm-med-wrap').style.display='none';
  document.getElementById('cm-med-slot').innerHTML='';
  openModal('comp-modal');
}

function closeComp(save) {
  if(completingId){
    var t=tasks.find(function(x){return x.id===completingId;});
    if(t){
      if(save&&cmMedia) t.doneMedia=cmMedia;
      t.completedAt=new Date().toLocaleDateString('en-US',{month:'short',day:'numeric',hour:'2-digit',minute:'2-digit'});
      doneTasks.unshift(t);
      tasks=tasks.filter(function(x){return x.id!==completingId;});
    }
  }
  closeModal('comp-modal');
  completingId=null; cmMedia=null;
  renderStrip(); renderFeed(); renderDone();
}

/* ═══════════════════════════
   RENDER STRIP
═══════════════════════════ */
function renderStrip() {
  var el = document.getElementById('strip-row');

  /* Remove any existing floating dropdowns */
  document.querySelectorAll('.sub-drop').forEach(function(d){ d.remove(); });

  if (!tasks.length) {
    el.innerHTML = '<div style="font-size:13px;color:var(--gray);font-weight:600;padding:5px 0">All done! 🎉 Check the Done tab.</div>';
    return;
  }

  el.innerHTML = tasks.map(function(t) {
    var dc      = t.subs.filter(function(s){ return s.done; }).length;
    var hasSubs = t.subs.length > 0;
    var prog    = hasSubs ? '<span class="s-prog">'+dc+'/'+t.subs.length+'</span>' : '';
    var arr     = hasSubs ? '<button class="s-arr" id="arr-'+t.id+'" onclick="event.stopPropagation();toggleDD('+t.id+')" title="Show checklist">▾</button>' : '';
    var thumb   = t.media && t.media.type==='image' ? '<img class="s-thumb" src="'+t.media.url+'">' : '';
    var click   = hasSubs ? 'toggleDD('+t.id+')' : 'startComp('+t.id+')';
    return '<div class="strip-wrap" id="sw-'+t.id+'">'+
      '<div class="s-pill" onclick="'+click+'" id="pill-'+t.id+'">'+
        '<div class="s-dot"></div>'+
        '<span class="s-txt">'+t.text+'</span>'+
        '<span class="s-tag tag-'+t.tag+'">'+t.tag+'</span>'+
        prog + thumb + arr +
        '<button class="s-edit" onclick="event.stopPropagation();editTask('+t.id+')" title="Edit">✏️</button>'+
      '</div>'+
    '</div>';
  }).join('');

  /* Create one shared floating dropdown div appended to body */
  var dd = document.createElement('div');
  dd.className = 'sub-drop';
  dd.id = 'floating-dd';
  dd.addEventListener('click', function(e){ e.stopPropagation(); });
  document.body.appendChild(dd);
}

/* ═══════════════════════════
   HOME FEED
═══════════════════════════ */
function renderFeed() {
  /* Task */
  var te=document.getElementById('feed-task'), t=tasks[0];
  if(t){
    var mh='';
    if(t.media) mh='<div class="media-prev">'+(t.media.type==='video'?'<video src="'+t.media.url+'" controls></video>':'<img src="'+t.media.url+'">')+'</div>';
    if(t.doneMedia) mh+='<div class="done-lbl">🎉 Completion</div><div class="media-prev">'+(t.doneMedia.type==='video'?'<video src="'+t.doneMedia.url+'" controls></video>':'<img src="'+t.doneMedia.url+'">')+'</div>';
    te.innerHTML='<div class="feed-card"><div class="fc-body"><div class="fc-row"><div class="fc-chk"></div><span class="fc-txt">'+t.text+'</span><span class="fc-tag tag-'+t.tag+'">'+t.tag+'</span></div>'+mh+'</div></div>';
  } else { te.innerHTML='<div class="no-item">No tasks yet ✅</div>'; }

  /* Note */
  var ne=document.getElementById('feed-note'), n=notes[0];
  if(n){
    var nbg=S.sectionImgs['note-'+n.id]?'background-image:url('+S.sectionImgs['note-'+n.id]+');':'';
    ne.innerHTML='<div class="feed-card note-card nc'+(n.color%6)+'" style="'+nbg+'"><div class="n-ttl">'+n.title+'</div><div class="n-bod">'+n.body+'</div><div class="n-dt">'+n.date+'</div></div>';
  } else { ne.innerHTML='<div class="no-item">No notes yet 📝</div>'; }

  /* Photo */
  var pe=document.getElementById('feed-photo'), p=photos[photos.length-1];
  if(p){ pe.innerHTML='<div class="feed-card"><img style="width:100%;max-height:200px;object-fit:cover;display:block" src="'+p.url+'"><div style="padding:8px 12px;font-size:13px;font-weight:700;color:var(--gray)">📷 '+p.name+'</div></div>'; }
  else { pe.innerHTML='<div class="no-item">No photos yet 📸</div>'; }
}

/* ═══════════════════════════
   GALLERY
═══════════════════════════ */
function loadPhotos(e) {
  Array.from(e.target.files).forEach(function(f){
    var r=new FileReader();
    r.onload=function(ev){ photos.push({url:ev.target.result,name:f.name.replace(/\.[^.]+$/,'')}); renderGallery(); renderFeed(); };
    r.readAsDataURL(f);
  });
}
function renderGallery() {
  var g=document.getElementById('photo-grid');
  if(!photos.length){ g.innerHTML='<div style="grid-column:1/-1;text-align:center;color:var(--gray);font-weight:700;padding:16px">No photos yet 🌸</div>'; return; }
  g.innerHTML=photos.map(function(p){ return '<div class="photo-wrap"><img src="'+p.url+'" alt="'+p.name+'"><div class="photo-nm">'+p.name+'</div></div>'; }).join('');
}

/* ═══════════════════════════
   NOTES
═══════════════════════════ */
function renderNotes() {
  var g=document.getElementById('notes-grid');
  if(!notes.length){ g.innerHTML='<div style="color:var(--gray);font-size:14px;font-weight:700">No notes yet 📝</div>'; return; }
  g.innerHTML=notes.map(function(n){
    var k='note-'+n.id, hasBg=S.sectionImgs[k]?' has-img':'', bg=S.sectionImgs[k]?'background-image:url('+S.sectionImgs[k]+');':'';
    return '<div class="note-card nc'+(n.color%6)+hasBg+'" style="'+bg+'" onclick="openNote('+n.id+')"><div class="n-ttl">'+n.title+'</div><div class="n-bod">'+n.body+'</div><div class="n-dt">'+n.date+'</div></div>';
  }).join('');
}
function openNote(id) {
  noteEditId = id;
  var ttlEl = document.getElementById('note-modal-ttl');
  if (id) {
    var n = notes.find(function(x){ return x.id === id; });
    document.getElementById('note-ttl-inp').value = n.title;
    document.getElementById('note-bod-inp').value  = n.body;
    if (ttlEl) ttlEl.textContent = '✏️ Edit Note';
  } else {
    document.getElementById('note-ttl-inp').value = '';
    document.getElementById('note-bod-inp').value  = '';
    if (ttlEl) ttlEl.textContent = '📝 New Note';
  }
  openModal('note-modal');
  setTimeout(function(){ document.getElementById('note-ttl-inp').focus(); }, 80);
}
function saveNote() {
  var title=document.getElementById('note-ttl-inp').value.trim()||'Untitled';
  var body=document.getElementById('note-bod-inp').value.trim();
  var date=new Date().toLocaleDateString('en-US',{month:'short',day:'numeric'});
  if(noteEditId){ var n=notes.find(function(x){return x.id===noteEditId;}); n.title=title; n.body=body; n.date=date; }
  else notes.unshift({id:Date.now(),title,body,color:noteColorIdx++,date});
  renderNotes(); renderFeed(); closeModal('note-modal');
}

/* ═══════════════════════════
   CALENDAR
═══════════════════════════ */
function renderCalendar() {
  document.getElementById('cal-lbl').textContent=MONTHS[calM]+' '+calY;
  var fd=new Date(calY,calM,1).getDay(), dm=new Date(calY,calM+1,0).getDate(), pd=new Date(calY,calM,0).getDate();
  var today=new Date();
  function isToday(d){return d===today.getDate()&&calM===today.getMonth()&&calY===today.getFullYear();}
  var h=WDAYS.map(function(d){return '<div class="dn">'+d+'</div>';}).join('');
  for(var i=0;i<fd;i++) h+='<button class="dc om">'+(pd-fd+1+i)+'</button>';
  for(var d=1;d<=dm;d++){
    var k=calY+'-'+(calM+1)+'-'+d, cls='dc';
    if(isToday(d)) cls+=' td'; else if(d===selD) cls+=' sl';
    if(calEvs[k]&&calEvs[k].length) cls+=' he';
    h+='<button class="'+cls+'" onclick="pickDay('+d+')">'+d+'</button>';
  }
  document.getElementById('cal-grid').innerHTML=h;
  renderEvents();
}
function pickDay(d){selD=d;renderCalendar();}
function moveCal(dir){calM+=dir; if(calM<0){calM=11;calY--;}if(calM>11){calM=0;calY++;} renderCalendar();}
function renderEvents(){
  var k=calY+'-'+(calM+1)+'-'+selD, list=calEvs[k]||[];
  document.getElementById('ev-hd').textContent=MONTHS[calM]+' '+selD;
  if(!list.length){document.getElementById('ev-list').innerHTML='<div class="no-ev">No events yet!</div>';return;}
  document.getElementById('ev-list').innerHTML=list.map(function(ev,i){
    return '<div class="ev-row"><div class="ev-dot" style="background:'+DOT[i%DOT.length]+'"></div><div><div class="ev-nm">'+ev.name+'</div><div class="ev-tm">'+ev.time+'</div></div></div>';
  }).join('');
}
function addEvent(){
  var name=document.getElementById('ev-inp').value.trim(), time=document.getElementById('ev-time').value;
  if(!name)return;
  var k=calY+'-'+(calM+1)+'-'+selD;
  if(!calEvs[k])calEvs[k]=[];
  calEvs[k].push({name,time:time||'All day'});
  document.getElementById('ev-inp').value=''; document.getElementById('ev-time').value='';
  renderCalendar();
}

/* ═══════════════════════════
   COMPLETED
═══════════════════════════ */
function renderDone() {
  var el=document.getElementById('done-list');
  if(!doneTasks.length){ el.innerHTML='<div style="text-align:center;color:var(--gray);font-size:14px;font-weight:700;padding:40px 20px">No completed tasks yet.<br>Check things off to see them here! 🌸</div>'; return; }
  el.innerHTML=doneTasks.map(function(t){
    var subs=t.subs&&t.subs.length?'<div class="dc-subs">'+t.subs.map(function(s){return '<span class="dc-sub">✓ '+s.text+'</span>';}).join('')+'</div>':'';
    var med=t.doneMedia?'<div class="dc-med">'+(t.doneMedia.type==='video'?'<video src="'+t.doneMedia.url+'" controls></video>':'<img src="'+t.doneMedia.url+'">')+'</div>':'';
    return '<div class="done-card">'+
      '<div class="dc-top"><span style="font-size:18px">✅</span><span class="dc-txt">'+t.text+'</span><span class="s-tag tag-'+t.tag+'">'+t.tag+'</span></div>'+
      (t.completedAt?'<div class="dc-dt">Completed '+t.completedAt+'</div>':'')+
      subs+med+
      '<button class="restore-btn" onclick="restoreTask('+t.id+')">↩ Restore</button>'+
      '</div>';
  }).join('');
}
function restoreTask(id){
  var idx=doneTasks.findIndex(function(t){return t.id===id;});
  if(idx===-1)return;
  var t=doneTasks.splice(idx,1)[0];
  t.doneMedia=null; t.completedAt=null; t.subs.forEach(function(s){s.done=false;});
  tasks.unshift(t); renderStrip(); renderFeed(); renderDone();
}
function clearCompleted(){
  if(!doneTasks.length)return;
  if(confirm('Clear all '+doneTasks.length+' completed tasks?')){ doneTasks=[]; renderDone(); }
}

/* ═══════════════════════════
   30-MIN POPUP
═══════════════════════════ */
function launchConfetti(){
  var a=document.getElementById('conf-area'); a.innerHTML='';
  for(var i=0;i<26;i++){
    var p=document.createElement('div'); p.className='conf-p';
    p.style.left=Math.random()*100+'%';
    p.style.background=CONF_CLR[Math.floor(Math.random()*CONF_CLR.length)];
    p.style.animationDelay=(Math.random()*0.8)+'s';
    p.style.animationDuration=(1.2+Math.random()*0.8)+'s';
    a.appendChild(p);
  }
}
function openRemind(){
  var total=tasks.length+doneTasks.length, done=doneTasks.length;
  var pct=total?Math.round(done/total*100):0;
  document.getElementById('rem-em').textContent=pct===100?'🏆':pct>=50?'🔥':'⏰';
  document.getElementById('rem-ttl').textContent=pct===100?'All done! You crushed it!':pct>=50?"You're on a roll!":'Task Check-in!';
  document.getElementById('rem-score').textContent=total?done+' of '+total+' done ('+pct+'%)':'';
  if(pct>=50)launchConfetti();
  document.getElementById('rem-list').innerHTML=tasks.length
    ? tasks.map(function(t){
        var sub=t.subs.length?' ('+t.subs.filter(function(s){return s.done;}).length+'/'+t.subs.length+' sub-tasks)':'';
        return '<div class="rem-item" onclick="closeRemind();toggleDD('+t.id+')"><div class="rem-chk"></div><span class="rem-txt">'+t.text+sub+'</span></div>';
      }).join('')
    : '<div style="text-align:center;padding:10px;color:var(--green);font-weight:700">🎉 All complete!</div>';
  document.getElementById('remind').classList.add('open');
}
function closeRemind(){document.getElementById('remind').classList.remove('open');}
function applyFreq(){
  var v=parseInt(document.getElementById('s-freq').value); S.remMins=v;
  if(remTimer){clearInterval(remTimer);remTimer=null;}
  if(v>0)remTimer=setInterval(openRemind,v*60*1000);
}

/* ═══════════════════════════
   MEDIA HELPERS
═══════════════════════════ */
function prevMedia(e,prefix){
  var f=e.target.files[0]; if(!f)return;
  var isVid=f.type.indexOf('video')===0;
  var r=new FileReader();
  r.onload=function(ev){
    var data={url:ev.target.result,type:isVid?'video':'image',name:f.name};
    if(prefix==='tm')tmMedia=data; else cmMedia=data;
    document.getElementById(prefix+'-med-slot').innerHTML=isVid
      ?'<video src="'+ev.target.result+'" controls style="width:100%;max-height:140px;border-radius:9px"></video>'
      :'<img src="'+ev.target.result+'" style="width:100%;max-height:140px;object-fit:cover;border-radius:9px">';
    var lbl=document.getElementById(prefix+'-att-lbl'); if(lbl)lbl.textContent=f.name;
    var badge=document.getElementById(prefix+'-badge'); if(badge)badge.textContent=isVid?'🎬 Video':f.name.toLowerCase().includes('.gif')?'🎞️ GIF':'🖼️ Image';
    document.getElementById(prefix+'-med-wrap').style.display='block';
  };
  r.readAsDataURL(f); e.target.value='';
}
function rmMedia(prefix){
  if(prefix==='tm')tmMedia=null; else cmMedia=null;
  document.getElementById(prefix+'-med-slot').innerHTML='';
  document.getElementById(prefix+'-med-wrap').style.display='none';
  var lbl=document.getElementById(prefix+'-att-lbl');
  if(lbl)lbl.textContent=prefix==='tm'?'Attach photo, GIF or video':'Attach celebration media (optional)';
}

/* ═══════════════════════════
   MODAL HELPERS
═══════════════════════════ */
function openModal(id){document.getElementById(id).classList.add('open');}
function closeModal(id){
  document.getElementById(id).classList.remove('open');
  if(id==='note-modal')noteEditId=null;
}
['task-modal','comp-modal','note-modal'].forEach(function(id){
  document.getElementById(id).addEventListener('click',function(e){if(e.target===this)closeModal(id);});
});

/* ═══════════════════════════
   SETTINGS — APPLY
═══════════════════════════ */
function applyS(){
  S.username=document.getElementById('s-name').value||'';
  S.greeting=document.getElementById('s-greet').value||'Good morning';
  S.font=document.getElementById('s-font').value;

  /* Username pill */
  var up=document.getElementById('user-pill');
  if(S.username){up.textContent='👤 '+S.username; up.style.display='inline-block';}
  else up.style.display='none';

  /* Greeting */
  document.getElementById('greet-h').textContent=S.greeting+(S.username?', '+S.username:'')+' 🌸';

  /* Font */
  document.body.style.fontFamily="'"+S.font+"',sans-serif";

  /* Wallpaper */
  document.body.style.backgroundImage=S.wallpaper?'url('+S.wallpaper+')':'';
  document.body.style.backgroundSize='cover';
  document.body.style.backgroundPosition='center';

  applyLabels();
  applyNavLabels();
}

function applyLabels(){
  var L=S.labels;
  function t(id,val){var el=document.getElementById(id);if(el)el.textContent=val;}
  t('strip-lbl-el', L['strip'].icon+' '+L['strip'].text);
  t('ft-lbl',       L['feed-task'].icon+' '+L['feed-task'].text);
  t('fn-lbl',       L['feed-note'].icon+' '+L['feed-note'].text);
  t('fp-lbl',       L['feed-photo'].icon+' '+L['feed-photo'].text);
  t('add-icon',     L['add-task'].icon);
  t('add-lbl',      L['add-task'].text);
  var gallTtl=document.getElementById('gallery-ttl'); if(gallTtl) gallTtl.textContent=L['gallery'].icon+' '+L['gallery'].text;
  var notesTtl=document.getElementById('notes-ttl'); if(notesTtl) notesTtl.textContent=L['notes'].icon+' '+L['notes'].text;
  var calTtl=document.getElementById('cal-ttl'); if(calTtl) calTtl.textContent=L['calendar'].icon+' '+L['calendar'].text;
}

function applyNavLabels(){
  NAV_DEFS.forEach(function(id){
    var ni=document.getElementById('ni-'+id), nl=document.getElementById('nl-'+id);
    if(ni)ni.textContent=S.navLabels[id].icon;
    if(nl)nl.textContent=S.navLabels[id].text;
  });
}

function applyDM(on){ S.dm=on; document.body.classList.toggle('dm',on); }

function setAccent(val){
  S.accent=val;
  document.documentElement.style.setProperty('--accent',val);
  var chip=document.getElementById('acc-chip'), hex=document.getElementById('acc-hex');
  if(chip)chip.style.background=val;
  if(hex)hex.value=val.toUpperCase();
  document.querySelector('#app-name span').style.color=val;
}

function setShadow(val){
  S.shadowColor=val;
  var chip=document.getElementById('sh-chip'), hex=document.getElementById('sh-hex');
  if(chip)chip.style.background=val;
  if(hex)hex.value=val.toUpperCase();
  applyShadow();
}

function applyShadow(){
  var on=document.getElementById('s-sh-on'), sl=document.getElementById('sh-op'), pct=document.getElementById('sh-pct');
  var op=sl?parseInt(sl.value):8;
  if(pct)pct.textContent=op+'%';
  if(!on||!on.checked){document.documentElement.style.setProperty('--shadow','none');return;}
  var c=S.shadowColor||'#000000';
  var r=parseInt(c.slice(1,3),16), g=parseInt(c.slice(3,5),16), b=parseInt(c.slice(5,7),16);
  document.documentElement.style.setProperty('--shadow','0 2px 16px rgba('+r+','+g+','+b+','+(op/100).toFixed(2)+')');
}

/* ═══════════════════════════
   SETTINGS — BUILD UI
═══════════════════════════ */
function buildSettingsUI(){
  buildLblRows(); buildImgRows(); buildNavRows(); buildExpList();
  buildQS('acc-qs',QS_ACC,function(c){setAccent(c);document.getElementById('acc-w').value=c;});
  buildQS('sh-qs',QS_SH,function(c){setShadow(c);document.getElementById('sh-w').value=c;});
  /* sync inputs */
  var aw=document.getElementById('acc-w'); if(aw)aw.value=S.accent;
  var sw=document.getElementById('sh-w'); if(sw)sw.value=S.shadowColor||'#000000';
  var dm=document.getElementById('s-dm'); if(dm)dm.checked=S.dm;
  var rf=document.getElementById('s-freq'); if(rf)rf.value=String(S.remMins);
  buildEmojiPicker();
}

function buildQS(elId,colors,cb){
  var el=document.getElementById(elId); if(!el)return;
  el.innerHTML=colors.map(function(c){
    return '<div class="qs" style="background:'+c+';border:1px solid #ccc" onclick="('+cb.toString()+')(\''+c+'\')" title="'+c+'"></div>';
  }).join('');
}

function buildLblRows(){
  document.getElementById('lbl-rows').innerHTML=LBL_DEFS.map(function(d){
    var L=S.labels[d.id];
    return '<div class="sett-row">'+
      '<div class="sett-ico">'+L.icon+'</div>'+
      '<div style="flex:1"><div class="sett-lbl">'+d.title+'</div></div>'+
      '<div class="sett-right">'+
        '<button class="e-btn" onclick="openEmoji(event,\'L:'+d.id+'\')">'+L.icon+'</button>'+
        '<input class="s-inp" style="width:110px" value="'+L.text+'" oninput="S.labels[\''+d.id+'\'].text=this.value;applyLabels()">'+
      '</div></div>';
  }).join('');
}

function buildImgRows(){
  document.getElementById('img-rows').innerHTML=IMG_TARGETS.map(function(t){
    var img=S.sectionImgs[t.id];
    var prev=img?'<img class="s-img-prev" src="'+img+'">':'<span style="font-size:16px">🖼️</span>';
    return '<div class="sett-row">'+
      '<div class="sett-ico">🖼️</div>'+
      '<div style="flex:1"><div class="sett-lbl">'+t.label+'</div></div>'+
      '<div class="sett-right">'+prev+
        '<button class="up-btn" onclick="triggerImg(\''+t.id+'\')">📁 Upload</button>'+
        '<button class="clr-btn" onclick="clearImg(\''+t.id+'\')">✕</button>'+
      '</div></div>';
  }).join('');
}

function buildNavRows(){
  document.getElementById('nav-rows').innerHTML=NAV_DEFS.map(function(id){
    var N=S.navLabels[id];
    return '<div class="sett-row">'+
      '<div class="sett-ico">'+N.icon+'</div>'+
      '<div style="flex:1"><div class="sett-lbl">'+id.charAt(0).toUpperCase()+id.slice(1)+' Tab</div></div>'+
      '<div class="sett-right">'+
        '<button class="e-btn" onclick="openEmoji(event,\'N:'+id+'\')">'+N.icon+'</button>'+
        '<input class="s-inp" style="width:80px" value="'+N.text+'" oninput="S.navLabels[\''+id+'\'].text=this.value;applyNavLabels()">'+
      '</div></div>';
  }).join('');
}

/* ═══════════════════════════
   IMAGE UPLOAD (settings)
═══════════════════════════ */
var settImgPending=null;
function triggerImg(id){ settImgPending=id; var f=document.getElementById('sett-file'); f.value=''; f.click(); }
document.getElementById('sett-file').addEventListener('change',function(e){
  var f=e.target.files[0]; if(!f||!settImgPending)return;
  var id=settImgPending; settImgPending=null;
  var r=new FileReader();
  r.onload=function(ev){
    var url=ev.target.result;
    if(id==='wp'){
      S.wallpaper=url;
      var wp=document.getElementById('wp-prev');
      if(wp){wp.innerHTML='';wp.style.backgroundImage='url('+url+')';wp.style.backgroundSize='cover';}
      applyS();
    } else {
      S.sectionImgs[id]=url;
      var el=document.getElementById(id);
      if(el){el.style.backgroundImage='url('+url+')';el.style.backgroundSize='cover';el.style.backgroundPosition='center';el.classList.add('has-img');}
      if(id.indexOf('note-')===0){renderNotes();renderFeed();}
      buildImgRows();
    }
  };
  r.readAsDataURL(f);
});
function clearImg(id){
  if(id==='wp'){
    S.wallpaper=null; document.body.style.backgroundImage='';
    var wp=document.getElementById('wp-prev'); if(wp){wp.style.backgroundImage='';wp.innerHTML='🌅';}
  } else {
    delete S.sectionImgs[id];
    var el=document.getElementById(id); if(el){el.style.backgroundImage='';el.classList.remove('has-img');}
    if(id.indexOf('note-')===0){renderNotes();renderFeed();}
    buildImgRows();
  }
}

/* ═══════════════════════════
   EMOJI PICKER
═══════════════════════════ */
var emojiTarget=null;
function buildEmojiPicker(){
  document.getElementById('ep-grid').innerHTML=EMOJIS.map(function(em){
    return '<div class="ep" onclick="pickEmoji(\''+em+'\')">'+em+'</div>';
  }).join('');
}
function openEmoji(e,target){
  e.stopPropagation(); emojiTarget=target;
  var p=document.getElementById('epick');
  var r=e.currentTarget.getBoundingClientRect();
  p.style.top=(r.bottom+4)+'px'; p.style.left=Math.max(6,r.left-80)+'px';
  p.classList.add('open');
}
function pickEmoji(em){
  var p=document.getElementById('epick'); p.classList.remove('open');
  if(!emojiTarget)return;
  if(emojiTarget.indexOf('L:')===0){ var id=emojiTarget.slice(2); S.labels[id].icon=em; applyLabels(); buildLblRows(); }
  if(emojiTarget.indexOf('N:')===0){ var id=emojiTarget.slice(2); S.navLabels[id].icon=em; applyNavLabels(); buildNavRows(); }
  emojiTarget=null;
}
document.addEventListener('click',function(){document.getElementById('epick').classList.remove('open');});

/* ═══════════════════════════
   EXPORT
═══════════════════════════ */
function buildExpList(){
  var items=[];
  tasks.forEach(function(t){items.push({key:'t-'+t.id,icon:'📋',text:t.text,type:'Task'});});
  doneTasks.forEach(function(t){items.push({key:'d-'+t.id,icon:'✅',text:t.text,type:'Done'});});
  notes.forEach(function(n){items.push({key:'n-'+n.id,icon:'📝',text:n.title,type:'Note'});});
  photos.forEach(function(p,i){items.push({key:'p-'+i,icon:'📸',text:p.name,type:'Photo'});});
  var el=document.getElementById('exp-list');
  if(!items.length){el.innerHTML='<div style="color:var(--gray);font-size:13px;font-weight:600;padding:6px 0">Nothing to export yet.</div>';return;}
  el.innerHTML=items.map(function(it){
    var sel=expSel[it.key];
    return '<div class="exp-item'+(sel?' sel':'')+'" onclick="togExp(\''+it.key+'\')" id="ei-'+it.key+'">'+
      '<div class="exp-chk" id="ec-'+it.key+'">'+(sel?'✓':'')+'</div>'+
      '<span class="exp-ico">'+it.icon+'</span>'+
      '<span class="exp-txt">'+it.text+'</span>'+
      '<span class="exp-typ">'+it.type+'</span>'+
      '</div>';
  }).join('');
}
function togExp(key){
  expSel[key]=!expSel[key];
  var item=document.getElementById('ei-'+key), chk=document.getElementById('ec-'+key);
  if(item)item.classList.toggle('sel',expSel[key]);
  if(chk)chk.textContent=expSel[key]?'✓':'';
}
function selAll(){document.querySelectorAll('.exp-item').forEach(function(el){var k=el.id.replace('ei-','');expSel[k]=true;el.classList.add('sel');var c=document.getElementById('ec-'+k);if(c)c.textContent='✓';});}
function deselAll(){expSel={};document.querySelectorAll('.exp-item').forEach(function(el){el.classList.remove('sel');var k=el.id.replace('ei-','');var c=document.getElementById('ec-'+k);if(c)c.textContent='';});}

function buildExpTxt(){
  var lines=['Essenceloved Export','Generated: '+new Date().toLocaleString(),''];
  var hasT=false,hasD=false,hasN=false,hasP=false;
  Object.keys(expSel).forEach(function(key){
    if(!expSel[key])return;
    if(key.startsWith('t-')){
      var id=parseInt(key.slice(2)),t=tasks.find(function(x){return x.id===id;});
      if(t){if(!hasT){lines.push('=== TASKS ===');hasT=true;} lines.push('[ ] '+t.text+' ('+t.tag+')');}
    }
    if(key.startsWith('d-')){
      var id=parseInt(key.slice(2)),t=doneTasks.find(function(x){return x.id===id;});
      if(t){if(!hasD){lines.push('=== COMPLETED ===');hasD=true;} lines.push('[✓] '+t.text+' ('+t.tag+')');}
    }
    if(key.startsWith('n-')){
      var id=parseInt(key.slice(2)),n=notes.find(function(x){return x.id===id;});
      if(n){if(!hasN){lines.push('','=== NOTES ===');hasN=true;} lines.push('--- '+n.title+' ('+n.date+')'); lines.push(n.body); lines.push('');}
    }
    if(key.startsWith('p-')){
      var i=parseInt(key.slice(2)),p=photos[i];
      if(p){if(!hasP){lines.push('=== PHOTOS ===');hasP=true;} lines.push('📸 '+p.name);}
    }
  });
  return lines.join('\n');
}

function expCount(){return Object.keys(expSel).filter(function(k){return expSel[k];}).length;}
function setExpStatus(msg){var el=document.getElementById('exp-status');if(el){el.textContent=msg;setTimeout(function(){el.textContent='';},4000);}}

function expEmail(){
  var cnt=expCount(); if(!cnt){setExpStatus('⚠️ Select at least one item first.');return;}
  window.location.href='mailto:?subject=Essenceloved Export&body='+encodeURIComponent(buildExpTxt());
  setExpStatus('✅ Opening email with '+cnt+' item(s)…');
}
function expFile(){
  var cnt=expCount(); if(!cnt){setExpStatus('⚠️ Select at least one item first.');return;}
  var blob=new Blob([buildExpTxt()],{type:'text/plain'});
  var a=document.createElement('a'); a.href=URL.createObjectURL(blob); a.download='essenceloved-export.txt'; a.click();
  URL.revokeObjectURL(a.href);
  setExpStatus('✅ File downloaded with '+cnt+' item(s)!');
}

</script>
</body>
</html>
