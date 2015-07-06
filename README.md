# Installation

## Install sablecc in your local repo

Download sablecc jar from the sablecc website, and install it into
your local repo:

```
mvn install:install-file -Dfile=sablecc.jar \
                        -DartifactId=sablecc \
                        -DgroupId=sablecc \
                        -Dversion=3.7 \
                        -Dpackaging=jar \
                        -DgeneratePom=true

```

## Compile Maven plugin

```
mvn install
```

# Configuration

Here are the parameters that can be used to configure the sablecc
maven plugin:

- `sourceDirectory`: Directory containing grammar files.  By default,
_${basedir}/src/main/sablecc_.
- `outputDirectory`: Directory containing the generated sources. By
default, _${project.build.directory}/generated-sources/sablecc_.
- `timestampDirectory`: Directory to store processed grammars.  By
default, _${basedir}/target_.
- `extensions`: List of extensions for the grammar files.  By default,
_.grammar_.
- `staleMillis`: Time elapsed after which source will need to be
  tested for recompilation. By default, _0_.

# Example of Use

```xml
      <plugin>
        <groupId>org.codehaus.mojo</groupId>
        <artifactId>sablecc-maven-plugin</artifactId>
        <version>2.4-SNAPSHOT</version>
        <executions>
          <execution>
            <goals>
			  <goal>generate</goal>
			</goals>
          </execution>
        </executions>
      </plugin>

```
