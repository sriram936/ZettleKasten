NLP uses
1) Translation be diff lang
2) Free text qus ans (find, read doc and ans)
3) In 2018, pprocessing the info from pre existed docs and synthesizing
4) In 2019, llms, GPT 2
5) Now, GPT 4, ask qus n command n it will do, same tech multi modes like image, video, text, audio,,, Generating images based on text


Meaning of meaning

(symbol) => (idea)
![](/ZettleKasten/Unsorted/Attachment/Pasted_image_20250621010259.png)

WordNet is created in computers, pairing words with meaning,, but even though words are similarr some dont fit in sense of sentence

And it took human labour to update, less accuracy


Traditional NLP
Idea of converting wordss into one hot vectors
![](/ZettleKasten/Unsorted/Attachment/Pasted_image_20250621010943.png)

![](/ZettleKasten/Unsorted/Attachment/Pasted_image_20250621010905.png)
This too is troublesome, no relation or similarity between words even though its in form of one hot vectors

Next idea, words meaning comes from words around them(context) rather than individual word itself

![](/ZettleKasten/Unsorted/Attachment/Pasted_image_20250621011551.png)

Dot product bw dense word vectors (f each word) give the similarity bw 2 words

Step1) learn word vectors, representing in high dimensional space

Many ways to make word vector, now working with word2vec (mikolov google 2018)

(Now ppl working with 1000,2000dim vectors)