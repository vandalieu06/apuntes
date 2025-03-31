# COMANDOS LINUX + CHATGPT

## PANDOC

1. **Convertir de docx o odt a md por linea de comando**

```shell
pandoc -f docx|odt -t markdown -o output.md input.docx
```

## FIND

1. **Buscar archivos por nombre**

Buscar todos los archivos con el nombre `notas.txt`:

```
find ./ -name "notas.txt"
```

Buscar archivos con la extensión `.desktop`:

```
find ./ -name "*.desktop"
```

> **Nota**: Es importante usar comillas para evitar la expansión de la shell.

2. **Buscar por tipo***
- **Archivos**:

```
find ./ -type f -name "*.txt"
```

- **Directorios**:

```
find ./ -type d -name "proyectos"
```
