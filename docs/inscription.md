Adhésion au club:

+ Télécharger, remplir et transmettre la [^^fiche inscription 2023-2024^^](resources/Fiche-inscription-2023-2024.docx)



+ Pour une licence A (compétition):
    + lire le Questionnaire Santé relatif <a href="/resources/2-questionnaire_majeur.pdf">^^aux majeurs^^</a> ou <a href="/resources/2-questionnaire_mineur.pdf">^^aux mineurs^^</a>
        + si __NON__ à toutes les réponses, fournir <a href="/resources/2-Attestation_negative.pdf">^^l'attestation de réponse négative^^</a>
        + si __OUI__ à au moins une réponse, fournir un __certificat médical de moins de 3 ans__. Si le certificat médical a été établi il y a 2 ans pour une autre activité sportive, il est encore valable.


```mermaid
flowchart TD
    id0[Télécharger, remplir et transmettre <br/>la fiche inscription 2023-2024]
    id0 --> id1{Licence A <br/>ou <br/>licence B ?} -- Licence A --> id2[Lire le <br/>Questionnaire Santé]
    id2 -- Pour les majeurs --> id2a[Questionnaire majeur]
    id2 -- Pour les majeurs --> id2b[Questionnaire mineur]
    id2 -- NON<br/>à toutes les réponses ? --> id3[Fournir l'attestation<br/>de réponse négative]
    id2 -- OUI<br/>à au moins une réponse ? --> id4[Fournir un certificat médical<br/>de moins de 3 ans]
    id1 -- Licence B --> id5[Régler votre <br/>cotisation]
    id3 --> id5[Régler votre <br/>cotisation]
    id4 --> id5[Régler votre <br/>cotisation]
    click id0 "resources/Fiche-inscription-2023-2024.docx"
    click id2a "resources/2-questionnaire_majeur.pdf"
    click id2b "resources/2-questionnaire_mineur.pdf"
    click id3 "resources/2-Attestation_negative.pdf"
```