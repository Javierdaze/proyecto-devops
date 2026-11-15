# Reserva de Horas Médicas – Proyecto DevOps (demo)

Sitio web estático servido con Nginx en Docker. Sin API ni base de datos. Datos ficticios.

## Requisitos
Git y Docker Desktop en ejecución.

## Ejecución
    git clone https://github.com/TU_USUARIO/proyecto-devops.git
    cd proyecto-devops
    cp .env.example .env
    docker compose up -d --build

## Verificación
- Navegador: http://localhost:8080
- `docker compose ps`
- `docker compose logs`
- `docker stats --no-stream`

## Detener
    docker compose down

## Seguridad
- No se versionan credenciales: `.env` está en `.gitignore`.
- `.env.example` solo contiene valores no sensibles.
- Todos los datos del formulario son ficticios y no se envían a ningún servidor.

## Estrategia de ramas
`main` estable; trabajo en `feature/*` y fusión mediante Pull Request.
