<template>
    <!-- テキストボックス、送信ボタン④ -->
    <div id="bms_send">
        <textarea v-model="msg" id="bms_send_message"></textarea>
        <div v-on:click="sendMsg" id="bms_send_btn">送信</div>
    </div>    
</template>
<script>
import axios from "axios"

const botEndPoint = "http://localhost:3000/work/"
export default {
    name: "MessageForm",
    props: {
        msg: String
    },
    methods:{
        sendMsg: function sendMsg(event) {
            alert("hoge")
            axios.get(botEndPoint)
            .thne((res) => {
                console.log(res.data)
                const hoge = res.data["hoge"]
                alert(hoge)
            })
            .catch((res) => {
                console.log(res)
            })

            console.log(retbot)
            return null
        }
    }
}

</script>
<style>
/* テキストエリア、送信ボタン④ */
#bms_send {
    background-color:#eee;/*タイムラインの色と同じにする*/
    border-right: 1px solid #ddd;
    border-left: 1px solid #ddd;
    border-bottom: 1px solid #ddd;
    height: 48px;
    padding: 4px;
}
    #bms_send_message{
        width: calc(100% - 75px);/*常に送信ボタンの横幅を引いたサイズに動的に計算*/
        line-height: 16px;
        height: 48px;
        padding: 14px 6px 0px 6px;/*文字がテキストエリアの中心になる様に隙間調整*/
        border: 1px solid #ccc;
        border-radius: 4px;/*角丸*/
        text-align: left;/*文字を左寄せ*/
        box-shadow: 2px 2px 4px 0px rgba(0,0,0,0.2) inset;/*内側に影を入れてテキストエリアらしくした*/
        box-sizing: border-box;/*paddingとborderの要素の高さと幅の影響をなくす（要素に高さと幅を含める）*/

    }
    #bms_send_btn {
        width: 72px;
        height: 48px;
        font-size: 16px;
        line-height: 3em;
        float: right;/*bms_sendに対して右寄せ*/
        color: #fff;
        font-weight: bold;
        background: #bcbcbc;
        text-align: center;/*文字をボタン中央に表示*/
        border: 1px solid #bbb;
        border-radius: 4px;/*角丸*/
        box-sizing: border-box;/*paddingとborderの要素の高さと幅の影響をなくす（要素に高さと幅を含める）*/
    }
    #bms_send_btn:hover {
        background: #13178E; /*マウスポインタを当てた時にアクティブな色になる*/
        cursor: pointer;/*マウスポインタを当てた時に、カーソルが指の形になる*/
    }
</style>
