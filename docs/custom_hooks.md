---
id: custom_hooks
title: Custom Hooks
sidebar_label: Hooks creadas
---

# Listado de las **hooks** creadas en **WHMCS**

---
### 1. Edición del cliente
> file: includes/hooks/client.edit.account.php

> hook: ClientAreaFooterOutput

> <a href="http://stash.allytech.com:7990/projects/WHMCS/repos/whmcs-741/browse/includes/hooks/client.edit.account.php" target="_blank">Ver código en el repositorio</a>

Es un script en JS para que el cliente no pueda modificar el tipo de facturación. Si quisiera cambiar este dato debe enviar un email a info@allytech.com, solicitando el cambio de facturación, e internamente se debería crear un cliente nuevo con otro tipo de facturación.

---


### 2. Variables personalizadas al área del cliente
> file: includes/hooks/clientareainvoices.php

> hook: [ClientAreaPageInvoices](https://developers.whmcs.com/hooks-reference/client-area-interface/#clientareapageinvoices)

> <a href="http://stash.allytech.com:7990/projects/WHMCS/repos/whmcs-741/browse/includes/hooks/clientareainvoices.php" target="_blank">Ver código en el repositorio</a>


Estamos pasando por medio de los archivos de los lenguajes, los estados de las facturas. Por ejemplo "pagar", "pagada", "cancelada", etc.

---
