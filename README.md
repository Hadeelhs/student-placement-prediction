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

  The goal of the supervised approach is to predict the placement status of students using labeled data. We applied multiple classifiers :

  - Logistic Regression
  - Decision Tree
  - Random Forest
  - SVM
  - Naive Bayes
# Plot the comparison graph
fig, ax1 = plt.subplots(figsize=(12, 8))

ax2 = ax1.twinx()
width = 0.2

results_df.plot(kind='bar', x='Model', y='Accuracy', ax=ax1, position=1, width=width, legend=False, color='b')
results_df.plot(kind='bar', x='Model', y='F1 Score', ax=ax1, position=0, width=width, legend=False, color='g')
results_df.plot(kind='bar', x='Model', y='Training Time', ax=ax2, position=2, width=width, legend=False, color='r')
results_df.plot(kind='bar', x='Model', y='Prediction Time', ax=ax2, position=3, width=width, legend=False, color='y')

ax1.set_xlabel('Model')
ax1.set_ylabel('Accuracy / F1 Score')
ax2.set_ylabel('Time (seconds)')
ax1.set_title('Comparison of Classification Algorithms')

ax1.legend(['Accuracy', 'F1 Score'], loc='upper left')
ax2.legend(['Training Time', 'Prediction Time'], loc='upper right')

plt.show()
