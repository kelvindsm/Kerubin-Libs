---
cssclasses:
  - wide
  - custom-style
banner: "![[biblioteca.png]]"
"":
---

Text displayed above.
--- start-multi-column: ExampleRegion1  
```column-settings  
number of columns: 4
```

Texto 1

--- end-column ---

Texto 2

--- end-column ---

Texto 3

--- end-column ---

Texto 4

--- end-multi-column

---

--- start-multi-column: ExampleRegion2
```column-settings  
number of columns: 4
```

Texto 5

--- end-column ---

Texto 6

--- end-column ---

Texto 7

--- end-column ---

Texto 8

--- end-multi-column

> [!multi-column]
>
>> [!note]+ Lista de tarefas
>> - [ ] (adicione tarefas aqui)
>
>> [!warning]+ Lembretes
>> your notes or lists here. using markdown formatting
>
>> [!summary]+ Outros
>> your notes or lists here. using markdown formatting


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



---

