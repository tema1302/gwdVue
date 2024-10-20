<template>
  <div class="login__block">
    <div class="row login__title">
      <div class="container">
        <div class="row">
          <div class="col-12 col-md-6">
            <h1>Личный кабинет GOOD&nbsp;WOOD</h1>
            <p class="login__title-info">Здесь хранится вся информация:</p>
            <ul class="login__title-list">
              <li>о проектировании,</li>
              <li>покупке,</li>
              <li>строительстве,</li>
              <li>эксплуатации дома,</li>
              <li>а также размещаются новости и мероприятия компании</li>
            </ul>
          </div>
          <div class="col-12 col-md-6">
            <div id="login-app">
              <form method="POST" action="https://lk.gwd.ru/index.php?login=yes" class="login__form">
                <h3 class="login__form__header">Вход в личный кабинет</h3>
                <input type="hidden" name="AUTH_FORM" value="Y">
                <input type="hidden" name="TYPE" value="AUTH">
                <input type="hidden" name="backurl" value="/index.php">
                <div class="form-group">
                  <input type="text" placeholder="Логин" name="USER_LOGIN" class="form-control" />
                </div>
                <div class="form-group mb-4">
                  <input type="password" placeholder="Пароль" name="USER_PASSWORD" class="form-control" />
                </div>
                <a href="https://lk.gwd.ru/" class="login__form__forgot">Забыли пароль?</a>
                <label for="USER_REMEMBER" class="checkbox d-block">
                  <input id="USER_REMEMBER" type="checkbox" name="USER_REMEMBER" class="checkbox__input" value="Y" />
                  <span class="checkbox__box">
										<FontAwesomeIcon :icon="faCheck" />
									</span> Запомнить меня
                </label>
                <button type="submit" class="btn btn-orange btn-block login__form__submit">Войти</button>
              </form>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
</script>
