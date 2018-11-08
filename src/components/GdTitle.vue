<template>
    <div class="gd_title">
        <cell title="正品保障" value="hello" is-link @click.native="show13 = true">

        </cell>
    
        <div>
            <div v-transfer-dom class="gd_content">
                <popup v-model="show13" position="bottom" max-height="100%">
                    <group>
                    <cell >
                        <img class="gd_img" src="../assets/images/gd_1.png" >
                        <p>商品为正品行货</p>
                        <p>
                            所销售的商品均从品牌方、代理商、品牌分支机构、国际品牌驻中国办事处等正规渠道采购，并与之签订战略正品采购协议，可放心购买。
                        </p>
                        <img src="../assets/images/xieyi.png" alt="">
                        <br>
                    </cell>
                    <cell >
                        <img class="gd_img" src="../assets/images/gd_2.png" >
                        <p>平安保险保障正品</p>
                        <p>该商品由平安保险承保奶粉保险,凡购买自营奶粉的宝宝们都将免费获得此保险一份。如果宝宝在食用奶粉过程中出现过敏现象，或检测出不是正品，在取得第三方检测机构的鉴定报告后，可向我们发起理赔。</p>
                    </cell>
                    <cell >
                        <img class="gd_img" src="../assets/images/gd_3.png" >
                        <p>多重复审</p>
                        <p>每件商品都经过多重人工实物查验,力求让交易更加安全放心</p>
                    </cell>
                    <cell >
                        
                    </cell>
                    </group>
                    <div style="padding: 15px;">
                        
                    <x-button @click.native="show13 = false" plain type="primary"> 关闭 </x-button>
                    </div>
                </popup>
            </div>
        </div>
        
    </div>
</template>
<script>
import { TransferDom, Popup, Group, Cell, XButton, XSwitch, Toast, XAddress, ChinaAddressData, Grid, GridItem, CellBox} from 'vux'

    export default{
        data(){
            return{
                show13:false,
                prom:[{
                    num:'1',
                    img_url:'../assets/images/gd_1.png'
                
                }
                ]
            }
        },
        directives: {
            TransferDom
        },
        components: {
            XButton,
            Group,
            XSwitch,
            Popup,
            Cell,
            Toast,
            XAddress,
            Grid,
            GridItem,
            CellBox
        }
    }
</script>
<style scoped>

</style>
