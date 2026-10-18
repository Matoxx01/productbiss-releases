# ProductBiss POS - Releases

Este repositorio publico existe solo para alojar los **instaladores** de escritorio de
**ProductBiss POS**, el punto de venta de ProductBiss. No contiene codigo fuente: el codigo de la
aplicacion y del sitio web se mantiene en repositorios privados.

## Descargar

La forma recomendada de descargar es desde el sitio oficial, que siempre ofrece la ultima version:

**https://productbiss.cl/descargar/**

Tambien puede bajar el instalador desde la seccion **Releases** de este repositorio.

## Que se publica aqui

| Plataforma | Archivo | Ejemplo |
| --- | --- | --- |
| Windows (64 bits) | Instalador `.exe` | `ProductBiss-POS-1.0.0-x64.exe` |

Las versiones para **Android** e **iOS** no se publican aqui: se distribuyen por Google Play y App Store.

## Instalacion en Windows

1. Descargue el instalador y ejecutelo. Se instala por usuario, sin permisos de administrador.
2. Mientras el instalador no este firmado digitalmente, Windows puede mostrar **"Windows protegio
   su PC"**. No es un error: continue con **Mas informacion** y luego **Ejecutar de todas formas**.

Requisitos minimos: Windows 10 o superior, 64 bits, 4 GB de RAM y entre 2 y 5 GB de disco.

## Para quien publica una version

El sitio web lee estas releases automaticamente; no hay que tocar el sitio al publicar.

1. Compile el instalador en `ProductBiss` con `npm run electron:build`. Queda en `release/`.
2. Cree la release con el numero de version como etiqueta (`v1.0.0`). Esa etiqueta es la version que
   ve el visitante:

   ```bash
   gh release create v1.0.0 "release/ProductBiss-POS-1.0.0-x64.exe" \
     --repo Matoxx01/productbiss-releases \
     --title "ProductBiss POS 1.0.0" \
     --notes "Cambios de esta version"
   ```

3. Las **notas** aceptan Markdown y se muestran en la pagina de descargas.

Reglas que el sitio aplica:

- Muestra la release mas reciente que traiga un archivo `.exe`. Las versiones anteriores quedan
  disponibles en un desplegable.
- **Ignora** los borradores y las releases marcadas como *pre-release*.
- Los cambios pueden tardar hasta unos 15 minutos en verse, por la memoria cache del servidor.

---

(c) ProductBiss. Todos los derechos reservados.
