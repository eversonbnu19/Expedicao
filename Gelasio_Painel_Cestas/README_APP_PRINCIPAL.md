# Gelasio App Principal

Este pacote cria uma entrada unica para o Painel de Cestas:

- `Gelasio_App_Principal_Login.hta`: app principal com tela de login.
- `Gelasio_App_Principal_usuarios.json`: criado automaticamente na primeira abertura.

## Usuarios iniciais

| Usuario | Senha | Perfil |
| --- | --- | --- |
| admin | admin123 | Admin completo |
| jessica | 1234 | Movimentacao V1 |
| paula | 1234 | Movimentacao V2 |
| nathan | 1234 | Movimentacao V3 |
| expedicao | exp123 | Expedicao |
| financeiro | fin123 | Financeiro |

Troque as senhas antes de usar em producao.

## Como usar com o painel atual

Coloque a pasta `Gelasio_App_Principal` ao lado da pasta `Gelasio_Painel_Cestas`.
O app tenta encontrar automaticamente:

- `dados\painel_cestas_data.json`
- `painel_cestas_status`
- os arquivos `.hta` antigos, quando existirem

Enquanto as telas antigas nao forem migradas para dentro do app unico, o login funciona como entrada principal e libera os modulos conforme o perfil.

## Proximo passo recomendado

Quando o ZIP original puder ser lido, o ideal e migrar o codigo repetido dos arquivos por usuario para dentro deste HTA unico, mantendo apenas:

1. um arquivo principal;
2. um cadastro de usuarios;
3. uma tabela de permissoes;
4. um arquivo de dados compartilhado.

