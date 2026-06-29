# Forms PWA — Solução de Quiosque para Coleta de Avaliações

## O problema

Um cliente com 4 polos de atendimento precisava coletar avaliações de satisfação dos usuários em tablets fixos. O desafio: sem nenhum tipo de bloqueio, qualquer pessoa conseguia sair do formulário, navegar pelo dispositivo e comprometer a operação.

A solução padrão seria contratar um MDM (Mobile Device Management) profissional — Scalefusion, Miradore ou similares. O orçamento não permitia.

## A solução

Criação de um PWA (Progressive Web App) que funciona como launcher do formulário Google Forms, instalado como aplicativo nativo nos tablets Android. Combinado com o **modo quiosque nativo do Android** (recurso já presente no sistema operacional, sem custo adicional), o dispositivo fica bloqueado e só permite acesso ao formulário.

**Como funciona:**
1. O PWA é instalado no tablet como aplicativo (ícone na tela inicial, sem barra de navegador)
2. Ao abrir, redireciona diretamente para o Google Forms do cliente
3. O modo quiosque do Android impede o usuário de sair do aplicativo ou acessar outras funções do dispositivo

## Resultado

- 4 polos operando com tablets bloqueados em produção
- Zero custo adicional de software
- Sem necessidade de contratação de MDM profissional

## Tecnologias

- HTML5
- PWA (manifest.json + service worker)
- Google Forms
- Android Kiosk Mode (nativo)

## Estrutura do repositório

```
forms-pwa/
├── index.html        # Página de entrada com redirecionamento para o Forms
├── manifest.json     # Configuração do PWA (ícone, nome, display standalone)
├── assets/           # Ícones do aplicativo
└── apk/              # APK gerado para instalação nos dispositivos
```

## Demo

🔗 [prometheussolucoes.github.io/forms-pwa](https://prometheussolucoes.github.io/forms-pwa/)

---

Desenvolvido por [Paschoal Colombini](https://www.linkedin.com/in/paschoal-colombini) para Prometheus Soluções e Inovações.
