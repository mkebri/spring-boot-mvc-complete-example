Spring Maven Java 1.8
=======================

[![Coverage Status](https://coveralls.io/repos/cristianprofile/spring-boot-mvc-complete-example/badge.svg)](https://coveralls.io/r/cristianprofile/spring-boot-mvc-complete-example)  [![Build Status](https://travis-ci.org/cristianprofile/spring-boot-mvc-complete-example.svg?branch=develop)](https://travis-ci.org/cristianprofile/spring-boot-mvc-complete-example)
[![Gitter](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/cristianprofile/spring-boot-mvc-complete-example?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge)

NEW SPRING BOOT MVC APP CREATED, ENJOY IT (web module, rest module and spring data rest example)

**Important!!!!! First of all you have to install with "mvn install" modules "mylab-parent-pom" and after "mvn install" of module "mylab-core".**

run spring-boot-mvc-web-example module with maven  "mvn spring-boot:run" and access to http://localhost:9090/pizza
and user: "admin@ole.com" and password "admin@ole.com".You can create other users with ROLE_USER at add user left menu
option.

- Spring boot MVC with Spring Security Access
- I18n
- Responsive Bootstrap css witn Tiles 3
- Password encoding with Bcrypt  [BCRYPT password encoding](http://www.baeldung.com/spring-security-registration-password-encoding-bcrypt "BCRYPT password encoding") 
- Unit Testing and Integration Testing with spring-boot-starter-test dependency (all dependecies are transitive like mockito junit etc...)


------------------------------------------------------------------------------------------------------

If you want to access to Rest Service with Spring boot module "spring-boot-mvc" first run mvn spring-boot:run:

- http://localhost:9090/base (get list of all bases)
- http://localhost:9090/base/1 (get base info with id=1)
- http://localhost:9090/base/1 (delete base info with id=1)
- http://localhost:9090/base (post create new base sending json info. Example "name":"rolling pizza" )
- http://localhost:9090/base (update update existing base sending json info. Example {"name":"rolling pizza 2","id":1})

When you run Spring boot app Spring actuator add features to monitore your services:

- (get) http://localhost:9091/manage/metrics (Spring Boot Actuator includes a metrics service with 
“gauge” and “counter” support. A “gauge” records a single value; and a “counter” records a delta 
(an increment or decrement). Metrics for all HTTP requests are automatically 
recorded, so if you hit the metrics endpoint should see a sensible response.)
- (get) http://localhost:9091/manage/health (you can check if your app is available)
- (get) http://localhost:9091/manage/mappings (list of your app HTTP endpoints)
- (post) http://localhost:9091/manage/shutdown (list of your app HTTP endpoints)

![Spring Actuator values](/images/Spring_Actuator_EndPoints.png?raw=true "Spring Actuator values")


More info about Spring Actuator at: [Spring Actuator](https://github.com/spring-projects/spring-boot/tree/master/spring-boot-actuator "Spring Actuator")

-----------------------------------------------------------------------------------------------------------------------------------------------

Spring Data REST builds on top of Spring Data repositories, analyzes your application’s domain model and exposes hypermedia-driven HTTP resources for aggregates contained in the model.

If you want to access to Rest Service with Spring boot module "spring-boot-data-rest" first run mvn spring-boot:run:

- http://localhost:9090/api/bases to get all bases (get list of all bases)
- http://localhost:9090/api/bases (post create new base sending json info. Example "name":"rolling pizza" )
- http://localhost:9090/api/browser/index.html#/api to access to your rest api HAL Browser to be served up when you visit your application’s root URI in a browser. 

![Spring Actuator values](/images/SpringDataRestHalBrowser.png?raw=true "Spring Actuator values")

More info about Spring Data Rest at: [Spring Data Rest](http://projects.spring.io/spring-data-rest/ "Spring Data Rest") 











----------------------------------------------------------------------------------------------------------
Jenkins 2 automatic multibranch plugin mode with JenkinsFile file in main directory. More interesting information about new Jenkins 2 Pipeline script configuration at:

-  [DZONE refcard jenkins pipeline](https://dzone.com/refcardz/continuous-delivery-with-jenkins-workflow "DZONE refcard jenkins pipeline")
-  [Github examples](https://github.com/jenkinsci/pipeline-examples "Github examples")  

Docker integration in feature  branch called: docker_container_jenkins

-  [Docker container feature branch](https://github.com/cristianprofile/spring-boot-mvc-complete-example/blob/feature/docker_container_jenkins/Jenkinsfile "Run IC in a Docker container")  

![Pipeline plugin](/images/git-flow.png?raw=true "Pipeline plugin")

