<template>
  <v-container
    fluid
  >
    <v-card class="pa-3">
      <v-row no-gutters>
        <!-- col 은 row 하위에 위치 -->
        <!-- cols=auto: text 사이즈만큼 자동으로 크기 설정 -->
        <v-col cols="auto">
          <v-card
            class="pa-3"
            outlined
          >
            Col1
          </v-card>
        </v-col>
        <v-col>
          <v-card
            class="pa-3"
            outlined
          >
            Col2
          </v-card>
        </v-col>
        <!-- spacer: 여백 -->
        <v-spacer />
        <v-col>
          <v-card
            class="pa-3"
            outlined
          >
            Col3
          </v-card>
        </v-col>
      </v-row>
    </v-card>
    <v-card class="pa-3">
      <v-row
        :style="{ height: '120px'}"
        class="red"
        align="start"
      >
        <!-- col 은 row 하위에 위치 -->
        <v-col>
          <v-card
            class="pa-3"
            outlined
          >
            Col1
          </v-card>
        </v-col>
        <v-col>
          <v-card
            class="pa-3"
            outlined
          >
            Col2
          </v-card>
        </v-col>
        <v-col>
          <v-card
            class="pa-3"
            outlined
          >
            Col3
          </v-card>
        </v-col>
      </v-row>
    </v-card>
    <v-card class="pa-3">
      <v-row
        :style="{ height: '120px'}"
        class="yellow"
        align="start"
      >
        <!-- col 은 row 하위에 위치 -->
        <v-col
          align-self="end"
        >
          <v-card
            class="pa-3"
            outlined
          >
            Col1
          </v-card>
        </v-col>
        <v-col
          align-self="center"
        >
          <v-card
            class="pa-3"
            outlined
          >
            Col2
          </v-card>
        </v-col>
        <v-col>
          <v-card
            class="pa-3"
            outlined
          >
            Col3
          </v-card>
        </v-col>
      </v-row>
    </v-card>
    <v-card class="mt-5 pa-3">
      <v-row
        justify="space-between"
      >
        <!-- col 은 row 하위에 위치 -->
        <v-col
          cols="auto"
        >
          <v-card
            class="pa-3"
            outlined
          >
            Col1
          </v-card>
        </v-col>
        <v-col
          cols="auto"
        >
          <v-card
            class="pa-3"
            outlined
          >
            Col2
          </v-card>
        </v-col>
        <v-col
          cols="auto"
        >
          <v-card
            class="pa-3"
            outlined
          >
            Col3
          </v-card>
        </v-col>
      </v-row>
    </v-card>
  </v-container>
</template>

<script>
export default {
  name: "GridSystem"
}
</script>

<style scoped>

</style>
