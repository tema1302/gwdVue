<template>
  <div class="login__about__topics" id="login-about-topics">
		<div class="container">
			<LoginTopicItem
				v-for="(topic, index) in topics"
				:key="index"
				:title="topic.title"
				:description="topic.description"
				:listItems="topic.listItems"
				:imageSrc="topic.imageSrc"
				:imageAlt="topic.imageAlt"
				:imagePosition="topic.imagePosition"
			/>
		</div>
	</div>
</template>

<script setup>
import LoginTopicItem from './LoginTopicItem.vue';

const topics = [
  {
    title: 'Лента',
    description: 'С помощью этого раздела вы не пропустите ни одного важного события и действия в отношении дома.',
    listItems: [
      'Сообщения о запуске этапа, ходе работ и его приемке',
      'Фотоотчет со строительной площадки',
      'Комментарии ответственных лиц о производимых работах',
    ],
    imageSrc: '/src/assets/68f413ab426ea49a373121e376e34b24.png',
    imageAlt: 'Лента',
    imagePosition: 'right',
  },
  {
    title: 'Документы',
    description: 'В данном разделе собраны все документы.',
    listItems: [
      'Договоры',
      'Рекламации',
      'Оплаты по объекту с описанием стоимости, этапов, дат платежа, текущие и прошедшие согласования.',
    ],
    imageSrc: '/src/assets/8a4f7b8ef36f08ff0c29a83885cfa9c0.png',
    imageAlt: 'Документы',
    imagePosition: 'left',
  },
  {
    title: 'Галерея',
    description: 'Все фотоотчеты строительства отображаются не только в ленте, но и размещаются в данном разделе в хронологическом порядке от начала стройки до ее завершения.',
    listItems: [],
    imageSrc: '/src/assets/e2b46672baa209651034f25f38e01398.png',
    imageAlt: 'Галерея',
    imagePosition: 'right',
  },
  {
    title: 'Чат',
    description: 'Здесь вы можете задать любые вопросы. Менеджер проекта, инженеры, прорабы и другие участники процесса квалифицированно ответят вам.',
    listItems: [],
    imageSrc: '/src/assets/4b6a16e85a73d9a2db21127b6c2bb076.png',
    imageAlt: 'Чат',
    imagePosition: 'left',
  },
  {
    title: 'Гостевой доступ',
    description: 'Поделитесь с родными и близкими информацией о процессе строительства своего дома.',
    listItems: [],
    imageSrc: '/src/assets/f9bcfbfe75165e37fe1c8fea44f61de9.png',
    imageAlt: 'Гостевой доступ',
    imagePosition: 'right',
  },
  {
    title: 'Мобильная версия',
    description: 'Следите за процессом стройки в любой момент с удобного мобильного приложения.',
    listItems: [],
    imageSrc: '/src/assets/e6e713a1a85cd947afb87532eb861ca7.jpg',
    imageAlt: 'Мобильная версия',
    imagePosition: 'left',
  },
];
</script>
