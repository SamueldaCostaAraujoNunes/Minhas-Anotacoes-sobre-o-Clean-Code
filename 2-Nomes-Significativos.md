# Nomes Significativos

## Use Nomes que Revelem seu Propósito

1. O nome de uma variável, função ou classe deve responder a todas as grandes questões. Ele deve lhe dizer porque existe, o que faz e como é usado.

2. O nome de uma entidade deve ser claro e especifico, evitando redundâncias e más interpretações

Exemplo:

```
t = 12
```
Sem um contexto, a variável acima traz pouca informação do seu conteúdo e para que ele será usado.

```
response_time_in_seconds = 12
```
Nesta declaração de variável, tem informações mais completas sobre o seu significado. Sabemos, que ela será usada para determinar o tempo de resposta para algo, e que sua unidade de medida está em segundos. 

Tente descrever para si, qual o real significado daquela entidade. Crie um nome simples e direto que resuma bem o que ela representa. E ENTÃO, ESCREVA.

## Evite Informações Erradas

1. Programadores devem evitar passar dicas falsas que confundam o sentido do código.
2. Devemos evitar palavras cujo significados podem se desviar daquele que desejamos.

Cuidado com o uso de abreviaturas. Elas podem confundir você mesmo e os seus leitores. Quando são utilizadas, sem a devida atenção, abrem espaço para diversas interpretações no código. Já que seu significado não fica evidente. Podendo até ser confundido por outras abreviaturas consolidadas no meio da programação.

Exemplo:
```
str_movie = 'Netflix'
```
Imagine que você precisa guardar o nome de uma plataforma de streaming de filmes. E decide abreviar o nome da sua variável para ```str_movie```, usualmente o termo ```str```, está relacionado a Strings. Assim, qualquer programador, com certa experiência, pode facilmente confundir o seu significado. Já que a mesma, apresenta uma duplicidade de sentidos.

Refatorando:
```
stream_platform_movie = 'Netflix'
```
Veja como, o entendimento da variável ficou mais simples, direto e completo. Desta forma, as chances de gerar informações erradas são reduzidas.

Não se refira a um grupo de contas como ```account_list```, a menos que realmente seja uma ```List```, existem palavras que possuem significados muito específicos para programadores. List é um exemplo perfeito. Se o conteúdo da variável não pertencer a classe ```List```, possivelmente confundirá outros! Assim, é preferível usar termos como ```account_group```, ```bunch_of_accounts``` ou simplesmente, ```accounts```.

Evite usar nomes muito semelhantes. Fica difícil notar diferenças entre ```user_keyboard_input_handler``` para ```user_keyboard_input_storage```, o problema se destaca. Quando usamos as ferramentas de auto-complete das IDES, que nos sugestionam sentenças para se utilizar. Assim, termos muito similares, tornam-se facilmente confundíveis. Já que é intuitivo crer que a opção retornada como sugestão é realmente a esperada.

Outro caso, em que a confusão é clara, é o uso da letra 'i' minúscula ou da vogal 'o' maiúscula. Eles se parecem muito com o 1 e o 0, respectivamente.

Observe a semelhança:
```
O == 0 and i == 1
```
Um problema deste pode ser evitado facilmente resolvido, definindo nomes significativos para as variáveis.