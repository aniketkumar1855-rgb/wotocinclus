<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Otocinclus - HR Consultancy & HRMS Implementation Partner | Build, Operate, Transfer</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta
    name="description"
    content="Otocinclus delivers integrated HR infrastructure for India's growing businesses. Expert HR consultancy, HRMS implementation, payroll compliance, and flat 7% recruitment."
  />
  <meta
    name="keywords"
    content="HR consultancy, HRMS implementation, payroll services, recruitment agency, HR outsourcing, compliance management, Build-Operate-Transfer, SME HR solutions"
  />

  <style>
    /* ---------------------------------
       Core variables and global reset
    --------------------------------- */
    :root {
      --primary-blue: #4a90e2;
      --secondary-blue: #5ba3f5;
      --accent-orange: #e89f5f;
      --dark-navy: #1f2533;
      --light-bg: #fcfcf9;
      --text-dark: #1f2533;
      --text-light: #626c71;
      --white: #ffffff;

      --gradient-primary: linear-gradient(135deg, #4a90e2 0%, #5ba3f5 100%);
      --gradient-secondary: linear-gradient(135deg, #e89f5f 0%, #f5b87f 100%);

      --nav-height: 80px;
      --max-width: 1200px;
    }

    *,
    *::before,
    *::after {
      box-sizing: border-box;
    }

    html,
    body {
      margin: 0;
      padding: 0;
      width: 100%;
      height: 100%;
      scroll-behavior: smooth;
    }

    body {
      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto,
        "Helvetica Neue", Arial, sans-serif;
      color: var(--text-dark);
      line-height: 1.6;
      overflow-x: hidden;
      background-color: var(--light-bg);
    }

    img,
    svg {
      max-width: 100%;
      height: auto;
      display: block;
    }

    a {
      color: inherit;
    }

    /* ------------------------------
       Layout helpers
    ------------------------------ */
    .container {
      max-width: var(--max-width);
      margin: 0 auto;
      padding: 0 1.5rem;
      width: 100%;
    }

    section {
      width: 100%;
      padding: 5rem 0;
    }

    .section-title {
      text-align: center;
      margin-bottom: 3rem;
    }

    .section-title h2 {
      font-size: 2.4rem;
      margin-bottom: 0.75rem;
      color: var(--dark-navy);
      letter-spacing: -0.5px;
    }

    .section-title p {
      font-size: 1.05rem;
      color: var(--text-light);
      max-width: 640px;
      margin: 0 auto;
    }

    /* ------------------------------
       Navigation
    ------------------------------ */
    nav {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: var(--nav-height);
      background: rgba(255, 255, 255, 0.96);
      backdrop-filter: blur(10px);
      box-shadow: 0 2px 16px rgba(0, 0, 0, 0.08);
      z-index: 1000;
      transition: box-shadow 0.3s ease, background 0.3s ease;
    }

    nav.scrolled {
      box-shadow: 0 4px 24px rgba(0, 0, 0, 0.16);
      background: rgba(255, 255, 255, 0.98);
    }

    .nav-inner {
      height: 100%;
      display: flex;
      align-items: center;
      justify-content: space-between;
    }

    .logo-wrap {
      display: flex;
      align-items: center;
      gap: 0.75rem;
    }

    .logo-circle {
      width: 44px;
      height: 44px;
      border-radius: 50%;
      background: var(--gradient-primary);
      display: flex;
      align-items: center;
      justify-content: center;
      color: var(--white);
      font-weight: 800;
      font-size: 1.2rem;
      letter-spacing: -0.5px;
      animation: logoFloat 3s ease-in-out infinite;
    }

    .logo-text h1 {
      margin: 0;
      font-size: 1.4rem;
      font-weight: 800;
      letter-spacing: -0.6px;
      color: var(--dark-navy);
    }

    .logo-text p {
      margin: 0;
      font-size: 0.8rem;
      color: var(--primary-blue);
      font-weight: 500;
    }

    .nav-links {
      display: flex;
      list-style: none;
      gap: 1.75rem;
      margin: 0;
      padding: 0;
      align-items: center;
    }

    .nav-links a {
      text-decoration: none;
      font-size: 0.95rem;
      font-weight: 500;
      color: var(--text-dark);
      position: relative;
      padding-bottom: 3px;
    }

    .nav-links a::after {
      content: "";
      position: absolute;
      left: 0;
      bottom: 0;
      width: 0;
      height: 2px;
      background: var(--gradient-primary);
      transition: width 0.25s ease;
    }

    .nav-links a:hover::after {
      width: 100%;
    }

    .nav-cta {
      padding: 0.65rem 1.4rem;
      border-radius: 999px;
      border: none;
      background: var(--gradient-primary);
      color: var(--white);
      font-size: 0.95rem;
      font-weight: 600;
      cursor: pointer;
      box-shadow: 0 6px 16px rgba(74, 144, 226, 0.35);
      text-decoration: none;
      white-space: nowrap;
    }

    .nav-cta:hover {
      transform: translateY(-1px);
      box-shadow: 0 8px 20px rgba(74, 144, 226, 0.45);
    }

    .mobile-toggle {
      display: none;
      width: 26px;
      height: 20px;
      flex-direction: column;
      justify-content: space-between;
      cursor: pointer;
    }

    .mobile-toggle span {
      height: 3px;
      width: 100%;
      background: var(--text-dark);
      border-radius: 2px;
      transition: transform 0.3s ease, opacity 0.3s ease;
    }

    .mobile-toggle.active span:nth-child(1) {
      transform: translateY(8.5px) rotate(45deg);
    }

    .mobile-toggle.active span:nth-child(2) {
      opacity: 0;
    }

    .mobile-toggle.active span:nth-child(3) {
      transform: translateY(-8.5px) rotate(-45deg);
    }

    /* ------------------------------
       Hero (full-screen)
    ------------------------------ */
    .hero {
      min-height: calc(100vh - var(--nav-height));
      padding-top: calc(var(--nav-height) + 1rem);
      padding-bottom: 4rem;
      background: linear-gradient(
        135deg,
        rgba(74, 144, 226, 0.05) 0%,
        rgba(232, 159, 95, 0.08) 100%
      );
      position: relative;
      overflow: hidden;
      display: flex;
      align-items: center;
    }

    .hero::before {
      content: "";
      position: absolute;
      top: -40%;
      right: -10%;
      width: 600px;
      height: 600px;
      border-radius: 50%;
      background: radial-gradient(
        circle,
        rgba(74, 144, 226, 0.14) 0%,
        transparent 70%
      );
      pointer-events: none;
    }

    .hero-inner {
      position: relative;
      z-index: 1;
      display: grid;
      grid-template-columns: minmax(0, 1.3fr) minmax(0, 1fr);
      gap: 3.5rem;
      align-items: center;
    }

    .hero h2 {
      font-size: 3rem;
      line-height: 1.1;
      margin: 0 0 1rem;
      color: var(--dark-navy);
      letter-spacing: -1px;
    }

    .hero .highlight {
      background: var(--gradient-primary);
      -webkit-background-clip: text;
      background-clip: text;
      -webkit-text-fill-color: transparent;
    }

    .hero .tagline {
      font-size: 1.2rem;
      margin-bottom: 1.5rem;
      color: var(--text-light);
      font-weight: 500;
    }

    .hero p.lead {
      font-size: 1.03rem;
      color: var(--text-light);
      max-width: 640px;
      margin-bottom: 2rem;
    }

    .hero-buttons {
      display: flex;
      flex-wrap: wrap;
      gap: 1rem;
    }

    .btn-primary {
      border: none;
      border-radius: 999px;
      padding: 0.9rem 2.2rem;
      font-weight: 600;
      font-size: 1rem;
      cursor: pointer;
      background: var(--gradient-primary);
      color: var(--white);
      box-shadow: 0 8px 20px rgba(74, 144, 226, 0.4);
      text-decoration: none;
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 0.4rem;
    }

    .btn-primary:hover {
      transform: translateY(-2px);
      box-shadow: 0 10px 26px rgba(74, 144, 226, 0.5);
    }

    .btn-secondary {
      border-radius: 999px;
      padding: 0.9rem 2.2rem;
      font-weight: 600;
      font-size: 1rem;
      cursor: pointer;
      background: #ffffff;
      border: 2px solid var(--primary-blue);
      color: var(--primary-blue);
      text-decoration: none;
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 0.4rem;
    }

    .btn-secondary:hover {
      background: var(--primary-blue);
      color: var(--white);
      transform: translateY(-2px);
    }

    .hero-badges {
      margin-top: 1.5rem;
      display: flex;
      flex-wrap: wrap;
      gap: 0.75rem;
      font-size: 0.85rem;
      color: var(--text-light);
    }

    .hero-badge {
      padding: 0.3rem 0.75rem;
      border-radius: 999px;
      background: rgba(74, 144, 226, 0.05);
      border: 1px solid rgba(74, 144, 226, 0.18);
    }

    .hero-right {
      display: flex;
      flex-direction: column;
      gap: 1.2rem;
    }

    .floating-card {
      background: #ffffff;
      border-radius: 18px;
      padding: 1.4rem 1.6rem;
      box-shadow: 0 8px 30px rgba(0, 0, 0, 0.08);
      transition: transform 0.25s ease, box-shadow 0.25s ease;
    }

    .floating-card:hover {
      transform: translateY(-4px);
      box-shadow: 0 12px 40px rgba(0, 0, 0, 0.12);
    }

    .floating-card h3 {
      margin: 0 0 0.4rem;
      font-size: 1.1rem;
      color: var(--primary-blue);
    }

    .floating-card p {
      margin: 0;
      font-size: 0.92rem;
      color: var(--text-light);
    }

    /* ------------------------------
       Stats
    ------------------------------ */
    .stats {
      background: var(--gradient-primary);
      color: var(--white);
    }

    .stats-grid {
      display: grid;
      grid-template-columns: repeat(4, minmax(0, 1fr));
      gap: 2.5rem;
      text-align: center;
    }

    .stat-item h3 {
      font-size: 2.6rem;
      margin: 0 0 0.3rem;
      font-weight: 800;
    }

    .stat-item p {
      margin: 0;
      font-size: 0.98rem;
      opacity: 0.96;
    }

    /* ------------------------------
       Core Values Slideshow
    ------------------------------ */
    .core-values {
      padding-top: 4rem;
      padding-bottom: 4rem;
      background: linear-gradient(
        135deg,
        rgba(74, 144, 226, 0.03) 0%,
        rgba(232, 159, 95, 0.03) 100%
      );
    }

    .slideshow {
      border-radius: 18px;
      background: #ffffff;
      box-shadow: 0 10px 40px rgba(0, 0, 0, 0.08);
      overflow: hidden;
    }

    .slide {
      display: none;
      padding: 2.5rem 2.5rem 2.1rem;
      gap: 2.4rem;
      align-items: center;
    }

    .slide.active {
      display: grid;
      grid-template-columns: minmax(0, 1fr) minmax(0, 1.5fr);
    }

    .slide-text h2 {
      font-size: 2rem;
      margin: 0 0 0.5rem;
      color: var(--dark-navy);
    }

    .slide-text .highlight-orange {
      color: var(--accent-orange);
    }

    .slide-text .subtitle {
      font-size: 1.05rem;
      color: var(--text-light);
      margin: 0 0 1.5rem;
      font-weight: 500;
    }

    .how-points {
      display: flex;
      flex-direction: column;
      gap: 0.9rem;
      margin-bottom: 1.5rem;
    }

    .how-point {
      display: flex;
      gap: 0.8rem;
      padding: 0.9rem 1rem;
      border-radius: 12px;
      background: linear-gradient(
        135deg,
        rgba(74, 144, 226, 0.04) 0%,
        rgba(232, 159, 95, 0.04) 100%
      );
    }

    .point-icon {
      flex-shrink: 0;
      font-size: 1.3rem;
    }

    .point-text h4 {
      margin: 0 0 0.2rem;
      font-size: 0.98rem;
      color: var(--primary-blue);
    }

    .point-text p {
      margin: 0;
      font-size: 0.9rem;
      color: var(--text-light);
    }

    .pricing-showcase {
      display: flex;
      flex-direction: column;
      gap: 0.7rem;
      margin-bottom: 1.5rem;
    }

    .pricing-row {
      display: flex;
      align-items: center;
      gap: 0.9rem;
      font-size: 0.9rem;
      color: var(--text-dark);
    }

    .pricing-label {
      flex: 0 0 160px;
      font-weight: 500;
    }

    .pricing-bar-wrap {
      flex: 1;
      height: 34px;
      border-radius: 20px;
      background: rgba(0, 0, 0, 0.04);
      overflow: hidden;
      position: relative;
    }

    .pricing-bar {
      height: 100%;
      display: flex;
      align-items: center;
      justify-content: flex-end;
      padding-right: 0.75rem;
      font-size: 0.85rem;
      color: #ffffff;
      font-weight: 600;
      transition: width 1.2s ease;
    }

    .pricing-bar.traditional {
      background: linear-gradient(
        90deg,
        rgba(255, 107, 107, 0.75) 0%,
        rgba(255, 107, 107, 0.9) 100%
      );
    }

    .pricing-bar.otocinclus {
      background: var(--gradient-secondary);
    }

    .slide-cta {
      display: flex;
      flex-wrap: wrap;
      gap: 0.9rem;
      margin-top: 0.5rem;
    }

    .slideshow-controls {
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 1.2rem;
      padding: 0.9rem 1.2rem 1.4rem;
      background: linear-gradient(
        135deg,
        rgba(74, 144, 226, 0.05) 0%,
        rgba(232, 159, 95, 0.05) 100%
      );
    }

    .slide-btn {
      width: 36px;
      height: 36px;
      border-radius: 50%;
      border: 2px solid var(--primary-blue);
      background: #ffffff;
      color: var(--primary-blue);
      cursor: pointer;
      font-size: 1.2rem;
      display: flex;
      align-items: center;
      justify-content: center;
      transition: all 0.2s ease;
    }

    .slide-btn:hover {
      background: var(--primary-blue);
      color: #ffffff;
      transform: scale(1.06);
    }

    .dots {
      display: flex;
      gap: 0.5rem;
    }

    .dot {
      width: 10px;
      height: 10px;
      border-radius: 999px;
      background: rgba(74, 144, 226, 0.35);
      cursor: pointer;
      transition: all 0.2s ease;
    }

    .dot.active {
      width: 26px;
      background: var(--primary-blue);
    }

    /* ------------------------------
       Admin Trap
    ------------------------------ */
    .admin-trap {
      background: #ffffff;
    }

    .admin-grid {
      display: grid;
      grid-template-columns: minmax(0, 1.1fr) minmax(0, 1.1fr);
      gap: 2.5rem;
      align-items: start;
    }

    .trap-visual {
      border-radius: 18px;
      padding: 2rem;
      background: linear-gradient(
        135deg,
        rgba(74, 144, 226, 0.06) 0%,
        rgba(232, 159, 95, 0.08) 100%
      );
    }

    .trap-points {
      display: flex;
      flex-direction: column;
      gap: 1.1rem;
    }

    .trap-point {
      background: var(--light-bg);
      border-left: 4px solid var(--primary-blue);
      border-radius: 12px;
      padding: 1rem 1.25rem;
    }

    .trap-point h4 {
      margin: 0 0 0.25rem;
      color: var(--primary-blue);
      font-size: 1rem;
    }

    .trap-point p {
      margin: 0;
      font-size: 0.92rem;
      color: var(--text-light);
    }

    /* ------------------------------
       Services
    ------------------------------ */
    .services {
      background: var(--light-bg);
    }

    .services-grid {
      display: grid;
      grid-template-columns: repeat(3, minmax(0, 1fr));
      gap: 1.7rem;
    }

    .service-card {
      background: #ffffff;
      border-radius: 18px;
      padding: 1.8rem 1.6rem 1.8rem;
      box-shadow: 0 6px 24px rgba(0, 0, 0, 0.06);
      display: flex;
      flex-direction: column;
      gap: 0.6rem;
    }

    .service-card h3 {
      margin: 0;
      font-size: 1.15rem;
      color: var(--dark-navy);
    }

    .service-card p {
      margin: 0;
      font-size: 0.92rem;
      color: var(--text-light);
    }

    .service-card ul {
      margin: 0.6rem 0 0;
      padding-left: 1.1rem;
      font-size: 0.9rem;
      color: var(--text-light);
    }

    .service-card li + li {
      margin-top: 0.3rem;
    }

    /* ------------------------------
       Engagement Models (tabs)
    ------------------------------ */
    .models {
      background: #ffffff;
    }

    .model-tabs {
      display: flex;
      flex-wrap: wrap;
      gap: 1rem;
      justify-content: center;
      margin-bottom: 2.5rem;
    }

    .tab-btn {
      border-radius: 999px;
      padding: 0.8rem 1.8rem;
      border: 2px solid transparent;
      background: var(--light-bg);
      cursor: pointer;
      font-size: 0.98rem;
      font-weight: 600;
      color: var(--text-dark);
    }

    .tab-btn.active {
      background: var(--gradient-primary);
      color: #ffffff;
      box-shadow: 0 6px 20px rgba(74, 144, 226, 0.35);
    }

    .model-panel {
      display: none;
      border-radius: 18px;
      background: linear-gradient(
        135deg,
        rgba(74, 144, 226, 0.04) 0%,
        rgba(232, 159, 95, 0.05) 100%
      );
      padding: 2.2rem 2rem;
    }

    .model-panel.active {
      display: block;
    }

    .model-panel h3 {
      margin: 0 0 0.6rem;
      font-size: 1.5rem;
      color: var(--dark-navy);
    }

    .model-panel p {
      margin: 0 0 1.6rem;
      font-size: 0.98rem;
      color: var(--text-light);
    }

    .model-flow {
      display: flex;
      flex-wrap: wrap;
      gap: 0.9rem;
      margin-bottom: 1.6rem;
    }

    .flow-step {
      flex: 1 1 130px;
      background: #ffffff;
      border-radius: 12px;
      padding: 0.9rem 1rem;
      text-align: center;
      box-shadow: 0 4px 18px rgba(0, 0, 0, 0.06);
      font-size: 0.86rem;
    }

    .flow-step h4 {
      margin: 0 0 0.25rem;
      color: var(--primary-blue);
      font-size: 0.9rem;
    }

    .model-columns {
      display: grid;
      grid-template-columns: repeat(3, minmax(0, 1fr));
      gap: 1.3rem;
      margin-bottom: 1.6rem;
    }

    .feature-box {
      background: #ffffff;
      border-radius: 12px;
      padding: 1.1rem 1rem;
      font-size: 0.9rem;
      color: var(--text-light);
    }

    .feature-box h4 {
      margin: 0 0 0.4rem;
      color: var(--dark-navy);
      font-size: 0.98rem;
    }

    .feature-box ul {
      margin: 0.3rem 0 0;
      padding-left: 1.1rem;
    }

    .feature-box li + li {
      margin-top: 0.25rem;
    }

    .model-outcome {
      margin-top: 0.6rem;
      text-align: center;
      padding: 1.2rem 1rem;
      border-radius: 12px;
      background: #ffffff;
      font-size: 0.96rem;
      color: var(--text-light);
    }

    /* ------------------------------
       Recruitment
    ------------------------------ */
    .recruitment {
      background: var(--gradient-primary);
      color: #ffffff;
    }

    .recruitment .section-title h2,
    .recruitment .section-title p {
      color: #ffffff;
    }

    .recruitment-grid {
      display: grid;
      grid-template-columns: minmax(0, 1.1fr) minmax(0, 1.1fr);
      gap: 2.5rem;
      align-items: start;
    }

    .comparison-card {
      border-radius: 18px;
      padding: 2rem;
      background: rgba(255, 255, 255, 0.12);
      backdrop-filter: blur(8px);
    }

    .comparison-card h3 {
      margin: 0 0 1.2rem;
      font-size: 1.4rem;
    }

    .comparison-row {
      display: flex;
      justify-content: space-between;
      gap: 1rem;
      border-bottom: 1px solid rgba(255, 255, 255, 0.22);
      padding: 0.6rem 0;
      font-size: 0.94rem;
    }

    .comparison-row:last-child {
      border-bottom: none;
      padding-top: 1rem;
      margin-top: 0.6rem;
      border-top: 2px solid rgba(255, 255, 255, 0.4);
      font-size: 1.05rem;
      font-weight: 600;
    }

    .recruitment-benefits {
      display: flex;
      flex-direction: column;
      gap: 1rem;
    }

    .benefit {
      border-radius: 14px;
      padding: 1rem 1.2rem;
      background: rgba(255, 255, 255, 0.15);
      font-size: 0.94rem;
    }

    .benefit h4 {
      margin: 0 0 0.4rem;
      font-size: 1rem;
      color: #ffffff;
    }

    .benefit p {
      margin: 0;
      opacity: 0.96;
    }

    /* ------------------------------
       Case Studies
    ------------------------------ */
    .case-studies {
      background: var(--light-bg);
    }

    .case-grid {
      display: grid;
      grid-template-columns: minmax(0, 1fr);
      gap: 1.8rem;
    }

    .case-card {
      border-radius: 18px;
      background: #ffffff;
      padding: 1.8rem 1.6rem;
      box-shadow: 0 8px 28px rgba(0, 0, 0, 0.06);
    }

    .case-header {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      gap: 1rem;
      margin-bottom: 1.1rem;
    }

    .case-header h3 {
      margin: 0 0 0.3rem;
      font-size: 1.1rem;
      color: var(--dark-navy);
    }

    .case-header p {
      margin: 0;
      font-size: 0.9rem;
      color: var(--text-light);
    }

    .case-metrics {
      display: flex;
      flex-wrap: wrap;
      gap: 1.1rem;
      font-size: 0.86rem;
    }

    .metric {
      text-align: center;
      min-width: 90px;
    }

    .metric strong {
      display: block;
      font-size: 1.2rem;
      color: var(--primary-blue);
    }

    .case-body p {
      margin: 0.4rem 0 0;
      font-size: 0.9rem;
      color: var(--text-light);
    }

    /* ------------------------------
       Contact
    ------------------------------ */
    .contact {
      background: #ffffff;
    }

    .contact-grid {
      display: grid;
      grid-template-columns: minmax(0, 1.1fr) minmax(0, 1.1fr);
      gap: 2.5rem;
    }

    .contact-info h3 {
      margin: 0 0 0.7rem;
      font-size: 1.4rem;
      color: var(--dark-navy);
    }

    .contact-info p {
      margin: 0 0 1.4rem;
      font-size: 0.98rem;
      color: var(--text-light);
    }

    .contact-details {
      display: flex;
      flex-direction: column;
      gap: 0.7rem;
      font-size: 0.95rem;
      color: var(--text-dark);
    }

    .contact-card {
      background: var(--light-bg);
      border-radius: 14px;
      padding: 0.9rem 1rem;
    }

    .contact-form {
      border-radius: 18px;
      background: var(--light-bg);
      padding: 1.8rem 1.6rem;
    }

    .form-group {
      margin-bottom: 1rem;
    }

    .form-group label {
      display: block;
      margin-bottom: 0.35rem;
      font-weight: 600;
      font-size: 0.9rem;
      color: var(--dark-navy);
    }

    .form-group input,
    .form-group select,
    .form-group textarea {
      width: 100%;
      border-radius: 10px;
      border: 1px solid #e2e8f0;
      padding: 0.75rem 0.8rem;
      font-family: inherit;
      font-size: 0.95rem;
      transition: border-color 0.2s ease, box-shadow 0.2s ease;
      background: #ffffff;
    }

    .form-group textarea {
      min-height: 120px;
      resize: vertical;
    }

    .form-group input:focus,
    .form-group select:focus,
    .form-group textarea:focus {
      outline: none;
      border-color: var(--primary-blue);
      box-shadow: 0 0 0 1px rgba(74, 144, 226, 0.35);
    }

    .submit-btn {
      width: 100%;
      border-radius: 999px;
      border: none;
      padding: 0.9rem 1.2rem;
      font-size: 1rem;
      font-weight: 600;
      cursor: pointer;
      background: var(--gradient-primary);
      color: #ffffff;
      box-shadow: 0 7px 20px rgba(74, 144, 226, 0.4);
    }

    .submit-btn:hover {
      transform: translateY(-1px);
      box-shadow: 0 9px 28px rgba(74, 144, 226, 0.48);
    }

    /* ------------------------------
       Footer
    ------------------------------ */
    footer {
      background: var(--dark-navy);
      color: #ffffff;
      padding: 2.8rem 0 2rem;
    }

    .footer-grid {
      display: grid;
      grid-template-columns: repeat(3, minmax(0, 1fr));
      gap: 1.8rem;
      margin-bottom: 1.8rem;
      font-size: 0.9rem;
    }

    .footer-grid h4 {
      margin: 0 0 0.7rem;
      font-size: 1rem;
    }

    .footer-grid p {
      margin: 0;
      opacity: 0.8;
    }

    .footer-list {
      list-style: none;
      padding: 0;
      margin: 0;
    }

    .footer-list li + li {
      margin-top: 0.4rem;
    }

    .footer-list a {
      text-decoration: none;
      color: #ffffff;
      opacity: 0.8;
    }

    .footer-list a:hover {
      opacity: 1;
    }

    .footer-bottom {
      border-top: 1px solid rgba(255, 255, 255, 0.2);
      padding-top: 0.9rem;
      text-align: center;
      font-size: 0.86rem;
      opacity: 0.8;
    }

    /* ------------------------------
       Scroll animations
    ------------------------------ */
    .fade-in {
      opacity: 0;
      transform: translateY(24px);
      transition: opacity 0.6s ease, transform 0.6s ease;
    }

    .fade-in.visible {
      opacity: 1;
      transform: translateY(0);
    }

    /* ------------------------------
       Keyframes
    ------------------------------ */
    @keyframes logoFloat {
      0%,
      100% {
        transform: translateY(0);
      }
      50% {
        transform: translateY(-6px);
      }
    }

    /* ------------------------------
       Responsive
    ------------------------------ */
    @media (max-width: 1024px) {
      .hero-inner {
        grid-template-columns: minmax(0, 1.1fr) minmax(0, 1fr);
      }
      .services-grid {
        grid-template-columns: repeat(2, minmax(0, 1fr));
      }
      .model-columns {
        grid-template-columns: repeat(2, minmax(0, 1fr));
      }
      .stats-grid {
        grid-template-columns: repeat(2, minmax(0, 1fr));
      }
    }

    @media (max-width: 900px) {
      .nav-links {
        position: fixed;
        top: var(--nav-height);
        right: 0;
        left: 0;
        background: #ffffff;
        flex-direction: column;
        padding: 1rem 1.5rem 1.5rem;
        transform: translateY(-120%);
        opacity: 0;
        pointer-events: none;
        transition: transform 0.28s ease, opacity 0.28s ease;
      }

      .nav-links.open {
        transform: translateY(0);
        opacity: 1;
        pointer-events: auto;
      }

      .mobile-toggle {
        display: flex;
      }

      .hero-inner {
        grid-template-columns: minmax(0, 1fr);
      }

      .hero-right {
        order: -1;
      }

      .slide.active {
        grid-template-columns: minmax(0, 1fr);
      }

      .admin-grid,
      .recruitment-grid,
      .contact-grid {
        grid-template-columns: minmax(0, 1fr);
      }

      .footer-grid {
        grid-template-columns: repeat(2, minmax(0, 1fr));
      }
    }

    @media (max-width: 640px) {
      .hero h2 {
        font-size: 2.2rem;
      }

      .section-title h2 {
        font-size: 2rem;
      }

      .services-grid {
        grid-template-columns: minmax(0, 1fr);
      }

      .model-columns {
        grid-template-columns: minmax(0, 1fr);
      }

      .stats-grid {
        grid-template-columns: minmax(0, 1fr);
      }

      .footer-grid {
        grid-template-columns: minmax(0, 1fr);
      }

      .slide {
        padding: 2rem 1.6rem 1.6rem;
      }
    }
  </style>
</head>

<body>
  <!-- Navigation -->
  <nav id="navbar">
    <div class="container nav-inner">
      <div class="logo-wrap">
        <div class="logo-circle">O</div>
        <div class="logo-text">
          <h1>OTOCINCLUS</h1>
          <p>HR & HRMS Infrastructure</p>
        </div>
      </div>

      <ul class="nav-links" id="navLinks">
        <li><a href="#home">Home</a></li>
        <li><a href="#services">Services</a></li>
        <li><a href="#models">Engagement Models</a></li>
        <li><a href="#recruitment">Recruitment</a></li>
        <li><a href="#case-studies">Case Studies</a></li>
        <li><a href="#contact">Contact</a></li>
        <li>
          <a href="#contact" class="nav-cta">Schedule Free Audit</a>
        </li>
      </ul>

      <div class="mobile-toggle" id="mobileToggle" aria-label="Toggle navigation">
        <span></span><span></span><span></span>
      </div>
    </div>
  </nav>

  <!-- Hero -->
  <section class="hero" id="home">
    <div class="container hero-inner">
      <div class="hero-left fade-in">
        <h2>
          We Remove the <span class="highlight">Admin Trap</span>
        </h2>
        <p class="tagline">Audit. Advise. Implement. Transfer.</p>
        <p class="lead">
          Otocinclus is your HR consultancy and HRMS implementation partner for
          India's growing businesses. We build professional HR systems, operate
          them flawlessly, and transfer them to your team when you're ready.
        </p>

        <div class="hero-buttons">
          <a href="#contact" class="btn-primary">Schedule Consultation</a>
          <a href="#services" class="btn-secondary">Explore Services</a>
        </div>

        <div class="hero-badges">
          <span class="hero-badge">HR Governance & Policy</span>
          <span class="hero-badge">HRMS Implementation</span>
          <span class="hero-badge">Payroll & Compliance</span>
          <span class="hero-badge">Flat 7% Recruitment</span>
        </div>
      </div>

      <div class="hero-right fade-in">
        <div class="floating-card">
          <h3>Build-Operate-Transfer Model</h3>
          <p>
            We build your HR infrastructure, operate it seamlessly, then hand
            over to your internal HR team with complete documentation.
          </p>
        </div>
        <div class="floating-card">
          <h3>Vendor-Agnostic HRMS</h3>
          <p>
            Expert implementation of Keka, GreytHR, Zoho, Darwinbox and more.
            We help you select, configure, and operate the right system.
          </p>
        </div>
        <div class="floating-card">
          <h3>Flat 7% Recruitment – All Levels</h3>
          <p>
            Industry-disrupting recruitment pricing. Save 30–65% on senior hires
            versus traditional agencies, without compromising on quality.
          </p>
        </div>
      </div>
    </div>
  </section>

  <!-- Stats -->
  <section class="stats">
    <div class="container stats-grid fade-in">
      <div class="stat-item">
        <h3>30–65%</h3>
        <p>Cost savings vs. traditional recruitment agencies</p>
      </div>
      <div class="stat-item">
        <h3>20</h3>
        <p>Founder hours reclaimed every month</p>
      </div>
      <div class="stat-item">
        <h3>28</h3>
        <p>Average time-to-hire (days)</p>
      </div>
      <div class="stat-item">
        <h3>99.5%</h3>
        <p>Payroll accuracy target</p>
      </div>
    </div>
  </section>

  <!-- Core Value Propositions (Slideshow) -->
  <section class="core-values">
    <div class="container">
      <div class="section-title fade-in">
        <h2>How We Free You from HR Chaos</h2>
        <p>
          From policy design to HRMS operations and recruitment, we deliver a
          unified HR infrastructure that founders can trust.
        </p>
      </div>

      <div class="slideshow fade-in" id="slideshow">
        <!-- Slide 1: Admin Trap -->
        <div class="slide active">
          <div class="slide-text">
            <h2>
              We Remove the
              <span class="highlight-orange">Admin Trap</span>
            </h2>
            <p class="subtitle">
              Professional HR infrastructure so founders stop firefighting and
              focus on growth.
            </p>

            <div class="how-points">
              <div class="how-point">
                <div class="point-icon">✅</div>
                <div class="point-text">
                  <h4>Complete HR Infrastructure Setup</h4>
                  <p>
                    HR policies, HRMS, and compliance frameworks built from
                    scratch to support scale.
                  </p>
                </div>
              </div>
              <div class="how-point">
                <div class="point-icon">⚙️</div>
                <div class="point-text">
                  <h4>End-to-End Operations</h4>
                  <p>
                    Monthly payroll, statutory compliance, attendance, leave,
                    and lifecycle operations handled for you.
                  </p>
                </div>
              </div>
              <div class="how-point">
                <div class="point-icon">🛡️</div>
                <div class="point-text">
                  <h4>Zero Compliance Risk</h4>
                  <p>
                    Maker-checker processes, automated compliance calendars,
                    and professional indemnity coverage.
                  </p>
                </div>
              </div>
              <div class="how-point">
                <div class="point-icon">🔁</div>
                <div class="point-text">
                  <h4>Build-Operate-Transfer</h4>
                  <p>
                    We run the function till it is stable, then transfer
                    complete ownership to your internal team.
                  </p>
                </div>
              </div>
            </div>

            <div class="slide-cta">
              <a href="#admin-trap" class="btn-secondary">See the Admin Trap</a>
            </div>
          </div>

          <div>
            <strong>Growing businesses, 15–100 employees:</strong>
            <p style="margin-top:0.4rem; font-size:0.92rem; color:var(--text-light);">
              Too large for spreadsheets. Too early for a VP of HR. Too risky to
              ignore compliance. Otocinclus bridges this gap with a
              full-stack HR engine.
            </p>
          </div>
        </div>

        <!-- Slide 2: Flat 7 Recruitment -->
        <div class="slide">
          <div class="slide-text">
            <h2>
              <span class="highlight-orange">Flat 7% Recruitment</span> for All
              Levels
            </h2>
            <p class="subtitle">
              We eliminate the “leadership penalty” charged by traditional
              agencies and keep your costs predictable.
            </p>

            <div class="pricing-showcase">
              <div class="pricing-row">
                <span class="pricing-label">Traditional – Juniors</span>
                <div class="pricing-bar-wrap">
                  <div class="pricing-bar traditional" style="width: 45%">
                    8.33%
                  </div>
                </div>
              </div>
              <div class="pricing-row">
                <span class="pricing-label">Traditional – Mid</span>
                <div class="pricing-bar-wrap">
                  <div class="pricing-bar traditional" style="width: 70%">
                    12–15%
                  </div>
                </div>
              </div>
              <div class="pricing-row">
                <span class="pricing-label">Traditional – Senior</span>
                <div class="pricing-bar-wrap">
                  <div class="pricing-bar traditional" style="width: 100%">
                    20%+
                  </div>
                </div>
              </div>
              <div class="pricing-row">
                <span class="pricing-label"><strong>Otocinclus – All Levels</strong></span>
                <div class="pricing-bar-wrap">
                  <div class="pricing-bar otocinclus" style="width: 35%">
                    7% Flat
                  </div>
                </div>
              </div>
            </div>

            <p style="font-size:0.9rem; color:var(--text-light); margin-bottom:1rem;">
              Same quality sourcing, screening, coordination, and negotiation
              across junior, mid, and senior hires. 90‑day free replacement
              included.
            </p>

            <div class="slide-cta">
              <a href="#recruitment" class="btn-primary">View Recruitment Model</a>
            </div>
          </div>

          <div>
            <strong>Impact on your hiring budget:</strong>
            <p style="margin-top:0.4rem; font-size:0.92rem; color:var(--text-light);">
              Traditional agencies charge 20%+ for leadership roles. Flat 7%
              from Otocinclus can save ₹12L+ across a handful of senior hires,
              while integrating tightly with your HR and payroll operations.
            </p>
          </div>
        </div>

        <!-- Slideshow controls -->
        <div class="slideshow-controls">
          <button class="slide-btn" id="prevSlide" aria-label="Previous slide">
            ‹
          </button>
          <div class="dots">
            <div class="dot active" data-slide="0"></div>
            <div class="dot" data-slide="1"></div>
          </div>
          <button class="slide-btn" id="nextSlide" aria-label="Next slide">
            ›
          </button>
        </div>
      </div>
    </div>
  </section>

  <!-- Admin Trap -->
  <section class="admin-trap" id="admin-trap">
    <div class="container">
      <div class="section-title fade-in">
        <h2>The Admin Trap: Where Growth Stalls</h2>
        <p>
          Between 15–100 employees, founders start losing 20+ hours a month to
          HR admin, while compliance and people experience suffer quietly in
          the background.
        </p>
      </div>

      <div class="admin-grid fade-in">
        <div class="trap-visual">
          <h3 style="margin-top:0; margin-bottom:0.5rem;">Administrative Complexity vs. Headcount</h3>
          <p style="margin-top:0; font-size:0.9rem; color:var(--text-light);">
            Complexity increases non‑linearly as you grow: more employees,
            multiple locations, new statutes, and rising expectations.
          </p>
          <ul style="margin:0.6rem 0 0; padding-left:1.1rem; font-size:0.9rem; color:var(--text-light);">
            <li>15–30 employees: spreadsheets become fragile; manual payroll risks errors.</li>
            <li>30–60 employees: compliance filings and audits intensify.</li>
            <li>60–100 employees: investor due diligence and employer branding start to matter.</li>
          </ul>
        </div>

        <div class="trap-points">
          <div class="trap-point">
            <h4>Time Drain</h4>
            <p>
              Founders and CXOs spend 15–25 hours per week on HR administration
              — almost 25% of strategic capacity lost.
            </p>
          </div>
          <div class="trap-point">
            <h4>Compliance Risk</h4>
            <p>
              New Social Security Code and labour regulations bring penalties,
              interest, and even imprisonment. Ignorance is not protection.
            </p>
          </div>
          <div class="trap-point">
            <h4>Financial Loss</h4>
            <p>
              30–40% higher effective HR costs due to errors, delays, penalties,
              and missed opportunities to optimise structure.
            </p>
          </div>
          <div class="trap-point">
            <h4>Strategic Impact</h4>
            <p>
              Weak HR infrastructure blocks investor readiness, damages employer
              brand, and slows down hiring velocity exactly when you need
              momentum.
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Services -->
  <section class="services" id="services">
    <div class="container">
      <div class="section-title fade-in">
        <h2>Comprehensive HR Infrastructure Services</h2>
        <p>
          Full-stack HR and HRMS services designed for growing businesses. We
          handle the engine room so you can focus on customers and product.
        </p>
      </div>

      <div class="services-grid fade-in">
        <div class="service-card">
          <h3>HR Governance & Policy Design</h3>
          <p>
            Compliant, scalable HR foundations with professionally designed
            policies and frameworks.
          </p>
          <ul>
            <li>HR policy & employee handbook</li>
            <li>Org structure & role definitions</li>
            <li>HR process mapping & SOPs</li>
            <li>Compliance framework (PF, ESI, PT, labour laws)</li>
          </ul>
        </div>

        <div class="service-card">
          <h3>HRMS Selection, Implementation & Admin</h3>
          <p>
            Vendor-agnostic HRMS implementation and daily administration,
            integrated with your workflows.
          </p>
          <ul>
            <li>HRMS selection & fitment advisory</li>
            <li>Configuration: payroll, attendance, leave</li>
            <li>Data migration from legacy systems</li>
            <li>Ongoing HRMS administration & support</li>
            <li>HRMS training for your internal team</li>
          </ul>
        </div>

        <div class="service-card">
          <h3>Payroll & Statutory Compliance</h3>
          <p>
            Accurate, timely payroll with maker-checker and robust compliance
            controls.
          </p>
          <ul>
            <li>Monthly payroll processing & payslips</li>
            <li>PF, ESI, PT, TDS deductions & filings</li>
            <li>Statutory returns and challans</li>
            <li>Full & final settlements</li>
            <li>Payroll MIS & analytics</li>
          </ul>
        </div>

        <div class="service-card">
          <h3>Attendance, Leave & Time Management</h3>
          <p>
            Automated attendance tracking with clear, well-communicated rules
            and governance.
          </p>
          <ul>
            <li>Shift rules and attendance logic</li>
            <li>Leave policy design & automation</li>
            <li>Monthly attendance reconciliation</li>
            <li>Dashboards for managers & founders</li>
          </ul>
        </div>

        <div class="service-card">
          <h3>Employee Lifecycle Management</h3>
          <p>
            Seamless employee journey from offer to exit, backed by clean
            documentation.
          </p>
          <ul>
            <li>Onboarding documentation & KYC</li>
            <li>Digital employee records management</li>
            <li>Probation & confirmation tracking</li>
            <li>Appraisal cycle coordination</li>
            <li>Exit, NOC, and F&F processes</li>
          </ul>
        </div>

        <div class="service-card">
          <h3>Capability Building & Handover</h3>
          <p>
            We train your internal HR team to own a professionally set-up
            function.
          </p>
          <ul>
            <li>HRMS admin training for internal HR</li>
            <li>Payroll & compliance training</li>
            <li>Process walkthroughs with SOP handover</li>
            <li>Post-handover support as required</li>
          </ul>
        </div>
      </div>
    </div>
  </section>

  <!-- Engagement Models -->
  <section class="models" id="models">
    <div class="container">
      <div class="section-title fade-in">
        <h2>Engagement Models for Your Growth Stage</h2>
        <p>
          Whether you want fully managed HR or a build-operate-transfer model,
          choose a structure aligned to your internal capabilities.
        </p>
      </div>

      <div class="model-tabs fade-in">
        <button class="tab-btn active" data-tab="model1">Model 1 – Managed HR Services</button>
        <button class="tab-btn" data-tab="model2">Model 2 – Build-Operate-Transfer</button>
      </div>

      <!-- Model 1 -->
      <div class="model-panel active fade-in" id="model1">
        <h3>Model 1 – Complete Outsourced HR (Managed HR)</h3>
        <p>
          Best for companies that want us to handle everything. We act as your
          extended HR department with a per-employee subscription model.
        </p>

        <div class="model-flow">
          <div class="flow-step">
            <h4>Start</h4>
            <p>Discovery & scoping</p>
          </div>
          <div class="flow-step">
            <h4>Audit</h4>
            <p>Gap & risk analysis</p>
          </div>
          <div class="flow-step">
            <h4>Setup</h4>
            <p>Policies, HRMS, compliance</p>
          </div>
          <div class="flow-step">
            <h4>Operate</h4>
            <p>Ongoing HR operations</p>
          </div>
        </div>

        <div class="model-columns">
          <div class="feature-box">
            <h4>HR Policy & Process Setup</h4>
            <ul>
              <li>HR policies & employee handbook</li>
              <li>Org structure & role clarity</li>
              <li>Process mapping & documentation</li>
              <li>Compliance framework implementation</li>
            </ul>
          </div>
          <div class="feature-box">
            <h4>HRMS Implementation & Management</h4>
            <ul>
              <li>System selection & configuration</li>
              <li>Employee data setup & migration</li>
              <li>Ongoing system administration</li>
              <li>Issue resolution & enhancements</li>
            </ul>
          </div>
          <div class="feature-box">
            <h4>Payroll, Compliance & Lifecycle</h4>
            <ul>
              <li>Payroll & statutory filings</li>
              <li>Attendance & leave administration</li>
              <li>Onboarding, confirmation, exit</li>
              <li>HR MIS & founder dashboards</li>
            </ul>
          </div>
        </div>

        <div class="model-outcome">
          Get a fully functional HR department without hiring an internal HR
          team. Predictable monthly costs with enterprise-grade HR
          infrastructure built-in.
        </div>
      </div>

      <!-- Model 2 -->
      <div class="model-panel fade-in" id="model2">
        <h3>Model 2 – HR Setup & Transition to Internal HR</h3>
        <p>
          Best for companies planning to build an internal HR team. We set up,
          stabilise, then hand over a ready-to-run HR engine to your hires.
        </p>

        <div class="model-flow">
          <div class="flow-step">
            <h4>Phase 1</h4>
            <p>HR setup & HRMS implementation</p>
          </div>
          <div class="flow-step">
            <h4>Phase 2</h4>
            <p>Initial operations (2–3 months)</p>
          </div>
          <div class="flow-step">
            <h4>Phase 3</h4>
            <p>Training & handover</p>
          </div>
        </div>

        <div class="model-columns">
          <div class="feature-box">
            <h4>Phase 1 – Build</h4>
            <ul>
              <li>Policy & handbook creation</li>
              <li>Compliance & statutory setup</li>
              <li>HRMS implementation & config</li>
              <li>Payroll / attendance / leave setup</li>
              <li>SOP & process documentation</li>
            </ul>
          </div>
          <div class="feature-box">
            <h4>Phase 2 – Operate</h4>
            <ul>
              <li>Run payroll & compliance filings</li>
              <li>Administer HRMS & attendance</li>
              <li>Lifecycle support end-to-end</li>
              <li>Stabilise systems & fix issues</li>
            </ul>
          </div>
          <div class="feature-box">
            <h4>Phase 3 – Transfer</h4>
            <ul>
              <li>Train internal HR on systems</li>
              <li>Payroll & compliance training</li>
              <li>SOP walkthroughs & Q&A</li>
              <li>Post-handover support as needed</li>
            </ul>
          </div>
        </div>

        <div class="model-outcome">
          Your internal HR team inherits a professionally built, fully
          operational HR system with clean documentation, training, and
          optional ongoing support.
        </div>
      </div>
    </div>
  </section>

  <!-- Recruitment -->
  <section class="recruitment" id="recruitment">
    <div class="container">
      <div class="section-title fade-in">
        <h2>Recruitment Services – Flat 7% Across Levels</h2>
        <p>
          We remove the leadership premium charged by traditional agencies and
          align recruitment economics with your long-term growth.
        </p>
      </div>

      <div class="recruitment-grid fade-in">
        <div class="comparison-card">
          <h3>Pricing Comparison</h3>
          <div class="comparison-row">
            <span>Traditional Agency – Junior</span>
            <span>8.33%</span>
          </div>
          <div class="comparison-row">
            <span>Traditional Agency – Mid</span>
            <span>12–15%</span>
          </div>
          <div class="comparison-row">
            <span>Traditional Agency – Senior</span>
            <span>20%+</span>
          </div>
          <div class="comparison-row">
            <span>Otocinclus – All Levels</span>
            <span style="color:#e89f5f;">7% Flat</span>
          </div>
        </div>

        <div class="recruitment-benefits">
          <div class="benefit">
            <h4>End-to-End Talent Acquisition</h4>
            <p>
              Requirement understanding, JD creation, sourcing, screening,
              coordination, offer negotiation, joining coordination, and 90‑day
              free replacement.
            </p>
          </div>
          <div class="benefit">
            <h4>Faster, Aligned Hiring</h4>
            <p>
              28‑day average time-to-hire (vs. 45‑day market norm). Integrated
              with HR & payroll operations for seamless onboarding and Day 1
              readiness.
            </p>
          </div>
          <div class="benefit">
            <h4>Long-Term Partnership</h4>
            <p>
              Recruitment can continue even after HR has been handed over in
              Model 2, giving you a stable, long-term talent acquisition
              partner.
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Case Studies -->
  <section class="case-studies" id="case-studies">
    <div class="container">
      <div class="section-title fade-in">
        <h2>Case Studies</h2>
        <p>
          How we've helped growing businesses break free from the Admin Trap,
          clean up compliance, and scale confidently.
        </p>
      </div>

      <div class="case-grid fade-in">
        <div class="case-card">
          <div class="case-header">
            <div>
              <h3>B2B SaaS – Scaling 15 to 45 Employees in 8 Months</h3>
              <p>Industry: SaaS | Model: Managed HR Services (Model 1)</p>
            </div>
            <div class="case-metrics">
              <div class="metric">
                <strong>25+</strong>
                <span>Founder hours saved per week</span>
              </div>
              <div class="metric">
                <strong>0</strong>
                <span>Compliance issues in due diligence</span>
              </div>
              <div class="metric">
                <strong>99.5%</strong>
                <span>Payroll accuracy achieved</span>
              </div>
            </div>
          </div>
          <div class="case-body">
            <p>
              Founder was spending 25+ hours weekly on HR using spreadsheets.
              Rapid hiring created compliance risks and blocked Series A
              discussions. We implemented Managed HR Services, set up GreytHR
              with full payroll configuration, and built a compliance framework
              for PF, ESI, and PT. 30 new employees were onboarded seamlessly,
              resulting in clean HR due diligence for Series A.
            </p>
          </div>
        </div>

        <div class="case-card">
          <div class="case-header">
            <div>
              <h3>Manufacturing – Transition to Internal HR Team</h3>
              <p>Industry: Manufacturing | Model: Build-Operate-Transfer (Model 2)</p>
            </div>
            <div class="case-metrics">
              <div class="metric">
                <strong>₹12L+</strong>
                <span>Saved vs. traditional agencies</span>
              </div>
              <div class="metric">
                <strong>5</strong>
                <span>Senior hires at flat 7%</span>
              </div>
              <div class="metric">
                <strong>100%</strong>
                <span>Complete HR handover</span>
              </div>
            </div>
          </div>
          <div class="case-body">
            <p>
              The company wanted an internal HR team but lacked systems and
              processes. Previous agency fees were 15–20% per hire. We deployed
              Model 2: implemented Keka HRMS, ran operations for 3 months while
              they hired internal HR, then trained the new team and handed over
              SOPs. 5 senior roles were closed at flat 7%, saving ₹12L+ in
              recruitment fees.
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Contact -->
  <section class="contact" id="contact">
    <div class="container">
      <div class="section-title fade-in">
        <h2>Schedule a Free HR Infrastructure Audit</h2>
        <p>
          Share a few details and we’ll review your current HR setup, highlight
          key risks, and recommend the right engagement model for your
          business.
        </p>
      </div>

      <div class="contact-grid fade-in">
        <div class="contact-info">
          <h3>Let’s talk about your HR engine</h3>
          <p>
            We typically respond within one business day. Expect a focused,
            founder‑friendly conversation — no generic sales script.
          </p>

          <div class="contact-details">
            <div class="contact-card">
              <strong>Location</strong>
              <br />
              Bengaluru, Karnataka, India
            </div>
            <div class="contact-card">
              <strong>Email</strong>
              <br />
              contact@otocinclus.com
            </div>
            <div class="contact-card">
              <strong>Phone</strong>
              <br />
              +91 XXXXX XXXXX
            </div>
          </div>
        </div>

        <div class="contact-form">
          <form id="contactForm">
            <div class="form-group">
              <label for="name">Full Name</label>
              <input id="name" name="name" type="text" required />
            </div>

            <div class="form-group">
              <label for="email">Email Address</label>
              <input id="email" name="email" type="email" required />
            </div>

            <div class="form-group">
              <label for="phone">Phone Number</label>
              <input id="phone" name="phone" type="tel" required />
            </div>

            <div class="form-group">
              <label for="company">Company Name</label>
              <input id="company" name="company" type="text" required />
            </div>

            <div class="form-group">
              <label for="employees">Number of Employees</label>
              <select id="employees" name="employees" required>
                <option value="">Select range</option>
                <option value="1-15">1–15 employees</option>
                <option value="15-50">15–50 employees</option>
                <option value="50-100">50–100 employees</option>
                <option value="100-250">100–250 employees</option>
                <option value="250+">250+ employees</option>
              </select>
            </div>

            <div class="form-group">
              <label for="interest">Service Interest</label>
              <select id="interest" name="interest" required>
                <option value="">Select service</option>
                <option value="model1">Model 1 – Managed HR</option>
                <option value="model2">Model 2 – Build-Operate-Transfer</option>
                <option value="recruitment">Recruitment Only</option>
                <option value="hrms">HRMS Implementation</option>
                <option value="audit">HR & Compliance Audit</option>
              </select>
            </div>

            <div class="form-group">
              <label for="message">Context (optional)</label>
              <textarea
                id="message"
                name="message"
                placeholder="Share your current HR challenges or goals..."
              ></textarea>
            </div>

            <button class="submit-btn" type="submit">
              Submit & Request Audit
            </button>
          </form>
        </div>
      </div>
    </div>
  </section>

  <!-- Footer -->
  <footer>
    <div class="container">
      <div class="footer-grid">
        <div>
          <h4>Otocinclus</h4>
          <p>
            Integrated HR and HRMS infrastructure partner for India’s growing
            businesses — from 15 to 250+ employees.
          </p>
        </div>
        <div>
          <h4>Quick Links</h4>
          <ul class="footer-list">
            <li><a href="#home">Home</a></li>
            <li><a href="#services">Services</a></li>
            <li><a href="#models">Engagement Models</a></li>
            <li><a href="#recruitment">Recruitment</a></li>
            <li><a href="#case-studies">Case Studies</a></li>
          </ul>
        </div>
        <div>
          <h4>Contact</h4>
          <p>
            Bengaluru, Karnataka, India<br />
            contact@otocinclus.com<br />
            +91 XXXXX XXXXX
          </p>
        </div>
      </div>

      <div class="footer-bottom">
        © <span id="year"></span> Otocinclus. All rights reserved.
      </div>
    </div>
  </footer>

  <!-- Scripts -->
  <script>
    // Navbar scroll effect
    const navbar = document.getElementById("navbar");
    window.addEventListener("scroll", () => {
      if (window.scrollY > 40) {
        navbar.classList.add("scrolled");
      } else {
        navbar.classList.remove("scrolled");
      }
    });

    // Mobile menu toggle
    const mobileToggle = document.getElementById("mobileToggle");
    const navLinks = document.getElementById("navLinks");
    mobileToggle.addEventListener("click", () => {
      mobileToggle.classList.toggle("active");
      navLinks.classList.toggle("open");
    });
    navLinks.querySelectorAll("a").forEach((link) => {
      link.addEventListener("click", () => {
        navLinks.classList.remove("open");
        mobileToggle.classList.remove("active");
      });
    });

    // Smooth scroll for in-page anchor links (fallback)
    document.querySelectorAll('a[href^="#"]').forEach((anchor) => {
      anchor.addEventListener("click", function (e) {
        const targetId = this.getAttribute("href");
        const target = document.querySelector(targetId);
        if (target) {
          e.preventDefault();
          target.scrollIntoView({ behavior: "smooth", block: "start" });
        }
      });
    });

    // Scroll animations
    const observer = new IntersectionObserver(
      (entries) => {
        entries.forEach((entry) => {
          if (entry.isIntersecting) {
            entry.target.classList.add("visible");
            observer.unobserve(entry.target);
          }
        });
      },
      { threshold: 0.15 }
    );
    document.querySelectorAll(".fade-in").forEach((el) => observer.observe(el));

    // Engagement models tabs
    const tabButtons = document.querySelectorAll(".tab-btn");
    const tabPanels = document.querySelectorAll(".model-panel");
    tabButtons.forEach((btn) => {
      btn.addEventListener("click", () => {
        const target = btn.dataset.tab;
        tabButtons.forEach((b) => b.classList.remove("active"));
        tabPanels.forEach((panel) => panel.classList.remove("active"));
        btn.classList.add("active");
        document.getElementById(target).classList.add("active");
      });
    });

    // Core values slideshow
    const slides = document.querySelectorAll(".slide");
    const dots = document.querySelectorAll(".dot");
    const prevSlideBtn = document.getElementById("prevSlide");
    const nextSlideBtn = document.getElementById("nextSlide");
    let currentSlide = 0;

    function showSlide(index) {
      if (slides.length === 0) return;
      if (index < 0) index = slides.length - 1;
      if (index >= slides.length) index = 0;
      slides.forEach((s) => s.classList.remove("active"));
      dots.forEach((d) => d.classList.remove("active"));
      slides[index].classList.add("active");
      if (dots[index]) dots[index].classList.add("active");
      currentSlide = index;
    }

    prevSlideBtn.addEventListener("click", () => showSlide(currentSlide - 1));
    nextSlideBtn.addEventListener("click", () => showSlide(currentSlide + 1));
    dots.forEach((dot, idx) => {
      dot.addEventListener("click", () => showSlide(idx));
    });

    setInterval(() => {
      showSlide(currentSlide + 1);
    }, 8000);

    // Contact form (simulated submit)
    const contactForm = document.getElementById("contactForm");
    contactForm.addEventListener("submit", (e) => {
      e.preventDefault();
      alert(
        "Thank you for your interest! We will contact you within 24 hours to schedule your free HR infrastructure audit."
      );
      contactForm.reset();
    });

    // Footer year
    document.getElementById("year").textContent =
      new Date().getFullYear().toString();
  </script>
</body>
</html>

