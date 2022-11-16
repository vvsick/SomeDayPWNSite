<template>
    <div>
        <BaseHeader />
        <section id="team-info" class="hero">
            <div class="hero-body">
                <div class="mb-5">
                    <p class="title has-text-white-ter">
                        Few words about us:
                    </p>
                </div>
                <p class="subtitle has-text-grey-lighter">
                    SomeDayPWN - команда студентов и выпускников СПбГУТ, собранная для участия в различных CTF-ивентах. В нашей команде каждый участник развивает свои навыки, делится опытом и переживает неповторимые эмоции от решения различного рода задач. Для нас является первостепенным постоянный прогресс членов команды, совместное прохождение препятствий и приятное времяпрепровождение. SomeDayPWN участвует во многих CTF-ивентах преимущественно online формата, однако очень часто для этого собирается в одном месте. Спешим напомнить, что мы ищем новых членов команды в наш дружный коллектив, заполнить анкету ты сможешь в самом низу страницы. Мы ждем именно тебя!
                </p>
                <p class="subtitle has-text-grey-lighter">
                    SomeDayPWN - a team of students and graduates of St. Petersburg State University of Telecommunications, gathered to participate in various CTF-events. In our team, each participant develops his hard and soft skills, shares his experience between team members and feel unique emotions from solving various kind of tasks. For us, the constant progress of team members, the joint passage of obstacles and a pleasant pastime is paramount. SomeDayPWN participates in many CTF-events, mostly online, but very often gathers in one place for this. We hasten to remind you that we are looking for new team members to our friendly team, so you cab fill out the form at the very bottom of the page. We are waiting for you!
                </p>
            </div>
            
        </section>
        
        <div class="member-info-container mx-2">
            <ParticipantCard
            v-for="(participant, index) in participantsData"
            :key="index"
            :participant="participant"
            />
        </div>

        <div class="container">
            <p class="has-text-white-ter title my-5">Достижения / Achievments:</p>
        </div>

        <div class="achievments-container mx-2">
            <AchievmentCard
            v-for="(event, index) in eventsData"
            :key="index"
            :event="event"
            />
        </div>
            
        <BaseFooter />
    </div>
</template>

<script>
import BaseHeader from './BaseHeader.vue'
import BaseFooter from './BaseFooter.vue'
import ParticipantCard from './ParticipantCard.vue'
import AchievmentCard from './AchievmentCard.vue'

    export default {
        name: 'MainPage',
        components: {
            BaseFooter,
            BaseHeader,
            ParticipantCard,
            AchievmentCard
        },
        data() {
            return{
                participantsData: [
                    {
                        image: 'wella.jpg',
                        imageAlt: 'Photo of Vladimir Moiseev',
                        gitLink: 'https://github.com/wellafl3x',
                        vkLink: 'https://vk.com/sayhellotourmum',
                        telegramLink: 'https://t.me/wellaf13x',
                        nickname: 'wellafl3x',
                        ruDescription: 'Владимир Моисеев, 21 год. Студент Института Магистратуры СПбГУТ. Свое увлечение пентестингом нашел еще в старшей школе, тестируя свою систему на проникновение с помощью вредоносного ПО и утилит брутфорса. В университете развил свои навыки в области межсетевого взаимодействия и администрирования сетей.',
                        enDescription: 'Vladimir Moiseev, 21 y.o. Master`s degree student of SPbSUT. Found his passion for pentesting in high elementary school while testing his system for penetration using malware and bruteforce utilities. At the university developed his skills in the filed of internetworking and network administration.',
                        skills: ['traffic', 'forensic', 'crypto']
                    },
                    {
                        image: 'dim.jpg',
                        imageAlt: 'Photo of Dmitry Podobed',
                        gitLink: 'https://github.com/SpiritOfSea/',
                        vkLink: 'https://vk.com/blue_greebok',
                        telegramLink: 'https://t.me/justaspirit',
                        nickname: 'SpiritOfSea',
                        ruDescription: 'Дмитрий Подобед, 22 года. Выпускник факультета ИКСС СПбГУТ. Из предпочтений Дмитрия можно отметить решение задач по поиску WEB-уязвимостей, PWN, а также RE. В настоящее время работает инженером по информацонной безопасности в одной из больших компаний.',
                        enDescription: 'Dmitriy Podobed, 22 y.o. IKSS faculty graduate of SPbSUT. Among Dmitry`s preferences, we can note the solution for finding WEB vulnerabilities, PWN and Reverse engeneerin. He`s currently working as an cybersecurity engineer in one of the large companies.',
                        skills: ['web', 'pwn', 'forensic', 'programming']
                    },
                    {
                        image: 'vvsix.jpg',
                        imageAlt: 'Photo of Vladimir Osykin',
                        gitLink: 'https://github.com/vvsick',
                        vkLink: 'https://vk.com/vvsix',
                        telegramLink: 'https://t.me/antimaax',
                        nickname: 'vvsix',
                        ruDescription: 'Владимир Осыкин, 22 года. Выпускник факультета ИКСС СПбГУТ. Из сильных сторон можно отметить решение задач в сферах стеганографии, криптографии и OSINT, так же интересуется эксплуатацией WEB-уязвимостей.',
                        enDescription: 'Vladimir Osykin, 22 y.o. Graduate of the faculty of IKSS SPbSUT. Of the strengths, one can note the solution of problems in the areas of steganography, cryptography and OSINT, he is also interested in the exploitation of WEB vulnerabilities.',
                        skills: ['osint', 'stego', 'web']
                    },
                    {
                        image: 'andrey.jpg',
                        imageAlt: 'Photo of Andrey Ursegov',
                        gitLink: 'https://github.com/sweetysweat',
                        vkLink: 'https://vk.com/sweety_sweat',
                        telegramLink: 'https://t.me/sweety_sweat',
                        nickname: 'Sweety_Sweat',
                        ruDescription: 'Андрей Урсегов, 22 года. Студент Института Магистратуры СПбГУТ. В университете развил свои навыки администрирования различных серверных решений, отточил навыки взаимодействия с различными БД. Хорошо зарекомендовал себя в качетсве DevOps иженера, коим и работает в данный момент. Предпочитает решение RE, Programming  и PWN задач.',
                        enDescription: 'Andrey Ursegov, 22 y.o. Master`s degree student of SPbSUT. At the university, he developed his skills in administering various server solutions, honed his skills in interacting with various databases. He has proven himself as a DevOps engineer, which he currently works with. Prefers solving RE, Programming and PWN tasks.',
                        skills: ['reverse', 'sql', 'programming']
                    },
                    {
                        image: 'yana.jpg',
                        imageAlt: 'Photo of Yana Perminova',
                        gitLink: '',
                        vkLink: 'https://vk.com/yaperko',
                        telegramLink: 'https://t.me/yaperko',
                        nickname: 'Yaperko',
                        ruDescription: 'Яна Перминова, 22 года. Студет Института Магистратуры СПбГУТ. Предпочитает решать сложные задачи в областях OSINT, Digital Forensics, криптографии и стеганографии. В данный момент работает техническим инженером в научно-техническом центре.',
                        enDescription: 'Yana Perminova, 22 y.o. Master`s degree student of SPbSUT. Prefers solving hard tasks in OSINT, Digital Forensics, Crypto and Steganography. Currently working as technical engeneer in STC.',
                        skills: ['osint', 'stego', 'crypto']
                    }
                ],
                eventsData: [
                    {
                        image: 'Cyber_Sec.png',
                        imgAlt: 'Cyber Sec logo',
                        link: 'http://sut.ru/bonchnews/science/17-12-2021-Cyber_Security-hackathon',
                        title: 'Cyber_Security hackathon-2021',
                        description: '1st place among 29 teams',
                        date: '5.01.2021 - 10.01.2021',
                        format: 'Docker vuln`s'
                    },
                    {
                        image: 'knight.png',
                        imgAlt: 'KnightCTF logo',
                        link: 'https://ctftime.org/event/1545',
                        title: 'KnightCTF 2022',
                        description: '142nd  place among 751 teams',
                        date: '20.01.2022 - 21.01.2022',
                        format: 'Jeopardy'
                    },
                    {
                        image: 'home.png',
                        imgAlt: 'StayHome logo',
                        link: 'https://ctftime.org/event/1463',
                        title: 'Stay ~/ CTF 2022',
                        description: '32nd place among 112 teams',
                        date: '06.02.2022',
                        format: 'Attack / Defence'
                    },
                    {
                        image: 'Vu.png',
                        imgAlt: 'Vu Cyberthon logo',
                        link: 'https://ctftime.org/event/1518/',
                        title: 'Vu Cyberthon 2022',
                        description: '44th place among 404 teams',
                        date: '17.02.2022 - 18.02.2022',
                        format: 'Jeopardy'
                    },
                    {
                        image: 'logo_deadface_ctf.png',
                        imgAlt: 'Deadface Ctf logo',
                        link: 'https://ctftime.org/event/1692',
                        title: 'DeadFace CTF 2022',
                        description: '63rd place among 1173 teams',
                        date: '14.10.2022 - 16.10.2022',
                        format: 'Jeopardy'
                    }
                ],
            };
        }, 
        computed: {
            hasContent() {
                return !!this.$slots.tile
            }
        } 
    }
</script>

<style>
    .nickname {
        font-family: 'Silkscreen', cursive;
        font-size: 20px;
    }
    img {
        object-fit: cover;
        border-radius: 5px;
        
    }
    .description {
        line-height: 1.1;
        font-size: 20px;
    }
    .description_events {
        line-height: 1.1;
        font-size: 20px;
    }
    .member-info-container, .achievments-container {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(48%, 1fr));
        column-gap: 20px;
    }
    .achievments-container {
        row-gap: 20px;
    }
    .box {
        background-color: #222222;
    }
    .hoverable-link:hover {
        fill: #33614a !important;
        color: #33614a !important;
    }
    .icon {
        fill: #ffffff;
    }
</style>