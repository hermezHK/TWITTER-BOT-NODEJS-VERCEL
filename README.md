1. Instalar paquetes

   ```bash
   npm init 
   ```

2. Es necesario crear tu archivo .env:

   access

   llaves y keys de twitter.

   ```bash
   TWITTER_CUSTOMER_KEY=""
   TWITTER_CUSTOMER_SECRET=""
   TWITTER_ACCESS_TOKEN=""
   TWITTER_ACCESS_TOKEN_SECRET=""
   ```

3. dependence:

   ```bash
   npm i twitter-api-v2
   npm i node-cron
   npm i dotenv
   
   #vercel 
   vercel login
   vercel deploy
   ```

4. Ejecute el servidor lanzar el tweet:

   ```bash
   node app.js
   ```

5. crear tu archivo json raiz del proyecto:

    ```bash
        {
            "version": 2,
            "builds": [
            {
                "src": "main.js",
                "use": "@now/node"
            }
            ],
            "routes": [
            {
                "src": "/.*",
                "dest": "main.js"
            }
            ]
        }
    ```

4. funcionalidad node-cron:

   - Segundo: 0-59
   - Minuto: 0-59
   - Hora: 0-23
   - Día del mes: 1-31
   - Mes: 0-11 (0 = Enero)
   - Día de la semana: 0-7 (0 o 7 = Domingo)
   
        Puedes usar valores específicos, como 5 para el quinto día del mes, o rangos, como 1-10 para los primeros diez días del mes. También puedes usar comodines, como * para cualquier valor.

        Por ejemplo, para ejecutar una tarea todos los días a las 9:30 AM, podrías utilizar el siguiente código:

   ```bash
   cron.schedule('30 9 * * *', main);
   ```
 
    

    
        
        


    