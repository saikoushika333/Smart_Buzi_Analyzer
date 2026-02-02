# System Design – Smart Business Feasibility AI

## 1. Architecture Overview
The system follows a modular and scalable architecture where each component performs a dedicated role. The design ensures flexibility, explainability, and easy integration with external platforms.

## 2. High-Level Components
1. Web Application (Frontend)
2. n8n Workflow Engine
3. Machine Learning API
4. Large Language Model (Gemini)
5. Dataset Storage

## 3. Workflow Description
1. User submits business details through the web application
2. Request is sent to n8n via webhook
3. Input data is validated and formatted
4. n8n calls the ML Prediction API
5. ML model predicts feasibility, risk, and success probability
6. Gemini LLM converts numerical output into human-readable insights
7. Final response is sent back to the web application

## 4. Machine Learning Design
- Supervised learning model trained on historical business datasets
- Features include location coordinates, area size, competitor data, and profit estimates
- Model outputs probability scores instead of binary decisions
- Scalable API-based inference

## 5. API Design
- REST-based API using FastAPI
- JSON request-response format
- Secured using API key authentication
- Deployed locally and exposed using Ngrok

## 6. Automation Design (n8n)
- Webhooke