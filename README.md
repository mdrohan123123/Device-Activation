    }

    :root {
      --primary: #667eea;
      --primary-dark: #5a67d8;
      --primary-light: #e6e9ff;
      --secondary: #764ba2;
      --secondary-dark: #6b46a0;
      --success: #10b981;
      --success-dark: #059669;
      --danger: #ef4444;
      --danger-dark: #dc2626;
      --warning: #f59e0b;
      --warning-dark: #d97706;
      --info: #3b82f6;
      --info-dark: #2563eb;
      --dark: #1f2937;
      --darker: #111827;
      --light: #f9fafb;
      --lighter: #ffffff;
      --gray-100: #f3f4f6;
      --gray-200: #e5e7eb;
      --gray-300: #d1d5db;
      --gray-400: #9ca3af;
      --gray-500: #6b7280;
      --gray-600: #4b5563;
      --gray-700: #374151;
      --gray-800: #1f2937;
      --gray-900: #111827;
      --gradient-1: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
      --gradient-2: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
      --gradient-3: linear-gradient(135deg, #4facfe 0%, #00f2fe 100%);
      --gradient-4: linear-gradient(135deg, #43e97b 0%, #38f9d7 100%);
      --shadow-sm: 0 2px 4px rgba(0,0,0,0.05);
      --shadow-md: 0 4px 6px rgba(0,0,0,0.07);
      --shadow-lg: 0 10px 15px rgba(0,0,0,0.1);
      --shadow-xl: 0 20px 25px rgba(0,0,0,0.15);
      --shadow-2xl: 0 25px 50px rgba(0,0,0,0.25);
    }

    body {
      font-family: 'Inter', sans-serif;
      background: #f4f7fc;
      min-height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      padding: 20px;
    }

    /* Glassmorphism Effect */
    .glass {
      background: rgba(255, 255, 255, 0.95);
      backdrop-filter: blur(10px);
      border: 1px solid rgba(255, 255, 255, 0.2);
    }

    .glass-dark {
      background: rgba(17, 24, 39, 0.95);
      backdrop-filter: blur(10px);
      border: 1px solid rgba(255, 255, 255, 0.1);
    }

    /* Animations */
    @keyframes slideIn {
      from {
        opacity: 0;
        transform: translateY(20px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    @keyframes pulse {
      0%, 100% {
        transform: scale(1);
      }
      50% {
        transform: scale(1.05);
      }
    }

    @keyframes shimmer {
      0% {
        background-position: -1000px 0;
      }
      100% {
        background-position: 1000px 0;
      }
    }

    .animate-slide-in {
      animation: slideIn 0.5s ease forwards;
    }

    .animate-pulse-slow {
      animation: pulse 3s infinite;
    }

    /* Premium Container */
    .premium-container {
      max-width: 800px;
      width: 100%;
      margin: 0 auto;
    }

    /* Premium Header */
    .premium-header {
      background: var(--gradient-1);
      border-radius: 30px;
      padding: 25px 30px;
      margin-bottom: 30px;
      box-shadow: var(--shadow-2xl);
      display: flex;
      justify-content: space-between;
      align-items: center;
      flex-wrap: wrap;
      gap: 20px;
      position: relative;
      overflow: hidden;
    }

    .premium-header::before {
      content: '';
      position: absolute;
      top: -50%;
      left: -50%;
      width: 200%;
      height: 200%;
      background: radial-gradient(circle, rgba(255,255,255,0.1) 0%, transparent 70%);
      animation: shimmer 10s infinite linear;
    }

    .logo-area {
      display: flex;
      align-items: center;
      gap: 20px;
      position: relative;
      z-index: 1;
    }

    .logo-icon {
      width: 60px;
      height: 60px;
      background: rgba(255,255,255,0.2);
      border-radius: 20px;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 30px;
      color: white;
      border: 2px solid rgba(255,255,255,0.3);
      backdrop-filter: blur(5px);
    }

    .logo-text h1 {
      font-size: 24px;
      font-weight: 800;
      color: white;
      margin-bottom: 5px;
      text-shadow: 2px 2px 4px rgba(0,0,0,0.2);
    }

    .logo-text span {
      color: rgba(255,255,255,0.8);
      font-size: 13px;
      font-weight: 500;
    }

    .header-badge {
      background: rgba(255,255,255,0.2);
      backdrop-filter: blur(10px);
      padding: 10px 25px;
      border-radius: 50px;
      color: white;
      font-weight: 600;
      font-size: 14px;
      border: 2px solid rgba(255,255,255,0.3);
      position: relative;
      z-index: 1;
    }

    /* Main Card */
    .premium-card {
      background: white;
      border-radius: 30px;
      padding: 35px;
      box-shadow: var(--shadow-xl);
      transition: all 0.3s ease;
      margin-bottom: 25px;
      border-left: 5px solid var(--primary);
    }

    .premium-card:hover {
      box-shadow: var(--shadow-2xl);
    }

    .card-header {
      display: flex;
      align-items: center;
      gap: 15px;
      margin-bottom: 30px;
      padding-bottom: 15px;
      border-bottom: 2px solid var(--gray-100);
    }

    .card-header i {
      width: 50px;
      height: 50px;
      background: var(--gradient-1);
      border-radius: 15px;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 24px;
      color: white;
    }

    .card-header h3 {
      font-size: 22px;
      font-weight: 700;
      color: var(--gray-800);
    }

    .card-header p {
      color: var(--gray-500);
      font-size: 14px;
      margin-top: 3px;
    }

    /* Input Group Premium */
    .input-group-premium {
      margin-bottom: 25px;
    }

    .input-group-premium label {
      display: block;
      font-size: 15px;
      font-weight: 600;
      color: var(--gray-700);
      margin-bottom: 10px;
      letter-spacing: 0.3px;
    }

    .input-group-premium input,
    .input-group-premium textarea {
      width: 100%;
      padding: 18px 22px;
      border: 2px solid var(--gray-200);
      border-radius: 20px;
      font-size: 16px;
      transition: all 0.3s;
      background: var(--gray-100);
      font-family: 'Inter', sans-serif;
    }

    .input-group-premium input:focus,
    .input-group-premium textarea:focus {
      border-color: var(--primary);
      outline: none;
      background: white;
      box-shadow: 0 0 0 4px var(--primary-light);
    }

    .input-group-premium textarea {
      resize: vertical;
      min-height: 150px;
    }

    .input-hint {
      margin-top: 8px;
      font-size: 13px;
      color: var(--gray-500);
      display: flex;
      align-items: center;
      gap: 5px;
    }

    .input-hint i {
      color: var(--primary);
      font-size: 14px;
    }

    /* API Key row - now with mode selector */
    .api-key-row {
      display: flex;
      gap: 10px;
      align-items: center;
      margin-bottom: 20px;
      flex-wrap: wrap;
    }

    .api-key-row input {
      flex: 2;
      min-width: 200px;
      padding: 15px 20px;
      border: 2px solid var(--gray-200);
      border-radius: 20px;
      font-size: 14px;
      background: var(--gray-100);
    }

    .api-key-row select {
      flex: 1;
      min-width: 150px;
      padding: 15px 20px;
      border: 2px solid var(--gray-200);
      border-radius: 20px;
      font-size: 14px;
      background: var(--gray-100);
      font-weight: 500;
      color: var(--gray-700);
      cursor: pointer;
    }

    .api-key-row button {
      padding: 15px 25px;
      border: none;
      border-radius: 20px;
      background: var(--info);
      color: white;
      font-weight: 600;
      cursor: pointer;
      transition: 0.3s;
    }

    .api-key-row button:hover {
      background: var(--info-dark);
    }

    /* Premium Button */
    .premium-btn {
      width: 100%;
      padding: 18px;
      border: none;
      border-radius: 20px;
      background: var(--gradient-1);
      color: white;
      font-weight: 700;
      font-size: 18px;
      cursor: pointer;
      transition: all 0.3s;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 12px;
      box-shadow: 0 10px 20px rgba(102, 126, 234, 0.3);
    }

    .premium-btn:hover:not(:disabled) {
      transform: translateY(-3px);
      box-shadow: 0 15px 30px rgba(102, 126, 234, 0.5);
    }

    .premium-btn:disabled {
      opacity: 0.6;
      cursor: not-allowed;
    }

    .premium-btn i {
      font-size: 20px;
    }

    /* Progress Bar */
    .progress-container {
      margin-top: 20px;
      background: var(--gray-200);
      border-radius: 30px;
      height: 10px;
      overflow: hidden;
    }

    .progress-bar {
      height: 100%;
      background: var(--gradient-1);
      width: 0%;
      transition: width 0.3s;
    }

    .status-text {
      margin-top: 15px;
      font-size: 14px;
      color: var(--gray-600);
      display: flex;
      align-items: center;
      gap: 8px;
    }

    /* Info Cards */
    .info-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 20px;
      margin-top: 30px;
    }

    .info-card {
      background: var(--gray-100);
      border-radius: 20px;
      padding: 20px;
      display: flex;
      align-items: center;
      gap: 15px;
      transition: all 0.3s;
    }

    .info-card:hover {
      background: white;
      box-shadow: var(--shadow-md);
    }

    .info-icon {
      width: 45px;
      height: 45px;
      background: white;
      border-radius: 15px;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 20px;
      color: var(--primary);
    }

    .info-content h4 {
      font-size: 16px;
      font-weight: 700;
      color: var(--gray-800);
      margin-bottom: 5px;
    }

    .info-content p {
      font-size: 13px;
      color: var(--gray-600);
    }

    /* Sample Link */
    .sample-link {
      background: var(--primary-light);
      border-radius: 15px;
      padding: 15px 20px;
      margin-top: 20px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      flex-wrap: wrap;
      gap: 10px;
      color: var(--primary-dark);
      font-size: 14px;
      border: 1px dashed var(--primary);
    }

    .sample-link i {
      font-size: 16px;
      cursor: pointer;
      transition: 0.3s;
    }

    .sample-link i:hover {
      color: var(--primary-dark);
      transform: scale(1.1);
    }

    /* Error message */
    .error-message {
      background: #fee2e2;
      color: #b91c1c;
      padding: 15px 20px;
      border-radius: 20px;
      margin-top: 20px;
      display: flex;
      align-items: center;
      gap: 10px;
      border-left: 4px solid #ef4444;
    }

    /* Responsive */
    @media (max-width: 600px) {
      .premium-header {
        flex-direction: column;
        text-align: center;
        padding: 20px;
      }
      .logo-area {
        flex-direction: column;
      }
      .card-header {
        flex-direction: column;
        text-align: center;
      }
      .premium-card {
        padding: 25px;
      }
      .api-key-row {
        flex-direction: column;
      }
      .api-key-row input,
      .api-key-row select,
      .api-key-row button {
        width: 100%;
      }
    }
  </style>
</head>
<body>
  <div class="premium-container">
    <!-- Premium Header -->
    <div class="premium-header">
      <div class="logo-area">
        <div class="logo-icon">
          <i class="fas fa-layer-group"></i>
        </div>
        <div class="logo-text">
          <h1>ROG DRIVE SHEET MERGER</h1>
          <span><i class="fas fa-google-drive"></i> Google Drive লিংক থেকে শিট মার্জ</span>
        </div>
      </div>
      <div class="header-badge">
        <i class="fas fa-bolt"></i> DRIVE SUPPORT
      </div>
    </div>

    <!-- Main Card -->
    <div class="premium-card animate-slide-in">
      <div class="card-header">
        <i class="fas fa-drive"></i>
        <div>
          <h3>Google Drive শিটের লিঙ্কসমূহ</h3>
          <p>Drive-এ শেয়ার করা Google Sheets-এর লিঙ্ক দিন (প্রতি লাইনে একটি)</p>
        </div>
      </div>

      <!-- API Key Row with Mode Selector -->
      <div class="api-key-row">
        <input type="text" id="apiKey" placeholder="Google API Key (ঐচ্ছিক)" value="">
        <select id="modeSelect">
          <option value="auto" selected>🔄 অটো (API না থাকলে CSV)</option>
          <option value="api">🔑 শুধু API পদ্ধতি</option>
          <option value="csv">📥 শুধু CSV পদ্ধতি</option>
        </select>
        <button id="saveApiKey" title="API কী সংরক্ষণ"><i class="fas fa-save"></i></button>
      </div>

      <!-- Links Textarea -->
      <div class="input-group-premium">
        <label><i class="fas fa-list-ul" style="margin-right: 8px;"></i> Drive / Sheets লিঙ্ক (প্রতি লাইনে একটি)</label>
        <textarea id="sheetLinks" placeholder="যেমন:&#10;https://docs.google.com/spreadsheets/d/1ABCxyz/edit?usp=sharing&#10;https://drive.google.com/file/d/1DEFuvw/view?usp=sharing&#10;https://docs.google.com/spreadsheets/d/2GHIpqr/edit#gid=12345" rows="5"></textarea>
        <div class="input-hint">
          <i class="fas fa-info-circle"></i>
          <span>Drive লিঙ্ক বা সরাসরি Sheets লিঙ্ক দুটোই কাজ করবে। ফাইলটি "Anyone with link can view" মোডে শেয়ার করা থাকতে হবে।</span>
        </div>
      </div>

      <!-- Convert Button -->
      <button class="premium-btn" id="convertBtn">
        <i class="fas fa-blender-phone"></i> একত্রিত করে এক্সেল ডাউনলোড
      </button>

      <!-- Progress -->
      <div class="progress-container" id="progressContainer" style="display: none;">
        <div class="progress-bar" id="progressBar"></div>
      </div>
      <div class="status-text" id="statusMessage">
        <i class="fas fa-spinner fa-spin" style="display: none;" id="spinner"></i>
        <span id="statusText">প্রস্তুত</span>
      </div>

      <!-- Error Display -->
      <div id="errorMessage" class="error-message" style="display: none;">
        <i class="fas fa-exclamation-circle"></i>
        <span id="errorText"></span>
      </div>

      <!-- Sample Link -->
      <div class="sample-link">
        <div style="display: flex; align-items: center; gap: 8px;">
          <i class="fas fa-lightbulb" style="color: #f59e0b;"></i>
          <span>নমুনা Drive লিঙ্ক: <span id="sampleLinkText" style="font-weight: 600;">https://drive.google.com/file/d/1a2b3c4d5e/view</span></span>
        </div>
        <i class="fas fa-copy" id="copySample" title="কপি করুন"></i>
      </div>

      <!-- Info Cards -->
      <div class="info-grid">
        <div class="info-card">
          <div class="info-icon">
            <i class="fas fa-infinity"></i>
          </div>
          <div class="info-content">
            <h4>অসীম লিঙ্ক</h4>
            <p>যত খুশি Drive/Sheets লিঙ্ক</p>
          </div>
        </div>
        <div class="info-card">
          <div class="info-icon">
            <i class="fas fa-check-circle"></i>
          </div>
          <div class="info-content">
            <h4>অটো ডিটেক্ট</h4>
            <p>Drive বা Sheets লিঙ্ক চিনবে</p>
          </div>
        </div>
        <div class="info-card">
          <div class="info-icon">
            <i class="fas fa-file-excel"></i>
          </div>
          <div class="info-content">
            <h4>এক্সেল ফাইল</h4>
            <p>একটি শিটে সব তথ্য</p>
          </div>
        </div>
      </div>
    </div>

    <!-- Footer Note -->
    <div style="text-align: center; color: var(--gray-500); font-size: 13px; margin-top: 20px;">
      <i class="fas fa-crown" style="color: #fbbf24;"></i> ROG FB TEAM - প্রিমিয়াম টুলস (Drive Support)
    </div>
  </div>

  <script>
    (function() {
      // DOM elements
      const apiKeyInput = document.getElementById('apiKey');
      const saveApiKeyBtn = document.getElementById('saveApiKey');
      const modeSelect = document.getElementById('modeSelect');
      const sheetLinksArea = document.getElementById('sheetLinks');
      const convertBtn = document.getElementById('convertBtn');
      const progressContainer = document.getElementById('progressContainer');
      const progressBar = document.getElementById('progressBar');
      const spinner = document.getElementById('spinner');
      const statusTextEl = document.getElementById('statusText');
      const errorMessageDiv = document.getElementById('errorMessage');
      const errorText = document.getElementById('errorText');
      const copySample = document.getElementById('copySample');
      const sampleLinkText = document.getElementById('sampleLinkText').innerText;

      // Sample link copy
      copySample.addEventListener('click', function() {
        navigator.clipboard.writeText(sampleLinkText).then(() => {
          const original = copySample.className;
          copySample.className = 'fas fa-check';
          setTimeout(() => copySample.className = original, 1500);
        }).catch(() => alert('কপি করতে সমস্যা'));
      });

      // Save API Key to localStorage
      const savedKey = localStorage.getItem('google_api_key');
      if (savedKey) apiKeyInput.value = savedKey;

      saveApiKeyBtn.addEventListener('click', function() {
        const key = apiKeyInput.value.trim();
        if (key) {
          localStorage.setItem('google_api_key', key);
          showStatus('API কী সংরক্ষিত ✅', false);
        } else {
          showStatus('কী খালি রাখা যাবে না', false);
        }
      });

      // Helper to show status
      function showStatus(msg, showSpinner = false) {
        statusTextEl.innerText = msg;
        spinner.style.display = showSpinner ? 'inline-block' : 'none';
      }

      function showError(msg) {
        errorText.innerText = msg;
        errorMessageDiv.style.display = 'flex';
        setTimeout(() => errorMessageDiv.style.display = 'none', 5000);
      }

      // Extract sheet ID from various Google URL formats (Sheets or Drive)
      function extractSpreadsheetId(url) {
        // Try Sheets URL format: /d/{id}/
        let match = url.match(/\/d\/([a-zA-Z0-9_-]+)/);
        if (match) return match[1];
        
        // Try Drive file URL: /file/d/{id}/
        match = url.match(/\/file\/d\/([a-zA-Z0-9_-]+)/);
        if (match) return match[1];
        
        // Try open?id={id} format
        match = url.match(/[?&]id=([a-zA-Z0-9_-]+)/);
        if (match) return match[1];
        
        return null;
      }

      // Extract gid from URL
      function extractGid(url) {
        const gidMatch = url.match(/[#&]gid=(\d+)/);
        return gidMatch ? parseInt(gidMatch[1], 10) : null;
      }

      // --- API methods (require API key) ---
      async function getSheetName(spreadsheetId, targetGid, apiKey) {
        const url = `https://sheets.googleapis.com/v4/spreadsheets/${spreadsheetId}?fields=sheets.properties&key=${apiKey}`;
        const resp = await fetch(url);
        if (!resp.ok) {
          const err = await resp.json();
          throw new Error(err.error?.message || 'API ত্রুটি');
        }
        const data = await resp.json();
        const sheets = data.sheets;
        if (!sheets || sheets.length === 0) throw new Error('শিট পাওয়া যায়নি');
        if (targetGid !== null) {
          const sheet = sheets.find(s => s.properties.sheetId === targetGid);
          if (!sheet) throw new Error(`GID ${targetGid} সম্বলিত শিট খুঁজে পাওয়া যায়নি`);
          return sheet.properties.title;
        } else {
          // প্রথম শিটের নাম
          return sheets[0].properties.title;
        }
      }

      async function fetchSheetDataViaApi(spreadsheetId, sheetName, apiKey) {
        const range = encodeURIComponent(sheetName);
        const url = `https://sheets.googleapis.com/v4/spreadsheets/${spreadsheetId}/values/${range}?key=${apiKey}`;
        const resp = await fetch(url);
        if (!resp.ok) {
          const err = await resp.json();
          throw new Error(err.error?.message || 'ডেটা আনতে ব্যর্থ');
        }
        const data = await resp.json();
        return data.values || []; // array of arrays
      }

      // --- CSV export method (no API key, uses public proxy) ---
      async function fetchSheetDataViaCsv(spreadsheetId, gid) {
        // gid null হলে 0 (প্রথম শিট) ধরি
        const sheetGid = (gid !== null && gid !== undefined) ? gid : 0;
        const csvUrl = `https://docs.google.com/spreadsheets/d/${spreadsheetId}/export?format=csv&gid=${sheetGid}`;
        // CORS-এড়াতে পাবলিক প্রক্সি ব্যবহার (corsproxy.io)
        const proxyUrl = `https://corsproxy.io/?${encodeURIComponent(csvUrl)}`;
        
        const resp = await fetch(proxyUrl);
        if (!resp.ok) {
          throw new Error(`CSV ডেটা আনতে ব্যর্থ (HTTP ${resp.status})`);
        }
        const csvText = await resp.text();
        // CSV কে অ্যারে অফ অ্যারেতে কনভার্ট করতে XLSX ব্যবহার করি
        const workbook = XLSX.read(csvText, { type: 'string' });
        const firstSheet = workbook.Sheets[workbook.SheetNames[0]];
        // { header: 1 } দিলে অ্যারে অফ অ্যারে পাওয়া যায়
        const data = XLSX.utils.sheet_to_json(firstSheet, { header: 1 });
        return data; // data হলো অ্যারে অফ অ্যারে
      }

      // Main conversion
      convertBtn.addEventListener('click', async function() {
        // Reset UI
        errorMessageDiv.style.display = 'none';
        progressContainer.style.display = 'block';
        progressBar.style.width = '0%';
        showStatus('প্রক্রিয়াকরণ শুরু...', true);
        convertBtn.disabled = true;

        const apiKey = apiKeyInput.value.trim(); // may be empty
        const mode = modeSelect.value;
        const linksText = sheetLinksArea.value.trim();
        
        if (!linksText) {
          showError('কমপক্ষে একটি লিঙ্ক দিন');
          showStatus('লিঙ্ক দিন', false);
          convertBtn.disabled = false;
          progressContainer.style.display = 'none';
          return;
        }

        const links = linksText.split(/\r?\n/).map(l => l.trim()).filter(l => l !== '');
        if (links.length === 0) {
          showError('কোনো বৈধ লিঙ্ক নেই');
          showStatus('লিঙ্ক দিন', false);
          convertBtn.disabled = false;
          progressContainer.style.display = 'none';
          return;
        }

        const combinedData = []; // array of rows

        for (let i = 0; i < links.length; i++) {
          const link = links[i];
          showStatus(`প্রক্রিয়াধীন: লিঙ্ক ${i+1}/${links.length}`, true);
          progressBar.style.width = `${(i / links.length) * 100}%`;

          try {
            const spreadsheetId = extractSpreadsheetId(link);
            if (!spreadsheetId) {
              throw new Error(`লিঙ্ক ${i+1} থেকে স্প্রেডশিট আইডি পাওয়া যায়নি`);
            }
            
            const gid = extractGid(link);

            let values;
            const useApi = (mode === 'api' || (mode === 'auto' && apiKey));
            const useCsv = (mode === 'csv' || (mode === 'auto' && !apiKey));

            if (useApi) {
              // API পদ্ধতি
              if (!apiKey) throw new Error('API পদ্ধতির জন্য API কী প্রয়োজন');
              const sheetName = await getSheetName(spreadsheetId, gid, apiKey);
              values = await fetchSheetDataViaApi(spreadsheetId, sheetName, apiKey);
            } else if (useCsv) {
              // CSV পদ্ধতি (CORS প্রক্সি সহ)
              values = await fetchSheetDataViaCsv(spreadsheetId, gid);
            } else {
              throw new Error('কোনো পদ্ধতি নির্বাচন করা হয়নি');
            }

            if (values && values.length > 0) {
              // প্রথম লিঙ্কের জন্য সব ডাটা, পরবর্তী লিঙ্কের জন্য প্রথম সারি বাদ দিতে চাইলে
              // নিচের if কন্ডিশনটি ব্যবহার করতে পারেন
              if (i === 0) {
                combinedData.push(...values);
              } else {
                // দ্বিতীয় লিঙ্ক থেকে প্রথম সারি (হেডার) বাদ দিয়ে ডাটা যোগ করুন
                if (values.length > 1) {
                  combinedData.push(...values.slice(1));
                } else {
                  console.log(`লিঙ্ক ${i+1} এ ডাটা নেই`);
                }
              }
            } else {
              console.log(`শিট ${i+1} খালি`);
            }
          } catch (err) {
            showError(`লিঙ্ক ${i+1} ত্রুটি: ${err.message}`);
            showStatus('ত্রুটি ঘটেছে', false);
            convertBtn.disabled = false;
            progressContainer.style.display = 'none';
            return;
          }
        }

        progressBar.style.width = '100%';
        showStatus('এক্সেল তৈরি হচ্ছে...', true);

        if (combinedData.length === 0) {
          showError('কোনো ডাটা পাওয়া যায়নি');
          showStatus('কোনো ডাটা নেই', false);
          convertBtn.disabled = false;
          progressContainer.style.display = 'none';
          return;
        }

        // Create Excel workbook
        const wb = XLSX.utils.book_new();
        const ws = XLSX.utils.aoa_to_sheet(combinedData);
        XLSX.utils.book_append_sheet(wb, ws, 'Combined Data');
        // Generate Excel file and trigger download
        const fileName = `merged_${new Date().toISOString().slice(0,10)}.xlsx`;
        XLSX.writeFile(wb, fileName);

        showStatus('সম্পন্ন! ফাইল ডাউনলোড হচ্ছে ✅', false);
        convertBtn.disabled = false;
        progressContainer.style.display = 'none';
      });

    })();
  </script>
</body>
</html>
