----------------------------------------------------------------------------------
Citation Policy:
----------------------------------------------------------------------------------
If you publish material based on our algorithms, then, in your references, please cite one of the following:

[1] Junqiang Liu, Yunhe Pan, Ke Wang, and Jiawei Han. Mining frequent item sets by opportunistic projection. The 8th SIGKDD, pages 229-238, Edmonton, Canada, July, 2002.

[2] Junqiang Liu, and Yunhe Pan. An efficient algorithm for mining closed itemsets. Journal of Zhejiang University SCIENCE, 2004, 5(1).

----------------------------------------------------------------------------------
Example
----------------------------------------------------------------------------------

fp.txt  					(an example transaction file)

asc2bi fp.txt fp.bi 				(to convert a text-file into a binary-file)

fp.spec 					(an example specification file)

op	-dfp.spec -s60 -p1 -rResult.txt		(to run the algorithm - the complete set of patterns)

crop 	-dfp.spec -s60 -p1 -rResult.txt -u1 	(to run the algorithm - the closed set of patterns)

----------------------------------------------------------------------------------
Help
----------------------------------------------------------------------------------

OP - Mining Frquent Item Sets by Opportunistic Projection V3.0 (06.12.2002)
        Copyright (C) 2000-2005 Junqiang Liu
No distribution without written permission from Junqiang Liu

commandline: OP -Dspecfile -Sminsupp [-P] [-Exxx] [-Rresultfile]
-D the specification file of a transaction database
-S the support threshold(%) (default: 10%)
-P the option to write patterns to file (default: no)
-E the upper bound of free memory (default: 256M)
-R the output file path

FORMAT of specification file:
        the transaction file name
        the largest value of item_id (N items are identified by 1, .., N-1)
        the maximum length of transactions
        the number of transactions

FORMAT of transaction file (must be a binary file):
        the length_of_transaction    item_id_1   ...   item_id_n
                ......
        the length_of_transaction    item_id_1   ...   item_id_n

Assumptions:
        no repetitive items in the same transaction,
        the length of any transaction is less than 512,
        the total occurances of frequent items can be represented by a long integer,
        and the transaction file size is less than 2G bytes.

----------------------------------------------------------------------------------

