# Proyecto QA tester, ESET log_collector

_Para la prueba tecnica se dispone de 4 h para probar la aplicacion 'desktop'_

### Aplicacion a testear:

- **ESET log_collector**, desktop version.

### Organizacion prueba:

- **Pruebas UI:** Testeo de todos los apartados visuales de la aplicacion.
- **Pruebas funcionales:** Validar el funcionamiento de todas las caracteristicas que ofrece la aplicacion, aplicando pruebas de caja blanca/negra/gris, dependiendo de los privilegios que tengamos con la aplicacion.
- **Pruebas de rendimiento:** Tiempos de respuesta, velocidades de carga, consumo de recursos.

## Requerimientos para iniciar la aplicacion

- **TC-01:** Descarga, instalacion e inicio de aplicacion.

  - **TC-01.1.** Descargar _'ESET log_collector'_ e installar.

    - Prerrequisitos: SO windows 7 o superior y permisos administrador.

      | Pasos: |                                                               |
      | ------ | ------------------------------------------------------------- |
      | 1      | Ir a la pag (https://www.eset.com/int/support/log-collector/) |
      | 2      | Click boton 'download'                                        |
      | 3      | Esperar que la aplicacion se descargue                        |
      | 4      | Abrir el archivo descargado para instalar la aplicacion       |
      | 5      | Aceptar permisos y condiciones                                |

    - Resultado esperado: Deve poder hacerse la descarga y la instalacion del software.
    - Resultado obtenido: Correcta descarga e instalacion de la aplicacion.
    - **Estado:** ✅ Prueba pasada con exito.
    - Prioridad: Alta.
    - Bugs: N/A

  - **TC-01.2.** Abrir _'ESET log_collector'_ y dar permisos administrador (requerido por APP)

    - Prerrequisitos: SO windows 7 o superior y permisos administrador.

      | Pasos: |                                  |
      | ------ | -------------------------------- |
      | 1      | Abrir (eset_logcollector.exe)    |
      | 2      | Aceptar permisos administrador   |
      | 3      | Esperar que la aplicacion inicie |

    - Resultado esperado: Deve pedir permisos de administrador al iniciar la app. Iniciar.
    - Resultado obtenido: Correcta ventana de permisos de administrador (click 'SI', inicio correcto de app)
    - **Estado:** 🟨 Prueba pasada con _'bug-001'_
    - Prioridad: Alta.
    - Bugs:
      - Bug-001: La aplicacion se inicia antes de consentir los permisos de administrador.

## Pruebas UI

- **TC-02:** Comprobar si la ventana es como detalla en la documentacion oficial.
  - Prerrequisitos: Apartado grafico oficial (https://support.eset.com/en/kb3466-collect-logs-with-eset-log-collector-for-windows)
  - Resultado esperado: Deve poder verse la app igual que en la documentacion oficial.
  - Resultado obtenido: Correcta visualizacion, salvo _'bug-002'_
  - **Estado:** 🟨 Prueba pasada con _'bug-002'_
  - Prioridad: Media.
  - Bugs:
    - Bug-002:
      - La app detecta si tienes algun producto _'ESET'_ compatible instalado en el pc.
      - No se detecta fallo en la app, aunque no tengas ningun producto 'ESET' instalado.

## Pruebas componentes GUI

- **TC-03:** Boton desplegable 'Perfil de recopilacion'

  - **TC-03.1:** Boton desplegable: 'Perfil de recopilacion' > 'Predeterminado'

    - Prerrequisitos: Tener instalado e iniciado con permisos administrador _'ESET log collector'_

      | Pasos: |                                                 |
      | ------ | ----------------------------------------------- |
      | 1      | Click en desplegable _'Perfil de recopilacion'_ |
      | 2      | Seleccion de opcion _'predetermidado'_          |

    - Resultado esperado: Deve marcar los checked correspondientes a la configuracion predeterminada de la app.
    - Resultado obtenido: Correcta seleccion de los checked.
    - **Estado:** ✅ Prueba pasada con exito.
    - Prioridad: Alta.
    - Bugs: N/A

  - **TC-03.2:** Boton desplegable: 'Perfil de recopilacion' > 'Deteccion de amenazas'

    - Prerrequisitos: Tener instalado e iniciado con permisos administrador _'ESET log collector'_

      | Pasos: |                                                 |
      | ------ | ----------------------------------------------- |
      | 1      | Click en desplegable _'Perfil de recopilacion'_ |
      | 2      | Seleccion de opcion _'Deteccion de amenazas'_   |

    - Resultado esperado: Deve marcar los checked correspondientes a la configuracion para detectar amenazas en el sistema.
    - Resultado obtenido: Correcta seleccion de los checked.
    - **Estado:** ✅ Prueba pasada con exito.
    - Prioridad: Alta.
    - Bugs: N/A

  - **TC-03.3:** Boton desplegable: 'Perfil de recopilacion' > 'Todo'

    - Prerrequisitos: Tener instalado e iniciado con permisos administrador _'ESET log collector'_

      | Pasos: |                                                 |
      | ------ | ----------------------------------------------- |
      | 1      | Click en desplegable _'Perfil de recopilacion'_ |
      | 2      | Seleccion de opcion _'Todo'_                    |

    - Resultado esperado: Deve marcar todos los checked.
    - Resultado obtenido: Correcta seleccion de los checked.
    - **Estado:** ✅ Prueba pasada con exito.
    - Prioridad: Alta.
    - Bugs: N/A

  - **TC-03.4:** Boton desplegable: 'Perfil de recopilacion' > 'Ninguno'

    - Prerrequisitos: Tener instalado e iniciado con permisos administrador _'ESET log collector'_

      | Pasos: |                                                 |
      | ------ | ----------------------------------------------- |
      | 1      | Click en desplegable _'Perfil de recopilacion'_ |
      | 2      | Seleccion de opcion _'Ninguno'_                 |

    - Resultado esperado: Deve desmarcar todos los checked.
    - Resultado obtenido: Ningun checked marcado
    - **Estado:** ✅ Prueba pasada con exito.
    - Prioridad: Alta.
    - Bugs: N/A

  - **TC-03.5:** Boton desplegable: 'Perfil de recopilacion' > 'Personalizado'

    - Prerrequisitos: Tener instalado e iniciado con permisos administrador _'ESET log collector'_

      | Pasos: |                                                 |
      | ------ | ----------------------------------------------- |
      | 1      | Click en desplegable _'Perfil de recopilacion'_ |
      | 2      | Seleccion de opcion _'Personalizado'_           |
      | 3      | Seleccionar todos los checked que quiera        |

    - Resultado esperado: Deve dejarte marcar todos los checked que quiera.
    - Resultado obtenido: Se mantienen los checked que has marcado
    - **Estado:** ✅ Prueba pasada con exito.
    - Prioridad: Alta.
    - Bugs: N/A

- **TC-04:** Boton desplegable: 'Limite de antiguedad de los registros [dias]'

  - Prerrequisitos: Tener instalado e iniciado con permisos administrador _'ESET log collector'_

    | Pasos: |                                                                       |
    | ------ | --------------------------------------------------------------------- |
    | 1      | Click en desplegable _'Limite de antiguedad de los registros [dias]'_ |
    | 2      | Seleccion de opcion _'1'_                                             |
    | 3      | Seleccion de opcion _'5'_                                             |
    | 4      | Seleccion de opcion _'30'_                                            |
    | 5      | Seleccion de opcion _'60'_                                            |

  - Resultado esperado: Deve marcar, entre la seleccion, el numero maximo de dias de antiguedad de los registros
  - Resultado obtenido: Se puede marcar con exito las 4 opciones que nos da el desplegable.
  - **Estado:** ✅ Prueba pasada con exito.
  - Prioridad: Alta.
  - Bugs: N/A

- **TC-05:** Boton desplegable: _'Modo de recoleccion de los registros de ESET'_

  - Prerrequisitos: Tener instalado e iniciado con permisos administrador _'ESET log collector'_

    | Pasos: |                                                                       |
    | ------ | --------------------------------------------------------------------- |
    | 1      | Click en desplegable _'Modo de recoleccion de los registros de ESET'_ |
    | 2      | Seleccion de opcion _'Binario original desde disco'_                  |
    | 3      | Seleccion de opcion _'Binario filtrado'_                              |

  - Resultado esperado: Deve marcar, entre la seleccion, el modo de recoleccion deseado.
  - Resultado obtenido: Se puede marcar con exito las 2 opciones que nos da el desplegable.
  - **Estado:** ✅ Prueba pasada con exito.
  - Prioridad: Alta.
  - Bugs: N/A

- **TC-06:** Boton _'?'_

  - Prerrequisitos: Tener instalado e iniciado con permisos administrador _'ESET log collector'_

    | Pasos: |                      |
    | ------ | -------------------- |
    | 1      | Click en boton _'?'_ |

  - Resultado esperado: Deve abrinte en tu navegador la web oficial de ayuda de la aplicacion.
  - Resultado obtenido: Abre la pagina de ayuda _'https://help.eset.com/elc/4.9/es-ES/'_
  - **Estado:** ✅ Prueba pasada con exito.
  - Prioridad: Alta.
  - Bugs: N/A

- **TC-07:** Desplegable _'Guardar archivo como'_

  - Prerrequisitos: Tener instalado e iniciado con permisos administrador _'ESET log collector'_

    | Pasos: |                                              |
    | ------ | -------------------------------------------- |
    | 1      | Click en boton _'...'_                       |
    | 2      | Seleccionar carpeta donde guardar el archivo |
    | 3      | Click en aceptar                             |

  - Resultado esperado: Deve aparecer en el cuadro de dialogo la ruta especificada.
  - Resultado obtenido: Se muestra la ruta especificada en el cuadro de dialogo.
  - **Estado:** ✅ Prueba pasada con exito.
  - Prioridad: Alta.
  - Bugs: N/A

- **TC-08:** Checked _'Proteger archivo comprimido con contraseña'_

  - Prerrequisitos: Tener instalado e iniciado con permisos administrador _'ESET log collector'_

    | Pasos: |                  |
    | ------ | ---------------- |
    | 1      | Click en checked |

  - Resultado esperado: Deve marcar o desmarcar el checked.
  - Resultado obtenido: Correcta seleccion de checked.
  - **Estado:** ✅ Prueba pasada con exito.
  - Prioridad: Alta.
  - Bugs: N/A

- **TC-09:** _'Icono informacion'_

  - Prerrequisitos: Tener instalado e iniciado con permisos administrador _'ESET log collector'_

    | Pasos: |                                      |
    | ------ | ------------------------------------ |
    | 1      | Hover con raton sobre el icono _'i'_ |

  - Resultado esperado: Deve aparecer un modal informativo sobre la opcion _'Proteger archivo comprimido con contraseña'_
  - Resultado obtenido: Se visualiza el modal con la informacion sobre la opcion.
  - **Estado:** ✅ Prueba pasada con exito.
  - Prioridad: Alta.
  - Bugs: N/A

## Pruebas funcionales

- **TC-10:** Boton 'Recopilar'

  - Prerrequisitos: Tener instalado e iniciado con permisos administrador _'ESET log collector'_

    | Pasos: |                                                                                        |
    | ------ | -------------------------------------------------------------------------------------- |
    | 1      | Seleccion de opcion _'Personalizado'_                                                  |
    | 2      | Seleccion de checked _'Ejecucion de procesos (controladores abiertos y DLL cargados)'_ |
    | 3      | Seleccion de opcion _'30'_                                                             |
    | 4      | Seleccion de opcion _'Binario filtrado'_                                               |
    | 5      | Seleccion de opcion _'Guardar archivo como'_                                           |
    | 6      | Seleccionar ruta para guardar el archivo                                               |
    | 7      | Click en boton _'Recopilar'_                                                           |

  - Resultado esperado: Deve iniciar el proceso, mostrando en el 'registro del proceso' los log hechos con su fecha y despues guardar el '.zip' en la ruta marcada.
  - Resultado obtenido: Correcta visualizacion de los pasos en la consola de logs, correcto guardado de el archivo.
  - **Estado:** ✅ Prueba pasada con exito.
  - Prioridad: Alta.
  - Bugs: N/A

- **TC-11:** Boton 'Recopilar'

  - Prerrequisitos: Tener instalado e iniciado con permisos administrador _'ESET log collector'_

    | Pasos: |                                                                                        |
    | ------ | -------------------------------------------------------------------------------------- |
    | 1      | Seleccion de opcion _'Deteccion de amenazas'_                                          |
    | 2      | Seleccion de checked _'Ejecucion de procesos (controladores abiertos y DLL cargados)'_ |
    | 3      | Seleccion de opcion _'30'_                                                             |
    | 4      | Seleccion de opcion _'Binario original desde disco'_                                   |
    | 5      | Seleccion de opcion _'Guardar archivo como'_                                           |
    | 6      | Seleccionar ruta para guardar el archivo                                               |
    | 7      | Click en boton _'Recopilar'_                                                           |

  - Resultado esperado: Deve iniciar el proceso, mostrando en el 'registro del proceso' los log hechos con su fecha y despues guardar el '.zip' en la ruta marcada.
  - Resultado obtenido:
    - Lanza una ventana de error por no tener instalado el producto de ESET _'SysInspector'_.
    - Si se quita el checked _'Registro de ESET SysInspector'_ te deja continuar con el proceso.
    - Luego de terminar con el proceso lanza una ventada _'warning'_ explicando que se completo la recopilacion, pero con advertencias pendientes.
    - Las cuales se reflejaron en el registro guardado.
  - **Estado:** 🟨 Prueba pasada con 1 bug.
  - Prioridad: Alta.
  - Bugs:
    - **Bug-03:**
      - El programa detecta si se va a hacer un registro de aplicaciones instaladas.
      - Si este detecta que algun registro solicitado por la lista de checked necesita tener instalado en el sistema dicho programa, lanza una ventana de error que no te deja continuar.
      - En este caso si vuelves atras y desactivas el checked de dicho programa, el proceso tendra exito y se cumplira con el resultado esperado.

- **TC-12:** Boton 'Recopilar'

  - Prerrequisitos: Tener instalado e iniciado con permisos administrador _'ESET log collector'_

    | Pasos: |                                              |
    | ------ | -------------------------------------------- |
    | 1      | Seleccion de opcion _'Ninguno'_              |
    | 2      | Seleccion de opcion _'30'_                   |
    | 3      | Seleccion de opcion _'Binario filtrado'_     |
    | 4      | Seleccion de opcion _'Guardar archivo como'_ |
    | 5      | Seleccionar ruta para guardar el archivo     |
    | 6      | Click en boton _'Recopilar'_                 |

  - Resultado esperado: Deveria lanzar una ventana de error, no dejando continuar con el proceso porque no se ha seleccionado ningun checked.
  - Resultado obtenido: Visualizacion de una ventana de error con el mensaje esperado: _'No se ha seleccionado ningun artefacto'_
  - **Estado:** ✅ Prueba pasada con exito.
  - Prioridad: Alta.
  - Bugs: N/A

- **TC-13:** Boton 'Recopilar'

  - Prerrequisitos: Tener instalado e iniciado con permisos administrador _'ESET log collector'_

    | Pasos: |                                                                                        |
    | ------ | -------------------------------------------------------------------------------------- |
    | 1      | Seleccion de opcion _'Personalizado'_                                                  |
    | 2      | Seleccion de checked _'Ejecucion de procesos (controladores abiertos y DLL cargados)'_ |
    | 3      | Seleccion de opcion _'30'_                                                             |
    | 4      | Seleccion de opcion _'Binario filtrado'_                                               |
    | 5      | Seleccion de opcion _'Guardar archivo como'_                                           |
    | 6      | Seleccionar ruta para guardar el archivo                                               |
    | 7      | Marcar checked _'Proteger archivo comprimido con contraseña'_                          |
    | 7      | Click en boton _'Recopilar'_                                                           |

  - Resultado esperado: Tiene que abrir una ventana para solicitar una contraseña, para proteger el archivo creado.
  - Resultado obtenido: Una vez pulsado el boton _'Recopilar'_, todo continua sin pedir nada ni lanzar ninguna ventana.
  - **Estado:** 🟥 Test no superado.
  - Prioridad: Alta.
  - Bugs:
    - **Bug-04:**
      - El programa se inicia correctamente y acaba guardando el archivo en la ruta esperada.
      - Este deveria pedir una contraseña para cifrar el archivo creado.
      - En la ventana de logs no muestra nada al respecto.
      - El proceso termina correctamente, sin el resultado esperado.

- **TC-14:** Archivos creados por la app

  - Prerrequisitos: Tener algun archivo creado anteriormente por la app.

    | Pasos: |                                                     |
    | ------ | --------------------------------------------------- |
    | 1      | Ir a la ruta donde se ha guardo el archivo.         |
    | 2      | Abrir el archivo                                    |
    | 3      | Consultar si los datos solicitados estan correctos. |

  - Resultado esperado: Tiene que poderse abrir el archivo creado '.txt' y visualizarse bien los datos.
  - Resultado obtenido: Archivo en la ruta correcta, y con los datos solicitados
  - **Estado:** ✅ Prueba pasada con exito.
  - Prioridad: Alta.
  - Bugs: N/A

- **TC-15:** Archivos creados con contraseña.

  - Prerrequisitos: Tener algun archivo creado anteriormente por la app.

    | Pasos: |                                                     |
    | ------ | --------------------------------------------------- |
    | 1      | Ir a la ruta donde se ha guardo el archivo.         |
    | 2      | Abrir el archivo                                    |
    | 3      | Consultar si los datos solicitados estan correctos. |

  - Resultado esperado: Deveria abrir el archivo para poder visualizar correctamente los datos solicitados con anterioridad.
  - Resultado obtenido: El archivo creado no se puede abrir por no disponer de la contraseña.
  - **Estado:** 🟥 Test no superado.
  - Prioridad: Alta.
  - Bugs:
    - **Bug-05:**
      - El archivo no se puede abrir por no disponer de la contraseña.
      - Bug relacionado con el **TC-13:** Boton 'Recopilar'
      - Bug relacionado con el **Bug-04:**

- **TC-16:** Archivos creados con contraseña.

  - Prerrequisitos: Tener algun archivo creado anteriormente por la app.

    | Pasos: |                                                     |
    | ------ | --------------------------------------------------- |
    | 1      | Ir a la ruta donde se ha guardo el archivo.         |
    | 2      | Abrir el archivo                                    |
    | 3      | Consultar si los datos solicitados estan correctos. |

  - Resultado esperado: Deveria abrir el archivo para poder visualizar correctamente los datos solicitados con anterioridad.
  - Resultado obtenido:
    - Archivos creados correctamente.
    - Se puede observar que los logs guardados en los archivos no pertenecen a la antiguedad marcada al crear el registro.
  - **Estado:** 🟨 Prueba pasada con 1 bug.
  - Prioridad: Alta.
  - Bugs:
    - **Bug-06:**
      - El archivo no muestra los registros desde la antiguedad de 30 dias.
      - Solo muestra los registros de 2 dias antes a la creacion del archivo.
      - Puede que sea porque no constan mas logs que registrar en esas fechas.

## Pruebas automaticas

### Pruebas hechas con el programa TestComplete de SmartBear.

#### Instalar aplicacion para probarlas funcionalmente, [descargar.](https://smartbear.com/product/testcomplete/desktop-testing/)

#### [Archivo ejecutable en programa TestComplete](./TestProject1/TestProject1.pjs)

#### [Carpeta de fotos sobre los TC automaticos](./TestProject1/TestProject1/KeywordTests/Visualizer/)

#### Todos los TCA (casos de prueba automaticos) son E2E.

- **TCA-A1** / **TC-19**

  - Seleccion de perfil en 'Ninguno'
  - TC relacionado: **TC-12**
  - Link: [archivo test automatizado](./TestProject1/TestProject1/KeywordTests/Visualizer/TC_12_A1_tcKDTest/)
  - Resultado esperado: Deveria mostrar una ventana de 'warning' informando que no se realizara la accion por no seleccionar ningun artefacto.
  - Resultado obtenido: Lanza ventana explicando que no se ha seleccionado ningun artefacto
  - **Estado:** ✅ Prueba pasada con exito.
  - Prioridad: Alta.
  - Bugs: N/A

- **TCA-A2** / **TC-17**

  - Creacion archivo de logs.
  - TC relacionado: **TC-10**
  - Link: [archivo test automatizado](./TestProject1/TestProject1/KeywordTests/Visualizer/TC_10_A2_tcKDTest/)
  - Resultado esperado: Deveria crear y guardar un archivo en la ruta especificada.
  - Resultado obtenido: Crea un archivo y lo guarda en la ruta especificada.
  - **Estado:** ✅ Prueba pasada con exito.
  - Prioridad: Alta.
  - Bugs: N/A

- **TCA-A3** / **TC-18**

  - Creacion archivo de logs.
  - TC relacionado: **TC-11**
  - Link: [archivo test automatizado](./TestProject1/TestProject1/KeywordTests/Visualizer/TC_11_A3_tcKDTest/)
  - Resultado esperado: Deveria crear y guardar un archivo en la ruta especificada.
  - Resultado obtenido:
    - Tiempo estimado de espera para la finalizacion superado.
    - Proceso cancelado manualmente.
  - **Estado:** 🟥 Test no superado.
  - Prioridad: Alta.
  - Bugs:
    - **Bug-07:** El proceso se tuvo que cancelar manualmente por exceso de tiempo de respuesta de la aplicacion.

- **TCA-A4** / **TC-19**

  - Creacion archivo de logs.
  - TC relacionado: **TC-13-15**
  - Link: [archivo test automatizado](./TestProject1/TestProject1/KeywordTests/Visualizer/TC_13_15_A4_tcKDTest/)
  - Resultado esperado: Deveria pedir una contraseña para cifrar el archivo, y pedirla para abrir el mismo en la ruta.
  - Resultado obtenido:
    - No salta ninguna ventana para solicitar una contraseña.
    - Guarda el archivo en la ruta especificada.
    - No se puede habrir el archivo cifrado por contener contraseña.
  - **Estado:** 🟥 Test no superado.
  - Prioridad: Alta.
  - Bugs:
    - **Bug-07:** No se puede abrir el archivo por no disponer de la contraseña, con la cual se cifro el archivo.

## Documentacion extra

- Problema con aplicacion:
  - No he podido realizar las pruebas automaticas con la aplicacion [Katalon](https://katalon.com/).
  - Despues de crear la cuenta y descargar la aplicacion, no he sido capaz de probar la aplicacion [ESET Log Collector](https://www.eset.com/int/support/log-collector/)
  - El problema puede que sea por que la aplicacion de ESET es una version portable, y no esta instalada directamente en el sistema.
  - Aparte de esto, la aplicacion pide permisos de administrador para su ejecucion, lo que parece un problema, a priori, para empezar con el testeo de la app.
  - [Foto del error.](./img/Screenshot%202023-09-24%20125533.png)
