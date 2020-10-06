#Version NODE
FROM node:lts
#copiar archivos de codigo al docker
# [origen, destino]
COPY ["package.json", "package-lock.json","/usr/src/"]
# Moverse al espacio de trabajo del docker
WORKDIR /usr/src
#Ejecuta el comando npm install 
RUN npm install
#RUN npm audit fix
# le indica al contenedor el puerto por el cual va a salir 
# o exponer el contenedor
#, es el mismo puerto por donde esta escuchando node

#copia el resto de los archivos
COPY [".", "/usr/src/"]

EXPOSE 3000
# ejecuta el comando node index.js el cual levanta el servidor de express
CMD ["npx", "nodemon", "--legacy-watch", "index.js"]
