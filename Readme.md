# Course_k8s
Repositório dos Exercicios e Atividades do curso de kubernetes

Introdução
----------------

Este hands-on é um guia prático que tem como objetivo introduzir você ao Kubernetes, uma das ferramentas mais populares e poderosas para orquestração de containers. Aqui, você aprenderá passo a passo como criar e gerenciar um cluster Kubernetes no Azure, criar e escalar deployments, daemonsets e statefulsets, configurar um ingress controller com certificado TLS, e muito mais.

Você começará instalando o Azure CLI, criando um cluster AKS no Azure e configurando o Kubeconfig para acessar o cluster. Em seguida, você aprenderá sobre os conceitos básicos do Kubernetes, como o que é um pod e como criar um pod em YAML.

Depois disso, você aprenderá sobre o conceito de service, e como criar um service em YAML. Também discutiremos a diferença entre os tipos de serviços NodePort, ClusterIP e Load Balancer.

Em seguida, você aprenderá sobre o deployment, um objeto do Kubernetes que gerencia um conjunto de réplicas de pods. Você criará um deployment em YAML e aprenderá a configurar a escalabilidade do seu aplicativo.

Além disso, exploraremos o conceito de daemonset e statefulset, que permitem que você execute um conjunto de pods em cada nó do seu cluster, e que os pods tenham um identificador persistente, respectivamente.

Também veremos como criar e gerenciar ConfigMaps e Secrets, objetos que permitem que você armazene e gerencie dados sensíveis e configurações em seu cluster.

Por fim, você aprenderá a instalar e configurar o ingress controller nginx-ingress com o Helm e aplicar um certificado TLS usando o cert-manager.

Este hands-on é destinado a iniciantes no Kubernetes e pressupõe que você tenha conhecimento básico de containers e do ambiente de linha de comando. Se você está procurando uma introdução prática e completa ao Kubernetes, este guia é uma excelente maneira de começar.

Pré-requisitos
------------------

 Antes de começar este hands-on, você precisará ter alguns pré-requisitos instalados e configurados em seu ambiente. Aqui estão os requisitos:

1. Conhecimento básico de containers e do ambiente de linha de comando
2. Uma conta do Azure
3. O Azure CLI instalado em sua máquina. Você pode instalar o Azure CLI seguindo as instruções em https://docs.microsoft.com/en-us/cli/azure/install-azure-cli
4. Um editor de texto, como o Visual Studio Code, instalado em sua máquina
5. O kubectl, a ferramenta de linha de comando do Kubernetes, instalado em sua máquina. Você pode instalar o kubectl seguindo as instruções em https://kubernetes.io/docs/tasks/tools/install-kubectl/
6. O Helm, o gerenciador de pacotes do Kubernetes, instalado em sua máquina. Você pode instalar o Helm seguindo as instruções em https://helm.sh/docs/intro/install/

Certifique-se de ter todas essas ferramentas instaladas e configuradas corretamente antes de começar o hands-on.

Sobre Kubernetes
-------------------

Kubernetes é uma plataforma de orquestração de contêineres open source, projetada para automatizar a implantação, escalabilidade e gerenciamento de aplicativos em contêineres. Ele foi desenvolvido pelo Google e agora é mantido pela Cloud Native Computing Foundation (CNCF).

Com o Kubernetes, você pode implantar e gerenciar facilmente aplicativos contêinerizados em um ambiente de cluster, tornando mais fácil a orquestração de recursos e a gerência de infraestruturas de TI modernas.

Kubernetes é altamente escalável, permitindo que você gerencie clusters com milhares de nós e centenas de milhares de contêineres. Ele também é altamente configurável e personalizável, permitindo que você ajuste o sistema para atender às suas necessidades específicas.

Kubernetes usa um modelo declarativo para gerenciar a infraestrutura, permitindo que você defina o estado desejado do sistema em um arquivo YAML ou JSON e, em seguida, use o Kubernetes para aplicar essa definição ao ambiente de cluster. Isso torna mais fácil a implantação e gerenciamento de aplicativos, além de garantir que o estado do sistema seja consistente e previsível.

Em resumo, o Kubernetes é uma ferramenta poderosa e altamente flexível para orquestração de contêineres, que permite que você gerencie facilmente aplicativos em um ambiente de cluster, aumente a disponibilidade e a escalabilidade, além de garantir que o sistema esteja sempre em um estado consistente e previsível.

Criar um AKS no Azure:
-----------------------

1. Faça login no portal do Azure.
2. Crie um novo grupo de recursos.
3. Clique em "Criar um recurso".
4. Procure "AKS" e clique em "Criar".
5. Preencha as informações necessárias e clique em "Revisar e criar".
6. Clique em "Criar" para criar o cluster AKS.
