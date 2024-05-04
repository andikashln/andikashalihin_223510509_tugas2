<template>
  <div>
    <!-- 1. Beberapa elemen HTML yang berbeda -->
    <h1 style="font-family: Georgia, 'Times New Roman', Times, serif;">Welcome!!</h1>

    <!-- 2. Elemen input teks -->
    <input v-model="inputText" placeholder="Masukkan teks di sini" />

    <!-- 3. Penggunaan class bindings dan style bindings -->
    <div :class="{ 'highlighted': isHighlighted }" :style="{ color: textColor }">
      <h2><ul>coba masukkan teks apapun </ul></h2>
    </div>

    <!-- 4. Interaksi dinamis dengan event listener -->
    <button @click="changeText">Ubah Teks</button>
    <p>{{ dynamicText }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      inputText: '',
      isHighlighted: false,
      textColor: 'blue',
      dynamicText: 'Teks ini akan berubah!',
    };
  },
  methods: {
    changeText() {
      this.dynamicText = 'Teks telah diubah!';
      this.isHighlighted = !this.isHighlighted;
    },
  },
};
</script>

<style scoped>
.highlighted {
  background-color: plum;
}
h1 {
  margin-bottom: 10%;
}

</style>