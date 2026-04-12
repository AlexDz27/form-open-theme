<script setup></script>

<template>
  <main class="cont">
    <h1 class="c" style="margin-bottom: 3rem; font-size: 1.7rem;">Анонимный опрос: Желаемая тема для личного проекта на открытом уроке</h1>

    <form @submit.prevent>
      <div class="form-field">
        1. Какую программу ты хочешь использовать для своего проекта?
        <ul>
          <li>
            <label>
              <input name="topic" value="Scratch" type="radio">
              Scratch
            </label>
          </li>
          <li>
            <label>
              <input name="topic" value="Construct 2" type="radio">
              Construct 2
            </label>
          </li>
          <li>
            <label>
              <input name="topic" value="Figma" type="radio">
              Figma
            </label>
          </li>
          <li>
            <label>
              <input name="topic" value="HTML&CSS" type="radio">
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
        <textarea name="comments" class="textarea"></textarea>
      </div>

      <button class="btn form-btn" type="submit">Отправить</button>
    </form>
  </main>
</template>
