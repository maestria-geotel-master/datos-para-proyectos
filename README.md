
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
        
          - Características generales de las viviendas:
            
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
    
      - Personas:
    
      - Geomorfología:

  - `data/onamet_prec_anual_sf.*`.
