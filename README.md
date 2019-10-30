
<!-- Este .md fue generado a partir del .Rmd homónimo. Edítese el .Rmd -->

# Datos para proyectos

La carpeta `data` contiene dos conjuntos de datos en tres formatos
distintos (`.csv`, `.gpkg` y `.RDS` de R). Cada conjunto es descrito a
continuación:

  - `data/vivpersgeom_sf.*`. Un total de 850 variables, sobre viviendas,
    personas y geomorfometría a nivel municipal. La mayoría de las
    variables se encuentran bajo columnas con encabezados explícitos.
    Agrupadas, las variables son los
    siguientes:
    
    ``` r
    vivpersgeom_sf <- read.csv('data/vivpersgeom_sf.csv', check.names = F)
    columnas <- colnames(vivpersgeom_sf)
    ```
    
      - Códigos identificadores (6 columnas):
    
    <!-- end list -->
    
    ``` r
    cat(columnas[1:5], sep = '\n')
    ## PROV
    ## MUN
    ## REG
    ## TOPONIMIA
    ## ENLACE
    ```
    
      - Viviendas:
        
          - Tipo de vivienda:
        
        <!-- end list -->
        
        ``` r
        cat(grep('Tipo de vivienda:', columnas, value=T), sep = '\n')
        ## Tipo de vivienda: Casa independiente
        ## Tipo de vivienda: Apartamento
        ## Tipo de vivienda: Pieza en cuartería o parte atrás
        ## Tipo de vivienda: Barracón
        ## Tipo de vivienda: Vivienda compartida con negocio
        ## Tipo de vivienda: Local no construído para habitación
        ## Tipo de vivienda: Otra vivienda particular
        ## Tipo de vivienda: Pensión, casa de huéspedes, hotel
        ## Tipo de vivienda: Cuartel militar
        ## Tipo de vivienda: Cárcel
        ## Tipo de vivienda: Hostipal o centro de salud
        ## Tipo de vivienda: Institución religiosa o internado
        ## Tipo de vivienda: Otro tipo de vivienda colectiva
        ## Tipo de vivienda: Personas sin vivienda
        ```
        
          - Condición de
        ocupación:
        
        <!-- end list -->
        
        ``` r
        cat(grep('Condición de ocupación:', columnas, value=T), sep = '\n')
        ## Condición de ocupación: Ocupada con personas presentes
        ## Condición de ocupación: Desocupada
        ```
        
          - Material
        Construcción:
        
        <!-- end list -->
        
        ``` r
        cat(grep('Material Construcción', columnas, value=T), sep = '\n')
        ## Material Construcción Paredes Exteriores: Block o concreto
        ## Material Construcción Paredes Exteriores: Madera
        ## Material Construcción Paredes Exteriores: Tabla de palma
        ## Material Construcción Paredes Exteriores: Tejamanil
        ## Material Construcción Paredes Exteriores: Yagua
        ## Material Construcción Paredes Exteriores: Otro
        ## Material Construcción Techo: Concreto
        ## Material Construcción Techo: Zinc
        ## Material Construcción Techo: Asbesto cemento
        ## Material Construcción Techo: Cana
        ## Material Construcción Techo: Yagua
        ## Material Construcción Techo: Otro
        ## Material Construcción Piso: Mosaico
        ## Material Construcción Piso: Cemento
        ## Material Construcción Piso: Granito
        ## Material Construcción Piso: Mármol
        ## Material Construcción Piso: Cerámica
        ## Material Construcción Piso: Madera
        ## Material Construcción Piso: Tierra
        ## Material Construcción Piso: Otro
        ```
        
          - Tiene la vivienda cuarto de
        cocina:
        
        <!-- end list -->
        
        ``` r
        cat(grep('Tiene la vivienda cuarto de coc', columnas, value=T), sep = '\n')
        ## Tiene la vivienda cuarto de cocina: Si, dentro de la vivienda
        ## Tiene la vivienda cuarto de cocina: Si, fuera de la vivienda
        ## Tiene la vivienda cuarto de cocina: No tiene
        ```
        
          - Cantidad Cuartos tiene la
        vivienda:
        
        <!-- end list -->
        
        ``` r
        cat(grep('Cantidad Cuartos tiene la viv', columnas, value=T), sep = '\n')
        ## Cantidad Cuartos tiene la vivienda: 1
        ## Cantidad Cuartos tiene la vivienda: 2
        ## Cantidad Cuartos tiene la vivienda: 3
        ## Cantidad Cuartos tiene la vivienda: 4
        ## Cantidad Cuartos tiene la vivienda: 5
        ## Cantidad Cuartos tiene la vivienda: 6
        ## Cantidad Cuartos tiene la vivienda: 7
        ## Cantidad Cuartos tiene la vivienda: 8
        ## Cantidad Cuartos tiene la vivienda: 9
        ## Cantidad Cuartos tiene la vivienda: 10
        ## Cantidad Cuartos tiene la vivienda: 11
        ## Cantidad Cuartos tiene la vivienda: 12
        ## Cantidad Cuartos tiene la vivienda: 13
        ## Cantidad Cuartos tiene la vivienda: 14
        ## Cantidad Cuartos tiene la vivienda: 15
        ```
        
          - Cantidad Hogares en la
        vivienda:
        
        <!-- end list -->
        
        ``` r
        cat(grep('Cantidad Hogares en la vivienda:', columnas, value=T), sep = '\n')
        ## Cantidad Hogares en la vivienda: 1
        ## Cantidad Hogares en la vivienda: 2
        ## Cantidad Hogares en la vivienda: 3
        ## Cantidad Hogares en la vivienda: 4
        ## Cantidad Hogares en la vivienda: 5
        ## Cantidad Hogares en la vivienda: 6 y más
        ## Cantidad Hogares en la vivienda: 7
        ## Cantidad Hogares en la vivienda: 8
        ## Cantidad Hogares en la vivienda: 9
        ```
        
          - Acceso a las viviendas del
        segmento:
        
        <!-- end list -->
        
        ``` r
        cat(grep('Acceso a las viviendas del seg', columnas, value=T), sep = '\n')
        ## Acceso a las viviendas del segmento: Calle asfaltadas
        ## Acceso a las viviendas del segmento: Carretera asfaltada
        ## Acceso a las viviendas del segmento: Calle no asfaltada
        ## Acceso a las viviendas del segmento: Carretera no asfaltada
        ## Acceso a las viviendas del segmento: Callejón
        ## Acceso a las viviendas del segmento: Camino
        ## Acceso a las viviendas del segmento: Otro
        ## Acceso a las viviendas del segmento: No declarado
        ```
        
          - Estado de la mayoría de vías de acceso a viviendas del
            segmento:
        
        <!-- end list -->
        
        ``` r
        cat(grep('Estado de la mayoría de vías', columnas, value=T), sep = '\n')
        ## Estado de la mayoría de vías de acceso a viviendas del segmento: En buen estado
        ## Estado de la mayoría de vías de acceso a viviendas del segmento: Con algunos daños
        ## Estado de la mayoría de vías de acceso a viviendas del segmento: Muy deterioradas
        ## Estado de la mayoría de vías de acceso a viviendas del segmento: Intransitables
        ## Estado de la mayoría de vías de acceso a viviendas del segmento: No declarado
        ```
        
          - Principal medio de transporte utilizado por hogares del
            segmento:
        
        <!-- end list -->
        
        ``` r
        cat(grep('Principal medio de transporte', columnas, value=T), sep = '\n')
        ## Principal medio de transporte utilizado por hogares del segmento: Guagua pública
        ## Principal medio de transporte utilizado por hogares del segmento: Camioneta de transporte público
        ## Principal medio de transporte utilizado por hogares del segmento: Carro público
        ## Principal medio de transporte utilizado por hogares del segmento: Vehículo o carro privado
        ## Principal medio de transporte utilizado por hogares del segmento: Motoconcho
        ## Principal medio de transporte utilizado por hogares del segmento: Burro-caballo-mulo
        ## Principal medio de transporte utilizado por hogares del segmento: A pie
        ## Principal medio de transporte utilizado por hogares del segmento: Otro
        ## Principal medio de transporte utilizado por hogares del segmento: No declarado
        ```
        
          - Medio de transporte llega al
        segmento:
        
        <!-- end list -->
        
        ``` r
        cat(grep('Medio de transporte llega al seg', columnas, value=T), sep = '\n')
        ## Medio de transporte llega al segmento: Guagua: Si
        ## Medio de transporte llega al segmento: Guagua: No
        ## Medio de transporte llega al segmento: Guagua: No declarado
        ## Medio de transporte llega al segmento: Camioneta: Si
        ## Medio de transporte llega al segmento: Camioneta: No
        ## Medio de transporte llega al segmento: Camioneta: No declarado
        ## Medio de transporte llega al segmento: Motoconcho: Si
        ## Medio de transporte llega al segmento: Motoconcho: No
        ## Medio de transporte llega al segmento: Motoconcho: No declarado
        ## Medio de transporte llega al segmento: Otro: Si
        ## Medio de transporte llega al segmento: Otro: No
        ## Medio de transporte llega al segmento: Otro: No declarado
        ```
        
          - Hogares del segmento expuestos
        a:
        
        <!-- end list -->
        
        ``` r
        cat(grep('Hogares del segmento expuestos a:', columnas, value=T), sep = '\n')
        ## Hogares del segmento expuestos a: Derrumbes o deslizamiento de tierra: Si
        ## Hogares del segmento expuestos a: Derrumbes o deslizamiento de tierra: No
        ## Hogares del segmento expuestos a: Derrumbes o deslizamiento de tierra: No declarado
        ## Hogares del segmento expuestos a: Hundimiento de tierra: Si
        ## Hogares del segmento expuestos a: Hundimiento de tierra: No
        ## Hogares del segmento expuestos a: Hundimiento de tierra: No declarado
        ## Hogares del segmento expuestos a: Desprendimiento de rocas: Si
        ## Hogares del segmento expuestos a: Desprendimiento de rocas: No
        ## Hogares del segmento expuestos a: Desprendimiento de rocas: No declarado
        ## Hogares del segmento expuestos a: Incendios forestales: Si
        ## Hogares del segmento expuestos a: Incendios forestales: No
        ## Hogares del segmento expuestos a: Incendios forestales: No declarado
        ```
        
          - Contaminación:
        
        <!-- end list -->
        
        ``` r
        cat(grep('Contaminación:', columnas, value=T), sep = '\n')
        ## Contaminación: Aguas estancadas: Si
        ## Contaminación: Aguas estancadas: No
        ## Contaminación: Aguas estancadas: No declarado
        ## Contaminación: Basura: Si
        ## Contaminación: Basura: No
        ## Contaminación: Basura: No declarado
        ## Contaminación: Cañada: Si
        ## Contaminación: Cañada: No
        ## Contaminación: Cañada: No declarado
        ## Contaminación: Pocilga o granja: Si
        ## Contaminación: Pocilga o granja: No
        ## Contaminación: Pocilga o granja: No declarado
        ## Contaminación: Humo o gases de fábrica: Si
        ## Contaminación: Humo o gases de fábrica: No
        ## Contaminación: Humo o gases de fábrica: No declarado
        ## Contaminación: Desechos o residuos de fábrica, taller, hospital: Si
        ## Contaminación: Desechos o residuos de fábrica, taller, hospital: No
        ## Contaminación: Desechos o residuos de fábrica, taller, hospital: No declarado
        ## Contaminación: Envasadora de gas: Si
        ## Contaminación: Envasadora de gas: No
        ## Contaminación: Envasadora de gas: No declarado
        ## Contaminación: Bomba gasolina: Si
        ## Contaminación: Bomba gasolina: No
        ## Contaminación: Bomba gasolina: No declarado
        ## Contaminación: Fábrica productos químicos: Si
        ## Contaminación: Fábrica productos químicos: No
        ## Contaminación: Fábrica productos químicos: No declarado
        ## Contaminación: Ruído de vehículos y motores: Si
        ## Contaminación: Ruído de vehículos y motores: No
        ## Contaminación: Ruído de vehículos y motores: No declarado
        ## Contaminación: Ruídos de fábrica o taller: Si
        ## Contaminación: Ruídos de fábrica o taller: No
        ## Contaminación: Ruídos de fábrica o taller: No declarado
        ## Contaminación: Ruídos o humo de planta eléctrica: Si
        ## Contaminación: Ruídos o humo de planta eléctrica: No
        ## Contaminación: Ruídos o humo de planta eléctrica: No declarado
        ## Contaminación: Música alta de bares, colmados o vecinos: Si
        ## Contaminación: Música alta de bares, colmados o vecinos: No
        ## Contaminación: Música alta de bares, colmados o vecinos: No declarado
        ## Contaminación: Otra: Si
        ## Contaminación: Otra: No
        ## Contaminación: Otra: No declarado
        ```
        
          - Ubicación viviendas del
        segmento:
        
        <!-- end list -->
        
        ``` r
        cat(grep('Ubicación viviendas del segmento:', columnas, value=T), sep = '\n')
        ## Ubicación viviendas del segmento: Orilla de río o arroyo: Si
        ## Ubicación viviendas del segmento: Orilla de río o arroyo: No
        ## Ubicación viviendas del segmento: Orilla de río o arroyo: No declarado
        ## Ubicación viviendas del segmento: Orilla de cañada o canal: Si
        ## Ubicación viviendas del segmento: Orilla de cañada o canal: No
        ## Ubicación viviendas del segmento: Orilla de cañada o canal: No declarado
        ## Ubicación viviendas del segmento: Ladera de montaña: Si
        ## Ubicación viviendas del segmento: Ladera de montaña: No
        ## Ubicación viviendas del segmento: Ladera de montaña: No declarado
        ## Ubicación viviendas del segmento: En cerro: Si
        ## Ubicación viviendas del segmento: En cerro: No
        ## Ubicación viviendas del segmento: En cerro: No declarado
        ## Ubicación viviendas del segmento: Orilla del mar: Si
        ## Ubicación viviendas del segmento: Orilla del mar: No
        ## Ubicación viviendas del segmento: Orilla del mar: No declarado
        ## Ubicación viviendas del segmento: Playa marítima: Si
        ## Ubicación viviendas del segmento: Playa marítima: No
        ## Ubicación viviendas del segmento: Playa marítima: No declarado
        ## Ubicación viviendas del segmento: Orilla de presa: Si
        ## Ubicación viviendas del segmento: Orilla de presa: No
        ## Ubicación viviendas del segmento: Orilla de presa: No declarado
        ## Ubicación viviendas del segmento: Cercana a barranca: Si
        ## Ubicación viviendas del segmento: Cercana a barranca: No
        ## Ubicación viviendas del segmento: Cercana a barranca: No declarado
        ## Ubicación viviendas del segmento: Cercana de mina: Si
        ## Ubicación viviendas del segmento: Cercana de mina: No
        ## Ubicación viviendas del segmento: Cercana de mina: No declarado
        ## Ubicación viviendas del segmento: Otro lugar de riesgo: Si
        ## Ubicación viviendas del segmento: Otro lugar de riesgo: No
        ## Ubicación viviendas del segmento: Otro lugar de riesgo: No declarado
        ```
        
          - Desastres que afectaron a hogares del
        segmento:
        
        <!-- end list -->
        
        ``` r
        cat(grep('Desastres que afectaron a hogares', columnas, value=T), sep = '\n')
        ## Desastres que afectaron a hogares del segmento: Huracán: Si
        ## Desastres que afectaron a hogares del segmento: Huracán: No
        ## Desastres que afectaron a hogares del segmento: Huracán: No declarado
        ## Desastres que afectaron a hogares del segmento: Tornado: Si
        ## Desastres que afectaron a hogares del segmento: Tornado: No
        ## Desastres que afectaron a hogares del segmento: Tornado: No declarado
        ## Desastres que afectaron a hogares del segmento: Tormenta: Si
        ## Desastres que afectaron a hogares del segmento: Tormenta: No
        ## Desastres que afectaron a hogares del segmento: Tormenta: No declarado
        ## Desastres que afectaron a hogares del segmento: Inundaciones: Si
        ## Desastres que afectaron a hogares del segmento: Inundaciones: No
        ## Desastres que afectaron a hogares del segmento: Inundaciones: No declarado
        ## Desastres que afectaron a hogares del segmento: Lluvias torrenciales: Si
        ## Desastres que afectaron a hogares del segmento: Lluvias torrenciales: No
        ## Desastres que afectaron a hogares del segmento: Lluvias torrenciales: No declarado
        ## Desastres que afectaron a hogares del segmento: Frio excesivo: Si
        ## Desastres que afectaron a hogares del segmento: Frio excesivo: No
        ## Desastres que afectaron a hogares del segmento: Frio excesivo: No declarado
        ## Desastres que afectaron a hogares del segmento: Calor excesivo: Si
        ## Desastres que afectaron a hogares del segmento: Calor excesivo: No
        ## Desastres que afectaron a hogares del segmento: Calor excesivo: No declarado
        ## Desastres que afectaron a hogares del segmento: Maremoto: Si
        ## Desastres que afectaron a hogares del segmento: Maremoto: No
        ## Desastres que afectaron a hogares del segmento: Maremoto: No declarado
        ## Desastres que afectaron a hogares del segmento: Sequía: Si
        ## Desastres que afectaron a hogares del segmento: Sequía: No
        ## Desastres que afectaron a hogares del segmento: Sequía: No declarado
        ## Desastres que afectaron a hogares del segmento: Derrumbe o deslizamiento de tierra: Si
        ## Desastres que afectaron a hogares del segmento: Derrumbe o deslizamiento de tierra: No
        ## Desastres que afectaron a hogares del segmento: Derrumbe o deslizamiento de tierra: No declarado
        ## Desastres que afectaron a hogares del segmento: Hundimiento de tierra: Si
        ## Desastres que afectaron a hogares del segmento: Hundimiento de tierra: No
        ## Desastres que afectaron a hogares del segmento: Hundimiento de tierra: No declarado
        ## Desastres que afectaron a hogares del segmento: Incendio: Si
        ## Desastres que afectaron a hogares del segmento: Incendio: No
        ## Desastres que afectaron a hogares del segmento: Incendio: No declarado
        ## Desastres que afectaron a hogares del segmento: Terremoto: Si
        ## Desastres que afectaron a hogares del segmento: Terremoto: No
        ## Desastres que afectaron a hogares del segmento: Terremoto: No declarado
        ## Desastres que afectaron a hogares del segmento: Otros: Si
        ## Desastres que afectaron a hogares del segmento: Otros: No
        ## Desastres que afectaron a hogares del segmento: Otros: No declarado
        ```
        
          - Centros de refugio de la defensa civil en este
        segmento:
        
        <!-- end list -->
        
        ``` r
        cat(grep('Centros de refugio de la defensa civ', columnas, value=T), sep = '\n')
        ## Centros de refugio de la defensa civil en este segmento: Escuela o Liceo: Si
        ## Centros de refugio de la defensa civil en este segmento: Escuela o Liceo: No
        ## Centros de refugio de la defensa civil en este segmento: Escuela o Liceo: No declarado
        ## Centros de refugio de la defensa civil en este segmento: Iglesia: Si
        ## Centros de refugio de la defensa civil en este segmento: Iglesia: No
        ## Centros de refugio de la defensa civil en este segmento: Iglesia: No declarado
        ## Centros de refugio de la defensa civil en este segmento: Salón comunal: Si
        ## Centros de refugio de la defensa civil en este segmento: Salón comunal: No
        ## Centros de refugio de la defensa civil en este segmento: Salón comunal: No declarado
        ## Centros de refugio de la defensa civil en este segmento: Centro deportivo: Si
        ## Centros de refugio de la defensa civil en este segmento: Centro deportivo: No
        ## Centros de refugio de la defensa civil en este segmento: Centro deportivo: No declarado
        ## Centros de refugio de la defensa civil en este segmento: Otros: Si
        ## Centros de refugio de la defensa civil en este segmento: Otros: No
        ## Centros de refugio de la defensa civil en este segmento: Otros: No declarado
        ```
        
          - Distancia kms de viviendas del segmento hasta: Hospital más
            cercano:
        
        <!-- end list -->
        
        ``` r
        cat(grep('Distancia kms.*Hospital más cercano:', columnas, value=T), sep = '\n')
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 0
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 1
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 2
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 3
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 4
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 5
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 6
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 7
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 8
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 9
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 10
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 11
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 12
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 13
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 14
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 15
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 16
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 17
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 18
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 19
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 20
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 21
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 22
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 23
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 24
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 25
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 26
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 27
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 28
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 29
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 30
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 31
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 32
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 33
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 34
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 35
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 36
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 37
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 38
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 39
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 40
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 41
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 42
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 43
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 44
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 45
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 46
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 47
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 48
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 50
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 52
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 53
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 54
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 55
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 56
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 57
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 58
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 60
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 65
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 66
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 72
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 78
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 80
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: 99
        ## Distancia kms de viviendas del segmento hasta: Hospital más cercano: No declarada
        ```
        
          - Distancia kms de viviendas del segmento hasta: Clinica o
            dispensario más
        cercano:
        
        <!-- end list -->
        
        ``` r
        cat(grep('Distancia kms.*sario más cercano:', columnas, value=T), sep = '\n')
        ## Distancia kms de viviendas del segmento hasta: Clinica o dispensario más cercano: 0
        ## Distancia kms de viviendas del segmento hasta: Clinica o dispensario más cercano: 1
        ## Distancia kms de viviendas del segmento hasta: Clinica o dispensario más cercano: 2
        ## Distancia kms de viviendas del segmento hasta: Clinica o dispensario más cercano: 3
        ## Distancia kms de viviendas del segmento hasta: Clinica o dispensario más cercano: 4
        ## Distancia kms de viviendas del segmento hasta: Clinica o dispensario más cercano: 5
        ## Distancia kms de viviendas del segmento hasta: Clinica o dispensario más cercano: 6
        ## Distancia kms de viviendas del segmento hasta: Clinica o dispensario más cercano: 7
        ## Distancia kms de viviendas del segmento hasta: Clinica o dispensario más cercano: 8
        ## Distancia kms de viviendas del segmento hasta: Clinica o dispensario más cercano: 9
        ## Distancia kms de viviendas del segmento hasta: Clinica o dispensario más cercano: 10
        ## Distancia kms de viviendas del segmento hasta: Clinica o dispensario más cercano: 11
        ## Distancia kms de viviendas del segmento hasta: Clinica o dispensario más cercano: 12
        ## Distancia kms de viviendas del segmento hasta: Clinica o dispensario más cercano: 13
        ## Distancia kms de viviendas del segmento hasta: Clinica o dispensario más cercano: 14
        ## Distancia kms de viviendas del segmento hasta: Clinica o dispensario más cercano: 15
        ## Distancia kms de viviendas del segmento hasta: Clinica o dispensario más cercano: 16
        ## Distancia kms de viviendas del segmento hasta: Clinica o dispensario más cercano: 17
        ## Distancia kms de viviendas del segmento hasta: Clinica o dispensario más cercano: 18
        ## Distancia kms de viviendas del segmento hasta: Clinica o dispensario más cercano: 19
        ## Distancia kms de viviendas del segmento hasta: Clinica o dispensario más cercano: 20
        ## Distancia kms de viviendas del segmento hasta: Clinica o dispensario más cercano: 21
        ## Distancia kms de viviendas del segmento hasta: Clinica o dispensario más cercano: 22
        ## Distancia kms de viviendas del segmento hasta: Clinica o dispensario más cercano: 23
        ## Distancia kms de viviendas del segmento hasta: Clinica o dispensario más cercano: 24
        ## Distancia kms de viviendas del segmento hasta: Clinica o dispensario más cercano: 25
        ## Distancia kms de viviendas del segmento hasta: Clinica o dispensario más cercano: 26
        ## Distancia kms de viviendas del segmento hasta: Clinica o dispensario más cercano: 27
        ## Distancia kms de viviendas del segmento hasta: Clinica o dispensario más cercano: 28
        ## Distancia kms de viviendas del segmento hasta: Clinica o dispensario más cercano: 29
        ## Distancia kms de viviendas del segmento hasta: Clinica o dispensario más cercano: 30
        ## Distancia kms de viviendas del segmento hasta: Clinica o dispensario más cercano: 31
        ## Distancia kms de viviendas del segmento hasta: Clinica o dispensario más cercano: 32
        ## Distancia kms de viviendas del segmento hasta: Clinica o dispensario más cercano: 33
        ## Distancia kms de viviendas del segmento hasta: Clinica o dispensario más cercano: 34
        ## Distancia kms de viviendas del segmento hasta: Clinica o dispensario más cercano: 35
        ## Distancia kms de viviendas del segmento hasta: Clinica o dispensario más cercano: 36
        ## Distancia kms de viviendas del segmento hasta: Clinica o dispensario más cercano: 37
        ## Distancia kms de viviendas del segmento hasta: Clinica o dispensario más cercano: 39
        ## Distancia kms de viviendas del segmento hasta: Clinica o dispensario más cercano: 40
        ## Distancia kms de viviendas del segmento hasta: Clinica o dispensario más cercano: 42
        ## Distancia kms de viviendas del segmento hasta: Clinica o dispensario más cercano: 44
        ## Distancia kms de viviendas del segmento hasta: Clinica o dispensario más cercano: 48
        ## Distancia kms de viviendas del segmento hasta: Clinica o dispensario más cercano: 50
        ## Distancia kms de viviendas del segmento hasta: Clinica o dispensario más cercano: 60
        ## Distancia kms de viviendas del segmento hasta: Clinica o dispensario más cercano: 68
        ## Distancia kms de viviendas del segmento hasta: Clinica o dispensario más cercano: No declarada
        ```
        
          - Distancia kms de viviendas del segmento hasta: Liceo
            secundario más
        cercano:
        
        <!-- end list -->
        
        ``` r
        cat(grep('Distancia kms.*dario más cercano:', columnas, value=T), sep = '\n')
        ## Distancia kms de viviendas del segmento hasta: Liceo secundario más cercano: 0
        ## Distancia kms de viviendas del segmento hasta: Liceo secundario más cercano: 1
        ## Distancia kms de viviendas del segmento hasta: Liceo secundario más cercano: 2
        ## Distancia kms de viviendas del segmento hasta: Liceo secundario más cercano: 3
        ## Distancia kms de viviendas del segmento hasta: Liceo secundario más cercano: 4
        ## Distancia kms de viviendas del segmento hasta: Liceo secundario más cercano: 5
        ## Distancia kms de viviendas del segmento hasta: Liceo secundario más cercano: 6
        ## Distancia kms de viviendas del segmento hasta: Liceo secundario más cercano: 7
        ## Distancia kms de viviendas del segmento hasta: Liceo secundario más cercano: 8
        ## Distancia kms de viviendas del segmento hasta: Liceo secundario más cercano: 9
        ## Distancia kms de viviendas del segmento hasta: Liceo secundario más cercano: 10
        ## Distancia kms de viviendas del segmento hasta: Liceo secundario más cercano: 11
        ## Distancia kms de viviendas del segmento hasta: Liceo secundario más cercano: 12
        ## Distancia kms de viviendas del segmento hasta: Liceo secundario más cercano: 13
        ## Distancia kms de viviendas del segmento hasta: Liceo secundario más cercano: 14
        ## Distancia kms de viviendas del segmento hasta: Liceo secundario más cercano: 15
        ## Distancia kms de viviendas del segmento hasta: Liceo secundario más cercano: 16
        ## Distancia kms de viviendas del segmento hasta: Liceo secundario más cercano: 17
        ## Distancia kms de viviendas del segmento hasta: Liceo secundario más cercano: 18
        ## Distancia kms de viviendas del segmento hasta: Liceo secundario más cercano: 19
        ## Distancia kms de viviendas del segmento hasta: Liceo secundario más cercano: 20
        ## Distancia kms de viviendas del segmento hasta: Liceo secundario más cercano: 21
        ## Distancia kms de viviendas del segmento hasta: Liceo secundario más cercano: 22
        ## Distancia kms de viviendas del segmento hasta: Liceo secundario más cercano: 23
        ## Distancia kms de viviendas del segmento hasta: Liceo secundario más cercano: 24
        ## Distancia kms de viviendas del segmento hasta: Liceo secundario más cercano: 25
        ## Distancia kms de viviendas del segmento hasta: Liceo secundario más cercano: 26
        ## Distancia kms de viviendas del segmento hasta: Liceo secundario más cercano: 27
        ## Distancia kms de viviendas del segmento hasta: Liceo secundario más cercano: 28
        ## Distancia kms de viviendas del segmento hasta: Liceo secundario más cercano: 29
        ## Distancia kms de viviendas del segmento hasta: Liceo secundario más cercano: 30
        ## Distancia kms de viviendas del segmento hasta: Liceo secundario más cercano: 31
        ## Distancia kms de viviendas del segmento hasta: Liceo secundario más cercano: 32
        ## Distancia kms de viviendas del segmento hasta: Liceo secundario más cercano: 33
        ## Distancia kms de viviendas del segmento hasta: Liceo secundario más cercano: 34
        ## Distancia kms de viviendas del segmento hasta: Liceo secundario más cercano: 35
        ## Distancia kms de viviendas del segmento hasta: Liceo secundario más cercano: 36
        ## Distancia kms de viviendas del segmento hasta: Liceo secundario más cercano: 38
        ## Distancia kms de viviendas del segmento hasta: Liceo secundario más cercano: 40
        ## Distancia kms de viviendas del segmento hasta: Liceo secundario más cercano: 41
        ## Distancia kms de viviendas del segmento hasta: Liceo secundario más cercano: 42
        ## Distancia kms de viviendas del segmento hasta: Liceo secundario más cercano: 45
        ## Distancia kms de viviendas del segmento hasta: Liceo secundario más cercano: 50
        ## Distancia kms de viviendas del segmento hasta: Liceo secundario más cercano: 58
        ## Distancia kms de viviendas del segmento hasta: Liceo secundario más cercano: 60
        ## Distancia kms de viviendas del segmento hasta: Liceo secundario más cercano: 66
        ## Distancia kms de viviendas del segmento hasta: Liceo secundario más cercano: 68
        ## Distancia kms de viviendas del segmento hasta: Liceo secundario más cercano: 70
        ## Distancia kms de viviendas del segmento hasta: Liceo secundario más cercano: No declarada
        ```
        
          - Distancia kms de viviendas del segmento hasta: Farmacia más
            cercana:
        
        <!-- end list -->
        
        ``` r
        cat(grep('Distancia kms.*Farmacia más cercana:', columnas, value=T), sep = '\n')
        ## Distancia kms de viviendas del segmento hasta: Farmacia más cercana: 0
        ## Distancia kms de viviendas del segmento hasta: Farmacia más cercana: 1
        ## Distancia kms de viviendas del segmento hasta: Farmacia más cercana: 2
        ## Distancia kms de viviendas del segmento hasta: Farmacia más cercana: 3
        ## Distancia kms de viviendas del segmento hasta: Farmacia más cercana: 4
        ## Distancia kms de viviendas del segmento hasta: Farmacia más cercana: 5
        ## Distancia kms de viviendas del segmento hasta: Farmacia más cercana: 6
        ## Distancia kms de viviendas del segmento hasta: Farmacia más cercana: 7
        ## Distancia kms de viviendas del segmento hasta: Farmacia más cercana: 8
        ## Distancia kms de viviendas del segmento hasta: Farmacia más cercana: 9
        ## Distancia kms de viviendas del segmento hasta: Farmacia más cercana: 10
        ## Distancia kms de viviendas del segmento hasta: Farmacia más cercana: 11
        ## Distancia kms de viviendas del segmento hasta: Farmacia más cercana: 12
        ## Distancia kms de viviendas del segmento hasta: Farmacia más cercana: 13
        ## Distancia kms de viviendas del segmento hasta: Farmacia más cercana: 14
        ## Distancia kms de viviendas del segmento hasta: Farmacia más cercana: 15
        ## Distancia kms de viviendas del segmento hasta: Farmacia más cercana: 16
        ## Distancia kms de viviendas del segmento hasta: Farmacia más cercana: 17
        ## Distancia kms de viviendas del segmento hasta: Farmacia más cercana: 18
        ## Distancia kms de viviendas del segmento hasta: Farmacia más cercana: 19
        ## Distancia kms de viviendas del segmento hasta: Farmacia más cercana: 20
        ## Distancia kms de viviendas del segmento hasta: Farmacia más cercana: 21
        ## Distancia kms de viviendas del segmento hasta: Farmacia más cercana: 22
        ## Distancia kms de viviendas del segmento hasta: Farmacia más cercana: 23
        ## Distancia kms de viviendas del segmento hasta: Farmacia más cercana: 24
        ## Distancia kms de viviendas del segmento hasta: Farmacia más cercana: 25
        ## Distancia kms de viviendas del segmento hasta: Farmacia más cercana: 26
        ## Distancia kms de viviendas del segmento hasta: Farmacia más cercana: 27
        ## Distancia kms de viviendas del segmento hasta: Farmacia más cercana: 28
        ## Distancia kms de viviendas del segmento hasta: Farmacia más cercana: 29
        ## Distancia kms de viviendas del segmento hasta: Farmacia más cercana: 30
        ## Distancia kms de viviendas del segmento hasta: Farmacia más cercana: 31
        ## Distancia kms de viviendas del segmento hasta: Farmacia más cercana: 32
        ## Distancia kms de viviendas del segmento hasta: Farmacia más cercana: 33
        ## Distancia kms de viviendas del segmento hasta: Farmacia más cercana: 34
        ## Distancia kms de viviendas del segmento hasta: Farmacia más cercana: 35
        ## Distancia kms de viviendas del segmento hasta: Farmacia más cercana: 36
        ## Distancia kms de viviendas del segmento hasta: Farmacia más cercana: 37
        ## Distancia kms de viviendas del segmento hasta: Farmacia más cercana: 38
        ## Distancia kms de viviendas del segmento hasta: Farmacia más cercana: 39
        ## Distancia kms de viviendas del segmento hasta: Farmacia más cercana: 40
        ## Distancia kms de viviendas del segmento hasta: Farmacia más cercana: 41
        ## Distancia kms de viviendas del segmento hasta: Farmacia más cercana: 42
        ## Distancia kms de viviendas del segmento hasta: Farmacia más cercana: 43
        ## Distancia kms de viviendas del segmento hasta: Farmacia más cercana: 45
        ## Distancia kms de viviendas del segmento hasta: Farmacia más cercana: 50
        ## Distancia kms de viviendas del segmento hasta: Farmacia más cercana: 55
        ## Distancia kms de viviendas del segmento hasta: Farmacia más cercana: 56
        ## Distancia kms de viviendas del segmento hasta: Farmacia más cercana: 57
        ## Distancia kms de viviendas del segmento hasta: Farmacia más cercana: 60
        ## Distancia kms de viviendas del segmento hasta: Farmacia más cercana: 68
        ## Distancia kms de viviendas del segmento hasta: Farmacia más cercana: 70
        ## Distancia kms de viviendas del segmento hasta: Farmacia más cercana: 80
        ## Distancia kms de viviendas del segmento hasta: Farmacia más cercana: 81
        ## Distancia kms de viviendas del segmento hasta: Farmacia más cercana: 99
        ## Distancia kms de viviendas del segmento hasta: Farmacia más cercana: No declarada
        ```
        
          - Distancia kms de viviendas del segmento hasta: Colmado o
            supermercado más
        cercano:
        
        <!-- end list -->
        
        ``` r
        cat(grep('Distancia kms.*mercado más cercano:', columnas, value=T), sep = '\n')
        ## Distancia kms de viviendas del segmento hasta: Colmado o supermercado más cercano: 0
        ## Distancia kms de viviendas del segmento hasta: Colmado o supermercado más cercano: 1
        ## Distancia kms de viviendas del segmento hasta: Colmado o supermercado más cercano: 2
        ## Distancia kms de viviendas del segmento hasta: Colmado o supermercado más cercano: 3
        ## Distancia kms de viviendas del segmento hasta: Colmado o supermercado más cercano: 4
        ## Distancia kms de viviendas del segmento hasta: Colmado o supermercado más cercano: 5
        ## Distancia kms de viviendas del segmento hasta: Colmado o supermercado más cercano: 6
        ## Distancia kms de viviendas del segmento hasta: Colmado o supermercado más cercano: 7
        ## Distancia kms de viviendas del segmento hasta: Colmado o supermercado más cercano: 8
        ## Distancia kms de viviendas del segmento hasta: Colmado o supermercado más cercano: 9
        ## Distancia kms de viviendas del segmento hasta: Colmado o supermercado más cercano: 10
        ## Distancia kms de viviendas del segmento hasta: Colmado o supermercado más cercano: 11
        ## Distancia kms de viviendas del segmento hasta: Colmado o supermercado más cercano: 12
        ## Distancia kms de viviendas del segmento hasta: Colmado o supermercado más cercano: 13
        ## Distancia kms de viviendas del segmento hasta: Colmado o supermercado más cercano: 14
        ## Distancia kms de viviendas del segmento hasta: Colmado o supermercado más cercano: 15
        ## Distancia kms de viviendas del segmento hasta: Colmado o supermercado más cercano: 16
        ## Distancia kms de viviendas del segmento hasta: Colmado o supermercado más cercano: 17
        ## Distancia kms de viviendas del segmento hasta: Colmado o supermercado más cercano: 18
        ## Distancia kms de viviendas del segmento hasta: Colmado o supermercado más cercano: 19
        ## Distancia kms de viviendas del segmento hasta: Colmado o supermercado más cercano: 20
        ## Distancia kms de viviendas del segmento hasta: Colmado o supermercado más cercano: 22
        ## Distancia kms de viviendas del segmento hasta: Colmado o supermercado más cercano: 23
        ## Distancia kms de viviendas del segmento hasta: Colmado o supermercado más cercano: 24
        ## Distancia kms de viviendas del segmento hasta: Colmado o supermercado más cercano: 25
        ## Distancia kms de viviendas del segmento hasta: Colmado o supermercado más cercano: 28
        ## Distancia kms de viviendas del segmento hasta: Colmado o supermercado más cercano: 29
        ## Distancia kms de viviendas del segmento hasta: Colmado o supermercado más cercano: 30
        ## Distancia kms de viviendas del segmento hasta: Colmado o supermercado más cercano: 32
        ## Distancia kms de viviendas del segmento hasta: Colmado o supermercado más cercano: 35
        ## Distancia kms de viviendas del segmento hasta: Colmado o supermercado más cercano: 40
        ## Distancia kms de viviendas del segmento hasta: Colmado o supermercado más cercano: 50
        ## Distancia kms de viviendas del segmento hasta: Colmado o supermercado más cercano: 52
        ## Distancia kms de viviendas del segmento hasta: Colmado o supermercado más cercano: 53
        ## Distancia kms de viviendas del segmento hasta: Colmado o supermercado más cercano: 54
        ## Distancia kms de viviendas del segmento hasta: Colmado o supermercado más cercano: 56
        ## Distancia kms de viviendas del segmento hasta: Colmado o supermercado más cercano: 57
        ## Distancia kms de viviendas del segmento hasta: Colmado o supermercado más cercano: 60
        ## Distancia kms de viviendas del segmento hasta: Colmado o supermercado más cercano: No declarada
        ```
    
      - Personas:
        
          - Cuál es la relación o parentesco con la jefa o el jefe del
            hogar:
        
        <!-- end list -->
        
        ``` r
        cat(grep('Cuál es la relación o parentesco', columnas, value=T), sep = '\n')
        ## Cuál es la relación o parentesco con la jefa o el jefe del hogar: Jefa o jefe
        ## Cuál es la relación o parentesco con la jefa o el jefe del hogar: Esposo (a) o compañero (a)
        ## Cuál es la relación o parentesco con la jefa o el jefe del hogar: Hijo (a)
        ## Cuál es la relación o parentesco con la jefa o el jefe del hogar: Hijo (a) de crianza
        ## Cuál es la relación o parentesco con la jefa o el jefe del hogar: Padre o madre
        ## Cuál es la relación o parentesco con la jefa o el jefe del hogar: Nieto (a)
        ## Cuál es la relación o parentesco con la jefa o el jefe del hogar: Suegro (a)
        ## Cuál es la relación o parentesco con la jefa o el jefe del hogar: Abuelo (a)
        ## Cuál es la relación o parentesco con la jefa o el jefe del hogar: Hermano (a)
        ## Cuál es la relación o parentesco con la jefa o el jefe del hogar: Empleado (a) doméstico (a)
        ## Cuál es la relación o parentesco con la jefa o el jefe del hogar: Otro pariente
        ## Cuál es la relación o parentesco con la jefa o el jefe del hogar: Yerno o nuera
        ## Cuál es la relación o parentesco con la jefa o el jefe del hogar: No pariente
        ## Cuál es la relación o parentesco con la jefa o el jefe del hogar: Miembro de un hogar colectivo
        ```
        
          - Sexo y población total:
        
        <!-- end list -->
        
        ``` r
        cat(grep('Sexo|Población total', columnas, value=T), sep = '\n')
        ## Sexo: Hombres
        ## Sexo: Mujeres
        ## Población total
        ```
        
          - Edad en grupos (quinquenales 0, 1-4, …. 85 y más; decenales;
            grandes grupos):
        
        <!-- end list -->
        
        ``` r
        cat(grep('^Edad en ', columnas, value=T), sep = '\n')
        ## Edad en grupos quinquenales 0, 1-4, .... 85 y más: 0
        ## Edad en grupos quinquenales 0, 1-4, .... 85 y más: 1 -   4
        ## Edad en grupos quinquenales 0, 1-4, .... 85 y más: 5 -  9
        ## Edad en grupos quinquenales 0, 1-4, .... 85 y más: 10 - 14
        ## Edad en grupos quinquenales 0, 1-4, .... 85 y más: 15 - 19
        ## Edad en grupos quinquenales 0, 1-4, .... 85 y más: 20 - 24
        ## Edad en grupos quinquenales 0, 1-4, .... 85 y más: 25 - 29
        ## Edad en grupos quinquenales 0, 1-4, .... 85 y más: 30 - 34
        ## Edad en grupos quinquenales 0, 1-4, .... 85 y más: 35 - 39
        ## Edad en grupos quinquenales 0, 1-4, .... 85 y más: 40 - 44
        ## Edad en grupos quinquenales 0, 1-4, .... 85 y más: 45 - 49
        ## Edad en grupos quinquenales 0, 1-4, .... 85 y más: 50 - 54
        ## Edad en grupos quinquenales 0, 1-4, .... 85 y más: 55 - 59
        ## Edad en grupos quinquenales 0, 1-4, .... 85 y más: 60 - 64
        ## Edad en grupos quinquenales 0, 1-4, .... 85 y más: 65 - 69
        ## Edad en grupos quinquenales 0, 1-4, .... 85 y más: 70 - 74
        ## Edad en grupos quinquenales 0, 1-4, .... 85 y más: 75 - 79
        ## Edad en grupos quinquenales 0, 1-4, .... 85 y más: 80 - 84
        ## Edad en grupos quinquenales 0, 1-4, .... 85 y más: 85 - 89
        ## Edad en grupos quinquenales 0, 1-4, .... 85 y más: 90 - 94
        ## Edad en grupos quinquenales 0, 1-4, .... 85 y más: 95 - 99
        ## Edad en grupos quinquenales 0, 1-4, .... 85 y más: 100 y más
        ## Edad en grupos decenales: 0 -  9
        ## Edad en grupos decenales: 10 - 19
        ## Edad en grupos decenales: 20 - 29
        ## Edad en grupos decenales: 30 - 39
        ## Edad en grupos decenales: 40 - 49
        ## Edad en grupos decenales: 50 - 59
        ## Edad en grupos decenales: 60 - 69
        ## Edad en grupos decenales: 70 - 79
        ## Edad en grupos decenales: 80 - 89
        ## Edad en grupos decenales: 90 - 99
        ## Edad en grupos decenales: 100 y más
        ## Edad en grandes grupos: 0 - 14
        ## Edad en grandes grupos: 15 - 64
        ## Edad en grandes grupos: 65 y más
        ```
        
          - Discapacidades:
        
        <!-- end list -->
        
        ``` r
        cat(grep('^Dificultad', columnas, value=T), sep = '\n')
        ## Dificultad para Ver, aunque use anteojos o lentes: Si
        ## Dificultad para Ver, aunque use anteojos o lentes: No
        ## Dificultad para Ver, aunque use anteojos o lentes: No declarado
        ## Dificultad para Oir, aunque use audifonos: Si
        ## Dificultad para Oir, aunque use audifonos: No
        ## Dificultad para Oir, aunque use audifonos: No declarado
        ## Dificultad para Caminar o subir escalones: Si
        ## Dificultad para Caminar o subir escalones: No
        ## Dificultad para Caminar o subir escalones: No declarado
        ## Dificultad para mover uno o los dos brazos: Si
        ## Dificultad para mover uno o los dos brazos: No
        ## Dificultad para mover uno o los dos brazos: No declarado
        ## Dificultad para mover uno o las dos piernas: Si
        ## Dificultad para mover uno o las dos piernas: No
        ## Dificultad para mover uno o las dos piernas: No declarado
        ## Dificultad para recordar o concentrarse: Si
        ## Dificultad para recordar o concentrarse: No
        ## Dificultad para recordar o concentrarse: No declarado
        ## Dificultad para agarrar objetos y/o abrir recipientes con las manos: Si
        ## Dificultad para agarrar objetos y/o abrir recipientes con las manos: No
        ## Dificultad para agarrar objetos y/o abrir recipientes con las manos: No declarado
        ## Dificultad para hablar: Si
        ## Dificultad para hablar: No
        ## Dificultad para hablar: No declarado
        ## Dificultad, es Mudo: Si
        ## Dificultad, es Mudo: No
        ## Dificultad, es Mudo: No declarado
        ## Dificultad, tiene problemas mentales: Si
        ## Dificultad, tiene problemas mentales: No
        ## Dificultad, tiene problemas mentales: No declarado
        ## Dificultad, le falta una o las dos piernas: Si
        ## Dificultad, le falta una o las dos piernas: No
        ## Dificultad, le falta una o las dos piernas: No declarado
        ## Dificultad, le falta uno o los dos brazos: Si
        ## Dificultad, le falta uno o los dos brazos: No
        ## Dificultad, le falta uno o los dos brazos: No declarado
        ```
        
          - Educación,
        instrucción:
        
        <!-- end list -->
        
        ``` r
        cat(grep('^Sabe|^Asiste|^Nivel educativo', columnas, value=T), sep = '\n')
        ## Sabe leer y escribir: Sabe leer y escribir
        ## Sabe leer y escribir: No sabe leer ni escribir
        ## Asiste o asistió a la escuela: Asiste
        ## Asiste o asistió a la escuela: No asiste, pero asistió
        ## Asiste o asistió a la escuela: Nunca asistió
        ## Nivel educativo más alto al que asistió: Preprimaria
        ## Nivel educativo más alto al que asistió: Primaria o básica
        ## Nivel educativo más alto al que asistió: Secundaria o media
        ## Nivel educativo más alto al que asistió: Universitaria o superior
        ```
        
          - Categoría
        Ocupacional:
        
        <!-- end list -->
        
        ``` r
        cat(grep('Categoría Ocupacional', columnas, value=T), sep = '\n')
        ## Categoría Ocupacional: Ocupado
        ## Categoría Ocupacional: Cesante
        ## Categoría Ocupacional: Busca trab. 1era Vez
        ## Categoría Ocupacional: Desalentado
        ## Categoría Ocupacional: Quehaceres domésticos
        ## Categoría Ocupacional: Estudiante
        ## Categoría Ocupacional: Rentista
        ## Categoría Ocupacional: Jubilado/Pensionado
        ## Categoría Ocupacional: Discapacitado
        ## Categoría Ocupacional: Anciano
        ## Categoría Ocupacional: Otra actividad
        ## Categoría Ocupacional: Ninguna actividad
        ## Categoría Ocupacional: No declarada
        ```
        
          - Condición Actividad
        Económica:
        
        <!-- end list -->
        
        ``` r
        cat(grep('Condición Actividad Económica: ', columnas, value=T), sep = '\n')
        ## Condición Actividad Económica: Empleado(a) a sueldo o salario
        ## Condición Actividad Económica: Empleador(a) o patrón
        ## Condición Actividad Económica: Trabajador(a) familiar o no familiar sin paga o ganancia
        ## Condición Actividad Económica: Trabajador(a) por cuenta propia
        ## Condición Actividad Económica: Otra
        ## Condición Actividad Económica: No declarada
        ```
    
      - Geomorfometría:
    
    <!-- end list -->
    
    ``` r
    cat(
      unique(
      gsub('_[0-9]*_pct.*$|_min.*$|_max.*$|_media.*$|_mediana.*$|_cuartil.*$|_desv.*$', '',
           columnas[min(grep('^aspect', columnas)):max(grep('^vrm', columnas))])),
      sep = '\n'
    )
    ## aspect_cosine
    ## aspect_sine
    ## aspect
    ## convergence
    ## cti
    ## dev_magnitude
    ## dev_scale
    ## dx
    ## dxx
    ## dxy
    ## dy
    ## dyy
    ## eastness
    ## elev_stdev
    ## geomorfonos
    ## northness
    ## pcurv
    ## rough_magnitude
    ## rough_scale
    ## roughness
    ## slope
    ## spi
    ## tcurv
    ## tpi
    ## tri
    ## vrm
    ```
    
      - Para una descripción de cada variable, consultar el *preprint*
        [“Data Descriptor: Geomorpho90m - Global high-resolution
        geomorphometry layers: empirical evaluation and accuracy
        assessment”](https://peerj.com/preprints/27595.pdf)
    
      - Todas las variables son cuantitativas, excepto `geom`, que se
        refiere a los “geomórfonos” (*geomorphons*). Por medio de
        estadística zonal, para cada municipio se obtuvieron los
        estadísticos descriptivos de las variables cuantitativas (valor
        mínimo, primer cuartil (25%), media, mediana, tercer cuartil
        (75%), valor máximo y desviación estándar). De los geomórfonos,
        al ser cualitativa, se obtuvieron los porcentajes ocupados por
        cada geomórfono en el municipio.

  - `data/onamet_prec_anual_sf.*`. Precipitación anual, desde 1979 hasta
    2014, de las siguientes
estaciones:

<!-- end list -->

``` r
onamet_prec_anual_sf <- read.csv('data/onamet_prec_anual_sf.csv', check.names = F, stringsAsFactors = F)
cat(onamet_prec_anual_sf$Estación, sep = '\n')
## Barahona
## Bayaguana
## Cabrera
## Constanza
## Gaspar Hernández
## Hondo Valle
## Jimaní
## La Unión
## La Vega
## Las Américas
## Moca
## Monte Cristi
## Padre Las Casas
## Polo
## Punta Cana
## Rancho Arriba
## Río San Juan
## Sabana de la Mar
## Salcedo
## Samaná
## San Cristóbal
## Santiago
## Santiago Rodríguez
## Santo Domingo
## Villa Vázquez
```
