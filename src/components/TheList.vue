<script lang="ts">
let id = 0;

export default {
  data() {
    return {
      newName: "",
      isHidden: true,
      names: [{ id: id++, text: "Bob" }],
    };
  },
  methods: {
    addNewName() {
      this.names.push({ id: id++, text: this.newName });
      this.newName = "";
    },
    removeTodo(name: { id: number; text: string }) {
      this.names = this.names.filter((n) => n !== name);
    },
    shuffleNames() {
      this.names.sort(() => Math.random() - 0.5);
      this.isHidden = false;
    },
  },
};
</script>

<template>
  <div class="m-12">
    <form @submit.prevent="addNewName" class="flex justify-center w-full">
      <input
        v-model="newName"
        placeholder="Enter a name"
        class="px-4 py-2 m-2 bg-white border rounded-md shadow-sm border-slate-300 placeholder-slate-400 focus:outline-none focus:border-[#428082] focus:ring-1 focus:ring-[#428082] disabled:bg-slate-50 disabled:text-slate-500 disabled:border-slate-200 disabled:shadow-none invalid:border-pink-500 invalid:text-pink-600 focus:invalid:border-pink-500 focus:invalid:ring-pink-500"
      />
      <button
        class="px-4 py-2 m-2 rounded-3xl text-white bg-[#428082] hover:opacity-90"
      >
        Add name
      </button>
    </form>
    <p class="font-bold text-center text-[#428082] text-7xl my-12">
      {{ isHidden ? "" : `${names[1].text} makes the tea this time!` }}
    </p>
    <ul
      class="flex flex-wrap h-fit justify-center max-w-5xl gap-6 px-12 overflow-y-scroll py-24 m-auto outline-dashed rounded-md outline-[#ccc]"
    >
      <li
        v-for="name in names"
        :key="name.id"
        class="flex flex-col items-center justify-between px-4 py-2 bg-white rounded-md shadow-lg w-fit outline outline-1 outline-gray-100"
      >
        {{ name.text }}
        <button
          @click="removeTodo(name)"
          class="px-4 py-1 m-2 text-white rounded-3xl bg-[#428082] hover:opacity-90"
        >
          delete
        </button>
      </li>
    </ul>
    <div class="pt-6 text-center">
      <button
        @click="shuffleNames()"
        class="px-4 py-2 m-2 text-white rounded-3xl bg-[#428082] hover:opacity-90"
      >
        Pick randomly
      </button>
    </div>
  </div>
</template>
