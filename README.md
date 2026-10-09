# Prueba técnica Fullstack Junior — Pymedesk

Aplicación pequeña de gestión de pedidos con Flask, SQLite y JavaScript nativo. Tiempo estimado: **30–45 minutos**. Puedes usar asistentes de IA.

## Preparación

Requiere Python 3.11 o superior. En la raíz del repositorio:

```bash
python -m venv .venv
```

Activa el entorno virtual con `.venv\Scripts\activate` en Windows o `source .venv/bin/activate` en macOS/Linux. Después:

```bash
pip install -r requirements.txt
python seed.py
python app.py
```

Abre <http://127.0.0.1:5000>. El seed se puede ejecutar más de una vez sin duplicar pedidos. La base local se crea en `data/orders.sqlite3` y no se incluye en Git.

## Tu tarea

1. Un pedido cancelado no debe poder pasar a enviado: el servidor debe rechazar la operación y conservar su estado cancelado. Un pedido pendiente sí debe poder pasar a enviado.
2. Cuando falle una actualización, muestra en la interfaz un mensaje visible y comprensible. Actualmente el fallo no se comunica claramente.

Si encuentras algún otro error imprevisto en la aplicación, puedes corregirlo sin necesidad de preguntar. Si no estás seguro de cómo proceder, documenta el problema y tu propuesta de solución en el repositorio.

Mantén la solución pequeña. No se requiere despliegue, documentación extensa ni pruebas automatizadas adicionales.

## API inicial

- `GET /api/orders`: devuelve todos los pedidos.
- `POST /api/orders/<id>/ship`: intenta marcar un pedido como enviado.

## Entrega

Comparte el enlace a tu repositorio con los cambios y un video de **2–4 minutos** donde muestres la aplicación, expliques el problema encontrado, tu solución y cómo comprobaste el resultado. Puedes usar asistentes de IA durante todo el ejercicio.
