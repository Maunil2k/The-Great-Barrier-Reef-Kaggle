# TensorFlow - Help Protect the Great Barrier Reef
Australia's stunningly beautiful Great Barrier Reef is the world’s largest coral reef and home to 1,500 species of fish, 400 species of corals, 130 species of sharks, rays, and a massive variety of other sea life.

Unfortunately, the reef is under threat, in part because of the overpopulation of one particular starfish – the coral-eating crown-of-thorns starfish (or COTS for short). Scientists, tourism operators and reef managers established a large-scale intervention program to control COTS outbreaks to ecologically sustainable levels.

To know where the COTS are, a traditional reef survey method, called "Manta Tow", is performed by a snorkel diver. While towed by a boat, they visually assess the reef, stopping to record variables observed every 200m. While generally effective, this method faces clear limitations, including operational scalability, data resolution, reliability, and traceability.

The Great Barrier Reef Foundation established an [innovation program](https://www.barrierreef.org/what-we-do/reef-trust-partnership/crown-of-thorns-starfish-control) to develop new survey and intervention methods to provide a step change in COTS Control. Underwater cameras will collect thousands of reef images and AI technology could drastically improve the efficiency and scale at which reef managers detect and control COTS outbreaks.

To scale up video-based surveying systems, Australia’s national science agency, CSIRO has teamed up with Google to develop innovative machine learning technology that can analyse large image datasets accurately, efficiently, and in near real-time.

# Goal of the Competition
The goal of this competition was to accurately identify starfish in real-time by building an object detection model trained on underwater videos of coral reefs.

# Approach
This was my first object detection and localization based competition. The dataset provided had labels in COCO file format (x_min, y_min, width, height) which had to be converted to YOLO format [class_id, x_mid, y_mid, width, height]. Once the labels were converted to desired format, the dataset needed to arranged in certain format as shown below

Dataset
  |
  |--Images
  |   |--Train
  |   |--Validation
  |
  |--Labels
  |   |--Train
  |   |--Validation
