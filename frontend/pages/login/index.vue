<template>
  <v-container>
    <v-row align="center" justify="center">
      <v-col cols="12">
        <v-card class="elevation-6 mt-10">
          <v-window v-model="step">
            <v-window-item :value="1">
              <v-row>
                <v-col cols="6">
                  <v-card-text class="mt-12">
                    <h2 class="text-center">Login</h2>
                    <v-row align="center" justify="center">
                      <v-col cols="8">
                        <v-text-field
                          label="Email"
                          outlined
                          dense
                          color="blue"
                          autocomplete="false"
                          class="mt-12"
                        />
                        <v-text-field
                          label="Senha"
                          outlined
                          dense
                          color="blue"
                          autocomplete="false"
                          type="password"
                        />
                        <v-row>
                          <v-col cols="5">
                            <span class="caption blue--text"
                              >Esqueceu sua senha?</span
                            >
                          </v-col>
                        </v-row>
                        <v-btn color="blue" dark block tile to="/home">Log in</v-btn>
                      </v-col>
                    </v-row>
                  </v-card-text>
                </v-col>
                <v-col cols="6" class="blue">
                  <div style="text-align: center; padding: 180px 0">
                    <v-card-text class="white--text">
                      <h3 class="text-center">Ainda não possui uma conta?</h3>
                      <h6 class="text-center">
                        Vamos preparar tudo para você começar a ler!
                      </h6>
                    </v-card-text>
                    <div class="text-center">
                      <v-btn tile outlined dark @click="step++">Cadastre-se</v-btn>
                    </div>
                  </div>
                </v-col>
              </v-row>
            </v-window-item>
            <v-window-item :value="2">
              <v-row>
                <v-col cols="6" class="blue">
                  <div style="text-align: center; padding: 180px 0">
                    <v-card-text class="white--text">
                      <h3 class="text-center">Já possui uma conta?</h3>
                      <h6 class="text-center">
                        Entre em sua conta para continuar a organizar sua biblioteca!
                      </h6>
                    </v-card-text>
                    <div class="text-center">
                      <v-btn tile outlined dark @click="step--">Log in</v-btn>
                    </div>
                  </div>
                </v-col>

                <v-col cols="6">
                  <v-card-text class="mt-6">
                    <h2 class="text-center">Crie uma conta</h2>
                    <v-row align="center" justify="center">
                      <v-col cols="8">
                        <v-row>
                          <v-col cols="12">
                            <v-text-field
                              label="Nome Completo"
                              outlined
                              dense
                              color="blue"
                              autocomplete="false"
                              class="mt-4"
                            />
                          </v-col>
                        </v-row>
                        <v-text-field
                          label="Email"
                          outlined
                          dense
                          color="blue"
                          autocomplete="false"
                        />
                        <v-text-field
                          label="Data de Nascimento"
                          outlined
                          dense
                          color="blue"
                          autocomplete="false"
                          type="date"
                        />
                        <v-text-field
                          label="Senha"
                          outlined
                          dense
                          color="blue"
                          autocomplete="false"
                          type="password"
                        />
                        <v-row>
                            <v-radio-group
                                v-model="row"
                                row
                            >
                                <v-col cols="4">
                                    <v-radio
                                        label="Masculino"
                                        value="m"
                                    ></v-radio>
                                </v-col>
                                <v-col cols="4">
                                    <v-radio
                                        label="Feminino"
                                        value="f"
                                    ></v-radio>
                                </v-col>
                                <v-col cols="4">
                                    <v-radio
                                        label="Outro"
                                        value="x"
                                    ></v-radio>
                                </v-col>
                            </v-radio-group>
                        </v-row>
                        <v-btn color="blue" dark block tile>Cadastre-se</v-btn>
                      </v-col>
                    </v-row>
                  </v-card-text>
                </v-col>
              </v-row>
            </v-window-item>
          </v-window>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>
  
  <script>
export default {
  data: () => ({
    step: 1,
  }),
  props: {
    source: String,
  },
};
</script>