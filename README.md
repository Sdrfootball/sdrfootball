## Hi there 👋

<!--
**Sdrfootball/sdrfootball** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
--><div class="card">
    <h2>📊 Maç Programı</h2>
    <div id="maclar">Yükleniyor...</div>
</div>

<script>
fetch("SHEET_URL_JSON")
.then(res => res.json())
.then(data => {
    let html = "";
    data.forEach(mac => {
        html += `
        <p><strong>${mac.EvSahibi}</strong> vs <strong>${mac.Deplasman}</strong><br>
        📅 ${mac.Tarih} | ⏰ ${mac.Saat} | 🏟️ ${mac.Stadyum}</p><hr>`;
    });
    document.getElementById("maclar").innerHTML = html;
});
</script>
