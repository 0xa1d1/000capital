<template>
  <header id="header">
    <nav id="main-navigation">
      <a :href="`#${section.id}`" :class="{ 'active': currentSection === section.id }" v-for="section in sections"
        :key="section.id">
        <span class="title">{{ section.name }}</span>
        <span class="ticker"></span>
      </a>
    </nav>
    <div id="container" class="container"></div>
  </header>
  <main id="main" data-bs-spy="scroll" data-bs-target="#main-navigation">
    <div class="section home section-with-link" id="home">
      <div class="section-inner container px-4">
        <div class="text-center px-4 px-md-0"><img class="img-fluid" src="./assets/hero.svg" @load="pageReady = true;"></div>
        <div class="text-center subheading mt-5 pt-4" ref="scrambleText" style="height:20px">WE'RE BUSY ADDING ZEROS</div>

        <a href="mailto:venture@000.capital" class="section-link">
          <span class="text-end">Get Funding</span>
          <svg xmlns="http://www.w3.org/2000/svg" width="40" height="40" viewBox="0 0 40 40" fill="none" stroke="#fff"
            stroke-width="1">
            <g transform="translate(-90 -4935)">
              <g transform="translate(90 4935)">
                <rect width="40" height="40" stroke="none"></rect>
                <rect x="0.5" y="0.5" width="39" height="39" fill="none"></rect>
              </g>
            </g>
            <g transform="translate(14 14)">
              <path d="M0,0,5.545,5.546,0,11.091" transform="translate(9.843 2) rotate(45)" fill="none" stroke="#fff"
                stroke-width="2"></path>
              <line x1="9" y1="9" fill="none" stroke="#fff" stroke-width="2"></line>
            </g>
          </svg>
        </a>
      </div>
    </div>

    <div class="section-heading container d-md-none">
      <div class="angle-down opacity-50 mb-2"></div>
      <div class="angle-down"></div>
    </div>
    <div class="section-heading container">
      <div class="heading">Members</div>
    </div>
    <div class="section members section-with-link" id="members">
      <div class="section-inner container py-3 py-md-5">
        <div class="members-gallery" id="members-gallery">
          <a class="member-item" v-for="(m, i) in members" :key="i" :href="`https://twitter.com/${m.x}`" target="_blank">
            <figure>
              <img class="img-fluid" :src="require(`@/assets/pfps/${m.file}`)">
            </figure>
            <div class="member-name">@{{ m.x }}</div>
            <div class="member-social">{{ m.job }}</div>
          </a>
        </div>
        <a href="mailto:venture@000.capital" class="section-link">
          <span class="text-end">Apply to Join 000</span>
          <svg xmlns="http://www.w3.org/2000/svg" width="40" height="40" viewBox="0 0 40 40" fill="none" stroke="#fff"
            stroke-width="1">
            <g transform="translate(-90 -4935)">
              <g transform="translate(90 4935)">
                <rect width="40" height="40" stroke="none"></rect>
                <rect x="0.5" y="0.5" width="39" height="39" fill="none"></rect>
              </g>
            </g>
            <g transform="translate(14 14)">
              <path d="M0,0,5.545,5.546,0,11.091" transform="translate(9.843 2) rotate(45)" fill="none" stroke="#fff"
                stroke-width="2"></path>
              <line x1="9" y1="9" fill="none" stroke="#fff" stroke-width="2"></line>
            </g>
          </svg>
        </a>
      </div>
    </div>

    <div class="section-heading container-fluid">
      <div class="heading">Portfolio</div>
    </div>
    <div class="section portfolio pb-0" id="portfolio">
      <div class="section-inner section-inner-portfolio container py-3 py-md-5">
        <div class="portfolio-container" id="portfolio-gallery">
          <a class="portfolio-item" href="https://steadystack.io/" target="_blank">
            <div class="portfolio-icon">
              <img class="img-fluid" src="./assets/steadystack.png">
            </div>
            <div class="portfolio-body">
              <div class="portfolio-title">Steady Stack</div>
              <div class="portfolio-text">Venture Capital</div>
            </div>
          </a>
        </div>
      </div>
    </div>

    <footer id="footer">
      <div class="container">
        <div class="row align-items-center">
          <div class="col-auto d-none d-lg-block order-lg-1">
            <img class="img-fluid" src="./assets/logo.svg">
          </div>
          <div class="col text-center text-lg-start order-lg-2 order-3 mt-5 mt-lg-0">
            © 2024 000 CAPITAL. All rights reserved.
          </div>
          <div class="col-lg-auto order-1 order-lg-3">
            <a href="mailto:venture@000.capital" class="nav-link">
              <svg xmlns="http://www.w3.org/2000/svg" width="40" height="40" viewBox="0 0 40 40" fill="none" stroke="#fff"
                stroke-width="1">
                <g transform="translate(-90 -4935)">
                  <g transform="translate(90 4935)">
                    <rect width="40" height="40" stroke="none"></rect>
                    <rect x="0.5" y="0.5" width="39" height="39" fill="none"></rect>
                  </g>
                  <path
                    d="M16.7,59.882H1.728A1.73,1.73,0,0,0,0,61.61V71.978a1.73,1.73,0,0,0,1.728,1.728H16.7a1.73,1.73,0,0,0,1.728-1.728V61.61A1.73,1.73,0,0,0,16.7,59.882Zm0,1.152a.573.573,0,0,1,.221.045L9.216,67.76,1.507,61.079a.573.573,0,0,1,.221-.045Zm0,11.52H1.728a.576.576,0,0,1-.576-.576V62.3l7.687,6.662a.577.577,0,0,0,.755,0L17.28,62.3v9.682A.576.576,0,0,1,16.7,72.554Z"
                    transform="translate(101 4888.118)" fill="#fff"></path>
                </g>
              </svg>
              <span>venture@000.capital</span>
            </a>

          </div>
          <div class="col-lg-auto order-2 order-lg-4">
            <a href="https://twitter.com/000_capital" target="_blank" class="nav-link">
              <svg xmlns="http://www.w3.org/2000/svg" width="40" height="40" viewBox="0 0 40 40" fill="none" stroke="#fff"
                stroke-width="1">
                <g transform="translate(-90 -5000)">
                  <g transform="translate(90 5000)">
                    <rect width="40" height="40" stroke="none"></rect>
                    <rect x="0.5" y="0.5" width="39" height="39" fill="none"></rect>
                  </g>
                  <path
                    d="M9.687,6.9,15.746,0H14.311L9.047,5.988,4.846,0H0L6.354,9.055,0,16.288H1.435L6.99,9.963l4.437,6.325h4.846M1.953,1.06H4.159L14.31,15.28H12.1"
                    transform="translate(102 5012)" fill="#fff"></path>
                </g>
              </svg>
              <span>@000_capital</span>
            </a>
          </div>
        </div>
      </div>
    </footer>
  </main>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      currentSection: null,
      pageReady: false,
      sections: [
        { name: 'Home', id: 'home' },
        { name: 'Members', id: 'members' },
        { name: 'Portfolio', id: 'portfolio' },
      ],
      members: [
        { file: 'dtk.png', x: '0x_eth_', job: 'Fund & Risk Management' },
        { file: 'gfl.jpeg', x: 'gofuckinglong', job: 'Biz Dev' },
        { file: 'zezima.png', x: 'zezima_233', job: 'Angel' },
        { file: 'goku.jpeg', x: 'imCryptoGoku', job: 'Analyst' },
        { file: 'bittm.jpg', x: 'Bittm_', job: 'Analyst' },
        { file: 'jack.jpg', x: 'jackhaute', job: 'Analyst' },
        { file: 'fizzi.png', x: 'Fizziohh', job: 'Analyst' },
        { file: 'pingpong.png', x: 'DegenMAYC', job: 'NFT Researcher' },
        { file: 'popiwops.jpeg', x: 'popiwops', job: 'Trader' },
        { file: 'selca.jpg', x: 's3lc4', job: 'Trader' },
        { file: 'sofa.png', x: 'sofacestmoi', job: 'Trader' },
        { file: 'stu.png', x: 'stu_vrai_', job: 'Pet' },
        { file: 'cdec.png', x: 'c_de_c', job: 'Data Engineer' },
        { file: 'rxbt.png', x: '0rxbt', job: 'Dev' }
      ]
    }
  },
  mounted() {
    window.addEventListener('scroll', this.onScroll);
    this.onScroll();
    this.scrambleText();
  },
  beforeUnmount() {
    window.removeEventListener('scroll', this.onScroll);
  },
  methods: {
    scrambleText() {
      const element = this.$refs.scrambleText;
      const originalText = element.innerText;
      let scrambledText = '';
      const scrambleDuration = 1000; // Duration of the effect in milliseconds
      const scrambleIntervalTime = 30; // Time between each scramble in milliseconds
      let elapsedTime = 0;

      const scrambleInterval = setInterval(() => {
        scrambledText = '';

        for (let i = 0; i < originalText.length; i++) {
          scrambledText += this.randomChar();
        }

        element.innerText = scrambledText;

        elapsedTime += scrambleIntervalTime;
        if (elapsedTime >= scrambleDuration) {
          clearInterval(scrambleInterval);
          element.innerText = originalText; // Reset to original text after scrambling
        }
      }, scrambleIntervalTime);
    },
    randomChar() {
      const chars = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789!@#$%^&*()-_=+[{]};:\'",<.>/?';
      return chars.charAt(Math.floor(Math.random() * chars.length));
    },
    onScroll() {
      const sections = document.querySelectorAll('.section');
      const scrollPosition = window.scrollY + window.innerHeight / 3; // Adjusted to a third of the viewport
      let currentActive = this.currentSection;

      for (const section of sections) {
        const sectionTop = section.offsetTop;
        const sectionHeight = section.offsetHeight;

        // Section becomes active when its top is less than a third of the viewport height from the top
        if (scrollPosition >= sectionTop && scrollPosition < sectionTop + sectionHeight) {
          currentActive = section.id;
          break; // Break the loop once the active section is found
        }
      }

      // Check if the user has scrolled to the bottom of the page
      if ((window.innerHeight + window.scrollY) >= document.body.offsetHeight) {
        currentActive = sections[sections.length - 1].id;
      }

      this.currentSection = currentActive;
    }
  }
}
</script>
