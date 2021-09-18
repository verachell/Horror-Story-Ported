# Horror-Story-Ported
My NaNoGenMo story from 2020 (originally in Ruby) ported to YeetWords

This is an example of a YeetWords program. My NaNoGenMo project from 2020 [Horror Story With Monster](https://github.com/verachell/Horror-Story-with-Monster-NaNoGenMo-2020) (written in Ruby) is ported here to YeetWords as a practical demonstration of the use of [YeetWords](https://github.com/verachell/YeetWords) to create a story. 

This repository may also be used as a demo to make sure you have YeetWords installed and running properly.

## Usage
You need Ruby installed on your machine to use this. 

1. Download this repository.  

2. In its working directory also download and include the file ```yeetwords.rb``` from the [YeetWords repository](https://github.com/verachell/YeetWords). 

3. Then on your command line, type ```ruby yeetwords.rb horror_ported.txt``` to run the program. It will output a Markdown file containing the story.

An example of output in Markdown format is included in this repository.

## Changes that were made in the port versus the original
Changes to word and sentence data from the original to the ported were minimized as much as possible, and are documented here:
### Changes to sentences
replaced CHARACTER in sentences with PERSON.NAME and HIMHER with PERSON.HIMHER  
replaced JOB with PERSON.JOB  
replaced FAVEVERB with PERSON.FAVEVERB  
removed exclamation marks and question marks from all dialogue (explanation below)

### Originally hard-coded word data variables in the original that were put into data files for this YeetWords port
This could equally well have been accomplished via an ASSIGNLIST command in YeetWords, but in either case, there was hard-coded data in the original that had to make its way into the port for these variables:

conj  
direction  
sense  
monsterallnames  
monstermove  
monsteradv  
monsterfeature  

### ASSIGNLIST commands in YeetWords to rename variable names that did not match their files names
In the original program, some variable names did not match file names, which would have posed a problem for YeetWords. Additionally, some of the original filenames contained special characters, making them incompatible with the YeetWords word substitution process. Instead of renaming the original files, to minimize changes to original word and sentence data, ASSIGNLIST commands were used in this port to rename variables to compatible allowable ones.

### Vocabulary that changes gradually over time in the original is changed in 3 sharp jumps in the YeetWords port
The original Horror Story With Monster featured certain parts of the vocabulary changing gradually over time (positive words -> neutral words -> negative words). YeetWords does not have a corresponding function or ability to achieve this. Therefore, the YeetWords port had 3 sections which started with positive words, then switched to neutral words, and then to negative words. 

### Composition of main/messages/dialogue in the YeetWords port is not quite as random as that of the original
This is because the original selected from a range of different sentences, and if one was a text message or dialog, it would format it accordingly on the spot. YeetWords by contrast needs to know ahead of time if the sentence is to be a text message or dialog in order to format it appropriately. The composition in YeetWords was set up to result in a similar amount of those types of sentences, but because of the need to select these separately, they occurred at slightly less random intervals. Using ranges of words and ranges of repeats in YeetWords helped overcome this to an extent, but not completely.

## The differences seen in original vs the ported for the end result of the story output
The main differences seen in the original versus the ported version were:

- Vocabulary that changed over time in the original was done in sudden jumps in the YeetWords port versus gradually over time in the original, and this was unavoidable because YeetWords has no function to allow gradually changing vocabulary over time.

- The main text of the YeetWords port was not quite as random as that of the original, but it is fairly close

- Dialog in the YeetWords port has no exclamation marks and question marks for reasons outline previously, so some of the dialog does not sound natural compared to the original. The missing exclamation marks and question marks was because these needed to be formatted differently. This could have been done if those types of dialog were placed in a separate list than the main dialog. However, this port had the overriding desire to minimize changes to the original data, and the original data did not distinguish between regular dialog and that which needed special punctuation.
