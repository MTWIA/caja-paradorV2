Caja del Parador

Caja para cobrar en el parador de los sábados. Se usa desde el celular, anda aunque se caiga el wifi y todo queda guardado en un Google Sheet.

Link de la caja: https://mtwia.github.io/caja-paradorV2/

Para cobrar (operador)

Entrá con tu usuario y PIN. Tocá Menú o Bebida las veces que pida el cliente y se van sumando al ticket de abajo. Si te pasaste, corregí con − y +. Cuando el cliente paga, tocá Efectivo o Mercado Pago. La venta se registra y el ticket queda en blanco para el siguiente.

Si tocaste el medio de pago equivocado, apretá Deshacer dentro de los 5 segundos. La venta se anula y los productos vuelven al ticket para cobrarla de nuevo.

Para anular una venta más vieja, buscala en la lista de ventas de hoy, tocá la ✕ y volvé a tocar ¿Anular? para confirmar.

Arriba a la derecha ves el estado. "Al día" quiere decir que todo está guardado en el Sheet. Si dice "Subiendo" o "Sin conexión", seguí cobrando tranquilo, todo sube solo cuando vuelve la señal. Con ventas sin subir la app no te deja cerrar sesión.

Para el admin

Además de cobrar, tenés dos pestañas más arriba.

Estadísticas: elegí el período (hoy, 7 días, 30 días, este mes o todo) y ves lo recaudado, la cantidad de ventas, el ticket promedio, efectivo contra Mercado Pago, y el detalle por día, por cajero y por hora. El botón CSV descarga el período completo.

Ajustes: cargás el precio del menú y de la bebida (hacelo antes de abrir la caja) y creás o desactivás usuarios. Para un operador nuevo alcanza con usuario, nombre, rol operador y un PIN de 4 a 8 dígitos. Si alguien se olvida el PIN, editás su usuario y le ponés uno nuevo.

Cuando cambiás un precio, las ventas ya cobradas conservan el precio con el que se hicieron. Los celulares toman el precio nuevo al volver a abrir o refrescar la app.

Si algo falla

Si no podés entrar, revisá el PIN. Después de 5 intentos fallidos el usuario se bloquea 10 minutos. La sesión dura 12 horas, y si se vence solo volvés a entrar, lo pendiente no se pierde. Si una venta no aparece en el Sheet, mirá que arriba no diga "Subiendo".

Detalles técnicos

El front es el index.html de este repo (GitHub Pages) y el backend es Code.gs en Google Apps Script, con un Google Sheet de base de datos (pestañas Ventas, Config y Usuarios). Cada venta tiene un id único, así que un reintento no la duplica. Anular no borra: la fila queda en el Sheet marcada como anulada, con quién la anuló y cuándo.

No subas al repo PIN ni datos del Sheet.
