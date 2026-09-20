Python/FastAPI AI microservice goes here.

This folder will contain the FitFlow AI orchestration service, built with Python and FastAPI, as recommended in Lab 5, Activity 4.

Planned structure:
- app/models/        — recommendation model (adaptive workout plans), cloud computer-vision model (meal recognition)
- app/api/           — FastAPI routes called by the Node.js backend
- app/tflite/        — on-device TensorFlow Lite model assets shared with the mobile app

Setup (once code is added):
    pip install -r requirements.txt
    uvicorn main:app --reload
