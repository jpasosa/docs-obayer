---
id: request_admin_cancel_invoice
title: Admin | Cancelar Factura
sidebar_label: Admin | Cancelar Factura
---

## Cancelar la Factura desde el Panel Administrador
------

Vamos a describir cuando cancelamos una factura desde el panel administrador . . .

Pedido que le pasamos al web service del Calipso


```
(
    [tipo] => creditocc
    [cliente] => Array
        (
            [id] => W20065
            [nombre] => Juan Pablo Sosa
            [mail] => juans+clienteivaexento@allytech.com
            [domicilio] => kjhj
            [localidad] => kjh
            [codpostal] => 7474
            [tipoiva] => X
            [provincia] => S
            [DocTipo] => 80
            [idimpositivo] => 30-58571293-7
        )

    [ordenid] => 1204
    [total] => 364.68
    [descuentogeneral] => 0
    [observacion] => observaciones de la factura
    [PtoVta] => 1
    [CbteTipo] => 8
    [FchProceso] => 20190320171150
    [CantReg] => 1
    [Resultado] => A
    [Reproceso] => N
    [Concepto] => 3
    [CbteDesde] => 8
    [CbteHasta] => 8
    [CbteFch] => 20190320
    [CAE] => 69124733689830
    [CAEFchVto] => 20190330
    [WsVersion] => wsfev1
    [items] => Array
        (
            [0] => Array
                (
                    [productoid] => 01HOSBONAVA
                    [detalle] => Express - test01nov20181934.com (01/11/2018 - 30/11/2018)
                    [cantidad] => 1
                    [precio] => 284.20
                    [importe] => 284.20
                )

            [1] => Array
                (
                    [productoid] => HOSPAGDIF
                    [detalle] => Cargo por demora (Agregar 04/11/2018)
                    [cantidad] => 1
                    [precio] => 17.19
                    [importe] => 17.19
                )

        )

)
```



Nueva lógica para cancelación de la factura.

```
(
    [tipo] => creditocc
    [cliente] => Array
        (
            [id] => W20065
            [nombre] => Juan Pablo Sosa
            [mail] => juans+clienteivaexento@allytech.com
            [domicilio] => kjhj
            [localidad] => kjh
            [codpostal] => 7474
            [tipoiva] => X
            [provincia] => S
            [DocTipo] => 80
            [idimpositivo] => 30-58571293-7
        )

    [ordenid] => 1204
    [total] => 364.68
    [descuentogeneral] => 0
    [observacion] => observaciones de la factura
    [items] => Array
        (
            [0] => Array
                (
                    [productoid] => 01HOSBONAVA
                    [detalle] => Express - test01nov20181934.com (01/11/2018 - 30/11/2018)
                    [cantidad] => 1
                    [precio] => 284.20
                    [importe] => 284.20
                )

            [1] => Array
                (
                    [productoid] => HOSPAGDIF
                    [detalle] => Cargo por demora (Agregar 04/11/2018)
                    [cantidad] => 1
                    [precio] => 17.19
                    [importe] => 17.19
                )

        )

)
```