# resumo-do-lab
Este repositório contém o resumo das lições aprendidas durante o desenvolvimento do lab na DIO

 IaaS (Infrastructure as a Service):

Você aluga máquinas virtuais (VMs) e cuida de tudo dentro dela: sistema operacional, atualizações, segurança.

Exemplo no Azure: Azure Virtual Machines.
 Você acessa por SSH e instala o que quiser.

 PaaS (Platform as a Service):

Você aluga uma plataforma pronta pra rodar seu app, sem se preocupar com o sistema operacional, atualizações, infraestrutura.

Exemplo no Azure: App Service.
 Nem sempre tem SSH, você faz o deploy do seu app direto na plataforma.

Regiões no Azure
As regiões no Azure são basicamente os lugares no mundo onde o Azure tem data centers. Quando você cria qualquer recurso (uma máquina virtual, um banco, um app service), precisa escolher uma região. Isso importa por alguns motivos:

Quanto mais perto do seu público ou de você, menor a latência (mais rápido o acesso).

Nem todas as regiões oferecem todos os serviços (alguns só existem em regiões específicas).

O preço de alguns serviços pode variar de uma região para outra.

Por exemplo: se seus usuários estão no Brasil, faz mais sentido escolher a região Brazil South (São Paulo).

Armazenamento (Blob Storage)
O Blob Storage é o serviço do Azure para armazenar arquivos na nuvem. Pode ser usado para guardar imagens, vídeos, PDFs, backups de banco de dados, etc.
Ele funciona diferente de um HD normal — você acessa os arquivos por API ou SDK, não por um “explorador de arquivos” comum.

Existem alguns tipos de blobs:

Block blobs: arquivos normais (imagens, vídeos, etc).

Append blobs: arquivos de log, onde você sempre adiciona mais dados no final.

Page blobs: usados por máquinas virtuais para armazenar os discos virtuais.

No seu caso, se você não vai trabalhar com upload/download de arquivos em apps, não precisa se preocupar com isso agora.

Máquinas Virtuais (VMs)
Uma máquina virtual no Azure é como se fosse um computador remoto, funcionando na nuvem. Você escolhe qual sistema operacional vai usar (Windows ou Linux), define a quantidade de memória, CPU, armazenamento, e faz a configuração que quiser.

Você acessa a VM por SSH (se for Linux) ou Área de Trabalho Remota (se for Windows).
O ponto é: você é responsável por tudo dentro dela. Precisa configurar, atualizar, instalar segurança, cuidar das aplicações.

É uma solução mais flexível, mas dá mais trabalho e geralmente sai mais caro do que usar uma plataforma pronta. Para projetos pessoais ou apps simples, talvez seja mais do que você precisa.

Outros conceitos importantes
Além dessas partes, alguns outros nomes que aparecem bastante no Azure:

App Service: serviço que já cuida de infraestrutura pra você rodar um site ou API. Você só faz o deploy do seu código.

Functions: roda pequenas partes de código sob demanda, sem precisar manter um servidor ligado o tempo todo.

Resource Group: uma espécie de “pasta” onde você organiza todos os recursos de um projeto.

Virtual Network: rede virtual privada, usada pra conectar recursos entre si com mais segurança.

Load Balancer: distribui o tráfego entre várias instâncias do seu app, pra garantir performance e disponibilidade.
