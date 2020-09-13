# Chipsets Soportados/No soportados

Con macOS hay una cantida limitada de hardware compatible sin importar de qué categoría es, y las tarjetas de WiFi no son excepción.

## Chipsets Soportados

### Big Sur(11)

* BCM943602
* BCM94360
* BCM94352
* BCM94350

### Mojave(10.14) y Catalina(10.15)

* BCM94331
  * Podría requerir que fuerces la carga de IO80211Family.kext cuando corres macOS 10.15, Catalina. Mira `Kernel -> Force` en OpenCore para obtener más detalles. 
* Todos los mencionados en Big Sur(11) también son soportados en Mojave(10.14) y Catalina(10.15)

### High Sierra(10.13)

* BCM943224
* AR9285
* AR9287
* AR9280
* AR9380
* Todos los mencionados en Mojave y posterior también son soportados en High Sierra

# Chipsets no soportados

## Broadcom

* BCM4311
* BCM4312
* BCM4313
* BCM4356
* BCM43142
* BCM43228

## Atheros

* AR5424

## Intel

Actualmente estos chipsets de Intel no están soportados oficialmente en macOS (dirígete aquí para encontrar posibles soluciones: [¿Dónde está mi WiFi Intel?](../misc/intel.md)):

Intel Wireless AX

* Intel® Wi-Fi 6 AX201
* Intel® Wi-Fi 6 AX200

Intel Wireless AC

* Intel® Wireless-AC 9560
* Intel® Wireless-AC 9462
* Intel® Wireless-AC 9461
* Intel® Wireless-AC 9260
* Intel® Dual Band Wireless-AC 3168
* Intel® Dual Band Wireless-AC 8265
* Intel® Dual Band Wireless-AC 8260
* Intel® Dual Band Wireless-AC 3165
* Intel® Dual Band Wireless-AC 7265
* Intel® Dual Band Wireless-AC 7260
* Intel® Dual Band Wireless-AC 3160
* Intel® Dual Band Wireless-AC 7260

Wireless N

* Intel® Dual Band Wireless-N 7265
* Intel® Wireless-N 7265
* Intel® Dual Band Wireless-N 7260
* Intel® Wireless-N 7260
* Intel® Centrino® Advanced-N 6230
* Intel® Centrino® Wireless-N 1030
* Intel® Centrino® Wireless-N 130
* Intel® Centrino® Advanced-N 6235
* Intel® Centrino® Wireless-N 135
* Intel® Centrino® Wireless-N 105
* Intel® Centrino® Wireless-N 2200
* Intel® Centrino® Wireless-N 2230
* Intel® Centrino® Wireless-N 1000
* Intel® Centrino® Advanced-N 6205
* Intel® Centrino® Wireless-N 100
* Intel® Centrino® Wireless-N + WiMAX 6150
* Intel® Centrino® Advanced-N + WiMAX 6250
* Intel® Centrino® Ultimate-N 6300
* Intel® Centrino® Advanced-N 6200
* Intel® Wireless WiFi Link 5100AGN
* Intel® Wireless WiFi Link 5300AGN
* Intel® Wireless WiFi Link 5350AGN
* Intel® Wireless WiFi Link 5150AGN
