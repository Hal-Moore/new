<template>
<div>
    <main class="content">
    <div class="page-title">
        <h4>
            <a href="#">Заказ</a>
            <i class="material-icons">keyboard_arrow_right</i>
            Добавить продукцию
        </h4>
        <button class="waves-effect btn grey darken-1 modal-trigger" data-target="explore-order">
            Завершить
        </button>
    </div>


    <table class="highlight">
        <thead>
        <tr>
            <th>Название</th>
            <th>Стоимость</th>
            <th>Количество</th>
            <th></th>
        </tr>
        </thead>

        <tbody>
        <tr>
            <td>Coffee</td>
            <td>200 руб.</td>
            <td>
                <div class="input-field inline order-position-input">
                    <input type="number" value="1" min="1">
                </div>
            </td>
            <td>
                <button class="btn waves-effect wavers-light btn-small">Добавить</button>
            </td>
        </tr>
        <tr>
            <td>Coffee</td>
            <td>200 руб.</td>
            <td>
                <div class="input-field inline order-position-input">
                    <input type="number" value="1" min="1">
                </div>
            </td>
            <td>
                <button class="btn waves-effect wavers-light btn-small">Добавить</button>
            </td>
        </tr>
        <tr>
            <td>Coffee</td>
            <td>200 руб.</td>
            <td>
                <div class="input-field inline order-position-input">
                    <input type="number" value="1" min="1">
                </div>
            </td>
            <td>
                <button class="btn waves-effect wavers-light btn-small">Добавить</button>
            </td>
        </tr>
        </tbody>
    </table>

</main>

<div id="explore-order" class="modal modal-fixed-footer">
    <div class="modal-content">
        <h4 class="mb1">Ваш заказ</h4>
        <table class="highlight">
            <thead>
            <tr>
                <th>Название</th>
                <th>Количество</th>
                <th>Цена</th>
                <th></th>
            </tr>
            </thead>

            <tbody>
            <tr>
                <td>Alvin</td>
                <td>3</td>
                <td>$0.87</td>
                <td><i class="material-icons pointer">delete</i></td>
            </tr>
            <tr>
                <td>Alan</td>
                <td>1</td>
                <td>$3.76</td>
                <td><i class="material-icons pointer">delete</i></td>

            </tr>
            <tr>
                <td>Jonathan</td>
                <td>2</td>
                <td>$7.00</td>
                <td><i class="material-icons pointer">delete</i></td>
            </tr>
            </tbody>
        </table>
        <div class="order-summary">
            <p>Общая стоимость <strong>22 231 руб.</strong></p>
        </div>
    </div>
    <div class="modal-footer">
        <a href="#!" class="modal-action waves-effect waves-black btn-flat">Отмена</a>
        <button class="modal-action btn waves-effect">Подтвердить</button>
    </div>
</div>


<!--Floating button-->
<div class="fixed-action-btn">
    <a class="btn-floating btn-large red">
        <i class="large material-icons">add</i>
    </a>
    <ul>
        <li><a class="btn-floating green"><i class="material-icons">assignment</i></a></li>
        <li><a class="btn-floating blue"><i class="material-icons">list</i></a></li>
    </ul>
</div>


</div>
</template>

<script>

export default {
    
}
</script>
