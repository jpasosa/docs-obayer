---
id: response_front_buy_service
title: FRONT | Respuesta del WS-Calipso al Comprar un servicio
sidebar_label: FRONT | Respuesta del WS-Calipso al Comprar un servicio
---

## Respuesta del WS-Calipso al Comprar servicios desde el panel del usuario.






```
(
    [status] => OK
    [transacid] => V1000100000630A
)

```

## Según nueva lógica utilizada, la respuesta debe ser la siguiente
Aclaración: En una primer etapa del desarrollo para fines prácticos, vamos a estar esperando la devolución del Calipso.
Vamos a ver si se puede manejar el tiempo del calipso.
En la siguiente etapa esta devolución va a ser realizada en segundo plano.


```
[result] => OK   o [result] => ERROR
[transacid] => V1000100000630A
[items] => Array
        (
            [0] => Array
                (
                    [productoid] => 01HOSBONAVA
                    [detalle] => Express - test20mar1726.com (20/03/2019 - 19/04/2019)
                    [cantidad] => 1
                    [precio] => 292.32
                    [importe] => 292.32
                )

        )
[subtotal]  => 102.50
[porc_iva]  => 21
[valor_iva] => 34.45
[porc_imputacion]  => 21
[valor_imputacion] => 34.45
[total]     =>354.23
[id_fact_calipso] =>2343 ( la idea de esto es saber en donde está la factura del calipso, para mostrarla )
```


En caso de que dé error, deberán enviar en un array todos los errores encontrados, solamente para que los loguamos y comprendamos.
En principio cuando suceda un error se va a sincronizar manualmente, es decir se va a entrar al Calipso y/o al WHMCS y se van a modificar las datos manualmente,
intentando dejar asentado cual fue el origen del error, para poder resolver automáticamente más adelante.




