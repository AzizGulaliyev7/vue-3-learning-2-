<script setup>
import Modal from "@/components/Teams/Modal.vue";
import { useTeamStore } from "@/stores/TeamStore";
import {ref} from "vue";

let team = useTeamStore();
let showModal = ref(false);
</script>

<template>
  <button
      class="bg-green-500 hover:bg-green-600 text-white px-4 py-2 rounded disabled:bg-gray-400"
      :disabled="! team.spotsRemaining"
      @click="showModal = true"
  >
    Add Member ({{ team.spotsRemaining }} Spots Left)
  </button>

  <Teleport to="body">
    <Modal :show="showModal" @close="showModal = false">
      <template #default>
        <p>
          Need to add a new member to your team?
        </p>

        <form class="mt-6">
          <div class="flex gap-2">
            <input class="flex-1" type="email" placeholder="Email address...">

            <button>
              Add
            </button>
          </div>

        </form>
      </template>
    </Modal>
  </Teleport>
</template>

<style scoped>

</style>