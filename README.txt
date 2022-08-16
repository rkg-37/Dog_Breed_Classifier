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
    * --arch,--dir,--dog  are the argument type defined using **argparse module** in python
    example:
             python check_images.py --dir pet_images/ --arch vgg --dogfile dognames.txt
             
  This step outputs the result of the given architecture on the terminal
  
 # How to use this repository
 
 To use classfier for the new Images 
      * add the files in new folder(created by the user)
      * using the execution script add the directory 
      * run it



# sample output


Command Line Arguments:
     dir = pet_images/ 
    arch = resnet 
 dogfile = dognames.txt

Pet Image Label Dictionary has 40 key-value pairs.
Below are 10 of them:
 1 key:           Great_dane_05320.jpg  label:                 great dane
 2 key:               Beagle_01125.jpg  label:                     beagle
 3 key:               Collie_03797.jpg  label:                     collie
 4 key:            Dalmatian_04068.jpg  label:                  dalmatian
 5 key:  Miniature_schnauzer_06884.jpg  label:        miniature schnauzer
 6 key:  German_shepherd_dog_04890.jpg  label:        german shepherd dog
 7 key:              Basenji_00963.jpg  label:                    basenji
 8 key:                     cat_02.jpg  label:                        cat
 9 key:     Golden_retriever_05223.jpg  label:           golden retriever
10 key:        great_horned_owl_02.jpg  label:           great horned owl

 ** Statistics from calculates_results_stats() function:
N Images: 40  N Dog Images: 30  N NotDog Images: 10 
Pct Corr dog: 100.0 Pct Corr NOTdog:  90.0  Pct Corr Breed:  90.0

 ** Check Statistics - calculated from this function as a check:
N Images: 40  N Dog Images: 30  N NotDog Images: 10 
Pct Corr dog: 100.0 Pct Corr NOTdog:  90.0  Pct Corr Breed:  90.0


*** Results Summary for CNN Model Architecture RESNET ***
N Images: 40
N Dog Images: 30
N Non Dog Images: 10
N matches between pet & classifier labels : 33
N correctly classfied dog images : 30
N correctly classfied NON-dog images: 9
N correctly classified dog breeds : 27
P correct matches : 82.5
P correctly classfied dog images : 100.0
P correctly classfied NON-dog images: 90.0
P correctly classified dog breeds: 90.0

               pet label is-a-dog and classifier label is-NOT-a-dog 
                           -OR- 
               pet label is-NOT-a-dog and classifier label is-a-dog 
        
pet_label: cat , classifier_label:norwegian elkhound, elkhound

INCORRECT Dog Breed :
Real: great pyrenees   Classifier: kuvasz
Real: beagle   Classifier: walker hound, walker foxhound
Real: golden retriever   Classifier: leonberg

** Total Elapsed Runtime: 0:0:6
