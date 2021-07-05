A cracker for a Vigenère-like cipher. Nothing sinister ;)

Requires a "crib mine file" that provides example plaintext, ideally from the authors of the ciphertext.

A typical usage involves sweeping a range of passwords lengths. This can be parallelized, e.g. for a quad-core system:

    seq 4 32 | xargs -n1 -P4 -J% ./crack --password_size % --crib_mine_file=home.html ciphertext
