<template>
  <div class="bg-[#33333385] fixed top-0 left-0 right-0 bottom-0 flex items-center sm:justify-center font-montserrat" >
    <div @click="inviteMember">
      <div class="bg-white rounded-lg shadow-lg">
        <header-member @closeMem="closeMem"></header-member>
        <div class="pl-5 pr-5">
          <form @submit.prevent="postMember">
            <email-member></email-member>
            <role-member></role-member>
            <button-send></button-send>
            <member-join></member-join>
          </form>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import HeaderMember from './HeaderMember.vue';
import EmailMember from './EmailMember.vue';
import RoleMember from './RoleMember.vue';
import ButtonSend from './ButtonSend.vue';
import MemberJoin from './MemberJoin.vue';

export default {
  components: {
    HeaderMember,
    EmailMember,
    RoleMember,
    ButtonSend,
    MemberJoin,
  },
  data(){
    return{
      PopupMember:false,
      items:{
        email: '',
        role:''
      }
    }
  },
 
  methods:{
    closeMem(){
      this.PopupMember=false;
    },
    inviteMember() {
      this.$emit("inviteMember")
    },
  },
}
</script>
