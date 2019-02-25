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

### 3. Alta de un cliente
> file: includes/hooks/clients.php

> hook: [ClientAdd](https://developers.whmcs.com/hooks-reference/client/#clientadd)

> <a href="http://stash.allytech.com:7990/projects/WHMCS/repos/whmcs-741/browse/includes/hooks/clients.php" target="_blank">Ver código en el repositorio</a>

> Web Service, está apuntando a URL http://ws.allytech.com/public/data-get/new-client/send para luego desde nuestro web service poder enviar al web service del calipso.

Va a enviar todos los datos del nuevo cliente, en principio a nuestro web service (ws.allytech.com), para luego conectarlo contra el web service del calipso.


---
