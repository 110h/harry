<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>病毒扫描</title>
</head>
<body>
    <h1>病毒扫描中...</h1>
    <p id="status">正在初始化...</p>

    <script>
        function simulateScan() {
            const status = document.getElementById("status");
            status.innerText = "正在扫描病毒...";
            setTimeout(() => {
                status.innerText = "发现病毒：Trojan.Win32.Malware!";
                setTimeout(() => {
                    status.innerText = "正在删除病毒...";
                    setTimeout(() => {
                        status.innerText = "开玩笑的！你的电脑很安全。";
                    }, 3000);
                }, 2000);
            }, 2000);
        }

        simulateScan();
    </script>
</body>
</html>
