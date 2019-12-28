<template>
  <div>
    <h2 class="centralizado">Engenheiros de Software responsáveis pela criação do Clean</h2>
    <ul class="corpo lista-fotos">
      <li v-for="user in users" :key="user.id" class="lista-fotos-item">
          <meu-painel v-bind:titulo="user.name" v-bind:repositories="user.public_repos" >
              <a :href="user.html_url" target="_blank">
            <img class="imagem-resposiva" :src="user.avatar_url" :alt="user.name" :title="user.login" />
              </a>
          </meu-painel>
      </li>
    </ul>
  </div>
</template>

<script>
import axios from 'axios'
import Painel from '~/components/shared/Painel'
export default {
  computed: {
  },
  name: 'Tela',
  components: {
    'meu-painel': Painel
  },
  created () {
    const gitHubUsers = ['vilson-passos', 'gabrieljsantos', 'jjaviles2010', 'lecosas']
    gitHubUsers.map((gitUser) => {
      axios
        .get(`https://api.github.com/users/${gitUser}`)
        .then((response) => {
          this.users.push(response.data)
        }).catch((erro) => {
          this.erros.push(erro)
        })
    })
  },
  methods: {
  },
  data () {
    return {
      titulo: 'Título da minha página',
      seen: false,
      users: [],
      erros: []
    }
  },
  props: {
    msg: String
  }
}
</script>

<style scoped>
.centralizado {
  text-align: center;
  font-weight: bold;
  margin: 5%
}

.corpo {
  font-family: Helvetica, Arial, sans-serif;
  margin: 5% 30%;
  width: 50%;
}

.lista-fotos {
  list-style: none;
  color: #ffffff;
}

.lista-fotos .lista-fotos-item {
  display: inline-block;
}

.imagem-responsiva {
    width: 100%;
  }

</style>
