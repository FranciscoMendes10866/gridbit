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
                    FwPY29RzAsGUo01B
                  </h5>
                  <div class="level">
                    <div class="level-item has-text-centered">
                      <div>
                        <vs-switch square val="css" danger>ABC</vs-switch>
                      </div>
                    </div>
                    <div class="level-item has-text-centered">
                      <div>
                        <vs-switch square val="css" danger>abc</vs-switch>
                      </div>
                    </div>
                    <div class="level-item has-text-centered">
                      <div>
                        <vs-switch square val="css" danger>123</vs-switch>
                      </div>
                    </div>
                    <div class="level-item has-text-centered">
                      <div>
                        <vs-switch square val="css" danger>#$&</vs-switch>
                      </div>
                    </div>
                  </div>
                  <div class="level">
                    <div class="level-item has-text-centered">
                      <div>
                        <vs-button
                          danger
                          style="min-width: 60px"
                          animation-type="scale"
                        >
                          <i class="bx bxs-copy"></i>
                          <template #animate>Copy</template>
                        </vs-button>
                      </div>
                    </div>
                    <div class="level-item has-text-centered">
                      <div>
                        <vs-button icon circle danger animation-type="rotate">
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
export default {}
</script>
