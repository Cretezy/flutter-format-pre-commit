# Flutter Format `pre-commit`

[`pre-commit`](https://pre-commit.com) hook for formatting Flutter files.

Add the following in your `.pre-commit-config.yaml`:
```yaml
- repo: https://github.com/Cretezy/flutter-format-pre-commit
  rev: "master"
  hooks:
    - id: flutter-format
```
By default, the flutter format command uses a [line length of 80](https://github.com/dart-lang/dart_style/issues/833). You can customize what line length is used by passing the `--line-length` argument to the hook:
```yaml
- repo: https://github.com/Cretezy/flutter-format-pre-commit
  rev: "master"
  hooks:
    - id: flutter-format
      args: [--line-length=100]
```

You can also only include/exclude some files (defaults to only `.dart`, is a pattern):

```yaml
- repo: https://github.com/Cretezy/flutter-format-pre-commit
  rev: "master"
  hooks:
    - id: flutter-format
      files: lib/* # Only format source files
      exclude: lib/src/avatar.dart # Exclude the avatar widget
```

## Dart

Also see [Dart Format `pre-commit`](https://github.com/Cretezy/dart-format-pre-commit) for formatting only Dart code.
