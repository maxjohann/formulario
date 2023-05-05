<script setup>
import { ref } from 'vue'
const nome = ref('')
const email = ref('')
const senha = ref('')
const confirmaSenha = ref('')
const data = ref('')
const endereço = ref('')
const cidade = ref('')
const estado = ref('')
const hobbies = ref('')
const linguagemProg = ref([])
const biografia = ref('')
const sexo = ref('') 
const user = ref('')
const aceitar = ref(false)
</script>

<template>
    <form class="info" @submit.prevent="enviar()">
      <p>Nome:</p>
      <input type="text" v-model="nome" minlength="3" maxlength="20" placeholder="Nome" required autocomplete="on"/>
      <p>Email:</p>
      <input type="email" v-model="email" placeholder="Email" required autocomplete="on"/>
      <p>Senha:</p>
      <input type="password" v-model="senha" placeholder="senha" required>
      <p>Confirmar senha:</p>
      <input type="password" v-model="confirmaSenha" placeholder="repita a senha" required>
      <p>Data de nascimento:</p>
      <input type="date" v-model="data" required>
      <p>Endereço:</p>
      <input type="text" v-model="endereço" placeholder="Endereço" required autocomplete="on">
      <P>Cidade:</P>
      <input type="string" v-model="cidade" placeholder="Cidade" required autocomplete="on">
      <p>Estado:</p>
      <select type="string" v-model="estado" required>
        <option>AC</option>
        <option>AL</option>
        <option>AP</option>
        <option>AM</option>
        <option>BA</option>
        <option>CE</option>
        <option>DF</option>
        <option>ES</option>
        <option>GO</option>
        <option>MA</option>
        <option>MT</option>
        <option>MS</option>
        <option>MG</option>
        <option>PA</option>
        <option>PB</option>
        <option>PR</option>
        <option>PE</option>
        <option>PI</option>
        <option>RJ</option>
        <option>RN</option>
        <option>RS</option>
        <option>RO</option>
        <option>RR</option>
        <option>SC</option>
        <option>SP</option>
        <option>SE</option>
        <option>TO</option>
      </select>
      <p>Hobbies:</p>
      <input type="text" v-model="hobbies" placeholder="Hobbies" required>
      <p>Linguagem de Programação:</p>
      <input type="checkbox" v-model="linguagemProg" value="JavaScript">
      <label for="linguagemProg">JavaScript</label>
      <br>
      <input type="checkbox" v-model="linguagemProg" value="C++">
      <label for="linguagemProg">C++</label>
      <br>
      <input type="checkbox" v-model="linguagemProg" value="Python">
      <label for="linguagemProg">Python</label>
      <br>
      <input type="checkbox" v-model="linguagemProg" value="HTML">
      <label for="linguagemProg">HTML</label>
      <br>
      <p>Biografia:</p>
      <input type="text" v-model="biografia" placeholder="Biografia" required>
      <p>Sexo:</p>
      <input type="radio" v-model="sexo" value="Masculino"> Masculino
      <input type="radio" v-model="sexo" value="Feminino"> Feminino
      <br>
      <input type="file" id="avatarField" @change="handleFileUpload($event)">
      <br>
      <button type="submit" @click="aceitar = !aceitar">Enviar</button>
      <br>
      <div v-if="aceitar">formulario aceito</div>
    </form>

  <div v-if="aceitar" id="div">

<p>{{ nome }}</p>
<p>{{ email }}</p>
<p>{{ senha }}</p>
<p>{{ data }}</p>
<p>{{ endereço }}</p>
<p>{{ cidade }}</p>
<p>{{ estado }}</p>
<p>{{ hobbies }}</p>
<p>{{ linguagemProg }}</p>
<p>{{ biografia }}</p>
  </div>
</template>


<style scoped>
.info {
  background-color: rgba(35,12,22,1);
  padding: 20px 30px;
  color: rgb(183, 210, 219);
  border-radius: 10px;
}
h1 {
  color: white;
  font-weight: bold;
  font-size: 1.5em;
}
#div {
  background-color: rgba(35,12,22,1);
  padding: 20px 30px;
  color: rgb(183, 210, 219);
  border-radius: 10px;
  text-align: center;
  margin: 0px 0px 0px 50px;
  height: fit-content;
}
</style>