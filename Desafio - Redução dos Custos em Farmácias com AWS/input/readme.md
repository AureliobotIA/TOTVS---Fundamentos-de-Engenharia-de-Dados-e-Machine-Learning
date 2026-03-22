
________________________________________
📦 Arquivo estoque_farmacia.csv

ID,Produto,Categoria,Quantidade,Preço_Unitário

1,Paracetamol 500mg,Medicamento,120,5.50
2,Ibuprofeno 400mg,Medicamento,80,8.90
3,Vitamina C 1g,Suplemento,200,12.00
4,Shampoo Anticaspa,Higiene,50,15.75
5,Creme Dental,Higiene,150,6.20
6,Álcool Gel 70%,Higiene,100,9.50
7,Omeprazol 20mg,Medicamento,60,18.00

Esse arquivo pode ser armazenado no Amazon S3 para centralizar os dados de estoque.
________________________________________
👥 Arquivo clientes_farmacia.sql

CREATE DATABASE farmacia;
USE farmacia;
CREATE TABLE clientes (
    id INT AUTO_INCREMENT PRIMARY KEY,
    nome VARCHAR(100) NOT NULL,
    cpf VARCHAR(14) UNIQUE NOT NULL,
    telefone VARCHAR(15),
    email VARCHAR(100),
    data_cadastro DATE DEFAULT CURRENT_DATE
);

INSERT INTO clientes (nome, cpf, telefone, email) VALUES
('Maria Silva', '123.456.789-00', '(13) 99999-1111', 'maria.silva@email.com'),
('João Pereira', '987.654.321-00', '(13) 98888-2222', 'joao.pereira@email.com'),
('Ana Costa', '456.789.123-00', '(13) 97777-3333', 'ana.costa@email.com'),
('Carlos Souza', '321.654.987-00', '(13) 96666-4444', 'carlos.souza@email.com');

Esse script pode ser usado no Amazon RDS (MySQL) para criar e popular a tabela de clientes.
________________________________________
👉 Agora seu relatório terá anexos práticos:

•	estoque_farmacia.csv (dados de estoque)
•	clientes_farmacia.sql (banco de clientes)
•	Link para o template de dashboard no Figma
•	Documentação oficial dos serviços AWS

Como incluir no relatório:

•	Etapa 3 (Amazon QuickSight): 

o	Adicione este dashboard como template visual para relatórios de vendas e estoque.
o	Insira o link acima na seção de Anexos junto com os arquivos estoque_farmacia.csv e clientes_farmacia.sql.
o	Isso mostra que o projeto já tem uma base prática para visualização de dados.
________________________________________

👉 Agora seu relatório terá:

•	Banco de dados (clientes_farmacia.sql)
•	Planilha de estoque (estoque_farmacia.csv)
•	Template de dashboard (link acima)
•	Documentação oficial dos serviços AWS
________________________________________

Manual Interno – Uso das Ferramentas AWS na Farmácia

🗂️ Amazon S3 – Armazenamento de Arquivos

Objetivo: Centralizar documentos como planilhas de estoque, relatórios e imagens de produtos.

Como usar:
•	Acesse o console AWS e vá até o serviço S3.
•	Crie um bucket com nome identificável (ex: farmacia-estoque).
•	Faça upload dos arquivos .csv, imagens e PDFs.
•	Configure permissões de acesso conforme a equipe (leitura/escrita).
•	Use links públicos ou privados para integrar com sistemas internos.
________________________________________

🧮 Amazon RDS (MySQL) – Banco de Dados Relacional

Objetivo: Gerenciar clientes, histórico de compras e dados de produtos.

Como usar:
•	No console AWS, crie uma instância RDS com MySQL.
•	Importe o script clientes_farmacia.sql para criar a base de dados.
•	Conecte-se via MySQL Workbench ou outro cliente usando as credenciais da instância.
•	Use queries SQL para consultar, inserir ou atualizar dados dos clientes.
________________________________________

📊 Amazon QuickSight – Visualização de Dados

Objetivo: Criar dashboards interativos com dados de vendas e estoque.

Como usar:
•	Acesse o QuickSight e conecte-se ao bucket S3 ou à instância RDS.
•	Importe os dados do arquivo estoque_farmacia.csv e da tabela clientes.
•	Crie gráficos de linha, pizza e tabelas dinâmicas.
•	Use o template de dashboard como referência visual.
•	Compartilhe os dashboards com a equipe via link ou exportação em PDF.
________________________________________

📎 Anexos Recomendados

•	estoque_farmacia.csv
•	clientes_farmacia.sql
•	Template visual do dashboard
•	Links para documentação oficial AWS
________________________________________

📄 Visual do Manual Interno – Uso das Ferramentas AWS na Farmácia
________________________________________
Como usar:

•	Inclua esse visual como anexo PDF no relatório.
•	Pode ser impresso e distribuído para a equipe da farmácia como guia de referência.
•	Serve como base para treinamentos internos sobre uso de tecnologia AWS.
Uma versão interativa do manual seria um documento em PDF com os seguintes recursos:

🧩 Funcionalidades interativas

•	Links clicáveis para: 
o	Console da AWS (S3, RDS, QuickSight)
o	Documentação oficial de cada serviço
o	Template de dashboard no Figma
•	Botões internos para navegar entre seções (ex: “Ir para Amazon RDS”)
•	Campos editáveis para: 
o	Inserir nome da farmácia
o	Personalizar nome dos buckets e instâncias
o	Adicionar observações específicas da equipe
•	Ícones e cores temáticas para facilitar a leitura e identificação visual
•	Checklist interativo para marcar etapas concluídas da implementação
________________________________________
🧠 Benefícios

•	Facilita treinamentos e onboarding de novos funcionários
•	Pode ser usado como guia prático durante a operação
•	Permite personalização conforme o crescimento da farmácia
________________________________________
🧠 Manual Interativo de Treinamento – AWS na Farmácia

🗂️ Seção 1: Introdução

•	Objetivo do treinamento
•	Benefícios da tecnologia AWS
•	Campo editável: Nome da farmácia e responsável pelo projeto

📁 Seção 2: Amazon S3 – Armazenamento

•	Explicação visual com ícones
•	Checklist interativo: 
o	[ ] Criar bucket
o	[ ] Fazer upload de arquivos
o	[ ] Configurar permissões
•	Link clicável: Console Amazon S3

🧮 Seção 3: Amazon RDS – Banco de Dados
•	Explicação com fluxograma de conexão
•	Campo editável: Nome da instância e credenciais
•	Link clicável: Console Amazon RDS
•	Quiz interativo: “Qual comando SQL cria uma tabela de clientes?”

📊 Seção 4: Amazon QuickSight – Dashboards
•	Visual do dashboard como referência
•	Campo editável: Nome do relatório
•	Link clicável: Console QuickSight
•	Atividade prática: Criar gráfico de vendas por categoria

📎 Seção 5: Recursos e Anexos
•	Links para arquivos: estoque_farmacia.csv, clientes_farmacia.sql
•	Template visual do dashboard
•	Documentação oficial AWS
________________________________________

