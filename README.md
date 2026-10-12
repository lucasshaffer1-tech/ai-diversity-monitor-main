<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>TrustScan</title>
  <style>
    body{font-family:Arial,Helvetica,sans-serif;background:#f5f7f6;color:#1a1a1a;margin:0;line-height:1.6}
    .container{max-width:980px;margin:0 auto;padding:40px 20px 60px}
    .hero{background:linear-gradient(135deg,#0e2a3f,#173d57);color:#fff;border-radius:18px;padding:36px 30px;box-shadow:0 12px 30px rgba(0,0,0,.12)}
    h1{font-size:clamp(2rem,4vw,3.5rem);margin:0 0 12px;letter-spacing:-.04em}
    .lead{font-size:1.1rem;color:#dfeaf2;margin:0 0 20px;max-width:700px}
    .actions{display:flex;flex-wrap:wrap;gap:12px;margin:20px 0 10px}
    .btn{display:inline-block;padding:12px 18px;border-radius:10px;text-decoration:none;font-weight:700}
    .btn.primary{background:#1a472a;color:#fff}
    .btn.secondary{background:#fff;color:#0e2a3f;border:1px solid rgba(255,255,255,.35)}
    .section{margin-top:24px;display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:16px}
    .card{background:white;border:1px solid #dde5eb;border-radius:12px;padding:18px;box-shadow:0 5px 12px rgba(12,24,32,.04)}
    .card h2{margin:0 0 8px;font-size:1.1rem;color:#0e2a3f}
    .card p{margin:0 0 12px;color:#475569;font-size:0.96rem}
    .card a{color:#0f766e;text-decoration:none;font-weight:700}
    ul{margin:10px 0 0 18px;padding:0;color:#475569}
    footer{margin-top:24px;color:#64748b;font-size:.92rem}
  </style>
</head>
<body>
  <div class="container">
    <header class="hero">
      <h1>TrustScan</h1>
      <p class="lead">Verify true second opinions. A concept for monitoring whether hospital AI imaging tools are genuinely independent or quietly sharing the same blind spots.</p>
      <div class="actions">
        <a class="btn primary" href="../prototype.html">Open prototype</a>
        <a class="btn secondary" href="../records.html">Enter records</a>
        <a class="btn secondary" href="../docs.html">Read docs</a>
      </div>
    </header>

    <div class="section">
      <div class="card">
        <h2>Prototype</h2>
        <p>View the interactive dashboard with case alerts, tools, reports, and settings.</p>
        <a href="../prototype.html">Go to dashboard</a>
      </div>

      <div class="card">
        <h2>Enter records</h2>
        <p>Add made-up cases and see how the TrustScan rating logic reacts.</p>
        <a href="../records.html">Open records page</a>
      </div>

      <div class="card">
        <h2>Docs</h2>
        <p>Review the README, SWOT, and project notes.</p>
        <a href="../docs.html">Browse project docs</a>
      </div>
    </div>

    <div class="card" style="margin-top:24px">
      <h2>Prototype tabs</h2>
      <ul>
        <li><a href="../dashboard.html">Dashboard</a></li>
        <li><a href="../cases.html">Cases</a></li>
        <li><a href="../records.html">Records</a></li>
        <li><a href="../tools.html">Tools</a></li>
        <li><a href="../alerts.html">Alerts</a></li>
        <li><a href="../reports.html">Reports</a></li>
        <li><a href="../settings.html">Settings</a></li>
      </ul>
    </div>

    <footer>
      Sample data only. No hospital or patient information is connected to this prototype.
    </footer>
  </div>
</body>
</html>
