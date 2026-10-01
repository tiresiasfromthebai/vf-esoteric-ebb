# VF d'Esoteric Ebb

Traduction française non officielle d'[Esoteric Ebb](https://store.steampowered.com/app/2057760/Esoteric_Ebb/), **en cours**.

La version de test actuelle (0.3) couvre le début du jeu : le prologue (« Lower Lair »), l'antre de Visken et la ville de Tolstad, soit environ 17 500 répliques, ainsi que l'interface, le glossaire et le journal de ces zones. Le reste du jeu est encore en anglais. Les noms des objets et des sorts, ainsi que les caractéristiques, sont traduits dans tout le jeu.

## Téléchargement

Dans l'onglet [Releases](../../releases), l'archive `VF_Esoteric_Ebb_<version>.zip` est la version « patch » :
- elle pèse 13 Mo et ne contient aucun fichier du jeu, seulement des différences (xdelta3) ;
- elle fonctionne sous Windows, Linux et Steam Deck ;
- elle vérifie vos fichiers avant d'installer et refuse si la version du jeu ne correspond pas ;
- elle garde une copie des originaux et se désinstalle proprement ;
- elle convertit vos sauvegardes à l'installation et à la désinstallation (voir plus bas).

Une version « fichiers complets », sans script, est aussi disponible sur Nexus Mods. Ses utilisateurs trouveront ici le **convertisseur de sauvegardes** seul (`VF_Esoteric_Ebb_<version>_convertisseur.zip`).

> **Avertissement** : cette version s'installe en lançant des scripts (.bat, .sh) et un exécutable (xdelta3). Ils sont lisibles et ne font que modifier les fichiers du jeu, mais exécuter des scripts téléchargés reste un risque. Si la sécurité de votre machine est critique (poste de travail, données sensibles…), ne l'utilisez pas : préférez la version « fichiers complets » de Nexus Mods, qui ne contient aucun script ni exécutable.

**Compatible uniquement avec la version Steam du jeu, build 22657387.**

## Installation

1. Fermez le jeu.
2. Extrayez l'archive **dans** le dossier du jeu, à côté de `Esoteric Ebb.exe` (Steam : clic droit sur le jeu, Gérer, Parcourir les fichiers locaux). Vous devez obtenir un dossier `VF_Esoteric_Ebb`.
3. Windows : lancez `VF_Esoteric_Ebb\installer_windows.bat`. Linux et Steam Deck : lancez `VF_Esoteric_Ebb/installer_linux.sh`.

Pour désinstaller : `desinstaller_windows.bat` ou `desinstaller_linux.sh`, ou « Vérifier l'intégrité des fichiers » dans Steam.

## Sauvegardes

La VF traduit les noms des objets et des sorts, qui servent aussi de clés dans les sauvegardes. Une partie commencée en anglais, ou avec la VF 0.1, perdrait ses objets et ses sorts sans conversion :

- la version patch convertit automatiquement (vers la VF à l'installation, vers la VO à la désinstallation) ;
- avec la version complète de Nexus, ou si vous désinstallez par « Vérifier l'intégrité des fichiers », lancez `convertir_vers_vf` ou `convertir_vers_vo` (`.bat` sous Windows, `.sh` sous Linux), jeu fermé.

Une copie de vos sauvegardes est faite à chaque conversion. Windows : PowerShell (inclus dans Windows). Linux et Steam Deck : python3.

**À tester** : tout a été testé sous Linux, mais pas encore sur un vrai Windows. Signalez tout problème dans les [issues](../../issues).

## Limites connues

- Les **noms de lieux**, la monnaie (« Crowns ») et le « DC » du glossaire restent en anglais : le jeu s'en sert comme clés internes.
- Une partie commencée en anglais se charge (après conversion), mais les choix déjà faits peuvent réapparaître.
- Une mise à jour du jeu par Steam efface la traduction. Il faut alors attendre la version de la VF qui correspond au nouveau build.

## Choix de traduction

- Le narrateur et les voix intérieures **tutoient** le héros. Les menus vous vouvoient.
- Le ton du jeu est drôle et grinçant. La traduction cherche l'effet (jeux de mots adaptés, registre propre à chaque voix) plutôt que le mot à mot.
- Pour les termes de D&D, on suit la VF officielle de la 5e édition.

## Transparence sur l'IA

Cette traduction est faite **avec l'aide d'une IA** (Claude, d'Anthropic), sous la direction et la relecture d'un joueur francophone. Elle s'appuie sur une charte de style, un lexique, des relectures indépendantes de chaque lot et des tests en jeu. Le résultat n'est pas parfait : vos retours comptent.

## Retours

Ouvrez une [issue](../../issues) pour tout ce qui sonne faux, déborde d'une boîte ou reste en anglais, de préférence avec une capture d'écran.

## Crédits et licences

- Esoteric Ebb © Christoffer Bodegård / Sudden Snail AB, édité par Raw Fury. Ce projet n'est ni affilié ni approuvé par eux. Il faut posséder le jeu pour l'utiliser.
- Merci à Ravnow et KamelAkar, auteurs du premier patch FR, pour leurs découvertes techniques.
- Le texte de la traduction est sous licence [CC BY-NC-SA 4.0](LICENSE) : partage et adaptation autorisés, avec attribution, sans usage commercial et sous la même licence. Cette licence ne couvre que le travail de traduction, pas le jeu.
- Outil de patch : [xdelta3](https://github.com/jmacd/xdelta). Le binaire Linux (3.0.11) est sous GPL v2, et ses sources sont jointes à chaque release. Le binaire Windows (3.1.0) est sous Apache 2.0.
