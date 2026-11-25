# Esquema de la tabla acondicionada

**Fuente:** hoja *Registros* y catálogos entregados por FEMSA (socio formador).
**Granularidad:** una fila por línea de documento contable.

| Campo | Uso en el modelo dimensional |
|---|---|
| Fecha contable | Dim_Fecha (rol contable) |
| Fecha de creación | Dim_Fecha (rol creación) |
| Código de sociedad, sociedad, país, moneda | Dim_Sociedad |
| Número de cuenta, descripción, rubro, tipo, naturaleza | Dim_Cuenta |
| Tipo de documento, origen | Dim_TipoDocumento |
| Usuario, área, sociedad asignada, estatus, fecha de baja, tipo de usuario | Dim_Usuario |
| Código de transacción | Dim_Transaccion |
| Indicador cargo/abono (S/H), tipo de captura (A/M) | Dim_Indicadores |
| Número de documento, número de línea, posición | Fact_RegistroDiario (dimensiones degeneradas) |
| Importe MXP, importe moneda documento, tipo de cambio, cantidad | Fact_RegistroDiario (medidas) |
