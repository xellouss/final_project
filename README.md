# Waste Sorting Assistant 

 Description: My Project is using classification to help people sort out different types of trash and to help people classify the different types of trash. 
![add image descrition here](direct image link here)

## The Algorithm

	For my model, I would use one line of code, specifically “python3 train.py --model-dir=models/trashclassset data/trashclassset” and i used it multiple times so that my AI model will be able to recognize different trash objects, like cardboard,in which it recognizes cardboard by 97.75%.

## Running this project

To run this project, there would be 6 different steps into running the project. 

First, we would start running the project by using “cd ~/jetson-inference/
./docker/run.sh”
Secondly, We have to cd into the correct folder by using the command “
cd python/training/classification”, (we are cding into classification because the Waste Sorting Assistant will be classifying different pieces of trash).
Thirdly, we have to start training the model by doing “python3 train.py --model-dir=models/trashclassset data/trashclassset”, so it will be trained to classify and identify different objects.
Fourthly, we would export the model by doing the command “python3 onnx_export.py --model-dir=models/trashclassset”
Fifth on the list, we would have to identify the dataset right before we start the image classification for the AI,, using the model “NET=models/trashclassset DATASET=data/trashclassset”
Sixth and Lastly, we would start the classification process by using the command “imagenet.py \
  --model=$NET/resnet18.onnx \
  --labels=$DATASET/labels.txt \
  --input_blob=input_0 \
  --output_blob=output_0 \
  $DATASET/test/cardboard/cardboard3.jpg $DATASET/output.jpg” 

