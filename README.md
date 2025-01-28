# Guia de Instalação e Primeiros Passos no Pharo e Moose (Windows)

Este repositório contém um guia passo a passo para instalar o **Pharo** e o **Moose**, além de fornecer instruções para começar a analisar código Java utilizando o **VerveineJ**. O Moose é uma ferramenta poderosa para análise e visualização de sistemas de software, enquanto o Pharo é o ambiente de desenvolvimento onde o Moose é executado.

## Sumário

1. [Instalação do Pharo](#instalação-do-pharo)
2. [Configuração do VerveineJ para Análise de Código Java](#configuração-do-verveinej-para-análise-de-código-java)
3. [Importando e Analisando o Projeto no Moose](#importando-e-analisando-o-projeto-no-moose)
4. [Configurações Avançadas](#configurações-avançadas)
5. [Dicas e Boas Práticas](#dicas-e-boas-práticas)
6. [Conclusão](#conclusão)

---

## Instalação do Pharo

### 1. Baixe o Pharo Launcher
- Acesse o site oficial do Pharo: [https://pharo.org/download](https://pharo.org/download).
- Faça o download do **Pharo Launcher** para Windows.

### 2. Instale o Pharo Launcher
- Execute o instalador baixado e siga as instruções para instalar o Pharo Launcher.

### 3. Crie uma nova imagem do Moose
- Abra o Pharo Launcher.
- No canto superior direito, clique no ícone **"New"**.
- Na lista de imagens disponíveis, procure por **"Moose Suite 11 (stable)"**.
- Selecione a versão correspondente ao seu sistema (64 bits) e clique em **"Create"**.
- Aguarde o download e a criação da imagem.

### 4. Inicie a imagem do Moose
- Após a criação da imagem, ela aparecerá na lista de imagens no Pharo Launcher.
- Clique em **"Launch"** para iniciar a imagem do Moose.

---

## Configuração do VerveineJ para Análise de Código Java

O **VerveineJ** é uma ferramenta que extrai modelos **FAMIX** (um meta-modelo usado no Moose) a partir de código-fonte Java. Ele transforma o código em uma representação estruturada que pode ser analisada no Moose.

### 1. Clone o repositório do VerveineJ
- Abra o terminal (ou Git Bash) e execute o seguinte comando para clonar o repositório do VerveineJ:

  ```bash
  git clone https://github.com/NicolasAnquetil/VerveineJ

### 2. Instale o Java 17
- O VerveineJ requer Java 17 para funcionar. Caso não tenha o Java instalado:
- Baixe e instale o Java 17 a partir do site oficial da Oracle ou de uma distribuição OpenJDK.
- Configure a variável de ambiente JAVA_HOME para apontar para a instalação do Java 17.

### 3. Execute o VerveineJ
- Navegue até a pasta do VerveineJ clonado:
   ```bash
    cd VerveineJ 
- Execute o script verveinej.sh passando o caminho da pasta que contém o código Java que deseja analisar:
   ```bash
   ./verveinej.sh caminho/para/pasta/do/projeto
- Isso gerará um arquivo output.mse, que contém a representação do código no formato FAMIX.

---

## Importando e Analisando o Projeto no Moose

### 1. Abra o Moose
- Inicie a imagem do Moose no Pharo Launcher, como descrito na seção 1.

### 2. Importe o arquivo output.mse
- No Moose, vá até o "Models Browser" (canto superior esquerdo).
- Clique em "Select one file" e selecione o arquivo output.mse gerado pelo VerveineJ.

### 3. Selecione o modelo correto
- Para projetos Java, selecione "FamixJavaModel" no campo "File path".
- Clique em "Propagate" para carregar o modelo.

### 4. Navegue pelos dados
- Após a importação, clique em "Query Browser".
- Aqui você poderá visualizar a estrutura do projeto, aplicar filtros e segmentações.

### 5. Aplique consultas (queries)
- No Query Browser, use o botão "+" para criar consultas personalizadas.
- Por exemplo, selecione todas as classes do projeto e clique em "Propagate".
- Em seguida, vá até "Architecture Map" para visualizar um mapa arquitetural baseado nas classes do projeto.

---

## Configurações Avançadas

### 1. Conexões entre classes
- Navegue até "Settings" para acessar uma janela de configuração que permite criar conexões entre as classes do projeto.

### 2. Personalização
- O Moose é altamente personalizável. Explore as diversas ferramentas e visualizações disponíveis para adaptar a análise às suas necessidades.

---

## Dicas e Boas Práticas

- Mantenha o Java atualizado: Certifique-se de que o Java 17 está corretamente instalado e configurado.
- Explore a documentação oficial: Consulte a documentação do Moose e do Pharo para mais detalhes e funcionalidades avançadas.
- Experimente diferentes projetos: Teste o Moose com diferentes projetos Java para se familiarizar com as ferramentas e visualizações.

---

## Conclusão
Com este guia, você deve ser capaz de instalar o Pharo, configurar o Moose e começar a analisar projetos Java utilizando o VerveineJ. O Moose é uma ferramenta poderosa para engenharia de software, e explorar suas funcionalidades pode trazer insights valiosos sobre a estrutura e qualidade do código.

Se tiver dúvidas ou precisar de mais ajuda, sinta-se à vontade para consultar a comunidade Pharo ou Moose, ou entrar em contato com outros desenvolvedores que utilizam essas ferramentas.
