<a id="readme-top"></a>

<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/jluisalias/users-api">
    <img src="assets/logo.png" alt="Logo" width="150" height="150">
  </a>

<h3 align="center">The API Test</h3>

  <p align="center">
    Draft project to practice the principal techniques and technologies involved in the microservices development.
    <br />
    <a href="https://github.com/jluisalias/theapitest-crm"><strong>Explore the docs »</strong></a>
    <br />
  </p>
</div>

<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#contact">Contact</a></li>
  </ol>
</details>

## About The Project

I set out to create this project to practice some cutting-edge techniques in the world of distributed architectures (DDD, microservices), as well as other more general ones related to the framework (Spring Security, Spring AOP...), and others from software development in general (Clean Code, SOLID, Patterns...).

The definition provided for this project is:

The goal here is to build a REST API that helps manage customer data for a small shop. This API will serve as the backend for a CRM interface that another team is working on. As the lead developer on this backend project, you’ll be responsible for designing and building the API. Below are the key requirements we’ll need to meet:
- The API should be only accessible by a registered user by providing an authentication mechanism.
- A user can only:
  - List all customers in the database.
  - Get full customer information, including a photo URL.
  - Create a new customer:
    - A customer should have at least name, surname, id and a photo field.
    - Name, surname and id are required fields. 
    - Image uploads should be able to be managed. 
    - The customer should have a reference to the user who created it. 
  - Update an existing customer.
    - The customer should hold a reference to the last user who modified it.
  - Delete an existing customer.
- An admin can also:
  - Manage users:
  - Create users.
  - Delete users.
  - Update users.
  - List users.
  - Change admin status.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

### Built With

[![Springboot][Springboot]][Springboot-url]
[![Docker][Docker]][Docker-url]
[![AWS S3][AWSS3]][AWSS3-url]

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Getting Started

### Requirements

1. The only requirement to install and execute this API is to have Docker and Docker Compose installed in the environment where it's going to be executed. 
To use it is useful to have Postman (or another similar software).

### Installation

1. Clone the repo
   ```sh
   git clone https://github.com/jluisalias/theapitest-crm.git
   ```
2. Go to the root folder, and open ```docker-compose.yml``` file, you will see:
   ```
   AWS_ACCESS_KEY: 'XXXXXXXXXXXXXXXXXXXXXXXXXX'
   AWS_SECRET_KEY: 'XXXXXXXXXXXXXXXXXXXXXXXXXX'
   AWS_REGION: 'eu-north-1'
   AWS_BUCKET_NAME: 'mycustomersapibucket'
   ```
   You could either asks this repo owner to add your IAM account to the bucket list of accepted users, or configure your own bucket to accept calls from your account, 
and then set here its properties and your credentials.
<p></p>

3. Open a terminal, go to /crmservice, and run:
```.gradlew build```
It is expected to throw an exception with a test, but it will create the .jar file correctly.

4. Still in the terminal, go to the root folder, and execute:

``` docker-compose up```

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Usage
A Postman collection of usecases can be found in the project under the /assets folder, you can import it to your Postman and test the calls.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- CONTACT -->
## Contact

José Luis Alías - [@joseLalias](https://twitter.com/joseLalias) - jluis.alias@gmail.com

Project Link: [https://github.com/jluisalias/users-api](https://github.com/jluisalias/users-api)

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- MARKDOWN LINKS & IMAGES -->
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/jluisalias
[logo]: assets/logo.png
[AWSS3]: https://img.shields.io/badge/aws_s3-569A31?style=for-the-badge&logo=amazons3&logoColor=white
[AWSS3-url]: https://aws.amazon.com/s3/
[Docker]: https://img.shields.io/badge/docker-0db7ed?style=for-the-badge&logo=docker&logoColor=white
[Docker-url]: https://www.docker.com/
[Springboot]: https://img.shields.io/badge/springboot-6db33f?style=for-the-badge&logo=springboot&logoColor=white
[Springboot-url]: https://spring.io/projects/spring-boot