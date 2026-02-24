# California-Housing-Price-Predictor
Deploying Machine Learning model using Scikit-learn with Docker

## Project Overview
This project demonstrates how to:

- Train a Machine Learning regression model
- Serve it via a REST API using FastAPI
- Containerize the application using Docker
- 
## Project Structure

```
ml-model-docker-deployment/
│
├── app/                 # API layer
│   └── main.py          # FastAPI application
│
├── model/               # Model training logic
│   └── model.py         # Model training script
│
├── requirements.txt     # Python dependencies
├── Dockerfile           # Container configuration
├── .dockerignore        # Files excluded from Docker build
└── README.md            # Project documentation
```

##  Running the Project Locally

###  Create Virtual Environment

python3 -m venv venv  
source venv/bin/activate  

###  Install the Dependencies

pip install -r requirements.txt  

###  Train the Model
python model.py  

### Start API

uvicorn app.main:app --reload  

Visit:
http://localhost:8000/docs

## Containerize with Docker

### Build Image

docker build -t ml-model-app .

### Run Container

docker run -p 8000:8000 ml-model-app
![WhatsApp Image 2026-02-22 at 00 18 04](https://github.com/user-attachments/assets/7c77c895-5518-425c-95c8-65ab6d3b7327)


open your browser and navigate to http://localhost:8081/docs. 

![WhatsApp Image 2026-02-22 at 00 18 46](https://github.com/user-attachments/assets/6e783dce-6397-437f-84cf-57d46a120526)


![WhatsApp Image 2026-02-22 at 00 19 26](https://github.com/user-attachments/assets/e34634a5-9143-4766-b4d2-915470b74050)



---
