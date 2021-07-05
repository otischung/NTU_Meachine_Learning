# NTU ML

Instructor: HUNG-YI LEE, Associate professor of EE and CSIE of NTU

Course URL: https://www.youtube.com/playlist?list=PLJV_el3uVTsMhtt7_Y6sgTHGHp1Vb2P2J

Out-Line and Code Submissions: https://speech.ee.ntu.edu.tw/~hylee/ml/2021-spring.html



## Syllabus

### HW1: Regression

We use SGD or Adam to find a function that predicts the third day of people infected by SARS-CoV-2

The training data is the past two days of report of 40 states in US.

Each 40 states is encoded in one-hot vector, with data including COVID-like illness, e.g. CLI (COVID-Like Illness), ILI (Influenza-Like Illness), behavior indicators, mental health indicators, and the tested positive cases of that day.

Since we only have one known data and a test data, we must splitting training data from our known data into training set and validation set (development set). We choose # of data which is not divisible by 5, that is , `i mod 5 != 0`, to be training set; and # of data which is divisible by 5 to be validation set.

We also try L1/L2 regularization to make lower loss.

#### Result

The validation loss is 0.8051 and the prediction loss is 0.95505 (using MSE, Mean Square Error), **we've passed the medium baseline** (1.36937). The strong baseline requires the prediction loss less than 0.89266

