# Color Module

Utilities for working with colors and converting between RGB, hex, and byte color representations.

## Usage

```ez
Simply copy the `color` directory into your projects structure
Then, in the file you plan on using the `color` modules functions or constants write the following at the top of said file:

import "relative/path/to/color"
```

### RGB to Hex

```ez
temp hex = color.color_rgb_to_hex(255, 128, 0)  // Returns "FF8000"
```

### Hex to RGB

```ez
temp r, g, b = color.color_hex_to_rgb("FF8000")  // Returns 255, 128, 0
```

### Byte to Hex

```ez
temp high, low = color.color_byte_to_hex(255)  // Returns 'F', 'F'
```

### Hex to Byte

```ez
temp byte = color.color_hex_to_byte('F', 'F')  // Returns 255
```

## API Reference

| Function | Description |
|----------|-------------|
| `color_rgb_to_hex(r, g, b u8) -> string` | Convert RGB values to a hex string |
| `color_hex_to_rgb(hex string) -> (u8, u8, u8)` | Convert a hex string to RGB values |
| `color_byte_to_hex(b u8) -> (char, char)` | Convert a byte to two hex characters |
| `color_hex_to_byte(high, low char) -> u8` | Convert two hex characters to a byte |

## Potential Use Cases

- **Web development**: Convert RGB colors to hex for CSS
- **Image processing**: Convert between color formats
- **UI theming**: Work with color values programmatically
