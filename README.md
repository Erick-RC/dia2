# Sistema de Autenticación con JWT en Node.js

## Descripción

Este proyecto implementa un sistema de autenticación básico utilizando JSON Web Tokens (JWT) en una aplicación Node.js con Express.js. Incluye funcionalidad para generar tokens con expiración y verificar su validez.

## Instalación

1. npm install

## Uso Endpoints 
## POST /login ##
Descripción: Endpoint para autenticar un usuario y generar un token JWT.
Cuerpo de la solicitud:
    {
    "username": "user",
    "password": "password"
    }
Respuesta exitosa:
    {
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9..."
    }
Respuesta en caso de error:
    {
    "message": "Credenciales inválidas"
    }

## GET /verify ##
Descripción: Endpoint para verificar la validez de un token JWT.
Encabezados: Authorization: <token-generado-en-login>
Respuesta exitosa:
    {
    "message": "Token válido",
    "username": "user"
    }
Respuesta en caso de error:
    {
    "message": "Token inválido o expirado"
    }

### Servidor Express

Para iniciar el servidor:
```bash
node index.mjs
