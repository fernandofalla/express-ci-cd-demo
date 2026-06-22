# express-ci-cd-demo

Proyecto de demostración de un pipeline básico de CI/CD con un backend en Node.js/Express, Docker y GitHub Actions con despliegue automatizado a AWS EC2.

## ¿Qué hace este proyecto?

- API REST básica construida con Express
- Aplicación dockerizada con Docker Compose
- Pipeline de CI/CD automatizado con GitHub Actions
- Despliegue seguro a AWS EC2 usando GitHub Secrets (sin credenciales en el código)
- Suite básica de pruebas con Supertest

## Estructura del proyecto

```text
├── .github/workflows/   # Pipeline de GitHub Actions
├── Backend/
│   ├── src/
│   │   └── app.js
│   ├── test/
│   │   └── app.test.js
│   ├── .dockerignore
│   ├── .gitignore
│   ├── Dockerfile
│   ├── package-lock.json
│   └── package.json
├── README.md
└── docker-compose.yml
```

## Tecnologías

- Node.js / Express
- Docker / Docker Compose
- GitHub Actions
- AWS EC2
- Supertest

## Flujo del pipeline

1. Un push a `main` dispara el workflow
2. Se instalan dependencias y se ejecutan las pruebas
3. Se construye la imagen de Docker
4. La imagen se despliega en EC2 vía SSH usando GitHub Secrets
