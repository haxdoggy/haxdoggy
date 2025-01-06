<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HaxDoggy's World</title>
    <style>
        body {
            background-color: #1a1a1a;
            color: #e6e6e6;
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;
            line-height: 1.6;
        }
        .container {
            max-width: 1200px;
            margin: auto;
            padding: 20px;
        }
        .tabs {
            display: flex;
            flex-wrap: wrap;
            border-bottom: 2px solid #4CAF50;
        }
        .tabs button {
            background-color: inherit;
            border: none;
            outline: none;
            cursor: pointer;
            padding: 14px 16px;
            transition: 0.3s;
            font-size: 17px;
            color: #e6e6e6;
        }
        .tabs button:hover {
            background-color: #333;
        }
        .tabs button.active {
            background-color: #4CAF50;
            color: white;
        }
        .tabcontent {
            display: none;
            padding: 6px 12px;
            border: 1px solid #ccc;
            border-top: none;
        }
        a {
            color: #4CAF50;
            text-decoration: none;
        }
        a:hover {
            text-decoration: underline;
        }
        img {
            max-width: 100%;
            height: auto;
        }
        h1 {
            color: #4CAF50;
        }
    </style>
</head>
<body>

<div class="container">
    <h1>Hello world! 👋</h1>

    <div class="tabs">
        <button class="tablinks" onclick="openTab(event, 'Tab1')">Tab 1</button>
        <button class="tablinks" onclick="openTab(event, 'Tab2')">Tab 2</button>
    </div>

    <div id="Tab1" class="tabcontent">
        <a href="https://wigle.net">
            <img border="0" src="assets/images/wigle-logo.png" alt="Wigle.net logo">
        </a>
        <p>Wardriving, Mayhem H4M portapack, Flipper Zero, Hak5 Pineapple and other script kiddie stuff.</p>
        <p>Working as an Information Security Specialist.</p>
        <a href="https://www.flightaware.com/adsb/stats/user/haxdoggy">
            Watch my flight data from my RTL-SDR and Raspberry Pi setup on FlightAware
        </a>
    </div>

    <div id="Tab2" class="tabcontent">
        <!-- Anpassa innehållet i denna flik enligt dina önskemål -->
        <h2>Anpassa denna flik</h2>
        <p>Du kan lägga till vad som helst här.</p>
    </div>

    <script>
        function openTab(evt, tabName) {
            var i, tabcontent, tablinks;
            tabcontent = document.getElementsByClassName("tabcontent");
            for (i = 0; i < tabcontent.length; i++) {
                tabcontent[i].style.display = "none";
            }
            tablinks = document.getElementsByClassName("tablinks");
            for (i = 0; i < tablinks.length; i++) {
                tablinks[i].className = tablinks[i].className.replace(" active", "");
            }
            document.getElementById(tabName).style.display = "block";
            evt.currentTarget.className += " active";
        }
        // Visa första fliken som standard
        document.getElementById("Tab1").style.display = "block";
        document.getElementsByClassName("tablinks")[0].className += " active";
    </script>
</div>

</body>
</html>
