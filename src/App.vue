<script>
import './style.css'
import axios from "axios"

export default {
  data(){
    return{
      username: '',
      usernumber: '+998',
    }
  },
  methods: {
    send() {
      let fullmessage = `Имя клиента: ${this.username} \n
      
      Телефон номер: ${this.usernumber}`;
      // console.log(this.$http);
      // let a = `https://api.telegram.org/bot${this.token}:AAEti3PIansCHmv1kPY_HSki4Q8wq2PJa5c/sendMessage?chat_id=${this.chatId}&text=${fullmessage}`;

      let api = `https://api.telegram.org/bot6779827682:AAHn49qs8hwRRxlr9fdfmdepNFIlIwN8Ix8/sendMessage?chat_id=-4133301982&text=${fullmessage}`


      axios.get(api).then(
        (response) => {
          console.log("Succsessfully!", response.data);
          this.response = true
          this.username = ''
          this.usernumber = ''
        },
        (error) => {
          console.log(error);
        }
      );
    }
  }
}



</script>

<template>
  <div>

    <header class="h-[90px] z-[30] fixed w-[100%] left-0 top-0 flex bg-[#121011]">
      <div class="flex cont  w-[100%] mx-auto justify-between items-center">
        <img class="h-[80%] logo" src="./assets/sigma.svg" alt="">
        <div class="flex gap-[50px] nav">
          <a class="text-white font-[Gilroy] font-[400] text-[25px]" href="#whowe">Кто мы ?</a>
          <a class="text-white font-[Gilroy] font-[400] text-[25px]" href="#advantages"> Преимущества</a>
          <a class="text-white font-[Gilroy] font-[400] text-[25px]" href="#contact">Контакты</a>
        </div>
        <div class="btn-wrp flex gap-[35px]">
          <a href="#contact"> <button
              class="header-btn-call font-[Gilroy] text-white font-[600] text-[22px] px-[40px] py-[10px]">Позвонить</button></a>
          <a href="#sign"><button
              class="header-btn-sign font-[Gilroy] text-white font-[600] text-[22px] px-[40px] py-[10px]">Записаться</button></a>
        </div>
      </div>
    </header>

    <main>

      <section class="h-[100vh] font-[Gilroy] relative one-screen">
        <div class="one-screen-decor"></div>
        <div class="cont cont-wrp-one h-[100%] one-screen-cont mx-auto flex items-center">
          <div class="w-[50%] one-screen-left">
            <span class="flex one-screen-title text-[25px] items-center font-[600] text-[#AF1416]">
              <div class="h-[17px] mr-[10px] w-[17px] bg-[#AF1416] rounded-[50%]"></div> Поднимай железо с SigmaGym
            </span>
            <h1 class="text-[54px] my-[10px] font-[1000] leading-[50px] text-white">Вступай в SigmaGym: стань лучшей
              версией себя</h1>
            <p class="text-[25px] mt-[20px] one-screen-paragraf text-white max-w-[550px] leading-[30px]">Здесь нет места
              для слабаков. SigmaGym — это место, где ты сможешь добиться своих целей, перейдя через себя.</p>
            <div class="mt-[38px] flex nums-block gap-[60px]">
              <div class="w-[300px] nums h-[100%]">
                <span class="text-[52px] text-white  font-[500]">150+</span>
                <p class="text-[22px] mb-[25px] text-white font-[400]">единиц <br class="nonenone"> оборудования,
                  жесткие тренировки.</p>
                <a href="#sign">
                  <button
                    class="header-btn-sign w-[100%] h-[70px] font-[Gilroy] text-white font-[600] text-[30px] px-[40px] py-[10px]">
                    Записаться
                  </button>
                </a>
              </div>
              <div class="w-[300px] nums h-[100%]">
                <span class="text-[52px] text-white  font-[500]">30+ </span>
                <p class="text-[22px] mb-[25px] text-white font-[400]">видов групповых занятий, безжалостная тренировка.
                </p>
                <a href="#contact"><button
                    class="header-btn-call w-[100%] h-[70px] font-[Gilroy] text-white font-[600] text-[30px] px-[40px] py-[10px]">
                    Позвонить
                  </button></a>
              </div>
            </div>
          </div>

          <div class="w-[50%] one-screen-right z-[21] h-[100%]">
            <img class="one-screen-right-img" src="./assets/one-screen-image1.png" alt="img">
            <div class="flex flex-col one-screen-right-texts">
              <span>SIGMAGYM</span>
              <span>SIGMAGYM</span>
              <span>SIGMAGYM</span>
              <span>SIGMAGYM</span>
            </div>
            <div class="h-[180px] sitata w-[550px] p-[33px] pt-[40px] one-screen-right-block">
              <div
                class="bg-[red] quotes p-[15px] h-[50px] top-[0%] translate-y-[-50%] shadow-sm absolute rounded-[100%]">
                <img class="h-[17px]" src="./assets/quotes.png" alt="">
              </div>
              <span class="text-white font-[Gilroy] text-[22px]">“Большая сила приходит из больших мучений.”</span>
              <p class="text-white font-[Gilroy] text-[32px] font-[1000]">Уильям Шекспир</p>
            </div>
          </div>
        </div>
      </section>

      <section class="second_section">
        <div class="second_section_block">
          <div class="second_section_block_top">
            <div class="second_section_block_top_svg">
              <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="0"
                stroke="currentColor" class="w-6 h-6">
                <path stroke-linecap="round" stroke-linejoin="round"
                  d="M15 19.128a9.38 9.38 0 0 0 2.625.372 9.337 9.337 0 0 0 4.121-.952 4.125 4.125 0 0 0-7.533-2.493M15 19.128v-.003c0-1.113-.285-2.16-.786-3.07M15 19.128v.106A12.318 12.318 0 0 1 8.624 21c-2.331 0-4.512-.645-6.374-1.766l-.001-.109a6.375 6.375 0 0 1 11.964-3.07M12 6.375a3.375 3.375 0 1 1-6.75 0 3.375 3.375 0 0 1 6.75 0Zm8.25 2.25a2.625 2.625 0 1 1-5.25 0 2.625 2.625 0 0 1 5.25 0Z" />
              </svg>

            </div>
            <div>
              <span>Занятия</span>
              <p> Наши групповые </p>
            </div>
          </div>
          <p class="second_section_block_p"> — это не просто тренировки, это настоящий вызов для твоего тела и духа.
          </p>
        </div>
        <div class="second_section_block">
          <div class="second_section_block_top">
            <div class="second_section_block_top_svg">
              <svg width="71" height="71" viewBox="0 0 71 71" fill="none" xmlns="http://www.w3.org/2000/svg"
                xmlns:xlink="http://www.w3.org/1999/xlink">
                <mask id="mask0_5_2158" style="mask-type:alpha" maskUnits="userSpaceOnUse" x="0" y="0" width="71"
                  height="71">
                  <rect width="71" height="71" fill="url(#pattern0_5_2158)" />
                </mask>
                <g mask="url(#mask0_5_2158)">
                  <rect x="-0.970703" y="2.08008" width="85.8379" height="71.1387" fill="white" />
                </g>
                <defs>
                  <pattern id="pattern0_5_2158" patternContentUnits="objectBoundingBox" width="1" height="1">
                    <use xlink:href="#image0_5_2158" transform="scale(0.00195312)" />
                  </pattern>
                  <image id="image0_5_2158" width="512" height="512"
                    xlink:href="data:image/png;base64,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" />
                </defs>
              </svg>

            </div>
            <div>
              <span>Тренеры</span>
              <p>профессиональные </p>
            </div>
          </div>
          <p class="second_section_block_p">Наши тренеры — это настоящие гуру фитнеса.</p>
        </div>
        <div class="second_section_block">
          <div class="second_section_block_top">
            <div class="second_section_block_top_svg">
              <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="0"
                stroke="currentColor" class="w-6 h-6">
                <path stroke-linecap="round" stroke-linejoin="round"
                  d="M21 8.25c0-2.485-2.099-4.5-4.688-4.5-1.935 0-3.597 1.126-4.312 2.733-.715-1.607-2.377-2.733-4.313-2.733C5.1 3.75 3 5.765 3 8.25c0 7.22 9 12 9 12s9-4.78 9-12Z" />
              </svg>
            </div>
            <div>
              <span>Здоровье </span>
              <p> это наш приоритет</p>
            </div>
          </div>
          <p class="second_section_block_p">Здоровье и благополучие наших клиентов.</p>
        </div>

      </section>

      <section class="three_screen">
        <div class="three_screen__left">
          <div class="three_screen__left_docor"></div>
          <img src="./assets/image3.png" alt="image">
          <div class="three_screen__left_moreimage">
            <img src="./assets/image5.png" alt="image">
            <img src="./assets/image2.png" alt="image">
            <img src="./assets/image4.png" alt="image">
          </div>
        </div>
        <div class="three_screen__right">
          <span>SIGMAGYM</span>
          <img src="./assets/arrows.png" alt="arrows">
          <p>
            Стань несокрушимым титаном своей судьбы. Подними железо с SigmaGym!
          </p>
        </div>
      </section>

      <section id="whowe" class="four_screen">
        <h2>SigmaGym <br> это не просто <br> "клуб"</h2>
        <p>— А место где культивируется стальной характер и брутальная сила. Здесь растут настоящие лидеры, готовые к
          смелым действиям и невероятным достижениям. Мы вдохновляем наших участников становиться лучшей версией себя
          каждый день, преодолевая любые препятствия на пути к своим целям.</p>

        <div class="four_screen_wrapper">
          <button class="four_screen_wrapper_open" onclick="my_modal_3.showModal()">Когда увижу результат ?</button>
          <dialog id="my_modal_3" class="modal">
            <span class="sigmagymdecor">SIGMAGYM</span>
            <span class="sigmagymdecor">SIGMAGYM</span>
            <span class="sigmagymdecor">SIGMAGYM</span>
            <span class="sigmagymdecor">SIGMAGYM</span>
            <span class="sigmagymdecor">SIGMAGYM</span>
            <span class="sigmagymdecor">SIGMAGYM</span>
            <div class="modal-box">
              <h3 class="font-bold text-lg">Через 2-3 месяца увижу результат?</h3>
              <p class="py-4">Да, если будешь работать крепко каждый день. Сжигай лень и отвлечения в огне своей
                страсти. Результаты не приходят к тем, кто ждет, они подчиняются тем, кто действует с безудержным
                голодом к победе. Тут нет места для слабаков или сомневающихся. Только упорство, дисциплина и
                бескомпромиссное стремление к превосходству приведут тебя к заветной цели. В SigmaGym мы создаем не
                просто тела, мы лепим из железа настоящих титанов. Поэтому, бери железо и двигайся вперед – результаты
                не заставят себя долго ждать!</p>
              <div class="modal-action">
                <form method="dialog">
                  <!-- if there is a button in form, it will close the modal -->
                  <button onclick="my_modal_69.showModal()"
                    class="btn mr-[10px]  bg-red-800 text-white border-[1]">Записаться</button>
                  <button class="btn">Закрыть</button>
                </form>
              </div>
            </div>
          </dialog>

          <button class="four_screen_wrapper_open" onclick="my_modal_1.showModal()">Совет новичку</button>
          <dialog id="my_modal_1" class="modal">
            <span class="sigmagymdecor">SIGMAGYM</span>
            <span class="sigmagymdecor">SIGMAGYM</span>
            <span class="sigmagymdecor">SIGMAGYM</span>
            <span class="sigmagymdecor">SIGMAGYM</span>
            <span class="sigmagymdecor">SIGMAGYM</span>
            <span class="sigmagymdecor">SIGMAGYM</span>
            <div class="modal-box">
              <h3 class="font-bold text-lg">Совет новичку</h3>
              <p class="py-4">Самый важный шаг уже сделан — ты решил начать свой путь к здоровью и силе. В SigmaGym мы
                готовы поддержать тебя на этом пути. Не бойся трудностей, каждый стартует с нуля. Слушай свое тело, учи
                его язык, иди на встречу силе и энергии. Наши тренеры и программа поддержки помогут тебе разбудить в
                себе настоящего воина. Помни, что каждая тренировка — это шаг к новой версии тебя. Давай начнем!</p>
              <div class="modal-action">
                <form method="dialog">
                  <!-- if there is a button in form, it will close the modal -->
                  <button onclick="my_modal_69.showModal()"
                    class="btn mr-[10px]  bg-red-800 text-white border-[1]">Записаться</button>
                  <button class="btn">Закрыть</button>
                </form>
              </div>
            </div>
          </dialog>

          <button class="four_screen_wrapper_open" onclick="my_modal_2.showModal()">Почему именно мы?</button>
          <dialog id="my_modal_2" class="modal">
            <span class="sigmagymdecor">SIGMAGYM</span>
            <span class="sigmagymdecor">SIGMAGYM</span>
            <span class="sigmagymdecor">SIGMAGYM</span>
            <span class="sigmagymdecor">SIGMAGYM</span>
            <span class="sigmagymdecor">SIGMAGYM</span>
            <span class="sigmagymdecor">SIGMAGYM</span>
            <div class="modal-box">
              <h3 class="font-bold text-lg">Почему именно мы?</h3>
              <p class="py-4">Потому что SigmaGym — это не просто фитнес-клуб, это арена для железных душ, где рождаются
                настоящие легенды. У нас ты найдешь не только современное оборудование и профессиональных тренеров, но и
                атмосферу силы, страсти и целеустремленности. Мы не боимся вызовов, мы их принимаем и преодолеваем.
                Здесь ты станешь частью команды победителей, готовых сокрушать границы и достигать невероятных высот.
                Присоединяйся к SigmaGym и покажи миру, что ты настоящий титан!"</p>
              <div class="modal-action">
                <form method="dialog">
                  <!-- if there is a button in form, it will close the modal -->
                  <button onclick="my_modal_69.showModal()"
                    class="btn mr-[10px]  bg-red-800 text-white border-[1]">Записаться</button>
                  <button class="btn">Закрыть</button>
                </form>
              </div>
            </div>
          </dialog>


        </div>


      </section>


      <section id="advantages" class="five_screen">
        <div class="five_screen_item">
          <h3>
            СИЛА.<br>
            МОЩЬ. <br>
            ПОБЕДА.
          </h3>
        </div>
        <div class="five_screen_item five_screen_item2">
          <div>
            <h4>Индивид программы.</h4>
            <p>В SigmaGym мы создаем персонализированные программы тренировок, учитывая твои цели, физическую подготовку
              и предпочтения. Каждая тренировка - это шаг к достижению твоих максимальных результатов.</p>
          </div>
          <div>
            <h4>Экспертные тренеры.</h4>
            <p>Наши тренеры - высококвалифицированные специалисты, готовые вложить свой опыт и знания, чтобы помочь тебе
              преодолеть любые трудности и достичь фитнес-целей, которые ты задал себе.</p>
          </div>
          <div>
            <h4>Уютная обстановка.</h4>
            <p>В SigmaGym мы создаем уютную и дружественную атмосферу, где каждый чувствует себя комфортно и
              вдохновленно. У нас нет места для стресса, только место для твоего развития и успеха в тренировках.</p>
          </div>
        </div>
      </section>

      <section id="sign" class="six_screen">
        <div class="six_screen_item">
          <h3 class="uppercase">Запишись на тренировку уже сегодня!</h3>
          <p>Не жди завтрашнего дня, чтобы начать свой путь к лучшей версии себя. Присоединяйся к SigmaGym прямо сейчас
            и начни свой путь к фитнесу, силе и здоровью.</p>
          <button onclick="my_modal_69.showModal()">ЗАПИСАТЬСЯ</button>

        </div>
        <dialog id="my_modal_69" class="modal bg-[black]">
          <span class="sigmagymdecor">SIGMAGYM</span>
          <span class="sigmagymdecor">SIGMAGYM</span>
          <span class="sigmagymdecor">SIGMAGYM</span>
          <span class="sigmagymdecor">SIGMAGYM</span>
          <span class="sigmagymdecor">SIGMAGYM</span>
          <span class="sigmagymdecor">SIGMAGYM</span>
          <div class="modal-box">
            <h3 class="font-bold text-lg">Наша арена ждет твоего громкого рева! Прокачай свою силу и доминирование в
              SigmaGym!</h3>
            <div>
              <div class="mt-2">
                <input id="name" v-model="username" name="name" type="text" placeholder="Имя" autocomplete="current-password" required
                  class="block pl-[15px] mt-[15px] font-[Gilroy] font-[800] w-full rounded-md border-0 py-1.5 text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-indigo-600 sm:text-sm sm:leading-6">
              </div>
              <div class="mt-2">
                <input v-model="usernumber" type="text" placeholder="Номер Телефона" autocomplete="current-password"
                  required
                  class="block pl-[15px] mt-[15px] font-[Gilroy] font-[800] w-full rounded-md border-0 py-1.5 text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-indigo-600 sm:text-sm sm:leading-6">
              </div>
            </div>
            <div class="modal-action">
              <form method="dialog">
                <!-- if there is a button in form, it will close the modal -->
                <button @click="send()" class="btn mr-[10px]  bg-red-800 text-white border-[1]">Записаться</button>
                <button class="btn">Закрыть</button>
              </form>
            </div>
          </div>
        </dialog>
      </section>



      <footer id="contact">
        <h3>ДЕРЖИ НАШИ <br> КОНТАКТЫ.</h3>
        <img src="./assets/footerarrow.png" alt="image">
        <p class="w-[max-content]px-[15px] ledled leading-[33px] py-[5px]">
          <span class="text-white block nije">Филиал №1 :</span> <br> <span class="text-black bg-white">Юнусабад 6кв (конечка автобусов)</span>
        </p>
        <p class="w-[max-content]px-[15px] ledled leading-[33px] py-[5px]">
          <span class="text-white block nije"> Филиал №2 :</span> <br> <span class="text-black bg-white"> Кибрай, улица Гулистон 8-открытая дом 1А</span>
        </p>
        <a href="tel:+998974626323">☎️ 97 462 63 23</a> <br> <br>
        <a href="tel:+9989770023525">☎️ 77 002 35 25</a>
      </footer>

    </main>
  </div>
</template>

<style>
main {
  height: 100% !important;
}

body {
  height: 100%;
  background: #121011;
}

.cont {
  max-width: 90%;
}

.header-btn-call {
  background: transparent;
  border: 1px solid white;
}

.header-btn-sign {
  background: linear-gradient(90deg, #AF1416, #3D1220);
}

.one-screen-decor {
  width: 575px;
  height: 750px;
  background: linear-gradient(#AF1416, #3B1220);
  position: absolute;
  right: 0;
  bottom: 0;
  z-index: 20;
}

.one-screen-right {
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
}

.one-screen-right-img {
  height: 700px;
  margin-bottom: -200px;
  z-index: 11;
}

.one-screen-right-texts {
  position: absolute;
  font-weight: 1000;
  font-size: 120px;
  line-height: 130px;
  color: transparent;
  -webkit-text-stroke-color: white;
  -webkit-text-stroke-width: 1px;
  z-index: 10;
}

.one-screen-right-texts :nth-child(2) {
  color: white;
}

.one-screen-right-block {
  position: absolute;
  background: linear-gradient(90deg, #AF1416, #3b1220ba);
  left: 0;
  bottom: 40px;
  z-index: 21;
}
</style>
