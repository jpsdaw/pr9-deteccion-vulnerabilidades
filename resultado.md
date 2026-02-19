# Dependabot

## Vulnerabilidades

- **body-parser vulnerable to denial of service when url encoding is enabled**

La librería body-parser tiene una vulnerabilidad que permite provocar un Denial of Service (DoS) enviando  peticiones especialmente manipuladas cuando el urlencoded parser está activo.

- **Denial-of-Service Memory Exhaustion in qs**

La librería qs (usada para parsear query strings) puede ser explotada para un Denial of Service consumiendo toda la memoria del servidor al procesar entradas maliciosas muy grandes o profundamente anidadas.

- **auth0/node-jws Improperly Verifies HMAC Signature**

La librería node-jws puede validar mal firmas HMAC, lo que permite que un atacante pueda falsificar tokens JSON Web (JWT) y hacer que el servidor los acepte como válidos.

# Renovate
 ## PR'S CREADAS
- Bump @eslint/eslintrc from 3.2.0 to 3.3.3 dependencies javascript

- Bump eslint from 9.16.0 to 10.0.0 dependencies javascript

- Bump express from 4.0.0 to 5.2.1 dependencies javascript

- Bump eslint-plugin-security from 3.0.1 to 4.0.0 dependencies javascript

- Bump mysql from 2.0.1 to 2.18.1 dependencies javascript

- Bump the npm_and_yarn group across 1 directory with 15 updates dependencies javascript

**Estas pull request proponen actualizaciones de dependencias.**

# eslint
**warning Found child_process.exec() with non Literal first argument** security/detect-child-process

Esto significa que estás usando child_process.exec() con un argumento que no es un string literal, es decir, puede venir de entrada externa o variable. Puede haber inyección de comandos.

# SonarQubes

## Problemas detectados

- "Revoke and change this password, as it is compromised" — Password expuesto
- "Change this code to not construct SQL queries directly from user-controlled data" — SQL construido con datos de usuario
- "Change this code to not construct the path from user-controlled data" — Ruta construida con datos de usuario
-  "Prefer `node:child_process` over `child_process`" — Uso de `child_process`
-  "Change this code to not construct the OS command from user-controlled data" — Comando OS construido con datos de usuario

**Todos estos problemas se encuentran en el código, no en librerías externas.**

# npm audit

Es una herramienta de Node.js / npm que revisa las dependencias en busca de vulnerabilidades conocidas.

Aplicamos la corrección con **npm audit fix --force** , corrige la mayoría, aunque queda alguna.

# Preguntas finales 

**Pregunta:** Si quisieras detectar qué librerías o dependencias son vulnerables en tu proyecto, ¿qué herramientas de las estudiadas utilizarías?  
**Respuesta:** `npm audit` o Dependabot.

**Pregunta:** Si quisieras detectar vulnerabilidades en el código propio del proyecto, ¿qué herramientas de las estudiadas utilizarías?  
**Respuesta:** ESLint con reglas de seguridad (`eslint-plugin-security`) o SonarQubes.

