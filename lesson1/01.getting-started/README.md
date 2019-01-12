# Avant commencer

![IDE](http://www.commitstrip.com/wp-content/uploads/2015/04/Strip-Ce-que-le-codeur-detest-dans-lIDE-650-final.jpg)

Pour écrire du code vous pouvez utiliser NotePad, vim (comme un pro!) ou un IDE (Integrated Development Environment).
Les IDEs les plus populaire sont:

+ VSCode 💖
+ WebStorm (payant)
+ SublimeText
+ Atom

Utiliser des raccourcis est gangner du temps. Voici la liste de raccoucis de VSCode pour [Mac](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-macos.pdf) et [Windows](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf)


## Commentaires

N'oubliez pas d'utiliser les commentaires JavaScript d'une ligne (*inline*) et de plusieurs lignes (*multiline*). C'est un moyen de faciliter le travail aux collegues et nous-même dans l'avenir.

```js
// quick inline commment

/*
I am 
so
multiline
*/

```

## Langue de développement

Toutes les lettres d'Unicode peuvent être utilisé pour écrire du code, ça veut dire que c'est possible de le faire en français, anglais, russe, chinois ou n'importe quelle autre langue.
Généralement la meilleure pratique est d'écrire le code et les commentaires en anglais.

![Coding in French](http://www.commitstrip.com/wp-content/uploads/2015/08/Strip-à-la-française-650-final.jpg)


## Code style

![Indent your code properly](http://www.commitstrip.com/wp-content/uploads/2013/02/Strips-Indentation-600-final.jpg)

Le plus important lorsqu'on écrit du code est d'être consistant. Il faut se mettre d'accord avec l'équipe ou soi-même sur les règles de syntax et d'indentation que l'on va utiliser.
[Airbnb](https://github.com/airbnb/javascript) et [Google](https://google.github.io/styleguide/jsguide.html) ont créé leurs styleguides que chacun est libre de suivre (ou pas). 

Si vous avez une hésitation sur la manière d'indenter votre code, retournez voir le styleguide choisi.
Pour automatiser ce processus, vous pouvez installer un *code linter* [ESLint](https://eslint.org/) dans votre projet ou en global.

Comment installer ESLint en local?

1. Installez la dernière version de [NodeJS](https://nodejs.org/en/download/) sur votre ordinateur.

2. Ouvrez le programme Terminal (Mac) ou Command Prompt (Windows) et allez à la racine de ce projet avec la commande `cd`.
```
cd /Users/yourname/path/to/project/javascript-101
```

3. La configuration de ce projet est déjà prête, il ne reste plus qu'à installer les dependences nécessaires avec la commande :
```
npm install
```

<details>
<summary>
Installer ESLint en global
</summary>

Comment [installer ESLint en global](https://medium.com/@davidchristophersally/how-to-set-up-eslint-in-vscode-globally-253f25fbaff9) (pour utiliser les mêmes reglès sur tous vos projets) et l'utiliser avec VSCode?

1. Installez la dernière version de [NodeJS](https://nodejs.org/en/download/) sur votre ordinateur.

2. Installez les modules eslint et les règles Airbnb
```
npm install --global eslint eslint-config-airbnb-base eslint-plugin-import
```

3. Créez le ficher de config ESLint
```
touch .eslintrc
```

4. Ouvrez ce fichier 
<!-- 4.1 Avec vim
```
vi .eslintrc
```
4.2 Ou avec VSCode
Dans VSCode ouvrez [*Command Palette*](https://code.visualstudio.com/docs/getstarted/userinterface#_command-palette) en appuyant Ctrl+Shift+P (Windows) ou (Cmnd+Shift+P) et choisissez "Shell Command: Install 'code' command in PATH command".

Ensuite retournez sur le terminal et exécutez: 
```
code .eslintrc
``` -->

5. Ajoutez ce code dans le ficher et sauvegardez
```json
{
 "extends": "airbnb",
 "env": {
 "node": true,
 "es6": true,
 "browser": true
 },
 "rules": { }
}
```

6. Installez l'extension ESLint dans la partie des [extensions sur VSCode](https://code.visualstudio.com/docs/editor/extension-gallery)
</details>