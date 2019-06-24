<template>
    <!--メッセージ１（左側）-->
    <div class="bms_message bms_left">
        <div class="bms_message_box">
            <div class="bms_message_content">
                <div class="bms_message_text">{{msg}}</div>
            </div>
        </div>
    </div>    
</template>
<script>
export default {
    name: "LeftMessage",
    props: {
        msg: String
    }
}
</script>

<style>
    /* メッセージ１（左側） */
    .bms_left {
        float: left;/*吹き出しをbms_messagesに対して左寄せ*/
        line-height: 1.3em;
    }
    /*
    *追加
    */
    .bms_left .bms_message_box {
        color: #333;/*テキストを黒にする*/
        background: #fff;
        border: 2px solid #13178E;
        border-radius: 30px 30px 30px 0px;/*左下だけ尖らせて吹き出し感を出す*/
        margin-right: 50px;/*左側の発言だとわかる様に、吹き出し右側に隙間を入れる*/
    }
</style>
