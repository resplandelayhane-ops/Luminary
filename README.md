```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Luminary Studio AI — O Estúdio Definitivo para Escritores</title>
    <!-- Tailwind CSS para Estilização Premium -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        absblack: '#050505',
                        charcoal: '#111111',
                        coal: '#181818',
                        graphite: '#222222',
                        goldold: '#c5a880',
                        goldbright: '#f4e3b1',
                        bronze: '#a3753f',
                        creme: '#fefcf9',
                        cremeclaro: '#f4ede2'
                    },
                    fontFamily: {
                        cinzel: ['"Cinzel"', 'serif'],
                        cinzeldec: ['"Cinzel Decorative"', 'serif'],
                        crimson: ['"Crimson Pro"', 'serif'],
                        inter: ['"Inter"', 'sans-serif']
                    }
                }
            }
        }
    </script>
    <!-- Google Fonts Premium -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel+Decorative:wght@400;700&family=Cinzel:wght@400;600;700&family=Crimson+Pro:ital,wght@0,300;0,400;0,600;1,400&family=Inter:wght@300;400;500;600&display=swap" rel="stylesheet">
    <!-- Lucide Icons para Interface -->
    <script src="https://unpkg.com/lucide@latest"></script>
    <style>
        body {
            background-color: #050505;
            color: #f4ede2;
            font-family: 'Inter', sans-serif;
            overflow-x: hidden;
        }
        .text-glow {
            text-shadow: 0 0 12px rgba(197, 168, 128, 0.45);
        }
        .gold-border {
            border-image: linear-gradient(to right, #a3753f, #c5a880, #a3753f) 1;
        }
        .scrollbar-premium::-webkit-scrollbar {
            width: 6px;
            height: 6px;
        }
        .scrollbar-premium::-webkit-scrollbar-track {
            background: #111111;
        }
        .scrollbar-premium::-webkit-scrollbar-thumb {
            background: #c5a880;
            border-radius: 4px;
        }
        #ambient-canvas {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: 0;
            pointer-events: none;
            opacity: 0.45;
        }
        .interactive-panel {
            background: rgba(17, 17, 17, 0.88);
            backdrop-filter: blur(14px);
            border: 1px solid rgba(197, 168, 128, 0.15);
            transition: all 0.4s cubic-bezier(0.16, 1, 0.3, 1);
        }
        .interactive-panel:hover {
            border-color: rgba(197, 168, 128, 0.4);
            box-shadow: 0 12px 36px rgba(0, 0, 0, 0.65);
        }
        input[type="range"] {
            -webkit-appearance: none;
            background: #222222;
            height: 5px;
            border-radius: 3px;
        }
        input[type="range"]::-webkit-slider-thumb {
            -webkit-appearance: none;
            height: 16px;
            width: 16px;
            border-radius: 50%;
            background: #c5a880;
            cursor: pointer;
            box-shadow: 0 0 10px #c5a880;
        }
    </style>
</head>
<body class="scrollbar-premium">

    <!-- Canvas de Efeitos Atmosféricos -->
    <canvas id="ambient-canvas"></canvas>

    <!-- Notificações Customizadas Premium -->
    <div id="custom-notification" class="hidden fixed top-6 right-6 z-50 max-w-sm bg-charcoal border border-goldold p-4 rounded-sm shadow-2xl flex items-start space-x-3 transition-all duration-500 transform translate-y-2">
        <div class="p-1 bg-goldold/10 rounded-full">
            <i id="notif-icon" data-lucide="sparkles" class="w-5 h-5 text-goldbright"></i>
        </div>
        <div class="flex-1">
            <h5 id="notif-title" class="font-cinzel text-xs text-goldold tracking-wider">Aviso da Biblioteca</h5>
            <p id="notif-desc" class="text-xs text-cremeclaro/80 mt-1">Sua ação foi executada com êxito.</p>
        </div>
        <button onclick="fecharNotificacao()" class="text-cremeclaro/40 hover:text-cremeclaro">
            <i data-lucide="x" class="w-3.5 h-3.5"></i>
        </button>
    </div>

    <!-- ==================== LANDING PAGE CINEMATOGRÁFICA ==================== -->
    <section id="landing-page" class="relative z-10 min-h-screen flex flex-col justify-between items-center px-6 py-12 transition-all duration-1000 ease-in-out">
        <div></div>
        
        <div class="text-center max-w-4xl space-y-8">
            <div class="flex items-center justify-center space-x-4">
                <div class="h-[1px] w-20 bg-gradient-to-r from-transparent to-goldold"></div>
                <i data-lucide="scroll" class="w-5 h-5 text-goldold"></i>
                <div class="h-[1px] w-20 bg-gradient-to-l from-transparent to-goldold"></div>
            </div>

            <h1 class="font-cinzeldec text-5xl md:text-7xl lg:text-8xl tracking-widest text-glow bg-gradient-to-b from-creme via-goldold to-bronze bg-clip-text text-transparent">
                LUMINARY
            </h1>
            <p class="font-cinzel text-xl md:text-2xl tracking-widest text-goldold opacity-95 uppercase">
                Studio AI
            </p>
            
            <p class="font-crimson italic text-lg md:text-2xl text-cremeclaro/80 max-w-2xl mx-auto leading-relaxed">
                "Não geramos apenas histórias simples. Forjamos universos inteiros para escritores imortalizarem suas maiores sagas."
            </p>

            <div class="flex justify-center my-6">
                <div class="w-40 h-[1px] bg-gradient-to-r from-transparent via-goldold to-transparent"></div>
            </div>

            <button onclick="entrarNoUniverso()" class="group relative px-10 py-5 bg-charcoal border border-goldold/50 hover:border-goldold transition-all duration-500 overflow-hidden rounded-sm">
                <span class="absolute inset-0 w-full h-full bg-gradient-to-r from-bronze/10 to-goldold/10 transform scale-x-0 group-hover:scale-x-100 transition-transform duration-500 origin-left"></span>
                <span class="relative font-cinzel text-sm tracking-widest text-creme group-hover:text-goldbright flex items-center gap-3">
                    ENTRAR NO TEMPLO <i data-lucide="compass" class="w-4 h-4 text-goldold group-hover:rotate-45 transition-transform duration-500"></i>
                </span>
            </button>
        </div>

        <div class="text-center space-y-2 opacity-60">
            <p class="font-inter text-xs tracking-widest text-goldold/70">O TEMPLO DIGITAL DA ALTA LITERATURA</p>
            <div class="text-[10px] text-creme/40">Versão 3.5 Pro • Estúdio Literário Inteligente</div>
        </div>
    </section>

    <!-- ==================== ECOSSISTEMA PRINCIPAL DO SOFTWARE ==================== -->
    <main id="app-container" class="hidden relative z-10 min-h-screen flex flex-col bg-absblack transition-all duration-1000 ease-in-out">
        
        <!-- CABEÇALHO FIXO PREMIUM -->
        <header class="sticky top-0 z-50 h-16 bg-charcoal/95 backdrop-blur-md border-b border-goldold/15 flex items-center justify-between px-6">
            <div class="flex items-center space-x-3">
                <div class="w-8 h-8 rounded-full border border-goldold/40 flex items-center justify-center bg-absblack">
                    <span class="font-cinzel text-sm text-goldold">L</span>
                </div>
                <div>
                    <h2 class="font-cinzel text-sm tracking-wider text-creme">LUMINARY STUDIO</h2>
                    <p class="text-[9px] text-goldold/60 tracking-widest uppercase">Estúdio Profissional</p>
                </div>
            </div>

            <!-- Configurações e Chave de API no Cabeçalho (Pode ser adicionada quando o site for para o ar) -->
            <div class="hidden lg:flex items-center space-x-6">
                <div class="flex items-center space-x-2 bg-coal border border-goldold/15 rounded-sm px-3 py-1.5">
                    <i data-lucide="key" class="w-3.5 h-3.5 text-goldold"></i>
                    <input type="password" id="gemini-api-key" placeholder="Sua Chave Gemini API..." onchange="salvarChaveAPI(this.value)" class="bg-transparent text-[11px] text-creme placeholder-creme/30 focus:outline-none w-44">
                </div>

                <div class="flex items-center space-x-2 bg-coal border border-goldold/15 rounded-sm px-2.5 py-1.5 text-xs text-creme">
                    <i data-lucide="cpu" class="w-3.5 h-3.5 text-goldold"></i>
                    <select id="gemini-model-select" class="bg-transparent focus:outline-none cursor-pointer">
                        <option value="gemini-2.5-flash-preview-09-2025" class="bg-charcoal text-creme">Gemini 2.5 Flash</option>
                        <option value="gemini-2.5-pro-preview" class="bg-charcoal text-creme">Gemini 2.5 Pro (Criativo)</option>
                    </select>
                </div>
            </div>

            <div class="flex items-center space-x-4">
                <button onclick="salvarObraAtual()" class="flex items-center space-x-1 px-3 py-1.5 border border-goldold/30 hover:border-goldold bg-coal/50 text-xs text-goldold rounded-sm transition-all">
                    <i data-lucide="save" class="w-3.5 h-3.5"></i>
                    <span class="hidden sm:inline">Salvar Obra</span>
                </button>
                
                <div class="px-3 py-1 bg-goldold/10 border border-goldold/20 text-xs text-goldbright rounded-sm font-cinzel">
                    Ativa: <span id="active-work-indicator">Nenhuma</span>
                </div>
            </div>
        </header>

        <!-- CONTAINER DO MENU E CONTEÚDOS -->
        <div class="flex-1 flex overflow-hidden">
            
            <!-- MENU LATERAL RETRÁTIL -->
            <aside id="sidebar-menu" class="w-16 hover:w-64 md:w-64 flex flex-col justify-between border-r border-goldold/15 bg-charcoal/40 backdrop-blur-md transition-all duration-300 z-30 group">
                <div class="p-3 space-y-4">
                    <div class="hidden group-hover:flex md:flex flex-col p-3 bg-coal/60 rounded-sm border border-goldold/10 space-y-2">
                        <span class="text-[9px] text-goldold tracking-widest uppercase">Manuscrito Ativo</span>
                        <h4 id="menu-work-title" class="font-cinzel text-xs text-creme truncate">Selecione uma Obra</h4>
                        <div class="w-full bg-absblack h-1 rounded-full overflow-hidden">
                            <div id="menu-work-progress" class="bg-goldold h-full" style="width: 0%"></div>
                        </div>
                    </div>

                    <!-- Botões de Navegação -->
                    <nav class="space-y-1">
                        <button onclick="navegarPara('biblioteca-obras')" class="nav-btn w-full flex items-center space-x-3 p-3 hover:bg-goldold/10 text-cremeclaro/70 hover:text-goldbright rounded-sm transition-all">
                            <i data-lucide="book-open" class="w-5 h-5 text-goldold"></i>
                            <span class="text-sm font-inter tracking-wide hidden group-hover:inline md:inline">Biblioteca de Obras</span>
                        </button>
                        
                        <button onclick="navegarPara('dashboard')" class="nav-btn w-full flex items-center space-x-3 p-3 hover:bg-goldold/10 text-cremeclaro/70 hover:text-goldbright rounded-sm transition-all">
                            <i data-lucide="layout-dashboard" class="w-5 h-5 text-goldold"></i>
                            <span class="text-sm font-inter tracking-wide hidden group-hover:inline md:inline">Painel de Controle</span>
                        </button>

                        <button onclick="navegarPara('forjador-sagas')" class="nav-btn w-full flex items-center space-x-3 p-3 hover:bg-goldold/10 text-cremeclaro/70 hover:text-goldbright rounded-sm transition-all">
                            <i data-lucide="map" class="w-5 h-5 text-goldold"></i>
                            <span class="text-sm font-inter tracking-wide hidden group-hover:inline md:inline">Forjador de Sagas</span>
                        </button>

                        <button onclick="navegarPara('editor-capitulos')" class="nav-btn w-full flex items-center space-x-3 p-3 hover:bg-goldold/10 text-cremeclaro/70 hover:text-goldbright rounded-sm transition-all">
                            <i data-lucide="feather" class="w-5 h-5 text-goldold"></i>
                            <span class="text-sm font-inter tracking-wide hidden group-hover:inline md:inline">Gerador & Editor</span>
                        </button>

                        <button onclick="navegarPara('worldbuilding')" class="nav-btn w-full flex items-center space-x-3 p-3 hover:bg-goldold/10 text-cremeclaro/70 hover:text-goldbright rounded-sm transition-all">
                            <i data-lucide="globe" class="w-5 h-5 text-goldold"></i>
                            <span class="text-sm font-inter tracking-wide hidden group-hover:inline md:inline">Worldbuilding</span>
                        </button>

                        <button onclick="navegarPara('personagens')" class="nav-btn w-full flex items-center space-x-3 p-3 hover:bg-goldold/10 text-cremeclaro/70 hover:text-goldbright rounded-sm transition-all">
                            <i data-lucide="users" class="w-5 h-5 text-goldold"></i>
                            <span class="text-sm font-inter tracking-wide hidden group-hover:inline md:inline">Personagens</span>
                        </button>
                    </nav>
                </div>

                <div class="p-4 border-t border-goldold/10">
                    <div class="flex items-center space-x-3 text-xs text-goldold/60" id="key-indicator">
                        <i data-lucide="shield-alert" class="w-5 h-5 text-yellow-600"></i>
                        <span class="hidden group-hover:inline md:inline">Sem Chave API</span>
                    </div>
                </div>
            </aside>

            <!-- CONTEÚDOS DAS ABAS -->
            <section class="flex-1 overflow-y-auto scrollbar-premium p-4 md:p-6 relative">
                
                <!-- ==================== TELA 1: BIBLIOTECA DE OBRAS ==================== -->
                <div id="view-biblioteca-obras" class="view-panel space-y-6">
                    <div class="flex flex-col md:flex-row md:items-center justify-between gap-4 border-b border-goldold/15 pb-4">
                        <div>
                            <h3 class="font-cinzel text-2xl text-creme">Biblioteca de Universos</h3>
                            <p class="text-xs text-goldold/80">Estantes contendo suas obras completas e independentes.</p>
                        </div>
                        <button onclick="abrirModalNovaObra()" class="flex items-center space-x-2 bg-gradient-to-r from-bronze to-goldold text-absblack font-bold text-xs px-5 py-3 rounded-sm hover:opacity-90 transition-all">
                            <i data-lucide="plus" class="w-4 h-4"></i>
                            <span>Nova Obra (Criar Universo)</span>
                        </button>
                    </div>

                    <div id="grid-obras" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
                        <!-- Gerado Dinamicamente -->
                    </div>
                </div>

                <!-- ==================== TELA 2: PAINEL DE CONTROLE (DASHBOARD) ==================== -->
                <div id="view-dashboard" class="view-panel hidden space-y-6">
                    <div class="flex items-center justify-between border-b border-goldold/15 pb-4">
                        <div>
                            <h3 id="dash-title" class="font-cinzel text-2xl text-creme">Nenhuma Obra Ativa</h3>
                            <p id="dash-subtitle" class="text-xs text-goldold/80">Crie ou selecione uma obra na Biblioteca para começar.</p>
                        </div>
                    </div>

                    <div class="grid grid-cols-2 md:grid-cols-4 gap-4">
                        <div class="interactive-panel p-4 rounded-sm">
                            <span class="text-xs text-goldold/60">Capítulos</span>
                            <h4 id="dash-capitulos-count" class="font-cinzel text-3xl text-creme text-glow mt-1">0</h4>
                        </div>
                        <div class="interactive-panel p-4 rounded-sm">
                            <span class="text-xs text-goldold/60">Palavras</span>
                            <h4 id="dash-palavras-count" class="font-cinzel text-3xl text-creme text-glow mt-1">0</h4>
                        </div>
                        <div class="interactive-panel p-4 rounded-sm">
                            <span class="text-xs text-goldold/60">Personagens</span>
                            <h4 id="dash-personagens-count" class="font-cinzel text-3xl text-creme text-glow mt-1">0</h4>
                        </div>
                        <div class="interactive-panel p-4 rounded-sm">
                            <span class="text-xs text-goldold/60">Regiões/Itens</span>
                            <h4 id="dash-locais-count" class="font-cinzel text-3xl text-creme text-glow mt-1">0</h4>
                        </div>
                    </div>

                    <div class="grid grid-cols-1 lg:grid-cols-3 gap-6">
                        <div class="interactive-panel p-5 rounded-sm lg:col-span-2 space-y-4">
                            <h4 class="font-cinzel text-sm text-goldold tracking-wider">Forças Motrizes do Manuscrito</h4>
                            <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                                <div class="bg-coal/55 p-4 border border-goldold/10 rounded-sm">
                                    <span class="text-[10px] text-goldold tracking-widest uppercase">Protagonista I</span>
                                    <h5 id="dash-protagonist-1" class="font-cinzel text-sm text-creme mt-1">Não Definido</h5>
                                </div>
                                <div class="bg-coal/55 p-4 border border-goldold/10 rounded-sm">
                                    <span class="text-[10px] text-goldold tracking-widest uppercase">Protagonista II / Rival</span>
                                    <h5 id="dash-protagonist-2" class="font-cinzel text-sm text-creme mt-1">Não Definido</h5>
                                </div>
                            </div>
                            <div class="p-3 bg-coal/30 border border-goldold/5 rounded text-xs text-cremeclaro/70">
                                <strong>Sinopse Primordial:</strong>
                                <p id="dash-sinopse" class="mt-1 italic"></p>
                            </div>
                        </div>

                        <div class="interactive-panel p-5 rounded-sm space-y-4">
                            <h4 class="font-cinzel text-sm text-goldold tracking-wider">Ações de Forja</h4>
                            <div class="space-y-2">
                                <button onclick="navegarPara('editor-capitulos')" class="w-full py-2.5 bg-goldold/10 hover:bg-goldold/20 border border-goldold/20 text-xs text-goldbright rounded transition-all text-left px-3 flex justify-between items-center">
                                    <span>Escrever/Gerar Novo Capítulo</span>
                                    <i data-lucide="chevron-right" class="w-4 h-4"></i>
                                </button>
                                <button onclick="navegarPara('personagens')" class="w-full py-2.5 bg-goldold/10 hover:bg-goldold/20 border border-goldold/20 text-xs text-goldbright rounded transition-all text-left px-3 flex justify-between items-center">
                                    <span>Cadastrar Personagem</span>
                                    <i data-lucide="chevron-right" class="w-4 h-4"></i>
                                </button>
                                <button onclick="navegarPara('worldbuilding')" class="w-full py-2.5 bg-goldold/10 hover:bg-goldold/20 border border-goldold/20 text-xs text-goldbright rounded transition-all text-left px-3 flex justify-between items-center">
                                    <span>Adicionar Worldbuilding</span>
                                    <i data-lucide="chevron-right" class="w-4 h-4"></i>
                                </button>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- ==================== TELA 3: FORJADOR DE SAGAS ==================== -->
                <div id="view-forjador-sagas" class="view-panel hidden space-y-6">
                    <div class="border-b border-goldold/15 pb-4">
                        <h3 class="font-cinzel text-2xl text-creme">Forjador de Sagas</h3>
                        <p class="text-xs text-goldold/80">Planeje arcos narrativos complexos usando inteligência artificial de ponta.</p>
                    </div>

                    <div class="grid grid-cols-1 lg:grid-cols-3 gap-6">
                        <div class="interactive-panel p-5 rounded-sm space-y-4 h-fit">
                            <h4 class="font-cinzel text-sm text-goldold tracking-wider">Diretrizes da Saga</h4>
                            
                            <div class="space-y-3">
                                <div>
                                    <label class="block text-[10px] uppercase text-goldold/70 mb-1">Tom Dramático</label>
                                    <select id="saga-tom" class="w-full bg-coal border border-goldold/20 rounded p-2 text-xs text-creme focus:outline-none focus:border-goldold">
                                        <option value="Sombrio, melancólico e cruel (Dark Fantasy)">Sombrio, melancólico e cruel</option>
                                        <option value="Épico, heroico e de alta magia (High Fantasy)">Épico, heroico e alta magia</option>
                                        <option value="Poético, reflexivo e focado em dilemas morais">Poético e reflexivo</option>
                                        <option value="Rápido, frenético e cheio de reviravoltas">Frenético e ágil</option>
                                    </select>
                                </div>

                                <div>
                                    <label class="block text-[10px] uppercase text-goldold/70 mb-1">Foco Principal deste Arco</label>
                                    <textarea id="saga-diretriz" rows="4" placeholder="Ex: O exército de cinzas marcha em direção à muralha de obsidiana..." class="w-full bg-coal border border-goldold/20 rounded p-2 text-xs text-creme focus:outline-none focus:border-goldold resize-none"></textarea>
                                </div>

                                <div>
                                    <label class="block text-[10px] uppercase text-goldold/70 mb-1">Número de Capítulos a Estruturar</label>
                                    <input type="number" id="saga-capitulos-num" min="1" max="10" value="3" class="w-full bg-coal border border-goldold/20 rounded p-2 text-xs text-creme focus:outline-none focus:border-goldold">
                                </div>

                                <button onclick="gerarEsqueletoSaga()" class="w-full py-3 bg-gradient-to-r from-bronze to-goldold text-absblack font-bold text-xs rounded-sm hover:opacity-90 transition-all flex items-center justify-center space-x-2">
                                    <i data-lucide="sparkles" class="w-4 h-4"></i>
                                    <span>Forjar Esqueleto Narrativo</span>
                                </button>
                            </div>
                        </div>

                        <div class="interactive-panel p-5 rounded-sm lg:col-span-2 space-y-4">
                            <div class="flex items-center justify-between">
                                <h4 class="font-cinzel text-sm text-goldold tracking-wider">Esboço Narrativo Inteligente</h4>
                                <button onclick="importarSagaComoCapitulos()" class="text-xs text-goldbright hover:underline flex items-center space-x-1">
                                    <i data-lucide="download" class="w-3 h-3"></i>
                                    <span>Importar para Meus Capítulos</span>
                                </button>
                            </div>

                            <div id="saga-output" class="bg-coal/40 border border-goldold/10 rounded p-4 text-xs leading-relaxed text-cremeclaro/95 max-h-[500px] overflow-y-auto scrollbar-premium whitespace-pre-wrap">
                                O plano da sua saga aparecerá aqui após a forja com o Gemini AI.
                            </div>
                        </div>
                    </div>
                </div>

                <!-- ==================== TELA 4: GERADOR E EDITOR DE CAPÍTULOS (TABELADO MOBILE) ==================== -->
                <div id="view-editor-capitulos" class="view-panel hidden space-y-4">
                    <div class="border-b border-goldold/15 pb-3 flex flex-col md:flex-row md:items-center justify-between gap-4">
                        <div>
                            <h3 class="font-cinzel text-2xl text-creme">Gerador & Editor</h3>
                            <p class="text-xs text-goldold/80">Crie, planeje de forma coerente e escreva sem distrações.</p>
                        </div>
                        <div class="flex items-center space-x-2">
                            <button onclick="salvarCapituloManual()" class="px-4 py-2.5 bg-charcoal border border-goldold text-goldold hover:bg-goldold/10 text-xs rounded transition-all flex items-center space-x-1.5">
                                <i data-lucide="save" class="w-4 h-4"></i>
                                <span>Salvar Versão</span>
                            </button>
                        </div>
                    </div>

                    <!-- Seletor de Abas de Visibilidade para Telas Pequenas (Mobile) -->
                    <div class="flex lg:hidden border-b border-goldold/10 w-full mb-2">
                        <button id="tab-btn-config" onclick="toggleMobileEditorTab('config')" class="flex-1 py-3 text-center font-cinzel text-xs tracking-widest text-goldbright border-b-2 border-goldold">
                            Ajustes do Capítulo
                        </button>
                        <button id="tab-btn-manuscrito" onclick="toggleMobileEditorTab('manuscrito')" class="flex-1 py-3 text-center font-cinzel text-xs tracking-widest text-cremeclaro/40 border-b-2 border-transparent">
                            Escrever & Ler
                        </button>
                    </div>

                    <div class="grid grid-cols-1 lg:grid-cols-12 gap-6">
                        
                        <!-- Lado A: Configurar Capítulo (Ocultável no celular) -->
                        <div id="editor-col-config" class="interactive-panel p-5 rounded-sm lg:col-span-4 space-y-4 h-fit block">
                            <h4 class="font-cinzel text-sm text-goldold tracking-wider">Configurar Capítulo</h4>
                            
                            <div class="space-y-4">
                                <div>
                                    <label class="block text-[10px] uppercase text-goldold/70 mb-1">Capítulo Ativo</label>
                                    <div class="flex space-x-2">
                                        <select id="editor-capitulo-select" onchange="carregarCapituloSelecionado()" class="flex-1 bg-coal border border-goldold/20 rounded p-2 text-xs text-creme focus:outline-none focus:border-goldold">
                                            <option value="">Novo Capítulo (Defina abaixo)...</option>
                                        </select>
                                        <button onclick="limparCamposCapitulo()" class="p-2 bg-coal border border-goldold/20 hover:border-goldold rounded text-goldold text-xs" title="Novo Capítulo">
                                            <i data-lucide="plus" class="w-4 h-4"></i>
                                        </button>
                                    </div>
                                </div>

                                <div class="grid grid-cols-3 gap-2">
                                    <div class="col-span-1">
                                        <label class="block text-[10px] uppercase text-goldold/70 mb-1">Número</label>
                                        <input type="number" id="chapter-number" placeholder="Ex: 1" class="w-full bg-coal border border-goldold/20 rounded p-2 text-xs text-creme focus:outline-none focus:border-goldold">
                                    </div>
                                    <div class="col-span-2">
                                        <label class="block text-[10px] uppercase text-goldold/70 mb-1">Título do Capítulo</label>
                                        <input type="text" id="chapter-title" placeholder="Título..." class="w-full bg-coal border border-goldold/20 rounded p-2 text-xs text-creme focus:outline-none focus:border-goldold">
                                    </div>
                                </div>

                                <!-- SELETOR DE PONTO DE VISTA (POV) REESTRUTURADO CONFORME REQUISITOS -->
                                <div>
                                    <label class="block text-[10px] uppercase text-goldold/70 mb-1">Ponto de Vista (POV) Ativo</label>
                                    <select id="chapter-pov-select" class="w-full bg-coal border border-goldold/20 rounded p-2 text-xs text-creme focus:outline-none focus:border-goldold">
                                        <!-- Preenchido dinamicamente no JS com Protagonista 1, 2, Alternado e Coadjuvantes -->
                                    </select>
                                </div>

                                <div>
                                    <div class="flex justify-between text-[10px] uppercase text-goldold/70 mb-1">
                                        <span>Quantidade de Palavras</span>
                                        <span id="label-range-words" class="text-goldbright">1000 Palavras</span>
                                    </div>
                                    <input type="range" id="chapter-word-range" min="300" max="3000" step="100" value="1000" oninput="document.getElementById('label-range-words').innerText = this.value + ' Palavras'" class="w-full">
                                </div>

                                <div>
                                    <label class="block text-[10px] uppercase text-goldold/70 mb-1">O que acontece neste capítulo?</label>
                                    <textarea id="chapter-guidelines" rows="3" placeholder="Insira diretrizes, lutas, revelações ou diálogos importantes..." class="w-full bg-coal border border-goldold/20 rounded p-2 text-xs text-creme focus:outline-none focus:border-goldold resize-none"></textarea>
                                </div>

                                <button onclick="gerarTextoCapitulo()" class="w-full py-3 bg-gradient-to-r from-bronze to-goldold text-absblack font-bold text-xs rounded-sm hover:opacity-90 transition-all flex items-center justify-center space-x-2">
                                    <i data-lucide="feather" class="w-4 h-4"></i>
                                    <span>Escrever com Gemini AI</span>
                                </button>
                            </div>
                        </div>

                        <!-- Lado B: Editor Principal (Ocupará toda a tela no mobile se selecionado) -->
                        <div id="editor-col-manuscrito" class="interactive-panel p-5 rounded-sm lg:col-span-8 space-y-4 flex flex-col h-[50vh] lg:h-[75vh] hidden lg:flex">
                            <div class="flex items-center justify-between border-b border-goldold/10 pb-2">
                                <h4 class="font-cinzel text-sm text-goldold tracking-wider">Manuscrito em Produção</h4>
                                <div class="text-[10px] text-cremeclaro/50 flex space-x-4">
                                    <span>Palavras Atuais: <strong id="chapter-real-word-count" class="text-goldold">0</strong></span>
                                </div>
                            </div>

                            <!-- O Editor agora ocupa todo o espaço vertical disponível -->
                            <textarea id="manuscript-editor" placeholder="Sua história começa a ser forjada aqui..." class="flex-1 w-full bg-coal/20 border border-goldold/10 rounded p-4 text-sm md:text-base leading-relaxed text-cremeclaro/95 font-crimson focus:outline-none focus:border-goldold/40 resize-none scrollbar-premium"></textarea>
                        </div>

                    </div>
                </div>

                <!-- ==================== TELA 5: WORLDBUILDING ==================== -->
                <div id="view-worldbuilding" class="view-panel hidden space-y-6">
                    <div class="border-b border-goldold/15 pb-4 flex flex-col md:flex-row md:items-center justify-between gap-4">
                        <div>
                            <h3 class="font-cinzel text-2xl text-creme">Enciclopédia de Worldbuilding</h3>
                            <p class="text-xs text-goldold/80">Crie, detalhe e catalogue os reinos, facções, leis de magia e segredos de seu mundo.</p>
                        </div>
                        <button onclick="abrirModalLocal()" class="flex items-center space-x-2 bg-gradient-to-r from-bronze to-goldold text-absblack font-bold text-xs px-4 py-2 rounded-sm hover:opacity-90 transition-all">
                            <i data-lucide="plus" class="w-4 h-4"></i>
                            <span>Adicionar Elemento/Local</span>
                        </button>
                    </div>

                    <div id="list-worldbuilding" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
                        <!-- Gerado Dinamicamente -->
                    </div>
                </div>

                <!-- ==================== TELA 6: GERENCIAMENTO DE PERSONAGENS ==================== -->
                <div id="view-personagens" class="view-panel hidden space-y-6">
                    <div class="border-b border-goldold/15 pb-4 flex flex-col md:flex-row md:items-center justify-between gap-4">
                        <div>
                            <h3 class="font-cinzel text-2xl text-creme">Bíblia de Personagens</h3>
                            <p class="text-xs text-goldold/80">Monitore as ambições, medos, fraquezas e as aparências físicas e psicológicas do seu elenco.</p>
                        </div>
                        <button onclick="abrirModalPersonagem()" class="flex items-center space-x-2 bg-gradient-to-r from-bronze to-goldold text-absblack font-bold text-xs px-4 py-2 rounded-sm hover:opacity-90 transition-all">
                            <i data-lucide="plus" class="w-4 h-4"></i>
                            <span>Adicionar Personagem</span>
                        </button>
                    </div>

                    <div id="list-personagens" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
                        <!-- Gerado Dinamicamente -->
                    </div>
                </div>

            </section>
        </div>
    </main>

    <!-- ==================== MODAIS DE CRIAÇÃO E CONFIGURAÇÃO ==================== -->

    <!-- Modal Nova Obra -->
    <div id="modal-nova-obra" class="hidden fixed inset-0 z-50 bg-absblack/90 flex items-center justify-center p-4 backdrop-blur-sm">
        <div class="w-full max-w-lg bg-charcoal border border-goldold p-6 rounded shadow-2xl space-y-4">
            <h4 class="font-cinzel text-base text-goldold tracking-wider">Forjar Nova Saga</h4>
            
            <div class="space-y-3">
                <div>
                    <label class="block text-[10px] uppercase text-goldold/70 mb-1">Título da Obra</label>
                    <input type="text" id="new-work-title" placeholder="Ex: Crônicas de Obsidiana" class="w-full bg-coal border border-goldold/20 rounded p-2.5 text-xs text-creme focus:outline-none focus:border-goldold">
                </div>
                <div>
                    <label class="block text-[10px] uppercase text-goldold/70 mb-1">Gênero Literário</label>
                    <select id="new-work-genre" class="w-full bg-coal border border-goldold/20 rounded p-2.5 text-xs text-creme focus:outline-none focus:border-goldold">
                        <option value="Fantasia Épica">Fantasia Épica / Alta Fantasia</option>
                        <option value="Ficção Científica Space Opera">Ficção Científica / Space Opera</option>
                        <option value="Romance Histórico">Romance Histórico</option>
                        <option value="Suspense Psicológico">Suspense / Thriller</option>
                    </select>
                </div>
                <div class="grid grid-cols-2 gap-3">
                    <div>
                        <label class="block text-[10px] uppercase text-goldold/70 mb-1">Primeiro Protagonista</label>
                        <input type="text" id="new-work-p1" placeholder="Ex: Kaelen, o Sem-Nome" class="w-full bg-coal border border-goldold/20 rounded p-2.5 text-xs text-creme focus:outline-none focus:border-goldold">
                    </div>
                    <div>
                        <label class="block text-[10px] uppercase text-goldold/70 mb-1">Segundo Protagonista / Rival</label>
                        <input type="text" id="new-work-p2" placeholder="Ex: Rainha Lyra" class="w-full bg-coal border border-goldold/20 rounded p-2.5 text-xs text-creme focus:outline-none focus:border-goldold">
                    </div>
                </div>
                <div>
                    <label class="block text-[10px] uppercase text-goldold/70 mb-1">Sinopse Primordial</label>
                    <textarea id="new-work-synopsis" rows="3" placeholder="Insira o conflito central que impulsiona o universo..." class="w-full bg-coal border border-goldold/20 rounded p-2.5 text-xs text-creme focus:outline-none focus:border-goldold resize-none"></textarea>
                </div>
            </div>

            <div class="flex justify-end space-x-3 pt-3">
                <button onclick="fecharModalNovaObra()" class="px-4 py-2 bg-coal border border-goldold/20 text-xs text-cremeclaro/60 rounded hover:bg-coal/80">Cancelar</button>
                <button onclick="salvarNovaObra()" class="px-5 py-2 bg-gradient-to-r from-bronze to-goldold text-absblack font-bold text-xs rounded hover:opacity-90">Forjar Universo</button>
            </div>
        </div>
    </div>

    <!-- Modal Novo Personagem -->
    <div id="modal-personagem" class="hidden fixed inset-0 z-50 bg-absblack/90 flex items-center justify-center p-4 backdrop-blur-sm">
        <div class="w-full max-w-lg bg-charcoal border border-goldold p-6 rounded shadow-2xl space-y-4">
            <h4 class="font-cinzel text-base text-goldold tracking-wider">Adicionar Personagem Coadjuvante/Aliado</h4>
            
            <div class="space-y-3">
                <div class="grid grid-cols-2 gap-3">
                    <div>
                        <label class="block text-[10px] uppercase text-goldold/70 mb-1">Nome Completo</label>
                        <input type="text" id="char-name" placeholder="Ex: Lorde Kaelen" class="w-full bg-coal border border-goldold/20 rounded p-2.5 text-xs text-creme focus:outline-none focus:border-goldold">
                    </div>
                    <div>
                        <label class="block text-[10px] uppercase text-goldold/70 mb-1">Função / Alinhamento</label>
                        <input type="text" id="char-role" placeholder="Ex: Guardião das Cinzas" class="w-full bg-coal border border-goldold/20 rounded p-2.5 text-xs text-creme focus:outline-none focus:border-goldold">
                    </div>
                </div>
                <div>
                    <label class="block text-[10px] uppercase text-goldold/70 mb-1">Aparência Física & Estilo</label>
                    <textarea id="char-physical" rows="2" placeholder="Cicatrizes, vestimentas, marcas..." class="w-full bg-coal border border-goldold/20 rounded p-2.5 text-xs text-creme focus:outline-none focus:border-goldold resize-none"></textarea>
                </div>
                <div>
                    <label class="block text-[10px] uppercase text-goldold/70 mb-1">Motivação & Segredo</label>
                    <textarea id="char-drive" rows="2" placeholder="O maior conflito interno dele..." class="w-full bg-coal border border-goldold/20 rounded p-2.5 text-xs text-creme focus:outline-none focus:border-goldold resize-none"></textarea>
                </div>
            </div>

            <div class="flex justify-end space-x-3 pt-3">
                <button onclick="fecharModalPersonagem()" class="px-4 py-2 bg-coal border border-goldold/20 text-xs text-cremeclaro/60 rounded hover:bg-coal/80">Cancelar</button>
                <button onclick="salvarPersonagem()" class="px-5 py-2 bg-gradient-to-r from-bronze to-goldold text-absblack font-bold text-xs rounded hover:opacity-90">Inscrever na Bíblia</button>
            </div>
        </div>
    </div>

    <!-- Modal Novo Local/Elemento Worldbuilding -->
    <div id="modal-local" class="hidden fixed inset-0 z-50 bg-absblack/90 flex items-center justify-center p-4 backdrop-blur-sm">
        <div class="w-full max-w-lg bg-charcoal border border-goldold p-6 rounded shadow-2xl space-y-4">
            <h4 class="font-cinzel text-base text-goldold tracking-wider">Adicionar Elemento à Mitologia</h4>
            
            <div class="space-y-3">
                <div class="grid grid-cols-2 gap-3">
                    <div>
                        <label class="block text-[10px] uppercase text-goldold/70 mb-1">Nome do Local ou Conceito</label>
                        <input type="text" id="world-name" placeholder="Ex: Império de Tharis" class="w-full bg-coal border border-goldold/20 rounded p-2.5 text-xs text-creme focus:outline-none focus:border-goldold">
                    </div>
                    <div>
                        <label class="block text-[10px] uppercase text-goldold/70 mb-1">Categoria</label>
                        <select id="world-category" class="w-full bg-coal border border-goldold/20 rounded p-2.5 text-xs text-creme focus:outline-none focus:border-goldold">
                            <option value="Reino/Cultura">Reino, Nação ou Cultura</option>
                            <option value="Geografia">Geografia Natural/Muralhas</option>
                            <option value="Sistema de Magia">Sistema de Magia / Leis Físicas</option>
                            <option value="Facção/Clã">Facção / Organização Secreta</option>
                        </select>
                    </div>
                </div>
                <div>
                    <label class="block text-[10px] uppercase text-goldold/70 mb-1">Descrição Detalhada & Clima</label>
                    <textarea id="world-description" rows="4" placeholder="Detalhes geográficos, crenças, leis..." class="w-full bg-coal border border-goldold/20 rounded p-2.5 text-xs text-creme focus:outline-none focus:border-goldold resize-none"></textarea>
                </div>
            </div>

            <div class="flex justify-end space-x-3 pt-3">
                <button onclick="fecharModalLocal()" class="px-4 py-2 bg-coal border border-goldold/20 text-xs text-cremeclaro/60 rounded hover:bg-coal/80">Cancelar</button>
                <button onclick="salvarLocal()" class="px-5 py-2 bg-gradient-to-r from-bronze to-goldold text-absblack font-bold text-xs rounded hover:opacity-90">Consolidar Conceito</button>
            </div>
        </div>
    </div>

    <!-- ==================== LÓGICA JAVASCRIPT DE ALTO NÍVEL ==================== -->
    <script>
        let APP_STATE = {
            apiKey: '',
            selectedModel: 'gemini-2.5-flash-preview-09-2025',
            activeWorkId: null,
            obras: []
        };

        function inicializarEstado() {
            const salvo = localStorage.getItem('LUMINARY_PRO_STATE');
            if (salvo) {
                try {
                    APP_STATE = JSON.parse(salvo);
                } catch(e) {
                    console.error("Erro ao carregar dados salvos.", e);
                }
            }
            
            document.getElementById('gemini-api-key').value = APP_STATE.apiKey || '';
            document.getElementById('gemini-model-select').value = APP_STATE.selectedModel || 'gemini-2.5-flash-preview-09-2025';
            
            atualizarIndicadorChave();
            renderizarEstanteObras();
            
            if (APP_STATE.activeWorkId) {
                selecionarObra(APP_STATE.activeWorkId);
            }
        }

        function salvarEstado() {
            localStorage.setItem('LUMINARY_PRO_STATE', JSON.stringify(APP_STATE));
        }

        function salvarChaveAPI(valor) {
            APP_STATE.apiKey = valor;
            salvarEstado();
            atualizarIndicadorChave();
            mostrarNotificacao("Chave Registrada", "Sua API Key foi configurada com sucesso para gerações.");
        }

        function atualizarIndicadorChave() {
            const indicator = document.getElementById('key-indicator');
            if (APP_STATE.apiKey && APP_STATE.apiKey.trim() !== '') {
                indicator.innerHTML = `
                    <i data-lucide="shield-check" class="w-5 h-5 text-green-600"></i>
                    <span class="hidden group-hover:inline md:inline text-green-600">Chave Pronta</span>
                `;
            } else {
                indicator.innerHTML = `
                    <i data-lucide="shield-alert" class="w-5 h-5 text-yellow-600"></i>
                    <span class="hidden group-hover:inline md:inline text-yellow-600">Sem Chave API</span>
                `;
            }
            lucide.createIcons();
        }

        function entrarNoUniverso() {
            document.getElementById('landing-page').classList.add('hidden');
            document.getElementById('app-container').classList.remove('hidden');
            lucide.createIcons();
            navegarPara('biblioteca-obras');
        }

        function navegarPara(tabId) {
            document.querySelectorAll('.view-panel').forEach(panel => {
                panel.classList.add('hidden');
            });
            const targetPanel = document.getElementById(`view-${tabId}`);
            if (targetPanel) {
                targetPanel.classList.remove('hidden');
            }

            document.querySelectorAll('.nav-btn').forEach(btn => {
                btn.classList.remove('bg-goldold/10', 'text-goldbright');
            });

            if (tabId === 'editor-capitulos') {
                atualizarSeletoresEDiretrizes();
            }
        }

        // CONTROLADOR DE ABAS MOBILE PARA O EDITOR DE CAPÍTULOS (EVITA TEXTAREA PEQUENA)
        function toggleMobileEditorTab(aba) {
            const colConfig = document.getElementById('editor-col-config');
            const colManuscrito = document.getElementById('editor-col-manuscrito');
            const btnConfig = document.getElementById('tab-btn-config');
            const btnManuscrito = document.getElementById('tab-btn-manuscrito');

            if (aba === 'config') {
                colConfig.classList.remove('hidden');
                colConfig.classList.add('block');
                colManuscrito.classList.add('hidden');
                colManuscrito.classList.remove('flex');
                
                btnConfig.classList.add('text-goldbright', 'border-goldold');
                btnConfig.classList.remove('text-cremeclaro/40', 'border-transparent');
                btnManuscrito.classList.add('text-cremeclaro/40', 'border-transparent');
                btnManuscrito.classList.remove('text-goldbright', 'border-goldold');
            } else {
                colConfig.classList.add('hidden');
                colConfig.classList.remove('block');
                colManuscrito.classList.remove('hidden');
                colManuscrito.classList.add('flex');
                
                btnManuscrito.classList.add('text-goldbright', 'border-goldold');
                btnManuscrito.classList.remove('text-cremeclaro/40', 'border-transparent');
                btnConfig.classList.add('text-cremeclaro/40', 'border-transparent');
                btnConfig.classList.remove('text-goldbright', 'border-goldold');
            }
        }

        function mostrarNotificacao(titulo, desc) {
            const notif = document.getElementById('custom-notification');
            document.getElementById('notif-title').innerText = titulo;
            document.getElementById('notif-desc').innerText = desc;
            
            notif.classList.remove('hidden');
            setTimeout(() => {
                fecharNotificacao();
            }, 5000);
        }

        function fecharNotificacao() {
            document.getElementById('custom-notification').classList.add('hidden');
        }

        // ==================== OPERAÇÕES COM OBRAS ====================
        function abrirModalNovaObra() {
            document.getElementById('modal-nova-obra').classList.remove('hidden');
        }

        function fecharModalNovaObra() {
            document.getElementById('modal-nova-obra').classList.add('hidden');
        }

        function salvarNovaObra() {
            const titulo = document.getElementById('new-work-title').value;
            const genero = document.getElementById('new-work-genre').value;
            const p1 = document.getElementById('new-work-p1').value;
            const p2 = document.getElementById('new-work-p2').value;
            const sinopse = document.getElementById('new-work-synopsis').value;

            if(!titulo) {
                mostrarNotificacao("Preenchimento Obrigatório", "Sua obra necessita de um nome para ser forjada.");
                return;
            }

            const novaObra = {
                id: 'obra_' + Date.now(),
                titulo: titulo,
                genero: genero,
                protagonista1: p1 || 'Herói I',
                protagonista2: p2 || 'Herói II / Rival',
                sinopse: sinopse || 'Em branco',
                capitulos: [],
                personagens: [],
                worldbuilding: []
            };

            // Inscreve automaticamente os dois protagonistas originais na bíblia
            if(p1) novaObra.personagens.push({ name: p1, role: 'Primeiro Protagonista', physical: 'Líder / Foco central', drive: 'Seu desejo primário' });
            if(p2) novaObra.personagens.push({ name: p2, role: 'Segundo Protagonista / Rival', physical: 'Líder antagonista ou aliado de peso', drive: 'Opor-se ou guiar o Protagonista I' });

            APP_STATE.obras.push(novaObra);
            APP_STATE.activeWorkId = novaObra.id;
            
            salvarEstado();
            fecharModalNovaObra();
            renderizarEstanteObras();
            selecionarObra(novaObra.id);
            
            mostrarNotificacao("Universo Forjado", `"${titulo}" foi registrado.`);
            navegarPara('dashboard');
        }

        function selecionarObra(id) {
            const obra = APP_STATE.obras.find(o => o.id === id);
            if (!obra) return;

            APP_STATE.activeWorkId = id;
            salvarEstado();

            document.getElementById('active-work-indicator').innerText = obra.titulo;
            document.getElementById('menu-work-title').innerText = obra.titulo;
            document.getElementById('menu-work-progress').style.width = obra.capitulos.length > 0 ? '55%' : '5%';

            document.getElementById('dash-title').innerText = obra.titulo;
            document.getElementById('dash-subtitle').innerText = `Gênero: ${obra.genero}`;
            document.getElementById('dash-protagonist-1').innerText = obra.protagonista1;
            document.getElementById('dash-protagonist-2').innerText = obra.protagonista2;
            document.getElementById('dash-sinopse').innerText = obra.sinopse;

            atualizarContadoresDash(obra);
            renderizarPersonagens();
            renderizarWorldbuilding();
            atualizarSeletoresEDiretrizes();
        }

        function atualizarContadoresDash(obra) {
            document.getElementById('dash-capitulos-count').innerText = obra.capitulos.length;
            document.getElementById('dash-personagens-count').innerText = obra.personagens.length;
            document.getElementById('dash-locais-count').innerText = obra.worldbuilding.length;

            let totalWords = 0;
            obra.capitulos.forEach(cap => {
                totalWords += cap.content ? cap.content.split(/\s+/).filter(w => w.length > 0).length : 0;
            });
            document.getElementById('dash-palavras-count').innerText = totalWords;
        }

        function renderizarEstanteObras() {
            const grid = document.getElementById('grid-obras');
            grid.innerHTML = '';

            if (APP_STATE.obras.length === 0) {
                grid.innerHTML = `
                    <div class="col-span-full border border-dashed border-goldold/20 p-8 text-center rounded-sm">
                        <i data-lucide="book-open" class="w-8 h-8 text-goldold/40 mx-auto mb-3"></i>
                        <h4 class="font-cinzel text-sm text-goldold">Estante Vazia</h4>
                        <p class="text-xs text-cremeclaro/60 mt-1">Sua estante aguarda seu primeiro universo.</p>
                    </div>
                `;
                lucide.createIcons();
                return;
            }

            APP_STATE.obras.forEach(obra => {
                const isActive = obra.id === APP_STATE.activeWorkId;
                const card = document.createElement('div');
                card.className = `interactive-panel p-5 rounded-sm flex flex-col justify-between space-y-4 ${isActive ? 'border-goldold shadow-[0_0_15px_rgba(197,168,128,0.2)]' : ''}`;
                card.innerHTML = `
                    <div>
                        <div class="flex justify-between items-start">
                            <span class="text-[9px] px-2 py-0.5 bg-goldold/10 text-goldbright border border-goldold/20 rounded uppercase">${obra.genero}</span>
                            ${isActive ? '<span class="text-[9px] text-green-500 uppercase tracking-widest font-bold">Ativa</span>' : ''}
                        </div>
                        <h4 class="font-cinzel text-base text-creme mt-3">${obra.titulo}</h4>
                        <p class="text-xs text-cremeclaro/60 line-clamp-2 mt-1 italic">"${obra.sinopse}"</p>
                    </div>
                    <div class="flex justify-between items-center pt-3 border-t border-goldold/10 text-xs">
                        <span class="text-goldold/70 font-cinzel">${obra.capitulos.length} Capítulos</span>
                        <div class="flex space-x-2">
                            <button onclick="selecionarObra('${obra.id}')" class="px-3 py-1.5 bg-goldold text-absblack font-bold text-[10px] rounded hover:opacity-90 transition-all">Abrir</button>
                            <button onclick="excluirObra('${obra.id}')" class="p-1.5 bg-red-950/40 text-red-400 border border-red-900/30 rounded hover:bg-red-950/70"><i data-lucide="trash" class="w-3.5 h-3.5"></i></button>
                        </div>
                    </div>
                `;
                grid.appendChild(card);
            });
            lucide.createIcons();
        }

        function excluirObra(id) {
            if(confirm("Deseja deletar essa obra? Esta ação é permanente.")) {
                APP_STATE.obras = APP_STATE.obras.filter(o => o.id !== id);
                if (APP_STATE.activeWorkId === id) {
                    APP_STATE.activeWorkId = APP_STATE.obras.length > 0 ? APP_STATE.obras[0].id : null;
                }
                salvarEstado();
                renderizarEstanteObras();
                if (APP_STATE.activeWorkId) {
                    selecionarObra(APP_STATE.activeWorkId);
                } else {
                    document.getElementById('active-work-indicator').innerText = "Nenhuma";
                }
                mostrarNotificacao("Apagado", "Obra removida.");
            }
        }

        function salvarObraAtual() {
            salvarEstado();
            mostrarNotificacao("Salvo", "Todos os dados foram consolidados no armazenamento local.");
        }

        // ==================== GESTÃO DE PERSONAGENS ====================
        function abrirModalPersonagem() {
            if(!APP_STATE.activeWorkId) {
                mostrarNotificacao("Aviso", "Selecione uma obra ativa primeiro.");
                return;
            }
            document.getElementById('modal-personagem').classList.remove('hidden');
        }

        function fecharModalPersonagem() {
            document.getElementById('modal-personagem').classList.add('hidden');
        }

        function salvarPersonagem() {
            const obra = APP_STATE.obras.find(o => o.id === APP_STATE.activeWorkId);
            if(!obra) return;

            const name = document.getElementById('char-name').value;
            const role = document.getElementById('char-role').value;
            const physical = document.getElementById('char-physical').value;
            const drive = document.getElementById('char-drive').value;

            if(!name) {
                mostrarNotificacao("Erro", "Indique o nome do personagem.");
                return;
            }

            obra.personagens.push({ name, role, physical, drive });
            salvarEstado();
            fecharModalPersonagem();
            renderizarPersonagens();
            atualizarContadoresDash(obra);
            atualizarSeletoresEDiretrizes();
            mostrarNotificacao("Registrado", `${name} está na Bíblia.`);
        }

        function renderizarPersonagens() {
            const container = document.getElementById('list-personagens');
            container.innerHTML = '';

            const obra = APP_STATE.obras.find(o => o.id === APP_STATE.activeWorkId);
            if (!obra || obra.personagens.length === 0) {
                container.innerHTML = `
                    <div class="col-span-full border border-dashed border-goldold/20 p-8 text-center rounded-sm">
                        <h4 class="font-cinzel text-sm text-goldold">Sem Personagens</h4>
                    </div>
                `;
                return;
            }

            obra.personagens.forEach((char, idx) => {
                const item = document.createElement('div');
                item.className = 'interactive-panel p-5 rounded-sm space-y-3 relative';
                item.innerHTML = `
                    <div class="flex justify-between items-start">
                        <div>
                            <h4 class="font-cinzel text-sm text-creme">${char.name}</h4>
                            <span class="text-[9px] uppercase tracking-wider text-goldold font-bold">${char.role}</span>
                        </div>
                        <button onclick="removerPersonagem(${idx})" class="text-cremeclaro/30 hover:text-red-400">
                            <i data-lucide="user-minus" class="w-4 h-4"></i>
                        </button>
                    </div>
                    <div class="text-xs space-y-2 pt-2 border-t border-goldold/10 text-cremeclaro/80">
                        <p><strong>Físico:</strong> <span class="italic text-cremeclaro/70">${char.physical || 'Normal'}</span></p>
                        <p><strong>Desejo/Fraqueza:</strong> <span class="italic text-cremeclaro/70">${char.drive || 'Mistério'}</span></p>
                    </div>
                `;
                container.appendChild(item);
            });
            lucide.createIcons();
        }

        function removerPersonagem(index) {
            const obra = APP_STATE.obras.find(o => o.id === APP_STATE.activeWorkId);
            if(obra && confirm(`Deseja remover esse personagem?`)) {
                obra.personagens.splice(index, 1);
                salvarEstado();
                renderizarPersonagens();
                atualizarContadoresDash(obra);
                atualizarSeletoresEDiretrizes();
            }
        }

        // ==================== GESTÃO DE WORLDBUILDING ====================
        function abrirModalLocal() {
            if(!APP_STATE.activeWorkId) return;
            document.getElementById('modal-local').classList.remove('hidden');
        }

        function fecharModalLocal() {
            document.getElementById('modal-local').classList.add('hidden');
        }

        function salvarLocal() {
            const obra = APP_STATE.obras.find(o => o.id === APP_STATE.activeWorkId);
            if(!obra) return;

            const name = document.getElementById('world-name').value;
            const category = document.getElementById('world-category').value;
            const description = document.getElementById('world-description').value;

            if(!name) return;

            obra.worldbuilding.push({ name, category, description });
            salvarEstado();
            fecharModalLocal();
            renderizarWorldbuilding();
            atualizarContadoresDash(obra);
            mostrarNotificacao("Adicionado", `${name} catalogado.`);
        }

        function renderizarWorldbuilding() {
            const container = document.getElementById('list-worldbuilding');
            container.innerHTML = '';

            const obra = APP_STATE.obras.find(o => o.id === APP_STATE.activeWorkId);
            if (!obra || obra.worldbuilding.length === 0) {
                container.innerHTML = `<div class="col-span-full p-4 text-center text-xs text-creme/50">Nenhum conceito catalogado ainda.</div>`;
                return;
            }

            obra.worldbuilding.forEach((item, idx) => {
                const block = document.createElement('div');
                block.className = 'interactive-panel p-5 rounded-sm space-y-3';
                block.innerHTML = `
                    <div class="flex justify-between items-start">
                        <div>
                            <h4 class="font-cinzel text-sm text-creme">${item.name}</h4>
                            <span class="text-[9px] uppercase tracking-wider text-goldold font-bold">${item.category}</span>
                        </div>
                        <button onclick="removerWorldbuilding(${idx})" class="text-cremeclaro/30 hover:text-red-400">
                            <i data-lucide="trash-2" class="w-4 h-4"></i>
                        </button>
                    </div>
                    <p class="text-xs text-cremeclaro/70 border-t border-goldold/10 pt-2 whitespace-pre-wrap">${item.description}</p>
                `;
                container.appendChild(block);
            });
            lucide.createIcons();
        }

        function removerWorldbuilding(index) {
            const obra = APP_STATE.obras.find(o => o.id === APP_STATE.activeWorkId);
            if(obra && confirm(`Excluir elemento?`)) {
                obra.worldbuilding.splice(index, 1);
                salvarEstado();
                renderizarWorldbuilding();
                atualizarContadoresDash(obra);
            }
        }


        // ==================== SISTEMA DE POV INTELIGENTE & ATUALIZAÇÃO ====================
        function atualizarSeletoresEDiretrizes() {
            const povSelect = document.getElementById('chapter-pov-select');
            const capSelect = document.getElementById('editor-capitulo-select');
            const obra = APP_STATE.obras.find(o => o.id === APP_STATE.activeWorkId);

            if(!obra) return;

            // 1. POV SELETOR REFORMULADO (Protagonistas explícitos e POV alternado)
            povSelect.innerHTML = `
                <option value="Primeiro Protagonista: ${obra.protagonista1}">1º Protagonista (POV: ${obra.protagonista1})</option>
                <option value="Segundo Protagonista: ${obra.protagonista2}">2º Protagonista (POV: ${obra.protagonista2})</option>
                <option value="Alternado: ${obra.protagonista1} e ${obra.protagonista2}">POV Alternado (Ambos os Protagonistas)</option>
                <option value="Narrador Omnisciente">Narrador Omnisciente</option>
                <option value="Narrador Observador">Narrador Observador</option>
            `;

            // Adiciona outros secundários da Bíblia de Personagens
            obra.personagens.forEach(p => {
                if(p.name !== obra.protagonista1 && p.name !== obra.protagonista2) {
                    const opt = document.createElement('option');
                    opt.value = `Coadjuvante: ${p.name}`;
                    opt.innerText = `Coadjuvante (POV: ${p.name})`;
                    povSelect.appendChild(opt);
                }
            });

            // 2. SELETOR DE CAPÍTULOS
            capSelect.innerHTML = `<option value="">Novo Capítulo (Defina abaixo)...</option>`;
            obra.capitulos.forEach((cap, idx) => {
                const opt = document.createElement('option');
                opt.value = idx;
                opt.innerText = `Cap. ${cap.number || (idx+1)} - ${cap.title}`;
                capSelect.appendChild(opt);
            });
        }

        function limparCamposCapitulo() {
            document.getElementById('editor-capitulo-select').value = '';
            document.getElementById('chapter-number').value = '';
            document.getElementById('chapter-title').value = '';
            document.getElementById('chapter-pov-select').selectedIndex = 0;
            document.getElementById('chapter-guidelines').value = '';
            document.getElementById('manuscript-editor').value = '';
            document.getElementById('chapter-real-word-count').innerText = '0';
        }

        function carregarCapituloSelecionado() {
            const idx = document.getElementById('editor-capitulo-select').value;
            const obra = APP_STATE.obras.find(o => o.id === APP_STATE.activeWorkId);
            
            if (idx === '' || !obra) {
                limparCamposCapitulo();
                return;
            }

            const cap = obra.capitulos[idx];
            document.getElementById('chapter-number').value = cap.number || '';
            document.getElementById('chapter-title').value = cap.title || '';
            document.getElementById('chapter-pov-select').value = cap.pov || 'Narrador Omnisciente';
            document.getElementById('chapter-guidelines').value = cap.guidelines || '';
            document.getElementById('manuscript-editor').value = cap.content || '';
            
            atualizarContadorPalavrasManuscrito();
        }

        document.getElementById('manuscript-editor').addEventListener('input', atualizarContadorPalavrasManuscrito);

        function atualizarContadorPalavrasManuscrito() {
            const text = document.getElementById('manuscript-editor').value.trim();
            const words = text === '' ? 0 : text.split(/\s+/).filter(w => w.length > 0).length;
            document.getElementById('chapter-real-word-count').innerText = words;
        }

        function salvarCapituloManual() {
            const obra = APP_STATE.obras.find(o => o.id === APP_STATE.activeWorkId);
            if(!obra) return;

            const num = document.getElementById('chapter-number').value;
            const title = document.getElementById('chapter-title').value;
            const pov = document.getElementById('chapter-pov-select').value;
            const guidelines = document.getElementById('chapter-guidelines').value;
            const content = document.getElementById('manuscript-editor').value;

            if(!title) {
                mostrarNotificacao("Preenchimento Necessário", "Indique o título do capítulo.");
                return;
            }

            const capData = {
                number: num,
                title: title,
                pov: pov,
                guidelines: guidelines,
                content: content
            };

            const idx = document.getElementById('editor-capitulo-select').value;
            if (idx !== '') {
                obra.capitulos[idx] = capData;
                mostrarNotificacao("Capítulo Atualizado", "As alterações foram integradas.");
            } else {
                obra.capitulos.push(capData);
                mostrarNotificacao("Capítulo Salvo", `Capítulo ${num || 'Novo'} registrado com sucesso.`);
            }

            salvarEstado();
            atualizarContadoresDash(obra);
            atualizarSeletoresEDiretrizes();
        }


        // ==================== INTEGRAÇÃO DO GEMINI COM HISTÓRICO DE COERÊNCIA ====================
        
        async function fazerChamadaComBackoff(endpoint, payload) {
            const maxRetries = 5;
            let delay = 1000;

            for (let i = 0; i < maxRetries; i++) {
                try {
                    const response = await fetch(endpoint, {
                        method: 'POST',
                        headers: { 'Content-Type': 'application/json' },
                        body: JSON.stringify(payload)
                    });

                    if (response.ok) {
                        return await response.json();
                    } else {
                        throw new Error(`Erro API: ${response.status}`);
                    }
                } catch (err) {
                    if (i === maxRetries - 1) throw err;
                    await new Promise(resolve => setTimeout(resolve, delay));
                    delay *= 2;
                }
            }
        }

        async function gerarTextoCapitulo() {
            const key = APP_STATE.apiKey ? APP_STATE.apiKey.trim() : '';
            if (key === '') {
                mostrarNotificacao("Chave de API requerida", "Por favor, insira sua API Key do Gemini no cabeçalho antes de gerar.");
                return;
            }

            const obra = APP_STATE.obras.find(o => o.id === APP_STATE.activeWorkId);
            if(!obra) return;

            const targetWords = document.getElementById('chapter-word-range').value;
            const currentNum = parseInt(document.getElementById('chapter-number').value) || (obra.capitulos.length + 1);
            const title = document.getElementById('chapter-title').value || 'Sem Título';
            const pov = document.getElementById('chapter-pov-select').value;
            const guidelines = document.getElementById('chapter-guidelines').value;

            // --- RESOLUÇÃO DO REQUISITO 2: MEMÓRIA DE COERÊNCIA (ANÁLISE DE CAPÍTULOS ANTERIORES) ---
            let historicoAnterior = "";
            
            // Filtra e organiza os capítulos com numeração anterior ao atual para enviar como histórico
            const capsAnteriores = obra.capitulos
                .filter(c => parseInt(c.number) < currentNum)
                .sort((a, b) => parseInt(a.number) - parseInt(b.number));

            if(capsAnteriores.length > 0) {
                historicoAnterior = "\nHISTÓRICO CONTEXTUAL DE CAPÍTULOS ANTERIORES (Para manter a química e evitar incoerências de roteiro):\n";
                capsAnteriores.forEach(cap => {
                    const resumoCap = cap.content ? cap.content.substring(0, 450) + "..." : "Sem conteúdo";
                    historicoAnterior += `\n-> Capítulo ${cap.number}: "${cap.title}" | POV: ${cap.pov}\n   Diretrizes anteriores: ${cap.guidelines || "Nenhuma"}\n   Início do texto anterior: ${resumoCap}\n`;
                });
            } else {
                historicoAnterior = "\nEste é o capítulo inicial. Siga fielmente a sinopse primordial da obra.";
            }

            const systemPrompt = `Você é um co-escritor literário premium. Seu trabalho é redigir manuscritos de altíssimo nível, ricos em detalhes sensoriais, profundidade psicológica de personagens e coerência absoluta com os eventos anteriores. Nunca apresse os acontecimentos.`;

            const userPrompt = `
                Escreva o Capítulo ${currentNum} intitulado "${title}" para a obra de gênero "${obra.genero}".
                
                DADOS GERAIS DA SAGA:
                - Título Geral da Saga: ${obra.titulo}
                - Conflito Geral: ${obra.sinopse}
                - Protagonista Principal I: ${obra.protagonista1}
                - Protagonista Principal II: ${obra.protagonista2}
                
                ${historicoAnterior}
                
                DIRETRIZES EXCLUSIVAS DESTE NOVO CAPÍTULO:
                - Ponto de Vista (POV) que DEVE conduzir o capítulo: "${pov}"
                - O que deve acontecer de primordial nesse capítulo: ${guidelines || 'Desenvolva conflitos que levem a história adiante de forma natural.'}
                - Tamanho Alvo do Texto: Aproximadamente ${targetWords} palavras de narrativa de ficção primorosa.
                
                IMPORTANTE: Escreva o texto literário diretamente. Não faça comentários extras nem notas de autor.
            `;

            mostrarNotificacao("Forjando Manuscrito", "Integrando os capítulos anteriores e redigindo com o Gemini...");

            // Se o usuário estiver no mobile, alternamos visualmente para a aba de "Escrever & Ler" para ver o resultado se formando
            if(window.innerWidth < 1024) {
                toggleMobileEditorTab('manuscrito');
            }

            try {
                const model = document.getElementById('gemini-model-select').value;
                const endpoint = `https://generativelanguage.googleapis.com/v1beta/models/${model}:generateContent?key=${key}`;
                const payload = {
                    contents: [{ parts: [{ text: userPrompt }] }],
                    systemInstruction: { parts: [{ text: systemPrompt }] }
                };

                const data = await fazerChamadaComBackoff(endpoint, payload);
                const text = data.candidates?.[0]?.content?.parts?.[0]?.text;

                if (text) {
                    document.getElementById('manuscript-editor').value = text;
                    atualizarContadorPalavrasManuscrito();
                    mostrarNotificacao("Texto Gerado", `Capítulo "${title}" forjado com sucesso.`);
                } else {
                    throw new Error("Vazio");
                }

            } catch (err) {
                console.error(err);
                mostrarNotificacao("Erro de Geração", "Verifique sua conexão ou se a chave API inserida é válida.");
            }
        }

        async function gerarEsqueletoSaga() {
            const key = APP_STATE.apiKey ? APP_STATE.apiKey.trim() : '';
            if (key === '') {
                mostrarNotificacao("Aviso", "Insira sua Gemini API Key no topo do cabeçalho.");
                return;
            }

            const obra = APP_STATE.obras.find(o => o.id === APP_STATE.activeWorkId);
            if(!obra) return;

            const tom = document.getElementById('saga-tom').value;
            const diretriz = document.getElementById('saga-diretriz').value;
            const numCaps = document.getElementById('saga-capitulos-num').value;

            const systemPrompt = `Você é um planejador de arcos narrativos. Ajude o escritor a montar um outline robusto.`;

            const userPrompt = `
                Mapeie a saga de "${obra.genero}" intitulada "${obra.titulo}".
                Sinopse Primária: ${obra.sinopse}
                Protagonistas principais: ${obra.protagonista1} e ${obra.protagonista2}
                
                Parâmetros:
                - Tom: ${tom}
                - Número de Capítulos: ${numCaps}
                - Foco de acontecimentos: ${diretriz}

                Esboce detalhadamente cada capítulo informando: Número e Título do capítulo, POV indicado, Conflito Central e Gancho Final.
            `;

            mostrarNotificacao("Forjando Esqueleto", "Consultando o Gemini para estruturar o arco...");

            try {
                const model = document.getElementById('gemini-model-select').value;
                const endpoint = `https://generativelanguage.googleapis.com/v1beta/models/${model}:generateContent?key=${key}`;
                const payload = {
                    contents: [{ parts: [{ text: userPrompt }] }],
                    systemInstruction: { parts: [{ text: systemPrompt }] }
                };

                const data = await fazerChamadaComBackoff(endpoint, payload);
                const text = data.candidates?.[0]?.content?.parts?.[0]?.text;

                if (text) {
                    document.getElementById('saga-output').innerText = text;
                    mostrarNotificacao("Esboço Mapeado", "Arco pronto para importação.");
                }

            } catch (err) {
                console.error(err);
                mostrarNotificacao("Erro", "Erro ao conectar-se à API.");
            }
        }

        function importarSagaComoCapitulos() {
            const output = document.getElementById('saga-output').innerText;
            const obra = APP_STATE.obras.find(o => o.id === APP_STATE.activeWorkId);
            
            if(!obra || output.startsWith("O plano") || output === '') {
                mostrarNotificacao("Erro", "Nenhum esqueleto para importar.");
                return;
            }

            const lines = output.split('\n');
            let capituloNum = 1;

            lines.forEach(line => {
                if (line.toLowerCase().includes("capítulo") || line.toLowerCase().includes("capitulo")) {
                    obra.capitulos.push({
                        number: capituloNum,
                        title: `Sugerido: Capítulo ${capituloNum}`,
                        pov: `Primeiro Protagonista: ${obra.protagonista1}`,
                        guidelines: line.substring(0, 200),
                        content: `Esboço importado do Forjador de Sagas:\n\n${line}`
                    });
                    capituloNum++;
                }
            });

            if (capituloNum === 1) {
                obra.capitulos.push({
                    number: 1,
                    title: "O Despertar",
                    pov: `Primeiro Protagonista: ${obra.protagonista1}`,
                    guidelines: "Expandir o esqueleto geral de capítulos gerado.",
                    content: output
                });
            }

            salvarEstado();
            atualizarContadoresDash(obra);
            atualizarSeletoresEDiretrizes();
            mostrarNotificacao("Importado", "Esboços integrados na fila de capítulos.");
            navegarPara('editor-capitulos');
        }


        // ==================== CLIMA ATMOSFÉRICO (CANVAS) ====================
        const canvas = document.getElementById('ambient-canvas');
        const ctx = canvas.getContext('2d');
        let particlesArray = [];

        function resizeCanvas() {
            canvas.width = window.innerWidth;
            canvas.height = window.innerHeight;
        }

        class Particle {
            constructor() {
                this.x = Math.random() * canvas.width;
                this.y = Math.random() * canvas.height;
                this.size = Math.random() * 2 + 0.3;
                this.speedX = Math.random() * 0.4 - 0.2;
                this.speedY = Math.random() * 0.3 + 0.1;
                this.opacity = Math.random() * 0.5 + 0.1;
            }

            update() {
                this.x += this.speedX;
                this.y += this.speedY;

                if (this.y > canvas.height) {
                    this.y = -10;
                    this.x = Math.random() * canvas.width;
                }
            }

            draw() {
                ctx.fillStyle = `rgba(197, 168, 128, ${this.opacity})`;
                ctx.beginPath();
                ctx.arc(this.x, this.y, this.size, 0, Math.PI * 2);
                ctx.fill();
            }
        }

        function initParticles() {
            particlesArray = [];
            const count = Math.floor((canvas.width * canvas.height) / 9500);
            for (let i = 0; i < count; i++) {
                particlesArray.push(new Particle());
            }
        }

        function animate() {
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            particlesArray.forEach(p => {
                p.update();
                p.draw();
            });
            requestAnimationFrame(animate);
        }

        window.addEventListener('resize', () => {
            resizeCanvas();
            initParticles();
        });


        // ==================== BOOTSTRAP GERAL ====================
        window.onload = function () {
            resizeCanvas();
            initParticles();
            animate();
            inicializarEstado();
            lucide.createIcons();
        }
    </script>
</body>
</html>
