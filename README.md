# GitHub Repository Forecasting Platform

A full-stack time-series forecasting application that predicts GitHub repository activity using machine learning. The application combines a React frontend with a Python/Flask backend to generate interactive forecasts from historical repository metrics using Facebook Prophet.

---

## Overview

This project demonstrates the design and implementation of a full-stack machine learning application, integrating data visualization, REST APIs, and forecasting models into a single user-facing platform.

The application allows users to analyze historical GitHub repository activity and generate future trend predictions through an interactive web interface.

---

## Features

- Interactive dashboard built with React and Material UI
- Time-series forecasting using Facebook Prophet
- REST API powered by Flask
- Interactive visualization of historical and forecasted trends
- Containerized application using Docker
- Cloud-ready architecture for deployment on Google Cloud Platform
- Modular frontend and backend architecture

---

## Architecture

```
                    GitHub Repository Metrics
                               │
                               ▼
                    Data Collection Layer
                               │
                               ▼
                   Data Preprocessing Pipeline
                               │
                               ▼
                Facebook Prophet Forecast Model
                               │
                               ▼
                     Flask REST API
                               │
                               ▼
               React + Material UI Frontend
                               │
                               ▼
                            End User
```

---

## Tech Stack

### Frontend

- React
- Material UI
- JavaScript
- HTML5
- CSS3

### Backend

- Python
- Flask
- Facebook Prophet
- TensorFlow

### Infrastructure

- Docker
- Nginx
- Google Cloud Platform

---

## System Design

The application follows a layered architecture to separate user interface, application logic, and forecasting services.

### Frontend

- React single-page application
- Material UI components
- API communication through HTTP requests
- Interactive chart rendering

### Backend

- Flask REST API
- Forecast generation service
- Time-series preprocessing
- Machine learning inference

### Infrastructure

- Docker containerization
- Reverse proxy using Nginx
- Cloud-ready deployment architecture

---

## Forecasting Workflow

1. User selects a GitHub repository.
2. Historical repository metrics are retrieved.
3. Data is cleaned and prepared for forecasting.
4. Facebook Prophet generates future predictions.
5. Results are returned through the REST API.
6. Forecasts are displayed as interactive visualizations.

---

## API

### Generate Forecast

**POST**

```
/forecast
```

### Request

```json
{
  "repository": "facebook/react",
  "forecastDays": 30
}
```

### Response

```json
{
  "forecast": [
    {
      "date": "2022-08-01",
      "value": 1542
    }
  ]
}
```

---

## Project Structure

```
react-forecasting/
│
├── public/
├── src/
├── Dockerfile
├── nginx.default.conf
├── package.json
├── README.md
└── ...
```

---

## Running the Project

### Clone the repository

```bash
git clone https://github.com/vidhikakani/react-forecasting.git
```

### Install dependencies

```bash
npm install
```

### Start the React application

```bash
npm start
```

### Build for production

```bash
npm run build
```

### Docker

```bash
docker build -t react-forecasting .

docker run -p 3000:3000 react-forecasting
```

---

## Future Enhancements

- Support multiple forecasting models
- Real-time GitHub API integration
- User authentication
- Historical model comparison
- CI/CD pipeline automation
- Kubernetes deployment
- Performance monitoring and observability

---

## Engineering Concepts Demonstrated

- Full-stack application development
- Time-series forecasting
- REST API design
- Machine learning integration
- Component-based frontend architecture
- Docker containerization
- Cloud-native application design

---

## Repository

GitHub: https://github.com/vidhikakani/react-forecasting

---

## License

This project is available under the MIT License.
