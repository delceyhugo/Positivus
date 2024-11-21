<script setup>
import { ref } from 'vue'
import Header from './components/Header.vue'
import Button from './components/base/Button.vue'
import Logotypes from './components/Logotypes.vue'
import HeadingSub from './components/HeadingSub.vue'
import ServiceBlock from './components/ServiceBlock.vue'
import CaseStudies from './components/CaseStudies.vue'
import ProcessBlock from './components/ProcessBlock.vue'
import TeamCard from './components/TeamCard.vue'
import Testimonial from './components/TestimonialSlider.vue'
import Contact from './components/Contact.vue'
import Footer from './components/Footer.vue'

</script>

<template>

  <div id="LandingPage" class="no-padding">
    <Header></Header>
    <main>
      <div id="hero">
        <section>
          <h1>Navigating the digital landscape for success</h1>
          <p>Our digital marketing agency helps businesses grow and succeed online through a range of services including SEO, PPC, social media marketing, and content creation.</p>
          <img src="@/assets/hero-illustration.png" alt="Illustration of a megaphone">
          <Button :type="'primary'">Book a consultation</Button>
        </section>
      </div>
    </main>
    <aside>
      <Logotypes></Logotypes>
    </aside>
  </div>
  <section id="Services">
    <HeadingSub :title="'Services'">
      At our digital marketing agency, we offer a range of services to help businesses grow and succeed online. These services include:
    </HeadingSub>
    <main>
      <ServiceBlock :setup="{title: 'Search engine optimization', labelType: 'tertiary', linkType: 'secondary', linkColor: 3, cardColor: 'bg', img: 'loupe'}"></ServiceBlock>
      <ServiceBlock :setup="{title: 'Pay-per-click advertising', labelType: 'secondary', linkType: 'secondary', linkColor: 3, cardColor: 'accent', img: 'click'}"></ServiceBlock>
      <ServiceBlock :setup="{title: 'Social Media Marketing', labelType: 'secondary', linkType: 'secondary', linkColor: 4, cardColor: 'dark', img: 'screen'}"></ServiceBlock>
      <ServiceBlock :setup="{title: 'Email Marketing', labelType: 'tertiary', linkType: 'secondary', linkColor: 3, cardColor: 'bg', img: 'letter'}"></ServiceBlock>

      <ServiceBlock :setup="{title: 'Pay-per-click advertising', labelType: 'secondary', linkType: 'secondary', linkColor: 3, cardColor: 'accent', img: 'tab'}"></ServiceBlock>
      <ServiceBlock :setup="{title: 'Social Media Marketing', labelType: 'tertiary', linkType: 'secondary', linkColor: 4, cardColor: 'dark', img: 'chart'}"></ServiceBlock>
    </main>
  </section>
  <section id="CTA" class="no-padding">
    <div>
      <h3>Let's make things happen</h3>
      <p>Contact us today to learn more about how our digital marketing services can help your business grow and succeed online.</p>
      <Button :type="'primary'">Get your free proposal</Button>
    </div>
    <img src="@/assets/cta-illustration.webp" alt="">
  </section>
  <section id="CaseStudies" class="no-padding">
    <HeadingSub :title="'Case Studies'">
      Explore Real-Life Exemples of Our Proven Digital Marketing Success through Our Case Studies
    </HeadingSub>
    <CaseStudies></CaseStudies>
  </section>
  <section id="WorkingProcess">
    <HeadingSub :title="'Our Working Process'">
      Step-by-Step Guide to Achieving Your Business Goals
    </HeadingSub>
    <main>
      <ProcessBlock :title="'Consultation'" :number="'01'">During the initial consultation, we will discuss your business goals and objectives, target audience, and current marketing efforts. This will allow us to understand your needs and tailor our services to best fit your requirements.</ProcessBlock>
      <ProcessBlock :title="'Research and Strategy Development'" :number="'02'">Once we have a clear understanding of your business, we will develop a comprehensive strategy for digital marketing that aligns with your goals.</ProcessBlock>
      <ProcessBlock :title="'Implementation'" :number="'03'" >Once the strategy is finalized, we will implement the digital marketing campaign to drive traffic, engagement, and conversions.</ProcessBlock>
      <ProcessBlock :title="'Monitoring and Optimization'" :number="'04'">We will monitor the campaign's performance and make adjustments as needed to optimize its effectiveness and reach your target audience.</ProcessBlock>
      <ProcessBlock :title="'Reporting and Communication'" :number="'05'">We will provide regular updates on campaign progress, results, and any areas for improvement.</ProcessBlock>
      <ProcessBlock :title="'Continual Improvement'" :number="'06'">We will continue to monitor and optimize the campaign to ensure it remains effective and relevant to your audience.</ProcessBlock>
    </main>

  </section>
  <section id="Team">
    <HeadingSub :title="'Team'">
      Meet the skilled team behind our successful digital marketing strategies
    </HeadingSub>
    <main>
      <TeamCard :setup="{name: 'John Smith', job: 'CEO and Founder', img: '1'}">10+ years of experience in digital marketing. Expertise in SEO, PPC, and content strategy</TeamCard>
      <TeamCard :setup="{name: 'Jane Dow', job: 'Director of Operations', img: '2'}">7+ years of experience in project management and team leadership. Strong organizational and communication skills</TeamCard>
      <TeamCard :setup="{name: 'Mickael Brown', job: 'Senior CEO Specialist', img: '3'}">5+ years of experience in SEO and content creation. Proficient in keyword research and on-page optimization</TeamCard>
      <TeamCard :setup="{name: 'Emily Davis', job: 'PPC Manager', img: '4'}">3+ years of experience in paid search advertising. Skilled in campaign management and performance analysis</TeamCard>
      <TeamCard :setup="{name: 'Brian White', job: 'Social Media Specialist', img: '5'}">4+ years of experience in social media marketing. Proficient in creating and scheduling content, analyzing metrics, and building engagement</TeamCard>
      <TeamCard :setup="{name: 'Sarah Green', job: 'Content Creator', img: '6'}">2+ years of experience in writing and editing<br>Skilled in creating compelling, SEO-optimized content for various industries</TeamCard>
    </main>
    <footer>
      <Button>See all team</Button>
    </footer>
  </section>
  <section id="Testimonials">
    <HeadingSub :title="'Testimonials'">
      Hear from Our Satisfied Clients: Read Our Testimonials to Learn More about Our Digital Marketing Services
    </HeadingSub>
    <Testimonial></Testimonial>
  </section>
  <section id="Contact">
    <HeadingSub :title="'Contact Us'">
      Connect with Us: Let's Discuss Your Digital Marketing Needs
    </HeadingSub>
    <Contact></Contact>
  </section>
  <section id="Footer">
    <Footer></Footer>
  </section>

</template>

<style lang="scss" scoped>
// Breakpoints
$small : 480px;
$med : 768px;
$large : 1280px;

#LandingPage{
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  gap: 70px;
  @media screen and (max-width: $large) {
    >header{
      padding: 20px 5vw !important;
    } 
    >main{
      padding: 0px 5vw !important;
    }
  }
  main{
    #hero{
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 15vw;
      section{
        flex: 1;
        display: grid;
        align-items: center;
        justify-items: center;
        grid-template: 
        "a d" auto
        "b d" auto
        "c d" auto / minmax(0px, 501px) 1fr;
        gap: 35px;
        @media screen and (max-width: $large) {
          display: grid;
          justify-items: center;
          grid-template: 
            "a a" auto
            "b d" auto
            "c d" auto;
        }
        @media screen and (max-width: $med) {
          display: grid;
          justify-items: stretch;
          grid-template: 
            "a" auto
            "d" auto
            "b" auto
            "c" auto;
        }
        h1{
          grid-area: a;
        }
        p{
          grid-area: b;
          font-size: 20px;
          line-height: 28px;
        }
        img{
          grid-area: d;
          width: 100%;
          max-width: 600px;
        }
        :last-child{
          grid-area: c;
        }
      }
    }
  }
}
#Services{
  display: flex;
  flex-direction: column;
  justify-content: center;
  gap: 70px;
  main{
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 50px;
    @media screen and (max-width: $med) {
      grid-template-columns: 1fr;
    }
  }
}
#CTA{
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  background-color: var(--color-bg);
  border-radius: 45px;
  justify-content: space-around;
  margin: 0px 5vw;
  div{
    display: flex;
    flex-direction: column;
    gap: 35px;
    @media screen and (min-width: $large) {
      max-width: 501px;
      padding: 3vw 5vw !important;
    }
    @media screen and (max-width: $large) and (min-width: $med) {
      margin: 20px 30px;
    }
    @media screen and (max-width: $med) {
      padding: 3vw 5vw !important;
    }
  }
  img{
    position: relative;
    transform: scale(1.15);
    pointer-events: none;
    @media screen and (max-width: $large) {
      display: none;
    }
  }
}
#CaseStudies{
  display: flex;
  flex-direction: column;
  justify-content: center;
  gap: 70px;
  &>:first-child{
    padding: 0px 5vw;
  }
}
#WorkingProcess{
  display: flex;
  flex-direction: column;
  justify-content: center;
  gap: 70px;
  main{
    display: flex;
    flex-direction: column;
    gap: 30px;
  }
}
#Team{
  display: flex;
  flex-direction: column;
  justify-content: center;
  gap: 70px;
  main{
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    gap: 40px;
    @media screen and (max-width: $large) {
      grid-template-columns: 1fr 1fr;
    }
    @media screen and (max-width: $med) {
      grid-template-columns: 1fr;
    }
  }
  footer{
    display: flex;
    justify-content: flex-end;
    @media screen and (max-width: $med) {
      flex-direction: column;
    }
    button{
      padding: 15px 75px !important;
    }
  }

}
#Testimonials{
  display: flex;
  flex-direction: column;
  justify-content: center;
  gap: 70px;
}
#Contact{
  display: flex;
  flex-direction: column;
  justify-content: center;
  gap: 70px;
}
#Footer{
  display: flex;
  flex-direction: column;
  justify-content: center;
  gap: 70px;
}
</style>