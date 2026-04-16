# 🛡️ The Blackwall XDR (Extended Detection and Response)

> **Sistema de monitorização de endpoints de próxima geração com arquitetura poliglota e análise forense assistida por IA.**

![Rust](https://img.shields.io/badge/language-Rust-orange) ![C++](https://img.shields.io/badge/language-C++-blue) ![Go](https://img.shields.io/badge/language-Go-00ADD8) ![Python](https://img.shields.io/badge/language-Python-3776AB) ![License](https://img.shields.io/badge/license-MIT-green)

A **Blackwall XDR** é uma solução avançada de cibersegurança desenvolvida para detetar, isolar e analisar ameaças em tempo real. Utilizando uma abordagem de micro-serviços integrados, o sistema combina a performance de linguagens de baixo nível com a inteligência de modelos de linguagem de última geração.

---

## 📸 Interface do Sistema
![Dashboard Preview](imagem.png)
*Visualização do Painel de Controlo Operacional (Interface Estilo Cyberpunk/Arasaka).*

---

## 🏗️ Arquitetura do Ecossistema

O projeto é dividido em módulos especializados, cada um utilizando a stack tecnológica mais eficiente para a sua função:

### 🧠 Core Engine (Rust)
O sistema nervoso central. Responsável pela monitorização de memória e ficheiros críticos.
- **Função:** Detecção de I/O anómalo e proteção de *Honeytokens*.
- **Vantagem:** Segurança de memória nativa e latência zero.

### 🗡️ Guardian Module (C++)
A ferramenta de execução e resposta rápida do sistema.
- **Função:** Interação com a Win32 API para finalização forçada de processos (Kill PID) e bloqueio de IPs no Firewall nativo.
- **Vantagem:** Acesso direto ao Kernel do Windows.

### 📡 Network Intelligence (Go)
O módulo de inteligência de rede e radar.
- **Função:** Gestão de Honeypots ativos e integração com a API AlienVault OTX para verificação de reputação de IPs.
- **Vantagem:** Alta concorrência com *Goroutines* para monitorização múltipla.

### 🤖 AI Analyst (Python)
O perito forense automatizado.
- **Função:** Integração com o Google Gemini para converter logs técnicos em relatórios forenses detalhados.
- **Vantagem:** Consciência contextual sobre a anatomia do ataque.

---

## 🚀 Funcionalidades Principais

1. **Defesa Ativa contra Ransomware:** Monitorização de ficheiros isca que, ao serem tocados, disparam o bloqueio imediato do processo agressor.
2. **Rede de Decepção (Honeypots):** Criação de portas falsas no sistema para capturar scanners e movimentos laterais de invasores.
3. **Análise Forense em Tempo Real:** Relatórios gerados por IA que explicam o que aconteceu, o risco envolvido e como prevenir futuras ocorrências.
4. **Dashboard de Telemetria:** Interface tática para monitorização de saúde do sistema e eventos de segurança.

---

## 🛠️ Como Executar (Ambiente de Desenvolvimento)

### Pré-requisitos
- Rust (Cargo)
- Go 1.22+
- Python 3.10+ (com `google-genai`)
- Compilador C++ (MSVC/MinGW)


​AI Analyst (Python/Gemini): A consciência. Processa logs brutos e gera relatórios forenses detalhados em linguagem natural utilizando modelos de linguagem avançados.
​Command Dashboard (Tauri/React): A interface. Um console operacional nativo de baixo consumo, oferecendo telemetria tática e controle total sobre o endpoint.


​1. Detecção Ativa de Ransomware (Sentinela)
​Implementação de Honeytokens (arquivos isca) monitorados diretamente pelo Kernel. Qualquer tentativa de leitura, modificação ou remoção por processos não autorizados dispara o protocolo de contenção imediata.
​
2. Defesa de Rede e Movimentação Lateral
​Honeypots Invisíveis: Abertura de portas sintéticas (ex: 4455, 2222) para capturar scanners de rede e worms.
​Geo-Fencing & IP Reputation: Bloqueio automático de conexões baseadas em reputação global e localização geográfica.
​
3. Telemetria Tática (Osquery Style)
​Capacidade de consultar o estado do sistema operacional (processos, portas abertas, consumo de hardware) como dados estruturados, permitindo uma visibilidade clara sobre a saúde do endpoint.
​
4. Resposta de Incidência Assistida (AI-Driven)
​Integração com a API do Google Gemini para transformar logs técnicos em relatórios legíveis, explicando a anatomia do ataque e sugerindo medidas de remediação.
​
Diferenciais Técnicos

​Zero CPU Idle: O uso de eventos nativos do SO elimina a necessidade de loops de verificação constantes.
​Anti-Tampering: Mecanismos de proteção que impedem que o próprio malware finalize o processo do EDR.
​Pegada de Memória Reduzida: Arquitetura otimizada para rodar em segundo plano sem impactar a performance do usuário final.
​Nota de Isenção de Responsabilidade: Este projeto foi desenvolvido para fins educacionais e de pesquisa em cibersegurança em ambientes controlados (Laboratórios/VMs). O uso indevido de ferramentas de segurança pode causar instabilidade no sistema.
