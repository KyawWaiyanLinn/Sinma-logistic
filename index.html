<!DOCTYPE html>
<html lang="my">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=yes">
    <title>SINMA Mall • Direct API</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root { --bg: #f5f5f5; --white: #fff; --primary: #ff5000; --text: #333; }
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { background: var(--bg); font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif; display: flex; justify-content: center; min-height: 100vh; color: var(--text); }
        .app-container { max-width: 500px; width: 100%; min-height: 100vh; background: var(--bg); padding-bottom: 70px; }
        .header { background: var(--primary); padding: 12px 16px; position: sticky; top: 0; z-index: 50; }
        .search-box { background: rgba(255,255,255,0.95); border-radius: 20px; padding: 8px 16px; display: flex; align-items: center; gap: 8px; }
        .search-box input { border: none; outline: none; flex: 1; font-size: 14px; background: transparent; }
        .search-btn { background: var(--primary); color: white; border: none; padding: 8px 16px; border-radius: 16px; font-size: 13px; font-weight: 700; cursor: pointer; white-space: nowrap; }
        .categories { display: flex; gap: 8px; overflow-x: auto; padding: 12px 16px; scrollbar-width: none; }
        .categories::-webkit-scrollbar { display: none; }
        .cat-item { background: var(--white); padding: 10px 16px; border-radius: 20px; white-space: nowrap; font-size: 13px; font-weight: 600; cursor: pointer; box-shadow: 0 2px 12px rgba(0,0,0,0.08); display: flex; align-items: center; gap: 6px; }
        .cat-item:active { transform: scale(0.95); background: #fff0e8; }
        .cat-item.active { background: var(--primary); color: white; }
        .product-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 10px; padding: 0 16px; }
        .product-card { background: var(--white); border-radius: 12px; overflow: hidden; box-shadow: 0 2px 12px rgba(0,0,0,0.08); cursor: pointer; }
        .product-card:active { transform: scale(0.97); }
        .product-card img { width: 100%; height: 200px; object-fit: cover; background: #f0f0f0; }
        .product-card .info { padding: 10px; }
        .product-card .name { font-size: 12px; line-height: 1.4; overflow: hidden; display: -webkit-box; -webkit-line-clamp: 2; -webkit-box-orient: vertical; height: 34px; margin-bottom: 6px; }
        .product-card .price { font-size: 16px; font-weight: 800; color: var(--primary); }
        .product-card .shop { font-size: 10px; color: #999; margin-top: 2px; }
        .cart-bar { position: fixed; bottom: 0; left: 50%; transform: translateX(-50%); max-width: 500px; width: 100%; background: white; border-top: 1px solid #eee; padding: 10px 16px; display: flex; align-items: center; justify-content: space-between; z-index: 50; }
        .cart-icon { position: relative; font-size: 24px; color: #333; }
        .cart-badge { position: absolute; top: -8px; right: -10px; background: var(--primary); color: white; font-size: 10px; width: 20px; height: 20px; border-radius: 50%; display: flex; align-items: center; justify-content: center; font-weight: 700; }
        .modal { position: fixed; top: 0; left: 0; right: 0; bottom: 0; background: rgba(0,0,0,0.5); z-index: 100; display: flex; align-items: flex-end; justify-content: center; }
        .modal-content { background: white; border-radius: 20px 20px 0 0; padding: 20px; max-width: 500px; width: 100%; max-height: 70vh; overflow-y: auto; }
        .btn-orange { background: linear-gradient(135deg, #ff5000, #ff6a00); color: white; font-weight: 700; border: none; border-radius: 20px; padding: 14px; font-size: 15px; cursor: pointer; width: 100%; }
        .btn-orange:active { transform: scale(0.97); }
        @keyframes spin { from { transform: rotate(0deg); } to { transform: rotate(360deg); } }
        .animate-spin { animation: spin 1s linear infinite; }
        .toast { position: fixed; bottom: 80px; left: 50%; transform: translateX(-50%); background: #333; color: white; padding: 10px 20px; border-radius: 20px; font-size: 13px; font-weight: 600; z-index: 200; }
        .popup { position: fixed; top: 0; left: 0; right: 0; bottom: 0; background: rgba(0,0,0,0.7); z-index: 9999; display: flex; align-items: center; justify-content: center; }
        .popup-card { background: white; border-radius: 24px; padding: 32px 24px; text-align: center; max-width: 350px; width: 90%; }
    </style>
</head>
<body>

<div id="welcomePopup" class="popup">
    <div class="popup-card">
        <div style="font-size:60px;">🛍️</div>
        <h2 style="font-size:20px;font-weight:900;color:#333;">မင်္ဂလာပါ</h2>
        <p style="font-size:16px;font-weight:700;color:#ff5000;">SINMA Mall</p>
        <p style="font-size:11px;color:#666;margin-bottom:12px;">Created by <strong>Kyaw Waiyan Linn</strong></p>
        <button onclick="document.getElementById('welcomePopup').style.display='none'" class="btn-orange">စတင်ဈေးဝယ်မယ်</button>
    </div>
</div>

<div class="app-container">
    <div class="header">
        <div style="display:flex;align-items:center;gap:6px;margin-bottom:8px;">
            <span style="color:white;font-size:18px;font-weight:900;">SINMA Mall</span>
        </div>
        <div class="search-box">
            <i class="fa-solid fa-magnifying-glass" style="color:#999;"></i>
            <input type="text" id="searchKeyword" placeholder="ပစ္စည်းရှာရန်...">
            <button onclick="searchProducts()" class="search-btn">ရှာမယ်</button>
        </div>
    </div>
    
    <div class="categories">
        <div class="cat-item active" onclick="loadHomeProducts()">🔥 Hot</div>
        <div class="cat-item" onclick="searchCategory('shoes')">👟 ဖိနပ်</div>
        <div class="cat-item" onclick="searchCategory('shirt')">👕 အင်္ကျီ</div>
        <div class="cat-item" onclick="searchCategory('bag')">👜 အိတ်</div>
        <div class="cat-item" onclick="searchCategory('phone')">📱 ဖုန်း</div>
        <div class="cat-item" onclick="searchCategory('electronics')">🔌 လျှပ်စစ်</div>
    </div>
    
    <div style="margin:16px 16px 12px;font-size:16px;font-weight:800;">🔥 Hot Products</div>
    
    <div id="productGrid" class="product-grid">
        <div style="grid-column:1/-1;text-align:center;padding:60px;color:#999;">
            <i class="fa-solid fa-spinner animate-spin" style="font-size:32px;color:#ff5000;display:block;margin-bottom:12px;"></i>
            Loading...
        </div>
    </div>
    
    <div class="cart-bar">
        <div class="cart-icon" onclick="openCart()">
            <i class="fa-solid fa-basket-shopping"></i>
            <span class="cart-badge" id="cartBadge">0</span>
        </div>
        <div style="flex:1;margin-left:12px;">
            <span id="cartTotalKs" style="font-weight:800;color:#ff5000;">0 Ks</span>
        </div>
        <button onclick="openCart()" class="btn-orange" style="width:auto;padding:10px 24px;font-size:13px;">ခြင်းတောင်း</button>
    </div>
</div>

<script>
const TOKEN = 'kKIu6qEmpkwi0Uvo';
const SHEET = 'https://script.google.com/macros/s/AKfycbz3zejT0DgFLpkNMqxAb7nSjs7I3iTxZrHM1r9Y75j0bwyj2xXNY6zXhYct7Pjbe1jW7w/exec';
const API = 'https://api.justoneapi.com/api/taobao';
const RATE = 650;

function toKs(y) { return Math.round(y*RATE); }
function fmtKs(a) { return a.toLocaleString('en-US')+' Ks'; }
function toast(m) { const t=document.createElement('div'); t.className='toast'; t.innerText=m; document.body.appendChild(t); setTimeout(()=>t.remove(),2000); }

// ==================== DIRECT API CALL (NO PROXY) ====================
async function fetchProductsByKeyword(kw) {
    const grid = document.getElementById('productGrid');
    grid.innerHTML = '<div style="grid-column:1/-1;text-align:center;padding:60px;"><i class="fa-solid fa-spinner animate-spin" style="font-size:32px;color:#ff5000;display:block;margin-bottom:12px;"></i>Loading...</div>';
    
    try {
        const url = `${API}/search/v1?token=${TOKEN}&keyword=${encodeURIComponent(kw)}&page=1&sort=sale&tmall=1`;
        console.log('Fetching:', url);
        
        const res = await fetch(url);
        console.log('Response status:', res.status);
        
        const data = await res.json();
        console.log('Response data:', data);
        
        const items = data?.data?.model?.itemList || [];
        
        if(items.length > 0) {
            grid.innerHTML = items.slice(0,20).map(item => {
                const priceYuan = item.priceYuanDouble || item.discntPriceYuan || 0;
                const priceKs = toKs(priceYuan);
                return `<div class="product-card" onclick="openProductDetail('${item.itemId}')">
                    <img src="${item.picUrlFull||''}" onerror="this.src='https://via.placeholder.com/300'">
                    <div class="info">
                        <div class="name">${item.itemName||''}</div>
                        <div class="price">${fmtKs(priceKs)}</div>
                        <div class="shop">${item.shopName||''}</div>
                    </div>
                </div>`;
            }).join('');
        } else {
            grid.innerHTML = '<div style="grid-column:1/-1;text-align:center;padding:40px;color:#999;">⚠️ ပစ္စည်းမတွေ့ပါ</div>';
        }
    } catch(e) {
        console.error('Error:', e);
        grid.innerHTML = `<div style="grid-column:1/-1;text-align:center;padding:40px;color:#ff5000;">❌ ${e.message}</div>`;
    }
}

function loadHomeProducts() { fetchProductsByKeyword('shoes'); }
function searchCategory(kw) { document.querySelectorAll('.cat-item').forEach(c=>c.classList.remove('active')); event.target.classList.add('active'); fetchProductsByKeyword(kw); }
function searchProducts() {
    const kw = document.getElementById('searchKeyword').value.trim();
    if(!kw) return toast('နာမည်ထည့်ပါ');
    document.querySelectorAll('.cat-item').forEach(c=>c.classList.remove('active'));
    fetchProductsByKeyword(kw);
}

async function openProductDetail(itemId) {
    try {
        const res = await fetch(`${API}/get-item-detail/v4?token=${TOKEN}&itemId=${itemId}`);
        const data = await res.json();
        if(data?.data) {
            const item = data.data;
            const discountYuan = (parseFloat(item.DiscountPrice)||0)/100;
            const itemYuan = (parseFloat(item.itemPrice)||0)/100;
            const displayYuan = discountYuan > 0 ? discountYuan : itemYuan;
            
            const cart = JSON.parse(localStorage.getItem('sinma_cart')||'[]');
            cart.push({ title:item.title, priceYuan:displayYuan, qty:1, spec:'', totalKs:toKs(displayYuan) });
            localStorage.setItem('sinma_cart',JSON.stringify(cart));
            updateCartUI();
            toast('✅ Cart ထဲထည့်ပြီး — ' + fmtKs(toKs(displayYuan)));
        }
    } catch(e) { toast('Error'); }
}

function updateCartUI() {
    const cart = JSON.parse(localStorage.getItem('sinma_cart')||'[]');
    document.getElementById('cartBadge').innerText = cart.length;
    document.getElementById('cartTotalKs').innerText = fmtKs(cart.reduce((s,i)=>s+(i.totalKs||toKs(i.priceYuan*i.qty)),0));
}

function openCart() {
    const cart = JSON.parse(localStorage.getItem('sinma_cart')||'[]');
    const modal = document.createElement('div');
    modal.className = 'modal';
    modal.style.display = 'flex';
    modal.onclick = function(e) { if(e.target===modal) modal.remove(); };
    modal.innerHTML = `
        <div class="modal-content">
            <div style="display:flex;justify-content:space-between;margin-bottom:16px;">
                <h3 style="font-weight:800;">🛒 ခြင်းတောင်း</h3>
                <button onclick="this.closest('.modal').remove()" style="background:none;border:none;font-size:20px;">✕</button>
            </div>
            <div style="max-height:300px;overflow-y:auto;margin-bottom:12px;">
                ${cart.length ? cart.map((item,i)=>`
                    <div style="display:flex;justify-content:space-between;padding:10px 0;border-bottom:1px solid #eee;">
                        <div><p style="font-size:12px;font-weight:600;">${item.title}</p><p style="font-size:13px;font-weight:700;color:#ff5000;">${fmtKs(item.totalKs||toKs(item.priceYuan*item.qty))}</p></div>
                        <button onclick="removeCartItem(${i}); this.closest('.modal').remove(); openCart();" style="color:#ff5000;background:none;border:none;">🗑</button>
                    </div>`).join('') : '<p style="color:#999;text-align:center;padding:20px;">ပစ္စည်းမရှိပါ</p>'}
            </div>
            <input type="tel" id="cartPhone" placeholder="ဖုန်းနံပါတ်ထည့်ပါ" style="width:100%;padding:12px;border:1px solid #ddd;border-radius:10px;margin-bottom:12px;">
            <button onclick="submitOrder()" class="btn-orange">Order တင်မယ်</button>
        </div>`;
    document.body.appendChild(modal);
}

function removeCartItem(i) {
    const cart = JSON.parse(localStorage.getItem('sinma_cart')||'[]');
    cart.splice(i,1);
    localStorage.setItem('sinma_cart',JSON.stringify(cart));
    updateCartUI();
}

async function submitOrder() {
    const cart = JSON.parse(localStorage.getItem('sinma_cart')||'[]');
    const phone = document.getElementById('cartPhone')?.value?.trim();
    if(!cart.length) return toast('ပစ္စည်းမရှိ');
    if(!phone) return toast('ဖုန်းထည့်ပါ');
    try {
        await fetch(SHEET, {method:'POST',mode:'no-cors',headers:{'Content-Type':'application/json'},body:JSON.stringify({orderId:'SINMA-'+Date.now(),phone,items:cart})});
        toast('✅ Order တင်ပြီး');
        localStorage.removeItem('sinma_cart');
        updateCartUI();
        document.querySelectorAll('.modal').forEach(m=>m.remove());
    } catch(e) { toast('❌ Error'); }
}

document.addEventListener('DOMContentLoaded',()=>{ updateCartUI(); loadHomeProducts(); });
</script>
</body>
</html>
