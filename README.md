# Template de aplicação das práticas de clean code

## Orientações de desenvolvimento

- Código deve ter testes;
- O código deve ser encontrado no local onde deveria estar;
- Mais tarde é igual a nunca;
- O código deve conter apenas o necessário;
- Código curto é melhor;
- Evitar duplicações;
- Deixar o código melhor do que foi encontrado (regra dos escoteiros);
- Linhas seguinte de **if**, **else** e **while** devem ter uma linha apenas;
- Evitar comentários desnecessários;
- Arquivos pequenos são melhores de entender; 
- Uma linha deve ter no máximo 120 caracteres;
- Colocar espaços entre o operador de atribuição **=**;
- Evitar chamadas em cadeia, **x.getB().getA()...**
- Evitar passar null como argumento.

## Nomenclaturas

- Nomes tem que revelar o propósito;
- Nomes devem ser pronunciáveis;
- Nomes devem ser fáceis para buscar;
- **NÃO** utilizar nomes codificados;
- **NÃO** utilizar nomes com uma letra;
- Métodos/Funções devem ter verbos ou verboSubstantivo como nome exemplo: **postPagamento**
- Métodos de acesso, alteração e verificação devem ter prefixo **get**, **set** e **is**;
- Ser consistente na escolha de prefixos, exemplo: addName (para funções que adicionam um elemento a uma lista, caso uma função tenha um objetivo diferente o predicado deve ser outro se for utilizar);
- Buscar usar nomes curtos, mas que sejam descritivos;

## Variáveis

- [ ] O nome responde às perguntas de pôr que existe, o que faz e como se utiliza?

- [ ] Variáveis são declaradas próximas de sua utilização?

## Funções

- [ ] O nome responde às perguntas de pôr que existe, o que faz e como se utiliza?

- [ ] A função é curta? É possível encurtar mais? É possível reduzir para 2 a 4 linhas?

- [ ] **if**, **else** ou **while** possuem uma linha em seu escopo?

```javascript
// examplo if/else
if(isValid()){
    doThis()
}else{
    doThat()
}
// examplo while
while(a>1){
    doSomething(a)
}
```

- [ ] O nível de indentação é de no máximo 1 ou 2?

- [ ] A função está fazendo apenas uma coisa? Ela não pode alterar o estado de um objeto e retornar um dado do objeto.

- [ ] A função passa mais de 3 argumentos? Ideal é zero, caso for maior que 3 melhor criar um objeto ou analizar a necessidade de aplicação de uma classe.

- [ ] A função não recebe booleano como argumento? Remover caso contrário.

- [ ] Uma função que chama outra função, a última está perto de sua chamada caso esteja no mesmo arquivo?

- [ ] O parenteses da função está grudado ao nome?

- [ ] Os argumentos da função possuem um espaço após a virgula?

## Classes

- [ ] O nome responde às perguntas de pôr que existe, o que faz e como se utiliza?

- [ ] O nome é um substantivo ou frase nominal?

- [ ] As variáveis de instância estão declaradas no topo?

- [ ] As variáveis/funções estão em ordem?
    1. public static constants;
    2. private static variables;
    3. private instance variables;
    4. public functions.

- [ ] A classe possui apenas uma responsábilidade?

- [ ] é possível descrever a classe em 25 palavras sem usar **if/se**, **and/e**, **or/ou** ou **but/mas**?

## Objeto

- [ ] O nome responde às perguntas de pôr que existe, o que faz e como se utiliza?

- [ ] O nome é um substantivo ou frase nominal?

## Exceções

- [ ] O bloco de try{} catch{} está em uma função isolada onde o corpo do try e do catch são funções que tratam as devidas partes?
```javascript
// exemplo
try{
    doSomething()
}catch(e){
    handleException(e)
}
```

- [ ] A excessão gerada provê contexto necessário para determinar onde foi gerado o erro?

- [ ] Alguma função retorna null? Altere para gerar um erro.

## Comentários

- Manter comentários apenas se for do tipo:
    - [ ] comentário de razão legal;
    - [ ] comentário informativo (nesse caso buscar solucionar pelo nome da função/variável);
    - [ ] comentário que informa sobre uma decisão tomada;
    - [ ] comentário de clarificação (nesse caso buscar solucionar pelo nome da função/variável);
    - [ ] comentários sobre consequências;
    - [ ] comentário de TODOS.

## Testes

- [ ] Padrão BUILD-OPERATE-CHECK separa os testes em três partes:
    1. constroi os dados do teste;
    2. opera sobre os dados;
    3. valida se os resultados das operações geraram os dados esperados.
- [ ] Cada teste está separado em um expect?
- [ ] Given-When-Then?
- [ ] Regra F.I.R.T.S.:
    1. teste deve ser rápido (Fast);
    2. teste deve ser independente dos outros (Independent);
    3. teste deve ser possível de ser repetido em qualquer ambiente (Repeatable);
    4. teste deve ser escrito antes do código de produção (Timely);
    5. teste deve passar ou falhar (Self-Validating)
