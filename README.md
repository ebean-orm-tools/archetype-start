# ebean-start maven archetype
A maven archetype to generate a project with basic setup.


## Example use:

```sh
mvn archetype:generate                                 \
  -DinteractiveMode=f                                  \
  -DarchetypeGroupId=org.avaje.ebeanorm                \
  -DarchetypeArtifactId=ebean-start                    \
  -DarchetypeVersion=1.0                               \
  -DgroupId=com.foo.myapp                              \
  -DartifactId=my-app

```
**where:**
- `com.foo.myapp` ... is your groupId 
- `my-app` ... is your artifactId 

This will generate a maven project with an Entity bean and some tests.
Note that this uses maven tiles so it is best to use maven 3.3+.

## Then run the tests ...
```sh
cd my-app
mvn clean test
```

This application is setup to run tests using H2 (via test-ebean.properties). 
There is a test-logback.xml with common logging configuration for sql / transactions etc.
