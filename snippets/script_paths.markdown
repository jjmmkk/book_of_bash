# Script paths

How to get paths related to the running script.

This taps into a lot of what appears to be quirks, like whitespace characters and whether or not the script is accessed by means of being in your `$PATH`.

```bash
script_cwd="$( cd "$( dirname "${BASH_SOURCE[0]}" )" && pwd)"
echo "$script_cwd"
script_dir=${script_cwd##*/}
echo "$script_dir"
```
