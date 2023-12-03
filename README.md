# Laboratório 

# Introduction to AWS CloudFormation
![image](https://github.com/SamiraCavalcanti/Introduction-to-AWS-CloudFormation-/assets/86758007/0f15d9ec-2dd3-474e-8ab7-912838b7273f)

O AWS CloudFormation permite modelar, provisionar e gerenciar recursos da AWS e de terceiros ao tratar a infraestrutura como código.
#

# Visão geral
Este laboratório apresenta o AWS CloudFormation. Você usará um modelo pré-configurado do CloudFormation que cria uma instância do Amazon       
EC2 e instala o WordPress com um banco de dados MySQL local para armazenamento. Depois, você excluirá a pilha para limpar os recursos.    
Ele oferece aos desenvolvedores e administradores de sistemas uma maneira fácil de criar e gerenciar um grupo de recursos relacionados à AWS,      
provisionando e atualizando-os de forma organizada e previsível      

# TÓPICOS ABORDADOS
Ao final do laboratório, você conseguirá:        

Criar uma pilha usando um modelo do AWS CloudFormation      
Monitorar o progresso da criação da pilha      
Explorar parâmetros, recursos e saídas do CloudFormation      
Usar os recursos da pilha      
Fazer a limpeza quando a pilha não for mais necessária     


# Tarefa 1: criar uma pilha do CloudFormation

![image](https://github.com/SamiraCavalcanti/Introduction-to-AWS-CloudFormation-/assets/86758007/919b5ed3-34f6-4bfa-93ea-39c215dbd87d)

# Tarefa 2: monitorar o CloudFormation

Na guia Templante nos mostra o conteúdo do modelo 

![image](https://github.com/SamiraCavalcanti/Introduction-to-AWS-CloudFormation-/assets/86758007/3cadbdeb-911d-4f15-b3d5-a55f8f230e1b)

#
A guia Parameters (Parâmetros) exibe os parâmetros e seus valores correspondentes que fazem parte do modelo.

![image](https://github.com/SamiraCavalcanti/Introduction-to-AWS-CloudFormation-/assets/86758007/6950c503-bd6f-463a-846e-50422e4125bb)
#
A guia Events (Eventos) exibe cada evento principal na criação da pilha classificado pela hora, com os eventos mais recentes no topo.        
Você pode ver eventos diferentes e os respectivos status, como CREATE_IN_PROGRESS ou CREATE_COMPLETE.    

![image](https://github.com/SamiraCavalcanti/Introduction-to-AWS-CloudFormation-/assets/86758007/887c074c-2fbc-445f-82db-e4a2241363c5)

#
A guia Resources (Recursos) exibe os recursos que fazem parte da pilha. 

![image](https://github.com/SamiraCavalcanti/Introduction-to-AWS-CloudFormation-/assets/86758007/5b88f299-8139-4160-8d8d-769ae8d33c29)


# Os seguintes recursos são definidos no modelo que  está sendo implantando.

WebServerSecurityGroup: um grupo de segurança que permite o acesso via porta 80 (HTTP).      
VPC: nuvem privada virtual usada para os outros recursos      
InternetGateway: um gateway para acessar a Internet      
AttachGateway: uma maneira de se conectar ao internet gateway      
PublicSubnet1: a primeira sub-rede pública      
PublicSubnet2: a segunda sub-rede pública      
PublicRouteTable: uma tabela das rotas da VPC      
PublicRoute: uma rota pública para a tabela de rotas      
PublicSubnet1RouteTableAssociation: uma maneira de associar a primeira sub-rede à tabela de rotas pública        
PublicSubnet2RouteTableAssociation: uma maneira de associar a segunda sub-rede à tabela de rotas pública        
WebServer: instância do Amazon EC2 criada como um servidor WordPress  


# ANALISAR AS SAÍDAS DO CLOUDFORMATION
Quando uma pilha é implantada, ela pode exibir informações de saída. Essa pilha contém um link para o site do WordPress.

![image](https://github.com/SamiraCavalcanti/Introduction-to-AWS-CloudFormation-/assets/86758007/a3ebd2bb-31e8-48b2-b09b-047f88355056)


# CONECTE-SE AO SEU SITE DO WORDPRESS USANDO UM NAVEGADOR DA WEB

Abri uma nova página no navegador e colei o link que a pilha implantou          


![image](https://github.com/SamiraCavalcanti/Introduction-to-AWS-CloudFormation-/assets/86758007/f04c112b-34f0-4878-b2c4-5cf20da2a927)

#
Depois de configurar o site foi instalado

![image](https://github.com/SamiraCavalcanti/Introduction-to-AWS-CloudFormation-/assets/86758007/9d62039b-bc2e-426d-aab7-7035c185c6fb)

#
Efetuando login

![image](https://github.com/SamiraCavalcanti/Introduction-to-AWS-CloudFormation-/assets/86758007/c806775c-003b-45b2-84e9-d2d5c82ff3f0)

#
Painel do WordPress que você pode criar publicações de blog para adicionar informações ao site

![image](https://github.com/SamiraCavalcanti/Introduction-to-AWS-CloudFormation-/assets/86758007/ae33666e-f070-46c5-a1bf-905e41bc400a)

# CONECTAR-SE À INSTÂNCIA DO EC2 VIA GERENCIADOR DE SESSÃO

Copiei e colei em uma nova guia do navegador o link que a pilha criou isso me conectou        
à instância do EC2 usada para a instalação do WordPress por meio do Gerenciador de sessão.        

![image](https://github.com/SamiraCavalcanti/Introduction-to-AWS-CloudFormation-/assets/86758007/6e68796b-ac94-46cd-9347-25f72defcca1)

#
Verificando os processos que estão sendo executados no sistema com o comando ps -ef

![image](https://github.com/SamiraCavalcanti/Introduction-to-AWS-CloudFormation-/assets/86758007/010eed5e-7652-47e9-8159-f9133a0c5207)


# Tarefa 3: excluir a pilha

Selecionando a pilha a ser excluída 

![image](https://github.com/SamiraCavalcanti/Introduction-to-AWS-CloudFormation-/assets/86758007/a126d08e-de86-4903-9867-e306e89da1b0)

#
Delete iniciado e em progresso

![image](https://github.com/SamiraCavalcanti/Introduction-to-AWS-CloudFormation-/assets/86758007/7aaacd72-471e-46c1-8c19-9e6afca859bb)


# Conclusão
Você realizou com êxito as seguintes tarefas:

Criou uma pilha usando um modelo do AWS CloudFormation      
Monitorou o progresso da criação de pilha      
Explorou parâmetros, recursos e saídas do CloudFormation      
Usou os recursos da pilha      
Limpou a pilha      



















