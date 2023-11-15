<template>
    <div class="input-container" v-if="file == ''">
          <input name="file" type="file" id="input-file" class="input-container_input-file" @change="addFile">
          <label   for="input-file" class="input-container_button button">
              <span class="button_text">Прикрепить скриншот</span>
              <span class="button_ext">.png / .jpg / .pdf</span>    
          </label>
          
        </div> 
        <div v-else class="file-container">
          <span class="file-container_name">{{file.name}}</span>
          <remove-icon class="file-container_dlt-btn" @click="deleteFile"></remove-icon>
        </div>
</template>
<script>
import RemoveIcon from './icons/RemoveIcon.vue'
export default {
  name: 'InputFile',
  components: {
    RemoveIcon
  },
  data() {
    return {
      file: ''
    }
  },
  methods: {
    addFile(e) {
      this.file = e.target.files[0]
      this.$emit('input', this.file)
    },
    deleteFile() {
      this.file = ''
      this.$emit('input', this.file)
    }
  }
}
</script>

<style scoped lang="scss">
.file-container {
  display: flex;
  align-items: center;
  padding: 50px 0px;
  &_name {
    text-decoration: underline;
    margin-right: 15px;
    font-size: 18px;
    @media (min-width: 320px) and (max-width: 1024px) {
      font-size: 16px;
    }
  }
  &_dlt-btn {
    cursor: pointer;
  }
}
.input-container {
  padding:  39px 137px;
  background-image: url("data:image/svg+xml,%3csvg width='100%25' height='100%25' xmlns='http://www.w3.org/2000/svg'%3e%3crect width='100%25' height='100%25' fill='none' stroke='%23333' stroke-width='4' stroke-dasharray='6%2c 14' stroke-dashoffset='0' stroke-linecap='square'/%3e%3c/svg%3e");
  box-sizing: border-box;
  &_input-file {
    opacity: 0;
    visibility: hidden;
    display: none;
  }
  .button {
    display: flex;
    flex-direction: column;
    align-items: center;
    cursor: pointer;
    &_text {
      border-bottom: 1px solid #ffffff;
      margin-bottom: 7px;
      white-space: nowrap;
    }
    &_ext {
      font-size: 12px;
      line-height: 14px;
    }
  }
}
@media (min-width: 320px) and (max-width: 1024px) {
  .input-container {
    padding: 50px 65px;
    width: 296px;
    display: flex;
    .button_ext {
       display: none;
    }
  }
}
</style>