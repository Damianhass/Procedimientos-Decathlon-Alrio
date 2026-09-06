# Procedimientos de tienda · Decathlon

Manual de procedimientos y evaluaciones para el equipo de tienda.

| Página | Qué es |
|---|---|
| `index.html` | Portada con los dos accesos |
| `manual.html` | Los tres manuales de repaso: recepción de mercadería, cambios y reclamos de averías, e inventarios cíclicos |
| `evaluacion.html` | Las tres evaluaciones de 10 preguntas, de a una por vez |

## Publicarlo en GitHub Pages

1. Creá un repositorio nuevo y subí estos cuatro archivos a la raíz.
2. En el repo: **Settings → Pages**.
3. En *Source* elegí **Deploy from a branch**, rama `main` y carpeta `/ (root)`.
4. Guardá. En un par de minutos queda publicado en
   `https://<tu-usuario>.github.io/<nombre-del-repo>/`

Ese link es el que compartís con el equipo.

## Cómo funciona

- **Manual**: tres solapas, una por procedimiento. Se lee bajando, sin deslizar.
- **Evaluación**: pide nombre y universo antes de empezar. Después van las 10 preguntas
  de a una, con corrección al instante y el porqué de cada respuesta. Al final muestra el
  puntaje, marca aprobado desde el 80% y lista las preguntas que se erraron.

### Resultados

Al terminar, la persona puede:

- **Copiar resultado** — texto listo para pegar en WhatsApp.
- **Enviar por mail** — abre el correo ya escrito a `damian.hassan.partner@decathlon.com`.

Para cambiar esa dirección, editá la primera línea de la configuración en `evaluacion.html`:

```js
const DESTINO_MAIL = "damian.hassan.partner@decathlon.com";
```

Si querés que los resultados se registren solos en vez de llegar por mail, hace falta un
backend (un formulario de Google, una hoja de cálculo conectada o similar). El código ya
tiene el punto donde engancharlo: la función `guardar()` en `evaluacion.html`.

## Editar el contenido

Todo está en un solo archivo por página, sin librerías ni dependencias.

- Los manuales están en el objeto `MP` dentro de `manual.html`.
- Las preguntas están en el objeto `EV` dentro de `evaluacion.html`. Cada una es
  `{ q: pregunta, o: [opciones], c: índice de la correcta, e: explicación }`.

Los universos que aparecen en el desplegable están en la constante `UNIVERSOS`.

## Notas de contenido

- Los **elementos de protección** (cascos, rodilleras, pecheras) no se cambian ni se
  devuelven **por seguridad**: fuera de la tienda no hay forma de saber si recibieron un
  golpe, y un golpe que no se ve puede dejarlos sin capacidad de protección. La única
  excepción es el defecto de fábrica.
- Los **trajes de baño** sí se aceptan para cambio, siempre que estén sin uso, con
  etiquetas y empaque original.

---

Documento de uso interno · Tienda
