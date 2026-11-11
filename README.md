# Invitations de mariage — Jadik'Art

Application web d'invitations de mariage personnelles, conçue par **Jadik'Art Design Studio** (Lubumbashi).
Un même site sert pour plusieurs mariages : chaque invité reçoit son propre lien.

## Ce que fait la page
- Invitation personnelle : noms des mariés, invité, nombre de personnes, table, programme (cérémonie civile, religieuse, soirée) avec lieu, heure, tenue et itinéraire.
- Réponse séparée pour chaque événement, avec le nombre exact de personnes et leurs prénoms.
- Pass d'entrée avec QR code personnel, disponible même sans connexion une fois la page ouverte.
- Réponse gardée sur le téléphone en cas de coupure réseau, puis envoyée automatiquement.
- Options grands caractères, contraste élevé et mode sombre.

## Liens
| Usage | Adresse |
|---|---|
| Invitation d'un invité | `/?i=code-de-l-invite` |
| Démonstration (filigrane, rien n'est enregistré) | `/?demo=1` |
| Administration (connexion requise) | `/admin.html` |

## Fichiers
| Fichier | Rôle |
|---|---|
| `index.html` | La page d'invitation (textes, style et fonctionnement) |
| `admin.html` | L'administration : mariages, invités, plan de salle, équipe (accès par connexion e-mail) |
| `qr.js` | Génération du QR code (d'après Kazuhiko Arase, licence MIT) |

## Sécurité
- La page ne contient que la clé **publique** de la base de données. Aucune clé secrète ni aucun mot de passe ne doit être ajouté dans ce dépôt.
- Un invité ne peut lire que sa propre invitation ; la liste des invités et leurs téléphones ne sont jamais accessibles depuis la page publique.
- L'administration n'affiche rien sans connexion. Les droits (administrateur, organisateur, hôte) sont contrôlés par la base elle-même, pas par la page.

## Hébergement
Déployé automatiquement sur Vercel à chaque modification de la branche `main`.

---
© Jadik'Art Design Studio
