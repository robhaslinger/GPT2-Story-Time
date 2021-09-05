# GPT-2 Story-Time: Fine-tuning language models on children's stories.

This repo contains a notebook with a simple example of fine-tuning a GPT-2 language model. Specifically,
fine-tuning on some old children's stories off of Project Gutenberg (because they are free). 

I did this back when I was first starting to learn about NLP and transformer models. I wanted 
to work through the process of fine-tuning a language model in detail, so I understood it. This is the
result. It's pretty simple. There's a notebook [GPT2_Fine_Tuning](notebooks/GPT2_Fine_Tuning.ipynb) which
you can use to tokenize text and fine-tune a model. Hopefully 
it's reasonably self-explanatory. There's some 
[utility code for tokenization](src/text_tokenization_utils.py) and also I included a small amount of 
[raw text data](textdata/) from Beatrix Potter, Brothers Grimm and Lewis Carrol.

I used a pre-trained model from the [Huggingface transformers](https://huggingface.co/transformers/) 
library, but tried to do as much 
of this in "raw" PyTorch as I could, just to go through the exercise. As I'm not a software engineer
by training, I sadly found the Huggingface
source code a bit hard to parse. It's an excellent, indeed amazing, library ... but it's rather large, 
and tracing back all the class inheritances through different files to understand what was going on was 
a bit rough for me.
In the end, I found [this blog post](https://towardsdatascience.com/film-script-generation-with-gpt-2-58601b00d371) 
very helpful to understand the general approach. Of course, I also did a lot of reading of the PyTorch docs.  

## Installation

Should be pretty straightforward. Make a virtual environment and pip install jupyter, numpy, torch and transformers.
Then clone the repo.  Go to the notebook [GPT2_Fine_Tuning](notebooks/GPT2_Fine_Tuning.ipynb) and run it. Note
that when you run the jupyter cells tokenizing the text, the text tokenization utilities will make some new subdirectories in [textdata/](textdata/) directory. These
won't be tracked by git unless you change the .gitignore file to comment out it ignoring .pkl files.

That's it. Hopefully this helps someone else get going with learning how to train transformer models in PyTorch. 
Feel free to reach out with questions, comments, and improvements.


