<script setup>
import { ref } from 'vue'

const formState = ref({
  topic: null,
  comments: null
})

function submitForm() {
  console.log(formState.value)
}
</script>

<template>
  <main class="cont">
    <h1 class="c" style="margin-bottom: 3rem; font-size: 1.7rem;">Анонимный опрос: Желаемая тема для личного проекта на открытом уроке</h1>

    <form @submit.prevent="submitForm">
      <div class="form-field">
        1. Какую программу ты хочешь использовать для своего проекта?
        <ul>
          <li>
            <label>
              <input v-model="formState.topic" value="Scratch" type="radio">
              Scratch
            </label>
          </li>
          <li>
            <label>
              <input v-model="formState.topic" value="Construct 2" type="radio">
              Construct 2
            </label>
          </li>
          <li>
            <label>
              <input v-model="formState.topic" value="Figma" type="radio">
              Figma
            </label>
          </li>
          <li>
            <label>
              <input v-model="formState.topic" value="HTML&CSS" type="radio">
              HTML&CSS
            </label>
          </li>
        </ul>
      </div>

      <div style="margin-bottom: 3rem;">
        2. Комментарий (необязательно):<br>
        <p class="any-comments" style="margin-top: .3rem; padding-left: 1.1rem; background-color: gray; color: white; font-style: italic;">
          У тебя есть какие-то мысли насчёт личного проекта? Можешь тут поделиться.<br>
          Может, хочется сделать несколько проектов? Опиши свои пожелания.
        </p>
        <textarea v-model="formState.comments" class="textarea"></textarea>
      </div>

      <button class="btn form-btn" type="submit">Отправить</button>
    </form>
  </main>
</template>
