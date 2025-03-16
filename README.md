# student-placement-prediction

This repository is a machine learning project aimed at predicting student placement status based on various academic and extracurricular features using both supervised and unsupervised algorithms to compare their performance.

# Dataset

The dataset includes the following features:

- **StudentID**: Unique identifier for each student (removed during preprocessing)
- **CGPA**: Cumulative Grade Point Average
- **Internships**: Number of internships completed
- **Projects**: Number of projects completed
- **Workshops/Certifications**: Number of workshops or certifications completed
- **AptitudeTestScore**: Score in the aptitude test
- **SoftSkillsRating**: Rating of soft skills
- **ExtracurricularActivities**: Participation in extracurricular activities (Yes/No)
- **PlacementTraining**: Participation in placement training (Yes/No)
- **SSC_Marks**: Marks obtained in Secondary School Certificate
- **HSC_Marks**: Marks obtained in Higher Secondary Certificate
- **PlacementStatus**: Placement status (Placed/NotPlaced)

  # Unsupervised Approach: Clustering

  The goal of the unsupervised approach is to group students into clusters based on their features and predict their placement status.
  The clustering approach yielded the following results:

  - Accuracy: 0.7849
  - Precision: 0.7181
  - Recall: 0.8025
  - F1-Score: 0.7580

  # Supervised Approach: Classification

  The goal of the supervised approach is to predict the placement status of students using labeled data. We applied a Logistic Regression model to classify students based on their features.

  - Accuracy: 0.7945
  - Precision: 0.7444
  - Recall: 0.7669
  - F1-Score: 0.7555
