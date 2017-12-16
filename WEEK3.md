Url to your Jenkins instance:
http://ec2-35-177-160-67.eu-west-2.compute.amazonaws.com:8080

Url to your live TicTacToe instance:
http://ec2-35-176-231-110.eu-west-2.compute.amazonaws.com:8080/

Datadog URL:
https://p.datadoghq.com/sb/ef1a64b35-4c910d4338

List of things you finished / did not finish (with comments):
* Completed the migrations needed for the application to work
  * I created a new db-migrate file using db-migrate, and then added in up and down, addcolumn and removecolumn
* On Git push Jenkins pulls my code and the Tic Tac Toe application is deployed through a build pipeline, but only if all my tests are successful
  * This works
* Filled out the Assignments: for the API and Load tests
  * The answers are found in the apitest folder and are named Assignment.md and on Jenkins in the pipeline on the bottom is a link "Latest test results"
* The API and Load test run in my build pipeline on Jenkins and everything is cleaned up afterwards  
  * This works
* My test reports are published in Jenkins
  * This Works
* My Tic Tac Toe game works, two people can play a game till the end and be notified who won.
  * TODO: Tell who won.
* My TicCell is tested
  * TODO: Very few tests.
* I've set up Datadog
  * This Works
