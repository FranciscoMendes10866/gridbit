<template>
  <section class="hero bg pb-6">
    <div class="hero-body">
      <div class="container has-text-centered">
        <div class="columns is-centered">
          <div class="column is-6">
            <div class="card bg-card">
              <div class="card-content">
                <div class="content">
                  <h5
                    class="has-text-grey-light is-size-3 has-text-weight-light"
                  >
                    {{ generatedPassword }}
                  </h5>
                  <div class="level">
                    <div
                      v-for="(option, index) in optiondata"
                      :key="index"
                      class="level-item has-text-centered"
                    >
                      <div>
                        <vs-switch
                          v-model="option.status"
                          square
                          val="css"
                          primary
                        >
                          {{ option.name }}
                        </vs-switch>
                      </div>
                    </div>
                  </div>
                  <div class="level">
                    <div class="level-item has-text-centered">
                      <div>
                        <vs-button
                          primary
                          style="min-width: 60px"
                          animation-type="scale"
                          @click="Selected"
                        >
                          <i class="bx bxs-copy"></i>
                          <template #animate>Copy</template>
                        </vs-button>
                      </div>
                    </div>
                    <div class="level-item has-text-centered">
                      <div>
                        <vs-button
                          icon
                          circle
                          primary
                          animation-type="rotate"
                          @click="refreshPassword = !refreshPassword"
                        >
                          <i class="bx bx-refresh"></i>
                          <template #animate>
                            <i class="bx bx-refresh"></i>
                          </template>
                        </vs-button>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
/* eslint-disable */
export default {
  data: () => ({
    refreshPassword: false,
    randomPassword: null,
    optiondata: [
      {
        name: 'ABC',
        status: true,
        chars: 'ABCDEFGHJKLMNOPQRSTUVWXYZ',
      },
      {
        name: 'abc',
        status: true,
        chars: 'abcdefghjkmnopqrstuvwxyz',
      },
      {
        name: '123',
        status: true,
        chars: '0123456789',
      },
      {
        name: '%&?',
        status: false,
        chars: '!$%&?+*#-/',
      },
    ],
  }),
  computed: {
    charset() {
      return [...this.optiondata]
        .map((element) => {
          if (element.status === true) return element.chars
        })
        .join('')
    },
    generatedPassword() {
      if (process.client) {
        this.refreshPassword
        const passwordLength = Math.floor(Math.random() * 1) + 24  
        return [
          ...window.crypto.getRandomValues(
            new Uint32Array(passwordLength)
          ),
        ]
          .map((value) => this.charset[value % this.charset.length])
          .join('')
      }
    },
  },
  watch: {
    generatedPassword(newValue) {
      this.randomPassword = newValue
    }
  },
  methods: {
    Selected() {
      this.$copyText(this.randomPassword).then(
        () => {
          this.$vs.notification({
            duration: '4000',
            progress: 'auto',
            icon: '<i class="bx bxs-copy"></i>',
            color: 'primary',
            position: 'top-center',
            title: 'Copied successfully.',
            text: `Keep your password in a safe place.`
          })
        },
        () => {
          this.$vs.notification({
            duration: '4000',
            progress: 'auto',
            icon: '<i class="bx bxs-error"></i>',
            color: 'danger',
            position: 'top-center',
            title: 'An error has occurred.',
            text: `Try to generate a new password.`
          })
        }
      )
    },
  },
}
</script>
