# AutoCorrect Module

This Python module provides a simple autocorrect feature that suggests the most similar word from a predefined database of words, based on bigram similarity.

## Functions

### create_bigram(word)
Creates bigrams from a given word.

**Parameters:**
- `word` (str): The word to create bigrams from.

**Returns:**
- `list`: A list of bigrams.

### get_similarity_ratio(word1, word2)
Calculates the similarity ratio between two words based on their bigrams.

**Parameters:**
- `word1` (str): The first word.
- `word2` (str): The second word.

**Returns:**
- `float`: The similarity ratio between the two words.

### AutoCorrect(word, database, sim_threshold)
Suggests the most similar word from the database based on the bigram similarity ratio.

**Parameters:**
- `word` (str): The word to be autocorrected.
- `database` (set): A set of words to compare against. Default is a predefined set of common English words.
- `sim_threshold` (float): The similarity threshold to consider a word as a suitable suggestion. Default is 0.5.

**Returns:**
- `str`: The most similar word from the database if the similarity ratio exceeds the threshold, otherwise returns the original word.

## Usage

To use this module, simply run the script and input a word when prompted:

```python
if __name__ == "__main__":
    print("Input your word: ")
    print(AutoCorrect(input()))
