# Agrovex Comercial

App del sistema comercial de Agrovex (seguimiento, tablero, clientes, pre-visita, cierre del mes y guía de uso).
Se instala en el teléfono como app (PWA), funciona sin señal y guarda los datos en Firebase.

## Archivos
- `index.html`: la app completa.
- `config.js`: configuración de Firebase (pegar los valores del proyecto).
- `manifest.json`, `sw.js`, íconos: instalación en el teléfono y uso sin señal.
- `firestore.rules`: reglas de seguridad para pegar en Firebase (solo los correos del equipo acceden).

## Publicar
1. Subir todos los archivos a la raíz del repositorio.
2. Settings > Pages > Deploy from a branch > `main` / root.
3. La app queda en `https://<usuario>.github.io/<repositorio>/`.

## Firebase (una vez)
1. Crear proyecto en console.firebase.google.com.
2. Agregar app web y copiar la configuración en `config.js`.
3. Authentication > Sign-in method > Correo/contraseña: habilitar.
4. Authentication > Settings > Authorized domains: agregar `<usuario>.github.io`.
5. Firestore Database > Crear (región southamerica-west1, Santiago) > Reglas: pegar `firestore.rules` con los correos del equipo.
6. Authentication > Users: crear el usuario de cada persona (cada uno define su contraseña con "Olvidé mi contraseña").
