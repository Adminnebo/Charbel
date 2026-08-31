# Nebo y Closers

Cotizador de servicios y calculadora de comisiones para closers de NEBO AI.

## Qué hace

- Arma la cotización de un cliente: plan, implementación y módulos mensuales.
- Calcula en vivo el total de implementación y el servicio mensual.
- Muestra la comisión del closer (porcentajes editables desde la interfaz).
- Proyecta esa misma configuración sobre una cartera de hasta 500 clientes.
- Genera dos PDFs: uno para el cliente y otro para el closer con la comisión.
- Seis escenarios predefinidos, tema claro y oscuro.

## Ejecutar en local

```bash
npm install
npm start
```

Queda en http://localhost:3000

## Desplegar en Railway

```bash
railway link <ID del proyecto>
railway up
railway domain
```

El `railway.json` ya define el comando de arranque con el puerto que Railway inyecta.

## Estructura

- `index.html` — la aplicación completa, sin dependencias externas.
- `package.json` — sirve el estático con `serve`.
- `railway.json` — configuración de despliegue.

## Nota sobre el acceso

La pantalla de acceso valida en el navegador. Sirve para que nadie vea las
comisiones por accidente, **no es una barrera de seguridad**: el código es
visible para cualquiera que abra la URL. Si el contenido debe quedar
realmente protegido, la validación tiene que moverse a un servidor.
