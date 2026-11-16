# OpoQuest ⚡ — Tu rutina como un juego

Aplicación web para organizar el día como un juego: tareas, plan semanal del preparador, hábitos, límites (tabaco, fiesta, redes…), castigos, dinero, tienda de skins, ligas semanales y ranking entre colegas.

Funciona en el navegador del móvil o del ordenador, y se puede **instalar como una app** en la pantalla de inicio. No necesita servidor ni base de datos.

---

## 🚀 Publicarla en GitHub Pages (5 minutos)

1. Entra en [github.com](https://github.com) y crea un repositorio nuevo (por ejemplo `opoquest`). Márcalo como **Public**.
2. Pulsa **"uploading an existing file"** (o *Add file → Upload files*).
3. Arrastra **todo el contenido de esta carpeta** (`index.html`, `manifest.webmanifest`, `sw.js`, `README.md`, `.nojekyll` y la carpeta `icons`). Importante: sube los archivos, no la carpeta que los contiene.
4. Pulsa **Commit changes**.
5. Ve a **Settings → Pages**. En *Source* elige **Deploy from a branch**, rama **main** y carpeta **/ (root)**. Guarda.
6. En 1–2 minutos tendrás la app en:
   `https://TU-USUARIO.github.io/opoquest/`

Ese es el enlace que le pasas a tu cliente.

> Si los archivos `.nojekyll` no se ven al arrastrar (son ocultos), no pasa nada: la app funciona igual.

---

## 📲 Instalarla en el móvil

**Android (Chrome):** abre el enlace → menú ⋮ → **Instalar aplicación** (o *Añadir a pantalla de inicio*).

**iPhone (Safari):** abre el enlace → botón **Compartir** → **Añadir a pantalla de inicio**.

Una vez instalada se abre a pantalla completa, con su propio icono, y funciona sin conexión.

---

## 🔔 Avisos

Dentro de la app: **Liga → Perfil → 🔔 Activar avisos** y aceptar el permiso.

- Los avisos (tareas, agua, salir de casa, cierre del día, plan del domingo…) saltan mientras la app está abierta o en segundo plano reciente.
- En iPhone los avisos solo funcionan con la app **instalada** en la pantalla de inicio (iOS 16.4 o superior).
- Para avisos con la app totalmente cerrada haría falta un servidor de notificaciones push (posible ampliación futura).

---

## 💾 Datos

- Todo se guarda **en el propio dispositivo** (navegador). No se envía nada a ningún servidor.
- Si se borra el historial/datos del navegador, se pierden: usa **Liga → Perfil → 💾 Copia de seguridad** de vez en cuando y guarda el texto.
- Para pasar los datos a otro móvil: copia de seguridad en uno → **📂 Restaurar** en el otro.

---

## 🏆 Ranking

- **Colegas:** cada persona pulsa *📤 Mi código* y lo envía por WhatsApp; los demás lo añaden con *🤝 Añadir colega*. Para actualizar los puntos, se vuelve a mandar el código.
- **Mundial:** en esta versión los rivales son simulados (marcados con 🤖). Un ranking mundial real requiere un servidor propio.

---

## 📥 Formato del plan semanal

Una tarea por línea:

```
DÍA HORA MINUTOS Título #tipo !
```

- Días: `LUN MAR MIE JUE VIE SAB DOM`
- Tipos: `#estudio #test #repaso #coche #gym #otro`
- `!` al final = tarea **agrandada** (doble XP, doble castigo)

Ejemplo:

```
LUN 09:00 120 Tema 9 · Ley 39/2015 #estudio !
LUN 16:00 45 Test tema 8 #test
SAB 10:00 180 Simulacro oficial #test !
```

También acepta un `.json` con objetos `{ "dia": "lun", "hora": "09:00", "min": 120, "titulo": "...", "tipo": "estudio", "agrandada": true }`.

---

## 🛠️ Actualizar la app

Sustituye `index.html` en el repositorio por la versión nueva (*Add file → Upload files*). Los usuarios reciben la actualización al volver a abrirla; sus datos se conservan.
