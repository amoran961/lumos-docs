# Documentación de la API pública de Lumos CRM

Sitio Mintlify con guías en español y referencia de las 22 operaciones de la API pública v1.

## Fuentes

- Contrato fuente: `lumosai-core-ms/docs/public-api-v1.openapi.yaml`.
- Implementación: `lumosai-core-ms/src/routes/publicApi.ts` y `src/lib/publicApi`.
- Contrato publicado: `api-reference/openapi.json`, convertido desde el YAML fuente sin modificar rutas ni esquemas.
- Navegación: `docs.json`. Las páginas de endpoints vinculan operaciones del contrato publicado.

Confirma que `PUBLIC_API_V1_ENABLED=true` en el entorno antes de utilizar esta documentación para una integración. El host predeterminado del contrato no demuestra que el entorno esté habilitado o sea accesible.

## Desarrollo y validación

Con el CLI de Mintlify instalado, ejecuta desde este directorio:

```bash
mint dev
mint broken-links
```

Cuando cambie el contrato del core, actualiza `api-reference/openapi.json`, las páginas de operaciones y las guías afectadas. Comprueba los permisos y ejemplos contra la implementación.

## Material anterior

Las páginas de la integración legacy que ya no aparecen en `docs.json` y la colección `api-reference/postman/lumos-external-v1.postman_collection.json` conservan el contrato anterior. No las uses como ejemplos de la nueva API pública v1. Incluyen operaciones de correo y administración que no forman parte de la referencia actual.

## Publicación

Estos cambios locales no publican el sitio. Si Mintlify está conectado al repositorio, la publicación depende de su configuración de rama y despliegue.

## Identidad visual

- `favicon.svg` reutiliza el símbolo de nodos de `lumosai-web/public/favicon.svg`.
- `logo/light.svg` y `logo/dark.svg` adaptan ese símbolo a la cabecera de documentación.
- `docs.json` configura Plus Jakarta Sans y el violeta de `lumosai-design-system/src/styles/tokens.css` (258 / 84% / 56%, 68% en oscuro).
- `style.css` adapta superficies, bordes, radio y movimiento del DS. La portada toma el degradado índigo de `lumosai-web/src/styles/tokens.css`.

Los tokens están copiados con nombres `--lumos-*` para evitar conflictos con Mintlify. Revisa estos archivos cuando cambie la identidad del DS. Los bloques de código mantienen la tipografía monoespaciada del tema.
