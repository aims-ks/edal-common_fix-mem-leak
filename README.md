This project was build to fix a memory leak in edal-common, preventing the NcAnimate project to produce its images.

The project only contains copy of the class which require modifications.

This jar is not a replacement for edal-commons, it's just an overwrite. It needs to be added before any other edal library in you project POM file.

```
    <repositories>
        <!-- AIMS ks maven repository on GitHub -->
        <repository>
            <id>aims-ks.mvn-repo</id>
            <name>AIMS Knowledge System MVN Repo</name>
            <url>https://raw.githubusercontent.com/aims-ks/mvn-repo/master/</url>
        </repository>

        <repository>
            <id>edu-ucar-snapshots-repo</id>
            <name>UCAR snapshots repo</name>
            <url>https://artifacts.unidata.ucar.edu/content/repositories/unidata-snapshots/</url>
        </repository>
    </repositories>

    <dependencies>
        <dependency>
            <groupId>uk.ac.rdg.resc</groupId>
            <artifactId>edal-common_fix-mem-leak</artifactId>
            <version>1.2.4</version>
            <type>jar</type>
        </dependency>
        ...
    </dependencies>
```
