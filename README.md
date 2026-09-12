<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
<meta name="theme-color" content="#667eea">
<meta name="mobile-web-app-capable" content="yes">
<meta name="apple-mobile-web-app-capable" content="yes">
<title>Join SITANSHU Team</title>
<style>
  * { margin: 0; padding: 0; box-sizing: border-box; font-family: -apple-system, 'Segoe UI', Roboto, sans-serif; -webkit-tap-highlight-color: transparent; }
  html, body { height: 100%; overflow-x: hidden; }
  body {
    background: linear-gradient(135deg, #667eea, #764ba2);
    display: flex; justify-content: center; align-items: center;
    font-size: 15px;
  }

  .app {
    width: 100%;
    max-width: 430px;
    height: 100vh;
    max-height: 880px;
    background: #f5f7fb;
    display: flex;
    flex-direction: column;
    overflow: hidden;
    position: relative;
  }
  @media (min-width: 480px) {
    .app { border-radius: 28px; box-shadow: 0 30px 80px rgba(0,0,0,0.4); }
  }

  .appbar {
    background: linear-gradient(135deg, #667eea, #764ba2);
    color: white;
    padding: 18px 20px;
    display: flex; align-items: center; gap: 12px;
    box-shadow: 0 2px 10px rgba(0,0,0,0.1);
    z-index: 10;
  }
  .appbar .logo {
    width: 40px; height: 40px;
    background: rgba(255,255,255,0.2);
    border-radius: 12px;
    display: flex; align-items: center; justify-content: center;
    font-size: 22px;
  }
  .appbar h1 { font-size: 18px; font-weight: 600; }
  .appbar p { font-size: 12px; opacity: 0.9; margin-top: 2px; }

  .content {
    flex: 1;
    overflow-y: auto;
    padding: 20px 18px 100px;
    -webkit-overflow-scrolling: touch;
  }

  .card {
    background: white;
    border-radius: 18px;
    padding: 24px 22px;
    box-shadow: 0 2px 12px rgba(0,0,0,0.06);
    margin-bottom: 18px;
  }

  .card h2 { color: #333; margin-bottom: 20px; font-size: 17px; font-weight: 600; }

  label {
    display: block;
    color: #444;
    margin-bottom: 8px;
    font-size: 14px;
    font-weight: 600;
  }

  input, select {
    width: 100%;
    padding: 14px 16px;
    border: 1.5px solid #e0e0e0;
    border-radius: 12px;
    font-size: 15px;
    margin-bottom: 18px;
    outline: none;
    transition: 0.2s;
    background: #fafbff;
    -webkit-appearance: none;
    appearance: none;
  }
  input:focus, select:focus {
    border-color: #667eea;
    background: white;
    box-shadow: 0 0 0 3px rgba(102,126,234,0.1);
  }
  select {
    background-image: url("data:image/svg+xml;charset=UTF-8,%3csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 24 24' fill='none' stroke='%23667eea' stroke-width='2'%3e%3cpolyline points='6 9 12 15 18 9'/%3e%3c/svg%3e");
    background-repeat: no-repeat;
    background-position: right 14px center;
    background-size: 18px;
    padding-right: 42px;
  }

  .row { display: grid; grid-template-columns: 1fr 1fr; gap: 14px; }

  .consent-box {
    background: #fff8e1;
    border-left: 5px solid #ffc107;
    padding: 18px 18px;
    border-radius: 14px;
    margin-bottom: 22px;
    margin-top: 4px;
  }
  .consent-box label {
    display: flex;
    align-items: flex-start;
    gap: 12px;
    color: #4a4a4a;
    font-weight: 500;
    cursor: pointer;
    font-size: 14px;
    line-height: 1.6;
    margin: 0;
  }
  .consent-box input[type="checkbox"] {
    width: 22px;
    height: 22px;
    margin: 2px 0 0 0;
    cursor: pointer;
    accent-color: #ff9800;
    flex-shrink: 0;
  }

  .btn {
    width: 100%;
    padding: 16px;
    background: linear-gradient(135deg, #667eea, #764ba2);
    color: white;
    border: none;
    border-radius: 12px;
    font-size: 16px;
    font-weight: 600;
    cursor: pointer;
    transition: 0.2s;
    box-shadow: 0 4px 14px rgba(102,126,234,0.35);
  }
  .btn:active { transform: scale(0.98); }
  .btn-danger { background: #e74c3c; box-shadow: 0 4px 12px rgba(231,76,60,0.3); }
  .btn-success { background: #28a745; box-shadow: 0 4px 12px rgba(40,167,69,0.3); }
  .btn-small { padding: 10px 14px; font-size: 13.5px; width: auto; }

  .search-box { display: flex; gap: 10px; margin-bottom: 16px; }
  .search-box input { margin-bottom: 0; flex: 1; }
  .search-box button {
    padding: 0 20px;
    background: #667eea;
    color: white;
    border: none;
    border-radius: 12px;
    cursor: pointer;
    font-weight: 600;
    font-size: 14px;
  }

  .person-card {
    background: #f8f9ff;
    border-left: 4px solid #667eea;
    padding: 16px;
    border-radius: 12px;
    margin-bottom: 12px;
    position: relative;
    animation: fadeIn 0.3s;
  }
  .person-card h3 { color: #333; margin-bottom: 10px; font-size: 16px; padding-right: 55px; }
  .person-card p { color: #555; font-size: 13.5px; margin: 6px 0; line-height: 1.5; }
  .person-card p strong { color: #333; }
  .person-card a { color: #667eea; text-decoration: none; font-weight: 500; }
  .delete-btn {
    position: absolute; top: 12px; right: 12px;
    background: #ffe5e5; color: #e74c3c;
    border: none; padding: 6px 12px;
    border-radius: 8px; cursor: pointer;
    font-size: 12px; font-weight: 600;
  }

  .msg {
    padding: 14px;
    border-radius: 12px;
    margin-top: 16px;
    font-size: 14px;
    display: none;
    text-align: center;
    font-weight: 600;
    line-height: 1.5;
  }
  .msg.success { background: #d4edda; color: #155724; display: block; }
  .msg.error { background: #f8d7da; color: #721c24; display: block; }

  .empty { text-align: center; color: #999; padding: 40px 20px; font-size: 14px; }
  .stats {
    background: linear-gradient(135deg, #667eea, #764ba2);
    color: white; padding: 18px;
    border-radius: 14px; margin-bottom: 16px;
    text-align: center; font-weight: 600; font-size: 15px;
  }

  .section { display: none; }
  .section.active { display: block; animation: fadeIn 0.3s; }
  @keyframes fadeIn { from { opacity: 0; transform: translateY(8px); } to { opacity: 1; transform: translateY(0); } }

  .bottom-nav {
    position: absolute; bottom: 0; left: 0; right: 0;
    background: white;
    display: flex;
    box-shadow: 0 -2px 12px rgba(0,0,0,0.08);
    border-top: 1px solid #eee;
    padding-bottom: env(safe-area-inset-bottom);
  }
  .nav-item {
    flex: 1;
    padding: 12px 0 14px;
    background: none; border: none;
    display: flex; flex-direction: column;
    align-items: center; gap: 4px;
    cursor: pointer; color: #999;
    font-size: 11.5px; font-weight: 600;
    transition: 0.2s;
  }
  .nav-item .icon { font-size: 22px; }
  .nav-item.active { color: #667eea; }
  .nav-item.active .icon { transform: scale(1.1); }

  .pass-wrapper { position: relative; }
  .pass-wrapper input { padding-right: 48px; }
  .eye-btn {
    position: absolute; right: 14px; top: 50%;
    transform: translateY(-50%);
    background: none; border: none;
    cursor: pointer; font-size: 20px;
    color: #999; padding: 4px;
    margin-top: -9px;
  }
</style>
</head>
<body>
  <div class="app">
    <div class="appbar">
      <div class="logo">🚀</div>
      <div>
        <h1>Join Our Team</h1>
        <p>Fill the form & we'll connect</p>
      </div>
    </div>

    <div class="content">
      <!-- JOIN -->
      <div class="section active" id="joinSection">
        <div class="card">
          <h2>📝 Apni details bharein</h2>

          <label>Full Name *</label>
          <input type="text" id="jName" placeholder="Aapka pura naam" autocomplete="name">

          <div class="row">
            <div>
              <label>Age *</label>
              <input type="number" id="jAge" placeholder="Age" min="15" max="100" inputmode="numeric">
            </div>
            <div>
              <label>State *</label>
              <select id="jState">
                <option value="">Select</option>
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
          <input type="tel" id="jWhatsapp" placeholder="+91 XXXXX XXXXX" inputmode="tel" autocomplete="tel">

          <label>Email *</label>
          <input type="email" id="jEmail" placeholder="aapka@email.com" inputmode="email" autocomplete="email">

          <div class="consent-box">
            <label>
              <input type="checkbox" id="jConsent">
              <span>Main <strong>consent deta/deti hoon</strong> ki meri ye information team join karne ke liye use ki jaye. Meri info safe rahegi aur kisi ke saath share nahi hogi.</span>
            </label>
          </div>

          <button class="btn" onclick="submitJoin()">✓ Join Karein</button>
          <div class="msg" id="joinMsg"></div>
        </div>
      </div>

      <!-- ADMIN -->
      <div class="section" id="adminSection">
        <div id="adminLogin">
          <div class="card">
            <h2>🔐 Admin Login</h2>
            <label>Password</label>
            <div class="pass-wrapper">
              <input type="password" id="adminPass" placeholder="Password daalein" autocomplete="off">
              <button class="eye-btn" onclick="toggleEye()" id="eyeIcon">👁️</button>
            </div>
            <button class="btn" onclick="adminLogin()">Login</button>
            <div class="msg" id="loginMsg"></div>
          </div>
        </div>

        <div id="adminPanel" style="display:none;">
          <div class="stats" id="stats">Total: 0 Joiners</div>

          <div class="search-box">
            <input type="text" id="adminSearch" placeholder="🔍 Naam ya state...">
            <button onclick="renderList()">Go</button>
          </div>

          <div style="display:flex;gap:10px;margin-bottom:16px;">
            <button class="btn btn-success btn-small" style="flex:1;" onclick="exportCSV()">📥 CSV</button>
            <button class="btn btn-danger btn-small" style="flex:1;" onclick="logout()">🚪 Logout</button>
          </div>

          <div id="peopleList"></div>
        </div>
      </div>
    </div>

    <div class="bottom-nav">
      <button class="nav-item active" id="navJoin" onclick="showTab('join')">
        <span class="icon">📝</span>
        <span>Join</span>
      </button>
      <button class="nav-item" id="navAdmin" onclick="showTab('admin')">
        <span class="icon">🔐</span>
        <span>Admin</span>
      </button>
    </div>
  </div>

<script>
  // ============================================
  // PASSWORD VERIFY — actual password: 766743@sr
  // Char codes: 7=55, 6=54, 6=54, 7=55, 4=52, 3=51, @=64, s=115, r=114
  // ============================================
  function _verify(input) {
    const _p = [55, 54, 54, 55, 52, 51, 64, 115, 114];
    if (input.length !== _p.length) return false;
    for (let i = 0; i < _p.length; i++) {
      if (input.charCodeAt(i) !== _p[i]) return false;
    }
    return true;
  }

  function getPeople() {
    try { return JSON.parse(localStorage.getItem('joiners_secure') || '[]'); }
    catch { return []; }
  }
  function savePeople(p) {
    localStorage.setItem('joiners_secure', JSON.stringify(p));
  }

  function showTab(name) {
    document.querySelectorAll('.section').forEach(s => s.classList.remove('active'));
    document.querySelectorAll('.nav-item').forEach(n => n.classList.remove('active'));
    if (name === 'join') {
      document.getElementById('joinSection').classList.add('active');
      document.getElementById('navJoin').classList.add('active');
    } else {
      document.getElementById('adminSection').classList.add('active');
      document.getElementById('navAdmin').classList.add('active');
    }
    document.querySelector('.content').scrollTop = 0;
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
    if (!/^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(email)) {
      msg.className = 'msg error';
      msg.textContent = '❌ Sahi email daalein';
      return;
    }

    const people = getPeople();
    people.push({
      id: Date.now(),
      name, age, state, whatsapp, email,
      date: new Date().toLocaleString('en-IN')
    });
    savePeople(people);

    msg.className = 'msg success';
    msg.textContent = '✅ Thank you! Aapki details mil gayi.';

    ['jName','jAge','jState','jWhatsapp','jEmail'].forEach(id => document.getElementById(id).value = '');
    document.getElementById('jConsent').checked = false;
    setTimeout(() => msg.className = 'msg', 4000);
  }

  function adminLogin() {
    const pass = document.getElementById('adminPass').value;
    const msg = document.getElementById('loginMsg');
    if (_verify(pass)) {
      document.getElementById('adminLogin').style.display = 'none';
      document.getElementById('adminPanel').style.display = 'block';
      document.getElementById('adminPass').value = '';
      msg.className = 'msg';
      renderList();
    } else {
      msg.className = 'msg error';
      msg.textContent = '❌ Galat password';
      document.getElementById('adminPass').value = '';
    }
  }

  function logout() {
    document.getElementById('adminLogin').style.display = 'block';
    document.getElementById('adminPanel').style.display = 'none';
    document.getElementById('adminPass').value = '';
    document.getElementById('loginMsg').className = 'msg';
  }

  function toggleEye() {
    const inp = document.getElementById('adminPass');
    const icon = document.getElementById('eyeIcon');
    if (inp.type === 'password') { inp.type = 'text'; icon.textContent = '🙈'; }
    else { inp.type = 'password'; icon.textContent = '👁️'; }
  }

  function renderList() {
    const query = (document.getElementById('adminSearch')?.value || '').toLowerCase();
    const people = getPeople();
    const filtered = people.filter(p =>
      p.name.toLowerCase().includes(query) ||
      p.state.toLowerCase().includes(query)
    );

    document.getElementById('stats').textContent = `👥 Total: ${people.length} Joiners`;

    const list = document.getElementById('peopleList');
    if (filtered.length === 0) {
      list.innerHTML = '<p class="empty">Koi joiner nahi mila</p>';
      return;
    }

    list.innerHTML = filtered.map(p => `
      <div class="person-card">
        <button class="delete-btn" onclick="deletePerson(${p.id})">🗑</button>
        <h3>👤 ${escapeHtml(p.name)}</h3>
        <p><strong>Age:</strong> ${escapeHtml(p.age)}</p>
        <p><strong>State:</strong> ${escapeHtml(p.state)}</p>
        <p><strong>WhatsApp:</strong> <a href="https://wa.me/${p.whatsapp.replace(/\D/g,'')}" target="_blank">${escapeHtml(p.whatsapp)}</a></p>
        <p><strong>Email:</strong> ${escapeHtml(p.email)}</p>
        <p style="font-size:12px;color:#999;margin-top:8px;">📅 ${p.date}</p>
      </div>
    `).join('');
  }

  function escapeHtml(s) {
    return String(s).replace(/[&<>"']/g, c => ({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[c]));
  }

  function deletePerson(id) {
    if (!confirm('Pakka delete karna hai?')) return;
    savePeople(getPeople().filter(p => p.id !== id));
    renderList();
  }

  function exportCSV() {
    const people = getPeople();
    if (people.length === 0) { alert('Koi data nahi hai'); return; }
    const headers = ['Name', 'Age', 'State', 'WhatsApp', 'Email', 'Date'];
    const rows = people.map(p => [p.name, p.age, p.state, p.whatsapp, p.email, p.date]);
    const csv = [headers, ...rows].map(r => r.map(c => `"${String(c).replace(/"/g,'""')}"`).join(',')).join('\n');
    const blob = new Blob(['\ufeff' + csv], { type: 'text/csv;charset=utf-8' });
    const url = URL.createObjectURL(blob);
    const a = document.createElement('a');
    a.href = url;
    a.download = `joiners_${new Date().toISOString().slice(0,10)}.csv`;
    a.click();
    URL.revokeObjectURL(url);
  }

  document.getElementById('adminSearch')?.addEventListener('keypress', e => {
    if (e.key === 'Enter') renderList();
  });
  document.getElementById('adminPass')?.addEventListener('keypress', e => {
    if (e.key === 'Enter') adminLogin();
  });
</script>
</body>
</html>
