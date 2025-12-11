# 📝 T20Web — Ficha de Personagem Tormenta20

Bem-vindo à página oficial do meu projeto de desenvolvimento de um **aplicativo web para ficha de personagem de Tormenta20 (T20)**. Esta iniciativa surgiu a partir da necessidade de **criar, editar e consultar fichas de personagem** de forma simples, rápida e acessível diretamente no navegador, **sem instalar programas**.

https://docs.google.com/spreadsheets/d/1KXuMJ9TK7GPyahR_BfLwfn4ec7vX7DgiHx42vFc4E7g/edit?gid=932601097#gid=932601097

---

## 🎯 Objetivo do Projeto

Desenvolver um **site de fichas T20** que permita:

* Criar, editar e visualizar fichas de personagem no navegador;
* **Salvar e carregar** dados usando armazenamento local (localStorage);
* **Exportar e importar** fichas em JSON (compatível entre navegadores);
* Oferecer layout simples, responsivo e usável em qualquer dispositivo.

---

## 🧩 Tecnologias Utilizadas

---

## ❗ Situação-Problema

* Jogadores muitas vezes **perdem fichas** ou mantêm versões desatualizadas (papel, imagens, planilhas dispersas);
* Dificuldade em **editar rapidamente** durante a sessão;
* Ausência de **padrão único** para guardar informações essenciais de T20.

---

## 💡 Solução Proposta

Uma **aplicação web** centralizada, responsiva e leve que:

* Organiza os **campos essenciais** da ficha de T20 (dados básicos, atributos, perícias, poderes, magias, inventário, anotações);
* **Valida campos** obrigatórios e tipos (número/texto);
* **Salva automaticamente** (autosave) no navegador e permite **exportar/importar** JSON;
* Oferece **limpar ficha** (reset) para começar uma nova rapidamente;
* (Opcional futuro) **Exportar para PDF** e **impressão**.

---

## 🛠️ Funcionalidades Previstas

* **Criar/Editar Ficha:** Formulários para dados básicos e seções de T20;
* **Carregar Ficha:** Restaura dados salvos no navegador;
* **Exportar/Importar JSON:** Levar a ficha para outro navegador ou compartilhar;
* **Nova Ficha (Reset):** Limpa todos os campos com confirmação;
* **Autosave (opcional):** Salva mudanças a cada edição;
* **Validações mínimas:** Campos obrigatórios (Nome, Nível, Classe, Raça) e numéricos;
* **Acessibilidade básica:** Navegação por teclado e rótulos claros.

---

## 👥 Equipe de Desenvolvimento

* **Luiz Miguel Lima de Souza** — [GitHub: LMSLima](https://github.com/LMSLima)

👨‍🏫 **Professor orientador:** **Marco André Mendes** — [GitHub: marrcandre](https://github.com/marrcandre)

---

## 🔗 Links Importantes

* 📄 Documentação do Projeto: # [https://github.com/T20Web]
* 🎨 Repositório Frontend: # [[https://github.com/T20Web/Frontend](https://github.com/T20Web/Frontend-T20Web)]
* ⚙️ Repositório Backend: # [[https://github.com/T20Web/Backend](https://github.com/LMSLima/Backend-T20Web)]
* 🌐 Deploy-Frontend: # [[https://frontend-t20-web-flge.vercel.app/](https://frontend-t20-web-flge.vercel.app/)]
* 🌐 Deploy-Backend: # [[https://backend-t20web-lnil.onrender.com/](https://backend-t20web-lnil.onrender.com/)]

---

## 📬 Contato

* E-mail: **[lmiguells095@gmail.com](mailto:lmiguells095@gmail.com)**

---

## 📘 Especificação do Projeto — **T20Web**

### 📌 Regras de Negócio

1. O sistema deve manter **pelo menos uma ficha ativa** no navegador (por padrão “Ficha Padrão”).
2. Campos **obrigatórios:** Nome, Raça, Classe, Nível (≥1), Tendência (opcional), Jogador.
3. Campos numéricos devem aceitar **apenas números inteiros** onde aplicável (ex.: Nível).
4. **Atributos base:** Força, Destreza, Constituição, Inteligência, Sabedoria, Carisma.
5. **Modificadores de atributo** podem ser calculados automaticamente (opcional) com base nas regras de T20.
6. O usuário pode **exportar** a ficha em JSON e **importar** para continuar em outro navegador.
7. A ação **“Nova Ficha”** limpa todos os campos após **confirmação** do usuário.
8. Caso exista autosave, os dados podem ser gravados **a cada alteração** ou ao sair da página.
9. A aplicação **não exige autenticação** (para simplificar o escopo e focar nos requisitos básicos do TCC).
10. O sistema deve manter **compatibilidade entre versões** de exportação (JSON inclui versão do schema).

---

### ✅ Requisitos Funcionais

#### 🧾 Núcleo da Ficha

* **RF01:** O sistema deve permitir **preencher** dados básicos da ficha (Nome, Raça, Classe, Nível, Jogador).
* **RF02:** O sistema deve permitir **editar/atualizar** todas as informações da ficha.
* **RF03:** O sistema deve permitir **salvar** os dados no navegador via `localStorage`.
* **RF04:** O sistema deve permitir **carregar** a ficha salva no navegador.
* **RF05:** O sistema deve permitir **apagar/limpar** todos os dados para criar uma **nova ficha**, com confirmação.

#### 🧠 Atributos e Seções Essenciais

* **RF06:** O sistema deve oferecer campos para **Atributos** (For, Des, Con, Int, Sab, Car) e (opcional) **modificadores**.
* **RF07:** O sistema deve oferecer campos para **Perícias** e **Proficências**.
* **RF08:** O sistema deve oferecer campos para **Poderes/Habilidades de Classe**.
* **RF09:** O sistema deve oferecer campos para **Magias** (se aplicável) e **Pontos de Mana** (PM).
* **RF10:** O sistema deve oferecer campos para **Pontos de Vida** (PV), **Defesa**, **Deslocamento** e **Resistências** (livre).
* **RF11:** O sistema deve oferecer campos para **Equipamentos/Inventário** e **Anotações**.

#### 💾 Persistência e Portabilidade

* **RF12:** O sistema deve permitir **exportar** a ficha em **arquivo JSON**.
* **RF13:** O sistema deve permitir **importar** uma ficha a partir de **arquivo JSON** válido.

#### 🧭 Usabilidade

* **RF14:** O sistema deve oferecer **feedback** (mensagens de sucesso/erro) para salvar, carregar, exportar, importar e limpar ficha.
* **RF15:** O sistema deve **validar** campos obrigatórios e impedir salvar/exportar quando faltarem dados críticos.

---

### 🚫 Requisitos Não Funcionais

#### 🔒 Segurança

* **RNF01:** Não armazenar senhas; dados limitam-se às fichas. (Sem autenticação.)
* **RNF02:** Sanitizar entradas para evitar XSS ao exibir texto salvo.
* **RNF03:** Ao importar JSON, validar o **schema** e rejeitar conteúdo inválido.

#### 📱 Usabilidade e Acessibilidade

* **RNF04:** Interface **responsiva** e funcional em dispositivos móveis e desktop.
* **RNF05:** Navegação por **teclado** e rótulos/descrições (ARIA) nas principais entradas.
* **RNF06:** Interface **simples e organizada**, com seções claras (abas ou acordes).

#### ⚙️ Performance

* **RNF07:** A página inicial deve carregar em **< 2s** em rede 4G em dispositivo médio.
* **RNF08:** Operações de salvar/carregar local devem ocorrer em **tempo quase instantâneo** (<100ms para fichas típicas).

#### 🕒 Disponibilidade e Backup

* **RNF09:** Sem backend (offline-first); dados ficam **no dispositivo** do usuário.
* **RNF10:** O sistema deve permitir **exportar** JSON como forma de **backup** manual.

#### 📂 Documentação e Manutenção

* **RNF11:** Código comentado e README com instruções de build e uso (Vite + Vue).
* **RNF12:** Padrões de código (ESLint/Prettier) e organização de componentes.

---
