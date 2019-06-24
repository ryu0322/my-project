<template>
<div class="bms_message bms_right">
    <div class="bms_message_box">
        <div class="bms_message_content">
            <div class="bms_message_text">{{msg}}</div>
        </div>
    </div>
</div>
</template>
<script>
export default {
    name: "SelfMessage",
    props: {
        msg: String
    }
}


</script>

<style>
     /* メッセージ２（右側） */
    .bms_right {
        float: right;/*吹き出しをbms_messagesに対して右寄せ*/
        line-height: 1.3em;
    }
    /*
    *追加
    */
    .bms_right .bms_message_box {
        color: #fff;/*テキストを白にする*/
        background: #13178E;
        border: 2px solid #13178E;
        border-radius: 30px 30px 0px 30px;/*右下だけ尖らせて吹き出し感を出す*/
        margin-left: 50px;/*右側の発言だとわかる様に、吹き出し左側に隙間を入れる*/
    }
</style>
