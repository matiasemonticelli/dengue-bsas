La carpeta contiene los siguientes archivos:

* NBI.gpkg
* Dengue Casos BA.txt
* GIT_DengueBA.ipynb

El archivo "NBI.gpkg" se obtuvo del servidor WFS de INDEC. Contiene los datos correspondientes a los valores de NBI de la provincia de Buenos Aires, discriminado por partido. El script toma la geometría y datos de NBI de dicha capa y le une los datos obtenidos del Boletín Epidemiológico.
El archivo "Dengue Casos BA.txt" contiene la información copiada de la página 17 del Boletín Epidemiológico Semanal de la Provincia de Buenos Aires correspondiente a la semana 17 de 2020 (http://www.ms.gba.gov.ar/sitios/media/files/2020/03/Boletin-epidemiologico-semanal-SE-11-1.pdf-1.pdf). Simplemente se copió y se pegó la información y se cambiaron los nombres de los partidos para hacerlos coincidir con los que figuran en la capa proveniente de INDEC.
El script toma la última columna de la información copiada (la suma de todos los casos, ya sea confirmados o probables), la agrega a la capa de INDEC y agrega columnas con valores ajustados a la cantidad de población. 

Bugs conocidos:
Según las bibliotecas instaladas en Python, puede producirse un bug que provoca que la capa de salida no tenga SRC asignado. En dicho caso, se le puede asignar manualmente en argGis, QGIS o el SIG que se utilice. El SRC correspondiente es EPSG:4326 - WGS 84 - Geográfico.

GIT.DengyeBA.ipynb se encuentra bajo licencia Creative Commons Attribution 4.0 International (CC BY 4.0) (https://creativecommons.org/licenses/by/4.0/). Puede modificar y utilizar el código en sus productos. Le solicito por cortesía que si lo hace, me avise para poder seguir mejorando mi trabajo.
