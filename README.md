from flask import Flask

app = Flask(__name__)

@app.route("/")
def home():
    return """
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Site sur l'Autisme</title>
        <style>
            body {
                font-family: Arial, sans-serif;
                margin: 0;
                padding: 0;
                background-color: #f4f4f9;
                color: #333;
            }
            header {
                background-color: #0056b3;
                color: white;
                padding: 1em;
                text-align: center;
            }
            section {
                padding: 20px;
                max-width: 800px;
                margin: auto;
                line-height: 1.6;
            }
            footer {
                text-align: center;
                padding: 1em;
                background-color: #0056b3;
                color: white;
                position: fixed;
                bottom: 0;
                width: 100%;
            }
            a {
                color: #0056b3;
                text-decoration: none;
            }
            a:hover {
                text-decoration: underline;
            }
        </style>
    </head>
    <body>
        <header>
            <h1>Bienvenue sur le site de l'Autisme</h1>
        </header>
        <section>
            <h2>Qu'est-ce que l'autisme ?</h2>
            <p>L'autisme, ou trouble du spectre autistique (TSA), est une condition neurodéveloppementale qui affecte la manière dont une personne perçoit et interagit avec le monde. Les principales caractéristiques incluent :</p>
            <ul>
                <li>Difficultés de communication et d'interaction sociale.</li>
                <li>Comportements répétitifs ou intérêts spécifiques.</li>
                <li>Perception sensorielle atypique.</li>
            </ul>
            <h2>Ressources utiles</h2>
            <p>Voici quelques sites pour en savoir plus sur l'autisme :</p>
            <ul>
                <li><a href="https://www.autisme-france.fr" target="_blank">Autisme France</a></li>
                <li><a href="https://www.centres-ressources-autisme.fr" target="_blank">Centres de Ressources Autisme</a></li>
                <li><a href="https://www.fondation-autisme.org" target="_blank">Fondation Autisme</a></li>
            </ul>
        </section>
        <footer>
            <p>© 2025 Site sur l'Autisme - Tous droits réservés.</p>
        </footer>
    </body>
    </html>
    """

if __name__ == "__main__":
    app.run(debug=True)
    
