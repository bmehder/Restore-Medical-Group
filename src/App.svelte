<script>
  import { fade } from "svelte/transition";
  import { quintOut } from "svelte/easing";
  import Header from "./Layouts/Header.svelte";
  import Section from "./Layouts/Section.svelte";
  import Grid from "./Layouts/Grid.svelte";
  import Flex from "./Layouts/Flex.svelte";
  import Hero from "./UI/Hero.svelte";
  import CTA from "./UI/CTA.svelte";
  import Button from "./UI/Button.svelte";
  import Form from "./UI/Form.svelte";
  import Footer from "./Layouts/Footer.svelte";

  let page = "Home";
  const handleNav = (e) => (page = e.detail);
</script>

<div class="wrapper">
  <Header on:nav={handleNav} background="#333" />
  <main>
    <Section boxed background="white">
      <img
        src="/header-restore-medical-group.jpg"
        alt="Header - Restore Medical Group" />
    </Section>
    {#if page === 'Home'}
      <div transition:fade={{ easing: quintOut }}>
        <Section background="white" padding="0.5em 2em 0em" boxed>
          <h3>Welcome to a revolution in chronic wound care.</h3>
          <Grid columns="1fr 1fr" gap="2em">
            <article>
              <p>
                Welcome to the
                <strong>Restore Medical Group</strong>
                Wound Care division - a truly unique health care practice.
                Restore Medical Group has developed an insurance backed protocol
                for treating recalcitrant wounds that prove difficult to heal
                using conventional wound care methods.
              </p>

              <p>
                Our treatment protocol incorporates a combination of therapies
                including our exclusively sourced amnio products that rapidly
                promote healing in wound areas.
              </p>

              <p>
                Our approach can provide either in-clinic or on-location care
                options.
              </p>

              <p><strong>Insurance Accepted:</strong> Medicare Part B</p>
            </article>
            <figure>
              <img
                src="https://source.unsplash.com/random/300x200?1"
                alt="Restore Medical Group" />
            </figure>
          </Grid>
        </Section>

        <Section boxed background="white" padding="2em">
          <hr />
        </Section>

        <Section background="white" padding="0.5em 2em 4em" boxed>
          <h4>Identifying Patients</h4>
          <Grid columns="1fr 1fr" gap="2em">
            <article>
              <p>
                When evaluating patients for this protocol please consider the
                following before recommending care.
              </p>
              <p>
                When evaluating patients referral please consider the following
                contraindications:
              </p>
              <ul>
                <li>infected wound,</li>
                <li>active cancer treatment,</li>
                <li>and/or immunosuppressive treatment.</li>
              </ul>

              <h5>Pre-Assessment</h5>
              <p>
                Restore Medical will conduct assessment and amnio products
                preauthorization on all patients prior to treatment to ensure
                the protocol is applicable and insurance is confirmed for the
                treatment.
              </p>

              <h5>Transport</h5>
              <p>
                Transport to our clinical locations can be arranged on behalf of
                the patient if not provided with their current facility or home
                care provider.
              </p>
            </article>

            <figure>
              <img
                src="https://source.unsplash.com/random/300x200?2"
                alt="Restore Medical Group" />
            </figure>
          </Grid>
        </Section>

        <Section boxed>
          <Hero
            background="https://images.unsplash.com/photo-1546805220-8638b5ff0d42?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=802&q=80"
            height="400px"
            padding="0 0 2em 0">
            <CTA
              heading="We travel to you!"
              subtitle="To schedule an on-site patient evaluation appointment, please call (303) 216-2661."
              href="tel:3032162661"
              buttonText="Call Today!"
              src="https://source.unsplash.com/random/400x400?10" />
          </Hero>
        </Section>
      </div>
    {/if}

    {#if page === 'Case Studies'}
      <div transition:fade={{ easing: quintOut }}>
        <Section boxed background="white" padding="0.5em 2em 0em">
          <h3 style="text-align:center;">Case Studies</h3>
          <Grid columns="1fr 1fr" gap="2em">
            <div>
              <h5 class="before-after">Before</h5>
              <div>
                <img
                  src="https://source.unsplash.com/random/400x400?4"
                  alt="before" />
                <aside>
                  6.5CM wide persistent wound unable to be healed with
                  traditional treatments.
                </aside>
              </div>
            </div>
            <div>
              <h5 class="before-after">After</h5>
              <div>
                <img
                  src="https://source.unsplash.com/random/400x400?5"
                  alt="after" />
                <aside>
                  After 7 weeks of treatment using Restore’s Wound Care
                  Protocol.
                </aside>
              </div>
            </div>
          </Grid>
          <Grid columns="1fr 1fr" gap="2em">
            <div>
              <h5 class="before-after">Before</h5>
              <div>
                <img
                  src="https://source.unsplash.com/random/400x400?6"
                  alt="before" />
                <aside>Picture taken 2 weeks into treatment</aside>
              </div>
            </div>
            <div>
              <h5 class="before-after">After</h5>
              <div>
                <img
                  src="https://source.unsplash.com/random/400x400?7"
                  alt="after" />
                <aside>Picture taken 3-4 weeks into treatment</aside>
              </div>
            </div>
          </Grid>
          <Grid columns="1fr 1fr" gap="2em">
            <div>
              <h5 class="before-after">Before</h5>
              <div>
                <img
                  src="https://source.unsplash.com/random/400x400?8"
                  alt="before" />
                <aside>Two year old sacrum wound starting at 5.5CM</aside>
              </div>
            </div>
            <div>
              <h5 class="before-after">After</h5>
              <div>
                <img
                  src="https://source.unsplash.com/random/400x400?9"
                  alt="after" />
                <aside>Reduced to 3.5CM in 4 weeks. Still in treatment.</aside>
              </div>
            </div>
          </Grid>
          <Grid columns="1fr 1fr" gap="2em">
            <div>
              <h5 class="before-after">Before</h5>
              <div>
                <img
                  src="https://source.unsplash.com/random/400x400?9"
                  alt="before" />
                <aside>
                  Two wounds being simultaneously treated on the left gluteus.
                  Persistent wound for nearly 6 months unable to be treated with
                  conventional treatment. In this first picture the little arrow
                  is pointing to a tunnel wound that is 6 centimeters deep and
                  1CM wide at entry.. The second wound is roughly 15CM square.
                </aside>
              </div>
            </div>
            <div>
              <h5 class="before-after">After</h5>
              <div>
                <img
                  src="https://source.unsplash.com/random/400x400?10"
                  alt="after" />
                <aside>
                  The second picture shows the arrow is pointing to that same
                  wound within several weeks of treatment. Estimated to be
                  nearly closed to 60%. The second wound has an obvious big
                  change and progressing nicely towards full healing.
                </aside>
              </div>
            </div>
          </Grid>
        </Section>
      </div>
    {/if}

    {#if page === 'Contact'}
      <div transition:fade={{ easing: quintOut }}>
        <Section boxed background="white" padding="0.5em 2em 0em">
          <Flex direction="column" justify="center" align="center">
            <CTA
              heading="Schedule an Appointment"
              subtitle="<big><strong>(303) 216-2661</strong></big>"
              href="tel:3032162661"
              buttonText="Call Today!"
              src="https://source.unsplash.com/random/400x400?10" />

            <p style="text-align:center;">
              <big><strong>Restore Medical Group</strong></big><br />
              is a DBA of<br />
              Restore Osteo of Colorado, LLC<br />
              400 Indian Street, Suite 280<br />
              Golden, CO 80401
            </p>
            <Button>Get Directions</Button>

            <h3>Send Us A Message</h3>

            <Form
              buttonColor="dodgerblue"
              buttonText="Send Message"
              buttonTextColor="white" />
          </Flex>
        </Section>
      </div>
    {/if}
  </main>
  <Footer background="#333" color="#eee">
    Restore Medical Group is a DBA of Restore Osteo of Colorado, LLC
  </Footer>
</div>

<style>
  .wrapper {
    display: grid;
    grid-template-rows: auto 1fr auto;
    min-height: 100vh;
  }
  main {
    background: linear-gradient(
      to bottom right,
      transparent,
      rgba(0, 0, 0, 0.24)
    );
  }
  .before-after {
    margin-top: 2em;
    text-align: center;
    font-size: 150%;
  }
  aside {
    display: block;
    background: #eee;
    text-align: center;
    padding: 2em;
  }
  img {
    width: 100%;
    height: auto;
    object-fit: cover;
    border-radius: 2px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.24);
  }
  @media (min-width: 640px) {
  }
</style>
