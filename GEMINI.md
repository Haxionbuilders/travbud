# TravBud Development & Deployment Rules

## 1. Secrets & Credentials Hygiene
- **Never commit real credentials:** Do not write real API tokens, Personal Access Tokens (e.g. `ghp_*`), private keys, or passwords into code, configuration, or documentation markdown files.
- **Redaction:** Always use placeholders (e.g., `ghp_[REDACTED]`) in documentation, logs, and commit messages to prevent GitHub Push Protection rejections.

## 2. Inlined HTML & Script Safety
- **No raw closing script tags in strings:** When embedding or generating scripts within HTML template strings, never write raw `</script>`. The browser's HTML parser terminates the outer `<script>` block regardless of JavaScript quotes.
- **Safe alternatives:** Use `'</' + 'script>'`, `<\\/script>`, or inline event handlers like `<body onload="...">`.

## 3. Pre-Deployment AST & Syntax Verification
- **Automated syntax checks:** Before copying build outputs to deploy directories or committing changes to git, always validate all `<script>` blocks using Node's AST checker (`node --check <file>` or `new vm.Script(code)`).
- **Zero-error gate:** Only commit and push builds that pass 100% of syntax and AST validations.

## 4. UI Invariants
- **Aspect Ratio Protection:** When replacing vector logos with bitmap images, always preserve the natural aspect ratio (for TravBud: 1.83:1 / 1024x558) to prevent stretching or letterboxing.
- **Dark Mode Persistence:** Always guarantee that dark themes are enforced on `<html>` and in initial state so that light theme white backgrounds never flash during navigation.
