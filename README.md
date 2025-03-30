# Proyecto API entrega 1 proyecto DevOPS


1.  **Levantar Servicios:**
    ```
    docker-compose up --build -d
    ```

2.  **Inicializar Base de Datos (una vez apenas se hayan buildeado los servicios):**
    ```
    docker-compose exec web flask init_db
    ```

Se maneja un token bearer de 1234


1.  **Enviar Request   (POST a Blacklist):**
    ```
    curl -X POST http://localhost:5000/api/v1/blacklists \
         -H "Content-Type: application/json" \
         -H "Authorization: Bearer <TU_STATIC_BEARER_TOKEN>" \
         -d '{
               "email": "test@example.com",
               "app_uuid": "a1b2c3d4-e5f6-7890-1234-567890abcdef",
               "blocked_reason"```Testeo"
             }'
    ```