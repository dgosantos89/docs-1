Documentação do Behat
=====================

Esta é uma tradução não oficial feita por `Diego Santos`_, portanto pode estar desatualizada. Sinta-se encorajado para me ajudar a mantê-la atualizada.  

Behat é um framework open source de Behavior Driven Development (BDD - Desenvolvimento Dirigido por Comportamento) para PHP 5.3+.
O que é *Behavior Driven Development*, você pergunta? É uma maneira de desenvolver software
através de uma comunicação constante com as partes interessadas em forma de exemplos;
exemplos de como este programa deve ajudá-los, e você, para alcançar seus objetivos.

Por exemplo, imagine que você está prestes a criar o famoso comando UNIX ``ls``.
Antes de começar, você vai ter uma conversa com seus stakeholders (usuários de UNIX) e eles poderiam dizer que mesmo que eles gostem muito do UNIX, eles precisam de uma maneira de ver todos os arquivos no diretório de trabalho atual. Você então tem um bate-papo vai-e-vem com eles sobre como eles vêem esta característica trabalhando e que você venha com o seu primeiro cenário (um nome alternativo, por exemplo, na metodologia BDD):

.. code-block:: gherkin

    # language: pt
    Funcionalidade: Comando de listagem
      A fim de alterar a estrutura da pasta em que estou atualmente
      Como um usuário de UNIX
      Eu preciso ser capaz de ver os arquivos e pastas disponíveis atualmente lá

      Cenário: Listando dois arquivos em um diretório
        Dado que estou em um diretório "teste"
        E tenho um arquivo chamado "foo"
        E tenho um arquivo chamado "bar"
        Quando executar o "ls"
        Então eu devo ter:
          """
          bar
          foo
          """


Se você é um stakeholder, esta é a sua prova de que os desenvolvedores entenderam exatamente como você quer que esse
recurso funcione. Se você é um desenvolvedor, esta é a sua prova de que o stakeholder espera que você implemente este
recurso exatamente da maneira que você está planejando implementá-lo.

Então, como um desenvolvedor seu trabalho estará terminado tão logo você faça o comando ``ls`` e faça o comportamento descrito no cenário "Comando de listagem".

Você provavelmente já ouviu sobre a prática moderna de desenvolvimento chamada TDD, onde você escreve testes para o seu
código antes, não depois, do código. Bem, BDD é parecido, exceto pelo fato de que você não precisa começar com um teste - seus *cenários* são seus testes. Isto é exatamente o que o Behat faz! Como você vai ver, Behat é fácil de aprender, rápido de usar e vai trazer a diversão de volta para os seus testes.

.. nota::

    Behat foi fortemente inspirado no projeto em Ruby `Cucumber`. Desde v3.0,
    Behat é considerada uma implementação oficial de Cucumber em PHP e é parte
    da grande família de ferramentas de BDD.

Intro Rápida
------------

Para começar a ser um *Behat'er* em 30 minutos, basta apenas mergulhar no guia de início rápido e desfrutar!

.. toctree::
    :maxdepth: 1

    quick_intro_pt1

Guias
-----

Aprenda Behat com os seguintes guias:

.. toctree::
    :maxdepth: 1

    guides/1.gherkin
    guides/2.definitions
    guides/3.hooks
    guides/4.contexts
    guides/5.suites
    guides/6.profiles
    guides/7.run

Cookbook
--------

Aprenda soluções específicas para necessidades específicas:

.. toctree::
    :maxdepth: 1

    cookbooks/1.symfony2_integration
    cookbooks/context_communication

Mais sobre BDD
--------------

Quando estiver com o Behat instalado e funcionando, você pode aprender mais sobre o BDD através dos seguintes links (em inglês). Embora ambos os tutoriais sejão específicos do Cucumber, Behat compartilha muito com Cucumber e as filosofias são as mesmas.

* `Dan North's "What's in a Story?" <http://dannorth.net/whats-in-a-story/>`_
* `Cucumber's "Backgrounder" <https://github.com/cucumber/cucumber/wiki/Cucumber-Backgrounder>`_

.. _`Cucumber`: http://cukes.info/
.. _Diego Santos: http://dgosantos89.github.io/
