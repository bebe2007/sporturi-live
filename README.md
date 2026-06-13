<!DOCTYPE html>
<html lang="ro">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Tutorial Sporturi Live - CM 2026</title>

<style type="text/css">
  *{
    box-sizing:border-box;
  }

  body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background-color: #f5f5f5;
    margin: 0;
    padding: 0;
    color:#222;
  }

  .page{
    width:min(1200px,100%);
    margin:0 auto;
    padding:24px 14px 50px;
  }

  .hero{
    background:#ffffff;
    border-radius:12px;
    box-shadow:0 0 15px rgba(0, 0, 0, 0.1);
    padding:24px;
    margin-bottom:24px;
  }

  .hero h1{
    margin:0 0 12px;
    color:#222;
    font-size:32px;
    line-height:1.2;
    text-align:center;
  }

  .hero p{
    margin:0 auto 16px;
    max-width:850px;
    text-align:center;
    color:#444;
    font-size:16px;
    line-height:1.6;
  }

  .quick-links{
    display:flex;
    justify-content:center;
    flex-wrap:wrap;
    gap:10px;
    margin-top:18px;
  }

  .quick-links a{
    display:inline-block;
    padding:10px 16px;
    text-decoration:none;
    background-color:#007BFF;
    color:white;
    border-radius:6px;
    font-weight:700;
    transition:background-color 0.3s ease;
  }

  .quick-links a:hover{
    background-color:#0056b3;
  }

  .tutorial{
    background:#ffffff;
    border-radius:12px;
    box-shadow:0 0 15px rgba(0, 0, 0, 0.1);
    padding:22px;
    margin-bottom:24px;
  }

  .tutorial h2{
    text-align:center;
    margin:0 0 20px;
    color:#333;
  }

  .steps{
    display:grid;
    grid-template-columns:repeat(3,minmax(0,1fr));
    gap:14px;
  }

  .step{
    border:1px solid #e5e7eb;
    border-radius:10px;
    padding:16px;
    background:#fafafa;
  }

  .step strong{
    display:block;
    margin-bottom:8px;
    color:#007BFF;
    font-size:18px;
  }

  .step p{
    margin:0;
    color:#444;
    line-height:1.55;
    font-size:14px;
  }

  h2.table-title {
    text-align: center;
    margin: 0 0 20px;
    color: #333;
  }

  .table-container {
    width: 100%;
    background-color: #fff;
    border-radius: 8px;
    box-shadow: 0 0 15px rgba(0, 0, 0, 0.1);
    overflow-x: auto;
  }

  table {
    width: 100%;
    border-collapse: collapse;
  }

  th, td {
    padding: 15px;
    text-align: left;
    border-bottom: 1px solid #ddd;
    vertical-align:middle;
  }

  th {
    background-color: #f9f9f9;
    color: #333;
    font-size: 16px;
    text-transform: uppercase;
  }

  .event {
    cursor: pointer;
    background-color: #f9f9f9;
    transition: background-color 0.3s ease;
  }

  .event:hover {
    background-color: #007BFF;
    color: white;
  }

  .event .flag {
    background-color: transparent;
  }

  .links {
    display: none;
    background-color: #eef4f9;
  }

  .links a {
    display:inline-block;
    margin: 4px 8px 4px 0;
    padding: 8px 15px;
    text-decoration: none;
    background-color: #007BFF;
    color: white;
    border-radius: 4px;
    font-size: 14px;
    transition: background-color 0.3s ease;
  }

  .links a:hover {
    background-color: #0056b3;
  }

  .flag img {
    width: 30px;
    height: auto;
  }

  .live-btn {
    padding: 8px 15px;
    background-color: #28a745;
    color: white;
    border-radius: 4px;
    text-decoration: none;
    font-weight: bold;
    transition: background-color 0.3s ease;
  }

  .live-btn:hover {
    background-color: #218838;
  }

  .status-finished{
    color:#777;
    font-weight:700;
  }

  .status-upcoming{
    color:#007BFF;
    font-weight:700;
  }

  .status-live{
    color:#28a745;
    font-weight:900;
  }

  .loading,
  .error{
    text-align:center;
    padding:24px;
    background:#fff;
    border-radius:8px;
    box-shadow:0 0 15px rgba(0,0,0,.1);
    color:#333;
  }

  @media (max-width: 768px) {
    .hero h1{
      font-size:26px;
    }

    .steps{
      grid-template-columns:1fr;
    }

    th, td {
      padding: 10px;
      font-size: 14px;
    }

    .links a {
      padding: 5px 10px;
      font-size: 12px;
    }
  }

  @media (max-width: 480px) {
    .page{
      padding:14px 8px 34px;
    }

    table {
      font-size: 12px;
    }

    th, td {
      padding: 8px;
    }

    .live-btn {
      padding: 5px 10px;
      font-size: 12px;
    }
  }
</style>
</head>

<body>

<div class="page">

  <section class="hero">
    <h1>Sporturi Live - Tutorial CM 2026</h1>
    <p>
      Pe această pagină găsești un tutorial rapid pentru folosirea platformei Sporturi Live,
      plus lista completă de evenimente încărcată automat din fișierul <strong>eventos.json</strong>.
    </p>

    <div class="quick-links">
      <a href="https://bebe2007.github.io/sporturi-live/" target="_blank" rel="noopener">
        Deschide Sporturi Live
      </a>
      <a href="https://bebe2007.github.io/sporturi-live/eventos.json" target="_blank" rel="noopener">
        Vezi fișierul eventos.json
      </a>
      <a href="#tabel-evenimente">
        Vezi tabelul evenimentelor
      </a>
    </div>
  </section>

  <section class="tutorial">
    <h2>Cum folosești pagina Sporturi Live</h2>

    <div class="steps">
      <div class="step">
        <strong>1. Intră pe site</strong>
        <p>
          Accesează pagina principală Sporturi Live folosind butonul de mai sus sau link-ul:
          <br>
          <a href="https://bebe2007.github.io/sporturi-live/" target="_blank" rel="noopener">
            https://bebe2007.github.io/sporturi-live/
          </a>
        </p>
      </div>

      <div class="step">
        <strong>2. Alege evenimentul</strong>
        <p>
          Caută meciul dorit în listă. Poți verifica data, ora, competiția și echipele participante
          înainte să deschizi sursele video.
        </p>
      </div>

      <div class="step">
        <strong>3. Deschide sursele video</strong>
        <p>
          În tabelul de mai jos, apasă pe un eveniment pentru a afișa toate sursele disponibile.
          Fiecare buton deschide canalul video într-o filă nouă.
        </p>
      </div>
    </div>
  </section>

  <h2 class="table-title" id="tabel-evenimente">Tabel evenimente CM 2026</h2>

  <div id="loading" class="loading">Se încarcă evenimentele din eventos.json...</div>

  <div class="table-container" id="tableContainer" style="display:none;">
    <table>
      <thead>
        <tr>
          <th><strong>#</strong></th>
          <th><strong>Dată</strong></th>
          <th><strong>Ora</strong></th>
          <th><strong>Competiție</strong></th>
          <th><strong>Eveniment</strong></th>
        </tr>
      </thead>
      <tbody id="eventsBody"></tbody>
    </table>
  </div>

</div>

<script>
const EVENTS_URL = "eventos.json";

const eventsBody = document.getElementById("eventsBody");
const loading = document.getElementById("loading");
const tableContainer = document.getElementById("tableContainer");

let activeLink = null;

function escapeHTML(value){
  return String(value ?? "")
    .replaceAll("&","&amp;")
    .replaceAll('"',"&quot;")
    .replaceAll("<","&lt;")
    .replaceAll(">","&gt;");
}

function getEventName(event){
  const team1 = event.team1 || "";
  const team2 = event.team2 || "";

  if(team1 && team2){
    return `${team1} - ${team2}`;
  }

  return event.title || "Eveniment";
}

function getIcon(event){
  const sport = String(event.sport || "").toLowerCase();

  if(sport.includes("fotbal")) return "⚽";
  if(sport.includes("hochei")) return "🏒";
  if(sport.includes("baschet")) return "🏀";
  if(sport.includes("tenis")) return "🎾";
  if(sport.includes("handbal")) return "🤾";

  return "🏆";
}

function getStatusClass(status){
  const value = String(status || "").toLowerCase();

  if(value.includes("live") || value.includes("direct")) return "status-live";
  if(value.includes("finished") || value.includes("ended") || value.includes("final") || value.includes("terminat")) return "status-finished";

  return "status-upcoming";
}

function renderEvents(events){
  eventsBody.innerHTML = "";

  events.forEach((event, index) => {
    const eventId = index + 1;
    const streams = Array.isArray(event.streams) ? event.streams : [];

    const row = document.createElement("tr");
    row.className = "event";
    row.setAttribute("data-event", eventId);

    row.innerHTML = `
      <td class="flag">${getIcon(event)}</td>
      <td>${escapeHTML(event.day ? `${event.day}, ${event.date || ""}` : event.date || "")}</td>
      <td>${escapeHTML(event.time || "--:--")}</td>
      <td>
        ${event.competition_logo ? `<img src="${escapeHTML(event.competition_logo)}" alt="" style="width:24px;height:24px;object-fit:contain;vertical-align:middle;margin-right:6px;">` : ""}
        ${escapeHTML(event.competition || "Competiție")}
        ${event.stage ? `<br><small>${escapeHTML(event.stage)}</small>` : ""}
      </td>
      <td>
        ${event.team1_logo ? `<img src="${escapeHTML(event.team1_logo)}" alt="" style="width:26px;height:18px;object-fit:cover;vertical-align:middle;margin-right:6px;">` : ""}
        ${escapeHTML(getEventName(event))}
        ${event.team2_logo ? `<img src="${escapeHTML(event.team2_logo)}" alt="" style="width:26px;height:18px;object-fit:cover;vertical-align:middle;margin-left:6px;">` : ""}
        <br>
        <small class="${getStatusClass(event.status)}">${escapeHTML(event.status || "upcoming")}</small>
      </td>
    `;

    const linksRow = document.createElement("tr");
    linksRow.className = "links";
    linksRow.id = `links-${eventId}`;

    if(streams.length){
      linksRow.innerHTML = `
        <td colspan="5">
          ${streams.map((stream, streamIndex) => `
            <a href="${escapeHTML(stream.url || "#")}" target="_blank" rel="noopener">
              ${escapeHTML(stream.name || `Sursa ${streamIndex + 1}`)}
            </a>
          `).join("")}
        </td>
      `;
    }else{
      linksRow.innerHTML = `
        <td colspan="5">
          Nu există surse video disponibile pentru acest eveniment.
        </td>
      `;
    }

    row.addEventListener("click", () => {
      const currentLink = document.getElementById(`links-${eventId}`);

      if(activeLink && activeLink !== currentLink){
        activeLink.style.display = "none";
      }

      if(currentLink.style.display === "none" || !currentLink.style.display){
        currentLink.style.display = "table-row";
        activeLink = currentLink;
      }else{
        currentLink.style.display = "none";
        activeLink = null;
      }
    });

    eventsBody.appendChild(row);
    eventsBody.appendChild(linksRow);
  });
}

async function loadEvents(){
  try{
    const response = await fetch(EVENTS_URL, {cache:"no-store"});

    if(!response.ok){
      throw new Error("Nu pot încărca eventos.json");
    }

    const events = await response.json();

    if(!Array.isArray(events)){
      throw new Error("Fișierul eventos.json nu conține o listă validă.");
    }

    renderEvents(events);

    loading.style.display = "none";
    tableContainer.style.display = "block";
  }catch(error){
    loading.className = "error";
    loading.innerHTML = `
      Nu am putut încărca fișierul <strong>eventos.json</strong>.
      Verifică dacă acest fișier este în același folder cu pagina HTML.
    `;
  }
}

loadEvents();
</script>

</body>
</html>
