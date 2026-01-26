# Path Module

Cross-platform file path manipulation utilities for EZ.

## What is the Path Module?

The path module provides functions for working with file and directory paths in a platform-independent way. It automatically handles the differences between Unix-style paths (`/`) and Windows-style paths (`\`).

```
Unix:      /home/user/documents/file.txt
Windows:   C:\Users\user\documents\file.txt

Both work seamlessly with this module.
```

## Usage

### Importing the Module

```ez
Simply copy the `path` directory into your project structure.
Then, in the file you plan on using the `path` module's functions write the following at the top of said file:

import "relative/path/to/path"
```

### Joining Paths

```ez
// Create a path from segments (uses correct separator for OS)
temp filePath string = path.join({"home", "user", "documents", "file.txt"})
// Unix:    "home/user/documents/file.txt"
// Windows: "home\user\documents\file.txt"
```

### Extracting Path Components

```ez
temp p string = "/home/user/documents/report.pdf"

temp base string = path.get_base_name(p)    // "report.pdf"
temp dir string = path.get_dir_name(p)      // "/home/user/documents"
temp ext string = path.get_extension(p)     // ".pdf"
```

### Parsing Paths

```ez
temp info path.PathInfo = path.parse("/home/user/file.txt")

std.println(info.dir)   // "/home/user"
std.println(info.base)  // "file.txt"
std.println(info.name)  // "file"
std.println(info.ext)   // ".txt"
```

### Working with Extensions

```ez
temp p string = "/home/user/document.txt"

// Check extension
temp extToCheck string = "txt"
temp hasTxt bool = path.has_extension(p, extToCheck)  // true

// Change extension
temp newExt string = "md"
temp newPath string = path.change_extension(p, newExt)  // "/home/user/document.md"

// Remove extension
temp noExt string = path.strip_extension(p)  // "/home/user/document"
```

### Checking Path Properties

```ez
temp absolute bool = path.is_absolute("/usr/bin")     // true (Unix)
temp relative bool = path.is_absolute("docs/file")   // false
```

### Platform Detection

```ez
temp sep string = path.separator()    // "/" on Unix, "\" on Windows
temp delim string = path.delimiter()  // ":" on Unix, ";" on Windows (for PATH)
```

## API Reference

### Types

| Type | Description |
|------|-------------|
| `PathInfo` | Struct containing parsed path components (dir, base, name, ext) |

### Path Operations

| Function | Description |
|----------|-------------|
| `join(arr [string]) -> string` | Join path segments with OS separator |
| `split(p string) -> (string, string)` | Split into (directory, base name) |
| `parse(p string) -> PathInfo` | Parse path into all components |

### Component Extraction

| Function | Description |
|----------|-------------|
| `get_base_name(p string) -> string` | Get filename with extension |
| `get_dir_name(p string) -> string` | Get directory portion |
| `get_extension(p string) -> string` | Get extension with dot (e.g., ".txt") |

### Extension Operations

| Function | Description |
|----------|-------------|
| `has_extension(p string, &ext string) -> bool` | Check if path has extension (case-insensitive) |
| `change_extension(p string, &newExt string) -> string` | Replace extension |
| `strip_extension(p string) -> string` | Remove extension from path |

### Path Properties

| Function | Description |
|----------|-------------|
| `is_absolute(p string) -> bool` | Check if path is absolute |
| `separator() -> string` | Get OS path separator ("/" or "\") |
| `delimiter() -> string` | Get OS path list delimiter (":" or ";") |

## PathInfo Struct

The `PathInfo` struct contains the following fields:

| Field | Type | Description |
|-------|------|-------------|
| `dir` | `string` | Directory portion of the path |
| `base` | `string` | Filename with extension |
| `name` | `string` | Filename without extension |
| `ext` | `string` | Extension with leading dot |

## Potential Use Cases

- **File management**: Building paths for reading/writing files
- **Configuration**: Parsing config file paths
- **Build systems**: Manipulating source and output paths
- **Asset pipelines**: Changing file extensions during processing
- **Cross-platform tools**: Writing code that works on any OS
- **Path validation**: Checking if paths are absolute or relative
