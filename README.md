# Machine-Learning-Project

---

## Overview

This repository contains code for a machine learning pipeline, including data ingestion, data transformation, and model training. The code is organized into modular components to facilitate flexibility and maintainability.

## Directory Structure

- **artifacts**: Directory to store output files, such as trained models and processed data.
- **notebook**: Contains sample datasets and Jupyter notebooks for exploration.
- **src**: Source code for the machine learning pipeline.
  - **components**: Modules for different components of the pipeline (data transformation, model training, etc.).
  - **exception.py**: Definition of custom exceptions.
  - **logger.py**: Logging configuration.
- **README.md**: Documentation file providing an overview and guide on using the machine learning pipeline.

## Dependencies

Ensure you have the following dependencies installed:

- Python 3.x
- pandas
- scikit-learn
- dataclasses

Install dependencies using the following command:

```bash
pip install -r requirements.txt
```

## Usage

### Data Ingestion

1. Place your dataset in the `notebook\data` directory.
2. Update the file path in the `initiate_data_ingestion` method of `DataIngestion` class in `src/data_ingestion.py`.
3. Run the script:

    ```bash
    python data_ingestion.py
    ```

4. The processed data will be saved in the `artifacts` directory.

### Data Transformation

1. Configure data transformation settings in `DataTransformationConfig` class in `src/components/data_transformation.py`.
2. Run the script:

    ```bash
    python data_transformation.py
    ```

3. Transformed data will be saved in the `artifacts` directory.

### Model Training

1. Configure model training settings in `ModelTrainerConfig` class in `src/components/model_trainer.py`.
2. Run the script:

    ```bash
    python model_trainer.py
    ```

3. Trained models and evaluation metrics will be saved in the `artifacts` directory.

## Additional Information

- Custom exceptions are defined in `src/exception.py` to handle errors gracefully.
- Logging is configured in `src/logger.py` to provide information and debug messages.

## License

This project is licensed under the self License - see the [LICENSE.md](LICENSE.md) file for details.
