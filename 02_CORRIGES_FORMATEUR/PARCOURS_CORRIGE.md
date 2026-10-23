# Parcours corrigés - S4

## P01 - Réserver (FR-02 / US-02 / RM-02)
**Précondition :** séance publiée et ouverte, capacité définie ; modalités d'identification **à arbitrer**.
1. Visiteur consulte F01 et ouvre F03 ; il lit les informations disponibles.
2. Il demande une réservation F05 via un parcours utilisable sur téléphone (B-02).
3. Le système contrôle les droits/validations pertinentes et **la capacité au moment de l'enregistrement** F06.
4. Si quota disponible, il enregistre **une seule** réservation confirmée et affiche un état explicite F07.
5. Si séance complète, il refuse la confirmation ferme et affiche le refus.
6. Si deux demandes concourent pour une seule place, une seule au plus reçoit une confirmation.
**Ouvert :** compte requis, champs, confirmation externe, délai d'annulation.

## P02 - Modifier une séance (FR-06 / US-06 / FR-05)
1. Gestionnaire de S1 accède à la gestion des séances S1 selon une habilitation à valider.
2. Il sélectionne une séance S1, saisit un nouvel horaire, confirme.
3. Le système conserve le nouvel horaire et indique que l'opération a réussi.
4. Si gestionnaire S1 tente une modification S2, elle est refusée, sans altération.
**Ouvert :** notification des inscrits, validation des modifications exceptionnelles RA-01, gestion des conflits horaires.
