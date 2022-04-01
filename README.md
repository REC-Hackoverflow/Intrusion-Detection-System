# Intrusion-Detection-System
It is an System for detecting any kind of intrusion at your home. 

# How does the System works
Initially the camera connected to the Raspberry pi captures images, then the images from the Raspberry pi are sent to an AWS Windows VM (capturing and sending images from linux to windows is done through a bash script). 
The VM itself has UiPath studio running with the necessary python ML models. Each image being captured will be sent to the VM running UiPath for movement and object detection. It is necessary to train the faces of the householders at the start, for the model to classify them as safe, additionally it can also identify animals and birds if the customer wishes, so there is no gap for false alerts. If an unregistered face is detected, the model takes images of their face and sends an e-mail to the owner of the household for further confirmation. If the owner identifies them as an intruder, the bot provides options to contact emergency numbers or police directly and can inform about the incident.
