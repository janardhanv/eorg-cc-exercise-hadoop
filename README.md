eorg-cc-exercise-hadoop
=======================

Exercise on Hadoop and Elastic MapReduce

Instructions
------------

1. Download the project (as ZIP-file, https://github.com/mugglmenzel/eorg-cc-exercise-hadoop/raw/master/eorg-cc-exercise-hadoop.zip, or via git) and import into Eclipse.

2. Complete TODOs in the code to add the requested functionality.

  2a. For WordCountYahoo count words in yahoo.txt file with "Y" at the beginning. 

  2b.For WordCountDarwin count words in darwin.txt file that include "evolution".

3. Compile & Export the project as executable jar with main class
  
  3a. de.eorg.cloudcomputing.exercises.hadoop.WordCountYahoo
  
  3b. de.eorg.cloudcomputing.exercises.hadoop.WordCountDarwin

4. Upload executable jar and *.txt files (yahoo.txt, darwin.txt) to a S3 bucket.

5. Create a new Job Flow on AWS Elastic MapReduce (via AWS Management Console) with type "Custom JAR".

6. Set jar file "s3n://\<bucketname\>/\<executable-jar-file\>" and arguments to "s3n://\<bucketname\>/\<.txt-file\> s3n://\<bucketname\>/\<output-dir\>".

7. Run Job Flow (1 small instance is sufficient).

8. Results will be in the output dir on S3 you provided as an argument to the jar in the Job Flow.

Note: Output dir must be different for every Job Flow execution since MapReduce cannot overwrite files.