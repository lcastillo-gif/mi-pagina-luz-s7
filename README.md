# Mi página

Plantilla de la Sesión 7 del curso Claude for Business: una página pública que
alguien sin experiencia de código arma con ayuda de Claude — un formulario que
guarda lo que la gente escribe y una lista que lo muestra. Hoy `index.html`
solo trae el aviso "todavía no hay nada aquí"; así empieza toda página nueva,
antes de construir la versión real.

## De dónde salen los datos

Todo lo que la página muestre sale de una tabla de Supabase llamada
`registros`, nunca de texto escrito a mano en el HTML. Sus columnas se
documentan en `CLAUDE.md`, sección 2, una vez que la tabla exista.

## Qué hay en `.claude`

`.claude/agents/revisor-antes-de-publicar.md` define un subagente que, antes
de publicar, busca llaves expuestas, cambios fuera de lo pedido y problemas de
calidad. Solo reporta: nunca corrige ni publica por su cuenta.

## Cómo seguir

1. Lee `CLAUDE.md`: ahí están las reglas de esta página.
2. Pide a Claude el formulario real y su conexión a Supabase.
3. Antes de fusionar, corre el subagente `revisor-antes-de-publicar`.
4. Fusiona solo con tu visto bueno — eso es lo único que publica en Netlify.
