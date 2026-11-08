# Proceso de venta completo: del presupuesto a la factura
## Paso a paso
### 1. Creación del Presupuesto
* __Usuario:__ Comercial Juan
* __Acción:__ Crea el presupuesto para Little Inc con tres líneas de producto (incluyendo un pantalón de felpa con un 20% de descuento, una chaqueta de punto y el envío), configurando la fecha de validez y el plazo de pago. Se exporta el documento en PDF.
* __Referencia:__ `S00026`
* __Estado:__ Presupuesto.

### 2. Confirmación a Pedido de Venta
* __Usuario:__ Responsable Fernando
* __Acción:__ Tras la aceptación del presupuesto, se accede a él y se pulsa el botón Confirmar, convirtiéndolo formalmente en un pedido de venta y generando la orden de salida en el inventario.
* __Referencia:__ `S00026`
* __Estado:__ Pedido de Venta.

### 3. Validación de la Orden de Entrega en Inventario
* __Usuario:__ Responsable Fernando
* __Acción:__ Se accede al módulo de Inventario para procesar la salida de mercancía. Verificamos que la cantidad coincide con la pedida (en este caso es 1 unidad de cada producto pedido) y se valida la transferencia, comprobando que el stock en el sistema disminuye.
* __Referencia:__ `PT_IN/OUT/00002`
* __Estado:__ Hecho.

### 4. Facturación y Registro del Pago
* __Usuario:__ Facturación Eloy
* __Acción:__ Se crea una factura a partir del pedido de `S00026`. Se revisan las líneas, se __publica__ la factura y se registra el cobro mediante el botón de pago.
* __Referencia:__ `INV/2026/00011`
* __Estado:__ Pagado.

### 5. Estado Final
* __Usuario:__ Eloy Jiménez Medina
* __Acción:__ Al volver a consultar el pedido de venta original (`S00026`), se comprueba visualmente que el indicador de facturación se encuentra completo al 100% (__Facturado__).