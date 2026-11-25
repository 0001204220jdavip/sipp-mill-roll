PROJETO SIPP - MILL ROLL
Cadastro e consulta de rolos industriais
========================================

Esta versao foi feita com HTML, CSS e JavaScript. Nao utiliza Node.js,
XAMPP, MySQL, SQL, npm ou servidor proprio.

O sistema guarda uma copia dos cadastros no navegador por meio do
localStorage. Alem disso, o QR Code leva os dados do produto dentro dele.
Assim, outro celular ou computador consegue ler as informacoes sem precisar
consultar o armazenamento do navegador que fez o cadastro.

1. ARQUIVOS DO PROJETO
----------------------
- index.html: formulario de cadastro, lista local, geracao do QR Code e exportacao da planilha Excel.
- produto.html: pagina que mostra os dados quando o QR Code e escaneado.
- catalogo.js: lista de produtos usada nas sugestoes do formulario.
- logo-mill-roll.png: logotipo enviado para o projeto.

A exportacao para Excel usa a biblioteca ExcelJS, carregada automaticamente
pela internet quando a pagina e aberta. Nao e necessario instalar nada.

Mantenha todos esses arquivos na mesma pasta.

2. COMO ABRIR E TESTAR NO COMPUTADOR
------------------------------------
1. Extraia a pasta Projeto_SIPP.
2. Abra a pasta.
3. De dois cliques em index.html.
4. Preencha os campos e clique em "Cadastrar e Gerar QR Code".
5. O cadastro aparece na lista e fica salvo nesse navegador.

Nao precisa abrir o VS Code, terminal ou instalar programas para fazer o
cadastro local.

ATENCAO: quando o projeto e aberto diretamente pelo arquivo index.html,
o QR Code e gerado como texto. Ao escanear, o leitor mostra os dados do
produto. Para que o QR Code abra a pagina bonita de consulta em outro
navegador, siga a proxima etapa.

3. COMO FAZER O QR CODE ABRIR A FICHA EM OUTRO CELULAR OU COMPUTADOR
--------------------------------------------------------------------
Para abrir a pagina produto.html em outro aparelho, os arquivos do site
precisam estar publicados em um endereco da internet. Isso e uma hospedagem
de paginas estaticas: nao usa banco de dados, nao guarda cadastros em um
servidor e nao exige um servidor proprio.

Uma opcao gratuita para um projeto escolar e o GitHub Pages:

1. Crie uma conta no GitHub, caso ainda nao tenha uma.
2. Crie um repositorio para o projeto.
3. Envie para ele os arquivos index.html, produto.html, catalogo.js e
   logo-mill-roll.png.
4. No repositorio, abra Settings (Configuracoes) e depois Pages.
5. Em Build and deployment, escolha Deploy from a branch.
6. Selecione a branch main e a pasta / (root), depois salve.
7. O GitHub mostrara o endereco publico do site. Abra esse endereco e faca
   os cadastros pela pagina publicada.

Quando o site e aberto por um endereco https, o sistema monta o QR Code com
um link para produto.html e coloca os dados do rolo dentro do proprio link.
Ao escanear, qualquer aparelho com internet abre a ficha do produto.
Nao e preciso que o outro aparelho tenha os cadastros guardados no navegador.

4. COMO OS DADOS SAO GUARDADOS
------------------------------
- A lista completa fica no localStorage do navegador que fez os cadastros.
- O QR Code leva uma copia das informacoes no momento em que foi gerado.
- A pagina produto.html le os dados que estao no QR Code e mostra a ficha.
- O QR Code nao consulta nem atualiza automaticamente o cadastro original.
- Se a situacao ou a localizacao mudar, atualize o cadastro no navegador onde
  ele foi criado e gere/imprima uma nova etiqueta.
- Outro navegador consegue consultar os dados pelo QR Code, mas nao altera a
  lista que esta salva no primeiro navegador.

5. LIMITES E CUIDADOS
---------------------
- Sem banco de dados compartilhado, os cadastros locais nao sincronizam entre
  aparelhos.
- Se limpar os dados do navegador, os cadastros locais podem ser apagados.
- O QR Code mostra as informacoes para qualquer pessoa que consiga escanea-lo.
  Nao coloque nele informacoes sigilosas que nao devam ser vistas.
- A biblioteca que cria o QR Code e carregada de um site externo; por isso,
  e necessario ter internet na hora de gerar o codigo.
- Ao usar o site publicado, a pagina de consulta tambem precisa de internet.

6. EXPORTAR A LISTA PARA O EXCEL
---------------------------------
Na tela inicial, clique em "Exportar para Excel (.xlsx)". O sistema cria uma
planilha com titulo, total de cadastros, cabecalhos destacados, filtros,
colunas com largura ajustada e linhas alternadas para facilitar a leitura.

A planilha e gerada no proprio navegador. Para carregar a biblioteca que
monta o arquivo Excel, e necessario estar conectado a internet no momento
da exportacao. Os cadastros continuam guardados somente neste navegador.

7. RESUMO
---------
O projeto nao usa servidor de aplicacao nem banco de dados. Para que uma
pagina formatada abra em outro dispositivo, e necessario apenas publicar os
arquivos estaticos em um endereco acessivel pela internet. Os dados do rolo
viajam dentro do QR Code, nao dentro de um banco central.
