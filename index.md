---
layout: default
title: Mostafa Mehdipour Ghazi, Ph.D.
avatar: "/photo-art.jpg"
---

# Mostafa Mehdipour Ghazi, Ph.D.

![My Photo](/photo-art.jpg)

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

[Full Publication List →](/publications/)  

[Google Scholar →](https://scholar.google.com/citations?user=8LoF2mEAAAAJ)  

---

## Students

[Full Student List →](/students/)  

<div style="display: flex; flex-wrap: wrap; gap: 20px;">
  <div style="width: 250px; height: 150px;">
    <canvas id="studentsLevelChart"></canvas>
  </div>
  <div style="width: 250px; height: 150px;">
    <canvas id="papersLevelChart"></canvas>
  </div>
  <div style="width: 300px; height: 200px;">
    <canvas id="studentsGenderChart"></canvas>
  </div>
  <div style="width: 300px; height: 200px;">
    <canvas id="papersGenderChart"></canvas>
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
  // Sample Data for charts
  const studentsData = {
    levels: ['B.Sc.', 'M.Sc.', 'Ph.D.'],
    gender: ['Male', 'Female'],
    papersByLevel: [10, 13, 3],
    studentsByLevel: [50, 30, 20],
    papersByGender: [8, 5],
    studentsByGender: [17, 9]
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
  // Number of students per gender chart
  new Chart(document.getElementById('studentsGenderChart'), {
    type: 'pie',
    data: {
      labels: studentsData.gender,
      datasets: [{
        label: 'Gender Distribution',
        data: studentsData.studentsByGender,
        backgroundColor: ['rgba(75, 192, 192, 0.2)', 'rgba(255, 99, 132, 0.2)'],
        borderColor: ['rgba(75, 192, 192, 1)', 'rgba(255, 99, 132, 1)'],
        borderWidth: 1
      }]
    },
    options: {
      responsive: true
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
  // Number of papers per gender chart
  new Chart(document.getElementById('papersGenderChart'), {
    type: 'pie',
    data: {
      labels: studentsData.gender,
      datasets: [{
        label: 'Papers by Gender',
        data: studentsData.papersByGender,
        backgroundColor: ['rgba(75, 192, 192, 0.2)', 'rgba(255, 159, 64, 0.2)'],
        borderColor: ['rgba(75, 192, 192, 1)', 'rgba(255, 159, 64, 1)'],
        borderWidth: 1
      }]
    },
    options: {
      responsive: true
    }
  });
</script>
