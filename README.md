<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Travaux Express</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>

  <header>
    <h1>Travaux Express</h1>
    <p>L’application mobile qui connecte clients et artisans en toute simplicité.</p>
    <a href="#inscription" class="cta-button">Devenir partenaire</a>
  </header>

  <section>
    <h2>Comment ça marche</h2>
    <div class="steps">
      <div>
        <h3>1. Inscription</h3>
        <p>Remplissez le formulaire pour rejoindre notre réseau.</p>
      </div>
      <div>
        <h3>2. Validation</h3>
        <p>Nous vérifions vos informations et activons votre profil.</p>
      </div>
      <div>
        <h3>3. Missions</h3>
        <p>Recevez des demandes de clients dans votre zone.</p>
      </div>
    </div>
  </section>

  <section id="inscription">
    <h2>Formulaire d’inscription</h2>
    <form action="https://formspree.io/f/xeopgnbj" method="post">
      <input type="text" name="nom" placeholder="Nom / Prénom" required>
      <input type="text" name="entreprise" placeholder="Nom de l’entreprise">
      <input type="text" name="metier" placeholder="Métier / Spécialité" required>
      <input type="text" name="zone" placeholder="Zone d’intervention" required>
      <input type="email" name="email" placeholder="Email" required>
      <input type="tel" name="telephone" placeholder="Téléphone">
      <textarea name="message" placeholder="Message complémentaire"></textarea>
      <label><input type="checkbox" name="newsletter"> Je souhaite être informé des nouveautés</label>
      <button type="submit">Envoyer ma demande</button>
    </form>
  </section>

  <section>
    <h2>Services supplémentaires</h2>
    <a href="https://buy.stripe.com/test_8x24gA05X1G862WgwZfQI00" class="cta-button" target="_blank">💳 Paiement sécurisé</a>
    <a href="mailto:travauxexpress@laposte.net" class="cta-button">📧 Contactez-nous</a>
  </section>

  <footer>
    <div id="clock"></div>
    📧 travauxexpress@laposte.net 
    <a href="https://formspree.io/f/xeopgnb">Mentions légales</a> | <a href="https://formspree.io/f/xeopgnb">Politique de confidentialité</a> | <a href="https://formspree.io/f/xeopgnb">CGU</a>
  </footer>

  <script>
    document.querySelector("form").addEventListener("submit", function(e) {
      const email = document.querySelector("input[name='email']").value;
      if (!email.includes("@")) {
        alert("Veuillez entrer un email valide.");
        e.preventDefault();
      }
    });

    if ("geolocation" in navigator) {
      navigator.geolocation.getCurrentPosition(function(position) {
        const zoneInput = document.querySelector("input[name='zone']");
        zoneInput.value = `Lat: ${position.coords.latitude}, Long: ${position.coords.longitude}`;
      });
    }

    function updateClock() {
      const now = new Date();
      document.getElementById("clock").textContent = now.toLocaleTimeString();
    }
    setInterval(updateClock, 1000);
    updateClock();
  </script>

</body>
</html>
<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Informations légales – Travaux Express</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f4f4f4;
      margin: 0;
      padding: 0;
    }
    .container {
      max-width: 900px;
      margin: auto;
      padding: 20px;
      background: #fff;
    }
    h1, h2, h3 {
      color: #333;
      text-align: center;
      margin-top: 40px;
    }
    p, ul, li {
      color: #555;
      line-height: 1.6;
    }
    ul {
      padding-left: 20px;
    }
    .section {
      margin-top: 40px;
    }
    .highlight {
      background: #eaf4ff;
      padding: 10px;
      border-left: 4px solid #007BFF;
      margin-bottom: 20px;
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>🔐 Politique de confidentialité</h1>
    <div class="highlight">
      Travaux Express respecte votre vie privée :
      <ul>
        <li>Vos données sont utilisées uniquement pour le bon fonctionnement de l’application.</li>
        <li>Aucune information personnelle n’est vendue à des tiers.</li>
        <li>Vous pouvez à tout moment demander la suppression de votre compte et de vos données.</li>
        <li>Les paiements sont sécurisés via Stripe ou PayPal.</li>
      </ul>
    </div>

    <div class="section">
      <h2>📜 Conditions Générales d’Utilisation (CGU)</h2>
      <p><strong>Dernière mise à jour :</strong> [date]</p>
      <ul>
        <li><strong>1. Objet :</strong> Travaux Express est une plateforme de mise en relation entre clients et partenaires professionnels.</li>
        <li><strong>2. Utilisateurs :</strong> Clients publient des demandes, partenaires y répondent via forfait ou abonnement.</li>
        <li><strong>3. Engagements :</strong> Respect des règles, exactitude des informations, prestations conformes.</li>
        <li><strong>4. Paiement :</strong> Réponses payantes via Stripe ou PayPal.</li>
        <li><strong>5. Responsabilité :</strong> Travaux Express n’intervient pas dans la réalisation des travaux.</li>
        <li><strong>6. Suspension / Résiliation :</strong> Comportement abusif = suspension ou suppression du compte.</li>
      </ul>
    </div>

    <div class="section">
      <h2>📘 À propos</h2>
      <p>Travaux Express, c’est la solution simple et rapide pour trouver un professionnel du bâtiment près de chez vous. Notre mission : faciliter la mise en relation entre particuliers et artisans qualifiés, en toute transparence.</p>
      <p>Que vous soyez client ou partenaire, notre plateforme vous accompagne à chaque étape : publication, réponse, paiement sécurisé, suivi.</p>
      <p>Travaux Express est une initiative indépendante, née de la volonté de moderniser le secteur des petits et grands travaux.</p>
    </div>

    <div class="section">
      <h2>❓ FAQ</h2>
      <ul>
        <li><strong>Comment publier une demande ?</strong> Créez un compte client, remplissez le formulaire, validez.</li>
        <li><strong>Qui peut répondre aux demandes ?</strong> Les partenaires inscrits avec forfait ou abonnement.</li>
        <li><strong>Pourquoi payer pour répondre ?</strong> Pour garantir des échanges sérieux et limiter le spam.</li>
        <li><strong>Comment sont sélectionnés les partenaires ?</strong> Validation manuelle selon métier, zone et références.</li>
        <li><strong>Que se passe-t-il après une réponse ?</strong> Le client est notifié et peut accepter ou refuser.</li>
        <li><strong>Puis-je annuler une demande ?</strong> Oui, depuis le tableau de bord client.</li>
        <li><strong>Mes données sont-elles protégées ?</strong> Oui, Travaux Express respecte le RGPD.</li>
      </ul>
    </div>
  </div>
</body>
</html>
