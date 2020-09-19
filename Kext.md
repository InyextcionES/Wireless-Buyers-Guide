# Cuándo y qué kexts usar

## [AirportBrcmFixup](https://github.com/acidanthera/AirportBrcmFixup)

Esto es necesario para arreglar el WiFi en muchas tarjetas Broadcom. Mientras no todas lo necesitan generalmente es requerido tenerlo cuando usas tarjetas inalámbricas que no son de Apple. Esto también tiene la adición de la funcionalidad de inyectar kexts Broadcom antiguos a versiones más nuevas de macOS

Nota:

* Tarjetas Airport de Apple y Fenvi no necesitan de este kext

## [BrcmPatchRAM](https://github.com/acidanthera/BrcmPatchRAM/releases)

Requerido para todas las tarjetas inalámbricas que no son de Apple, debido a cómo es manejado el firmware. Esto es en realidad un paquete con varios kexts:

* BrcmBluetoothInjector
* BrcmFirmwareData
* BrcmPatchRAM fix:
  * BrcmPatchRAM3 para 10.14+ (debe ser emparejado con BrcmBluetoothInjector)
  * BrcmPatchRAM2 para 10.11-10.14
  * BrcmPatchRAM para 10.10 o más viejo

Nota:

* Tarjetas Airport de Apple y Fenvi no necesitan de este kext
* El orden de OpenCore es alfabético: Injector -> Data -> RAM

## [BT4LEContinuityFixup](https://github.com/acidanthera/BT4LEContinuityFixup)

Necesario para arreglar errores raros de Continuity que permiten el uso de:

* Handoff
* Hotspot instantáneo
* Airdrop nuevo
* Desbloqueo con Apple Watch

Generalmente no es necesario así que evita el uso de este si ves problemas con tu tarjeta

Nota:

* Tarjetas Airport de Apple y Fenvi no deberían necesitar de este kext
* Continuity requiere una tarjeta soportada Bluetooth 4.0 de baja energía

## [AirPortAtheros40](https://github.com/khronokernel/Wifi-Buyers-Guide/blob/master/AirPortAtheros40.kext.zip)

Este kext es requerido para todos los chipsets Atheros que perdieron soporte en Mojave, incluyendo:

* AR9285
* AR9287
* AR9280
* AR9380

Para instalar AirPortAtheros40 tienes 2 opciones:

* Inyección del Kext via bootloader
* Instalación dentro de macOS(Library/Extensions)

El primer método es el recomendado, y el segundo debería ser evitado pero puede funcionar mejor para algunos usuarios. **Prueba el método de inyección primero**

Para la instalación a macOS:

Necesitarás copiarlo a Library/Extensions(**NO** a System/Library/Extensions) y luego correr el siguiente comando:

```
sudo chown -R root:wheel /L*/E*; sudo chmod -R 755 /L*/E*; sudo kextcache -i /
```

**Nota para usuarios de Catalina**: Estos métodos no funcionan si no portas el framework IO80211 entero, lo que no es ideal por razones de estabilidad

## [ATH9KFixup](https://github.com/chunnann/ATH9KFixup)

Para ser emparejado con AirPortAtheros40 para arreglar soporte con muchas tarjetas Atheros, idea similar a AirportBrcmFixup
