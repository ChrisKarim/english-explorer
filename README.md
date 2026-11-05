# 🏡➡️🌳➡️🚲 English Explorer

Jeu éducatif en 3D pour apprendre l'anglais en explorant. Conçu pour un enfant
francophone de 7 ans, jouable sur **ordinateur, iPhone et Android**.

---

## 0. Personnaliser le message d'accueil

Par défaut, l'accueil affiche *« created with ❤️ »*. Pour y mettre le prénom de
l'enfant, ajoutez `?pour=` à la fin de l'adresse :

```
https://…/index.html?pour=Méalua      →  created for Méalua
```

Le prénom n'est **jamais écrit dans le code** : il vit uniquement dans votre lien.
C'est volontaire — si le jeu est hébergé sur une page publique, aucun prénom
d'enfant n'y est exposé ni indexable par les moteurs de recherche. Mettez votre
lien personnalisé en favori ou sur l'écran d'accueil du téléphone.

---

## 1. Lancer le jeu

Tout le jeu tient dans **un seul fichier : `index.html`**. Il n'y a rien à installer.

### Sur l'ordinateur (test rapide)

Double-cliquez sur `index.html`. Le jeu s'ouvre dans le navigateur.

⚠️ **Attention** : ouvert de cette façon (adresse `file://`), le **micro ne fonctionne
pas** (sécurité du navigateur). Le jeu bascule automatiquement sur le *mode parent* :
l'enfant parle, et vous validez à l'oreille avec ✅ / 🔁.

### Avec le micro (recommandé)

Le micro n'est autorisé qu'en `localhost` ou en **HTTPS**. Deux solutions :

**a) Sur l'ordinateur, via un petit serveur local**

```bash
cd english-explorer
python3 -m http.server 8000
```
Puis ouvrez `http://localhost:8000` dans Chrome, Edge ou Safari.

**b) Sur téléphone et tablette : héberger le fichier (le plus simple)**

Déposez le dossier sur un hébergeur gratuit qui fournit du HTTPS :

| Service | Comment faire |
|---|---|
| **Netlify Drop** | Allez sur `app.netlify.com/drop`, glissez le dossier `english-explorer`. Vous obtenez une adresse `https://…netlify.app` à ouvrir sur le téléphone. |
| **GitHub Pages** | Déposez `index.html` dans un dépôt, activez Pages dans les réglages. |
| **Cloudflare Pages** | Même principe, glisser-déposer du dossier. |

Ouvrez ensuite l'adresse sur l'iPhone (Safari) ou sur Android (Chrome), puis
**« Ajouter à l'écran d'accueil »** pour avoir une icône comme une vraie application.

> Au tout premier lancement, une connexion internet est nécessaire : le moteur 3D
> (Babylon.js) et la police sont téléchargés depuis un CDN. Ensuite le navigateur
> les garde en cache.

---

## 2. Comment on joue

```
EXPLORER ──► ÉCOUTER ──► DÉFI : LES MOTS ──► BONUS : LES PHRASES ──► ÉTOILES ──► PORTE 🎉
```

1. **Explorer** : l'enfant se promène librement dans le lieu.
2. **Écouter** : il touche un objet **entouré en rouge 🔴**. Le jeu dit le mot
   **en anglais, lentement**, puis **sa traduction en français** pour qu'il comprenne.
   Le contour passe au vert quand l'objet est découvert.
3. **Le défi** : quand tout est trouvé, le gros bouton 🎤 apparaît. Pour chaque mot,
   l'image s'affiche sans le texte, l'enfant appuie sur le micro et dit le mot.
   Il a 3 essais ❤️❤️❤️ et peut réécouter autant qu'il veut.
4. **Les phrases bonus** : 2 à 3 courtes phrases à répéter. La phrase est lue
   **en anglais puis traduite en français**. Le mot clé est surligné en rouge, et
   les mots reconnus passent au vert. **Les phrases ne bloquent jamais la porte** :
   elles rapportent des bulles 💬.
5. **Les étoiles** : 1 à 3 étoiles selon les mots réussis. La zone est validée à
   partir de 70 % (réglable), et la porte du lieu suivant s'ouvre.

### Les quatre lieux (7 zones)

| Lieu | Zones | Mots à apprendre | Objets bonus (en option) |
|---|---|---|---|
| 🏠 The House | Bedroom, Bathroom, Kitchen, Living room | 18 | 16 |
| 🌳 The Garden | 1 | 8 | 4 |
| 🚦 The Street | 1 | 8 | 4 |
| 🛝 The Park | 1 | 8 | 4 |

Les **objets bonus** se découvrent et se répètent pour le plaisir : ils donnent des
bulles 💬 mais ne comptent pas dans les étoiles et ne bloquent jamais la progression.
On peut les masquer depuis l'espace parent.

---

## 3. Les commandes

### Ordinateur
- **Flèches** (ou Z/W et S) : avancer, reculer
- **Flèches gauche / droite** (ou Q/A et D) : tourner
- **Clic maintenu + glisser** : regarder autour de soi
- **Clic sur le sol** : le personnage s'y rend tout seul
- **Clic sur un objet** : l'entendre

### iPhone, Android, tablette
- **Joystick en bas** : haut = avancer, bas = reculer, côtés = tourner
  (zone morte au centre, position gauche ou droite réglable)
- **Glisser un doigt ailleurs** : regarder autour
- **Toucher le sol** : marcher jusque là
- **Toucher un objet** : l'entendre

Le jeu s'adapte seul : marche lente, pas de saut, pas de secousses de caméra,
impossible de tomber ou de sortir du décor.

---

## 4. L'espace parent ⚙️

Accès par le bouton ⚙️ (une petite multiplication protège l'entrée).

| Réglage | Effet |
|---|---|
| Volume / vitesse de la voix | La voix anglaise peut être ralentie jusqu'à 0,5× |
| Accent | Américain (en-US) ou britannique (en-GB) |
| **Traduction française à l'oral** | Dire ou non la traduction après chaque mot et chaque phrase |
| Messages de Hoot lus à voix haute | La mascotte parle en français |
| Seuil de réussite | 50 %, 70 % ou 90 % des mots pour valider une zone |
| Phrases bonus | Auto (2 maison / 3 dehors), 2, 3 ou aucune |
| Objets bonus | Affichés ou masqués |
| **Validation par l'adulte** | Sans micro : vous validez à l'oreille avec ✅ / 🔁 |
| Qualité graphique | Auto, Haute ou Économie |
| Joystick | À gauche ou à droite |
| Mots à revoir | La liste de ce qui a été raté |
| 🔓 Débloquer tous les lieux · 🗑️ Tout recommencer | |

---

## 5. Ajouter du vocabulaire

Tout est au même endroit, en haut du `<script>` de `index.html`, dans la liste
`ZONES` (section **A. DONNÉES**). Aucune autre partie du code n'est à modifier.

**Ajouter un mot** — copiez une ligne et changez-la :

```js
{ en:"lamp", fr:"la lampe", emo:"💡", model:"lamp", pos:[3.3, 0, 2.6] }
```

| Champ | À quoi ça sert |
|---|---|
| `en` | le mot anglais (dit à voix haute) |
| `fr` | la traduction française (dite juste après) |
| `emo` | l'emoji affiché sur la carte et pendant le défi |
| `model` | le nom du constructeur 3D (section **F.5**). Si le nom est inconnu, une caisse colorée est utilisée : le jeu ne plante pas. |
| `pos` | la position `[x, hauteur, z]` dans le lieu |
| `rotY` | *(facultatif)* rotation, pour les objets accrochés à un mur |
| `accept` | *(facultatif)* autres prononciations acceptées, ex. `["tv","tee vee"]` |

**Ajouter une phrase** :

```js
{ en:"The lamp is on.", fr:"La lampe est allumée.", key:"lamp" }
```

`key` est le mot du vocabulaire qui **doit** être entendu pour valider la phrase.

Règles d'écriture : 3 à 6 mots, du vocabulaire du lieu, **pas d'apostrophe**
(la reconnaissance vocale les découpe mal), et cohérent avec le décor.

**Ajouter un lieu** : copiez un bloc de `ZONES` entier, puis ajoutez son `id` dans
la liste `LIEUX` juste en dessous.

---

## 6. Améliorer les voix et les images (facultatif)

### De vrais enregistrements audio
Créez un dossier `audio/` à côté de `index.html` et placez-y des fichiers
`.mp3` nommés d'après le mot ou la phrase, en minuscules et avec des tirets :

```
audio/teddy-bear.mp3
audio/i-love-my-teddy-bear.mp3
```

Le jeu les utilise automatiquement à la place de la voix de synthèse. Si le fichier
n'existe pas, la voix du navigateur prend le relais : rien ne casse.

### Les textures
Toutes les textures (parquet, carrelage, briques, herbe, fourrure, eau…) sont
**dessinées par le code**, il n'y a donc rien à télécharger. Pour un rendu encore
plus réaliste, on peut remplacer la fonction `Tex.get()` par des textures CC0
de [Poly Haven](https://polyhaven.com) ou [ambientCG](https://ambientcg.com).

### Les modèles 3D
Même principe : les objets sont construits avec des formes simples assemblées
(section **F.5**). On peut les remplacer par des modèles `.glb` gratuits
(packs CC0 [Kenney](https://kenney.nl/assets) ou [Quaternius](https://quaternius.com))
en chargeant le fichier avec `BABYLON.SceneLoader` dans le constructeur de l'objet.

---

## 7. Performance

| | Ordinateur | Téléphone |
|---|---|---|
| Textures | 512 px | 256 px |
| Ombres | 2048 px | 1024 px, une image sur deux |
| Post-traitement | oui (anticrénelage, halo, vignette) | non |

Le décor immobile est **fusionné par matériau** (on passe de plusieurs centaines
d'éléments à quelques dizaines) et la résolution baisse toute seule si les images
par seconde chutent. Le parent peut forcer « Haute » ou « Économie ».

---

## 8. Vie privée 🔒

- **Aucun enregistrement audio n'est conservé**, ni sur l'appareil ni ailleurs.
- Aucune publicité, aucun traceur, aucune statistique.
- La progression est enregistrée uniquement dans le navigateur de l'appareil
  (`localStorage`). La vider, c'est perdre la progression, rien d'autre.
- ⚠️ À savoir : la reconnaissance vocale est celle du navigateur. Pendant la
  transcription, **la voix peut transiter par les serveurs de l'éditeur du
  navigateur** (Google pour Chrome, Apple pour Safari). Si cela vous gêne, activez
  la **validation par l'adulte** dans l'espace parent : le micro n'est alors
  jamais utilisé.

---

## 9. Navigateurs

| Navigateur | 3D | Micro |
|---|---|---|
| Chrome, Edge (ordinateur, Android) | ✅ | ✅ |
| Safari (Mac, iPhone, iPad) | ✅ | ✅ |
| Firefox | ✅ | ❌ → bascule automatique en validation par l'adulte |

Si le micro est refusé ou indisponible, le jeu ne bloque jamais : il passe tout
seul en mode « un adulte valide à l'oreille ».

---

## 10. En cas de souci

| Problème | Solution |
|---|---|
| Écran bloqué sur « Préparation du monde… » | Pas de connexion au premier lancement : le moteur 3D n'a pas pu être téléchargé. Reconnectez-vous et rechargez. |
| Aucun son | Appuyez bien sur ▶️ **Jouer** : c'est ce premier appui qui débloque l'audio (obligatoire sur iPhone). |
| Le micro ne réagit pas | Vous êtes en `file://`. Utilisez `localhost` ou une adresse HTTPS (voir §1). |
| Pas de voix anglaise | L'espace parent affiche l'état exact de la voix. Sur Android, installez une voix anglaise dans les réglages du système. |
| Ça rame | Espace parent → Qualité graphique → **Économie**. |
| L'enfant est bloqué sur un mot | Espace parent → Seuil de réussite → **50 %**, ou activez la validation par l'adulte. |
