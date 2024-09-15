Voici la traduction complète du guide pour contribuer à Cal.com :

---

# Contribuer à Cal.com

Les contributions sont ce qui rend la communauté open source si incroyable pour apprendre, inspirer et créer. Toute contribution que vous apportez est **grandement appréciée**.

## Règles de base

- Avant de soumettre un nouvel issue ou PR, vérifiez s'il existe déjà dans [issues](https://github.com/calcom/cal.com/issues) ou [PRs](https://github.com/calcom/cal.com/pulls).
- Issues GitHub : prenez note de l'étiquette `🚨 needs approval`.
  - **Pour les contributeurs** :
    - Demandes de fonctionnalités : Attendez l'approbation d'un membre central et la suppression de l'étiquette `🚨 needs approval` avant de commencer à coder ou de soumettre un PR.
    - Bugs, Sécurité, Performance, Documentation, etc. : Vous pouvez commencer à coder immédiatement, même si l'étiquette `🚨 needs approval` est présente. Cette étiquette concerne principalement les demandes de fonctionnalités.
  - **Notre Processus** :
    - Les issues provenant de non-membres centraux reçoivent automatiquement l'étiquette `🚨 needs approval`.
    - Nous apprécions beaucoup les nouvelles idées de fonctionnalités. Afin d'assurer la cohérence dans la direction du produit, elles sont examinées et approuvées.

## Priorités

<table>
  <tr>
    <td>
      Type de problème
    </td>
    <td>
      Priorité
    </td>
  </tr>
  <tr>
    <td>
      Améliorations mineures, demandes de fonctionnalités non essentielles
    </td>
    <td>
      <a href="https://github.com/calcom/cal.com/issues?q=is:issue+is:open+sort:updated-desc+label:%22Low+priority%22">
        <img src="https://img.shields.io/badge/-Low%20Priority-green">
      </a>
    </td>
  </tr>
   <tr>
    <td>
      UX confuse (... mais fonctionnelle)
    </td>
    <td>
      <a href="https://github.com/calcom/cal.com/issues?q=is:issue+is:open+sort:updated-desc+label:%22Medium+priority%22">
        <img src="https://img.shields.io/badge/-Medium%20Priority-yellow">
      </a>
    </td>
  </tr>
  <tr>
    <td>
      Fonctionnalités principales (Page de réservation, disponibilité, calcul de fuseau horaire)
    </td>
    <td>
      <a href="https://github.com/calcom/cal.com/issues?q=is:issue+is:open+sort:updated-desc+label:%22High+priority%22">
        <img src="https://img.shields.io/badge/-High%20Priority-orange">
      </a>
    </td>
  </tr>
  <tr>
    <td>
      Bugs principaux (Connexion, Page de réservation, Emails ne fonctionnent pas)
    </td>
    <td>
      <a href="https://github.com/calcom/cal.com/issues?q=is:issue+is:open+sort:updated-desc+label:Urgent">
        <img src="https://img.shields.io/badge/-Urgent-red">
      </a>
    </td>
  </tr>
</table>

## Développement

La branche de développement est `main`. C'est la branche contre laquelle toutes les demandes de tirage (pull requests) doivent être faites. Les modifications de la branche `main` sont taguées dans une version mensuelle.

Pour développer localement :

1. [Fork](https://github.com/calcom/cal.com/fork/) ce dépôt vers votre propre compte GitHub et ensuite
   [clonez](https://help.github.com/articles/cloning-a-repository/) le sur votre appareil local.
2. Créez une nouvelle branche :

   ```sh
   git checkout -b NOM_DE_VOTRE_BRANCHE
   ```

3. Installez yarn :

   ```sh
   npm install -g yarn
   ```

4. Installez les dépendances avec :

   ```sh
   yarn
   ```

5. Configurez votre fichier `.env` :

   - Dupliquez `.env.example` en `.env`.
   - Utilisez `openssl rand -base64 32` pour générer une clé et ajoutez-la sous `NEXTAUTH_SECRET` dans le fichier `.env`.
   - Utilisez `openssl rand -base64 32` pour générer une clé et ajoutez-la sous `CALENDSO_ENCRYPTION_KEY` dans le fichier `.env`.

6. Configurez Node
   Si votre version de Node ne répond pas aux exigences du projet comme indiqué dans la documentation, "nvm" (Node Version Manager) permet d'utiliser Node à la version requise par le projet :

   ```sh
   nvm use
   ```

   Vous devrez peut-être d'abord installer la version spécifique puis l'utiliser :

   ```sh
   nvm install && nvm use
   ```

   Vous pouvez installer nvm depuis [ici](https://github.com/nvm-sh/nvm).

7. Commencez à développer et surveillez les modifications du code :

   ```sh
   yarn dev
   ```

## Construction

Vous pouvez construire le projet avec :

```bash
yarn build
```

Assurez-vous de pouvoir faire une construction complète en production avant de pousser du code.

## Tests

Plus d'infos sur comment ajouter de nouveaux tests à venir.

### Exécution des tests

Cela exécutera et testera tous les flux dans plusieurs fenêtres Chromium pour vérifier qu'aucun flux critique ne casse :

```sh
yarn test-e2e
```

#### Résolution des problèmes

##### Navigateurs de test E2E non installés

Exécutez `npx playwright install` pour télécharger les navigateurs de test et résoudre l'erreur ci-dessous lors de l'exécution de `yarn test-e2e` :

```
Executable doesn't exist at /Users/alice/Library/Caches/ms-playwright/chromium-1048/chrome-mac/Chromium.app/Contents/MacOS/Chromium
```

## Linting

Pour vérifier le formatage de votre code :

```sh
yarn lint
```

Si vous obtenez des erreurs, assurez-vous de les corriger avant de valider.

## Faire une demande de tirage (Pull Request)

- Assurez-vous de [cocher l'option "Allow edits from maintainers"](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/allowing-changes-to-a-pull-request-branch-created-from-a-fork) lors de la création de votre PR.
- Si votre PR fait référence à ou corrige un problème, assurez-vous d'ajouter `refs #XXX` ou `fixes #XXX` à la description de la PR. Remplacez `XXX` par le numéro d'issue respectif. Voir plus sur [Lier une demande de tirage à une issue](https://docs.github.com/en/issues/tracking-your-work-with-issues/linking-a-pull-request-to-an-issue).
- Assurez-vous de remplir le modèle de PR en conséquence.
- Consultez les [Directives de contribution à l'application](./packages/app-store/CONTRIBUTING.md) lors de la construction d'intégrations.

## Directives pour la validation du fichier yarn lockfile

Ne validez pas votre `yarn.lock` à moins que vous n'ayez apporté des modifications au `package.json`. Si vous avez déjà validé `yarn.lock` par inadvertance, suivez ces étapes pour annuler :

Si votre dernier commit a le fichier `yarn.lock` avec d'autres fichiers et que vous souhaitez uniquement annuler le commit de `yarn.lock` :

   ```bash
   git checkout HEAD~1 yarn.lock
   git commit -m "Annuler les modifications de yarn.lock"
   ```

_NB_ : Vous devrez peut-être contourner le hook pré-commit en ajoutant `--no-verify` à la commande git commit.
Si vous avez poussé le commit avec `yarn.lock` :

   1. Corrigez le commit localement en utilisant la méthode ci-dessus.
   2. Poussez soigneusement :

   ```bash
   git push origin <nom-de-votre-branche> --force
   ```

Si `yarn.lock` a été validé il y a un certain temps et qu'il y a eu plusieurs commits depuis, vous pouvez utiliser les étapes suivantes pour revenir uniquement aux modifications de `yarn.lock` sans impacter les changements suivants :

1. **Vérifier une version antérieure** :
   - Trouvez le hash de commit avant que `yarn.lock` ait été validé par inadvertance. Vous pouvez le faire en consultant le journal Git :

     ```bash
     git log yarn.lock
     ```

   - Une fois que vous avez identifié le hash du commit, utilisez-le pour vérifier la version précédente de `yarn.lock` :

     ```bash
     git checkout <commit_hash> yarn.lock
     ```

2. **Validez la version restaurée** :
   - Après avoir vérifié la version précédente de `yarn.lock`, validez ce changement :

     ```bash
     git commit -m "Revenir à yarn.lock à son état avant les modifications non intentionnelles"
     ```

3. **Procédez avec prudence** :
   - Si vous devez pousser ce changement, commencez par tirer les dernières modifications de votre branche distante pour vous assurer de ne pas

 écraser d'autres changements récents :

     ```bash
     git pull origin <nom-de-votre-branche>
     ```

   - Ensuite, poussez la branche mise à jour :

     ```bash
     git push origin <nom-de-votre-branche>
     ```

Enfin, assurez-vous de garder les branches à jour (par exemple, cliquez sur le bouton `Update branch` sur la PR GitHub).

---