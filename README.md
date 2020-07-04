



[![Build Status](https://travis-ci.org/AbdullahTaher93/TFM.svg?branch=master)](https://travis-ci.org/AbdullahTaher93/TFM)

[![Language](https://img.shields.io/badge/laguage-java-green.svg)](https://www.java.com/)
# Cryptanalysis Ciphertext Based Genetic Algorithms

## ABSTRACT  
Cryptanalysis is breaking the ciphertext(codes) to find the
plaintext (original text) .There are many tools used in the cryptanalysis.Genetic algorithm(GA).Is an optimization search
tool to find the best solution.In this project ,Genetic algorithm(GA) used as a cryptanalysis tool to search the decryption key for obtaining the plaintext from the ciphertext.When the ciphertext generated by the transpositioncipher.

## Introduction
Cryptanalysis is the technique of deriving the original message from the cipher text without any prior knowledge of secret key or the erivation of key from the cipher text. A general technique for cryptanalysis, applied to all cryptographic algos is to try all the possible keys until the correct key is matched, it is known as exhaustive key search. 

A symmetric key cipher, especially a stream cipher is assumed secure, if the computational capability required for breaking the cipher by best-known attack is greater than or equal to exhaustive key search. 
Cryptanalysis is the science of making encrypted data unencrypted use convert cipher text to plaintext because cryptanalysis used to convert plaintext to cipher text and used cryptanalysis Return to plaintext or clear text or original text cryptanalysis is used to break codes by finding weaknesses. There are many techniques used in the cryptanalysis. This project used the genetics algorithm.

The genetic algorithm is a search algorithm based on the mechanics of natural selection and natural genetics The genetic algorithm belongs to the family of evolutionary algorithms, along with genetic programming, Evolution strategies and evolutionary programming. The set of operators usually consists of mutation, crossover and selection,

Cryptanalysis is the technique of extracting useful information about the key by observing the plaintext and cipher text using cryptanalysis   try to break the secrecy provided by the cipher. There is no fixed method for cryptanalysis and every cipher is a different challenge to the attacker and hence demands different insight to attack  In this chapter, explained the history of cryptanalysis, the technology of cryptanalysis, transposition cipher, and description genetics algorithm (GA).

## Cryptanalysis
Cryptanalysis are the basic techniques on block cipher and till today, many cryptanalytic attacks are developed based on these. The cryptanalysis return cipher text to clear text  (or original text) by different methods to find the decryption  key, in other words, cryptanalysis is a method to reveal the key by the Receiver to transform cipher text to plaintext (or original text)

![Cryptanalysis](https://github.com/AbdullahTaher93/TFM/blob/master/images/Cryptanalysis.png)

## Implementation

genetic algorithm (GA) can be used for  obtaining  the decryption key to break ciphertext and transfer ciphertext message to plaintext message (readable message). GA is a search tool to insure high probability of finding a solution by decreasing the amount of time in the key space searching. GA consists of many operations: Evaluation fitness, Selection, Crossover, and Mutation. In Figure below Flowchart of proposed method of cryptanalysis.

![Flowchart](https://github.com/AbdullahTaher93/TFM/blob/master/images/Flowchart.png)


### 1- Initialization (Population)
In initialization stage, generate a pool of random keys, when the length of the key is N digits  and the pool size is M keys. Also, The key condition is random and non-repetitive in each key. These keys are changeable  by the other stages of GA and the better one used in derivation the plaintext.

### 2- Transposition Cipher
The transposition cipher is rearranged (change position only) the characters in the message but not change the characters. Transposition cipher have a pool of keys and ciphertext  that rearranged the ciphertext  for M times depended on the pool of keys. The output of transposition cipher saved in array of M locations we can called it  "plaintext_array".

Example: Decipherment process by columner Transposition. Ciphertext: PORPRYCTAYGH, Key: 3 1 4 2,

![Transposition](https://github.com/AbdullahTaher93/TFM/blob/master/images/Transposition.png)

### 3- Evaluation Fitness 
Fitness is evaluated based on the biagrams (sequence of two letters) frequency in the decrypted cipher text and Trigrams (sequence of three letters) frequency in the decrypted cipher text. the tables below illustrated the most popular biagrams and Trigrams  in English language. Triagrams and diagrams   are   computationally expensive the fitness calculation.  Fitness function is as shown below equation:

     Fitness function= β. ∑| (K (bi, j) −D (bi, j))|+   γ. ∑| (K (ti, j) −D (ti, j))|

Where β and γ are a constant
* K represents Known English Language
* D represents Decrypted the message
* Bi represents the bigram (two letter sequence).
* Ti represents the triagram (three letter sequence).

![TiBi](https://github.com/AbdullahTaher93/TFM/blob/master/images/TIBI.png)


### 4- Selection operation
In this operation, selection (choosing) the best keys only. The best key which has the high value of fitness. In the proposed work select only M/2 keys which have the high fitness.  To perform the selection operation nedded a sorting function to sort pool of keys from high fitness to low fitness.


### 5- Crossover Operation
In this operation, after selecting the best M/2 keys by the selection operation, applying the crossover operation to obtain the remainder M/2 keys. In the crossover operation, each key performs a crossover to obtain a new key with the condition non-primitive keys. After the crossover operation, a new pool of keys obtaining, these are called "new population".

### 6- Mutation Operation 
In this operation, applying the mutation operation for the new population.  To perform the mutation operation, two random numbers  generated  such as R1, and R2 representing  two positions in each key then swap between value of the position R1 and the value of the position R2.  Repeat this operation for all keys in the "new population" pool.

### 7- Display the Round No. and Plaintext
In this operation, display the plaintext (clear text is unencrypted information) for storage or transmission after decrypted the ciphertext. Also, display the Round number that obtaining the plaintext from ciphertext.

## Programming

### 1 
