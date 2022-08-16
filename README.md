# tera-template

This is a port of [eseom's excellent Nunjucks Template extension](https://github.com/eseom/nunjucks-template) for the Tera template language and the Zola ssg. 

# feature

- tera template syntax
- tera formatter with prettydiff2
- yaml syntax

## configurations

- By default, detects .nj, .njk files automatically.
- Additionally, use `files.associations`

#### extension's own configurations

```json
"teraTemplate.preserveEmptyLine": 3
```

(suggested at issue PR #30 by @sdegutis)

#### other configurations

```json
"files.associations": {
  "*.html": "tera"
},
```

- For vscode embedded emmet, notify that `tera` is html file type

```json
"emmet.includeLanguages": {
  "tera": "html"
},
```

- max line length follows standard vscode html.format.wrapLineLength

```json
"html.format.wrapLineLength": 120
```

- for vscode-icons ([issue #6](https://github.com/eseom/nunjucks-template/issues/6))

```json
"vsicons.associations.files": [
  { "icon": "tera", "extensions": ["tera"], "format": "svg" }
],
```

- for Material Icon Theme by [Heitor Augusto](https://github.com/HeitorAugustoLN)

```json
"material-icon-theme.files.associations": {
  "*.html": "tera"
},
```

## snippets

| Trigger   | Snippet                             |
| --------- | ----------------------------------- |
| t-extends | {% extends '${name}' %}             |
| t-block   | {% block ${name} %}{% endblock %}   |
| t-if      | {% if condition %}{% endif %}       |
| t-for     | {% for ${condition} %}{% endfor %}  |
| t-macro   | {% macro ${name}() %}{% endmacro %} |

## links

- https://github.com/eseom/nunjucks-template
- https://github.com/edwardwolcher/tera-template
