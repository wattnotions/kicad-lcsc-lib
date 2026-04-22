# KiCad LCSC Library

Reusable KiCad library generated from LCSC parts with `easyeda2kicad`.

## Layout

- `lcsc.kicad_sym` - symbol library
- `lcsc.pretty/` - footprint library
- `lcsc.3dshapes/` - 3D models used by the footprints

## Import a new part

```bash
./import-part C25804
```

You can pass one or more LCSC IDs:

```bash
./import-part C25804 C223881
```

The script calls `easyeda2kicad` with the correct fixed output target for this
repo:

```bash
easyeda2kicad --full --lcsc_id ... --output /home/shane/Documents/Github/kicad-lcsc-lib/lcsc.kicad_sym --overwrite
```

## Add to KiCad

- Symbol library: `/home/shane/Documents/Github/kicad-lcsc-lib/lcsc.kicad_sym`
- Footprint library: `/home/shane/Documents/Github/kicad-lcsc-lib/lcsc.pretty`

## Notes

- Keep the library basename as `lcsc`.
- Do not move `.kicad_mod` files out of `lcsc.pretty/`.
- The `lcsc.3dshapes/` directory should stay next to the symbol and footprint libraries.
