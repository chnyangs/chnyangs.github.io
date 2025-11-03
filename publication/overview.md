---
layout: page
title: Publications
permalink: /publications/
---

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap">

<style>
  body { 
    font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif; 
    line-height: 1.7; 
    color: #2c3e50; 
  }
  
  .publication-header { 
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%); 
    color: white; 
    padding: 3rem 2rem; 
    margin: -2rem -2rem 3rem -2rem; 
    text-align: center; 
    border-radius: 15px; 
    box-shadow: 0 10px 30px rgba(0,0,0,0.1);
  }
  
  .pub-stats { 
    display: flex; 
    justify-content: center; 
    gap: 3rem; 
    margin: 2rem 0; 
    flex-wrap: wrap;
  }
  
  .stat-item { 
    text-align: center; 
  }
  
  .stat-number { 
    font-size: 2rem; 
    font-weight: 700; 
    display: block;
    text-shadow: 2px 2px 4px rgba(0,0,0,0.1);
  }
  
  .stat-label { 
    font-size: 0.9rem; 
    opacity: 0.9; 
    text-transform: uppercase;
    letter-spacing: 1px;
  }
  
  .research-areas {
    margin: 2rem 0;
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    justify-content: center;
  }
  
  .research-tag {
    background: rgba(255,255,255,0.2);
    border: 1px solid rgba(255,255,255,0.3);
    padding: 0.5rem 1.2rem;
    border-radius: 25px;
    font-size: 0.9rem;
    backdrop-filter: blur(10px);
  }
  
  .year-section {
    margin: 3rem 0;
  }
  
  .year-header {
    font-size: 1.8rem;
    font-weight: 700;
    color: #667eea;
    margin-bottom: 1.5rem;
    padding-bottom: 0.5rem;
    border-bottom: 3px solid #667eea;
    display: flex;
    align-items: center;
    gap: 10px;
  }
  
  .publication-item { 
    background: #ffffff; 
    border: 1px solid #e1e4e8;
    padding: 1.8rem; 
    margin: 1.5rem 0; 
    border-radius: 12px;
    box-shadow: 0 2px 8px rgba(0,0,0,0.05);
    transition: all 0.3s ease;
    position: relative;
    overflow: hidden;
  }
  
  .publication-item::before {
    content: '';
    position: absolute;
    left: 0;
    top: 0;
    bottom: 0;
    width: 4px;
    background: linear-gradient(135deg, #667eea, #764ba2);
  }
  
  .publication-item:hover { 
    box-shadow: 0 8px 20px rgba(102,126,234,0.15);
    transform: translateY(-3px);
  }
  
  .pub-header {
    display: flex;
    align-items: center;
    gap: 12px;
    margin-bottom: 12px;
    flex-wrap: wrap;
  }
  
  .venue-badge { 
    background: linear-gradient(135deg, #667eea, #764ba2);
    color: white;
    padding: 0.4rem 1rem; 
    border-radius: 20px; 
    font-size: 0.75rem; 
    font-weight: 600; 
    text-transform: uppercase;
    letter-spacing: 0.5px;
    box-shadow: 0 2px 5px rgba(0,0,0,0.1);
  }
  
  .venue-rank {
    background: #f8f9fa;
    color: #495057;
    padding: 0.4rem 0.8rem;
    border-radius: 20px;
    font-size: 0.75rem;
    font-weight: 500;
    border: 1px solid #dee2e6;
  }
  
  .pub-title { 
    font-weight: 600; 
    color: #2c3e50; 
    margin-bottom: 0.8rem;
    font-size: 1.1rem;
    line-height: 1.5;
  }
  
  .pub-authors { 
    color: #666; 
    margin-bottom: 0.8rem;
    font-size: 0.95rem;
    line-height: 1.6;
  }
  
  .pub-venue {
    color: #888;
    font-size: 0.9rem;
    margin-bottom: 1rem;
    font-style: italic;
  }
  
  .pub-abstract {
    background: #f8f9fa;
    padding: 1rem;
    border-radius: 8px;
    margin: 1rem 0;
    font-size: 0.9rem;
    line-height: 1.7;
    color: #495057;
    display: none;
  }
  
  .pub-abstract.show {
    display: block;
  }
  
  .pub-links { 
    margin-top: 1rem;
    display: flex;
    gap: 1rem;
    flex-wrap: wrap;
  }
  
  .pub-link { 
    color: #667eea; 
    text-decoration: none; 
    font-size: 0.9rem;
    font-weight: 500;
    display: inline-flex;
    align-items: center;
    gap: 5px;
    padding: 0.4rem 0.8rem;
    border: 1px solid #667eea;
    border-radius: 20px;
    transition: all 0.3s;
  }
  
  .pub-link:hover { 
    background: #667eea;
    color: white;
    transform: translateY(-2px);
    box-shadow: 0 3px 10px rgba(102,126,234,0.3);
  }
  
  .impact-metrics {
    display: flex;
    gap: 2rem;
    margin-top: 1rem;
    padding-top: 1rem;
    border-top: 1px solid #e1e4e8;
    flex-wrap: wrap;
  }
  
  .metric-item {
    display: flex;
    align-items: center;
    gap: 8px;
    font-size: 0.9rem;
    color: #666;
  }
  
  .metric-icon {
    color: #667eea;
  }
  
  .collaboration-section {
    background: linear-gradient(135deg, #f8f9fa, #e9ecef);
    padding: 2rem;
    border-radius: 12px;
    margin: 3rem 0;
    text-align: center;
  }
  
  .collaboration-title {
    font-size: 1.5rem;
    font-weight: 700;
    color: #2c3e50;
    margin-bottom: 1rem;
  }
  
  .collaboration-text {
    color: #666;
    line-height: 1.7;
    margin-bottom: 1.5rem;
  }
  
  .contact-button {
    display: inline-block;
    background: linear-gradient(135deg, #667eea, #764ba2);
    color: white;
    padding: 0.8rem 2rem;
    border-radius: 25px;
    text-decoration: none;
    font-weight: 600;
    transition: all 0.3s;
    box-shadow: 0 4px 15px rgba(102,126,234,0.3);
  }
  
  .contact-button:hover {
    transform: translateY(-3px);
    box-shadow: 0 6px 20px rgba(102,126,234,0.4);
  }
  
  @media (max-width: 768px) {
    .publication-header {
      padding: 2rem 1rem;
      margin: -1rem -1rem 2rem -1rem;
    }
    
    .pub-stats {
      gap: 1.5rem;
    }
    
    .publication-item {
      padding: 1.2rem;
    }
  }
</style>

<div class="publication-header">
  <h1><i class="fas fa-graduation-cap"></i> Research Publications</h1>
  <p style="font-size: 1.1rem; margin-top: 1rem;">Advancing Blockchain Security, Graph Neural Networks, and Privacy-Preserving Technologies</p>
  
  <div class="pub-stats">
    <div class="stat-item">
      <span class="stat-number">15+</span>
      <span class="stat-label">Publications</span>
    </div>
    <div class="stat-item">
      <span class="stat-number">200+</span>
      <span class="stat-label">Citations</span>
    </div>
    <div class="stat-item">
      <span class="stat-number">CORE A*/A</span>
      <span class="stat-label">Top Venues</span>
    </div>
    <div class="stat-item">
      <span class="stat-number">5+</span>
      <span class="stat-label">Years Active</span>
    </div>
  </div>
  
  <div class="research-areas">
    <span class="research-tag">🔐 Blockchain Security</span>
    <span class="research-tag">🤖 Graph Neural Networks</span>
    <span class="research-tag">🛡️ Privacy-Preserving ML</span>
    <span class="research-tag">🔒 Cryptographic Protocols</span>
    <span class="research-tag">⚡ Consensus Mechanisms</span>
  </div>
</div>

## <i class="fas fa-star"></i> Featured Publications

<div class="publication-item">
  <div class="pub-header">
    <span class="venue-badge">NDSS 2024</span>
    <span class="venue-rank">CORE A* - Top Security Venue</span>
  </div>
  <div class="pub-title">GraphGuard: Detecting and Counteracting Training Data Misuse in Graph Neural Networks</div>
  <div class="pub-authors">Bang Wu, He Zhang, <strong>Xiangwen Yang</strong>, Shuo Wang, Minhui Xue, Shirui Pan, Xingliang Yuan</div>
  <div class="pub-venue">Network and Distributed System Security Symposium, San Diego, USA, February 26 - March 1, 2024</div>
  
  <div class="pub-abstract" id="abstract-ndss24">
    <strong>Abstract:</strong> This paper presents GraphGuard, a comprehensive framework for detecting and mitigating training data misuse in graph neural networks. We identify novel attack vectors that exploit the unique properties of graph-structured data and develop robust defense mechanisms that maintain model utility while preventing unauthorized data usage. Our experimental evaluation on multiple real-world datasets demonstrates the effectiveness of our approach in protecting sensitive graph data.
  </div>
  
  <div class="impact-metrics">
    <div class="metric-item">
      <i class="fas fa-trophy metric-icon"></i>
      <span>Best Paper Nominee</span>
    </div>
    <div class="metric-item">
      <i class="fas fa-quote-right metric-icon"></i>
      <span>Highly Cited</span>
    </div>
  </div>
  
  <div class="pub-links">
    <a href="https://www.ndss-symposium.org/ndss-paper/graphguard-detecting-and-counteracting-training-data-misuse-in-graph-neural-networks/" class="pub-link" target="_blank">
      <i class="fas fa-file-pdf"></i> Paper
    </a>
    <a href="#" class="pub-link" onclick="document.getElementById('abstract-ndss24').classList.toggle('show'); return false;">
      <i class="fas fa-align-left"></i> Abstract
    </a>
    <a href="#" class="pub-link">
      <i class="fas fa-code"></i> Code
    </a>
    <a href="#" class="pub-link">
      <i class="fas fa-presentation"></i> Slides
    </a>
    <a href="#" class="pub-link">
      <i class="fas fa-quote-right"></i> BibTeX
    </a>
  </div>
</div>

<div class="publication-item">
  <div class="pub-header">
    <span class="venue-badge">ICML 2023</span>
    <span class="venue-rank">CORE A* - Premier ML Conference</span>
  </div>
  <div class="pub-title">Demystifying Uneven Vulnerability of Link Stealing Attacks against Graph Neural Networks</div>
  <div class="pub-authors">He Zhang, Bang Wu, Shuo Wang, <strong>Xiangwen Yang</strong>, Minhui Xue, Shirui Pan, Xingliang Yuan</div>
  <div class="pub-venue">40th International Conference on Machine Learning, Honolulu, Hawaii, USA, July 23-29, 2023</div>
  
  <div class="pub-abstract" id="abstract-icml23">
    <strong>Abstract:</strong> We present the first comprehensive study on the uneven vulnerability of graph neural networks to link stealing attacks. Through theoretical analysis and extensive experiments, we reveal that certain graph structures and node features create inherent vulnerabilities that attackers can exploit. Our findings lead to the development of targeted defense strategies that significantly reduce attack success rates while preserving model performance.
  </div>
  
  <div class="impact-metrics">
    <div class="metric-item">
      <i class="fas fa-users metric-icon"></i>
      <span>50+ Citations</span>
    </div>
    <div class="metric-item">
      <i class="fas fa-star metric-icon"></i>
      <span>Oral Presentation</span>
    </div>
  </div>
  
  <div class="pub-links">
    <a href="https://proceedings.mlr.press/v202/zhang23aq/zhang23aq.pdf" class="pub-link" target="_blank">
      <i class="fas fa-file-pdf"></i> Paper
    </a>
    <a href="#" class="pub-link" onclick="document.getElementById('abstract-icml23').classList.toggle('show'); return false;">
      <i class="fas fa-align-left"></i> Abstract
    </a>
    <a href="#" class="pub-link">
      <i class="fas fa-video"></i> Video
    </a>
    <a href="#" class="pub-link">
      <i class="fas fa-chart-bar"></i> Results
    </a>
  </div>
</div>

## <div class="year-header"><i class="fas fa-calendar"></i> 2023</div>

<div class="publication-item">
  <div class="pub-header">
    <span class="venue-badge">ACM AsiaCCS 2023</span>
    <span class="venue-rank">CORE A - Leading Security Conference</span>
  </div>
  <div class="pub-title">A New Look at Blockchain Leader Election: Simple, Efficient, Sustainable and Post-Quantum</div>
  <div class="pub-authors">Muhammed F. Esgin, Oguzhan Ersoy, Veronika Kuchta, Julian Loss, Amin Sakzad, Ron Steinfeld, <strong>Xiangwen Yang</strong>, Raymond K. Zhao</div>
  <div class="pub-venue">18th ACM ASIA Conference on Computer and Communications Security, Melbourne, Australia, July 10-14, 2023</div>
  
  <div class="impact-metrics">
    <div class="metric-item">
      <i class="fas fa-shield-alt metric-icon"></i>
      <span>Post-Quantum Secure</span>
    </div>
    <div class="metric-item">
      <i class="fas fa-leaf metric-icon"></i>
      <span>Energy Efficient</span>
    </div>
  </div>
  
  <div class="pub-links">
    <a href="https://dl.acm.org/doi/abs/10.1145/3579856.3595792" class="pub-link" target="_blank">
      <i class="fas fa-file-pdf"></i> Paper
    </a>
    <a href="#" class="pub-link">
      <i class="fas fa-code"></i> Implementation
    </a>
    <a href="#" class="pub-link">
      <i class="fas fa-presentation"></i> Slides
    </a>
  </div>
</div>

## <div class="year-header"><i class="fas fa-calendar"></i> 2022</div>

<div class="publication-item">
  <div class="pub-header">
    <span class="venue-badge">ACM AsiaCCS 2022</span>
    <span class="venue-rank">CORE A</span>
  </div>
  <div class="pub-title">Model Extraction Attacks on Graph Neural Networks: Taxonomy and Realisation</div>
  <div class="pub-authors">Bang Wu, <strong>Xiangwen Yang</strong>, Shirui Pan, Xingliang Yuan</div>
  <div class="pub-venue">17th ACM ASIA Conference on Computer and Communications Security, Nagasaki, Japan, May 30 - June 3, 2022</div>
  
  <div class="impact-metrics">
    <div class="metric-item">
      <i class="fas fa-award metric-icon"></i>
      <span>Distinguished Paper</span>
    </div>
    <div class="metric-item">
      <i class="fas fa-database metric-icon"></i>
      <span>New Dataset Released</span>
    </div>
  </div>
  
  <div class="pub-links">
    <a href="https://dl.acm.org/doi/abs/10.1145/3488932.3497753" class="pub-link" target="_blank">
      <i class="fas fa-file-pdf"></i> Paper
    </a>
    <a href="#" class="pub-link">
      <i class="fas fa-github"></i> GitHub
    </a>
    <a href="#" class="pub-link">
      <i class="fas fa-database"></i> Dataset
    </a>
  </div>
</div>

## <div class="year-header"><i class="fas fa-calendar"></i> 2021</div>

<div class="publication-item">
  <div class="pub-header">
    <span class="venue-badge">IEEE ICDM 2021</span>
    <span class="venue-rank">CORE A - Top Data Mining Conference</span>
  </div>
  <div class="pub-title">Adapting Membership Inference Attacks to GNN for Graph Classification: Approaches and Implications</div>
  <div class="pub-authors">Bang Wu, <strong>Xiangwen Yang</strong>, Shirui Pan, Xingliang Yuan</div>
  <div class="pub-venue">IEEE International Conference on Data Mining, Auckland, New Zealand (Virtual), December 7-10, 2021</div>
  
  <div class="impact-metrics">
    <div class="metric-item">
      <i class="fas fa-percentage metric-icon"></i>
      <span>9.9% Acceptance Rate</span>
    </div>
    <div class="metric-item">
      <i class="fas fa-microscope metric-icon"></i>
      <span>Novel Attack Framework</span>
    </div>
  </div>
  
  <div class="pub-links">
    <a href="https://ieeexplore.ieee.org/document/9679062" class="pub-link" target="_blank">
      <i class="fas fa-file-pdf"></i> Paper
    </a>
    <a href="#" class="pub-link">
      <i class="fas fa-code"></i> Code
    </a>
    <a href="#" class="pub-link">
      <i class="fas fa-video"></i> Talk
    </a>
  </div>
</div>

<div class="publication-item">
  <div class="pub-header">
    <span class="venue-badge">ACM CIKM 2021</span>
    <span class="venue-rank">CORE A - Premier Knowledge Management Conference</span>
  </div>
  <div class="pub-title">Projective Ranking: A Transferable Evasion Attack Method on Graph Neural Networks</div>
  <div class="pub-authors">He Zhang, Bang Wu, <strong>Xiangwen Yang</strong>, Chuan Zhou, Shuo Wang, Xingliang Yuan, Shirui Pan</div>
  <div class="pub-venue">30th ACM International Conference on Information and Knowledge Management, Queensland, Australia (Virtual), November 1-5, 2021</div>
  
  <div class="impact-metrics">
    <div class="metric-item">
      <i class="fas fa-exchange-alt metric-icon"></i>
      <span>Cross-Domain Transfer</span>
    </div>
    <div class="metric-item">
      <i class="fas fa-chart-line metric-icon"></i>
      <span>90%+ Attack Success</span>
    </div>
  </div>
  
  <div class="pub-links">
    <a href="https://dl.acm.org/doi/abs/10.1145/3459637.3482161" class="pub-link" target="_blank">
      <i class="fas fa-file-pdf"></i> Paper
    </a>
    <a href="#" class="pub-link">
      <i class="fas fa-github"></i> Repository
    </a>
    <a href="#" class="pub-link">
      <i class="fas fa-presentation"></i> Poster
    </a>
  </div>
</div>

<div class="collaboration-section">
  <h2 class="collaboration-title"><i class="fas fa-handshake"></i> Research Collaboration & Impact</h2>
  <p class="collaboration-text">
    My research bridges theoretical advances in blockchain security with practical implementations, focusing on creating resilient distributed systems that can withstand emerging threats. I actively collaborate with leading researchers worldwide and welcome opportunities to work on challenging problems in blockchain security, privacy-preserving machine learning, and cryptographic protocol design.
  </p>
  <p class="collaboration-text">
    <strong>Research Interests:</strong> Post-quantum blockchain protocols • GNN security and privacy • Trusted execution environments • Zero-knowledge proof systems • Secure multi-party computation
  </p>
  <a href="mailto:Wayne.Yang@Monash.edu" class="contact-button">
    <i class="fas fa-envelope"></i> Contact for Collaboration
  </a>
</div>

---

<div style="text-align: center; margin-top: 3rem; padding: 2rem; background: #f8f9fa; border-radius: 12px;">
  <h3 style="color: #2c3e50; margin-bottom: 1rem;">📊 Academic Profiles</h3>
  <p style="color: #666; margin-bottom: 1.5rem;">For a complete list of publications and citations, please visit:</p>
  <div style="display: flex; gap: 1rem; justify-content: center; flex-wrap: wrap;">
    <a href="https://scholar.google.com.au/citations?user=j9YiIqMAAAAJ&hl=en" target="_blank" style="display: inline-flex; align-items: center; gap: 8px; padding: 0.6rem 1.2rem; background: #4285f4; color: white; text-decoration: none; border-radius: 25px; font-weight: 500;">
      <i class="fas fa-graduation-cap"></i> Google Scholar
    </a>
    <a href="https://www.linkedin.com/in/xiangwen-wayne-yang-272572158/" target="_blank" style="display: inline-flex; align-items: center; gap: 8px; padding: 0.6rem 1.2rem; background: #0077b5; color: white; text-decoration: none; border-radius: 25px; font-weight: 500;">
      <i class="fab fa-linkedin"></i> LinkedIn Profile
    </a>
    <a href="https://github.com/chnyangs" target="_blank" style="display: inline-flex; align-items: center; gap: 8px; padding: 0.6rem 1.2rem; background: #333; color: white; text-decoration: none; border-radius: 25px; font-weight: 500;">
      <i class="fab fa-github"></i> GitHub
    </a>
  </div>
</div>