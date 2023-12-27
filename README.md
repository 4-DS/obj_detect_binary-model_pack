# Step CV-Pipeline: model_pack

During the CV Pipeline Model_Pack stage, the following steps take place:
1. Model conversion     
   The model trained in the previous CV-Pipeline Model_Train stage is converted into a format suitable for specific scenarios. For example, in the case of the Binary CV-Pipeline scenario, the model can be passed in PyTorch or another format in which it was trained.
2. Packaging into BentoArchive     
   After model conversion, the model weights and all necessary artifacts (e.g., test image, predictions on the test image) are packaged into BentoArchive. Packaging into BentoArchive allows creating a containerized application that can be easily deployed and used artifact delivery (inference files) to the production environment.

Input and output for the CV pipeline step:     
<a id="blob-path" href="https://github.com/4-DS/obj_detect_binary-model_pack/blob/main/model_pack.ipynb?short_path=f6cb892#L57C1-L92C17">model_pack.ipynb</a>
