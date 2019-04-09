---
id: request_pedido_wan
title: Pedido entero al WAN
sidebar_label: Pedido entero al WAN
---

## Esto es todo lo que trae actualmente para armar el pedido al WAN

Esto lo trae de la siguiente manera en archivo app/Http/Controllers/PaymentController.php
```php
$data_to_wswan['invoice']   = $this->invoice;
$data_to_wswan['cliente']   = $this->client;
$data_to_wswan['resp_afip'] = $resp_afip;
$data_to_wswan['transaction'] = $transactions;
```

Describo las cuatro


```
(
    [invoice] => Array
        (
            [result] => success
            [invoiceid] => 1349
            [invoicenum] =>
            [userid] => 191
            [date] => 2019-02-04
            [duedate] => 2019-02-04
            [datepaid] => 0000-00-00 00:00:00
            [lastcaptureattempt] => 0000-00-00 00:00:00
            [subtotal] => 292.32
            [credit] => 0.00
            [tax] => 0.00
            [tax2] => 0.00
            [total] => 292.32
            [balance] => 292.32
            [taxrate] => 0.00
            [taxrate2] => 0.00
            [status] => Unpaid
            [paymentmethod] => payinoffice
            [notes] =>
            [ccgateway] =>
            [items] => Array
                (
                    [item] => Array
                        (
                            [0] => Array
                                (
                                    [id] => 3058
                                    [type] => Hosting
                                    [relid] => 1320
                                    [description] => Express - test04feb1417.com (04/02/2019 - 03/03/2019)
                                    [amount] => 292.32
                                    [taxed] => 1
                                )

                        )

                )

            [transactions] =>
        )

    [cliente] => Array
        (
            [result] => success
            [userid] => 191
            [id] => 191
            [uuid] => 3ea6cbfd-2ddd-4aa8-8d9a-3cc7ccc4b4c1
            [firstname] => juan Pablo Testothercountry
            [lastname] => Sosa
            [fullname] => juan Pablo Testothercountry Sosa
            [companyname] => sadas
            [email] => juans+test25ene0949-other-country@allytech.com
            [address1] => asdasd
            [address2] => asd
            [city] => asdasd
            [fullstate] => MG
            [state] => MG
            [postcode] => 8383
            [countrycode] => BR
            [country] => BR
            [phonenumber] => 233323232323
            [password] => $2y$10$CjRqbUkdHKM5HoDRqFb92uWiRHueloRNf/24rJtCgWbjSsS9N0bQa
            [statecode] => MG
            [countryname] => Brazil
            [phonecc] => 55
            [phonenumberformatted] => +55.233323232323
            [telephoneNumber] => +55.233323232323
            [billingcid] => 0
            [notes] =>
            [twofaenabled] =>
            [currency] => 2
            [defaultgateway] =>
            [cctype] =>
            [cclastfour] =>
            [gatewayid] =>
            [securityqid] => 1
            [securityqans] => asdasd
            [groupid] => 0
            [status] => Inactive
            [credit] => 0.00
            [taxexempt] => 1
            [latefeeoveride] =>
            [overideduenotices] =>
            [separateinvoices] =>
            [disableautocc] =>
            [emailoptout] =>
            [overrideautoclose] =>
            [allowSingleSignOn] => 1
            [language] =>
            [lastlogin] => Date: 04/02/2019 14:15<br>IP Address: 190.210.152.178<br>Host: customer-static-210-152-178.iplannetworks.net
            [customfields1] => W20086
            [customfields] => Array
                (
                    [0] => Array
                        (
                            [id] => 1
                            [value] => W20086
                        )

                    [1] => Array
                        (
                            [id] => 16
                            [value] => 55000000050
                        )

                    [2] => Array
                        (
                            [id] => 17
                            [value] =>  Exportación
                        )

                    [3] => Array
                        (
                            [id] => 18
                            [value] => CUIT
                        )

                    [4] => Array
                        (
                            [id] => 19
                            [value] =>
                        )

                )

            [customfields2] => 55000000050
            [customfields3] =>  Exportación
            [customfields4] => CUIT
            [customfields5] =>
            [currency_code] => ARS
            [client] => Array
                (
                    [userid] => 191
                    [id] => 191
                    [uuid] => 3ea6cbfd-2ddd-4aa8-8d9a-3cc7ccc4b4c1
                    [firstname] => juan Pablo Testothercountry
                    [lastname] => Sosa
                    [fullname] => juan Pablo Testothercountry Sosa
                    [companyname] => sadas
                    [email] => juans+test25ene0949-other-country@allytech.com
                    [address1] => asdasd
                    [address2] => asd
                    [city] => asdasd
                    [fullstate] => MG
                    [state] => MG
                    [postcode] => 8383
                    [countrycode] => BR
                    [country] => BR
                    [phonenumber] => 233323232323
                    [password] => $2y$10$CjRqbUkdHKM5HoDRqFb92uWiRHueloRNf/24rJtCgWbjSsS9N0bQa
                    [statecode] => MG
                    [countryname] => Brazil
                    [phonecc] => 55
                    [phonenumberformatted] => +55.233323232323
                    [telephoneNumber] => +55.233323232323
                    [billingcid] => 0
                    [notes] =>
                    [twofaenabled] =>
                    [currency] => 2
                    [defaultgateway] =>
                    [cctype] =>
                    [cclastfour] =>
                    [gatewayid] =>
                    [securityqid] => 1
                    [securityqans] => asdasd
                    [groupid] => 0
                    [status] => Inactive
                    [credit] => 0.00
                    [taxexempt] => 1
                    [latefeeoveride] =>
                    [overideduenotices] =>
                    [separateinvoices] =>
                    [disableautocc] =>
                    [emailoptout] =>
                    [overrideautoclose] =>
                    [allowSingleSignOn] => 1
                    [language] =>
                    [lastlogin] => Date: 04/02/2019 14:15<br>IP Address: 190.210.152.178<br>Host: customer-static-210-152-178.iplannetworks.net
                    [customfields1] => W20086
                    [customfields] => Array
                        (
                            [0] => Array
                                (
                                    [id] => 1
                                    [value] => W20086
                                )

                            [1] => Array
                                (
                                    [id] => 16
                                    [value] => 55000000050
                                )

                            [2] => Array
                                (
                                    [id] => 17
                                    [value] =>  Exportación
                                )

                            [3] => Array
                                (
                                    [id] => 18
                                    [value] => CUIT
                                )

                            [4] => Array
                                (
                                    [id] => 19
                                    [value] =>
                                )

                        )

                    [customfields2] => 55000000050
                    [customfields3] =>  Exportación
                    [customfields4] => CUIT
                    [customfields5] =>
                    [currency_code] => ARS
                )

        )

    [resp_afip] => Array
        (
            [FeCabResp] => Array
                (
                    [Cuit] => 30708390174
                    [PtoVta] => 5
                    [CbteTipo] => 51
                    [FchProceso] => 20190204141807
                    [CantReg] => 1
                    [Resultado] => A
                    [Reproceso] => N
                )

            [FeDetResp] => Array
                (
                    [FECAEDetResponse] => Array
                        (
                            [Concepto] => 3
                            [DocTipo] => 80
                            [DocNro] => 55000000050
                            [CbteDesde] => 82
                            [CbteHasta] => 82
                            [CbteFch] => 20190204
                            [Resultado] => A
                            [CAE] => 69054725811643
                            [CAEFchVto] => 20190214
                            [Observaciones] => Array
                                (
                                    [Obs] => Array
                                        (
                                            [0] => Array
                                                (
                                                    [Code] => 10017
                                                    [Msg] => Factura individual, DocTipo: 80, DocNro 55000000050 no se encuentra registrado en los padrones de AFIP o se encuentra inactivo.
                                                )

                                        )

                                )

                        )

                )

            [WsVersion] => wsfev1
        )
        [transaction] => Array
                (
                    [0] => Array
                        (
                            [id] => 1129
                            [userid] => 2
                            [currency] => 0
                            [gateway] => payu
                            [date] => 2018-12-28 14:48:53
                            [description] => Invoice Payment
                            [amountin] => 364.68
                            [fees] => 0.00
                            [amountout] => 0.00
                            [rate] => 1.00000
                            [transid] => 28/12/2018
                            [invoiceid] => 1272
                            [refundid] => 0
                        )

                )

)
```