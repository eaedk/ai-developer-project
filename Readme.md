# Devices Price Classification System

## Project Overview

This project, **Devices Price Classification System**, utilizes Python and Spring Boot to build an AI-driven system for classifying device prices based on their specifications. It comprises two main components:

1. **Python Project**: This part focuses on machine learning techniques to predict and classify device prices.
2. **Spring Boot Project**: This part provides RESTful API endpoints to interact with the machine learning model and manage device information.

## Python Project

### Machine Learning Report

A detailed summary of the machine learning process can be found in the [Colab Notebook](https://colab.research.google.com/github/eaedk/ai-developer-project-python/blob/main/ML_Step_By_Step_AI_Developer.ipynb). Here are the key highlights:

- **Best Model**: Linear Regression achieved the best result.
- **Optimal Parameters**:
  - `classifier__C`: 200
  - `classifier__max_iter`: 300
  - `preprocessor__numerical__num_imputer__strategy`: 'mean'
- **Dataset Split**: 80% of the training dataset was used for training the model.
- **Performance Metrics**:
  - Accuracy: 97.75%
  - F1-score: 0.977

### Python ML API

For the Python API, Flask was utilized for creation, and Docker was used for deployment on Hugging Face.

## Spring Boot Project

### Endpoints

- **GET /api/devices/**: Retrieve a list of all devices.
- **GET /api/devices/{id}**: Retrieve details of a specific device by ID.
- **POST /api/devices**: Add a new device.
- **POST /api/predict/{deviceId}**:
  - Predict the price for a device based on its specifications.
  - Call the Python API to predict the price and save the result in the device entity.
  - Apply best practices like transaction management.

### Data Storage

For data storage, MongoDB was chosen due to its flexibility, scalability, and document-oriented structure, which align well with the project's requirements. An online MongoDB cluster was preferred for its accessibility, scalability options, built-in monitoring tools, and convenience. While an online MongoDB cluster is currently being used, this choice may be subject to change to resolve any configuration issues that may arise during development. Flexibility in database selection ensures that the project can adapt to evolving requirements and technical challenges as they arise.

## Repository Status

- **Python Part**: Completed and deployed on Hugging Face. [Python Repository Link](https://github.com/eaedk/ai-developer-project-python). [Python Prediction API Deployed](https://huggingface.co/spaces/eaedk/DevicesPricePredictionAPI)
- **Spring Boot Part**: Under development. Will be completed soon. [Spring Boot Repository Link](https://github.com/eaedk/ai-developer-project-spring-boot)

## Contributions

Contributions to enhance the project are welcome. Kindly submit pull requests with detailed descriptions of the changes.

## License

This project is licensed under the [MIT License](LICENSE).

---

Feel free to reach out for any further clarifications or assistance! [LinkedIn](https://www.linkedin.com/in/esa%C3%AFe-alain-emmanuel-dina-koupoh-7b974a17a/)
