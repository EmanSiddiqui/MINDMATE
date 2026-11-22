# MINDMATE AI — GUI version

Updated questionnaire-based GUI, with the original olive/cream visual style.

## Features
- Ten user-supplied daily wellness questions.
- Simple C++ score calculation through POST /api/assessment.
- Personalized Wellness Studio and SUKOON suggestions.
- Monthly report with category bars and assessment-history chart.
- SUKOON Quranic reflections and Wellness Studio activities.
- Browser-local storage, export and delete.
- Get Help page and special handling of question 10.

## Scoring
Q1,Q2,Q5,Q6,Q7,Q8,Q9 use 0=very poor through 4=very good; difficulty = 4-answer. Q3,Q4 use 0=none through 4=extreme; difficulty = answer. Q10 is Yes=1, No=0, Prefer not to answer=-1; it is never added to a score. Skipped questions are -1 and excluded. Each scored response has difficulty 0..4. Overall difficulty is the average of answered Q1..Q9 multiplied by 25, using integer division. Categories: mood Q1-2, stress Q3-4, sleep Q5-6, focus Q7 and Q9, social Q8. Category scores are averages multiplied by 25. Higher scores mean greater reported difficulty, not illness. The overall score does not imply clinical validity.

## Privacy and safety
History is stored only in the browser's unencrypted localStorage, which is inappropriate for shared/public devices. The C++ server does not store assessment answers. Positive Q10 responses display urgent human-support guidance; the app does not contact anyone or monitor emergencies.

## Run
See HOW_TO_RUN.txt.
