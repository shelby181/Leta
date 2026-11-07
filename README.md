<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Juste pour toi ❤️</title>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    min-height: 100vh;
    background: #0d0b12;
    color: white;
    font-family: Georgia, serif;
    padding: 30px 18px;
    overflow-x: hidden;
}

.container {
    width: 100%;
    max-width: 460px;
    margin: 35px auto;
    text-align: center;
}

.top {
    color: #d6b46a;
    font-size: 11px;
    letter-spacing: 5px;
    margin-bottom: 35px;
}

h1 {
    color: #e6c477;
    font-size: 32px;
    font-weight: normal;
    margin-bottom: 18px;
}

.intro {
    color: #c9bdc8;
    font-size: 15px;
    line-height: 1.9;
    margin-bottom: 35px;
}

.line {
    width: 65px;
    height: 1px;
    background: #d6b46a;
    margin: 25px auto;
}

.main-card {
    background: linear-gradient(145deg, #1c1722, #151019);
    border: 1px solid #55452a;
    border-radius: 24px;
    padding: 28px 20px;
    box-shadow: 0 15px 45px #0008;
}

.heart {
    font-size: 45px;
    color: #e6a1b7;
    margin-bottom: 18px;
    animation: beat 2s infinite;
}

@keyframes beat {
    50% {
        transform: scale(1.13);
    }
}

.subtitle {
    color: #e6c477;
    font-size: 19px;
    font-weight: normal;
    margin-bottom: 25px;
}

.choice {
    display: block;
    width: 100%;
    padding: 17px 12px;
    margin: 13px 0;
    background: #211a26;
    border: 1px solid #76603c;
    border-radius: 14px;
    color: #f3d9e4;
    font-family: Georgia, serif;
    font-size: 15px;
    cursor: pointer;
    transition: .3s;
}

.choice:active {
    background: #493044;
    transform: scale(.97);
}

.message {
    display: none;
    background: #211a26;
    border: 1px solid #8d6d49;
    border-radius: 16px;
    padding: 25px 19px;
    margin: 15px 0 22px;
    text-align: left;
    color: #eee0e9;
    font-size: 15px;
    line-height: 2;
    animation: appear .8s ease;
    overflow-wrap: break-word;
}

.message h2 {
    text-align: center;
    color: #e6c477;
    font-size: 21px;
    font-weight: normal;
    margin-bottom: 18px;
}

.message .signature {
    color: #e6c477;
    text-align: center;
    margin-top: 22px;
    font-style: italic;
}

@keyframes appear {
    from {
        opacity: 0;
        transform: translateY(18px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

footer {
    color: #a18e9d;
    font-size: 10px;
    letter-spacing: 3px;
    margin-top: 35px;
    line-height: 2;
}

@media(max-width: 380px) {
    h1 {
        font-size: 27px;
    }

    .main-card {
        padding: 23px 15px;
    }
}
</style>
</head>

<body>

<div class="container">

    <div class="top">UNE PETITE ATTENTION</div>

    <h1>Juste pour toi</h1>

    <p class="intro">
        J'ai quelques mots à te laisser...
        <br>
        Chacun d'eux a une petite place dans mon cœur.
        <br>
        À toi de les découvrir. ❤️
    </p>

    <div class="line"></div>

    <div class="main-card">

        <div class="heart">♥</div>

        <h2 class="subtitle">Choisis ton petit message</h2>

        <button class="choice" data-message="message1">
            ✦ Je t'aime ❤️
        </button>

        <div class="message" id="message1">
            <h2>Je t'aime ❤️</h2>

            Trois petits mots, mais derrière eux
            se cache un sentiment que les mots
            ne pourront jamais entièrement expliquer.
        </div>

        <button class="choice" data-message="message2">
            ✦ Et même si je te l'ai dit... 💗
        </button>

        <div class="message" id="message2">
            <h2>Et même si... 💗</h2>

            Et même si je te l'ai dit 1 million de fois,
            je ne me lasserai jamais de te le rappeler.
            Tu mérites de savoir combien tu es importante
            pour moi.
        </div>

        <button class="choice" data-message="message3">
            ✦ Quelques mots du cœur 💌
        </button>

        <div class="message" id="message3">
            <h2>À toi, Manmi ❤️</h2>

            Je sais que je te l'ai déjà dit un million
            de fois, mais je le pense sincèrement.

            Je suis tombé amoureux de chaque partie de toi.

            Je n'ai jamais connu un bonheur pareil à celui
            que je ressens quand nous sommes ensemble.

            Le simple fait de t'entendre parler ou de te
            voir sourire fait briller quelque chose en moi,
            même dans mes journées les plus sombres.

            Je t'aime de tout mon cœur.

            <div class="signature">
                Avec amour, Papi ❤️
            </div>
        </div>

    </div>

    <footer>
        FAIT AVEC AMOUR
        <br>
        10 NOVEMBRE 2026
    </footer>

</div>

<script>
document.addEventListener("DOMContentLoaded", function() {

    const boutons = document.querySelectorAll(".choice");

    boutons.forEach(function(bouton) {

        bouton.addEventListener("click", function() {

            const id = bouton.getAttribute("data-message");
            const message = document.getElementById(id);

            if (message.style.display === "block") {
                message.style.display = "none";
            } else {
                message.style.display = "block";

                setTimeout(function() {
                    message.scrollIntoView({
                        behavior: "smooth",
                        block: "nearest"
                    });
                }, 100);
            }

        });

    });

});
</script>

</body>
</html>
