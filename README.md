# Custom Byte Pair Encoding (BPE) Tokenizer from Scratch

## 📌 Project Overview

This project implements the **Byte Pair Encoding (BPE)** algorithm from scratch using **Python** and **NumPy**. BPE is a subword tokenization algorithm widely used in Natural Language Processing (NLP) models such as GPT, BERT, and other transformer-based architectures.

The tokenizer learns subword vocabulary by repeatedly merging the most frequent adjacent symbol pairs in a text corpus.

---

## 🎯 Objective

- Implement the Byte Pair Encoding (BPE) algorithm from scratch.
- Learn subword vocabulary from a given corpus.
- Store merge rules for future encoding.
- Encode unseen words into subword tokens.
- Decode tokens back into the original words.
- Demonstrate the complete BPE workflow using Python.

---

## 🚀 Features

- Read text corpus from a file
- Text preprocessing
- Character-level tokenization
- End-of-word (`</w>`) symbol handling
- Word frequency calculation
- Adjacent pair frequency counting
- Most frequent pair merging
- Vocabulary update after every merge
- Merge rule storage
- Final vocabulary generation
- Encode function
- Decode function
- Sample testing with unseen words

---

## 📂 Project Structure

```
BPE_Tokenizer/
│
├── corpus.txt
├── BPE_Tokenizer.ipynb
├── README.md
```

---

## 📖 Algorithm Workflow

```
Read Text Corpus
        │
        ▼
Preprocess Text
        │
        ▼
Split Words into Characters
        │
        ▼
Add </w> Symbol
        │
        ▼
Count Word Frequencies
        │
        ▼
Find Adjacent Symbol Pairs
        │
        ▼
Count Pair Frequencies
        │
        ▼
Select Most Frequent Pair
        │
        ▼
Merge Pair
        │
        ▼
Update Vocabulary
        │
        ▼
Repeat Until Desired Merges
        │
        ▼
Store Merge Rules
        │
        ▼
Build Final Vocabulary
        │
        ▼
Encode New Words
        │
        ▼
Decode Tokens
```

---

## 🛠️ Technologies Used

- Python 3
- NumPy
- Jupyter Notebook

---

## 📚 Implementation Steps

1. Read the text corpus.
2. Preprocess the input text.
3. Split words into characters.
4. Append the `</w>` end-of-word symbol.
5. Count word frequencies.
6. Find adjacent symbol pairs.
7. Count pair frequencies.
8. Select the most frequent pair.
9. Merge the selected pair.
10. Update the vocabulary.
11. Repeat the merge process.
12. Store merge rules.
13. Build the final vocabulary.
14. Implement the encoder.
15. Implement the decoder.
16. Test the tokenizer.
17. Display the final results.

---

## 📄 Sample Corpus

```
low
lower
lowest
new
newer
widest
```

---

## 📊 Sample Output

### Initial Vocabulary

```
l o w </w>
l o w e r </w>
l o w e s t </w>
n e w </w>
n e w e r </w>
w i d e s t </w>
```

### Example Merge Rules

```
('l','o')
('lo','w')
('low','e')
('r','</w>')
('s','t')
```

### Encoding Example

Input

```
newest
```

Encoded Output

```
['new', 'e', 'st</w>']
```

Decoded Output

```
newest
```

---

## 📈 Results

- Successfully learned subword vocabulary.
- Generated merge rules based on pair frequencies.
- Encoded unseen words into subword tokens.
- Decoded tokens back into the original word.
- Demonstrated the complete Byte Pair Encoding algorithm from scratch.

---

## 💡 Applications

- Natural Language Processing (NLP)
- Transformer Models
- GPT Tokenization
- Machine Translation
- Text Compression
- Language Modeling
- Speech Processing

---

## 🔮 Future Improvements

- Interactive user input for encoding and decoding
- Custom corpus support
- Configurable vocabulary size
- Token ID generation
- Save and load trained vocabularies
- GUI-based tokenizer visualization
