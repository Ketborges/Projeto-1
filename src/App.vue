<script setup>
import { ref } from 'vue'
  const nome = ref('')
  const data = ref('')
  const email = ref ('')
  const senha = ref ('')
  const confirma = ref ('')
  const estado = ref('')
  const endereco = ref('')
  const cidade = ref('')
  const hobby = ref('')
  const linguagem = ref ('')
  const biografia = ref('')
  const mostrar = ref (false)
</script>

<template>
  <div class="mae">
    <form @submit.prevent="">
      <label for="text">Nome: </label>
        <input type="text" v-on:keypress="ok= false" v-model="nome" required placeholder="digite seu nome" /> 
        <span>Nome: {{ nome }}</span>
      
      <label for="date">Data de nascimento: </label>
        <input type="date" v-on:keypress="ok= false" v-model="data" required placeholder="data de nascimento" /> 
        <span>Data: {{ data }}</span>
      
      <label for="text">Endereço: </label>
        <input type="text" v-on:keypress="ok=false" v-model="endereco" required placeholder="Digite seu endereço" />
        <span>Endereço: {{ endereco }}</span>  
      
      <label for="text">Cidade: </label>
        <input type="text" v-on:keypress="ok=false" v-model="cidade" required placeholder="Digite sua cidade" />
        <span>Cidade: {{ cidade }}</span>
      
      <label for="email">Email: </label>
        <input type="email" v-on:keypress="ok= false" v-model="email" required placeholder="digite seu email"/> 
        <span>Email: {{ email }}</span>
      
      <label for="text">Hobby: </label>
        <input type="text" v-on:keypress="ok= false" v-model="hobby" required placeholder="digite seu hobby"/> 
        <span>Hobby: {{ hobby}}</span>
          
      <label for="text">Linguagem de programação: </label>
        <input type="text" v-on:keypress="ok=false" v-model="linguagem" required placeholder="Digite sua linguagem" />
        <span>Linguagem de programação: {{ linguagem }}</span>
      
      <label for="text">Biografia: </label>
        <input type="text" v-on:keypress="ok=false" v-model="biografia" placeholder="Digite sua biografia" />
        <span>Biografia: {{ biografia }}</span>
      
      <label for="Estados">Estado</label>
      <select v-on:keypress="ok =false" v-model="estado">
        <option value="">Escolha seu Estado</option>
        <option value="12">AC - Acre</option>
        <option value="27">AL - Alagoas</option>
        <option value="16">AP - Amapa</option>
        <option value="13">AM - Amazonas</option>
        <option value="29">BA - Bahia</option>
        <option value="23">CE - Ceara</option>
        <option value="53">DF - Distrito Federal</option>
        <option value="32">ES - Espirito Santo</option>
        <option value="52">GO - Goias</option>
        <option value="21">MA- Maranhão</option>
        <option value="51">MT - Mato Grosso</option>
        <option value="50">MS - Mato Grosso do Sul</option>
        <option value="31">MG - Minas Gerais</option>
        <option value="15">PA - Pará</option>
        <option value="25">PB - Paraiba</option>
        <option value="41">PR - Paraná</option>
        <option value="26">PE - Pernambuco</option>
        <option value="22">PI - Piaui</option>
        <option value="33">RJ - Rio de Janeiro</option>
        <option value="24">RN - Rio Grande do Norte</option>
        <option value="43">RS - Rio Grande do Sul</option>
        <option value="11">RO - Rondônia</option>
        <option value="14">RR - Roraima</option>
        <option value="42">SC - Santa Catarina</option>
        <option value="35">SP - São Paulo</option>
        <option value="28">SE - Sergipe</option>
        <option value="17">TO - Tocantins</option>
      </select> 
      <span>O estado escolhido é é: {{ estado }}</span>  
      <label for="password">senha: </label>
      <input type="password" v-on:keypress="ok= false" v-model="senha" maxlength="8" required placeholder="digite sua senha(máximo de 8 caracteres)" />
      <span>Senha: {{ senha }}</span>      
      <label for="password">Confire sua senha: </label>
      <input type="password" v-on:keypress="ok= false" v-model="confirma" maxlength="8" required placeholder="digite novamente"/>
      <span>Confirmação: {{ confirma}}</span>      
      <button @click="mostrar = !mostrar"> confirmar</button>    
    </form>
    <div v-if="mostrar" class= "mostrar">
      <p>Nome: {{ nome }}</p>
      <p>Endereço: {{ endereco}}</p>
      <p>Cidade digitada: {{ cidade}}</p>
      <p>Email: {{ email}}</p>
      <p>Hobby: {{ hobby }}</p>
      <p>Linguagem de programação: {{ linguagem}}</p>
      <p>Biografia: {{ biografia}}</p>
      <p>Estado: {{estado}}</p>
      <p>Senha: {{ senha }}</p>
      <p>Confirmação:{{ confirma}}</p>
    </div>
  </div>
</template>
<style>
form{
  display: block;
  align-items: center;
  justify-content: center;
  background-color: rgb(255, 0, 0);
}
</style>





