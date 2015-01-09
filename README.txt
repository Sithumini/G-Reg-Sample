CustomTagServiceHandler Sample
-----------------------------
Introduction
============
The idea of this sample is to apply namespace as a Tag while creating the service .

Steps
-----
1. Copy the 'org.wso2.carbon.registry.samples.handler-5.0.0-SNAPSHOT.jar' into
	GREG_HOME/repository/components/dropins.

   You also can upload handlers through the administration console by visiting the Extensions --> Add menu.

2. Edit the registry.xml file which is in 'GREG_HOME/repository/conf' folder with the following xml snippet.

    	<handler class="org.wso2.carbon.registry.samples.handler.CustomTagServiceHandler">
        	<filter class="org.wso2.carbon.registry.core.jdbc.handlers.filters.MediaTypeMatcher">
           		 <property name="mediaType">application/vnd.wso2-service+xml</property>
       		</filter>
    	</handler>

   You also can add the handler configuration through the administration console by opening the
   'Handlers' configuration (Extensions --> Configure --> Handlers) menu and clicking on 'Add New Handler'.

3. Start the server.

4. Go to admin console.

5. Browse the resources tree and add a new resource by visiting Resources --> Browse menue.

6. Select the 'Upload content from file' from from the drop down list.

7. Select your project proposal and type the media type as 'pp' (you can use whatever the media type you prefer).

	Note:- Sample project proposals are available in "GREG_HOME/samples/handler/src/resources" folder.

8. And 'Add' it.

9. Browse to the added project proposal. You could see the Properties and the Tag have been added to the resource.
