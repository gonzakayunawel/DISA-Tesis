# Logística urbana asimétrica chilena bajo shocks externos
Gonzalo Cayunao Erices
abril 2026

# El problema

El mercado logístico chileno de e-commerce presenta una asimetría
estructural particularmente marcada: un puñado de operadores integrados
(Blue Express, Chilexpress, Starken, Correos Chile) concentra la mayor
parte del volumen consolidado, mientras un tejido atomizado de
operadores de última milla MiPyME absorbe la entrega final bajo
condiciones contractuales heredadas del nivel superior. Esta estructura
no es solo descriptiva: condiciona cuantitativamente cómo el sistema
responde a shocks exógenos —variaciones del precio del diésel, tipo de
cambio, regulaciones de bajas emisiones, normativa laboral de
repartidores— de formas que los modelos clásicos de optimización de
cadena de suministro no capturan.

La pregunta de investigación es directa: ***¿cómo se transmiten los
shocks regulatorios y de precios desde el nivel oligopólico hacia el
last-mile, y qué implicancias tiene esa transmisión para el diseño de
política pública en logística urbana?*** Responderla cuantitativamente
requiere un modelo donde el entorno enfrentado por los operadores
pequeños (tarifas de subcontratación, cobertura geográfica disponible)
no sea un dato exógeno, sino una variable endógena que reacciona a las
decisiones estratégicas del nivel superior y a los shocks externos.

# Gap en la literatura

Los modelos clásicos de Vehicle Routing Problem (VRP) e Inventory
Routing Problem (IRP) optimizan la respuesta de un agente —o de un
decisor centralizado— frente a un entorno dado. Esa formulación es
poderosa pero asume implícitamente simetría de poder y exogeneidad del
entorno tarifario, dos supuestos que no se sostienen en el caso chileno.

Una auditoría bibliométrica preliminar en Scopus (PRISMA, en curso)
sugiere un gap específico: la intersección entre **(i) modelamiento del
comportamiento estratégico del oligopolio logístico**, **(ii)
interacción de campo medio entre operadores de última milla
atomizados**, y **(iii) evaluación contrafactual de escenarios de
política pública en tiempo razonable**, aplicada al contexto de mercados
logísticos asimétricos en economías emergentes, no ha sido cubierta de
manera sistemática. Es justamente en esa intersección donde la presente
propuesta busca posicionarse.

# Propuesta metodológica

Se propone modelar el sistema como una estructura jerárquica de tres
niveles, con shocks exógenos entrando paramétricamente en cada nivel:

- **Nivel oligopólico:** juego dinámico estocástico sobre tarifas
  zonales, capacidad de red y compromiso de niveles de servicio, con dos
  regímenes de equilibrio (colusión tácita / Nash competitivo) cuya
  transición depende de los shocks exógenos. Forma reducida defendible
  en la tradición de Porter (1983) y Ellison (1994).
- **Acoplamiento Stackelberg:** los operadores principales actúan como
  líderes anticipando la respuesta agregada del continuo de last-milers,
  en la tradición de equilibrios Stackelberg-Nash-Cournot estocásticos
  (De Wolf y Smeers 1997).
- **Nivel atomizado:** los last-milers MiPyMEs resuelven un problema de
  control óptimo de ruteo y aceptación de pedidos en interacción de
  campo medio, donde la distribución $m(x,t)$ representa la densidad
  espacial de capacidad de delivery.

Formalmente, los tres niveles se acoplan en el siguiente sistema
(presentado en forma compacta a modo de mapa, no de compromiso técnico
definitivo):

La aproximación numérica del sistema acoplado está prevista vía técnicas
de scientific machine learning como los operadores neuronales informados
por física o PINO (Karniadakis et al. 2021), las cuales permiten evaluar
familias paramétricas de soluciones —es decir, escenarios
contrafactuales de política— en tiempos compatibles con su uso por
tomadores de decisión. Esa pieza computacional puede explorarse en
colaboración con el claustro DISA en la línea de Sistemas de Información
e Inteligencia de los Datos.

# Predicciones empíricas falsables

El framework genera tres predicciones falsables con datos chilenos
potencialmente disponibles:

- **Asimetría tarifaria tipo “rockets and feathers”** frente a shocks
  del precio del diésel: ajuste rápido al alza, lento a la baja,
  condicional al régimen estimado.
- **Probabilidad de régimen colusivo creciente** en la volatilidad
  cambiaria y decreciente en la intensidad regulatoria observable
  (proxies vía DT, SERNAC, normativa de bajas emisiones).
- **Zonas de cobertura sub-atendidas predecibles** por el equilibrio de
  campo medio, incluso en presencia de demanda económicamente viable
  —fenómeno consistente con observaciones cualitativas de exclusión
  logística en comunas periféricas.

# Relación de la propuesta de investigación con el CTL / CATLEC

El centro CATLEC explicita como una de sus líneas de investigación su
orientación a la Competitividad Logística Nacional (CATLEC 2026) con
foco en políticas públicas basadas en evidencia. Esta propuesta calza
con esa agenda en tres dimensiones concretas: (i) el objeto de estudio
es directamente el sistema logístico urbano chileno y su respuesta a
regulación; (ii) el output principal es una herramienta de simulación de
escenarios contrafactuales utilizable por reguladores —no solo un modelo
teórico—; (iii) las predicciones falsables permiten contrastar
empíricamente hipótesis sobre comportamiento de mercado que hoy se
discuten cualitativamente.

El doctorando aporta capacidades específicas en aceleración GPU
(PyTorch/CUDA), modelamiento matemático y metaheurísticas híbridas (tema
de su tesis de magíster), que complementan la experticia aplicada del
CTL en *operations research* logístico.

# Síntesis Final

La propuesta estudia cómo los shocks regulatorios y de precios se
transmiten a través de un mercado logístico estructuralmente asimétrico:
un oligopolio de operadores integrados en la cúspide y un tejido
atomizado de MiPyMEs de última milla en la base. El aporte central no es
solo descriptivo sino cuantitativo: modelar ese sistema jerárquico
—juego dinámico estocástico en el nivel oligopólico, acoplamiento
Stackelberg, interacción de campo medio en el nivel atomizado— de modo
que las condiciones enfrentadas por los operadores pequeños emerjan como
variable endógena y no como dato exógeno.

El resultado esperado no es únicamente un artículo académico, sino una
herramienta de simulación de escenarios contrafactuales calibrada con
datos chilenos, utilizable por reguladores para anticipar efectos
distributivos de política pública logística antes de implementarla.

# Referencias

<div id="refs" class="references csl-bib-body hanging-indent">

<div id="ref-CATLEC2026" class="csl-entry">

CATLEC. 2026. «CATLEC: Línea 1 - Competividad logística nacional». En
*Centro Avanzado de Transporte, Logística y Competitividad Económica*.
Https://catlec.cl/linea-1/.

</div>

<div id="ref-dewolfStochasticVersionStackelbergNashCournot1997"
class="csl-entry">

De Wolf, Daniel, y Yves Smeers. 1997. «A Stochastic Version of a
Stackelberg-Nash-Cournot Equilibrium Model». *Management Science* 43
(2): 190-97. <https://www.jstor.org/stable/2661683>.

</div>

<div id="ref-ellisonTheoriesCartelStability1994" class="csl-entry">

Ellison, Glenn. 1994. «Theories of Cartel Stability and the Joint
Executive Committee». *The RAND Journal of Economics* 25 (1): 37-57.
<https://doi.org/10.2307/2555852>.

</div>

<div id="ref-karniadakisPhysicsinformedMachineLearning2021"
class="csl-entry">

Karniadakis, George Em, Ioannis G. Kevrekidis, Lu Lu, Paris Perdikaris,
Sifan Wang, y Liu Yang. 2021. «Physics-Informed Machine Learning».
*Nature Reviews Physics* 3 (6): 422-40.
<https://doi.org/10.1038/s42254-021-00314-5>.

</div>

<div id="ref-porterStudyCartelStability1983" class="csl-entry">

Porter, Robert H. 1983. «A Study of Cartel Stability: The Joint
Executive Committee, 1880-1886». *The Bell Journal of Economics* 14 (2):
301-14. <https://doi.org/10.2307/3003634>.

</div>

</div>
