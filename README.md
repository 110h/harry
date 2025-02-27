<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>蓝屏模拟</title>
    <style>
        body {
            background-color: #0078D7;
            color: white;
            font-family: Arial, sans-serif;
            padding: 20px;
        }
    </style>
</head>
<body>
    <h1>:(</h1>
    <p>你的设备遇到问题，需要重启。</p>
    <p>我们只收集一些错误信息，然后为你重新启动。</p>
    <p id="progress">0% 完成</p>

    <script>
        let progress = 0;
        const progressElement = document.getElementById("progress");

        function updateProgress() {
            if (progress < 100) {
                progress += 10;
                progressElement.innerText = `${progress}% 完成`;
                setTimeout(updateProgress, 1000);
            } else {
                progressElement.innerText = "开玩笑的！没有蓝屏。";
            }
        }

        updateProgress();
    </script>
</body>
</html>
