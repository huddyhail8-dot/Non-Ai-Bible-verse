# Non-Ai-Bible-verse
Bible Scripture on Command
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>E-Commerce Readiness Dashboard</title>
    <!-- Load Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Load Chart.js for data visualization -->
    <script src="https://cdn.jsdelivr.net/npm/chart.js@3.7.1/dist/chart.min.js"></script>
    <!-- Load Lucide icons -->
    <script src="https://unpkg.com/lucide@latest"></script>
    
    <style>
        /* Custom scrollbar styling for better aesthetics */
        ::-webkit-scrollbar {
            width: 8px;
            height: 8px;
        }
        ::-webkit-scrollbar-thumb {
            background-color: #3b82f6; /* Blue-500 */
            border-radius: 4px;
        }
        ::-webkit-scrollbar-track {
            background-color: #1f2937; /* Gray-800 */
        }
        body {
            font-family: 'Inter', sans-serif;
            background-color: #111827; /* Dark background */
        }
        .card {
            background-color: #1f2937; /* Card background */
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2);
            border: 1px solid #374151; /* Subtle border */
        }
    </style>
</head>
<body>

<div id="app" class="min-h-screen p-4 sm:p-6 lg:p-8">
    
    <!-- Header -->
    <header class="mb-8">
        <h1 class="text-3xl font-extrabold text-white sm:text-4xl">E-Commerce Readiness Dashboard</h1>
        <p class="text-lg text-gray-400 mt-1">Q3 2025 Performance Review & Strategic Analysis</p>
    </header>

    <!-- Main Grid Layout -->
    <div class="grid grid-cols-1 lg:grid-cols-4 gap-6">

        <!-- Column 1: Key Metrics (Span 3 columns on large screens) -->
        <div class="lg:col-span-3 space-y-6">
            
            <!-- Key Performance Indicators (KPIs) -->
            <div class="grid grid-cols-2 md:grid-cols-4 gap-4">
                
                <!-- Card 1: Revenue -->
                <div class="card p-5 rounded-xl transition hover:ring-2 hover:ring-blue-500">
                    <div class="flex items-center justify-between">
                        <span class="text-sm font-medium text-gray-400">Total Revenue</span>
                        <i data-lucide="line-chart" class="w-5 h-5 text-green-400"></i>
                    </div>
                    <p class="text-3xl font-bold text-white mt-2">$1.8M</p>
                    <p class="text-sm text-green-400 mt-1 flex items-center">
                        <i data-lucide="arrow-up" class="w-4 h-4 mr-1"></i>
                        +12.5% vs Last Q
                    </p>
                </div>

                <!-- Card 2: Conversion Rate -->
                <div class="card p-5 rounded-xl transition hover:ring-2 hover:ring-blue-500">
                    <div class="flex items-center justify-between">
                        <span class="text-sm font-medium text-gray-400">Conversion Rate</span>
                        <i data-lucide="check-circle" class="w-5 h-5 text-purple-400"></i>
                    </div>
                    <p class="text-3xl font-bold text-white mt-2">3.1%</p>
                    <p class="text-sm text-yellow-400 mt-1 flex items-center">
                        <i data-lucide="minus" class="w-4 h-4 mr-1"></i>
                        0.0% vs Last Q
                    </p>
                </div>

                <!-- Card 3: New Customers -->
                <div class="card p-5 rounded-xl transition hover:ring-2 hover:ring-blue-500">
                    <div class="flex items-center justify-between">
                        <span class="text-sm font-medium text-gray-400">New Customers</span>
                        <i data-lucide="users" class="w-5 h-5 text-red-400"></i>
                    </div>
                    <p class="text-3xl font-bold text-white mt-2">4,521</p>
                    <p class="text-sm text-red-400 mt-1 flex items-center">
                        <i data-lucide="arrow-down" class="w-4 h-4 mr-1"></i>
                        -5.8% vs Last Q
                    </p>
                </div>

                <!-- Card 4: Average Order Value -->
                <div class="card p-5 rounded-xl transition hover:ring-2 hover:ring-blue-500">
                    <div class="flex items-center justify-between">
                        <span class="text-sm font-medium text-gray-400">AOV</span>
                        <i data-lucide="dollar-sign" class="w-5 h-5 text-cyan-400"></i>
                    </div>
                    <p class="text-3xl font-bold text-white mt-2">$88.90</p>
                    <p class="text-sm text-green-400 mt-1 flex items-center">
                        <i data-lucide="arrow-up" class="w-4 h-4 mr-1"></i>
                        +3.2% vs Last Q
                    </p>
                </div>
            </div>

            <!-- Revenue and Traffic Chart -->
            <div class="card p-6 rounded-xl h-[400px]">
                <h2 class="text-xl font-semibold text-white mb-4">Quarterly Revenue & Session Trends</h2>
                <div class="h-full">
                    <canvas id="revenueTrafficChart"></canvas>
                </div>
            </div>

            <!-- Regional Performance Table -->
            <div class="card p-6 rounded-xl">
                <h2 class="text-xl font-semibold text-white mb-4">Regional Sales Performance (Q3)</h2>
                <div class="overflow-x-auto">
                    <table class="min-w-full divide-y divide-gray-700">
                        <thead class="bg-gray-800">
                            <tr>
                                <th scope="col" class="px-4 py-3 text-left text-xs font-medium text-gray-400 uppercase tracking-wider rounded-tl-lg">Region</th>
                                <th scope="col" class="px-4 py-3 text-left text-xs font-medium text-gray-400 uppercase tracking-wider">Sales ($)</th>
                                <th scope="col" class="px-4 py-3 text-left text-xs font-medium text-gray-400 uppercase tracking-wider">Growth (YoY)</th>
                                <th scope="col" class="px-4 py-3 text-left text-xs font-medium text-gray-400 uppercase tracking-wider rounded-tr-lg">Readiness Score</th>
                            </tr>
                        </thead>
                        <tbody class="divide-y divide-gray-800 text-gray-300">
                            <tr class="hover:bg-gray-800 transition">
                                <td class="px-4 py-3 whitespace-nowrap font-medium">North America</td>
                                <td class="px-4 py-3 whitespace-nowrap text-green-400">$850,000</td>
                                <td class="px-4 py-3 whitespace-nowrap text-green-400">+18%</td>
                                <td class="px-4 py-3 whitespace-nowrap"><span class="px-2 inline-flex text-xs leading-5 font-semibold rounded-full bg-green-900 text-green-300">92/100</span></td>
                            </tr>
                            <tr class="hover:bg-gray-800 transition">
                                <td class="px-4 py-3 whitespace-nowrap font-medium">Europe</td>
                                <td class="px-4 py-3 whitespace-nowrap text-green-400">$610,000</td>
                                <td class="px-4 py-3 whitespace-nowrap text-green-400">+10%</td>
                                <td class="px-4 py-3 whitespace-nowrap"><span class="px-2 inline-flex text-xs leading-5 font-semibold rounded-full bg-blue-900 text-blue-300">85/100</span></td>
                            </tr>
                            <tr class="hover:bg-gray-800 transition">
                                <td class="px-4 py-3 whitespace-nowrap font-medium">Asia-Pacific</td>
                                <td class="px-4 py-3 whitespace-nowrap text-red-400">$340,000</td>
                                <td class="px-4 py-3 whitespace-nowrap text-red-400">-2%</td>
                                <td class="px-4 py-3 whitespace-nowrap"><span class="px-2 inline-flex text-xs leading-5 font-semibold rounded-full bg-red-900 text-red-300">68/100</span></td>
                            </tr>
                        </tbody>
                    </table>
                </div>
            </div>

        </div> <!-- End Column 1 -->

        <!-- Column 2: Conversion Funnel and Mobile Readiness (Span 1 column on large screens) -->
        <div class="lg:col-span-1 space-y-6">
            
            <!-- Conversion Funnel Chart -->
            <div class="card p-6 rounded-xl h-[400px]">
                <h2 class="text-xl font-semibold text-white mb-4">Conversion Funnel Drop-off</h2>
                <div class="h-full">
                    <canvas id="funnelChart"></canvas>
                </div>
            </div>

            <!-- Mobile Readiness Score -->
            <div class="card p-6 rounded-xl">
                <h2 class="text-xl font-semibold text-white mb-4 flex items-center">
                    Mobile Readiness 
                    <i data-lucide="smartphone" class="w-5 h-5 text-blue-400 ml-2"></i>
                </h2>
                <div class="text-center">
                    <div id="mobileScoreRing" class="relative w-32 h-32 mx-auto">
                        <!-- SVG for circular progress bar -->
                        <svg viewBox="0 0 36 36" class="circular-chart text-blue-500 transform -rotate-90">
                            <path class="circle-bg"
                                d="M18 2.0845
                                a 15.9155 15.9155 0 0 1 0 31.831
                                a 15.9155 15.9155 0 0 1 0 -31.831"
                                fill="none"
                                stroke="#374151" /* Gray-700 */
                                stroke-width="3"
                            />
                            <path class="circle"
                                stroke-dasharray="85, 100"
                                d="M18 2.0845
                                a 15.9155 15.9155 0 0 1 0 31.831
                                a 15.9155 15.9155 0 0 1 0 -31.831"
                                fill="none"
                                stroke="currentColor"
                                stroke-width="3"
                                stroke-linecap="round"
                                id="mobileScorePath"
                            />
                        </svg>
                        <div class="absolute inset-0 flex items-center justify-center">
                            <span class="text-3xl font-extrabold text-blue-400">85%</span>
                        </div>
                    </div>
                    <p class="text-sm text-gray-400 mt-3">Mobile conversion is 1.2% lower than Desktop.</p>
                    <button class="mt-4 w-full py-2 bg-blue-600 hover:bg-blue-700 text-white font-semibold rounded-lg transition duration-200">
                        View Audit Report
                    </button>
                </div>
            </div>

            <!-- Action Items -->
            <div class="card p-6 rounded-xl">
                <h2 class="text-xl font-semibold text-white mb-4 flex items-center">
                    Action Items 
                    <i data-lucide="clipboard-list" class="w-5 h-5 text-yellow-400 ml-2"></i>
                </h2>
                <ul class="space-y-3">
                    <li class="flex items-start text-gray-300">
                        <i data-lucide="alert-triangle" class="w-4 h-4 text-yellow-500 mr-2 mt-1 flex-shrink-0"></i>
                        <span class="text-sm">Investigate APAC region sales drop (-2%).</span>
                    </li>
                    <li class="flex items-start text-gray-300">
                        <i data-lucide="trending-up" class="w-4 h-4 text-green-500 mr-2 mt-1 flex-shrink-0"></i>
                        <span class="text-sm">Optimize Checkout page to reduce funnel drop-off (40%).</span>
                    </li>
                    <li class="flex items-start text-gray-300">
                        <i data-lucide="bug" class="w-4 h-4 text-red-500 mr-2 mt-1 flex-shrink-0"></i>
                        <span class="text-sm">Fix reported bug: Empty cart after login (priority high).</span>
                    </li>
                </ul>
            </div>

        </div> <!-- End Column 2 -->

    </div> <!-- End Main Grid -->

    <!-- Footer -->
    <footer class="mt-8 text-center text-gray-500 text-sm">
        Dashboard Data as of September 30, 2025. All rights reserved.
    </footer>

</div>

<script>
    // Initialize Lucide icons
    lucide.createIcons();

    // --- CHART DATA AND CONFIGURATION ---

    // 1. Revenue and Traffic Line/Bar Chart
    const revenueTrafficCtx = document.getElementById('revenueTrafficChart').getContext('2d');
    
    // Create gradient for the Revenue area under the line
    const revenueGradient = revenueTrafficCtx.createLinearGradient(0, 0, 0, 400);
    revenueGradient.addColorStop(0, 'rgba(16, 185, 129, 0.4)'); // Green-500
    revenueGradient.addColorStop(1, 'rgba(16, 185, 129, 0)');

    const revenueTrafficChart = new Chart(revenueTrafficCtx, {
        type: 'line',
        data: {
            labels: ['Jul', 'Aug', 'Sep', 'Oct', 'Nov', 'Dec'],
            datasets: [
                {
                    type: 'line',
                    label: 'Revenue ($K)',
                    data: [250, 280, 320, 350, 400, 450],
                    borderColor: '#10b981', // Green-500
                    backgroundColor: revenueGradient,
                    fill: 'origin',
                    tension: 0.4,
                    yAxisID: 'y1'
                },
                {
                    type: 'bar',
                    label: 'Sessions (K)',
                    data: [120, 135, 150, 160, 180, 200],
                    backgroundColor: '#60a5fa', // Blue-400
                    yAxisID: 'y2',
                    borderRadius: 4,
                }
            ]
        },
        options: {
            responsive: true,
            maintainAspectRatio: false,
            plugins: {
                legend: {
                    labels: {
                        color: '#9ca3af' // Gray-400
                    }
                },
                title: {
                    display: false,
                }
            },
            scales: {
                x: {
                    grid: {
                        display: false,
                        borderColor: '#374151'
                    },
                    ticks: {
                        color: '#9ca3af'
                    }
                },
                y1: {
                    type: 'linear',
                    position: 'left',
                    grid: {
                        color: '#374151',
                    },
                    ticks: {
                        color: '#9ca3af',
                        callback: function(value) {
                            return '$' + value + 'K';
                        }
                    }
                },
                y2: {
                    type: 'linear',
                    position: 'right',
                    grid: {
                        drawOnChartArea: false,
                        borderColor: '#374151'
                    },
                    ticks: {
                        color: '#9ca3af',
                        callback: function(value) {
                            return value + 'K';
                        }
                    }
                }
            }
        }
    });

    // 2. Conversion Funnel Chart (Horizontal Bar Chart simulating a funnel)
    const funnelCtx = document.getElementById('funnelChart').getContext('2d');

    const funnelData = [100000, 60000, 36000, 18000]; // Sessions, Views, Carts, Purchases
    const funnelLabels = ['Sessions', 'Product Views', 'Added to Cart', 'Purchases'];
    
    // Calculate percentages for display (optional)
    const funnelPercentages = funnelData.map((value, index) => {
        if (index === 0) return '100%';
        return (value / funnelData[0] * 100).toFixed(1) + '%';
    });


    // Custom plugin to draw the labels inside the bars
    const insideLabelPlugin = {
        id: 'insideLabel',
        beforeDraw: (chart) => {
            const ctx = chart.ctx;
            ctx.save();
            ctx.font = 'bold 12px Inter, sans-serif';
            ctx.fillStyle = '#1f2937'; // Dark text for contrast
            ctx.textAlign = 'right';
            ctx.textBaseline = 'middle';

            chart.data.datasets.forEach((dataset, i) => {
                const meta = chart.getDatasetMeta(i);
                if (meta.type !== 'bar') return;

                meta.data.forEach((bar, index) => {
                    const label = funnelPercentages[index];
                    const x = bar.x - 10; // Position label slightly to the left of the bar end
                    const y = bar.y;

                    // Only draw if the bar is wide enough
                    if (bar.width > 50) {
                        ctx.fillText(label, x, y);
                    }
                });
            });
            ctx.restore();
        }
    };


    const funnelChart = new Chart(funnelCtx, {
        type: 'bar',
        data: {
            labels: funnelLabels,
            datasets: [{
                label: 'Users',
                data: funnelData.slice().reverse(), // Reverse to display funnel top-down
                backgroundColor: ['#f87171', '#fbbf24', '#60a5fa', '#10b981'].reverse(), // Red, Yellow, Blue, Green (reversed)
                borderColor: '#111827',
                borderWidth: 1
            }]
        },
        options: {
            indexAxis: 'y', // Make it horizontal
            responsive: true,
            maintainAspectRatio: false,
            plugins: {
                legend: {
                    display: false,
                },
                tooltip: {
                    callbacks: {
                        label: function(context) {
                            let label = context.dataset.label || '';
                            if (label) {
                                label += ': ';
                            }
                            if (context.parsed.x !== null) {
                                label += new Intl.NumberFormat('en-US').format(context.parsed.x);
                            }
                            return label + ' Users';
                        },
                        afterLabel: function(context) {
                             const index = context.dataIndex;
                             return `Retention: ${funnelPercentages.slice().reverse()[index]}`;
                        }
                    }
                }
            },
            scales: {
                x: {
                    beginAtZero: true,
                    grid: {
                        color: '#374151',
                    },
                    ticks: {
                        color: '#9ca3af',
                        callback: function(value) {
                            return value / 1000 + 'K';
                        }
                    },
                    title: {
                        display: true,
                        text: 'User Count',
                        color: '#9ca3af'
                    }
                },
                y: {
                    grid: {
                        display: false,
                    },
                    ticks: {
                        color: '#9ca3af'
                    }
                }
            }
        },
        plugins: [insideLabelPlugin]
    });
</script>

</body>
</html>
