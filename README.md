# Arcturus Murphy

**Arcturus Murphy** es un fork privado de Arcturus Emulator desarrollado con fines educativos y de aprendizaje.  
Basado originalmente en Arcturus Emulator de TheGeneral y adaptado/modificado para uso personal y privado.

Este proyecto **no tiene fines de lucro** y no está destinado a distribución pública o comercial.

Compatible con revisiones modernas y proyectos de comunidad como:

| Community Clients | Cliente |
| ----------------- | -------- |
| Nitro Client | https://github.com/billsonnn/nitro-react |

---

# Proyecto Privado

Arcturus Murphy es un proyecto privado mantenido únicamente para desarrollo, pruebas y mejoras internas.

- ? No se ofrece soporte público.
- ? No se aceptan contribuciones externas.
- ? No se garantiza estabilidad.
- ? Uso exclusivamente personal y educativo.

---

# Conexión

Se recomienda utilizar el plugin de Websocket.

## ¿Cómo conectarme usando Secure WebSockets (WSS)?

Existen varias formas de habilitar soporte WSS para tu servidor websocket.

### Opción 1 — Certificados locales

Puedes agregar tu certificado SSL y key en las siguientes rutas:

```txt
/ssl/cert.pem
/ssl/privkey.pem
```

> Nota: Los clientes Nitro no aceptan certificados autofirmados.  
> Se recomienda usar certificados válidos emitidos por una CA como Let's Encrypt.

---

### Opción 2 — Proxy con Cloudflare o Nginx (Recomendado)

También puedes utilizar Cloudflare o Nginx para proxyear conexiones WSS.

> Nota: Si utilizas proxy, deberás configurar:

```txt
ws.nitro.ip.header
```

Para que el emulador pueda obtener la IP real del usuario.

---

# Proxy WSS con Cloudflare

Asegúrate de utilizar un puerto compatible con HTTPS Proxy de Cloudflare.

Puertos compatibles actualmente:

- 443
- 2053
- 2083
- 2087
- 2096
- 8443

Luego:

1. Crea un subdominio para websocket.
2. Activa el proxy de Cloudflare (nube naranja).
3. Apunta el registro A a la IP del VPS.
4. Desactiva SSL en las reglas de página para el subdominio websocket.

Ejemplo:

```txt
wss://ws.tudominio.com:2096
```

---

# Ramas

| Rama | Descripción |
| ---- | ------------ |
| master | Versión principal estable para uso diario. |
| dev | Versión experimental con nuevas funciones y posibles errores. |

No existe un calendario definido para actualizaciones o nuevas versiones.

---

# Base de Datos

Puedes utilizar cualquier database compatible con Arcturus/Nitro.

Después de importar la base de datos, asegúrate de ejecutar:

```txt
UpdateDatabase.sql
```

Para aplicar las últimas modificaciones necesarias.

---

# Sistema de Plugins

Arcturus Murphy mantiene el robusto sistema de plugins original de Arcturus Emulator.

Esto permite:

- Crear funcionalidades personalizadas.
- Añadir eventos propios.
- Modificar comportamientos sin editar el core.
- Mantener compatibilidad y organización del proyecto.

---

# Soporte

Este proyecto es privado y no posee soporte oficial.

---

# Créditos

## Proyecto Original
- TheGeneral — Arcturus Emulator

## Inspiraciones y forks
- Krews — Morningstar Extended
- Comunidad Arcturus
- Comunidad Nitro

---

# Licencia

Arcturus Murphy respeta los créditos originales y sus respectivas licencias.

Este fork es utilizado únicamente con fines educativos y de desarrollo privado.