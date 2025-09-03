# CLI tools

## Testing the REPL

Open the Clojure CLI in a terminal:

```bash
clj
```

Test if the REPL works by issuing

```clojure
(str (java.time.LocalDateTime/now))
```

in the REPL.
The output should be the current time with nanosecond precision, e.g.,

```clojure
"2025-09-02T20:44:42.873013064"
```

Exit the REPL using `CTRL-D`.

## Pulling in a dependency

In a new working directory, create a file `deps.edn` and paste the following:

```clojure
{:deps
  {clojure.java-time/clojure.java-time {:mvn/version "1.1.0"}}}
```

Open the REPL again and issue:

```clojure
(require '[java-time.api :as time])
(str (time/instant))
```

The output should be similar to the first command you issued above.
