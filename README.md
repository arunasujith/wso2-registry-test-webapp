wso2-registry-test-webapp
=========================

This is a sample webapp to test registry resource specific operations

1. Add a resource
2. Get a resource
3. Delete a resource

Build the application using
mvn clean install

Deploy the webapp in WSO2 Application Server

Adding resource

  curl --data "action=add&path=<resource-path>&resource=<resource-value>" -v http://localhost:9763/CarbonTest-1.0.0/RegistryTest

e.g

 curl --data "action=add&path=/foo/bar&resource=AAAAAAAAA" -v http://localhost:9763/CarbonTest-1.0.0/RegistryTest


Getting resource

  curl --data "action=get&path=<resource-path>" -v http://localhost:9763/CarbonTest-1.0.0/RegistryTest

e.g
curl --data "action=get&path=/foo/bar" -v http://localhost:9763/CarbonTest-1.0.0/RegistryTest


Deleting resource

  curl --data "action=delete&path=<resource-path>" -v http://localhost:9763/CarbonTest-1.0.0/RegistryTest

e.g

curl --data "action=delete&path=/foo/bar" -v http://localhost:9763/CarbonTest-1.0.0/RegistryTest
