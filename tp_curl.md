# TP curl - comprendre les requêtes et les réponses HTTP

Pour les questions suivantes, vous devez utiliser l'url suivante : https://webhook.site/6f594809-a4b4-483e-841b-0c3b0a00edfe

Pour tous les appels vous devez ajouter un header pour identifier votre appel parmis ceux des autres étudiants : x-student : VOTRE_NOM

## Faire un appel curl : copier la commande exécutée et indiquer la requête et la réponse
curl https://webhook.site/6f594809-a4b4-483e-841b-0c3b0a00edfe -H "x-student:khelafi"


## Quel est la version du protocole utilisé par le serveur ?

curl -v  https://webhook.site/6f594809-a4b4-483e-841b-0c3b0a00edfe


## Quels sont les headers que l'on envoie dans la requête ? Quels sont leur sens ?

 HTTP/1.1 

## Quelles informations pouvez-vous trouver à propos du certificat SSL ?

SSL connection using TLSv1.3 / TLS_AES_256_GCM_SHA384

## Quel est le code de la réponse ? Que signifie-t-il ?

200 OK, le code de réponse de l'état de réussite indique que la demande a réussi


## Quels headers recevez vous dans la response ? Quels sont leur sens ?


## Faire un appel curl en envoyant du texte brut : copier la commande exécutée et indiquer la requête et la réponse


curl https://webhook.site/6f594809-a4b4-483e-841b-0c3b0a00edfe -X POST -d "option=valeur&champs=autrevaleur" -H "Content-Type: text/plain"


<html>
<head><title>400 Bad Request</title></head>
<body bgcolor="white">
<center><h1>400 Bad Request</h1></center>
<hr><center>nginx</center>
</body>
</html>


## Faire un appel curl en envoyant du JSON (avec les bons headers) : copier la commande exécutée et indiquer la requête et la réponse

curl -d '{"option": "value", "queqluechose": "autrevaleur"}' -H "text/plain" -X POST https://webhook.site/6f594809-a4b4-483e-841b-0c3b0a00edfe


## Faire une appel curl en envoyant une basic authentication en utilisant 2 méthodes différentes : copier les commandes exécutées et indiquer la requête et la réponse à chaque fois 


## Exécuter la commande suivante avec la méthode GET puis indiquer la réponse : curl https://demo.api-platform.com/books/07dd4786-aaa7-4d08-a467-076b76f1d1b6 

{"@context":"\/contexts\/Error","@type":"hydra:Error","hydra:title":"An error occurred","hydra:description":"Not Found"}

## Exécuter la commande suivante avec la méthode PATCH  puis indiquer la réponse : curl https://demo.api-platform.com/top_books/1

<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8" />
    <meta name="robots" content="noindex,nofollow,noarchive" />
    <title>An Error Occurred: Method Not Allowed</title>
    <style>body { background-color: #fff; color: #222; font: 16px/1.5 -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; margin: 0; }
.container { margin: 30px; max-width: 600px; }
h1 { color: #dc3545; font-size: 24px; }
h2 { font-size: 18px; }</style>
</head>
<body>
<div class="container">
    <h1>Oops! An Error Occurred</h1>
    <h2>The server returned a "405 Method Not Allowed".</h2>

    <p>
        Something is broken. Please let us know what you were doing when this error occurred.
        We will fix it as soon as possible. Sorry for any inconvenience caused.
    </p>
</div>
</body>
</html>



## Quel est le code HTTP reçu ? Quel est sa signification ?
The server returned a "405 Method Not Allowed", the target resource doesn't support this method.

## Exécuter la commande suivante puis indiquer la réponse : curl https://demo.api-platform.com/top_books/1

{
  "@context": "/contexts/TopBook",
  "@id": "/top_books/1",
  "@type": "TopBook",
  "id": 1,
  "title": "Depuis l'au-delà",
  "author": "Werber Bernard",
  "part": "",
  "place": "F WER",
  "borrowCount": 9
}

## Exécuter la commande suivante puis indiquer la réponse : curl https://demo.api-platform.com/top_books/9999

{"@context":"\/contexts\/Error","@type":"hydra:Error","hydra:title":"An error occurred","hydra:description":"Not Found"}


## Quel est le code HTTP ? Que signifie-t-il ?
404 Not Found, soit le livre n'éexiste pas soit on a pas le droit a l'accéder.

## Exécuter la requête suivante et copier la réponse : curl https://google.fr

<HTML><HEAD><meta http-equiv="content-type" content="text/html;charset=utf-8">
<TITLE>301 Moved</TITLE></HEAD><BODY>
<H1>301 Moved</H1>
The document has moved
<A HREF="https://www.google.fr/">here</A>.
</BODY></HTML>


## Quel est le code HTTP reçu ? Pouvez-vous expliquer cette réponse ?
301, Permanently redirect status indique que la ressource demandée a été définitivement déplacée vers l'URL donnée par les en-têtes Location dans notre cas : https://www.google.fr/ .

## Comment éviter cette réponse ? Trouvez 2 solutions différentes et détaillez les.
