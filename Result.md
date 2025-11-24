# Resnet-50 model

<img width="532" height="340" alt="image" src="https://github.com/user-attachments/assets/8d2700f9-cc00-4261-8410-12bf0cbfc700" />

                               Graph accuracy plot 


<img width="522" height="340" alt="image" src="https://github.com/user-attachments/assets/4834e42e-e284-4e96-9a9f-43cace686deb" />


                               Graph loss plot



     Confusion matrix for validation process of the ResNet-50

| Class label          | Precision (%) | Recall (%) | F1-score (%) |
| -------------------- | ------------- | ---------- | ------------ |
| 1                    | 84            | 92         | 88           |
| 10                   | 88            | 69         | 77           |
| 11                   | 85            | 80         | 82           |
| 12                   | 72            | 77         | 75           |
| **Accuracy (%)**     | 82            | -          | -            |
| **Macro avg (%)**    | 82            | 80         | 80           |
| **Weighted avg (%)** | 82            | 82         | 82           |


# Xception model

<img width="544" height="348" alt="image" src="https://github.com/user-attachments/assets/21088168-da1e-4fd3-9074-fbdf0676924c" />


                               Graph accuracy plot 
<img width="547" height="356" alt="image" src="https://github.com/user-attachments/assets/94dce56a-091c-4019-a1a2-e04df65dccf9" />



                               Graph loss plot


     Confusion matrix for validation process of the Xception
| Class label          | Precision (%) | Recall (%) | F1-score (%) |
| -------------------- | ------------- | ---------- | ------------ |
| 1                    | 92            | 92         | 92           |
| 10                   | 81            | 93         | 86           |
| 11                   | 92            | 82         | 87           |
| 12                   | 81            | 77         | 79           |
| **Accuracy (%)**     | 87            | -          | -            |
| **Macro avg (%)**    | 86            | 86         | 86           |
| **Weighted avg (%)** | 87            | 87         | 87           |
                               
# Conclusion

| Model     | Accuracy | Evaluation                                                                                                              |
| --------- | -------- | ----------------------------------------------------------------------------------------------------------------------- |
| ResNet-50 | 82%      | • Slight overfit<br>• Lower accuracy compared to Xception<br>• Has lower values for precision, recall, and F1-score     |
| Xception  | 87%      | • Good fit model<br>• Highest accuracy compared to ResNet-50<br>• Has higher values for precision, recall, and F1-score |

