# Relatório da Regressão Linear para Calibração do Sensor de Chuva

Coeficientes do Modelo:

air_humidity_100: -104.916950

air_temperature_100: 446.765321

atm_pressure_main: 84.513110

num_of_resets: 6741.205201

piezo_temperature: -448.679757

chuva: -221.146543

Intercepto: -756727.1338104222

Mean Absolute Error (Erro Absoluto Médio): 8572.756622671082

Análise dos Coeficientes:

air_humidity_100: Um aumento de 1 unidade na umidade relativa do ar externo (air_humidity_100) está associado a uma diminuição de aproximadamente 104.92 unidades nas medições do sensor de chuva (piezo_charge).

air_temperature_100: Um aumento de 1 grau Celsius na temperatura do ar externo (air_temperature_100) está associado a um aumento de aproximadamente 446.77 unidades nas medições do sensor de chuva.

atm_pressure_main: Um aumento de 1 unidade na pressão atmosférica (atm_pressure_main) está associado a um aumento de cerca de 84.51 unidades nas medições do sensor de chuva.

num_of_resets: Cada reset realizado na placa do sensor (num_of_resets) está associado a um aumento significativo de aproximadamente 6741.21 unidades nas medições do sensor de chuva. Isso indica que os resets têm um forte impacto nas medições do sensor.

piezo_temperature: Um aumento de 1 grau Celsius na temperatura da placa do sensor (piezo_temperature) está associado a uma diminuição de aproximadamente 448.68 unidades nas medições do sensor de chuva.

chuva: A variável "chuva" representa as medições reais de chuva a partir da estação meteorológica próxima. Surpreendentemente, ela tem um coeficiente negativo de -221.15. Isso indica que, quando há um aumento na quantidade de chuva real medida, as medições do sensor de chuva (piezo_charge) tendem a diminuir.

Interpretando o Resultado:

O intercepto (-756727.13) representa o valor esperado das medições do sensor de chuva (piezo_charge) quando todas as outras variáveis independentes são iguais a zero.

O modelo de regressão linear ajustado indica que, em geral, as variáveis atmosféricas como a umidade relativa do ar (air_humidity_100), temperatura do ar (air_temperature_100) e pressão atmosférica (atm_pressure_main) têm um impacto positivo nas medições do sensor de chuva. Isso significa que um aumento nessas variáveis geralmente leva a um aumento nas medições do sensor.

Além disso, o número de resets da placa do sensor (num_of_resets) tem um impacto positivo significativo nas medições do sensor. 

Cada reset causa um aumento considerável nas medições.

Surpreendentemente, a temperatura da placa do sensor (piezo_temperature) tem um impacto negativo nas medições do sensor de chuva. 

Isso sugere que, à medida que a temperatura da placa aumenta, as medições do sensor diminuem.

A variável "chuva", que representa as medições reais de chuva obtidas da estação meteorológica próxima, também tem um impacto negativo nas medições do sensor de chuva. Isso pode indicar que o sensor de chuva baseado em impactos mecânicos pode ter alguma sensibilidade a mudanças na quantidade real de chuva medida.

Avaliação do Modelo:

O Mean Absolute Error (Erro Absoluto Médio) do modelo é de aproximadamente 8572.76 unidades. Essa métrica mede a diferença média absoluta entre as previsões do modelo e os valores reais de chuva. Quanto menor o valor do MAE, melhor é o desempenho do modelo em fazer previsões precisas.
