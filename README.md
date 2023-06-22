# HLT-project

## General

Recently, the diffusion of online conspiracy theories has been associated with episodes of brutal offline violence like the attack at Capitol Hill in Washington, anti-vax protests, and the attack on the CGIL in Rome.
Given the societal harm that the diffusion of such theories can cause, we propose the Automatic Conspiracy Theory Identification task (ACTI).
The goal of this task is to develop models that can automatically identify conspiratorial content, conspiracy categories, and the type of arguments used to support, and therefore diffuse, conspiratorial claims.

Specifically, the ACTI task proposes the automatic identification of conspiracy content in the Italian language in Telegram. This task is organized according to two main subtasks

[**Subtask A: Conspiratorial Content Classification:**](https://www.kaggle.com/competitions/acti-subtask-a/data?select=subtaskA_test.csv) A system must recognize if a telegram
post is conspiratorial or not.

* A sentence is _Conspiratorial_ if either (i) expresses the belief that major events(e.g., covid) are manipulation created by powerful people to protect their interests or (ii) an interpretation of events meant to contribute to strengthening the underlying narrative of the conspiracy theory.
*  A sentence is _Not Conspiratorial_ if it does not diffuse any kind of beliefs linked to the conspiracy theory.

## Dataset Description
### What Should I expect the data format to be?
The primary data for the competition is, in each provided file, the `comment_text` column. This contains the text of a comment which has been labeled as Conspiratorial (1) or non-conspiratorial (0).
The train set’s comments are entirely in Italian with sporadic citation of external resources in English and come exclusively from Telegram Channels.

The `subtaskA_train.csv` contains a `conspiratorial` column that it is the target to be trained on.
The values of such column are either `1` indicating that the corresponding comment in `comment_text` column is Conspiratorial. Otherwise it is `0`.
### What am I predicting?
You are predicting if a comment is Conspiratorial (1) or not (0).
In the test set all comments are classified as either 1 or 0.
#### Files
* **subtaskA_train.csv** - the **training** set for **Subtask A**: Conspiratorial Content Classification. It contains the column `Id`, `comment_text` and `conspiratorial`.
* **subtaskA_test.csv** - the **test** set for **Subtask A**: Conspiratorial Content Classification. It contains only the `Id` and `comment_text` columns 
* **sample_submission.csv** - a sample submission file in the correct format

#### Columns
* `Id` - the id associated with a comment 
* `comment_text` - the text of a comment 
* `conspiratorial` - (only subtaskA_train.csv) the label indicating if a comment is conspiratorial (1) or not(0)
