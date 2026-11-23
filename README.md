# Encuestas de satisfacción · La Voz del Cliente

Encuestas de satisfacción de **Autocentro Chrysler** (Servicio y Ventas), con su dashboard de resultados y la página para dar seguimiento a las alertas.
Las respuestas se guardan en el Sheet de encuestas y todo se muestra con datos al momento.

---

## 📝 Encuestas para clientes

| Encuesta | Enlace |
|---|---|
| **Servicio** | [Abrir encuesta de Servicio](https://axisautomotivelab.github.io/encuestas-autocentro/encuesta/?encuesta=servicio) |
| **Ventas** | [Abrir encuesta de Ventas](https://axisautomotivelab.github.io/encuestas-autocentro/encuesta/?encuesta=ventas) |

Estos son los enlaces que se envían a los clientes (por ejemplo, desde Momentum).

- Para que el asesor o vendedor ya aparezca seleccionado, añada al final `&rep=` con su nombre. Ejemplo: `...?encuesta=servicio&rep=Jan%20Ortega`
- El enlace de reseña de Google solo se muestra a los clientes con una experiencia positiva. Si la experiencia no fue buena, se genera una alerta para que el equipo llame al cliente.

---

## 📊 Dashboard de resultados

[Abrir el dashboard](https://axisautomotivelab.github.io/encuestas-autocentro/)

- Muestra los resultados de **Servicio** y **Ventas**: satisfacción, respuestas por pregunta, resultados por asesor y vendedor, y un resumen de las alertas.
- Se actualiza al abrirlo, al pulsar **Actualizar** y, si se deja abierto, cada 5 minutos.
- Es de solo lectura.

---

## 🔔 Alertas de encuestas

[Abrir alertas](https://axisautomotivelab.github.io/encuestas-autocentro/alertas/)

Página donde el equipo de La Voz del Cliente da seguimiento a los clientes insatisfechos.

1. Arriba, en **«¿Quién está trabajando las alertas?»**, escoja su nombre. El equipo lo recuerda para las próximas veces.
2. En cada alerta, escriba la nota de seguimiento (contacto realizado, acuerdo, próximo paso) y pulse **Anotar seguimiento**.
3. Cuando el caso esté cerrado, pulse **Marcar como resuelta**.

Cada nota queda con la fecha, la hora y el nombre de quien la escribió, y el nombre también queda en la columna **Agente** del Sheet. Así se sabe quién trabajó cada alerta.

Los nombres de la lista se editan en el Sheet de encuestas, pestaña **Listas**, columna **«Agentes (La Voz del Cliente)»**.

---

## 🔑 Acceso

El dashboard y la página de alertas necesitan una **clave de acceso** al final del enlace (`?key=...`).
Por seguridad, **las claves no se publican aquí**: este repositorio es público y los datos de los clientes son confidenciales.
La administración entrega el enlace completo, con la clave, a cada persona autorizada.

Las encuestas para clientes no necesitan clave.

---

## 🛠️ Para la administración

- Las páginas leen y guardan los datos en la app de Apps Script **Encuestas Chrysler**. Si se cambia su código, hay que publicar una **Nueva versión** (Implementar → Administrar implementaciones → lápiz → Nueva versión). El enlace no cambia.
- Si se cambia el diseño del dashboard o de la encuesta en Apps Script, hay que volver a generar y subir los archivos de este repositorio.
- Estructura del repositorio:
  - `index.html`: dashboard
  - `alertas/index.html`: alertas
  - `encuesta/index.html`: encuesta para clientes
