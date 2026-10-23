# fd-midia

Mídia das notas de atualização do Web Frigo (imagens que a nota de versão referencia).
A nota guarda só o endereço; o sistema carrega a imagem daqui em tempo de execução.

## Como o sistema usa

- A nota de versão escreve `![legenda](https://raw.githubusercontent.com/gabeemolina/fd-midia/main/notas/AAAA-MM/arquivo.webp)`.
- O Web Frigo só carrega imagem deste repositório (lista fechada de hosts e caminhos no `fd_web`).
- Sem internet, sem o arquivo ou com erro, a nota mostra apenas a legenda. Nunca fica com buraco.

## Regras

- Pasta por mês da versão: `notas/AAAA-MM/`.
- Formato WebP, largura até 1600 px, até ~200 KB. Nome com hash curto do conteúdo (`01-painel-sino.3f9a2c.webp`): um arquivo nunca muda de conteúdo; correção = arquivo novo.
- Nada de dado real de cliente nas capturas: base de teste, usuários de teste, nomes borrados quando preciso.
- Quem fecha a versão gera os arquivos com o `publicar_midia.py` (na pasta da feat de notificações) e commita aqui. O script devolve as linhas `![legenda](url)` prontas para a nota.

## Endereços

Prefixo público: `https://raw.githubusercontent.com/gabeemolina/fd-midia/main/`
Para endereço imutável no script oficial da versão, trocar `main` pelo código do commit.
