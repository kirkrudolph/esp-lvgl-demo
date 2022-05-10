# LVGL Integration
This was super simple to get integrated with `menuconfig` and compiling.

Simply run:
```
git submodule add https://github.com/lvgl/lvgl.git components/lvgl
git submodule add https://github.com/lvgl/lvgl_esp32_drivers.git components/lvgl_esp32_drivers
```

Because the ESP build system [adds all components found in the COMPONENT_DIRS directories by default](https://docs.espressif.com/projects/esp-idf/en/latest/esp32/api-guides/build-system.html#optional-project-variables), no extra cmake include nonsense is necessary.

Note: I had to pin lvgl_esp32_drivers to the `develop` branch because `main` wasn't working.
