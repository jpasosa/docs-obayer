---
id: response_admin_add_pay
title: ADMIN | Respuesta del WS-Calipso al pagar desde el panel Administrador
sidebar_label: ADMIN | Respuesta del WS-Calipso al pagar desde el panel Administrador
---

## Respuesta del WS-Calipso al Pagar desde el panel Administrador servicios desde el panel del usuario.






```
(
    [status] => OK
    [registros] => 1
    [transacid] => 100125825
)

```


## Según nueva lógica utilizada, la respuesta debe ser la siguiente
Aclaración: En la parte del ADMIN vamos a esperar el tiempo necesario hasta la devolución del Calipso.


```
[result] => OK   o [result] => ERROR
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
