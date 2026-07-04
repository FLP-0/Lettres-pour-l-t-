# ✉️🌞 Lettres pour l'été

Un petit site tout doux pour **s'écrire des lettres** : on entre un code secret,
on ouvre sa boîte, et on peut **écrire, dessiner et ajouter des photos** (façon
petites photos argentiques). Chaque lettre terminée rejoint la pile d'enveloppes.

## Comment ça marche

1. **Accueil** — on saisit un code secret.
2. **La boîte** — on y voit toutes les enveloppes déjà écrites + un bouton « ✍️ Écrire ».
3. **L'éditeur** — une feuille vierge où l'on peut :
   - ✍️ écrire du texte,
   - 🎨 dessiner au doigt (ou à la souris),
   - 📷 ajouter des photos (affichées en style polaroïd).
4. La lettre terminée **s'ajoute à la pile** de la boîte.

## Les codes secrets

Les codes sont écrits **en dur** dans `index.html` (pas de serveur, tout reste simple).
Pour les modifier, ouvre `index.html` et cherche la section `const CODES` :

```js
const CODES = {
  "ete2026":  "Boîte de l'été",
  "soleil":   "Boîte de Soleil",
  "lettre":   "Boîte secrète",
};
```

Ajoute, retire ou renomme les codes comme tu veux. **Chaque code a sa propre boîte.**

## Bon à savoir

- ⚠️ **Pas de serveur pour l'instant** : les lettres sont enregistrées dans la
  mémoire du navigateur (`localStorage`) de **l'appareil utilisé**. Une lettre
  écrite sur un téléphone n'apparaît donc pas sur un autre appareil. C'est parfait
  comme carnet de lettres personnel ; un vrai partage entre plusieurs personnes
  demandera d'ajouter un petit serveur plus tard.
- Les photos sont automatiquement redimensionnées pour rester légères.

## Déploiement sur Vercel

Le projet est un simple fichier statique — **aucune configuration nécessaire**.

1. Va sur [vercel.com](https://vercel.com) et connecte ton compte GitHub.
2. **Add New → Project**, puis importe le dépôt `Lettres-pour-l-t-`.
3. Laisse tous les réglages par défaut (framework : *Other*) et clique **Deploy**.
4. Vercel te donne une URL du type `https://lettres-pour-l-ete.vercel.app` 🎉

À chaque `git push`, Vercel redéploie automatiquement le site.
