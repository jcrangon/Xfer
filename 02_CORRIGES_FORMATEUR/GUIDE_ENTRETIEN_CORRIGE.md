# Guide de questions et d'entretien - corrigé commenté

Le rôle analyste commence par des questions ouvertes, relance avec un cas limite, puis vérifie la portée de la réponse.
Chaque ligne RA indique une réponse **simulée et conditionnée à la question posée**, pas une signature.

| ID | Origine | Question neutre | Relance utile | Réponse simulée possible |
|---|---|---|---|---|
| E01 | B-11,B-12 | Comment un participant s'inscrit-il aujourd'hui ? | Un compte est-il exigé, pourquoi ? | RA-07 ; arbitrage ouvert |
| E02 | B-02 | Quelles actions doivent fonctionner sur téléphone ? | Exigez-vous une application à installer ? | RA-06 ; non-natif |
| E03 | B-06 | Comment s'applique la capacité d'une séance ? | Deux demandes sur la dernière place ? | RA-04 ; pas de 11e confirmation |
| E04 | B-08 | Comment traitez-vous les personnes en attente ? | Qui est prioritaire ? | INCONNU |
| E05 | B-09 | Que se passe-t-il lorsqu'une inscription est annulée ? | La place revient-elle disponible ? | RA-05 ; réattribution inconnue |
| E06 | B-07 | Qui publie et modifie une séance ? | Qui valide une exception ? | RA-01 ; exception inconnue |
| E07 | B-16 | Quelles données et quelle finalité ? | Qui décide la durée ? | INCONNU |
| E08 | B-15 | Qui peut consulter les inscriptions de chaque structure ? | Animateur S1+S2 ? | RA-02 / RA-03 |
| E09 | B-13 | Comment sait-on que la réservation est confirmée ? | Canal, contenu, preuve ? | RA-08 ; canal inconnu |
| E10 | B-04 | Le paiement est-il nécessaire dès V1 ? | Quel atelier facturé ? | RA-08 ; non décidé |
| E11 | B-10 | Quelle liaison avec le site existant ? | Qui détient la documentation ? | INCONNU |
| E12 | B-05 | Sur quels usages voulez-vous évaluer la V1 ? | Que reporteriez-vous ? | À négocier carte B |

## Mise au propre après entretien
- Reporter **mot à mot** RA-01 à RA-08 dans `REPONSES_ENTRETIEN.csv`.
- Pour toute réponse absente, garder `INCONNU` ; ne jamais compléter avec l'IA.
- Transformer les réponses utiles en `CONSOLIDATION_BESOINS.csv` avec leurs sources, et seulement ensuite aborder `BACKLOG.csv`.
