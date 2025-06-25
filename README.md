# 🎮 VIBRASENS_controller

**VIBRASENS_controller** est le contrôleur sans fil du système **VIBRASENS**, un dispositif de stimulation vibratoire destiné aux enfants en situation de polyhandicap.  
Ce contrôleur permet de **piloter à distance** le module vibrant via une **connexion Wi-Fi**, en ajustant précisément l'intensité, la fréquence et le canal de communication.

---

## 🧰 Composition Matérielle

### 🔩 Boîtier imprimé en 3D

- Capot (PLA)
- Base (PLA)
- Porte_composants (PLA)
- 8 vis M3 L10 tête fraisée  
  🔗 [Réf. RS Online](https://fr.rs-online.com/web/p/vis-a-metaux/9087485)

---

### ⚡ Composants électroniques

| Composant                | Référence produit | Lien |
|--------------------------|-------------------|------|
| Microcontrôleur          | M5StickC Plus 2   | [🔗 M5Stack](https://shop.m5stack.com/products/m5stickc-plus2-esp32-mini-iot-development-kit) |
| Molette haute            | M5Encoder (x1)    | [🔗 M5Stack](https://shop.m5stack.com/products/scroll-unit-with-hollow-shaft-encoder-ec10e1220501) |
| Molette basse            | M5Encoder (x1)    | [🔗 M5Stack](https://shop.m5stack.com/products/scroll-unit-with-hollow-shaft-encoder-ec10e1220501) |
| Hub I2C pour extensions  | PaHUB             | [🔗 M5Stack](https://shop.m5stack.com/products/i2c-hub-1-to-6-expansion-unit-pca9548apw) |
| Câbles de connexion      | Grove M/M (1×5 cm + 2×10 cm) | [🔗 M5Stack](https://shop.m5stack.com/products/4pin-buckled-grove-cable) |

---

## 🧾 Instructions de Montage

Les instructions de montage se trouve dans **documents_techniques** et se résume en : 
- Assemblage des composants électronique et mécanique
- Câblage des composants 

---

## 💻 Instructions de Programmation

Les instructions de programmation se trouve dans **documents_techniques** et se résume en : 
- Télécharger les différents logiciels (VSCode, Git, etc.)
- Installer les extensions (PlatformIO)
- Téléverser le code au M5StickC

---

## ⚙️ Fonctionnalités de la Télécommande

Le contrôleur permet de régler plusieurs paramètres importants du module vibrant :

### 📶 Canal Wi-Fi

- Permet la communication avec un ou plusieurs modules vibrants.
- **Obligation** : le contrôleur et le(s) module(s) doivent être configurés sur le **même canal Wi-Fi**.
- Ce réglage s’effectue via le **menu des paramètres**.

> 💡 Il est théoriquement possible de piloter plusieurs modules avec une seule télécommande, à condition qu’ils partagent le même canal.

---

### 🎚️ Intensité de vibration

- **Plage** : de **0** (aucune vibration) à **10** (intensité maximale).
- Réglage via la **molette haute** de la télécommande.

---

### 🔁 Fréquence de vibration

- **Plage** : de **0 ms** (vibration continue) à **2000 ms** (mode pulsé).
- Exemple : à 1000 ms, le module vibre pendant 1000 ms, puis s’arrête 1000 ms, etc.
- Réglage via la **molette basse** de la télécommande.

![image](https://github.com/user-attachments/assets/af71a602-d572-49e3-a598-3a5eb67b4512)

---
## 🔄 Schéma de la Machine à États

![image](https://github.com/user-attachments/assets/03921408-3648-4b7a-ae5b-b0afdf741081)

--- 

## 📂 Arborescence du dépôt

```bash
VIBRASENS_controller/
├── firmware/               # Code source Arduino/ESP-IDF
├── documents_techniques/            # Documentation technique
├── fichiers_3d/                     # Fichiers STL du boîtier
├── photos/                 # Images pour la notice de montage
└── README.md
