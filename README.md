# exec-path-from-shell-cache.el - Cache environment variables set via exec-path-from-shell

[exec-path-from-shell](https://github.com/purcell/exec-path-from-shell) is a
library which set environment variables from the shell.
exec-path-from-shell-cache caches the results of exec-path-from-shell execution
and saves time on shell calls.

## Usage

If you have the following configuration,

```elisp
(require 'exec-path-from-shell)
(exec-path-from-shell-initialize)
```

rewrite it as follows:

```elisp
(require 'exec-path-from-shell-cache)
(exec-path-from-shell-cache-initialize-with-cache)
```

Cache data is saved to the file specified by `exec-path-from-shell-cache-file`.
If environment variables in your shell are updated,
run `exec-path-from-shell-cache-force-initialize` to reload them.
