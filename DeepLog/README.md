## DeepLog for anomaly detection
 This folder contains our implementation of DeepLog for anomaly detection as one of our baselines.
 
## running instructions
1. install the requirement.txt of the repository
```
$ pip install -r requirements.txt
```
2. download and unzip the data set files introduced in the main readme file
3. Inside the folder containing the data sets, move data_set_processing.py file there and run it:
```
$ python data_set_processing.py
```
4. move the precessed data sets, small version of them, inside the small_code folder. 
5. convert the data set file to csv file by the following command
```
$ python data_text_to_csv.py
```
run the above command three times, each time targetfile variable inside the file is the name of one of the three datasets. 

6. run the main file
``` shell script
$ python main.py
```

inside the main file you can set the target file to be either bgl, thunderbird, or spirit.

Deeplog will be run for all the different traina and test set split and results will be saved in a folder called "results"
