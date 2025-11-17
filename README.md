# Plano-de-Testes-de-Seguran-a
Objetivo: Validar se o sistema atende aos requisitos de segurança, garantindo confidencialidade, integridade, disponibilidade e conformidade com normas aplicáveis (LGPD, GDPR, ISO 27001).  Escopo: Aplicações web, sistemas corporativos ou aplicativos móveis que armazenam dados sensíveis.

1️⃣ Cenário de Teste – Acesso e Autenticação

Garantir que apenas usuários autorizados consigam acessar o sistema.

Item	Passo	Resultado Esperado	Status
1	Login com usuário e senha corretos	Usuário autenticado com sucesso	☐
2	Login com usuário inválido	Mensagem de erro genérica (não detalha se usuário existe)	☐
3	Login com senha incorreta	Mensagem de erro genérica e registro da tentativa	☐
4	Teste de autenticação multifator (2FA)	Login só permitido após validar segundo fator	☐
5	Bloqueio após múltiplas tentativas	Conta bloqueada após 5 tentativas	☐

2️⃣ Cenário de Teste – Controle de Acesso

Garantir que usuários só possam acessar funções permitidas por seu perfil.

Item	Passo	Resultado Esperado	Status
1	Usuário comum acessa área de admin	Acesso negado	☐
2	Administrador acessa funcionalidades	Todas disponíveis	☐
3	Acesso via URL direta a páginas restritas	Redirecionamento ou negação	☐


3️⃣ Cenário de Teste – Criptografia e Proteção de Dados

Validar proteção de dados sensíveis.

Item	Passo	Resultado Esperado	Status
1	Transmissão de dados (login, formulários)	HTTPS/TLS ativo	☐
2	Armazenamento de senhas	Hash seguro (bcrypt/argon2)	☐
3	Criptografia de dados em banco	Somente leitura com chave autorizada	☐
4️⃣ Cenário de Teste – Proteção contra Vulnerabilidades

Garantir que o sistema não esteja vulnerável a ataques básicos.

Item	Passo	Resultado Esperado	Status
1	Teste de SQL Injection	Sistema bloqueia requisições maliciosas	☐
2	Teste de XSS	Scripts maliciosos não executam	☐
3	Teste de CSRF	Requisições maliciosas bloqueadas	☐
4	Upload de arquivos maliciosos	Sistema valida tipo, tamanho e extensão	☐
5️⃣ Cenário de Teste – Conformidade Legal e Normativa

Garantir conformidade com normas de proteção de dados e segurança da informação.

Item	Requisito	Verificação	Status
1	LGPD / GDPR	Consentimento explícito para coleta de dados	☐
2	LGPD / GDPR	Usuário pode solicitar exclusão de dados	☐
3	ISO 27001	Políticas de senha e controle de acesso implementadas	☐
4	ISO 27001	Logs de auditoria de atividades sensíveis registrados	☐
5	Normas internas	Atualizações e patches aplicados	☐
6️⃣ Cenário de Teste – Backup e Recuperação

Garantir disponibilidade e recuperação de dados.

Item	Passo	Resultado Esperado	Status
1	Backup automático	Backup consistente no horário programado	☐
2	Recuperação de dados	Restauração correta de dados	☐
3	Redundância do sistema	Operação mínima mantida durante falhas	☐
✅ Checklist Resumido de Segurança

 Login seguro e autenticação multifator

 Controle de acesso baseado em perfis

 Criptografia de dados em trânsito e repouso

 Proteção contra SQLi, XSS, CSRF e uploads maliciosos

 Conformidade com LGPD, GDPR e ISO 27001

 Registro de logs e auditorias

 Backup automático e plano de recuperação de desastres

📌 Observações

Este plano é genérico e escalável para qualquer sistema.

Pode ser adaptado para aplicativos móveis, sistemas corporativos ou IoT.

Serve como base para auditorias internas e testes de segurança.
