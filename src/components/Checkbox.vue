<template>
    <label class="label">Согласен на обработку персональных данных
      <input type="checkbox" checked="checked">
      <span class="checkmark"></span>
    </label>
</template>
<script>
export default {
  name: 'CheckboxComponent',
}
</script>


<style scoped lang="scss">
.label {
  display: block;
  position: relative;
  padding-left: 24px;
  cursor: pointer;
  font-size: 12px;
  line-height: 14.06px;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

/* Hide the browser's default checkbox */
.label input {
  position: absolute;
  opacity: 0;
  cursor: pointer;
  height: 0;
  width: 0;
}

/* Create a custom checkbox */
.checkmark {
  position: absolute;
  top: 0px;
  left: 0px;
  height: 14px;
  width: 14px;
  border: 1px solid #777777;
}

/* Create the checkmark/indicator (hidden when not checked) */
.checkmark:after {
  content: "";
  position: absolute;
  display: none;
}

/* Show the checkmark when checked */
.label input:checked ~ .checkmark:after {
  display: block;
  background-image: url('data:image/svg+xml,\<svg width="10" height="7" viewBox="0 0 10 7" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M8.94976 1.08233L4.00002 6.03208L1.17159 3.20365" stroke="#F8F200"/>\</svg>');
  background-repeat: no-repeat;
  background-position: center center;
  background-size: 50% 50%;
}

/* Style the checkmark/indicator */
.label .checkmark:after {
  left: 4px;
  top: 1px;
  width: 4px;
  height: 7px;
  border: solid #F8F200;
  border-width: 0 1.5px 1.5px 0;
  -webkit-transform: rotate(45deg);
  -ms-transform: rotate(45deg);
  transform: rotate(45deg);
}
</style>