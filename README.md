# fastq-lossy
A high compression fastq lossy library

A dictionary representation of the original order and one ordered by quality score of each base pair is created.

The dictionary uses run-length encoding (RLE) so that recurring bases are identified by base and count.

A dictionary coder is used to represent each unique RLE base and count.

Linear prediction is used to replace the quality values (when plotted along the quality score order series).

Overall the storage required for sequencing values is less than optimal (compared with other compression techniques) due to the maintenance of multiple dictionaries. However the quality score storage is greatly reduced.

There is a loss of data (lossy) due to linear prediction of quality scores and the replacement of the 'N' base value with alternative base value with 0 score. 
