# VAC® — Victoria's Portfolio: código fuente

Este archivo reúne el código del portfolio separado en tres partes: HTML (estructura), CSS (estilos) y JavaScript (interacciones).

**Importante:** en el archivo real (`Victoria_s_Portfolio.html`) las imágenes de la portada están incrustadas en base64. Acá se reemplazaron por marcadores `[IMAGEN_BASE64_nn]` para que el código sea legible. Para que el sitio funcione hay que usar el archivo HTML completo, no este.

## Imágenes incrustadas (reemplazadas por marcadores)

| N.º | Tipo | Tamaño aprox. |
|---|---|---|
| 01 | image/webp | ~18 KB |
| 02 | image/webp | ~5 KB |
| 03 | image/webp | ~17 KB |
| 04 | image/webp | ~12 KB |
| 05 | image/webp | ~17 KB |
| 06 | image/webp | ~16 KB |
| 07 | image/webp | ~6 KB |
| 08 | image/webp | ~12 KB |
| 09 | image/webp | ~13 KB |
| 10 | image/webp | ~30 KB |
| 11 | image/webp | ~14 KB |
| 12 | image/webp | ~19 KB |
| 13 | image/webp | ~16 KB |
| 14 | image/webp | ~13 KB |
| 15 | image/webp | ~20 KB |
| 16 | image/webp | ~17 KB |
| 17 | image/webp | ~10 KB |
| 18 | image/webp | ~17 KB |
| 19 | image/webp | ~326 KB |
| 20 | image/webp | ~96 KB |
| 21 | image/webp | ~164 KB |
| 22 | image/webp | ~0 KB |

## 1. HTML (estructura)

````html
<!DOCTYPE html>
<html lang="es"><head><meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Victoria’s Portfolio</title>
<style>/* ver sección CSS */</style></head><body>
<main class="page on" id="home" aria-label="Inicio">
 <h1 class="sr">Victoria’s Portfolio</h1>
 <div class="stage" id="stage">
  <div class="tb" id="tb" aria-hidden="true"></div>
  <div class="bb" id="bb">
   <button class="bd" id="badge" type="button" aria-label="Abrir ABOUT: credencial de Victoria Agustina Cruz, comunicadora">
    <span class="sway"><span class="strap" aria-hidden="true"></span><img id="badgeimg" alt="" draggable="false"></span>
   </button>
  </div>
  <div class="hint" id="hint" aria-hidden="true">Click to discover <svg viewBox="0 0 30 10" width="2.8em" height="1em" fill="none" stroke="currentColor" stroke-width="1.2" aria-hidden="true"><path d="M0 5h28M24 1l4 4-4 4"/></svg></div>
 <button class="cue" id="cue" type="button">Deslizá para descubrir ↓</button>
 </div>
<nav class="menu hm" id="hm" aria-label="Principal"></nav>
<div class="flow" id="flow">
 <section class="fs" id="sm" aria-label="Sobre mí"><h2 class="rv3">Sobre<em>mí</em></h2><div id="smx"></div>
<div class="cv rv3">
<div><h3>Formación</h3><ul><li>Licenciatura en Ciencias de la Comunicación, UNSa (ingreso 2022). Estudiante avanzada; orientación en comunicación institucional y gestión de la comunicación interna.</li><li>Diplomatura universitaria en Gestión de Redes (UNSa y Ministerio de Desarrollo Social de Salta).</li><li>Bachiller en Turismo, Colegio 11 de Septiembre (2015–2019).</li></ul></div>
<div><h3>Actividades y formación</h3><ul><li>CONPEST 2018: organizadora y exponente, con mérito académico.</li><li>12.º Congreso FOPEA (2023).</li><li>Jornada «Relaciones Públicas en Acción: Potenciando Sectores» (UCASAL).</li><li>Talleres y cursos: escritura académica, análisis morfológico, Derechos Humanos y discriminación, Marketing Digital (ENCIC), gestión de comunicación de riesgos (Provincia de Buenos Aires).</li><li>Investigaciones de cátedra, proyecto CIUNSa tipo B y articulación para contenido informativo sobre Chagas.</li></ul></div>
<div><h3>Herramientas</h3><ul><li>Photoroom</li><li>Ibis</li><li>Canva</li><li>CapCut</li><li>PicsArt</li></ul></div>
<div><h3>Idiomas</h3><ul><li>Inglés (B2)</li><li>Francés (básico)</li><li>Coreano (básico)</li></ul></div></div>
<div class="cam rv3" id="cam"><div class="vf" aria-hidden="true"><i></i><i></i><i></i><i></i><span>Visor · fotografías pendientes de cargar</span></div><div class="strip" id="strip" role="group" aria-label="Fotografías en movimiento continuo"></div><button class="cpause" id="cp" type="button" aria-pressed="false">Pausar</button></div><a class="go rv3" href="#about">Ver Sobre mí completo</a></section>
 <section class="fs" id="pr" aria-label="Proyectos"><h2 class="rv3">Proyectos<em>archivo</em></h2><p class="lead rv3">Elegí un proyecto con las flechas o el índice, o seguí bajando para recorrerlos.</p><div class="scene" id="scene"></div></section>
 <section class="fs" id="contacto" aria-label="Contacto"><h2 class="rv3">Contacto<em>hablemos</em></h2><dl class="card ct rv3"><dt>Instagram</dt><dd id="igc"></dd><dt>Correo</dt><dd><a href="mailto:victoriacruzok@gmail.com">victoriacruzok@gmail.com</a></dd><dt>LinkedIn</dt><dd><a href="https://www.linkedin.com/in/victoria-agustina-cruz-357405251" target="_blank" rel="noopener">linkedin.com/in/victoria-agustina-cruz-357405251</a></dd></dl><p class="gfx pl" aria-hidden="true">VAC® Archive</p></section>
</div>
</main>
<section class="page" id="about" aria-labelledby="ab" aria-hidden="true">
 <button class="back" type="button" data-go="home">← Home</button>
 <nav class="menu" aria-label="Principal"></nav>
 <div class="wrap">
  <h2 id="ab" class="rv" style="--r:0">About<em>me</em></h2>
  <div class="grid">
   <dl class="card rv" style="--r:1">
    <dt>Nombre</dt><dd>Victoria Agustina Cruz</dd>
    <dt>Profesión</dt><dd>Comunicadora</dd>
    <dt>Estudios</dt><dd>Ciencias de la Comunicación, UNSa</dd>
    <dt>Ubicación</dt><dd>Salta, Argentina</dd>
    <dt>Instagram</dt><dd><a class="ig" href="https://www.instagram.com/viktoria_cstyle/" target="_blank" rel="noopener" aria-label="Instagram, @viktoria_cstyle (abre en una pestaña nueva)"><span class="igl"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" aria-hidden="true"><rect x="3" y="3" width="18" height="18" rx="5"/><circle cx="12" cy="12" r="4"/><circle cx="17.3" cy="6.7" r="1" fill="currentColor" stroke="none"/></svg>Instagram</span><span class="igu">@viktoria_cstyle</span></a></dd>
   </dl>
   <div class="copy rv" style="--r:2">
    
    <p>Soy estudiante avanzada de la Licenciatura en Ciencias de la Comunicación de la Universidad Nacional de Salta. Mi recorrido académico y profesional se construye en torno al interés por la comunicación estratégica, la planificación y el desarrollo de proyectos comunicacionales.</p>
    <p>A lo largo de mi formación participé en experiencias vinculadas con la comunicación institucional, el diagnóstico y la planificación estratégica, la producción de contenidos y el diseño de propuestas visuales y audiovisuales. Estos espacios me permitieron explorar distintas dimensiones de la comunicación y comprender su papel en la construcción de vínculos entre organizaciones, instituciones y comunidades.</p>
    <p>Me interesa pensar la comunicación como una práctica estratégica y creativa: analizar contextos, identificar necesidades, construir narrativas y transformar ideas en proyectos con sentido.</p>
   </div>
  </div>
 </div>
</section>
<section class="page pg" id="archivo" aria-labelledby="pt" aria-hidden="true">
 <nav class="menu" aria-label="Principal"></nav>
 <div class="wrap">
  <h2 id="pt" class="rv2">Proyectos<em>archivo</em></h2>
  <p class="lead rv2">Archivo de trabajos y experiencias comunicacionales: el pensamiento, las decisiones y las producciones que hay detrás de cada proyecto.</p>
  <ol class="idx rv2" id="idx" aria-label="Categorías"></ol>
  <div id="cats"></div>
 </div>
</section>
<article class="page pg" id="proyecto" aria-label="Proyecto" aria-hidden="true">
 <a class="back" href="#archivo">← Proyectos</a>
 <nav class="menu" aria-label="Principal"></nav>
 <div class="wrap" id="pw"></div>
</article>
<noscript><p style="position:fixed;bottom:12px;left:12px">Esta página necesita JavaScript.</p></noscript>
<script>/* ver sección JavaScript */</script></body></html>
````

## 2. CSS (estilos)

````css
:root{color-scheme:light;--bg:#e2e2e2;--ink:#151515;--paper:#e7dfcf;--u:min(calc(100vw/1920),calc(100svh/900));--tu:var(--u);--ox:0;--oy:0}
*{box-sizing:border-box;margin:0}
html,body{height:100%;background:var(--bg);color:var(--ink);font-family:"Helvetica Neue",Arial,sans-serif;overflow:hidden}
.sr{position:absolute;width:1px;height:1px;overflow:hidden;clip:rect(0 0 0 0)}
.page{position:fixed;inset:0;overflow:auto;opacity:0;visibility:hidden;transition:opacity .7s ease,transform .7s ease,filter .7s ease,visibility 0s .7s}
.page.on{opacity:1;visibility:visible;transition-delay:.25s,.25s,.25s,0s}
#home{background:var(--bg) var(--ext) repeat-y 50% calc(900*var(--u))/calc(1920*var(--u)) calc(400*var(--u))}
#home:not(.on){transform:scale(.985);filter:blur(4px)}
.stage{position:relative;margin:0 auto;width:calc(1920*var(--u));height:calc(900*var(--u))}
.tb{position:absolute;inset:0;background:var(--plate) 0 0/100% 100%}
.g{position:absolute;left:calc((var(--x) - var(--ox))*var(--tu));top:calc((var(--y) - var(--oy))*var(--tu));width:calc(var(--w)*var(--tu));height:calc(var(--h)*var(--tu));background-size:100% 100%;opacity:0;animation:rise 1.15s cubic-bezier(.2,.7,.2,1) var(--d) forwards;will-change:transform,opacity,filter}
@keyframes rise{from{opacity:0;transform:translateY(calc(var(--tu)*30)) scale(.97);filter:blur(12px)}to{opacity:1;transform:none;filter:blur(0)}}
.tb.static .g{animation:none;opacity:1;will-change:auto}
.bb{position:absolute;left:calc(1270*var(--u));top:0;width:calc(650*var(--u));height:calc(900*var(--u))}
.bd{position:absolute;inset:0;border:0;background:none;cursor:pointer;display:block;padding:0;-webkit-tap-highlight-color:transparent}
.sway{position:absolute;left:calc(7*var(--u));top:0;width:calc(638*var(--u));height:calc(877*var(--u));transform-origin:calc(353*var(--u)) 0;animation:swayIn 4.6s cubic-bezier(.33,0,.2,1) 1.2s both,sway 8s ease-in-out 5.8s infinite;will-change:transform}
.sway img{display:block;width:100%;height:100%;user-select:none;-webkit-user-drag:none}
.strap{position:absolute;left:calc(316*var(--u));width:calc(74*var(--u));bottom:100%;height:calc(300*var(--u));background:var(--strap) 0 100%/100% calc(6*var(--u)) repeat-y}
@keyframes swayIn{0%{transform:rotate(0)}18%{transform:rotate(2.6deg)}40%{transform:rotate(-1.9deg)}60%{transform:rotate(1.3deg)}80%{transform:rotate(-.8deg)}100%{transform:rotate(0)}}
@keyframes sway{0%,100%{transform:rotate(0)}25%{transform:rotate(.9deg)}75%{transform:rotate(-.9deg)}}
.bd:hover .sway,.bd:focus-visible .sway{filter:drop-shadow(0 calc(10*var(--u)) calc(14*var(--u)) rgba(0,0,0,.22))}
.bd:focus-visible{outline:2px solid var(--ink);outline-offset:-4px;border-radius:12px}
.hint{position:absolute;left:calc(840*var(--u));top:calc(800*var(--u));display:flex;align-items:center;gap:.7em;font:700 clamp(10px,calc(21*var(--u)),15px)/1 "Helvetica Neue",Arial,sans-serif;letter-spacing:.24em;text-transform:uppercase;opacity:0;transition:opacity .8s ease;pointer-events:none}
.hint.show{opacity:1}
.hint svg{animation:nudge 1.8s ease-in-out infinite}
@keyframes nudge{0%,100%{transform:translateX(0)}50%{transform:translateX(.6em)}}
.bd:hover~.hint,.stage:has(.bd:hover) .hint{opacity:1}
@media (max-aspect-ratio:1/1){
 #home{background:var(--bg);--ub:min(calc(100vw/650),calc((100svh - 320px)/900));--tu:calc(100vw/1300);--ox:0;--oy:200}
 .stage{width:100%;height:auto;display:flex;flex-direction:column;align-items:center;padding-bottom:28px}
 .bb{order:1;position:relative;left:auto;width:calc(650*var(--ub));height:calc(900*var(--ub));background:var(--plate) calc(-1270*var(--ub)) 0/calc(1920*var(--ub)) calc(900*var(--ub));-webkit-mask-image:linear-gradient(90deg,transparent,#000 12%,#000 88%,transparent),linear-gradient(#000 82%,transparent);-webkit-mask-composite:source-in;mask-image:linear-gradient(90deg,transparent,#000 12%,#000 88%,transparent),linear-gradient(#000 82%,transparent);mask-composite:intersect}
 .sway{left:calc(7*var(--ub));width:calc(638*var(--ub));height:calc(877*var(--ub));transform-origin:calc(353*var(--ub)) 0}
 .strap{left:calc(316*var(--ub));width:calc(74*var(--ub));height:calc(200*var(--ub));background-size:100% calc(6*var(--ub))}
 .tb{order:2;position:relative;inset:auto;width:100%;height:calc(560*var(--tu));margin-top:6px;background:var(--plate) 0 calc(-200*var(--tu))/calc(1920*var(--tu)) calc(900*var(--tu));-webkit-mask-image:linear-gradient(transparent,#000 14%,#000 86%,transparent);mask-image:linear-gradient(transparent,#000 14%,#000 86%,transparent)}
 .hint{order:3;position:relative;left:auto;top:auto;margin-top:10px;font-size:11px}
 .bd:hover .sway{filter:none}
}
@media (prefers-reduced-motion:reduce){
 .g{animation:none;opacity:1}.sway{animation:none}.hint svg{animation:none}
 .page,.page.on{transition:opacity .2s ease;transition-delay:0s}#home:not(.on){transform:none;filter:none}
}
/* ABOUT */
#about{background:radial-gradient(ellipse at 0 100%,rgba(15,15,15,.78),transparent 42%),radial-gradient(#8c8c8c 1.7px,transparent 2.2px) 0 0/16px 16px,#ececec}
.back{position:fixed;z-index:5;top:max(18px,env(safe-area-inset-top));left:max(18px,env(safe-area-inset-left));font:700 12px/1 "Helvetica Neue",Arial,sans-serif;letter-spacing:.24em;text-transform:uppercase;color:var(--ink);background:#f4f4f2;border:1.5px solid var(--ink);padding:12px 16px;cursor:pointer;transition:background .2s,color .2s}
.back:hover,.back:focus-visible{background:var(--ink);color:#f4f4f2;outline:none}
.wrap{max-width:1080px;margin:0 auto;padding:clamp(86px,12vh,130px) clamp(20px,5vw,56px) 64px}
h2{font:900 clamp(56px,11vw,150px)/.92 "Arial Black","Helvetica Neue",Arial,sans-serif;letter-spacing:-.02em;text-transform:uppercase}
h2 em{display:block;font:italic 400 clamp(56px,11vw,150px)/.9 Cambria,Georgia,serif;text-transform:none;letter-spacing:0;margin-top:-.04em}
.grid{display:grid;grid-template-columns:minmax(260px,380px) 1fr;gap:clamp(24px,5vw,64px);margin-top:clamp(28px,6vh,56px);align-items:start}
.card{background:var(--paper);padding:26px 26px 22px;box-shadow:0 18px 40px -18px rgba(0,0,0,.4)}
.card dt{font:700 10px/1 "Helvetica Neue",Arial,sans-serif;letter-spacing:.22em;text-transform:uppercase;margin-top:18px}
.card dt:first-child{margin-top:0}
.card dd{font-size:18px;padding:7px 0 6px;border-bottom:1px solid rgba(21,21,21,.55)}
.card a{color:inherit;text-decoration:none}.igl{display:inline-flex;align-items:center;gap:.55em}.igl svg{width:1.05em;height:1.05em;flex:none}.card a:hover,.card a:focus-visible{text-decoration:underline}
.copy{background:rgba(244,244,242,.86);padding:clamp(20px,3vw,34px);font:19px/1.6 Cambria,Georgia,serif}
.copy p+p{margin-top:1em}
#about .rv{opacity:0;transform:translateY(22px)}
#about.on .rv{opacity:1;transform:none;transition:opacity .8s ease,transform .8s cubic-bezier(.2,.7,.2,1);transition-delay:calc(.45s + var(--r)*.12s)}
@media (max-width:760px){.grid{grid-template-columns:1fr}}
@media (prefers-reduced-motion:reduce){#about .rv{opacity:1;transform:none;transition:none}}

/* PROYECTOS */
.pg{background:radial-gradient(#8c8c8c 1.7px,transparent 2.2px) 0 0/16px 16px,#ececec}
.pg .wrap{max-width:1240px}
.pg h2,.pg h2 em{font-size:clamp(38px,10vw,140px)}
a.back{display:inline-block;text-decoration:none}
.menu{position:fixed;z-index:5;top:max(18px,env(safe-area-inset-top));right:max(18px,env(safe-area-inset-right));display:flex;gap:6px}
.menu a{font:700 12px/1 "Helvetica Neue",Arial,sans-serif;letter-spacing:.24em;text-transform:uppercase;color:var(--ink);background:#f4f4f2;border:1.5px solid var(--ink);padding:12px 14px;text-decoration:none;transition:background .2s,color .2s}
.menu a:hover,.menu a:focus-visible,.menu a[aria-current]{background:var(--ink);color:#f4f4f2;outline:none}
.card .ig{display:block}.card .igu{display:block;margin-top:5px;font-size:16px;text-decoration:underline;text-underline-offset:3px}
.lead{font:italic 20px/1.5 Cambria,Georgia,serif;max-width:34em;margin-top:22px}
.idx{list-style:none;padding:0;margin-top:clamp(28px,6vh,56px);border-top:2px solid var(--ink)}
.idx a{display:grid;grid-template-columns:1.3em 1fr auto;align-items:baseline;gap:14px;padding:14px 6px;border-bottom:1.5px solid var(--ink);color:inherit;text-decoration:none;font:900 clamp(18px,4vw,52px)/1.05 "Arial Black","Helvetica Neue",Arial,sans-serif;text-transform:uppercase;transition:background .25s,color .25s,padding .25s}
.idx a:hover,.idx a:focus-visible{background:var(--ink);color:#ececec;padding-left:22px;outline:none}
.idx small{font:italic 400 clamp(13px,1.6vw,18px)/1 Cambria,Georgia,serif;text-transform:none}
.cat{margin-top:clamp(56px,10vh,110px)}
.cat-h{display:flex;align-items:baseline;gap:16px;border-bottom:2px solid var(--ink);padding-bottom:10px}
.cat-h span,.sh span{font:italic 400 clamp(30px,4.6vw,60px)/1 Cambria,Georgia,serif}
.cat-h h3,.sh h3{font:900 clamp(20px,3.2vw,42px)/1.05 "Arial Black","Helvetica Neue",Arial,sans-serif;text-transform:uppercase}
.pj{display:grid;grid-template-columns:repeat(12,1fr);gap:20px;margin-top:30px;align-items:end}
.pj-img{grid-column:1/span 6;display:block;color:inherit}
.pj-t{grid-column:8/span 5}
.pj.fl .pj-img{grid-column:7/span 6;grid-row:1}.pj.fl .pj-t{grid-column:1/span 5;grid-row:1}
.pj-img img{display:block;width:100%;object-fit:cover}
.pj-img .ph{transition:transform .3s,box-shadow .3s}
.pj-img:hover .ph,.pj-img:focus-visible .ph{transform:translate(-5px,-5px);box-shadow:9px 9px 0 var(--ink)}
.pj-n{display:block;font:900 clamp(64px,12vw,170px)/.8 "Arial Black",Arial,sans-serif;letter-spacing:-.04em;color:transparent;-webkit-text-stroke:1.5px var(--ink)}
.pj-t h4{font:900 clamp(20px,2.6vw,34px)/1.1 "Arial Black","Helvetica Neue",Arial,sans-serif;text-transform:uppercase;margin-top:18px}
.tg{display:flex;flex-wrap:wrap;gap:6px;margin:14px 0 18px}
.tg span{border:1.5px solid var(--ink);padding:5px 9px;font:700 10px/1 "Helvetica Neue",Arial,sans-serif;letter-spacing:.16em;text-transform:uppercase}
.go{font:700 12px/1 "Helvetica Neue",Arial,sans-serif;letter-spacing:.2em;text-transform:uppercase;color:inherit;text-decoration:none;border-bottom:1.5px solid var(--ink);padding-bottom:4px}
.go:hover,.go:focus-visible{background:var(--ink);color:#ececec;outline:none}
.ph{display:flex;align-items:flex-end;width:100%;padding:12px;background:repeating-linear-gradient(135deg,transparent 0 9px,rgba(21,21,21,.14) 9px 10px),var(--paper);border:1.5px dashed var(--ink);font:italic 15px/1.2 Cambria,Georgia,serif}
.ph b{font:700 10px/1 "Helvetica Neue",Arial,sans-serif;letter-spacing:.2em;text-transform:uppercase;margin-right:.9em}
.pend{font-style:italic;opacity:.65}
.meta{display:grid;grid-template-columns:repeat(4,1fr);background:var(--paper);box-shadow:0 18px 40px -18px rgba(0,0,0,.4);margin-top:32px}
.meta div{padding:16px 18px;border-right:1px solid rgba(21,21,21,.55)}.meta div:last-child{border:0}
.meta dt{font:700 10px/1 "Helvetica Neue",Arial,sans-serif;letter-spacing:.22em;text-transform:uppercase}
.meta dd{font-size:18px;margin-top:9px}
.pbody{display:grid;grid-template-columns:200px 1fr;gap:clamp(24px,5vw,64px);margin-top:48px}
.toc{position:sticky;top:84px;align-self:start;list-style:none;padding:0}
.toc button{display:grid;grid-template-columns:1.7em 1fr;width:100%;text-align:left;background:none;border:0;border-bottom:1px solid rgba(21,21,21,.45);padding:10px 4px;font:700 12px/1.3 "Helvetica Neue",Arial,sans-serif;color:var(--ink);cursor:pointer}
.toc button:hover,.toc button:focus-visible{background:var(--ink);color:#ececec;outline:none}
.sx{padding:clamp(26px,5vh,46px) 0;border-top:2px solid var(--ink);scroll-margin-top:80px}
.sh{display:flex;align-items:baseline;gap:14px}
.sc{display:grid;grid-template-columns:1fr 1fr;gap:28px;margin-top:22px;align-items:start}
.sx.fl .mm{order:-1}.sx.nm .sc{grid-template-columns:minmax(0,40em)}
.mm{display:grid;gap:16px}.mm img,.mm video{display:block}
.tx{font:19px/1.6 Cambria,Georgia,serif;background:rgba(244,244,242,.86);padding:20px}.tx p+p{margin-top:1em}
.tx.pd{background:transparent;border:1.5px dashed var(--ink);font-style:italic}.tx.pd b{font:700 10px/1 "Helvetica Neue",Arial,sans-serif;letter-spacing:.2em;text-transform:uppercase}
.pager{display:flex;justify-content:space-between;align-items:center;gap:16px;margin-top:56px;border-top:2px solid var(--ink);padding-top:20px}
.pager span{flex:1}.pager span:last-child{text-align:right}
.pg .rv2{opacity:0;transform:translateY(18px)}
.pg .rv2.in{opacity:1;transform:none;transition:opacity .7s ease,transform .7s cubic-bezier(.2,.7,.2,1)}
@media (max-width:760px){.pbody,.sc{grid-template-columns:1fr}.toc{display:none}.meta{grid-template-columns:1fr 1fr}.meta div{border-bottom:1px solid rgba(21,21,21,.55)}.pj{grid-template-columns:1fr}.pj-img,.pj-t,.pj.fl .pj-img,.pj.fl .pj-t{grid-column:1;grid-row:auto}.sx.fl .mm{order:0}}
@media (max-width:700px){.menu{top:auto;right:0;left:0;bottom:0;gap:0;padding-bottom:env(safe-area-inset-bottom);background:#f4f4f2;border-top:1.5px solid var(--ink)}.menu a{flex:1;text-align:center;border:0;border-right:1.5px solid var(--ink);padding:15px 4px;font-size:10px;letter-spacing:.14em}.menu a:last-child{border-right:0}.wrap{padding-bottom:96px}}
@media (prefers-reduced-motion:reduce){.pg .rv2{opacity:1;transform:none}.pg .rv2.in{transition:none}.idx a,.pj-img .ph{transition:none}}

/* RECORRIDO */
.cue{position:absolute;left:calc(40*var(--u));top:calc(836*var(--u));z-index:3;background:none;border:0;cursor:pointer;font:700 clamp(10px,calc(21*var(--u)),15px)/1 "Helvetica Neue",Arial,sans-serif;letter-spacing:.24em;text-transform:uppercase;color:var(--ink);text-shadow:0 0 8px #e2e2e2;animation:bob 2s ease-in-out infinite}
@keyframes bob{50%{transform:translateY(.5em)}}
@media (max-aspect-ratio:1/1){.cue{position:relative;left:auto;top:auto;order:4;margin-top:10px;font-size:11px}}
.menu.hm{transition:opacity .4s}.menu.hm:not(.show){opacity:0;visibility:hidden}
.flow{position:relative;background:radial-gradient(#8c8c8c 1.7px,transparent 2.2px) 0 0/16px 16px,#ececec}
.flow::before{content:"";position:absolute;left:0;right:0;bottom:100%;height:140px;background:linear-gradient(transparent,#ececec);pointer-events:none}
.fs{max-width:1240px;margin:0 auto;padding:clamp(60px,12vh,130px) clamp(20px,5vw,56px)}
.flow h2,.flow h2 em{font-size:clamp(38px,10vw,140px)}
.flow .grid{margin-bottom:36px}
.pl{translate:0 calc(var(--pp,0)*1px)}.pl2{translate:0 calc(var(--pp,0)*-.6px)}
.flow .rv3{opacity:0;transform:translateY(24px)}.flow .rv3.in{opacity:1;transform:none;transition:opacity .8s ease,transform .8s cubic-bezier(.2,.7,.2,1)}
.gfx{font:900 clamp(60px,16vw,230px)/.9 "Arial Black",Arial,sans-serif;letter-spacing:-.04em;color:transparent;-webkit-text-stroke:1.5px var(--ink);margin-top:70px}
.ct{max-width:420px;margin-top:36px}.ct dd.pend{font-size:18px}
.scene{margin:28px -56px 0}
.stick{position:sticky;top:0;height:100svh;display:flex;flex-direction:column;align-items:center;justify-content:center;gap:18px}
.mw{display:flex;align-items:center;justify-content:center;gap:clamp(10px,2vw,28px);flex-wrap:wrap;width:100%}
.arr{width:48px;height:48px;border:1.5px solid var(--ink);background:#f4f4f2;color:var(--ink);font:700 20px/1 Arial,sans-serif;cursor:pointer;transition:background .2s,color .2s}
.arr:hover,.arr:focus-visible{background:var(--ink);color:#f4f4f2;outline:none}
.mon{position:relative;width:min(calc(100vw - 150px),calc(76svh*1.6),1000px);background:var(--ink);padding:14px 14px 30px;border-radius:14px;box-shadow:0 40px 60px -30px rgba(0,0,0,.55)}
.mon::after{content:"";position:absolute;left:50%;top:100%;width:22%;height:6svh;margin-left:-11%;background:linear-gradient(90deg,#3a3a3a,#8a8a8a 45%,#3a3a3a);clip-path:polygon(18% 0,82% 0,100% 100%,0 100%)}
.mon::before{content:"";position:absolute;left:50%;top:calc(100% + 6svh - 6px);width:34%;height:8px;margin-left:-17%;background:var(--ink);border-radius:4px}
.scr{container-type:inline-size;aspect-ratio:16/10;background:radial-gradient(#8c8c8c 1.2px,transparent 1.7px) 0 0/12px 12px,#ececec;display:flex;flex-direction:column;overflow:hidden}
.bar{display:flex;justify-content:space-between;padding:1.3cqw 2cqw;background:var(--ink);color:#ececec;font:700 1.5cqw/1 "Helvetica Neue",Arial,sans-serif;letter-spacing:.2em;text-transform:uppercase}
.sb{flex:1;display:grid;grid-template-columns:30% 1fr;min-height:0}
.mi{list-style:none;padding:0;border-right:1.5px solid var(--ink)}
.mi button{display:flex;gap:1.4cqw;width:100%;text-align:left;background:none;border:0;border-bottom:1px solid rgba(21,21,21,.4);padding:1.6cqw 2cqw;font:700 1.7cqw/1.2 "Helvetica Neue",Arial,sans-serif;color:var(--ink);cursor:pointer}
.mi button:hover,.mi button[aria-current]{background:var(--ink);color:#ececec;outline:none}
.mp{padding:2.4cqw;overflow:hidden;min-height:0}
.slide{display:grid;grid-template-columns:1fr 1fr;gap:2cqw;align-items:end;height:100%;animation:swap .55s cubic-bezier(.2,.7,.2,1)}
@keyframes swap{from{opacity:0;transform:translateX(var(--dx))}}
.slide .pj-n{font-size:12cqw}.slide h4{font-size:2.6cqw;margin-top:1.4cqw}.slide .tg span{font-size:1.1cqw}.slide .go{font-size:1.3cqw}.slide .ph{max-height:100%;font-size:1.6cqw}
.pps{height:300svh;margin-top:28px}.pv{position:sticky;top:0;height:100svh;display:flex;align-items:center;justify-content:center;gap:clamp(20px,5vw,70px)}
.phn{width:min(300px,64vw);aspect-ratio:9/19;border:10px solid var(--ink);border-radius:40px;overflow:hidden;background:#ececec;position:relative;box-shadow:0 30px 60px -25px rgba(0,0,0,.5)}
.phn::before{content:"";position:absolute;top:8px;left:50%;width:70px;height:18px;margin-left:-35px;background:var(--ink);border-radius:9px;z-index:2}
.reel{display:flex;height:100%;will-change:transform}.sl{flex:0 0 100%;display:flex;flex-direction:column;justify-content:center;gap:10px;padding:44px 12px 16px}
.pcap{max-width:16em}.pcap .pj-n{font-size:clamp(56px,9vw,120px)}
@media (max-width:760px){.scene{margin:28px -20px 0}.mon{width:min(calc(100vw - 24px),calc(60svh*.8))}.scr{aspect-ratio:4/5}.sb{grid-template-columns:1fr;grid-template-rows:auto 1fr}.mi{display:flex;border:0;border-bottom:1.5px solid var(--ink)}.mi button{justify-content:center}.mi button b{display:none}.slide{grid-template-columns:1fr;align-content:center}.slide .pj-n{font-size:20cqw}.slide h4{font-size:4.6cqw}.slide .go{font-size:2.4cqw}.slide .tg span{font-size:2cqw}.slide .ph{display:none}.bar,.mi button{font-size:2.6cqw}.pv{flex-direction:column;gap:12px}.pcap{text-align:center}}
@media (prefers-reduced-motion:reduce){.cue,.slide{animation:none}.flow .rv3{opacity:1;transform:none}.flow .rv3.in{transition:none}.pl,.pl2{translate:none}}

/* AJUSTES: paleta, visor, ficha */
:root{--cin:#24292E;--chi:#4A5156;--sea:#808A92;--dol:#BDC7CE;--blm:#050505;--cha:#EFE1CE;--ros:#B9857C;--bc:#721D35;--bcd:#42121F;--nb:#1C0B12}
[data-t=inta]{--ac:#B4553A}[data-t=wak]{--ac:var(--bc)}
#proyecto .sh span,#proyecto h2 em{color:var(--ac,inherit)}
.scope{margin-top:18px;border-left:3px solid var(--ac,var(--ink));padding-left:14px;max-width:46em;font:italic 18px/1.5 Cambria,Georgia,serif}.scope b{font:700 10px/1 "Helvetica Neue",Arial,sans-serif;font-style:normal;letter-spacing:.2em;text-transform:uppercase;margin-right:.9em}
.pl3{list-style:none;padding:0;margin-top:1.6cqw;display:grid;gap:1.1cqw}
.cv{display:grid;grid-template-columns:repeat(2,1fr);gap:30px 44px;margin-top:44px;border-top:2px solid var(--ink);padding-top:26px}
.cv h3{font:900 clamp(16px,2vw,24px)/1.1 "Arial Black",Arial,sans-serif;text-transform:uppercase;color:var(--bc);margin-bottom:10px}
.cv ul{list-style:none;padding:0}.cv li{font:17px/1.5 Cambria,Georgia,serif;padding:7px 0;border-bottom:1px solid rgba(21,21,21,.25)}
.cam{position:relative;margin-top:50px;background:var(--nb);padding:34px 0;overflow:hidden}
.vf{position:absolute;inset:10px;z-index:2;pointer-events:none}.vf i{position:absolute;width:24px;height:24px;border:0 solid var(--ros)}
.vf i:nth-child(1){left:0;top:0;border-width:2px 0 0 2px}.vf i:nth-child(2){right:0;top:0;border-width:2px 2px 0 0}.vf i:nth-child(3){left:0;bottom:0;border-width:0 0 2px 2px}.vf i:nth-child(4){right:0;bottom:0;border-width:0 2px 2px 0}
.vf span{position:absolute;left:34px;bottom:4px;font:700 10px/1 "Helvetica Neue",Arial,sans-serif;letter-spacing:.2em;text-transform:uppercase;color:var(--ros)}
.strip{overflow:hidden}.trk{display:flex;width:max-content;animation:run 46s linear infinite}
.cam:hover .trk,.cam.paused .trk{animation-play-state:paused}
@keyframes run{to{transform:translateX(-50%)}}
.trk .ph,.trk img{flex:none;height:210px;width:auto;aspect-ratio:var(--r);margin-right:16px;color:var(--cha);border-color:var(--cha);background:repeating-linear-gradient(135deg,transparent 0 9px,rgba(239,225,206,.1) 9px 10px),var(--bcd)}.trk img{object-fit:cover;display:block}
.cpause{position:absolute;right:16px;bottom:12px;z-index:3;height:30px;padding:0 12px;background:var(--cha);color:var(--nb);border:0;font:700 10px/1 "Helvetica Neue",Arial,sans-serif;letter-spacing:.18em;text-transform:uppercase;cursor:pointer}
.cpause:focus-visible{outline:2px solid var(--ros);outline-offset:2px}
.ct{max-width:540px}.ct dd a{text-decoration:underline;text-underline-offset:3px;word-break:break-all}
@media (max-width:760px){.cv{grid-template-columns:1fr}.trk .ph,.trk img{height:170px}}
@media (prefers-reduced-motion:reduce){.trk{animation:none}.strip{overflow-x:auto}.cpause{display:none}}
````

## 3. JavaScript (interacciones, navegación y datos de proyectos)

````javascript
const D={"L":[{"line":0,"i":0,"x":20,"y":200,"w":199,"h":236,"src":"[IMAGEN_BASE64_01]"},{"line":0,"i":1,"x":219,"y":200,"w":64,"h":236,"src":"[IMAGEN_BASE64_02]"},{"line":0,"i":2,"x":283,"y":200,"w":155,"h":235,"src":"[IMAGEN_BASE64_03]"},{"line":0,"i":3,"x":438,"y":200,"w":124,"h":234,"src":"[IMAGEN_BASE64_04]"},{"line":0,"i":4,"x":562,"y":266,"w":162,"h":170,"src":"[IMAGEN_BASE64_05]"},{"line":0,"i":5,"x":724,"y":266,"w":143,"h":170,"src":"[IMAGEN_BASE64_06]"},{"line":0,"i":6,"x":868,"y":269,"w":63,"h":167,"src":"[IMAGEN_BASE64_07]"},{"line":0,"i":7,"x":931,"y":222,"w":154,"h":214,"src":"[IMAGEN_BASE64_08]"},{"line":0,"i":8,"x":1085,"y":204,"w":182,"h":229,"src":"[IMAGEN_BASE64_09]"},{"line":1,"i":0,"x":20,"y":436,"w":268,"h":324,"src":"[IMAGEN_BASE64_10]"},{"line":1,"i":1,"x":288,"y":436,"w":187,"h":324,"src":"[IMAGEN_BASE64_11]"},{"line":1,"i":2,"x":475,"y":436,"w":158,"h":322,"src":"[IMAGEN_BASE64_12]"},{"line":1,"i":3,"x":633,"y":436,"w":138,"h":322,"src":"[IMAGEN_BASE64_13]"},{"line":1,"i":4,"x":771,"y":439,"w":91,"h":320,"src":"[IMAGEN_BASE64_14]"},{"line":1,"i":5,"x":862,"y":436,"w":123,"h":323,"src":"[IMAGEN_BASE64_15]"},{"line":1,"i":6,"x":985,"y":436,"w":100,"h":322,"src":"[IMAGEN_BASE64_16]"},{"line":1,"i":7,"x":1085,"y":454,"w":70,"h":303,"src":"[IMAGEN_BASE64_17]"},{"line":1,"i":8,"x":1155,"y":445,"w":145,"h":313,"src":"[IMAGEN_BASE64_18]"}],"plate":"[IMAGEN_BASE64_19]","badge":"[IMAGEN_BASE64_20]","ext":"[IMAGEN_BASE64_21]","strap":"[IMAGEN_BASE64_22]"};
const R=document.documentElement,rs=R.style;
rs.setProperty('--plate','url('+D.plate+')');rs.setProperty('--ext','url('+D.ext+')');rs.setProperty('--strap','url('+D.strap+')');
document.getElementById('badgeimg').src=D.badge;
const tb=document.getElementById('tb'),reduce=matchMedia('(prefers-reduced-motion:reduce)').matches;
D.L.forEach(l=>{const s=document.createElement('span');s.className='g';
 s.style.cssText='--x:'+l.x+';--y:'+l.y+';--w:'+l.w+';--h:'+l.h+';--d:'+((l.line?750:250)+l.i*85)+'ms;background-image:url('+l.src+')';tb.appendChild(s)});
const gs=tb.querySelectorAll('.g'),hint=document.getElementById('hint');
let n=0;const fin=()=>{tb.classList.add('static');hint.classList.add('show')};
if(reduce)fin();else gs.forEach(g=>g.addEventListener('animationend',()=>{if(++n===gs.length)fin()}));
const $=id=>document.getElementById(id),esc=s=>String(s).replace(/[&<>"]/g,c=>({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;'}[c]));
const home=$('home'),about=$('about'),PG={home,about,archivo:$('archivo'),proyecto:$('proyecto')};
const CATS=[['estrategica','Comunicación estratégica'],['institucional','Comunicación institucional'],['audiovisual','Audiovisual y documental'],['diseno','Diseño visual y editorial'],['investigacion','Investigación y academia']];
const SEC=[['Contexto','Origen del proyecto, situación y antecedentes.'],['Objetivos comunicacionales','Qué se buscó comunicar y con qué propósito.'],['Proceso de trabajo','Etapas, decisiones y metodología utilizadas.'],['Desarrollo','Cómo se construyó la propuesta y su enfoque conceptual.'],['Producción','Piezas, herramientas, recursos y materiales desarrollados.'],['Resultados','Productos finales y resultados verificables.'],['Mi participación','Responsabilidades, aportes y tareas dentro del proyecto.']];
const PHS=[[['Antecedente','4/5']],[],[['Foto de proceso','3/2']],[['Concepto','1/1']],[['Video o pieza','16/9'],['Material original','4/5']],[['Producto final','4/5']],[]];
const RT=['4/5','16/9','1/1','3/4','21/9'];
/* PROYECTOS: completar acá. Cada objeto es una página. Lo vacío se muestra como "pendiente".
   Ejemplo: title:'…', year:'…', format:'…', role:'…', cover:'foto.jpg', tags:['…'],
   sections:{'Contexto':'texto'}, media:{'Producción':[{src:'img.jpg',alt:'…',ratio:'4/5'},{video:'clip.mp4',ratio:'16/9'}]}
   Para sumar un proyecto, agregá otro objeto con un slug nuevo (proyecto-06) y su categoría (cat). */
const P=[
{slug:'proyecto-01',cat:'estrategica',cats:['estrategica','institucional','diseno'],title:'Territorios que Alimentan',year:'2026',format:'Experiencia colectiva y voluntaria',role:'Diseño de carruseles para redes; ideación y contenidos',scope:'Trabajo colectivo y voluntario con el área de comunicación de INTA Regional Salta-Jujuy y la EEA Salta. Aporte individual: diseño de varios carruseles con fotografías del trabajo y participación en la ideación colectiva y el desarrollo de contenidos. No se atribuye en solitario la planificación ni la producción audiovisual.',cover:'',tags:[],kind:'social',theme:'inta',sections:{'Contexto':`Evento «Territorios que Alimentan | Sembrando identidad y cosechando futuro», vinculado al área de comunicación de INTA Regional Salta-Jujuy y la EEA Salta. Se realizó el 11 de agosto de 2026, 09:30 hs, en INTA Cerrillos (Ruta Nac. 68, Km 172).`,'Mi participación':`Diseño de varios carruseles para redes sociales con fotografías del trabajo, y participación en la ideación colectiva y en el desarrollo de contenidos.`},media:{}},
{slug:'proyecto-02',cat:'estrategica',cats:['estrategica','diseno'],title:'Grupo CENOA / Autolux',year:'',format:'Pasantía breve en marketing',role:'',scope:'Pasantía de aproximadamente dos semanas. Se distingue entre propuestas no implementadas y piezas efectivamente publicadas.',cover:'',tags:[],kind:'social',theme:'',sections:{'Contexto':`Pasantía breve en marketing (aprox. 2 semanas) en Grupo CENOA / Autolux.`,'Resultados':`Propuestas no implementadas: estrategia y piezas para la Feria Potencia Salta (reels, historias y carrusel).\n\nPiezas creadas que sí se subieron a canales de la empresa: contenido de la sucursal Orán / pieza vertical (a confirmar según disponibilidad).`},media:{}},
{slug:'proyecto-03',cat:'audiovisual',cats:['audiovisual'],title:`WAK'A`,year:'2025',format:'Cortometraje académico',role:'Idea original, guion, producción general, dirección, dirección de arte y asistencia en montaje',scope:'Trabajo colectivo de la productora IMMA STELLAR, en la cátedra Teoría y Práctica de Cine (UNSa).',cover:'',tags:[],kind:'',theme:'wak',sections:{'Contexto':`Cortometraje académico (2025) realizado en Teoría y Práctica de Cine, UNSa, bajo la productora colectiva IMMA STELLAR. Nombre definitivo: WAK'A.`,'Producción':`Materiales de referencia: afiche oficial, fotografías, tráiler/teaser (15/10/25), película completa, dossier y PDF de la exposición final de pitching.`,'Resultados':`Reconocimiento «Mejor Producción en general», por votación dentro de la cátedra.`,'Mi participación':`Idea original y modificaciones en el guion (junto a Lizeth Rivera), producción general, dirección, dirección de arte/estética (incluye el criterio sobre la indumentaria típica en escena, consignada como escenografía y maquillaje en el dossier) y asistencia en montaje.`},media:{}},
{slug:'proyecto-04',cat:'audiovisual',cats:['audiovisual'],title:'Giménez Viajes — 48 horas de crisis',year:'',format:'Video de apoyo a una investigación',role:'Producción del video, guion, voz en off y edición',scope:'No formé parte del equipo de investigación. El video acompañó una investigación en comunicación estratégica.',cover:'',tags:[],kind:'',theme:'',sections:{'Contexto':`Video de apoyo a una investigación en comunicación estratégica, utilizado en talleres en universidades de México en el marco de una red de investigación originada en la Universidad Católica de Salta (UCASAL). No formé parte del equipo de investigación.`,'Producción':`Producción desde cero a partir de fotografías provistas y reconstrucción de guion, con voz en off y edición propia. Se usó IA para generar algunas imágenes con fines de simulación o recreación y para resguardar el anonimato y el uso de imagen de las personas.`,'Mi participación':`Producción del video desde cero, reconstrucción del guion, voz en off y edición.`},media:{}}
].map(p=>({year:'',format:'',role:'',cover:'',tags:[],sections:{},media:{},kind:'',theme:'',scope:'',...p}));
const pad=n=>String(n).padStart(2,'0'),catName=k=>CATS.find(c=>c[0]===k)[1],pend='<span class="pend">Pendiente</span>';
document.querySelectorAll('.menu').forEach(m=>m.innerHTML=[['home','inicio','Inicio'],['about','about','Sobre mí'],['proyectos','proyectos','Proyectos'],['contacto','contacto','Contacto']].map(([p,h,t])=>`<a href="#${h}" data-p="${p}">${t}</a>`).join(''));
const card=p=>{const i=P.indexOf(p),n=pad(i+1),h='#'+p.slug,fl=CATS.findIndex(c=>c[0]===p.cat)%2?' fl':'';
 return `<article class="pj${fl}"><a class="pj-img" href="${h}" aria-label="Abrir proyecto ${n}">${p.cover?`<img src="${esc(p.cover)}" alt="" style="aspect-ratio:${RT[i%5]}">`:`<div class="ph" style="aspect-ratio:${RT[i%5]}"><b>Pendiente</b>Imagen principal</div>`}</a><div class="pj-t"><span class="pj-n">${n}</span><h4>${p.title?esc(p.title):'Título pendiente'}</h4><div class="tg"><span>${catName(p.cat)}</span>${p.title?'':'<span>Contenido pendiente</span>'}${p.tags.map(t=>`<span>${esc(t)}</span>`).join('')}</div><a class="go" href="${h}">Ver proyecto ↗</a></div></article>`};
$('idx').innerHTML=CATS.map(([k,n],i)=>{const c=P.filter(p=>p.cats.includes(k)).length;return `<li><a href="#categoria-${k}"><span>${i+1}</span><span>${n}</span><small>${c} proyecto${c==1?'':'s'}</small></a></li>`}).join('');
$('cats').innerHTML=CATS.map(([k,n],i)=>`<section class="cat rv2" id="cat-${k}"><header class="cat-h"><span>${i+1}</span><h3>${n}</h3></header>${(L=>L.length?L.map(card).join(''):'<p class="tx pd" style="margin-top:24px"><b>Contenido pendiente de cargar</b></p>')(P.filter(p=>p.cats.includes(k)))}</section>`).join('');
const phone=()=>`<div class="pps"><div class="pv"><div class="phn"><div class="reel">${[1,2,3,4,5].map(n=>`<div class="sl"><div class="ph" style="aspect-ratio:1/1"><b>Pendiente</b>Pieza ${n}</div><p class="pend">Texto de la publicación pendiente.</p></div>`).join('')}</div></div><div class="pcap"><span class="pj-n pn">01</span><p class="pend">Maqueta de carrusel para redes: las piezas avanzan con el scroll.</p></div></div></div>`;
function renderProject(p){$('proyecto').dataset.t=p.theme||'';const i=P.indexOf(p),pv=P[i-1],nx=P[i+1],v=x=>x?esc(x):pend;
 $('pw').innerHTML=`<h2 class="rv2">${p.title?esc(p.title):'Título'}${p.title?'':'<em>pendiente</em>'}</h2>
<dl class="meta rv2"><div><dt>Categoría</dt><dd>${p.cats.map(catName).join(' · ')}</dd></div><div><dt>Año</dt><dd>${v(p.year)}</dd></div><div><dt>Formato</dt><dd>${v(p.format)}</dd></div><div><dt>Rol</dt><dd>${v(p.role)}</dd></div></dl>${p.scope?`<p class="scope rv2"><b>Alcance</b>${esc(p.scope)}</p>`:''}
<div class="pbody"><ol class="toc" aria-label="Apartados">${SEC.map((s,j)=>`<li><button type="button" data-s="${j}"><span>${j+1}</span>${s[0]}</button></li>`).join('')}</ol><div>${SEC.map(([name,fn],j)=>{
 const t=p.sections[name],m=p.media[name],md=(m&&m.length?m.map(x=>x.video?`<video controls preload="metadata" src="${esc(x.video)}" style="width:100%;aspect-ratio:${x.ratio||'16/9'}"></video>`:`<img src="${esc(x.src)}" alt="${esc(x.alt||'')}" style="width:100%;aspect-ratio:${x.ratio||'4/5'};object-fit:cover">`):PHS[j].map(([l,r])=>`<div class="ph" style="aspect-ratio:${r}"><b>Pendiente</b>${l}</div>`)).join('');
 return `<section class="sx rv2${j%2?' fl':''}${md?'':' nm'}" id="s${j}"><div class="sh"><span>${j+1}</span><h3>${name}</h3></div><div class="sc"><div>${t?`<div class="tx">${t.split('\n\n').map(x=>`<p>${esc(x)}</p>`).join('')}</div>`:`<div class="tx pd"><b>Contenido pendiente</b><br>${fn}</div>`}</div>${md?`<div class="mm">${md}</div>`:''}</div>${p.kind==='social'&&j===4?phone():''}</section>`}).join('')}</div></div>
<nav class="pager" aria-label="Entre proyectos"><span>${pv?`<a class="go" href="#${pv.slug}">← Proyecto ${pad(i)}</a>`:''}</span><a class="go" href="#archivo">Volver al archivo</a><span>${nx?`<a class="go" href="#${nx.slug}">Proyecto ${pad(i+2)} →</a>`:''}</span></nav>`;
 $('pw').querySelectorAll('.toc button').forEach(b=>b.onclick=()=>$('s'+b.dataset.s).scrollIntoView({behavior:reduce?'auto':'smooth'}))}
function reveal(pg){pg._io&&pg._io.disconnect();const io=pg._io=new IntersectionObserver(es=>es.forEach(e=>{if(e.isIntersecting){e.target.classList.add('in');io.unobserve(e.target)}}),{root:pg,threshold:.08});pg.querySelectorAll('.rv2').forEach(e=>{e.classList.remove('in');io.observe(e)})}
let first=true,cur=-1;
const clamp=(v,a=0,b=1)=>Math.min(b,Math.max(a,v)),prog=e=>{const r=e.getBoundingClientRect();return clamp(-r.top/(r.height-innerHeight))},beh=()=>reduce||first?'auto':'smooth';
const sc=$('scene');sc.style.height=`calc(100svh + ${(CATS.length-1)*65}svh)`;
sc.innerHTML=`<div class="stick"><div class="mw"><button class="arr" id="prv" type="button" aria-label="Proyecto anterior">←</button><div class="mon"><div class="scr"><div class="bar"><span>VAC® archivo</span><span id="ctr"></span></div><div class="sb"><ol class="mi" aria-label="Índice de proyectos">${CATS.map((c,i)=>`<li><button type="button" data-i="${i}"><span>${pad(i+1)}</span><b>${c[1]}</b></button></li>`).join('')}</ol><div class="mp" id="mp" aria-live="polite"></div></div></div></div><button class="arr" id="nxt" type="button" aria-label="Proyecto siguiente">→</button></div><a class="go" href="#archivo">Ver archivo completo</a></div>`;
function setMon(i){const d=i>cur?1:-1,c=CATS[i],L=P.filter(p=>p.cats.includes(c[0]));cur=i;$('ctr').textContent=pad(i+1)+' / '+pad(CATS.length);
 sc.querySelectorAll('.mi button').forEach(b=>+b.dataset.i===i?b.setAttribute('aria-current','true'):b.removeAttribute('aria-current'));
 $('mp').innerHTML=`<div class="slide" style="--dx:${d*40}px"><div><span class="pj-n">${pad(i+1)}</span><h4>${c[1]}</h4>${L.length?`<ul class="pl3">${L.map(p=>`<li><a class="go" href="#${p.slug}">${esc(p.title)} ↗</a></li>`).join('')}</ul>`:'<div class="tg"><span>Contenido pendiente de cargar</span></div>'}</div><div class="ph" style="aspect-ratio:${RT[i]}"><b>Pendiente</b>Vista previa</div></div>`}
function goTo(i){i=clamp(i,0,CATS.length-1);const r=sc.offsetHeight-innerHeight,t=home.scrollTop+sc.getBoundingClientRect().top-home.getBoundingClientRect().top;home.scrollTo({top:t+(i+.5)/CATS.length*r,behavior:reduce?'auto':'smooth'})}
sc.addEventListener('click',e=>{const b=e.target.closest('button');if(!b)return;if(b.dataset.i)goTo(+b.dataset.i);if(b.id==='prv')goTo(cur-1);if(b.id==='nxt')goTo(cur+1)});
$('cue').onclick=()=>$('sm').scrollIntoView({behavior:reduce?'auto':'smooth'});
const g=about.querySelector('.grid').cloneNode(true);g.querySelectorAll('.rv').forEach(e=>{e.classList.remove('rv');e.classList.add('rv3')});g.querySelector('.card').classList.add('pl');g.querySelector('.copy').classList.add('pl2');$('smx').appendChild(g);
$('igc').appendChild(about.querySelector('.ig').cloneNode(true));
const fio=new IntersectionObserver(es=>es.forEach(e=>{if(e.isIntersecting){e.target.classList.add('in');fio.unobserve(e.target)}}),{root:home,threshold:.08});document.querySelectorAll('.flow .rv3').forEach(e=>fio.observe(e));
function tick(){$('hm').classList.toggle('show',home.scrollTop>innerHeight*.5);
 const i=Math.min(CATS.length-1,Math.floor(prog(sc)*CATS.length));if(i!==cur)setMon(i);
 document.querySelectorAll('.pps').forEach(e=>{const q=prog(e),n=5;e.querySelector('.reel').style.transform=`translateX(${-q*(n-1)*100}%)`;e.querySelector('.pn').textContent=pad(Math.round(q*(n-1))+1)});
 if(!reduce)document.querySelectorAll('.pl,.pl2').forEach(e=>{const r=e.getBoundingClientRect();e.style.setProperty('--pp',(r.top+r.height/2-innerHeight/2)/innerHeight*-28)})}
const PHOTOS=[];/* Fotos reales del visor: rutas a archivos existentes en la carpeta, ej. 'fotos/01.jpg'. Vacío = marcadores pendientes. */
const VR=['4/5','3/2','1/1','16/9','3/4','4/5'],fr=n=>PHOTOS[n]?`<img src="${esc(PHOTOS[n])}" alt="" style="aspect-ratio:${VR[n%6]}">`:`<div class="ph" style="--r:${VR[n%6]}"><b>Pendiente</b>Fotografía ${pad(n+1)}</div>`,set=Array.from({length:Math.max(PHOTOS.length,6)},(_,n)=>fr(n)).join('');
$('strip').innerHTML=`<div class="trk">${set}<span aria-hidden="true" style="display:contents">${set}</span></div>`;
$('cp').onclick=()=>{const q=$('cam').classList.toggle('paused');$('cp').setAttribute('aria-pressed',q);$('cp').textContent=q?'Reanudar':'Pausar'};
let tk=0;const req=()=>tk||(tk=requestAnimationFrame(()=>{tk=0;tick()}));
home.addEventListener('scroll',req,{passive:true});PG.proyecto.addEventListener('scroll',req,{passive:true});addEventListener('resize',req);
function show(p,arg){
 Object.entries(PG).forEach(([k,el])=>{const on=k===p;el.classList.toggle('on',on);el.setAttribute('aria-hidden',!on);el.inert=!on});
 const cu=p==='home'?(arg||'home'):p==='about'?'about':'proyectos';
 document.querySelectorAll('.menu a').forEach(a=>a.dataset.p===cu?a.setAttribute('aria-current','page'):a.removeAttribute('aria-current'));
 const el=PG[p];if(p==='proyecto')renderProject(arg);
 if(p!=='home'){el.scrollTop=0;reveal(el)}
 if(p==='home'){const t=arg&&$(arg==='proyectos'?'pr':arg);t?t.scrollIntoView({behavior:beh()}):home.scrollTop=0}
 req();if(first&&p==='home')return;
 setTimeout(()=>{if(p==='archivo'&&arg){const c=$('cat-'+arg);c&&c.scrollIntoView({behavior:reduce?'auto':'smooth'})}
  if(p==='home'&&arg)return;(p==='home'?$('badge'):el.querySelector('.back')||el.querySelector('.menu a[aria-current]')).focus({preventScroll:true})},reduce?0:500)}
function route(){const h=decodeURIComponent(location.hash.slice(1)),pr=P.find(x=>x.slug===h);
 if(h==='about'||h==='archivo')return show(h);
 if(h==='proyectos'||h==='contacto')return show('home',h);
 if(h.startsWith('categoria-')&&CATS.some(c=>c[0]===h.slice(10)))return show('archivo',h.slice(10));
 if(pr)return show('proyecto',pr);
 show('home')}
$('badge').addEventListener('click',()=>{location.hash='about'});
document.querySelectorAll('[data-go]').forEach(b=>b.addEventListener('click',()=>{try{location.hash='inicio'}catch(e){}route()}));
addEventListener('popstate',route);
route();first=false;
````
