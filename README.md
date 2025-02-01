<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Découverte de Sbiba</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #f4f4f4;
        }
        #videoContainer, #languageSelection, #profileSelection, #epochSelection, #message {
            display: none;
        }
        .btn {
            padding: 10px 20px;
            margin: 10px;
            background-color: #007BFF;
            color: white;
            border: none;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <h1>Bienvenue à Sbiba</h1>
    <div id="videoContainer">
        <video id="promoVideo" width="80%" controls>
            <source src="video.mp4" type="video/mp4">
            Votre navigateur ne supporte pas la lecture de vidéos.
        </video>
    </div>
    
    <div id="languageSelection">
        <h2>Choisissez votre langue</h2>
        <button class="btn" onclick="selectLanguage('fr')">Français</button>
        <button class="btn" onclick="selectLanguage('en')">English</button>
    </div>
    
    <div id="profileSelection">
        <h2>Vous êtes :</h2>
        <button class="btn" onclick="selectProfile('enfant')">Enfant</button>
        <button class="btn" onclick="selectProfile('citoyen')">Citoyen</button>
        <button class="btn" onclick="selectProfile('historien')">Historien</button>
    </div>
    
    <div id="epochSelection">
        <h2>Choisissez une époque</h2>
        <button class="btn" onclick="showMessage()">Islamique</button>
        <button class="btn" onclick="showMessage()">Byzantine</button>
        <button class="btn" onclick="showMessage()">Romaine</button>
    </div>
    
    <div id="message">
        <h2>Curieux de voir la suite ?</h2>
        <p>Viens nous rendre visite et accumule encore plus de points… mais attention, le fun est garanti ! 😄🎉</p>
    </div>
    
    <script>
        document.getElementById("videoContainer").style.display = "block";
        let video = document.getElementById("promoVideo");
        video.onended = function() {
            document.getElementById("languageSelection").style.display = "block";
        };
        
        function selectLanguage(lang) {
            document.getElementById("languageSelection").style.display = "none";
            document.getElementById("profileSelection").style.display = "block";
        }
        
        function selectProfile(profile) {
            document.getElementById("profileSelection").style.display = "none";
            document.getElementById("epochSelection").style.display = "block";
        }
        
        function showMessage() {
            document.getElementById("epochSelection").style.display = "none";
            document.getElementById("message").style.display = "block";
        }
    </script>
</body>
</html>
