<!DOCTYPE html>
<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Videospiel Quiz</title>
    <style>
        body {
    margin: 0;
    padding: 0;
    height: 100vh; /* Der Hintergrund nimmt die gesamte Höhe des Bildschirms ein */
    background-size: cover; /* Bild wird auf den gesamten Bildschirm angepasst */
    background-position: center center; /* Bild bleibt zentriert */
    background-attachment: fixed; /* Bild bleibt fixiert, wenn die Seite gescrollt wird */
    background-repeat: no-repeat; /* Verhindert, dass das Bild wiederholt wird */
            font-family: Arial, sans-serif;
            background-color: #030303;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            padding: 0;
            background-size: cover; /* Das Bild wird so skaliert, dass es den gesamten Bildschirm ausfüllt */
            background-position: center center; /* Das Bild wird zentriert */
            background-attachment: fixed; /* Das Bild bleibt beim Scrollen fixiert */
            background-repeat: no-repeat; /* Das Bild wiederholt sich nicht */
        }

        .container {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100%; /* Container füllt die gesamte Bildschirmhöhe */
            color: white;
            text-align: center;
            font-family: Arial, sans-serif;
            max-width: 600px;
            margin: 20px;
            display: none; /* Fragen sind zunächst ausgeblendet */
        }
        .container.active {
            display: block; /* Aktivierte Fragen werden angezeigt */
        }

        .question {
            font-size: 1.5em;
            margin-bottom: 20px;
            color: #fcfcfc;
        }
        .answers {
            font-size: 1.2em;
            margin: 20px 0;
            text-align: left;
            display: inline-block;
        }
        .answers div {
            margin: 10px 0;
        }
        .button {
            font-size: 1.2em;
            padding: 10px 20px;
            background-color: #007bff;
            color: white;
            border: none;
            cursor: pointer;
            margin-top: 20px;
            border-radius: 5px;
        }
        .button:hover {
            background-color: #0056b3;
        }
    </style>
</head>
<body>
    <form id="quizForm">
        <!-- Frage 1 -->
        <div class="container active" id="question1">
            <div class="question">
                <h3>Frage 1: In welchem Jahr wurde das erste Spiel der „Final Fantasy“-Reihe veröffentlicht?</h3>
                <div class="answers">
                    <div>A) 1987</div>
                    <div>B) 1990</div>
                    <div>C) 1984</div>
                    <div>D) 1992</div>
                </div>
            </div>
            <button type="button" class="button" onclick="nextQuestion('z1')">Weiter zur nächsten Frage</button>
        </div>

 <!-- Zusatzfrage 1 -->
 <div class="container" id="z1">
    <div class="question">
        <h3>Zusatzfrage 1: Welches dieser Spiele wurde zuerst veröffentlicht?</h3>
        <div class="answers">
            <div>1) Super Mario Bros.</div>
            <div>2) Sonic the Hedgehog</div>
            <div>3) Pac-Man</div>
            <div>4) Donkey Kong</div>
        </div>
    </div>
    <button type="button" class="button" onclick="prevQuestion(1)">Zurück</button>
    <button type="button" class="button" onclick="nextQuestion(2)">Weiter zur nächsten Frage</button>
    </div>

                    <!-- Frage 2 -->
                <div class="container" id="question2">
             <div class="question">
             <h3>Frage 2: Wie viele „The Legend of Zelda“-Spiele wurden bis 2024 offiziell veröffentlicht?</h3>
            <div class="answers">
            <div>A) 22</div>
            <div>B) 21</div>
            <div>C) 19</div>
            <div>D) 20</div>
        </div>
    </div>
    <button type="button" class="button" onclick="prevQuestion('z1')">Zurück</button>
    <button type="button" class="button" onclick="nextQuestion('z2')">Weiter zur nächsten Frage</button>
    </div>

 <!-- Zusatzfrage 2 -->
 <div class="container" id="z2">
    <div class="question">
        <h3>Zusatzfrage 2: In „The Witcher 3: Wild Hunt“ gehört Geralt von Riva welcher Gilde an?</h3>
        <div class="answers">
            <div>1) Die Viper-Schule</div>
            <div>2) Die Wolfsschule</div>
            <div>3) Die Greifenschule</div>
            <div>4) Die Katzenschule</div>
        </div>
     </div>
     <button type="button" class="button" onclick="prevQuestion(2)">Zurück</button>
    <button type="button" class="button" onclick="nextQuestion(3)">Weiter zur nächsten Frage</button>
    </div>

<!-- Frage 3 -->
<div class="container" id="question3">
    <div class="question">
        <h3>Frage 3: Welches Videospielstudio entwickelte das berühmte Spiel „Half-Life“?</h3>
        <div class="answers">
            <div>A) id Software</div>
            <div>B) Valve</div>
            <div>C) Bethesda</div>
            <div>D) Bungie</div>
        </div>
    </div>
    <button type="button" class="button" onclick="prevQuestion('z2')">Zurück</button>
<button type="button" class="button" onclick="nextQuestion('z3')">Weiter zur nächsten Frage</button>
        </div>

        <!-- Zusatzfrage 3 -->
        <div class="container" id="z3">
            <div class="question">
                <h3>Zusatzfrage 3: Welcher Charakter aus „Street Fighter“ ist für den „Hadouken“-Angriff bekannt?</h3>
                <div class="answers">
                    <div>1) Ken</div>
                    <div>2) Chun-Li</div>
                    <div>3) Guile</div>
                    <div>4) Ryu</div>
                </div>
            </div>
            <button type="button" class="button" onclick="prevQuestion(3)">Zurück</button>
            <button type="button" class="button" onclick="nextQuestion(4)">Weiter zur nächsten Frage</button>
        </div>

         <!-- Frage 4 -->
         <div class="container" id="question4">
            <div class="question">
                <h3>Frage 4: In welchem Spiel taucht die Figur „Ciri“ als spielbarer Charakter auf?</h3>
                <div class="answers">
                    <div>A) The Witcher 3: Wild Hunt</div>
                    <div>B) Dragon Age: Inquisition</div>
                    <div>C) Dark Souls III</div>
                    <div>D) Elder Scrolls V: Skyrim</div>
                </div>
            </div>
            <button type="button" class="button" onclick="prevQuestion('z3')">Zurück</button>
            <button type="button" class="button" onclick="nextQuestion('z4')">Weiter zur nächsten Frage</button>
        </div>

        <!-- Zusatzfrage 4 -->
         <div class="container" id="z4">
            <div class="question">
                <h3>Zusatzfrage 4: In welcher Stadt spielt der größte Teil von „Grand Theft Auto: Vice City“?</h3>
                <div class="answers">
                    <div>1) Liberty City</div>
                    <div>2) Los Santos</div>
                    <div>3) Vice City</div>
                    <div>4) San Fierro</div>
                </div>
            </div>
            <button type="button" class="button" onclick="prevQuestion(4)">Zurück</button>
            <button type="button" class="button" onclick="nextQuestion(5)">Weiter zur nächsten Frage</button>
        </div>

 <!-- Frage 5 -->
 <div class="container" id="question5">
    <div class="question">
        <h3>Frage 5: Welches dieser Spiele wurde nicht von Nintendo entwickelt?</h3>
        <div class="answers">
            <div>A) Pokémon Rot</div>
            <div>B) Animal Crossing</div>
            <div>C) Sonic the Hedgehog</div>
            <div>D) The Legend of Zelda: Wind Waker</div>
        </div>
    </div>
    <button type="button" class="button" onclick="prevQuestion('z4')">Zurück</button>
    <button type="button" class="button" onclick="nextQuestion('z5')">Weiter zur nächsten Frage</button>
</div>

 <!-- Zusatzfrage 5 -->
 <div class="container" id="z5">
    <div class="question">
        <h3>Zusatzfrage 5: In „Metal Gear Solid“ kämpft der Spieler gegen einen Boss, der die Gedanken des Spielers liest. Wer ist dieser Boss?</h3>
        <div class="answers">
            <div>1) Liquid Snake</div>
            <div>2) Vulcan Raven</div>
            <div>3) Psycho Mantis</div>
            <div>4) Revolver Ocelot</div>
        </div>
    </div>
    <button type="button" class="button" onclick="prevQuestion(5)">Zurück</button>
    <button type="button" class="button" onclick="nextQuestion(6)">Weiter zur nächsten Frage</button>
</div>

<!-- Frage 6 -->
<div class="container" id="question6">
    <div class="question">
        <h3>Frage 6: In welcher fiktiven Welt spielt das „Dark Souls“-Franchise hauptsächlich?</h3>
        <div class="answers">
            <div>A) Drangleic</div>
            <div>B) Boletaria</div>
            <div>C) Lordran</div>
            <div>D) Farron</div>
        </div>
    </div>
    <button type="button" class="button" onclick="prevQuestion('z5')">Zurück</button>
    <button type="button" class="button" onclick="nextQuestion('z6')">Weiter zur nächsten Frage</button>
</div>

<!-- Zusatzfrage 6 -->
<div class="container" id="z6">
    <div class="question">
        <h3>Zusatzfrage 6: Wie lautet der volle Name des Charakters „Lara Croft“?</h3>
        <div class="answers">
            <div>1) Lara Anne Croft</div>
            <div>2) Lara Elizabeth Croft</div>
            <div>3) Lara Amelia Croft</div>
            <div>4) Lara Catherine Croft</div>
        </div>
    </div>
    <button type="button" class="button" onclick="prevQuestion(6)">Zurück</button>
    <button type="button" class="button" onclick="nextQuestion(7)">Weiter zur nächsten Frage</button>
</div>

<!-- Frage 7 -->
<div class="container" id="question7">
    <div class="question">
        <h3>Frage 7: Welches Spiel wurde als erstes kommerzielles 3D-Spiel angesehen?</h3>
        <div class="answers">
            <div>A) Wolfenstein 3D</div>
            <div>B) DOOM</div>
            <div>C) Battlezone</div>
            <div>D) Quake</div>
        </div>
    </div>
    <button type="button" class="button" onclick="prevQuestion('z6')">Zurück</button>
    <button type="button" class="button" onclick="nextQuestion('z7')">Weiter zur nächsten Frage</button>
</div>

<!-- Zusatzfrage 7 -->
<div class="container" id="z7">
    <div class="question">
        <h3>Zusatzfrage 7: Welche der folgenden Figuren ist kein Charakter aus „Overwatch“?</h3>
        <div class="answers">
            <div>1) Mercy</div>
            <div>2) Tracer</div>
            <div>3) Illidan</div>
            <div>4) Hanzo</div>
        </div>
    </div>
    <button type="button" class="button" onclick="prevQuestion(7)">Zurück</button>
    <button type="button" class="button" onclick="nextQuestion(8)">Weiter zur nächsten Frage</button>
</div>

<!-- Frage 8 -->
<div class="container" id="question8">
    <div class="question">
        <h3>Frage 8: Wie heißt die Stadt, die im ersten „Resident Evil“-Spiel erkundet wird?</h3>
        <div class="answers">
            <div>A) Racoon City</div>
            <div>B) Sheena Island</div>
            <div>C) Rockfort Island</div>
            <div>D) Los Iluminados Village</div>
        </div>
    </div>
    <button type="button" class="button" onclick="prevQuestion('z7')">Zurück</button>
    <button type="button" class="button" onclick="nextQuestion('z8')">Weiter zur nächsten Frage</button>
</div>

<!-- Zusatzfrage 8 -->
<div class="container" id="z8">
    <div class="question">
        <h3>Zusatzfrage 8: In welchem Jahr wurde die Xbox 360 veröffentlicht?</h3>
        <div class="answers">
            <div>1) 2004</div>
            <div>2) 2006</div>
            <div>3) 2005</div>
            <div>4) 2007</div>
        </div>
    </div>
    <button type="button" class="button" onclick="prevQuestion(8)">Zurück</button>
    <button type="button" class="button" onclick="nextQuestion(9)">Weiter zur nächsten Frage</button>
</div>

<!-- Frage 9 -->
<div class="container" id="question9">
    <div class="question">
        <h3>Frage 9: Was war das erste Spiel, das 100 Millionen Dollar Umsatz machte?</h3>
        <div class="answers">
            <div>A) Pac-Man</div>
            <div>B) Super Mario Bros</div>
            <div>C) Street Fighter II</div>
            <div>D) Space Invaders</div>
        </div>
    </div>
    <button type="button" class="button" onclick="prevQuestion('z8')">Zurück</button>
    <button type="button" class="button" onclick="nextQuestion('z9')">Weiter zur nächsten Frage</button>
</div>

<!-- Zusatzfrage 9 -->
<div class="container" id="z9">
    <div class="question">
        <h3>Zusatzfrage 9: Welcher Charakter aus „League of Legends“ ist als „The Blind Monk“ bekannt?</h3>
        <div class="answers">
            <div>1) Jax</div>
            <div>2) Yasuo</div>
            <div>3) Lee Sin</div>
            <div>4) Zed</div>
        </div>
    </div>
    <button type="button" class="button" onclick="prevQuestion(9)">Zurück</button>
    <button type="button" class="button" onclick="nextQuestion(10)">Weiter zur nächsten Frage</button>
</div>

<!-- Frage 10 -->
<div class="container" id="question10">
    <div class="question">
        <h3>Frage 10: In welchem Spiel gehört die Map „Dust II“ zu den bekanntesten?</h3>
        <div class="answers">
            <div>A) Call of Duty</div>
            <div>B) Counter-Strike</div>
            <div>C) Overwatch</div>
            <div>D) Rainbow Six Siege</div>
        </div>
    </div>
    <button type="button" class="button" onclick="prevQuestion('z9')">Zurück</button>
    <button type="button" class="button" onclick="nextQuestion('z10')">Weiter zur nächsten Frage</button>
</div>

<!-- Zusatzfrage 10 -->
<div class="container" id="z10">
    <div class="question">
        <h3>Zusatzfrage 10: Wie heißt der Hauptcharakter von „Red Dead Redemption 2“?</h3>
        <div class="answers">
            <div>1) John Marston</div>
            <div>2) Dutch van der Linde</div>
            <div>3) Arthur Morgan</div>
            <div>4) Micah Bell</div>
        </div>
        <button type="button" class="button" onclick="prevQuestion(10)">Zurück</button>
    </div>
</div>

<script>
    let currentQuestion = "question1"; // Start mit Frage 1
    const questionHistory = [currentQuestion]; // Liste zur Speicherung der Historie

    function nextQuestion(next) {
        // Verstecke die aktuelle Frage
        document.getElementById(currentQuestion).classList.remove('active');

        // Zeige die nächste Frage
        currentQuestion = next.toString().startsWith("z") ? next : "question" + next;
        document.getElementById(currentQuestion).classList.add('active');

        // Füge die neue Frage zur Historie hinzu
        questionHistory.push(currentQuestion);
    }

    function prevQuestion() {
        if (questionHistory.length > 1) {
            // Entferne die aktuelle Frage aus der Historie
            questionHistory.pop();

            // Gehe zur letzten Frage in der Historie zurück
            document.getElementById(currentQuestion).classList.remove('active');
            currentQuestion = questionHistory[questionHistory.length - 1];
            document.getElementById(currentQuestion).classList.add('active');
        }
    }
</script>
</body>
</html>
