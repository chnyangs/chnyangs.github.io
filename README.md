<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Arial:wght@400;600;700&display=swap">

<style>
  * { margin: 0; padding: 0; box-sizing: border-box; }
  
  body { 
    font-family: Arial, sans-serif; 
    line-height: 1.6; 
    color: #333; 
    background: #ffffff;
    font-size: 14px;
  }
  
  .container { 
    max-width: 1000px; 
    margin: 0 auto; 
    padding: 0 20px; 
  }
  
  /* Navigation */
  .nav-bar {
    background: #f8f9fa;
    border-bottom: 1px solid #dee2e6;
    padding: 15px 0;
    margin-bottom: 30px;
  }
  
  .nav-menu {
    display: flex;
    justify-content: center;
    gap: 30px;
    flex-wrap: wrap;
  }
  
  .nav-item {
    color: #333;
    text-decoration: none;
    font-weight: 600;
    padding: 8px 15px;
    border-radius: 4px;
    transition: background-color 0.3s;
  }
  
  .nav-item:hover {
    background-color: #e9ecef;
  }
  
  /* Header */
  .header {
    text-align: left;
    margin-bottom: 40px;
    padding: 30px 0;
  }
  
  .name {
    font-size: 36px;
    font-weight: 700;
    color: #333;
    margin-bottom: 10px;
  }
  
  .title {
    font-size: 18px;
    font-weight: 600;
    color: #666;
    margin-bottom: 5px;
  }
  
  .affiliation {
    font-size: 14px;
    color: #666;
    margin-bottom: 15px;
  }
  
  .contact-info {
    font-size: 14px;
    color: #666;
  }
  
  .contact-links {
    margin-top: 15px;
  }
  
  .contact-links a {
    color: #0066cc;
    text-decoration: none;
    margin-right: 20px;
  }
  
  .contact-links a:hover {
    text-decoration: underline;
  }
  
  /* Sections */
  .section {
    margin-bottom: 50px;
  }
  
  .section-title {
    font-size: 24px;
    font-weight: 700;
    color: #333;
    margin-bottom: 20px;
    border-bottom: 2px solid #333;
    padding-bottom: 5px;
  }
  
  .section-content {
    font-size: 14px;
    line-height: 1.6;
    color: #333;
  }
  
  /* Overview */
  .overview p {
    margin-bottom: 15px;
    text-align: justify;
  }
  
  /* News */
  .news-list {
    list-style: none;
  }
  
  .news-item {
    margin-bottom: 15px;
    padding-left: 0;
  }
  
  .news-date {
    font-weight: 600;
    color: #0066cc;
    display: inline;
  }
  
  .news-content {
    display: inline;
    margin-left: 10px;
  }
  
  /* Publications */
  .pub-category {
    margin-bottom: 30px;
  }
  
  .pub-category-title {
    font-size: 18px;
    font-weight: 600;
    color: #333;
    margin-bottom: 15px;
  }
  
  .pub-list {
    list-style: none;
  }
  
  .pub-item {
    margin-bottom: 15px;
    padding-left: 0;
  }
  
  .venue-tag {
    font-weight: 600;
    color: #0066cc;
    margin-right: 5px;
  }
  
  .pub-title {
    font-weight: 600;
    color: #333;
  }
  
  .pub-authors {
    color: #666;
    font-style: italic;
  }
  
  .pub-venue {
    color: #666;
  }
  
  .pub-link {
    color: #0066cc;
    text-decoration: none;
    margin-left: 10px;
  }
  
  .pub-link:hover {
    text-decoration: underline;
  }
  
  /* Experience */
  .exp-item {
    margin-bottom: 25px;
  }
  
  .exp-title {
    font-weight: 600;
    color: #333;
    font-size: 16px;
  }
  
  .exp-org {
    color: #666;
    font-style: italic;
  }
  
  .exp-date {
    color: #666;
    font-size: 13px;
  }
  
  .exp-desc {
    margin-top: 8px;
    color: #333;
  }
  
  .exp-desc ul {
    margin-left: 20px;
    margin-top: 5px;
  }
  
  .exp-desc li {
    margin-bottom: 5px;
  }
  
  /* Skills */
  .skills-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 20px;
  }
  
  .skill-category {
    background: #f8f9fa;
    padding: 20px;
    border-radius: 5px;
  }
  
  .skill-category h4 {
    font-weight: 600;
    margin-bottom: 10px;
    color: #333;
  }
  
  .skill-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
  }
  
  .skill-tag {
    background: #e9ecef;
    color: #333;
    padding: 4px 8px;
    border-radius: 3px;
    font-size: 12px;
  }
  
  /* Footer */
  .footer {
    text-align: center;
    padding: 30px 0;
    border-top: 1px solid #dee2e6;
    margin-top: 50px;
    color: #666;
    font-size: 12px;
  }
  
  /* Responsive */
  @media (max-width: 768px) {
    .nav-menu {
      flex-direction: column;
      align-items: center;
      gap: 10px;
    }
    
    .name {
      font-size: 28px;
    }
    
    .skills-grid {
      grid-template-columns: 1fr;
    }
  }
</style>

<!-- Navigation -->
<div class="nav-bar">
  <div class="container">
    <nav class="nav-menu">
      <a href="#overview" class="nav-item">Home</a>
      <a href="#research" class="nav-item">Research</a>
      <a href="#publications" class="nav-item">Publications</a>
      <a href="#experience" class="nav-item">Experience</a>
      <a href="#news" class="nav-item">News</a>
      <a href="#contact" class="nav-item">Contact</a>
    </nav>
  </div>
</div>

<!-- Header -->
<div class="container">
  <div class="header">
    <h1 class="name">Xiangwen Yang</h1>
    <div class="title">Software Programmer & Blockchain Researcher</div>
    <div class="affiliation">
      Cybersecurity Group<br>
      Department of Software Systems and Cybersecurity<br>
      Monash University<br>
      School of Computer Science and Engineering<br>
      University of Sydney
    </div>
    <div class="contact-info">
      Email: Wayne.Yang [at] Monash.edu | xyan0559 [at] sydney.edu.au
    </div>
    <div class="contact-links">
      <a href="https://scholar.google.com.au/citations?user=j9YiIqMAAAAJ&hl=en" target="_blank">
        <i class="fas fa-graduation-cap"></i> Google Scholar
      </a>
      <a href="https://www.linkedin.com/in/xiangwen-wayne-yang-272572158/" target="_blank">
        <i class="fab fa-linkedin"></i> LinkedIn
      </a>
      <a href="publication/overview.md">Publications</a>
    </div>
  </div>

  <!-- Overview Section -->
  <div class="section" id="overview">
    <h2 class="section-title">Overview</h2>
    <div class="section-content overview">
      <p>I am a Software Programmer and Blockchain Researcher at Monash University's Department of Software Systems and Cybersecurity, with a joint appointment at the University of Sydney's School of Computer Science and Engineering. My work focuses on enhancing blockchain resilience through innovative system design, bridging the critical gap between theoretical security models and practical implementation challenges.</p>
      
      <p>With a Master's degree in Information Technology from Monash University and extensive experience in both industry and academia, I specialize in blockchain security, graph neural networks, and privacy-preserving technologies. My research has been published at premier venues including NDSS, ICML, ICDM, and ACM AsiaCCS, contributing significantly to the fields of distributed systems security and machine learning privacy.</p>
      
      <p>I am always looking for self-motivated students and research collaborators. Please email me your CV, research interests, and a brief statement (no more than 200 words) describing your background and research goals.</p>
    </div>
  </div>

  <!-- News Section -->
  <div class="section" id="news">
    <h2 class="section-title">News</h2>
    <div class="section-content">
      <ul class="news-list">
        <li class="news-item">
          <span class="news-date">[Jan'24]</span>
          <span class="news-content">Our paper "GraphGuard: Detecting and Counteracting Training Data Misuse in Graph Neural Networks" has been accepted by NDSS'24.</span>
        </li>
        <li class="news-item">
          <span class="news-date">[Dec'23]</span>
          <span class="news-content">Presented latest findings on diversity-aware blockchain systems at the International Blockchain Security Conference.</span>
        </li>
        <li class="news-item">
          <span class="news-date">[Sep'23]</span>
          <span class="news-content">Started research collaboration with University of Sydney on post-quantum cryptographic implementations for blockchain systems.</span>
        </li>
        <li class="news-item">
          <span class="news-date">[Jul'23]</span>
          <span class="news-content">Our paper "Demystifying Uneven Vulnerability of Link Stealing Attacks against Graph Neural Networks" has been accepted by ICML'23.</span>
        </li>
        <li class="news-item">
          <span class="news-date">[Apr'23]</span>
          <span class="news-content">Our paper "A New Look at Blockchain Leader Election: Simple, Efficient, Sustainable and Post-Quantum" has been accepted by ACM AsiaCCS'23.</span>
        </li>
      </ul>
    </div>
  </div>

  <!-- Research Section -->
  <div class="section" id="research">
    <h2 class="section-title">Research Interests</h2>
    <div class="section-content">
      <p>I have broad interests in computer security, including secure distributed systems, trustworthy machine learning, and blockchain resilience. My recent research focus includes:</p>
      
      <div class="skills-grid">
        <div class="skill-category">
          <h4>Blockchain Security & Resilience</h4>
          <div class="skill-tags">
            <span class="skill-tag">Diversity-aware Systems</span>
            <span class="skill-tag">Consensus Mechanisms</span>
            <span class="skill-tag">Post-quantum Cryptography</span>
            <span class="skill-tag">Smart Contract Security</span>
          </div>
        </div>
        
        <div class="skill-category">
          <h4>Graph Neural Networks Security</h4>
          <div class="skill-tags">
            <span class="skill-tag">Privacy Attacks & Defenses</span>
            <span class="skill-tag">Model Extraction</span>
            <span class="skill-tag">Membership Inference</span>
            <span class="skill-tag">Adversarial Robustness</span>
          </div>
        </div>
        
        <div class="skill-category">
          <h4>Privacy-Preserving Technologies</h4>
          <div class="skill-tags">
            <span class="skill-tag">Trusted Execution Environments</span>
            <span class="skill-tag">Encrypted Databases</span>
            <span class="skill-tag">Secure Multi-party Computation</span>
            <span class="skill-tag">Zero-Knowledge Proofs</span>
          </div>
        </div>
        
        <div class="skill-category">
          <h4>Technical Skills</h4>
          <div class="skill-tags">
            <span class="skill-tag">Python</span>
            <span class="skill-tag">JavaScript/TypeScript</span>
            <span class="skill-tag">Solidity</span>
            <span class="skill-tag">PyTorch</span>
            <span class="skill-tag">TensorFlow</span>
            <span class="skill-tag">Ethereum</span>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- Publications Section -->
  <div class="section" id="publications">
    <h2 class="section-title">Recent Publications</h2>
    <div class="section-content">
      <p>My full publication list can be found at <a href="https://scholar.google.com.au/citations?user=j9YiIqMAAAAJ&hl=en" target="_blank">Google Scholar</a> and <a href="publication/overview.md">detailed publication page</a>.</p>
      
      <div class="pub-category">
        <h3 class="pub-category-title">Secure and Trustworthy Graph Learning</h3>
        <ul class="pub-list">
          <li class="pub-item">
            <span class="venue-tag">[NDSS'24]</span>
            <span class="pub-title">GraphGuard: Detecting and Counteracting Training Data Misuse in Graph Neural Networks</span><br>
            <span class="pub-authors">Bang Wu, He Zhang, <strong>Xiangwen Yang</strong>, Shuo Wang, Minhui Xue, Shirui Pan, Xingliang Yuan</span><br>
            <span class="pub-venue">Network and Distributed System Security Symposium, San Diego, USA, 2024</span>
            <a href="https://www.ndss-symposium.org/ndss-paper/graphguard-detecting-and-counteracting-training-data-misuse-in-graph-neural-networks/" class="pub-link" target="_blank">PDF</a>
          </li>
          
          <li class="pub-item">
            <span class="venue-tag">[ICML'23]</span>
            <span class="pub-title">Demystifying Uneven Vulnerability of Link Stealing Attacks against Graph Neural Networks</span><br>
            <span class="pub-authors">He Zhang, Bang Wu, Shuo Wang, <strong>Xiangwen Yang</strong>, Minhui Xue, Shirui Pan, Xingliang Yuan</span><br>
            <span class="pub-venue">International Conference on Machine Learning, Honolulu, Hawaii, USA, 2023</span>
            <a href="https://proceedings.mlr.press/v202/zhang23aq/zhang23aq.pdf" class="pub-link" target="_blank">PDF</a>
          </li>
          
          <li class="pub-item">
            <span class="venue-tag">[ACM AsiaCCS'22]</span>
            <span class="pub-title">Model Extraction Attacks on Graph Neural Networks: Taxonomy and Realisation</span><br>
            <span class="pub-authors">Bang Wu, <strong>Xiangwen Yang</strong>, Shirui Pan, Xingliang Yuan</span><br>
            <span class="pub-venue">17th ACM ASIA Conference on Computer and Communications Security, 2022</span>
            <a href="https://dl.acm.org/doi/abs/10.1145/3488932.3497753" class="pub-link" target="_blank">PDF</a>
          </li>
          
          <li class="pub-item">
            <span class="venue-tag">[IEEE ICDM'21]</span>
            <span class="pub-title">Adapting Membership Inference Attacks to GNN for Graph Classification: Approaches and Implications</span><br>
            <span class="pub-authors">Bang Wu, <strong>Xiangwen Yang</strong>, Shirui Pan, Xingliang Yuan</span><br>
            <span class="pub-venue">IEEE International Conference on Data Mining, 2021</span>
            <a href="https://ieeexplore.ieee.org/document/9679062" class="pub-link" target="_blank">PDF</a>
          </li>
        </ul>
      </div>
      
      <div class="pub-category">
        <h3 class="pub-category-title">Blockchain Security and Cryptography</h3>
        <ul class="pub-list">
          <li class="pub-item">
            <span class="venue-tag">[ACM AsiaCCS'23]</span>
            <span class="pub-title">A New Look at Blockchain Leader Election: Simple, Efficient, Sustainable and Post-Quantum</span><br>
            <span class="pub-authors">Muhammed F Esgin, Oguzhan Ersoy, Veronika Kuchta, Julian Loss, Amin Sakzad, Ron Steinfeld, <strong>Xiangwen Yang</strong>, Raymond K Zhao</span><br>
            <span class="pub-venue">18th ACM ASIA Conference on Computer and Communications Security, 2023</span>
            <a href="https://dl.acm.org/doi/abs/10.1145/3579856.3595792" class="pub-link" target="_blank">PDF</a>
          </li>
          
          <li class="pub-item">
            <span class="venue-tag">[ACM CIKM'21]</span>
            <span class="pub-title">Projective Ranking: A Transferable Evasion Attack Method on Graph Neural Networks</span><br>
            <span class="pub-authors">He Zhang, Bang Wu, <strong>Xiangwen Yang</strong>, Chuan Zhou, Shuo Wang, Xingliang Yuan, Shirui Pan</span><br>
            <span class="pub-venue">30th ACM International Conference on Information and Knowledge Management, 2021</span>
            <a href="https://dl.acm.org/doi/abs/10.1145/3459637.3482161" class="pub-link" target="_blank">PDF</a>
          </li>
        </ul>
      </div>
    </div>
  </div>

  <!-- Experience Section -->
  <div class="section" id="experience">
    <h2 class="section-title">Professional Experience</h2>
    <div class="section-content">
      <div class="exp-item">
        <div class="exp-title">Software Programmer</div>
        <div class="exp-org">Monash University</div>
        <div class="exp-date">Dec 2020 - Present</div>
        <div class="exp-desc">
          <ul>
            <li>Leading full-stack development for cutting-edge blockchain research projects</li>
            <li>Coordinating cross-functional teams including researchers and PhD students</li>
            <li>Bridging academic research and practical implementation in blockchain security</li>
            <li>Developing scalable solutions for distributed systems and consensus mechanisms</li>
          </ul>
        </div>
      </div>
      
      <div class="exp-item">
        <div class="exp-title">Teaching Associate</div>
        <div class="exp-org">Monash University</div>
        <div class="exp-date">Jul 2020 - Dec 2020</div>
        <div class="exp-desc">
          <ul>
            <li>Conducted Network Security tutorials for undergraduate and postgraduate students</li>
            <li>Mentored students in cybersecurity concepts and practical implementations</li>
            <li>Developed educational materials for security protocol analysis</li>
          </ul>
        </div>
      </div>
      
      <div class="exp-item">
        <div class="exp-title">Research Assistant / Data Analyst</div>
        <div class="exp-org">Monash University</div>
        <div class="exp-date">Sep 2019 - Nov 2020</div>
        <div class="exp-desc">
          <ul>
            <li>Spearheaded data analysis and modeling for Planning & Equipment Utilization Review Project</li>
            <li>Enhanced AI integration into system prototypes and research frameworks</li>
            <li>Developed machine learning models for predictive analytics and optimization</li>
          </ul>
        </div>
      </div>
      
      <div class="exp-item">
        <div class="exp-title">Organizer - ACE-SIP Blockchain Hackathon</div>
        <div class="exp-org">Monash University</div>
        <div class="exp-date">Sep 2022 - Dec 2022</div>
        <div class="exp-desc">
          Led comprehensive blockchain hackathon focused on sustainability informatics, coordinating projects across environmental, governmental, and social impact themes.
        </div>
      </div>
      
      <div class="exp-item">
        <div class="exp-title">Research Scholar - Summer Research Scholarship</div>
        <div class="exp-org">Monash University</div>
        <div class="exp-date">Dec 2019 - Mar 2020</div>
        <div class="exp-desc">
          Developed and evaluated advanced encrypted database systems, enhancing data security frameworks for academic and commercial applications.
        </div>
      </div>
    </div>
  </div>

  <!-- Education Section -->
  <div class="section">
    <h2 class="section-title">Education</h2>
    <div class="section-content">
      <div class="exp-item">
        <div class="exp-title">Master of Information Technology</div>
        <div class="exp-org">Monash University</div>
        <div class="exp-date">2018 - 2020</div>
        <div class="exp-desc">Specialization: Software Systems and Cybersecurity</div>
      </div>
      
      <div class="exp-item">
        <div class="exp-title">Bachelor of Software Engineering</div>
        <div class="exp-org">Nanjing University of Posts and Telecommunications</div>
        <div class="exp-date">2009 - 2013</div>
        <div class="exp-desc">Foundation in software development and computer science principles</div>
      </div>
    </div>
  </div>

  <!-- Contact Section -->
  <div class="section" id="contact">
    <h2 class="section-title">Contact</h2>
    <div class="section-content">
      <p>I am always interested in discussing research collaborations, consulting opportunities, and potential PhD student supervision. Please feel free to reach out!</p>
      
      <div style="margin-top: 20px;">
        <strong>Email:</strong> Wayne.Yang [at] Monash.edu | xyan0559 [at] sydney.edu.au<br>
        <strong>Google Scholar:</strong> <a href="https://scholar.google.com.au/citations?user=j9YiIqMAAAAJ&hl=en" target="_blank">Research Profile</a><br>
        <strong>LinkedIn:</strong> <a href="https://www.linkedin.com/in/xiangwen-wayne-yang-272572158/" target="_blank">Professional Network</a><br><br>
        
        <strong>Affiliations:</strong><br>
        Monash University - Department of Software Systems and Cybersecurity<br>
        University of Sydney - School of Computer Science and Engineering
      </div>
    </div>
  </div>
</div>

<!-- Footer -->
<div class="footer">
  <div class="container">
    <p>Last Update: January, 2025</p>
    <p>"Bridging the gap between theoretical blockchain security and practical implementation"</p>
  </div>
</div>