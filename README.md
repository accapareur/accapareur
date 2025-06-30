<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Interface Accapareur</title>
<style>
  /* Reset & basics */
  * {
    box-sizing: border-box;
  }
  body, html {
    margin: 0; padding: 0; height: 100%;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    color: white;
    overflow: hidden;
  }

  /* Background image with blur and dark overlay */
  body {
    position: relative;
    background: url('https://images.unsplash.com/photo-1506744038136-46273834b3fb?auto=format&fit=crop&w=1470&q=80') no-repeat center/cover;
  }
  body::before {
    content: "";
    position: fixed;
    top:0; left:0; right:0; bottom:0;
    background: inherit;
    filter: blur(12px) brightness(0.4);
    z-index: -2;
  }
  body::after {
    content: "";
    position: fixed;
    top:0; left:0; right:0; bottom:0;
    background: rgba(0,0,0,0.5);
    z-index: -1;
  }

  /* Container centrée verticale et horizontale */
  .container {
    height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: flex-start;
    padding-top: 50px;
    position: relative;
  }

  /* Profil principal */
  .profile-pic {
    width: 130px; height: 130px;
    border-radius: 50%;
    border: 5px solid #FF4444; /* rouge */
    position: relative;
    overflow: hidden;
    background: #a00;
  }
  .profile-pic img {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }
  /* Etoile en coin */
  .profile-pic::after {
    content: "⭐";
    position: absolute;
    top: 5px;
    right: 8px;
    font-size: 28px;
    filter: drop-shadow(0 0 1px black);
  }

  /* Nom utilisateur */
  .username {
    margin-top: 15px;
    font-size: 2.8rem;
    font-weight: 700;
    text-align: center;
  }

  /* ID */
  .user-id {
    margin-top: 4px;
    font-size: 0.95rem;
    color: #bbb;
    text-align: center;
  }

  /* Statut */
  .status-text {
    margin-top: 15px;
    max-width: 380px;
    font-size: 1.2rem;
    font-style: italic;
    text-align: center;
    line-height: 1.3;
  }

  /* Section épuisant (à gauche du centre, vers milieu page) */
  .section-epuisant {
    position: absolute;
    top: 50%;
    left: 10%;
    transform: translateY(-50%);
    display: flex;
    align-items: center;
    gap: 12px;
    color: white;
    max-width: 300px;
  }
  .epuisant-icon {
    width: 48px;
    height: 48px;
    border-radius: 50%;
    background: #444;
    overflow: hidden;
    flex-shrink: 0;
  }
  .epuisant-icon img {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }
  .epuisant-texts {
    display: flex;
    flex-direction: column;
    gap: 4px;
    flex-grow: 1;
  }
  .epuisant-main {
    font-weight: 700;
    font-size: 1.3rem;
    display: flex;
    align-items: center;
    gap: 6px;
  }
  .epuisant-main span.emoji {
    font-size: 1.3rem;
  }
  .listening-to {
    font-size: 0.9rem;
    opacity: 0.8;
  }
  .artist-name {
    font-weight: 600;
    font-size: 1rem;
    margin-top: 2px;
  }
  .album-art {
    width: 60px;
    height: 60px;
    border-radius: 8px;
    overflow: hidden;
    margin-left: 10px;
    flex-shrink: 0;
    box-shadow: 0 0 8px rgba(255,255,255,0.2);
  }
  .album-art img {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }

  /* Bas de page, icônes sociales centrées */
  .footer-socials {
    position: fixed;
    bottom: 30px;
    left: 50%;
    transform: translateX(-50%);
    display: flex;
    gap: 25px;
  }
  .footer-socials a {
    color: white;
    font-size: 28px;
    transition: color 0.3s;
  }
  .footer-socials a:hover {
    color: #ff4444;
  }

  /* Compteur de vues en bas à gauche */
  .view-counter {
    position: fixed;
    bottom: 28px;
    left: 20px;
    font-weight: 700;
    font-size: 1.1rem;
    background: rgba(255,255,255,0.15);
    padding: 6px 14px;
    border-radius: 20px;
    user-select: none;
    letter-spacing: 1.2px;
  }

  /* Icônes sociales SVG inline (GitHub, Discord, Instagram, Globe) */
  /* Utilisation d'icônes simples en SVG */
</style>
</head>
<body>

<div class="container">
  <!-- Photo de profil -->
  <div class="profile-pic" title="Profil Accapareur">
    <img src="https://i.pravatar.cc/130?img=15" alt="Avatar rouge avec étoile"/>
  </div>

  <!-- Nom utilisateur -->
  <div class="username">accapareur</div>

  <!-- ID -->
  <div class="user-id">ID 622,934</div>

  <!-- Texte de statut -->
  <div class="status-text">Money doesn't buy happiness, but I want to cry in an Aston</div>
</div>

<!-- Section épuisant à gauche du centre -->
<div class="section-epuisant" aria-label="Statut épuisant">
  <div class="epuisant-icon" title="Profil petit">
    <img src="https://i.pravatar.cc/48?img=32" alt="Petit avatar rond" />
  </div>
  <div class="epuisant-texts">
    <div class="epuisant-main">
      épuisant <span class="emoji">😭 😡 😱</span>
    </div>
    <div class="listening-to">Listening to</div>
    <div class="artist-name">by АСАЈЅ ToJIb</div>
  </div>
  <div class="album-art" title="Album cover">
    <img src="https://i.pinimg.com/736x/24/82/b2/2482b2e6b7ef6cc5b7b39e444b8f42eb.jpg" alt="Album Art"/>
  </div>
</div>

<!-- Bas de page icônes sociales -->
<div class="footer-socials" role="contentinfo" aria-label="Réseaux sociaux">
  <a href="https://github.com/" target="_blank" rel="noopener" aria-label="GitHub">
    <svg height="28" viewBox="0 0 16 16" width="28" fill="currentColor" aria-hidden="true"><path fill-rule="evenodd" d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.58.82-2.14-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82a7.7 7.7 0 012.01-.27c.68 0 1.36.09 2.01.27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.14 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0016 8c0-4.42-3.58-8-8-8z"></path></svg>
  </a>
  <a href="https://discord.com/" target="_blank" rel="noopener" aria-label="Discord">
    <svg height="28" viewBox="0 0 245 240" width="28" fill="currentColor" aria-hidden="true"><path d="M104.4 120.8c-5.7 0-10.3-4.9-10.3-10.9 0-6 4.6-10.9 10.3-10.9 5.7 0 10.3 4.9 10.3 10.9 0 6-4.6 10.9-10.3 10.9zm36.2 0c-5.7 0-10.3-4.9-10.3-10.9 0-6 4.6-10.9 10.3-10.9 5.7 0 10.3 4.9 10.3 10.9 0 6-4.6 10.9-10.3 10.9z"/><path d="M189.5 20H55.4C35.8 20 20 36.7 20 56.9v126.2c0 20.2 15.8 36.9 35.4 36.9h99.5l-4.6-15.9 11 10.3 10.3 9.5 18.2 15.9V56.9c0-20.2-15.8-36.9-35.4-36.9zM141 160.4s-4.2-5 6-9.6c11.6-5 20.3-16.2 20.3-16.2-1.5 1.1-3 2.1-4.4 3-19.8 13.1-34.3 16.6-43 16-3.2-.2-6.3-.6-9.1-1.1-2.4-.4-4.6-.9-6.6-1.4l-1.5-9.2c11.2 2.9 19.7 3.5 19.7 3.5-14.2-7.6-19.7-16-19.7-16 13-7.6 22.4-17.3 22.4-17.3-20.5 4.1-28.3 10.2-28.3 10.2-7.7 4.8-13 10.9-13 10.9l-21.6-7.1 4.9 16.5c0 0 8.5 24.4 41.4 29.4 25.2 3.6 39.2-4.5 39.2-4.5z"/></svg>
  </a>
  <a href="https://instagram.com/" target="_blank" rel="noopener" aria-label="Instagram">
    <svg height="28" viewBox="0 0 512 512" width="28" fill="currentColor" aria-hidden="true"><path d="M349.33 69.33h-186.66C102.19 69.33 69.33 102.19 69.33 162.67v186.66c0 60.48 32.85 93.33 93.34 93.33h186.66c60.48 0 93.34-32.85 93.34-93.33v-186.66c0-60.48-32.86-93.34-93.34-93.34zm62.07 280.9c0 34.07-22.21 56.28-56.27 56.28h-153.3c-34.07 0-56.28-22.21-56.28-56.27v-100.57h44.91c-2.13 7.89-3.23 16.29-3.23 25.03 0 50.94 41.36 92.3 92.3 92.3 8.74 0 17.14-1.1 25.03-3.23v44.91zm-45.3-94.5c0-24.28-19.73-44-44-44-24.28 0-44 19.72-44 44 0 24.27 19.72 44 44 44 24.27 0 44-19.73 44-44z"/></svg>
  </a>
  <a href="https://www.google.com" target="_blank" rel="noopener" aria-label="Site web">
    <svg height="28" viewBox="0 0 24 24" width="28" fill="currentColor" aria-hidden="true"><path d="M12 2a10 10 0 1010 10A10 10 0 0012 2zm5.94 8h-2.05a6.07 6.07 0 00-1.55-4.04 7.86 7.86 0 012.84 2.44zM12 4.07a8.06 8.06 0 015.1 1.89 8.15 8.15 0 00-8.08 8.08A8.08 8.08 0 0112 4.07zM4.08 12a7.87 7.87 0 011.92-4.9 6.06 6.06 0 00-3.14 4.25A7.81 7.81 0 014.08 12zm-.02 1.93a7.91 7.91 0 01-1.52 4.5 6.12 6.12 0 003.09-4.26A7.84 7.84 0 014.06 13.93zM6.62 16.4a7.92 7.92 0 011.49 4.46 7.89 7.89 0 01-3.16-4.24 7.7 7.7 0 011.67-.22zm9.17 0a7.67 7.67 0 011.67.21 7.92 7.92 0 01-3.15 4.24 7.92 7.92 0 011.48-4.46z"/></svg>
  </a>
</div>

<!-- Compteur de vues -->
<div class="view-counter" aria-label="Nombre de vues">
  14****
</div>

</body>
</html>
