<script setup>
import GuestLayout from '@/Layouts/GuestLayout.vue'
import Label from '@/Components/InputLabel.vue'
import Input from '@/Components/TextInput.vue'

const emitTest = e => console.log(e)

</script>

<template>
  <GuestLayout>
    <Label value="件名">タイトル</Label>
    <!-- @update:modelValueはemit処理のこと。子コンポーネントで入力があればemitTestの処理が走る -->
    <Input
      modelValue="初期値が入ります"
      @update:modelValue="emitTest"
    ></Input>
  </GuestLayout>
  
</template>
