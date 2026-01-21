# Style Module

ANSI terminal color and text styling utilities for CLI applications.

## Usage

```ez
Simply copy the `style` directory into your projects structure
Then, in the file you plan on using the `style` modules functions or constants write the following at the top of said file:

import "relative/path/to/style"
```

### Text Styling

```ez
temp text = "Hello"
style.style_make_bold(text)      // Makes text bold
style.style_make_italic(text)    // Makes text italic
style.style_make_underline(text) // Makes text underlined
style.style_make_dim(text)       // Makes text dim
style.style_make_strike(text)    // Strikes through text
style.style_make_reverse(text)   // Swaps foreground/background colors
```

### Foreground Colors

```ez
temp text = "Hello"
style.style_make_red(text)          // Red text
style.style_make_green(text)        // Green text
style.style_make_blue(text)         // Blue text
style.style_make_bright_yellow(text) // Bright yellow text
```

### Background Colors

```ez
temp text = "Hello"
style.style_make_bg_red(text)          // Red background
style.style_make_bg_green(text)        // Green background
style.style_make_bg_bright_cyan(text)  // Bright cyan background
```

## API Reference

### Text Style Functions

| Function | Description |
|----------|-------------|
| `style_make_bold(&t string) -> string` | Make text bold |
| `style_make_dim(&t string) -> string` | Make text dim |
| `style_make_italic(&t string) -> string` | Make text italic |
| `style_make_underline(&t string) -> string` | Make text underlined |
| `style_make_reverse(&t string) -> string` | Swap foreground/background colors |
| `style_make_strike(&t string) -> string` | Strike through text |
| `style_reset() -> string` | Reset all styling |

### Foreground Color Functions

| Function | Description |
|----------|-------------|
| `style_make_black(&t string) -> string` | Black text |
| `style_make_red(&t string) -> string` | Red text |
| `style_make_green(&t string) -> string` | Green text |
| `style_make_yellow(&t string) -> string` | Yellow text |
| `style_make_blue(&t string) -> string` | Blue text |
| `style_make_magenta(&t string) -> string` | Magenta text |
| `style_make_cyan(&t string) -> string` | Cyan text |
| `style_make_white(&t string) -> string` | White text |

### Bright Foreground Color Functions

| Function | Description |
|----------|-------------|
| `style_make_bright_black(&t string) -> string` | Bright black text |
| `style_make_bright_red(&t string) -> string` | Bright red text |
| `style_make_bright_green(&t string) -> string` | Bright green text |
| `style_make_bright_yellow(&t string) -> string` | Bright yellow text |
| `style_make_bright_blue(&t string) -> string` | Bright blue text |
| `style_make_bright_magenta(&t string) -> string` | Bright magenta text |
| `style_make_bright_cyan(&t string) -> string` | Bright cyan text |
| `style_make_bright_white(&t string) -> string` | Bright white text |

### Background Color Functions

| Function | Description |
|----------|-------------|
| `style_make_bg_black(&t string) -> string` | Black background |
| `style_make_bg_red(&t string) -> string` | Red background |
| `style_make_bg_green(&t string) -> string` | Green background |
| `style_make_bg_yellow(&t string) -> string` | Yellow background |
| `style_make_bg_blue(&t string) -> string` | Blue background |
| `style_make_bg_magenta(&t string) -> string` | Magenta background |
| `style_make_bg_cyan(&t string) -> string` | Cyan background |
| `style_make_bg_white(&t string) -> string` | White background |

### Bright Background Color Functions

| Function | Description |
|----------|-------------|
| `style_make_bg_bright_black(&t string) -> string` | Bright black background |
| `style_make_bg_bright_red(&t string) -> string` | Bright red background |
| `style_make_bg_bright_green(&t string) -> string` | Bright green background |
| `style_make_bg_bright_yellow(&t string) -> string` | Bright yellow background |
| `style_make_bg_bright_blue(&t string) -> string` | Bright blue background |
| `style_make_bg_bright_magenta(&t string) -> string` | Bright magenta background |
| `style_make_bg_bright_cyan(&t string) -> string` | Bright cyan background |
| `style_make_bg_bright_white(&t string) -> string` | Bright white background |

### Constants

Text style constants: `STYLE_RESET`, `STYLE_BOLD`, `STYLE_DIM`, `STYLE_ITALIC`, `STYLE_UNDERLINE`, `STYLE_REVERSE`, `STYLE_STRIKE`

Foreground color constants: `STYLE_FG_BLACK`, `STYLE_FG_RED`, `STYLE_FG_GREEN`, `STYLE_FG_YELLOW`, `STYLE_FG_BLUE`, `STYLE_FG_MAGENTA`, `STYLE_FG_CYAN`, `STYLE_FG_WHITE` (and bright variants with `BRIGHT_` prefix)

Background color constants: `STYLE_BG_BLACK`, `STYLE_BG_RED`, `STYLE_BG_GREEN`, `STYLE_BG_YELLOW`, `STYLE_BG_BLUE`, `STYLE_BG_MAGENTA`, `STYLE_BG_CYAN`, `STYLE_BG_WHITE` (and bright variants with `BRIGHT_` prefix)

## Potential Use Cases

- **CLI tools**: Add color and emphasis to command-line output
- **Log formatting**: Highlight errors in red, warnings in yellow
- **Interactive prompts**: Style user prompts and menus
