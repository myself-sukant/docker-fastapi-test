
<div align="center">
  <img src="https://i.giphy.com/media/v1.Y2lkPTc5MGI3NjExYm5vaHRnaGpjbXl0M2V2ZGo4Y3E3ZDlua2tmaDZidHVyNTdyazY0NiZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9cw/KzJkzjggfGN5Py6nkT/giphy.gif" width="200"/>
</div>

<h1 align="center">
  <span class="bold">Welcome aboard! Explore our realm</span>
  <img src="https://media.giphy.com/media/WUlplcMpOCEmTGBtBW/giphy.gif" width="40px"/>
</h1>

<div id="badges" align="center">
  <a href="https://www.linkedin.com/in/tekade-sukant-3343bb252">
    <img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn Badge" style="border-radius: 5px;"/>
  </a>
  <a href="https://www.instagram.com/muschifresser/" target="_blank">
    <img src="https://img.shields.io/badge/Instagram-AA336A?style=for-the-badge&logo=instagram&logoColor=white" alt="Instagram Badge" style="margin-bottom: 5px;" />
  </a>
  <a href="https://github.com/tekadesukant">
    <img src="https://img.shields.io/badge/GitHub-purple?style=for-the-badge&logo=github&logoColor=white" alt="GitHub Badge"/>
  </a>
</div>

# FastAPI Docker User API

This project is a simple FastAPI application that handles user data using a JSON file instead of a database. The entire application is containerized using Docker and can be run using Docker Compose.

---

## Project Features

- Built using [FastAPI](https://fastapi.tiangolo.com/)
- Stores user data in a `users.json` file (no database used)
- Containerized using Docker
- Easy to run with `docker-compose`
- API documentation available at `/docs`


## Project Structure

```
docker-fastapi-userapi/
├── app/
│   ├── main.py            # FastAPI app entry point
│   ├── services.py        # Logic to handle file operations
│   └── data/              # Contains users.json
│       └── users.json     # Auto-created when user data is posted
├── Dockerfile             # Docker image instructions
├── docker-compose.yml     # Docker Compose file
├── requirements.txt       # Python dependencies
└── README.md              # Project documentation
```


## Example User Payload

```json
{
  "data": [
     {
        "first_name": "Sukant"
        "last_name": "Tekade"
        "age": 23
     }
  ] 
}
```

---

## Sample Docker Compose File

```yaml
version: '3.8'

services:
  fastapi-app:
    build: .
    container_name: fastapi-app
    ports:
      - "8000:8000"
    volumes:
      - .:/app
      - ./app/data:/app/app/data
    restart: always
```

## Author

- **TekadeSukant**
- [GitHub Profile](https://github.com/tekadesukant)

---
