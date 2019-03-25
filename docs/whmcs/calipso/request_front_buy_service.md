---
id: request_front_buy_service
title: FRONT | Comprar un servicio
sidebar_label: FRONT | Comprar un servicio
---

## Coprar servicios desde el panel del usuario.


Vamos a describir cuando compramos servicio/s desde el panel del usuario . . .



Pedido que envíamos al web service del Calipso al comprar un servicio desde el panel del usuario

```
(
    [tipo] => facturacc
    [cliente] => Array
        (
            [id] => WH018657
            [nombre] => Juan Pablo Sosa
            [mail] => juanpablososa@gmail.com
            [domicilio] => Lopez y Planes 6081
            [localidad] => asd
            [codpostal] => 2323
            [tipoiva] => C
            [provincia] => B
            [DocTipo] => 80
            [idimpositivo] => 20-27861007-2
        )

    [ordenid] => 1428
    [total] => 353.71   // el total lo debería calcular calipso, dependiendo de tipo de
                        // factura y sumando los valores de los ítems que si le pasamos.
                        // acá lo que tenemos que decidir es quien prioriza los
                        // valores de los servicios.
    [descuentogeneral] => 0
    [observacion] => observaciones de la factura
    [PtoVta] => 1 // esto con la nueva logica no deberiamos pasar por que lo maneja Calipso
    [CbteTipo] => 1 // esto con la nueva logica no deberiamos pasar por que lo maneja Calipso
    [FchProceso] => 20190320172653 // esto con la nueva logica no deberiamos pasar por que lo maneja Calipso
    [CantReg] => 1 // esto con la nueva logica no deberiamos pasar por que lo maneja Calipso
    [Resultado] => A // esto con la nueva logica no deberiamos pasar por que lo maneja Calipso
    [Reproceso] => N // esto con la nueva logica no deberiamos pasar por que lo maneja Calipso
    [Concepto] => 3 // esto con la nueva logica no deberiamos pasar por que lo maneja Calipso
    [CbteDesde] => 629 // esto con la nueva logica no deberiamos pasar por que lo maneja Calipso
    [CbteHasta] => 629 // esto con la nueva logica no deberiamos pasar por que lo maneja Calipso
    [CbteFch] => 20190320 // esto con la nueva logica no deberiamos pasar por que lo maneja Calipso
    [CAE] => 69124733690326 // esto con la nueva logica no deberiamos pasar por que lo maneja Calipso
    [CAEFchVto] => 20190330 // esto con la nueva logica no deberiamos pasar por que lo maneja Calipso
    [WsVersion] => wsfev1 // esto con la nueva logica no deberiamos pasar por que lo maneja Calipso
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

    [cobros] => Array
        (
            [0] => Array
                (
                    [tipoid] =>
                    [importe] => 0
                    [num_ref] => 0
                    [valor] => 0
                )

        )

)

```