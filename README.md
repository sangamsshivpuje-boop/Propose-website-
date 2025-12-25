# Propose-website-
This web is made for propose 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>For My Forever</title>
    <style>
        body {
            margin: 0;
            font-family: 'Georgia', serif;
            background-color: #fff5f5;
            color: #4a4a4a;
            text-align: center;
            overflow-x: hidden;
        }
        .container {
            padding: 50px 20px;
            max-width: 800px;
            margin: auto;
        }
        h1 { color: #d63384; font-size: 3rem; }
        p { font-size: 1.2rem; line-height: 1.6; }
        
        /* The Question Section */
        #proposal-section {
            margin-top: 50px;
            padding: 40px;
            background: white;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
        }
        .buttons {
            margin-top: 30px;
            display: flex;
            justify-content: center;
            gap: 20px;
        }
        button {
            padding: 15px 40px;
            font-size: 1.2rem;
            border: none;
            border-radius: 50px;
            cursor: pointer;
            transition: transform 0.2s;
        }
        #yesBtn { background-color: #ff4d6d; color: white; }
        #noBtn { background-color: #adb5bd; color: white; position: relative; }
        
        /* Celebration State */
        #celebration { display: none; }
        .heart { color: #ff4d6d; font-size: 5rem; }
    </style>
</head>
<body>

    <div class="container">
        <section id="main-content">
            <h1>Hi [Her Name],</h1>
            <p>From the moment we met, my life has been brighter. Every laugh we've shared and every challenge we've faced has made me realize one thing...</p>
            
            <div id="proposal-section">
                <h2>Will you make me the luckiest person in the world and be mine forever?</h2>
                <div class="buttons">
                    <button id="yesBtn" onclick="celebrate()">YES!</button>
                    <button id="noBtn" onmouseover="moveButton()">No</button>
                </div>
            </div>
        </section>

        <section id="celebration">
            <div class="heart">❤️</div>
            <h1>I love you!</h1>
            <p>I can't wait to start this next chapter with you.</p>
        </section>
    </div>

    <script>
        // Function to move the "No" button so she can't click it (playful)
        function moveButton() {
            const btn = document.getElementById('noBtn');
            const x = Math.random() * (window.innerWidth - btn.offsetWidth);
            const y = Math.random() * (window.innerHeight - btn.offsetHeight);
            btn.style.position = 'absolute';
            btn.style.left = x + 'px';
            btn.style.top = y + 'px';
        }

        // Function to show the "Yes" screen
        function celebrate() {
            document.getElementById('main-content').style.display = 'none';
            document.getElementById('celebration').style.display = 'block';
            // You could add a confetti trigger here!
        }
    </script>
</body>
</html>
