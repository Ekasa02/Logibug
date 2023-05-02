<template>
  <div class="bg-[#33333385] fixed top-0 left-0 right-0 bottom-0 flex items-center sm:justify-center font-['monserrat']">
    <div>
      <div class="bg-white rounded-lg shadow-lg">
        <header-member></header-member>
        <div class="pl-5 pr-5">
          <email-member></email-member>
          <role-member></role-member>
          <button-send></button-send>
          <member-join></member-join>
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
}
</script>
