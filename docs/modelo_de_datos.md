# Modelo de datos del proyecto

## Empleado
| Campo | Tipo | Descripción |
|---|---|---|
| cod_empleado | texto | identificador único del empleado |
| name | texto | nombre del empleado |
| mail | texto | correo del empleado |
| muni | texto | municipio de destino |
| dir_registrada | texto | direccion de traslado asociada a cod_empleado |
| lat_t | float | latitud de dir_registrada |
| lon_t | float | longitud estraida de de dir_registrada |
| nivel_geocodificacion | enumeración | reporte del geocodificador |
| ubicacion_verificada | boolean | confirmacion del reporte del geocodificador |

## Solicitud
| Campo | Tipo | Descripción |
|---|---|---|
| id_solicitud| int | identificador de solicitud de ruta generada |
| fecha_op | fecha | dia de la operacion |
| cod_empleado | texto | identificador único del empleado |
| id_sede | texto | identificador de la sede de salida |
| cambio_dir | boolean | registro optativo de cambio de direccion |
| dir_temp | texto | Si cambio_dir = si se asigna nueva direccion temporal de traslado (dir_temp)|
| lat_tmp | float | latitud de cambio_dir |
| lon_tmp | float | longitud estraida de de cambio_dir |
| h_salida | enumeración | franja horaria de recogida |
| obs_ | texto | observaciones del usuario |
| nvl_geocod_temp | enumeración | reporte del geocodificador para dir_temp |
| ubic_veri_temp | boolean | confirmacion del reporte del geocodificador para nvl_geocod_temp |

## Sede
| Campo | Tipo | Descripción |
|---|---|---|
| id_sede | texto | identificador de la sede de salida |
| lat_s | float | latitud de la sede registrada |
| lon_s | float | longitud de la sede registrada |

## Vehiculo
| Campo | Tipo | Descripción |
|---|---|---|
| id_vehi | int | identificador unico del vehiculo |
| pl_vehi | texto | placa del vehiculo |
| tp_vehi | texto | tipo de vehiculo (duster - van) |
| cap_vehi | int | plazas disponibles por tp_vehi |

## Conductor
| Campo | Tipo | Descripción |
|---|---|---|
| id_drv | int | identificador unico del conductor |
| drv_name | texto | nombre del conductor |
| drv_cell | texto | telefono de contacto del conductor |
| drv_status | enumeración | resume si el conductor se encuentra en "servicio" u "off" |

## Asignación
| Campo | Tipo | Descripción |
|---|---|---|
| id_asignacion | int | Identificador unico de asignacion generada |
| fch_asignacion | fecha | dia de la operacion |
| franja_op | fecha y hora | Hora de la operacion asignada | 
| drv_name | texto | nombre del conductor asignado |
| pl_vehi | texto | placa del vehiculo asignado |

## Ruta / parada
| Campo | Tipo | Descripción |
|---|---|---|
| ruta_id | int | identificador unico de la ruta generada |
| ord_id | int | orden genrada |
| sol_id | texto | identificador de solicitud |
| hr_est | fecha | Hora estimada de llegada |








