# Step CV-Pipeline: model_pack

During the CV Pipeline Model_Pack stage, the following steps take place:
1. Model conversion     
   The model trained in the previous CV-Pipeline Model_Train step is converted into a format suitable for specific scenarios. For example, in the case of the Binary CV-Pipeline scenario, the model can be passed in PyTorch or another format in which it was trained.
2. Packaging into BentoArchive     
   After model conversion, the model weights and all necessary artifacts (e.g., test image, predictions on the test image) are packaged into BentoArchive.

Input data for step CV-Pipeline: model_pack
- **obj_detect_inference_files**     
Saved weights of the trained model (weights of the last epoch and with the best achieved metrics), configuration files from the previous CV-Pipeline step (model_train)

The output of this step CV-Pipeline is
- **bento_service**     
BentoArchive, packaged model service via BentoML (saved as a zip archive)

## How to run a step CV-Pipeline: model_pack

### clone the repository: model_pack
```
git clone --recurse-submodules https://github.com/4-DS/obj_detect_binary-model_pack.git
cd obj_detect_binary-model_pack
```  

### run step CV-Pipeline:model_pack
```
python step.dev.py
```  
or
```
step.prod.py
``` 

