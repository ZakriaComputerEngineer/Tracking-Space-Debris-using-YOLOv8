# Tracking-Space-Debris-using-YOLOv8

Project Description: Tracking Space Debris and Other Objects Through Camera

Overview
This project involves tracking space debris and other objects through a camera using a custom-trained YOLOv8 model. The goal was to detect and track multiple classes of objects in images & video, ensuring high accuracy and robustness of the model.

![img091706_jpg rf 749ed824458ea96a34234383f52e5faf](https://github.com/ZakriaComputerEngineer/Tracking-Space-Debris-using-YOLOv8/assets/150436890/ac828cbf-1a3f-49c9-8144-7d365d46d458)


Dataset Preparation

Initial Dataset: Utilized an existing dataset but chose not to use its labels due to their subpar quality.
Link- https://drive.google.com/drive/folders/1cYUHXstqUCjXKG7hKuKqtUsWeQQ_3cYz?usp=sharing

Manual Labeling: Manually boxed and labeled objects in the dataset. Selected 120 images for each of the 11 classes, resulting in a total of 1,320 manually labeled images.
![image](https://github.com/ZakriaComputerEngineer/Tracking-Space-Debris-using-YOLOv8/assets/150436890/0927ff7b-b087-438c-9d46-9595bae88c26)

Data Augmentation: Applied horizontal and vertical flips, and resized all images to 640x640 pixels, expanding the dataset to 2467 images.

Data Split: Divided the dataset into training (70%), validation (20%), and test (10%) sets using Roboflow, ensuring a comprehensive and balanced dataset for model training.
![image](https://github.com/ZakriaComputerEngineer/Tracking-Space-Debris-using-YOLOv8/assets/150436890/44027909-91c4-49c4-ad9e-e071dbbdc9cc)

![image](https://github.com/ZakriaComputerEngineer/Tracking-Space-Debris-using-YOLOv8/assets/150436890/f750172b-364c-470d-b995-9a59b6827a61)

Dataset foramt: Organiszing the images and labels as per YOLOv8 provided format for training and generating the yaml file.
![image](https://github.com/ZakriaComputerEngineer/Tracking-Space-Debris-using-YOLOv8/assets/150436890/af0c5a66-2ddd-43d4-a11e-53a0a66be22b)
![image](https://github.com/ZakriaComputerEngineer/Tracking-Space-Debris-using-YOLOv8/assets/150436890/25a24b5d-276f-4aa4-92b7-87604b375940)
![image](https://github.com/ZakriaComputerEngineer/Tracking-Space-Debris-using-YOLOv8/assets/150436890/6799dc04-ca13-4276-af63-1da465071d27)

Final Dataset: 2467 fined labelled, resized, randomly flipped dataset on yolov8 format.
Link- https://www.kaggle.com/datasets/muhammadzakria2001/space-debris-detection-dataset-for-yolov8

Environment Setup
YOLOv8 Loading: Leveraged the Ultralytics YOLOv8 library for object detection.
![image](https://github.com/ZakriaComputerEngineer/Tracking-Space-Debris-using-YOLOv8/assets/150436890/331f21cf-09eb-400a-a81c-34c8ec024f53)

Kaggle Environment: Utilized Kaggle’s resources for model training, including the latest CUDA, two Tesla T4 GPUs, an Intel Xeon 4-core CPU, 30 GB RAM, and 100 GB disk space.

Model Architecture
![image](https://github.com/ZakriaComputerEngineer/Tracking-Space-Debris-using-YOLOv8/assets/150436890/678dfdc9-4ccd-4202-9764-52c93a91b254)

Model Training

Configuration:
Epochs: 100
Image Size: 640x640 pixels RGB
Optimizer: Adam
Training Duration: Completed the custom training within approximately one hour.
![image](https://github.com/ZakriaComputerEngineer/Tracking-Space-Debris-using-YOLOv8/assets/150436890/272cddd1-6b77-4360-bec2-6184c8cabffb)
![image](https://github.com/ZakriaComputerEngineer/Tracking-Space-Debris-using-YOLOv8/assets/150436890/0cfb8511-6137-49e5-bd87-ef2eeac431df)
![image](https://github.com/ZakriaComputerEngineer/Tracking-Space-Debris-using-YOLOv8/assets/150436890/0d819a21-a4aa-4628-94d9-a901aca9ef17)

Model Testing
Performance: Evaluated the model using the test set, achieving highly accurate and satisfactory results.
Confusion matrix: ![image](https://github.com/ZakriaComputerEngineer/Tracking-Space-Debris-using-YOLOv8/assets/150436890/05eb2450-91e1-42bc-bef6-6a79ab9b55ff)
Training statistics: ![image](https://github.com/ZakriaComputerEngineer/Tracking-Space-Debris-using-YOLOv8/assets/150436890/367996d1-1629-4514-b55f-9e67ea13749b)
![image](https://github.com/ZakriaComputerEngineer/Tracking-Space-Debris-using-YOLOv8/assets/150436890/9f7bf396-b6e3-417c-8f9e-333ef23f2fd9)
Plots: 
Labels
![image](https://github.com/ZakriaComputerEngineer/Tracking-Space-Debris-using-YOLOv8/assets/150436890/0842a33f-fb3d-45bd-ae3c-12fdeb6b302e)
Prediction
![image](https://github.com/ZakriaComputerEngineer/Tracking-Space-Debris-using-YOLOv8/assets/150436890/c61155bd-442c-482f-83b6-ef3a5132670b)

Conclusion
This project demonstrates a comprehensive approach to preparing a high-quality dataset, setting up an efficient training environment, and successfully training and testing a YOLOv8 model for tracking space debris and other objects with impressive accuracy.
