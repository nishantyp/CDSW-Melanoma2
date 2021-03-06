# Deep Learning In Medicine 
## Classifying Melanoma on Cloudera Data Science Workbench, and Cloudera Machine Learning   

[skiaie@cloudera.com](mailto:skiaie@cloudera.com)

<BR>



### Summary

1. Take open source images of skin lesions, and use those to build a classifier to detect malignant skin lesions
2. Evaluate the performance of the model using TensorBoard, and matplotlib in CDSW
3. Deploy the model onto a mobile device for use in clinical settings
4. Use the mobile app to determine if a patient needs critical attention from a physician (Note: in the demo we use a model deployed on a mobile device, for simplicity.  I.e. inference happens on the edge, using a low latency, MobileNet model.  The more likely choice for this use case would be to perform classification in batch or perform the inference centrally, using a model with superior performance characteristics (measured by AUC).


<p><br><p>


<p align="center"><b>1.</b> </p>
	<p align="center"><img src="images/ISIC.PNG" width="600"></p>

<!-- downarrow -->
<h1> <p align="center"> &downarrow; </p> </h1>



<p align="center"><b>2.</b></p>
<p align="center"><img src="images/TensorboardGraphs.PNG" width="600"></p>

<!-- downarrow -->
<h1> <p align="center"> &downarrow; </p> </h1>


<p align="center"><b>3.</b></p>
	<p align="center"><img src="images/TensorboardHistograms.PNG" width="600"></p>

<!-- downarrow -->
<h1> <p align="center"> &downarrow; </p> </h1>


<p align="center"><b>4.</b></p>
	<p align="center"><img src="images/Mobile.PNG" width="600"></p>

<p><br><br><p>

### Talk Tracks (Preliminary):

- [Deck and Demo Talk Track](https://rebrand.ly/6t1d66b)


### Deck:

- [De](https://rebrand.ly/nrdz1m)[ck](https://rebrand.ly/nrdz1m)

<p><br><p>


### Demo Setup

The setup takes 5 minutes

<br>


1. In CDSW Go to Projects, and create a New Project

<br>

<p align="center"><img src="images/CreateProject.PNG" width="600"></p>

<p><br><p>


2. Name the Project "Melanoma Classification", and in the initial setup use git repo: https://github.com/hortonworks-sk/CDSW-Melanoma2.git , and hit the create button

<p><br><p>

<p align="center"><img src="images/CreateProject2.PNG" width="600"></p>

<p><br><p>


3. Launch a Python 3 workbench session

<p><br><p>

<p align="center"><img src="images/OpenWorkBench.PNG" width="600"></p>

<p><br><p>

4. Navigate to the load-libraries.sh script, and run the script. This will load the libraries needed for the demo.

<p><br><p>

<p align="center"><img src="images/OpenWorkBench2.PNG" width="600"></p>

<p><br><p>

5. Stop the Python 3 workbench session, and open another Python 3 session. This is required for some of the libraries to be available.

<p><br><p>

<p align="center"><img src="images/StopSession.PNG" width="600"></p>

<p><br><p>

6. Navigate to the start_tensorboard.py script, and run this.  

If this step fails reach out on email/slack, and continue on with the rest of the steps.  Sometimes there are issues with package loads.  I can work with you on those. 

<p><br><p>

<p align="center"><img src="images/StartTensorboard.PNG" width="600"></p>

<p><br><p>

7. Check that the Tensorboard link is displaying in CDSW and that tensorboard is running, by clicking the tensorboard link

<p><br><p>

<p align="center"><img src="images/OpenTensorboard.PNG" width="600"></p>

<p><br><p>


8. Click on the tensorboard tabs for Scalars , Graph and the Histograms , to check that these are displaying correctly (each are shown in order below)

<p><br><p>

<p align="center"><img src="images/TensorboardGraphs.PNG" width="600"></p>

<p><br><p>


<p align="center"><img src="images/TensorboardScalars.PNG" width="600"></p>

<p><br><p>

<p align="center"><img src="images/TensorboardHistograms.PNG" width="600"></p>

<p><br><p>

9. Navigate to experiments and click run experiment

<p><br><p>

<p align="center"><img src="images/Experiments.PNG" width="600"></p>


<p><br><p>

10. Run experiments for the **_Inception3.py , and ** _VGG16.py**, scripts.  Use the python 3 kernel. No need to supply arguments for these. 

<p><br><p>

<p align="center"><img src="images/Experiments-Inception.PNG" width="600"></p>

<p><br><p>


11. When these runs have completed, you should see the experiments listed as successful in the experiments view (as in the screenshot below)

<p><br><p>

<p align="center"><img src="images/Experiments-List.PNG" width="600"></p>

<p><br><p>

### Pre-Demo Setup

Having the following tabs open, in a Chrome window, may be useful (these are the tabs open in the talk track video):

<p><br><p>


1.  The ISIC dataset homepage (https://www.isic-archive.com/#!/topWithHeader/wideContentTop/main)


2.  The CDSW file view of the training data folder http://your-cdsw-host.and-domain.com/yourusername/melanoma-classification/files/demo/data/test/   (This is at the folder path:    demo > data > test  in CDSW)

<p><br><p>

<p align="center"><img src="images/DataFolders.PNG" width="600"></p>

<p><br><p>

3.  A Python 3 workbench session (loaded within the Classifying Melanoma project) pointing to the script to train the classifier  (This is at the path:    demo > models > classifier3.py, in CDSW)

<p><br><p>

<p align="center"><img src="images/CDSWSession_Classifier.PNG" width="600"></p>

<p><br><p>

4.  Tensorboard, with the Graph view 

<p><br><p>

<p align="center"><img src="images/TensorboardGraphs.PNG" width="600"></p>

<p><br><p>

5.  The new Projects http://your-cdsw-host.and-domain.com/projects/new

<p><br><p>

<p align="center"><img src="images/CDSWSession_Classifier.PNG" width="600"></p>

<p><br><p>

6.  The experiments page


7.   http://[your-cdsw-host.and-domain.com]/projects/new/[your-username]/mel2/runs admin/mel2/runs



### Use Case & Industry Applicability

- Use Case:  Diagnosing Melanoma
- Broader Healthcare Applicability:
  - Disease diagnosis using medical images
    - radiology (arteriography, mammography, radiomics)
    - dermatology
    - oncology

- Broader Industry applicability
  - Biotech
  - Pharma
  - Semiconductor Fabrication

