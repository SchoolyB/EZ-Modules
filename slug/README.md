# Slug Module

URL-safe string slugification utilities for EZ.

## What is a Slug?

A slug is a URL-friendly version of a string. It's commonly used for creating readable URLs from titles or names.

```
"Hello World!"        → "hello-world"
"My Blog Post #1"     → "my-blog-post-1"
"Café & Restaurant"   → "caf-restaurant"
"  Extra   Spaces  "  → "extra-spaces"
```

### Slug Rules

- Lowercase letters only
- Numbers allowed
- Spaces become separators (default: `-`)
- Special characters removed
- No leading/trailing separators
- No consecutive separators

## Usage

### Importing the Module

```ez
Simply copy the `slug` directory into your project structure.
Then, in the file you plan on using the `slug` module's functions write the following at the top of said file:

import "relative/path/to/slug"
```

### Creating Slugs

```ez
// Basic slugification
temp title string = "My Awesome Blog Post!"
temp urlSlug string = slug.make(title)  // "my-awesome-blog-post"

// With custom separator
temp underscored string = slug.create_with_separator(title, "_")  // "my_awesome_blog_post"

// Shorthand for underscore separator
temp snake string = slug.create_with_underscore(title)  // "my_awesome_blog_post"
```

### Validating Slugs

```ez
// Check if a string is already a valid slug
temp valid bool = slug.is_valid("hello-world")      // true
temp invalid bool = slug.is_valid("Hello World!")   // false
temp bad bool = slug.is_valid("--double-dash")      // false

// Validate with custom separator
temp validUnderscore bool = slug.is_valid_with_separator("hello_world", "_")  // true
```

## API Reference

### Constants

| Constant | Value | Description |
|----------|-------|-------------|
| `DEFAULT_SEPARATOR` | `"-"` | Default separator used in slugs |
| `ALLOWED_CHARS` | `"abcdefghijklmnopqrstuvwxyz0123456789"` | Characters allowed in slugs |

### Core Functions

| Function | Description |
|----------|-------------|
| `make(s string) -> string` | Convert string to slug with `-` separator |
| `create_with_separator(s string, sep string) -> string` | Convert string to slug with custom separator |
| `create_with_underscore(s string) -> string` | Convert string to slug with `_` separator |

### Validation Functions

| Function | Description |
|----------|-------------|
| `is_valid(s string) -> bool` | Check if string is valid slug (using `-`) |
| `is_valid_with_separator(s string, sep string) -> bool` | Check if string is valid slug with custom separator |

## Examples

### Blog Post URLs

```ez
temp postTitle string = "10 Tips for Better Code"
temp postSlug string = slug.make(postTitle)
// URL: /blog/10-tips-for-better-code
```

### File Naming

```ez
temp fileName string = "My Document (Final Version).txt"
temp safeFileName string = slug.create_with_underscore(fileName) + ".txt"
// Result: "my_document_final_version.txt"
```

### Validation Before Save

```ez
temp userInput string = get_user_input()
if !slug.is_valid(userInput) {
    userInput = slug.make(userInput)
}
```

## Potential Use Cases

- **URL generation**: Create SEO-friendly URLs from titles
- **File naming**: Generate safe filenames from user input
- **Database keys**: Create readable unique identifiers
- **API endpoints**: Generate consistent resource paths
- **Anchor links**: Create HTML anchor IDs from headings
