<script lang="ts">
  export let currentId: string;
  export let id: string;
  export let message: string;
</script>

<div class="message-container" class:mine={currentId === id}>
  <img
    width="40px"
    src={`https://avatars.dicebear.com/api/bottts/` + id + ".svg"}
    alt="Avatar"
  />
  <div class="balloon">{message}</div>
</div>

<style>
  .message-container {
    display: flex;
    flex-direction: row;
  }
  .mine {
    flex-direction: row-reverse;
  }
  .mine .balloon {
    background-color: #3273dc;
    color: #fff;
  }
  .balloon {
    position: relative;
    background-color: #fff;
    padding: 10px;
    color: #333;
    margin: 15px;
    border-radius: 3px;
    white-space: pre-wrap;
    word-break: break-word;
  }
</style>
