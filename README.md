This project is an extention of the work done by Mr. Kaifeng Gao et al. https://github.com/Dawn-LX
is aimed to provide a code for tracklet files generation for classification-and-grounding approach for object detection, tracking, and grounding in video streams. We used Faster R-CNN for classification, modification of deepSORT algorithm for multiple object tracking (MOT), BIG model for generating bipartite graphs, and grounding the detected objects and their relationships between each other on the timestamp of the video.
This code is tested on a small piece of video from the movie The One Flew Over the Cuckoo's Nest.

Usage
To replicate the results, please follow the instructions below:

Generate the output dictionary for deepSORT and save it as a pickle file using the Faster R-CNN output/cuckoo's_nest.ipynb script

Run the deepSORT_tracking_v2.py file, indicating the path to your output dictionary. This will generate a new *.npy file, which represents the tracklet.
Copy your *.npy file to the ~/VidSGG-BIG/tracking_results/[your folder] directory.
Run the BIG model on the tracklet using the infer_nest.py script, indicating the path to your config and checkpoint files, as well as the CUDA device you want to use. This will generate a JSON file with the classification and grounding results.

Contributing

We welcome contributions to this project! Feel free to use this code not for a single file but to adjust it for a bigger dataset, for example.

License
This project is licensed under the MIT License. Please see the LICENSE file for more information.





