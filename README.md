# VIX FRONTEND TEST

### Requirements
- Have [Docker](https://docs.docker.com/engine/install/) installed
- Have [docker-compose](https://docs.docker.com/compose/install/) installed
- Do not have services running on the ports (9191, 8181, 8080 and 2222)

### Test

We will provide a docker image for you, this image will have an enviroment like we have on VIX. It will have:

- GITEA - software development version control.
- Staging Environment - The application you will work on available for testing purpose.
- Drone - Continuos Integration/Continuos Delivery
- SSH - Secure Shell 

### Step by Step

In order to proced here you have to have all the requirements.

##### Clone the Repo

```bash
git clone https://github.com/vixtech/frontend-test.git
```

#### Run the docker image

Inside the project direcoty.
```bash
docker-compose up
```

#### Access all the services with your browser

- [Gitea](http://localhost:9191) (User: candidate, Password: changeit)
- [Staging enviroment](http://localhost:8181)
- [Drone](http://localhost:8080)

#### Commom problems
- drone cookie error (just clear the site data)