# Sistema-Informatico-Jardineria
## Se pide
Se necesita un formato de archivo para intercambiar productos entre almacenes de productos de jardinería y se desea una DTD que incluya estas restricciones:
Debe haber un elemento raíz pedido que puede constar de plantas, flores y/o utensilios. Los tres elementos pueden aparecer repetidos y en cualquier orden. También pueden aparecer por ejemplo 4 plantas, 2 flores y luego 4 utensilios de nuevo.
- Todo planta tiene un atributo obligatorio nombre.
- Los elementos flores tiene un atributo optativo color.
- Todo elemento utensilio debe tener dentro un elemento obligatorio número.

### Propuesta de xml:
```bash
<?xml version="1.0" encoding="utf-8" standalone="yes"?>
<!DOCTYPE pedido [
    <!ELEMENT plantas (nombre)+ >
        <!ATTLIST nombre (#PCDATA)>
    <!ELEMENT flores (nombre, color?)>
        <!ATTLIST nombre (#PCDATA)>
        <!ATTLIST color (#PCDATA)>
    <!ELEMENT utensilio (numero)>
        <!ATTLIST numero (#PCDATA)>]>      
<pedido>
    <plantas>
        <nombre> "helecho" </nombre>
    </plantas>    
    <flores>
        <nombre> "rosa, gardenia" </nombre>
        <color> "lila, rojo, blanco" </color>
    </flores>    
    <utensilio>
        <numero> 4 </numero>
    </utensilio>
</pedido>    
```
