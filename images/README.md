# Images 🖼️

Put your own pictures here — a photo, an avatar, a logo, whatever you like for your
profile card or a page.

## How to use an image in your profile

1. Drop your file in this folder, e.g. `images/maria.jpg`.
   Keep the filename lowercase, no spaces (use `-` instead), e.g. `maria-andersson.jpg`.
2. In your profile file (`people/your-name.qmd`), point the `image:` field at it with a
   path **relative to your profile**, which means starting with `../images/`:

   ```yaml
   image: ../images/maria.jpg
   ```

See `people/example-maria.qmd` for a working example (it uses `../images/example-maria.svg`).

## Tips

- Roughly square images look best in the card grid.
- Keep files small (under ~500 KB) so the site stays fast — resize big photos first.
- No image handy? You can use an auto-generated avatar URL instead, like
  `people/example-johan.qmd` does. Both work.
