# CCGN Hospital System - Replit.md

## Overview

This is a Streamlit-based prototype application for the **Contextual Clinical Graph Network (CCGN)** - an AI-powered clinical decision support system designed specifically for Jigjiga University Hassan Yabare Referral Hospital. The system demonstrates graph-based patient data representation using synthetic hospital data to showcase advanced clinical analytics and decision support capabilities.

## System Architecture

### Frontend Architecture
- **Framework**: Streamlit web framework
- **Multi-page Application**: Uses Streamlit's native page routing system
- **Interactive Visualizations**: Plotly for charts, graphs, and network visualizations
- **User Interface**: Custom CSS styling with responsive design
- **Pages Structure**:
  - Main dashboard with system overview
  - Interactive graph visualization
  - Model architecture documentation
  - Data preparation workflows
  - Evaluation metrics display
  - Research thesis generator

### Backend Architecture
- **Core Model**: Custom PyTorch-based Graph Neural Network (CCGN)
- **Data Processing**: Pandas and NumPy for data manipulation
- **Graph Operations**: NetworkX for graph construction and analysis
- **Synthetic Data Generation**: Faker library for realistic hospital data simulation
- **Model Components**:
  - Graph Convolution Layers
  - Attention mechanisms
  - Feature encoding layers
  - Prediction layers

### Data Storage Solutions
- **Primary Storage**: In-memory storage using Streamlit session state
- **Data Format**: Pandas DataFrames for structured data
- **Graph Storage**: NetworkX graph objects
- **Synthetic Data**: Generated on-demand using controlled random seeds
- **No Persistent Database**: Currently operates with synthetic data only

## Key Components

### 1. CCGN Model (`utils/ccgn_model.py`)
- Custom Graph Neural Network implementation
- PyTorch-based architecture with graph convolution layers
- Attention mechanisms for clinical context understanding
- Support for multi-task learning (diagnosis, treatment recommendation)

### 2. Graph Builder (`utils/graph_builder.py`)
- Constructs clinical graphs from patient data
- Supports multiple node types (patients, symptoms, diagnoses, medications)
- Implements various edge types (causal, temporal, correlation)
- Provides graph visualization capabilities

### 3. Synthetic Data Generator (`utils/synthetic_data.py`)
- Creates realistic hospital data for demonstration
- Generates patients, medical records, lab results, medications
- Uses Faker library for realistic names, addresses, dates
- Maintains data consistency and relationships

### 4. Thesis Generator (`utils/thesis_generator.py`)
- Automated academic document generation
- Supports multiple citation styles (APA, IEEE, Harvard, Vancouver)
- Generates research proposals, full thesis documents
- Structured academic writing with proper formatting

## Data Flow

1. **Data Generation**: Synthetic hospital data is generated using controlled parameters
2. **Graph Construction**: Clinical data is transformed into graph structures with nodes and edges
3. **Model Processing**: CCGN model processes graph data for predictions
4. **Visualization**: Results are displayed through interactive Streamlit interface
5. **User Interaction**: Users can explore different patients, graph types, and model parameters

## External Dependencies

### Core Libraries
- `streamlit`: Web application framework
- `pandas`: Data manipulation and analysis
- `numpy`: Numerical computing
- `plotly`: Interactive visualizations
- `torch`: Deep learning framework
- `torch-geometric`: Graph neural network operations
- `networkx`: Graph analysis and manipulation
- `scikit-learn`: Machine learning utilities
- `faker`: Synthetic data generation

### Visualization Libraries
- `plotly.express`: Statistical visualizations
- `plotly.graph_objects`: Custom plot objects
- `plotly.subplots`: Multi-panel visualizations
- `plotly.figure_factory`: Specialized plot types

## Deployment Strategy

### Current Setup
- **Platform**: Designed for Replit deployment
- **Entry Point**: `app.py` serves as the main application file
- **Page Structure**: Multi-page Streamlit app with organized page directory
- **Dependencies**: All requirements managed through pip/requirements.txt

### Scalability Considerations
- **Session Management**: Uses Streamlit session state for user data persistence
- **Memory Management**: Efficient data structures for large patient datasets
- **Performance**: Lazy loading of expensive computations
- **Caching**: Streamlit caching for model predictions and graph generation

### Future Enhancements
- Integration with real Odoo HMS system
- Database connectivity for persistent storage
- User authentication and authorization
- API endpoints for external system integration
- Production deployment on cloud platforms

## Changelog

```
Changelog:
- July 05, 2025. Initial setup
```

## User Preferences

```
Preferred communication style: Simple, everyday language.
```

## Technical Notes

### Model Architecture Decisions
- **Graph Neural Networks**: Chosen for their ability to capture complex relationships in clinical data
- **Attention Mechanisms**: Implemented to focus on relevant clinical features
- **Multi-task Learning**: Supports simultaneous prediction of multiple clinical outcomes
- **Synthetic Data**: Used for demonstration due to privacy constraints with real patient data

### Integration Points
- **Odoo HMS**: Designed to integrate with hospital's existing management system
- **Clinical Workflows**: Aligned with hospital's operational procedures
- **Ethiopian Healthcare Context**: Tailored for resource-constrained environments

### Performance Considerations
- **Memory Efficiency**: Optimized for handling large patient datasets
- **Computation Speed**: Efficient graph operations and model inference
- **User Experience**: Responsive interface with real-time updates
- **Scalability**: Architecture supports growth in data volume and user base
