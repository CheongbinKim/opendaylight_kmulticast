# OpenDaylight OSGi bundle Sample project

use Netbeans

File->New Project->Maven->OSGi Bundle

Group Id : kr.ac.konkuk.cclab

Version : 1.0-SNAPSHOT

Package : kr.ac.konkuk.cclab.kmulticast

or

use archetype


    $ mvn archetype:generate -DarchetypeGroupId=org.apache.karaf.archetypes -DarchetypeArtifactId=karaf-bundle-archetype


# Edit POM.xml

* Add dependency

      <dependencies>

      <dependency>

        <groupId>org.opendaylight.controller</groupId>
            
        <artifactId>sal</artifactId>

        <version>0.7.0</version>

      </dependency>

      </dependencies>
      
* Add repository

      <repositories>
      <!-- OpenDaylight releases -->
      <repository>
              <id>opendaylight-mirror</id>
              <name>opendaylight-mirror</name>
              <url>http://nexus.opendaylight.org/content/groups/public/</url>
              <snapshots>
                  <enabled>false</enabled>
              </snapshots>
              <releases>
                  <enabled>true</enabled>
                  <updatePolicy>never</updatePolicy>
              </releases>
          </repository>
          <!-- OpenDaylight snapshots -->
          <repository>
              <id>opendaylight-snapshot</id>
              <name>opendaylight-snapshot</name>
              <url>http://nexus.opendaylight.org/content/repositories/opendaylight.snapshot/</url>
              <snapshots>
                  <enabled>true</enabled>
              </snapshots>
              <releases>
                  <enabled>false</enabled>
              </releases>
          </repository>
      </repositories>
      
* Edit Activator and configureInstance()
소스참고 
