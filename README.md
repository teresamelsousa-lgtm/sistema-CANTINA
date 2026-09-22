EduControl — Sistema de Gestão Escolar e Cantina
​1. Visão Geral
​O EduControl é uma plataforma web para gestão integrada de cantinas escolares e controle de acesso de alunos. Desenvolvido para modernizar a rotina das instituições de ensino, o sistema combina leitor de QR Code, confirmação prévia de presença no cardápio semanal e sincronização em nuvem via Google Sheets (Google Apps Script), funcionando sem a necessidade de servidores pagos ou infraestruturas complexas.
​2. Perfis de Acesso e Funcionalidades
​O sistema possui uma estrutura modular dividida em três níveis de acesso direcionados aos diferentes públicos da escola:
​🎓 Módulo do Aluno (Público)
​Consulta por Matrícula: O estudante insere sua matrícula/ID para acessar seu painel pessoal.
​Geração de QR Code: Criação dinâmica de um QR Code individual no dispositivo do aluno para ser apresentado no balcão da cantina.
​Cardápio Semanal Interativo: Visualização das refeições programadas de segunda a sexta-feira.
​Confirmação Prévia ("Vou comer" / "Não vou"): O aluno informa com antecedência se irá almoçar em dias específicos da semana, auxiliando a equipe da cozinha no planejamento da produção.
​Status do Dia: Exibição clara se o check-in do dia já foi efetuado ou se permanece pendente.
​🍱 Módulo da Cantina (Restrito por Senha)
​Scanner de QR Code em Tempo Real: Leitura dinâmica usando a câmera de smartphones, tablets ou computadores com suporte a webcam.
​Validação Instantânea de Acesso:
​Autorizado: Confirma o direito do aluno à refeição e registra a presença.
​Bloqueio por Duplicidade: Impede que o mesmo aluno almoce mais de uma vez no mesmo dia.
​Bloqueio por Recusa Prévia: Alerta a equipe caso o aluno tenha marcado no cardápio que "Não iria comer".
​Alerta de Matrícula Inválida: Identifica IDs não cadastrados no sistema.
​Entrada Manual de ID: Opção de digitação rápida da matrícula para situações em que o QR Code não possa ser lido.
​Painel de Atividade: Exibição do contador total de refeições servidas no dia e feed em tempo real com as últimas entradas validadas.
​🛡️ Módulo da Direção (Restrito por Senha)
​Gestão de Alunos: Cadastrar novos alunos (Nome Completo e Matrícula) e remover registros.
​Tabela de Alunos Cadastrados: Visualização organizada de toda a base escolar.
​Sincronização com Nuvem: Botão para forçar a atualização de dados diretamente com a planilha mestre no Google Sheets.
​3. Arquitetura e Tecnologias
​O sistema foi arquitetado como uma aplicação Single Page Application (SPA) leve e responsiva:
​Frontend: HTML5 semântico, JavaScript (ES6+) e Tailwind CSS para interface moderna e responsiva em celulares, tablets e PCs.
​Componentes JS Integrados:
​html5-qrcode: Para leitura precisa de códigos QR via câmera do dispositivo.
​qrcode.js: Para renderização instantânea do QR Code do aluno no navegador.
​FontAwesome: Para ícones visuais e interativos.
​Backend & Banco de Dados (Nuvem):
​Google Sheets + Google Apps Script (GAS): Funciona como banco de dados serverless. As escolhas de cardápio, cadastros e check-ins são persistidos diretamente em abas de uma planilha do Google Drive.
​Fallbacks Locais: O sistema opera com armazenamento local temporário caso haja indisponibilidade temporária de conexão.
​4. Benefícios e Impacto Operacional
​Redução Zero de Custos de Servidor: Utiliza a infraestrutura gratuita do Google Workspace.
​Redução de Filas na Cantina: A validação via QR Code leva menos de 2 segundos por aluno.
​Combate ao Desperdício de Alimentos: Com a confirmação prévia no cardápio, a cozinha prepara a quantidade exata de alimentos para o dia.
​Controle e Transparência: Impede refeições duplicadas e fornece relatórios auditáveis em tempo real na Planilha Google.
​Interface Inclusiva e Responsiva: Funciona em qualquer navegador sem necessidade de instalação de aplicativos nas lojas (App Store / Play Store).
