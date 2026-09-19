<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>منصة كلمات - Nostr</title>
    <style>
        body {
            font-family: system-ui, -apple-system, sans-serif;
            background-color: #0f172a;
            color: #f8fafc;
            margin: 0;
            padding: 20px;
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        .container {
            max-width: 600px;
            width: 100%;
        }
        h1 {
            color: #38bdf8;
            text-align: center;
        }
        .status {
            background-color: #1e293b;
            padding: 10px 15px;
            border-radius: 8px;
            margin-bottom: 20px;
            font-size: 14px;
            color: #94a3b8;
            text-align: center;
        }
        .post-card {
            background-color: #1e293b;
            border-radius: 12px;
            padding: 15px;
            margin-bottom: 15px;
            border: 1px solid #334155;
            word-break: break-word;
        }
        .post-author {
            font-size: 12px;
            color: #38bdf8;
            margin-bottom: 8px;
            font-weight: bold;
        }
        .post-content {
            font-size: 15px;
            line-height: 1.5;
        }
    </style>
</head>
<body>

    <div class="container">
        <h1>كلمات 🌐</h1>
        <div id="status" class="status">جاري الاتصال بشبكة Nostr العالمية...</div>
        
        <div id="feed"></div>
    </div>

    <script>
        // الاتصال بمرحل (Relay) عام مجاني في شبكة Nostr
        const relayUrl = 'wss://relay.damus.io';
        const socket = new WebSocket(relayUrl);
        const statusDiv = document.getElementById('status');
        const feedDiv = document.getElementById('feed');

        socket.onopen = () => {
            statusDiv.innerText = 'تم الاتصال بنجاح! جاري جلب أحدث المنشورات...';
            statusDiv.style.color = '#4ade80';

            // طلب أحدث 10 منشورات (Kind 1 = منشور نصي)
            const request = JSON.stringify([
                "REQ", "main-feed",
                { kinds: [1], limit: 10 }
            ]);
            socket.send(request);
        };

        socket.onmessage = (event) => {
            const data = JSON.parse(event.data);
            if (data[0] === "EVENT") {
                const nostrEvent = data[2];
                displayPost(nostrEvent);
            }
        };

        socket.onerror = (error) => {
            statusDiv.innerText = 'حدث خطأ في الاتصال بالشبكة.';
            statusDiv.style.color = '#f87171';
        };

        function displayPost(event) {
            const card = document.createElement('div');
            card.className = 'post-card';
            
            const author = document.createElement('div');
            author.className = 'post-author';
            author.innerText = `ناشر: ${event.pubkey.substring(0, 10)}...`;

            const content = document.createElement('div');
            content.className = 'post-content';
            content.innerText = event.content;

            card.appendChild(author);
            card.appendChild(content);

            feedDiv.appendChild(card);
        }
    </script>
</body>
</html>
