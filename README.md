<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>FREE FIRE GAME - VIP PRO | Tích Hợp Đầy Đủ</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@700&family=Rajdhani:wght@500;700&display=swap');
        
        /* CÁC BIẾN MÀU CHỦ ĐẠO (Đỏ) */
        :root {
            --red-primary: #FF0000;
            --red-dark: #A00000;
            --red-light: #FF3333;
            --red-gradient-start: #FF0000;
            --red-gradient-end: #CC0000;
            --text-color: #FFFFFF;
            --red-background-deep: #400000;
        }
        
        body {
            font-family: 'Rajdhani', sans-serif;
            margin: 0;
            padding: 0;
            background-color: #000;
            color: var(--text-color);
            background: 
                radial-gradient(circle at 20% 30%, rgba(255, 0, 0, 0.15) 0%, transparent 40%),
                radial-gradient(circle at 80% 70%, rgba(200, 0, 0, 0.15) 0%, transparent 40%);
            animation: bgPulse 12s infinite alternate;
            overflow-y: auto;
            min-height: 100vh;
        }
        
        @keyframes bgPulse {
            0% { background-color: #110000; }
            100% { background-color: #000011; }
        }
        
        .container {
            max-width: 380px;
            margin: 30px auto;
            background: rgba(15, 5, 5, 0.85);
            border-radius: 16px;
            padding: 20px;
            box-shadow: 
                0 0 15px var(--red-primary),
                0 0 30px rgba(255, 0, 0, 0.3);
            border: 1px solid var(--red-primary);
            backdrop-filter: blur(8px);
            position: relative;
            overflow: hidden;
        }
        
        .container::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: linear-gradient(
                to bottom right,
                transparent 45%,
                var(--red-primary) 50%,
                transparent 55%
            );
            opacity: 0.3;
            animation: scan 6s linear infinite;
            z-index: -1;
        }
        
        @keyframes scan {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }
        
        .header {
            text-align: center;
            margin-bottom: 25px;
            padding-bottom: 15px;
            border-bottom: 1px solid var(--red-primary);
            position: relative;
        }
        
        .header h1 {
            font-family: 'Orbitron', sans-serif;
            color: transparent;
            background: linear-gradient(90deg, var(--red-primary), var(--red-light));
            -webkit-background-clip: text;
            background-clip: text;
            margin: 0;
            font-size: 26px;
            letter-spacing: 2px;
            text-shadow: 0 0 10px rgba(255, 0, 0, 0.7);
        }
        
        .header p {
            color: var(--red-light);
            margin: 8px 0 0;
            font-size: 14px;
            font-weight: bold;
            letter-spacing: 1px;
        }
        
        .feature {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 12px 15px;
            margin: 12px 0;
            background: linear-gradient(90deg, rgba(80, 0, 0, 0.3), transparent);
            border-radius: 10px;
            border-left: 3px solid var(--red-primary);
            transition: all 0.3s;
            position: relative;
            overflow: hidden;
        }
        
        .feature::after {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 0, 0, 0.2), transparent);
            transition: 0.5s;
        }
        
        .feature:hover {
            background: linear-gradient(90deg, rgba(120, 0, 0, 0.5), transparent);
            box-shadow: 0 0 10px rgba(255, 0, 0, 0.3);
        }
        
        .feature:hover::after {
            left: 100%;
        }
        
        .feature-info {
            flex: 1;
        }
        
        .feature-name {
            font-weight: bold;
            color: var(--red-primary);
            font-size: 17px;
            letter-spacing: 0.5px;
            text-shadow: 0 0 5px var(--red-primary);
        }
        
        .feature-desc {
            font-size: 13px;
            color: #aaa;
            margin-top: 4px;
            letter-spacing: 0.3px;
        }
        
        /* Nút bật/tắt NEON (Giữ nguyên) */
        .toggle-switch {
            position: relative;
            display: inline-block;
            width: 55px;
            height: 28px;
        }
        
        .toggle-switch input {
            opacity: 0;
            width: 0;
            height: 0;
        }
        
        .slider {
            position: absolute;
            cursor: pointer;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: rgba(102, 0, 0, 0.5);
            transition: .4s;
            border-radius: 28px;
            box-shadow: inset 0 0 5px #000;
        }
        
        .slider:before {
            position: absolute;
            content: "";
            height: 22px;
            width: 22px;
            left: 3px;
            bottom: 3px;
            background: linear-gradient(145deg, #ccc, #fff);
            transition: .4s;
            border-radius: 50%;
            box-shadow: 0 0 5px #fff;
        }
        
        input:checked + .slider {
            background: linear-gradient(90deg, var(--red-gradient-start), var(--red-gradient-end));
            box-shadow: 0 0 10px var(--red-primary);
        }
        
        input:checked + .slider:before {
            transform: translateX(27px);
            background: #fff;
            box-shadow: 0 0 10px #fff;
        }
        
        .vip-badge {
            background: linear-gradient(90deg, #ff0, #f90);
            color: #000;
            font-size: 11px;
            padding: 2px 8px;
            border-radius: 10px;
            margin-left: 8px;
            font-weight: bold;
            text-shadow: 0 0 2px rgba(0,0,0,0.3);
            box-shadow: 0 0 5px #ff0;
        }
        
        .footer {
            text-align: center;
            margin-top: 25px;
            font-size: 11px;
            color: #555;
            letter-spacing: 1px;
            text-transform: uppercase;
        }
        
        /* Hiệu ứng chớp ngẫu nhiên */
        .glitch {
            animation: glitch-effect 5s infinite linear;
        }
        
        @keyframes glitch-effect {
            0%, 100% { text-shadow: 0 0 5px var(--red-primary); }
            25% { text-shadow: -2px 0 5px var(--red-light), 2px 0 5px var(--red-dark); }
            50% { text-shadow: 0 0 10px var(--red-primary); }
            75% { text-shadow: -3px 0 5px var(--red-dark), 3px 0 5px var(--red-light); }
        }

        /* --- PHẦN 1: VÒNG TRÒN HIỆU SUẤT (CPU/RAM/NETWORK) --- */
        
        .performance-card {
            padding: 20px 0;
            margin-bottom: 25px;
            background: rgba(15, 5, 5, 0.6);
            border-radius: 10px;
            border: 1px solid var(--red-primary);
            box-shadow: 0 0 10px rgba(255, 0, 0, 0.3);
        }

        .performance-stats {
            display: flex;
            justify-content: space-around;
        }

        .stat-circle-container {
            position: relative;
            width: 80px; 
            height: 80px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
        }

        .stat-circle-container svg {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            transform: rotate(-90deg);
        }

        .stat-circle-container circle {
            fill: none;
            stroke-width: 6; 
            stroke-linecap: round;
        }

        .bg-circle {
            stroke: rgba(255, 255, 255, 0.15); 
        }

        .progress-circle {
            stroke-dasharray: 251.2; 
            transition: stroke-dashoffset 1.5s ease-out, stroke 0.5s;
        }
        
        #cpu-progress {
            stroke: var(--red-light); 
            animation: cpu-load-ring 3s infinite alternate;
        }

        @keyframes cpu-load-ring {
            0% { stroke-dashoffset: 200.96; } 
            50% { stroke-dashoffset: 175.84; } 
            100% { stroke-dashoffset: 200.96; }
        }
        
        #ram-progress {
            stroke: #ff7f00; 
        }
        
        #network-progress {
            stroke: #00ff00; 
        }

        .stat-circle-text {
            position: absolute;
            font-size: 16px; 
            font-weight: bold;
            color: var(--text-color); 
            z-index: 10;
        }
        .stat-circle-label {
            position: absolute;
            font-size: 10px;
            color: var(--red-light); 
            margin-top: 25px; 
            z-index: 10;
            font-weight: bold;
        }

        /* --- PHẦN 2: BIỂU ĐỒ FPS --- */
        .fps-chart-section {
            margin-top: 30px;
            padding: 15px;
            background: rgba(15, 5, 5, 0.6);
            border-radius: 10px;
            border: 1px solid var(--red-primary);
            box-shadow: 0 0 10px rgba(255, 0, 0, 0.3);
        }

        .chart-header {
            text-align: center;
            margin-bottom: 15px;
        }

        .chart-header h2 {
            font-family: 'Rajdhani', sans-serif;
            font-weight: 700;
            font-size: 20px;
            margin: 0;
            color: var(--text-color);
            text-shadow: 0 0 5px var(--red-light);
        }

        .chart-header .icon {
            font-size: 22px;
            margin-right: 5px;
            display: inline-block;
        }
        
        .chart-header .red-text {
            color: var(--red-light);
            display: block;
            font-size: 24px;
            letter-spacing: 1px;
        }

        .chart-box {
            position: relative;
            width: 100%;
            height: 180px;
            background-color: var(--red-background-deep);
            border-radius: 5px;
            overflow: hidden;
            border: 1px solid var(--red-dark);
            box-shadow: inset 0 0 8px #000;
        }

        .chart-grid {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-image: 
                linear-gradient(to right, rgba(255, 0, 0, 0.2) 1px, transparent 1px),
                linear-gradient(to bottom, rgba(255, 0, 0, 0.2) 1px, transparent 1px);
            background-size: 12.5% 18px;
            pointer-events: none;
        }

        .fps-labels {
            position: absolute;
            width: 100%;
            padding: 5px 10px;
            box-sizing: border-box;
            font-size: 13px;
            font-weight: bold;
            color: var(--text-color);
            z-index: 10;
        }

        .fps-labels .max-fps {
            position: absolute;
            top: 5px;
            left: 10px;
            color: #fff;
        }
        
        .fps-labels .current-fps {
            position: absolute;
            top: 5px;
            right: 10px;
            color: var(--red-light);
            text-shadow: 0 0 5px var(--red-primary);
        }

        .fps-labels .min-fps {
            position: absolute;
            bottom: 5px;
            left: 10px;
            color: #fff;
        }

        /* SVG Chart Styles */
        #fpsChartSVG {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
        }
        
        #fpsLine {
            fill: none;
            stroke: var(--red-light);
            stroke-width: 2;
            filter: drop-shadow(0 0 5px var(--red-primary));
            transition: stroke-dashoffset 0.1s linear; 
        }

        /* --- TÂM ẢO VÀ MODAL MỚI --- */

        /* Style cho nút Tâm Ảo */
        .crosshair-button {
            background: linear-gradient(90deg, var(--red-primary), var(--red-light));
            color: #fff;
            border: none;
            padding: 10px 20px;
            border-radius: 8px;
            cursor: pointer;
            font-size: 16px;
            font-weight: bold;
            letter-spacing: 1px;
            box-shadow: 0 0 10px rgba(255, 0, 0, 0.5);
            transition: background 0.3s, transform 0.1s;
        }

        .crosshair-button:hover {
            background: linear-gradient(90deg, var(--red-light), var(--red-primary));
            transform: translateY(-1px);
        }

        /* Thẻ ảnh Tâm Ảo cố định trên màn hình (Đã xóa translate để dùng trong JS) */
        #virtualCrosshair {
            position: fixed;
            top: 50%;
            left: 50%;
            /* transform được tính toán trong JS để căn giữa + offset */
            z-index: 9999; 
            width: 64px; /* Kích thước mặc định */
            height: 64px;
            pointer-events: none; 
            filter: drop-shadow(0 0 5px rgba(255, 0, 0, 0.5));
        }

        /* Modal nền mờ */
        .crosshair-modal {
            display: none; 
            position: fixed; 
            z-index: 10000; 
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            overflow: auto; 
            background-color: rgba(0,0,0,0.7); 
            backdrop-filter: blur(3px);
        }

        /* Khung cài đặt */
        .crosshair-settings {
            background: rgba(15, 5, 5, 0.95);
            margin: 15% auto; 
            padding: 20px;
            border: 1px solid var(--red-primary);
            width: 80%; 
            max-width: 300px;
            border-radius: 12px;
            box-shadow: 0 0 20px var(--red-primary);
        }

        .modal-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            border-bottom: 1px solid var(--red-dark);
            padding-bottom: 10px;
            margin-bottom: 15px;
        }

        .modal-header h3 {
            margin: 0;
            color: var(--red-light);
            font-family: 'Orbitron', sans-serif;
        }

        .close-btn {
            color: var(--red-light);
            font-size: 28px;
            font-weight: bold;
            cursor: pointer;
        }

        .control-group {
            margin-bottom: 15px;
        }

        .control-group label {
            display: block;
            font-weight: bold;
            color: #fff;
            margin-bottom: 5px;
        }

        .control-group input[type="range"] {
            width: 100%;
            height: 8px;
            background: var(--red-dark);
            border-radius: 4px;
            outline: none;
            opacity: 0.8;
            transition: opacity .2s;
        }

        .control-group input[type="range"]:hover {
            opacity: 1;
        }

        .toggle-crosshair-btn {
            width: 100%;
            padding: 10px;
            background: var(--red-primary);
            color: white;
            border: none;
            border-radius: 6px;
            cursor: pointer;
            margin-top: 10px;
            font-weight: bold;
        }
    </style>
</head>
<body onload="updateStatsInitial()">
    
    <div class="container">
        <div class="header">
            <h1 class="glitch">MENU AIMLOCK PRO </h1>
            <p>DEV XUÂN DUY</p>
        </div>
        
        <div class="performance-card">
            <div class="performance-stats">
                <div class="stat-circle-container">
                    <svg viewBox="0 0 100 100">
                        <circle class="bg-circle" cx="50" cy="50" r="40"></circle>
                        <circle id="cpu-progress" class="progress-circle" cx="50" cy="50" r="40"></circle>
                    </svg>
                    <span class="stat-circle-text" id="cpu-percent">25%</span>
                    <span class="stat-circle-label">CPU</span>
                </div>
                
                <div class="stat-circle-container">
                    <svg viewBox="0 0 100 100">
                        <circle class="bg-circle" cx="50" cy="50" r="40"></circle>
                        <circle id="ram-progress" class="progress-circle" cx="50" cy="50" r="40"></circle>
                    </svg>
                    <span class="stat-circle-text" id="ram-percent">0%</span>
                    <span class="stat-circle-label">RAM</span>
                </div>
                
                <div class="stat-circle-container">
                    <svg viewBox="0 0 100 100">
                        <circle class="bg-circle" cx="50" cy="50" r="40"></circle>
                        <circle id="network-progress" class="progress-circle" cx="50" cy="50" r="40"></circle>
                    </svg>
                    <span class="stat-circle-text" id="network-percent">0%</span>
                    <span class="stat-circle-label">NETWORK</span>
                </div>
            </div>

            <div class="button-container" style="text-align: center; margin-top: 15px;">
                <button class="crosshair-button" onclick="openCrosshairModal()">🎯 TÂM ẢO (VIRTUAL CROSSHAIR)</button>
            </div>
        </div>

        <div class="feature">
            <div class="feature-info">
                <div class="feature-name">OPTIMIZE GAME </span></div>
                <div class="feature-desc">Tối Ưu Game Fix Lag</div>
            </div>
            <label class="toggle-switch">
                <input type="checkbox">
                <span class="slider"></span>
            </label>
        </div>
        
        <div class="feature">
            <div class="feature-info">
                <div class="feature-name">FPS 240HZ UNLOCKER<span class="vip-badge">VIP</div>
                <div class="feature-desc">On 240Hz Tối Ưu Máy</div>
            </div>
            <label class="toggle-switch">
                <input type="checkbox">
                <span class="slider"></span>
            </label>
        </div>
        
        <div class="feature">
            <div class="feature-info">
                <div class="feature-name">FIX LỐ + FIX RUNG<span class="vip-badge">VIP</span></div>
                <div class="feature-desc">Giảm Tỉ Lệ Lố Đầu Fix Rung Tâm</div>
            </div>
            <label class="toggle-switch">
                <input type="checkbox">
                <span class="slider"></span>
            </label>
        </div>
        
        <div class="feature">
            <div class="feature-info">
                <div class="feature-name">AIMLOCK PRO</div>
                <div class="feature-desc">Tăng Tỉ Lệ Headshot 95%</div>
            </div>
            <label class="toggle-switch">
                <input type="checkbox">
                <span class="slider"></span>
            </label>
        </div>
        
        <div class="feature">
            <div class="feature-info">
                <div class="feature-name">Sensivity Pro<span class="vip-badge">VIP</span></div>
                <div class="feature-desc">Tăng Nhẹ Tâm Nhạy Màn </div>
            </div>
            <label class="toggle-switch">
                <input type="checkbox">
                <span class="slider"></span>
            </label>
        </div>
        
        <div class="feature">
            <div class="feature-info">
                <div class="feature-name">AIMBOT PRO</div>
                <div class="feature-desc">Khoá Chặt Vùng Đầu Aim Chặt</div>
            </div>
            <label class="toggle-switch">
                <input type="checkbox">
                <span class="slider"></span>
            </label>
        </div>
        
        <div class="feature">
            <div class="feature-info">
                <div class="feature-name">SUPPER CONFIG PRO</div>
                <div class="feature-desc">Mượt Màn Tối Ưu Tăng Nhạy Cảm Ứng</div>
            </div>
            <label class="toggle-switch">
                <input type="checkbox">
                <span class="slider"></span>
            </label>
        </div>

        <div class="fps-chart-section">
            <div class="chart-header">
                <h2><span class="icon">📊</span> Biểu Đồ FPS <span class="red-text">Thời Gian Thực</span></h2>
            </div>
            <div class="chart-box">
                <div class="fps-labels">
                    <span class="max-fps">144 FPS</span>
                    <span class="current-fps" id="currentFps">60 FPS</span>
                    <span class="min-fps">30 FPS</span>
                </div>
                <div class="chart-grid"></div>
                
                <svg id="fpsChartSVG" viewBox="0 0 340 180" preserveAspectRatio="none">
                    <polyline id="fpsLine" points=""></polyline>
                </svg>
            </div>
        </div>
        <div class="footer">
            © 2025 TikTok : sakura.loveyou_1
        </div>
    </div>
    
    <div id="crosshairModal" class="crosshair-modal">
        <div class="crosshair-settings">
            <div class="modal-header">
                <h3>⚙️ Cài Đặt Tâm Ảo</h3>
                <span class="close-btn" onclick="closeCrosshairModal()">&times;</span>
            </div>
            
            <div class="control-group">
                <label for="sizeRange">Kích Thước (<span id="sizeValue">100</span>%)</label>
                <input type="range" id="sizeRange" min="50" max="200" value="100" oninput="updateCrosshair()">
            </div>

            <div class="control-group">
                <label for="xRange">Vị Trí Ngang X (<span id="xValue">0</span> px)</label>
                <input type="range" id="xRange" min="-150" max="150" value="0" oninput="updateCrosshair()">
            </div>

            <div class="control-group">
                <label for="yRange">Vị Trí Dọc Y (<span id="yValue">0</span> px)</label>
                <input type="range" id="yRange" min="-150" max="150" value="0" oninput="updateCrosshair()">
            </div>

            <div class="control-group">
                <label for="opacityRange">Độ Mờ (<span id="opacityValue">1.0</span>)</label>
                <input type="range" id="opacityRange" min="0.1" max="1.0" step="0.1" value="1.0" oninput="updateCrosshair()">
            </div>

            <button class="toggle-crosshair-btn" onclick="toggleCrosshairDisplay()">BẬT/TẮT TÂM ẢO</button>
        </div>
    </div>

    <img id="virtualCrosshair" src="https://i.postimg.cc/FzQNpVZ5/IMG-2481.png" alt="Tâm Ảo" style="display: none;">

    <script>
        // --- LOGIC ÂM THANH MỚI (DÙNG WEB AUDIO API) ---
        const sounds = (()=>{
            let ctx;
            const ensureCtx=()=>{ 
                if(!ctx){ 
                    try{ 
                        // Khởi tạo Audio Context khi có tương tác
                        ctx=new (window.AudioContext||window.webkitAudioContext)(); 
                    }catch(e){
                         console.error("Lỗi khởi tạo Audio Context:", e);
                    } 
                } 
                return ctx; 
            };
            const osc = (f=920,ms=90)=>{ // f: tần số (Hz), ms: thời lượng (ms)
                const c=ensureCtx(); 
                if(!c) return;
                
                const o=c.createOscillator(), g=c.createGain();
                o.connect(g).connect(c.destination);
                o.frequency.value=f;
                g.gain.setValueAtTime(.08, c.currentTime); // Âm lượng tối đa
                o.start();
                // Giảm âm lượng về 0 sau thời gian ms
                g.gain.exponentialRampToValueAtTime(0.001, c.currentTime+ms/1000); 
                o.stop(c.currentTime+ms/1000);
            };
            // Định nghĩa loại âm thanh duy nhất cho nút bật/tắt (toggle)
            return { toggle:()=>osc(920,90) }; 
        })();

        function play(name){
            if(name==='toggle') sounds.toggle();
            // Có thể thêm 'success' hoặc 'error' nếu cần:
            // else if(name==='success') sounds.success(); 
        }

        // --- SCRIPT CHUNG (ĐÃ CẬP NHẬT GỌI HÀM play('toggle')) ---
        
        document.querySelectorAll('.toggle-switch input').forEach(toggle => {
            toggle.addEventListener('change', function() {
                const feature = this.closest('.feature');
                const name = feature.querySelector('.feature-name');
                const RED_LIGHT = 'var(--red-light)';
                const RED_PRIMARY = 'var(--red-primary)';
                
                // 🎧 PHÁT ÂM THANH
                play('toggle');
                
                if (this.checked) {
                    // Cập nhật giao diện Bật
                    feature.style.borderLeft = `3px solid ${RED_LIGHT}`;
                    name.style.textShadow = `0 0 10px ${RED_LIGHT}`;
                    name.style.color = RED_LIGHT;
                    feature.style.boxShadow = `0 0 15px ${RED_LIGHT}`;
                    setTimeout(() => {
                        feature.style.boxShadow = '0 0 10px rgba(255, 0, 0, 0.3)';
                    }, 300);
                } else {
                    // Cập nhật giao diện Tắt
                    feature.style.borderLeft = `3px solid ${RED_PRIMARY}`;
                    name.style.textShadow = `0 0 5px ${RED_PRIMARY}`;
                    name.style.color = RED_PRIMARY;
                    feature.style.boxShadow = 'none';
                }
            });
        });
        
        const glitchText = document.querySelector('.glitch');
        setInterval(() => {
            if (Math.random() > 0.7) {
                glitchText.style.animation = 'none';
                setTimeout(() => {
                    glitchText.style.animation = 'glitch-effect 5s infinite linear';
                }, 100);
            }
        }, 3000);

        function getRandomInt(min, max) {
            return Math.floor(Math.random() * (max - min + 1)) + min;
        }

        // --- SCRIPT 1: VÒNG TRÒN HIỆU SUẤT (CPU/RAM/NETWORK) ---
        
        const TOTAL_LENGTH = 251.2; 
        const CPU_INITIAL_PERCENT = 25; 
        const CPU_INITIAL_OFFSET = TOTAL_LENGTH - (TOTAL_LENGTH * CPU_INITIAL_PERCENT / 100); 
        
        let initialRamPercent = 0; 
        let initialNetworkPercent = 0; 

        function setCircleValue(id, percent, color, textContent) {
            const progress = document.getElementById(id + '-progress');
            const textElement = document.getElementById(id + '-percent');
            
            const offset = TOTAL_LENGTH - (TOTAL_LENGTH * percent / 100);

            textElement.textContent = textContent !== undefined ? textContent : (percent + '%');
            progress.style.stroke = color; 

            if (id !== 'cpu' || !window.isCpuTextUpdating) {
                 setTimeout(() => {
                     progress.style.strokeDashoffset = offset;
                 }, 10);
            }
        }
        
        function updateCpuText() {
            const cpuText = document.getElementById('cpu-percent');
            const newPercent = getRandomInt(20, 30);
            cpuText.textContent = newPercent + '%';
            
            const newInterval = getRandomInt(300, 700); 
            
            if (window.isCpuTextUpdating) {
                window.cpuTimeout = setTimeout(updateCpuText, newInterval);
            }
        }
        
        // --- SCRIPT 2: BIỂU ĐỒ FPS ĐỘNG ---

        const fpsLine = document.getElementById('fpsLine');
        const currentFpsElement = document.getElementById('currentFps');
        
        const CHART_WIDTH = 340; 
        const CHART_HEIGHT = 180;
        const FPS_MIN = 30;
        const FPS_MAX = 144;
        const FPS_RANGE = FPS_MAX - FPS_MIN;
        const MAX_POINTS = 50; 
        
        let fpsHistory = [];

        function getRandomFps() {
            let baseFps = 60 + (Math.random() - 0.5) * 10; 
            
            if (Math.random() < 0.05) baseFps = 100 + Math.random() * 44; // Đỉnh cao 
            else if (Math.random() < 0.05) baseFps = 35 + Math.random() * 10; // Đỉnh thấp (lag)

            return Math.min(FPS_MAX, Math.max(FPS_MIN, Math.round(baseFps)));
        }

        function updateChart() {
            const newFps = getRandomFps();
            
            fpsHistory.push(newFps);
            if (fpsHistory.length > MAX_POINTS) {
                fpsHistory.shift(); 
            }

            let points = "";
            const stepX = CHART_WIDTH / (MAX_POINTS - 1);
            
            for (let i = 0; i < fpsHistory.length; i++) {
                const fpsValue = fpsHistory[i];
                
                const normalizedFps = (fpsValue - FPS_MIN) / FPS_RANGE;
                const y = CHART_HEIGHT * (1 - normalizedFps);
                const x = i * stepX;
                
                points += `${x},${y} `;
            }

            fpsLine.setAttribute('points', points.trim());

            currentFpsElement.textContent = `${newFps} FPS`;
            if (newFps > 60) {
                 currentFpsElement.style.color = 'var(--red-light)';
            } else {
                 currentFpsElement.style.color = 'var(--red-primary)';
            }
        }
        
        function initFpsChart() {
             for(let i = 0; i < MAX_POINTS; i++) {
                fpsHistory.push(getRandomFps());
            }
            updateChart();
            setInterval(updateChart, 100);
        }
        
        // --- SCRIPT 3: ĐIỀU KHIỂN TÂM ẢO ---

        const crosshair = document.getElementById('virtualCrosshair');
        const modal = document.getElementById('crosshairModal');
        let isCrosshairVisible = false;

        // 1. Mở Modal
        function openCrosshairModal() {
            modal.style.display = 'block';
            updateCrosshair(); 
        }

        // 2. Đóng Modal
        function closeCrosshairModal() {
            modal.style.display = 'none';
        }

        // 3. Khởi tạo trạng thái Bật/Tắt Tâm Ảo (Đảm bảo Tâm Ảo ẩn và nút hiển thị TẮT ban đầu)
        function initCrosshairState() {
            isCrosshairVisible = false;
            crosshair.style.display = 'none';
            
            const button = document.querySelector('.toggle-crosshair-btn');
            button.textContent = 'ĐANG TẮT: BẤM ĐỂ BẬT';
            button.style.background = 'var(--red-primary)'; 
        }

        // 4. Bật/Tắt hiển thị Tâm Ảo
        function toggleCrosshairDisplay() {
            isCrosshairVisible = !isCrosshairVisible;
            
            // Chỉ BẬT/TẮT hiển thị tâm ảo
            crosshair.style.display = isCrosshairVisible ? 'block' : 'none';
            
            const button = document.querySelector('.toggle-crosshair-btn');
            if (isCrosshairVisible) {
                button.textContent = 'ĐANG BẬT: BẤM ĐỂ TẮT';
                button.style.background = '#00CC00'; 
            } else {
                button.textContent = 'ĐANG TẮT: BẤM ĐỂ BẬT';
                button.style.background = 'var(--red-primary)'; 
            }
        }

        // 5. Cập nhật Vị trí, Kích thước, Độ mờ
        function updateCrosshair() {
            const sizeRange = document.getElementById('sizeRange').value;
            const xRange = document.getElementById('xRange').value;
            const yRange = document.getElementById('yRange').value;
            const opacityRange = document.getElementById('opacityRange').value;

            document.getElementById('sizeValue').textContent = sizeRange;
            document.getElementById('xValue').textContent = xRange;
            document.getElementById('yValue').textContent = yRange;
            document.getElementById('opacityValue').textContent = opacityRange;

            // Chỉnh kích thước
            const baseSize = 64; 
            const newSize = (baseSize * sizeRange) / 100;
            
            // 1. Đặt kích thước ảnh
            crosshair.style.width = `${newSize}px`;
            crosshair.style.height = `${newSize}px`;

            // 2. Vị trí ảnh: Dùng Transform để căn giữa và áp dụng offset
            crosshair.style.transform = `translate(calc(-50% + ${xRange}px), calc(-50% + ${yRange}px))`;
            
            // Chỉnh độ mờ
            crosshair.style.opacity = opacityRange;
        }

        // Đóng modal khi click ra ngoài
        window.onclick = function(event) {
            if (event.target == modal) {
                closeCrosshairModal();
            }
        }
        
        // --- HÀM KHỞI TẠO CHUNG ---
        function updateStatsInitial() {
            // Khởi tạo RAM và Network
            initialRamPercent = getRandomInt(30, 60); 
            setCircleValue('ram', initialRamPercent, '#ff7f00'); 
            
            initialNetworkPercent = getRandomInt(0, 54); 
            setCircleValue('network', initialNetworkPercent, '#00ff00'); 
            
            // Khởi tạo CPU
            document.getElementById('cpu-progress').style.strokeDashoffset = CPU_INITIAL_OFFSET;
            window.isCpuTextUpdating = true;
            updateCpuText(); 
            
            // Khởi tạo FPS Chart
            initFpsChart();
            
            // Khởi tạo Tâm Ảo
            updateCrosshair();
            initCrosshairState(); 
            
            // *** ĐÃ BỎ LỆNH TẢI ÂM THANH CŨ ***
        }

        // Gọi hàm khởi tạo khi trang tải xong
        if (document.readyState === 'loading') {
            document.addEventListener('DOMContentLoaded', updateStatsInitial);
        } else {
            updateStatsInitial();
        }
    </script>
</body>
</html>
