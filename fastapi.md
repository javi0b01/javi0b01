# :memo: Notes
## FASTAPI
### Learn
1. What is it
2. What does it do
3. Why to use it
4. Getting started
5. Concepts
6. Code samples
7. Documentation
### Resources
- [FastAPI](https://fastapi.tiangolo.com/)
- [FastAPI in Containers - Docker](https://fastapi.tiangolo.com/deployment/docker/)
- [The OpenAPI Specification](https://github.com/OAI/OpenAPI-Specification)
- [OpenAPI Specification](https://swagger.io/specification/)
- [Starlette](https://www.starlette.io/)
- [Pydantic](https://docs.pydantic.dev/)
- [Uvicorn](https://www.uvicorn.org/)
- [Gunicorn](https://gunicorn.org/)
- [Swagger UI](https://github.com/swagger-api/swagger-ui)
- [Redoc](https://github.com/Redocly/redoc)
### Requirements
- [Python](https://www.python.org/)
### Terms and concepts
- Python
- Python module
- Python types
- Python enumerations
- Python web framework
- API
- Rest API
* Automatic API documentation
  - Interactive API docs
  - Alternative API docs
* Installation
  - Import FastAPI
  - Create an instance of FastAPI
- Path or Endpoint or Route
- Operation
- Decorator
- Function
- Path operation decorator
- Path operation function
- Validation constraints or Data parsing
* Parameters
  - Path parameters
  - Path parameters with types
  - Order matters
  - Predefined values
  * Path parameters containing paths
    - Path convertor
  * Query parameters
    - Set parameters
    - Optional parameters
    - Default parameters
    - Multiple path and query parameters
    - Required query parameters
  - Headers
  - Cookies
  - Form fields
  - Files
* Request body
  * BaseModel
    - Schema
    - Required value
    - Default value
    - Optional value
  - Request body + path parameters
  - Request body + path + query parameters
- Query parameters and String validations
- Response body
- Dependency injection system
- Security
- Authentication
- Deeply nested JSON models
- Web sockets
- Tests
- CORS
- Cookie sessions
- Performance
- Optional dependencies
- ORM
- ODM
### Setup
#### Create a FastAPI project in virtual environment
#### Create a FastAPI project in Docker
requirements.txt
```
fastapi==0.100.1
pydantic==2.1.1
uvicorn==0.23.1
```
Dockerfile
```
FROM python:3.11.4
ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1
WORKDIR /core
COPY requirements.txt ./
RUN python -m pip install -r requirements.txt
COPY ./src ./src
```
compose.yaml
```
version: '3.8'
services:
  api:
    container_name: <name>
    build: .
    working_dir: /core
    command: uvicorn src.main:api --host 0.0.0.0 --reload
    volumes:
      - .:/core
    ports:
      - 8000:8000
```
## Software Developer
Built by [JAVI](https://github.com/javi0b01/) :copyright: 2023  
Found a bug or have an idea? [Contact me](https://www.linkedin.com/in/javi0b01/).
