# CheckMate Bet — Juego de Ajedrez (Scaffold inicial)

Este repositorio contiene el scaffold inicial del proyecto "CheckMate Bet" (rama `feat/scaffold`).

Importante: Esto es el primer commit con la estructura inicial, contenedores y documentación para levantar localmente. En commits siguientes se implementará la lógica completa, backend, mobile y panel admin.

Resumen rápido
- Repo: aroncpj-arch/juego-de-ajedrez-2
- Rama de trabajo: feat/scaffold
- Modo real por defecto: OFF (REAL_MONEY_ENABLED = OFF)

Cuenta ADMIN de prueba
- Email: aroncpj@gmail.com
- Usuario: admin
- Contraseña temporal: AdmTemp!2026$CMB
- TOTP (Google Authenticator) - clave secreta (BASE32) para ingresar manualmente: JBSWY3DPEHPK3PXP

Nota de seguridad: Cambia la contraseña del admin y guarda la clave TOTP en un gestor de contraseñas. No uses la contraseña temporal en producción.

Cómo levantar el entorno (desarrollo, Docker Compose)

Requisitos:
- Docker & Docker Compose (v2)
- Git

Pasos básicos:
1. Clona el repo y cambia a la rama:
   git fetch origin
   git checkout -b feat/scaffold origin/feat/scaffold

2. Copia el archivo de ejemplo de entorno y ajusta variables si deseas:
   cp .env.example backend/.env

3. Levanta los servicios con Docker Compose:
   docker compose up -d

Servicios incluidos por defecto:
- PostgreSQL (puerto 5432)
- Redis (puerto 6379)
- MinIO (puerto 9000) — usado para almacenamiento de comprobantes en local

4. Sigue las instrucciones en backend/README.md para ejecutar el backend (migraciones y seeds) y en mobile/README.md para instalar la APK de prueba.

APK de prueba
- Archivo APK debug se subirá dentro de `/artifacts` en esta rama cuando esté listo. Para pruebas rápidas en Android permite instalación de orígenes desconocidos.

Estado y siguientes pasos
- En 48 horas aproximadamente subiré el primer commit con el scaffold completo y el APK debug en `/artifacts`.
- Etapas siguientes: API completa (auth, wallets, ledger, depósitos, retiros, matchmaking, motor de ajedrez server-side), panel admin, mobile app, pruebas e integración.

Contacto
- Si necesitas que cambie la clave TOTP o la contraseña temporal, dímelo.

---

Aviso legal y cumplimiento
- Esta entrega inicial es un scaffold técnico. No habilites REAL_MONEY_ENABLED en entornos públicos hasta verificar cumplimiento legal y configuraciones de seguridad e integraciones con bancos y servicios de pago.
