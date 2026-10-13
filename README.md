<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<meta name="theme-color" content="#0b0d12">
<title>NandanTrades Gold Calculator</title>
<style>
:root{color-scheme:dark;--bg:#090b10;--panel:#11151d;--panel2:#171c26;--line:#293140;--text:#f4f6fa;--muted:#9ba6b7;--gold:#e8b84b;--green:#62d6a4;--red:#ff7777}
*{box-sizing:border-box}body{margin:0;background:radial-gradient(ellipse at top,#1a1a1b 0,#090b10 55%);font:16px/1.5 system-ui,-apple-system,Segoe UI,Roboto,Arial,sans-serif;color:var(--text);min-height:100vh}
.wrap{width:min(920px,100%);margin:auto;padding:28px 18px 40px}.top{display:flex;align-items:center;gap:13px;margin-bottom:28px}.logo{width:48px;height:48px;display:grid;place-items:center;background:var(--gold);color:#151515;font-weight:900;font-size:20px;letter-spacing:-1px;border-radius:12px}.brand{font-size:20px;font-weight:800;letter-spacing:.2px}.brand span{color:var(--gold)}.tag{font-size:12px;color:var(--muted);letter-spacing:1.4px;text-transform:uppercase}.socials{margin-left:auto;display:flex;gap:8px;flex-wrap:wrap}.socials a{color:var(--text);text-decoration:none;border:1px solid var(--line);background:var(--panel2);padding:8px 11px;border-radius:9px;font-size:12px;font-weight:750}.socials a:hover{border-color:var(--gold);color:var(--gold)}
.hero{margin-bottom:24px}.eyebrow{color:var(--gold);font-weight:750;font-size:12px;letter-spacing:2px;text-transform:uppercase}.hero h1{font-size:clamp(30px,5vw,46px);line-height:1.08;letter-spacing:-1.6px;margin:8px 0 10px}.hero p{color:var(--muted);max-width:650px;margin:0}
.card{background:rgba(17,21,29,.96);border:1px solid var(--line);border-radius:16px;padding:22px;margin:18px 0}.card h2{font-size:17px;margin:0 0 18px}.grid{display:grid;grid-template-columns:repeat(2,minmax(0,1fr));gap:16px}.field label{display:block;color:#c8d0dc;font-size:13px;font-weight:650;margin-bottom:7px}.field input,.field select{width:100%;padding:13px 12px;border:1px solid #333c4b;border-radius:9px;background:#0b0e14;color:var(--text);font:inherit;outline:none}.field input:focus,.field select:focus{border-color:var(--gold);box-shadow:0 0 0 3px #e8b84b20}.hint{font-size:12px;color:var(--muted);margin-top:6px}.riskmode{display:flex;gap:8px;margin-bottom:12px}.riskmode button{flex:1;padding:10px;border:1px solid var(--line);border-radius:8px;background:var(--panel2);color:var(--muted);font-weight:700;cursor:pointer}.riskmode button.active{border-color:var(--gold);background:#e8b84b18;color:var(--gold)}
.results{display:grid;grid-template-columns:repeat(3,minmax(0,1fr));gap:12px}.metric{background:#0b0e14;border:1px solid var(--line);border-radius:12px;padding:16px}.metric.primary{border-color:#8f702d;background:linear-gradient(145deg,#211c10,#0b0e14)}.metric .label{font-size:12px;color:var(--muted);margin-bottom:7px}.metric .value{font-size:clamp(22px,3vw,30px);font-weight:850;letter-spacing:-.6px;overflow-wrap:anywhere}.metric.primary .value{color:var(--gold)}.metric .sub{font-size:12px;color:var(--muted);margin-top:5px}
.details{display:grid;grid-template-columns:repeat(2,minmax(0,1fr));gap:10px;margin-top:16px}.detail{display:flex;justify-content:space-between;gap:12px;padding:12px 0;border-bottom:1px solid #252c37;font-size:14px}.detail span:first-child{color:var(--muted)}.detail strong{text-align:right}
.warning{font-size:12px;color:var(--muted);margin-top:16px;padding:12px;border-left:3px solid var(--gold);background:#e8b84b0b}.bytefx{background:linear-gradient(145deg,#19170f,#11151d 65%);border-color:#655022}.bytefx h2{margin:4px 0 6px;font-size:24px}.bytefx-badge{color:var(--gold);font-size:11px;font-weight:850;letter-spacing:1.7px;text-transform:uppercase}.bytefx p{color:var(--muted);margin:0}.bytefx-grid{display:grid;grid-template-columns:repeat(4,minmax(0,1fr));gap:10px;margin:18px 0}.bytefx-feature{padding:13px;border:1px solid var(--line);background:#0b0e14;border-radius:11px}.bytefx-feature strong{display:block;font-size:13px;margin-bottom:3px}.bytefx-feature span{display:block;color:var(--muted);font-size:11px}.open-account{display:inline-flex;align-items:center;justify-content:center;padding:13px 20px;border-radius:10px;background:var(--gold);color:#151515;text-decoration:none;font-weight:900;font-size:14px}.bytefx-note{font-size:11px;color:var(--muted);margin-top:12px}.footer{text-align:center;color:var(--muted);font-size:12px;margin-top:26px}.footer strong{color:var(--text)}.error{color:var(--red);font-size:13px;margin-top:12px;min-height:18px}
@media(max-width:620px){.wrap{padding:20px 13px 30px}.card{padding:16px}.grid,.details{grid-template-columns:1fr}.results{grid-template-columns:1fr}.metric{padding:13px}.metric .value{font-size:27px}}
@media(max-width:620px){.top{align-items:flex-start;flex-wrap:wrap}.socials{margin-left:0}.bytefx-grid{grid-template-columns:1fr 1fr}}
</style>
</head>
<body>
<main class="wrap">

<header class="top">
<div class="logo">NT</div>
<div>
<div class="brand">Nandan<span>Trades</span></div>
<div class="tag">Gold risk calculator</div>
</div>
<nav class="socials">
<a href="https://www.instagram.com/nandan.trades" target="_blank" rel="noopener noreferrer">Instagram</a>
<a href="https://t.me/nandanxauusd" target="_blank" rel="noopener noreferrer">Telegram</a>
</nav>
</header>

<section class="hero">
<div class="eyebrow">Plan the risk before the trade</div>
<h1>Gold Lot Size<br>Calculator</h1>
<p>Calculate an estimated XAUUSD position size from your account risk and stop-loss distance. Set the contract size to match your broker.</p>
</section>

<section class="card">
<h2>01 / Trade settings</h2>
<div class="grid">
<div class="field"><label for="balance">Account balance (USD)</label><input id="balance" type="number" min="0" step="any" value="1000"></div>
<div class="field"><label>Risk method</label><div class="riskmode"><button id="percentBtn" class="active" type="button">Risk %</button><button id="amountBtn" type="button">Fixed $</button></div><input id="risk" type="number" min="0" step="any" value="1"><div class="hint" id="riskHint">1% of account balance</div></div>
<div class="field"><label for="entry">Entry price (USD)</label><input id="entry" type="number" min="0" step="any" value="2350"></div>
<div class="field"><label for="stop">Stop-loss price (USD)</label><input id="stop" type="number" min="0" step="any" value="2345"></div>
<div class="field"><label for="contract">Contract size (oz per 1.00 lot)</label><input id="contract" type="number" min="0.0001" step="any" value="100"><div class="hint">Many standard XAUUSD contracts use 100 oz per lot. Verify with your broker.</div></div>
<div class="field"><label for="maxlot">Maximum lot size (optional)</label><input id="maxlot" type="number" min="0" step="any" placeholder="No cap"></div>
</div>
<div class="error" id="error" role="status" aria-live="polite"></div>
</section>

<section class="card">
<h2>02 / Calculated position</h2>
<div class="results">
<div class="metric primary"><div class="label">Suggested lot size</div><div class="value" id="lots">0.0200</div><div class="sub">Before broker volume-step rounding</div></div>
<div class="metric"><div class="label">Amount at risk</div><div class="value" id="riskDollars">$10.00</div><div class="sub" id="riskPercent">1.00% of balance</div></div>
<div class="metric"><div class="label">Stop-loss distance</div><div class="value" id="distance">$5.00</div><div class="sub">Price difference per ounce</div></div>
</div>
<div class="details">
<div class="detail"><span>Risk per 1.00 lot</span><strong id="perLot">$500.00</strong></div>
<div class="detail"><span>Estimated position size</span><strong id="ounces">2.00 oz</strong></div>
<div class="detail"><span>Trade direction check</span><strong id="direction">Entry above stop</strong></div>
<div class="detail"><span>Risk after lot cap</span><strong id="cappedRisk">$10.00</strong></div>
</div>
<div class="warning">Estimate only. This calculation excludes spread, commissions, slippage, swaps and gaps. Broker contract size, tick value, minimum lot and lot step can differ. Confirm the specifications in your trading platform before placing an order.</div>
</section>

<section class="card bytefx">
<div class="bytefx-badge">Trading with NandanTrades</div>
<h2>ByteFX</h2>
<p>Open your trading account and explore the platform for your trading journey.</p>
<div class="bytefx-grid">
<div class="bytefx-feature"><strong>Trading Platform</strong><span>Access your trading account online</span></div>
<div class="bytefx-feature"><strong>Flexible Account</strong><span>Choose an account suited to your needs</span></div>
<div class="bytefx-feature"><strong>Market Access</strong><span>Trade financial markets with leverage</span></div>
<div class="bytefx-feature"><strong>Account Support</strong><span>Platform and account assistance</span></div>
</div>
<a class="open-account" href="https://my.bytefx.com/client/register/Nandan09" target="_blank" rel="noopener noreferrer">Open Account</a>
<div class="bytefx-note">NandanTrades · Trading involves risk. Review the broker's terms, conditions and product disclosures before trading.</div>
</section>

<footer class="footer"><strong>NandanTrades Gold Calculator</strong><br>Educational tool · Trade responsibly · Not financial advice</footer>

</main>

<script>
(() => {
 const $ = id => document.getElementById(id);
 let mode = 'percent';
 const money = n => Number.isFinite(n) ? n.toLocaleString('en-US',{style:'currency',currency:'USD',minimumFractionDigits:2,maximumFractionDigits:2}) : '—';
 const num = id => parseFloat($(id).value);

 function setMode(next){
   mode=next;
   $('percentBtn').classList.toggle('active',mode==='percent');
   $('amountBtn').classList.toggle('active',mode==='amount');
   $('riskHint').textContent=mode==='percent'?'Percent of account balance':'Fixed dollar amount';
   if(mode==='percent' && num('risk')>100) $('risk').value='1';
   if(mode==='amount' && num('risk')<=0) $('risk').value='10';
   calculate();
 }

 $('percentBtn').addEventListener('click',()=>setMode('percent'));
 $('amountBtn').addEventListener('click',()=>setMode('amount'));
 ['balance','risk','entry','stop','contract','maxlot'].forEach(id=>$(id).addEventListener('input',calculate));

 function calculate(){
   const balance=num('balance'), riskInput=num('risk'), entry=num('entry'), stop=num('stop'), contract=num('contract'), maxlotRaw=$('maxlot').value.trim(), maxlot=maxlotRaw===''?Infinity:parseFloat(maxlotRaw);
   const error=$('error');
   error.textContent='';

   if(![balance,riskInput,entry,stop,contract].every(Number.isFinite) || balance<=0 || riskInput<=0 || entry<=0 || stop<=0 || contract<=0 || (mode==='percent' && riskInput>100) || (maxlot!==Infinity && (!Number.isFinite(maxlot)||maxlot<0))){
     error.textContent='Enter valid positive values. Risk % must be above 0 and no more than 100.';
     ['lots','riskDollars','distance','perLot','ounces','direction','cappedRisk','riskPercent'].forEach(id=>$(id).textContent='—');
     return;
   }

   const dist=Math.abs(entry-stop);
   if(dist===0){
     error.textContent='Entry and stop-loss prices must be different.';
     return;
   }

   const riskDollars=mode==='percent'?balance*riskInput/100:riskInput;
   const perLot=dist*contract;
   const rawLots=riskDollars/perLot;
   const lots=Math.min(rawLots,maxlot);
   const actualRisk=lots*perLot;

   $('lots').textContent=lots>0?lots.toFixed(4):'0.0000';
   $('riskDollars').textContent=money(riskDollars);
   $('riskPercent').textContent=(riskDollars/balance*100).toFixed(2)+'% of balance';
   $('distance').textContent='$'+dist.toFixed(2);
   $('perLot').textContent=money(perLot);
   $('ounces').textContent=(lots*contract).toLocaleString('en-US',{maximumFractionDigits:4})+' oz';
   $('direction').textContent=entry>stop?'Entry above stop':entry<stop?'Entry below stop':'Invalid';
   $('cappedRisk').textContent=money(actualRisk);

   if(Number.isFinite(maxlot) && lots<rawLots)
     error.textContent='Lot cap applied. Actual planned risk is lower than your selected risk.';
 }

 calculate();
})();
</script>

</body>
</html>
