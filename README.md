# clase-26-09-2024
# Diseño de redes de atraso por analisis de frecuencia
Para analizar un sistema basandonos en su respuesta a distintas frecuencias podemos utilizar dos metodos, cada uno con vnetajas y desventajas.

## 1. Diseño por diagrama de bode:
en este metodo de diseño, contamos con tres sub metodos con caracteristicas diferentes:
### 1.1 control por adelanto de fase:
Este tiene la caracteristica de hacer funcionar un sistema mas repido, pero a cambio, este sera mas vulnerable al ruido.
### 1.2 control por atraso de fase:
Este a diferencia del anterior reduce la suceptibilidad del sistema al ruido, pero sacrificando velocidad de respuesta.
### 1.3 control en adelanto-atraso de fase:
por ultimo tenemos una combinacion de los dos metodos anteriores, este toma caracteristicas de ambos, y si no se necesita algo muy especifico, este metodo puede ser el adecuado.

## 2. Control PID:
Es posible sintonizar un controlador PID basandose en la frecuencia sobre todo teniendo en cuenta que efectos tiene cada etapa en el espectro de la frecuencia:

 ### 2.1 Control PD:
 Esta arquitectura mejora la estabilidad este en la alta frecuancia.
 ### 2.2 control PI
 por otro lado este control mejora la estabilidad en la baja frecuencia.

## 3. Margen de fase y ganancia:
Estas son dos caracteristicas que se pueden encontrar en el digrama de Bode de cualquier sistema, nos ayuda a enconrar caracteristicas dinamicas del sistema.

## 3.1 Margen de ganancia:
Este es el cambio de ganancia que hace que un sistema sea inestable en lazo abierto, se mide tomando como referencia la fase de 180° y se representa con el simbolo de MG y unidades de dB.

$$MG>0dB$$ es positivo

$$MG<0dB$$ es negativo

## 3.2 Margen de fase:
Es el cambio de fase necesario para inestabilizar un sistema en lazo abierto, se mide tomando como referencia 0dB de ganancia y se representa con el simbolo de MP y unidades de °.

$$Mp>-180°$$ es positivo

$$Mp<-180°$$ es negativo

## 3.3 Caracteristicas por margen de ganancia y fase
Si MG y MP son positivos el sistema es estable en lazo cerrado.
si MG y MP son cero o negativos el sistema puede ser inestable en lazo cerrado.

![Ejemplo margen de fase y megnitud](imagenes/untitled.jpg)

Figura 1. Ejemplo margen de fase y megnitud
