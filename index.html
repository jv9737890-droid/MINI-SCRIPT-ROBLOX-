<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Game Overlay — Painel de Controle</title>
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; font-family: 'Segoe UI', Arial, sans-serif; }
        body { background: transparent; overflow: hidden; height: 100vh; }

        /* ✅ TELA DE PERMISSÃO */
        #tela-permissao {
            position: fixed; top: 0; left: 0; width: 100%; height: 100%;
            background: linear-gradient(135deg, #1a1a2e, #16213e);
            display: flex; flex-direction: column; align-items: center; justify-content: center;
            z-index: 99999; color: white; padding: 30px;
        }
        #tela-permissao h1 { font-size: 28px; margin-bottom: 15px; color: #00d4ff; }
        #tela-permissao p { font-size: 16px; max-width: 400px; text-align: center; margin-bottom: 30px; color: #ccc; line-height: 1.6; }
        .btn-principal {
            padding: 15px 40px; font-size: 18px; background: linear-gradient(90deg, #00d4ff, #0099cc);
            color: white; border: none; border-radius: 10px; cursor: pointer; font-weight: bold;
            transition: transform 0.2s, box-shadow 0.2s; margin: 8px;
        }
        .btn-principal:hover { transform: scale(1.05); box-shadow: 0 0 20px #00d4ff80; }
        .btn-secundario {
            padding: 12px 30px; font-size: 16px; background: #333; color: white;
            border: none; border-radius: 8px; cursor: pointer;
        }

        /* ✅ BARRINHA FLUTUANTE */
        #barrinha {
            position: fixed; top: 15px; right: 15px;
            background: rgba(10, 15, 30, 0.9);
            border: 1px solid #00d4ff60; border-radius: 12px;
            padding: 10px 12px; z-index: 9999;
            min-width: 260px; box-shadow: 0 4px 20px rgba(0, 0, 0, 0.5);
            display: none; backdrop-filter: blur(10px);
        }
        .barra-topo { display: flex; justify-content: space-between; align-items: center; margin-bottom: 8px; }
        .barra-titulo { color: #00d4ff; font-weight: bold; font-size: 14px; }
        .btn-fechar {
            background: #ff475720; color: #ff6b81; border: none; width: 28px; height: 28px;
            border-radius: 50%; cursor: pointer; font-weight: bold; font-size: 16px;
            display: flex; align-items: center; justify-content: center;
        }
        .btn-fechar:hover { background: #ff4757; color: white; }

        /* ✅ INPUT DE COMANDOS */
        .comando-input {
            width: 100%; padding: 8px 10px; background: #0f1419; border: 1px solid #2a3a4a;
            border-radius: 6px; color: #00ff88; font-size: 13px; outline: none; margin-bottom: 8px;
        }
        .comando-input:focus { border-color: #00d4ff; }

        /* ✅ ÁREA DE MENSAGENS */
        .mensagens { max-height: 150px; overflow-y: auto; font-size: 12px; }
        .msg { padding: 4px 6px; margin-bottom: 3px; border-radius: 3px; }
        .msg-info { color: #74b8ff; background: #74b9ff15; }
        .msg-sucesso { color: #00ff88; background: #00ff8815; }
        .msg-aviso { color: #ffcc00; background: #ffcc0015; }
        .msg-erro { color: #ff6b6b; background: #ff6b6b15; }

        /* ✅ MENU DE COMANDOS */
        #menu-comandos {
            margin-top: 8px; padding-top: 8px; border-top: 1px solid #2a3a4a; display: none;
        }
        .cmd-item {
            padding: 5px 8px; color: #ccc; font-size: 12px; cursor: pointer; border-radius: 4px;
            margin-bottom: 2px;
        }
        .cmd-item:hover { background: #2a3a4a; color: white; }
        .cmd-desc { color: #888; font-size: 10px; margin-left: 8px; }

        /* ✅ BOTÕES RÁPIDOS */
        .botoes-rapidos { display: flex; gap: 6px; margin-top: 8px; flex-wrap: wrap; }
        .btn-rapido {
            padding: 5px 8px; font-size: 11px; border: none; border-radius: 4px;
            cursor: pointer; font-weight: 500;
        }
        .btn-sair { background: #ff475720; color: #ff6b81; }
        .btn-sair:hover { background: #ff4757; color: white; }
        .btn-jogadores { background: #00d4ff20; color: #00d4ff; }
        .btn-jogadores:hover { background: #00d4ff; color: #000; }
        .btn-ping { background: #00ff8820; color: #00ff88; }
        .btn-ping:hover { background: #00ff88; color: #000; }

        /* ✅ NOTIFICAÇÃO DE JOGADOR ENTRANDO */
        #notificacao {
            position: fixed; top: 80px; right: 15px;
            background: rgba(0, 30, 60, 0.9); border: 1px solid #00ff88;
            border-radius: 8px; padding: 12px 18px; color: white;
            z-index: 99999; display: none; animation: aparece 0.3s ease;
        }
        @keyframes aparece {
            from { transform: translateX(100%); opacity: 0; }
            to { transform: translateX(0); opacity: 1; }
        }
        .notif-nome { color: #00ff88; font-weight: bold; }
    </style>
</head>
<body>

<!-- ✅ TELA INICIAL — PERGUNTA SE PODE ATIVAR -->
<div id="tela-permissao">
    <h1>🎮 Game Overlay — Painel de Controle</h1>
    <p>Esse painel flutua sobre sua tela enquanto você joga. Funciona em qualquer jogo ou app.<br><br>
    <strong>Como usar:</strong><br>
    1. Clique em "Ativar Painel"<br>
    2. Compartilhe sua tela/jogo no navegador<br>
    3. A barrinha vai aparecer no canto da tela! ✅</p>
    <button class="btn-principal" onclick="ativarPainel()">✅ Ativar Painel na Tela</button>
    <button class="btn-secundario" onclick="document.body.style.opacity='0.5'">❌ Não, obrigado</button>
</div>

<!-- ✅ NOTIFICAÇÃO DE JOGADOR NOVO -->
<div id="notificacao">
    <span id="notif-texto">👋 Jogador <span class="notif-nome">[Nome]</span> entrou no servidor!</span>
</div>

<!-- ✅ A BARRINHA EM SI -->
<div id="barrinha">
    <div class="barra-topo">
        <span class="barra-titulo">🎮 Painel do Servidor</span>
        <button class="btn-fechar" onclick="sairDoJogo()">✕</button>
    </div>

    <input type="text" class="comando-input" id="campo-comando" placeholder="Digite um comando... (!ping, /cmds)" onkeydown="processarComando(event)">

    <div class="botoes-rapidos">
        <button class="btn-rapido btn-ping" onclick="enviarComando('!ping ALL')">📊 Ping/FPS</button>
        <button class="btn-rapido btn-jogadores" onclick="enviarComando('/cmds')">📋 Comandos</button>
        <button class="btn-rapido btn-sair" onclick="sairDoJogo()">🚪 Sair</button>
    </div>

    <div id="menu-comandos">
        <div class="cmd-item" onclick="enviarComando('!ping ALL')">
            !ping ALL <span class="cmd-desc">→ Mostra Ping e FPS de todos</span>
        </div>
        <div class="cmd-item" onclick="enviarComando('/cmds')">
            /cmds <span class="cmd-desc">→ Abre este menu</span>
        </div>
        <div class="cmd-item" onclick="simularJogadorEntrando()">
            /avisar <span class="cmd-desc">→ Simula aviso de jogador novo</span>
        </div>
        <div class="cmd-item" onclick="sairDoJogo()">
            /sair <span class="cmd-desc">→ Sai do jogo rapidamente</span>
        </div>
    </div>

    <div class="mensagens" id="area-mensagens"></div>
</div>

<script>
const jogadoresSimulados = [
    { nome: "Player_X", ping: 42, fps: 60 },
    { nome: "Caio_Gamer", ping: 67, fps: 52 },
    { nome: "BrunoPro", ping: 28, fps: 59 },
    { nome: "Lucas_XD", ping: 89, fps: 45 },
    { nome: "Você", ping: 15, fps: 60 }
];

// ✅ ATIVAR PAINEL
function ativarPainel() {
    document.getElementById('tela-permissao').style.display = 'none';
    document.getElementById('barrinha').style.display = 'block';
    adicionarMensagem('Sistema', '✅ Painel ativado com sucesso! Digite /cmds para ver os comandos.', 'sucesso');
    
    // Simula jogadores entrando de tempos em tempos
    setInterval(() => {
        if (Math.random() > 0.7) {
            const nomes = ['NovoJogador123', 'Gamer_X', 'Player_Novo', 'Jogador_99'];
            const nomeAleatorio = nomes[Math.floor(Math.random() * nomes.length)];
            mostrarNotificacao(nomeAleatorio);
        }
    }, 45000); // a cada 45s pode aparecer um jogador novo
}

// ✅ PROCESSAR COMANDOS
function processarComando(event) {
    if (event.key === 'Enter') {
        const entrada = document.getElementById('campo-comando');
        const comando = entrada.value.trim();
        if (!comando) return;
        
        adicionarMensagem('Você', `> ${comando}`, 'info');
        executarComando(comando);
        entrada.value = '';
    }
}

function enviarComando(cmd) {
    document.getElementById('campo-comando').value = cmd;
    executarComando(cmd);
}

function executarComando(cmd) {
    cmd = cmd.toLowerCase();
    
    if (cmd === '!ping all') {
        mostrarPingEFPS();
    }
    else if (cmd === '/cmds' || cmd === '/comandos') {
        const menu = document.getElementById('menu-comandos');
        menu.style.display = menu.style.display === 'block' ? 'none' : 'block';
        adicionarMensagem('Sistema', menu.style.display === 'block' ? '📋 Lista de comandos aberta!' : '📋 Lista fechada', 'info');
    }
    else if (cmd === '/sair' || cmd === '/leave') {
        sairDoJogo();
    }
    else if (cmd === '/avisar') {
        simularJogadorEntrando();
    }
    else {
        adicionarMensagem('Sistema', `Comando "${cmd}" não reconhecido. Use /cmds para ajuda.`, 'erro');
    }
}

// ✅ MOSTRAR PING E FPS DE TODOS
function mostrarPingEFPS() {
    adicionarMensagem('═══════════════════════', '', 'info');
    adicionarMensagem('📊 STATUS DOS JOGADORES', '', 'sucesso');
    jogadoresSimulados.forEach(j => {
        const corPing = j.ping < 50 ? '✅' : j.ping < 80 ? '⚠️' : '🔴';
        const corFps = j.fps >= 55 ? '✅' : j.fps >= 40 ? '⚠️' : '🔴';
        adicionarMensagem(j.nome, `${corPing} Ping: ${j.ping}ms | ${corFps} FPS: ${j.fps}`, 'info');
    });
    adicionarMensagem('═══════════════════════', '', 'info');
}

// ✅ NOTIFICAÇÃO DE JOGADOR NOVO
function mostrarNotificacao(nomeJogador) {
    const notif = document.getElementById('notificacao');
    document.querySelector('.notif-nome').textContent = nomeJogador;
    notif.style.display = 'block';
    
    adicionarMensagem('SERVIDOR', `👋 ${nomeJogador} entrou no servidor!`, 'aviso');
    
    setTimeout(() => {
        notif.style.display = 'none';
    }, 5000);
}

function simularJogadorEntrando() {
    const nomes = ['Miguel', 'Pedro_X', 'Ana_Play', 'JoaoGamer', 'Leticia'];
    mostrarNotificacao(nomes[Math.floor(Math.random() * nomes.length)]);
}

// ✅ SAIR DO JOGO — FECHAR PAINEL RÁPIDO
function sairDoJogo() {
    if (confirm('🚪 Tem certeza que deseja sair? Seu personagem será removido do servidor.')) {
        adicionarMensagem('Sistema', '👋 Saindo do jogo... Personagem removido!', 'aviso');
        document.getElementById('barrinha').style.display = 'none';
        document.getElementById('tela-permissao').style.display = 'flex';
    }
}

// ✅ ADICIONAR MENSAGENS NA TELA
function adicionarMensagem(autor, texto, tipo) {
    const area = document.getElementById('area-mensagens');
    const div = document.createElement('div');
    div.className = `msg msg-${tipo}`;
    div.innerHTML = autor ? `<strong>${autor}:</strong> ${texto}` : texto;
    area.appendChild(div);
    area.scrollTop = area.scrollHeight;
    
    // Limitar mensagens na tela
    while (area.children.length > 15) {
        area.removeChild(area.firstChild);
    }
}
</script>

</body>
</html>
