#  Use a Pre-trained Image Classifier to Identify Dog Breeds

This Project uses pretrained Image classifier dog breed model
Architecture: 
    * Alexnet
    * ResNet
    * Vgg
    
Image File:
  * pet_images
  * uploaded Images
  
  
Shell Script:
This files help in batch processing i.e classifying images using different architecture using different models.
This files execute using command: sh file-name.sh
On execution, outputs are saved in the txt file for different architecture.

  * run_models_batch.sh
  * run_models_batch_uploaded.sh
  
# Execution step

* python check_images.py --dir (directory with images) --arch model --dogfile (ile that contains dognames) 
    * --arch,--dir,--dog  are the argument type defined using argparse module in python
    example:
             python check_images.py --dir pet_images/ --arch vgg --dogfile dognames.txt
             
  This step outputs the result of the given architecture on the terminal
  
 # How to use this repository
 
 To use classfier for the new Images 
      * add the files in new folder(created by the user)
      * using the execution script add the directory 
      * run it
