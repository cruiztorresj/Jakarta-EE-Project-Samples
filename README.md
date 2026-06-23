# Jakarta-EE-Project-Samples

![hello-web Jakarta EE](https://cdn.hostmora.app/calebjosue/34828440-8d97-4de3-9202-7f8eb639aca6/images/hello-web.png)

**Jakarta EE Project Samples** represented for me the opportunity to have some fun migrating the original code base in [this repository](https://github.com/RedHatTraining/JB083x-lab) to Jakarta EE 11, the linked repository is using Java EE 7 and is being run on JBoss EAP, I have opted for WildFly 40, which adds support for Jakarta EE 11 (A rebranding for Java EE). I would like to mention my initiative has nothing to do with Red Hat (The owner of the original codebase), for me it was just a way to entertain myself, since I happen to like Java. I am publishing this because there may be people looking for example Jakarta EE applications.

## Running the projects.
+ Clone this repository or download the code.
+ Change directory into your recently cloned project (Jakarta-EE-Project-Samples).
  - [x] Java 25 is installed in your machine.
  - [x] JAVA_HOME environment variable is set up.
  - [x] Maven is installed in your machine.
  - [x] M2_HOME environment cariable is set up.
  - [x] [WildFly 40](https://www.wildfly.org/downloads/) or above is installed in your machine. Choose `WildFly Distribution`.
+ Now that you are in the cloned directory you will find the `labs` folder, comprised of the following projects.
  - `todojse`, this is a CLI application, use `mvn exec:java` inside this project if you want to see it in action.
  - hello-web
  - stateless-ejb
  - persist-entity
  - create-queries
  - entity-relationships
  - hello-rest
+ Chose one of the listed projects above and switch directory into it.
+ For any given directory you have chosen to install WildFly, we will call it `WILDFLY_HOME`, run WildFly by means of executing the progran `standalone` (Chose the file extension in relation to your operating system), this program is located inside `WILDFLY_HOME/bin/`.
+ Let the above program running since you would like to check all sort of logs being print, open another tab in your console and make sure you are inside the project you want to see in action.
+ `mvn wildfly:deploy` will get you up and running.
+ visit your application using your favorite web browser at `http:localhost:8080/project-name`

Check the README files inside every project for instructions specific to that project.

## Undeploy the application.
Given you just run the project as mentioned and you are done interacting with it, use `mvn wildfly:undeploy` to undeploy the application, in the tab running WildFly, you can use `Ctrl-C` to stop the process.

## Stay tuned.
I will try to add more content in relation to the technologies being used here.
