---
cssclasses:
  - wide
---

```dataviewjs
// 1. Defina aqui as tags que você quer comparar no gráfico
const tagsParaComparar = ["#Concluido", "#EmProgresso", "#NaoConcluido"];

// 2. Calcula a quantidade de arquivos para cada tag
const contagens = tagsParaComparar.map(tag => dv.pages(tag).length);

// 3. Limpa os nomes das tags para as legendas (remove o # para ficar mais bonito)
const nomesTags = tagsParaComparar.map(tag => tag.replace("#", ""));

const chartData = {
    type: 'doughnut',
    data: {
        labels: nomesTags, // No eixo X aparecerão os nomes das tags
        datasets: [{
            label: 'Total de Arquivos',
            data: contagens,   // No eixo Y aparecerá a contagem total
            backgroundColor: [
                'rgba(75, 192, 192, 0.2)',
                'rgba(54, 162, 235, 0.2)',
                'rgba(255, 206, 86, 0.2)',
                'rgba(255, 99, 132, 0.2)'
            ],
            borderColor: [
                'rgba(75, 192, 192, 1)',
                'rgba(54, 162, 235, 1)',
                'rgba(255, 206, 86, 1)',
                'rgba(255, 99, 132, 1)'
            ],
            borderWidth: 1
        }]
    },
    options: {
		aspectRatio: 5, // Quanto maior o número, menor a altura do gráfico
		plugins: { 
			legend: { 
				position: 'bottom', // Coloca a legenda abaixo do círculo }, 
				datalabels: { color: 'white', // Texto branco para contrastar com as cores das fatias 
				font: { weight: 'bold', size: 14 }, 
				formatter: (value) => value, // Mostra o número puro 
				anchor: 'center', // Centraliza o texto na fatia 
				align: 'center' 
			} 
		}
    }
}
}

window.renderChart(chartData, this.container)
```

```dataviewjs
const concluido = dv.pages("#Concluido").length
dv.table(["Status", "Total"], [["Arquivos Concluídos", concluido]])

const emProgresso = dv.pages("#EmProgresso").length
dv.table(["Status", "Total"], [["Arquivos em progresso", emProgresso]])

const nConcluido = dv.pages("#NaoConcluido").length
dv.table(["Status", "Total"], [["Arquivos Não Concluídos", nConcluido]])
```

---


```dataviewjs
// 1. Definição das tags e coleta de dados
const tagsParaComparar = ["#Concluido", "#EmProgresso", "#NaoConcluido"];
const contagens = tagsParaComparar.map(tag => dv.pages(tag).length);
const nomesTags = tagsParaComparar.map(tag => tag.replace("#", ""));

const chartData = {
    type: 'doughnut',
    data: {
        labels: nomesTags,
        datasets: [{
            label: 'Total',
            data: contagens,
            // Aumentei a opacidade para 0.6 para o texto branco ficar legível
            backgroundColor: [
                'rgba(75, 192, 192, 0.2)',
                'rgba(54, 162, 235, 0.2)',
                'rgba(255, 206, 86, 0.2)',
                'rgba(255, 99, 132, 0.2)'
            ],
            borderColor: [
                'rgba(75, 192, 192, 1)',
                'rgba(54, 162, 235, 1)',
                'rgba(255, 206, 86, 1)',
                'rgba(255, 99, 132, 1)'
            ],
            borderWidth: 1
        }]
    },
    options: {
        // Importante: permite que o gráfico respeite o tamanho do container abaixo
        maintainAspectRatio: false, 
        plugins: {
            legend: {
                position: 'bottom',
            },
            datalabels: {
                color: 'white',
                display: true, // Garante que o label apareça
                font: {
                    weight: 'bold',
                    size: 14
                },
                // Mostra o valor numérico
                formatter: (value) => {
                    // Se o valor for 0, não mostra nada para não poluir
                    return value > 0 ? value : "";
                },
                anchor: 'center', // Fixa o ponto no centro da fatia
                align: 'center'   // Alinha o texto ao centro desse ponto
            }
        }
    }
}

// Criei este container para você controlar o tamanho do gráfico.
// Mude 'width' e 'height' aqui para ajustar o tamanho da rosca.
const container = this.container.createEl("div", { 
    style: "width: 50px; height: 50px; margin: auto;" 
});

window.renderChart(chartData, container);
```

---
