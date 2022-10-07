https://forensiksoft.com/email-forensics.html
1:
El primer punto en el que tenemos que prestar atención es la dirección de correo electrónico del remitente, ya que existen varias técnicas que persiguen hacer creer que un correo electrónico proviene de una fuente legítima y confiable, cuando en realidad no lo es.

La más simple consiste en mandar un correo en el que el nombre del remitente parezca confiable.

Facebook <johndoe@fakedomain.com>
Action de sécurité requise
To: your@gmail.com

2:

Una variación de la técnica anterior consiste en mandar un correo en el que el nombre del remitente sea el e-mail de una cuenta de correo confiable.

security@facebook.com <spookycactus@mydarkemail.com>
Action de sécurité requise
To: your@gmail.com

3:

Otra técnica muy común consiste en mandar el correo desde una cuenta de correo similar a un servicio legítimo.
 
Twitter <security@twittter.com>
Password changed
To: your@gmail.com

4:

Otra técnica utilizada consiste en mandar un correo desde una cuenta de correo legítima, pero poniendo en la cabecera "Reply-To" una cuenta controlada por el atacante. De esta manera, cuando se clicke en responder al correo electrónico, la apicación de correo electrónico, por defecto, pondrá como destinatario el e-mail que aparece en la cabecera "Reply-To" y no el de la cabecera "From".

To: andrew.tennat@capsulecorp.com
From: "Phoebe Larson" <phoebe.larson@capsulecorp.com>
Reply-To: "Phoebe Larson" <phoebelarson9981@protonmail.com>

5:

El segundo punto en el que tenemos que prestar atención es si el cuerpo del correo electrónico incluye algún enlace a una web externa. La utilización de HTML para la construcción de mensajes de correo electrónico permite la creación de enlaces mediante la etiqueta <A HREF>. Para construir el enlace, hace falta el texto donde se clickará para acceder al enlace y la URL de la web a la que se desea acceder. Por ejemplo:

<p><a href="https://givemeallyourdataforfree.net">https://www.thebank.com/security/changepassword</a></p>

6:

NOTA IMPORTANTE: nunca se debe clickar sobre un acortador de URL si no tiene la certeza absoluta de que es totalmente fiable. Existen servicios en Internet que te permiten mostrar una previsualización de la web destino antes de acceder a la misma.
Para ver el redirecionamiento sin ir a la página del atacante, agregar + al final: https://bit.ly/3nlsrcx+
Otra manera: `curl https://bit.ly/3nlsrcx -I -s | grep 'location:'`

<p><a href="https://bit.ly/3nlsrcx">https://www.thebank.com/security/changepassword</a></p>

7:

El método clásico utilizado por los atacantes es incluir un fichero ejecutable (.exe)
NOTA IMPORTANTE: Virtualizar a la hora de descargar y manipular los archivos del mail
changePassowrd.exe

8:

Engañando con un icono y nombre:
image.jpg.exe

9:

El método clásico utilizado por los atacantes es incluir un fichero ejecutable (.exe) como adjunto a un correo. Debido a que hoy en día cualquier solución antispam dispone de mecanismos para bloquear estos correos, el atacante puede mejorar la técnica utilizada y comprimir el fichero ejecutable en un fichero .zip para que el antivirus y filtros antispam de la víctima no pueda analizarlo.

10:

Debido a que hoy en día cualquier solución antispam dispone de mecanismos para bloquear estos correos, el atacante puede mejorar la técnica utilizada y comprimir el fichero ejecutable en un fichero .zip para que el antivirus y filtros antispam de la víctima no pueda analizarlo.