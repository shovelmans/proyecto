# Imagen base ligera con Nginx
FROM nginx:alpine

# Elimina la página por defecto de Nginx (opcional)
RUN rm -rf /usr/share/nginx/html/*

# Copia tu index.html al directorio que sirve Nginx
COPY index.html /usr/share/nginx/html/index.html

# Puerto por defecto de Nginx
EXPOSE 80

# Comando por defecto
CMD ["nginx", "-g", "daemon off;"]
