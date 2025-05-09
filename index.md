---
layout: default
---

## Welcome

I am an Assistant Professor in AI at the Department of Computer Science, University of Copenhagen. My research focuses on deep generative models, robust representation learning, and medical data analysis. I work at the intersection of computer vision, health data science, and responsible AI. This website provides more information about my research, teaching, publications, and academic activities.

---

## Education

- Ph.D. in Medical Imaging, University College London, 2020  
  Disease Progression Modeling and Deep Learning  
- M.Sc. in Electronics Engineering, Sabanci University, 2015  
  Computer Vision and Pattern Analysis  
- M.Sc. in Electrical Engineering, University of Tehran, 2010  
  Communication Systems and Image Analysis  

---

## Research

My research focuses on artificial intelligence with interests in deep machine learning and computer vision methods that are robust, generalizable, and applicable to real-world data. 

- **Deep Generative Models for Images** 🎨  
  Generative adversarial networks, variational autoencoders, and denoising diffusion models  
  Bias mitigation ⚖️, fairness 🧑‍⚖️, privacy 🔐, and quality assessment  

- **Robust Representation Learning** 🤖  
  Unsupervised, self-supervised, and active learning  
  Transfer learning 🔁, domain adaptation, and data augmentation 📊  
  Multimodal, heterogeneous, and time-series data ⏱️  

- **Brain Health Data Analysis** 🧠  
  Disease progression modeling and prediction 🧬  
  Alzheimer’s disease 🧓, stroke, tumors 🧫, and psychiatric disorders  

---

## Teaching

- Advanced Topics in Deep Learning ([Fall 2025](https://kurser.ku.dk/course/ndak24003u/2025-2026))  
- Introduction to Data Science ([Spring 2025](https://kurser.ku.dk/course/ndak16003u))  
- Deep Learning ([Fall 2024](https://kurser.ku.dk/course/ndak24002u/2024-2025))  
- Advanced Topics in Deep Learning ([Fall 2024](https://kurser.ku.dk/course/ndak24003u/2024-2025))  
- Advanced Deep Learning ([Spring 2024](https://kurser.ku.dk/course/ndak22002u/2023-2024))  
- Introduction to Data Science ([Spring 2024](https://kurser.ku.dk/course/ndak16003u/2024-2025))    

---

## Publications

[Full Publication List](/publications/)  

[![Google Scholar](https://img.shields.io/badge/Google%20Scholar-Profile-blue?logo=google-scholar&logoColor=white)](https://scholar.google.com/citations?user=8LoF2mEAAAAJ)  

<div style="display: flex; flex-wrap: wrap; gap: 30px;">
  <div style="width: 320px; height: 190px;">
    <canvas id="papersPerYearChart"></canvas>
  </div>
  <div style="width: 150px; height: 150px;">
    <canvas id="authorshipChart"></canvas>
  </div>
</div>

---

## Students

[Full Student List](/students/)  

<div style="display: flex; flex-wrap: wrap; gap: 10px;">
  <div style="width: 240px; height: 160px;">
    <canvas id="studentsLevelChart"></canvas>
  </div>
  <div style="width: 240px; height: 160px;">
    <canvas id="papersLevelChart"></canvas>
  </div>
</div>

---

## Contact

I am open to supervising Bachelor’s, Master’s, and Ph.D. students interested in computer vision, deep learning, and medical AI. If you are motivated and have a strong background in computer vision, machine learning, applied mathematics, or related areas, feel free to get in touch.  

📧 **Email:** ghazi(at)di.ku.dk  
🏫 **Institution:** Pioneer Centre for AI, Department of Computer Science, University of Copenhagen  
📍 **Address:** Øster Voldgade 3, 1350 Copenhagen, Denmark  

---

<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
<script src="https://cdn.jsdelivr.net/npm/chartjs-plugin-datalabels@2"></script>
<script>
  Chart.register(ChartDataLabels);
  const publicationData = {
    years: ['2015', '2016', '2017', '2018', '2019', '2020', '2021', '2022', '2023', '2024', '2025'],
    papersByYear: [2, 4, 3, 1, 4, 3, 1, 3, 8, 5, 3],
    authors: ['First', 'Last', 'Middle'],
    authorsByOrder: [16, 12, 9],
  };
  // Papers per Year Chart
  new Chart(document.getElementById('papersPerYearChart'), {
    type: 'bar',
    data: {
      labels: publicationData.years,
      datasets: [{
        label: 'Number of Papers',
        data: publicationData.papersByYear,
        backgroundColor: 'rgba(33, 150, 243, 0.2)',
        borderColor: 'rgba(33, 150, 243, 1)',
        borderWidth: 1
      }]
    },
    options: {
      responsive: true,
      plugins: {
        datalabels: {
          display: false
        }
      },      
      scales: {
        y: {
          beginAtZero: true
        }
      }
    }
  });
  // Authorship Order Chart
  new Chart(document.getElementById('authorshipChart'), {
    type: 'pie',
    data: {
      labels: publicationData.authors,
      datasets: [{
        data: publicationData.authorsByOrder,
        backgroundColor: [
          'rgba(100, 149, 237, 0.5)',
          'rgba(60, 179, 113, 0.5)',
          'rgba(255, 160, 122, 0.5)'
        ],
        borderColor: '#fff',
        borderWidth: 1
      }]
    },
    options: {
      plugins: {
        legend: { display: false },
        title: {
          display: true,
          text: 'Authorship',
          font: {
            size: 12
          }
        },
        datalabels: {
          color: '#fff',
          font: {
            weight: 'bold',
            size: 11
          },
          formatter: (value, context) => {
            return context.chart.data.labels[context.dataIndex];
          }
        }
      }
    }
  });
</script>

<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
<script>
  // Data for charts
  const studentsData = {
    levels: ['B.Sc.', 'M.Sc.', 'Ph.D.'],
    studentsByLevel: [10, 13, 3],
    papersByLevel: [2, 10, 1],
  };
  // Number of students per level chart
  new Chart(document.getElementById('studentsLevelChart'), {
    type: 'bar',
    data: {
      labels: studentsData.levels,
      datasets: [{
        label: 'Number of Students',
        data: studentsData.studentsByLevel,
        backgroundColor: 'rgba(75, 192, 192, 0.2)',
        borderColor: 'rgba(75, 192, 192, 1)',
        borderWidth: 1
      }]
    },
    options: {
      responsive: true,
      scales: {
        y: {
          beginAtZero: true
        }
      }
    }
  });
  // Number of papers per level chart
  new Chart(document.getElementById('papersLevelChart'), {
    type: 'bar',
    data: {
      labels: studentsData.levels,
      datasets: [{
        label: 'Number of Papers',
        data: studentsData.papersByLevel,
        backgroundColor: 'rgba(153, 102, 255, 0.2)',
        borderColor: 'rgba(153, 102, 255, 1)',
        borderWidth: 1
      }]
    },
    options: {
      responsive: true,
      scales: {
        y: {
          beginAtZero: true
        }
      }
    }
  });
</script>
