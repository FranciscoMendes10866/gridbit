<template>
  <div>
    <!-- Hero Landing -->
    <section class="hero bg pt-6">
      <div class="hero-body">
        <div class="container has-text-centered-desktop has-text-left-mobile">
          <div class="columns is-centered">
            <div class="column is-12-mobile is-12-tablet is-8-desktop">
              <h5 class="intro is-size-4">Introducing GridBit</h5>
              <h1 class="mt-3 has-text-white has-text-weight-bold is-size-1">
                Random Password Generator
              </h1>
              <p class="mt-4 has-text-grey-light is-size-4">
                Linear helps streamline software projects, sprints, tasks, and
                bug tracking. It's built for high-performance teams.
              </p>
              <vs-button class="reset mt-6" size="large" primary floating>
                <i class="bx bxs-down-arrow"></i>
                &nbsp;Learn more</vs-button
              >
            </div>
          </div>
        </div>
      </div>
    </section>
    <!-- Generator -->
    <Generator />
    <!-- Safety section -->
    <section class="hero has-background-black-bis py-6">
      <div class="hero-body">
        <div class="container">
          <div class="columns">
            <div class="column is-5">
              <h1 class="is-size-1 has-text-white has-text-weight-semibold">
                Safety.
              </h1>
              <p class="has-text-grey is-size-5 mt-5">
                All passwords you create with GridBit are generated on your
                computer.
              </p>
              <p class="has-text-grey is-size-5 mt-5">
                They are not saved or shared anywhere else. Not even GridBit can
                see the password you create.
              </p>
              <p class="has-text-grey is-size-5 mt-5">
                Just be sure to close this page once you’ve generated and copied
                your password to prevent anyone else from seeing it if they use
                your computer.
              </p>
            </div>
          </div>
        </div>
      </div>
    </section>
    <!-- Randomness section -->
    <section class="hero bg py-6">
      <div class="hero-body">
        <div class="container">
          <div class="columns">
            <div class="column is-5">
              <h1 class="is-size-1 has-text-white has-text-weight-semibold">
                Randomness.
              </h1>
              <p class="has-text-grey-light is-size-5 mt-5">
                People often use words or numbers that mean something to them.
                The problem with this is that you end up with passwords that are
                easy to guess.
              </p>
              <p class="has-text-grey-light is-size-5 mt-5">
                And an ordinary desktop computer can test over a hundred million
                passwords per second.
              </p>
              <p class="has-text-grey-light is-size-5 mt-5">
                So don’t risk it. Use a random password generator to create
                truly random passwords that even the strongest computers can’t
                crack.
              </p>
            </div>
          </div>
        </div>
      </div>
    </section>
    <!-- Singularity section -->
    <section class="hero has-background-black-bis py-6">
      <div class="hero-body">
        <div class="container">
          <div class="columns">
            <div class="column is-5">
              <h1 class="is-size-1 has-text-white has-text-weight-semibold">
                Singularity.
              </h1>
              <p class="has-text-grey is-size-5 mt-5">
                Using the same password across multiple accounts is a huge
                no-no.
              </p>
              <p class="has-text-grey is-size-5 mt-5">
                If hackers learn the password to one of your accounts, they’ll
                have your password for all the others, too.
              </p>
              <p class="has-text-grey is-size-5 mt-5">
                So never recycle passwords. Use different, unique passwords for
                every account.
              </p>
            </div>
          </div>
        </div>
      </div>
    </section>
    <!-- Robust section -->
    <section class="hero bg py-6">
      <div class="hero-body">
        <div class="container">
          <div class="columns">
            <div class="column is-5">
              <h1 class="is-size-1 has-text-white has-text-weight-semibold">
                Robust.
              </h1>
              <p class="has-text-grey-light is-size-5 mt-5">
                Remember, short passwords are weak passwords. They’re too easily
                cracked.
              </p>
              <p class="has-text-grey-light is-size-5 mt-5">
                For the best password security, you need a long, complex
                password composed of a random string of characters.
              </p>
              <p class="has-text-grey-light is-size-5 mt-5">
                You should also avoid common words and phrases to prevent a
                dictionary attack.
              </p>
              <p class="has-text-grey-light is-size-5 mt-5">
                Only then will you have a strong password.
              </p>
            </div>
          </div>
        </div>
      </div>
    </section>
    <!-- Go Bact to top section -->
    <section class="hero has-background-black-bis py-6">
      <div class="hero-body">
        <div class="container">
          <div class="columns is-centered has-text-centered">
            <div class="column is-8">
              <h1 class="is-size-1 has-text-white has-text-weight-semibold">
                Have you got it?
              </h1>
              <p class="has-text-grey is-size-5 mt-5">
                I hope you understand why you should use GridBit.
              </p>
              <vs-button class="reset mt-6" size="large" primary floating>
                <i class="bx bxs-up-arrow"></i>
                &nbsp;Back To Top</vs-button
              >
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import Generator from '../components/Generator'

export default {
  components: {
    Generator,
  },
}
</script>

<style>
.reset {
  margin: auto;
}
.intro {
  color: rgb(0, 60, 255);
}
.bg {
  background: #1c1d1f;
}
.bg-card {
  background: linear-gradient(180deg, #28292c 0%, rgba(39, 40, 43, 0.82) 100%);
  box-shadow: 0px 13px 40px rgba(0, 0, 0, 0.3), 0px 4px 4px rgba(0, 0, 0, 0.2);
  border: none;
  border-radius: 16px;
}
</style>
