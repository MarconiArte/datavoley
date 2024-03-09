Instalar tailwind css:
Primero vamos al contenedor del server:
    docker compose exec server bash
Despues instalamos Tailwind CSS
    npm install -D tailwindcss postcss autoprefixer
Creamos el archivo de tailwind
    npx tailwindcss init -p
En el tailwind.config.js cambiamos el content por este:
    content: [
        "./resources/**/*.blade.php",
        "./resources/**/*.js",
    ],

cambiar en resources/css/app.css
    @tailwind base;
    @tailwind components;
    @tailwind utilities;

Para que se reflejen los cambios en tailwind con vite en vite.config.js
    server: { 
        hmr: {
            host: 'localhost',
        },
    },  

Luego iniciamos con docker compose exec server npm run dev
