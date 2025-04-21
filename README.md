# Factorio Blueprint Optimiser

To run an instance, a parameter file is needed.  
Sample files are stored in the `/param` directory.

## Usage

Download Savile Row Here: https://www-users.york.ac.uk/peter.nightingale/savilerow/index.html

## Usage

```bash
python factorio_opt.py --param [path to param file] (--max-recipes [n]) (--max-bpp [n]) (--keep-files) (--save-log)

# Example run:
python factorio_opt.py --param param/3x5_in.param --max-recipes 150 --save-log
```

**Note:** Savile Row must be available in your `$PATH`.

If you prefer, you can also hardcode the path manually in `@lib/utils/config.py`:
```python
savilerow_path = "/Users/idanlau/Downloads/savilerow-1.10.1-mac-arm/savilerow"
```

---

## Command Line Arguments

| Argument        | Required | Description                                                                 |
|-----------------|----------|-----------------------------------------------------------------------------|
| `--param`       | ✅       | Path to the parameter file to use.                                          |
| `--max_recipes` | ❌       | Max number of attempts for the recipe stage (default: `100`).               |
| `--max_bpp`     | ❌       | Max bin-packing attempts per recipe stage attempt (default: `100`).         |
| `--keep-files`  | ❌       | Whether to keep intermediate Savile Row output files (default: `False`).    |
| `--save-log`    | ❌       | Whether to save the error log in the output folder (default: `False`).      |

---

## Output

Results are stored in the `/out` directory, under a subfolder named after the parameter file and timestamp.
