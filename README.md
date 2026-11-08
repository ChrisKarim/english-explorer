# 🏡➡️🌳➡️🚲 English Explorer

Jeu éducatif en 3D pour apprendre l'anglais en explorant. Conçu pour un enfant
francophone de 7 ans, jouable sur **ordinateur, iPhone et Android**.

*created by CKN*

---

## 1. Lancer le jeu

Tout le jeu tient dans **un seul fichier : `index.html`**. Il n'y a rien à installer.

### Sur l'ordinateur (test rapide)

Double-cliquez sur `index.html`. Le jeu s'ouvre dans le navigateur.

⚠️ **Attention** : ouvert de cette façon (adresse `file://`), le **micro ne fonctionne
pas** (sécurité du navigateur). Le jeu bascule automatiquement sur le *mode parent* :
l'enfant parle, et vous validez à l'oreille avec ✅ / 🔁.

### Avec le micro (recommandé)

Le micro n'est autorisé qu'en `localhost` ou en **HTTPS**.

**a) Sur l'ordinateur, via un petit serveur local**

```bash
cd english-explorer
python3 -m http.server 8000
```
Puis ouvrez `http://localhost:8000` dans Chrome, Edge ou Safari.

**b) Sur téléphone et tablette : héberger le fichier**

| Service | Comment faire |
|---|---|
| **GitHub Pages** | Déjà en place : https://chriskarim.github.io/english-explorer/ |
| **Netlify Drop** | `app.netlify.com/drop`, glissez le dossier, vous obtenez une adresse HTTPS |

Ouvrez l'adresse sur l'iPhone (Safari) ou Android (Chrome), puis
**Partager → Ajouter à l'écran d'accueil** pour avoir une icône comme une vraie app.

> Au premier lancement, une connexion internet est nécessaire : le moteur 3D
> (Babylon.js) et la police sont téléchargés depuis un CDN, puis mis en cache.

### Dédier le jeu à quelqu'un

L'accueil affiche *« created by CKN »*. Pour le dédier à un enfant, ajoutez `?pour=`
à la fin de l'adresse :

```
https://…/index.html?pour=Léo      →  created for Léo
```

Le prénom n'est alors écrit nulle part dans le code : il vit uniquement dans votre
lien, qu'on peut mettre en favori ou sur l'écran d'accueil du téléphone.

---

## 2. Comment on joue

```
EXPLORER ──► ÉCOUTER ──► DÉFI : LES MOTS ──► BONUS : LES PHRASES ──► ÉTOILES ──► PORTE 🎉
```

1. **Explorer** : l'enfant se promène librement dans le lieu.
2. **Écouter** : il touche un objet **entouré de rouge 🔴**. Le jeu dit le mot
   **en anglais**, puis **sa traduction en français** pour qu'il comprenne le sens.
   Le contour passe au vert menthe une fois l'objet découvert.
3. **Le défi** : quand tous les objets obligatoires sont trouvés, le bouton 🎤 apparaît.
   Pour chaque mot, une image s'affiche sans le texte, l'enfant appuie sur le micro et
   dit le mot. Il a 3 essais ❤️❤️❤️ et peut réécouter autant qu'il veut.
4. **Les phrases bonus** : 2 à 3 courtes phrases à répéter, tirées au hasard parmi 7.
   La phrase est lue **en anglais puis traduite en français**. Le mot clé est surligné
   en rouge, les mots reconnus passent au vert. **Les phrases ne bloquent jamais la
   porte** : elles rapportent des bulles 💬.
5. **Les étoiles** : 1 à 3 étoiles selon les mots réussis. La zone est validée à partir
   de 70 % (réglable), et la porte du lieu suivant s'ouvre.

### Les quatre lieux (7 zones)

| Lieu | Zones | Mots obligatoires | Objets en option | Phrases |
|---|---|---|---|---|
| 🏠 The House | Bedroom, Bathroom, Kitchen, Living room | 18 | 16 | 28 |
| 🌳 The Garden | 1 | 8 | 4 | 7 |
| 🚦 The Street | 1 | 8 | 4 | 7 |
| 🎈 The Park | 1 | 8 | 4 | 7 |

**Les objets en option** (compteur ⭐ dans la barre du haut) se découvrent et se
répètent pour le plaisir. Ils passent **après** les mots obligatoires pendant le défi,
et ne comptent ni pour les étoiles ni pour l'ouverture de la porte.

Il y a aussi des **objets de révision** (marqués « révision » sur la carte du mot) :
des objets des lieux précédents, cliquables pour réentendre leur nom.

---

## 3. Les commandes

### Ordinateur
- **Flèches** / **Z** / **W** : avancer · **S** : reculer
- **Flèches gauche-droite** / **Q** / **A** / **D** : tourner
- **Clic maintenu + glisser** : regarder autour de soi
- **Clic sur le sol** : le personnage s'y rend tout seul
- **Clic sur un objet** : l'entendre

### iPhone, Android, tablette
- **Joystick** : haut = avancer, bas = reculer, côtés = tourner (zone morte au centre,
  position gauche ou droite réglable)
- **Glisser un doigt ailleurs** : regarder autour
- **Toucher le sol** : marcher jusque là
- **Toucher un objet** : l'entendre

Marche lente, pas de saut, pas de secousses de caméra, impossible de tomber ou de
sortir du décor.

---

## 4. L'espace parent ⚙️

Accès par le bouton ⚙️ (une petite multiplication protège l'entrée).

| Réglage | Effet |
|---|---|
| Volume de la voix / des effets | |
| Vitesse de la voix anglaise | de 0,6× à 1,1× |
| Accent | 🇺🇸 américain ou 🇬🇧 britannique |
| Hoot lit ses messages | la mascotte parle en français |
| **Dire la traduction française** | activer / couper la traduction après l'anglais |
| Mots à réussir pour ouvrir la porte | 50 %, 70 % ou 90 % |
| Phrases bonus | Auto (2 maison / 3 dehors), 2, 3 ou aucune |
| **Validation par l'adulte** | sans micro : vous validez à l'oreille ✅ / 🔁 |
| Qualité graphique | Auto, Haute ou Économie |
| Joystick | à gauche ou à droite |
| Mots à revoir | la liste de ce qui a été raté, réécoutable |
| 🔓 Débloquer tous les lieux · ♻️ Tout recommencer | |

---

## 5. Ajouter du vocabulaire

Tout le contenu est dans la liste **`LEVELS`** (chercher `DONNÉES DES NIVEAUX` dans le
fichier). Aucune autre partie du code n'est à modifier.

**Ajouter un mot** — copiez une ligne dans `items` :

```js
{ w: "lamp", fr: "la lampe", b: "lamp", e: "💡", at: [[-2.85, 0, 26.9, 0, 1]] },
```

| Champ | À quoi ça sert |
|---|---|
| `w` | le mot anglais (dit à voix haute) |
| `fr` | la traduction française (dite juste après) |
| `b` | le nom du modèle 3D, dans la liste `BUILD` |
| `e` | l'emoji de secours si la miniature 3D n'a pas pu être calculée |
| `at` | `[[x, y, z, rotation, taille], …]` — plusieurs emplacements possibles |
| `opt` | `true` = objet **en option** (ne bloque jamais la porte) |
| `collide` | `true` = on ne peut pas le traverser |
| `accept` | autres prononciations acceptées, ex. `["tv", "tee vee"]` |

**Ajouter une phrase** — dans `sentences` de la zone :

```js
{ en: "The lamp is on.", fr: "La lampe est allumée.", key: "lamp" }
```

`key` est le mot du vocabulaire qui **doit** être entendu pour valider la phrase.
Règles : 3 à 6 mots, vocabulaire du lieu, **pas d'apostrophe** (la reconnaissance les
découpe mal), et cohérent avec le décor.

**Ajouter un modèle 3D** : une fonction dans `BUILD`, qui reçoit la boîte à outils `K`
(`box`, `cyl`, `sph`, `tor`, `plane`, `line`, `rot`, `scl`) et le nœud racine. L'objet
est centré en x/z, posé sur y = 0, et regarde vers −z.

> ⚠️ Règle importante : un objet de **décor** ne doit jamais ressembler à un mot à
> trouver du même lieu, sinon l'enfant le touche et rien ne se passe.

---

## 6. La voix anglaise

### Choisir la voix
Espace parent → **Voix anglaise** et **Voix française**. Le menu liste toutes les voix
installées sur l'appareil, **les plus naturelles en premier** (Premium, Enhanced,
Neural, Google…). Deux boutons permettent de les essayer avant de choisir.

Le jeu impose toujours une voix de la bonne langue. Si aucune voix anglaise n'est
installée, l'espace parent le signale clairement : sans cela, le navigateur lirait
l'anglais avec la voix française de l'appareil, d'où un fort accent.

### Obtenir une voix vraiment fluide (gratuit)
Les voix livrées par défaut sont les plus robotiques. Les voix « améliorées » sont
beaucoup plus naturelles et se téléchargent gratuitement :

- **iPhone / iPad** : Réglages → Accessibilité → Contenu énoncé → Voix → English →
  choisir une voix **Premium** (Ava, Evan, Zoe, Serena…) et la télécharger.
- **Android** : Paramètres → Système → Langues et saisie → Synthèse vocale →
  moteur Google → Installer les données vocales → English.
- **Ordinateur** : dans Chrome, les voix **Google US English / Google UK English**
  sont les plus naturelles et ne demandent aucune installation.

Puis revenez dans l'espace parent choisir la nouvelle voix.

### Aller plus loin : une voix de type assistant IA
Les voix très fluides des assistants (Claude, ChatGPT…) sont des voix *neuronales*
servies par une API payante : elles ne peuvent pas tourner dans une page web seule,
et une clé d'API ne doit jamais être mise dans une page publique.

La solution, si la voix du navigateur ne suffit pas : **pré-enregistrer les mots et les
phrases en mp3** avec le service de votre choix, puis les déposer dans un dossier
`audio/`. Le jeu les utilise automatiquement. Il y a 70 mots et 49 phrases à générer.

Créez un dossier `audio/` à côté de `index.html` avec des `.mp3` nommés d'après le mot
ou la phrase, en minuscules et avec des tirets :

```
audio/teddy-bear.mp3
audio/i-love-my-teddy-bear.mp3
```

Le jeu les utilise automatiquement à la place de la voix de synthèse. Si le fichier
n'existe pas, la voix du navigateur prend le relais : rien ne casse. La traduction
française, elle, reste dite par la voix de synthèse.

Les **textures** (parquet, carrelage, briques, herbe, fourrure, eau…) et tous les
**modèles 3D** sont générés par le code. Aucun fichier à télécharger.

---

## 7. Performance

| | Ordinateur | Téléphone |
|---|---|---|
| Textures | 512 px | 256 px |
| Ombres | 2048 px | 1024 px, une image sur deux |
| Post-traitement | halo lumineux, vignette, anticrénelage | non |

Le décor immobile est fusionné par matériau, et la résolution baisse toute seule si les
images par seconde chutent. Le parent peut forcer « Haute » ou « Économie ».

---

## 8. Vie privée 🔒

- **Aucun enregistrement audio n'est conservé**, ni sur l'appareil ni ailleurs.
- Aucune publicité, aucun traceur, aucune statistique.
- La progression est enregistrée uniquement dans le navigateur (`localStorage`).
- ⚠️ La reconnaissance vocale est celle du navigateur : pendant la transcription, **la
  voix peut transiter par les serveurs de son éditeur** (Google pour Chrome, Apple pour
  Safari). Si cela vous gêne, activez la **validation par l'adulte** : le micro n'est
  alors jamais utilisé.

---

## 9. Navigateurs

| Navigateur | 3D | Micro |
|---|---|---|
| Chrome, Edge (ordinateur, Android) | ✅ | ✅ |
| Safari (Mac, iPhone, iPad) | ✅ | ✅ |
| Firefox | ✅ | ❌ → bascule automatique en validation par l'adulte |

---

## 10. En cas de souci

| Problème | Solution |
|---|---|
| Bloqué sur « Hoot prépare le décor… » | Pas de connexion au premier lancement : le moteur 3D n'a pas pu être téléchargé. Reconnectez-vous et rechargez. |
| Aucun son | Appuyez bien sur ▶️ **Jouer** : ce premier appui débloque l'audio (obligatoire sur iPhone). |
| Le micro ne réagit pas | Vous êtes en `file://`. Utilisez `localhost` ou une adresse HTTPS (voir §1). |
| L'anglais est prononcé avec l'accent français | Aucune voix anglaise n'est installée sur l'appareil : le navigateur se rabat sur la voix française. Voir §6 pour en installer une, puis choisissez-la dans l'espace parent. |
| La voix est robotique | Installez une voix « améliorée » (§6), puis sélectionnez-la dans l'espace parent. |
| Ça rame | Espace parent → Qualité graphique → **Économie**. |
| L'enfant est bloqué sur un mot | Espace parent → seuil à **50 %**, ou validation par l'adulte. |
| Les objets apparaissent avec leur emoji et non une photo | Les miniatures 3D n'ont pas pu être calculées sur cet appareil. Sans conséquence sur le jeu. |
