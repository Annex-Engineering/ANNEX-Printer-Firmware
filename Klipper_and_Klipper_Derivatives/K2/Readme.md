# Readme

## Recommended Firmware Changes
 - z_tilt.py

    Replace 
        ```return self.retry_helper.check_retry([p[2] for p in positions])```
    With
        ```return self.retry_helper.check_retry(adjustments)```

This allows the bed (with 4 motors) to actually converge around adjustments, instead of floating around in lala land already converged