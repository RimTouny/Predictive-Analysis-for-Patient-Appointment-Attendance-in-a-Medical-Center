# **Predictive-Analysis-for-Patient-Appointment-Attendance-in-a-Medical-Center-using R programming language**
This project predicts patient attendance for medical appointments at Bay Clinic using 'medicalcentre.csv'. It employs SVM, Decision Trees, and DNN models, assessing accuracy, sensitivity, specificity, and conducting ROC analysis. The goal is to optimize resource utilization and financial stability in the [MedicalCentre.csv](https://github.com/RimTouny/Predictive-Analysis-for-Patient-Appointment-Attendance-in-a-Medical-Center/files/13894014/MedicalCentre.csv)
er. This analysis was conducted as part of a Data Science course in my master's program at the University of Ottawa 2023.

- Required libraries: scikit-learn, pandas, matplotlib.
- Execute cells in a Jupyter Notebook environment.
- The uploaded code has been executed and tested successfully within the [Google Colab](https://colab.google/) environment.


## Binary-class classification problem
Task is to classify if a patient will show up for an appointment: Yes/ No

### Independent Variables:
   +	'PatientId': Identification of the patient.
   +	'AppointmentID': Identification of the appointment.
   +	'Gender': Gender of the patient.
   +	'ScheduledDay': Date when the appointment is scheduled.
   +	'AppointmentDay': Actual date of the appointment.
   +	'Age': Age of the patient.
   +	'Neighbourhood': Location of the medical center.
   +	'Scholarship': Indicates whether the patient is enrolled in a scholarship program.
   +	'Hipertension': Presence of hypertension in the patient.
   +	'Diabetes': Presence of diabetes in the patient.
   +	'Alcoholism': Indicates whether the patient is affected by alcoholism.
   +	'Handcap': Level of handicap of the patient.
   +	'SMS_received': Indicates if the patient received an SMS reminder.
     
### Target variable:
   +	'No show': Predicting patient attendance (Yes/No) for scheduled medical appointments.

## **Key Tasks Undertaken**

1. **Data Preparation:**
   - Handled missing values and initialized a function for outlier visualization.
   - Counted and removed observations with negative values in the 'Age' feature.
   - Transformed negative values in 'AwaitingTime' to positive values.
   - Encoded string categorical values into integer codes.
   - Separated date features into date components.
   - Rescaled the 'Age' feature using min_max normalization or z_score standardization.
   - Conducted a variability comparison between features using a correlation matrix and dropped correlated features.

2. **Model Development I:**
   - Developed SVM and Decision Tree classifiers for predicting appointment status.
   - Evaluated classifier performance using a 70-30 train-test split.

3. **Model Development II:**
   - Trained a Deep Neural Network using Keras, experimenting with configurations for optimal accuracy.
   - Explored the effects of changing activation functions or dropout rates on model performance.

4. **Model Evaluation & Comparison:**
   - Implemented a function to detect model accuracy and identify potential overfitting.
   - Tuned the models using GridSearchCV for optimization.
   - Evaluated SVM, Decision Tree, and Deep Neural Network classifiers based on Accuracy, Sensitivity, and Specificity.
   - Conducted a ROC analysis to compare SVM and Decision Tree models and plotted the ROC graph for performance assessment.
