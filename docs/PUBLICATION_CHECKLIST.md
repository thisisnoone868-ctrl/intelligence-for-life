# Liste de contrôle — première édition officielle

Statut : **à réaliser**, aucune release v1.0 approuvée.

## Confidentialité et provenance
- [ ] Vérifier les métadonnées des documents téléchargeables (auteur, commentaires, révisions, propriétés et fichiers embarqués).
- [ ] Vérifier les noms, adresses e-mail et identités de commits, y compris dans l'historique Git.
- [ ] Vérifier que les contributions de tiers sont autorisées à la publication et à la redistribution.
- [ ] Confirmer la formulation de l'origine humaine–IA et l'absence d'approbation institutionnelle.

## Texte et traductions
- [ ] Validation explicite du texte français de référence par l'auteur.
- [ ] Corriger le libellé « candidat RC4 » dans l'édition finale, sans écraser l'archive candidate.
- [ ] Réviser chaque traduction par une personne compétente avant de la marquer « relue ».
- [ ] Documenter les langues provisoires et leurs limites.

## Gouvernance
- [ ] Définir la procédure initiale d'approbation et les voies de contestation.
- [ ] Définir les rôles de maintenance et de modération.
- [ ] Prévoir un forum accessible aux personnes non techniques, sans le rendre obligatoire pour contribuer.

## Authenticité
- [ ] Produire les fichiers officiels à partir d'une source figée.
- [ ] Calculer les empreintes SHA-256 de tous les fichiers de la release.
- [ ] Générer et protéger une clé de signature dédiée au pseudonyme.
- [ ] Signer un manifeste d'empreintes et publier la clé publique par un canal de confiance.
- [ ] Vérifier la signature depuis une machine ou une session distincte.
- [ ] Créer un tag/release v1.0 uniquement après accord explicite.

Une empreinte SHA-256 seule détecte les différences entre fichiers, mais n'authentifie pas l'auteur. Une signature ne vaut que si la clé publique est elle-même authentifiée.
