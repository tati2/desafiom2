<template>
<section>
  <div class="menu">
    <img class="menu-img" src="../assets/menuhamburguer.svg">
    <img class="menu-text" src="../assets/logo.svg">
    <img class="menu-img" src="../assets/Lupa-busca.svg">
  </div>
    <div class="conteiner-descriçao">
      <h1>
        De tanto ganhar meias de Natal, <br>tio-avô ganha livro e tenta calçá-lo</br>
      </h1>
      <img class="img-descriçao" src="../assets/cacarlivros.jpg">
      <p class="text-descriçao">
        Foi uma cena estranha no Natal antecipado da família Siqueira, na zona norte do Rio de Janeiro. Bem mais estranha do que a Tia Julinha perguntando à sobrina Cássia pela 76a vez quando ela ia se casar. Ou o cunhado Valcir tentando entoar Então é Natal, da Simone. Eram quase onze da noite quando o tio-avô Onofre, de 77 anos, ganhou seu presente. Abriu e era um livro, a biografia de Jô Soares, que sua irmã Olga comprara com ótimo preço na Saraiva. Onofre olhou, olhou e olhou o livro por muitos minutos. Os parentes imaginaram que ele estava emocionado. De repente Onofre se sentou, tirou seu sapato e colocou o livro perto do pé. A família demorou a entender: ele estava tentando calçar o livro. Resultado das meias que ganhou nos últimos 17 anos.
      </p>
      <p>Comentário</p>
      <hr>
    </div>
    <div v-for="recado in usuario.recados">
      <p>{{recado}}</p>
    </div>
   <div  class="conteiner-comentario">
    <ul>
      <li>
        <img src="../assets/profile.svg">
         <input v-model="recado" v-on:keyup.enter="addRecado">
          <button v-on:click>{{Envio}}</button>
      </li>
      <li>
        <img src="../assets/profile2.svg">
        <p class="comentario-nome">
          Camila RJ
        </p>
        <p class="comentario-texto">
          "Eu teria feito o mesmo sinceramente. Papai Noel nunca me deu oq eu pedi"
        </p>     
      </li>
      <li>
        <img src="../assets/profile3.svg">        
         <p class="comentario-nome">
            Joaquim Campinas
          </p>
          <p class="comentario-texto">"kkkkkkkkkkkkkkkkkkkk rindo até 2049. Muito engraçado!!!!!"</p>
      </li>
    </ul>
    </div>
  </div>
</section>
</template>
<script>
export default {
  name: 'hello',
  data () {
     return {
        Envio: 'Enviar',
        usuario:'',         
          recados: ['']
      } 
    },
  
  methodos:{
      methods: {
      addRecado(recado){
        return this.usuario.recados.push(this.recado),
             this.recado = ''
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.menu{
  display: flex;
  flex-direction: row;
  justify-content: space-around;
  align-items: center;
  background-color: #000; 
}
.menu-img{
  width: 8%;
  padding: 2%;

}
.menu-text{
width:50%;


}
hr{
  height:1px; border:none; color:#000; background-color:#000; margin-top: 0px; margin-bottom: 0px;      
}

.conteiner-descriçao{
  margin: 2.5%;
  justify-content: center;
  align-items: center;
  font-family: 'Open Sans,Bold';
}
h1{
  text-align: center;
  font-size: 1.2em;  
}
.img-descriçao{
  width: 100%;
}
.text-descriçao{

}
ul{
  width: 20%;
  /*display: flex;
  flex-direction: column;
  flex-wrap: wrap;*/
  
  list-style: none;
}
.conteiner-comentario{
 max-width:20%;
  display: flex;
  flex-direction: column;
  flex-wrap: wrap;
  
}
.comentario-texto{
  width: 3%;
  height:4%;

}
.comentario-nome{

}
</style>

