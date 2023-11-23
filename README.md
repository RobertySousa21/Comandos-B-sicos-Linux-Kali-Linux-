Linux
Diretórios
~ - pasta home

/ - diretório raiz

bin - arquivos binários

boot - arquivos de inicialização

dev - arquivos entrada e saída do sistema

etc - arquivo de configuração

home - usuários do sistema

lib - arquivo de bibliotecas

media - pasta dos dispositivos

opt - arquivos de aplicações não oficiais do sistema

sbin - arquivos binários de inicialização

tmp - arquivos temporários

usr - arquivos de modo leitura

var - arquivos de log / arquivos variáveis

Comandos básicos para manipulação de arquivos
ls - listar diretórios

cd - serve para mudar de diretórios

cd nome do diretório - muda para o diretório especifico

cd / raiz dos arquivos

cd .. / retornar um diretório

cd - volta para o diretório anterior

cd ~ - vai para a home

cd table - auto completa o nome do diretório

ls -l - mostra todos os detalhes dos arquivos e diretórios

ls -a - mostra os arquivos ocultos

ls -lh - mostra num formato mais amigável os detalhes dos arquivos e diretórios

ls -ltr - mostra a data de última alteração do arquivo

ls -lr - imprimi os arquivos na hora reversa

ls -R - exibe os subdiretórios

ls -lS - ordena pelo tamanho do arquivo

ls -m - lista arquivos e diretórios separados por virgula

ls --help - mostra todos os comandos possíveis

CTRL + ALT + T - abri o terminal no Linux

clear - limpa o terminal

cat + nome do arquivo - serve para criar um arquivo ou exibir o conteúdo de um arquivo

cat teste + teste2 > teste3 concatena o conteúdo dos arquivos

cat nome do arquivo 1 + nome do arquivo 2 > nome do arquivo 3 - concatena o conteúdo dos arquivos

cat -n + nome arquivo - exibe o arquivo com números de linha

cat -e adiciona o $ no final do arquivo para delimita-los

cat + teste4 >> teste3 concatena o conteúdo do arquivo 4 no final do arquivo3

cat -e + nome do arquivo - adiciona o $ no final do arquivo para delimita-los

cat + nome do arquivo 4 >> nome do arquivo 3 concatena o conteúdo do arquivo 4 no final do arquivo3

touch + teste2nome do arquivo 2 - altera informações da última alteração do arquivo

touch + nome do arquivo - ele cria um arquivo

man + nome do comando - exibe todos os parâmetros possíveis para aquele comando

ctrl + shif + r abrir a opção para busca de comando anteriores + ctrl + r + nome do comando encontra o comando especifico

mkdir + nome do diretório - cria um diretório

mkdir -v - exibi o que o comando está fazendo

mkdir -p + nome do diretório/nome do diretório/nome do diretório - cria múltiplos diretórios

mkdir ../ + nome do diretório - retorna um diretório e cria um diretório

rm + nome do arquivo - apaga um arquivo

rm -i + nome do arquivo - exibi um informativo, para confirmar se você deseja apagar o arquivo

rm -dv + nome do diretório - apaga diretórios vazios

rm -rfv + nome do diretório - apaga o diretório com os arquivos de forma recursiva

rmdir + nome do diretório - apaga só o diretório

rmdir -p + nome dos diretórios - apaga varios diretórios de uma vez

cp + nome do arquivo + nome do arquivo2 - ele criar uma cópia do arquivo

cp -r + nome do diretório + nome do diretório destino - ele copia um diretório para dentro de outro diretório

mv + nome do arquivo + nome do arquivo2 - ele cópiacopia e apaga o arquivo de origem e mantem apenas o arquivo de destino

mv + nome do arquivo + pasta de destino - ele copia o arquivo de origem

pwd - saber exatamente onde estamos na estrutura dos diretórios

Atualizar pacotes no Linux
sudo apt-get update - atualiza todos os repositórios

sudo apt-get upgrade - atualiza todos os aplicativos

nome do programa + enter - verificar se tem o programa instalado na máquina

sudo apt-get install + nome do programa - instala aplicativos

sudo apt-get purge + nome do programa - instala aplicativos

sudo apt-get dist-upgrade - atualizar o Linux(usar com cautela)

sudo apt-get autoremove - remove aplicativos que não estão sendo utilizados

apt-cache search + nome do aplicativo - buscar um aplicativo no Linux

Buscas em arquivos e diretórios

head + nome do documento - exibe o topo de um documento

head -n 1 nome do documento - exibe a primeira linha do documento

head -n 1 nome do documento > documento 2 - passa o conteúdo do documento de origem para o documento de destino

tail + nome do documento - exibe o final de um documento

tail -n 1 nome do documento - exibe a final da linha do documento

tail -n 1 nome do documento > documento 2 - passa o conteúdo do documento de origem para o documento de destino (final do arquivo)

tail -f + nome do documento - ele atualiza o documento dinamicamente (utilizado para debug de log)

grep 'nome de palavra a ser procurada' + nome do documento - ele busca a palavra dentro do documento

grep -i 'nome de palavra a ser procurada' + nome do documento - ele busca a palavra dentro do documento sem fazer diferença entre maiúscula e minúscula

grep -c 'nome de palavra a ser procurada' + nome do documento - ele contas as ocorrências da palavra dentro do documento

grep 'nome de palavra a ser procurada' + nome do documento -r - ele procura em todos os arquivos do diretório

find -name 'nome do documento'- ele procura em todos os arquivos de todos os diretórios anteriores

find -iname 'nome do documento'- ele procura em todos os arquivos de todos os diretórios anteriores, ignorando case sensitive

find -empty - ele busca por diretórios vazios

locate + nome do documento - localiza arquivos em uma base de dados (somente arquivos antigos)

locate -S - Verifica informações do banco de dados

!! - Executa o último comando utilizado

Which + nome do comando - mostra o caminho do aplicativo que está sendo executado

vim
Vim + nome do arquivo a ser criado - abre o editor vazio para criar o arquivo

I + ENTER - modo de inserção

Esc - sai do modo de inserção

: + X - Salva o arquivo e sai

: + W - Salva o arquivo, mas não fecha o editor

:q - fecha o editor

Vim + nome do arquivo - abre o editor para editar o arquivo

D+D - deleta a linha

U - Desfaz as alterações

CTRL + R - refaz todas as alterações

/ + palavra a ser buscada - ele encontra a primeira ocorrência

N - Navega em todas as ocorrências

Shift + n - volta em todas as ocorrências da palavra

:%s + palavra/palavra que irá substituir/g - substitui uma palavra ou sentença todas as ocorrências

:s + palavra/palavra que irá substituir/g - substitui uma palavra ou sentença apenas de uma linha

:q! - sai e perde todas as alterações no arquivo

Gerenciamento de usuários e grupos
sudo + Adduser + nome do usuário - cria um usuário

Ls /home/ - exibi todos os usuários

sudo userdel —remove + nome do usuário a ser deletado - remove um usuário do sistema

sudo usermod -c ‘+ nome do usuário a ser alterado’ + nome do usuário - altera o nome do display

sudo usermod -l + nome do usuário a ser alterado -d /home/ nome alterado -m + nome do usuário antigo

sudo user mod - L + nome do usuário a ser bloqueado - bloqueia a o usuário

sudo user mod - U + nome do usuário a ser bloqueado - desbloqueia a o usuário

getent group - exile todos os grupos criados no sistema

sudo groupadd -g + id do grupo + nome do grupo - cria um grupo

sudo groupdel + nome do grupo - deleta um grupo

groups + nome do usuário - exibi os grupos pertencente ao usuário

sudo usermod -a -G + nome do grupo que o usuário irá + nome do usuário - move um usuário de um grupo para outro

sudo gpasswd -d + nome do usuário + grupo que ela está - retira um usuário de um grupo

sudo su - transforma um usuário em super usuário e exit + enter sai do super usuário

passwd - trocar a senha do usuário atual
