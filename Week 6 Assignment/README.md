# Semaine 6 – Amélioration du modèle, analyse d'erreurs et validation

Diagnostic des faiblesses du modèle de référence de la semaine 5, ingénierie d'une nouvelle
caractéristique et comparaison de modèles candidats, en s'appuyant sur le modèle de base de la
semaine 5.

## Ce qui a été fait

- Reproduit et vérifié le modèle de référence de la semaine 5 (ROC-AUC 0,677, précision 0,627)
- Analysé la matrice de confusion : 166 absences manquées et 194 fausses alertes sur 966 cas de test
- Identifié que le modèle repose surtout sur `booking_lead_days` : les absences correctement
  détectées ont un délai de réservation moyen de ~44 jours, contre ~19 jours pour celles manquées
- Conçu une nouvelle caractéristique d'interaction `leaddays_x_prevrate` (délai × taux d'absences
  passées) pour mieux capturer ce signal
- Entraîné et comparé trois modèles candidats (régression logistique + interaction, Random Forest,
  Gradient Boosting) sur le même découpage par patient que la semaine 5
- Contacté la track Data Analytics (DA) pour obtenir des insights complémentaires par segment
  (en attente de réponse)

## Résultat

Le **Random Forest** est le meilleur candidat : ROC-AUC 0,687, précision 0,636 — une amélioration
réelle mais modeste par rapport à la référence. `booking_lead_days` et la nouvelle interaction
`leaddays_x_prevrate` restent les prédicteurs les plus importants ; `distance_to_clinic_km` ressort
aussi de façon inattendue et reste à approfondir.

## Fichiers

- `notebooks/week6_model_improvement_validation.ipynb`
- `reports/week6_project_summary.docx` *(à préparer)*
- `visuals/`
