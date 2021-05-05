# VIX FRONTEND TEST

### Requirements
- Have an account on [Docker Hub](https://hub.docker.com/)
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

In order to proceed here you have to have all the [requirements](https://github.com/vixtech/frontend-test#requirements).

##### Clone the Repo

```bash
git clone https://github.com/vixtech/frontend-test.git
```

#### Run the docker image

Inside the project directory.
```bash
docker-compose up
```

#### Access all the services with your browser

- [Gitea](http://localhost:9191) (User: candidate, Password: changeit)
- [Staging enviroment](http://localhost:8181)
- [Drone](http://localhost:8080)


#### After you solve the test

Commit the available container by just executing this command:

**Change the** `change-here-for-your-docker-hub-username` **for your docker-hub username**

```bash
docker commit $(docker ps | grep frontend-test | awk '{print $1}') change-here-for-your-docker-hub-username/frontend-test
```

Then make a docker login:

```bash
docker login
```

Then push the image.

**Change the** `change-here-for-your-docker-hub-username` **for your docker-hub username**

```bash
docker push change-here-for-your-docker-hub-username/frontend-test
```

Send us back the name of your image, like:

```
change-here-for-your-docker-hub-username/frontend-test
```

#### Commom problems
- drone cookie error (just clear the site data)
