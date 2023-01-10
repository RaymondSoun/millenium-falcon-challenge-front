# Millenium Falcon Challenge

The Death Star - the Empire's ultimate weapon - is almost operational and is currently approaching the Endor planet. The countdown has started.

Han Solo, Chewbacca, Leia and C3PO are currently on Tatooine boarding on the Millennium Falcon. They must reach Endor to join the Rebel fleet and destroy the Death Star before it annihilates the planet.

The Empire has hired the best bounty hunters in the galaxy to capture the Millennium Falcon and stop it from joining the rebel fleet...


# Prerequisites
*In this tutorial, we will suppose that node 16 or above is installed on your machine, if not follow the links below:*
*https://nodejs.org/en/download/*

*We will also suppose that you installed the backend project and the server is running, if not please refer to [this tutorial](https://github.com/RaymondSoun/millenium-falcon-challenge)*

# Installing the package
## Install with docker
Run the following commands to install the frontend project with Docker:

```
$ docker pull raymond93/millenium-falcon-challenge-front
```

```
$ docker run -p 3000:3000 raymond93/millenium-falcon-challenge-front
```

You should now be able to access the link [http://localhost:3000](http://localhost:3000) and use the app.

## Install with npm

Create a new folder for the front end project

```
$ mkdir <path/to/project>
```

```
$ cd <path/to/project>
```

Initialize git and clone the project

```
$ git init
```

```
$ git clone https://github.com/RaymondSoun/millenium-falcon-challenge-front.git
```

Install the dependencies with the following command:

```
$ npm install
```

Compile and minify

```
$ npm run build
```

Launch the app:
```
$ serve -s dist
```

You can now access the interface on [http://localhost:3000](http://localhost:3000)