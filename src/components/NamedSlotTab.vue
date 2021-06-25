<template>
  <div>
    <app-card>
      <template #header>
        <h2 class="text-xl font-semibold">Überschrift</h2>
      </template>
      <template #default>
        <p>
          Lorem ipsum, dolor sit amet consectetur adipisicing elit. Inventore,
          animi. Explicabo, cupiditate exercitationem officia blanditiis
          expedita recusandae nam aperiam eum. Voluptatem, repellendus ipsa
          porro quasi quisquam enim eos fuga cum.
        </p>
        <p>
          Fugit nulla doloremque recusandae iure at necessitatibus tempora
          quidem, quibusdam soluta, provident odit numquam enim repudiandae eos
          dolorem, esse tenetur. Corporis deleniti repudiandae dolorem
          voluptatem possimus eos quod enim atque.
        </p>
      </template>
      <template #footer>
        <div class="text-right">
          <app-button class="w-32">Ok</app-button>
        </div>
      </template>
    </app-card>
  </div>
</template>

<script>
import AppButton from '../lib/AppButton.vue';
import AppCard from '../lib/AppCard.vue';
export default {
  components: { AppCard, AppButton },
};
</script>
