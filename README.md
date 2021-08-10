# tesseractTrainingSurveyPlans


The files listed are models that will help tesseract ocr detect bearing and distances found on modern survey plans.

They were trainined using QLD survey plans using tesseract's tesstrain files.
https://github.com/tesseract-ocr/tesstrain

The files were validated against some plans and the percent coincidence indicates how close the predicted text was to the ground truth text.

| Model                   | Border settings | Percent Coincidence |   |   |
|-------------------------|-----------------|---------------------|---|---|
| jess2                   | 0               | 88.4158427          |   |   |
| jess2                   | 0               | 97.09078652         |   |   |
| jess_border2            | 0               | 76.32561798         |   |   |
| jess_border2            | 0               | 93.90359551         |   |   |
| jess_whiteborder2       | 0               | 81.74561798         |   |   |
| jess_whiteborder2       | 0               | 96.89966292         |   |   |
| jess2                   | 0               | 86.86914286         |   |   |
| jess2                   | 0               | 94.42647619         |   |   |
| jess_border2            | 0               | 76.79047619         |   |   |
| jess_border2            | 0               | 92.54285714         |   |   |
| jess_whiteborder2       | 0               | 81.44295238         |   |   |
| jess_whiteborder2       | 0               | 95.1852381          |   |   |
| jess_whiteborder3       | 0               | 83.06019048         |   |   |
| jess_whiteborder3       | 0               | 96.66942857         |   |   |
| jess_whiteborder3-1     | 0               | 84.79980952         |   |   |
| jess_whiteborder3-1     | 0               | 96.68285714         |   |   |
| jess_whiteborder3-2     | 0               | 82.168              |   |   |
| jess_whiteborder3-2     | 0               | 96.76838095         |   |   |
| eng+jess_whiteborder3-2 | 0               | 80.33066667         |   |   |
| eng+jess_whiteborder3-2 | 0               | 93.72619048         |   |   |
|                         |                 |                     |   |   |
