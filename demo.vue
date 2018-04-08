<template>
    <div>
        <div id = "app" > 
            {{ message }} 
        </div> 

        <!-- 计算属性 -->
        <div id="eg">
            <p>Original message:"{{message}}"</p>
            <p>Computed reversed message:"{{reversedMessage}}"</p>
        </div>
    </div>
</template>

<script >
    var app = new Vue({
        el: "app",
        data: {
            message: 'Hello Vue！'
        }
    }) 
    var vm=new Vue({
        el:"eg",
        data:{
         message:'Hello'
        },
    computed:{
        reversedMessage:function(){
            return this.message.split('').reverse().join('')
        }
    }
    })
</script>