---
layout: default
---

## Welcome

I am an Assistant Professor in AI at the Department of Computer Science, University of Copenhagen. My research focuses on deep generative models, robust representation learning, and medical data analysis. I work at the intersection of computer vision, health data science, and responsible AI. On this website, you can learn more about my research, teaching, publications, and academic activities.

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

- **Deep Generative Models for Images**  
  Generative adversarial networks, variational autoencoders, and denoising diffusion models  
  Bias mitigation, fairness, privacy, and quality assessment  

- **Robust Representation Learning**  
  Unsupervised, self-supervised, and active learning  
  Transfer learning, domain adaptation, and data augmentation  
  Multimodal, heterogeneous, and time-series data  

- **Brain Health Data Analysis**  
  Disease progression modeling and prediction  
  Alzheimer’s disease, stroke, tumors, and psychiatric disorders  

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

[Google Scholar](https://scholar.google.com/citations?user=8LoF2mEAAAAJ)  

<div style="display: flex; flex-wrap: wrap; gap: 10px;">
  <div style="width: 240px; height: 150px;">
    <canvas id="papersPerYearChart"></canvas>
  </div>
  <div style="width: 250px; height: 200px;">
    <canvas id="authorshipChart"></canvas>
  </div>
</div>

---

## Students

[Full Student List](/students/)  

<div style="display: flex; flex-wrap: wrap; gap: 10px;">
  <div style="width: 240px; height: 150px;">
    <canvas id="studentsLevelChart"></canvas>
  </div>
  <div style="width: 240px; height: 150px;">
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
<script>
  // Data for the number of papers chart
  const yearData = {
    labels: ['2015', '2016', '2017', '2018', '2019', '2020', '2021', '2022', '2023', '2024', '2025'],
    datasets: [{
      label: 'Number of Papers',
      data: [2, 4, 3, 1, 3, 4, 1, 3, 6, 6, 5],
      backgroundColor: 'rgba(33, 150, 243, 0.2)',
      borderColor: 'rgba(33, 150, 243, 1)',
      borderWidth: 1
    }]
  };
  // Data for authorship chart
  const authorshipData = {
    labels: ['First Author', 'Last Author', 'Middle Author'],
    datasets: [{
      data: [16, 12, 10],
      backgroundColor: [
      'rgba(102, 187, 255, 0.2)',
      'rgba(129, 199, 132, 0.2)',
      'rgba(255, 183, 77, 0.2)'
      ],
      borderColor: [
      'rgba(102, 187, 255, 1)',
      'rgba(129, 199, 132, 1)',
      'rgba(255, 183, 77, 1)'
      ],
      borderWidth: 1
    }]
  };
  // Number of papers per year chart
  new Chart(document.getElementById('papersPerYearChart'), {
    type: 'bar',
    data: yearData,
    options: {
      scales: {
        y: {
          beginAtZero: true,
          stepSize: 1
        }
      }
    }
  });
  // Authorship chart
  new Chart(document.getElementById('authorshipChart'), {
    type: 'pie',
    data: authorshipData
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
