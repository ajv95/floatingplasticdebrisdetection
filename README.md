# Floating Plastic Debris Detection with Deep Learning and Computer Vision
This repository comprises all the code and notebooks that I used for the content of my MSc thesis. The content revolves around the detection of floating plastic debris in waterways with computer vision and deep learning techniques.

The model accuracies for the detection of plastic debris for a from scratch built baseline model and five state-of-the-art algorithms was done in the Tensorflow and Keras libraries. The notebooks can be found in in the 'image classification' folder. For carrying out the computations the notebook should be uploaded to Google Drive to run the notebook via Google Colab (enable the GPU). 
For training with **pre-trained weights** and **from scratch** in the 'Transfer Learning for four classes' notebook, set **model.trainable=False** or **model.trainable=True** respectively. 


Please send a mail to andrevallendar95@gmail.com, if you want to have access to all the data and model weights.

set PYTHONPATH=C:\river_plastic_detection;C:\river_plastic_detection\slim
set PATH=%PATH%;PYTHONPATH

cd C:/river_plastic_detection
protoc --python_out=. .\object_detection\protos\anchor_generator.proto .\object_detection\protos\argmax_matcher.proto .\object_detection\protos\bipartite_matcher.proto .\object_detection\protos\box_coder.proto .\object_detection\protos\box_predictor.proto .\object_detection\protos\eval.proto .\object_detection\protos\faster_rcnn.proto .\object_detection\protos\faster_rcnn_box_coder.proto .\object_detection\protos\grid_anchor_generator.proto .\object_detection\protos\hyperparams.proto .\object_detection\protos\image_resizer.proto .\object_detection\protos\input_reader.proto .\object_detection\protos\losses.proto .\object_detection\protos\matcher.proto .\object_detection\protos\mean_stddev_box_coder.proto .\object_detection\protos\model.proto .\object_detection\protos\optimizer.proto .\object_detection\protos\pipeline.proto .\object_detection\protos\post_processing.proto .\object_detection\protos\preprocessor.proto .\object_detection\protos\region_similarity_calculator.proto .\object_detection\protos\square_box_coder.proto .\object_detection\protos\ssd.proto .\object_detection\protos\ssd_anchor_generator.proto .\object_detection\protos\string_int_label_map.proto .\object_detection\protos\train.proto .\object_detection\protos\keypoint_box_coder.proto .\object_detection\protos\multiscale_anchor_generator.proto .\object_detection\protos\graph_rewriter.proto

python setup.py build
python setup.py install

