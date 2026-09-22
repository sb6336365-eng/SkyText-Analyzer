# SkyText-Analyzer
print("Welcome to SkyText Analyzer!")

sentence = input("Enter a sentence: ")

words = sentence.split()

count = {}

for word in words:
    word = word.lower()

    if word in count:
        count[word] = count[word] + 1
    else:
        count[word] = 1

max_word = ""
max_count = 0

for word in count:
    if count[word] > max_count:
        max_count = count[word]
        max_word = word

print()
print("----- Analysis -----")
print("Number of words:", len(words))
print("Number of characters:", len(sentence))
print("Most frequent word:", max_word)
print("Frequency:", max_count)