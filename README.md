# UTTER WP2 - MS9 - Meeting Data - June-Dec 2023

# Context

- We developed a meeting assistant prototype: MrMeeting (answers to questions related to a meeting; meeting transcripts are put in the LLM prompt)
- Video can be watched [here](https://tinyurl.com/UTTER-Meeting-Assistant)
- Prototype was evaluated using UTTER (internal) meeting data and using [ELITR] (https://lindat.mff.cuni.cz/repository/xmlui/handle/11234/1-4692) (public) meeting data
- This page gathers the collection of annotated Q&A after interaction with MrMeeting
    - **ELITR English dev set (done)**
    - ELITR English test set (todo)
    - UTTER English dataset (done, but needs anonymization)
- Question are of 4 types: (1) **What/Why** (2) **Who** (3) **When** (4) **How many**
- We also annotate if answer to question is in the **B**eginning (1st 1/3d), **M**iddle (2d 1/3d) or **E**nd (3d 1/3d) or on **S**everal blocks - of the meeting transcript in order to see if we can confirm results of [this paper ('lost in the middle')] (https://cs.stanford.edu/~nfliu/papers/lost-in-the-middle.arxiv2023.pdf)

# Structure

**ELITR English dev set**

[dev001](ELITR-English-dev/meeting_en_dev_001.md)

[dev002](ELITR-English-dev/meeting_en_dev_002.md)

[dev003](ELITR-English-dev/meeting_en_dev_003.md)

[dev004](ELITR-English-dev/meeting_en_dev_004.md)

[dev005](ELITR-English-dev/meeting_en_dev_005.md)

[dev006](ELITR-English-dev/meeting_en_dev_006.md)

[dev007](ELITR-English-dev/meeting_en_dev_007.md)

[dev008](ELITR-English-dev/meeting_en_dev_008.md)

[dev009](ELITR-English-dev/meeting_en_dev_009.md)

[dev010](ELITR-English-dev/meeting_en_dev_010.md)

**ELITR English test set**

**UTTER English data set**


# Evaluation Results

**ELITR English dev set**

Correct responses depending on the type of question (What, Who, When, How-Many) - Overall the LLM (gpt3.5-16k) answered correctly to 63,12% of questions on ELITR dev set


|        | WHAT(correct) | WHAT(all) | WHO(correct) | WHO(all) | WHEN(correct) | WHEN(all) | HOW MANY(correct) | HOW MANY (all) | ALL (correct) |
|--------|---------------|-----------|--------------|----------|---------------|-----------|-------------------|----------------|---------------|
| dev001 | 6             | 8         | 3            | 6        | 0             | 1         | 1                 | 1              |               |
| dev002 | 4             | 5         | 5            | 7        | 1             | 1         | 1                 | 1              |               |
| dev003 | 1             | 6         | 3            | 5        | 1             | 2         | 1                 | 1              |               |
| dev004 | 3             | 4         | 3            | 6        | 1             | 1         | 1                 | 2              |               |
| dev005 | 6             | 8         | 3            | 5        | 2             | 2         | 1                 | 1              |               |
| dev006 | 2             | 4         | 5            | 5        | 3             | 4         | 0                 | 0              |               |
| dev007 | 6             | 8         | 2            | 4        | 2             | 2         | 1                 | 1              |               |
| dev008 | 3             | 5         | 3            | 5        | 1             | 2         | 1                 | 1              |               |
| dev009 | 4             | 7         | 1            | 2        | 0             | 1         | 1                 | 1              |               |
| dev010 | 3             | 4         | 2            | 6        | 2             | 5         | 0                 | 1              |               |
| total  | 38            | 59        | 30           | 51       | 13            | 21        | 8                 | 10             |               |
| stats  | 64,41 %     |           | 58,82 %    |          | 61,90 %     |           | 80,00 %         |                | 63,12 %     |



Correct responses depending on the position of the answer in the meeting transcript (**B**egin, **M**iddle, **E**nd, **S**everal)

|        |            |        |            |        |            |        |            |        |
|--------|------------|--------|------------|--------|------------|--------|------------|--------|
|        | B(correct) | B(all) | M(correct) | M(all) | E(correct) | E(all) | S(correct) | S(all) |
| dev001 | 2          | 3      | 3          | 5      | 2          | 3      | 3          | 5      |
| dev002 | 2          | 2      | 3          | 5      | 2          | 2      | 4          | 5      |
| dev003 | 2          | 6      | 0          | 2      | 2          | 2      | 2          | 4      |
| dev004 | 2          | 3      | 1          | 3      | 2          | 3      | 3          | 4      |
| dev005 | 6          | 7      | 0          | 1      | 6          | 6      | 0          | 2      |
| dev006 | 5          | 5      | 3          | 3      | 1          | 3      | 1          | 2      |
| dev007 | 3          | 4      | 2          | 3      | 4          | 4      | 2          | 4      |
| dev008 | 3          | 3      | 2          | 3      | 0          | 2      | 3          | 5      |
| dev009 | 2          | 4      | 1          | 1      | 2          | 3      | 1          | 3      |
| dev010 | 2          | 7      | 2          | 3      | 3          | 4      | 0          | 2      |
| total  | 29         | 44     | 17         | 29     | 24         | 32     | 19         | 36     |
| stats  | 65,91 %  |        | 58,62 %  |        | 75,00 %  |        | 52,78 %  |        |



**ELITR English test set**

**UTTER English data set**

Correct responses depending on the type of question (What, Who, When) - Overall the LLM (gpt3.5-16k) answered correctly to 60,98% of questions on UTTER meetings dataset

|       | WHAT(correct) | WHAT(all) | WHO(correct) | WHO(all) | WHEN(correct) | WHEN(all) | ALL (correct) |
|-------|---------------|-----------|--------------|----------|---------------|-----------|---------------|
| #1    | 4             | 6         | 3            | 6        | 1             | 3         |               |
| #2    | 9             | 9         | 3            | 3        | 3             | 3         |               |
| #3    | 3             | 5         | 1            | 5        | 4             | 5         |               |
| #4    | 4             | 7         | 3            | 4        | 2             | 4         |               |
| #5    | 6             | 7         | 2            | 4        | 1             | 4         |               |
| #6    | 7             | 8         | 4            | 5        | 1             | 2         |               |
| #7    | 3             | 8         | 3            | 4        | 1             | 3         |               |
| #8    | 6             | 7         | 0            | 4        | 1             | 3         |               |
| #9    | 3             | 6         | 5            | 5        | 3             | 4         |               |
| #10   | 3             | 5         | 4            | 6        | 0             | 4         |               |
| #11   | 3             | 6         | 1            | 4        | 3             | 5         |               |
| total | 51            | 74        | 29           | 50       | 20            | 40        |               |
| stats | 68,92 %     |           | 58,00 %    |          | 50,00 %     |           | 60,98 %     |




