# 24Fall HPML-project
## Team members
Huaqiu Liu

Bonan Wang

## A description of the project
### Problem statement: 
Aims to discover the difference in pruning in each of the MLP layers from different attention blocks
### Solution approach: 
(1) Divide layers of GPT2 into three blocks: the front one, the middle one, and the back one
(2) Select different pruning ratios on each block, and find out their influence on the performance of the model.
### Benefit: 
We can use a more efficient pruning method on the transformer.

## Project milestones and their completion status
Nov 24, 2024: Finish learning the code for training and inference of GPT2, and pruning.
Dec 5, 2024: Finish the fine-tuning of our base dataset.
Dec 7, 2024: Finish the parameter sweeping, and gain the importance of different parts.
Dec 8, 2024: Finish the testing of different kinds of addition.

## A description of the repository and code structure
In this repository, we have all the code required in the ipynb file. You can check the code and our running result from it.

## Example commands to execute the code
To run the experiments, you can simply upload the ipynb file to your google colab, and then run the code blocks one by one.
You may need to modify the datapath for model and dataset storage so the generated training dataset and fine-tuned model can be successfully stored.

## Results (including charts/tables) and observations:
![image](https://github.com/user-attachments/assets/222b924e-b0e6-4486-8a70-85f107bb5e48)
![image](https://github.com/user-attachments/assets/e3cc546b-495c-41f0-a93b-1d4c624d8c73)
![image](https://github.com/user-attachments/assets/9f812795-b16b-4d97-8e9e-80650b9b4442)
When pruning the MLP layers of GPT2, if the model size is restricted, we may prune more in the back layers, which may lead the model to have a better performance.
For the 3 parts, a linear addition from the front layers to the back layers is better than an exponential one.
As the model and the dataset are both widely used in experiments, we believe that our conclusion is reliable and should be able to guide the pruning to different Transformer models trained by different data sets.

