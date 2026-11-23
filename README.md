# LLM-Assisted CAD/CAM Model Generation

## Project Overview

This project explores the generation of 3D CAD models using Large Language Models (LLMs) and natural-language inputs.

The system aims to reduce manual CAD modelling effort by converting user descriptions into executable Python scripts that generate 3D models using FreeCAD.

The repository contains multiple approaches to model generation, including automated text-based generation and experimental image-assisted workflows.

**Note:** This repository is an adapted copy of a project originally developed by a teammate. The original project and its authors should be credited when presenting or distributing this work.

## Key Features

- Natural-language-based 3D model generation.
- AI-assisted generation of FreeCAD Python scripts.
- Automated execution of generated scripts.
- Export of generated 3D models in STL format.
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
| Pydantic | Request data validation |
| PyAutoGUI | Desktop automation |
| Pyperclip | Clipboard interaction |
| HTML, CSS, JavaScript | Frontend development |
| STL | 3D model export format |

## System Architecture

The main automated workflow follows these stages:

1. **User Input:** The user provides a natural-language description of the required 3D model.
2. **Backend Processing:** FastAPI receives the request through the `/3dobj` endpoint.
3. **AI Code Generation:** The system obtains a Python script intended to create the requested CAD model.
4. **Script Execution:** The generated Python script is executed using the FreeCAD Python environment.
5. **3D Model Generation:** FreeCAD processes the script and generates the 3D geometry.
6. **File Export:** The generated model is saved in STL format.
7. **Response:** The backend returns the generated STL file to the client.

## Project Structure

| Directory/File | Description |
|---|---|
| `AutomatedApproach/` | Automated CAD generation workflow |
| `DirectTextApproach/` | Direct text-based generation workflow |
| `3D_Downloads/` | Generated 3D model exports |
| `data/` | Project data and supporting resources |
| `frontend/` | Frontend application |
| `netflix-gpt/` | Additional application component |
| `server.py` | FastAPI backend and automated generation endpoint |
| `README.md` | Project documentation |

## Installation and Setup

### Prerequisites

- Windows operating system for the inspected desktop automation workflow.
- Python.
- FreeCAD.
- Visual Studio Code.
- Ollama for workflows that use locally hosted models.

### Step 1: Clone the repository

```bash
git clone https://github.com/karthikk89/LLM-CAD-CAM.git
```

### Step 2: Navigate to the project

```bash
cd LLM-CAD-CAM
```

### Step 3: Install Python dependencies

Install the dependencies required by the particular workflow you intend to run. These include the relevant Python packages for FastAPI, Pydantic, PyAutoGUI and Pyperclip.

### Step 4: Configure FreeCAD

Install FreeCAD and configure the FreeCAD Python executable path in `server.py` to match your system.

### Step 5: Configure Ollama

For workflows using Ollama, install Ollama and download the required models.

## Running the Project

1. Install and configure the required software.
2. Configure the relevant model runtime.
3. Start the backend using the appropriate Python environment.
4. Provide a natural-language description through the supported frontend or API.
5. Allow the system to generate and execute the CAD script.
6. Retrieve the generated STL model from the export directory.

**Important:** The inspected `server.py` uses Windows desktop automation to interact with ChatGPT. It also contains a machine-specific FreeCAD executable path. These settings must be configured before running that particular workflow.

## Output

The system aims to generate 3D CAD models in STL format, which can subsequently be viewed or processed using compatible 3D modelling and slicing applications.

## Project Background and Attribution

This project is based on an existing teammate-developed project and draws inspiration from the Query2CAD research direction.

The repository is maintained here as an adapted project copy. Original contributors and upstream work should receive appropriate credit.

## Future Improvements

- Improve the accuracy of generated CAD scripts.
- Integrate the different generation approaches.
- Improve error handling and script validation.
- Enhance the frontend experience.
- Improve compatibility across operating systems.

