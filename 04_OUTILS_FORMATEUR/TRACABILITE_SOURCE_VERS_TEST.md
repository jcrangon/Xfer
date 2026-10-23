# Exemple fil rouge unique - B-06 vers T-03

**Source** B-06 « Chaque séance a un nombre de places ; nous devons éviter les inscriptions au-delà du nombre prévu. »
**Réponse** RA-04 « Pour une séance de dix places, nous ne voulons pas onze inscriptions confirmées. »
**Consolidation** NB-03 « Empêcher les confirmations au-delà de la capacité de la séance ».
**Fonction candidate** F06 contrôle de capacité, nécessaire à F05 réservation.
**Décision MoSCoW** Must candidat (sans cela, le cœur de réservation est incorrect).
**Exigence** FR-02 : confirmer uniquement si l'enregistrement respecte le quota.
**Story** US-02 : le participant demande une place et connaît le résultat.
**Règle** RM-02 : total des confirmations ≤ capacité.
**Parcours** P01 : demande → contrôle atomique de la capacité → confirmation ou refus.
**Tests** T-01 normal, T-02 complet, T-03 concurrence dernière place.
**Risques J3** transaction/concurrence, estimation charge, faisabilité budgétaire.

Si une ligne manque, l'étudiant ne doit pas avancer en inventant sa justification.
