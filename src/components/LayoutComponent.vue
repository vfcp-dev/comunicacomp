<template>
    <div>
      <Header />
      <HeaderComponent/>
      <div class="content">
        
        <AsideComponent >
          <Aside @show-form="showForm = true" @show-name="showName = true" />
        </AsideComponent>
        <Main>
          <MainComponent></MainComponent>
          <FormComponent v-if="showForm" @submit-name="nameSubmitted" />
          <p v-if="showName">Nombre del estudiante: {{ studentName }}</p>
          
        </Main>
      </div>
    </div>
  </template>
  
  <script>
  import HeaderComponent from './HeaderComponent.vue';
  import AsideComponent from './AsideComponent.vue';
  import MainComponent from './MainComponent.vue';
  import FormComponent from './FormComponent.vue';
  
  
  export default {
    components: {
      HeaderComponent,
      AsideComponent,
      MainComponent,
      FormComponent,
      
    },
    
   
  };
  </script>
  
  <style>
  .content {
    display: flex;
  }
  </style>
  