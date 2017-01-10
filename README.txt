To build
mvn clean package

For a quick build without the unit testing.
mvn clean package -DskipTests=true

This will create a rally-defect-creation.hpi file in the target directory.

For development/testing/debugging 

# Set the following MAVEN_OPTS
export MAVEN_OPTS="-Xdebug -Xrunjdwp:transport=dt_socket,server=y,address=8000,suspend=n"

# Run the plugin in it's own Jenkins system with the following command.
mvn hpi:run

# If 8080 port is already used reset it with the maven option below
mvn hpi:run -Djetty.port=8090
