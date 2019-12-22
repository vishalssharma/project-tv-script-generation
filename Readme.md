# Generating_TV_Scripts

This project was developed as a part of Udacity's Deep Learning Nanodegree. In this project, i have created a Recurrent neural network from scratch using pytorch. In this project, i generated my own Seinfeld TV scripts using RNNs. I used a Seinfeld dataset of scripts from 9 seasons. The Neural Network i built will generate a new, "fake" TV script.

## Getting Started

Just run the ipynb notebook. Tune the hyper parameters for better accuracy.
<img src='/seinfeld.jpg' width=500 px>

### Prerequisites

* Python 3
* Numpy
* MatPlotLib
* Pytorch 
## Dependencies

### Configure and Manage Your Environment with Anaconda

Per the Anaconda [docs](http://conda.pydata.org/docs):

> Conda is an open source package management system and environment management system 
for installing multiple versions of software packages and their dependencies and 
switching easily between them. It works on Linux, OS X and Windows, and was created 
for Python programs but can package and distribute any software.

## Overview
Using Anaconda consists of the following:

1. Install [`miniconda`](http://conda.pydata.org/miniconda.html) on your computer, by selecting the latest Python version for your operating system. If you already have `conda` or `miniconda` installed, you should be able to skip this step and move on to step 2.
2. Create and activate * a new `conda` [environment](http://conda.pydata.org/docs/using/envs.html).

\* Each time you wish to work on any exercises, activate your `conda` environment!

---

### 1. Installation

**Download** the latest version of `miniconda` that matches your system.

|        | Linux | Mac | Windows | 
|--------|-------|-----|---------|
| 64-bit | [64-bit (bash installer)][lin64] | [64-bit (bash installer)][mac64] | [64-bit (exe installer)][win64]
| 32-bit | [32-bit (bash installer)][lin32] |  | [32-bit (exe installer)][win32]

[win64]: https://repo.continuum.io/miniconda/Miniconda3-latest-Windows-x86_64.exe
[win32]: https://repo.continuum.io/miniconda/Miniconda3-latest-Windows-x86.exe
[mac64]: https://repo.continuum.io/miniconda/Miniconda3-latest-MacOSX-x86_64.sh
[lin64]: https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh
[lin32]: https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86.sh

**Install** [miniconda](http://conda.pydata.org/miniconda.html) on your machine. Detailed instructions:

- **Linux:** http://conda.pydata.org/docs/install/quick.html#linux-miniconda-install
- **Mac:** http://conda.pydata.org/docs/install/quick.html#os-x-miniconda-install
- **Windows:** http://conda.pydata.org/docs/install/quick.html#windows-miniconda-install

### 2. Create and Activate the Environment

For Windows users, these following commands need to be executed from the **Anaconda prompt** as opposed to a Windows terminal window. For Mac, a normal terminal window will work. 

#### Git and version control
These instructions also assume you have `git` installed for working with Github from a terminal window, but if you do not, you can download that first with the command:
```
conda install git
```

If you'd like to learn more about version control and using `git` from the command line, take a look at our [free course: Version Control with Git](https://www.udacity.com/course/version-control-with-git--ud123).

**Now, we're ready to create our local environment!**

1. Clone the repository, and navigate to the downloaded folder. This may take a minute or two to clone due to the included image data.
```
git clone https://github.com/vishalssharma/project-tv-script-generation.git
```

2. Create (and activate) a new environment, named `deep-learning` with Python 3.6. If prompted to proceed with the install `(Proceed [y]/n)` type y.

	- __Linux__ or __Mac__: 
	```
	conda create -n deep-learning python=3.6
	source activate deep-learning
	```
	- __Windows__: 
	```
	conda create --name deep-learning python=3.6
	activate deep-learning
	```
	
	At this point your command line should look something like: `(deep-learning) <User>:deep-learning-v2-pytorch <user>$`. The `(deep-learning)` indicates that your environment has been activated, and you can proceed with further package installations.

3. Install PyTorch and torchvision; this should install the latest version of PyTorch.
	
	- __Linux__ or __Mac__: 
	```
	conda install pytorch torchvision -c pytorch 
	```
	- __Windows__: 
	```
	conda install pytorch -c pytorch
	pip install torchvision
	```

6. Install a few required pip packages, which are specified in the requirements text file (including OpenCV).
```
pip install -r requirements.txt
```


To exit the environment when you have completed your work session, simply close the terminal window.


### Architecture

* Tried both GRU and LSTM. LSTM performed better than GRU.

### Project results

This project has met the following specifications:
* The submission includes all required, complete notebook files.
* All the unit tests in project have passed.
* The function create_lookup_tables creates two dictionaries:
   - Dictionary to go from the words to an id, we'll call vocab_to_int
   - Dictionary to go from the id to word, we'll call int_to_vocab
   - The function create_lookup_tables return these dictionaries as a tuple (vocab_to_int, int_to_vocab).
* The function token_lookup returns a dict that can correctly tokenizes the provided symbols.
* The function batch_data breaks up word id's into the appropriate sequence lengths, such that only complete sequence lengths are constructed.
* In the function batch_data, data is converted into Tensors and formatted with TensorDataset.
* Finally, batch_data returns a DataLoader for the batched training data.
* The RNN class has complete __init__, forward , and init_hidden functions.
* The RNN must include an LSTM or GRU and at least one fully-connected layer. The LSTM/GRU should be correctly initialized, where         relevant.
* Enough epochs to get near a minimum in the training loss, no real upper limit on this. Just need to make sure the training loss is low   and not improving much with more training.
* Batch size is large enough to train efficiently, but small enough to fit the data in memory. No hard and fast rule here, depends on GPU   memory usually.
* Embedding dimension, significantly smaller than the size of the vocabulary, if you choose to use word embeddings
* Hidden dimension (number of units in the hidden layers of the RNN) is large enough to fit the data well. Again, no hard and fast rule here.
* n_layers (number of layers in a GRU/LSTM) is between 1-3.
* The sequence length (seq_length) here should be about the size of the length of sentences you want to look at before you generate the   next word.
* The learning rate shouldn't be too large because the training algorithm won't converge. But needs to be large enough that training       doesn't take forever.
* The printed loss should decrease during training. The loss should reach a value lower than 3.5.
* There is a provided answer that justifies choices about model size, sequence length, and other parameters.
* The generator code generates a complete script.

## Losses

### Model :
Training loss: 3.28

## Generated Script

jerry: geraldo.

[new witness: talker:, wet, the district court, the heat. i am not gonna be a bright party for the lipo. it's a good time.

jerry: i was a little girl.

george: well, i think i would get out of here.

jerry: you know, i was thinking i could go in a prostitute, and he challenged the defective wheelchair.

george: yes, yes, yes, yes. it's the same one. i mean, i have to be a little more. i think that would work!

captain: i think it's something.

george: you think she would be?

jerry: no, no, it's not.

jerry: i don't even feel like that.

hoyt: i don't know if you could get a lot of prostitutes.

george: i don't know what it happened.

jerry: you know what this is? you were just reeling it up.

chiles: so, what did you say?

george: i think that's not bad, but it's not the puffy- talker, and i have the best to see you.

jerry: so?

jerry: no, no, no, i didn't.

elaine: oh, yeah.

jerry: yeah, well, i think i could be ready.

[new witness: the defendants, and the judge, and inconsequential.

hoyt: i know.

jerry: i think i was the one i was in snitzer's.

george: so you don't want any of you?

george: what do you think about the maid?

elaine: what happened?

george: you know, this is jerry costanza.

george: what do you mean if you could be a virgin, and then you know, i am going to see the puffy shirt in the building. it's a wheelchair!

elaine: what about the library?

george: you know who this is?

jerry: no, but i was just a

## Built With

* Python 3

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details

## Acknowledgments

* The data comes from Udacity.
