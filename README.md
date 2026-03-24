Overview of the Assignment Research Task 1 COMP6011

This report implements and evaluates a computer vision perception pipeline for Advanced Driver Assistance Systems (ADAS).

It consists of three main experiments:

            1. YOLOv5 → Object Detection
            2. DeepLabV3+ → Semantic Segmentation
            3. Combined Pipeline → Integrated Scene Understanding

Objectives - 

  Perform object detection using YOLOv5
  Perform semantic segmentation using DeepLabV3+
  Combine both outputs into a unified perception pipeline
  Evaluate the performance qualitatively and quantitatively

Technologies used - 

      Python
      PyTorch
      YOLOv5 (Ultralytics)
      segmentation-models-pytorch
      OpenCV
      NumPy
      Matplotlib
      Google Colab


Experiment 1 - yolov5

Steps:  Clone YOLOv5 repository.
        Manually add the test_image.jpg image to the folder
        Load pretrained weights.
        Run inference on test image.
        Visualize detections.

Output: Bounding boxes
        Class labels (car, person, bicycle)
        Confidence scores

Observation:  Fast and suitable for real-time detection
              Works well for common road objects
              Slight drop in accuracy for small/distant objects


Experiment 2 - DeepLabv3+

Steps:  Change the Runtime type from CPU to T4 GPU
        Load the pretrained DeepLabV3+ model
        Manually add the test_image.jpg and the mask.png images to the folder
        Preprocess the image
        Generate the segmentation mask
        Visualize the results

Output: Pixel-wise segmentation mask
        Color-coded classes
        Overlay visualization

Observation:  Provides detailed scene understanding
              Accurate road and lane detection
              Slight noise in boundaries


Experiment 3 - Combined pipeline evaluation

Steps:  Input images (test_image.jpg and mask.png)
        YOLO detects objects
        DeepLab segments scene
        Outputs are merged

Observations: Combined pipeline improves the scene understanding
              Detection and segmentation provides richer context
              Slight increase in the computation time


