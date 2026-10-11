# Using DETR Transformers for Basic Sign Language Estimation
It's a full end to end DETR object detection pipeline, in this video its fine tuned for detecting signs but it could definitely be repurposed for other object detection tasks. It covers: 
⚡️ Detections using my pre-trained transformer

💾 Collecting custom data for you to train your own

🏋🏽‍♀️ Fine tuning, with or without pre-trained weights



# Setup 🪛
1. Install UV - `pip install uv`
2. Clone the repo - `git clone https://github.com/nicknochnack/SignDETR .`
3. Install all the dependencies `uv sync`

# Collecting images 
1. Update classes in `src/utils/collect_images.py`
2. Run the script `uv run src/utils/collect_images.py`

# Labelling them 
1. Make sure label-studio is installed `uv pip list | grep label-studio`
2. Run the labelling tool `uv run label-studio`
3. Create new project, setup 
4. Labelling shortcuts CTRL + Enter submit, enter number per label 

# Training 🦾
1. Create a checkpoints folder `mkdir checkpoints`
2. Run the training pipeline `uv run src/train.py`

# Running  🚀 
1. To test on your test set, update the checkpoint parameter in `test.py` then run `uv run src/test.py`
2. To run in real time, update the checkpoint parameter in `realtime.py` then run `uv run src/realtime.py`</br> 
<strong>N.B.</strong> you might need need to update your camera parameter in cv2.VideoCapture() to get the right webcam for your machine. 

