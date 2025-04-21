# Factorio Blueprint Optimiser

To run an instance, a parameter file is needed.  
Samples are stored in the `/param` directory.

## Run with:

```bash
python factorio_opt.py --param [path to param file] (--max-recipes [n]) (--max-bpp [n]) (--keep-files) (--save-log)

# Example run:
python factorio_opt.py --param param/3x5_in.param --max-recipes 150 --save-log
```

NB: Savile Row must be in $PATH
I personally did it differenlty, in @lib/utils/config.py I set savilerow_path = "/Users/idanlau/Downloads/savilerow-1.10.1-mac-arm/savilerow"

<br>
<br>
`--param`       (required): The parameter file to use <br>
`--max_recipes` (optional): How many attempts are allowed of the recipe stage (default 100) <br>
`--max_bpp`     (optional): How many attempts are allowed of the bin-packing stage per recipe stage attempt (default 100) <br>
`--keep-files`  (optional): Whether to keep non-solution Savile Row output (default False) <br>
`--save-log`    (optional): Whether to store the error log in the output folder (default False) <br>
<br>
Output is stored in /out in a folder named for the parameter file and time



