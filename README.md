# TensorFlow - Help Protect the Great Barrier Reef
Australia's stunningly beautiful Great Barrier Reef is the world’s largest coral reef and home to 1,500 species of fish, 400 species of corals, 130 species of sharks, rays, and a massive variety of other sea life.

Unfortunately, the reef is under threat, in part because of the overpopulation of one particular starfish – the coral-eating crown-of-thorns starfish (or COTS for short). Scientists, tourism operators and reef managers established a large-scale intervention program to control COTS outbreaks to ecologically sustainable levels.

[<img width="400" height="250" src="https://user-images.githubusercontent.com/51321172/183879687-e5201d27-5b78-4b88-8e2c-887a51110f2f.jpg">](https://www.youtube.com/watch?v=UT2noVDFoaA)

To know where the COTS are, a traditional reef survey method, called "Manta Tow", is performed by a snorkel diver. While towed by a boat, they visually assess the reef, stopping to record variables observed every 200m. While generally effective, this method faces clear limitations, including operational scalability, data resolution, reliability, and traceability.

The Great Barrier Reef Foundation established an [innovation program](https://www.barrierreef.org/what-we-do/reef-trust-partnership/crown-of-thorns-starfish-control) to develop new survey and intervention methods to provide a step change in COTS Control. Underwater cameras will collect thousands of reef images and AI technology could drastically improve the efficiency and scale at which reef managers detect and control COTS outbreaks.

To scale up video-based surveying systems, Australia’s national science agency, CSIRO has teamed up with Google to develop innovative machine learning technology that can analyse large image datasets accurately, efficiently, and in near real-time.

# Goal of the Competition
The goal of this competition was to accurately identify starfish in real-time by building an object detection model trained on underwater videos of coral reefs.

# Approach
<img align = "right" src="https://user-images.githubusercontent.com/51321172/183874293-6b47e957-7de4-4d14-87b6-c5d95206d76a.jpg">
<p align="left">
This was my first object detection and localization based competition. The dataset provided had labels in COCO file format (x_min, y_min, width, height) which had to be converted to YOLO format [class_id, x_mid, y_mid, width, height]. Once the labels were converted to desired format, the dataset needed to arranged in certain format as shown in the figure.

Next, instead of training the model from scratch, I downloaded the pretrained weights for my model (YOLOv5s in this case) from [here](https://github.com/ultralytics/yolov5/releases). The public score attained on finetuning the model on 50 epochs was 0.335, which I believe is quite poor.
<p/>

# Final Word and Future Scope
There are several ways in which the accuracy of the model can be increased: 
1) Finetuning YOLOv5s on 50 epochs seems quite less, atleast a 100 epochs would give decent results.
2) YOLOv5s has very less parameters compared to YOLOv5m, YOLOv5l, YOLOv5x and YOLOv5x6. Hence trying out those models might give better results.
3) Several competition winners have made their solutions public, where some have tried ensemble technique with different version of YOLOv5 and have also got good results. It is therefore recommended to checkout top 10 winners solutions.
4) A full documentation for finetuning the model to get best results are mentioned in this [document](https://docs.ultralytics.com/tutorials/training-tips-best-results/#).
5) Also, YOLOv6 and YOLOv7 are out now, so they should be definitely given a chance.

# References
1) Kaggle competition: [TensorFlow - Help Protect the Great Barrier Reef](https://www.kaggle.com/competitions/tensorflow-great-barrier-reef/overview) organised by Tensorflow.
2) YouTube Video: [Help Protect the Great Barrier Reef with Machine Learning](https://www.youtube.com/watch?v=UT2noVDFoaA) on [Tensorflow's YouTube Channel](https://www.youtube.com/c/TensorFlow).
3) Yolov5 github: [Ultralytics YOLOv5](https://github.com/ultralytics/yolov5).
4) Abhisek Thankur's Video on [YOLOv5 Tutorial](https://www.youtube.com/watch?v=NU9Xr_NYslo&t=670s) 
