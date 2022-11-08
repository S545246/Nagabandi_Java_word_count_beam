1) First Downloaded Java JDK and placed in path varable in Env variables and also created a JAVA_HOME Varable and placed Java JDK path to it.
Once after successful installion of JDK and JDK setup, I did downlaoded Maven from this link https://dlcdn.apache.org/maven/maven-3/3.8.6/binaries/apache-maven-3.8.6-bin.zip after sucessful installation, I have unziped and placed the maven folder in C drive which will be safe location after placing it I have added the Maven bin path for Env variables in path variable once after sucessful setup I did restarted the pc to show the Maven version I used mvn -v to check the maven version.
2) I did created a new folder in my desktop with name Java-word-count-beam and I used Powershell to perform the beam Operations in Maven.
3) First I used below command to go to the right location from my local folder cd "C:\Users\S545246\OneDrive - nwmissouri.edu\Documents\big-data\Java-word-count-beam"
4) To Generate a Maven example project that builds against the latest Beam release and get all the dependencies of the project used the below command 
mvn archetype:generate `
  -D archetypeGroupId=org.apache.beam `
  -D archetypeArtifactId=beam-sdks-java-maven-archetypes-examples `
  -D archetypeVersion=2.42.0 `
  -D groupId=org.example `
  -D artifactId=word-count-beam `
  -D version="0.1" `
  -D package=org.apache.beam.examples `
  -D interactiveMode=false
5) After running the above Maven commands it creates a new project in the word-count-beam directory.
6) Changed into word-count-beam -- cd .\word-count-beam
7) For listing the example pipelines used this command: dir .\src\main\java\org\apache\beam\examples
8) After running the above command it will show list of examples in that loaction I used word count beam program
9) In the word-count-beam directory I created a file called sample.txt and Added text to the file. For this example.
10) Now I used below command to run the Wordcount using maven.
    mvn compile exec:java -D exec.mainClass=org.apache.beam.examples.WordCount `
        -D exec.args="--inputFile=sample.txt --output=counts" -P direct-runner 
11) 