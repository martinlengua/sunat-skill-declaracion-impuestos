# Skill de Claude: declaración de impuestos en la SUNAT

Un skill para que **Claude** haga contigo tu **declaración anual de renta** en la SUNAT (Perú),
manejando tu navegador Chrome:

1. Revisa tus **gastos deducibles** (restaurantes, alquiler, honorarios, EsSalud del hogar).
2. Revisa y valida el **Formulario Virtual 709** precargado.
3. Te muestra un resumen y **solo lo presenta si tú dices que sí**.
4. Si tienes saldo a favor, llena la **solicitud de devolución (Formulario 1649)** y te pide
   confirmación antes de enviarla.
5. Guarda las **constancias** y te deja un resumen con los números de orden.

> Es para personas naturales con rentas del trabajo (4ta y/o 5ta categoría). No sirve para
> empresas ni renta de 3ra categoría (MYPE, RER, NRUS, régimen general).

## Tu seguridad primero

- **Tu Clave SOL la escribes tú.** Claude nunca te la pide ni la escribe.
- **Tu número de cuenta (CCI) lo registras tú.** Claude solo te muestra los últimos 4 dígitos de
  la cuenta ya registrada para que confirmes.
- **Nada se presenta sin tu "sí".** Hay dos confirmaciones: antes de presentar el 709 y antes de
  enviar la devolución, siempre después de que veas los montos.
- **Claude no paga.** Si te sale impuesto por pagar, te muestra el monto y pagas tú.

## Qué necesitas

- Una cuenta de **Claude** con plan de pago (Pro o Max).
- **Google Chrome** con la extensión **Claude in Chrome** instalada y conectada.
- Tu **Clave SOL**.
- Tu **CCI registrado en la SUNAT**, si vas a pedir devolución.

## Cómo instalarlo

### Opción A: Claude Code (la que uso en el video)

1. Instala Claude Code: <https://claude.com/claude-code>
2. Copia el skill a tu carpeta de skills. En la terminal:

   ```bash
   git clone https://github.com/martinlengua/sunat-skill-declaracion-impuestos.git
   mkdir -p ~/.claude/skills
   cp -R sunat-skill-declaracion-impuestos/declaracion-sunat ~/.claude/skills/
   ```

   O, más fácil, abre Claude Code y pégale esto:

   ```
   Instala el skill de https://github.com/martinlengua/sunat-skill-declaracion-impuestos
   copiando la carpeta declaracion-sunat a ~/.claude/skills/
   ```

3. Abre Claude Code con Chrome conectado:

   ```bash
   claude --chrome
   ```

### Opción B: app de Claude (escritorio o claude.ai)

1. Descarga [`declaracion-sunat.zip`](declaracion-sunat.zip) de este repo.
2. En Claude, ve a **Configuración → Capacidades → Skills** y sube el zip.
   (Los nombres del menú pueden variar un poco según la versión).
3. Asegúrate de tener la extensión **Claude in Chrome** conectada.

## Cómo usarlo

Escríbele a Claude algo como:

```
Hazme la declaración de impuestos de 2025 en la SUNAT
```

Claude abre la página de la SUNAT, tú ingresas con tu Clave SOL y le avisas. Desde ahí revisa
todo, te muestra el resumen y espera tu "dale".

Toma entre 5 y 20 minutos.

## Aviso

Claude no es contador ni asesor tributario, y este skill no reemplaza una revisión profesional.
Tú eres responsable de lo que presentas: lee el resumen antes de confirmar. Si tienes rentas
del extranjero, alquileres, venta de acciones o inmuebles, o un negocio, consúltalo con un
contador. El portal de la SUNAT cambia seguido; si algo no funciona, abre un *issue* en este
repo.

## Licencia

[MIT](LICENSE)
