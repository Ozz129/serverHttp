# serverHttp

// http -> modulo para crear servidores que se incluye en core de node
const http = require('http');

// Eleccion de la puerta de ingreso
const port = 3000;

/**
 * Configuración de nuestro servidor
 * 
 * El servidor va a recibir la solicitud y la respuesta como parametros
 * 
 * req -> request: Solicitud
 *  {
 *      ... propiedades
 *  }
 * res -> response: Respuesta 
 * {
 *      ... propiedades
 * }
 */

 const server = http.createServer((req, res) => {
    // Rutas: La dirección del recurso al que quiero acceder

    /**
     * req.method -> Trae el metodo que se esta usando en la solicitud
     * req.url -> Trae la definicion del recurso al que queremos ingresar
     */

    // Esta es la definicion de una ruta
    if(req.method === 'GET' && req.url === '/user' ){
        console.log('Entro a ruta get') 
        /**
         * Son datos que se encuentran ya registrados en nuestro servidor
         * Adjuntar toda la logica, que permita retornar una lista de usuarios
         */
        res.statusCode = 200;
        res.end('Hasta luego');
    } else if(req.method === 'POST' && req.url === '/user') {
        /**
         * Datos que ingresan no se encuentran en nuestro servidor
         * Adjuntar toda la logica, que permita crear un usuario
         */

        // Revise el espacio disponible

        // si ya se lleno responda no hay espacio

        // si todavia hay espacio disponible, siga almacenando
    } else if(req.method === 'PUT' && req.url === '/user') {
        /**
         * Datos que estan dentro del servidor pero que requieren un cambio
         * Adjuntar toda la logica, que permita crear un usuario
         */
    }else if(req.method === 'DELETE' && req.url === '/user') {
        /**
         * Datos que eliminaremos deberian estar dentro de mi servidor
         * Adjuntar toda la logica, que permita eliminar un usuario
         */
    }
 })

 server.listen(port, () => {
    console.log('Servidor corriendo');
 })

