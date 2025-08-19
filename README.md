<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Top Up Free Fire 🇮🇩</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&display=swap" rel="stylesheet">
  <style>
    *{margin:0;padding:0;box-sizing:border-box;font-family:'Poppins',sans-serif}
    body{
      background:url('https://cdn.oneesports.gg/cdn-data/2022/07/FreeFire_Wallpaper2022.jpg') no-repeat center center fixed;
      background-size:cover;
      color:#222;
    }
    .overlay{background:rgba(0,0,0,0.6);position:fixed;top:0;left:0;right:0;bottom:0;z-index:-1}

    header{background:rgba(46,125,50,0.9);color:#fff;padding:14px 20px;display:flex;justify-content:space-between;align-items:center;position:sticky;top:0;z-index:10}
    header .logo{display:flex;align-items:center;gap:10px;font-weight:700;font-size:18px}
    header .logo img{width:32px;height:32px;border-radius:50%}
    header nav a{margin-left:20px;color:#c8e6c9;text-decoration:none;font-size:14px}
    header nav a:hover{color:#fff}

    .banner{background:#388e3c;color:#fff;text-align:center;padding:6px;font-size:14px}

    .container{background:#fff;width:100%;max-width:720px;padding:25px 20px;margin:20px auto;box-shadow:0 4px 12px rgba(0,0,0,0.2);border-radius:12px}
    h1{text-align:center;font-size:26px;margin-bottom:20px;color:#2e7d32}

    label{font-size:14px;margin:8px 0 4px;display:block}
    input{width:100%;padding:12px;border-radius:10px;border:1px solid #ccc;margin-bottom:14px;background:#f9f9f9}

    .packages{display:grid;gap:10px}
    .pkg{padding:14px;border-radius:10px;border:1px solid #c8e6c9;background:#f1f8f1;display:flex;justify-content:space-between;align-items:center;cursor:pointer;transition:.2s;font-size:15px}
    .pkg:hover{border-color:#2e7d32;background:#e8f5e9;transform:scale(1.02)}
    .pkg.active{border-color:#2e7d32;box-shadow:0 0 8px rgba(46,125,50,0.4)}
    .badge{background:#ff5252;color:#fff;font-size:11px;padding:2px 6px;border-radius:6px;margin-left:8px}

    .payment{display:flex;gap:10px;margin:10px 0 20px}
    .payment input{display:none}
    .payment label{flex:1;background:#f1f8f1;padding:12px;text-align:center;border-radius:8px;border:1px solid #c8e6c9;cursor:pointer}
    .payment input:checked+label{border-color:#2e7d32;box-shadow:0 0 6px rgba(46,125,50,0.4)}

    button{width:100%;padding:16px;border:none;border-radius:12px;font-size:16px;font-weight:700;cursor:pointer;background:linear-gradient(90deg,#2e7d32,#66bb6a);color:#fff;margin-top:10px}
    button:hover{opacity:0.9}

    .preview{margin-top:16px;background:#f1f8f1;padding:16px;border-radius:12px;font-size:14px;white-space:pre-wrap;border:1px dashed #c8e6c9}

    footer{text-align:center;margin:20px 0;font-size:12px;color:#fff;text-shadow:0 1px 2px rgba(0,0,0,0.7)}
  </style>
</head>
<body>
  <div class="overlay"></div>

  <header>
    <div class="logo">
      <img src="https://cdn-icons-png.flaticon.com/512/5969/5969120.png">
      <span>TopUpMuWani</span>
    </div>
    <nav>
      <a href="#">Beranda</a>
      <a href="#">Harga</a>
      <a href="#">Kontak</a>
    </nav>
  </header>

  <div class="banner"><marquee>🔥 Promo Free Fire • Diamond Murah • Proses Cepat • Aman 100% 🔥</marquee></div>

  <div class="container">
    <h1>Top Up Free Fire 🇮🇩</h1>
    <label for="ffid">Masukkan ID Free Fire</label>
    <input type="text" id="ffid" placeholder="Masukkan ID Free Fire Anda">

    <label>Pilih Paket Diamond / Produk</label>
    <div class="packages" id="packages"></div>

    <label>Metode Pembayaran</label>
    <div class="payment">
      <input type="radio" name="pay" id="dana" value="DANA" checked>
      <label for="dana">DANA</label>
      <input type="radio" name="pay" id="qris" value="QRIS Allpay">
      <label for="qris">QRIS Allpay</label>
    </div>

    <button id="confirm">Konfirmasi</button>
    <div class="preview" id="preview">Pratinjau pesan WhatsApp akan muncul di sini...</div>
  </div>

  <footer>
    © <span id="year"></span> AlwiztopupFF • Semua Hak Dilindungi
  </footer>

  <script>
    // Paket
    const PACKS=[
      {price:1000,diamonds:5},
      {price:2000,diamonds:10},
      {price:4000,diamonds:20},
      {price:10000,diamonds:70,badge:'🔥 Best Seller'},
      {price:14000,diamonds:90},
      {price:17500,diamonds:120,badge:'Promo'},
      {price:50000,diamonds:355},
      {price:69000,diamonds:500},
      {price:31000,label:'Member Mingguan'},
      {price:46000,label:'BP Card'},
      {price:92000,label:'Member Bulanan'}
    ];
    const packagesEl=document.getElementById('packages');
    const previewEl=document.getElementById('preview');
    const ffidEl=document.getElementById('ffid');
    let selectedIndex=null;

    function formatRupiah(num){return new Intl.NumberFormat('id-ID',{style:'currency',currency:'IDR',maximumFractionDigits:0}).format(num)}
    function renderPackages(){
      PACKS.forEach((p,i)=>{
        const div=document.createElement('div');
        div.className='pkg';
        const label=p.diamonds?`${formatRupiah(p.price)} = ${p.diamonds} 💎`:`${p.label}`;
        div.innerHTML=`<span>${label} ${p.badge?'<span class="badge">'+p.badge+'</span>':''}</span><span>${formatRupiah(p.price)}</span>`;
        div.onclick=()=>{selectedIndex=i;document.querySelectorAll('.pkg').forEach(el=>el.classList.remove('active'));div.classList.add('active');updatePreview();};
        packagesEl.appendChild(div);
      });
    }
    function getPayment(){return document.querySelector('input[name="pay"]:checked').value;}
    function updatePreview(){
      const id=ffidEl.value.trim()||'(belum diisi)';
      const pack=selectedIndex!=null?PACKS[selectedIndex]:null;
      const pay=getPayment();
      let msg=`Top Up Free Fire 🇮🇩\n=====================\nID: ${id}\nPaket: ${pack?(pack.diamonds?`${formatRupiah(pack.price)} = ${pack.diamonds}💎`:pack.label+' ('+formatRupiah(pack.price)+')'):'(belum dipilih)'}\nMetode Pembayaran: ${pay}\n\nMohon diproses kak 🙏`;
      previewEl.textContent=msg;return msg;
    }
    ffidEl.oninput=updatePreview;
    document.querySelectorAll('input[name="pay"]').forEach(r=>r.onchange=updatePreview);
    document.getElementById('confirm').onclick=()=>{
      if(!ffidEl.value.trim()){alert('Harap isi ID Free Fire dahulu');return;}
      if(selectedIndex===null){alert('Harap pilih paket.');return;}
      const msg=updatePreview();const phone='6285189283822';window.location.href=`https://wa.me/${phone}?text=${encodeURIComponent(msg)}`;
    };
    renderPackages();
    document.getElementById('year').textContent=new Date().getFullYear();
  </script>
</body>
</html>
