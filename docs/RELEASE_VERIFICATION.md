# Vérifier une édition officielle

**État : procédure proposée, non encore appliquée à une release.**

## Pourquoi la licence ne suffit pas

La licence CC BY-SA 4.0 régit la réutilisation du texte. Elle n'authentifie pas une édition. Une empreinte SHA-256 permet de comparer des fichiers, mais ne prouve pas à elle seule qui les a publiés.

## Procédure de publication envisagée

1. L'auteur approuve explicitement le texte français de référence et les règles initiales.
2. Une branche de préparation est relue ; les modifications sont documentées.
3. Les fichiers de diffusion sont produits à partir de sources figées et contrôlés pour les métadonnées sensibles.
4. Un fichier `SHA256SUMS.txt` contient une empreinte SHA-256 pour chaque fichier distribué.
5. Une clé de signature dédiée au pseudonyme signe le manifeste d'empreintes. Sa clé publique et son empreinte sont publiées par un canal vérifiable.
6. Une release GitHub porte un numéro de version, une date, un changelog, la source française et les traductions explicitement qualifiées.
7. Une vérification indépendante compare les empreintes, la signature et le tag/commit annoncés.

## Exemple de vérification locale

Sur un ordinateur avec `sha256sum` :

```bash
sha256sum -c SHA256SUMS.txt
```

Cette commande ne vérifie **pas** la signature de l'éditeur. La vérification cryptographique de la signature devra être documentée selon l'outil effectivement choisi (par exemple minisign ou GPG) ; ne pas prétendre qu'elle existe avant de l'avoir créée et testée.

## Limites

- Une clé compromise peut signer une édition frauduleuse ; prévoir une procédure de révocation.
- Un dépôt public peut être copié ou adapté légalement selon la licence ; cela ne fait pas des copies des éditions officielles.
- Les tags Git peuvent être déplacés si les protections sont insuffisantes. Les releases doivent être conservées et idéalement protégées contre la modification.
- L'historique Git peut révéler des noms et adresses e-mail même si les fichiers actuels sont anonymisés.

**Aucune signature officielle n'a encore été émise.**
