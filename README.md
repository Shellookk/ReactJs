# ReactJs
<p>Repositório exclusivo para o estudo do React</p><br>
<p>Seja bem-vindo e volte sempre!!!</p>

# Modulo 1: Iniciando com React.js
<strong>Bundlers:</strong> 
- Servem para organizar as importações javascript e fazer a comunicação assertiva.<br>

<strong>Compilers:</strong>
- Servem para compilar o codigo e transformar-lo em uma versão que o navegador consiga entender.<br>

<strong>Vite:</strong>
- É um framework que ja faz o trabalho dos bundlers e do compilers. A vantagem é que ele possui um compilador interno e também ele é mais rapido ja que não possui bundlers e sim usa componentes nativos.<br>

<strong>Criando um projeto com React:</strong>

 <ol>
 <strong><li>Instalando o NodeJS:</li></strong>
 <ul>
    <li>
     Instalação pelo site oficial: Você pode seguir os passos de instalação no site oficial do Node.js. O site irá fornecer um instalador apropriado para o seu ambiente.    
    </li>
    <li>
     Utilizando um gerenciador de versões: Se você é um usuário  mais avançado, pode optar por um gerenciador de versões para o Node.js, facilitando a troca e o uso de diferentes versões do Node.js conforme necessário.<br>
    Link: https://nodejs.org/en
    </li>
 </ul>
 
 <strong><li>Instalando o Vite:</li></strong>
 <ol>

 <li>Execute o código:</li>

    npm create vite@latest

 <li>Aperte <strong>Y</strong> para continuar a instalação dos pacotes.</li>
 <li>Nomeie o projeto.</li>
 <li>Selecione o Framework que você irá utilizar.</li>
 <li>Selecione a linguagem do projeto e acesso o projeto.</li>
 </ol>   

<strong><li>Inicializando o projeto</li></strong>
 <ol>
 <li>instale as dependencias do projeto</li>
    
    npm i
 
 <li>inicie o projeto com o comando abaixo:</li>
    
    npm run dev
 </ol>


 <strong><li>Componentes</li></strong>
 <p>Componentes são uma parte da integração que podem ser repetidos várias vezes e com informações diferentes. 
 O componente no React é um função que retorna um html. Todos os componentes da aplicação React, precisam ter extensão .jsx === JavaScript + XML.
 </p>

  <strong>Boas Práticas de Desenvolvimento:</strong>
 <ol>
   <li>É necessário ter um elemento pai para ter multiplos componentes. 
   <br>
   <strong>Exemplo:</strong></li><br>

   ```
   function App(){
      return(
         <Post/>
         <Post/>
         <Post/>
         <Post/>
      )
   }

   export default App
   ```

   <p>O código acima retornará um erro, pois é necessário ter um elemento pai para conseguir ter vários elementos no mesmo componente.<br></p>
   <strong>Solução:</strong>
   
   ```
   function App(){
      return(
         <> ou <div>
            <Post/>
            <Post/>
            <Post/>
            <Post/>
         <> ou </div>
      )
   }

   export default App
   ```

   O código acima se comportará de acordo com o esperado pois ele tem um elemento pai.
   <li>Exportação de funções ou componentes(Default Exports vs named Exports).</li><br>
   <strong><p>export default:</p></strong>
   <p>Quando exportamos uma função ou componente por padrão utilizando:</p>
   
   <strong><p>Exemplo de exportação:</p></strong>
  
   ```
      export default App
   ```

   <p>Podemos renomear o componente na hora de importa-lo:</p>

   <strong><p>Exemplo de importação:</p></strong>
   
   ```
      import NomeAleatorio from  './App';
   ```

   <p>No exemplo acima, mesmo eu importando com qualquer nome, o código irá funcionar normalmente, pois a importação de um componente exportado por default ignora o nome dado na hora da exportação.</p>
   <p>Um ponto negativo para se falar é que esse tipo de importação pode acabar afetando negativamente o código, pois caso você dê um nome diferente do nome do componente ou função, ele irá aceitar e ficará dessa forma.</p>

   <strong><p>named exports:</p></strong>
   <p>para utilizar o named export, exportamos a função/componente utilizando o export antes de declarar afunção como mostra no exemplo abaixo.</p>
   
   <strong><p>Exemplo de exportação:</p></strong>
   
   ```
      export function App(){
         return <h1>Hello World!</h1>
      }
   ```

   <p>Desse jeito só é possivel importar o componente utilizando o nome exato do componente ou função.</p>
   <strong><p>Exemplo de importação:</p></strong>
   
   ```
      import { App } from  './App';
   ```

   <p> Assim, ao importar dessa forma você terá a certeza que estará chamando o componente que precisa.</p>
 </ol>
 <strong><li>Propriedades</li></strong>
 <p>Propriedades são atributos que podem ser passados dentro dos componentes e funções, elas podem diferenciar os componentes e váriam de acordo com cada um. Isto é, você cria um componente para ser usado várias vezes, ai você passa a propriedade para mudar o conteudo ou alguma caracteristica do componente para ele servir de acordo com o seu critério de aceite.</p>

 <strong><p>Exemplo de declaração de uma propriedade dentro de um componente importado:</p></strong>
 
 ```
 import { Post } from './Post'

 export function App(){
   return(
      <div>
         <Post author="Isaque Rodrigues" />
      </div>
   )
 }
 ```
 <p>Nesse exemplo de cima eu estou passando a propriedade author para o componente Post. Para que essa propriedade seja visualizada e o componente aceite ela, é preciso fazer algumas modificações dentro do arquivo.</p>

 <strong><p>Exemplo de um componente que aceita uma propriedade:</p></strong>

 ```
 export function Post(props){
   return(
      <>
         <p>{props.author}</p>
      </>
   )
 }
 ```
 <p>No exemplo acima eu criei uma função onde eu passo props como parametro e eu retorno um paragrafo com o author. Sabe-se pelo primeiro exemplo que eu passei dentro do componente a propriedade author que no começo não era aceito, a partir do momento que eu passei o parametro dentro da função, ela passou a reconhecer a props author.</p><br>
 <p>Esse é um exemplo prático de como criar um componente para ser reutilizado várias vezes e como passar uma propriedade ou várias ao mesmo tempo. nesse caso alem de author eu poderia ter criado várias outras e no componente eu poderia editar caso eu desejasse melhorar a visualização, ou outra coisa.</p>



</ol>