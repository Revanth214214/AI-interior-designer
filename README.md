# AI-interior-designer
An AI system where the user uploads an image of their room and the system suggests changes based on the style of the room to make it better.

ai-interior-designer/
│
├── research/                      # 🧪 EXPERIMENTATION ZONE (Notebooks)
│   ├── 01_data_ingestion.ipynb    # Explore and inspect ADE20K dataset
│   ├── 02_object_detection.ipynb  # Experiment with YOLO/ADE20K detectors
│   ├── 03_style_classification.ipynb # Test CLIP/ViT style & palette extraction
│   └── 04_recommendation_engine.ipynb # Test FAISS vector search & design rules
│
├── data/                          # Datasets and catalog storage
│   ├── raw/                       # Downloaded ADE20K indoor samples
│   ├── processed/                 # Preprocessed image/annotation subsets
│   └── catalog/                   # Sample furniture catalog (JSON/Parquet) IKEA
│
├── .github/
│   └── workflows/
│       ├── ci.yml                 # Code quality, linting, unit tests
│       └── cd.yml                 # Docker build & deployment (for production phase)
│
├── src/                           # 🚀 PRODUCTION CODE (Built after research stage)
│   ├── __init__.py
│   ├── components/                # Modular ML classes
│   │   ├── __init__.py
│   │   ├── detector.py
│   │   ├── style_classifier.py
│   │   ├── palette_extractor.py
│   │   └── recommender.py
│   ├── pipelines/                 # Training and inference pipelines
│   │   ├── __init__.py
│   │   └── inference_pipeline.py
│   └── utils/                     # Logging, config parser, helpers
│       ├── __init__.py
│       ├── logger.py
│       └── config.py
│
├── app/                           # Web API & UI
│   ├── main.py                    # FastAPI entrypoint
│   └── ui.py                      # Interactive UI
│
├── tests/                         # Pytest test suites
├── Dockerfile                     # Multi-stage Docker configuration
├── docker-compose.yml
├── requirements.txt
└── README.md