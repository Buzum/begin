### Requirements

1. Create a REST API using Javascript, Python or Go, the api must:
    * Must have 1 GET endpoint `/user` that returns a random user using this api https://randomuser.me/.
    Output format should be: 
    `<title> <firstname> <lastname> lives at <street-address> in <city>, <state>, <country>. Has logged in with username <username>.` 
    * Must have at least 1 unit test 
2. Containerize the API that you just built with any containerization technology (e.g, Docker)
3. Create a CI/CD pipeline using github actions, connected to this repo. The pipeline must:  
    - Must perform some sort of linting or formatting
    - Must run the tests, collect code coverage and fail the build if code coverage is below 80%
    - Must build the containerized app
    - Must fail the pipeline if any of the steps above fail 
 
<b>Optional</b>:
* Create a CLI based off of the API built earlier.
* Create a Github Release when the version of the code gets increase.
  The code should have some sort of way to track its version, so when that increases, the pipeline should trigger a Github Release.
  * Do not create a release for every merge, just the increase of version

#### Additional Info
* Perform all work on a feature branch and when done, create a PR against the main branch
* Update the readme with any steps on how to run/build the application 


### HOW TO

* Application will be automaticly deployed on dockerhub if all github actions will be successfully finished, after pushes or PR in master branch.
* For run this application u will need in docker on your machine. If you haven't it, https://docs.docker.com/engine/install/ will help your. Just choose your OS, download and install docker. 
* Open your CLI and  write ` docker run -p 4444:5000 keton/pytestapi `. 
* Wait a minute
* Open your browser and write in addrespage `localhost:4444/user`
* Done!