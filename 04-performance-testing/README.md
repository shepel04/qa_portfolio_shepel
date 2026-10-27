# 📈 Performance testing

[← Back to portfolio](../README.md)

| Game | Device | CPU / GPU / RAM | OS | Graphics | Duration | Tool |
|---|---|---|---|---|---|---|
| Tank Busters | Samsung Galaxy S23 (SM-S911B/DS) | Snapdragon 8 Gen 2 / Adreno 740 / 8 GB | Android 16 | Default | ~9 min | [perfgrab](https://github.com/shepel04/Perfgrab) |

## Results

| Metric | Value |
|---|---|
| Average FPS | 59.6 |
| Min / Max FPS | ~54 / ~61 |
| Avg frame time | ~16.8 ms |
| Avg CPU (game) | ~14% (peak ~23%) |
| Avg GPU | ~30% (peak ~46%) |
| RAM used by the game (PSS) | ~1050 MB after loading → ~1200 MB peak |
| Battery °C: start → end | 27.5 → 33.0 °C |

![FPS, CPU, GPU, RAM chart](../assets/performance-chart.jpg)

## Method

- FPS: SurfaceFlinger frame timestamps / frame counters
- CPU: `/proc/stat` + `/proc/<pid>/stat`, share of all cores
- RAM: `dumpsys meminfo` (PSS), `/proc/meminfo` (MemAvailable)
- Temperature: `dumpsys battery`, `dumpsys thermalservice`

## Conclusion

FPS is stable and stays at the 60 FPS cap (avg 59.6). There are only two short drops to ~54 FPS around 140-150 s, which are not noticeable in gameplay. CPU (~14%) and GPU (~30%) load is low. RAM grows from ~1050 to ~1200 MB in the first 6 minutes and then stays flat, so no memory leak is visible in this run. The battery warms up by ~5.5 °C in 9 minutes (27.5 → 33 °C), which is normal - the phone does not overheat.
