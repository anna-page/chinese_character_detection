# Chinese Character Detection

In addition to the report and the original notebook, this repository contains two pickle files which contain the training and validation history for the two models, `NoPoolsAllowed` and `UnspiredNet`. It also contains trained parameter files for these two models. For all of these, the files names specify the model used, the optimizer used (Adam), the learning rate, and the number of epochs.

## Generating Predictions on New Test Images

In order to generate and evaluate the predictions on a novel test dataset for either of the two models, there is an additional `simplified_duplicate_for_test_images.ipynb` notebook. To use this, you will need to populate two variables at the start of the notebook: 

  - `IMAGE_DIR`: this is the directory that contains the test images on which you want to generate predictions 
  - `JSON_DIR`: this directory must contain an `ìnfo.json` file and a `jsonl` file. These files contain metadata about the images such as height and width, and the locations of bounding boxes, respectively

Once these variables have been specified, it should be possible to run the entire notebook to generate predictions from the test set, evaluate their performance, and display the predicted location of bounding boxes (if any).
