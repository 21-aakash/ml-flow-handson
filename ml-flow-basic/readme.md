

# MLflow Quickstart Guide

> A concise guide to the most essential core APIs and workflow of MLflow Tracking.

---

## What is MLflow?

MLflow is an open-source platform designed to manage the complete machine learning lifecycle, including experimentation, reproducibility, deployment, and a central model registry. It helps individuals and teams:
- Track experiments to record and compare parameters and results
- Package ML code in a reusable, reproducible form
- Deploy models to various serving environments
- Manage and share models using a central registry

**Key Features:**
- Language-agnostic (Python, R, Java, REST API)
- Integrates with many ML libraries (scikit-learn, TensorFlow, PyTorch, etc.)
- Simple, extensible API

---

## Core MLflow Workflow

### 1. Install MLflow
```bash
pip install mlflow
```

### 2. Start a Local MLflow Tracking Server
```bash
mlflow server --host 127.0.0.1 --port 8080
```

---

## Essential MLflow Operations

| Step | Operation                  | MLflow Function/Method           |
|------|----------------------------|----------------------------------|
| 1    | Set Tracking URI           | `mlflow.set_tracking_uri()`      |
| 2    | Set Experiment             | `mlflow.set_experiment()`        |
| 3    | Start Run                  | `mlflow.start_run()`             |
| 3.1  | Log Parameters             | `mlflow.log_params()`            |
| 3.2  | Log Metrics                | `mlflow.log_metric()`            |
| 3.3  | Infer Model Signature      | `infer_signature()`              |
| 3.4  | Log and Register Model     | `mlflow.sklearn.log_model()`     |
| 3.5  | Set Model Tags             | `mlflow.set_logged_model_tags()` |
| 4    | Load Model for Inference   | `mlflow.pyfunc.load_model()`     |

---

## Typical MLflow Usage Flow

1. **Set the tracking server URI** to specify where runs are logged.
2. **Create or select an experiment** to organize runs.
3. **Start a run** to log parameters, metrics, and artifacts.
4. **Log model parameters and metrics** (e.g., accuracy, hyperparameters).
5. **Infer and log the model signature** for input/output schema.
6. **Log and register the trained model** for versioning and deployment.
7. **Set tags** for easier model management and search.
8. **Load the model** for inference or deployment.

---

## References
- [MLflow Documentation](https://mlflow.org/docs/latest/index.html)
- [MLflow GitHub](https://github.com/mlflow/mlflow)
- [MLflow Quickstart Tutorial](https://mlflow.org/docs/latest/quickstart.html)

