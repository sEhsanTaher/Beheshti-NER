# Beheshti-NER
## Beheshti-NER: Persian named entity recognition Using BERT
paper: [ACL web link](https://www.aclweb.org/anthology/2019.nsurl-1.6)

Named entity recognition is a natural language processing task to recognize and extract spans of text associated with named entities and classify them in semantic Categories. 

Google BERT is a deep bidirectional language model, pretrained on large corpora that can be fine-tuned to solve many NLP tasks such as question answering, named entity recognition, part of speech tagging and etc. 

In this paper, we use the pretrained deep bidirectional network, BERT, to make a model for named entity recognition in Persian. We also compare the results of our model with the previous state of the art results achieved on Persian NER. Our evaluation metric is CONLL 2003 score in two levels of word and phrase. This model achieved second place in NSURL-2019 task 7 competition which associated with NER for the Persian language. our results in this competition are 83.5 and 88.4 f1 CONLL score respectively in phrase and word level evaluation.

# Citation
  you can cite to this work with this:
```
@inproceedings{taher-etal-2019-beheshti,
    title = "Beheshti-{NER}: {P}ersian named entity recognition Using {BERT}",
    author = "Taher, Ehsan  and
      Hoseini, Seyed Abbas  and
      Shamsfard, Mehrnoush",
    booktitle = "Proceedings of The First International Workshop on NLP Solutions for Under Resourced Languages (NSURL 2019) co-located with ICNLSP 2019 - Short Papers",
    month = "11--12 " # sep,
    year = "2019",
    address = "Trento, Italy",
    publisher = "Association for Computational Linguistics",
    url = "https://www.aclweb.org/anthology/2019.nsurl-1.6",
    pages = "37--42",
}
```
# Usage
## STEPs before use:
0. Download this zip file (contains source code and model):
[Beheshti_NER_final.zip](https://www.dropbox.com/s/3ytftpz3l8ucy1u/Beheshti_NER_final.zip?dl=0)

1. Create a new python3 virtual environment with run this command(replace the venv path before run!): 
```SHELL
python3 -m venv /path/to/new/virtual/environment
```
2. Activate virtual environment with run this command(replace <venv> with venv path that created in step 1): 
```shell
  source <venv>/bin/activate
```
3. Install requirements.txt (in BERT-NER directory) with 
  ```shell
  pip install -r requirements.txt
  ```
4. Create a folder in BERT-NER directory for input documents (for example input_folder)
5. Copy your documents into folder created at step 4 in this format:
  + All files MUST be in CONLL format.(example in end of this file!)
  + The filenames don't matter BUT SHOULD end with ".txt"
6. create a folder in BERT-NER directory for NER outputs (for example output_folder)
  + NER results will be placed here after running Step 7! The filenames will not be changed BUT file formats will be changing from ".txt" to ".predict". 
7. Run this command for start NER tagging (please replace folder names input_folder & output_folder according to steps 4&6):   
  ```shell
python3 main.py input_folder output_folder
  ```



## CONLL format : 
* Tokens are separated by a new line(\n) 
* There is a empty line between sentences
* EXAMPLE:
```
این
یک
تست
است
.

سلام
ایران
!

من
به
بانک
ملی
رفتم
و
وزیر
نفت
را
دیدم
.

با
دیدن
دکتر
علوی
در
روز
چهارشنبه
هفتم
خرداد
بسیار
خوشحال
گشتم
!
```
