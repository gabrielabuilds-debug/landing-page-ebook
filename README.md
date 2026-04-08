<!DOCTYPE html>
<html lang="ro">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Pomoja – #unaltfeldeebook</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Fraunces:ital,opsz,wght@0,9..144,300;0,9..144,700;1,9..144,300;1,9..144,700&family=DM+Sans:wght@300;400;500;600;700&display=swap" rel="stylesheet">
<style>
:root{
  --black:#0c0c0a;
  --dark:#141410;
  --card:#1a1a16;
  --border:rgba(255,255,255,0.07);
  --acid:#d4f53c;
  --acid-dim:rgba(212,245,60,0.1);
  --orange:#ff5c2b;
  --red:#e53935;
  --cream:#f4efe4;
  --stone:#bfb9ac;
  --muted:#6b6659;
  --white:#f0ece4;
}
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0}
html{scroll-behavior:smooth}
body{background:var(--black);color:var(--white);font-family:'DM Sans',sans-serif;font-size:17px;line-height:1.65;overflow-x:hidden}
body::after{content:'';position:fixed;inset:0;background-image:url("data:image/svg+xml,%3Csvg viewBox='0 0 200 200' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.85' numOctaves='4'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='0.03'/%3E%3C/svg%3E");pointer-events:none;z-index:9999;opacity:.5}
 
.display{font-family:'Bebas Neue',sans-serif;letter-spacing:.02em;line-height:.95}
.accent{color:var(--acid)}
.hl{background:rgba(212,245,60,0.18);color:var(--acid);padding:1px 6px;border-radius:2px;font-style:normal}
.hl-red{background:rgba(255,92,43,0.12);color:var(--orange);padding:1px 6px;border-radius:2px}
 
.btn{display:inline-block;font-family:'DM Sans',sans-serif;font-weight:700;font-size:.95rem;letter-spacing:.04em;text-transform:uppercase;text-decoration:none;border-radius:3px;cursor:pointer;transition:all .18s;border:none;line-height:1}
.btn-acid{background:var(--acid);color:var(--black);padding:19px 44px}
.btn-acid:hover{background:#bfdc30;transform:translateY(-2px)}
.btn-acid-lg{background:var(--acid);color:var(--black);padding:22px 52px;font-size:1.05rem}
.btn-acid-lg:hover{background:#bfdc30;transform:translateY(-2px)}
.btn-outline{border:1.5px solid var(--acid);color:var(--acid);background:transparent;padding:17px 40px}
.btn-outline:hover{background:var(--acid);color:var(--black)}
 
.wrap{max-width:1040px;margin:0 auto;padding:0 24px}
.wrap-narrow{max-width:680px;margin:0 auto;padding:0 24px}
section{padding:88px 0}
.divider{height:1px;background:linear-gradient(90deg,transparent,rgba(212,245,60,.22),transparent)}
 
.r{opacity:0;transform:translateY(24px);transition:opacity .6s ease,transform .6s ease}
.r.on{opacity:1;transform:none}
.r.d1{transition-delay:.1s}.r.d2{transition-delay:.2s}.r.d3{transition-delay:.3s}.r.d4{transition-delay:.4s}
 
/* ══════════════════════════
   HERO  — 2 cols
══════════════════════════ */
#hero{
  min-height:100vh;padding:72px 0 60px;
  position:relative;overflow:hidden;
  display:flex;align-items:center;
}
#hero::before{content:'';position:absolute;top:-200px;right:-180px;width:700px;height:700px;background:radial-gradient(circle,rgba(212,245,60,.07) 0%,transparent 68%);pointer-events:none}
#hero::after{content:'';position:absolute;bottom:-80px;left:-80px;width:440px;height:440px;background:radial-gradient(circle,rgba(255,92,43,.05) 0%,transparent 65%);pointer-events:none}
 
.hero-grid{display:grid;grid-template-columns:1fr 420px;gap:60px;align-items:center}
@media(max-width:860px){.hero-grid{grid-template-columns:1fr;gap:48px}}
 
.hero-badge{display:inline-flex;align-items:center;gap:9px;background:var(--acid-dim);border:1px solid rgba(212,245,60,.22);color:var(--acid);font-size:.77rem;font-weight:700;letter-spacing:.1em;text-transform:uppercase;padding:8px 18px;border-radius:100px;margin-bottom:24px;animation:fadeDown .5s ease both}
.badge-dot{width:7px;height:7px;background:var(--acid);border-radius:50%;animation:blink 1.8s ease infinite}
@keyframes blink{0%,100%{opacity:1;transform:scale(1)}50%{opacity:.4;transform:scale(.75)}}
@keyframes fadeDown{from{opacity:0;transform:translateY(-10px)}to{opacity:1;transform:translateY(0)}}
@keyframes fadeUp{from{opacity:0;transform:translateY(22px)}to{opacity:1;transform:translateY(0)}}
 
.hero-h1{font-size:clamp(3rem,8.5vw,6.8rem);animation:fadeUp .65s ease .06s both;margin-bottom:20px}
.hero-h1 .line-not-you{font-family:'Fraunces',serif;font-style:italic;color:var(--acid);display:block;font-size:clamp(2.8rem,8vw,6.4rem)}
 
.hero-lead{font-size:clamp(1rem,2.5vw,1.15rem);color:var(--stone);font-weight:300;line-height:1.7;margin-bottom:26px;animation:fadeUp .65s ease .18s both}
.hero-lead strong{color:var(--white);font-weight:600}
 
.hero-points{list-style:none;display:flex;flex-direction:column;gap:10px;margin-bottom:32px;animation:fadeUp .65s ease .26s both}
.hero-points li{display:flex;align-items:flex-start;gap:12px;font-size:.97rem;color:#c8c3ba;line-height:1.55}
.hero-points li::before{content:'👉';flex-shrink:0;margin-top:1px}
 
.hero-cta-wrap{display:flex;flex-wrap:wrap;gap:12px;align-items:center;animation:fadeUp .65s ease .34s both}
.hero-cta-note{font-size:.8rem;color:var(--muted);margin-left:2px}
 
.hero-stats{display:flex;gap:36px;flex-wrap:wrap;margin-top:48px;padding-top:36px;border-top:1px solid var(--border);animation:fadeUp .65s ease .44s both}
.hstat-n{font-family:'Bebas Neue',sans-serif;font-size:2.5rem;color:var(--acid);line-height:1}
.hstat-l{font-size:.75rem;color:var(--muted);text-transform:uppercase;letter-spacing:.07em;margin-top:2px}
 
/* mockup col */
.hero-mockup{display:flex;align-items:center;justify-content:center;animation:fadeUp .65s ease .2s both}
@media(max-width:860px){.hero-mockup{order:-1}}
.mockup-phone{
  width:240px;height:420px;
  background:linear-gradient(160deg,#1c2a0c,#2a3e12,#131a08);
  border-radius:32px;
  border:2px solid rgba(212,245,60,.2);
  display:flex;flex-direction:column;align-items:center;justify-content:center;
  position:relative;padding:28px 20px;
  box-shadow:0 32px 80px rgba(0,0,0,.6),0 0 0 1px rgba(212,245,60,.06);
}
/* ── ÎNLOCUIEȘTE CU MOCKUP REAL AL EBOOK-ULUI ── */
.mockup-phone::before{
  content:'[ Mockup ebook ]';
  position:absolute;inset:12px;
  border:1px dashed rgba(212,245,60,.2);
  border-radius:22px;
  display:flex;align-items:center;justify-content:center;
  font-size:.75rem;font-weight:700;letter-spacing:.08em;text-transform:uppercase;
  color:rgba(212,245,60,.25);font-family:'DM Sans',sans-serif;
}
.mockup-tag{
  position:absolute;bottom:-18px;
  background:var(--acid);color:var(--black);
  font-family:'Bebas Neue',sans-serif;font-size:.95rem;letter-spacing:.06em;
  padding:7px 20px;border-radius:100px;
  white-space:nowrap;
}
 
/* ══════════════════════════
   PROOF STRIP
══════════════════════════ */
#proof-strip{background:var(--card);border-top:1px solid var(--border);border-bottom:1px solid var(--border);padding:24px 0}
.proof-strip-inner{display:flex;flex-wrap:wrap;gap:0;justify-content:center}
.ps-item{
  display:flex;align-items:center;gap:12px;
  padding:14px 32px;border-right:1px solid var(--border);
  font-size:.92rem;
}
.ps-item:last-child{border-right:none}
@media(max-width:700px){.ps-item{border-right:none;border-bottom:1px solid var(--border)}}
.ps-item .check{color:var(--acid);font-weight:700;font-size:1rem}
.ps-item span{color:var(--stone)}
.ps-item strong{color:var(--white)}
 
/* ══════════════════════════
   MYTHS — cards
══════════════════════════ */
#myths{background:var(--cream);color:var(--black);position:relative;overflow:hidden}
#myths::before{content:'"';position:absolute;top:-80px;left:-20px;font-family:'Fraunces',serif;font-size:26rem;color:rgba(0,0,0,.04);line-height:1;pointer-events:none}
 
.myths-intro{margin-bottom:52px}
.eyebrow{font-size:.75rem;font-weight:700;letter-spacing:.14em;text-transform:uppercase;margin-bottom:14px}
.myths-intro .eyebrow{color:var(--orange)}
.myths-intro h2{font-family:'Bebas Neue',sans-serif;font-size:clamp(2.4rem,6vw,4.8rem);color:var(--black);line-height:.95}
.myths-intro p{margin-top:16px;font-size:1.05rem;color:#3d3b34;max-width:540px;line-height:1.7}
 
.myths-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(280px,1fr));gap:12px;margin-bottom:40px}
 
.myth-card{background:#fff;padding:24px 26px;border-radius:4px;border-top:3px solid #e8e0d4;transition:border-color .2s,transform .2s;box-shadow:0 2px 12px rgba(0,0,0,.06)}
.myth-card:hover{border-color:var(--orange);transform:translateY(-2px)}
.myth-x{font-size:.72rem;font-weight:700;letter-spacing:.1em;text-transform:uppercase;color:#c0392b;margin-bottom:10px;display:flex;align-items:center;gap:6px}
.myth-x::before{content:'✕';font-size:1rem}
.myth-label{font-size:1.05rem;font-weight:600;color:#1a1a16;text-decoration:line-through;text-decoration-color:#c0392b;text-decoration-thickness:2px;margin-bottom:8px;line-height:1.4}
.myth-note{font-size:.85rem;color:#6b6659;line-height:1.55}
 
.myths-closing{
  background:var(--black);color:var(--white);
  padding:32px 40px;position:relative;
}
.myths-closing::before{content:'';position:absolute;left:0;top:0;bottom:0;width:4px;background:var(--acid)}
.myths-closing p{font-size:1.05rem;color:#c8c3ba;line-height:1.7}
.myths-closing strong{color:var(--acid)}
 
/* ══════════════════════════
   EMPATHY
══════════════════════════ */
#empathy{position:relative}
 
.empathy-grid{display:grid;grid-template-columns:1.1fr 1fr;gap:64px;align-items:start}
@media(max-width:780px){.empathy-grid{grid-template-columns:1fr;gap:40px}}
 
.empathy-left .eyebrow{color:var(--acid)}
.empathy-left h2{font-family:'Bebas Neue',sans-serif;font-size:clamp(2.4rem,6vw,4.8rem);line-height:.95;margin-bottom:32px}
 
.pain-list{list-style:none;display:flex;flex-direction:column;gap:2px;margin-bottom:36px}
.pain-item{background:var(--card);padding:20px 24px;display:flex;align-items:flex-start;gap:14px;border-left:3px solid transparent;transition:border-color .18s,background .18s}
.pain-item:hover{border-left-color:var(--orange);background:#1e1e1a}
.pain-item .arr{color:var(--orange);flex-shrink:0;font-size:1rem;margin-top:3px}
.pain-item p{font-size:.97rem;color:#b8b3aa;line-height:1.6}
.pain-item p em{font-style:normal;color:var(--white);font-weight:600}
 
.not-you{
  background:rgba(212,245,60,.07);
  border:1px solid rgba(212,245,60,.18);
  padding:24px 28px;border-radius:3px;
}
.not-you p{font-family:'Fraunces',serif;font-style:italic;font-size:1.15rem;color:var(--acid);line-height:1.65}
.not-you span{display:block;margin-top:10px;font-family:'DM Sans',sans-serif;font-style:normal;font-size:.9rem;color:var(--stone)}
 
.transition-box{background:var(--card);padding:32px;border-left:4px solid var(--acid)}
.transition-box p{font-size:1.05rem;color:#c8c3ba;line-height:1.7;margin-bottom:20px}
.transition-box strong{color:var(--white)}
.transition-points{list-style:none;display:flex;flex-direction:column;gap:8px}
.transition-points li{font-size:.95rem;color:var(--stone);padding-left:22px;position:relative;line-height:1.6}
.transition-points li::before{content:'→';position:absolute;left:0;color:var(--acid)}
.transition-cta{margin-top:28px}
 
/* ══════════════════════════
   BULLETS / CE PRIMEȘTI
══════════════════════════ */
#inside{background:var(--dark)}
 
.inside-header{margin-bottom:52px}
.inside-header .eyebrow{color:var(--acid)}
.inside-header h2{font-family:'Bebas Neue',sans-serif;font-size:clamp(2.4rem,6vw,4.8rem);line-height:.95}
.inside-header p{margin-top:16px;color:var(--stone);font-size:1.05rem;max-width:520px;line-height:1.7}
 
.inside-grid{display:flex;flex-direction:column;gap:1px;background:rgba(255,255,255,.04);border:1px solid rgba(255,255,255,.04)}
.inside-row{
  background:var(--dark);padding:26px 32px 26px 28px;
  display:flex;align-items:flex-start;gap:22px;
  border-left:3px solid transparent;
  transition:background .18s,border-color .18s;
}
.inside-row:hover{background:var(--card);border-left-color:var(--acid)}
.inside-row.warning:hover{border-left-color:var(--orange)}
.inside-icon{font-size:1.25rem;flex-shrink:0;margin-top:3px}
.inside-body strong{display:block;font-weight:600;font-size:1rem;color:var(--white);margin-bottom:5px;line-height:1.4}
.inside-body span{font-size:.9rem;color:var(--stone);line-height:1.6}
.inside-row.plus{background:var(--card);border-left:3px solid var(--orange)}
.inside-row.plus .inside-body strong{color:var(--acid)}
 
.result-box{
  margin-top:40px;padding:32px 36px;
  background:rgba(212,245,60,.06);border:1px solid rgba(212,245,60,.18);
}
.result-box h3{font-family:'Bebas Neue',sans-serif;font-size:1.8rem;color:var(--acid);margin-bottom:16px;letter-spacing:.04em}
.result-list{list-style:none;display:flex;flex-direction:column;gap:8px}
.result-list li{font-size:.97rem;color:var(--stone);padding-left:22px;position:relative;line-height:1.55}
.result-list li::before{content:'✓';position:absolute;left:0;color:var(--acid);font-weight:700}
.result-list li strong{color:var(--white)}
 
.inside-cta{margin-top:44px;text-align:center}
.inside-cta p{font-size:.85rem;color:var(--muted);margin-top:12px}
 
/* ══════════════════════════
   AUTHOR
══════════════════════════ */
#author{background:var(--card);position:relative;overflow:hidden}
#author::before{content:'';position:absolute;top:0;right:0;width:40%;height:100%;background:linear-gradient(135deg,transparent,rgba(212,245,60,.04));pointer-events:none}
 
.author-grid{display:grid;grid-template-columns:1fr 1.3fr;gap:72px;align-items:center}
@media(max-width:720px){.author-grid{grid-template-columns:1fr;gap:40px}}
 
.author-img-wrap{position:relative}
.author-img{
  width:100%;aspect-ratio:4/5;
  background:linear-gradient(160deg,#1e2a0e,#2d3f14,#141a08);
  border-radius:4px;overflow:hidden;position:relative;
  /* ── ÎNLOCUIEȘTE CU: <img src="foto-razvan.jpg" style="width:100%;height:100%;object-fit:cover"> ── */
}
.author-img::before{
  content:'[ Foto Răzvan Pomoja ]';
  position:absolute;inset:0;display:flex;align-items:center;justify-content:center;
  font-size:.8rem;font-weight:700;letter-spacing:.08em;text-transform:uppercase;
  color:rgba(212,245,60,.2);border:1px dashed rgba(212,245,60,.15);
  font-family:'DM Sans',sans-serif;
}
.author-badge{
  position:absolute;bottom:-14px;right:-14px;
  background:var(--acid);color:var(--black);
  padding:12px 16px;font-family:'Bebas Neue',sans-serif;
  font-size:.95rem;letter-spacing:.05em;line-height:1.3;text-align:center;z-index:2;
}
 
.author-eyebrow{font-size:.75rem;font-weight:700;letter-spacing:.14em;text-transform:uppercase;color:var(--acid);margin-bottom:14px}
.author-name{font-family:'Bebas Neue',sans-serif;font-size:clamp(2.5rem,5.5vw,4.2rem);line-height:.95;margin-bottom:24px}
 
.author-text{font-size:1rem;color:#a09890;line-height:1.75;margin-bottom:14px}
.author-text strong{color:var(--white)}
 
.author-proof{
  margin-top:24px;padding:20px 24px;
  background:rgba(212,245,60,.06);border:1px solid rgba(212,245,60,.15);
  border-radius:3px;
}
.author-proof p{font-family:'Fraunces',serif;font-style:italic;font-size:1rem;color:var(--acid);line-height:1.6}
 
/* ── PLACEHOLDER CIFRE REALE ── */
.author-numbers{
  margin-top:24px;display:flex;flex-direction:column;gap:8px;
  border:2px dashed rgba(212,245,60,.15);padding:20px 24px;border-radius:3px;
}
.author-numbers p{font-size:.8rem;font-weight:700;letter-spacing:.08em;text-transform:uppercase;color:rgba(212,245,60,.3)}
.author-numbers span{font-size:.78rem;color:#3e3c38;font-weight:400;letter-spacing:0;text-transform:none;margin-top:4px;display:block}
 
.author-tags{display:flex;flex-wrap:wrap;gap:8px;margin-top:24px}
.tag{background:rgba(255,255,255,.05);border:1px solid rgba(255,255,255,.09);color:#7a7468;padding:5px 14px;font-size:.78rem;border-radius:100px;font-weight:500}
.tag.hi{background:rgba(212,245,60,.07);border-color:rgba(212,245,60,.18);color:var(--acid)}
 
.author-cta{margin-top:32px}
 
/* ══════════════════════════
   TESTIMONIALE
══════════════════════════ */
#testimonials{background:var(--cream);color:var(--black)}
 
.test-head{text-align:center;margin-bottom:52px}
.test-head .eyebrow{color:var(--orange)}
.test-head h2{font-family:'Bebas Neue',sans-serif;font-size:clamp(2.2rem,5.5vw,4.2rem);color:var(--black)}
.test-head p{margin-top:10px;color:var(--muted);font-size:1rem}
 
/* screenshot placeholder */
.screenshot-zone{
  border:2px dashed rgba(0,0,0,.12);border-radius:4px;
  padding:52px 32px;text-align:center;background:rgba(0,0,0,.02);
  margin-bottom:36px;
}
.screenshot-zone .ph-title{font-size:.8rem;font-weight:700;letter-spacing:.1em;text-transform:uppercase;color:#aaa59d}
.screenshot-zone .ph-note{font-size:.8rem;color:#c8c3ba;margin-top:8px;line-height:1.6;max-width:440px;margin-left:auto;margin-right:auto}
 
.tgrid{display:grid;grid-template-columns:repeat(auto-fit,minmax(280px,1fr));gap:20px;margin-bottom:32px}
 
/* card placeholder */
.tcard-ph{
  background:#fff;padding:28px;border-radius:4px;
  box-shadow:0 2px 16px rgba(0,0,0,.07);
  border:2px dashed rgba(0,0,0,.1);
  min-height:180px;display:flex;flex-direction:column;justify-content:flex-end;
}
.tcard-ph .ph-inner{font-size:.77rem;font-weight:700;letter-spacing:.09em;text-transform:uppercase;color:#c8c3ba}
.tcard-ph .ph-sub{font-size:.75rem;color:#d4cfc8;margin-top:4px;font-weight:400;text-transform:none;letter-spacing:0}
 
.tcard-ph.dark{background:var(--black)}
.tcard-ph.dark .ph-inner{color:rgba(212,245,60,.2)}
.tcard-ph.dark .ph-sub{color:#2a2a26}
 
/* second screenshot zone */
.screenshot-zone-sm{
  border:2px dashed rgba(0,0,0,.1);border-radius:4px;
  padding:36px 32px;text-align:center;background:rgba(0,0,0,.02);
  margin-top:32px;
}
.screenshot-zone-sm .ph-title{font-size:.8rem;font-weight:700;letter-spacing:.1em;text-transform:uppercase;color:#aaa59d}
.screenshot-zone-sm .ph-note{font-size:.78rem;color:#c8c3ba;margin-top:6px;line-height:1.5}
 
/* ══════════════════════════
   FINAL CTA
══════════════════════════ */
#cta{background:var(--black);text-align:center;padding:100px 0;position:relative;overflow:hidden}
#cta::before{content:'';position:absolute;top:50%;left:50%;transform:translate(-50%,-50%);width:900px;height:900px;background:radial-gradient(circle,rgba(212,245,60,.06) 0%,transparent 62%);pointer-events:none}
 
.cta-eyebrow{font-size:.77rem;font-weight:700;letter-spacing:.14em;text-transform:uppercase;color:var(--acid);margin-bottom:18px}
.cta-h{font-size:clamp(2.6rem,7.5vw,5.8rem);margin-bottom:16px}
.cta-sub{color:#7a7468;font-size:1.05rem;max-width:500px;margin:0 auto 40px;line-height:1.65}
.cta-sub strong{color:var(--white)}
 
.form{max-width:420px;margin:0 auto;display:flex;flex-direction:column;gap:12px}
.form-row{display:flex;gap:10px}
@media(max-width:480px){.form-row{flex-direction:column}}
.finput{flex:1;background:rgba(255,255,255,.07);border:1px solid rgba(255,255,255,.11);color:var(--white);font-family:'DM Sans',sans-serif;font-size:.97rem;padding:16px 20px;border-radius:3px;outline:none;transition:border-color .2s,background .2s}
.finput::placeholder{color:#3e3c38}
.finput:focus{border-color:rgba(212,245,60,.38);background:rgba(255,255,255,.1)}
.fsub{width:100%;background:var(--acid);color:var(--black);font-family:'DM Sans',sans-serif;font-weight:700;font-size:1.02rem;letter-spacing:.04em;text-transform:uppercase;padding:20px 32px;border:none;border-radius:3px;cursor:pointer;transition:background .18s,transform .15s}
.fsub:hover{background:#bfdc30;transform:translateY(-2px)}
.gdpr{display:flex;align-items:flex-start;gap:10px;font-size:.77rem;color:#45433e;line-height:1.55}
.gdpr input{margin-top:3px;accent-color:var(--acid);flex-shrink:0}
.form-ok{display:none;font-size:.87rem;color:var(--acid);text-align:center;margin-top:4px}
.cta-reassure{margin-top:22px;font-size:.78rem;color:#3a3830}
 
/* ══════════════════════════
   P.S.
══════════════════════════ */
#ps{background:var(--dark);padding:72px 0}
.ps-box{border:1px solid rgba(212,245,60,.15);background:rgba(212,245,60,.04);padding:48px 52px;position:relative}
@media(max-width:600px){.ps-box{padding:32px 24px}}
.ps-label{position:absolute;top:-14px;left:32px;background:var(--acid);color:var(--black);font-family:'Bebas Neue',sans-serif;font-size:1rem;letter-spacing:.08em;padding:5px 16px}
.ps-intro{font-family:'Fraunces',serif;font-style:italic;font-size:1.2rem;color:var(--white);line-height:1.7;margin-bottom:20px}
.ps-desc{font-size:1rem;color:var(--stone);line-height:1.7;margin-bottom:28px}
.ps-checks{list-style:none;display:flex;flex-direction:column;gap:8px;margin-bottom:36px}
.ps-checks li{font-size:.97rem;color:var(--stone);padding-left:24px;position:relative;line-height:1.6}
.ps-checks li::before{content:'✓';position:absolute;left:0;color:var(--acid);font-weight:700}
.ps-checks li strong{color:var(--white)}
 
/* ── PROOF SUPLIMENTAR PLACEHOLDER ── */
.ps-proof-ph{
  border:2px dashed rgba(212,245,60,.12);padding:32px;text-align:center;margin-bottom:36px;border-radius:3px;
}
.ps-proof-ph .ph-title{font-size:.78rem;font-weight:700;letter-spacing:.1em;text-transform:uppercase;color:rgba(212,245,60,.25)}
.ps-proof-ph .ph-note{font-size:.76rem;color:#2e2c28;margin-top:6px;line-height:1.5}
 
.ps-final{text-align:center}
 
/* ══════════════════════════
   FOOTER
══════════════════════════ */
footer{background:#090908;padding:24px 0;text-align:center;border-top:1px solid rgba(255,255,255,.04);color:#2e2c28;font-size:.8rem}
footer a{color:#4a4840;text-decoration:none}
footer a:hover{color:var(--acid)}
</style>
</head>
<body>
 
 
<!-- ════════════════════════
     HERO
════════════════════════ -->
<section id="hero">
<div class="wrap">
<div class="hero-grid">
 
  <div>
    <div class="hero-badge r"><span class="badge-dot"></span>Ebook gratuit · Fără dietă · Fără bullfit</div>
 
    <h1 class="display hero-h1 r">
      Dacă ai ținut<br>
      <em class="line-not-you">5+ diete…</em>
      și tot ai pus<br>kilogramele înapoi…
    </h1>
 
    <p class="hero-lead r">
      <strong>Nu tu ai eșuat.</strong> Ai urmat niște reguli care sunt
      <em style="font-style:normal;color:var(--orange)">făcute să nu funcționeze pe termen lung.</em>
    </p>
 
    <ul class="hero-points r">
      <li>de ce ai slăbit <span class="hl">5–6 kg</span>… și le-ai pus înapoi în câteva săptămâni</li>
      <li>de ce <span class="hl-red">800 kcal</span> pare să funcționeze… dar te distruge după</li>
      <li>cum să recunoști instant ce e bullshit și ce nu — fără să fii nutriționistă</li>
    </ul>
 
    <p style="font-size:.9rem;color:var(--stone);margin-bottom:28px;font-weight:300" class="r">
      30,5 mituri din nutriție explicate simplu — fără jargon, fără morală, fără diete
    </p>
 
    <div class="hero-cta-wrap r">
      <a href="#cta" class="btn btn-acid-lg">Vreau să nu mai fiu păcălită de diete →</a>
    </div>
    <p class="hero-cta-note r" style="margin-top:12px">0 lei · se citește în ~1h pe telefon</p>
 
    <div class="hero-stats r">
      <div><div class="hstat-n">30,5</div><div class="hstat-l">mituri demontate</div></div>
      <div><div class="hstat-n">0 lei</div><div class="hstat-l">cost total</div></div>
      <div><div class="hstat-n">∞</div><div class="hstat-l">imunizare la bullcrap</div></div>
    </div>
  </div>
 
  <div class="hero-mockup r d2">
    <div style="position:relative">
      <div class="mockup-phone">
        <!--
          ╔═══════════════════════════════════╗
          ║ ÎNLOCUIEȘTE CU MOCKUP REAL:       ║
          ║ telefon în mână cu cover ebook    ║
          ║ sau render 3D al ebook-ului       ║
          ╚═══════════════════════════════════╝
        -->
      </div>
      <div class="mockup-tag">Descarcă gratuit →</div>
    </div>
  </div>
 
</div>
</div>
</section>
 
 
<!-- ════════════════════════
     PROOF STRIP
════════════════════════ -->
<div id="proof-strip">
<div class="wrap">
<div class="proof-strip-inner">
  <!--
    ╔══════════════════════════════════════════════════════╗
    ║ ÎNLOCUIEȘTE cifrele de mai jos cu date REALE din:   ║
    ║ · dashboard newsletter (nr. abonați)                ║
    ║ · analytics descărcări                              ║
    ║ · nr. comentarii / DM-uri primite                   ║
    ╚══════════════════════════════════════════════════════╝
  -->
  <div class="ps-item"><span class="check">✔</span><span><strong>[X.XXX]</strong> persoane au descărcat deja</span></div>
  <div class="ps-item"><span class="check">✔</span><span>Zeci de mesaje de genul <strong>„în sfârșit are sens"</strong></span></div>
  <div class="ps-item"><span class="check">✔</span><span>Aceleași idei care au strâns <strong>milioane de vizualizări</strong> online</span></div>
</div>
</div>
</div>
 
<div class="divider"></div>
 
 
<!-- ════════════════════════
     MYTHS — CARDS
════════════════════════ -->
<section id="myths">
<div class="wrap">
 
  <div class="myths-intro r">
    <p class="eyebrow">Ai auzit și tu probabil</p>
    <h2>Lucruri pe care<br>le-ai crezut ani de zile</h2>
    <p>Problema nu e că le-ai crezut. E că <strong>nimeni nu ți le-a explicat corect.</strong></p>
  </div>
 
  <div class="myths-grid">
    <div class="myth-card r">
      <div class="myth-x">Mit</div>
      <div class="myth-label">„Carbohidrații îngrașă"</div>
      <div class="myth-note">Unul dintre cele mai toxice mituri. Explicat complet în ebook — cu logică, nu cu interdicții.</div>
    </div>
    <div class="myth-card r d1">
      <div class="myth-x">Mit</div>
      <div class="myth-label">„800 kcal/zi = slăbit rapid"</div>
      <div class="myth-note">Funcționează 2 săptămâni. Apoi îți sabotează metabolismul și kilogramele revin cu dobândă.</div>
    </div>
    <div class="myth-card r d2">
      <div class="myth-x">Mit</div>
      <div class="myth-label">„Sucul de lămâie arde grăsimea"</div>
      <div class="myth-note">Fără comentarii. Dar înăuntru — cu umor.</div>
    </div>
    <div class="myth-card r d1">
      <div class="myth-x">Mit</div>
      <div class="myth-label">„Metabolismul meu e lent"</div>
      <div class="myth-note">Concluzia la care ajunge oricine după 3 diete eșuate. De ce e greșită — în ebook.</div>
    </div>
    <div class="myth-card r d2">
      <div class="myth-x">Mit</div>
      <div class="myth-label">„Trebuie cardio ca să slăbești"</div>
      <div class="myth-note">Motivul pentru care sute de ore de alergat nu au adus rezultatele promise.</div>
    </div>
    <div class="myth-card r d3">
      <div class="myth-x">Mit</div>
      <div class="myth-label">„Dacă nu transpiri, n-ai muncit"</div>
      <div class="myth-note">Și alte standarde imposibile cu care industria fitness îți vinde vinovăție.</div>
    </div>
  </div>
 
  <div class="myths-closing r">
    <p>Problema nu e că le-ai crezut. E că <strong>ai primit aceste informații ca adevăruri</strong>, de la oameni cu autoritate, timp de ani de zile.<br>Ebook-ul nu îți dă altă regulă de urmat. Îți dă <strong>filtrul ca să nu mai ai nevoie de reguli.</strong></p>
  </div>
 
</div>
</section>
 
<div class="divider"></div>
 
 
<!-- ════════════════════════
     EMPATHY + TRANSITION
════════════════════════ -->
<section id="empathy">
<div class="wrap">
<div class="empathy-grid">
 
  <div>
    <p class="eyebrow r" style="color:var(--acid)">Dacă ai ajuns aici, probabil</p>
    <h2 class="display r">Sună<br>familiar?</h2>
 
    <ul class="pain-list r">
      <li class="pain-item">
        <span class="arr">→</span>
        <p>Ai slăbit rapid… și ai pus totul înapoi <em>la primul weekend normal</em></p>
      </li>
      <li class="pain-item">
        <span class="arr">→</span>
        <p>Urmărești <em>10 conturi diferite</em> și fiecare spune altceva</p>
      </li>
      <li class="pain-item">
        <span class="arr">→</span>
        <p>Ai plătit sală, nutriționist, suplimente — și ai rămas <em>la același punct</em></p>
      </li>
      <li class="pain-item">
        <span class="arr">→</span>
        <p>Ai ajuns să crezi că <em>„ceva e greșit cu tine"</em></p>
      </li>
    </ul>
 
    <div class="not-you r">
      <p>Nu e greșit cu tine.</p>
      <span>Ai fost expusă la informații contradictorii ani de zile. Și nimeni nu ți-a dat un filtru.</span>
    </div>
  </div>
 
  <div class="r d1">
    <div class="transition-box">
      <p>De asta am creat ebook-ul ăsta:</p>
      <ul class="transition-points">
        <li><strong>nu ca să-ți dau o altă dietă</strong></li>
        <li><strong>ci ca să-ți dau filtrul pe care nimeni nu ți l-a dat</strong></li>
        <li>ca să înțelegi de ce nu a mers nimic din ce ai încercat</li>
        <li>ca să nu mai depinzi de niciun plan, coach sau trend nou</li>
      </ul>
      <div class="transition-cta">
        <a href="#cta" class="btn btn-acid">Vreau filtrul care îmi arată ce e bullshit →</a>
      </div>
    </div>
  </div>
 
</div>
</div>
</section>
 
<div class="divider"></div>
 
 
<!-- ════════════════════════
     CE PRIMEȘTI
════════════════════════ -->
<section id="inside">
<div class="wrap">
 
  <div class="inside-header r">
    <p class="eyebrow">Ce vei înțelege după ce îl citești</p>
    <h2 class="display">Nu o dietă.<br><span class="accent">Un filtru.</span></h2>
    <p>Diferența față de tot ce ai încercat până acum: nu urmezi ceva — înțelegi de ce.</p>
  </div>
 
  <div class="inside-grid">
 
    <div class="inside-row r">
      <span class="inside-icon">🧠</span>
      <div class="inside-body">
        <strong>De ce dietele restrictive eșuează aproape de fiecare dată</strong>
        <span>Nu e lipsă de voință. E biologie. Înțelegând asta, scapi de ani de vinovăție cronică — și poți în sfârșit să faci ceva care funcționează.</span>
      </div>
    </div>
 
    <div class="inside-row r d1">
      <span class="inside-icon">🍞</span>
      <div class="inside-body">
        <strong>De ce „carbohidrații îngrașă" e unul dintre cele mai toxice mituri — și cum îți afectează direct rezultatele</strong>
        <span>Nu e teorie. E explicat exact cum credința asta îți sabotează zilnic alegerile alimentare.</span>
      </div>
    </div>
 
    <div class="inside-row warning r d2">
      <span class="inside-icon">⚠️</span>
      <div class="inside-body">
        <strong>De ce dietele de 800 kcal îți sabotează progresul — chiar dacă „funcționează" la început</strong>
        <span>Ce se întâmplă în corp după săptămânile 2–3 de restricție extremă. Și de ce kilogramele puse înapoi nu sunt „vina ta".</span>
      </div>
    </div>
 
    <div class="inside-row r">
      <span class="inside-icon">🍕</span>
      <div class="inside-body">
        <strong>De ce pizza poate fi un mic dejun ok — și cum să nu mai vezi mâncarea ca „bună" sau „rea"</strong>
        <span>Logica simplă din spatele nutriției pe care nimeni nu ți-a explicat-o. Fără să-ți distrugă plăcerea de a mânca.</span>
      </div>
    </div>
 
    <div class="inside-row r d1">
      <span class="inside-icon">💪</span>
      <div class="inside-body">
        <strong>Ce funcționează de fapt pentru femei ocupate — nu pentru influenceri cu 4h/zi libere</strong>
        <span>Mitul cardio-ului, mitul transpirației, mitul „dacă n-ai timp nu poți" — toate demontate cu context real.</span>
      </div>
    </div>
 
    <div class="inside-row plus r d2">
      <span class="inside-icon">🎯</span>
      <div class="inside-body">
        <strong>PLUS — Cel mai important: după ebook, nu mai depinzi de nimeni</strong>
        <span>Nu de diete. Nu de influenceri. Nu de reclame. Îți dai singură seama ce e bullshit — pe viață, nu pe 30 de zile.</span>
      </div>
    </div>
 
  </div>
 
  <div class="result-box r">
    <h3>Ce se schimbă după ce citești</h3>
    <ul class="result-list">
      <li>Mergi la restaurant fără să calculezi nimic</li>
      <li>Mănânci un desert fără vinovăție — pentru că înțelegi de ce e ok</li>
      <li>Recunoști instant reclamele false fără să ai nevoie de un expert</li>
      <li><strong>Nu mai „începi de luni"</strong> — pentru că nu mai ai nevoie de un plan nou</li>
    </ul>
  </div>
 
  <div class="inside-cta r">
    <a href="#cta" class="btn btn-acid-lg">Vreau să înțeleg de ce nu a mers până acum →</a>
    <p>Gratuit. Fără card. Fără suplimente recomandate înăuntru.</p>
  </div>
 
</div>
</section>
 
<div class="divider"></div>
 
 
<!-- ════════════════════════
     AUTHOR
════════════════════════ -->
<section id="author">
<div class="wrap">
<div class="author-grid">
 
  <div class="author-img-wrap r">
    <div class="author-img"></div>
    <div class="author-badge">Educator,<br>nu influencer</div>
  </div>
 
  <div class="r d1">
    <p class="author-eyebrow">Cine e Pomoja și de ce să-l asculți</p>
    <h2 class="display author-name">Răzvan<br><span class="accent">Pomoja</span></h2>
 
    <p class="author-text">Nu sunt influencer. Nu vând suplimente. Nu promit rezultate în 30 de zile.</p>
    <p class="author-text">Din 2019 explic zilnic pe internet <strong>de ce majoritatea lucrurilor din fitness nu funcționează.</strong></p>
    <p class="author-text">Fac un singur lucru: explic simplu. Și dacă te mai fac să și râzi — <strong>e bonus din partea casei.</strong></p>
 
    <div class="author-proof">
      <p>„Scopul meu principal este să te învăț, ajut și susțin. Nu să pozez în chiloți. Sunt un educator."</p>
    </div>
 
    <!--
      ╔══════════════════════════════════════════════════════╗
      ║ ÎNLOCUIEȘTE cu cifre REALE:                         ║
      ║ · nr. urmăritori TikTok / Instagram / Facebook      ║
      ║ · nr. vizualizări total                             ║
      ║ · nr. DM-uri / comentarii primite                   ║
      ╚══════════════════════════════════════════════════════╝
    -->
    <div class="author-numbers">
      <p>[ Cifre reale: urmăritori / vizualizări ]</p>
      <span>Ex: „X milioane de vizualizări pe TikTok" sau „Xk urmăritori" — cu captură de ecran din platformă</span>
    </div>
 
    <div class="author-tags">
      <span class="tag hi">Anti-bullfit</span>
      <span class="tag hi">Educator</span>
      <span class="tag">TikTok · Instagram · Facebook</span>
      <span class="tag">România · din 2019</span>
    </div>
 
    <div class="author-cta">
      <a href="#cta" class="btn btn-acid">Vreau ebook-ul lui →</a>
    </div>
  </div>
 
</div>
</div>
</section>
 
<div class="divider"></div>
 
 
<!-- ════════════════════════
     TESTIMONIALE
════════════════════════ -->
<section id="testimonials">
<div class="wrap">
 
  <div class="test-head r">
    <p class="eyebrow">Reacții reale</p>
    <h2>Ce spun<br>cititoarele</h2>
    <p>Screenshot-uri reale — fără text editat sau inventat</p>
  </div>
 
  <!--
    ╔══════════════════════════════════════════════════════════╗
    ║ SCREENSHOT-URI MARI — DM-uri / comentarii               ║
    ║ Surse recomandate:                                      ║
    ║ · DM-uri Instagram sau Messenger                        ║
    ║ · Comentarii sub postări sau reels                      ║
    ║ · Story-uri în care ești taguit                         ║
    ║ IMPORTANT: autentic > design fancy                      ║
    ╚══════════════════════════════════════════════════════════╝
  -->
  <div class="screenshot-zone r">
    <div class="ph-title">[ Screenshot-uri testimoniale reale — DM-uri / comentarii ]</div>
    <div class="ph-note">Adaugă 2–4 capturi de ecran reale din DM-uri Instagram/Messenger sau comentarii.<br>Autentic bate design fancy — nu edita textul, pune captura direct.</div>
  </div>
 
  <div class="tgrid r">
    <!--
      ╔══════════════════════════════════════════════════════════╗
      ║ ÎNLOCUIEȘTE fiecare card cu un citat REAL               ║
      ║ cuvânt cu cuvânt din comentarii, DM-uri sau recenzii.   ║
      ║ NU inventa sau parafrazeza.                             ║
      ╚══════════════════════════════════════════════════════════╝
    -->
    <div class="tcard-ph dark r">
      <div class="ph-inner">[ Citat real — cuvânt cu cuvânt ]</div>
      <div class="ph-sub">Prenume, vârstă, oraș — din DM/comentariu real</div>
    </div>
    <div class="tcard-ph r d1">
      <div class="ph-inner">[ Citat real — cuvânt cu cuvânt ]</div>
      <div class="ph-sub">Prenume, vârstă, oraș — din DM/comentariu real</div>
    </div>
    <div class="tcard-ph r d2">
      <div class="ph-inner">[ Citat real — cuvânt cu cuvânt ]</div>
      <div class="ph-sub">Prenume, vârstă, oraș — din DM/comentariu real</div>
    </div>
    <div class="tcard-ph dark r d1">
      <div class="ph-inner">[ Citat real — cuvânt cu cuvânt ]</div>
      <div class="ph-sub">Prenume, vârstă, oraș — din DM/comentariu real</div>
    </div>
    <div class="tcard-ph r d2">
      <div class="ph-inner">[ Citat real — cuvânt cu cuvânt ]</div>
      <div class="ph-sub">Prenume, vârstă, oraș — din DM/comentariu real</div>
    </div>
    <div class="tcard-ph r d3">
      <div class="ph-inner">[ Citat real — cuvânt cu cuvânt ]</div>
      <div class="ph-sub">Prenume, vârstă, oraș — din DM/comentariu real</div>
    </div>
  </div>
 
  <!--
    ╔══════════════════════════════════════════════════════════╗
    ║ PROOF VIZUAL SUPLIMENTAR                                ║
    ║ · Captură din analytics / dashboard (nr. descărcări)    ║
    ║ · Captură pagina de Facebook (nr. urmăritori)           ║
    ║ · Captură comentarii virale de pe TikTok                ║
    ╚══════════════════════════════════════════════════════════╝
  -->
  <div class="screenshot-zone-sm r">
    <div class="ph-title">[ Proof vizual: nr. descărcări / urmăritori / comentarii virale ]</div>
    <div class="ph-note">Captură din dashboard, analytics sau platformă — număr real, vizibil</div>
  </div>
 
</div>
</section>
 
<div class="divider"></div>
 
 
<!-- ════════════════════════
     FINAL CTA
════════════════════════ -->
<section id="cta">
<div class="wrap-narrow">
 
  <p class="cta-eyebrow r">Dacă vrei să nu mai sari din dietă în dietă…</p>
  <h2 class="display cta-h r">
    Înțelege în sfârșit<br>
    <span class="accent">ce funcționează</span><br>
    pentru tine
  </h2>
  <p class="cta-sub r">
    Descarcă ebook-ul și vezi exact unde ai fost păcălită.<br>
    <strong>0 lei · fără card · fără abonament</strong>
  </p>
 
  <form class="form r" onsubmit="handleForm(event)">
    <div class="form-row">
      <input class="finput" type="text" placeholder="Prenumele tău" required>
      <input class="finput" type="email" placeholder="Email-ul tău" required>
    </div>
    <button type="submit" class="fsub">Descarcă ebook-ul și vezi exact unde ai fost păcălită →</button>
    <label class="gdpr">
      <input type="checkbox" required>
      <span>Sunt de acord să primesc ocazional emailuri de la pomoja.ro. Fără spam. Fără reclame la ceaiuri de slăbit.</span>
    </label>
    <p class="form-ok" id="formOk">✓ Verifică-ți emailul (și folderul Spam / Promotions). Vine în câteva minute.</p>
  </form>
 
  <p class="cta-reassure r">🔒 Gratuit. Fără card. Poți da unsubscribe oricând.</p>
 
</div>
</section>
 
 
<!-- ════════════════════════
     P.S.
════════════════════════ -->
<section id="ps">
<div class="wrap-narrow">
<div class="ps-box r">
  <span class="ps-label">P.S.</span>
 
  <p class="ps-intro">Dacă ai citit până aici — probabil ai încercat deja destule.</p>
 
  <p class="ps-desc">Ebook-ul ăsta nu e încă o soluție. Nu îți dă o altă dietă de urmat.<br>E <strong style="color:var(--white)">ultimul filtru de care ai nevoie</strong> ca să nu mai fii păcălită.</p>
 
  <ul class="ps-checks">
    <li>E gratuit. Zero lei, zero capcane.</li>
    <li>Se citește în ~1 oră pe telefon.</li>
    <li>O să râzi. <strong>Serios, chiar sunt neserios de amuzant.</strong></li>
    <li>Funcționează chiar dacă ai mai „eșuat" de 5 ori — pentru că <strong>nu tu ai eșuat.</strong></li>
  </ul>
 
  <!--
    ╔═════════════════════════════════════════════════════╗
    ║ PROOF SUPLIMENTAR DE FINAL                         ║
    ║ · Comentarii virale TikTok / Instagram             ║
    ║ · Nr. share-uri ale ebook-ului                     ║
    ║ · Recenzii Google / Facebook Page                  ║
    ╚═════════════════════════════════════════════════════╝
  -->
  <div class="ps-proof-ph">
    <div class="ph-title">[ Proof final: comentarii virale / nr. share-uri / recenzii ]</div>
    <div class="ph-note">Screenshot comentarii virale, cifre reale de engagement sau recenzii de pagină</div>
  </div>
 
  <div class="ps-final">
    <a href="#cta" class="btn btn-acid-lg">Vreau filtrul →</a>
    <p style="margin-top:12px;font-size:.8rem;color:#3a3830">0 lei · fără card · fără abonament</p>
  </div>
 
</div>
</div>
</section>
 
 
<!-- ════════════════════════
     FOOTER
════════════════════════ -->
<footer>
  <div class="wrap">
    <p>© 2024 Pomoja Fitness &nbsp;·&nbsp; <a href="#">pomoja.ro</a> &nbsp;·&nbsp; <a href="#">Instagram</a> &nbsp;·&nbsp; <a href="#">Facebook</a> &nbsp;·&nbsp; <a href="#">TikTok</a></p>
    <p style="margin-top:6px;font-size:.75rem">Nu suntem influenceri. Nu pozăm în chiloți. Promitem.</p>
  </div>
</footer>
 
 
<script>
const els = document.querySelectorAll('.r');
const io = new IntersectionObserver(entries => {
  entries.forEach(e => { if(e.isIntersecting) e.target.classList.add('on'); });
}, { threshold: 0.1, rootMargin: '0px 0px -32px 0px' });
els.forEach(el => io.observe(el));
 
function handleForm(e){
  e.preventDefault();
  document.getElementById('formOk').style.display = 'block';
  const btn = e.target.querySelector('.fsub');
  btn.textContent = '✓ Trimis! Verifică emailul.';
  btn.style.background = '#1a3808';
  btn.style.color = 'var(--acid)';
}
 
document.querySelectorAll('a[href^="#"]').forEach(a => {
  a.addEventListener('click', e => {
    const t = document.querySelector(a.getAttribute('href'));
    if(t){ e.preventDefault(); t.scrollIntoView({ behavior:'smooth', block:'start' }); }
  });
});
</script>
</body>
</html>
