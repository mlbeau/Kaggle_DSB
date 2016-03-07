# Kaggle_DSB
Model Submission repository for Kaggle Second Annual Data Science Bowl - Model based on Marko Jocic's Keras solution posted on this site: https://github.com/jocicmarko/kaggle-dsb2-keras/

a. Hardware / OS Platform used for competition: AWS Linux Ubuntu (ami-eda8fc87) g2.2xlarge instance type (8 CPUs, 1 GPU)
b. 3rd-party software (installation steps): Instance image contains Python Keras library and the MXNet Deep Learning framework.
  Keras Dependency - Theano: pip install git+git://github.com/Theano/Theano.git
c. How to train model.  Point train.py at the DSB data.  We used a partition to store the data: /data, so it is necessary to mount the partition unless this process is automated by editing /etc/fstab
execute python train.py to train the model.
d. Making predictions on a new test set:
  
    
