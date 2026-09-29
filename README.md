# 🌦️ RAHMB: Regime-Aware Hybrid Multi-Model Blending

**Dynamic AI-NWP Blending Engine for Impact-Based Weather Advisories**

[![Smart India Hackathon 2026](https://img.shields.io/badge/SIH_2026-Problem_SIH26081-orange.svg)](#)
[![Python 3.10+](https://img.shields.io/badge/python-3.10+-blue.svg)](https://www.python.org/downloads/)
[![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?logo=pytorch&logoColor=white)](#)
[![Xarray](https://img.shields.io/badge/Xarray-Processing-lightgrey)](#)

> **Team:** Runtime Rebels
> **Problem Statement:** SIH26081 - Hybrid AI–NWP Multi-Model Forecast Blending System
> **Organization:** Ministry of Earth Sciences (MoES)

---

## 📖 Project Overview
Conflicting weather models produce generalized, uncertain forecasts that hinder safe and timely decision-making. **RAHMB** solves this by utilizing a software-defined, AI-driven engine that dynamically weights multi-model forecasts. By ingesting both physics-based NWP models (ECMWF, GFS) and data-driven AI models (GraphCast, Pangu-Weather), RAHMB outputs a single, high-confidence consensus forecast with probabilistic confidence levels.

## ✨ Key Innovations
*   🧠 **Continuous Self-Learning:** AI dynamically updates model trust weights based on historical accuracy and recent verification.
*   🌪️ **Regime-Aware Blending:** Shifts strategies automatically for localized extreme events like monsoons, heatwaves, and cyclones.
*   📊 **Probabilistic Confidence:** Exposes forecast uncertainty using Conformal Prediction rather than hiding it behind simple averages.
*   🔍 **Explainable AI (XAI):** Provides SHAP/Attention visual maps so meteorologists can see *why* the engine trusted specific models.

---

## 🏗️ System Architecture

Our solution follows a 6-phase pipeline to transform raw, conflicting data into actionable intelligence:

1. **Data Acquisition:** Ingests ground observations, satellite/radar data, and historical ERA5 reanalysis.
2. **Forecast Generation:** Concurrently runs NWP (ECMWF, GFS, WRF) and AI Foundation Models (GraphCast, FourCastNet).
3. **Harmonization:** Uses Xarray/Dask for spatiotemporal alignment, creating a multi-dimensional **Unified Forecast Tensor**.
4. **Forecast Intelligence Layer:** CNN+LSTM models extract context (Weather Regime, Disagreement, Extreme Events, Stability).
5. **Adaptive MoE Blending:** A Transformer-based Mixture-of-Experts (MoE) network calculates dynamic Softmax weights and mathematically fuses the forecasts.
6. **Delivery:** Outputs deterministic metrics, uncertainty quantifications, and explainable AI maps via a Fast API backend to a web dashboard.

---

## 💻 Tech Stack

### AI & Core Engine
*   **Deep Learning:** PyTorch, TensorFlow
*   **Architectures:** Transformers (MoE, Self-Attention), GNNs, CNN+LSTM
*   **Explainability:** SHAP

### Spatial Data Processing
*   **Libraries:** Xarray, Dask, NumPy, Pandas
*   **Data Formats:** NetCDF, GRIB

### Backend & Delivery
*   **API Framework:** FastAPI
*   **Dashboard Frontend:** React.js / Next.js
*   **Deployment:** Docker, Uvicorn

---

## 🚀 Getting Started

### Prerequisites
* Python 3.10 or higher
* [Conda](https://docs.conda.io/en/latest/) (Recommended for managing geospatial libraries)

### Installation

1. **Clone the repository**
   ```bash
   git clone [https://github.com/YourUsername/RAHMB-SIH2026.git](https://github.com/YourUsername/RAHMB-SIH2026.git)
   cd RAHMB-SIH2026
