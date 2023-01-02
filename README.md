---

Engines MySQL
Esse texto visa apresentar o funcionamento das engines do banco de dados MySQL.
A assunto busca mostrar as principais diferenças entre as engines do MySQL, de forma simples e não técnica.
Esse texto é voltado para quem está iniciando no mundo do SQL e quer entender um pouco mais sobre esse assunto.

---

Quais as diferenças entre os motores de banco de dados no MySQL?
O que é um motor de banco de dados?
Um motor de banco de dados é um software que permite que os usuários acessem e manipulem dados armazenados em um banco de dados. O motor de banco de dados é responsável por gerenciar o acesso aos dados, bem como a recuperação e armazenamento de dados.

---

Quais são os motores de banco de dados no MySQL?
Os principais motores de banco de dados no MySQL são:
MyISAM
InnoDB
MEMORY
ARCHIVE
CSV
MERGE
NDB
NDBCLUSTER

Hoje vamos falar sobre os motores MyISAM, InnoDB e MEMORY e suas diferenças.

---

InnoDB
O que é o InnoDB?
O InnoDB é um motor de banco de dados de transação, que suporta transações de banco de dados com recursos de recuperação de falhas e bloqueio de linha. Ele armazena dados em tabelas em arquivos de dados e índices em arquivos de índice.
Quais são as principais características do InnoDB?
Todas as tabelas InnoDB são armazenadas em arquivos de dados e índices em arquivos de índice. Os arquivos de dados tem a extensão .ibd e os arquivos de índice, que contêm o formato da tabela, têm a extensão .frm.
O InnoDB suporta transações de banco de dados com recursos de recuperação de falhas e bloqueio de linha.
O InnoDB suporta tabelas com chaves primárias compostas.
Ao fazer uma consulta, o InnoDB verifica se a consulta pode ser resolvida usando um índice. Se não puder, ele faz uma varredura completa da tabela.
Quando tiver uma mudança de dados na tabela, o InnoDB bloqueia somente as linhas afetadas. Dessa forma, o InnoDB pode lidar com grandes quantidades de dados.
O InnoDB hoje é o motor padrão do MySQL. Depois que o InnoDB foi introduzido, o MyISAM foi considerado obsoleto e não é mais recomendado para novos projetos.

---

MyISAM
O que é o MyISAM?
O MyISAM é um motor de banco de dados de tabela, que armazena dados em tabelas em arquivos de dados e índices em arquivos de índice. O MyISAM não suporta transações de banco de dados com recursos de recuperação de falhas e bloqueio de linha.
Quais são as principais características do MyISAM?
Todas as tabelas MyISAM são armazenadas em arquivos de dados e índices em arquivos de índice. Os arquivos de dados têm a extensão .MYD e os arquivos de índice, que contêm o formato da tabela, têm a extensão .MYI.
O MyISAM não suporta transações de banco de dados com recursos de recuperação de falhas e bloqueio de linha.
O MyISAM não suporta tabelas com chaves primárias compostas.
Quando tiver uma mudança de dados na tabela, o MyISAM bloqueia a tabela inteira. Dessa forma, o MyISAM não pode lidar com grandes quantidades de dados.

---

MEMORY
O que é o MEMORY?
O MEMORY é um motor de banco de dados de tabela, que armazena dados em tabelas em memória. O MEMORY não suporta transações de banco de dados com recursos de recuperação de falhas e bloqueio de linha.
Quais são as principais características do MEMORY?
Todas as tabelas MEMORY são armazenadas em memória.
O MEMORY não suporta transações de banco de dados com recursos de recuperação de falhas e bloqueio de linha.
Caso surja uma falha no servidor, os dados serão perdidos.
O MEMORY não suporta tabelas com chaves primárias compostas.
Quando tiver uma mudança de dados na tabela, o MEMORY bloqueia a tabela inteira. Dessa forma, o MEMORY não pode lidar com grandes quantidades de dados.

---

MyISAM vs MEMORY
Realmente não há muita diferença entre os motores MyISAM e MEMORY. Ambos armazenam dados em arquivos de dados e índices em arquivos de índice. Ambos não suportam transações de banco de dados com recursos de recuperação de falhas e bloqueio de linha. Ambos não suportam tabelas com chaves primárias compostas. Ambos bloqueiam a tabela inteira quando tiver uma mudança de dados na tabela. Ambos não podem lidar com grandes quantidades de dados.
A diferença entre os motores MyISAM e MEMORY é que o MEMORY armazena dados em memória RAM e o MyISAM armazena dados em arquivos de dados.
Dessa forma, o MEMORY é incrivelmente rápido. Ele é usado para armazenar dados temporários, como dados de sessão, dados de cache e dados de fila.

---

Espero que tenha ajudado. Qualquer dúvida, correção ou sugestão, por favor, deixe nos comentários.
