---
id: button_whatsapp
title: Botón de WhatsApp
sidebar_label: Botón de WhatsApp
---

## Implementación de boton de WhatsApp
------

Se busca ubicar el boton de whatsapp flotado abajo a la derecha, y que al hacer click envíe mensaje por whatsapp.

Fuente, https://codepen.io/demoonkevin/pen/MvPEpV
Se han modificado algunos valores de la fuente para que funcione correctamente en el proyecto en donde estábamos trabajando que era un Opencart3 con el template Journal2.
Debemos incluir el archivo whatsapp.css en la vista para que agarre bien los estilos.

file: index.html 
```html
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/font-awesome/4.5.0/css/font-awesome.min.css">
<a href="https://api.whatsapp.com/send?phone=51955081075&text=Hola" id="float-whatsapp" target="_blank">
          <i class="fa-1 fa-whatsapp my-float"></i>
</a>
```

file whatsapp.css
```css
#float-whatsapp {
    position:fixed;
    width:60px;
    height:60px;
    bottom:25px;
    right:40px;
    background-color:#25d366;
    color:#FFF;
    border-radius:50px;
    text-align:center;
    font-size:42px;
    box-shadow: 2px 2px 3px #999;
    z-index:100;
}

.my-float {
    margin-top:16px;
}
```


---
