# Miawork
<!DOCTYPE html>
<html lang="zh">
<head>
    <meta charset="UTF-8">
    <title>王蓓奕 Portfolio</title>
    <style>
        body { font-family: 'Helvetica Neue', sans-serif; background: #fdfdfd; color: #333; margin: 0; padding: 50px 20px; text-align: center; }
        .intro { margin-bottom: 50px; }
        .grid { display: flex; justify-content: center; gap: 20px; flex-wrap: wrap; }
        /* 卡片基础样式 */
        .card { width: 250px; padding: 20px; border: 2px solid #333; border-radius: 15px; cursor: pointer; transition: all 0.3s; background: white; }
        /* 鼠标移上去的效果：轻微放大和阴影，体现活泼 */
        .card:hover { transform: translateY(-10px); box-shadow: 10px 10px 0px #FFB6C1; border-color: #FFB6C1; }
        .card h3 { margin-top: 0; color: #FF6B81; }
        /* 弹窗样式 */
        #modal { display: none; position: fixed; top: 0; left: 0; width: 100%; height: 100%; background: rgba(255,255,255,0.95); justify-content: center; align-items: center; flex-direction: column; }
    </style>
</head>
<body>

    <div class="intro">
        <h1>✨ 王蓓奕 | 视觉与内容增长</h1>
        <p>中日英三语背景 | IP开发 | 社交媒体专家</p>
    </div>

    <div class="grid">
        <div class="card" onclick="openWork('运营', '这里放你小红书爆款的截图和数据')">
            <h3>📱 账号运营</h3>
            <p>HBC实习 & 个人爆款</p>
        </div>
        <div class="card" onclick="openWork('IP设计', '这里放你设计的纪念章和吉祥物图片')">
            <h3>🎨 IP形象</h3>
            <p>博物馆及校级IP开发</p>
        </div>
        <div class="card" onclick="openWork('视觉', '这里放你的原画、摄影和海报')">
            <h3>📸 视觉艺术</h3>
            <p>平面、摄影、原画</p>
        </div>
    </div>

    <div id="modal" onclick="this.style.display='none'">
        <h2 id="modal-title"></h2>
        <div id="modal-content">作品内容加载中...</div>
        <p style="color: #999; margin-top: 20px;">(点击任意位置关闭)</p>
    </div>

    <script>
        function openWork(title, content) {
            document.getElementById('modal').style.display = 'flex';
            document.getElementById('modal-title').innerText = title;
            document.getElementById('modal-content').innerText = content;
        }
    </script>
</body>
</html>
