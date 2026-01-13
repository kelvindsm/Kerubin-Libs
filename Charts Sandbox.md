```dataviewjs
const concluido = dv.pages("#Concluido").length
dv.table(["Status", "Total"], [["Arquivos Concluídos", concluido]])

const nConcluido = dv.pages("#NaoConcluido").length
dv.table(["Status", "Total"], [["Arquivos Não Concluídos", nConcluido]])
```



```dataview
TABLE length(rows) AS "Total Concluído", file.tags FROM #Concluido GROUP BY file.folder AS "Pasta"
```

|       | Test1 | Test2 | Test3 |
| ----- | ----- | ----- | ----- |
| Data1 | 1     | 2     | 3.33  |
| Data2 | 3     | 2     | 1     |
| Data3 | 6.7   | 4     | 2     |
^table

```chart
type: bar
id: table
layout: rows
width: 80%
beginAtZero: true
```


```dataviewjs
// 1. Defina aqui as tags que você quer comparar no gráfico
const tagsParaComparar = ["#Concluido", "#EmProgresso", "#NaoConcluido"];

// 2. Calcula a quantidade de arquivos para cada tag
const contagens = tagsParaComparar.map(tag => dv.pages(tag).length);

// 3. Limpa os nomes das tags para as legendas (remove o # para ficar mais bonito)
const nomesTags = tagsParaComparar.map(tag => tag.replace("#", ""));

const chartData = {
    type: 'bar',
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
	    aspectRatio: 5,
        scales: {
            y: {
                beginAtZero: true,
                ticks: {
                    stepSize: 1 // Garante que a escala use números inteiros
                }
            }
        }
    }
}

window.renderChart(chartData, this.container)
```

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




---


```dataviewjs
const tagsParaComparar = ["#Concluido", "#EmProgresso", "#NaoConcluido"];
const contagens = tagsParaComparar.map(tag => dv.pages(tag).length);
const nomesTags = tagsParaComparar.map(tag => tag.replace("#", ""));

const chartData = {
    type: 'pie', // Alterado para pizza
    data: {
        labels: nomesTags,
        datasets: [{
            data: contagens,
            backgroundColor: [
                'rgba(75, 192, 192, 0.6)',
                'rgba(54, 162, 235, 0.6)',
                'rgba(255, 99, 132, 0.6)'
            ],
            borderColor: [
                'rgba(255, 255, 255, 1)' // Borda branca entre as fatias
            ],
            borderWidth: 2
        }]
    },
    options: {
        maintainAspectRatio: false, // Permite controlar o tamanho via container
        plugins: {
            legend: {
                position: 'bottom', // Coloca a legenda abaixo do círculo
            },
            datalabels: {
                color: '#fff',       // Texto branco para contrastar com as cores das fatias
                font: {
                    weight: 'bold',
                    size: 14
                },
                formatter: (value) => value, // Mostra o número puro
                anchor: 'center',    // Centraliza o texto na fatia
                align: 'center'
            }
        }
    }
}

// Criando um container menor para o gráfico de pizza não ficar gigante
const container = this.container.createEl("div", { 
    style: "width: 350px; height: 350px; margin: auto;" 
});

window.renderChart(chartData, container)
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


