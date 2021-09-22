# ps-spring-boot-and-angular

1 - Create Folder WEB-INF inside src angular folder and add web.xml with below code :

<web-app>
  <welcome-file-list>    
   <welcome-file>index.html</welcome-file>
  </welcome-file-list>
  <error-page>
    <error-code>404</error-code>
    <location>/index.html</location>
  </error-page>
</web-app>
2 - Modify angular.json search on "assets" and add "src/WEB-INF" as below :

  "assets": [
              "src/favicon.ico",
              "src/assets",
              "src/WEB-INF"
            ],
3 - Build angular project with this command :

ng build --prod

4 - Modify <base href="/"> in index.html after build it in dist/index.html to be <base href="./">

5 - Restart Tomcat Server
