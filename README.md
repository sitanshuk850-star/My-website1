<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Join Our Team</title>
<style>
  * { margin: 0; padding: 0; box-sizing: border-box; font-family: 'Segoe UI', sans-serif; }
  body {
    background: linear-gradient(135deg, #667eea, #764ba2);
    min-height: 100vh;
    padding: 30px 15px;
  }
  .container { max-width: 750px; margin: 0 auto; }

  .header { text-align: center; color: white; margin-bottom: 25px; }
  .header h1 { font-size: 28px; margin-bottom: 8px; }
  .header p { opacity: 0.9; font-size: 14px; }

  .tabs { display: flex; gap: 10px; margin-bottom: 20px; }
  .tab {
    flex: 1; padding: 14px;
    background: rgba(255,255,255,0.2);
    color: white; border: none;
    border-radius: 12px; font-size: 15px;
    cursor: pointer; font-weight: 600; transition: 0.3s;
  }
  .tab.active { background: white; color: #667eea; }

  .card {
    background: white;
    border-radius: 20px;
    padding: 30px;
    box-shadow: 0 20px 60px rgba(0,0,0,0.3);
  }
  .section { display: none; }
  .section.active { display: block; animation: fadeIn 0.4s; }
  @keyframes fadeIn { from { opacity: 0; transform: translateY(10px); } to { opacity: 1; transform: translateY(0); } }

  .card h2 { color: #333; margin-bottom: 20px; font-size: 20px; }

  label { display: block; color: #555; margin-bottom: 6px; font-size: 14px; font-weight: 600; }
  input, select {
    width: 100%; padding: 12px;
    border: 2px solid #e0e0e0;
    border-radius: 10px; font-size: 15px;
    margin-bottom: 15px; outline: none;
    transition: 0.3s; background: white;
  }
  input:focus, select:focus { border-color: #667eea; }

  .row { display: grid; grid-template-columns: 1fr 1fr; gap: 15px; }
  @media (max-width: 500px) { .row { grid-template-columns: 1fr; } }

  .consent-box {
    background: #fff8e1;
    border-left: 4px solid #ffc107;
    padding: 15px;
    border-radius: 10px;
    margin-bottom: 20px;
  }
  .consent-box label {
    display: flex; align-items: flex-start; gap: 10px;
    color: #555; font-weight: 500; cursor: pointer; font-size: 13px;
    margin: 0;
  }
  .consent-box input[type="checkbox"] {
    width: auto; margin: 3px 0 0 0;
    transform: scale(1.3); cursor: pointer;
  }

  .btn {
    width: 100%; padding: 14px;
    background: #667eea; color: white;
    border: none; border-radius: 10px;
    font-size: 16px; font-weight: 600;
    cursor: pointer; transition: 0.3s;
  }
  .btn:hover { background: #5568d3; }
  .btn-danger { background: #e74c3c; }
  .btn-danger:hover { background: #c0392b; }

  .search-box { display: flex; gap: 10px; margin-bottom: 20px; }
  .search-box input { margin-bottom: 0; }
  .search-box button {
    padding: 12px 24px; background: #667eea; color: white;
    border: none; border-radius: 10px; cursor: pointer; font-weight: 600;
  }

  .person-card {
    background: #f8f9ff;
    border-left: 4px solid #667eea;
    padding: 18px;
    border-radius: 10px;
    margin-bottom: 12px;
    animation: fadeIn 0.3s;
    position: relative;
  }
  .person-card h3 { color: #333; margin-bottom: 10px; font-size: 17px; }
  .person-card p { color: #555; font-size: 14px; margin: 5px 0; }
  .person-card p strong { color: #333; }
  .delete-btn {
    position: absolute; top: 12px; right: 12px;
    background: #e74c3c; color: white; border: none;
    padding: 6px 12px; border-radius: 6px;
    cursor: pointer; font-size: 12px;
  }

  .msg {
    padding: 12px; border-radius: 10px;
    margin-top: 15px; font-size: 14px;
    display: none; text-align: center; font-weight: 600;
  }
  .msg.success { background: #d4edda; color: #155724; display: block; }
  .msg.error { background: #f8d7da; color: #721c24; display: block; }

  .empty { text-align: center; color: #888; padding: 30px; font-size: 14px; }
  .stats {
    background: #f0f4ff; padding: 15px;
    border-radius: 10px; margin-bottom: 20px;
    text-align: center; color: #667eea;
    font-weight: 600; font-size: 15px;
  }
  .export-btn {
    background: #28a745; color: white;
    padding: 10px 20px; border: none;
    border-radius: 8px; cursor: pointer;
    font-weight: 600; margin-bottom: 15px;
  }
</style>
</head>
<body>
  <div class="container">
    <div class="header">
      <h1>🚀 Join Our Team</h1>
      <p>Fill the form and we'll contact you soon</p>
    </div>

    <div class="tabs">
      <button class="tab active" onclick="showTab('join')">📝 Join Form</button>
      <button class="tab" onclick="showTab('admin')">🔐 Admin</button>
    </div>

    <div class="card">
      <!-- JOIN FORM -->
      <div class="section active" id="joinSection">
        <h2>Apni details bharein</h2>

        <label>Full Name *</label>
        <input type="text" id="jName" placeholder="Aapka pura naam">

        <div class="row">
          <div>
            <label>Age *</label>
            <input type="number" id="jAge" placeholder="Aapki age" min="15" max="100">
          </div>
          <div>
            <label>State *</label>
            <select id="jState">
              <option value="">Select State</option>
              <option>Andhra Pradesh</option>
              <option>Assam</option>
              <option>Bihar</option>
              <option>Chhattisgarh</option>
              <option>Delhi</option>
              <option>Goa</option>
              <option>Gujarat</option>
              <option>Haryana</option>
              <option>Himachal Pradesh</option>
              <option>Jharkhand</option>
              <option>Karnataka</option>
              <option>Kerala</option>
              <option>Madhya Pradesh</option>
              <option>Maharashtra</option>
              <option>Odisha</option>
              <option>Punjab</option>
              <option>Rajasthan</option>
              <option>Tamil Nadu</option>
              <option>Telangana</option>
              <option>Uttar Pradesh</option>
              <option>Uttarakhand</option>
              <option>West Bengal</option>
              <option>Other</option>
            </select>
          </div>
        </div>

        <label>WhatsApp Number *</label>
        <input type="tel" id="jWhatsapp" placeholder="+91 XXXXX XXXXX">

        <label>Email *</label>
        <input type="email" id="jEmail" placeholder="aapka@email.com">

        <div class="consent-box">
          <label>
            <input type="checkbox" id="jConsent">
            <span>Main <strong>consent deta/deti hoon</strong> ki meri ye information team join karne ke liye use ki jaye. Main jaanta hoon ki meri info safe rahegi aur kisi ke saath share nahi hogi.</span>
          </label>
        </div>

        <button class="btn" onclick="submitJoin()">Join Karein</button>
        <div class="msg" id="joinMsg"></div>
      </div>

      <!-- ADMIN PANEL -->
      <div class="section" id="adminSection">
        <div id="adminLogin">
          <h2>🔐 Admin Login</h2>
          <label>Password</label>
          <input type="password" id="adminPass" placeholder="Password daalein">
          <button class="btn" onclick="adminLogin()">Login</button>
          <div class="msg" id="loginMsg"></div>
          <p style="font-size:12px;color:#888;margin-top:15px;text-align:center;">Default password: <strong>admin123</strong> (ise change karna!)</p>
        </div>

        <div id="adminPanel" style="display:none;">
          <div style="display:flex;justify-content:space-between;align-items:center;margin-bottom:15px;">
            <h2 style="margin:0;">👥 Joiners List</h2>
            <button class="delete-btn" style="position:static;" onclick="logout()">Logout</button>
          </div>

          <div class="stats" id="stats">Total: 0 Joiners</div>

          <button class="export-btn" onclick="exportCSV()">📥 Export CSV</button>

          <div class="search-box">
            <input type="text" id="adminSearch" placeholder="Naam ya state se dhundein...">
            <button onclick="renderList()">Search</button>
          </div>

          <div id="peopleList"></div>
        </div>
      </div>
    </div>
  </div>

<script>
  const ADMIN_PASSWORD = "admin123"; // ← ise change karo!

  function getPeople() {
    return JSON.parse(localStorage.getItem('joiners') || '[]');
  }
  function savePeople(p) {
    localStorage.setItem('joiners', JSON.stringify(p));
  }

  function showTab(name) {
    document.querySelectorAll('.tab').forEach(t => t.classList.remove('active'));
    document.querySelectorAll('.section').forEach(s => s.classList.remove('active'));
    if (name === 'join') {
      document.querySelectorAll('.tab')[0].classList.add('active');
      document.getElementById('joinSection').classList.add('active');
    } else {
      document.querySelectorAll('.tab')[1].classList.add('active');
      document.getElementById('adminSection').classList.add('active');
    }
  }

  function submitJoin() {
    const name = document.getElementById('jName').value.trim();
    const age = document.getElementById('jAge').value.trim();
    const state = document.getElementById('jState').value;
    const whatsapp = document.getElementById('jWhatsapp').value.trim();
    const email = document.getElementById('jEmail').value.trim();
    const consent = document.getElementById('jConsent').checked;
    const msg = document.getElementById('joinMsg');

    if (!name || !age || !state || !whatsapp || !email) {
      msg.className = 'msg error';
      msg.textContent = '❌ Saari details bharna zaroori hai';
      return;
    }
    if (!consent) {
      msg.className = 'msg error';
      msg.textContent = '❌ Consent dena zaroori hai';
      return;
    }
    if (age < 15 || age > 100) {
      msg.className = 'msg error';
      msg.textContent = '❌ Age 15 se 100 ke beech honi chahiye';
      return;
    }

    const people = getPeople();
    people.push({
      id: Date.now(),
      name, age, state, whatsapp, email,
      date: new Date().toLocaleString()
    });
    savePeople(people);

    msg.className = 'msg success';
    msg.textContent = '✅ Thank you! Aapki details mil gayi. Hum jaldi contact karenge.';

    document.getElementById('jName').value = '';
    document.getElementById('jAge').value = '';
    document.getElementById('jState').value = '';
    document.getElementById('jWhatsapp').value = '';
    document.getElementById('jEmail').value = '';
    document.getElementById('jConsent').checked = false;
  }

  function adminLogin() {
    const pass = document.getElementById('adminPass').value;
    const msg = document.getElementById('loginMsg');
    if (pass === ADMIN_PASSWORD) {
      document.getElementById('adminLogin').style.display = 'none';
      document.getElementById('adminPanel').style.display = 'block';
      renderList();
    } else {
      msg.className = 'msg error';
      msg.textContent = '❌ Galat password';
    }
  }

  function logout() {
    document.getElementById('adminLogin').style.display = 'block';
    document.getElementById('adminPanel').style.display = 'none';
    document.getElementById('adminPass').value = '';
    document.getElementById('loginMsg').className = 'msg';
  }

  function renderList() {
    const query = (document.getElementById('adminSearch')?.value || '').toLowerCase();
    const people = getPeople();
    const filtered = people.filter(p =>
      p.name.toLowerCase().includes(query) ||
      p.state.toLowerCase().includes(query)
    );

    document.getElementById('stats').textContent = `Total: ${people.length} Joiners`;

    const list = document.getElementById('peopleList');
    if (filtered.length === 0) {
      list.innerHTML = '<p class="empty">Koi joiner nahi mila</p>';
      return;
    }

    list.innerHTML = filtered.map(p => `
      <div class="person-card">
        <button class="delete-btn" onclick="deletePerson(${p.id})">🗑 Delete</button>
        <h3>👤 ${p.name}</h3>
        <p><strong>Age:</strong> ${p.age}</p>
        <p><strong>State:</strong> ${p.state}</p>
        <p><strong>WhatsApp:</strong> <a href="https://wa.me/${p.whatsapp.replace(/\D/g,'')}" target="_blank">${p.whatsapp}</a></p>
        <p><strong>Email:</strong> ${p.email}</p>
        <p style="font-size:12px;color:#888;margin-top:8px;">📅 ${p.date}</p>
      </div>
    `).join('');
  }

  function deletePerson(id) {
    if (!confirm('Pakka delete karna hai?')) return;
    const people = getPeople().filter(p => p.id !== id);
    savePeople(people);
    renderList();
  }

  function exportCSV() {
    const people = getPeople();
    if (people.length === 0) { alert('Koi data nahi hai'); return; }
    const headers = ['Name', 'Age', 'State', 'WhatsApp', 'Email', 'Date'];
    const rows = people.map(p => [p.name, p.age, p.state, p.whatsapp, p.email, p.date]);
    const csv = [headers, ...rows].map(r => r.map(c => `"${c}"`).join(',')).join('\n');
    const blob = new Blob([csv], { type: 'text/csv' });
    const url = URL.createObjectURL(blob);
    const a = document.createElement('a');
    a.href = url;
    a.download = 'joiners.csv';
    a.click();
  }

  document.getElementById('adminSearch')?.addEventListener('keypress', e => {
    if (e.key === 'Enter') renderList();
  });
</script>
</body>
</html>
