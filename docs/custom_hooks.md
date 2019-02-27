---
id: custom_hooks
title: Custom Hooks
sidebar_label: Listado Hooks Creadas
---

# Listado de las **hooks** creadas en **WHMCS**

---
### 1. Cliente, no permite modificar su facturación.
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

### 4. Edición de un cliente
> file: includes/hooks/clients.php

> hook: [ClientEdit](https://developers.whmcs.com/hooks-reference/client/#clientedit)

> <a href="http://stash.allytech.com:7990/projects/WHMCS/repos/whmcs-741/browse/includes/hooks/clients.php" target="_blank">Ver código en el repositorio</a>

> Web Service, está apuntando a URL http://ws.allytech.com/public/data-get/edit-client/send para luego desde nuestro web service poder enviar al web service del calipso.

Va a enviar todos los datos cuando se edita el cliente, en principio a nuestro web service (ws.allytech.com), para luego conectarlo contra el web service del calipso.


---

### 5. Validación del Cliente
> file: includes/hooks/clientvalidation.php

> hook: [ClientDetailsValidation](https://developers.whmcs.com/hooks-reference/client/#clientdetailsvalidation)

> <a href="http://stash.allytech.com:7990/projects/WHMCS/repos/whmcs-741/browse/includes/hooks/clientvalidation.php" target="_blank">Ver código en el repositorio</a>


Hace una validación directa en el HOOK de una edición / alta de un nuevo cliente sea a través del ADMIN o del FRONT. Va a estar validando el CUIT verificando el último código directamente, va a validar si el CUIT ya existe dentro de los clientes, va a validar el DNI, el código postal y la provincia, que esté bien escrita. Luego el registro trae validaciones por defecto, y campos que se pueden editar (https://clientes.allytech.com/admally/configcustomfields.php)


---

### 6. Creación de una Factura
> file: includes/hooks/invoices.php

> hook: [InvoiceCreated](https://developers.whmcs.com/hooks-reference/invoices-and-quotes/#invoicecreated)

> <a href="http://stash.allytech.com:7990/projects/WHMCS/repos/whmcs-741/browse/includes/hooks/invoices.php" target="_blank">Ver código en el repositorio</a>


Al generar una factura si es Factura B, modifica manualmente los precios de los ítems.


---
