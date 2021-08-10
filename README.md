# tesseractTrainingSurveyPlans


The files listed are models that will help tesseract ocr detect bearing and distances found on modern survey plans.

They were trained using QLD survey plans using tesseract's tesstrain files.
https://github.com/tesseract-ocr/tesstrain

The files were validated against some plans and the percent coincidence indicates how close the predicted text was to the ground truth text.


| Model                   | Percent Coincidence |Validation Type |
|-------------------------|---------------------|---------------------|
| QLD_B_D2                   | 88.4158427          |ValidationSet |
| QLD_B_D2                   | 97.09078652         |ValidationSetWithBorders |
| QLD_B_D_border2            | 76.32561798         |ValidationSet |
| QLD_B_D_border2            | 93.90359551         |ValidationSetWithBorders |
| QLD_B_D_whiteborder2       | 81.74561798         |ValidationSet |
| QLD_B_D_whiteborder2       | 96.89966292         |ValidationSetWithBorders |
| QLD_B_D2                   | 86.86914286         |ValidationSet |
| QLD_B_D2                   | 94.42647619         |ValidationSetWithBorders |
| QLD_B_D_border2            | 76.79047619         |ValidationSet |
| QLD_B_D_border2            | 92.54285714         |ValidationSetWithBorders |
| QLD_B_D_whiteborder2       | 81.44295238         |ValidationSet |
| QLD_B_D_whiteborder2       | 95.1852381          |ValidationSetWithBorders |
| QLD_B_D_whiteborder3       | 83.06019048         |ValidationSet |
| QLD_B_D_whiteborder3       | 96.66942857         |ValidationSetWithBorders |
| QLD_B_D_whiteborder3-1     | 84.79980952         |ValidationSet |
| QLD_B_D_whiteborder3-1     | 96.68285714         |ValidationSetWithBorders |
| QLD_B_D_whiteborder3-2     | 82.168              |ValidationSet |
| QLD_B_D_whiteborder3-2     | 96.76838095         |ValidationSetWithBorders |
| eng+QLD_B_D_whiteborder3-2 | 80.33066667         |ValidationSet |
| eng+QLD_B_D_whiteborder3-2 | 93.72619048         |ValidationSetWithBorders |
|                         |                     | |

As suggested by tesseract. Additionaly we found that after getting cropping out the text from the image adding a small border around the text improves tesserect's performance.

| Models	|	Borders Used in training	|
|-------------------------|---------------------|
| jess, jess2	|	No borders	|
| jess_border, jess_border 2	|	Images have a border of 3 and an additional white_border of 10	|
| jess_whiteborder, jess_whiteborder2, jess_whiteborder3	|	Images have a border of 0 and a white_border of 10	|

#The Validation Sets I created are listed below:
| Validation Set	|	Borders used in validation set	|
|-------------------------|---------------------|
| ValidationSet	|	No borders	|
| ValidationSetWithBorders	|	Images have a border of 3 and an additional white_border of 10	|


In summary, if you are going to give tesseract a raw bearing and distance image, use: QLD_B_D2, but if you add a border around the image before you do use: QLD_B_D_whiteborder3-2 

