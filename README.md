## Program

**`align`**  
  Performs automatic word alignment between English and French using the probabilistic models IBM Model 1 and Model 2. Aligns words in parallel sentences that support multiple iterations of Expectation Maximization to improve the accuracy of word alignments. The customized command-line options we have include:

  - `-d, --data` : Data file prefix (default: `data/hansards`)
  - `-e, --english` : Suffix of the English file (default: `e`)
  - `-f, --french` : Suffix of the French file (default: `f`)
  - `-n, --num_sentences` : Number of sentences to use for training (default: 1000)
  - `-i, --iterations` : Number of EM iterations (default: 5)

  For example: python align -n 1000 -i 10 > alignment.a to run the alignment model on 1000 sentence pairs and perform 10 iterations of EM, and store the output in alignment.a

  Run python score-alignments < alignment.a to compute accuracy.
