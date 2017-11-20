# D7018E-Decryption
This branch discusses the safety differences between branch 3a and 3b.
Both when 3a and 3b is compiled and run the program panics when the array ends due to the array being shortened by one for each char until it disappears. This problem could in both implementations be fixed by for each recursion check the length of the data array. Because of this error (the program does not go outside its allocated space in both cases) and since there is only one thread there should not be any risk of race conditions.
