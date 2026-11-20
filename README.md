# SOUR-STORE
 India's Direct Value Superstore
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>SOUR — Indian Online Marketplace &amp; Deals</title>
  <style>
    :root {
      --primary: #0f172a;
      --primary-hover: #1e293b;
      --accent: #ea580c;
      --accent-hover: #c2410c;
      --green: #15803d;
      --green-bg: #dcfce7;
      --red: #dc2626;
      --red-bg: #fee2e2;
      --bg: #f8fafc;
      --surface: #ffffff;
      --border: #e2e8f0;
      --text: #0f172a;
      --muted: #64748b;
      --shadow-sm: 0 1px 2px rgba(0, 0, 0, 0.05);
      --shadow-md: 0 4px 12px rgba(15, 23, 42, 0.08);
      --shadow-lg: 0 12px 28px rgba(15, 23, 42, 0.14);
      --radius: 12px;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Inter, Helvetica, Arial, sans-serif;
    }

    body {
      background-color: var(--bg);
      color: var(--text);
      line-height: 1.5;
    }

    /* Top Announcement Bar */
    .top-bar {
      background: var(--primary);
      color: #f8fafc;
      font-size: 12px;
      padding: 7px 16px;
      text-align: center;
      font-weight: 500;
    }
    .top-bar span {
      color: #fdba74;
      font-weight: 700;
    }

    /* Header / Navbar */
    header {
      background: var(--surface);
      border-bottom: 1px solid var(--border);
      position: sticky;
      top: 0;
      z-index: 40;
      box-shadow: var(--shadow-sm);
    }

    .nav-container {
      max-width: 1280px;
      margin: 0 auto;
      padding: 12px 20px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 16px;
      flex-wrap: wrap;
    }

    .brand {
      display: flex;
      align-items: center;
      gap: 10px;
      text-decoration: none;
      color: var(--primary);
      cursor: pointer;
    }

    .brand-badge {
      background: var(--primary);
      color: #fff;
      font-weight: 900;
      font-size: 20px;
      letter-spacing: -0.5px;
      padding: 4px 10px;
      border-radius: 8px;
    }

    .brand-sub {
      font-size: 11px;
      font-weight: 700;
      color: var(--accent);
      text-transform: uppercase;
      letter-spacing: 0.8px;
      display: block;
    }

    .search-box {
      flex: 1;
      min-width: 240px;
      max-width: 520px;
      position: relative;
    }

    .search-box input {
      width: 100%;
      padding: 10px 14px 10px 38px;
      border: 1.5px solid var(--border);
      border-radius: 10px;
      font-size: 14px;
      background: #f1f5f9;
      transition: all 0.2s;
    }

    .search-box input:focus {
      outline: none;
      background: #fff;
      border-color: var(--primary);
    }

    .search-icon {
      position: absolute;
      left: 12px;
      top: 50%;
      transform: translateY(-50%);
      color: var(--muted);
      pointer-events: none;
    }

    .nav-actions {
      display: flex;
      align-items: center;
      gap: 10px;
    }

    .btn {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 7px;
      padding: 9px 15px;
      border-radius: 9px;
      font-size: 13px;
      font-weight: 600;
      cursor: pointer;
      border: 1px solid transparent;
      transition: all 0.18s;
      position: relative;
      white-space: nowrap;
    }

    .btn-outline {
      background: #fff;
      border-color: var(--border);
      color: var(--text);
    }
    .btn-outline:hover {
      background: #f1f5f9;
    }

    .btn-accent {
      background: var(--accent);
      color: #fff;
    }
    .btn-accent:hover {
      background: var(--accent-hover);
    }

    .btn-primary {
      background: var(--primary);
      color: #fff;
    }
    .btn-primary:hover {
      background: var(--primary-hover);
    }

    .btn-success {
      background: var(--green);
      color: #fff;
    }
    .btn-success:hover {
      background: #166534;
    }

    .btn-danger {
      background: var(--red-bg);
      color: var(--red);
    }
    .btn-danger:hover {
      background: #fecaca;
    }

    .badge-count {
      background: var(--red);
      color: #fff;
      font-size: 11px;
      font-weight: 700;
      padding: 1px 6px;
      border-radius: 99px;
      min-width: 19px;
      text-align: center;
    }

    .badge-count.dark {
      background: var(--primary);
    }

    /* Trust Strip */
    .trust-strip {
      background: #fff;
      border-bottom: 1px solid var(--border);
      padding: 10px 20px;
    }

    .trust-inner {
      max-width: 1280px;
      margin: 0 auto;
      display: flex;
      justify-content: space-between;
      align-items: center;
      flex-wrap: wrap;
      gap: 12px;
      font-size: 12.5px;
      color: var(--muted);
      font-weight: 500;
    }

    .trust-item {
      display: flex;
      align-items: center;
      gap: 6px;
    }

    .trust-item strong {
      color: var(--text);
    }

    /* Main Container */
    .container {
      max-width: 1280px;
      margin: 0 auto;
      padding: 24px 20px 64px;
    }

    /* Hero Banner */
    .hero {
      background: linear-gradient(135deg, #0f172a 0%, #1e293b 65%, #334155 100%);
      color: #fff;
      border-radius: 16px;
      padding: 32px;
      margin-bottom: 28px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 24px;
      flex-wrap: wrap;
      box-shadow: var(--shadow-md);
    }

    .hero-tag {
      display: inline-block;
      background: rgba(234, 88, 12, 0.22);
      color: #fdba74;
      border: 1px solid rgba(253, 186, 116, 0.35);
      font-size: 11px;
      font-weight: 700;
      padding: 4px 10px;
      border-radius: 99px;
      margin-bottom: 10px;
      text-transform: uppercase;
      letter-spacing: 0.6px;
    }

    .hero h1 {
      font-size: 28px;
      font-weight: 800;
      letter-spacing: -0.5px;
      margin-bottom: 8px;
    }

    .hero p {
      color: #cbd5e1;
      font-size: 14.5px;
      max-width: 560px;
    }

    .hero-cta-group {
      display: flex;
      gap: 10px;
      flex-wrap: wrap;
    }

    /* Filter Bar */
    .toolbar {
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 12px;
      margin-bottom: 20px;
      flex-wrap: wrap;
    }

    .categories {
      display: flex;
      gap: 8px;
      flex-wrap: wrap;
    }

    .cat-pill {
      padding: 7px 14px;
      border-radius: 99px;
      font-size: 13px;
      font-weight: 600;
      border: 1px solid var(--border);
      background: #fff;
      color: var(--muted);
      cursor: pointer;
      transition: all 0.15s;
    }

    .cat-pill.active,
    .cat-pill:hover {
      background: var(--primary);
      color: #fff;
      border-color: var(--primary);
    }

    .sort-select {
      padding: 8px 12px;
      border-radius: 8px;
      border: 1px solid var(--border);
      background: #fff;
      font-size: 13px;
      font-weight: 500;
      color: var(--text);
    }

    /* Product Grid */
    .product-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
      gap: 20px;
    }

    .card {
      background: var(--surface);
      border: 1px solid var(--border);
      border-radius: var(--radius);
      overflow: hidden;
      display: flex;
      flex-direction: column;
      transition: transform 0.18s, box-shadow 0.18s;
      position: relative;
    }

    .card:hover {
      transform: translateY(-3px);
      box-shadow: var(--shadow-md);
    }

    .card-img-wrap {
      position: relative;
      width: 100%;
      height: 210px;
      background: #f1f5f9;
      overflow: hidden;
      cursor: pointer;
    }

    .card-img-wrap img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      transition: transform 0.25s;
    }

    .card:hover .card-img-wrap img {
      transform: scale(1.04);
    }

    .discount-badge {
      position: absolute;
      top: 10px;
      left: 10px;
      background: var(--green);
      color: #fff;
      font-size: 11px;
      font-weight: 800;
      padding: 3px 8px;
      border-radius: 6px;
    }

    .deal-tag {
      position: absolute;
      bottom: 10px;
      left: 10px;
      background: rgba(15, 23, 42, 0.85);
      color: #fff;
      font-size: 11px;
      font-weight: 600;
      padding: 3px 8px;
      border-radius: 5px;
    }

    .card-body {
      padding: 15px;
      display: flex;
      flex-direction: column;
      flex: 1;
    }

    .card-meta {
      display: flex;
      justify-content: space-between;
      align-items: center;
      font-size: 11.5px;
      color: var(--muted);
      margin-bottom: 5px;
    }

    .seller-verified {
      color: var(--green);
      font-weight: 600;
    }

    .card-title {
      font-size: 15px;
      font-weight: 700;
      color: var(--text);
      margin-bottom: 6px;
      cursor: pointer;
      display: -webkit-box;
      -webkit-line-clamp: 2;
      -webkit-box-orient: vertical;
      overflow: hidden;
    }

    .card-desc {
      font-size: 12.5px;
      color: var(--muted);
      margin-bottom: 12px;
      display: -webkit-box;
      -webkit-line-clamp: 2;
      -webkit-box-orient: vertical;
      overflow: hidden;
      flex: 1;
    }

    .price-row {
      display: flex;
      align-items: baseline;
      gap: 8px;
      margin-bottom: 12px;
    }

    .price-now {
      font-size: 19px;
      font-weight: 800;
      color: var(--text);
    }

    .price-mrp {
      font-size: 13px;
      color: var(--muted);
      text-decoration: line-through;
    }

    .card-actions {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 8px;
    }

    /* Modals & Drawers */
    .backdrop {
      position: fixed;
      inset: 0;
      background: rgba(15, 23, 42, 0.55);
      backdrop-filter: blur(2px);
      display: none;
      align-items: center;
      justify-content: center;
      padding: 16px;
      z-index: 60;
    }

    .backdrop.open {
      display: flex;
    }

    .modal {
      background: #fff;
      border-radius: 16px;
      width: 100%;
      max-width: 560px;
      max-height: 90vh;
      overflow-y: auto;
      box-shadow: var(--shadow-lg);
      animation: popIn 0.18s ease-out;
    }

    .modal.wide {
      max-width: 780px;
    }

    @keyframes popIn {
      from { opacity: 0; transform: scale(0.96); }
      to { opacity: 1; transform: scale(1); }
    }

    .modal-header {
      padding: 16px 20px;
      border-bottom: 1px solid var(--border);
      display: flex;
      justify-content: space-between;
      align-items: center;
      position: sticky;
      top: 0;
      background: #fff;
      z-index: 2;
    }

    .modal-header h2 {
      font-size: 17px;
      font-weight: 800;
    }

    .close-btn {
      background: #f1f5f9;
      border: none;
      width: 30px;
      height: 30px;
      border-radius: 8px;
      font-size: 18px;
      cursor: pointer;
      color: var(--muted);
    }

    .modal-body {
      padding: 20px;
    }

    /* Forms */
    .form-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 14px;
    }

    .form-group {
      display: flex;
      flex-direction: column;
      gap: 5px;
      margin-bottom: 14px;
    }

    .form-group.full {
      grid-column: 1 / -1;
    }

    label {
      font-size: 12.5px;
      font-weight: 700;
      color: var(--text);
    }

    input[type="text"],
    input[type="number"],
    input[type="password"],
    input[type="tel"],
    select,
    textarea {
      width: 100%;
      padding: 9px 12px;
      border: 1.5px solid var(--border);
      border-radius: 8px;
      font-size: 13.5px;
      background: #fff;
    }

    input:focus, select:focus, textarea:focus {
      outline: none;
      border-color: var(--primary);
    }

    .mode-switch {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 8px;
      background: #f1f5f9;
      padding: 4px;
      border-radius: 10px;
      margin-bottom: 16px;
    }

    .mode-tab {
      padding: 8px;
      text-align: center;
      font-size: 12.5px;
      font-weight: 700;
      border-radius: 7px;
      cursor: pointer;
      color: var(--muted);
      border: none;
      background: transparent;
    }

    .mode-tab.active {
      background: #fff;
      color: var(--primary);
      box-shadow: var(--shadow-sm);
    }

    .img-preview-box {
      width: 100%;
      height: 150px;
      border: 1.5px dashed var(--border);
      border-radius: 10px;
      display: flex;
      align-items: center;
      justify-content: center;
      overflow: hidden;
      background: #f8fafc;
      margin-top: 6px;
    }

    .img-preview-box img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }

    /* Cart Drawer */
    .drawer-backdrop {
      position: fixed;
      inset: 0;
      background: rgba(15, 23, 42, 0.5);
      display: none;
      justify-content: flex-end;
      z-index: 65;
    }

    .drawer-backdrop.open {
      display: flex;
    }

    .drawer {
      background: #fff;
      width: 100%;
      max-width: 420px;
      height: 100%;
      display: flex;
      flex-direction: column;
      box-shadow: var(--shadow-lg);
    }

    .drawer-items {
      flex: 1;
      overflow-y: auto;
      padding: 16px;
    }

    .cart-item {
      display: flex;
      gap: 12px;
      padding-bottom: 14px;
      margin-bottom: 14px;
      border-bottom: 1px solid var(--border);
    }

    .cart-item img {
      width: 68px;
      height: 68px;
      border-radius: 8px;
      object-fit: cover;
      background: #f1f5f9;
    }

    .qty-controls {
      display: inline-flex;
      align-items: center;
      border: 1px solid var(--border);
      border-radius: 6px;
      margin-top: 6px;
    }

    .qty-controls button {
      border: none;
      background: #f8fafc;
      padding: 2px 9px;
      font-weight: 700;
      cursor: pointer;
    }

    .qty-controls span {
      padding: 2px 10px;
      font-size: 13px;
      font-weight: 700;
    }

    .drawer-footer {
      padding: 16px 20px;
      border-top: 1px solid var(--border);
      background: #f8fafc;
    }

    /* Admin Queue Item */
    .request-card {
      border: 1px solid var(--border);
      border-radius: 12px;
      padding: 14px;
      margin-bottom: 12px;
      display: flex;
      gap: 14px;
      align-items: flex-start;
      background: #f8fafc;
    }

    .request-card img {
      width: 84px;
      height: 84px;
      border-radius: 8px;
      object-fit: cover;
      background: #e2e8f0;
      flex-shrink: 0;
    }

    .info-banner {
      background: #eff6ff;
      border: 1px solid #bfdbfe;
      color: #1e40af;
      padding: 10px 14px;
      border-radius: 8px;
      font-size: 12.5px;
      margin-bottom: 14px;
    }

    /* Toast Notification */
    .toast-container {
      position: fixed;
      bottom: 20px;
      right: 20px;
      z-index: 99;
      display: flex;
      flex-direction: column;
      gap: 8px;
    }

    .toast {
      background: var(--primary);
      color: #fff;
      padding: 11px 16px;
      border-radius: 10px;
      font-size: 13px;
      font-weight: 600;
      box-shadow: var(--shadow-lg);
      animation: slideUp 0.2s ease-out;
    }

    @keyframes slideUp {
      from { opacity: 0; transform: translateY(10px); }
      to { opacity: 1; transform: translateY(0); }
    }

    @media (max-width: 640px) {
      .form-grid { grid-template-columns: 1fr; }
      .hero h1 { font-size: 22px; }
      .request-card { flex-direction: column; }
    }
  </style>
</head>
<body>

  <!-- Top Promo Banner -->
  <div class="top-bar">
    FREE DELIVERY across India on orders above <span>₹499</span> &bull; Cash on Delivery &amp; UPI Available
  </div>

  <!-- Navigation Header -->
  <header>
    <div class="nav-container">
      <div class="brand" onclick="resetFilters()">
        <span class="brand-badge">SOUR</span>
        <div>
          <strong style="font-size: 15px; display:block; line-height:1.1;">SOUR Store</strong>
          <span class="brand-sub">India Deals Hub</span>
        </div>
      </div>

      <div class="search-box">
        <svg class="search-icon" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2">
          <circle cx="11" cy="11" r="8"></circle>
          <line x1="21" y1="21" x2="16.65" y2="16.65"></line>
        </svg>
        <input type="text" id="searchInput" placeholder="Search earbuds, watches, sneakers, home deals..." oninput="renderProducts()" />
      </div>

      <div class="nav-actions">
        <button class="btn btn-accent" onclick="openSellerModal()">
          <svg width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5">
            <line x1="12" y1="5" x2="12" y2="19"></line>
            <line x1="5" y1="12" x2="19" y2="12"></line>
          </svg>
          Sell Product
        </button>

        <button class="btn btn-outline" onclick="openAdminModal()">
          <svg width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2">
            <path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z"></path>
          </svg>
          Admin
          <span class="badge-count" id="adminBadge">0</span>
        </button>

        <button class="btn btn-primary" onclick="toggleCart(true)">
          <svg width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2">
            <circle cx="9" cy="21" r="1"></circle>
            <circle cx="20" cy="21" r="1"></circle>
            <path d="M1 1h4l2.68 13.39a2 2 0 0 0 2 1.61h9.72a2 2 0 0 0 2-1.61L23 6H6"></path>
          </svg>
          Cart
          <span class="badge-count dark" style="background:#ea580c;" id="cartBadge">0</span>
        </button>
      </div>
    </div>
  </header>

  <!-- Trust Strip -->
  <div class="trust-strip">
    <div class="trust-inner">
      <div class="trust-item"><strong>100% Verified</strong> Admin-Approved Sellers</div>
      <div class="trust-item"><strong>Pay on Delivery</strong> Cash / GPay / PhonePe</div>
      <div class="trust-item"><strong>7-Day Easy Returns</strong> Direct Doorstep Pickup</div>
      <div class="trust-item"><strong>GST Billing</strong> Available for Business Orders</div>
    </div>
  </div>

  <!-- Main Content -->
  <main class="container">
    <!-- Hero Banner -->
    <section class="hero">
      <div>
        <span class="hero-tag">Direct Factory &amp; Merchant Deals</span>
        <h1>Everyday Essentials at Unbeatable INR Prices</h1>
        <p>Shop curated electronics, fashion, and lifestyle steals from verified Indian sellers—or list your own products and deals after Admin approval.</p>
      </div>
      <div class="hero-cta-group">
        <button class="btn btn-accent" style="padding:11px 18px; font-size:14px;" onclick="openSellerModal()">+ List Your Product / Deal</button>
        <button class="btn btn-outline" style="padding:11px 18px; font-size:14px;" onclick="document.getElementById('catalogSection').scrollIntoView({behavior:'smooth'})">Browse Today's Steals</button>
      </div>
    </section>

    <!-- Filter & Sort Bar -->
    <div class="toolbar" id="catalogSection">
      <div class="categories" id="categoryPills">
        <button class="cat-pill active" onclick="setCategory('All', this)">All Deals</button>
        <button class="cat-pill" onclick="setCategory('Electronics', this)">Electronics</button>
        <button class="cat-pill" onclick="setCategory('Fashion', this)">Fashion</button>
        <button class="cat-pill" onclick="setCategory('Accessories', this)">Accessories</button>
        <button class="cat-pill" onclick="setCategory('Home & Lifestyle', this)">Home &amp; Lifestyle</button>
      </div>

      <select class="sort-select" id="sortSelect" onchange="renderProducts()">
        <option value="featured">Sort: Featured Deals</option>
        <option value="low">Price: Low to High</option>
        <option value="high">Price: High to Low</option>
        <option value="discount">Biggest Discount %</option>
      </select>
    </div>

    <!-- Product Grid -->
    <div class="product-grid" id="productGrid"></div>
  </main>

  <!-- SELLER SUBMISSION / PASSCODE MODAL -->
  <div class="backdrop" id="sellerBackdrop">
    <div class="modal">
      <div class="modal-header">
        <h2>Sell on SOUR Marketplace</h2>
        <button class="close-btn" onclick="closeModal('sellerBackdrop')">&times;</button>
      </div>
      <div class="modal-body">
        <div class="mode-switch">
          <button type="button" class="mode-tab active" id="tabRequest" onclick="switchSellerMode('request')">Request Admin Approval</button>
          <button type="button" class="mode-tab" id="tabPasscode" onclick="switchSellerMode('passcode')">Have Seller Passcode</button>
        </div>

        <div id="sellerModeInfo" class="info-banner">
          Submit your product details below. Your listing will go live immediately once the SOUR Admin reviews and accepts your request.
        </div>

        <form id="sellerForm" onsubmit="handleSellerSubmit(event)">
          <!-- Passcode Field (Shown only in Passcode Mode) -->
          <div class="form-group" id="passcodeFieldWrap" style="display:none;">
            <label>Verified Seller Passcode *</label>
            <input type="password" id="sellerPasscodeInput" placeholder="Enter seller passcode (e.g. SOUR2026)" />
          </div>

          <div class="form-grid">
            <div class="form-group">
              <label>Seller / Shop Name *</label>
              <input type="text" id="sellerName" required placeholder="e.g. Basu Electronics" />
            </div>
            <div class="form-group">
              <label>WhatsApp / Contact No. *</label>
              <input type="tel" id="sellerPhone" required placeholder="e.g. 9876543210" />
            </div>
          </div>

          <div class="form-grid">
            <div class="form-group">
              <label>Product Title *</label>
              <input type="text" id="prodTitle" required placeholder="e.g. Wireless ANC Earbuds" />
            </div>
            <div class="form-group">
              <label>Category *</label>
              <select id="prodCategory">
                <option value="Electronics">Electronics</option>
                <option value="Fashion">Fashion</option>
                <option value="Accessories">Accessories</option>
                <option value="Home & Lifestyle">Home &amp; Lifestyle</option>
              </select>
            </div>
          </div>

          <div class="form-grid">
            <div class="form-group">
              <label>Offer / Deal Price (₹ INR) *</label>
              <input type="number" id="prodPrice" required min="1" placeholder="e.g. 499" />
            </div>
            <div class="form-group">
              <label>Original MRP (₹ INR) *</label>
              <input type="number" id="prodMrp" required min="1" placeholder="e.g. 1499" />
            </div>
          </div>

          <div class="form-grid">
            <div class="form-group">
              <label>Deal Tag (Optional)</label>
              <input type="text" id="prodTag" placeholder="e.g. Today's Steal / Hot Deal" />
            </div>
            <div class="form-group">
              <label>Upload Product Photo</label>
              <input type="file" id="prodFile" accept="image/*" onchange="handleFilePreview(event)" />
            </div>
          </div>

          <div class="form-group">
            <label>Or Paste Product Image URL</label>
            <input type="text" id="prodUrl" placeholder="https://example.com/product.jpg" oninput="handleUrlPreview()" />
            <div class="img-preview-box" id="imgPreviewBox">
              <span style="font-size:12px; color:#94a3b8;">Image preview will appear here</span>
            </div>
          </div>

          <div class="form-group">
            <label>Product Highlights &amp; Description *</label>
            <textarea id="prodDesc" rows="2" required placeholder="Mention warranty, size, color, or special bundle offer..."></textarea>
          </div>

          <button type="submit" class="btn btn-accent" style="width:100%; padding:11px;" id="sellerSubmitBtn">
            Send Approval Request to Admin
          </button>
        </form>
      </div>
    </div>
  </div>

  <!-- ADMIN MODERATION MODAL -->
  <div class="backdrop" id="adminBackdrop">
    <div class="modal wide">
      <div class="modal-header">
        <h2>SOUR Admin Control Center</h2>
        <button class="close-btn" onclick="closeModal('adminBackdrop')">&times;</button>
      </div>
      <div class="modal-body">
        <!-- Admin Login Gate -->
        <div id="adminLoginView">
          <div class="info-banner">
            Restricted to Store Owner. Enter Admin Passcode to review seller requests, manage live listings, or update the Seller Passcode. (Default Passcode: <strong>SOUR2026</strong>)
          </div>
          <div class="form-group">
            <label>Admin Passcode</label>
            <input type="password" id="adminPassInput" placeholder="Enter Admin Passcode" onkeydown="if(event.key==='Enter') verifyAdmin()" />
          </div>
          <button class="btn btn-primary" style="width:100%; padding:10px;" onclick="verifyAdmin()">Unlock Admin Dashboard</button>
        </div>

        <!-- Unlocked Admin Dashboard -->
        <div id="adminDashboardView" style="display:none;">
          <div style="display:flex; justify-content:space-between; align-items:center; flex-wrap:wrap; gap:10px; background:#f8fafc; padding:12px; border-radius:10px; border:1px solid var(--border); margin-bottom:18px;">
            <div>
              <span style="font-size:12px; color:var(--muted); display:block;">Current Seller / Admin Passcode</span>
              <strong style="font-size:15px; color:var(--primary);" id="currentPassDisplay">SOUR2026</strong>
            </div>
            <div style="display:flex; gap:8px;">
              <input type="text" id="newPasscodeInput" placeholder="New passcode" style="width:150px; padding:7px 10px;" />
              <button class="btn btn-primary" onclick="updatePasscode()">Update Passcode</button>
            </div>
          </div>

          <h3 style="font-size:15px; margin-bottom:10px;">Pending Seller Approval Requests (<span id="pendingCountLabel">0</span>)</h3>
          <div id="pendingRequestsList"></div>

          <h3 style="font-size:15px; margin:20px 0 10px;">Live Store Products (<span id="liveCountLabel">0</span>)</h3>
          <div id="liveAdminProductsList"></div>
        </div>
      </div>
    </div>
  </div>

  <!-- PRODUCT QUICK VIEW MODAL -->
  <div class="backdrop" id="quickViewBackdrop">
    <div class="modal">
      <div class="modal-header">
        <h2 id="qvTitle">Product Details</h2>
        <button class="close-btn" onclick="closeModal('quickViewBackdrop')">&times;</button>
      </div>
      <div class="modal-body" id="qvBody"></div>
    </div>
  </div>

  <!-- CHECKOUT MODAL -->
  <div class="backdrop" id="checkoutBackdrop">
    <div class="modal">
      <div class="modal-header">
        <h2>Complete Your Order (INR)</h2>
        <button class="close-btn" onclick="closeModal('checkoutBackdrop')">&times;</button>
      </div>
      <div class="modal-body" id="checkoutBody">
        <form onsubmit="placeOrder(event)">
          <div class="form-grid">
            <div class="form-group">
              <label>Full Name *</label>
              <input type="text" id="custName" required placeholder="e.g. Sourish Basu" />
            </div>
            <div class="form-group">
              <label>Mobile Number *</label>
              <input type="tel" id="custPhone" required pattern="[0-9]{10}" placeholder="10-digit mobile number" />
            </div>
          </div>

          <div class="form-grid">
            <div class="form-group">
              <label>6-Digit PIN Code *</label>
              <input type="text" id="custPin" required pattern="[0-9]{6}" placeholder="e.g. 700058" />
            </div>
            <div class="form-group">
              <label>City &amp; State *</label>
              <input type="text" id="custCity" required placeholder="e.g. Kolkata, West Bengal" />
            </div>
          </div>

          <div class="form-group">
            <label>Complete Delivery Address *</label>
            <textarea id="custAddress" rows="2" required placeholder="House/Flat No., Street, Landmark..."></textarea>
          </div>

          <div class="form-group">
            <label>Payment Method *</label>
            <select id="custPayment">
              <option value="Cash on Delivery (COD)">Cash on Delivery (Pay at Doorstep)</option>
              <option value="UPI (GPay / PhonePe / Paytm)">UPI (GPay / PhonePe / Paytm)</option>
              <option value="Credit / Debit Card / NetBanking">Credit / Debit Card / NetBanking</option>
            </select>
          </div>

          <div style="background:#f8fafc; padding:12px; border-radius:10px; border:1px solid var(--border); margin-bottom:14px; display:flex; justify-content:space-between; font-weight:800;">
            <span>Total Payable Amount:</span>
            <span id="checkoutTotalDisplay">₹0</span>
          </div>

          <button type="submit" class="btn btn-success" style="width:100%; padding:12px; font-size:14px;">
            Confirm &amp; Place Order
          </button>
        </form>
      </div>
    </div>
  </div>

  <!-- SHOPPING CART DRAWER -->
  <div class="drawer-backdrop" id="cartDrawer">
    <div class="drawer">
      <div class="modal-header">
        <h2>Your Shopping Cart</h2>
        <button class="close-btn" onclick="toggleCart(false)">&times;</button>
      </div>
      <div class="drawer-items" id="cartItemsContainer"></div>
      <div class="drawer-footer">
        <div style="display:flex; justify-content:space-between; font-size:13px; color:var(--muted); margin-bottom:6px;">
          <span>Delivery Charges</span>
          <span id="deliveryFeeText" style="color:var(--green); font-weight:700;">FREE</span>
        </div>
        <div style="display:flex; justify-content:space-between; font-size:17px; font-weight:800; margin-bottom:12px;">
          <span>Subtotal</span>
          <span id="cartSubtotal">₹0</span>
        </div>
        <button class="btn btn-primary" style="width:100%; padding:12px;" onclick="openCheckout()">
          Proceed to Buy
        </button>
      </div>
    </div>
  </div>

  <!-- Toast Container -->
  <div class="toast-container" id="toastContainer"></div>

  <script>
    // Default Seed Catalog (Affordable Indian INR Pricing)
    const DEFAULT_PRODUCTS = [
      {
        id: "p1",
        title: "boAt Nirvana Ion ANC Wireless Earbuds (120H Playback)",
        category: "Electronics",
        price: 899,
        mrp: 2499,
        tag: "Bestseller Deal",
        seller: "SOUR Official",
        image: "https://images.unsplash.com/photo-1590658268037-6bf12165a8df?auto=format&fit=crop&w=600&q=80",
        desc: "Crystal clear calling with ENx quad mics, 32dB Active Noise Cancellation, and dual EQ modes."
      },
      {
        id: "p2",
        title: "Noise Pulse 2 Max 1.85\" Bluetooth Calling Smartwatch",
        category: "Electronics",
        price: 999,
        mrp: 2999,
        tag: "67% OFF",
        seller: "Metro Gadgets Kolkata",
        image: "https://images.unsplash.com/photo-1546868871-7041f2a55e12?auto=format&fit=crop&w=600&q=80",
        desc: "550 nits bright TFT display, 10-day battery backup, 100 sports modes, and SpO2 health tracking."
      },
      {
        id: "p3",
        title: "Urban Classic Oversized Cotton Drop-Shoulder Tee",
        category: "Fashion",
        price: 349,
        mrp: 899,
        tag: "Under ₹399",
        seller: "Bengal Looms",
        image: "https://images.unsplash.com/photo-1521572163474-6864f9cf17ab?auto=format&fit=crop&w=600&q=80",
        desc: "240 GSM pure combed bio-washed cotton. Breathable everyday streetwear fit."
      },
      {
        id: "p4",
        title: "Lightweight Running & Gym Sneakers (Breathable Mesh)",
        category: "Fashion",
        price: 699,
        mrp: 1799,
        tag: "Steal Deal",
        seller: "Kicks India",
        image: "https://images.unsplash.com/photo-1542291026-7eec264c27ff?auto=format&fit=crop&w=600&q=80",
        desc: "Memory foam cushioned insole with anti-skid EVA sole built for daily runs and workouts."
      },
      {
        id: "p5",
        title: "Polarized UV400 Wayfarer Sunglasses (Matte Black)",
        category: "Accessories",
        price: 299,
        mrp: 999,
        tag: "Combo Value",
        seller: "OpticHub",
        image: "https://images.unsplash.com/photo-1511499767150-a48a237f0083?auto=format&fit=crop&w=600&q=80",
        desc: "Scratch-resistant polarized lenses ideal for riding and bright afternoon sun."
      },
      {
        id: "p6",
        title: "Vacuum Insulated Stainless Steel Flask (1000ml)",
        category: "Home & Lifestyle",
        price: 399,
        mrp: 999,
        tag: "24H Hot/Cold",
        seller: "HomeCraft India",
        image: "https://images.unsplash.com/photo-1602143407151-7111542de6e8?auto=format&fit=crop&w=600&q=80",
        desc: "304 food-grade rust-free steel bottle with leakproof copper-coated thermal insulation."
      }
    ];

    // Persistent Application State
    let products = [];
    let pendingRequests = [];
    let cart = [];
    let activeCategory = "All";
    let sellerMode = "request";
    let uploadedImageData = "";
    let adminPasscode = "SOUR2026";
    let isAdminUnlocked = false;

    // Initialize on DOM load
    document.addEventListener("DOMContentLoaded", () => {
      try {
        const savedProducts = localStorage.getItem("sour_products_v1");
        products = savedProducts ? JSON.parse(savedProducts) : [...DEFAULT_PRODUCTS];

        const savedRequests = localStorage.getItem("sour_pending_v1");
        pendingRequests = savedRequests ? JSON.parse(savedRequests) : [];

        const savedCart = localStorage.getItem("sour_cart_v1");
        cart = savedCart ? JSON.parse(savedCart) : [];

        const savedPass = localStorage.getItem("sour_passcode_v1");
        if (savedPass) adminPasscode = savedPass;
      } catch (e) {
        products = [...DEFAULT_PRODUCTS];
        pendingRequests = [];
        cart = [];
      }

      saveState();
      renderProducts();
      updateBadges();
    });

    function saveState() {
      try {
        localStorage.setItem("sour_products_v1", JSON.stringify(products));
        localStorage.setItem("sour_pending_v1", JSON.stringify(pendingRequests));
        localStorage.setItem("sour_cart_v1", JSON.stringify(cart));
        localStorage.setItem("sour_passcode_v1", adminPasscode);
      } catch (e) {
        // Ignore storage quota errors if huge images are uploaded
      }
    }

    function formatINR(num) {
      return "₹" + Number(num).toLocaleString("en-IN");
    }

    function showToast(msg) {
      const container = document.getElementById("toastContainer");
      const el = document.createElement("div");
      el.className = "toast";
      el.textContent = msg;
      container.appendChild(el);
      setTimeout(() => el.remove(), 3200);
    }

    function updateBadges() {
      document.getElementById("adminBadge").textContent = pendingRequests.length;
      const totalQty = cart.reduce((sum, item) => sum + item.qty, 0);
      document.getElementById("cartBadge").textContent = totalQty;
    }

    // Category & Filter Controls
    function setCategory(cat, btn) {
      activeCategory = cat;
      document.querySelectorAll(".cat-pill").forEach(p => p.classList.remove("active"));
      if (btn) btn.classList.add("active");
      renderProducts();
    }

    function resetFilters() {
      activeCategory = "All";
      document.getElementById("searchInput").value = "";
      document.getElementById("sortSelect").value = "featured";
      document.querySelectorAll(".cat-pill").forEach((p, idx) => {
        p.classList.toggle("active", idx === 0);
      });
      renderProducts();
    }

    // Render Product Catalog
    function renderProducts() {
      const grid = document.getElementById("productGrid");
      const query = document.getElementById("searchInput").value.trim().toLowerCase();
      const sort = document.getElementById("sortSelect").value;

      let list = products.filter(p => {
        const matchCat = activeCategory === "All" || p.category === activeCategory;
        const matchQuery = !query ||
          p.title.toLowerCase().includes(query) ||
          p.category.toLowerCase().includes(query) ||
          p.seller.toLowerCase().includes(query);
        return matchCat && matchQuery;
      });

      if (sort === "low") list.sort((a, b) => a.price - b.price);
      if (sort === "high") list.sort((a, b) => b.price - a.price);
      if (sort === "discount") {
        list.sort((a, b) => ((b.mrp - b.price) / b.mrp) - ((a.mrp - a.price) / a.mrp));
      }

      if (list.length === 0) {
        grid.innerHTML = `<div style="grid-column:1/-1; text-align:center; padding:48px 20px; background:#fff; border-radius:12px; border:1px solid var(--border);">
          <h3 style="margin-bottom:6px;">No matching deals found</h3>
          <p style="color:var(--muted); font-size:13.5px;">Try clearing your search filter or list a new product.</p>
        </div>`;
        return;
      }

      grid.innerHTML = list.map(p => {
        const off = p.mrp > p.price ? Math.round(((p.mrp - p.price) / p.mrp) * 100) : 0;
        return `
          <article class="card">
            <div class="card-img-wrap" onclick="openQuickView('${p.id}')">
              <img src="${p.image}" alt="${p.title}" onerror="this.src='https://images.unsplash.com/photo-1523275335684-37898b6baf30?auto=format&fit=crop&w=600&q=80'" />
              ${off > 0 ? `<span class="discount-badge">${off}% OFF</span>` : ""}
              ${p.tag ? `<span class="deal-tag">${p.tag}</span>` : ""}
            </div>
            <div class="card-body">
              <div class="card-meta">
                <span>${p.category}</span>
                <span class="seller-verified">&#10003; ${p.seller}</span>
              </div>
              <h3 class="card-title" onclick="openQuickView('${p.id}')">${p.title}</h3>
              <p class="card-desc">${p.desc}</p>
              <div class="price-row">
                <span class="price-now">${formatINR(p.price)}</span>
                ${p.mrp > p.price ? `<span class="price-mrp">${formatINR(p.mrp)}</span>` : ""}
              </div>
              <div class="card-actions">
                <button class="btn btn-outline" onclick="addToCart('${p.id}')">+ Add to Cart</button>
                <button class="btn btn-primary" onclick="buyNow('${p.id}')">Buy Now</button>
              </div>
            </div>
          </article>
        `;
      }).join("");
    }

    // Quick View Modal
    function openQuickView(id) {
      const p = products.find(item => item.id === id);
      if (!p) return;
      const off = p.mrp > p.price ? Math.round(((p.mrp - p.price) / p.mrp) * 100) : 0;

      document.getElementById("qvTitle").textContent = p.category + " • Sold by " + p.seller;
      document.getElementById("qvBody").innerHTML = `
        <img src="${p.image}" style="width:100%; height:260px; object-fit:cover; border-radius:12px; margin-bottom:14px;" />
        <h3 style="font-size:19px; margin-bottom:8px;">${p.title}</h3>
        <div class="price-row">
          <span class="price-now" style="font-size:24px;">${formatINR(p.price)}</span>
          ${p.mrp > p.price ? `<span class="price-mrp">${formatINR(p.mrp)}</span>` : ""}
          ${off > 0 ? `<span style="color:var(--green); font-weight:700; font-size:13px;">(${off}% OFF)</span>` : ""}
        </div>
        <p style="color:var(--muted); font-size:14px; margin-bottom:16px;">${p.desc}</p>
        <div style="display:grid; grid-template-columns:1fr 1fr; gap:10px;">
          <button class="btn btn-outline" style="padding:11px;" onclick="addToCart('${p.id}'); closeModal('quickViewBackdrop')">Add to Cart</button>
          <button class="btn btn-accent" style="padding:11px;" onclick="closeModal('quickViewBackdrop'); buyNow('${p.id}')">Buy Now (COD / UPI)</button>
        </div>
      `;
      document.getElementById("quickViewBackdrop").classList.add("open");
    }

    // Seller Portal Logic
    function openSellerModal() {
      document.getElementById("sellerForm").reset();
      uploadedImageData = "";
      document.getElementById("imgPreviewBox").innerHTML = `<span style="font-size:12px; color:#94a3b8;">Image preview will appear here</span>`;
      switchSellerMode("request");
      document.getElementById("sellerBackdrop").classList.add("open");
    }

    function switchSellerMode(mode) {
      sellerMode = mode;
      document.getElementById("tabRequest").classList.toggle("active", mode === "request");
      document.getElementById("tabPasscode").classList.toggle("active", mode === "passcode");

      const passWrap = document.getElementById("passcodeFieldWrap");
      const info = document.getElementById("sellerModeInfo");
      const btn = document.getElementById("sellerSubmitBtn");

      if (mode === "passcode") {
        passWrap.style.display = "block";
        info.textContent = "Passcode Mode: Enter the authorized SOUR Seller Passcode to publish your product directly without waiting.";
        btn.textContent = "Verify Passcode & Publish Live";
      } else {
        passWrap.style.display = "none";
        info.textContent = "Approval Mode: Submit your product details below. An Admin notification will be triggered so the owner can approve your listing.";
        btn.textContent = "Send Approval Request to Admin";
      }
    }

    function handleFilePreview(e) {
      const file = e.target.files[0];
      if (!file) return;
      const reader = new FileReader();
      reader.onload = function(ev) {
        uploadedImageData = ev.target.result;
        document.getElementById("imgPreviewBox").innerHTML = `<img src="${uploadedImageData}" alt="Preview" />`;
      };
      reader.readAsDataURL(file);
    }

    function handleUrlPreview() {
      const url = document.getElementById("prodUrl").value.trim();
      if (url) {
        uploadedImageData = url;
        document.getElementById("imgPreviewBox").innerHTML = `<img src="${url}" alt="Preview" />`;
      }
    }

    function handleSellerSubmit(e) {
      e.preventDefault();
      const sellerName = document.getElementById("sellerName").value.trim();
      const sellerPhone = document.getElementById("sellerPhone").value.trim();
      const title = document.getElementById("prodTitle").value.trim();
      const category = document.getElementById("prodCategory").value;
      const price = Number(document.getElementById("prodPrice").value);
      const mrp = Number(document.getElementById("prodMrp").value);
      const tag = document.getElementById("prodTag").value.trim() || "New Arrival";
      const desc = document.getElementById("prodDesc").value.trim();
      const fallbackImg = "https://images.unsplash.com/photo-1523275335684-37898b6baf30?auto=format&fit=crop&w=600&q=80";
      const image = uploadedImageData || document.getElementById("prodUrl").value.trim() || fallbackImg;

      const newItem = {
        id: "prod_" + Date.now(),
        title,
        category,
        price,
        mrp: mrp >= price ? mrp : price,
        tag,
        seller: sellerName,
        phone: sellerPhone,
        image,
        desc,
        submittedAt: new Date().toLocaleString("en-IN")
      };

      if (sellerMode === "passcode") {
        const enteredPass = document.getElementById("sellerPasscodeInput").value.trim();
        if (enteredPass !== adminPasscode) {
          showToast("Invalid Seller Passcode! Switch to Request Approval instead.");
          return;
        }
        products.unshift(newItem);
        saveState();
        renderProducts();
        closeModal("sellerBackdrop");
        showToast("Passcode verified! Your product is now LIVE on SOUR.");
      } else {
        pendingRequests.unshift(newItem);
        saveState();
        updateBadges();
        closeModal("sellerBackdrop");
        showToast("Request sent! Admin notified for approval.");
      }
    }

    // Admin Moderation System
    function openAdminModal() {
      document.getElementById("adminBackdrop").classList.add("open");
      if (isAdminUnlocked) {
        renderAdminDashboard();
      } else {
        document.getElementById("adminLoginView").style.display = "block";
        document.getElementById("adminDashboardView").style.display = "none";
        document.getElementById("adminPassInput").value = "";
      }
    }

    function verifyAdmin() {
      const val = document.getElementById("adminPassInput").value.trim();
      if (val === adminPasscode) {
        isAdminUnlocked = true;
        document.getElementById("adminLoginView").style.display = "none";
        document.getElementById("adminDashboardView").style.display = "block";
        renderAdminDashboard();
        showToast("Admin access unlocked.");
      } else {
        showToast("Incorrect Admin Passcode.");
      }
    }

    function updatePasscode() {
      const next = document.getElementById("newPasscodeInput").value.trim();
      if (next.length < 4) {
        showToast("Passcode must be at least 4 characters.");
        return;
      }
      adminPasscode = next;
      saveState();
      document.getElementById("currentPassDisplay").textContent = adminPasscode;
      document.getElementById("newPasscodeInput").value = "";
      showToast("Passcode updated to: " + adminPasscode);
    }

    function renderAdminDashboard() {
      document.getElementById("currentPassDisplay").textContent = adminPasscode;
      document.getElementById("pendingCountLabel").textContent = pendingRequests.length;
      document.getElementById("liveCountLabel").textContent = products.length;

      const reqContainer = document.getElementById("pendingRequestsList");
      if (pendingRequests.length === 0) {
        reqContainer.innerHTML = `<p style="font-size:13px; color:var(--muted); padding:12px; background:#f8fafc; border-radius:8px;">No pending seller requests right now.</p>`;
      } else {
        reqContainer.innerHTML = pendingRequests.map((req, index) => `
          <div class="request-card">
            <img src="${req.image}" alt="${req.title}" />
            <div style="flex:1;">
              <div style="display:flex; justify-content:space-between; flex-wrap:wrap; gap:6px;">
                <strong>${req.title}</strong>
                <span style="font-weight:800; color:var(--green);">${formatINR(req.price)} <small style="color:var(--muted); text-decoration:line-through;">${formatINR(req.mrp)}</small></span>
              </div>
              <div style="font-size:12px; color:var(--muted); margin:4px 0;">
                Seller: <strong>${req.seller}</strong> &bull; Phone: <strong>${req.phone || "N/A"}</strong> &bull; Category: ${req.category}
              </div>
              <p style="font-size:12.5px; margin-bottom:10px;">${req.desc}</p>
              <div style="display:flex; gap:8px;">
                <button class="btn btn-success" onclick="approveRequest(${index})">&#10003; Accept &amp; Go Live</button>
                <button class="btn btn-danger" onclick="rejectRequest(${index})">&#10005; Reject</button>
              </div>
            </div>
          </div>
        `).join("");
      }

      const liveContainer = document.getElementById("liveAdminProductsList");
      liveContainer.innerHTML = products.map((p, index) => `
        <div style="display:flex; justify-content:space-between; align-items:center; padding:8px 12px; border:1px solid var(--border); border-radius:8px; margin-bottom:6px; font-size:13px;">
          <div>
            <strong>${p.title}</strong> <span style="color:var(--muted);">(${formatINR(p.price)} &bull; ${p.seller})</span>
          </div>
          <button class="btn btn-danger" style="padding:5px 10px; font-size:12px;" onclick="removeLiveProduct(${index})">Remove</button>
        </div>
      `).join("");
    }

    function approveRequest(index) {
      const approved = pendingRequests.splice(index, 1)[0];
      if (approved) {
        products.unshift(approved);
        saveState();
        updateBadges();
        renderProducts();
        renderAdminDashboard();
        showToast(`Approved "${approved.title}" — Now live!`);
      }
    }

    function rejectRequest(index) {
      const removed = pendingRequests.splice(index, 1)[0];
      saveState();
      updateBadges();
      renderAdminDashboard();
      if (removed) showToast(`Rejected submission from ${removed.seller}.`);
    }

    function removeLiveProduct(index) {
      products.splice(index, 1);
      saveState();
      renderProducts();
      renderAdminDashboard();
      showToast("Product removed from live store.");
    }

    // Cart & Buying Flow
    function addToCart(id) {
      const existing = cart.find(c => c.id === id);
      if (existing) {
        existing.qty += 1;
      } else {
        cart.push({ id, qty: 1 });
      }
      saveState();
      updateBadges();
      showToast("Added to your cart!");
    }

    function buyNow(id) {
      const existing = cart.find(c => c.id === id);
      if (!existing) {
        cart.push({ id, qty: 1 });
        saveState();
        updateBadges();
      }
      openCheckout();
    }

    function toggleCart(show) {
      const drawer = document.getElementById("cartDrawer");
      if (show) {
        renderCart();
        drawer.classList.add("open");
      } else {
        drawer.classList.remove("open");
      }
    }

    function changeQty(id, delta) {
      const idx = cart.findIndex(c => c.id === id);
      if (idx === -1) return;
      cart[idx].qty += delta;
      if (cart[idx].qty <= 0) cart.splice(idx, 1);
      saveState();
      updateBadges();
      renderCart();
    }

    function getCartTotals() {
      let subtotal = 0;
      cart.forEach(item => {
        const p = products.find(prod => prod.id === item.id);
        if (p) subtotal += p.price * item.qty;
      });
      const delivery = subtotal > 0 && subtotal < 499 ? 49 : 0;
      return { subtotal, delivery, total: subtotal + delivery };
    }

    function renderCart() {
      const container = document.getElementById("cartItemsContainer");
      if (cart.length === 0) {
        container.innerHTML = `<div style="text-align:center; padding:48px 16px; color:var(--muted);">
          <p style="font-weight:700; margin-bottom:6px;">Your SOUR cart is empty</p>
          <p style="font-size:13px;">Explore deals and add items to place an order.</p>
        </div>`;
        document.getElementById("cartSubtotal").textContent = "₹0";
        document.getElementById("deliveryFeeText").textContent = "FREE";
        return;
      }

      container.innerHTML = cart.map(item => {
        const p = products.find(prod => prod.id === item.id);
        if (!p) return "";
        return `
          <div class="cart-item">
            <img src="${p.image}" alt="${p.title}" />
            <div style="flex:1;">
              <div style="font-size:13.5px; font-weight:700; margin-bottom:3px;">${p.title}</div>
              <div style="font-size:14px; font-weight:800; color:var(--primary);">${formatINR(p.price)}</div>
              <div class="qty-controls">
                <button onclick="changeQty('${p.id}', -1)">-</button>
                <span>${item.qty}</span>
                <button onclick="changeQty('${p.id}', 1)">+</button>
              </div>
            </div>
          </div>
        `;
      }).join("");

      const { subtotal, delivery, total } = getCartTotals();
      document.getElementById("deliveryFeeText").textContent = delivery === 0 ? "FREE" : formatINR(delivery);
      document.getElementById("cartSubtotal").textContent = formatINR(total);
    }

    function openCheckout() {
      if (cart.length === 0) {
        showToast("Your cart is empty! Add an item first.");
        return;
      }
      toggleCart(false);
      const { total } = getCartTotals();
      document.getElementById("checkoutTotalDisplay").textContent = formatINR(total);
      document.getElementById("checkoutBackdrop").classList.add("open");
    }

    function placeOrder(e) {
      e.preventDefault();
      const name = document.getElementById("custName").value.trim();
      const phone = document.getElementById("custPhone").value.trim();
      const pin = document.getElementById("custPin").value.trim();
      const city = document.getElementById("custCity").value.trim();
      const payment = document.getElementById("custPayment").value;
      const { total } = getCartTotals();
      const orderId = "SOUR-" + Math.floor(100000 + Math.random() * 900000);

      cart = [];
      saveState();
      updateBadges();

      document.getElementById("checkoutBody").innerHTML = `
        <div style="text-align:center; padding:16px 8px;">
          <div style="width:52px; height:52px; background:var(--green-bg); color:var(--green); border-radius:99px; display:inline-flex; align-items:center; justify-content:center; font-size:26px; font-weight:900; margin-bottom:12px;">&#10003;</div>
          <h3 style="font-size:20px; margin-bottom:6px;">Order Confirmed!</h3>
          <p style="color:var(--muted); font-size:13.5px; margin-bottom:16px;">Thank you, <strong>${name}</strong>. Your order <strong>#${orderId}</strong> has been placed.</p>
          <div style="background:#f8fafc; border:1px solid var(--border); border-radius:10px; padding:12px; text-align:left; font-size:13px; margin-bottom:16px;">
            <div><strong>Amount Paid / Payable:</strong> ${formatINR(total)} (${payment})</div>
            <div><strong>Delivery Location:</strong> ${city} - ${pin}</div>
            <div><strong>SMS Updates Sent To:</strong> +91 ${phone}</div>
          </div>
          <button class="btn btn-primary" style="width:100%; padding:11px;" onclick="location.reload()">Continue Shopping</button>
        </div>
      `;
    }

    function closeModal(id) {
      document.getElementById(id).classList.remove("open");
    }
  </script>
</body>
</html>
