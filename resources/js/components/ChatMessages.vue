<template>
    <ul class="chat">
        <li class="left clearfix" v-for="message in messages">
            <div class="chat-body clearfix">
                <div class="header">
                    <strong class="primary-font">
                        {{ message.user.name }}
                    </strong>
                </div>
                <p>
                    {{ message.message }}
                </p>
            </div>
            <button class="btn btn-primary btn-sm" id="btn-chat" @click="deleteMessage"> Remove Message </button>
        </li>
    </ul>
</template>

<script>
  export default {
    props: ['messages']
  };
</script>

<!--TODO:
    -if message.user.id = user's id, render delete button
-->