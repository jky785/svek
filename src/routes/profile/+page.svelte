<div class="c1">
  <img alt="User avatar" src={$page.data?.session?.user?.image ?? "https://source.boringavatars.com/marble/120"} class="avatar"/>
  {#if $page.data.session}
    <strong>{$page.data.session.user?.email ?? $page.data.session.user?.name}</strong>
  <br>
    <SignOut />
  {:else}
    <strong>Please SignIn</strong>
  <br>
    <SignIn />
  {/if}
</div>
<script>
  import { page } from "$app/stores"
  import { SignIn, SignOut } from "@auth/sveltekit/components"
</script>
<style scoped>
  .c1{
    text-align: center;
  }
  .avatar{
    border-radius: 70%;
    overflow: hidden;
  }                     
</style>                           
                              