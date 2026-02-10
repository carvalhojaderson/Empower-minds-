<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Epower Minds × BDO - Apresentação</title>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@400;600;700&family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        /* ============================================
           CONFIGURAÇÃO DE SLIDES
           ============================================ */
        @page {
            size: 1920px 1080px;
            margin: 0;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html, body {
            margin: 0;
            padding: 0;
            width: 100%;
        }

        body {
            font-family: 'Inter', sans-serif;
            background: #1a1a1a;
            color: #F5F7FA;
            overflow-x: hidden;
        }

        /* Cada slide é uma "página" na impressão */
        .slide {
            width: 1920px;
            height: 1080px;
            margin: 0 auto 20px;
            position: relative;
            overflow: hidden;
            page-break-after: always;
            page-break-inside: avoid;
            background: linear-gradient(135deg, #061A2B 0%, #0B2F4A 100%);
            box-shadow: 0 10px 40px rgba(0,0,0,0.5);
        }

        .slide:last-child {
            page-break-after: auto;
            margin-bottom: 0;
        }

        /* ============================================
           ELEMENTOS COMUNS
           ============================================ */
        .slide-header {
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 80px;
            background: rgba(6, 26, 43, 0.9);
            border-bottom: 2px solid #C9A24A;
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 0 60px;
            z-index: 100;
        }

        .logo-epower {
            font-family: 'Cinzel', serif;
            font-size: 24px;
            font-weight: 700;
            color: #F5F7FA;
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .logo-epower svg {
            width: 40px;
            height: 40px;
        }

        .logo-bdo {
            font-family: 'Inter', sans-serif;
            font-size: 28px;
            font-weight: 700;
            color: #C9A24A;
            letter-spacing: 2px;
        }

        .slide-number {
            position: absolute;
            bottom: 30px;
            right: 60px;
            font-size: 14px;
            color: rgba(245, 247, 250, 0.5);
            font-weight: 500;
            z-index: 10;
        }

        .slide-content {
            padding: 120px 80px 80px;
            height: 100%;
            display: flex;
            flex-direction: column;
        }

        h1 {
            font-family: 'Cinzel', serif;
            font-size: 64px;
            font-weight: 700;
            line-height: 1.1;
            margin-bottom: 30px;
            color: #F5F7FA;
        }

        h2 {
            font-family: 'Cinzel', serif;
            font-size: 48px;
            font-weight: 600;
            color: #C9A24A;
            margin-bottom: 40px;
            line-height: 1.2;
        }

        h3 {
            font-family: 'Inter', sans-serif;
            font-size: 32px;
            font-weight: 600;
            color: #1AA6A6;
            margin-bottom: 20px;
        }

        h4 {
            font-family: 'Inter', sans-serif;
            font-size: 20px;
            font-weight: 600;
            color: #F5F7FA;
            margin-bottom: 10px;
        }

        p {
            font-size: 24px;
            line-height: 1.6;
            margin-bottom: 20px;
            max-width: 90%;
        }

        .texto-medio {
            font-size: 28px;
            line-height: 1.5;
        }

        .destaque {
            background: linear-gradient(90deg, rgba(201, 162, 74, 0.2) 0%, transparent 100%);
            border-left: 6px solid #C9A24A;
            padding: 30px 40px;
            margin: 30px 0;
            font-style: italic;
            font-size: 28px;
            color: #F5F7FA;
        }

        /* ============================================
           SLIDE 1: CAPA
           ============================================ */
        .slide-capa {
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            background: radial-gradient(ellipse at center, #0B2F4A 0%, #061A2B 70%);
        }

        .slide-capa .simbolo-principal {
            width: 200px;
            height: 200px;
            margin-bottom: 50px;
        }

        .slide-capa h1 {
            font-size: 80px;
            margin-bottom: 20px;
            background: linear-gradient(135deg, #F5F7FA 0%, #C9A24A 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .slide-capa .subtitulo {
            font-family: 'Cinzel', serif;
            font-size: 36px;
            color: #C9A24A;
            margin-bottom: 60px;
            font-weight: 400;
        }

        .slide-capa .descricao {
            font-size: 24px;
            max-width: 1000px;
            color: rgba(245, 247, 250, 0.9);
            line-height: 1.8;
            margin-bottom: 80px;
        }

        .slide-capa .meta {
            border-top: 1px solid rgba(201, 162, 74, 0.3);
            padding-top: 40px;
            font-size: 16px;
            color: rgba(245, 247, 250, 0.6);
        }

        .slide-capa .meta p {
            margin: 0;
            font-size: 16px;
        }

        /* ============================================
           SLIDE 2: SUMÁRIO
           ============================================ */
        .sumario-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 30px;
            margin-top: 20px;
        }

        .sumario-item {
            background: rgba(255, 255, 255, 0.05);
            border: 1px solid rgba(201, 162, 74, 0.3);
            border-radius: 12px;
            padding: 30px;
            display: flex;
            align-items: center;
            gap: 20px;
        }

        .sumario-numero {
            font-family: 'Cinzel', serif;
            font-size: 48px;
            font-weight: 700;
            color: #C9A24A;
            min-width: 80px;
        }

        .sumario-texto {
            font-size: 24px;
            font-weight: 500;
        }

        /* ============================================
           SLIDES DE CONTEÚDO
           ============================================ */
        .conteudo-duas-colunas {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 60px;
            flex: 1;
        }

        .coluna-texto {
            display: flex;
            flex-direction: column;
            justify-content: center;
        }

        .coluna-visual {
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
        }

        .card-info {
            background: rgba(255, 255, 255, 0.05);
            border-left: 4px solid #C9A24A;
            padding: 25px 30px;
            margin-bottom: 20px;
            border-radius: 0 8px 8px 0;
        }

        .card-info h4 {
            color: #C9A24A;
            font-size: 20px;
            margin-bottom: 10px;
        }

        .card-info p {
            font-size: 18px;
            margin: 0;
            color: rgba(245, 247, 250, 0.9);
        }

        .lista-destaque {
            list-style: none;
            margin: 20px 0;
            padding: 0;
        }

        .lista-destaque li {
            font-size: 22px;
            padding: 15px 0 15px 40px;
            position: relative;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }

        .lista-destaque li:before {
            content: "→";
            position: absolute;
            left: 0;
            color: #C9A24A;
            font-weight: bold;
            font-size: 24px;
        }

        /* ============================================
           TABELAS
           ============================================ */
        .tabela-slide {
            width: 100%;
            border-collapse: collapse;
            margin-top: 20px;
            font-size: 18px;
        }

        .tabela-slide th {
            background: #061A2B;
            color: #C9A24A;
            padding: 20px;
            text-align: left;
            font-weight: 600;
            text-transform: uppercase;
            font-size: 14px;
            letter-spacing: 1px;
            border-bottom: 3px solid #C9A24A;
        }

        .tabela-slide td {
            padding: 20px;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
            vertical-align: top;
        }

        .tabela-slide tr:nth-child(even) {
            background: rgba(255, 255, 255, 0.03);
        }

        /* ============================================
           FLUXO VISUAL
           ============================================ */
        .fluxo-visual {
            display: flex;
            align-items: center;
            justify-content: space-between;
            margin: 40px 0;
        }

        .fluxo-etapa {
            text-align: center;
            flex: 1;
        }

        .fluxo-etapa .icone {
            width: 100px;
            height: 100px;
            background: rgba(201, 162, 74, 0.2);
            border: 3px solid #C9A24A;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 20px;
            font-family: 'Cinzel', serif;
            font-size: 36px;
            color: #C9A24A;
        }

        .fluxo-etapa h4 {
            font-size: 20px;
            color: #F5F7FA;
            margin-bottom: 10px;
        }

        .fluxo-etapa p {
            font-size: 16px;
            color: rgba(245, 247, 250, 0.7);
            margin: 0 auto;
        }

        .fluxo-seta {
            color: #C9A24A;
            font-size: 40px;
            margin: 0 20px;
        }

        /* ============================================
           INDICADORES
           ============================================ */
        .indicadores-row {
            display: flex;
            justify-content: space-around;
            margin-top: 40px;
            gap: 30px;
        }

        .indicador-card {
            background: linear-gradient(135deg, #0B2F4A 0%, #061A2B 100%);
            border: 2px solid #C9A24A;
            border-radius: 16px;
            padding: 40px;
            text-align: center;
            flex: 1;
        }

        .indicador-numero {
            font-family: 'Cinzel', serif;
            font-size: 72px;
            font-weight: 700;
            color: #C9A24A;
            display: block;
            margin-bottom: 10px;
        }

        .indicador-label {
            font-size: 20px;
            color: #F5F7FA;
            font-weight: 500;
        }

        .indicador-sublabel {
            font-size: 14px;
            color: rgba(245, 247, 250, 0.6);
            margin-top: 5px;
        }

        /* ============================================
           TIMELINE
           ============================================ */
        .timeline {
            display: flex;
            justify-content: space-between;
            margin-top: 40px;
            position: relative;
        }

        .timeline:before {
            content: '';
            position: absolute;
            top: 50px;
            left: 10%;
            right: 10%;
            height: 4px;
            background: linear-gradient(90deg, #C9A24A 0%, #1AA6A6 100%);
        }

        .timeline-fase {
            text-align: center;
            flex: 1;
            position: relative;
        }

        .timeline-dot {
            width: 30px;
            height: 30px;
            background: #C9A24A;
            border-radius: 50%;
            margin: 35px auto 20px;
            position: relative;
            z-index: 2;
            border: 4px solid #061A2B;
        }

        .timeline-fase h4 {
            font-size: 24px;
            color: #C9A24A;
            margin-bottom: 10px;
        }

        .timeline-fase .periodo {
            font-size: 16px;
            color: #1AA6A6;
            font-weight: 600;
            margin-bottom: 15px;
        }

        .timeline-fase p {
            font-size: 16px;
            color: rgba(245, 247, 250, 0.8);
            margin: 0 auto;
            max-width: 300px;
        }

        /* ============================================
           SLIDE FINAL
           ============================================ */
        .slide-final {
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            background: radial-gradient(ellipse at center, #0B2F4A 0%, #061A2B 70%);
        }

        .slide-final h2 {
            font-size: 56px;
            margin-bottom: 40px;
        }

        .frase-final {
            font-family: 'Cinzel', serif;
            font-size: 36px;
            color: #C9A24A;
            font-style: italic;
            max-width: 1200px;
            line-height: 1.5;
            margin-bottom: 80px;
        }

        .contatos-final {
            display: flex;
            gap: 100px;
            margin-top: 60px;
        }

        .contato-box {
            text-align: center;
        }

        .contato-box h4 {
            font-size: 24px;
            color: #C9A24A;
            margin-bottom: 15px;
        }

        .contato-box p {
            font-size: 18px;
            color: rgba(245, 247, 250, 0.8);
            margin: 5px 0;
        }

        /* ============================================
           RESPONSIVIDADE PARA VISUALIZAÇÃO
           ============================================ */
        @media screen and (max-width: 1920px) {
            .slide {
                transform: scale(0.5);
                transform-origin: top center;
                margin-bottom: -540px;
            }
        }

        @media screen and (max-width: 960px) {
            .slide {
                transform: scale(0.25);
                margin-bottom: -810px;
            }
        }

        /* ============================================
           PRINT OPTIMIZATION
           ============================================ */
        @media print {
            body {
                background: white;
                margin: 0;
                padding: 0;
            }
            
            .slide {
                margin: 0;
                box-shadow: none;
                page-break-after: always;
                width: 1920px;
                height: 1080px;
            }
        }
    </style>
</head>
<body>

<!-- ============================================
     SLIDE 1: CAPA
     ============================================ -->
<div class="slide slide-capa">
    <svg class="simbolo-principal" viewBox="0 0 120 120" fill="none" xmlns="http://www.w3.org/2000/svg">
        <circle cx="60" cy="60" r="20" fill="#C9A24A" opacity="0.9"/>
        <path d="M60 20V30M60 90V100M20 60H30M90 60H100M32.7 32.7L39.8 39.8M80.2 80.2L87.3 87.3M32.7 87.3L39.8 80.2M80.2 39.8L87.3 32.7" stroke="#C9A24A" stroke-width="3" stroke-linecap="round"/>
        <path d="M85 60C85 43.4315 71.5685 30 55 30C60 30 65 43.4315 65 60C65 76.5685 60 90 55 90C71.5685 90 85 76.5685 85 60Z" fill="#F5F7FA" opacity="0.9"/>
        <path d="M60 75L45 95H75L60 75Z" fill="#1AA6A6" opacity="0.8"/>
    </svg>
    
    <h1>Epower Minds × BDO</h1>
    <div class="subtitulo">Ecossistema Conector para o Fundo de Sabedoria Prática ESG</div>
    
    <div class="descricao">
        Arquitetura de parceria estratégica para transformar estratégia ESG<br>
        em aplicação territorial mensurável, conectando precisão técnica<br>
        à execução social de alta performance
    </div>
    
    <div class="meta">
        <p>Documento Estratégico Confidencial | Fevereiro 2026</p>
    </div>
</div>

<!-- ============================================
     SLIDE 2: SUMÁRIO EXECUTIVO
     ============================================ -->
<div class="slide">
    <div class="slide-header">
        <div class="logo-epower">
            <svg viewBox="0 0 40 40" width="40" height="40" xmlns="http://www.w3.org/2000/svg">
                <circle cx="20" cy="20" r="8" fill="#C9A24A"/>
                <path d="M20 4V8M20 32V36M4 20H8M32 20H36" stroke="#C9A24A" stroke-width="2"/>
            </svg>
            Epower Minds
        </div>
        <div class="logo-bdo">BDO</div>
    </div>
    
    <div class="slide-content">
        <h2>Sumário Executivo</h2>
        
        <div class="sumario-grid">
            <div class="sumario-item">
                <div class="sumario-numero">01</div>
                <div class="sumario-texto">Contexto e Oportunidade</div>
            </div>
            <div class="sumario-item">
                <div class="sumario-numero">02</div>
                <div class="sumario-texto">Proposta: O Ecossistema Conector</div>
            </div>
            <div class="sumario-item">
                <div class="sumario-numero">03</div>
                <div class="sumario-texto">Arquitetura da Parceria</div>
            </div>
            <div class="sumario-item">
                <div class="sumario-numero">04</div>
                <div class="sumario-texto">Fundo de Sabedoria Prática ESG</div>
            </div>
            <div class="sumario-item">
                <div class="sumario-numero">05</div>
                <div class="sumario-texto">Modelo de Governança</div>
            </div>
            <div class="sumario-item">
                <div class="sumario-numero">06</div>
                <div class="sumario-texto">Plano de Implementação</div>
            </div>
            <div class="sumario-item">
                <div class="sumario-numero">07</div>
                <div class="sumario-texto">Indicadores e Metas</div>
            </div>
            <div class="sumario-item">
                <div class="sumario-numero">08</div>
                <div class="sumario-texto">Próximos Passos</div>
            </div>
        </div>
    </div>
    
    <div class="slide-number">02</div>
</div>

<!-- ============================================
     SLIDE 3: O DESAFIO
     ============================================ -->
<div class="slide">
    <div class="slide-header">
        <div class="logo-epower">
            <svg viewBox="0 0 40 40" width="40" height="40" xmlns="http://www.w3.org/2000/svg">
                <circle cx="20" cy="20" r="8" fill="#C9A24A"/>
            </svg>
            Epower Minds
        </div>
        <div class="logo-bdo">BDO</div>
    </div>
    
    <div class="slide-content">
        <h2>O Desafio: Do Relatório à Rua</h2>
        
        <div class="conteudo-duas-colunas">
            <div class="coluna-texto">
                <h3>O Mercado ESG Avançou em:</h3>
                <ul class="lista-destaque">
                    <li>Governança corporativa estruturada</li>
                    <li>Reporting e disclosure padronizado</li>
                    <li>Metas baseadas em ciência (SBTi)</li>
                    <li>Auditoria e assurance especializada</li>
                </ul>
                
                <div class="destaque" style="margin-top: 40px;">
                    "Mas enfrenta desafio crítico em aplicação territorial efetiva"
                </div>
            </div>
            
            <div class="coluna-texto">
                <h3>A Lacuna Identificada:</h3>
                <div class="card-info">
                    <h4>Abundância</h4>
                    <p>Estratégias escritas, indicadores projetados, compromissos assumidos</p>
                </div>
                <div class="card-info">
                    <h4>Escassez</h4>
                    <p>Projetos estruturados para execução, conexão efetiva entre atores, mensuração de impacto real, continuidade além do ciclo de reporte</p>
                </div>
            </div>
        </div>
    </div>
    
    <div class="slide-number">03</div>
</div>

<!-- ============================================
     SLIDE 4: CONTEXTO BDO
     ============================================ -->
<div class="slide">
    <div class="slide-header">
        <div class="logo-epower">
            <svg viewBox="0 0 40 40" width="40" height="40" xmlns="http://www.w3.org/2000/svg">
                <circle cx="20" cy="20" r="8" fill="#C9A24A"/>
            </svg>
            Epower Minds
        </div>
        <div class="logo-bdo">BDO</div>
    </div>
    
    <div class="slide-content">
        <h2>Contexto: Liderança BDO em ESG</h2>
        
        <div class="indicadores-row" style="margin-top: 60px;">
            <div class="indicador-card">
                <span class="indicador-numero">2x</span>
                <span class="indicador-label">Selo Ouro GHG Protocol</span>
                <span class="indicador-sublabel">Anos consecutivos</span>
            </div>
            <div class="indicador-card">
                <span class="indicador-numero">SBTi</span>
                <span class="indicador-label">Metas Aprovadas</span>
                <span class="indicador-sublabel">Setembro 2025</span>
            </div>
            <div class="indicador-card">
                <span class="indicador-numero">42%</span>
                <span class="indicador-label">Redução de Emissões</span>
                <span class="indicador-sublabel">Meta até 2030</span>
            </div>
            <div class="indicador-card">
                <span class="indicador-numero">100%</span>
                <span class="indicador-label">Energia Renovável</span>
                <span class="indicador-sublabel">Operações BDO</span>
            </div>
        </div>
        
        <div class="destaque" style="margin-top: 60px; text-align: center;">
            8º Estudo de Sustentabilidade BDO: 61% das empresas enxergam ESG como estratégia,<br>
            mas apenas 39% possuem departamento estruturado → Oportunidade de diferenciação
        </div>
    </div>
    
    <div class="slide-number">04</div>
</div>

<!-- ============================================
     SLIDE 5: PROPOSTA DE VALOR
     ============================================ -->
<div class="slide">
    <div class="slide-header">
        <div class="logo-epower">
            <svg viewBox="0 0 40 40" width="40" height="40" xmlns="http://www.w3.org/2000/svg">
                <circle cx="20" cy="20" r="8" fill="#C9A24A"/>
            </svg>
            Epower Minds
        </div>
        <div class="logo-bdo">BDO</div>
    </div>
    
    <div class="slide-content">
        <h2>Proposta: O Ecossistema Conector</h2>
        
        <div class="fluxo-visual" style="margin-top: 40px;">
            <div class="fluxo-etapa">
                <div class="icone">BDO</div>
                <h4>Estratégia & Compliance</h4>
                <p>Diagnóstico ESG<br>Metas SBTi<br>Reporting</p>
            </div>
            <div class="fluxo-seta">→</div>
            <div class="fluxo-etapa">
                <div class="icone" style="background: rgba(26, 166, 166, 0.2); border-color: #1AA6A6; color: #1AA6A6;">EM</div>
                <h4>Conexão & Aplicação</h4>
                <p>Engenharia de conexão<br>Governança de campo<br>Mensuração territorial</p>
            </div>
            <div class="fluxo-seta">→</div>
            <div class="fluxo-etapa">
                <div class="icone" style="background: rgba(245, 247, 250, 0.1); border-color: #F5F7FA; color: #F5F7FA;">★</div>
                <h4>Impacto Real</h4>
                <p>Projetos executados<br>Resultados mensuráveis<br>Legado sustentado</p>
            </div>
        </div>
        
        <div class="destaque" style="margin-top: 60px;">
            O Epower Minds não compete com a BDO em auditoria ou consultoria estratégica.<br>
            Atuamos como camada de aplicação que converte estratégia em execução territorial.
        </div>
    </div>
    
    <div class="slide-number">05</div>
</div>

<!-- ============================================
     SLIDE 6: OS TRÊS MOVIMENTOS
     ============================================ -->
<div class="slide">
    <div class="slide-header">
        <div class="logo-epower">
            <svg viewBox="0 0 40 40" width="40" height="40" xmlns="http://www.w3.org/2000/svg">
                <circle cx="20" cy="20" r="8" fill="#C9A24A"/>
            </svg>
            Epower Minds
        </div>
        <div class="logo-bdo">BDO</div>
    </div>
    
    <div class="slide-content">
        <h2>Metodologia: Os Três Movimentos</h2>
        
        <div class="indicadores-row" style="margin-top: 40px;">
            <div class="indicador-card" style="border-color: #C9A24A;">
                <div style="font-size: 60px; margin-bottom: 20px;">☉</div>
                <h3 style="color: #C9A24A; margin-bottom: 15px; font-size: 28px;">VISÃO</h3>
                <p style="font-size: 18px; color: rgba(245, 247, 250, 0.9); margin: 0;">Sol e Lua</p>
                <p style="font-size: 16px; color: rgba(245, 247, 250, 0.7); margin-top: 10px;">Discernir tempos e estações.<br>Ler o momento certo de agir.</p>
            </div>
            <div class="indicador-card" style="border-color: #1AA6A6;">
                <div style="font-size: 60px; margin-bottom: 20px;">⛵</div>
                <h3 style="color: #1AA6A6; margin-bottom: 15px; font-size: 28px;">NAVEGAÇÃO</h3>
                <p style="font-size: 18px; color: rgba(245, 247, 250, 0.9); margin: 0;">Barco e Diamante</p>
                <p style="font-size: 16px; color: rgba(245, 247, 250, 0.7); margin-top: 10px;">Traçar rota com segurança.<br>Navegar as correntes das leis.</p>
            </div>
            <div class="indicador-card" style="border-color: #F5F7FA;">
                <div style="font-size: 60px; margin-bottom: 20px;">🏹</div>
                <h3 style="color: #F5F7FA; margin-bottom: 15px; font-size: 28px;">APLICAÇÃO</h3>
                <p style="font-size: 18px; color: rgba(245, 247, 250, 0.9); margin: 0;">Arco e Celeiro</p>
                <p style="font-size: 16px; color: rgba(245, 247, 250, 0.7); margin-top: 10px;">Arco firme, flecha certa.<br>Implantar e sustentar.</p>
            </div>
        </div>
        
        <div class="destaque" style="margin-top: 50px; text-align: center; font-size: 32px;">
            "Não paramos na complexidade do sistema. Nós aplicamos no território."
        </div>
    </div>
    
    <div class="slide-number">06</div>
</div>

<!-- ============================================
     SLIDE 7: ARQUITETURA DA PARCERIA
     ============================================ -->
<div class="slide">
    <div class="slide-header">
        <div class="logo-epower">
            <svg viewBox="0 0 40 40" width="40" height="40" xmlns="http://www.w3.org/2000/svg">
                <circle cx="20" cy="20" r="8" fill="#C9A24A"/>
            </svg>
            Epower Minds
        </div>
        <div class="logo-bdo">BDO</div>
    </div>
    
    <div class="slide-content">
        <h2>Arquitetura da Parceria</h2>
        
        <table class="tabela-slide" style="margin-top: 30px;">
            <thead>
                <tr>
                    <th style="width: 15%;">Etapa</th>
                    <th style="width: 30%;">BDO</th>
                    <th style="width: 30%;">Epower Minds</th>
                    <th style="width: 25%;">Resultado</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td><strong>1. Diagnóstico</strong></td>
                    <td>Assessment ESG, materialidade, gaps regulatórios</td>
                    <td>Mapeamento territorial de oportunidades</td>
                    <td>Projetos viáveis identificados</td>
                </tr>
                <tr>
                    <td><strong>2. Estratégia</strong></td>
                    <td>Metas, KPIs, roadmap ESG</td>
                    <td>Discernimento de estações e janelas</td>
                    <td>Plano com timing preciso</td>
                </tr>
                <tr>
                    <td><strong>3. Estruturação</strong></td>
                    <td>Governança corporativa, compliance</td>
                    <td>Engenharia de conexão, viabilização legal</td>
                    <td>Projeto pronto para implementação</td>
                </tr>
                <tr>
                    <td><strong>4. Execução</strong></td>
                    <td>Oversight, assurance, monitoramento</td>
                    <td>Coordenação de rede, gestão de campo</td>
                    <td>Entrega territorial mensurável</td>
                </tr>
                <tr>
                    <td><strong>5. Reporte</strong></td>
                    <td>Assurance ESG, relatórios integrados</td>
                    <td>Mensuração de impacto, histórias de caso</td>
                    <td>Evidência auditável</td>
                </tr>
            </tbody>
        </table>
    </div>
    
    <div class="slide-number">07</div>
</div>

<!-- ============================================
     SLIDE 8: O FUNDO
     ============================================ -->
<div class="slide">
    <div class="slide-header">
        <div class="logo-epower">
            <svg viewBox="0 0 40 40" width="40" height="40" xmlns="http://www.w3.org/2000/svg">
                <circle cx="20" cy="20" r="8" fill="#C9A24A"/>
            </svg>
            Epower Minds
        </div>
        <div class="logo-bdo">BDO</div>
    </div>
    
    <div class="slide-content">
        <h2>Fundo de Sabedoria Prática ESG</h2>
        
        <div class="conteudo-duas-colunas" style="margin-top: 20px;">
            <div class="coluna-texto">
                <h3>Conceito</h3>
                <p class="texto-medio">Mecanismo de investimento social que prioriza aplicação sobre promessa, mensuração sobre narrativa, continuidade sobre evento isolado.</p>
                
                <div class="destaque" style="margin-top: 30px;">
                    "Sabedoria Prática": conhecimento gerado a partir da execução real, distinto da teoria ou planejamento abstrato.
                </div>
            </div>
            
            <div class="coluna-texto">
                <h3>Papel do Epower Minds</h3>
                <div class="card-info">
                    <h4>Originação</h4>
                    <p>Identificar projetos alinhados a critérios ESG</p>
                </div>
                <div class="card-info">
                    <h4>Due Diligence Social</h4>
                    <p>Avaliar capacidade de execução territorial</p>
                </div>
                <div class="card-info">
                    <h4>Engenharia de Conexão</h4>
                    <p>Articular governo, ONGs, academia</p>
                </div>
                <div class="card-info">
                    <h4>Governança de Campo</h4>
                    <p>Estabelecer gestão compartilhada</p>
                </div>
            </div>
        </div>
    </div>
    
    <div class="slide-number">08</div>
</div>

<!-- ============================================
     SLIDE 9: GOVERNANÇA
     ============================================ -->
<div class="slide">
    <div class="slide-header">
        <div class="logo-epower">
            <svg viewBox="0 0 40 40" width="40" height="40" xmlns="http://www.w3.org/2000/svg">
                <circle cx="20" cy="20" r="8" fill="#C9A24A"/>
            </svg>
            Epower Minds
        </div>
        <div class="logo-bdo">BDO</div>
    </div>
    
    <div class="slide-content">
        <h2>Modelo de Governança Conjunta</h2>
        
        <h3>Comitê de Sabedoria Prática</h3>
        
        <table class="tabela-slide" style="margin-top: 30px;">
            <thead>
                <tr>
                    <th style="width: 20%;">Papel</th>
                    <th style="width: 40%;">BDO</th>
                    <th style="width: 40%;">Epower Minds</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td><strong>Direção Estratégica</strong></td>
                    <td>Critérios ESG, frameworks globais (SBTi, TCFD, ISSB)</td>
                    <td>Tradução para realidade brasileira, adaptação territorial</td>
                </tr>
                <tr>
                    <td><strong>Seleção</strong></td>
                    <td>Risco, viabilidade financeira, compliance</td>
                    <td>Viabilidade territorial, capacidade de execução, timing</td>
                </tr>
                <tr>
                    <td><strong>Oversight</strong></td>
                    <td>Assurance, auditoria, reporte</td>
                    <td>Gestão de campo, coordenação, resolução de impedimentos</td>
                </tr>
                <tr>
                    <td><strong>Mensuração</strong></td>
                    <td>Verificação externa, validação de dados</td>
                    <td>Coleta de dados primários, indicadores de campo</td>
                </tr>
            </tbody>
        </table>
        
        <div style="margin-top: 40px; background: rgba(201, 162, 74, 0.1); padding: 20px; border-radius: 8px; border: 1px solid #C9A24A;">
            <h4 style="color: #C9A24A; margin-bottom: 10px;">Critérios de Priorização</h4>
            <p style="font-size: 16px; margin: 0;">Alinhamento ESG • Viabilidade Territorial • Estação • Escalabilidade • Mensurabilidade</p>
        </div>
    </div>
    
    <div class="slide-number">09</div>
</div>

<!-- ============================================
     SLIDE 10: IMPLEMENTAÇÃO
     ============================================ -->
<div class="slide">
    <div class="slide-header">
        <div class="logo-epower">
            <svg viewBox="0 0 40 40" width="40" height="40" xmlns="http://www.w3.org/2000/svg">
                <circle cx="20" cy="20" r="8" fill="#C9A24A"/>
            </svg>
            Epower Minds
        </div>
        <div class="logo-bdo">BDO</div>
    </div>
    
    <div class="slide-content">
        <h2>Plano de Implementação</h2>
        
        <div class="timeline" style="margin-top: 60px;">
            <div class="timeline-fase">
                <h4>Fase 1</h4>
                <div class="periodo">0-3 meses</div>
                <div class="timeline-dot"></div>
                <p>Formalização de parceria, definição de critérios, constituição do Fundo</p>
            </div>
            <div class="timeline-fase">
                <h4>Fase 2</h4>
                <div class="periodo">3-12 meses</div>
                <div class="timeline-dot"></div>
                <p>3-5 projetos-piloto, validação de metodologia, primeiros resultados</p>
            </div>
            <div class="timeline-fase">
                <h4>Fase 3</h4>
                <div class="periodo">12-24 meses</div>
                <div class="timeline-dot"></div>
                <p>Escala para carteira BDO, produto comercial integrado, fundo de investimento</p>
            </div>
        </div>
        
        <div class="indicadores-row" style="margin-top: 80px;">
            <div class="indicador-card" style="background: rgba(201, 162, 74, 0.1);">
                <span class="indicador-numero" style="font-size: 48px;">MVP</span>
                <span class="indicador-label">Projetos Piloto</span>
                <span class="indicador-sublabel">Validação rápida</span>
            </div>
            <div class="indicador-card" style="background: rgba(26, 166, 166, 0.1);">
                <span class="indicador-numero" style="font-size: 48px;">Scale</span>
                <span class="indicador-label">Expansão</span>
                <span class="indicador-sublabel">Carteira completa</span>
            </div>
            <div class="indicador-card" style="background: rgba(245, 247, 250, 0.1);">
                <span class="indicador-numero" style="font-size: 48px;">Inst.</span>
                <span class="indicador-label">Institucionalização</span>
                <span class="indicador-sublabel">Fundo dedicado</span>
            </div>
        </div>
    </div>
    
    <div class="slide-number">10</div>
</div>

<!-- ============================================
     SLIDE 11: METAS
     ============================================ -->
<div class="slide">
    <div class="slide-header">
        <div class="logo-epower">
            <svg viewBox="0 0 40 40" width="40" height="40" xmlns="http://www.w3.org/2000/svg">
                <circle cx="20" cy="20" r="8" fill="#C9A24A"/>
            </svg>
            Epower Minds
        </div>
        <div class="logo-bdo">BDO</div>
    </div>
    
    <div class="slide-content">
        <h2>Indicadores e Metas - Ano 1</h2>
        
        <div class="indicadores-row" style="margin-top: 40px;">
            <div class="indicador-card">
                <span class="indicador-numero">10</span>
                <span class="indicador-label">Projetos Estruturados</span>
                <span class="indicador-sublabel">Contratos firmados</span>
            </div>
            <div class="indicador-card">
                <span class="indicador-numero">R$5M</span>
                <span class="indicador-label">Recursos Mobilizados</span>
                <span class="indicador-sublabel">Fluxo auditado</span>
            </div>
            <div class="indicador-card">
                <span class="indicador-numero">15</span>
                <span class="indicador-label">Municípios Atendidos</span>
                <span class="indicador-sublabel">Geolocalizado</span>
            </div>
            <div class="indicador-card">
                <span class="indicador-numero">30</span>
                <span class="indicador-label">ONGs Integradas</span>
                <span class="indicador-sublabel">Rede validada</span>
            </div>
        </div>
        
        <div style="margin-top: 60px; display: grid; grid-template-columns: 1fr 1fr; gap: 30px;">
            <div class="card-info" style="margin: 0;">
                <h4>Governança</h4>
                <p style="font-size: 20px; margin: 0;">100% dos projetos com relatório de impacto auditado (assurance BDO)</p>
            </div>
            <div class="card-info" style="margin: 0;">
                <h4>Conhecimento</h4>
                <p style="font-size: 20px; margin: 0;">4 publicações sobre metodologia em veículos relevantes</p>
            </div>
        </div>
    </div>
    
    <div class="slide-number">11</div>
</div>

<!-- ============================================
     SLIDE 12: DIFERENCIAIS
     ============================================ -->
<div class="slide">
    <div class="slide-header">
        <div class="logo-epower">
            <svg viewBox="0 0 40 40" width="40" height="40" xmlns="http://www.w3.org/2000/svg">
                <circle cx="20" cy="20" r="8" fill="#C9A24A"/>
            </svg>
            Epower Minds
        </div>
        <div class="logo-bdo">BDO</div>
    </div>
    
    <div class="slide-content">
        <h2>Diferenciais da Parceria</h2>
        
        <div class="conteudo-duas-colunas" style="margin-top: 20px;">
            <div class="coluna-texto">
                <h3>Para o Mercado ESG</h3>
                <div class="card-info" style="margin-bottom: 25px;">
                    <h4>Fechamento do Ciclo</h4>
                    <p>Da estratégia à rua, do relatório ao resultado real</p>
                </div>
                <div class="card-info" style="margin-bottom: 25px;">
                    <h4>Governança sem Burocracia</h4>
                    <p>Estrutura leve, ágil, mas rigorosa</p>
                </div>
                <div class="card-info" style="margin-bottom: 25px;">
                    <h4>Mensuração Integrada</h4>
                    <p>Indicadores ESG conectados a transformação territorial</p>
                </div>
            </div>
            
            <div class="coluna-texto">
                <h3>Alinhamento Estratégico</h3>
                <div class="card-info" style="margin-bottom: 25px;">
                    <h4>BDO + Epower Minds</h4>
                    <p>Science Based Targets → Metas baseadas em realidade local</p>
                </div>
                <div class="card-info" style="margin-bottom: 25px;">
                    <h4>Responsible Sourcing</h4>
                    <p>Aquisição responsável de projetos sociais, não apenas bens</p>
                </div>
                <div class="card-info" style="margin-bottom: 25px;">
                    <h4>Stakeholder Engagement</h4>
                    <p>Comunidades como stakeholders centrais, não apenas consulta</p>
                </div>
            </div>
        </div>
    </div>
    
    <div class="slide-number">12</div>
</div>

<!-- ============================================
     SLIDE 13: PRÓXIMOS PASSOS
     ============================================ -->
<div class="slide">
    <div class="slide-header">
        <div class="logo-epower">
            <svg viewBox="0 0 40 40" width="40" height="40" xmlns="http://www.w3.org/2000/svg">
                <circle cx="20" cy="20" r="8" fill="#C9A24A"/>
            </svg>
            Epower Minds
        </div>
        <div class="logo-bdo">BDO</div>
    </div>
    
    <div class="slide-content">
        <h2>Próximos Passos</h2>
        
        <div style="margin-top: 40px;">
            <div style="display: flex; align-items: center; margin-bottom: 30px; padding: 25px; background: rgba(201, 162, 74, 0.1); border-radius: 12px; border-left: 4px solid #C9A24A;">
                <div style="font-family: 'Cinzel', serif; font-size: 36px; color: #C9A24A; margin-right: 30px; min-width: 60px;">01</div>
                <div>
                    <h4 style="font-size: 24px; color: #F5F7FA; margin-bottom: 5px;">Apresentação Institucional</h4>
                    <p style="font-size: 18px; color: rgba(245, 247, 250, 0.8); margin: 0;">Diretoria de ESG da BDO Brasil</p>
                </div>
            </div>
            
            <div style="display: flex; align-items: center; margin-bottom: 30px; padding: 25px; background: rgba(201, 162, 74, 0.1); border-radius: 12px; border-left: 4px solid #C9A24A;">
                <div style="font-family: 'Cinzel', serif; font-size: 36px; color: #C9A24A; margin-right: 30px; min-width: 60px;">02</div>
                <div>
                    <h4 style="font-size: 24px; color: #F5F7FA; margin-bottom: 5px;">Workshop de Alinhamento</h4>
                    <p style="font-size: 18px; color: rgba(245, 247, 250, 0.8); margin: 0;">Metodologia e integração de processos</p>
                </div>
            </div>
            
            <div style="display: flex; align-items: center; margin-bottom: 30px; padding: 25px; background: rgba(201, 162, 74, 0.1); border-radius: 12px; border-left: 4px solid #C9A24A;">
                <div style="font-family: 'Cinzel', serif; font-size: 36px; color: #C9A24A; margin-right: 30px; min-width: 60px;">03</div>
                <div>
                    <h4 style="font-size: 24px; color: #F5F7FA; margin-bottom: 5px;">Mapeamento de Oportunidades</h4>
                    <p style="font-size: 18px; color: rgba(245, 247, 250, 0.8); margin: 0;">3 oportunidades imediatas na carteira BDO</p>
                </div>
            </div>
            
            <div style="display: flex; align-items: center; padding: 25px; background: rgba(26, 166, 166, 0.1); border-radius: 12px; border-left: 4px solid #1AA6A6;">
                <div style="font-family: 'Cinzel', serif; font-size: 36px; color: #1AA6A6; margin-right: 30px; min-width: 60px;">04</div>
                <div>
                    <h4 style="font-size: 24px; color: #F5F7FA; margin-bottom: 5px;">Formalização da Parceria</h4>
                    <p style="font-size: 18px; color: rgba(245, 247, 250, 0.8); margin: 0;">Proposta comercial e início da Fase 1</p>
                </div>
            </div>
        </div>
    </div>
    
    <div class="slide-number">13</div>
</div>

<!-- ============================================
     SLIDE 14: FINAL
     ============================================ -->
<div class="slide slide-final">
    <h2>Obrigado</h2>
    
    <div class="frase-final">
        "A BDO traz a precisão do diamante.<br>
        O Epower Minds traz a rota do barco.<br>
        Juntos, chegamos ao celeiro."
    </div>
    
    <div class="contatos-final">
        <div class="contato-box">
            <h4>Epower Minds</h4>
            <p>Ecossistema de Aplicação Social</p>
            <p>contato@epowerminds.org</p>
            <p>www.epowerminds.org</p>
        </div>
        
        <div style="width: 2px; height: 150px; background: rgba(201, 162, 74, 0.3);"></div>
        
        <div class="contato-box">
            <h4>BDO Brasil</h4>
            <p>Advisory e Assurance</p>
            <p>www.bdo.com.br</p>
            <p>São Paulo, SP</p>
        </div>
    </div>
    
    <div style="margin-top: 80px; font-size: 14px; color: rgba(245, 247, 250, 0.5);">
        Documento Confidencial | Fevereiro 2026
    </div>
</div>

</body>
</html>
