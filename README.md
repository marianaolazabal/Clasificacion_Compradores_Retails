- [x] Limpieza de datos
- [] Hacer el EDA
- [] Probar modelo Kmeans
- [] Evaluar metodo del codo
- [] Evaluar silueta
- [] Probar modelo K-Prototypes
- [] Evaluar metodo del codo
- [] Evaluar silueta
- [] Analizar cual modelo es mejor
- [] Analizar los clusters
 
Ideas objetivos
Categoria deportistas, evento deportivo, ofrecer productos antes
Fijar patrones de compras segun clima
 
# Entendimiento del Negocio
 
Se trata de una empresa que se dedica al rubro de venta online. Compra y disponibiliza los productos en su plataforma para que los clientes compren con mejor comodidad, facilidad y rapidez.
 
# Problema
Con el crecimiento exponencial de las plataformas de ventas online, las empresas se enfrentan cada vez más a la necesidad de comprender los patrones de consumo, identificar oportunidades de ventas y optimizar los procesos productivos.
 
En este análisis, me gustaría centrar la atención en la clasificación de los distintos tipos de clientes. Entender quiénes son los clientes, qué compran y por qué, permite a las empresas diseñar estrategias personalizadas que pueden aumentar la satisfacción del cliente, fomentar la lealtad y, en última instancia, impulsar las ventas.
 
# 1.1 Alcance
 
# 1.1.1 Objetivo
 
Cuando una empresa competitiva busca optimizar sus beneficios, tiene varias estrategias a su disposición. Los beneficios se definen como la diferencia entre ingresos y costos. Los ingresos se calculan como el precio multiplicado por la cantidad vendida (I=p×q).
Para incrementar los ingresos, la empresa puede optar por aumentar el precio, aumentar la cantidad vendida, o una combinación de ambos.
 
La decisión sobre cuál estrategia seguir debe considerar la elasticidad-precio de la demanda, que mide cómo varía la cantidad demandada ante cambios en el precio.
Si la elasticidad-precio de la demanda es alta (demanda elástica), un aumento en el precio llevará a una reducción proporcionalmente mayor en la cantidad demandada, lo que puede resultar en una disminución de los ingresos totales. En cambio, si la elasticidad-precio de la demanda es baja (demanda inelástica), el aumento del precio puede llevar a un incremento en los ingresos, ya que la reducción en la cantidad demandada será menor que el aumento en el precio.
 
Para productos con demanda inelástica, la empresa puede justificar un aumento de precio para maximizar los ingresos, siempre y cuando el incremento en el precio no resulte en una caída significativa en la cantidad demandada. En cambio, para productos con demanda elástica, es crucial enfocarse en estrategias que minimicen los costos y maximicen el volumen de ventas.
 
En el caso de productos con demanda elástica, una estrategia viable podría ser la reducción de costos variables. La disminución de costos variables implica ajustar la cantidad ofertada. Si la empresa opera bajo un modelo de tercerización, donde no produce directamente los bienes, puede implementar ajustes rápidos en la oferta de productos sin necesariamente aumentar costos. Por ejemplo, podría optimizar el proceso de logística y distribución para reducir el costo variable por unidad. Esto incluye agrupar envíos para atender múltiples pedidos con un solo traslado, lo que disminuirá los costos de transporte y distribución.
 
Adicionalmente, la reducción de costos fijos puede ser considerada, aunque esto generalmente requiere una planificación a largo plazo y puede implicar cambios estructurales en la empresa.
 
Por lo tanto, la empresa debe estudiar las siguientes estrategias:
 
Incrementar precios en productos con demanda inelástica: Analizar cómo las variaciones de precio afectan la cantidad demandada y ajustar los precios para maximizar los ingresos.
 
Aumentar la cantidad vendida de productos: Evaluar si es posible incrementar el volumen de ventas sin que esto implique un aumento proporcional en los costos.
 
Optimizar el proceso de distribución: Implementar estrategias logísticas para reducir los costos variables asociados con el transporte, como consolidar envíos y mejorar la eficiencia en la cadena de suministro.


# 1.1.2 Hipótesis

Demandas Marshall y Hicks

Es la teoria economica que se utiliza para entender como los consumidores toman sus decisiones de consumo en base a sus recursos disponibles y sus preferencias de gustos. 

La demanda Marshalliana depende del ingreso del consumidor y de los precios de los bienes disponibles a este. El consumidor quisiera consumir una cantidad x de cada uno de los bienes pero dispone de un ingreso m para hacerlo, por lo que tiene un problema de asignacion de recursos, queriendo optimizar sus utilidades.

- Demanda Marshalliana Básica --> U=xy

- Demanda Marshalliana con Preferencias Cúbicas

- Demanda Marshalliana con Preferencias Heterogéneas

- Demanda Marshalliana con Funciones de Utilidad No Convexas

## IDEAS ##

Encontrar la demanda para cada producto. Tendria que encontrar una funcion de demanda para cada cliente, cada producto y despues sumarlas para tener la de la pagina.

Ligadas a las características de la orden

H1. El importe gastado en la orden puede ayudar a identificar patrones de consumo entre los usuarios.

H2. La cantidad comprada y el precio de productos son factores que permite definir perfiles de compradores.

La teoría microeconómica de las demandas Marshallianas se utiliza para entender cómo los consumidores toman decisiones de consumo en función de sus recursos disponibles y sus preferencias. La demanda Marshalliana depende del ingreso del consumidor y de los precios de los bienes disponibles. Dado que el consumidor tiene un ingreso limitado 𝑚 y desea consumir una cantidad 𝑥 de cada bien, enfrenta un problema de asignación de recursos para maximizar su utilidad.

Es crucial estudiar el concepto de elasticidad precio de la demanda, ya que la utilidad del consumidor está estrechamente relacionada con los precios de los bienes. Alfred Marshall, en su libro Principles of Economics (1890), desarrolló este concepto para analizar cómo cambian las decisiones de consumo cuando varía el precio de un bien.

Elasticidad Precio Mayor a 1:

Cuando la elasticidad precio de la demanda es mayor que 1, la cantidad demandada cambia más que proporcionalmente en relación con los cambios en el precio. Por ejemplo, si un aumento del precio del 10% resulta en una disminución de la cantidad demandada del 20%, la elasticidad es mayor a 1. Esto significa que un pequeño cambio en el precio puede provocar un cambio considerable en la cantidad demandada. Los bienes con sustitutos cercanos suelen tener una demanda más elástica. Por ejemplo, si un consumidor considera sustitutos similares como Coca-Cola y jugo de naranja, un aumento en el precio de uno de ellos puede llevar a un cambio rápido hacia el otro.
Elasticidad Precio Menor a 1:

Cuando la elasticidad precio de la demanda es menor que 1, la cantidad demandada cambia menos que proporcionalmente en respuesta a cambios en el precio. Este comportamiento es común en bienes esenciales, como medicamentos, donde la demanda es relativamente inelástica porque el consumidor necesita estos bienes independientemente de las variaciones en el precio.

Elasticidad Precio Igual a 1:

Cuando la elasticidad precio de la demanda es igual a 1, la cantidad demandada cambia exactamente en la misma proporción que el cambio en el precio. En este caso, el cambio en el precio resulta en un cambio proporcional en la cantidad demandada.

Por tanto, comprender cómo cambian las cantidades demandadas para cada producto puede ayudar a segmentar a los consumidores. Los consumidores que compran productos con alta elasticidad precio tienden a responder más significativamente a los cambios de precios. Este análisis puede ser útil para clasificar a los consumidores en grupos basados en su sensibilidad a los cambios de precios.

Fórmula de Elasticidad Precio de la Demanda:
Elasticidad Precio = (Variacion % en la cantidad demandada)/(Variacion % en el precio) = (Δ𝑄/𝑄)/(Δ𝑃/𝑃) 

El objetivo es calcular la elasticidad precio de la demanda para cada producto, lo que puede ayudar a clasificar a los consumidores y realizar una segmentación funcional basada en su sensibilidad al precio. Este análisis permite a las empresas ajustar sus estrategias de precios y marketing para maximizar la efectividad y mejorar la satisfacción del cliente.

H3. Los tipos de productos y las características inherentes a los productos comprados ayudan a explicar patrones de consumo.
H4. El tipo de envío solicitado para la entrega del pedido.
H5. Las promociones o descuentos aplicados en la compra permiten identificar la sensibilidad al precio y la respuesta a estrategias de marketing.
H6. Las categorías de productos más compradas pueden indicar intereses y necesidades predominantes entre diferentes grupos de compradores.
H7. El Raiting de productos permite entender porque los clientes compran determinados productos.
H7. El valor promedio del carrito de compras proporciona insights sobre el poder adquisitivo y las tendencias de gasto de los clientes.

Ligadas a las características del usuario

H8. El método de pago utilizado en la transacción es un factor determinante para analizar tipos de consumidores.
H9. La frecuencia de compras puede revelar la lealtad del cliente y su comportamiento de compra recurrente.
H10. El historial de compras del consumidor
H11. El poder adquisitivo del cliente permite identificar patrones de consumo.
H12. Las características demográficas del comprador, como edad, género y ubicación, permiten segmentar a los clientes en grupos específicos.

Ligadas al contexto

H13. La estacionalidad de las compras proporcionan información sobre preferencias estacionales y ciclos de compra.
H14. Las horas y días de la semana en que se realizan las compras pueden ofrecer información sobre los hábitos y comportamientos de compra.
H15. El clima puede ser un factor determinante por el cual se dan determinadas compras.

# 1.1.3 Limitantes




# Bibliografia 

Alfred Marshall Principles of Economics (1890)

Marshall and Hicks, Understanding the Ordinary and Compensated Demand, K.J. Wainwright March 3, 2013
https://www.sfu.ca/~wainwrig/Econ201/6500/hicks_marshall_explained.pdf