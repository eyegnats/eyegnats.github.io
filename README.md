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
.container{display:grid;grid-template-columns:repeat(4,220px);justify-content:center;gap:18px;padding:24px;box-sizing:border-box;flex:1;overflow:hidden}
@media (max-width:1000px){.container{grid-template-columns:repeat(2,220px)}}
@media (max-width:520px){.container{grid-template-columns:1fr;justify-items:center}}

.column{background:#fff;border:1px solid #e8e8e8;border-radius:10px;padding:10px;height:100%;overflow-y:auto;overflow-x:hidden}

.card{background:#fff;border:1px solid #ececec;border-radius:8px;margin-bottom:12px;padding:10px;cursor:pointer;transition:transform .08s ease,box-shadow .08s ease,opacity .35s ease;opacity:0}
.card.loaded{opacity:1}
.card:hover{transform:translateY(-2px);box-shadow:0 4px 10px rgba(0,0,0,0.06)}

.card img{width:32px;height:32px;aspect-ratio:1/1;object-fit:contain;border-radius:6px;margin-bottom:6px;background:#f6f6f6;padding:4px;display:block}

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
.column-title{
  font-size:16px;
  font-weight:600;
  text-align:center;
  margin:0 0 10px 0;
  padding:10px 8px;
  border:1px solid #e9e9e9;
  border-radius:8px;
  background:#fafafa;
  position:sticky;
  top:0;
  z-index:2;
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
  {"url":"https://www.jobcorps.gov/","category":"Career Tech"}
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

  const header=document.createElement("h2");
  header.textContent=title;
  header.className="column-title";

  col.appendChild(header);
  columnsContainer.appendChild(col);
  columns[title]=col;
 });

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
