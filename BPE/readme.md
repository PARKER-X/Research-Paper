#Demo
from collections import Counter, defaultdict

# Corpus as a list of words
corpus = ["low", "lower", "newest", "widest"]

# Split into characters and add end-of-word marker
tokens = [" ".join(list(word)) + " </w>" for word in corpus]

# Count word frequencies
vocab = Counter(tokens)

def get_stats(vocab):
    pairs = defaultdict(int)
    for word, freq in vocab.items():
        symbols = word.split()
        for i in range(len(symbols)-1):
            pair = (symbols[i], symbols[i+1])
            pairs[pair] += freq
    return pairs

def merge_vocab(pair, vocab):
    new_vocab = {}
    bigram = " ".join(pair)
    replacement = "".join(pair)
    for word in vocab:
        new_word = word.replace(bigram, replacement)
        new_vocab[new_word] = vocab[word]
    return new_vocab

# Perform BPE merges
num_merges = 10
for i in range(num_merges):
    pairs = get_stats(vocab)
    if not pairs:
        break
    best = max(pairs, key=pairs.get)
    vocab = merge_vocab(best, vocab)
    print(f"Step {i+1}: Merged {best} -> {''.join(best)}")

# Print final vocabulary
print("\nFinal vocabulary tokens:")
for word in vocab:
    print(word)
