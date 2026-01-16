<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
    <style>
      * {
        box-sizing: border-box;
        margin: 0;
        padding: 0;
      }

      img {
        max-width: 100%;
        height: auto;
      }

      :root {
        --primary-blue: #0041a3;
        --text-white: #ffffff;
        --green-badge: #2dca73;
      }

      body {
        margin: 0;
        font-family: "Segoe UI", Roboto, sans-serif;
        width: 100%;
        overflow-x: hidden;
        position: relative;
      }

      .navbar-container {
        background: rgba(0, 0, 0, 0.2);
        padding: 12px 40px;
        position: absolute;
        width: 100%;
        z-index: 100;
      }

      .navbar-content {
        display: flex;
        justify-content: space-between;
        align-items: center;
        max-width: 1400px;
        margin: 0 auto;
      }

      .left-section {
        display: flex;
        align-items: center;
        gap: 15px;
      }

      .logo {
        font-size: 24px;
        font-weight: 800;
        color: var(--text-white);
      }

      .location-selector {
        color: var(--text-white);
        font-size: 14px;
        cursor: pointer;
      }

      .center-nav ul {
        display: flex;
        list-style: none;
        gap: 20px;
      }

      .center-nav a {
        text-decoration: none;
        color: var(--text-white);
        font-size: 14px;
        font-weight: 500;
      }

      .insights {
        position: relative;
      }

      .new-badge {
        background: #eb3c44;
        color: white;
        font-size: 8px;
        padding: 1px 3px;
        border-radius: 2px;
        position: absolute;
        top: -8px;
        right: -25px;
      }

      .right-section {
        display: flex;
        align-items: center;
        gap: 20px;
      }

      .post-property-btn {
        background: white;
        color: #333;
        padding: 8px 16px;
        border-radius: 20px;
        text-decoration: none;
        font-size: 13px;
        font-weight: bold;
        display: flex;
        align-items: center;
        gap: 5px;
      }

      .free-badge {
        background: var(--green-badge);
        color: white;
        font-size: 9px;
        padding: 2px 4px;
        border-radius: 3px;
      }

      .icon-actions {
        display: flex;
        align-items: center;
        gap: 15px;
        color: white;
        font-size: 18px;
        cursor: pointer;
      }

      .user-profile {
        display: flex;
        align-items: center;
        gap: 5px;
        font-size: 20px;
      }

      .arrow {
        font-size: 10px;
      }

      .hero-banner {
        position: relative;
        width: 100vw;
        height: 200px;
        background-image: linear-gradient(
            to bottom,
            rgba(0, 0, 0, 0.3),
            rgba(0, 0, 0, 0.1)
          ),
          url("lohri.webp");
        background-size: cover;
        background-position: center;
        display: flex;
        flex-direction: column;
        align-items: center;
        box-sizing: border-box;
      }

      .hero-content {
        margin-top: 100px;
        width: 100vw;
        max-width: 100%;
        display: flex;
        justify-content: center;
      }

      .search-card {
        background: #ffffff;
        width: 95%;
        max-width: 1000px;
        border-radius: 12px;
        padding: 0;
        box-shadow: 0 8px 30px rgba(0, 0, 0, 0.15);
        overflow: hidden;
        margin: 20px auto;
      }

      .search-tabs {
        display: flex;
        align-items: center;
        padding: 0 20px;
        border-bottom: 1px solid #f0f0f0;
        gap: 25px;
        overflow-x: auto;
      }

      .tab {
        background: none;
        border: none;
        padding: 18px 0;
        font-size: 14px;
        font-weight: 600;
        color: #42526e;
        cursor: pointer;
        position: relative;
        white-space: nowrap;
      }

      .tab.active {
        color: #0078db;
      }

      .tab.active::after {
        content: "";
        position: absolute;
        bottom: 0;
        left: 0;
        width: 100%;
        height: 3px;
        background: #0078db;
      }

      .dot {
        height: 6px;
        width: 6px;
        background-color: #d8232a;
        border-radius: 50%;
        display: inline-block;
        margin-left: 2px;
      }

      .tab-divider {
        height: 24px;
        width: 1px;
        background: #e0e0e0;
      }

      .search-bar-row {
        display: flex;
        align-items: center;
        padding: 12px 20px;
      }

      .dropdown-filter {
        display: flex;
        align-items: center;
        gap: 8px;
        font-size: 14px;
        color: #091e42;
        padding-right: 15px;
        border-right: 1px solid #e0e0e0;
        cursor: pointer;
      }

      .search-input-wrapper {
        flex: 1;
        display: flex;
        align-items: center;
        padding: 0 15px;
      }

      .search-input-wrapper input {
        width: 100%;
        border: none;
        outline: none;
        font-size: 14px;
        color: #42526e;
      }

      .search-actions {
        display: flex;
        align-items: center;
        gap: 15px;
      }

      .icon-btn {
        background: #f4f5f7;
        border: none;
        border-radius: 50%;
        width: 32px;
        height: 32px;
        cursor: pointer;
      }

      .search-submit-btn {
        background: #0078db;
        color: white;
        border: none;
        padding: 10px 30px;
        border-radius: 6px;
        font-weight: bold;
        font-size: 14px;
        cursor: pointer;
      }
    </style>
  </head>
  <body>
    <header class="navbar-container">
      <div class="navbar-content">
        <div class="left-section">
          <div class="logo">99acres</div>
          <div class="location-selector">
            All India <span class="arrow">▼</span>
          </div>
        </div>

        <nav class="center-nav">
          <ul>
            <li><a href="#">For Buyers</a></li>
            <li><a href="#">For Tenants</a></li>
            <li><a href="#">For Owners</a></li>
            <li><a href="#">For Dealers / Builders</a></li>
            <li class="insights">
              <a href="#">Insights</a>
              <span class="new-badge">NEW</span>
            </li>
          </ul>
        </nav>

        <div class="right-section">
          <a href="#" class="post-property-btn">
            Post property <span class="free-badge">FREE</span>
          </a>
          <div class="icon-actions">
            <span class="icon">🎧</span>
            <span class="user-profile">👤 <span class="arrow">▼</span></span>
            <span class="hamburger">☰</span>
          </div>
        </div>
      </div>
    </header>

    <section class="hero-banner">
      <div class="hero-content"></div>
    </section>

    <div class="search-card">
      <div class="search-tabs">
        <button class="tab active">Buy</button>
        <button class="tab">Rent</button>
        <button class="tab">New Launch <span class="dot"></span></button>
        <button class="tab">Commercial</button>
        <button class="tab">Plots/Land</button>
        <button class="tab">Projects</button>
        <div class="tab-divider"></div>
        <button class="tab post-tab">
          Post Property <span class="free-badge">FREE</span>
        </button>
      </div>

      <div class="search-bar-row">
        <div class="dropdown-filter">
          <span>All Residential</span>
          <span class="chevron">⌄</span>
        </div>

        <div class="search-input-wrapper">
          <span class="search-icon">🔍</span>
          <input
            type="text"
            placeholder='Search "Flats for rent in sector 77 Noida"'
          />
        </div>

        <div class="search-actions">
          <button class="icon-btn">📍</button>
          <button class="icon-btn">🎙️</button>
          <button class="search-submit-btn">Search</button>
        </div>
      </div>
    </div>
  </body>
  <div>rahul side</div>
</html>
