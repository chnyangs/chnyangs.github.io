<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=SF+Pro+Display:wght@100;200;300;400;500;600;700;800;900&family=SF+Pro+Text:wght@300;400;500;600&display=swap">

<style>
  * { margin: 0; padding: 0; box-sizing: border-box; }
  
  body { 
    font-family: 'SF Pro Text', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif; 
    line-height: 1.47059; 
    color: #1d1d1f; 
    background: #ffffff;
    font-size: 17px;
    font-weight: 400;
  }
  
  .container { max-width: 980px; margin: 0 auto; padding: 0 22px; }
  
  /* Hero Section */
  .hero-section { 
    background: linear-gradient(135deg, #000000 0%, #1c1c1e 100%); 
    color: #ffffff; 
    padding: 80px 0 100px 0; 
    text-align: center; 
    position: relative;
    overflow: hidden;
  }
  
  .hero-section::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: radial-gradient(circle at 50% 50%, rgba(255,255,255,0.1) 0%, transparent 70%);
  }
  
  .hero-content { position: relative; z-index: 2; }
  
  .hero-title { 
    font-family: 'SF Pro Display', -apple-system, BlinkMacSystemFont, sans-serif;
    font-size: 56px; 
    font-weight: 700; 
    line-height: 1.07143;
    letter-spacing: -0.005em;
    margin-bottom: 16px; 
  }
  
  .hero-subtitle { 
    font-size: 28px; 
    font-weight: 400; 
    line-height: 1.14286;
    letter-spacing: 0.007em;
    opacity: 0.8; 
    margin-bottom: 8px; 
  }
  
  .hero-description { 
    font-size: 21px; 
    font-weight: 400; 
    line-height: 1.381;
    letter-spacing: 0.011em;
    opacity: 0.7; 
    margin-bottom: 40px;
    max-width: 640px;
    margin-left: auto;
    margin-right: auto;
  }
  
  .hero-links { 
    display: flex; 
    justify-content: center; 
    gap: 24px; 
    flex-wrap: wrap;
  }
  
  .hero-link { 
    color: #ffffff; 
    text-decoration: none; 
    padding: 12px 24px; 
    border: 1px solid rgba(255,255,255,0.3); 
    border-radius: 980px; 
    font-size: 17px;
    font-weight: 400;
    transition: all 0.3s cubic-bezier(0.25, 0.46, 0.45, 0.94);
    backdrop-filter: blur(20px);
    background: rgba(255,255,255,0.1);
  }
  
  .hero-link:hover { 
    background: rgba(255,255,255,0.2); 
    border-color: rgba(255,255,255,0.5);
    transform: translateY(-1px);
  }
  
  /* Section Styling */
  .section { 
    padding: 80px 0; 
    border-bottom: 1px solid #d2d2d7;
  }
  
  .section:last-child { border-bottom: none; }
  
  .section-header { 
    text-align: center; 
    margin-bottom: 60px; 
  }
  
  .section-title { 
    font-family: 'SF Pro Display', -apple-system, BlinkMacSystemFont, sans-serif;
    font-size: 48px; 
    font-weight: 700; 
    line-height: 1.08333;
    letter-spacing: -0.003em;
    color: #1d1d1f; 
    margin-bottom: 16px; 
  }
  
  .section-subtitle { 
    font-size: 21px; 
    font-weight: 400; 
    line-height: 1.381;
    letter-spacing: 0.011em;
    color: #86868b; 
    max-width: 640px;
    margin: 0 auto;
  }
  
  /* Stats */
  .stats-grid { 
    display: grid; 
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); 
    gap: 40px; 
    margin: 60px 0; 
  }
  
  .stat-card { 
    text-align: center; 
    padding: 40px 20px;
    background: #f5f5f7;
    border-radius: 18px;
    transition: transform 0.3s ease;
  }
  
  .stat-card:hover { transform: translateY(-4px); }
  
  .stat-number { 
    font-family: 'SF Pro Display', -apple-system, BlinkMacSystemFont, sans-serif;
    font-size: 64px; 
    font-weight: 700; 
    line-height: 1;
    color: #1d1d1f; 
    margin-bottom: 8px;
  }
  
  .stat-label { 
    font-size: 17px; 
    font-weight: 600; 
    color: #86868b; 
    text-transform: uppercase; 
    letter-spacing: 0.5px; 
  }
  
  /* Cards */
  .card-grid { 
    display: grid; 
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); 
    gap: 30px; 
    margin: 60px 0; 
  }
  
  .card { 
    background: #ffffff; 
    border-radius: 18px; 
    padding: 40px; 
    box-shadow: 0 4px 20px rgba(0,0,0,0.08);
    transition: all 0.3s cubic-bezier(0.25, 0.46, 0.45, 0.94);
    border: 1px solid #d2d2d7;
  }
  
  .card:hover { 
    transform: translateY(-8px); 
    box-shadow: 0 20px 40px rgba(0,0,0,0.15);
  }
  
  .card-icon { 
    font-size: 40px; 
    margin-bottom: 20px; 
    color: #007aff;
  }
  
  .card-title { 
    font-family: 'SF Pro Display', -apple-system, BlinkMacSystemFont, sans-serif;
    font-size: 24px; 
    font-weight: 600; 
    line-height: 1.16667;
    color: #1d1d1f; 
    margin-bottom: 12px; 
  }
  
  .card-description { 
    font-size: 17px; 
    line-height: 1.47059;
    color: #86868b; 
  }
  
  /* Content Blocks */
  .content-block { 
    background: #f5f5f7; 
    border-radius: 18px; 
    padding: 60px 40px; 
    margin: 40px 0; 
  }
  
  .content-block h3 { 
    font-family: 'SF Pro Display', -apple-system, BlinkMacSystemFont, sans-serif;
    font-size: 32px; 
    font-weight: 600; 
    line-height: 1.125;
    color: #1d1d1f; 
    margin-bottom: 20px; 
  }
  
  .content-block p { 
    font-size: 19px; 
    line-height: 1.42105;
    color: #1d1d1f; 
    margin-bottom: 16px;
  }
  
  .content-block ul { 
    list-style: none; 
    padding: 0; 
  }
  
  .content-block li { 
    font-size: 17px; 
    line-height: 1.47059;
    color: #1d1d1f; 
    margin-bottom: 8px; 
    padding-left: 20px;
    position: relative;
  }
  
  .content-block li::before { 
    content: '•'; 
    color: #007aff; 
    font-weight: bold; 
    position: absolute; 
    left: 0; 
  }
  
  /* Skills Tags */
  .skills-container { 
    display: flex; 
    flex-wrap: wrap; 
    gap: 12px; 
    margin: 30px 0; 
  }
  
  .skill-tag { 
    background: #007aff; 
    color: #ffffff; 
    padding: 8px 16px; 
    border-radius: 20px; 
    font-size: 14px; 
    font-weight: 600; 
    letter-spacing: 0.5px;
  }
  
  /* News Items */
  .news-list { 
    list-style: none; 
    padding: 0; 
  }
  
  .news-item { 
    padding: 30px 0; 
    border-bottom: 1px solid #d2d2d7; 
  }
  
  .news-item:last-child { border-bottom: none; }
  
  .news-date { 
    font-size: 14px; 
    font-weight: 600; 
    color: #86868b; 
    text-transform: uppercase; 
    letter-spacing: 0.5px; 
    margin-bottom: 8px; 
  }
  
  .news-title { 
    font-family: 'SF Pro Display', -apple-system, BlinkMacSystemFont, sans-serif;
    font-size: 24px; 
    font-weight: 600; 
    line-height: 1.16667;
    color: #1d1d1f; 
    margin-bottom: 8px; 
  }
  
  .news-description { 
    font-size: 17px; 
    line-height: 1.47059;
    color: #86868b; 
  }
  
  /* Responsive Design */
  @media (max-width: 768px) {
    .hero-title { font-size: 40px; }
    .hero-subtitle { font-size: 24px; }
    .hero-description { font-size: 19px; }
    .section-title { font-size: 32px; }
    .section { padding: 60px 0; }
    .card-grid { grid-template-columns: 1fr; }
    .stats-grid { grid-template-columns: repeat(2, 1fr); }
  }
  
  @media (max-width: 480px) {
    .container { padding: 0 16px; }
    .hero-title { font-size: 32px; }
    .stats-grid { grid-template-columns: 1fr; }
  }
</style>

<!-- Hero Section -->
<div class="hero-section">
  <div class="container">
    <div class="hero-content">
      <h1 class="hero-title">Xiangwen Yang</h1>
      <p class="hero-subtitle">Blockchain Security Researcher</p>
      <p class="hero-description">Advancing the frontiers of blockchain resilience and privacy-preserving technologies through innovative research and practical implementation.</p>
      
      <div class="hero-links">
        <a href="https://scholar.google.com.au/citations?user=j9YiIqMAAAAJ&hl=en" target="_blank" class="hero-link">
          <i class="fas fa-graduation-cap"></i> Google Scholar
        </a>
        <a href="https://www.linkedin.com/in/xiangwen-wayne-yang-272572158/" target="_blank" class="hero-link">
          <i class="fab fa-linkedin"></i> LinkedIn
        </a>
        <a href="mailto:Wayne.Yang@Monash.edu" class="hero-link">
          <i class="fas fa-envelope"></i> Contact
        </a>
      </div>
    </div>
  </div>
</div>

<!-- Research Impact Section -->
<div class="section">
  <div class="container">
    <div class="section-header">
      <h2 class="section-title">Research Impact</h2>
      <p class="section-subtitle">Advancing blockchain security and privacy-preserving technologies through cutting-edge research</p>
    </div>
    
    <div class="stats-grid">
      <div class="stat-card">
        <div class="stat-number">15+</div>
        <div class="stat-label">Publications</div>
      </div>
      <div class="stat-card">
        <div class="stat-number">5+</div>
        <div class="stat-label">Years Experience</div>
      </div>
      <div class="stat-card">
        <div class="stat-number">A/A*</div>
        <div class="stat-label">CORE Venues</div>
      </div>
    </div>
  </div>
</div>

<!-- About Section -->
<div class="section">
  <div class="container">
    <div class="section-header">
      <h2 class="section-title">About</h2>
      <p class="section-subtitle">Bridging theoretical research with practical blockchain applications</p>
    </div>
    
    <div class="content-block">
      <p>I am an accomplished Software Programmer and Blockchain Researcher at Monash University's Department of Software Systems and Cybersecurity. My work sits at the intersection of theoretical research and practical implementation, where I bridge the gap between cutting-edge academic research and real-world blockchain applications.</p>
      
      <p>With a Master's degree in Information Technology from Monash University and extensive experience in both industry and academia, I specialize in enhancing blockchain resilience through innovative system design and advanced machine learning techniques.</p>
      
      <p>My research has been published at premier venues including NDSS, ICML, ICDM, and ACM AsiaCCS, contributing to the fields of blockchain security, graph neural networks, and privacy-preserving technologies.</p>
    </div>
  </div>
</div>

<!-- Research Focus Section -->
<div class="section">
  <div class="container">
    <div class="section-header">
      <h2 class="section-title">Research Focus</h2>
      <p class="section-subtitle">Enhancing blockchain resilience through innovative system design and advanced cryptographic techniques</p>
    </div>
    
    <div class="card-grid">
      <div class="card">
        <div class="card-icon">🔐</div>
        <h3 class="card-title">Blockchain Security</h3>
        <p class="card-description">Developing diversity-aware blockchain systems, consensus mechanism resilience, and post-quantum cryptographic implementations for enhanced security.</p>
      </div>
      
      <div class="card">
        <div class="card-icon">🤖</div>
        <h3 class="card-title">Graph Neural Networks</h3>
        <p class="card-description">Researching privacy attacks and defenses in GNNs, model extraction attacks, and adversarial robustness in graph-based systems.</p>
      </div>
      
      <div class="card">
        <div class="card-icon">🛡️</div>
        <h3 class="card-title">Privacy-Preserving Tech</h3>
        <p class="card-description">Advancing Trusted Execution Environments, encrypted database systems, and privacy-preserving machine learning techniques.</p>
      </div>
      
      <div class="card">
        <div class="card-icon">🔒</div>
        <h3 class="card-title">Applied Cryptography</h3>
        <p class="card-description">Implementing leader election protocols, sustainable blockchain consensus mechanisms, and cryptographic protocol design.</p>
      </div>
    </div>
  </div>
</div>

<!-- Technical Expertise Section -->
<div class="section">
  <div class="container">
    <div class="section-header">
      <h2 class="section-title">Technical Expertise</h2>
      <p class="section-subtitle">Comprehensive technical skills spanning blockchain development, machine learning, and cybersecurity</p>
    </div>
    
    <div class="content-block">
      <h3>Programming Languages</h3>
      <div class="skills-container">
        <span class="skill-tag">Python</span>
        <span class="skill-tag">JavaScript/TypeScript</span>
        <span class="skill-tag">Java</span>
        <span class="skill-tag">C/C++</span>
        <span class="skill-tag">Solidity</span>
        <span class="skill-tag">Go</span>
        <span class="skill-tag">Rust</span>
      </div>
      
      <h3>Blockchain & Distributed Systems</h3>
      <div class="skills-container">
        <span class="skill-tag">Ethereum</span>
        <span class="skill-tag">Hyperledger Fabric</span>
        <span class="skill-tag">Consensus Algorithms</span>
        <span class="skill-tag">Smart Contracts</span>
        <span class="skill-tag">DeFi Protocols</span>
      </div>
      
      <h3>Machine Learning & AI</h3>
      <div class="skills-container">
        <span class="skill-tag">PyTorch</span>
        <span class="skill-tag">TensorFlow</span>
        <span class="skill-tag">Graph Neural Networks</span>
        <span class="skill-tag">Deep Learning</span>
        <span class="skill-tag">Privacy-Preserving ML</span>
      </div>
      
      <h3>Security & Cryptography</h3>
      <div class="skills-container">
        <span class="skill-tag">TEE (Intel SGX)</span>
        <span class="skill-tag">Cryptographic Protocols</span>
        <span class="skill-tag">Zero-Knowledge Proofs</span>
        <span class="skill-tag">Secure Multi-party Computation</span>
      </div>
    </div>
  </div>
</div>


<!-- Recent News Section -->
<div class="section">
  <div class="container">
    <div class="section-header">
      <h2 class="section-title">Recent News</h2>
      <p class="section-subtitle">Latest updates on research, publications, and professional activities</p>
    </div>
    
    <div class="news-list">
      <div class="news-item">
        <div class="news-date">January 2024</div>
        <h3 class="news-title">GraphGuard Paper Accepted at NDSS 2024</h3>
        <p class="news-description">Our research on detecting and counteracting training data misuse in graph neural networks has been accepted at the Network and Distributed System Security Symposium.</p>
      </div>
      
      <div class="news-item">
        <div class="news-date">December 2023</div>
        <h3 class="news-title">Speaking at Blockchain Security Conference</h3>
        <p class="news-description">Presented latest findings on diversity-aware blockchain systems and their impact on consensus mechanism resilience.</p>
      </div>
      
      <div class="news-item">
        <div class="news-date">September 2023</div>
        <h3 class="news-title">New Research Collaboration</h3>
        <p class="news-description">Started collaboration with University of Sydney on post-quantum cryptographic implementations for blockchain systems.</p>
      </div>
    </div>
  </div>
</div>

<!-- Education Section -->
<div class="section">
  <div class="container">
    <div class="section-header">
      <h2 class="section-title">Education</h2>
      <p class="section-subtitle">Academic foundation in information technology and software engineering</p>
    </div>

    <div class="card-grid">
      <div class="card">
        <div class="card-icon">🎓</div>
        <h3 class="card-title">Monash University</h3>
        <p class="card-description"><strong>Master of Information Technology</strong><br>2018 - 2020<br><em>Specialization: Software Systems and Cybersecurity</em></p>
      </div>
      
      <div class="card">
        <div class="card-icon">🎓</div>
        <h3 class="card-title">Nanjing University of Posts and Telecommunications</h3>
        <p class="card-description"><strong>Bachelor of Software Engineering</strong><br>2009 - 2013<br><em>Foundation in software development and computer science</em></p>
      </div>
    </div>
  </div>
</div>

<!-- Publications Section -->
<div class="section">
  <div class="container">
    <div class="section-header">
      <h2 class="section-title">Publications</h2>
      <p class="section-subtitle">Contributing to blockchain security, graph neural networks, and privacy-preserving technologies</p>
    </div>
    
    <div class="content-block">
      <p>My research contributions span blockchain security, graph neural networks, and privacy-preserving technologies, with publications at top-tier venues including NDSS, ICML, ICDM, and ACM AsiaCCS.</p>
      
      <div class="stats-grid">
        <div class="stat-card">
          <div class="stat-number">15+</div>
          <div class="stat-label">Peer-Reviewed Papers</div>
        </div>
        <div class="stat-card">
          <div class="stat-number">A/A*</div>
          <div class="stat-label">CORE Venues</div>
        </div>
        <div class="stat-card">
          <div class="stat-number">3</div>
          <div class="stat-label">Research Areas</div>
        </div>
      </div>
      
      <p style="text-align: center; margin-top: 40px;">
        <a href="publication/overview.md" class="hero-link" style="color: #007aff; border-color: #007aff;">View Complete Publication List</a>
      </p>
    </div>
  </div>
</div>

<!-- Professional Experience Section -->
<div class="section">
  <div class="container">
    <div class="section-header">
      <h2 class="section-title">Experience</h2>
      <p class="section-subtitle">Professional journey in blockchain research and software development</p>
    </div>
    
    <div class="card-grid">
      <div class="card">
        <div class="card-icon">💻</div>
        <h3 class="card-title">Software Programmer</h3>
        <p class="card-description"><strong>Monash University</strong><br>Dec 2020 - Present<br><br>Leading full-stack development for blockchain research projects, coordinating cross-functional teams, and bridging academic research with practical implementation.</p>
      </div>
      
      <div class="card">
        <div class="card-icon">👨‍🏫</div>
        <h3 class="card-title">Teaching Associate</h3>
        <p class="card-description"><strong>Monash University</strong><br>Jul 2020 - Dec 2020<br><br>Conducted Network Security tutorials, mentored students in cybersecurity concepts, and developed educational materials.</p>
      </div>
      
      <div class="card">
        <div class="card-icon">📊</div>
        <h3 class="card-title">Research Assistant</h3>
        <p class="card-description"><strong>Monash University</strong><br>Sep 2019 - Nov 2020<br><br>Spearheaded data analysis and modeling projects, enhanced AI integration, and developed machine learning models.</p>
      </div>
    </div>
  </div>
</div>

<!-- Achievements Section -->
<div class="section">
  <div class="container">
    <div class="section-header">
      <h2 class="section-title">Notable Achievements</h2>
      <p class="section-subtitle">Recognition and leadership in blockchain research and education</p>
    </div>
    
    <div class="card-grid">
      <div class="card">
        <div class="card-icon">🏗️</div>
        <h3 class="card-title">ACE-SIP Blockchain Hackathon</h3>
        <p class="card-description"><strong>Organizer</strong><br>Sep 2022 - Dec 2022<br><br>Led comprehensive blockchain hackathon focused on sustainability informatics, coordinating projects across environmental and social impact themes.</p>
      </div>
      
      <div class="card">
        <div class="card-icon">🎓</div>
        <h3 class="card-title">Summer Research Scholarship</h3>
        <p class="card-description"><strong>Monash University</strong><br>Dec 2019 - Mar 2020<br><br>Developed advanced encrypted database systems and enhanced data security frameworks for academic and commercial applications.</p>
      </div>
    </div>
  </div>
</div>

<!-- Contact Section -->
<div class="section">
  <div class="container">
    <div class="section-header">
      <h2 class="section-title">Let's Connect</h2>
      <p class="section-subtitle">Open to collaborations in blockchain security, privacy-preserving technologies, and graph neural networks</p>
    </div>
    
    <div class="content-block">
      <div style="text-align: center;">
        <p style="font-size: 21px; margin-bottom: 30px;">Ready to collaborate on cutting-edge blockchain security research?</p>
        
        <div class="hero-links" style="margin-bottom: 40px;">
          <a href="mailto:Wayne.Yang@Monash.edu" class="hero-link" style="color: #007aff; border-color: #007aff;">
            <i class="fas fa-envelope"></i> Wayne.Yang@Monash.edu
          </a>
          <a href="mailto:xyan0559@sydney.edu.au" class="hero-link" style="color: #007aff; border-color: #007aff;">
            <i class="fas fa-envelope"></i> xyan0559@sydney.edu.au
          </a>
        </div>
        
        <div class="hero-links">
          <a href="https://scholar.google.com.au/citations?user=j9YiIqMAAAAJ&hl=en" target="_blank" class="hero-link" style="color: #007aff; border-color: #007aff;">
            <i class="fas fa-graduation-cap"></i> Google Scholar
          </a>
          <a href="https://www.linkedin.com/in/xiangwen-wayne-yang-272572158/" target="_blank" class="hero-link" style="color: #007aff; border-color: #007aff;">
            <i class="fab fa-linkedin"></i> LinkedIn
          </a>
        </div>
        
        <p style="margin-top: 40px; color: #86868b;">
          <strong>Affiliations:</strong><br>
          Monash University - Department of Software Systems and Cybersecurity<br>
          University of Sydney - School of Computer Science and Engineering
        </p>
      </div>
    </div>
  </div>
</div>

<!-- Footer -->
<div style="background: #f5f5f7; padding: 60px 0; text-align: center; margin-top: 80px;">
  <div class="container">
    <p style="font-size: 19px; color: #86868b; font-style: italic;">
      "Bridging the gap between theoretical blockchain security and practical implementation"
    </p>
  </div>
</div>
