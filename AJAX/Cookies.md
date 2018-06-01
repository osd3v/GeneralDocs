escape() encodeURI() encodeURIComponent()

### escape() / unescape()

Este método retorna un string. Todo los caracteres non-ASCII son reemplazados código %XX, donde %XX es equivalente a la representación del caracterer hexadecimal. Esta en desuso o obsoleto.

Los caracteres con un significado reservado en un URI no se codifican.

### encodeURI() /  decodeURI()

Retorna  un URI codificado. Utilizado para codificar URL, codifica simbolos no permitidos en una URL.  
Los caracteres con un significado reservado en un URI serán codificados.

### encodeURIComponent() / 

Utilizando cuando se codifica parametros de la URL, también se puede codificar una URL. 

El String value de una cookie puede utilizar este método para garantizar que el String no contenga valores no permitidos.

Tabla de simbolos

| Char | encodeURI | encodeURIComponent | escape |
| ---- | --------- | ------------------ | ------ |
| *    | *         | *                  | *      |
| .    | .         | .                  | .      |
| -    | -         | -                  | -      |
| _    | _         | _                  | _      |
|      | ~         | ~                  | %7E    |
| '    | '         | '                  | %27    |
| !    | !         | !                  | %21    |
| (    | (         | (                  | %28    |
| )    | )         | )                  | %29    |
| /    | /         | %2F                | /      |
| +    | +         | %2B                | +      |
|      | @         | %40                | @      |
| ?    | ?         | %3F                | %3F    |
| =    | =         | %3D                | %3D    |
| :    | :         | %3A                | %3A    |
| #    | #         | %23                | %23    |
| ;    | ;         | %3B                | %3B    |
| ,    | ,         | %2C                | %2C    |
| $    | $         | %24                | %24    |
| &    | &         | %26                | %26    |
|      | %20       | %20                | %20    |
| %    | %25       | %25                | %25    |
| ^    | %5E       | %5E                | %5E    |
| [    | %5B       | %5B                | %5B    |
| ]    | %5D       | %5D                | %5D    |
| {    | %7B       | %7B                | %7B    |
| }    | %7D       | %7D                | %7D    |
| <    | %3C       | %3C                | %3C    |
| >    | %3E       | %3E                | %3E    |
| ''   | %22       | %22                | %22    |
|      | %5C       | %5C                | %5C    |
| \|   | %7C       | %7C                | %7C    |
| `    | %60       | %60                | %60    |

### Código para enlistar la tabla de caracteres

```javascript
for(let i=0;i<256;i++)
{ 
    let caracter=String.fromCharCode(i);
    let URIComponent=encodeURIComponent(caracter);
    let URI=encodeURI(caracter);
    let esc=escape(caracter);
    console.log(i+".- "+caracter+" | "+URIComponent+" | "+URI+" | "+esc);    
}
```

