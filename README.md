# Generative AI for the curious 
Touching on different Gen AI concepts

---

## Prerequisites
Before diving in, ensure your setup is as ready as your curiosity:

- **Python 3.8+** 
- **Docker** (a must-have for spinning up our PostgreSQL instance with the pgvector extension)

---

## Installation
Follow these steps to get your environment up and running:

### 1. Clone the Repository
```bash
git clone https://github.com/geraldsanga/gen-ai-mini-course.git
cd gen-ai-mini-course
```


### 2. Create a Virtual Environment
```python
python -m venv venv
source venv/bin/activate  # Windows users: use 'venv\Scripts\activate'
```

### 3. Install Dependencies
```python
pip install --upgrade pip
pip install -r requirements.txt
```

## Docker Setup for PostgreSQL with pgvector
Currently our RAG scripts rely on a PostgreSQL database with the pgvector extension. Here’s how to set it up:

### 1. Start the pgvector Docker Container
Navigate to the folder containing docker-compose.yaml (inside notebooks/) and run:

```bash
docker compose up
```

### 2. Create the pgvector Extension
Once your container is running, initialize the extension with:
```bash
docker exec -it postgres-pgvector psql -U postgres -c "CREATE EXTENSION vector"
```


## Getting Started
Once you’ve set up your environment, explore the rag folder to experience our simple RAG demo. 
Each concept folder is structured to provide detailed insights and instructions—ideal for building 
your own experiments as you progress.

## Contributing
Got a brilliant idea or an improvement suggestion? We welcome contributions! 
Open an issue or submit a pull request, and let’s build this repository into a comprehensive learning resource together.

## License
This project is licensed under the [MIT License](https://opensource.org/license/mit).