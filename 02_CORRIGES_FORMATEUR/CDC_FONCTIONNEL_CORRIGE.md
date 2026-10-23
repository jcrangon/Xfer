# CIVILINK - CAHIER DES CHARGES FONCTIONNEL v0.1 - EXEMPLE NON VALIDÉ

## 1. Objectif et périmètre
Terranova (15 structures) étudie une plateforme commune de publication et réservation de séances.
**Proposition MVP :** F01 F03 F04 F05 F06 F07 F09. **Options soumises à arbitrage :** F02 F08.
**Non retenues en V1 candidate :** F10 F11 F12 F13 F14. Objectifs 75 000 € et 6 mois **indicatifs** ; faisabilité à étudier J3.

## 2. Sources et statut
Le dossier pédagogique B-01..B-16 contient des expressions de besoins, hypothèses et options.
Un entretien simulé et non contractuel produit RA-01..RA-08 dans `REPONSES_ENTRETIEN.csv`.
Leurs reformulations documentées figurent dans NB-01..NB-14 dans `CONSOLIDATION_BESOINS.csv`.
Rien dans ce document ne vaut accord de gouvernance ou validation du client.

## 3. Acteurs et responsabilités
Visiteur, participant, gestionnaire local, animateur, direction réseau, DPO, référent technique.
L'accès local à d'autres structures est proposé interdit B-15/RA-02 ; cas animateur multi-structures RA-03 ouvert.
RACI provisoire ; pouvoir du A et politique d'habilitation à approuver.

## 4. Exigences fonctionnelles candidates
- **FR-01 / F01 :** le système présente aux visiteurs les séances publiées avec informations utiles (B-01).
- **FR-02 / F05-F06 :** pour une séance ouverte, le système ne confirme une réservation que si la capacité permet de l'enregistrer sans dépasser le quota (B-02,B-06,RA-04). **RM-02 : total des confirmations ≤ capacité**.
- **FR-03 / F07 :** toute demande traitée a un résultat lisible, confirmé ou refusé ; canal de notification externe non décidé (B-13,RA-08).
- **FR-04 / F09 :** une annulation autorisée libère la place associée ; délai et réattribution à arbitrer (B-09,RA-05).
- **FR-05 / F04 :** un gestionnaire local sans délégation ne consulte ni ne modifie les réservations d'une autre structure (B-15,RA-02). La politique des délégations reste ouverte.
- **FR-06 / F04 :** un rôle dûment autorisé modifie une séance de sa structure ; avis aux inscrits et modifications exceptionnelles à préciser (B-07,RA-01).
- **FR-07 / F05 :** le parcours de réservation doit être utilisable depuis un téléphone et au clavier ; vérifier NFR-02/03 (B-02,B-14,RA-06).
- **FR-08 / F08 :** mécanisme facultatif de liste d'attente, **hors MVP candidat**, non spécifié tant que règles et priorités ne sont pas décidées (B-08,carte C).

## 5. User stories et parcours
US-02 = « En tant que participant, je veux demander une place afin de savoir si ma réservation est confirmée. »
P01 = catalogue → fiche → demande → contrôle capacité → confirmation ou refus.
P02 = gestion S1 autorisée → modification S1 → résultat ; toute action S2 sans habilitation = refus.
Voir `USER_STORIES_CORRIGE.csv` et `PARCOURS_CORRIGE.md` pour les autres cas.

## 6. Acceptation
**T-01** capacité 2, 0 place confirmée → demande valide → 1 confirmation et 1 place restante.
**T-02** capacité 2, déjà 2 confirmées → demande supplémentaire → aucune confirmation supplémentaire.
**T-03** capacité 2, déjà 1 confirmée, deux demandes simultanées → une seule confirmation supplémentaire au plus.
**T-05** annulation autorisée → disponibilité restituée. **T-06** S1 ne lit pas / ne modifie pas S2.
**T-09** navigation intégrale au clavier. **T-11** attente conditionnelle, décision ouverte.
Les critères sont écrits avant développement ; aucun test n'est déclaré réussi.

## 7. Qualités attendues
NFR-01 isolation entre structures, NFR-02 clavier, NFR-03 téléphone ; autres cibles de performance,
disponibilité, restaurabilité ou conservation **non définies**. Des protocoles sont proposés dans NFR.csv.

## 8. Données et interfaces
Données de réservation et contacts éventuels soumis à analyse de nécessité et minimisation ; base légale et durée non établies.
Site vitrine connu (B-10), existence d'une API non prouvée. Fournisseur de notifications non choisi.

## 9. Questions ouvertes prioritaires
Q01 - Compte obligatoire ou facultatif (B-11,B-12,RA-07) ?
Q02 - Qui approuve les droits transverses et les modifications exceptionnelles (RA-01/03) ?
Q03 - Délai d'annulation et priorité liste d'attente (B-09,carte C) ?
Q04 - Canal de confirmation et besoin réel de données personnelles (B-13,RA-08) ?
Q05 - Existence d'API / interlocuteur du site (B-10) ?
Q06 - Volumes mesurés et critères de performance (B-03) ?
Q07 - Responsable du traitement, base légale et durées (B-16,carte D) ?

## 10. Transmission J3
Démontrer les options de solution et les hypothèses de charge ; étudier concurrence T-03 (transactions / verrouillage), sécurité inter-structures, intégration et conformité, puis budgétiser et planifier. La méthode MoSCoW n'est pas une étude de faisabilité.
