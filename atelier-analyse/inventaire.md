# Inventaire des points d'entrée

Le livrable de l'atelier d'analyse. Il dit ce que l'API devra **permettre** — pas comment on
l'écrira.

Une règle : tout ce qui figure ici doit se justifier par la lettre de mission ou par un écran
des maquettes. Si vous ne savez plus d'où vient une ligne, c'est peut-être qu'elle n'en vient
pas. (Seule exception : la section bonus, si vous en ajoutez une.)

---

## Ce que l'utilisateur peut faire

Une action par ligne, en français. Pas encore de chemins.

- S'inscrire
- Se connecter
- Rechercher les trajets disponibles
- Afficher les villes disponibles
- Afficher les détails d'un trajet
- Mettre ses réservations dans un panier
- Voir le panier
- Payer son panier
- Voir ses billets
- Voir ses données personnelles

## Les points d'entrée

| Ce que ça fait                       | Chemin proposé      | Qui peut l'appeler     |
|--------------------------------------|---------------------|------------------------|
| s'inscrire                           | POST /signin        | tous les utilisateurs  |
| se connecter                         | POST /login         | tous les utilisateurs  |
| rechercher les trajets correspondant | POST /search        | tous les utilisateurs  |
| lister les villes disponibles        | GET /cities         | tous les utilisateurs  |
| afficher les détails d'un trajet     | GET /detail{id}     | tous les utilisateur   |
| ajouter une réservation au panier    | POST /booking/{id}  | utilisateurs connectés |
| voir le panier                       | GET /cart           | utilisateurs connectés |
| supprimer un billet du panier        | DELETE /ticket/{id} | utilisateurs connéctés |
| payer son panier                     | POST /pay/{id}      | utilisateurs connectés |
| voir ses billets                     | GET /tickets        | utilisateurs connectés |
| voir ses données personnelles        | GET /profil         | utilisateurs connectés |

## Les données qui circulent

Pour chaque point d'entrée : ce qu'il reçoit, ce qu'il renvoie. Nommez les données comme
l'Office les nomme — les traduire en identifiants techniques, c'est le travail de demain.

### <POST /signin>
### <POST /login>
### <POST /search>
### <GET /cities>
### <GET /details/{id}>
### <POST /booking/{id}>
### <GET /cart>
### <DELETE /ticket/{id}>
### <POST /pay>
### <GET /tickets>
### <GET /profil>

## Ce dont on n'est pas sûrs

Les questions que la lettre et les maquettes ne tranchent pas. Une question notée vaut mieux
qu'une réponse inventée.

- supprimer un billet du panier
