# Instrumentation

Instrumentation example code to get Object size in java

Steps to get this project working:
1) compile Sizeof.java with "javac Sizeof.java" -> will create Sizeof.class file

2) Place Sizeof.class file in "bin-> com-> fetchingsize"

3) Open cmd in bin\ folder

4) run "jar -cfm Sizeof.jar ..\META-INF\MANIFEST.MF" to form jar file with name Sizeof.jar

5) Now, we have to compile Main.java

6) During compilation, provide the path to Sizeof.jar in classpath so that compiler does not throw error while searching for Sizeof class. Run "javac -cp "bin\Sizeof.jar" Main.java". This will create Main.class file

7) Now, we have to run Main.class with javaagent as Sizeof.jar so that premain method is run beforehand. Run "java -javaagent:bin\Sizeof.jar Main". This will print output with object sizes.
