![Rust](https://img.shields.io/badge/language-Rust-orange)
![C++](https://img.shields.io/badge/language-C++-blue)
![Go](https://img.shields.io/badge/language-Go-00ADD8)
![Python](https://img.shields.io/badge/language-Python-3776AB)
​

![Dashboard Preview]([imagem.png](https://github.com/Viscke/The-Blackwall-XDR-Extended-Detection-and-Response-/blob/main/image.png)

O projeto é fragmentado em módulos especializados, utilizando a melhor linguagem para cada domínio crítico:
​Core Engine (Rust): O "Cérebro" do sistema. Gerencia a memória de forma segura e utiliza a API de monitoramento nativa do Windows para detecção de alterações em nanossegundos.
​Guardian Module (C++): A lâmina do sistema. Interage diretamente com o Kernel do Windows (Win32 API) para terminação forçada de processos e injeção de regras de Firewall.
​Network Intelligence (Go): O radar. Gerencia múltiplos Honeypots simultâneos e integra-se com feeds de inteligência global (AlienVault OTX) via processamento assíncrono (Goroutines).
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
