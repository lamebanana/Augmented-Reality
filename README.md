# Augmented Reality
Computer Vision and Image Processing project. A label is overimposed on a video of a book. In the video rotations as well as translations and changes of brightness and saturation happen. The label is overimposed realistically over the video in a robust way, aligned with the rotations and saturation changes happening in the video.

Augmenting the label requires detecting the object in every frame of the video, thus requiring a reference frame acting as a query for our target image, which is the current video frame.

As far as the choice of the reference frame is concerned, two methods are employed:

1. **Frame to Reference method - F2R**

  The reference frame is the first frame of the video. The reference is the same throghout the whole process. This can lead to huge differences between the query image     and the target image, causing difficulties in finding correct correspondences. Still, only one homography is required, so there is no propagation error as in the F2F     method.

    [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1ZD_a8uxjsh4TGymP5mrJ3MxTmxuiJYOk?usp=sharing)
  
-------------------------------


2. **Frame to Frame method - F2F**

  The reference frame is the previous frame of the video. The query is constantly changing, so a different homography has to be chained for every frame of the video.       Even if in this way there are less differences between query and target image, this requires chaining various homographies, resulting in a propagation of errors that     can impact the overall augmentation result.


    [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1RGYtuFpIopyCx1y-1sidFPCJKJw1N3Vw?usp=sharing) 

-------------------------------
