# Ethical Hacking: Fundamentos y Metodologías

🌐 [Inglés](README.md) | [Español](README.es.md) | [Volver](https://github.com/martinmorente-dev/Ethical-Hacker)

## ¿Qué es el hacking ético?

Un hacker ético actúa como atacante para evaluar la postura de seguridad de una red o sistema y **minimizar el riesgo**. Usa las mismas herramientas que un atacante malicioso, pero con **permiso explícito** (el *alcance* o *scope* de la prueba) y reporta los hallazgos al cliente o proveedor.

- **Ético:** tiene permiso y divulga de forma responsable las vulnerabilidades.
- **No ético:** tiene intención maliciosa, accede sin autorización o divulga públicamente sin coordinar con el proveedor.
- Este proceso se conoce como **pruebas de penetración (pentesting)**.

## Actores de amenazas

| Actor | Motivación | Características |
|---|---|---|
| **Crimen organizado** | Dinero | Grupos financiados que usan las técnicas más recientes (ransomware, robo de datos). |
| **Hacktivistas** | Ideológica | Filtran datos confidenciales para avergonzar o dañar económicamente a un objetivo. |
| **Patrocinados por el estado** | Geopolítica | Ciberespionaje y ciberguerra para robar información y causar interrupciones. |
| **Amenazas internas** | Variada | Empleados engañados (phishing) o usuarios maliciosos movidos por venganza o dinero. |

## Tipos de pruebas

- **Infraestructura de red:** evalúa la red real, incluida la inalámbrica (eludir seguridad, romper cifrado, mapas de calor de señal).
- **Aplicaciones:** configuraciones incorrectas, validación de entrada, inyección y fallas lógicas, con el objetivo de llegar a la base de datos de soporte. Recurso clave: **OWASP**.
- **Nube:** se rige por el **modelo de responsabilidad compartida** (varía entre SaaS, PaaS e IaaS). Hay que definir detalles contractuales (SLA, recuperación ante desastres, cifrado) y revisar qué pruebas permite cada proveedor.
- **Ingeniería social:** suele quedar fuera del alcance porque prueba personas, no tecnología. Su objetivo es mejorar el programa de concienciación, no señalar a quien falla. Herramienta: **Social-Engineer Toolkit (SET)**, de Dave Kennedy.

## Perspectivas de prueba

| Enfoque | Información al evaluador | Notas |
|---|---|---|
| **Caja negra** | Mínima, como un atacante externo | Se parte de información pública. El equipo de defensa a veces no está avisado. |
| **Caja blanca** | Amplia: diagramas, IPs, configuraciones, credenciales, código fuente | Busca el máximo de vulnerabilidades. Alcance más amplio. Recomendada dado el nivel de los adversarios actuales. |
| **Caja gris** | Parcial: por ejemplo, credenciales sin documentación completa | Se empieza desde un equipo cliente y se pivota lateralmente para medir el impacto. |

El **tiempo y el costo** suelen determinar qué tipo de prueba se realiza.

## Estándares y metodologías

- **MITRE ATT&CK:** matrices de tácticas, técnicas y procedimientos (TTP) de adversarios (Enterprise, Network, Cloud, ICS, Mobile). Lo usan equipos ofensivos, de respuesta a incidentes y de threat hunting.
- **OWASP WSTG:** guía de pruebas de seguridad web. Cubre XSS, XXE, CSRF e inyección SQL, y cómo mitigarlos.
- **NIST SP 800-115:** guía del NIST para planificar y ejecutar pruebas de seguridad. Reemplazó a SP 800-42 y es un estándar de la industria.
- **OSSTMM:** manual de ISECOM (Pete Herzog) para pruebas de seguridad repetibles y uniformes. Cubre métricas operativas, análisis de confianza, seguridad humana, física, inalámbrica, telecomunicaciones y redes de datos, y genera el informe **STAR**. Versión 3, con la 4 en borrador.
- **PTES:** siete fases:
  1. Interacciones previas al compromiso
  2. Recopilación de inteligencia
  3. Modelado de amenazas
  4. Análisis de vulnerabilidades
  5. Explotación
  6. Post-explotación
  7. Informes
- **ISSAF:** recopilación de información → asignación de red → identificación de vulnerabilidades → penetración → acceso y escalamiento de privilegios → más enumeración → comprometer usuarios/sitios remotos → mantener el acceso → cubrir las pistas.

---

> ⚠️ **Aviso:** estas notas son con fines educativos. Prueba únicamente sistemas que sean tuyos o para los que tengas permiso explícito y por escrito.
