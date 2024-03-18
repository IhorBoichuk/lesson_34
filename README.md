# Overview 
This project is a Flask-based web application that serves as a backend for managing customer data and performing object detection using the YOLO (You Only Look Once) model. It allows users to create, read, update, and delete customer information, as well as perform object detection on images using YOLO.  

# Deployment Info  
The application can be deployed using a WSGI server such as Gunicorn or uWSGI in a production environment.  

# Installation Instructions  
To run the application locally or in a development environment, follow these steps:  

# Clone this repository.  
Install the required dependencies listed in requirements.txt by running:  
pip install -r requirements.txt  
python app.py  


# Modeling Info 
The project utilizes the Ultralytics YOLO model for object detection. This model is pre-trained on a large dataset and capable of detecting various objects in images. 

# Interface Description  
Endpoints/Event Handlers:  
GET /  - Returns a simple "Hello World" message.  
GET /customer/<customer_id>  - Retrieves information about a specific customer identified by customer_id. If customer_id is not provided, returns information about all customers.  
POST /customer  - Creates a new customer based on the provided JSON data in the request body. Expects JSON fields for customer details such as name, gender, birth_date, and description.  
POST /customer/<customer_id>  - Updates the customer information for the specified customer_id based on the provided JSON data in the request body. Expects JSON fields similar to the creation endpoint.  
PUT /customer/<customer_id>  - Similar to the POST method, this endpoint updates the customer information. However, it expects a complete set of data for the customer.  
DELETE /customer/<customer_id>  - Deletes the customer with the specified customer_id.  
POST /ml/get_yolo_objects  - Performs object detection on an uploaded image using YOLO. Expects an image file uploaded as part of the request.  
# Functionality:  
GET /customer  - Retrieve customer information.  
POST /customer  - Create a new customer.  
POST /customer/<customer_id>  - Update customer information.  
PUT /customer/<customer_id>  - Update customer information (full update).  
DELETE /customer/<customer_id>  - Remove a customer.  
POST /ml/get_yolo_objects  - Perform object detection on an image.  



