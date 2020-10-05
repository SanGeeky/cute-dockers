#Version NODE
FROM node:lts
#copiar archivos de imagen
# [origen, destino]
COPY [".", "/usr/src/"]
# Moverse al espacio de trabajo del docker
WORKDIR /usr/src
#Ejecuta el comando npm install 
RUN npm install
# le indica al contenedor el puerto por el cual va a salir 
# o exponer el contenedor
#, es el mismo puerto por donde esta escuchando node
EXPOSE 3000
# ejecuta el comando node index.js el cual levanta el servidor de express
CMD ["node", "index.js"]
