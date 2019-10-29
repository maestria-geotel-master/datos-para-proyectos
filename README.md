
<!-- Este .md fue generado a partir del .Rmd homónimo. Edítese el .Rmd -->

# Datos para proyectos

La carpeta `data` contiene dos conjuntos de datos en tres formatos
distintos (`.csv`, `.gpkg` y `.RDS` de R). Cada conjunto es descrito a
continuación:

  - `data/vivpersgeom_sf.*`. Un total de 850 variables, sobre viviendas,
    personas y geomorfología a nivel municipal. La mayoría de las
    variables se encuentran bajo columnas con encabezados explícitos.
    Agrupadas, las variables son los
    siguientes:
    
    ``` r
    vivpersgeom_sf <- read.csv('data/vivpersgeom_sf.csv', check.names = F)
    ```
    
      - Códigos identificadores (6 columnas):
    
    <!-- end list -->
    
    ``` r
    cat(colnames(vivpersgeom_sf)[1:6], sep = '\n')
    ## PROV
    ## MUN
    ## REG
    ## TOPONIMIA
    ## ENLACE
    ## Municipio de residencia
    ```
    
      - Viviendas:
        
          - Tipo de
        vivienda:
        
        <!-- end list -->
        
        ``` r
        cat(grep('Tipo de vivienda:', colnames(vivpersgeom_sf), value=T), sep = '\n')
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
        cat(grep('Condición de ocupación:', colnames(vivpersgeom_sf), value=T), sep = '\n')
        ## Condición de ocupación: Ocupada con personas presentes
        ## Condición de ocupación: Desocupada
        ```
        
          - Material
        Construcción:
        
        <!-- end list -->
        
        ``` r
        cat(grep('Material Construcción', colnames(vivpersgeom_sf), value=T), sep = '\n')
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
        cat(grep('Tiene la vivienda cuarto de coc', colnames(vivpersgeom_sf), value=T), sep = '\n')
        ## Tiene la vivienda cuarto de cocina: Si, dentro de la vivienda
        ## Tiene la vivienda cuarto de cocina: Si, fuera de la vivienda
        ## Tiene la vivienda cuarto de cocina: No tiene
        ```
        
          - Cantidad Cuartos tiene la
        vivienda:
        
        <!-- end list -->
        
        ``` r
        cat(grep('Cantidad Cuartos tiene la viv:', colnames(vivpersgeom_sf), value=T), sep = '\n')
        ```
        
          - Cantidad Hogares en la
        vivienda:
        
        <!-- end list -->
        
        ``` r
        cat(grep('Cantidad Hogares en la vivienda:', colnames(vivpersgeom_sf), value=T), sep = '\n')
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
        cat(grep('Acceso a las viviendas del seg', colnames(vivpersgeom_sf), value=T), sep = '\n')
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
        cat(grep('Estado de la mayoría de vías', colnames(vivpersgeom_sf), value=T), sep = '\n')
        ## Estado de la mayoría de vías de acceso a viviendas del segmento: En buen estado
        ## Estado de la mayoría de vías de acceso a viviendas del segmento: Con algunos daños
        ## Estado de la mayoría de vías de acceso a viviendas del segmento: Muy deterioradas
        ## Estado de la mayoría de vías de acceso a viviendas del segmento: Intransitables
        ## Estado de la mayoría de vías de acceso a viviendas del segmento: No declarado
        ```
        
          - Estado de la mayoría de vías de acceso a viviendas del
            segmento:
        
        <!-- end list -->
        
        ``` r
        cat(grep('Principal medio de transporte', colnames(vivpersgeom_sf), value=T), sep = '\n')
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
        cat(grep('Medio de transporte llega al seg', colnames(vivpersgeom_sf), value=T), sep = '\n')
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
        cat(grep('Hogares del segmento expuestos a:', colnames(vivpersgeom_sf), value=T), sep = '\n')
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
        cat(grep('Contaminación:', colnames(vivpersgeom_sf), value=T), sep = '\n')
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
        cat(grep('Ubicación viviendas del segmento:', colnames(vivpersgeom_sf), value=T), sep = '\n')
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
        cat(grep('Desastres que afectaron a hogares', colnames(vivpersgeom_sf), value=T), sep = '\n')
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
        cat(grep('Centros de refugio de la defensa civ', colnames(vivpersgeom_sf), value=T), sep = '\n')
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
    
      - Personas:
    
      - Geomorfología:

  - `data/onamet_prec_anual_sf.*`.
