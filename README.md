<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>For My Love</title>
    <style>
        body { 
            font-family: Arial, sans-serif; 
            background: #ffe6ee; 
            display: flex; 
            justify-content: center; 
            align-items: center; 
            height: 100vh; 
        }
        #container { 
            background: white; 
            padding: 25px; 
            border-radius: 20px; 
            width: 320px; 
            text-align: center; 
            box-shadow: 0 0 15px rgba(0,0,0,0.2); 
        }
        button { 
            padding: 10px 20px; 
            margin: 10px; 
            border: none; 
            border-radius: 10px; 
            background: #ff86a1; 
            color: white; 
            font-size: 16px; 
            cursor: pointer; 
        }
        button:disabled { 
            background: #d8a4af; 
            cursor: not-allowed; 
        }
        #gif { 
            width: 150px; 
            margin-top: 10px; 
        }
    </style>
</head>
<body>

    <div id="container">

        <!-- SCREEN 1 -->
        <div id="screen1">
            <h2>Hi sayang, good evening 💗</h2>
            <button onclick="nextScreen(2)">Next</button>
        </div>

        <!-- SCREEN 2 -->
        <div id="screen2" style="display:none;">
            <h3>Kamu sayang aku nggak? </h3>
            <button onclick="nextScreen(3)">Yes</button>
            <button onclick="nextScreen(3)">Yes</button>
        </div>

        <!-- SCREEN 3 -->
        <div id="screen3" style="display:none;">
            <h3>Kamu maafin aku nggak? </h3>
            <button onclick="nextScreen(4)">Yes</button>
            <button disabled>No</button>
        </div>

        <!-- SCREEN 4 -->
        <div id="screen4" style="display:none;">
            <img src="c:\Users\c2799\AppData\Local\Packages\5319275A.WhatsAppDesktop_cv1g1gvanyjgm\TempState\DF4FB1D4CC775DA225D5C5E70143E44D\WhatsApp Image 2025-11-29 at 14.44.27_9745471c.jpg" width="170px" style="border-radius:15px; margin-top:10px;">
            <p>makaciii cyangg aku cintaa km ckaliii</p>
            <button onclick="nextScreen(5)">→</button>
            <button onclick="nextScreen(6)">←</button>
        </div>

        <!-- SCREEN 5 (LOVE MESSAGE + VOICE) -->
        <div id="screen5" style="display:none;">
            <h3>akuuu cinta kamu banget tau gak? 💞</h3>
            <marquee scrollamount="5">
                Banyak banget... gabisa dihitung... makin hari makin sayangg!! 💗💗💗
            </marquee>

            <!-- BUTTON VOICE NOTE -->
            <button onclick="playAudio('loveAudio')">Putar Voice Note 💗</button>
            <audio id="loveAudio" src="c:\Users\c2799\AppData\Local\Packages\5319275A.WhatsAppDesktop_cv1g1gvanyjgm\TempState\7B5533ABAA9399471B8C5D1CAC9D4EB9\WhatsApp Audio 2025-11-29 at 14.17.48_2d44d063.waptt"></audio>

            <button onclick="nextScreen(4)">Back</button>
        </div>

        <!-- SCREEN 6 (SORRY + VOICE) -->
        <div id="screen6" style="display:none;">
            <h3>Maafin akuu yaa sayang 🥺💗</h3>
            <p>Maaf kalau aku pernah bikin kamu kesel atau sedih... aku bener-bener sayang sama kamu 🩷</p>

            <!-- BUTTON VOICE NOTE -->
            <button onclick="playAudio('sorryAudio')">Putar Voice Note Maaf 🥺</button>
            <audio id="sorryAudio" src="c:\Users\c2799\AppData\Local\Packages\5319275A.WhatsAppDesktop_cv1g1gvanyjgm\TempState\E47172648719CAD3559FED4241415C3F\WhatsApp Audio 2025-11-29 at 14.12.23_96a50d21.waptt"></audio>

            <button onclick="nextScreen(4)">Back</button>
        </div>

    </div>

    <script>
        function nextScreen(num){
            document.querySelectorAll('#container > div').forEach(d => d.style.display = 'none');
            document.getElementById('screen' + num).style.display = 'block';
        }

        /* FUNGSI PLAY AUDIO */
        function playAudio(id){
            const audio = document.getElementById(id);
            audio.currentTime = 0;
            audio.play();
        }
    </script>

</body>
</html>
