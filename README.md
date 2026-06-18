# Graphcore IPU Projects: camelyon17-wilds image classification 
## Resnet18 model & datasets:
>* Resnet18 to test a train model, a validation model and their weight transfer between the corresponding wrappers
>* A set of small datasets randomly selected from the original camelyon17-wilds to speed up the training and avoid the OOM.
>* some features:<br>
                  `Host model`<br>
                       ↓<br>
              **Training executable** -> copyWeightsToHost()<br>
                                               ↓<br>
                                          `Validation model`   ->     copyWeightsToDevice()<br>
                                                                             ↓<br>
                                                                   **Inference executable**<br>

      


