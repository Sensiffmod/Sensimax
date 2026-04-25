<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SENSIOBMAX.IO - V39.2.4 LUXURY</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        body { margin: 0; background: #020617; font-family: sans-serif; color: white; overflow-x: hidden; }
        /* Hiệu ứng quét sáng */
        @keyframes sweep { 0% { left: -100%; } 100% { left: 100%; } }
        .glow-effect { position: relative; overflow: hidden; }
        .glow-effect::before {
            content: ""; position: absolute; top: 0; left: -100%; width: 50%; height: 100%;
            background: linear-gradient(to right, transparent, rgba(255,255,255,0.2), transparent);
            transition: all 0.5s; animation: sweep 3s infinite;
        }
        /* Glassmorphism */
        .glass { background: rgba(15, 23, 42, 0.8); backdrop-filter: blur(10px); border: 1px solid rgba(255,255,255,0.1); }
        /* Menu & Popup */
        #menu-wrapper, #bank-popup { position: fixed; inset: 0; z-index: 100; display: none; align-items: center; justify-content: center; background: rgba(0,0,0,0.8); }
        #menu-wrapper.active, #bank-popup.active { display: flex; }
        .popup-content { width: 90%; max-width: 400px; padding: 20px; border-radius: 20px; border-left: 5px solid #3b82f6; }
    </style>
</head>
<body>

    <header class="p-4 flex items-center justify-between glass sticky top-0 z-50">
        <button onclick="toggleMenu()" class="text-2xl">☰</button>
        <h1 class="text-lg font-black italic text-blue-500">SENSIOBMAX.IO</h1>
        <button onclick="openBankPopup()" class="bg-blue-600 px-4 py-1 rounded-full text-xs font-bold shadow-[0_0_15px_rgba(37,99,235,0.6)]">NẠP TIỀN +</button>
    </header>

    <main class="p-4 space-y-6">
        <div class="glass p-3 rounded-xl border-l-4 border-blue-500 text-center">
            <p class="text-[10px] font-bold text-blue-400">HỆ THỐNG: V39.2.4 (FIX QR & FULL FILE)</p>
        </div>

        <div class="glass p-3 rounded-xl border-l-4 border-yellow-500">
            <p class="text-[10px] text-yellow-400 font-bold text-center">HOẠT ĐỘNG: 6H-12H | 14H-22H --- ZALO: 0397208110</p>
        </div>

        <h2 class="text-center text-red-500 font-black text-sm italic">--- FAKE LAG FREE 48H ---</h2>
        <div class="space-y-3">
            <div class="glass p-4 rounded-xl flex justify-between items-center glow-effect border-l-4 border-red-500">
                <span class="font-bold italic text-sm">NETPLUS V8</span>
                <button onclick="openBankPopup()" class="bg-red-600 px-4 py-2 rounded-lg text-[10px] font-black">LẤY KEY</button>
            </div>
            <div class="glass p-4 rounded-xl flex justify-between items-center glow-effect border-l-4 border-red-500">
                <span class="font-bold italic text-sm">HOPPER V10</span>
                <button onclick="openBankPopup()" class="bg-red-600 px-4 py-2 rounded-lg text-[10px] font-black">LẤY KEY</button>
            </div>
        </div>

        <h2 class="text-center text-blue-500 font-black text-sm italic">--- DANH SÁCH FILE VIP ---</h2>
        <div class="grid grid-cols-1 gap-3">
            <div class="glass p-4 rounded-xl flex justify-between items-center border-l-4 border-blue-500">
                <div>
                    <h4 class="text-blue-400 font-bold italic text-xs">AIMLOCK IOS 2.5 (200K)</h4>
                    <p class="text-[9px] text-gray-500">Đã bán: 84 | Còn: 3</p>
                </div>
                <button onclick="openBankPopup()" class="bg-blue-600 px-6 py-2 rounded-lg text-[10px] font-black">MUA</button>
            </div>
            <div class="glass p-4 rounded-xl flex justify-between items-center border-l-4 border-yellow-500">
                <div>
                    <h4 class="text-yellow-400 font-bold italic text-xs">AIMBODY IOS 3.0 (250K)</h4>
                    <p class="text-[9px] text-gray-500">Đã bán: 67 | Còn: 6</p>
                </div>
                <button onclick="openBankPopup()" class="bg-yellow-600 px-6 py-2 rounded-lg text-[10px] font-black">MUA</button>
            </div>
        </div>
    </main>

    <div id="menu-wrapper" onclick="toggleMenu()">
        <div class="glass popup-content space-y-4" onclick="event.stopPropagation()">
            <h2 class="text-blue-500 font-black italic text-center border-b border-blue-500/20 pb-2">MENU QUẢN TRỊ</h2>
            <nav class="flex flex-col gap-3">
                <a href="#" class="text-xs font-bold">🏠 TRANG CHỦ</a>
                <a href="#" onclick="openBankPopup(); toggleMenu()" class="text-xs font-bold text-yellow-400">💳 NẠP TIỀN HỆ THỐNG</a>
                <a href="https://zalo.me/0397208110" class="text-xs font-bold text-green-400">💬 HỖ TRỢ ZALO</a>
            </nav>
        </div>
    </div>

    <div id="bank-popup">
        <div class="glass popup-content text-center relative border-l-4 border-blue-500">
            <button onclick="closePopups()" class="absolute top-2 right-4 text-xl">&times;</button>
            <h2 class="text-blue-400 font-black italic mb-4">THANH TOÁN</h2>
            <div class="bg-white p-2 rounded-xl inline-block mb-4 shadow-lg">
                <img src="https://api.vietqr.io/image/970422-0397208110-3796D5.jpg?accountName=NGUYEN%20QUOC%20HUY" alt="QR Bank" class="w-48 h-48">
            </div>
            <div class="text-[10px] space-y-1 font-bold text-gray-300">
                <p>STK: 0397208110</p>
                <p>TÊN: NGUYỄN QUỐC HUY</p>
                <p>BANK: MB BANK</p>
            </div>
            <a href="https://zalo.me/0397208110" target="_blank" class="block w-full bg-green-600 mt-4 py-2 rounded-xl font-bold text-xs">XÁC NHẬN ĐÃ CHUYỂN</a>
        </div>
    </div>

    <script>
        function toggleMenu() {
            document.getElementById('menu-wrapper').classList.toggle('active');
        }
        function openBankPopup() {
            closePopups();
            document.getElementById('bank-popup').classList.add('active');
        }
        function closePopups() {
            document.getElementById('menu-wrapper').classList.remove('active');
            document.getElementById('bank-popup').classList.remove('active');
        }
        // Đóng khi bấm ra ngoài
        window.onclick = function(event) {
            if (event.target == document.getElementById('bank-popup')) closePopups();
        }
    </script>
</body>
</html>
