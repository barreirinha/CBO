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
- 225 - PROFISSIONAIS DA MEDICINA

Retirando os ultimo dígito novamente, chegamos ao Nível 2 (Sub-grupo principal):
- 22 - PROFISSIONAIS DAS CIÊNCIAS BIOLÓGICAS, DA SAÚDE E AFINS

Por fim... Nível 1 (Grande Grupo)
- 2 - PROFISSIONAIS DAS CIÊNCIAS E DAS ARTES

Outro Exemplo, com um de advogado de Direito administrativo:

* __Nível 1 - Grande Grupo__:
  * _Código 2_ - PROFISSIONAIS DAS CIÊNCIAS E DAS ARTES
  
* __Nível 2 - Sub-Grupo Principal__:
  * _Código 24_ - PROFISSIONAIS DAS CIÊNCIAS JURÍDICAS
  
* __Nível 3 - Sub-Grupo__:
  * _Código 241_ - ADVOGADOS, PROCURADORES, TABELIÃES E AFINS
  
* __Nível 4 - Família__:
  * _Código 2410_ - Advogados
  
* __Nível 5 - Ocupação__:
  * _Código 241020_ - Advogado (direito público)
  
* __Nível 6 - Sinônimo__:
  * _Código 241020_ - Advogado (direito administrativo)

### Arquivos

* Tabelas Individuais:
  * sql/nivel1_grandes_grupos.sql
  * sql/nivel2_sub_grupo_principal.sql
  * sql/nivel3_sub_grupo.sql
  * sql/nivel4_familia.sql
  * sql/nivel5_ocupacao.sql
  * sql/nivel6_sinonimos.sql

* Banco completo (As tabalas acima em um arquivo SQL único)
	 * sql/cbo.sql
  
* Tabela que uso em minha aplicações, um compilado de todas as informações acima em uma tabela única.
	 * sql/profissoes.sql

Os arquivos da pasta txt são um tipo de csv, têm uma barra vertical (|) como separador, no formato:
- codigo|descricao
