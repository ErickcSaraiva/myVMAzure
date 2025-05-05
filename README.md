# myVMAzure
usdo para projeto do bootcamp da DIO
🚀 Introdução
Este repositório documenta minha experiência na criação e configuração de uma máquina virtual (VM) na plataforma Microsoft Azure, conforme proposto no desafio da DIO. O objetivo principal deste projeto é aplicar os conhecimentos adquiridos nas aulas, documentar o processo de forma clara e estruturada, e utilizar o GitHub como ferramenta para compartilhamento de conhecimento técnico.

Aqui descrevo os passos que realizei para criar e configurar a máquina virtual no Azure:

Acesso ao Portal do Azure:

Realizei o login na minha conta do Azure através do portal web (https://www.google.com/search?q=https://portal.azure.com/).
Naveguei até o serviço de "Máquinas Virtuais".
Criação de uma Nova Máquina Virtual:

Cliquei no botão "+ Criar" e selecionei "Máquina virtual".
Preenchi as informações básicas da VM:
Grupo de recursos: Criei um novo grupo de recursos para organizar os recursos relacionados a esta VM (myVM).
Nome da máquina virtual: Escolhi um nome descritivo para a VM (myvm).
Região: Selecionei uma região geograficamente próxima (Australia East (Zone 1)).
Zona de disponibilidade: Mantive a opção padrão (sem redundância de zona para este laboratório).
Imagem: Escolhi uma imagem do sistema operacional (Windows (Windows Server 2019 Datacenter)).
Arquitetura: Mantive a arquitetura padrão x64.
Tamanho: Selecionei um tamanho de máquina virtual adequado para testes e aprendizado (Standard B1s (1 vcpu, 1 GiB memory)).
Configuração do Disco:

Mantive as configurações padrão para o disco do sistema operacional (disco gerenciado Premium SSD LRS).
Rede:

O Azure automaticamente criou uma rede virtual (dio-vm-vnet) e uma sub-rede (subnet-1).
Um endereço IP público foi automaticamente associado à VM para acesso externo.
Um Network Security Group (NSG) (dio-vm-nsg) foi criado para controlar o tráfego de entrada e saída.
Gerenciamento:

Mantive as configurações padrão para monitoramento e diagnóstico de inicialização.

Não realizei configurações avançadas específicas para este laboratório.

Adicionei uma etiqueta para facilitar a identificação do recurso (MyVM).

Revisar + criar:

Revisei todas as configurações e cliquei em "Criar" para provisionar a máquina virtual.
🔑 Acesso à Máquina Virtual
Após a criação da VM, realizei o acesso via SSH utilizando as seguintes informações:

Endereço IP Público: (20.11.1.195) Obtido na página de visão geral da máquina virtual no portal do Azure.
Nome de usuário: localhost\Azureuser.

utilizei o endereço: (https://learn.microsoft.com/pt-br/azure/virtual-machines/windows/quick-create-portal) para aprender mais sobre as ferramentas
e recursos.

📝 Anotações e Dicas
-Grupos de Recursos: A organização dos recursos em grupos de recursos é fundamental para o gerenciamento eficiente e controle de custos no Azure.
-Seleção da Região: Escolher a região correta pode impactar a latência e os custos dos serviços. Recomenda-se selecionar a região mais próxima dos usuários ou da infraestrutura existente.
-Tamanho da VM: A escolha do tamanho da VM deve ser baseada nos requisitos de desempenho e custo da aplicação ou carga de trabalho. Para testes e aprendizado, tamanhos menores como Standard_B1ls são geralmente suficientes.
-Network Security Groups (NSGs): Os NSGs são essenciais para a segurança da sua VM, permitindo controlar o tráfego de rede de entrada e saída. É importante configurar regras específicas para permitir apenas o tráfego necessário (ex: porta 22 para SSH, porta 80 para HTTP, porta 443 para HTTPS).
-Monitoramento: O Azure oferece diversas ferramentas de monitoramento para acompanhar o desempenho e a saúde da sua VM. 
-Custos: Esteja atento aos custos associados à execução da máquina virtual. Desligar a VM quando não estiver em uso pode ajudar a reduzir os custos.

🖼️ Capturas de Tela
 Uma pasta /images foi criada para armazenar capturas de tela relevantes do processo de criação e configuração da VM no portal do Azure. As imagens estão nomeadas de forma descritiva para facilitar a compreensão.

🎓 Conclusão
Este desafio proporcionou uma experiência prática valiosa na criação e configuração de uma máquina virtual no Azure. A documentação detalhada neste repositório reflete o processo realizado, as configurações importantes e as dicas relevantes para futuras implementações.
