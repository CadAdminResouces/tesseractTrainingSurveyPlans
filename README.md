# tesseractTrainingSurveyPlans


The files listed are models that will help tesseract ocr detect bearing and distances found on modern survey plans.

They were trained using QLD survey plans using tesseract's tesstrain files.
https://github.com/tesseract-ocr/tesstrain

The files were validated against two different validation sets as shown in the validation type column; one with borders and one without borders to generate a percent coincidence. The percent coincidence indicates how close the predicted text was to the ground truth text.


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

As suggested by tesseract. Additionally, we found that after cropping out the text from the image, adding a small border around the text improved tesseract's performance. The below table describes the border settings we used to crop these images out. Border refers to how much additional pixels of the image we cropped, and white border refers to the number of pixels of whitespace we added around the images.

| Models	|	Borders used in training	|
|-------------------------|---------------------|
| QLD_B_D, QLD_B_D2	|	No borders	|
| QLD_B_D_border, QLD_B_D_border 2	|	Images have a border of 3 and an additional white_border of 10	|
| QLD_B_D_whiteborder, QLD_B_D_whiteborder2, QLD_B_D_whiteborder3	|	Images have a border of 0 and a white_border of 10	|

The validation sets we created are listed below:
| Validation Set	|	Borders used in validation set	|
|-------------------------|---------------------|
| ValidationSet	|	No borders	|
| ValidationSetWithBorders	|	Images have a border of 3 and an additional white_border of 10	|


In summary, if you are going to give tesseract a raw bearing and distance image, use: QLD_B_D2, but if you add a border around the image before you do use: QLD_B_D_whiteborder3-2 

