# Projeto Banco de Dados

# Sistema de Adoção de Animais com Perfil Comportamental


> **Matéria:** Banco de Dados
> 
> **Nome:** Natasha Almeida Trindade
> 
> **RA:** 22123098-0  

---

## Contextualização
A adoção de animais é uma prática essencial para reduzir o número de cães e gatos abandonados nas ruas e em abrigos.  
No entanto, muitos processos de adoção falham por incompatibilidade entre o perfil do adotante e o comportamento do animal.  
Isso pode gerar devoluções, traumas e sobrecarga nos abrigos.  

Com o avanço da tecnologia e da ciência comportamental, é possível criar um sistema inteligente que auxilie na conexão entre adotantes e animais, considerando não apenas dados básicos, mas também perfis comportamentais, preferências e estilo de vida.

---

## Descrição do Problema
Atualmente, muitos abrigos utilizam métodos manuais ou simplificados para registrar animais e realizar adoções.  
Isso dificulta a personalização do processo e aumenta as chances de incompatibilidade.  

Além disso, não há um controle eficiente sobre:
- Histórico dos animais  
- Visitas  
- Entrevistas  
- Acompanhamento pós-adoção  

---

## Justificativa da Escolha
O tema foi escolhido por sua **relevância social, emocional e tecnológica**.  
A adoção responsável é um tema atual e urgente, e a proposta de um sistema que utilize dados comportamentais traz inovação e impacto positivo.

---

## Objetivos do Sistema
- Cadastrar animais com informações detalhadas, incluindo perfil comportamental  
- Cadastrar adotantes com preferências e estilo de vida  
- Realizar o **match** entre animais e adotantes com base em compatibilidade  
- Registrar visitas e entrevistas  
- Acompanhar o pós-adoção com feedbacks  
- Gerar estatísticas para os abrigos sobre adoções, devoluções e perfis mais comuns  

---

## Dicionário de Dados

### Entidades Principais
- **Animal**: id, nome, idade, espécie (gato ou cachorro), perfil comportamental (sociável, necessidade de cuidados extras), status (adotado ou disponível)  
- **Adotante**: id, nome, idade, endereço (rua, cidade, estado), estilo de vida, preferências (espécie e perfil comportamental do animal)  
- **Adoção**: id, data, status, feedback  
- **Abrigo**: nome, localização, capacidade, responsável  
- **Visita**: id, data  
- **Entrevista**: id, data, perguntas, respostas, resultado  

---

### Relacionamentos
- **Visita (Adotante — Animal)**:  
  Um adotante pode visitar vários animais.  
  Um animal pode receber visitas de vários adotantes.  
  **N:M**  

- **Entrevista (Adotante — Abrigo)**:  
  Um adotante pode ser entrevistado por vários abrigos.  
  Um abrigo pode entrevistar vários adotantes.  
  **N:M**  

- **Adoção (Adotante — Animal)**:  
  Um adotante pode adotar vários animais.  
  Mas cada animal só pode ser adotado uma vez.  
  **1:N**  

---

##  Exemplos e Cenários
- **Exemplo 1:**  
  Natasha, mora em apartamento e trabalha fora o dia todo, busca um animal calmo e independente.  
  O sistema sugere **Luna**, uma gata tranquila e sociável.  

- **Exemplo 2:**  
  Eduardo, que tem filhos pequenos, procura um cão brincalhão e paciente.  
  O sistema sugere **Thor**, um cão com alto nível de energia e bom histórico com crianças.  

---

## Exemplos de Operações Típicas
- Cadastrar novo animal com perfil comportamental  
- Registrar visita de um adotante a um animal  
- Realizar entrevista com o adotante  
- Gerar sugestão de animal com base no perfil do adotante  
- Registrar adoção e gerar relatório de feedback  
