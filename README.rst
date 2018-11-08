mkdir build
cd build

# Scenario 1, works
Build and flash without ext crystal (led works)

cmake -GNinja  -DBOARD=efr32mg_sltb004a -DCONF_FILE="prj.conf" ../
cp zephyr/zephyr.bin /<path>/TB004/

MCU will reset and board starts to blink

# Build with external clock support
cmake -GNinja  -DBOARD=efr32mg_sltb004a -DCONF_FILE="prj.conf overlay-hfxo.conf" ../
cp zephyr/zephyr.bin /<path>/TB004/

MCU will reset and doesnt blink
