# Simple Flask App with Docker

A step-by-step guide to creating a Flask web application and containerizing it with Docker.

## Table of Contents

- [Introduction](#introduction)
- [Prerequisites](#prerequisites)
- [Getting Started With Flask](#getting-started-with-flask)
  - [Clone the Repository](#clone-the-repository)
  - [Install Dependencies](#install-dependencies)
  - [Understanding the Flask Application](#understanding-the-flask-application)
  - [Run the Flask Application](#run-the-flask-application)
- [Containerization with Docker](#containerization-with-docker)
  - [Create a Dockerfile](#create-a-dockerfile)
  - [Build a Docker Image](#build-a-docker-image)
  - [Create a Docker Container](#create-a-docker-container)
- [Testing the Container](#testing-the-container)
- [Contributing](#contributing)
- [License](#license)

## Introduction

This repository provides a step-by-step guide to creating a simple Flask web application and containerizing it using Docker. It covers the entire process, from setting up the Flask app to building and running the Docker container.

## Prerequisites

Before you begin, make sure you have the following prerequisites installed:

- [Python](https://www.python.org/downloads/)
- [Docker](https://docs.docker.com/get-docker/)

## Getting Started With Flask

### Clone the Repository

Clone this repository to your local machine:

```bash
git clone https://github.com/chesah_kalu/Simple-Flask-App-Docker.git
```

### Install Dependencies

To install dependencies and modules required for the flask app work, run the command bellow to install the dependencies listed inside the ```requirements.txt``` file

```bash
pip3 install -r requirements.txt
```

### Understanding the Flask Application

Before running the Flask application, let's briefly understand the code in `product_list_app.py`. The Flask application provides a REST API for managing a list of products. It allows you to perform CRUD (Create, Retrieve, Update, Delete) operations on the product data.

#### API Endpoints

The Flask application exposes the following API endpoints:

- `GET /products`: Retrieves all products.
- `GET /products/<id>`: Retrieves a specific product by ID.
- `POST /products`: Creates a new product.
- `PUT /products/<id>`: Updates an existing product by ID.
- `DELETE /products/<id>`: Deletes a product by ID.

#### Application Logic

Here's a high-level overview of how the Flask application works:

- **GET /products**: When you access this endpoint, the application returns a JSON representation of all the products in the `products` list.

- **GET /products/<id>**: This endpoint allows you to retrieve a specific product by providing its ID as a parameter in the URL. If the product with the given ID exists, it is returned as JSON. Otherwise, an error message is returned.

- **POST /products**: To create a new product, you need to send a POST request to this endpoint with a JSON request body containing the `name` and `price` of the product. If the request is valid, the new product is added to the `products` list and returned as JSON with a 201 status code (created).

- **PUT /products/<id>**: To update an existing product, send a PUT request to this endpoint with the product's ID as a parameter in the URL and a JSON request body containing the updated `name` and `price` values. If a product with the provided ID is found, it is updated with the new values and returned as JSON with a 200 status code (OK).

- **DELETE /products/<id>**: To delete a product, send a DELETE request to this endpoint with the product's ID as a parameter in the URL. If a product with the provided ID is found, it is removed from the `products` list, and a success message is returned with a 200 status code (OK).

#### Code Comments

The code in `product_list_app.py` is well-commented, providing detailed explanations of how each endpoint and piece of logic works. You can refer to these comments for a more in-depth understanding of the application's inner workings.

This summary should help you get started with understanding the Flask application and its API endpoints.

### Run the Flask Application

Start the Flask application:

```bash
python3 product_list_app.py
```

The application will be accessible at http://localhost:5070.

