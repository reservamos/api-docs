# Errors

Reserbus API usa los siguientes códigos de error:

Código HTTP | Significado
---------- | -------
401 | Unauthorized -- Tu API Key o Secret es incorrecto.
404 | Not Found -- El recurso especificado no se encuentra.
422 | Unprocessable Entity -- Hubo un problema con los parámetros que enviaste.
500 | Internal Server Error -- Tuvimos un probrema con nuestro servidor. Intente de nuevo más tarde.
503 | Service Unavailable -- El servicio no está disponible en este momento. Intente de nuevo más tarde.
