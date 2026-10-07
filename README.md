# Cavany — Gestão de Motel para GitHub Pages

## Publicar pelo próprio site do GitHub
1. Crie um repositório no GitHub, por exemplo `cavany-motel`.
2. Extraia este ZIP no computador. Abra a pasta `cavany-github`.
3. No repositório, clique em **Add file → Upload files** e envie o conteúdo dessa pasta. O arquivo `index.html` deve ficar na raiz do repositório, e não dentro de outra pasta. Não envie apenas o ZIP.
4. Confirme o envio em **Commit changes**.
5. Abra **Settings → Pages**.
6. Em **Build and deployment**, escolha **Deploy from a branch**.
7. Selecione a branch **main**, a pasta **/ (root)** e clique em **Save**.
8. Aguarde a publicação e abra o endereço mostrado pelo GitHub Pages.

A disponibilidade de Pages para repositórios privados depende do plano do GitHub. A publicação do site normalmente torna a interface acessível pela URL; esta edição não tem login.

## Antes de começar
Abra Configurações e ajuste o nome, as tarifas, as suítes e os produtos. Os valores iniciais são exemplos. Abra um caixa antes de finalizar pagamentos.

## Onde os dados ficam
**Esta é uma edição local adaptada para hospedagem estática.** Todos os registros ficam no armazenamento do navegador (localStorage), apenas no aparelho e perfil em uso. Não são enviados ao repositório. Outro aparelho, navegador, perfil ou endereço de site terá dados diferentes. Limpar os dados do navegador ou usar modo privado pode apagar registros.

Use **Configurações → Exportar backup completo** para guardar cópias. Esta edição exporta backups, mas não oferece restauração pela interface. O arquivo pode ser usado para uma migração técnica posterior. Para usar em equipe com dados compartilhados, é necessário um servidor e autenticação; GitHub Pages sozinho não fornece isso.

## Recursos
Suítes, entrada e saída, cobrança por período e hora adicional, consumo, estornos, estoque, reservas, limpeza, manutenção, transferências, caixa, despesas, sangrias, suprimentos, pagamento dividido, descontos, histórico, relatórios, CSV e comprovantes de 58/80 mm.

A impressão abre a janela do navegador. Escolha a impressora e o tamanho de papel. Bluetooth direto depende de integração com o equipamento. Os pagamentos são registros manuais, sem cobrança bancária integrada. O comprovante não é fiscal.

## Arquivos principais
- `index.html`: interface.
- `app.js`: regras de operação e armazenamento local.
- `logo.jpg`: logo fornecido.
- `.nojekyll`: desativa processamento Jekyll quando enviado.
- `fonte-online/`: fonte completa da versão com servidor, para desenvolvimento e migração.

## Rodar localmente
Com Python instalado, execute `python -m http.server 8080` nesta pasta e abra `http://localhost:8080`. Para uso normal, publique por HTTPS. Não abra simplesmente o HTML com um duplo clique: alguns recursos exigem uma origem segura.

## Fonte da versão online
A pasta `fonte-online` preserva o aplicativo original, incluindo regras, testes e fonte do Worker. O Worker usa um binding R2 chamado `BUCKET`. A autenticação da versão original era aplicada pela plataforma de hospedagem, fora do Worker. **Não publique o Worker diretamente na internet sem acrescentar autenticação e autorização**: ele pressupõe essa proteção externa.

Não foram incluídos credenciais, histórico Git, identificadores privados de hospedagem ou registros operacionais. A cópia da fonte online precisa de configuração própria de build, binding e acesso antes de ser implantada em outro serviço. O pacote da raiz já está pronto para GitHub Pages.

## Verificação realizada
Regras de estadia, consumo, estorno, pagamento dividido, caixa e reservas testadas na fonte original. A adaptação local foi verificada para criação, leitura, persistência, gravação e conflito de versão. A aparência e a impressão física ainda precisam de verificação no navegador e na impressora de destino.
