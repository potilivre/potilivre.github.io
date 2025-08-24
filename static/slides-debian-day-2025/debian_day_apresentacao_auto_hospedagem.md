# Apresentação Debian Day

# Montando um servidor de midia caseiro

## Pisando o pézin na auto hospedagem

- Episódio com o plex

- Não curti, pq tinha funções que eu precisava pagar pra usar

- Prime video anunciando q ia colocar anúncio (depois todo mundo fazendo o mesmo)

## A descoberta

- Post no blusky de alguem falando da familia arr
- A maior surpresa: Todos os programas são GPL3

## O mergulho de cabeça

- Descobri que o jellyfin tinha uma cliente oficial pra tv la de casa
- Uns meses depois de uso, percebi que ficar tudo na minha maquina não ia dar certo

## Bora montar um servidor!

### Imposições a mim mesmo

- Gastar pouco
- Fazer o melhor possivel com software antes de gastar com hardware
- Toda os apps que vai rodar no servidor *_precisa_* , ser software livre

### Opções que eu tinha

- Comprar um computador usado
- Comprar um raspberryPI (ou qualquer outro frutaPI)
- Montar um servidor profissional

#### Fui garimpar na olx

- Positivo
- 100Gb de HD
- 4Gb de RAM

### Escolha do SO:

- Raspbian
- Debian

### Escolha do gerenciador de container:

- Infelizmente precisei usar docker
- Podman tinha incompatibilidade com os apps da stack

### A stack de aplicativos

#### O que vamos precisar??

- Criar uma pasta no seu computador, para guardar seus filmes e series
  
  - De dominio publico, ta?

- Organizar essa pasta
  
  - Renomear cada filme e serie
  - Colocar cada filme e cada serie em uma pastinha especifica
  - Colocar cada tamporada de serie numa pastinha especifica

- Monitorar essa pasta
  
  - Alguem pra te dizer o que voce tem e o que voce nao tem
  - Quais series eu tenho, e quais episodios faltam?
  
  *Exemplo*: Quero ver As Novas Aventuras de Tarzan (1035)
  
  - No meu HD só tem os episodios do 1 ao 6, e eu preciso baixar os episodios 7 ao 12
  
  - Boa noticia! Tarzan está em dominio publico e pode ser baixado por torrent!!

- Procurar os episodios que faltam
  
  - Procurar os episodios que faltam no torrent
  
  - Ao achar, encaminhar esse download para o torrent
  
  - Baixar os episodios que faltam

- Gerenciar as fontes de torrent
  
  - Voce usa um site de torrent, e do nada ele sai do ar, o que voce vai fazer?

- Mover os episodios baixados para a sua respectiva pasta

- Disponibilizar esses filmes e series para o resto da rede

#### Quem vai fazer o que?

| Função                                                    | Programa    |
| --------------------------------------------------------- | ----------- |
| Organizar essa pasta                                      | Sonarr      |
| Monitorar essa pasta                                      | Sonarr      |
| Procurar os episodios que faltam                          | Sonarr      |
| Gerenciar as fontes de torrent                            | Prowlarr    |
| Baixar                                                    | Qbittorrent |
| Mover os episodios baixados para a sua respectiva pasta   | Sonarr      |
| Disponibilizar esses filmes e series para o resto da rede | Jellyfin    |

#### Gerenciadores de mídia

| Programa | Tipo de mídia |
| -------- | ------------- |
| Sonarr   | Séries        |
| Radarr   | Filmes        |
| Lidarr   | Musicas       |
| Readarr  | Livros        |
| MyLar3   | Quadrinhos    |

#### Infinitas possibilidades!!

- Comunidade ativa
- Plugins (por falta melhor de palavra) de usuarios da comunidade

##### Add-ons que eu uso

| Função                                                                                | Programa   |
| ------------------------------------------------------------------------------------- | ---------- |
| Monitora a biblioteca e baixa legenda de filmes e episodios que estao em outra lingua | Bazarr     |
| Gerenciador de pedidos dos usuarios                                                   | Jellyseerr |
| Se por algum motivo o download não ocorrer, vai ficar tentando denovo                 | Huntarr    |
| Vai limpar a biblioteca excluindo coisas que não se usa mais                          | Janitorr   |
| Exclui downloads parados no meio                                                      | Cleanuparr |
| Ajuda na configuração de perfis de download                                           | Profilarr  |
| Recomenda novas series e filmes baseados no que cada usuario asiste                   | SuggestArr |

##### Recomendações pra quem quer começar (especificamente, hospedar mídia)

- Trash guides
- Servarr wiki
- Reddit (infelizmente)

##### Auto hospedagem no geral

- https://selfh.st/
- SauberLab
- Diolinux

### Upgrades futuros:

- Uma RAM de 8gb
- Um SSD de 256
- Um roteador movel (pra instalar uma VPN nele e tchau brigado)
