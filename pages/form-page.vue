<template>
  <div class="form-container">
    <main class="form-container__content">
      <h2 class="form-container__title">Send your data</h2>
      <form class="form-container__form" @submit.prevent="submitForm">
        <div class="form-container__field">
          <input
            class="form-container__input"
            type="text"
            placeholder="First Name"
            v-model="formData.name"
            required
          />
        </div>
        <div class="form-container__field">
          <input
            class="form-container__input"
            type="text"
            placeholder="Second Name"
            v-model="formData.second"
            required
          />
        </div>
        <div class="form-container__field">
          <input
            class="form-container__input"
            type="email"
            placeholder="Email"
            v-model="formData.email"
            required
          />
        </div>
        <div class="form-container__field">
          <input
            class="form-container__input"
            type="text"
            placeholder="Address"
            v-model="formData.address"
            required
          />
        </div>
        <button
          class="form-container__button"
          type="submit"
          :disabled="isLoading"
        >
          {{ isLoading ? 'Sending...' : 'Submit' }}
        </button>
        <p v-if="errorMessage" class="form-container__error">
          {{ errorMessage }}
        </p>
      </form>
    </main>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const formData = ref({
  name: '',
  second: '',
  email: '',
  address: '',
})

const isLoading = ref(false)
const errorMessage = ref(null)

const submitForm = async () => {
  errorMessage.value = null
  isLoading.value = true

  try {
    await new Promise((resolve) => setTimeout(resolve, 2000))

    console.log('Дані форми:', JSON.stringify(formData.value, null, 2))

    formData.value = {
      name: '',
      second: '',
      email: '',
      address: '',
    }
  } catch (error) {
    errorMessage.value = 'Сталася помилка при відправці даних!'
  } finally {
    isLoading.value = false
  }
}
</script>

<style scoped>
.form-container {
  display: flex;
  justify-content: center;
  align-items: center;
  padding-block: 100px;
  padding-inline: 340px;
  background-color: #f0f0f0;
}

.form-container__content {
  padding: 20px;
  max-width: 1240px;
  height: 560px;
  width: 100%;
  background-color: white;
  background-image: url('../assets/Subtract (1).svg');
  background-size: cover;
  background-position: center;
  border-radius: 8px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

.form-container__title {
  font-size: 50px;
  font-weight: 700;
  line-height: 60.95px;
  text-align: center;
  color: rgba(255, 255, 255, 1);
}

.form-container__form {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.form-container__field {
  margin-bottom: 15px;
}

.form-container__input {
  width: 392px;
  height: 58px;
  font-size: 20px;
  padding-left: 30px; 
  border: 1px solid rgba(200, 194, 198, 1);
  border-radius: 38px;
  outline: none;
}

.form-container__input:focus::placeholder {
  color: transparent;
}

.form-container__input::placeholder {
  font-size: 18px;
  font-weight: 400;
  line-height: 28px;
  text-align: left;
  color: rgba(136, 136, 136, 1);

  padding: 15px 0 15px 0;
}

.form-container__button {
  padding: 10px 20px;
  width: 392px;
  height: 58px;
  background: rgba(103, 80, 164, 1);
  color: white;
  border: none;
  color: rgba(255, 255, 255, 1);
  font-size: 18px;
  font-weight: 500;
  line-height: 28px;
  text-align: center;
  transition:
    background-color 0.3s ease,
    transform 0.3s ease;

  border-radius: 38px;
  cursor: pointer;
}

.form-container__button:disabled {
  background-color: blue;
  cursor: not-allowed;
}

.form-container__button:hover {
  background-color: #0056b3;
  transform: scale(1.05);
  box-shadow: 0 8px 15px rgba(0, 0, 0, 0.2);
  cursor: pointer;
}

.form-container__error {
  color: red;
  margin-top: 10px;
  text-align: center;
}
</style>
