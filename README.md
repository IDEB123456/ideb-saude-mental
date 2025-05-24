<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>IDEB Saúde Mental - Inovação em Psicologia</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap" rel="stylesheet">
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #0f172a; /* Dark Blue Background */
            color: #e0f2fe; /* Light Blue Text */
        }
        .nav-link {
            @apply px-4 py-2 text-sm font-medium text-teal-300 hover:text-teal-500 transition-colors duration-200;
        }
        .active-nav-link {
            @apply text-teal-500 border-b-2 border-teal-500;
        }
        .section-title {
            @apply text-3xl font-bold text-teal-400 mb-6 text-center;
        }
        .card {
            @apply bg-slate-800 p-6 rounded-lg shadow-lg transition-shadow duration-300 hover:shadow-xl;
        }
        .hero {
            position: relative;
            overflow: hidden;
            height: 80vh;
        }
        .hero-image {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            object-fit: cover;
            animation: parallax 10s linear infinite alternate;
        }
        .hero-content {
            position: relative;
            z-index: 10;
            text-align: center;
            padding-top: 20vh;
        }
        @keyframes parallax {
            0% { transform: translateY(0); }
            100% { transform: translateY(-20px); }
        }
        .expansion-step {
            @apply flex items-center p-4 bg-slate-700 rounded-lg shadow-md mb-3;
        }
        .expansion-number {
            @apply flex-shrink-0 w-10 h-10 bg-teal-500 text-white rounded-full flex items-center justify-center font-bold text-lg mr-4;
        }
        .accent-text {
            color: #2dd4cf; /* Teal accent */
        }
        .section-intro {
            @apply text-lg text-gray-300 mb-8 max-w-3xl mx-auto text-center;
        }
        .fade-in {
            animation: fadeIn 1s ease-in-out;
        }
        @keyframes fadeIn {
            0% { opacity: 0; transform: translateY(20px); }
            100% { opacity: 1; transform: translateY(0); }
        }
        .card-reveal {
            max-height: 200px;
            overflow: hidden;
            transition: max-height 0.5s ease-in-out;
            cursor: pointer;
        }
        .card-reveal.expanded {
            max-height: 800px;
        }
        .chart-container {
            position: relative;
            width: 100%;
            max-width: 800px; /* Max width for chart container */
            margin-left: auto;
            margin-right: auto;
            height: 450px; /* Base height for chart */
            max-height: 550px; /* Max height for chart */
        }
        @media (min-width: 768px) {
            .chart-container {
                height: 500px;
            }
        }
        .ideb-highlight {
            background: linear-gradient(to right, #facc15, #ea580c); /* Amarelo para Laranja */
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            font-weight: 700;
        }
    </style>
</head>
<body class="antialiased">

    <header class="hero">
        <img src="https://placehold.co/1920x1080/0F172A/2DD4CF?text=IMAGEM+IMPRESSIONANTE+AQUI" alt="Fundo abstrato e dinâmico para o site do IDEB Saúde Mental" class="hero-image">
        <div class="hero-content">
            <h1 class="text-4xl font-bold text-white mb-4">IDEB Saúde Mental</h1>
            <p class="text-xl text-teal-200">Transformando a psicologia com inovação e excelência.</p>
        </div>
    </header>

    <nav class="bg-slate-900 sticky top-0 z-50">
        <div class="container mx-auto px-6 py-4 flex flex-col sm:flex-row justify-between items-center">
            <div class="hidden sm:block"></div>
            <h1 class="text-2xl font-bold text-teal-400">IDEB</h1>
            <nav class="mt-4 sm:mt-0">
                <a href="#visao" class="nav-link active-nav-link" data-target="visao">Visão</a>
                <a href="#estrategia" class="nav-link" data-target="estrategia">Estratégia</a>
                <a href="#papel" class="nav-link" data-target="papel">Nosso Papel</a>
                <a href="#iniciativas" class="nav-link" data-target="iniciativas">Iniciativas</a>
                <a href="#estatisticas" class="nav-link" data-target="estatisticas">Estatísticas</a>
            </nav>
        </div>
    </nav>

    <main class="container mx-auto px-6 py-12">

        <section id="visao" class="py-16 fade-in">
            <h2 class="section-title">Visão e Abrangência do IDEB</h2>
            <p class="section-intro">
                O IDEB busca revolucionar a saúde mental, expandindo sua influência desde o Agreste Pernambucano até toda a América Latina.
            </p>
            <div class="grid md:grid-cols-2 gap-8 items-center">
                <div class="card">
                    <h3 class="text-2xl font-semibold text-teal-400 mb-4">Objetivo Principal</h3>
                    <p class="text-gray-300 text-lg">
                        Ser a <strong class="accent-text">referência</strong> em Saúde Mental.
                    </p>
                </div>
                <div class="card">
                    <h3 class="text-2xl font-semibold text-teal-400 mb-4">Expansão Geográfica</h3>
                    <div class="space-y-3">
                        <div class="expansion-step">
                            <div class="expansion-number">1</div>
                            <p class="text-gray-300">Agreste Pernambucano</p>
                        </div>
                        <div class="expansion-step">
                            <div class="expansion-number">2</div>
                            <p class="text-gray-300">Pernambuco</p>
                        </div>
                        <div class="expansion-step">
                            <div class="expansion-number">3</div>
                            <p class="text-gray-300">Nordeste</p>
                        </div>
                        <div class="expansion-step">
                            <div class="expansion-number">4</div>
                            <p class="text-gray-300">Brasil</p>
                        </div>
                        <div class="expansion-step">
                            <div class="expansion-number">5</div>
                            <p class="text-gray-300">América Latina</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section id="estrategia" class="py-16 bg-slate-900 rounded-lg fade-in">
            <h2 class="section-title">Estratégia de Implementação</h2>
            <p class="section-intro">
                A estratégia do IDEB se apoia em parcerias estratégicas e no reconhecimento dos desafios atuais da psicologia.
            </p>
            <div class="grid md:grid-cols-2 gap-8">
                <div class="card">
                    <h3 class="text-2xl font-semibold text-teal-400 mb-4">Pilares</h3>
                    <ul class="list-disc list-inside space-y-2 text-gray-300">
                        <li>
                            <strong>Apoio Institucional:</strong> Conselho Regional de Psicologia (CRP).
                        </li>
                        <li>
                            <strong>Parcerias Acadêmicas:</strong> Faculdades, como a Maurício de Nassau.
                        </li>
                    </ul>
                </div>
                <div class="card bg-slate-700 border-l-4 border-teal-500 card-reveal" onclick="this.classList.toggle('expanded')">
                    <h3 class="text-2xl font-semibold text-teal-400 mb-4">Desafios (Clique para expandir)</h3>
                    <p class="text-gray-300">
                        O CRP, apesar de cobrar anuidade, não promove o desenvolvimento da psicologia, resultando em perda de credibilidade para psicanalistas e terapeutas. O IDEB surge para suprir essa lacuna.
                    </p>
                </div>
            </div>
        </section>

        <section id="papel" class="py-16 fade-in">
            <h2 class="section-title">O Papel do IDEB na Psicologia</h2>
            <p class="section-intro">
                O IDEB complementa a formação acadêmica e preenche as lacunas deixadas pelos órgãos reguladores, aprofundando a intervenção psicoterapêutica.
            </p>
            <div class="grid md:grid-cols-2 gap-8">
                <div class="card">
                    <div class="flex items-center mb-3">
                        <span class="text-3xl mr-3">🎓</span>
                        <h3 class="text-2xl font-semibold text-teal-400">Complementar à Academia</h3>
                    </div>
                    <p class="text-gray-300">
                        A faculdade oferece apenas a base; o IDEB aprofunda a prática.
                    </p>
                </div>
                <div class="card">
                    <div class="flex items-center mb-3">
                        <span class="text-3xl mr-3">🧩</span>
                        <h3 class="text-2xl font-semibold text-teal-400">Preencher Lacunas</h3>
                    </div>
                    <p class="text-gray-300">
                        O IDEB faz o que o Conselho Federal de Psicologia (CFP) deveria fazer.
                    </p>
                </div>
            </div>
        </section>

        <section id="iniciativas" class="py-16 bg-slate-900 rounded-lg fade-in">
            <h2 class="section-title">Iniciativas e Propostas do IDEB</h2>
            <p class="section-intro">
                Ações concretas para promover o conhecimento, a excelência e a saúde mental.
            </p>
            <div class="grid md:grid-cols-2 gap-8">
                <div class="card">
                    <div class="flex items-center mb-3">
                        <span class="text-3xl mr-3">🗓️</span>
                        <h3 class="text-2xl font-semibold text-teal-400">Congresso de Psicologia</h3>
                    </div>
                    <p class="text-gray-300 mb-2">
                        Primeiro congresso do Agreste Pernambucano.
                    </p>
                    <p class="text-gray-300"><strong>Data:</strong> <strong class="accent-text">6 de Novembro</strong></p>
                </div>
                <div class="card">
                    <div class="flex items-center mb-3">
                        <span class="text-3xl mr-3">🏅</span>
                        <h3 class="text-2xl font-semibold text-teal-400">Selo IDEB</h3>
                    </div>
                    <p class="text-gray-300">
                        Certificação de excelência para psicólogos.
                    </p>
                </div>
            </div>
        </section>

        <section id="estatisticas" class="py-16 fade-in">
            <h2 class="section-title">O Desafio da Ansiedade e a Solução <span class="ideb-highlight">IDEB</span></h2>
            <p class="section-intro">
                Os dados da Organização Pan-Americana da Saúde (OPAS/OMS) e as estimativas do IBGE (2024) revelam um cenário desafiador: **milhões de pessoas sofrem com transtornos de ansiedade no Brasil.** No Agreste Pernambucano, esse quantitativo de indivíduos ansiosos está ativamente buscando por **profissionais de Saúde Mental de excelência**. É aqui que o **<span class="ideb-highlight">IDEB</span>** entra.
            </p>
            <div class="card">
                <h3 class="text-2xl font-semibold text-teal-400 mb-4 text-center">Prevalência de Transtornos de Ansiedade (OPAS/OMS e IBGE 2024)</h3>
                <div class="chart-container">
                    <canvas id="anxietyChart"></canvas>
                </div>
                <p class="text-gray-300 text-sm mt-6 text-center">
                    Com cerca de **19.77 milhões de brasileiros** (9,3% da população de 212,6 milhões) e aproximadamente **186 mil pessoas** no Agreste Pernambucano (9,3% de 2 milhões) convivendo com a ansiedade, a necessidade por profissionais qualificados é imensa. O **<span class="ideb-highlight">IDEB</span>** se posicionará como o selo de competência e a referência para quem busca excelência em saúde mental. Profissionais com o selo **<span class="ideb-highlight">IDEB</span>** serão reconhecidos como a vanguarda da psicologia.
                </p>
            </div>
        </section>

    </main>

    <footer class="bg-slate-800 text-slate-300 py-8 text-center">
        <p>&copy; 2025 IDEB Saúde Mental. Todos os direitos reservados.</p>
        <p class="text-sm">Transformando a psicologia com inovação e excelência.</p>
    </footer>

    <script>
        document.addEventListener('DOMContentLoaded', () => {
            const navLinks = document.querySelectorAll('nav a.nav-link');
            const sections = document.querySelectorAll('main section');

            navLinks.forEach(link => {
                link.addEventListener('click', (event) => {
                    event.preventDefault();
                    const targetId = link.getAttribute('href').substring(1);
                    const targetSection = document.getElementById(targetId);

                    if (targetSection) {
                        window.scrollTo({
                            top: targetSection.offsetTop - 80,
                            behavior: 'smooth'
                        });
                    }
                });
            });

            const observerOptions = {
                root: null,
                rootMargin: '0px',
                threshold: 0.4
            };

            const observerCallback = (entries, observer) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        navLinks.forEach(link => {
                            link.classList.remove('active-nav-link');
                            if (link.getAttribute('href').substring(1) === entry.target.id) {
                                link.classList.add('active-nav-link');
                            }
                        });
                    }
                });
            };

            const observer = new IntersectionObserver(observerCallback, observerOptions);
            sections.forEach(section => observer.observe(section));

            // Chart.js Initialization
            const ctx = document.getElementById('anxietyChart').getContext('2d');
            const anxietyChart = new Chart(ctx, {
                type: 'bar',
                data: {
                    labels: ['Brasil', 'Agreste Pernambucano'],
                    datasets: [{
                        label: 'Pessoas Afetadas (Milhões)',
                        data: [19.77, 0.186],
                        backgroundColor: [
                            'rgba(45, 212, 191, 0.8)',
                            'rgba(6, 182, 212, 0.8)'
                        ],
                        borderColor: [
                            'rgba(45, 212, 191, 1)',
                            'rgba(6, 182, 212, 1)'
                        ],
                        borderWidth: 1
                    },
                    {
                        label: 'Percentual da População (%)',
                        data: [9.3, 9.3],
                        backgroundColor: [
                            'rgba(14, 165, 233, 0.6)',
                            'rgba(34, 197, 94, 0.6)'
                        ],
                        borderColor: [
                            'rgba(14, 165, 233, 1)',
                            'rgba(34, 197, 94, 1)'
                        ],
                        borderWidth: 1,
                        type: 'line',
                        yAxisID: 'percentageAxis',
                        tension: 0.3
                    }]
                },
                options: {
                    responsive: true,
                    maintainAspectRatio: false,
                    plugins: {
                        legend: {
                            labels: {
                                color: '#e0f2fe'
                            }
                        },
                        tooltip: {
                            callbacks: {
                                label: function(context) {
                                    let label = context.dataset.label || '';
                                    if (label) {
                                        label += ': ';
                                    }
                                    if (context.parsed.y !== null) {
                                        if (context.dataset.label.includes('Milhões')) {
                                            label += context.parsed.y.toLocaleString('pt-BR', { minimumFractionDigits: 1, maximumFractionDigits: 3 }) + ' milhões de pessoas';
                                        } else {
                                            label += context.parsed.y + '% da população';
                                        }
                                    }
                                    return label;
                                },
                                title: function(context) {
                                    const title = context[0].label;
                                    if (title.length > 16) {
                                        return title.match(/.{1,16}/g);
                                    }
                                    return title;
                                }
                            }
                        }
                    },
                    scales: {
                        y: {
                            beginAtZero: true,
                            title: {
                                display: true,
                                text: 'Número de Pessoas Afetadas (Milhões)',
                                color: '#e0f2fe'
                            },
                            ticks: {
                                color: '#e0f2fe',
                                callback: function(value) {
                                    return value + 'M';
                                }
                            },
                            grid: {
                                color: 'rgba(224, 242, 254, 0.1)'
                            }
                        },
                        percentageAxis: {
                            type: 'linear',
                            position: 'right',
                            beginAtZero: true,
                            max: 100,
                            title: {
                                display: true,
                                text: 'Percentual da População (%)',
                                color: '#e0f2fe'
                            },
                            ticks: {
                                color: '#e0f2fe',
                                callback: function(value) {
                                    return value + '%';
                                }
                            },
                            grid: {
                                drawOnChartArea: false,
                                color: 'rgba(224, 242, 254, 0.1)'
                            }
                        },
                        x: {
                            title: {
                                display: true,
                                text: 'Região',
                                color: '#e0f2fe'
                            },
                            ticks: {
                                color: '#e0f2fe',
                                callback: function(value, index, values) {
                                    const label = this.getLabelForValue(value);
                                    if (label.length > 16) {
                                        return label.match(/.{1,16}/g);
                                    }
                                    return label;
                                }
                            },
                            grid: {
                                color: 'rgba(224, 242, 254, 0.1)'
                            }
                        }
                    }
                });
            });
        </script>

    </body>
    </html>
