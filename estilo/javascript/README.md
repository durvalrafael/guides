# JavaScript
> guia anti-espaguete

## Sumário
- [Formatação](#formata%C3%A7%C3%A3o)
- [Nomenclatura](#nomenclatura)
- [Manipulação do DOM](#manipula%C3%A7%C3%A3o-do-dom)
- [Referências](#refer%C3%AAncias)

[[⬅︎ Voltar para Estilo]](https://github.com/mktvirtual/guides/tree/master/estilo)


## Formatação

- Use ponto-e-vírgula.
    ```javascript
    // bad
    var me = $(this)
    test()

    // good
    var me = $(this);
    test();
    ```

- Use aspas simples.
    ```javascript
    // bad
    var string = "<p class='foo'>Lorem Ipsum</p>";
    var noteClick = me.attr("data-note");

    // good
    var string = '<p class="foo">Lorem Ipsum</p>';
    var noteClick = me.attr('data-note');
    ```

- Use `{}` em todos os blocos.
    ```javascript
    // bad
    if (condition) statement;
    else if (condition) statement;
    else statement;

    // good
    if (condition) {
        statement
    } else if (condition) {
        statement
    } else {
        statement
    }
    ```

- Use `/* comentários */`.
    - Inclua uma descrição, especifique tipos e valores para todos os parâmetros e retornos de funções e métodos.
    ```javascript
    /**
     * make() returns a new element
     * based on the passed in tag name
     *
     * @param <String> tag
     * @return <Element> element
     */
    function make(tag) {

        // stuff...

        return element;
    }
    ```

- Use `// comentários`.
    - Explique o que está acontecendo no seu código.
    ```javascript
    // good
    function getType() {
        console.log('fetching type...');

        // set the default type to 'no type'
        var type = this._type || 'no type';

        return type;
    }
    ```

- Não utilize vírgulas na frente da linha.
    ```javascript
    // bad
    var hero = {
          firstName: 'Bob'
        , lastName: 'Parr'
        , heroName: 'Mr. Incredible'
        , superPower: 'strength'
    };

    // good
    var hero = {
        firstName: 'Bob',
        lastName: 'Parr',
        heroName: 'Mr. Incredible',
        superPower: 'strength'
    };
    ```

- Prefixe objetos jQuery com `$`.
    ```javascript
    // bad
    var sidebar = $('.sidebar');

    // good
    var $sidebar = $('.sidebar');
    ```

- Use variáveis em `lowerCamelCase`
    ```javascript
    // bad
    var main_title, maintitle;

    // good
    var mainTitle;
    ```

- Use `{` na mesma linha da sentença.
    ```javascript
    // bad
    // the function returns undefined and not an object with a name property
    function func()
    {
        return
        {
            name: "Batman"
        };
    }
    // => undefined

    // good
    function func() {
        return {
            name: "Batman"
        };
    }
    // => { name: "Batman" }
    ```

[[⬆︎ Topo]](#sum%C3%A1rio)

## Nomenclatura

- Use `camelCase` para variáveis normais.
    ```javascript
    // bad
    var table_prefix = 'table-';
    var tableprefix = 'table-';
    var TablePrefix = 'table-';

    // good
    var tablePrefix = 'table-';
    ```

- Use `PascalCase` para "classes".
    ```javascript
    // bad
    var app = { /* ... */ };

    // good
    var App = { /* ... */ };
    ```

- Use `UPPER_CASE` para constantes.
    ```javascript
    // bad
    var maxWidth = 300;

    // good
    var MAX_WIDTH = 300;
    ```

[[⬆︎ Topo]](#sum%C3%A1rio)

## Manipulação do DOM

- Use o prefixo `js-` nas classes de elementos selecionados pelo JavaScript. [(?)](https://github.com/csswizardry/CSS-Guidelines#js-hooks)
    ```javascript
    // bad
    var $button = $('.button');

    // good
    var $button = $('.js-button');
    ```

[[⬆︎ Topo]](#sum%C3%A1rio)

## Referências

- [Coding Style por @LFeh](https://github.com/LFeh/coding-style#js)
    - Grande parte dos exemplos daqui vieram deste ótimo guia por [@LFeh](https://github.com/LFeh).

[[⬆︎ Topo]](#sum%C3%A1rio)
