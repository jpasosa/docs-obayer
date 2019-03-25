---
id: response_afip
title: Respuesta del WS-Calipso para que nosotros procesemos datos de la AFIP
sidebar_label: Respuesta del WS-Calipso para que nosotros procesemos datos de la AFIP
---

## Como debe ser la respuesta del WS-Calipso sobre la AFIP.




La respuesta sobre la afip debe ser de la siguiente manera.

```
(
    [resp_afip] => Array
        (
            [result]    => OK
            [FeCabResp] => Array
                (
                    [Cuit] => 30708390174
                    [PtoVta] => 0001
                    [CbteTipo] => 06
                    [FchProceso] => 20181031114917
                    [CantReg] => 1
                    [Resultado] => A
                    [Reproceso] => N
                )

            [FeDetResp] => Array
                (
                    [FECAEDetResponse] => Array
                        (
                            [DocNro] => 30585712937
                            [DocTipo] => 80
                            [Concepto] => 3
                            [CbteDesde] => 12
                            [CbteHasta] => 12
                            [CbteFch] => 20181031
                            [Resultado] => A
                            [CAE] => 68444692438496
                            [CAEFchVto] => 20181110
                        )

                )

            [WsVersion] => wsfev1
        )

)

```

Si hubiera un error en l respuesta de la AFIP y no nos entrega el CAE lo debe tratar Calipso, y su respuesta debe ser:

```
(
    [resp_afip] => Array
        (
            [result]    => ERROR
            [FeCabResp] => Array
                (
                    [Cuit] => 30708390174
                    [PtoVta] => 0001
                    [CbteTipo] => 06
                    [FchProceso] => 20181031114917
                    [CantReg] => 1
                    [Resultado] => A
                    [Reproceso] => N
                )

            [FeDetResp] => Array
                (
                    [FECAEDetResponse] => Array
                        (
                            [DocNro] => 30585712937
                            [DocTipo] => 80
                            [Concepto] => 3
                            [CbteDesde] => 12
                            [CbteHasta] => 12
                            [CbteFch] => 20181031
                            [Resultado] => A
                            [CAE] => 68444692438496
                            [CAEFchVto] => 20181110
                            [Observaciones] =>
                                    [Obs] =>
                                        array (
                                          0 =>
                                          (
                                            'Code' => 10018,
                                            'Msg' => 'Si ImpIva es igual a 0 el objeto Iva y AlicIva son obligatorios. Id iva = 3 (iva 0)',
                                          )
                                        )
                )

            [WsVersion] => wsfev1
        )
)
```


En resumen, si la respuesta de la AFIP es correcta se entrega dentro de un array resp_afip, lo único que se agrega es la clave "result" con valor "OK", si la respuesta de la AFIP fuera incorrecta
también se entrega todos los valores que entregó la AFIP, agregando solamente la clave "result" con valor "ERROR"
