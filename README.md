# cbo
CBO - Classificação Brasileira de Ocupações

Esta é a versão do ano de 2020 da CBO - CBO - Classificação Brasileira de Ocupações, até agora (agosto de 2020) é a mais atual que exite. O Fato de a VERSÃO ser 2002 não significa que de lá para cá nada foi alterado, algumas ocupações foram inclídas. Apenas o FORMATO de classificar permanece o mesmo.

## Site Oficial da CBO
- http://www.mtecbo.gov.br/ 

## Como funciona
A CBO segue algumas classificações, cada uma com seu código. 

- Nível 1 (1 dígito) - Grande Grupo
- Nível 2 (2 dígitos) - Sub-Grupo Principal
- Nível 3 (3 dígitos) - Sub-Grupo
- Nível 4 (4 dígitos) - Família
- Nível 5 (6 dígitos) - Ocupação
- Nível 6 (6 dígitos) - Sinônimos

### Exemplo:

No arquivo de Nível 6 (Sinônimos) achamos a seguinte ocupação: 
- 225103 - Médico de doenças infecciosas e parasitárias

Porém, esse registro é apenas um Sinônimo, um apelido para alguma ocupação contida no arquivo de Nivel 5 (Ocupação). Se procurarmos nele com o mesmo código acharemos:
- 225103 - Médico infectologista

Retirando os ultimos 2 dígitos do código, chegamos ao Nível 4 (Família):
- 2251 - Médicos clínicos

Retirando os ultimo dígito do código acima, chegamos ao Nível 3 (Sub-grupo):
- 2251 - PROFISSIONAIS DA MEDICINA

Retirando os ultimo dígito novamente, chegamos ao Nível 2 (Sub-grupo principal):
- 22 - PROFISSIONAIS DAS CIÊNCIAS BIOLÓGICAS, DA SAÚDE E AFINS

Por fim... Nível 1 (Grande Grupo)
- 2 - PROFISSIONAIS DAS CIÊNCIAS E DAS ARTES

### Formato

Os arquivos txt estã com uma barra vertical (|) como separador, no formato:
- codigo|descricao

### Como eu uso

Nas aplicações que fiz, juntei os dados do Nível 5 e 6, criando uma única tabela.
