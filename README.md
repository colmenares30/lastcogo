# LLM Pruebas

Repositorio de trabajo con modelos lenguaje largo usando ollama

# 1.Instalación

Como primer paso descargamos [ollama] (https://ollama.com/download/linux) de su página web, y ejecutamos el siguiente comando: 

````bash
$ curl -fsSL https://ollama.com/install.sh | sh
````

## 2. Ejecutar el servidor

Ejecutar el servidor (abriendo otra consola) de API REST de ollama con el siguiente comando: 

````bash
$ ollama serve
````

## 3. Descargar un modelo

En la página de ollama descarga un [modelo](https://ollama.com/library) utilizando el siguiente comando:

````bash
$ ollama pull tinyllama
````

# nota

(https://github.com/ollama/ollama/blob/main/docs/api.md)
(curl -X POST http://localhost:11434/api/generate -d '{
  "model": "tinyllama",
  "prompt": "Why is the sky blue?"
}')
Para enviar datos se utiliza -X POST.  
Puerto default 11434.
localhost, siginifica que se ejecuta de forma local, (-o salida. md) lo guarda en lineas.

## 4. Realizar un request a la API REST

Para realizar una consulta utilizamos el comando curl como se muestra en el siguiente ejemplo:

````bash
curl -X POST http://localhost:11434/api/generate -d '{
  "model": "tinyllama",
  "prompt": "Why is the sky blue?",
}'
````

## 5. Realizar un reques sin stream

Para realizar una consulta a la API REST sin stream se hace de la siguiente forma: 

````bash
curl http://localhost:11434/api/generate -d '{
  "model": "llama3",
  "prompt": "Why is the sky blue?",
  "stream": false
}'
````
"git add . " Lista de archivos
