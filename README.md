# De-Bruijn-graph
Directed graph used for de novo assembly of sequencing reads into a genome.
Function:
    getReads
Description:
    Generic for (paired and single)
    Read First line get K and G (Case Paired)
    Time Complexity: O(1)
Input:
    FileName: String carries the text fileName
    Paired: boolean carries 0 for single reads and 1 for paired reads
Returns:
    Either K-mers, gap and Reads for Paired Reads or K-mers and Reads for Single Reads
Invoked/Called:
    Called at the beginning in Main
    
    Function:  
    prefixExists
Description: 
    Generic for (paired and single)
    Checks if the prefix (aka key of the dictionary used to store reads) exists before i.e. prefix has more than one suffix.
    thus append the other suffix (where suffix is a list). if prefix doesn't exist then add it & it's first suffix element in 
    the list to the dictionary.
    Time Complexity: O(1)
Input: 
    Dictionary that is filled with { prefix : suffix } called "Graph"
    string carriers prefix used as the key for dict called "prefix"
    list of suffix carries suffix called "suffix"
Returns: 
    Graph
Invokes/Called: 
    Called in DebruijinGraph Function
'''

'''
Function: 
    Debruijn Graph
Description: 
    Generic Function for both single and paired
    Creates Graph using Splitting and Slicing Techniques
    Data Structure for graph -> used dictionary where value is a list
    Time Complexity -> O(N), where n is # of reads i.e. lines in file - 1
Input:
    Paired boolean
    Kmers and Reads 
Returns:
    Table/ Graph in a dictionary
Invokes/Called:
    Invokes: prefixExists
    Called: Main
'''

'''
Function: 
    eulerian_Path
Description: 
    Generic Function (paired and single) for finding path 
    Time Compexity -> O(2N) , N = dictionary length (keys)
Input:
    Graph dictionary
Returns:
    list carries the path of the reads called "walk"
Invokes/Called:
    Called in Main
'''
'''
Function:  
    Paired Assemble
Description: 
    Get Assembly for paired using Slicing Technique
    Time Complexity -> O(M); M = Path length
Input:
    Path (list)
Returns:
    3 strings carries prefix, suffix and Genome
Invokes/Called:
    called in Main
'''
