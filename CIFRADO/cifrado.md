## SISTEMA DE CIFRADO SIMETRICO

Tipo de cifrado que usa una misma clave para cifrar y para descifrar 

* 3DES

* Blowfish

* IDEA

  Un buen sistema de cifrado pone toda la seguridad en la clave y ninguna en el algoritmo. 

##AES (Advanced Encryption Standard)

Esquema de cifrado por bloques, es uno de los algoritmos más usados en la criptografica simetrica.

* Seguridad

* Rendimiento

* Flexibilidad

  NIST(instituto nacional de estandares y tecnologia)

  [Pagina para cifrar AES](https://cifraronline.com/descifrar-aes)

  - Vincent Rijmen

  - Joan Daemen

[Documentación](https://csrc.nist.gov/csrc/media/projects/cryptographic-standards-and-guidelines/documents/aes-development/rijndael-ammended.pdf)





## AES (Cifrado Asimetrico)

trabaja con dos claves diferentes: una pública y privada. Ambos trabajan complementariamente entre sí, lo que significa que un mensaje cifrado con uno de ellos sólo puede ser descifrado por su contraparte. Dado que la clave privada no puede calcularse a partir de la clave publica, esta generalemente disponible para el publico.

En el proceso de firma de un documento, una huella digital cifrada con RSA, se adjunta el archivo, y permite al receptor para verificar tanto el remitente como la integridad del documento. La seguridad de RSA se basa principalmente en el problema matemático de la factorización entera. Un mensaje qu esta a punto de ser cifrado se trata como un gran número. Al cifrar el mensaje, se eleva a la fuerza de la clave, y se divide con el resto por un producto fijo de dos primos. Repitiendo el proceso con la otra clave, el texto sin formato se puede recuperar de nuevo. El mejor método actualmente conocido para romper el cifrado requiere factorizar el producto utilizando la división 

 