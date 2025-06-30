<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8" />
  <title>Profil utilisateur</title>
</head>
<body style="margin:0; font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; color: white; position: relative; min-height: 100vh; background: url('https://images.unsplash.com/photo-1506744038136-46273834b3fb?auto=format&fit=crop&w=1470&q=80') no-repeat center center fixed; background-size: cover;">

  <!-- Overlay flou + sombre -->
  <div style="position: fixed; top: 0; left: 0; width: 100vw; height: 100vh; 
              backdrop-filter: blur(12px); background-color: rgba(0,0,0,0.5); z-index: -1;"></div>

  <!-- Conteneur principal -->
  <div style="max-width: 480px; margin: 40px auto; padding: 20px; background: rgba(0,0,0,0.5); border-radius: 16px; box-shadow: 0 0 15px rgba(255,0,0,0.7);">

    <!-- Photo de profil -->
    <div style="position: relative; width: 120px; height: 120px; margin: 0 auto;">
      <img src="https://randomuser.me/api/portraits/men/32.jpg" alt="Avatar" 
           style="width: 120px; height: 120px; border-radius: 50%; border: 4px solid #ff0000; display: block; object-fit: cover;" />
      <div style="position: absolute; top: 8px; right: 8px; width: 24px; height: 24px; 
                  background: yellow; border-radius: 50%; display: flex; align-items: center; justify-content: center; font-weight: bold; color: #444; font-size: 16px; box-shadow: 0 0 6px #ff0;">
        ★
      </div>
    </div>

    <!-- Nom, ID, statut -->
    <h1 style="text-align: center; margin: 12px 0 4px;">Utilisateur#1234</h1>
    <p style="text-align: center; margin: 0 0 16px; font-style: italic; color: #ccc;">En ligne</p>

    <!-- Section "épuisant" -->
    <div style="display: flex; align-items: center; justify-content: space-between; background: rgba(255,255,255,0.1); padding: 10px 16px; border-radius: 12px;">
      
      <div style="display: flex; align-items: center; gap: 12px;">
        <img src="https://randomuser.me/api/portraits/women/44.jpg" alt="Petit avatar" 
             style="width: 48px; height: 48px; border-radius: 50%; object-fit: cover; border: 2px solid #fff;" />
        <div>
          <div style="font-weight: bold; font-size: 18px;">épuisant 😓🔥</div>
          <div style="font-size: 14px; color: #eee;">Déjà 2h que je tiens, mais c’est chaud...</div>
        </div>
      </div>

      <img src="https://images.unsplash.com/photo-1511671782779-c97d3d27a1d4?auto=format&fit=crop&w=80&q=80" alt="Album" 
           style="width: 56px; height: 56px; border-radius: 8px; object-fit: cover;" />
    </div>

    <!-- Bas de page - réseaux sociaux -->
    <div style="margin-top: 30px; text-align: center; display: flex; justify-content: center; gap: 24px;">
      <a href="https://twitter.com/" target="_blank" aria-label="Twitter" 
         style="color: white; text-decoration: none; font-size: 28px;">
        🐦
      </a>
      <a href="https://instagram.com/" target="_blank" aria-label="Instagram" 
         style="color: white; text-decoration: none; font-size: 28px;">
        📸
      </a>
      <a href="https://www.google.com" target="_blank" aria-label="Site web" 
         style="color: white; text-decoration: none; font-size: 28px;">
        🌐
      </a>
    </div>

    <!-- Compteur de vues -->
    <div aria-label="Nombre de vues" 
         style="position: fixed; bottom: 16px; left: 16px; background: rgba(0,0,0,0.5); 
                padding: 6px 12px; border-radius: 16px; font-weight: bold; color: #eee; font-size: 14px; box-shadow: 0 0 8px rgba(255,255,255,0.2);">
      14,367 vues
    </div>

  </div>

</body>
</html>
