# Plantilla de sección — ANS Universe

**Copiá este repositorio para dar de alta una sección nueva.**

Una sección es una sesión de Claude Code persistente que trabaja para una
organización pública. Este repositorio es su cuerpo: `git clone` + `claude` y la
sección vuelve a ser ella misma, con su contexto, sus herramientas y su memoria.

## Qué hay adentro

| Archivo | Qué es |
|---|---|
| `seccion.json` | **La declaración.** Es lo único que lee el universo: quién es, qué zona atiende, qué herramientas lleva, qué capacidades declara y qué obras produjo. |
| `CLAUDE.md` | Quién es la sección y cómo trabaja. Claude Code lo carga solo al abrir el repo. |
| `notas/` | La documentación, en Markdown con encabezado. **Los `[[enlaces]]` entre notas son las aristas del grafo.** |
| `obras/` | Lo que produce. |
| `.github/workflows/universo.yml` | 20 líneas que llaman a la maquinaria central. |

## Cómo dar de alta una sección

1. Copiá esta plantilla a un repositorio nuevo.
2. Completá `seccion.json`.
3. Abrí un pull request contra el registro.
4. **El portón verifica cada capacidad declarada contra el diccionario vivo.**
   Si alguna no existe, el pull request no se puede fusionar.

## Por qué el repo está casi vacío

A propósito. **La lógica vive una sola vez, versionada, en la maquinaria** — así
se arregla en un lugar y todas las secciones lo reciben, en vez de tener que
tocar cada repositorio.

Calcado de cómo lo hace r-universe: su `universe-template` son 20 líneas que
llaman a `r-universe-org/workflows/.github/workflows/sync.yml@v3`.

## Lo que NO va acá

Ningún secreto. Las claves viven en la máquina y en los *Secrets* de GitHub.
**El repositorio es el cuerpo de la sección; las llaves son del fierro.**
