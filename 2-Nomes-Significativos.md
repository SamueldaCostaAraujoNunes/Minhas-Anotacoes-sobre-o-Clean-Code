# Nomes Significativos

## 📛 Use Nomes que Revelem seu Propósito

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

## ℹ❌ Evite Informações Erradas

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

## ⁉ Faça Distinções Significativas

1. Os programadores criam problemas para si próprios quando criam um código voltado unicamente para o interpretador/compilador.
2. Se os nomes precisam ser diferentes então também devem ter significados distintos.

Exemplo:
```
def crypt(text1, text2):
    text3 = ''
    for text4 in text1:
        text5 = text2[text4]
        text3 += text5
    return text3
```

Observe o exemplo acima. Sua sintaxe está correta, e funcionaria perfeitamente bem pelo interpretador. Mas, sua leitura é cansativa e confusa. Os nomes das variáveis, são muito similares e dificulta a interpretação do código.

Refatorando:
```
def crypt(message: str, key: dict) -> str:
    encrypted_message = ''
    for letter in message:
        new_letter = key[letter]
        encrypted_message += new_letter
    return encrypted_message
```

Agora, com o código refatorado. Observe como a sua leitura fica mais simples e mais explicita. As variáveis declaradas com um nome mais representativo, mudam completamente a velocidade de compreensão do que é, e como opera aquela função.

O uso arbitrário e indiscriminado de prefixos e sufixos nos nomes de variáveis, é uma péssima pratica. Como exemplo, temos os prefixos ```m_``` e ```n_```, que são formas de representar variáveis de membro e uma nova instância de uma variável já conhecida, respectivamente. Então, o uso de ```n_name```, para declarar uma variável qualquer, apenas para "enganar" o interpretado. Pode acabar atrapalhando você ou outro programador, futuramente.(O prefixo ```m_```, foi utilizado como exemplo, mas seu uso é desaconselhado hoje em dia)

## 🗣📛 Use Nomes Pronunciáveis

1. Crie nome de variáveis prenunciáveis.
2. Evite siglas/acrónimos, sempre que possível seja claro e objetivo.
3. Os nomes devem ser auto explicativos.

Exemplo:
```
genymdhms = Date()
```
Esta variável é utilizada para gerar um objeto, contendo o Ano, Mes, dia, hora, minuto e segundo. Imagine a complicação para incluir o nome desta variável em um dialogo.

Refatorando:
```
generation_timestamp = Date()
```
Desta forma, fica muito mais legível, fácil de ler e discutir sobre o dito código.

## 🔍📛 Use Nomes Passíveis de Busca

1. A especificidade do nome da variável, garante que ela será mais fácil de achar, usando as ferramentas de busca da IDE que você utiliza.

2. Nomes de variável que contem apenas uma letra ou números, possuem um problema particular por não ser fácil de localizá-los ao longo de um texto.

3. O tamanho de um nome deve ser proporcional ao tamanho de um escopo.

Se uma variável ou constante pode ser vista ou usda em vários lugares dentro do código, é imperativo atribuí-la um nome fácil para busca.

Exemplo:
```
for j in range(34):
    s += (t[j]*4)/5 
```

Refatorando:
```
real_days_per_ideal_day = 4
WORK_DAYS_PER_WEEK = 5
sum = 0

for j in range(NUMBER_OF_TASK):
    real_task_days = task_estimate[j] * real_days_per_ideal_day
    real_task_weeks = (real_days / WORK_DAYS_PER_WEEK)
    sum += real_task_weeks
```
Observe que foram usados nomes menos usuais e mais completos, assim se torna muito mais fácil encontrar uma variável dentro de um código. A exemplo, temos a constante ```WORK_DAYS_PER_WEEK```, que é tornou-se facilmente encontrada.

## 🗺 🧠 Evite o Mapeamento Mental

1. Os leitores não devem ter de traduzir mentalmente os nomes que vocês escolheu por outros que eles conheçam.

2. Não é porque você lembra o significado da variável ```abc``` agora, que você vai lembrar daqui uma semana. Ou pior, o leitor não tem nem como saber qual o significado, se ele está guardado apenas na sua cabeça.

3. Clareza é fundamental. Não se esqueça que além de um programador, você é um autor.

## 😀 Nome de Classes

Primordialmente, as classes são moldes para objetos. Representam um agente, algo tátil. Algo como características, com ações. Logo, é esperado que o nome desta Classe seja um Substantivo. Algo direto, que defina o que realmente é um objeto desta Classe.

```
class Client:
...
class Box:
...
class Window:
```

## 🚶‍♀️ Nome de Métodos~

1. Os métodos, são funções que determinam ações de um objeto. Logo, é esperado que a declaração destes métodos forem representados por Verbos.

2. O padrão CRUD, é um conceito utilizado na programação em qualquer linguagem. Em Java, são usados os prefixos ```set```, ```get```,  ```is```, nos métodos de acesso aos atributos. Em Python, uma das soluções adotadas, é o uso das ```propetys```, que não necessitam de prefixos nas declarações de métodos.
```
left_over = account.generate_extract()
...
status = lamp.is_on()
```
