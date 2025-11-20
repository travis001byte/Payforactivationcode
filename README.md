<!doctype html>

<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>PayforactivationCode</title>
  <meta name="description" content="Send payment to activate your code. Follow instructions and send proof to the admin/group." />
  <meta property="og:title" content="PayforactivationCode" />
  <meta property="og:description" content="Send payment to the account below and message proof to the admin/group." />
  <meta property="og:image" content="https://placehold.co/1200x630?text=PayforactivationCode" />
  <style>
    :root{--accent:#0b74de;--muted:#6b7280}
    body{font-family:Inter, ui-sans-serif, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial; margin:0; padding:20px; background:#f3f4f6; color:#111}
    .container{max-width:760px;margin:0 auto;background:#fff;border-radius:12px;padding:20px;box-shadow:0 6px 24px rgba(0,0,0,0.08)}
    header{display:flex;align-items:center;gap:12px}
    h1{margin:0;font-size:1.4rem}
    p.lead{margin:6px 0 14px;color:var(--muted)}
    .card{background:#f9fafb;padding:14px;border-radius:10px}
    .details p{margin:8px 0;font-size:1rem}
    .label{color:var(--muted);font-size:0.9rem}
    .big{font-weight:700;font-size:1.05rem}
    .actions{display:flex;gap:8px;margin-top:12px}
    .btn{padding:10px 14px;border-radius:8px;border:1px solid var(--accent);background:transparent;text-decoration:none;cursor:pointer}
    .btn-primary{background:var(--accent);color:#fff;border-color:transparent}
    .note{font-size:0.9rem;color:var(--muted);margin-top:12px}
    footer{font-size:0.85rem;color:var(--muted);text-align:center;margin-top:18px}
    pre{background:#eef2ff;padding:10px;border-radius:8px;overflow:auto}
    @media (max-width:480px){.actions{flex-direction:column}}
  </style>
</head>
<body>
  <div class="container">
    <header>
      <div style="flex:1">
        <h1>PayforactivationCode</h1>
        <p class="lead">Send your payment to the account below and share your payment proof to the admin or group.</p>
      </div>
    </header><div class="card" style="margin-top:14px">
  <div class="details">
    <p><span class="label">Provider / Bank:</span> <span class="big">MOMO PSB</span></p>
    <p><span class="label">Account name:</span> <span class="big">NANPYAL PONZING</span></p>
    <p><span class="label">Account number / Phone:</span> <span id="acct" class="big">8160976094</span></p>
    <p><span class="label">Amount:</span> <span class="big">(Enter amount during transfer)</span></p>
  </div>

  <div class="actions">
    <button class="btn" id="copyBtn">Copy details</button>
    <button class="btn btn-primary" id="copyMsgBtn">Copy payment message</button>
  </div>

  <p class="note">After payment: take a screenshot/receipt and send it to the admin/group along with your username or phone so your activation code can be issued. Do not share PINs or sensitive personal info.</p>

  <hr style="margin:14px 0;border:none;border-top:1px solid #e6eef8" />

  <h3 style="margin:0 0 8px">Quick payment message (ready-to-send)</h3>
  <pre id="paymentText">I have paid for PayforactivationCode.

Provider: MOMO PSB Account name: NANPYAL PONZING Account/Phone: 8160976094 Amount: [enter amount] Username/Phone: [your username] Transaction ID / Screenshot attached.</pre>

<p style="margin-top:10px;color:var(--muted)">Tip: After copying the payment message, paste it into the group chat or WhatsApp message and attach the payment screenshot.</p>
</div>

<footer>
  <div>If you want this page to include a direct WhatsApp link or an email contact, edit the HTML and replace the contact placeholders.</div>
  <div style="margin-top:8px">Hosted on Netlify (free) — just upload this file and you'll get a public URL.</div>
</footer>

  </div>  <script>
    const acct = document.getElementById('acct').innerText.trim();
    const copyBtn = document.getElementById('copyBtn');
    const copyMsgBtn = document.getElementById('copyMsgBtn');
    const paymentText = document.getElementById('paymentText').innerText;

    copyBtn.addEventListener('click', ()=>{
      const text = `Provider: MOMO PSB\nAccount name: NANPYAL PONZING\nAccount/Phone: ${acct}`;
      navigator.clipboard.writeText(text).then(()=>{
        copyBtn.textContent = 'Copied!';
        setTimeout(()=>copyBtn.textContent = 'Copy details',1500);
      });
    });

    copyMsgBtn.addEventListener('click', ()=>{
      navigator.clipboard.writeText(paymentText).then(()=>{
        copyMsgBtn.textContent = 'Message copied!';
        setTimeout(()=>copyMsgBtn.textContent = 'Copy payment message',1500);
      });
    });
  </script></body>
</html>
