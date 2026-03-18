<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Scholarship Opportunities</title>
<style>
body{font-family:-apple-system,BlinkMacSystemFont,"Segoe UI",Roboto,Helvetica,Arial,sans-serif;margin:0;background:#ffffff;color:#111;display:flex;flex-direction:column;height:100vh} 
.site-header{border-bottom:1px solid #e6e6e6;background:#fff;padding:20px}

.header-inner{max-width:900px;margin:0 auto;display:flex;align-items:center;gap:20px}

.header-image-wrap{flex:0 0 auto}

.header-image-wrap img{width:120px;height:auto;display:block;border-radius:8px}

.header-copy{flex:1}

.header-copy h1{margin:0;font-size:26px;font-weight:600;letter-spacing:-0.02em}

.subtitle{margin-top:6px;color:#666;font-size:14px;line-height:1.4}

@media (max-width:600px){
  .header-inner{flex-direction:column;align-items:flex-start}
  .header-image-wrap img{width:100px}
}
.header-image{display:block;margin:16px auto 8px auto;max-width:220px;height:auto}
header h1{margin:0;font-size:28px;font-weight:600;letter-spacing:-0.02em}
header p{margin-top:6px;color:#666;font-size:14px}

/* responsive column layout */
.container{display:grid;grid-template-columns: repeat(4, 260px);justify-content:center;gap:18px;padding:24px;box-sizing:border-box;flex:1;overflow-y: auto;overflow:hidden}
@media (max-width: 1200px) {
  .container { grid-template-columns: repeat(3, 260px); }
}
@media (max-width: 900px) {
  .container { grid-template-columns: repeat(2, 260px); }
}
@media (max-width: 520px) {
  .container { grid-template-columns: 1fr; justify-items: center; }
}

.column {
  background: #fff;
  border: 1px solid #e8e8e8;
  border-radius: 10px;
  padding: 0 0 10px 0; /* remove top padding */
  height: 100%;
  overflow-y: auto;
  overflow-x: hidden;
}

.card{background:#fff;border:1px solid #ececec;border-radius:8px;margin-bottom:12px;padding:10px;cursor:pointer;transition:transform .08s ease,box-shadow .08s ease,opacity .35s ease;opacity:0}
.card.loaded{opacity:1}
.card:hover{transform:translateY(-2px);box-shadow:0 4px 10px rgba(0,0,0,0.06)}

/* Default card icons */
.card img:not(.yt-thumb) {
  width: 32px;
  height: 32px;
  aspect-ratio: 1/1;
  object-fit: contain;
  border-radius: 6px;
  margin-bottom: 6px;
  background: #f6f6f6;
  padding: 4px;
  display: block;
}

.card h3{margin:4px 0 4px;font-size:14px;font-weight:600;display:-webkit-box;-webkit-line-clamp:2;-webkit-box-orient:vertical;overflow:hidden;word-break:break-word}
.card p{margin:0;font-size:12px;color:#666;line-height:1.35;display:-webkit-box;-webkit-line-clamp:3;-webkit-box-orient:vertical;overflow:hidden;word-break:break-word}

.skeleton{pointer-events:none;opacity:1}
.skeleton div{border-radius:6px}

.sk-img{width:100%;aspect-ratio:16/9;margin-bottom:6px}
.sk-title{height:14px;width:70%;margin:6px 0}
.sk-desc{height:12px;width:90%}

.skeleton .sk-img,
.skeleton .sk-title,
.skeleton .sk-desc{
 background:linear-gradient(90deg,#f0f0f0 25%,#e6e6e6 37%,#f0f0f0 63%);
 background-size:400% 100%;
 animation:shimmer 1.4s ease infinite;
}

@keyframes shimmer{
 0%{background-position:100% 0}
 100%{background-position:-100% 0}
}

/* footer */
.site-footer{border-top:1px solid #e6e6e6;background:#fff;margin-top:20px}
.footer-inner{max-width:900px;margin:0 auto;padding:18px 20px;display:flex;align-items:center;gap:16px;justify-content:center}
.footer-logo img{width:90px;height:auto;display:block}
.footer-text{font-size:12px;color:#666}

@media (max-width:600px){
  .footer-inner{flex-direction:column;text-align:center}
}


/* column title card */
.column-title {
  font-size: 16px;
  font-weight: 600;
  text-align: center;
  margin: 0;
  padding: 18px 0; /* remove side padding */
  width: 100%;     /* full width */
  border-radius: 10px 10px 0 0;
  background: #ffffff;
  position: sticky;
  top: 0;
  z-index: 3;
  box-shadow: 0 2px 4px rgba(0,0,0,0.06);
  border-bottom: 1px solid #e0e0e0;
}

.column.expanded .sticky-header-wrapper {
  position: sticky;
  top: 0;
  z-index: 60;
  background: #ffffff;
}

/* Expanded column mode */
.column.expanded {
  position: fixed;
  overflow-y: auto;
  z-index: 20;
  grid-column: 1 / -1; /* span full width */
  max-width: 900px;
  margin: 0 auto;
  box-shadow: 0 0 20px rgba(0,0,0,0.15);
  transform: scale(1.02);
  transition: transform 0.25s ease, box-shadow 0.25s ease;
}

/* Shrink other columns */
.column.shrunk {
  opacity: 0.25;
  transform: scale(0.95);
  pointer-events: none;
  transition: opacity 0.25s ease, transform 0.25s ease;
}

/* Close button */
.close-expanded {
  position: sticky;
  top: 6px;
  float: right;
  font-size: 20px;
  font-weight: bold;
  cursor: pointer;
  padding: 4px 10px;
  border-radius: 6px;
  background: #eee;
  border: 1px solid #ccc;
  margin-bottom: 10px;
  z-index: 20;
}
.close-expanded:hover {
  background: #ddd;
}

/* Backdrop for dimming */
#backdrop {
  position: fixed;
  inset: 0;
  background: rgba(0,0,0,0.45);
  opacity: 0;
  pointer-events: none;
  transition: opacity 0.25s ease;
  z-index: 5;
}

#backdrop.active {
  opacity: 1;
  pointer-events: auto;
}

/* Expanded column becomes a fullscreen panel */
.column.expanded {
  position: fixed;
  top: 60px;        /* leaves room for header */
  left: 50%;
  transform: translateX(-50%);
  width: min(900px, 95vw);
  height: calc(90vh - 80px);
  overflow-y: auto;
  background: white;
  z-index: 20;
  padding-bottom: 40px;
  animation: slideFadeIn 0.35s ease forwards;
  box-shadow: 0 0 25px rgba(0,0,0,0.25);
  border-radius: 10px;
}

.column.expanded::-webkit-scrollbar-track {
  padding-top: 20px;
  padding-bottom: 20px;
}

/* Double-layer sticky header underlay */
.column.expanded::before {
  content: "";
  position: absolute; /* not sticky */
  top: 0;
  left: 0;
  right: 0;
  height: 48px;
  background: #ffffff;
  z-index: 10; /* sits behind wrapper */
  border-bottom: 1px solid #e5e5e5;
}

.column.expanded::after {
  content: "";
  position: sticky;
  top: 48px; /* same as ::before height */
  height: 12px;
  background: linear-gradient(to bottom, rgba(255,255,255,1), rgba(255,255,255,0));
  z-index: 15;
  display: block;
}

/* Slide + fade animation */
@keyframes slideFadeIn {
  from { transform: translate(-50%, -20px); opacity: 0; }
  to   { transform: translate(-50%, 0); opacity: 1; }
}

/* Snap-back animation */
@keyframes snapBack {
  from { transform: translate(-50%, 0) scale(1.02); }
  to   { transform: translate(-50%, 0) scale(1); }
}

.column.snap-back {
  animation: snapBack 0.2s ease;
}

/* Shrink background columns */
.column.shrunk {
  opacity: 0.15;
  transform: scale(0.96);
  transition: opacity 0.25s ease, transform 0.25s ease;
  pointer-events: none;
}

/* Close button above expanded column */
#close-expanded-btn {
  position: fixed;
  top: 32px;
  right: 32px;
  width: 42px;
  height: 42px;
  font-size: 24px;
  font-weight: 600;
  cursor: pointer;
  border-radius: 50%;
  background: white;
  border: 1px solid #d0d0d0;
  box-shadow: 0 4px 14px rgba(0,0,0,0.18);
  display: flex;
  align-items: center;
  justify-content: center;
  transition: opacity 0.25s ease, transform 0.15s ease;
  z-index: 200;
  opacity: 0;
  pointer-events: none;
}

#close-expanded-btn:hover {
  transform: scale(1.08);
  background: #f7f7f7;
}

#close-expanded-btn.active {
  opacity: 1;
  pointer-events: auto;
}

/* Sticky header inside expanded column */
.column.expanded .column-title {
  position: sticky;
  top: 0;
  background: #ffffff; /* solid white */
  padding: 18px 0;
  border-radius: 10px 10px 0 0;
  width: 100%;
  z-index: 70;
  border-bottom: 1px solid #dcdcdc;
  box-shadow: 0 2px 6px rgba(0,0,0,0.08); /* stronger separation */

}

/* Shorter scrollbars everywhere */
*::-webkit-scrollbar {
  width: 10px;   /* normal thickness */
}

*::-webkit-scrollbar-track {
  background: #f1f1f1;
  border-radius: 10px;
  background-clip: content-box; /* allows padding to shorten track */
  padding-top: 12px;            /* shortens scrollbar */
  padding-bottom: 12px;         /* shortens scrollbar */
}

*::-webkit-scrollbar-thumb {
  background: #c1c1c1;
  border-radius: 10px;
}

*::-webkit-scrollbar-thumb:hover {
  background: #a8a8a8;
}




</style>
</head>
<body>
<header class="site-header">
  <div class="header-inner">
    <div class="header-image-wrap">
      <img src="https://images.wakelet.com/resize?id=XPDFvqHkNHXx5KKFW7pN7&w=1280&h=960&q=85" alt="Header image" />
    </div>
    <div class="header-copy">
      <h1>Scholarship Opportunities</h1>
      <p class="subtitle">Check out all the links below to explore different options to help pay for your student's college or tech school education.</p>
    </div>
  </div>
</header>

<div class="container" id="columns"></div>
<div id="backdrop"></div>
<!-- YOUTUBE MODAL -->
<div id="youtube-modal" style="
  position: fixed;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: min(800px, 90vw);
  height: min(450px, 60vh);
  background: white;
  border-radius: 10px;
  box-shadow: 0 8px 30px rgba(0,0,0,0.35);
  display: none;
  flex-direction: column;
  z-index: 300;
  overflow: hidden;
">
  <div style="
    padding: 12px 16px;
    font-size: 16px;
    font-weight: 600;
    border-bottom: 1px solid #ddd;
  " id="youtube-modal-title"></div>

  <iframe
    id="youtube-iframe"
    width="100%"
    height="100%"
    style="border:0; flex:1;"
    allowfullscreen
  ></iframe>
</div>
<div id="close-expanded-btn">×</div>


<script>

const columnTitles = [
  "Scholarship Databases",
  "Scholarship Applications",
  "Military",
  "Career Tech"
];

const data = [
  {
    url: "https://www.ushli.org/",
    category: "Scholarship Databases",
    title: "USHLI",
    description: "USHLI is a nationally recognized, Chicago-based nonprofit dedicated to empowering communities through education, leadership development, civic engagement, and research.",
    favicon: "https://www.ushli.org/wp-content/uploads/2025/12/cropped-admin-ajax-32x32.png"
  },
  {
    url: "https://www.careeronestop.org/toolkit/training/find-scholarships.aspx",
    category: "Scholarship Databases",
    title: "Scholarship Finder | CareerOneStop",
    description: "Looking for scholarships? You can search more than 9,500 scholarships, fellowships, grants, and other financial aid award opportunities.",
    favicon: "https://www.careeronestop.org/favicon.ico"
  },
  {"url":"https://www.sallie.com/scholarships/scholly?utm_source=scholly&utm_medium=web","category":"Scholarship Databases"},
  {"url":"https://www.appily.com/","category":"Scholarship Databases"},
  {"url":"https://bold.org/","category":"Scholarship Databases"},
  {"url":"https://scholarshipowl.com/","category":"Scholarship Databases"},
  {"url":"https://www.earnest.com/blog/going-merry-closing-faqs","category":"Scholarship Databases"},
  {"url":"https://bigfuture.collegeboard.org/pay-for-college","category":"Scholarship Databases"},
  {"url":"https://www.scholarships.com/","category":"Scholarship Databases"},
  {"url":"https://occf.org/","category":"Scholarship Databases"},
  {"url":"https://www.okcollegestart.org/","category":"Scholarship Databases"},
  {"url":"https://www.okcollegestart.org/Financial_Aid_Planning/Scholarships/Scholarship_Links.aspx","category":"Scholarship Databases"},
  {"url":"https://www.fastweb.com/","category":"Scholarship Databases"},
  {"url":"https://www.hsf.net/scholarship","category":"Scholarship Databases"},
  {"url":"https://collegefund.org/students/scholarships/external-scholarships/","category":"Scholarship Databases"},

  {"url":"https://www.smartscholarship.org/smart","category":"Scholarship Applications"},
  {"url":"https://okpromise.org/","category":"Scholarship Applications"},
  {"url":"https://abbottandfenner.com/scholarships.php","category":"Scholarship Applications"},
  {"url":"https://www.lnesc.org/scholarships/lulac/","category":"Scholarship Applications"},
  {"url":"https://foundation.caionline.org/scholarships/recent-fellowship-recipients/hanke/","category":"Scholarship Applications"},
  {"url":"https://theactuarialfoundation.submittable.com/submit","category":"Scholarship Applications"},
  {"url":"https://www.dennys.com/hfe","category":"Scholarship Applications"},

  {"url":"https://goarmy.com","category":"Military"},
  {
    url: "https://www.afrotc.com/scholarships/",
    category: "Military",
    title: "U.S. Airforce ROTC",
    description: "Focus on school, not paying for it.",
    favicon: "https://www.afrotc.com/wp-content/uploads/2023/09/cropped-favicon-32x32.png"
  },
  {"url":"https://www.navy.com/careers-benefits/education/nrotc","category":"Military"},
  {"url":"https://www.nationalguard.com/careers/become-an-officer/rotc","category":"Military"},
  {"url":"https://www.smartscholarship.org","category":"Military"},

  {"url":"https://oklahoma.gov/careertech.html","category":"Career Tech"},
  {"url":"https://www.apprenticeship.gov/","category":"Career Tech"},
  {"url":"https://www.jobcorps.gov/","category":"Career Tech"},
  {"url":"https://www.youtube.com/watch?v=aircAruvnKk","category":"Career Tech"}
];

async function fetchPreview(site) {
  // Manual overrides take priority
  if (site.title || site.description || site.favicon) {
    return {
      title: site.title || null,
      description: site.description || null,
      favicon: site.favicon || null
    };
  }

  // Otherwise fetch from Microlink
  const api = `https://api.microlink.io/?url=${encodeURIComponent(site.url)}`;
  try {
    const res = await fetch(api);
    const json = await res.json();
    return {
      title: json?.data?.title || null,
      description: json?.data?.description || null,
      favicon: json?.data?.logo?.url || null
    };
  } catch (e) {
    return { title: null, description: null, favicon: null };
  }
}

function createSkeletonCard(){
 const card=document.createElement("div");
 card.className="card skeleton";
 card.innerHTML=`
   <div class="sk-img"></div>
   <div class="sk-title"></div>
   <div class="sk-desc"></div>
 `;
 return card;
}

function isYouTube(url) {
  return (
    url.includes("youtube.com") ||
    url.includes("youtu.be")
  );
}

function getYouTubeID(url) {
  try {
    const u = new URL(url);

    // youtu.be/<id>
    if (u.hostname === "youtu.be") {
      return u.pathname.slice(1);
    }

    // youtube.com/watch?v=<id>
    if (u.searchParams.get("v")) {
      return u.searchParams.get("v");
    }

    // youtube.com/shorts/<id>
    if (u.pathname.startsWith("/shorts/")) {
      return u.pathname.split("/shorts/")[1];
    }

    return null;
  } catch {
    return null;
  }
}

async function fetchYouTubeMeta(videoID) {
  const api = `https://www.youtube.com/oembed?url=https://www.youtube.com/watch?v=${videoID}&format=json`;

  try {
    const res = await fetch(api);
    const json = await res.json();

    return {
      title: json.title || "YouTube Video",
      description: json.author_name || "",
    };
  } catch (e) {
    return {
      title: "YouTube Video",
      description: "",
    };
  }
}

function fillCard(card, info, url) {
  const domain = new URL(url).hostname;
  const fallback = domain.replace("www.", "");

  const title =
    info.title && info.title.trim()
      ? info.title
      : fallback;

  const description =
    info.description && info.description.trim()
      ? info.description
      : fallback;

  const favicon =
    info.favicon ||
    `https://www.google.com/s2/favicons?sz=128&domain=${domain}`;

  // ⭐ YOUTUBE CARD HANDLING
  if (isYouTube(url)) {
    const videoID = getYouTubeID(url);
    const thumbnail = `https://img.youtube.com/vi/${videoID}/hqdefault.jpg`;

    // Fetch YouTube metadata
    fetchYouTubeMeta(videoID).then(meta => {
      const ytTitle = meta.title;
      const ytDesc = meta.description;

      card.classList.remove("skeleton");
      card.innerHTML = `
        <div style="position:relative; border-radius:8px; overflow:hidden; margin-bottom:10px;">
          <img class="yt-thumb" src="${thumbnail}" style="width:100%; display:block; border-radius:8px;">
          <div style="
            position:absolute;
            inset:0;
            display:flex;
            align-items:center;
            justify-content:center;
            background:rgba(0,0,0,0.35);
          ">
            <div style="
              width:60px;
              height:60px;
              border-radius:50%;
              background:white;
              display:flex;
              align-items:center;
              justify-content:center;
              box-shadow:0 4px 12px rgba(0,0,0,0.25);
            ">
              <div style="
                width:0;
                height:0;
                border-top:12px solid transparent;
                border-bottom:12px solid transparent;
                border-left:18px solid red;
                margin-left:4px;
              "></div>
            </div>
          </div>
        </div>
        <h3>${ytTitle}</h3>
        <p>${ytDesc}</p>
      `;

      // prevent column expansion
      card.onclick = (event) => {
        event.stopPropagation();
        openYouTubeModal(videoID, ytTitle);
      };

      requestAnimationFrame(() => card.classList.add("loaded"));
    });

    return;
  }

  // ⭐ NON-YOUTUBE CARD HANDLING
  card.classList.remove("skeleton");
  card.innerHTML = `
    <img loading="lazy" src="${favicon}"
         onerror="this.src='https://www.google.com/s2/favicons?sz=128&domain=${domain}'" />
    <h3>${title}</h3>
    <p>${description}</p>
    <p style="font-size:11px; color:#888; margin-top:6px; word-break:break-all;">
      ${url}
    </p>
  `;

  card.onclick = () => window.open(url, "_blank");

  requestAnimationFrame(() => card.classList.add("loaded"));
}

async function init(){
 const columnsContainer=document.getElementById("columns");
 const columns={};

 columnTitles.forEach(title=>{
  const col=document.createElement("div");
  col.className="column";

const headerWrapper = document.createElement("div");
headerWrapper.className = "sticky-header-wrapper";

const header = document.createElement("h2");
header.textContent = title;
header.className = "column-title";

headerWrapper.appendChild(header);
col.appendChild(headerWrapper);

  columnsContainer.appendChild(col);
  columns[title]=col;
 });

 enableColumnExpansion();

const previewPromises = data.map(site =>
  fetchPreview(site).then(preview => ({ site, preview }))
);

 // create skeletons immediately
 const skeletonMap=[];
 data.forEach(site=>{
  if(columns[site.category]){
   const skeleton=createSkeletonCard();
   columns[site.category].appendChild(skeleton);
   skeletonMap.push({site,card:skeleton});
  }
 });

 const results = await Promise.all(previewPromises);

 results.forEach(({site,preview})=>{
  if(!preview.title){
    preview.title = new URL(site.url).hostname.replace("www.","");
  }
  const item=skeletonMap.find(s=>s.site.url===site.url);
  if(item){
    fillCard(item.card,preview,site.url);
  }
 });
}

function enableColumnExpansion() {
  const container = document.getElementById("columns");
  const backdrop = document.getElementById("backdrop");
  const closeBtn = document.getElementById("close-expanded-btn");
  const columns = Array.from(container.getElementsByClassName("column"));

  columns.forEach(col => {
    const title = col.querySelector(".column-title");
    title.style.cursor = "pointer";

    title.addEventListener("click", () => {
      if (col.classList.contains("expanded")) return;

      // Smooth scroll to top
      window.scrollTo({ top: 0, behavior: "smooth" });

      // Shrink others
      columns.forEach(c => {
        if (c !== col) c.classList.add("shrunk");
      });

      // Expand this one
      col.classList.add("expanded");

      // Activate backdrop + close button
      backdrop.classList.add("active");
      closeBtn.classList.add("active");

      // Close handler
      closeBtn.onclick = () => collapseColumn(col, columns, backdrop, closeBtn);
    });
  });
}

function collapseColumn(col, allColumns, backdrop, closeBtn) {
  col.classList.add("snap-back");

  setTimeout(() => {
    col.classList.remove("expanded", "snap-back");

    allColumns.forEach(c => c.classList.remove("shrunk"));

    backdrop.classList.remove("active");
    closeBtn.classList.remove("active");
  }, 180);
}

function openYouTubeModal(videoID, title) {
  const modal = document.getElementById("youtube-modal");
  const iframe = document.getElementById("youtube-iframe");
  const titleEl = document.getElementById("youtube-modal-title");
  const backdrop = document.getElementById("backdrop");

  titleEl.textContent = title;

  // Show modal first (so it has real size)
  modal.style.display = "flex";
  backdrop.classList.add("active");

  // Delay iframe load so YouTube sees correct dimensions
  setTimeout(() => {
    iframe.src = `https://www.youtube.com/embed/${videoID}`;
  }, 50);

  backdrop.onclick = closeYouTubeModal;
}

function closeYouTubeModal() {
  const modal = document.getElementById("youtube-modal");
  const iframe = document.getElementById("youtube-iframe");
  const backdrop = document.getElementById("backdrop");

  modal.style.display = "none";
  backdrop.classList.remove("active");

  // Clear AFTER hiding to avoid flicker
  setTimeout(() => {
    iframe.src = "";
  }, 50);

  backdrop.onclick = null;
}


init();

</script>
<footer class="site-footer">
  <div class="footer-inner">
    <div class="footer-logo">
      <img src="https://k20center.ou.edu/wp-content/uploads/2020/02/k20center-logo-full-1.png" alt="Footer logo" />
    </div>
    <div class="footer-text">
      <div> </div>
      <div> </div>
    </div>
  </div>
</footer>

</body>
</html>
