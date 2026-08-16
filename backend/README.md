# Backend — instrucciones iniciales

Este directorio contendrá el backend (NestJS + Prisma + Socket.IO). Aquí explico los pasos iniciales para desarrollo local una vez que los servicios de Docker estén arriba.

1. Instalar dependencias (en la carpeta backend):
   npm install

2. Crear archivo de entorno (basado en .env.example) y ajustar variables: DATABASE_URL, REDIS_URL, MINIO credentials, JWT secrets, etc.

3. Ejecutar migraciones y seeds (Prisma o tu ORM elegido):
   npx prisma migrate dev --name init
   npx prisma db seed

4. Levantar el servidor en modo desarrollo:
   npm run start:dev

Endpoints y características (planificadas):
- /auth: registro, login, recuperación de contraseña, 2FA TOTP
- /wallets: saldo, historial, bloqueos
- /deposits: crear solicitud, subir comprobante
- /withdrawals: solicitar retiro
- /matchmaking: cola por stake
- /matches: WebSocket endpoints para partidas en tiempo real

Nota: Este README es informativo; el código backend vendrá en próximos commits.
