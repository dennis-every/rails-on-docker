<a name="readme-top"></a>

<div align="center">

# Dockerizing a Ruby on Rails Application

  <br>
</div>

<!-- TABLE OF CONTENTS -->

## 📗 Table of Contents

- [📗 Table of Contents](#-table-of-contents)
- [📖 About this project ](#-about-project-)
  - [🛠 Built With ](#-built-with-)
    - [Tech Stack ](#tech-stack-)
    - [Key Features ](#key-features-)
  - [🚀 Live Demo ](#-live-demo-)
  - [💻 Getting Started ](#-getting-started-)
    - [Setup](#setup)
    - [Install](#install)
    - [Usage](#usage)
    - [Build steps](#steps)
  - [👥 Author ](#-author-)
  - [📝 License ](#-license-)

<br>
<!-- PROJECT DESCRIPTION -->

# 📖 Dockerizing a Ruby on Rails application <a name="about-project"></a>

This is a demo application to show how to use Docker to containize a Ruby on Rails application.

<br>

## 🛠 Built With <a name="built-with"></a>

<br>

### Tech Stack <a name="tech-stack"></a>

<details>
  <summary>Client</summary>
  <ul>
    <li>Ruby on Rails</li>
    <li>PostgreSql</li>
    <li>Docker</li>
  </ul>
</details>

<details>
  <summary>Server</summary>
  <ul>
    <li>Puma</li>
  </ul>
</details>

<details>
<summary>Database</summary>
  <ul>
    <li>PostgreSql</li>
  </ul>
</details>

<br>
<!-- Features -->

### Key Features <a name="key-features"></a>

- **Use Docker to containerize a Ruby on Rails application**

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- LIVE DEMO -->

## 🚀 Live Demo <a name="live-demo"></a>

- [Docker on Rails](https://dennis-every.github.io/docker-on-rails)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- GETTING STARTED -->

## 💻 Getting Started <a name="getting-started"></a>

<br>

### Setup

- git clone git@github.com:dennis-every/rails-on-docker.git
- cd rails-on-docker

<br>

### Install

- Install Docker from docker.com

<br>

### Usage

- docker compose up

<p align="right">(<a href="#readme-top">back to top</a>)</p>


### Build steps


- Create Dockerfile (refer to the file in repo)
- Create a Gemfile with rails version (refer to the file in repo)
- Create an empty Gemfile.lock
- Create an entrypoint.sh script to fix a Rails-specific issue that prevents the server from restarting when a certain server.pid file pre-exists. This script will be executed every time the container gets started (refer to this file in repo)
- Create a docker-compose.yml file (refer to the file in repo)
- Generate the rails app: docker compose run --no-deps web rails new . --force --database=postgresql
- docker compose build
- Update database.yml (refer to the file in repo)
- Boot the app with: docker compose up
- Create the database in another terminal, run: docker compose run web rake db:create
- Go to http://localhost:3000 on a web browser to see the Rails welcome page
- To stop the application, run docker compose down

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- AUTHOR -->

## 👥 Author <a name="author"></a>

👤 **Dennis Every**

- GitHub: [@dennis-every](https://github.com/dennis-every)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- LICENSE -->

## 📝 License <a name="license"></a>

This project is [MIT](./MIT.md) licensed

<p align="right">(<a href="#readme-top">back to top</a>)</p>
