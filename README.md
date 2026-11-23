# LLM-Assisted CAD/CAM Model Generation

## Project Overview

This project explores the generation of 3D CAD models using Large Language Models (LLMs) and natural-language inputs.

The system aims to reduce manual CAD modelling effort by converting user descriptions into executable Python scripts that generate 3D models using FreeCAD.

The repository contains multiple approaches to model generation, including automated text-based generation, direct text-based generation and experimental image-assisted workflows.

## Key Features

- Natural-language-based 3D model generation.
- AI-assisted generation of FreeCAD Python scripts.
- Automated execution of generated scripts.
- Generation and export of 3D models in STL format.
- Multiple approaches for CAD model generation.
- Experimental image-assisted generation workflow.

## Technologies Used

| Technology | Purpose |
|---|---|
| Python | Main programming language |
| FreeCAD | 3D CAD modelling and script execution |
| Ollama | Local LLM runtime for supported workflows |
| Granite 3.2 Vision | Visual assessment |
| Llama 3.2 1B | Entity extraction |
| Stable Code 3B | Code generation |
| FastAPI | Backend API development |
| Streamlit | Frontend development |
| STL | 3D model export format |

## System Architecture

The main automated workflow follows these stages:

1. **User Input:** The user provides a natural-language description of the required 3D model.
2. **Backend Processing:** FastAPI receives and processes the user request.
3. **AI Processing:** The system uses the configured AI models to interpret the input and generate the required CAD code.
4. **Code Generation:** A Python script is generated to create the requested 3D geometry.
5. **Script Execution:** The generated script is executed using the FreeCAD environment.
6. **3D Model Generation:** FreeCAD processes the script and generates the 3D geometry.
7. **File Export:** The generated model is exported in STL format.
8. **Output:** The generated 3D model is made available to the user.

## Project Structure

| Directory/File | Description |
|---|---|
| `AutomatedApproach/` | Automated CAD generation workflow |
| `DirectTextApproach/` | Direct text-based generation workflow |
| `3D_Downloads/` | Generated 3D model exports |
| `data/` | Project data and supporting resources |
| `frontend/` | Frontend application |
| `netflix-gpt/` | Additional application component |
| `server.py` | FastAPI backend |
| `README.md` | Project documentation |

## Installation and Setup

### Prerequisites

- Windows operating system for the relevant desktop-based workflows.
- Python.
- FreeCAD.
- Visual Studio Code.
- Ollama for workflows using locally hosted models.

### Step 1: Clone the Repository

```bash
git clone https://github.com/karthikk89/LLM-CAD-CAM.git
```

### Step 2: Navigate to the Project Directory

```bash
cd LLM-CAD-CAM
```

### Step 3: Install Dependencies

Install the Python dependencies required by the selected workflow.

```bash
pip install -r requirements.txt
```

### Step 4: Configure FreeCAD

Install FreeCAD and configure the appropriate FreeCAD Python executable path according to your system.

### Step 5: Configure Ollama

Install Ollama and download the required models for workflows that use locally hosted language models.

## Running the Project

1. Install the required dependencies.
2. Configure FreeCAD and the AI model runtime.
3. Start the backend server using the appropriate Python environment.
4. Launch the Streamlit frontend using the relevant application entry point.
5. Enter a natural-language description of the required 3D model.
6. Allow the system to process the request and generate the CAD model.
7. Retrieve the generated STL file from the output directory.

## Output

The system aims to generate 3D CAD models in STL format.

These models can subsequently be viewed, modified or processed using compatible 3D modelling and slicing applications.

## Project Background and Attribution

This repository is an adapted copy of a project originally developed by a teammate.

The project explores the integration of Large Language Models with CAD modelling workflows to simplify 3D model generation through natural-language interaction.

Original contributors and upstream work should receive appropriate credit.

## Future Improvements

- Improve the accuracy of generated CAD scripts.
- Integrate the different generation approaches.
- Improve error handling and script validation.
- Enhance the Streamlit user interface.
- Improve compatibility across operating systems.
- Expand support for different 3D model formats.
