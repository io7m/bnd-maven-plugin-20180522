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

------------------------------------------------------------------------

$ java -jar japicmp-0.12.0-jar-with-dependencies.jar --only-modified  --old /tmp/value-2.6.0-alpha3.jar --new /tmp/value-2.6.0.jar

Comparing source compatibility of /tmp/value-2.6.0.jar against /tmp/value-2.6.0-alpha3.jar
+++  NEW ANNOTATION: PUBLIC(+) ABSTRACT(+) org.immutables.value.Generated  (not serializable)
	+++  CLASS FILE FORMAT VERSION: 50.0 <- n.a.
	+++  NEW INTERFACE: java.lang.annotation.Annotation
	+++  NEW SUPERCLASS: java.lang.Object
	+++  NEW METHOD: PUBLIC(+) ABSTRACT(+) java.lang.String from()
	+++  NEW METHOD: PUBLIC(+) ABSTRACT(+) java.lang.String generator()
	+++  NEW ANNOTATION: java.lang.annotation.Target
		+++  NEW ELEMENT: value=java.lang.annotation.ElementType.TYPE (+)
	+++  NEW ANNOTATION: java.lang.annotation.Retention
		+++  NEW ELEMENT: value=java.lang.annotation.RetentionPolicy.RUNTIME (+)
***  MODIFIED CLASS: PUBLIC FINAL org.immutables.value.internal.$generator$.$AnnotationMirrors  (not serializable)
	===  CLASS FILE FORMAT VERSION: 51.0 <- 51.0
	+++  NEW METHOD: PUBLIC(+) STATIC(+) javax.lang.model.element.AnnotationMirror findAnnotation(java.util.List, java.lang.String)
		+++  NEW ANNOTATION: javax.annotation.Nullable
	+++  NEW METHOD: PUBLIC(+) STATIC(+) java.lang.CharSequence toCharSequence(javax.lang.model.element.AnnotationValue)
***! MODIFIED CLASS: PUBLIC FINAL org.immutables.value.internal.$generator$.$ExtensionLoader  (not serializable)
	===  CLASS FILE FORMAT VERSION: 51.0 <- 51.0
	***! MODIFIED METHOD: PUBLIC STATIC org.immutables.value.internal.$guava$.base.$Supplier (<-org.immutables.value.internal.$guava$.collect.$ImmutableSet) findExtensions(java.lang.String)
+++  NEW CLASS: PUBLIC(+) FINAL(+) org.immutables.value.internal.$guava$.base.$Suppliers  (not serializable)
	+++  CLASS FILE FORMAT VERSION: 50.0 <- n.a.
	+++  NEW SUPERCLASS: java.lang.Object
	+++  NEW METHOD: PUBLIC(+) STATIC(+) org.immutables.value.internal.$guava$.base.$Supplier compose(org.immutables.value.internal.$guava$.base.$Function, org.immutables.value.internal.$guava$.base.$Supplier)
	+++  NEW METHOD: PUBLIC(+) STATIC(+) org.immutables.value.internal.$guava$.base.$Supplier memoize(org.immutables.value.internal.$guava$.base.$Supplier)
	+++  NEW METHOD: PUBLIC(+) STATIC(+) org.immutables.value.internal.$guava$.base.$Supplier memoizeWithExpiration(org.immutables.value.internal.$guava$.base.$Supplier, long, java.util.concurrent.TimeUnit)
	+++  NEW METHOD: PUBLIC(+) STATIC(+) org.immutables.value.internal.$guava$.base.$Supplier ofInstance(java.lang.Object)
	+++  NEW METHOD: PUBLIC(+) STATIC(+) org.immutables.value.internal.$guava$.base.$Function supplierFunction()
	+++  NEW METHOD: PUBLIC(+) STATIC(+) org.immutables.value.internal.$guava$.base.$Supplier synchronizedSupplier(org.immutables.value.internal.$guava$.base.$Supplier)
	+++  NEW ANNOTATION: javax.annotation.CheckReturnValue
***  MODIFIED CLASS: PUBLIC FINAL org.immutables.value.internal.$processor$.encode.$Instantiation  (not serializable)
	===  CLASS FILE FORMAT VERSION: 51.0 <- 51.0
	+++  NEW METHOD: PUBLIC(+) org.immutables.value.internal.$processor$.meta.$ValueType getContainingType()
***  MODIFIED CLASS: PUBLIC FINAL org.immutables.value.internal.$processor$.meta.$AnnotationInjections  (not serializable)
	===  CLASS FILE FORMAT VERSION: 51.0 <- 51.0
	+++  NEW METHOD: PUBLIC(+) STATIC(+) java.util.Collection collectInjections(javax.lang.model.element.Element, org.immutables.value.internal.$processor$.meta.$AnnotationInjections$InjectAnnotation$Where, java.lang.Iterable[])
		+++  NEW ANNOTATION: java.lang.SafeVarargs
+++  NEW CLASS: PUBLIC(+) STATIC(+) FINAL(+) org.immutables.value.internal.$processor$.meta.$AnnotationInjections$AnnotationInjection  (not serializable)
	+++  CLASS FILE FORMAT VERSION: 51.0 <- n.a.
	+++  NEW SUPERCLASS: java.lang.Object
***  MODIFIED ENUM: PUBLIC STATIC FINAL org.immutables.value.internal.$processor$.meta.$AnnotationInjections$InjectAnnotation$Where  (compatible)
	===  CLASS FILE FORMAT VERSION: 51.0 <- 51.0
	+++  NEW FIELD: PUBLIC(+) STATIC(+) FINAL(+) org.immutables.value.internal.$processor$.meta.$AnnotationInjections$InjectAnnotation$Where CONSTRUCTOR
	+++  NEW FIELD: PUBLIC(+) STATIC(+) FINAL(+) org.immutables.value.internal.$processor$.meta.$AnnotationInjections$InjectAnnotation$Where MODIFIABLE_TYPE
***  MODIFIED CLASS: PUBLIC FINAL org.immutables.value.internal.$processor$.meta.$GsonMirrors  (not serializable)
	===  CLASS FILE FORMAT VERSION: 51.0 <- 51.0
	+++  NEW FIELD: PUBLIC(+) STATIC(+) java.lang.String JSON_OBJECT_TYPE
+++  NEW ANNOTATION: PUBLIC(+) ABSTRACT(+) STATIC(+) org.immutables.value.internal.$processor$.meta.$GsonMirrors$GsonOther  (not serializable)
	+++  CLASS FILE FORMAT VERSION: 51.0 <- n.a.
	+++  NEW INTERFACE: java.lang.annotation.Annotation
	+++  NEW SUPERCLASS: java.lang.Object
+++  NEW CLASS: PUBLIC(+) org.immutables.value.internal.$processor$.meta.$GsonOtherMirror  (not serializable)
	+++  CLASS FILE FORMAT VERSION: 51.0 <- n.a.
	+++  NEW INTERFACE: java.lang.annotation.Annotation
	+++  NEW INTERFACE: org.immutables.value.internal.$processor$.meta.$GsonMirrors$GsonOther
	+++  NEW SUPERCLASS: java.lang.Object
	+++  NEW FIELD: PUBLIC(+) STATIC(+) FINAL(+) java.lang.String MIRROR_QUALIFIED_NAME
	+++  NEW FIELD: PUBLIC(+) STATIC(+) FINAL(+) java.lang.String QUALIFIED_NAME
	+++  NEW METHOD: PUBLIC(+) java.lang.Class annotationType()
	+++  NEW METHOD: PUBLIC(+) boolean equals(java.lang.Object)
	+++  NEW METHOD: PUBLIC(+) STATIC(+) org.immutables.value.internal.$guava$.base.$Optional find(javax.lang.model.element.Element)
	+++  NEW METHOD: PUBLIC(+) STATIC(+) org.immutables.value.internal.$guava$.base.$Optional find(java.lang.Iterable)
	+++  NEW METHOD: PUBLIC(+) STATIC(+) org.immutables.value.internal.$processor$.meta.$GsonOtherMirror from(javax.lang.model.element.TypeElement)
	+++  NEW METHOD: PUBLIC(+) STATIC(+) org.immutables.value.internal.$guava$.base.$Optional from(javax.lang.model.element.AnnotationMirror)
	+++  NEW METHOD: PUBLIC(+) STATIC(+) org.immutables.value.internal.$guava$.collect.$ImmutableList fromAll(java.lang.Iterable)
	+++  NEW METHOD: PUBLIC(+) javax.lang.model.element.AnnotationMirror getAnnotationMirror()
	+++  NEW METHOD: PUBLIC(+) int hashCode()
	+++  NEW METHOD: PUBLIC(+) STATIC(+) boolean isPresent(javax.lang.model.element.Element)
	+++  NEW METHOD: PUBLIC(+) STATIC(+) java.lang.String mirrorQualifiedName()
	+++  NEW METHOD: PUBLIC(+) STATIC(+) java.lang.String qualifiedName()
	+++  NEW METHOD: PUBLIC(+) STATIC(+) java.lang.String simpleName()
	+++  NEW METHOD: PUBLIC(+) java.lang.String toString()
***! MODIFIED CLASS: PUBLIC FINAL org.immutables.value.internal.$processor$.meta.$ImmutableStyleInfo  (not serializable)
	===  CLASS FILE FORMAT VERSION: 51.0 <- 51.0
	===* UNCHANGED INTERFACE: org.immutables.value.internal.$processor$.meta.$ValueMirrors$Style
	+++  NEW METHOD: PUBLIC(+) boolean alwaysPublicInitializers()
	+++  NEW METHOD: PUBLIC(+) java.lang.String canBuild()
	---! REMOVED METHOD: PUBLIC(-) STATIC(-) org.immutables.value.internal.$processor$.meta.$ImmutableStyleInfo of(java.lang.String[], java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String[], java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, org.immutables.value.internal.$processor$.meta.$ValueImmutableInfo, boolean, org.immutables.value.internal.$processor$.meta.$ValueMirrors$Style$ValidationMethod, boolean, boolean, boolean, boolean, org.immutables.value.internal.$guava$.collect.$ImmutableSet, org.immutables.value.internal.$guava$.collect.$ImmutableSet, org.immutables.value.internal.$processor$.meta.$ValueMirrors$Style$ImplementationVisibility, boolean, boolean, boolean, boolean, boolean, boolean, boolean, boolean, boolean, boolean, boolean, boolean, boolean, boolean, org.immutables.value.internal.$processor$.meta.$ValueMirrors$Style$BuilderVisibility, java.lang.String, boolean, java.lang.String[], org.immutables.value.internal.$guava$.collect.$ImmutableSet, boolean, boolean, boolean, boolean, java.lang.String, boolean, java.lang.String[], java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, org.immutables.value.internal.$guava$.collect.$ImmutableSet)
	---! REMOVED METHOD: PUBLIC(-) STATIC(-) org.immutables.value.internal.$processor$.meta.$ImmutableStyleInfo of(java.lang.String[], java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String[], java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, org.immutables.value.internal.$processor$.meta.$ValueImmutableInfo, boolean, org.immutables.value.internal.$processor$.meta.$ValueMirrors$Style$ValidationMethod, boolean, boolean, boolean, boolean, java.lang.Iterable, java.lang.Iterable, org.immutables.value.internal.$processor$.meta.$ValueMirrors$Style$ImplementationVisibility, boolean, boolean, boolean, boolean, boolean, boolean, boolean, boolean, boolean, boolean, boolean, boolean, boolean, boolean, org.immutables.value.internal.$processor$.meta.$ValueMirrors$Style$BuilderVisibility, java.lang.String, boolean, java.lang.String[], java.lang.Iterable, boolean, boolean, boolean, boolean, java.lang.String, boolean, java.lang.String[], java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.Iterable)
	+++  NEW METHOD: PUBLIC(+) STATIC(+) org.immutables.value.internal.$processor$.meta.$ImmutableStyleInfo of(java.lang.String[], java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String[], java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, org.immutables.value.internal.$processor$.meta.$ValueImmutableInfo, boolean, org.immutables.value.internal.$processor$.meta.$ValueMirrors$Style$ValidationMethod, boolean, boolean, boolean, boolean, org.immutables.value.internal.$guava$.collect.$ImmutableSet, org.immutables.value.internal.$guava$.collect.$ImmutableSet, org.immutables.value.internal.$processor$.meta.$ValueMirrors$Style$ImplementationVisibility, boolean, boolean, boolean, boolean, boolean, boolean, boolean, boolean, boolean, boolean, boolean, boolean, boolean, boolean, boolean, org.immutables.value.internal.$processor$.meta.$ValueMirrors$Style$BuilderVisibility, java.lang.String, java.lang.String, boolean, java.lang.String[], org.immutables.value.internal.$guava$.collect.$ImmutableSet, boolean, boolean, boolean, boolean, java.lang.String, boolean, java.lang.String[], java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, org.immutables.value.internal.$guava$.collect.$ImmutableSet)
	+++  NEW METHOD: PUBLIC(+) STATIC(+) org.immutables.value.internal.$processor$.meta.$ImmutableStyleInfo of(java.lang.String[], java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String[], java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, org.immutables.value.internal.$processor$.meta.$ValueImmutableInfo, boolean, org.immutables.value.internal.$processor$.meta.$ValueMirrors$Style$ValidationMethod, boolean, boolean, boolean, boolean, java.lang.Iterable, java.lang.Iterable, org.immutables.value.internal.$processor$.meta.$ValueMirrors$Style$ImplementationVisibility, boolean, boolean, boolean, boolean, boolean, boolean, boolean, boolean, boolean, boolean, boolean, boolean, boolean, boolean, boolean, org.immutables.value.internal.$processor$.meta.$ValueMirrors$Style$BuilderVisibility, java.lang.String, java.lang.String, boolean, java.lang.String[], java.lang.Iterable, boolean, boolean, boolean, boolean, java.lang.String, boolean, java.lang.String[], java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.Iterable)
	+++  NEW METHOD: PUBLIC(+) java.lang.String throwForNullPointerName()
	+++  NEW METHOD: PUBLIC(+) FINAL(+) org.immutables.value.internal.$processor$.meta.$ImmutableStyleInfo withAlwaysPublicInitializers(boolean)
	+++  NEW METHOD: PUBLIC(+) FINAL(+) org.immutables.value.internal.$processor$.meta.$ImmutableStyleInfo withCanBuild(java.lang.String)
	+++  NEW METHOD: PUBLIC(+) FINAL(+) org.immutables.value.internal.$processor$.meta.$ImmutableStyleInfo withThrowForNullPointerName(java.lang.String)
***  MODIFIED CLASS: PUBLIC ABSTRACT STATIC org.immutables.value.internal.$processor$.meta.$Proto$AbstractDeclaring  (not serializable)
	===  CLASS FILE FORMAT VERSION: 51.0 <- 51.0
	+++  NEW METHOD: PUBLIC(+) java.util.List getAnnotationInjections()
**** MODIFIED CLASS: PUBLIC ABSTRACT org.immutables.value.internal.$processor$.meta.$StyleInfo  (not serializable)
	===  CLASS FILE FORMAT VERSION: 51.0 <- 51.0
	===* UNCHANGED INTERFACE: org.immutables.value.internal.$processor$.meta.$ValueMirrors$Style
	+++  NEW METHOD: PUBLIC(+) ABSTRACT(+) boolean alwaysPublicInitializers()
	+++  NEW METHOD: PUBLIC(+) ABSTRACT(+) java.lang.String canBuild()
	+++  NEW METHOD: PUBLIC(+) java.lang.Class throwForNullPointer()
		+++  NEW ANNOTATION: java.lang.Deprecated
	+++* NEW METHOD: PUBLIC(+) ABSTRACT(+) java.lang.String throwForNullPointerName()
***  MODIFIED CLASS: PUBLIC org.immutables.value.internal.$processor$.meta.$StyleMirror  (not serializable)
	===  CLASS FILE FORMAT VERSION: 51.0 <- 51.0
	===* UNCHANGED INTERFACE: org.immutables.value.internal.$processor$.meta.$ValueMirrors$Style
	+++  NEW METHOD: PUBLIC(+) boolean alwaysPublicInitializers()
	+++  NEW METHOD: PUBLIC(+) java.lang.String canBuild()
	+++  NEW METHOD: PUBLIC(+) java.lang.Class throwForNullPointer()
		+++  NEW ANNOTATION: java.lang.Deprecated
	+++  NEW METHOD: PUBLIC(+) javax.lang.model.type.TypeMirror throwForNullPointerMirror()
	+++  NEW METHOD: PUBLIC(+) java.lang.String throwForNullPointerName()
***  MODIFIED CLASS: PUBLIC FINAL org.immutables.value.internal.$processor$.meta.$Styles$UsingName$AttributeNames  (not serializable)
	===  CLASS FILE FORMAT VERSION: 51.0 <- 51.0
	+++  NEW METHOD: PUBLIC(+) java.lang.String addv()
	+++  NEW METHOD: PUBLIC(+) java.lang.String putv()
***  MODIFIED CLASS: PUBLIC org.immutables.value.internal.$processor$.meta.$Styles$UsingName$TypeNames  (not serializable)
	===  CLASS FILE FORMAT VERSION: 51.0 <- 51.0
	+++  NEW METHOD: PUBLIC(+) FINAL(+) java.lang.String canBuild()
***  MODIFIED CLASS: PUBLIC FINAL org.immutables.value.internal.$processor$.meta.$ValueAttribute  (not serializable)
	===  CLASS FILE FORMAT VERSION: 51.0 <- 51.0
	+++  NEW FIELD: PUBLIC(+) org.immutables.value.internal.$guava$.collect.$ImmutableList annotationInjections
	+++  NEW METHOD: PUBLIC(+) java.util.Collection accessorInjectedAnnotations()
	+++  NEW METHOD: PUBLIC(+) java.util.Collection constructorParameterInjectedAnnotations()
	+++  NEW METHOD: PUBLIC(+) java.util.Collection elementInitializerInjectedAnnotations()
	+++  NEW METHOD: PUBLIC(+) java.util.Collection fieldInjectedAnnotations()
	+++  NEW METHOD: PUBLIC(+) java.lang.String getIntializerAccess()
	+++  NEW METHOD: PUBLIC(+) java.util.Collection initializerInjectedAnnotations()
	+++  NEW METHOD: PUBLIC(+) boolean isGsonOther()
	+++  NEW METHOD: PUBLIC(+) java.util.Collection syntheticFieldsInjectedAnnotations()
**** MODIFIED ANNOTATION: PUBLIC ABSTRACT STATIC org.immutables.value.internal.$processor$.meta.$ValueMirrors$Style  (not serializable)
	===  CLASS FILE FORMAT VERSION: 51.0 <- 51.0
	+++* NEW METHOD: PUBLIC(+) ABSTRACT(+) boolean alwaysPublicInitializers()
	+++* NEW METHOD: PUBLIC(+) ABSTRACT(+) java.lang.String canBuild()
	+++* NEW METHOD: PUBLIC(+) ABSTRACT(+) java.lang.Class throwForNullPointer()
***  MODIFIED CLASS: PUBLIC FINAL org.immutables.value.internal.$processor$.meta.$ValueType  (not serializable)
	===  CLASS FILE FORMAT VERSION: 51.0 <- 51.0
	+++  NEW METHOD: PUBLIC(+) java.util.Collection builderTypeInjectedAnnotations()
	+++  NEW METHOD: PUBLIC(+) java.util.Collection constructorInjectedAnnotations()
	+++  NEW METHOD: PUBLIC(+) org.immutables.value.internal.$processor$.meta.$ValueAttribute getGsonOther()
		+++  NEW ANNOTATION: javax.annotation.Nullable
	+++  NEW METHOD: PUBLIC(+) java.lang.String getThrowForNullPointer()
	+++  NEW METHOD: PUBLIC(+) java.util.Collection immutableTypeInjectedAnnotations()
	+++  NEW METHOD: PUBLIC(+) boolean isGenerateCanBuild()
	+++  NEW METHOD: PUBLIC(+) java.util.Collection modifiableTypeInjectedAnnotations()
	+++  NEW METHOD: PUBLIC(+) java.util.Collection syntheticFieldsInjectedAnnotations()
===  UNCHANGED ANNOTATION: PUBLIC ABSTRACT STATIC org.immutables.value.Value$Auxiliary  (not serializable)
	===  CLASS FILE FORMAT VERSION: 50.0 <- 50.0
	---  REMOVED ANNOTATION: java.lang.annotation.Retention
		---  REMOVED ELEMENT: value=java.lang.annotation.RetentionPolicy.CLASS (-)
===  UNCHANGED ANNOTATION: PUBLIC ABSTRACT STATIC org.immutables.value.Value$Default  (not serializable)
	===  CLASS FILE FORMAT VERSION: 50.0 <- 50.0
	---  REMOVED ANNOTATION: java.lang.annotation.Retention
		---  REMOVED ELEMENT: value=java.lang.annotation.RetentionPolicy.CLASS (-)
===  UNCHANGED ANNOTATION: PUBLIC ABSTRACT STATIC org.immutables.value.Value$Lazy  (not serializable)
	===  CLASS FILE FORMAT VERSION: 50.0 <- 50.0
	---  REMOVED ANNOTATION: java.lang.annotation.Retention
		---  REMOVED ELEMENT: value=java.lang.annotation.RetentionPolicy.CLASS (-)
===  UNCHANGED ANNOTATION: PUBLIC ABSTRACT STATIC org.immutables.value.Value$Modifiable  (not serializable)
	===  CLASS FILE FORMAT VERSION: 50.0 <- 50.0
	---  REMOVED ANNOTATION: java.lang.annotation.Retention
		---  REMOVED ELEMENT: value=java.lang.annotation.RetentionPolicy.CLASS (-)
===  UNCHANGED ANNOTATION: PUBLIC ABSTRACT STATIC org.immutables.value.Value$Parameter  (not serializable)
	===  CLASS FILE FORMAT VERSION: 50.0 <- 50.0
	---  REMOVED ANNOTATION: java.lang.annotation.Retention
		---  REMOVED ELEMENT: value=java.lang.annotation.RetentionPolicy.CLASS (-)
===  UNCHANGED ANNOTATION: PUBLIC ABSTRACT STATIC org.immutables.value.Value$Redacted  (not serializable)
	===  CLASS FILE FORMAT VERSION: 50.0 <- 50.0
	---  REMOVED ANNOTATION: java.lang.annotation.Retention
		---  REMOVED ELEMENT: value=java.lang.annotation.RetentionPolicy.CLASS (-)
**** MODIFIED ANNOTATION: PUBLIC ABSTRACT STATIC org.immutables.value.Value$Style  (not serializable)
	===  CLASS FILE FORMAT VERSION: 50.0 <- 50.0
	+++* NEW METHOD: PUBLIC(+) ABSTRACT(+) boolean alwaysPublicInitializers()
	+++* NEW METHOD: PUBLIC(+) ABSTRACT(+) java.lang.String canBuild()
	+++* NEW METHOD: PUBLIC(+) ABSTRACT(+) java.lang.Class throwForNullPointer()
```
