# Introducción a la infraestructura virtual: concepto y soporte físico

## Ejercicio 1

**Consultar en el catálogo de alguna tienda de informática el precio de un
ordenador tipo servidor y calcular su coste de amortización a cuatro y siete
años. Consultar [este artículo en Infoautónomos sobre el tema](https://infoautonomos.eleconomista.es/consultas-a-la-comunidad/988/).**

El servidor elegido es [este](https://www.pccomponentes.com/dell-poweredge-t130-intel-xeon-v6-e3-1220-8-gb-1tb).

Para calcular la amortización, tenemos que dividir el valor real del servidor, es decir, 453.72€
(el precio sin IVA) entre el tiempo que dura. El valor obtenido nos indica cuánto del valor real
del bien tendríamos que ahorrar anualmente durante *X* años para poder sustituirlo al cabo de esos
*X* años por un nuevo bien del mismo valor en caso de ser necesario.


- Para el caso de cuatro años, tenemos la siguiente amortización:

<img src="https://latex.codecogs.com/gif.latex?\text{Amortizacion}=\frac{Valor\;Real}{Tiempo\;que\;dura}=\frac{453.72\euro}{4}=113.43\euro" />

Por tanto, habría que ahorrar unos 113.43€ anualmente para poder amortizar su coste.

- Para el caso de siete años, tenemos la siguiente amortización:

<img src="https://latex.codecogs.com/gif.latex?\text{Amortizacion}=\frac{Valor\;Real}{Tiempo\;que\;dura}=\frac{453.72\euro}{7}=64.82\euro" />

Por tanto, habría que ahorrar unos 64.82€ anualmente para poder amortizar su coste.

## Ejercicio 2

**Usando las tablas de precios de servicios de alojamiento en Internet “clásicos”,
es decir, que ofrezcan *Virtual Private Servers* o servidores físicos, y de proveedores
de servicios en la nube, comparar el coste durante un año de un ordenador con un
procesador estándar (escogerlo de forma que sea el mismo tipo de procesador en los
dos vendedores) y con el resto de las características similares (tamaño de disco
duro equivalente a transferencia de disco duro) en el caso de que la infraestructura
comprada se usa solo el 1% o el 10% del tiempo.**

He consultado dos páginas. La primera es la de [OVS](https://www.ovh.es/vps/vps-cloud.xml),
donde he seleccionado la segunda opción (VPS Cloud 2), la cuál tiene un coste de 19.35€ al mes,
con 2 CPUs, 4GB de RAM y 50 GB de almacenamiento. La segunda es la de [HispaWeb](https://hispaweb.com/cart.php#kvm-lin),
donde he escogido la opción Lowcost Cloud Server S, la cuál tiene un coste de 10€ al mes,
con 2CPUs, 4GB de RAM y 40 GB de almacenamiento.

El coste anual en cada caso es el siguiente:

* Para OVS, el coste anual es:

<img src="https://latex.codecogs.com/gif.latex?Coste\;OVS=19.35\euro\times12=232.20\euro" />

* Para HispaWeb, el coste es:

<img src="https://latex.codecogs.com/gif.latex?Coste\;HispaWeb=10\euro\times12=120\euro" />

Si usaramos la infraestructura solo un 1% del tiempo, el coste sería el siguiente,
para cada uno de los casos:

* Para OVS, el coste sería:

<img src="https://latex.codecogs.com/gif.latex?Coste\;OVS=232.20\euro\times0.01=2.32\euro" />

* Para HispaWeb, el coste es:

<img src="https://latex.codecogs.com/gif.latex?Coste\;HispaWeb=120\euro\times0.01=1.2\euro" />

Si usaramos la infraestructura solo un 10% del tiempo, el coste sería el siguiente,
para cada uno de los casos:

* Para OVS, el coste sería:

<img src="https://latex.codecogs.com/gif.latex?Coste\;OVS=232.20\euro\times0.1=23.2\euro" />

* Para HispaWeb, el coste es:

<img src="https://latex.codecogs.com/gif.latex?Coste\;HispaWeb=120\euro\times0.1=12\euro" />

## Ejercicio 3

**En general, cualquier ordenador con menos de 5 o 6 años tendrá estos *flags*.
¿Qué modelo de procesador es? ¿Qué aparece como salida de esa orden? Si usas una
máquina virtual, ¿qué resultado da? ¿Y en una Raspberry Pi o, si tienes acceso,
[el procesador del móvil](https://stackoverflow.com/questions/26239956/how-to-get-specific-information-of-an-android-device-from-proc-cpuinfo-file)?**

El procesador de mi portátil es un Intel i7-7700. Esto lo he obtenido utilizando el
siguiente comando:

```bash
lscpu
```

La salida que me ha ofrecido es:

```
Arquitectura:                        x86_64
modo(s) de operación de las CPUs:    32-bit, 64-bit
Orden de los bytes:                  Little Endian
CPU(s):                              8
Lista de la(s) CPU(s) en línea:      0-7
Hilo(s) de procesamiento por núcleo: 2
Núcleo(s) por «socket»:              4
«Socket(s)»                          1
Modo(s) NUMA:                        1
ID de fabricante:                    GenuineIntel
Familia de CPU:                      6
Modelo:                              158
Nombre del modelo:                   Intel(R) Core(TM) i7-7700HQ CPU @ 2.80GHz
Revisión:                            9
CPU MHz:                             1338.074
CPU MHz máx.:                        3800,0000
CPU MHz mín.:                        800,0000
BogoMIPS:                            5616.00
Virtualización:                      VT-x
Caché L1d:                           32K
Caché L1i:                           32K
Caché L2:                            256K
Caché L3:                            6144K
CPU(s) del nodo NUMA 0:              0-7
Indicadores:                         fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush dts acpi mmx fxsr sse sse2 ss ht tm pbe syscall nx pdpe1gb rdtscp lm constant_tsc art arch_perfmon pebs bts rep_good nopl xtopology nonstop_tsc cpuid aperfmperf tsc_known_freq pni pclmulqdq dtes64 monitor ds_cpl vmx est tm2 ssse3 sdbg fma cx16 xtpr pdcm pcid sse4_1 sse4_2 x2apic movbe popcnt tsc_deadline_timer aes xsave avx f16c rdrand lahf_lm abm 3dnowprefetch cpuid_fault epb invpcid_single pti ssbd ibrs ibpb stibp tpr_shadow vnmi flexpriority ept vpid fsgsbase tsc_adjust bmi1 avx2 smep bmi2 erms invpcid mpx rdseed adx smap clflushopt intel_pt xsaveopt xsavec xgetbv1 xsaves dtherm ida arat pln pts hwp hwp_notify hwp_act_window hwp_epp md_clear flush_l1d
```

Para ver qué *flags* tiene activados el procesador, he utilizado la orden:

```bash
egrep '^flags.*(vmx|svm)' /proc/cpuinfo
```

La salida que me ha dado la orden es la siguiente:

```
flags		: fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush dts acpi mmx fxsr sse sse2 ss ht tm pbe syscall nx pdpe1gb rdtscp lm constant_tsc art arch_perfmon pebs bts rep_good nopl xtopology nonstop_tsc cpuid aperfmperf tsc_known_freq pni pclmulqdq dtes64 monitor ds_cpl vmx est tm2 ssse3 sdbg fma cx16 xtpr pdcm pcid sse4_1 sse4_2 x2apic movbe popcnt tsc_deadline_timer aes xsave avx f16c rdrand lahf_lm abm 3dnowprefetch cpuid_fault epb invpcid_single pti ssbd ibrs ibpb stibp tpr_shadow vnmi flexpriority ept vpid fsgsbase tsc_adjust bmi1 avx2 smep bmi2 erms invpcid mpx rdseed adx smap clflushopt intel_pt xsaveopt xsavec xgetbv1 xsaves dtherm ida arat pln pts hwp hwp_notify hwp_act_window hwp_epp md_clear flush_l1d
flags		: fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush dts acpi mmx fxsr sse sse2 ss ht tm pbe syscall nx pdpe1gb rdtscp lm constant_tsc art arch_perfmon pebs bts rep_good nopl xtopology nonstop_tsc cpuid aperfmperf tsc_known_freq pni pclmulqdq dtes64 monitor ds_cpl vmx est tm2 ssse3 sdbg fma cx16 xtpr pdcm pcid sse4_1 sse4_2 x2apic movbe popcnt tsc_deadline_timer aes xsave avx f16c rdrand lahf_lm abm 3dnowprefetch cpuid_fault epb invpcid_single pti ssbd ibrs ibpb stibp tpr_shadow vnmi flexpriority ept vpid fsgsbase tsc_adjust bmi1 avx2 smep bmi2 erms invpcid mpx rdseed adx smap clflushopt intel_pt xsaveopt xsavec xgetbv1 xsaves dtherm ida arat pln pts hwp hwp_notify hwp_act_window hwp_epp md_clear flush_l1d
flags		: fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush dts acpi mmx fxsr sse sse2 ss ht tm pbe syscall nx pdpe1gb rdtscp lm constant_tsc art arch_perfmon pebs bts rep_good nopl xtopology nonstop_tsc cpuid aperfmperf tsc_known_freq pni pclmulqdq dtes64 monitor ds_cpl vmx est tm2 ssse3 sdbg fma cx16 xtpr pdcm pcid sse4_1 sse4_2 x2apic movbe popcnt tsc_deadline_timer aes xsave avx f16c rdrand lahf_lm abm 3dnowprefetch cpuid_fault epb invpcid_single pti ssbd ibrs ibpb stibp tpr_shadow vnmi flexpriority ept vpid fsgsbase tsc_adjust bmi1 avx2 smep bmi2 erms invpcid mpx rdseed adx smap clflushopt intel_pt xsaveopt xsavec xgetbv1 xsaves dtherm ida arat pln pts hwp hwp_notify hwp_act_window hwp_epp md_clear flush_l1d
flags		: fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush dts acpi mmx fxsr sse sse2 ss ht tm pbe syscall nx pdpe1gb rdtscp lm constant_tsc art arch_perfmon pebs bts rep_good nopl xtopology nonstop_tsc cpuid aperfmperf tsc_known_freq pni pclmulqdq dtes64 monitor ds_cpl vmx est tm2 ssse3 sdbg fma cx16 xtpr pdcm pcid sse4_1 sse4_2 x2apic movbe popcnt tsc_deadline_timer aes xsave avx f16c rdrand lahf_lm abm 3dnowprefetch cpuid_fault epb invpcid_single pti ssbd ibrs ibpb stibp tpr_shadow vnmi flexpriority ept vpid fsgsbase tsc_adjust bmi1 avx2 smep bmi2 erms invpcid mpx rdseed adx smap clflushopt intel_pt xsaveopt xsavec xgetbv1 xsaves dtherm ida arat pln pts hwp hwp_notify hwp_act_window hwp_epp md_clear flush_l1d
flags		: fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush dts acpi mmx fxsr sse sse2 ss ht tm pbe syscall nx pdpe1gb rdtscp lm constant_tsc art arch_perfmon pebs bts rep_good nopl xtopology nonstop_tsc cpuid aperfmperf tsc_known_freq pni pclmulqdq dtes64 monitor ds_cpl vmx est tm2 ssse3 sdbg fma cx16 xtpr pdcm pcid sse4_1 sse4_2 x2apic movbe popcnt tsc_deadline_timer aes xsave avx f16c rdrand lahf_lm abm 3dnowprefetch cpuid_fault epb invpcid_single pti ssbd ibrs ibpb stibp tpr_shadow vnmi flexpriority ept vpid fsgsbase tsc_adjust bmi1 avx2 smep bmi2 erms invpcid mpx rdseed adx smap clflushopt intel_pt xsaveopt xsavec xgetbv1 xsaves dtherm ida arat pln pts hwp hwp_notify hwp_act_window hwp_epp md_clear flush_l1d
flags		: fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush dts acpi mmx fxsr sse sse2 ss ht tm pbe syscall nx pdpe1gb rdtscp lm constant_tsc art arch_perfmon pebs bts rep_good nopl xtopology nonstop_tsc cpuid aperfmperf tsc_known_freq pni pclmulqdq dtes64 monitor ds_cpl vmx est tm2 ssse3 sdbg fma cx16 xtpr pdcm pcid sse4_1 sse4_2 x2apic movbe popcnt tsc_deadline_timer aes xsave avx f16c rdrand lahf_lm abm 3dnowprefetch cpuid_fault epb invpcid_single pti ssbd ibrs ibpb stibp tpr_shadow vnmi flexpriority ept vpid fsgsbase tsc_adjust bmi1 avx2 smep bmi2 erms invpcid mpx rdseed adx smap clflushopt intel_pt xsaveopt xsavec xgetbv1 xsaves dtherm ida arat pln pts hwp hwp_notify hwp_act_window hwp_epp md_clear flush_l1d
flags		: fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush dts acpi mmx fxsr sse sse2 ss ht tm pbe syscall nx pdpe1gb rdtscp lm constant_tsc art arch_perfmon pebs bts rep_good nopl xtopology nonstop_tsc cpuid aperfmperf tsc_known_freq pni pclmulqdq dtes64 monitor ds_cpl vmx est tm2 ssse3 sdbg fma cx16 xtpr pdcm pcid sse4_1 sse4_2 x2apic movbe popcnt tsc_deadline_timer aes xsave avx f16c rdrand lahf_lm abm 3dnowprefetch cpuid_fault epb invpcid_single pti ssbd ibrs ibpb stibp tpr_shadow vnmi flexpriority ept vpid fsgsbase tsc_adjust bmi1 avx2 smep bmi2 erms invpcid mpx rdseed adx smap clflushopt intel_pt xsaveopt xsavec xgetbv1 xsaves dtherm ida arat pln pts hwp hwp_notify hwp_act_window hwp_epp md_clear flush_l1d
flags		: fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush dts acpi mmx fxsr sse sse2 ss ht tm pbe syscall nx pdpe1gb rdtscp lm constant_tsc art arch_perfmon pebs bts rep_good nopl xtopology nonstop_tsc cpuid aperfmperf tsc_known_freq pni pclmulqdq dtes64 monitor ds_cpl vmx est tm2 ssse3 sdbg fma cx16 xtpr pdcm pcid sse4_1 sse4_2 x2apic movbe popcnt tsc_deadline_timer aes xsave avx f16c rdrand lahf_lm abm 3dnowprefetch cpuid_fault epb invpcid_single pti ssbd ibrs ibpb stibp tpr_shadow vnmi flexpriority ept vpid fsgsbase tsc_adjust bmi1 avx2 smep bmi2 erms invpcid mpx rdseed adx smap clflushopt intel_pt xsaveopt xsavec xgetbv1 xsaves dtherm ida arat pln pts hwp hwp_notify hwp_act_window hwp_epp md_clear flush_l1d
```

Como se puede ver, mi procesador es capaz de ofrecer virtualización, ya que el *flag* ```vmx```
se puede encontrar entre la lista de *flags*. Se puede ver además que se ofrece una línea de
salida por cada core lógico de la CPU.

He probado la orden en una máquina virtual que habíamos usado en la asignatura de Fundamentos
de Redes, la cuál tiene un Ubuntu 12.04. La salida que he obtenido ha sido:

![egrep en Ubuntu 12.04](img/tema1/egrep-vm.png)

Como se puede ver, no se dispone de tecnología de virtualización dentro de la máquina virtual,
ya que no aparece ningún *flag* que lo indique.

Al no disponer de unas Raspberry Pi, he tenido que recurrir a consultar la información sobre
la CPU de mi móvil (un OnePlus 6). La CPU que utiliza es Qualcomm SDM845 Snapdragon 845, el cuál
tiene 8 cores.

Para consultar la información, he ejecutado:

```bash
adb shell cat /proc/cpuinfo
```

La salida que he obtenido es:

```
Processor	: AArch64 Processor rev 12 (aarch64)
processor	: 0
BogoMIPS	: 38.40
Features	: fp asimd evtstrm aes pmull sha1 sha2 crc32 atomics fphp asimdhp
CPU implementer	: 0x51
CPU architecture: 8
CPU variant	: 0x7
CPU part	: 0x803
CPU revision	: 12

processor	: 1
BogoMIPS	: 38.40
Features	: fp asimd evtstrm aes pmull sha1 sha2 crc32 atomics fphp asimdhp
CPU implementer	: 0x51
CPU architecture: 8
CPU variant	: 0x7
CPU part	: 0x803
CPU revision	: 12

processor	: 2
BogoMIPS	: 38.40
Features	: fp asimd evtstrm aes pmull sha1 sha2 crc32 atomics fphp asimdhp
CPU implementer	: 0x51
CPU architecture: 8
CPU variant	: 0x7
CPU part	: 0x803
CPU revision	: 12

processor	: 3
BogoMIPS	: 38.40
Features	: fp asimd evtstrm aes pmull sha1 sha2 crc32 atomics fphp asimdhp
CPU implementer	: 0x51
CPU architecture: 8
CPU variant	: 0x7
CPU part	: 0x803
CPU revision	: 12

processor	: 4
BogoMIPS	: 38.40
Features	: fp asimd evtstrm aes pmull sha1 sha2 crc32 atomics fphp asimdhp
CPU implementer	: 0x51
CPU architecture: 8
CPU variant	: 0x6
CPU part	: 0x802
CPU revision	: 13

processor	: 5
BogoMIPS	: 38.40
Features	: fp asimd evtstrm aes pmull sha1 sha2 crc32 atomics fphp asimdhp
CPU implementer	: 0x51
CPU architecture: 8
CPU variant	: 0x6
CPU part	: 0x802
CPU revision	: 13

processor	: 6
BogoMIPS	: 38.40
Features	: fp asimd evtstrm aes pmull sha1 sha2 crc32 atomics fphp asimdhp
CPU implementer	: 0x51
CPU architecture: 8
CPU variant	: 0x6
CPU part	: 0x802
CPU revision	: 13

processor	: 7
BogoMIPS	: 38.40
Features	: fp asimd evtstrm aes pmull sha1 sha2 crc32 atomics fphp asimdhp
CPU implementer	: 0x51
CPU architecture: 8
CPU variant	: 0x6
CPU part	: 0x802
CPU revision	: 13
```

La información de los *flags* se puede consultar [aquí](https://en.wikichip.org/wiki/arm/armv8).
Al ser un procesador basado en ARM, y además al estar en un dispositivo móvil, éste no
dispone de tecnología de virtualización. Esto se debe a que posiblemente la virtualización
sea demasiado costosa en un teléfono móvil, teniendo en cuenta las limitadas capacidades
de CPU y batería que tienen éstos.

## Ejercicio 4

1. **Comprobar si el núcleo instalado en tu ordenador contiene este módulo del
kernel usando la orden ```kvm-ok```. Alternativamente (o además), usar ```lscpu```
como se indica arriba.**
2. **Instalar un hipervisor para gestionar máquinas virtuales, que más adelante
se podrá usar en pruebas y ejercicios.**

### Apartado 1

Al ejecutar ```kvm-ok```, he obtenido lo siguiente:

```
INFO: /dev/kvm exists
KVM acceleration can be used

```

He ejecutado también ```LC_ALL=C lscpu | grep Virtualization```,
y he obtenido la siguiente salida:

```
Virtualization:      VT-x
```

Por tanto, mi ordenador tiene el módulo KVM instalado.

### Apartado 2

En mi ordenador ya tenía instalado el hipervisor **VirtualBox**, de Oracle, el cuál
no es software libre. Lo he elegido más que nada por comodidad, ya que he trabajo con
él durante algún tiempo y más o menos sé manejarme.

![VirtualBox](img/tema1/virtualbox.png)


## Ejercicio 5

**Darse de alta en servicios de nube usando ofertas gratuitas o cupones que
pueda proporcionar el profesor.**

He creado una cuenta en **Amazon Web Services**, ya que ofrece servicios gratuitios
que pueden ser utilizados.

![AWS](img/tema1/aws.png)

## Ejercicio 6

**Darse de alta en una web que permita hacer pruebas con alguno de los
sistemas de gestión de nube anteriores.**

He creado una página en **WordPress** con AWS siguiendo [este tutorial](https://aws.amazon.com/es/getting-started/tutorials/launch-a-wordpress-website/).

![AWS estado WordPress](img/tema1/aws-wordpress.png)

Aquí se puede ver la página resultante:

![Página Wordpress](img/tema1/wordpress.png)
