# HTTP (Hypertext Transfer Protocol) 

Toda la WWW (World Wide Web) utiliza este protocolo, todo lo que aparece en un navegador como Chrome, Firefox, Edge, DuckDuckGo, etc, se transmite mediante requests y responses entre cliente y servidor.

---------------------------------

# Composición de un http request

Contiene la siguiente infomración
  * (método HTTP, URL y versión)
  * (Headers)
```
GET php.net HTTP/1.1
:authority: github.com
:method: GET
:path: /
:scheme: https
accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
accept-encoding: gzip, deflate, br
accept-language: es-ES,es;q=0.9
cache-control: max-age=0
cookie: _ga=GA1....
if-none-match: W/"dfb35719da0d23ae11c3fd61d5ac0d90"
sec-ch-ua: " Not A;Brand";v="99", "Chromium";v="99", "Google Chrome";v="99"
sec-fetch-user: ?1
upgrade-insecure-requests: 1
user-agent: Mozilla/5.0
X-Forwarded-For: IP
```
----------------------------------------------

# composición de http response: respuesta del servidor

Contiene la siguiente informacion

* (versión HTTP y código de respuesta)
* (http headers)
* (contenido html)
```
HTTP/1.1 200 OK
cache-control: max-age=0, private, must-revalidate
content-encoding: gzip
content-security-policy: 
content-type: text/html; charset=utf-8
date: 
etag: W/"b07718da30e93b1368fc4e7ebdb37644"
expect-ct: max-age=2592000, report-uri="https://api.github.com/_private/browser/errors"
permissions-policy: interest-cohort=()
referrer-policy: origin-when-cross-origin, strict-origin-when-cross-origin
server: GitHub.com
sted-With
x-content-type-options: nosniff
x-frame-options: deny
x-github-request-id: C60B:7563:8E3E14:F25600:621FE39A
x-xss-protection: 0

<!DOCTYPE html...
```
-----------------------

# Estructura de un HTTP request

https://developer.mozilla.org/es/docs/Web/HTTP/Methods
https://developer.mozilla.org/es/docs/Web/HTTP/Basics_of_HTTP/Evolution_of_HTTP

un request http se compone por:

* Método: GET, HEAD, POST, PUT, DELETE, CONNECT, OPTIONS, TRACE, PATCH. Indica que tipo de request
* Path: la URL que se solicita.
* Protocolo: contiene HTTP y su versión, actualmente 1.1.
* Ejemplo: GET php.net HTTP/1.1

-----------------------

# Estructura de un HTTP response

https://developer.mozilla.org/es/docs/Web/HTTP/Status

* Protocolo. Contiene HTTP y su versión, actualmente 1.1.
* Status code. El código de respuesta.
* Headers. La mayoría de los headers son opcionales. su composicion es "clave: valor", Contienen información sobre el software del servidor, cuando se modificó por última vez el resource solicitado, el mime type, etc.
* Body. Si el servidor devuelve información que no sean headers ésta va en el body
