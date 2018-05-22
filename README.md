```
$ mvn -Dimmutables.version=2.6.0-alpha3 clean package
[INFO] Scanning for projects...
[INFO] 
[INFO] ------------------------------------------------------------------------
[INFO] Building bnd-maven-plugin-20180522 0.0.1
[INFO] ------------------------------------------------------------------------
[INFO] 
[INFO] --- maven-clean-plugin:2.5:clean (default-clean) @ bnd-maven-plugin-20180522 ---
[INFO] Deleting /home/rm/git/com.github/io7m/bnd-maven-plugin-20180522/target
[INFO] 
[INFO] --- maven-resources-plugin:3.1.0:resources (default-resources) @ bnd-maven-plugin-20180522 ---
[WARNING] Using platform encoding (UTF-8 actually) to copy filtered resources, i.e. build is platform dependent!
[INFO] skip non existing resourceDirectory /home/rm/git/com.github/io7m/bnd-maven-plugin-20180522/src/main/resources
[INFO] 
[INFO] --- maven-compiler-plugin:3.7.0:compile (default-compile) @ bnd-maven-plugin-20180522 ---
[INFO] Changes detected - recompiling the module!
[WARNING] File encoding has not been set, using platform encoding UTF-8, i.e. build is platform dependent!
[INFO] Compiling 1 source file to /home/rm/git/com.github/io7m/bnd-maven-plugin-20180522/target/classes
[INFO] 
[INFO] --- bnd-maven-plugin:4.0.0:bnd-process (osgi-manifest) @ bnd-maven-plugin-20180522 ---
[INFO] 
[INFO] --- maven-resources-plugin:3.1.0:testResources (default-testResources) @ bnd-maven-plugin-20180522 ---
[WARNING] Using platform encoding (UTF-8 actually) to copy filtered resources, i.e. build is platform dependent!
[INFO] skip non existing resourceDirectory /home/rm/git/com.github/io7m/bnd-maven-plugin-20180522/src/test/resources
[INFO] 
[INFO] --- maven-compiler-plugin:3.7.0:testCompile (default-testCompile) @ bnd-maven-plugin-20180522 ---
[INFO] No sources to compile
[INFO] 
[INFO] --- maven-surefire-plugin:2.21.0:test (default-test) @ bnd-maven-plugin-20180522 ---
[INFO] No tests to run.
[INFO] 
[INFO] --- maven-bundle-plugin:3.5.0:bundle (default-bundle) @ bnd-maven-plugin-20180522 ---
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time: 4.302 s
[INFO] Finished at: 2018-05-22T13:37:42+01:00
[INFO] Final Memory: 23M/80M
[INFO] ------------------------------------------------------------------------

$ cat target/MANIFEST.MF
Manifest-Version: 1.0
Bnd-LastModified: 1526992766679
Bundle-ManifestVersion: 2
Bundle-Name: bnd-maven-plugin-20180522
Bundle-SymbolicName: bnd-maven-plugin-20180522
Bundle-Version: 0.0.1
Created-By: 10.0.1 (Oracle Corporation)
Private-Package: com.io7m.example
Require-Capability: osgi.ee;filter:="(&(osgi.ee=JavaSE)(version=9.0))"
Tool: Bnd-4.0.0.201805111645

$ bnd print target/bnd-maven-plugin-20180522-0.0.1.jar
[MANIFEST bnd-maven-plugin-20180522-0.0.1]
Bnd-LastModified                         1526992767507                           
Build-Jdk                                10.0.1                                  
Built-By                                 rm                                      
Bundle-ManifestVersion                   2                                       
Bundle-Name                              bnd-maven-plugin-20180522               
Bundle-SymbolicName                      com.io7m.examples.bnd-maven-plugin-20180522
Bundle-Version                           0.0.1                                   
Created-By                               Apache Maven Bundle Plugin              
Export-Package                           com.io7m.example;version="0.0.1"        
Manifest-Version                         1.0                                     
Require-Capability                       osgi.ee;filter:="(&(osgi.ee=JavaSE)(version=9.0))"
Tool                                     Bnd-3.5.0.201709291849                  

[IMPEXP]
Export-Package
  com.io7m.example                       {version=0.0.1}

$ mvn -Dimmutables.version=2.6.0 clean package
[INFO] Scanning for projects...
[INFO] 
[INFO] ------------------------------------------------------------------------
[INFO] Building bnd-maven-plugin-20180522 0.0.1
[INFO] ------------------------------------------------------------------------
[INFO] 
[INFO] --- maven-clean-plugin:2.5:clean (default-clean) @ bnd-maven-plugin-20180522 ---
[INFO] Deleting /home/rm/git/com.github/io7m/bnd-maven-plugin-20180522/target
[INFO] 
[INFO] --- maven-resources-plugin:3.1.0:resources (default-resources) @ bnd-maven-plugin-20180522 ---
[WARNING] Using platform encoding (UTF-8 actually) to copy filtered resources, i.e. build is platform dependent!
[INFO] skip non existing resourceDirectory /home/rm/git/com.github/io7m/bnd-maven-plugin-20180522/src/main/resources
[INFO] 
[INFO] --- maven-compiler-plugin:3.7.0:compile (default-compile) @ bnd-maven-plugin-20180522 ---
[INFO] Changes detected - recompiling the module!
[WARNING] File encoding has not been set, using platform encoding UTF-8, i.e. build is platform dependent!
[INFO] Compiling 1 source file to /home/rm/git/com.github/io7m/bnd-maven-plugin-20180522/target/classes
[INFO] 
[INFO] --- bnd-maven-plugin:4.0.0:bnd-process (osgi-manifest) @ bnd-maven-plugin-20180522 ---
[INFO] 
[INFO] --- maven-resources-plugin:3.1.0:testResources (default-testResources) @ bnd-maven-plugin-20180522 ---
[WARNING] Using platform encoding (UTF-8 actually) to copy filtered resources, i.e. build is platform dependent!
[INFO] skip non existing resourceDirectory /home/rm/git/com.github/io7m/bnd-maven-plugin-20180522/src/test/resources
[INFO] 
[INFO] --- maven-compiler-plugin:3.7.0:testCompile (default-testCompile) @ bnd-maven-plugin-20180522 ---
[INFO] No sources to compile
[INFO] 
[INFO] --- maven-surefire-plugin:2.21.0:test (default-test) @ bnd-maven-plugin-20180522 ---
[INFO] No tests to run.
[INFO] 
[INFO] --- maven-bundle-plugin:3.5.0:bundle (default-bundle) @ bnd-maven-plugin-20180522 ---
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time: 4.429 s
[INFO] Finished at: 2018-05-22T13:37:52+01:00
[INFO] Final Memory: 23M/84M
[INFO] ------------------------------------------------------------------------

$ cat target/MANIFEST.MF
Manifest-Version: 1.0
Bnd-LastModified: 1526992842169
Bundle-ManifestVersion: 2
Bundle-Name: bnd-maven-plugin-20180522
Bundle-SymbolicName: bnd-maven-plugin-20180522
Bundle-Version: 0.0.1
Created-By: 10.0.1 (Oracle Corporation)
Import-Package: org.immutables.value
                ^^^^^^^^^^^^^^^^^^^^
Private-Package: com.io7m.example
Require-Capability: osgi.ee;filter:="(&(osgi.ee=JavaSE)(version=9.0))"
Tool: Bnd-4.0.0.201805111645

$ bnd print target/bnd-maven-plugin-20180522-0.0.1.jar
[MANIFEST bnd-maven-plugin-20180522-0.0.1]
Bnd-LastModified                         1526992843028                           
Build-Jdk                                10.0.1                                  
Built-By                                 rm                                      
Bundle-ManifestVersion                   2                                       
Bundle-Name                              bnd-maven-plugin-20180522               
Bundle-SymbolicName                      com.io7m.examples.bnd-maven-plugin-20180522
Bundle-Version                           0.0.1                                   
Created-By                               Apache Maven Bundle Plugin              
Export-Package                           com.io7m.example;uses:="org.immutables.value";version="0.0.1"
Import-Package                           org.immutables.value                    
Manifest-Version                         1.0                                     
Require-Capability                       osgi.ee;filter:="(&(osgi.ee=JavaSE)(version=9.0))"
Tool                                     Bnd-3.5.0.201709291849                  

[IMPEXP]
Import-Package
  org.immutables.value                   
Export-Package
  com.io7m.example                       {version=0.0.1}

```
