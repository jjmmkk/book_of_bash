# Cut `ps` output

How to `cut` output of the `ps` command.

Since the output is delimited by spaces, first squeeze the spaces into single spaces, then use `cut` with space as delimiter.

```bash
ps aux | grep varnish | tr -s ' ' | cut -d ' ' -f 2
```
