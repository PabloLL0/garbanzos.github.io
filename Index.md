Informe NILs
================
Adrián Pérez Rial <z12peria@uco.es>
2026-11-18

<img src="Logo_UCO.png" style="width:10.0%" />

<img src="Logo_FacCiencias.png" style="width:10.0%" />

------------------------------------------------------------------------

<!-- Inicio Rmd -->

<!--  Antes de comenzar: Debes crear el archivo con las referencias de R y de los paquetes que vayas a utilizar.  Puedes actualizar este archivo en cualquier momento.  Solo tienes que añadir el nuevo paquete a la lista y ejecutar nuevamente el código.  Se creará un archivo con las referencias bibliográficas en formato BibTeX. De forma automática, también se incluirá la referencia de R. -->

<!-- Crear archivo BibTeX con las referencias de R y los paquetes utilizados -->

------------------------------------------------------------------------

<!-- Configuración global de los bloques de código, `echo = TRUE` -> todo el código utilizado en este documento aparecerá en el documento final salvo que se expecifique lo contrario, a excepción de este bloque de código, `include=TRUE`  -->

<!-- Para generar títulos, subtítulos etc se usa # el número de # determina el estilo y el formato del texto -->

# Introducción

## El trabajo seleccionado

<!-- Trabajamos los diferentes estilos de text (negrita, cursiva, tachado, superíndice y subíndice), notas a pie de página [^N], citas >  -->

<!-- En HTML podemos usar la etiqueda de css para usar diferentes colores en el texto:  -->

<!-- {style="color:______; font-size:_____;"} -->

Vamos a trabajar con los datos de . Este trabajo describe
<span style="color: green;">genes candidatos de la floración</span> en
<span style="color: red;">garbanzo</span> (*Cicer arietinum*) como
***MED16***, ***BBX24*** o ***ELF3***, este último también reportado por
otros estudios como . Los mecanismos básicos de floración estudiados en
la planta modelo *Arabidopsis thaliana* están conservados en las
leguminosas , exceptuando ciertos genes como ***CONSTANS***

## Los datos

<!-- Leer los datos desde el fichero que está en la misma carpeta que Rmarkdown. Si el fichero está en otra carpeta actualizar la localización del archivo -->

<!-- Links a páginas/archivos externos [](direcciónLink)  -->

Los datos de este proyecto fueron descargados desde [NILs
Adrián](https://bmcplantbiol.biomedcentral.com/articles/10.1186/s12870-024-05411-y).

<!-- Primera vista de los datos -->

| CHROM | POS | ID | REF | ALT | NF10/82-L | NF10/82-E | QUAL | FILTER | INFO | FORMAT |
|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|
| NC_021160.1 | 72 | . | T | C,G | 0/1 | 1/2 | 2117.19 | PASS | AC=2,1;AF=0.500,0.250;AN=4;ANN=C\|downstream_gene_variant\|MODIFIER\|exon-XR_001143330.2-1\|GENE_exon-XR_001143330.2-1\|transcript\|rna-XR_001143330.2\|pseudogene\|\|n.*169A\>G\|\|\|\|\|169\|,G\|downstream_gene_variant\|MODIFIER\|exon-XR_001143330.2-1\|GENE_exon-XR_001143330.2-1\|transcript\|rna-XR_001143330.2\|pseudogene\|\|n.*169A\>C\|\|\|\|\|169\|,C\|intergenic_region\|MODIFIER\|exon-XR_001143330.2-1\|GENE_exon-XR_001143330.2-1\|intergenic_region\|GENE_exon-XR_001143330.2-1\|\|\|n.72T\>C\|\|\|\|\|\|,G\|intergenic_region\|MODIFIER\|exon-XR_001143330.2-1\|GENE_exon-XR_001143330.2-1\|intergenic_region\|GENE_exon-XR_001143330.2-1\|\|\|n.72T\>G\|\|\|\|\|\|;BaseQRankSum=-3.993e+00;ClippingRankSum=0.00;DP=132;ExcessHet=3.0103;FS=7.468;MLEAC=2,1;MLEAF=0.500,0.250;MQ=42.94;MQRankSum=-2.035e+00;QD=18.74;ReadPosRankSum=1.20;SOR=0.208;SAL5=2;SAL10=2;SAL15=2;SAL20=2;SAL30=2;SAL40=2;SAL50=2 | GT:AD:DP:GQ:PL |
| NC_021160.1 | 126 | . | TA | T | 0/0 | 0/1 | 79.83 | QD2 | AC=1;AF=0.250;AN=4;ANN=T\|downstream_gene_variant\|MODIFIER\|exon-XR_001143330.2-1\|GENE_exon-XR_001143330.2-1\|transcript\|rna-XR_001143330.2\|pseudogene\|\|n.\*114delT\|\|\|\|\|114\|,T\|intergenic_region\|MODIFIER\|exon-XR_001143330.2-1\|GENE_exon-XR_001143330.2-1\|intergenic_region\|GENE_exon-XR_001143330.2-1\|\|\|n.127delA\|\|\|\|\|\|;BaseQRankSum=-1.883e+00;ClippingRankSum=0.00;DP=313;ExcessHet=3.9794;FS=5.326;MLEAC=2;MLEAF=0.500;MQ=56.41;MQRankSum=-5.369e+00;QD=0.66;ReadPosRankSum=-1.808e+00;SOR=0.182;SAL5=2;SAL10=2;SAL15=2;SAL20=2;SAL30=2;SAL40=2;SAL50=2 | GT:AD:DP:GQ:PL |
| NC_021160.1 | 161 | . | G | A | 0/0 | 0/1 | 22.21 | QD2 | AC=1;AF=0.250;AN=4;ANN=A\|downstream_gene_variant\|MODIFIER\|exon-XR_001143330.2-1\|GENE_exon-XR_001143330.2-1\|transcript\|rna-XR_001143330.2\|pseudogene\|\|n.\*80C\>T\|\|\|\|\|80\|,A\|intergenic_region\|MODIFIER\|exon-XR_001143330.2-1\|GENE_exon-XR_001143330.2-1\|intergenic_region\|GENE_exon-XR_001143330.2-1\|\|\|n.161G\>A\|\|\|\|\|\|;BaseQRankSum=3.05;ClippingRankSum=0.00;DP=418;ExcessHet=3.0103;FS=29.583;MLEAC=1;MLEAF=0.250;MQ=53.42;MQRankSum=-4.827e+00;QD=0.13;ReadPosRankSum=2.02;SOR=2.047;SAL5=2;SAL10=2;SAL15=2;SAL20=2;SAL30=2;SAL40=2;SAL50=2 | GT:AD:DP:GQ:PGT:PID:PL |
| NC_021160.1 | 450 | . | G | A | 0/0 | 0/1 | 50.19 | QD2 | AC=1;AF=0.250;AN=4;ANN=A\|intragenic_variant\|MODIFIER\|LOC101497325\|gene-LOC101497325\|gene_variant\|gene-LOC101497325\|\|\|n.450G\>A\|\|\|\|\|\|,A\|non_coding_transcript_exon_variant\|MODIFIER\|exon-XR_001143330.2-1\|GENE_exon-XR_001143330.2-1\|transcript\|rna-XR_001143330.2\|pseudogene\|3/3\|n.310C\>T\|\|\|\|\|\|;BaseQRankSum=3.69;ClippingRankSum=0.00;DP=161;ExcessHet=3.0103;FS=48.565;MLEAC=1;MLEAF=0.250;MQ=56.46;MQRankSum=0.268;QD=0.63;ReadPosRankSum=0.049;SOR=5.892;SAL5=2;SAL10=2;SAL15=2;SAL20=2;SAL30=2;SAL40=2;SAL50=2 | GT:AD:DP:GQ:PL |
| NC_021160.1 | 1942 | . | C | A | 0/1 | 1/1 | 1162.33 | MQ40;map;mrd30 | AC=3;AF=0.750;AN=4;ANN=A\|upstream_gene_variant\|MODIFIER\|exon-XR_001143330.2-1\|GENE_exon-XR_001143330.2-1\|transcript\|rna-XR_001143330.2\|pseudogene\|\|n.-960G\>T\|\|\|\|\|960\|,A\|intergenic_region\|MODIFIER\|exon-XR_001143330.2-1-exon-XR_001143419.2-1\|GENE_exon-XR_001143330.2-1-GENE_exon-XR_001143419.2-1\|intergenic_region\|GENE_exon-XR_001143330.2-1-GENE_exon-XR_001143419.2-1\|\|\|n.1942C\>A\|\|\|\|\|\|;BaseQRankSum=3.03;ClippingRankSum=0.00;DP=61;ExcessHet=3.0103;FS=1.436;MLEAC=3;MLEAF=0.750;MQ=36.83;MQRankSum=-1.360e-01;QD=19.05;ReadPosRankSum=0.477;SOR=0.364;SAL5=2;SAL10=2;SAL15=2;SAL20=2;SAL30=1;SAL40=0;SAL50=0 | GT:AD:DP:GQ:PL |
| NC_021160.1 | 4132 | . | G | T | 0/0 | 0/1 | 89.19 | QD2 | AC=1;AF=0.250;AN=4;ANN=T\|upstream_gene_variant\|MODIFIER\|exon-XR_001143330.2-1\|GENE_exon-XR_001143330.2-1\|transcript\|rna-XR_001143330.2\|pseudogene\|\|n.-3150C\>A\|\|\|\|\|3150\|,T\|intergenic_region\|MODIFIER\|exon-XR_001143330.2-1-exon-XR_001143419.2-1\|GENE_exon-XR_001143330.2-1-GENE_exon-XR_001143419.2-1\|intergenic_region\|GENE_exon-XR_001143330.2-1-GENE_exon-XR_001143419.2-1\|\|\|n.4132G\>T\|\|\|\|\|\|;BaseQRankSum=-5.200e-01;ClippingRankSum=0.00;DP=136;ExcessHet=3.0103;FS=0.000;MLEAC=1;MLEAF=0.250;MQ=57.11;MQRankSum=-6.841e+00;QD=1.27;ReadPosRankSum=-7.000e-02;SOR=0.717;SAL5=2;SAL10=2;SAL15=2;SAL20=2;SAL30=2;SAL40=2;SAL50=2 | GT:AD:DP:GQ:PGT:PID:PL |
| NC_021160.1 | 4147 | . | G | C | 0/0 | 0/1 | 82.19 | QD2 | AC=1;AF=0.250;AN=4;ANN=C\|upstream_gene_variant\|MODIFIER\|exon-XR_001143330.2-1\|GENE_exon-XR_001143330.2-1\|transcript\|rna-XR_001143330.2\|pseudogene\|\|n.-3165C\>G\|\|\|\|\|3165\|,C\|intergenic_region\|MODIFIER\|exon-XR_001143330.2-1-exon-XR_001143419.2-1\|GENE_exon-XR_001143330.2-1-GENE_exon-XR_001143419.2-1\|intergenic_region\|GENE_exon-XR_001143330.2-1-GENE_exon-XR_001143419.2-1\|\|\|n.4147G\>C\|\|\|\|\|\|;BaseQRankSum=0.265;ClippingRankSum=0.00;DP=131;ExcessHet=3.0103;FS=0.000;MLEAC=1;MLEAF=0.250;MQ=57.77;MQRankSum=-6.336e+00;QD=1.23;ReadPosRankSum=-6.480e-01;SOR=0.602;SAL5=2;SAL10=2;SAL15=2;SAL20=2;SAL30=2;SAL40=2;SAL50=2 | GT:AD:DP:GQ:PGT:PID:PL |
| NC_021160.1 | 6539 | . | C | A | 0/1 | 0/0 | 226.19 | PASS | AC=1;AF=0.250;AN=4;ANN=A\|intergenic_region\|MODIFIER\|exon-XR_001143330.2-1-exon-XR_001143419.2-1\|GENE_exon-XR_001143330.2-1-GENE_exon-XR_001143419.2-1\|intergenic_region\|GENE_exon-XR_001143330.2-1-GENE_exon-XR_001143419.2-1\|\|\|n.6539C\>A\|\|\|\|\|\|;BaseQRankSum=1.29;ClippingRankSum=0.00;DP=170;ExcessHet=3.0103;FS=22.385;MLEAC=1;MLEAF=0.250;MQ=57.27;MQRankSum=-6.478e+00;QD=2.41;ReadPosRankSum=-9.470e-01;SOR=4.461;SAL5=2;SAL10=2;SAL15=2;SAL20=2;SAL30=2;SAL40=2;SAL50=2 | GT:AD:DP:GQ:PL |

Tabla 1: Diez primeras filas

<!-- El código R en línea -->

Los datos tienen 120441 filas y 11 columnas.

Cada fila se corresponde con un SNP, por tanto, hay 120441 SNPs.

<!-- cargar las librerias que vamos a utilizar, queremos que el código se ejecute, pero no que aparezca en el documento final, también excluímos los avisos y mensajes -->

<!-- Filtra los datos para quedarte solo con los cromosomas (sus códigos empiezan por NC_) -->

Del total de SNPs detectados, 77170 se corresponden con SNPs situados en
cromosomas (Figura 1).

<!-- Calcula el número de SNPs por cromosoma que tiene el garbanzo con la función `count` y guarda los datos ordenados de forma descendiente en variable nueva -->

<!-- Utilizar la variable nueva para hacer un gráfico de barras incluyendo el pie de figura y la posición -->

<div class="figure" style="text-align: center">

<img src="Index_files/figure-gfm/grafico-cromosoma-SNPs-1.png" alt="Figura 1. Número de SNPs por cromosomas" width="60%" />
<p class="caption">

Figura 1. Número de SNPs por cromosomas
</p>

</div>

## Hipótesis

Nuestra hipótesis es que los cromosomas con mayor número de SNPs
presentan mayor % de SNPs que no pasan el filtro de calidad

------------------------------------------------------------------------

# Materiales y Métodos

Para llevar a cabo el análisis usamos R ([R Core Team
2026](#ref-R-base)) con las librerias dplyr ([Wickham, François, et al.
2026](#ref-R-dplyr)) y ggplot ([Wickham, Chang, et al.
2026](#ref-R-ggplot2); [Wickham 2016](#ref-ggplot22016)). Para cargar el
archivo excel hemos usado readxl ([Wickham and Bryan
2025](#ref-R-readxl)). Para la creación de este informe hemos utilizado
el paquete knitr ([Xie 2025](#ref-R-knitr), [2015](#ref-knitr2015),
[2014](#ref-knitr2014)) y pandoc.

------------------------------------------------------------------------

# Resultados

<!-- Selecciona del dataset `Data` únicamente las columnas **CHROM**, **POS** y **FILTER**.   -->

<!-- Puedes describir las columnas con las que te quedas.
<!-- Por ejemplo: En CHROM aparecen los diferentes cromosomas del garbanzo, 
<!-- en POS aparecen las posiciones de los SNPs
<!-- detectados y en FILTER aparece el filtro de calidad.
<!-- Los SNPs que pasan el filtro aparecen
<!-- descritos como PASS. -->

<!-- Crea una nueva variable en la que todo valor distinto de *PASS* se transforme en *NOT_PASS*.   -->

## Cálculo de porcentajes por cromosoma

El procentaje de SNPs que no pasan el filtro se muentra en la Tabla 2.

| CHROM       | total_SNPs | not_pass | porcentaje_not_pass |
|:------------|-----------:|---------:|--------------------:|
| NC_021160.1 |      31790 |    16175 |                50.9 |
| NC_021161.1 |       7012 |     5147 |                73.4 |
| NC_021162.1 |       5311 |     4591 |                86.4 |
| NC_021163.1 |       5371 |     4580 |                85.3 |
| NC_021164.1 |       6843 |     5814 |                85.0 |
| NC_021165.1 |      12594 |     8388 |                66.6 |
| NC_021166.1 |       6598 |     5699 |                86.4 |
| NC_021167.1 |       1651 |     1283 |                77.7 |

Tabla 2. Porcentaje de SNPs que pasan y no pasan el filtro por cromosoma

## Representación gráfica

El siguiente modelo muestra la relación entre el número total y los SNPs
no filtrados (Figura 2).

<figure>
<img src="Index_files/figure-gfm/grafico-relacion-1.png"
alt="Fig 2. Relación entre el número total de SNPs y el porcentaje de SNPs que no pasan el filtro de calidad" />
<figcaption aria-hidden="true">Fig 2. Relación entre el número total de
SNPs y el porcentaje de SNPs que no pasan el filtro de
calidad</figcaption>
</figure>

------------------------------------------------------------------------

# Conclusiones

Los datos NO apoyan nuestra hipótesis. Es la contraria: los cromosomas
en los que se detectan menos SNPs, presentan mayor porcentaje de SNPs
que no pasan el filtro.

------------------------------------------------------------------------

<!-- Para asegurar la reproducibilidad de los resultados es necesario conocer el sistema operativo y la versión de software y paquetes -->

# Información de la sesión y referencias

    ## Warning: Your system is mis-configured: '/etc/localtime' is not a symlink

    ## Warning: '/etc/localtime' is not identical to any known timezone file

    ## R version 4.5.3 (2026-03-11)
    ## Platform: x86_64-pc-linux-gnu
    ## 
    ## Matrix products: default
    ## BLAS:   /usr/local/lib64/R-4.5.3/lib/libRblas.so 
    ## LAPACK: /usr/local/lib64/liblapack.so.3.10.1  LAPACK version 3.10.1
    ## 
    ## locale:
    ##  [1] LC_CTYPE=es_ES.UTF-8       LC_NUMERIC=C              
    ##  [3] LC_TIME=es_ES.UTF-8        LC_COLLATE=es_ES.UTF-8    
    ##  [5] LC_MONETARY=es_ES.UTF-8    LC_MESSAGES=es_ES.UTF-8   
    ##  [7] LC_PAPER=es_ES.UTF-8       LC_NAME=C                 
    ##  [9] LC_ADDRESS=C               LC_TELEPHONE=C            
    ## [11] LC_MEASUREMENT=es_ES.UTF-8 LC_IDENTIFICATION=C       
    ## 
    ## time zone: NA
    ## tzcode source: system (glibc)
    ## 
    ## attached base packages:
    ## [1] datasets  utils     grDevices graphics  stats     methods   base     
    ## 
    ## other attached packages:
    ## [1] ggplot2_4.0.3 dplyr_1.2.1   readxl_1.4.5 
    ## 
    ## loaded via a namespace (and not attached):
    ##  [1] Matrix_1.7-5       gtable_0.3.6       compiler_4.5.3     tidyselect_1.2.1  
    ##  [5] splines_4.5.3      scales_1.4.0       yaml_2.3.12        fastmap_1.2.0     
    ##  [9] lattice_0.22-9     R6_2.6.1           labeling_0.4.3     generics_0.1.4    
    ## [13] knitr_1.51         tibble_3.3.1       pillar_1.11.1      RColorBrewer_1.1-3
    ## [17] rlang_1.2.0        xfun_0.57          S7_0.2.1           otel_0.2.0        
    ## [21] cli_3.6.5          withr_3.0.2        magrittr_2.0.5     mgcv_1.9-4        
    ## [25] digest_0.6.39      grid_4.5.3         rstudioapi_0.18.0  lifecycle_1.0.5   
    ## [29] nlme_3.1-169       vctrs_0.7.2        evaluate_1.0.5     glue_1.8.0        
    ## [33] farver_2.1.2       cellranger_1.1.0   rmarkdown_2.31     tools_4.5.3       
    ## [37] pkgconfig_2.0.3    htmltools_0.5.9

<div id="refs" class="references csl-bib-body hanging-indent"
entry-spacing="0">

<div id="ref-R-base" class="csl-entry">

R Core Team. 2026. *R: A Language and Environment for Statistical
Computing*. Vienna, Austria: R Foundation for Statistical Computing.
<https://www.R-project.org/>.

</div>

<div id="ref-ggplot22016" class="csl-entry">

Wickham, Hadley. 2016. *Ggplot2: Elegant Graphics for Data Analysis*.
Springer-Verlag New York. <https://ggplot2.tidyverse.org>.

</div>

<div id="ref-R-readxl" class="csl-entry">

Wickham, Hadley, and Jennifer Bryan. 2025. *Readxl: Read Excel Files*.
<https://readxl.tidyverse.org>.

</div>

<div id="ref-R-ggplot2" class="csl-entry">

Wickham, Hadley, Winston Chang, Lionel Henry, Thomas Lin Pedersen,
Kohske Takahashi, Claus Wilke, Kara Woo, Hiroaki Yutani, Dewey
Dunnington, and Teun van den Brand. 2026. *Ggplot2: Create Elegant Data
Visualisations Using the Grammar of Graphics*.
<https://ggplot2.tidyverse.org>.

</div>

<div id="ref-R-dplyr" class="csl-entry">

Wickham, Hadley, Romain François, Lionel Henry, Kirill Müller, and Davis
Vaughan. 2026. *Dplyr: A Grammar of Data Manipulation*.
<https://dplyr.tidyverse.org>.

</div>

<div id="ref-knitr2014" class="csl-entry">

Xie, Yihui. 2014. “Knitr: A Comprehensive Tool for Reproducible Research
in R.” In *Implementing Reproducible Computational Research*, edited by
Victoria Stodden, Friedrich Leisch, and Roger D. Peng. Chapman;
Hall/CRC.

</div>

<div id="ref-knitr2015" class="csl-entry">

———. 2015. *Dynamic Documents with R and Knitr*. 2nd ed. Boca Raton,
Florida: Chapman; Hall/CRC. <https://yihui.org/knitr/>.

</div>

<div id="ref-R-knitr" class="csl-entry">

———. 2025. *Knitr: A General-Purpose Package for Dynamic Report
Generation in r*. <https://yihui.org/knitr/>.

</div>

</div>
