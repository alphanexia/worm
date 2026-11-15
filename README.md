# 💥 Grubz Arena

Jeu d'artillerie au tour par tour sur navigateur. Terrain destructible, vent, 6 armes, **2 à 6 joueurs en ligne**. Se joue sur Android, iPhone et PC directement depuis le site, sans rien installer.

## Mise en ligne sur GitHub Pages (5 minutes)

1. Crée un compte sur https://github.com si tu n'en as pas.
2. Clique sur **New repository** → nomme-le `grubz-arena` → **Public** → **Create repository**.
3. Clique sur **uploading an existing file**, glisse `index.html` (et ce `README.md`), puis **Commit changes**.
4. Va dans **Settings → Pages** → *Source* : **Deploy from a branch** → branche **main**, dossier **/ (root)** → **Save**.
5. Attends environ 1 minute. Ton jeu est en ligne à l'adresse :
   `https://TON-PSEUDO.github.io/grubz-arena/`

## Jouer entre amis

1. Ouvre le lien, choisis un pseudo et appuie sur **Créer une partie en ligne**.
2. Appuie sur **📤 Partager le lien d'invitation** et envoie-le (WhatsApp, SMS…). Tes amis peuvent aussi taper le code à 5 lettres.
3. Quand tout le monde est dans le salon (6 max), appuie sur **Lancer la partie**.

Tu peux aussi ajouter des joueurs **sur le même appareil** (bouton « + Ajouter un joueur sur cet appareil »), ou lancer une **Partie locale** où tout le monde joue sur un seul écran en se passant le téléphone.

## Commandes

| Action | Tactile | Clavier |
|---|---|---|
| Se déplacer | ◀ ▶ | ← → |
| Viser | ▲ ▼ | ↑ ↓ |
| Sauter | ⤴ | Entrée |
| Tirer | maintenir **FEU** pour doser la puissance, puis relâcher | Espace |
| Arme | bouton en haut à droite | 1 à 6 |
| Voir toute la carte | 🔍, ou glisser le doigt sur l'écran | — |

**Armes :** Bazooka (dévié par le vent) · Grenade (rebondit, explose après 3 s) · Fusil (tir direct) · Grappe (×2, se divise en 5) · Dynamite (×1, énorme explosion, 5 s pour fuir) · Gant (coup de poing qui projette).

Tomber à l'eau élimine directement. La dernière équipe en vie gagne.

## Bon à savoir

- **L'hôte doit garder le jeu ouvert à l'écran.** C'est son appareil qui fait tourner la partie : s'il verrouille son téléphone ou change d'appli, la partie se met en pause pour tout le monde.
- Le multijoueur est en pair-à-pair (WebRTC via [PeerJS](https://peerjs.com)), donc **aucun serveur à payer**. Sur certains réseaux 4G/5G ou Wi-Fi d'entreprise, la connexion directe peut échouer. Dans ce cas, mettez-vous tous sur le même Wi-Fi, ou ajoutez un serveur TURN dans `PEER_OPTS` en haut du script (par exemple un compte gratuit Metered ou Twilio).
- Tout tient dans un seul fichier `index.html`, facile à modifier : dégâts, armes, couleurs, noms des Grubz…
