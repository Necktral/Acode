# Visión y límites v0.1

## Contexto del problema
Los supermercados requieren un control eficiente del inventario para evitar pérdidas por caducidad, mala gestión de lotes o faltantes de productos. Usualmente, la falta de una herramienta clara dificulta el seguimiento y la toma de decisiones rápidas.

## Objetivo del producto
Construir una aplicación de inventario para supermercado que registre productos, movimientos, gestión de lotes y fechas de vencimiento, capaz de escalar para varios usuarios, pero empezando con una operación monousuario.

## Usuarios y roles
- Administrador de inventario (v0.1): Un solo usuario en la primera versión, con capacidad de registrar, editar y consultar movimientos.
- Futuro: usuarios múltiples con distintos roles (ej: operadores y administradores).

## Alcance v0.1
- Registro de productos.
- Control de movimientos: entrada, salida y ajuste.
- Gestión de lotes para cada producto (con fechas de vencimiento).
- Consulta de existencias por producto y lote.
- Generación de reportes: kardex, stock actual.
- Soporte básico multiusuario (estructura prevista, aunque sólo se opera como monousuario inicialmente).

## Fuera de alcance v0.1
- Integraciones con sistemas de facturación o POS.
- Funcionalidad multiusuario completa (roles, permisos y sesiones avanzadas).
- Alertas avanzadas o notificaciones automáticas.
- Operación offline prolongada (requiere conexión para sincronización).
- Soporte para diferentes monedas.

## Suposiciones
- El primer usuario será administrador.
- Todos los movimientos afectan inmediatamente el inventario.
- El uso principal es en Nicaragua, moneda en córdobas.

## Riesgos
- Error humano en el registro manual de entradas/salidas/lotes y vencimientos.
- Uso monousuario puede generar confusión con datos multiusuario en el futuro si no se manejan correctamente los permisos.
- La omisión de lotes/vencimientos puede seguir ocurriendo si no se obliga su registro.

## Criterio de éxito v0.1 (medible)
- Todas las operaciones básicas de entrada y salida de inventario registran lote y vencimiento.
- El inventario se puede consultar por producto, lote y vencimiento.
- Kardex y stock actual disponibles en pantalla y exportables.