# 🔁 Fluxo de Automação - Lyra Oráculo da Noite

Este documento descreve o fluxo de automação mensal usado para enviar tiragens personalizadas de Lyra.

---

## 📥 1. Captura de dados
- Ferramenta: Google Forms
- Campos: Nome, Data de nascimento, E-mail, WhatsApp, Tema da tiragem

Os dados são enviados automaticamente para uma planilha no **Google Sheets**.

---

## 🔗 2. Integração com Zapier (ou Make/Integromat)
- Disparo programado: entre os dias 1 e 3 de cada mês
- Verifica planilha e seleciona novos usuários ou todos cadastrados
- Constrói a pergunta para IA baseada nos dados da planilha

**Exemplo de prompt automatizado enviado à IA:**
> Crie uma tiragem mística para o mês de Junho para Júlia, nascida em 04/06/1996, com foco em espiritualidade.

---

## ✨ 3. Consulta à IA (via API OpenAI ou GPTs)
- Resposta é gerada com base no prompt + exemplos da Lyra
- Estilo: poético, simbólico, sensível, com ritual ao final

---

## 📤 4. Envio da mensagem
- Canal: WhatsApp Business (via Twilio ou 360dialog) ou e-mail (Gmail via Zapier)
- Texto enviado com formatação e imagem opcional

---

## 🕰 5. Programação
- A automação roda 1x por mês (recomenda-se dia 2)
- Permite reenvio caso falhe

---

## 🗂 6. Armazenamento dos envios
- Planilha registra status do envio (✔ enviado / ❌ falhou)
- Pode gerar histórico de mensagens por usuário

---

## 🧪 Próximos passos:
- Criar webhook se desejar personalizar ainda mais
- Adicionar variações de prompt por tema (amor, trabalho, etc.)
- Integrar IA com banco de imagens rituais
