Apache Ant is a Java library and command-line tool whose mission is to drive processes described in build files as targets and extension points dependent upon each other. The main known usage of Ant is the build of Java applications. Ant supplies a number of built-in tasks allowing to compile, assemble, test and run Java applications. Ant can also be used effectively to build non Java applications, for instance C or C++ applications. More generally, Ant can be used to pilot any type of process which can be described in terms of targets and tasks.

Ant is a Java based build tool. In theory it is kind of like "make" 
without makes wrinkles and with the full portability of pure java code.

- Begin with official documentation, the user manual.
https://rawgit.com/apache/ant/master/manual/index.html

- Install Apache Ant
- https://rawgit.com/apache/ant/master/manual/install.html#installing

- I have omitted notekeeping of creating a jar and running it using java only commands in this note file and instead documented the process within Java Prep.


# build.xml
- Simple build tool usage (Process documented below)
https://ant.apache.org/manual/tutorial-HelloWorldWithAnt.html

Create a build.xml file that allows us to use ANT to do what we just did using java commands.

After creating the build.xml file at the base directory, we have use ANT to
- compile
- package
- run the application

done so by running the command:
	ant compiler jar run

![[Pasted image 20230521000508.png]]

We now have a working build file.

# Enhancements to build.xml 

Let's adjust the build file to take advantage of the attributes that ANT gives us. We'll use the properties attribute and adjust compilation.

![[Pasted image 20230521001816.png]]

Now, the only command needed to run was 
	ant


# External Libraries

Adjusted our main java class to import log4 for some nice logging.

![[Pasted image 20230522012108.png]]

- Created a lib folder and placed the required log4 jar within it
- Linked the external jar using the modulepath within eclipse to get rid of IDE compiler errors
- Linked the module path and external jar within the build.xml

![[Pasted image 20230522011955.png]]



# Configurations
- Removed our hardcoded configuration setup in the HelloWorld class
- Added a new log4j.properties file within src directory
- Adjusted the build.xml to copy these files upon compilation

![[Pasted image 20230522013257.png]]

![[Pasted image 20230522013239.png]]


# Conclusions
This ends our simple example of 
- utilizing ANT to have a steady build process
- referencing external jars and modules using ANT and eclipse
