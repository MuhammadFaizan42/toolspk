<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>All-in-One PDF, Unit & Currency Converter</title>
<style>
  body { font-family: Arial, sans-serif; margin: 0; background: #f9f9f9; }
  header { background: #007bff; padding: 15px; color: white; text-align: center; }
  nav { display: flex; justify-content: center; background: #0056b3; }
  nav a { color: white; padding: 10px 15px; text-decoration: none; transition: background 0.3s; }
  nav a:hover { background: #003f80; }
  section { background: white; padding: 20px; margin: 20px auto; border-radius: 10px; max-width: 900px; box-shadow: 0 2px 8px rgba(0,0,0,0.1); }
  h2 { margin-top: 0; color: #333; }
  label, input, select, button { margin: 8px 0; }
  input, select { width: 100%; padding: 8px; border-radius: 5px; border: 1px solid #ccc; }
  button { padding: 8px 14px; background: #007bff; color: white; border: none; border-radius: 6px; cursor: pointer; font-size: 14px; }
  button:hover { background: #0056b3; }
  .result { margin-top: 10px; font-weight: bold; color: #333; }
  .unit-container { display: flex; gap: 20px; flex-wrap: wrap; }
  .unit-form { flex: 1; min-width: 280px; }
  .unit-result { flex: 1; min-width: 280px; background: #f4f6f9; padding: 15px; border-radius: 8px; }
  footer { background: #0056b3; color: white; text-align: center; padding: 15px; margin-top: 40px; }
  .small { font-size: 13px; color: #666; }
  .pdf-row { display:flex; gap:12px; flex-wrap:wrap; align-items:center }
  .pdf-row input[type=file] { flex:1 }
  .inline { display:inline-block }
</style>
</head>
<body>
<header>
  <h1>All-in-One Tools</h1>
</header>
<nav>
  <a href="#pdfTools">PDF Tools</a>
  <a href="#unitConverter">Unit Converter</a>
  <a href="#currencyConverter">Currency Converter</a>
</nav>

<section id="pdfTools">
  <h2>PDF Tools</h2>
  <p class="small">Merge, split, and compress your PDFs directly in the browser. Files are processed locally — nothing is uploaded.</p>
  <div style="margin-top:12px">
    <label><strong>Merge PDFs</strong></label>
    <div class="pdf-row">
      <input id="mergeFilesInput" type="file" accept="application/pdf" multiple />
      <button id="mergeBtn" class="inline">Merge</button>
    </div>
    <div id="mergeList" class="small"></div>
  </div>

  <hr style="margin:14px 0" />

  <div>
    <label><strong>Split PDF</strong></label>
    <div class="pdf-row">
      <input id="splitFileInput" type="file" accept="application/pdf" />
      <input id="fromPage" type="number" min="1" placeholder="From Page" style="width:100px;padding:8px;border-radius:6px;border:1px solid #ccc" />
      <input id="toPage" type="number" min="1" placeholder="To Page" style="width:100px;padding:8px;border-radius:6px;border:1px solid #ccc" />
      <button id="splitBtn" class="inline">Split</button>
    </div>
    <div id="splitInfo" class="small"></div>
  </div>

  <hr style="margin:14px 0" />

  <div>
    <label><strong>Compress PDF (basic)</strong></label>
    <div class="pdf-row">
      <input id="compressFileInput" type="file" accept="application/pdf" />
      <select id="compressQuality" style="width:120px"> 
        <option value="0.6">Quality 60%</option>
        <option value="0.7" selected>Quality 70%</option>
        <option value="0.8">Quality 80%</option>
      </select>
      <button id="compressBtn" class="inline">Compress</button>
    </div>
    <div id="compressInfo" class="small"></div>
  </div>
</section>

<section id="unitConverter">
  <h2>Unit Converter</h2>
  <div class="unit-container">
    <div class="unit-form">
      <label>Type:</label>
      <select id="unitType" onchange="populateUnits()">
        <option value="length">Length</option>
        <option value="weight">Weight</option>
        <option value="temperature">Temperature</option>
        <option value="time">Time</option>
      </select>

      <label>Value:</label>
      <input type="number" id="unitValue" placeholder="Enter number" />

      <div style="display:flex;gap:8px;align-items:center;margin-top:8px">
        <select id="fromUnit" style="flex:1"></select>
        <div style="width:28px;text-align:center">→</div>
        <select id="toUnit" style="flex:1"></select>
      </div>

      <button onclick="convertUnit()" style="margin-top:12px">Convert</button>
    </div>
    <div class="unit-result">
      <h3>Result</h3>
      <div id="unitResultBox" class="result"></div>
      <div class="small">Tip: Use this for quick conversions. Currency converter below uses live rates.</div>
    </div>
  </div>
</section>

<section id="currencyConverter">
  <h2>Currency Converter</h2>
  <label>Amount:</label>
  <input type="number" id="currencyAmount" placeholder="Enter amount" />
  <label>From:</label>
  <select id="currencyFrom"></select>
  <label>To:</label>
  <select id="currencyTo"></select>
  <button onclick="convertCurrency()" style="margin-top:8px">Convert</button>
  <div class="result" id="currencyResult"></div>
</section>

<footer>
  <p>© 2025 All-in-One Tools | Processed locally in your browser • Fast & Private</p>
</footer>

<!-- Libraries -->
<script src="https://unpkg.com/pdf-lib/dist/pdf-lib.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/FileSaver.js/2.0.5/FileSaver.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/pdf.js/2.16.105/pdf.min.js"></script>

<script>
// --- PDF: Merge, Split, Compress (using pdf-lib & pdf.js) ---
const mergeFilesInput = document.getElementById('mergeFilesInput');
const mergeBtn = document.getElementById('mergeBtn');
const mergeList = document.getElementById('mergeList');
const splitFileInput = document.getElementById('splitFileInput');
const splitBtn = document.getElementById('splitBtn');
const splitInfo = document.getElementById('splitInfo');
const compressFileInput = document.getElementById('compressFileInput');
const compressBtn = document.getElementById('compressBtn');
const compressInfo = document.getElementById('compressInfo');

mergeFilesInput.addEventListener('change', ()=>{
  const files = Array.from(mergeFilesInput.files || []);
  mergeList.innerHTML = files.map((f,i)=>`${i+1}. ${f.name} (${Math.round(f.size/1024)} KB)`).join('<br>');
});

mergeBtn.addEventListener('click', async ()=>{
  const files = Array.from(mergeFilesInput.files || []);
  if (files.length < 2) { alert('Select at least 2 PDF files to merge.'); return; }
  mergeBtn.disabled = true; mergeBtn.innerText = 'Merging...';
  try {
    const mergedPdf = await PDFLib.PDFDocument.create();
    for (const f of files) {
      const arr = await f.arrayBuffer();
      const src = await PDFLib.PDFDocument.load(arr);
      const copied = await mergedPdf.copyPages(src, src.getPageIndices());
      copied.forEach(p => mergedPdf.addPage(p));
    }
    const bytes = await mergedPdf.save();
    saveAs(new Blob([bytes], { type: 'application/pdf' }), 'merged.pdf');
  } catch (err) {
    console.error(err); alert('Error while merging: ' + err.message);
  } finally { mergeBtn.disabled = false; mergeBtn.innerText = 'Merge'; }
});

splitBtn.addEventListener('click', async () => {
  const file = splitFileInput.files[0];
  if (!file) {
    alert('Choose a PDF to split.');
    return;
  }

  const from = parseInt(document.getElementById('fromPage').value, 10);
  const to = parseInt(document.getElementById('toPage').value, 10);

  splitBtn.disabled = true;
  splitBtn.innerText = 'Splitting...';

  try {
    const arr = await file.arrayBuffer();
    const srcDoc = await PDFLib.PDFDocument.load(arr);
    const totalPages = srcDoc.getPageCount();

    // If range is specified
    if (from && to && from >= 1 && to >= from && to <= totalPages) {
      const newPdf = await PDFLib.PDFDocument.create();
      const pageIndices = Array.from({ length: to - from + 1 }, (_, i) => i + from - 1);
      const copiedPages = await newPdf.copyPages(srcDoc, pageIndices);
      copiedPages.forEach(p => newPdf.addPage(p));
      const bytes = await newPdf.save();
      saveAs(new Blob([bytes], { type: 'application/pdf' }), `split_${from}-${to}.pdf`);
    } else {
      // Extract all pages individually
      for (let i = 0; i < totalPages; i++) {
        const singlePdf = await PDFLib.PDFDocument.create();
        const [copiedPage] = await singlePdf.copyPages(srcDoc, [i]);
        singlePdf.addPage(copiedPage);
        const bytes = await singlePdf.save();
        saveAs(new Blob([bytes], { type: 'application/pdf' }), `page_${i + 1}.pdf`);
      }
    }

    splitInfo.innerText = 'Split completed.';
  } catch (err) {
    console.error(err);
    alert('Error while splitting: ' + err.message);
  } finally {
    splitBtn.disabled = false;
    splitBtn.innerText = 'Split';
  }
});

// Basic compress: render pages & re-encode as JPGs into a new PDF
compressBtn.addEventListener('click', async ()=>{
  const f = compressFileInput.files[0];
  if (!f) { alert('Choose a PDF to compress.'); return; }
  const q = parseFloat(document.getElementById('compressQuality').value) || 0.7;
  compressBtn.disabled = true; compressBtn.innerText = 'Compressing...';
  try {
    const arr = await f.arrayBuffer();
    const loadingTask = pdfjsLib.getDocument({ data: arr });
    const pdf = await loadingTask.promise;
    const newPdf = await PDFLib.PDFDocument.create();
    for (let i=1;i<=pdf.numPages;i++){
      const page = await pdf.getPage(i);
      const viewport = page.getViewport({ scale: 1.5 });
      const canvas = document.createElement('canvas');
      canvas.width = Math.floor(viewport.width);
      canvas.height = Math.floor(viewport.height);
      const ctx = canvas.getContext('2d');
      await page.render({ canvasContext: ctx, viewport }).promise;
      const dataUrl = canvas.toDataURL('image/jpeg', q);
      const imgBytes = dataURLtoUint8Array(dataUrl);
      const embedded = await newPdf.embedJpg(imgBytes);
      const imgPage = newPdf.addPage([embedded.width, embedded.height]);
      imgPage.drawImage(embedded, { x:0, y:0, width: embedded.width, height: embedded.height });
    }
    const out = await newPdf.save();
    saveAs(new Blob([out], { type: 'application/pdf' }), 'compressed.pdf');
    compressInfo.innerText = 'Compression done.';
  } catch (err) {
    console.error(err); alert('Compression error: ' + err.message);
  } finally { compressBtn.disabled = false; compressBtn.innerText = 'Compress'; }
});

function dataURLtoUint8Array(dataURL){
  const base64 = dataURL.split(',')[1];
  const binary = atob(base64);
  const len = binary.length; const bytes = new Uint8Array(len);
  for (let i=0;i<len;i++) bytes[i]=binary.charCodeAt(i);
  return bytes;
}

// --- Unit & Currency (kept as before) ---
const unitOptions = {
  length: ["Meter (m)", "Kilometer (km)", "Centimeter (cm)", "Millimeter (mm)", "Mile (mi)", "Yard (yd)", "Foot (ft)", "Inch (in)"],
  weight: ["Kilogram (kg)", "Gram (g)", "Milligram (mg)", "Pound (lb)", "Ounce (oz)"],
  temperature: ["Celsius (°C)", "Fahrenheit (°F)", "Kelvin (K)"],
  time: ["Second (s)", "Minute (min)", "Hour (h)", "Day (d)"]
};

function populateUnits() {
  const type = document.getElementById('unitType').value;
  const from = document.getElementById('fromUnit');
  const to = document.getElementById('toUnit');
  from.innerHTML = unitOptions[type].map(u=>`<option value="${u}">${u}</option>`).join('');
  to.innerHTML = unitOptions[type].map(u=>`<option value="${u}">${u}</option>`).join('');
}

function convertUnit(){
  const type = document.getElementById('unitType').value;
  const value = parseFloat(document.getElementById('unitValue').value);
  const from = document.getElementById('fromUnit').value;
  const to = document.getElementById('toUnit').value;
  if (isNaN(value)) return;
  let result='';
  if (type==='length'){
    const factors = {"Meter (m)":1,"Kilometer (km)":1000,"Centimeter (cm)":0.01,"Millimeter (mm)":0.001,"Mile (mi)":1609.34,"Yard (yd)":0.9144,"Foot (ft)":0.3048,"Inch (in)":0.0254};
    result = (value * factors[from] / factors[to]).toFixed(4);
  } else if (type==='weight'){
    const factors = {"Kilogram (kg)":1,"Gram (g)":0.001,"Milligram (mg)":0.000001,"Pound (lb)":0.453592,"Ounce (oz)":0.0283495};
    result = (value * factors[from] / factors[to]).toFixed(4);
  } else if (type==='temperature'){
    result = convertTemperature(value, from, to).toFixed(2);
  } else if (type==='time'){
    const sec = {"Second (s)":1,"Minute (min)":60,"Hour (h)":3600,"Day (d)":86400};
    result = (value * sec[from] / sec[to]).toFixed(4);
  }
  document.getElementById('unitResultBox').innerText = `${value} ${from} = ${result} ${to}`;
}

function convertTemperature(v, from, to){
  let c;
  if (from.includes('Celsius')) c = v;
  else if (from.includes('Fahrenheit')) c = (v -32) * 5/9;
  else if (from.includes('Kelvin')) c = v - 273.15;
  if (to.includes('Celsius')) return c;
  if (to.includes('Fahrenheit')) return (c * 9/5) + 32;
  if (to.includes('Kelvin')) return c + 273.15;
}

populateUnits();

// Currency
const currencyFrom = document.getElementById('currencyFrom');
const currencyTo = document.getElementById('currencyTo');
let rates = {};
fetch('https://api.exchangerate-api.com/v4/latest/USD')
.then(r=>r.json())
.then(d=>{ rates = d.rates; const opts = Object.keys(rates).map(c=>`<option value="${c}">${c}</option>`).join(''); currencyFrom.innerHTML=opts; currencyTo.innerHTML=opts; currencyFrom.value='USD'; currencyTo.value='PKR'; })
.catch(e=>console.warn('Currency API error',e));
function convertCurrency(){ const amt = parseFloat(document.getElementById('currencyAmount').value); if (!amt) return; const f = currencyFrom.value; const t = currencyTo.value; const usd = amt / rates[f]; const conv = usd * rates[t]; document.getElementById('currencyResult').innerText = `${amt} ${f} = ${conv.toFixed(2)} ${t}`; }
</script>
</body>
</html>
