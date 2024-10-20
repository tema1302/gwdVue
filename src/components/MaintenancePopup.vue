<template>
<div id="maintenance-popup" class="maintenance-popup" style="display: none;">
    <h3 class="maintenance-popup__header">Пришло время для технического обслуживания вашего дома!</h3>
    <div class="maintenance-popup__buttons">
        <button type="button" class="btn btn-green" id="maintenance-alert-request">Заказать ТО</button>
        <button type="button" class="btn btn-white" id="maintenance-alert-call">Позвонить в GOOD WOOD</button>
    </div>

    <div class="maintenance-popup__call-dialog" id="maintenance-popup__call-dialog">
        <h3 class="maintenance-popup__header">Позвонить вашему менеджеру?</h3>
        <div class="maintenance-popup__buttons">
            <button type="button" class="btn btn-white" id="maintenance-alert-call-yes">ОК</button>
            <button type="button" class="btn btn-red" id="maintenance-alert-call-cancel">Отмена</button>
        </div>
    </div>

    <div class="maintenance-popup__call-dialog" id="maintenance-alert-call-success">
        <h3>Спасибо, ожидайте звонка на свой телефон</h3>
    </div>
    <div class="maintenance-popup__call-dialog" id="maintenance-alert-call-fail">
        <h3>Извините, похоже что-то пошло не так</h3>
    </div>
</div>
</template>

<script>
export default {
    name: 'MaintenancePopup',
};
</script>
