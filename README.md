
# Ollama Installation and Usage Guide on WSL

## Repository Overview

This repository contains clear instructions on how to set up and use the `llama3` and `mistral` models with Ollama. It includes all necessary scripts and configuration files used in the setup process.

## Watch the Demo Video

[![Ollama Installation Video](https://img.youtube.com/vi/Af362vPLuVQ/0.jpg)](https://www.youtube.com/watch?v=Af362vPLuVQ)


## Setup Instructions

### Step 1: Install Ollama

To install Ollama, run the following command in your terminal:

```sh
curl -fsSL https://ollama.com/install.sh | sh
```

### Step 2: Verify Installation

Check the installed version of Ollama to ensure it was installed correctly:

```sh
ollama --version
```

### Step 3: Run the `llama3` Model

To start the `llama3` model, use the command:

```sh
ollama run llama3
```

### Step 4: Query the `llama3` Model

Send a request to the `llama3` model to list the pros and cons of Xbox and PlayStation:

```sh
curl http://localhost:11434/api/chat -d '{
  "model": "llama3",
  "messages": [
    { "role": "user", "content": "List the pros and cons of Xbox and PlayStation" }
  ],
  "stream": false
}'
```

### Step 5: Run the `mistral` Model

To start the `mistral` model, use the command:

```sh
ollama run mistral
```

### Step 6: Query the `mistral` Model

Send a request to the `mistral` model to list the pros and cons of Xbox and PlayStation:

```sh
curl http://localhost:11434/api/chat -d '{
  "model": "mistral",
  "messages": [
    { "role": "user", "content": "List the pros and cons of Xbox and PlayStation" }
  ],
  "stream": false
}'
```

## Explanation of Setup Parts

1. **Installation Command**: Installs Ollama on your system using a simple shell script.
2. **Version Check**: Ensures that Ollama has been installed correctly by displaying its version.
3. **Running Models**: Shows how to start the `llama3` and `mistral` models using the `ollama run` command.
4. **Querying Models**: Demonstrates how to interact with the models by sending HTTP requests to the local API endpoint.

## Included Scripts and Configuration Files

- Installation script: Provided via the curl command.
- Example queries: Demonstrated in the curl commands for querying the models.

This repository is intended to help users quickly set up and utilize Ollama's models for various tasks, with a specific focus on comparing gaming consoles.
