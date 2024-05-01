# Azure Cognitive Search

O Azure Cognitive Search (agora conhecido também como Azure AI Search) é um serviço da Microsoft Azure que permite a recuperação segura de informações em grande escala sobre o conteúdo de propriedade do usuário em aplicativos de pesquisa de IA. Ele é projetado para facilitar a criação de experiências de pesquisa avançadas e aplicativos de IA generativa que combinam grandes modelos de linguagem com dados corporativos.

## Instruções📕

### Crie um recurso no Portal Azure

1 - Acesse o [Portal Azure](https://portal.azure.com/).

2 - Faça login com sua conta Azure/Microsoft.

3 - Procure a opção "Criar um Recurso" e pesquise "Azure Ai Search".

4 - Selecione a opção e crie
<details>
<summary>Imagem</summary>

![alt text](assets/image.png)
</details>ㅤ

5 - Preencha os campos

É aconselhado configurar da seguinte maneira (selecione básico no tipo de preço):
<details>
<summary>Imagem</summary>

![alt text](assets/image-1.png)
</details>ㅤ

6 - Depois clique em  Revisar + Criar, confira as informações e crie. Espere finalizar a implantação, assim que concluída vamos para o próximo passo.

7 - Procure a opção "Criar um Recurso" e selecione "AI + Machine Learning"

8 - Selecione a opção Serviços Cognitivos e criar

<details>
<summary>Imagem</summary>

![alt text](assets/image-2.png)
</details>ㅤ

9 - Preencha os campos e depois clique em Examinar + Criar, confira as informações e crie.

10 - Procure a opção "Criar um Recurso", selecione "Armazenamento" e procure "Storage Account".

<details>
<summary>Imagem</summary>

![alt text](assets/image-3.png)
</details>ㅤ

11 - É indicado configurar da seguinte maneira (o nome é da sua escolha):

<details>
<summary>Imagem</summary>

![alt text](assets/image-4.png)

</details>ㅤ

12 - Preencha os campos e depois clique em Examinar + Criar, confira as informações e crie.

13 - Após criado selecione "Ir para o Recurso".
<details>
<summary>Imagem</summary>

![alt text](assets/image-5.png)

</details>ㅤ

14 - Habilite a seguinte opção assim que chegar a página do recurso:
<details>
<summary>Imagem</summary>

![alt text](assets/image-6.png)

</details>ㅤ

Em seguida salve.

<details>
<summary>Imagem</summary>

![alt text](assets/image-8.png)

</details>ㅤ

15 - Assim que terminar de criar, clique no container criado e faça o upload de arquivos, no caso desse tutorial irei fazer o upload de reviews fakes, [baixe aqui](https://aka.ms/mslearn-coffee-reviews).

<details>
<summary>Imagem</summary>

![alt text](assets/image-7.png)

</details>ㅤ

16 - Agora voltaremos ao Azure Ai Search (Pesquisa de IA do Azure), e iremos selecionar importar dados.

<details>
<summary>Imagens</summary>

![alt text](assets/image-9.png)

Configure da seguinte maneira:
![alt text](assets/image-10.png)

Confirme e vá para a próxima etapa, em seguida configure como no vídeo:

<video controls src="video1.mp4" title="Title"></video>

Faça como na imagem abaixo:

![alt text](assets/image-11.png)

Prossiga e selecione como na image:
![alt text](assets/image-12.png)

Continue para a próxima etapa, faça como na imagem abaixo e envie:

![alt text](assets/image-13.png)


</details>ㅤ

17 - Retorne à página de recursos da Pesquisa de IA do Azure. No painel esquerdo, em Gerenciamento de Pesquisa, selecione Indexadores. Selecione o indexador recém-criado. 

![alt text](assets/image-14.png)

18 - Você pode também fazer uma consulta no índice, use o gerenciador de pesquisa para fazer uma consulta.

<details>
<summary>Imagens</summary>

![alt text](assets/image-15.png)

A consulta de pesquisa retorna todos os documentos no índice de pesquisa, incluindo uma contagem de todos os documentos no campo @odata.count. O índice de pesquisa deve retornar um documento JSON contendo os resultados da pesquisa

A consulta pesquisa todos os documentos no índice e filtra por revisões com um local de Chicago. Você deve ver no campo. 3 @odata.count

![alt text](assets/image-16.png)

Filtrando agora por localização:

![alt text](assets/image-17.png)

Filtrando por sentimento:

![alt text](assets/image-18.png)

</details>ㅤ

19 - Também é possível Revisar o repositório de conhecimento

Vamos ver o poder do armazenamento de conhecimento em ação. Ao executar o assistente Importar dados, você também criou um repositório de conhecimento. Dentro da loja de conhecimento, você encontrará os dados enriquecidos extraídos pelas habilidades de IA persistem na forma de projeções e tabelas

20 - Volte ao seu recurso de Armazenamento criado, selecione Contêineres. Selecione o contêiner knowledge-store.

21 - Selecione qualquer um dos itens e clique no arquivo objectprojection.json e em editar para ver o JSON produzido para um dos documentos do armazenamento de dados do Azure.

![alt text](assets/image-19.png)

22 - Retorne aos Contêineres da conta de armazenamento e selecione coffee-skillset-image-projection

![alt text](assets/image-20.png)

23 - Selecione qualquer um dos itens, selecione qualquer um dos .jpg arquivos. Selecione Editar para ver a imagem armazenada do documento. Observe como todas as imagens dos documentos são armazenadas dessa maneira.

![alt text](assets/image-21.png)

24 - Retorne aos Contêineres da conta de armazenamento, selecione Navegador de armazenamento no painel esquerdo e selecione Tabelas. Há uma tabela para cada entidade no índice. Selecione a tabela coffeeSkillsetKeyPhrases.

![alt text](assets/image-22.png)

Veja as frases-chave que a loja de conhecimento conseguiu capturar do conteúdo das avaliações. Muitos dos campos são chaves, portanto, você pode vincular as tabelas como um banco de dados relacional. O último campo mostra as frases-chave que foram extraídas pelo conjunto de habilidades.

## Conclusão

Aqui é finalizado o Laboratório do Azure Cognitive Search.