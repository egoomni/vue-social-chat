<template>
  <div>
    <hr>
    <h1>Email click to chat demo</h1>
    <SocialChat
      icon
      class="email-chat"
      :attendants="attendants"
    >
      <template v-slot:header>
        <p>Click one of our representatives below to send Email.</p>
      </template>
      <template v-slot:button>
        <img
          src="https://raw.githubusercontent.com/ktquez/vue-social-chat/master/src/icons/email.svg"
          alt="icon email"
          aria-hidden="true"
        >
      </template>
      <template v-slot:footer>
        <small>
          Call us to
          <a
            href="tel:+55988656544"
            title="Call us"
          >
            +55 95865-6544
          </a>
          from 8:00hs a 18:00hs
        </small>
      </template>
    </SocialChat>
  </div>
</template>

<script>
import { SocialChat } from '../../vue-social-chat'

export default {
  name: 'EmailPage',

  components: {
    SocialChat
  },

  data: () => ({
    attendants: [
      {
        label: 'Support',
        name: 'Alan Ktquez',
        href: 'mailto:ktquez@gmail.com?subject=Testing out mailto!',
        avatar: {
          src: 'https://avatars0.githubusercontent.com/u/8084606?s=460&u=20b6499a416cf7129a18e5c168cf387e159edb1a&v=4',
          alt: 'Alan Ktquez avatar'
        }
      },
      {
        label: 'Sales',
        name: 'Alexia Chapman',
        href: 'mailto:ktquez@gmail.com?subject=Testing out mailto!',
        avatar: {
          src: 'https://randomuser.me/api/portraits/women/63.jpg',
          alt: 'Alexia Chapman avatar'
        }
      },
      {
        label: 'Human Resources',
        name: 'April Gonçalves',
        href: 'mailto:ktquez@gmail.com?subject=Testing out mailto!',
        avatar: {
          src: 'https://avatars3.githubusercontent.com/u/609862?s=400&u=e58f7e1a6a5e5ce21979a183db43870582ffcde4&v=4',
          alt: 'Avatar Support April Gonçalves'
        }
      }
    ]
  })
}
</script>
