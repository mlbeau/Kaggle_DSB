# Kaggle - DSB

Model Submission repository for Kaggle Second Annual Data Science Bowl - Model based on Marko Jocic's Keras solution posted on this site: 
https://github.com/jocicmarko/kaggle-dsb2-keras/



Hardware / OS Platform used for competition: AWS Linux Ubuntu (ami-eda8fc87) g2.2xlarge instance type (8 CPUs, 1 GPU).

Instance image contains Python Keras library and the MXNet Deep Learning framework.
  Keras Dependency - Theano: pip install git+git://github.com/Theano/Theano.git

How to train model:
•	Download the data
•	Point train.py at the DSB data.  We used a partition to store the data: /data, so it is necessary to mount the partition unless this process is automated by editing /etc/fstab
•	execute python train.py to train the model.

Making predictions on a new test set:

•	Submission file is generated for the trained model by executing submission.py with:
   	  python submission.py.

This program loads the systole and diastole models and best weights saved in weights_systole_best.hd5 and weights_diastole_best.hd5 respectively.  Validation data is loaded into memory from the data stored in X_validate.npy and ids_validate.npy.
   
pred_systole and pred_diastole variables are constructed with the models using validation data.  Predictive Cumumlative Distribution Functions (CDF) are formed with real_to_cdf utility developed by Marko Jocic which incorporates predicted values and RMSE loss values for sigma.  
    
