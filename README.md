# -auto.waitFor();
var Maid = require("./common/Maid.js");
var maid = new Maid("com.jingdong.app.mall");
var Unlock = require("./common/Unlock.js");
var unlock = new Unlock();
maid.before();
unlock.unlock();
maid.sleep(2);


maid.kill();
maid.sleep(2);
maid.shell("am broadcast -a com.jozein.xedgepro.PERFORM -e data 438302433402230373023294E64756E647B336F6D607F6E656E647D336F6D6E2A696E67646F6E676E2160707E2D616C6C6F236F6D6E2A696E67646F6E676E236F6D6D6F6E6E2A6462756163647642716D65677F627B6E216364796679647965637E2A4442556163647E4164796675634F6D6D6F6E61436479667964797B337F65727365624F657E64637D3534303522303335343522303739383522303635313B335E2A657D607445637D3A646275616364736F6D6D6F6E6B335E2D6F64657C656E616D656D3A444255616364734F6C6C6563647A444245616E637B335E2160707E616D656D3A444255616364734F6C6C6563647A444245616E637B335E207C6577696E6E416D656D3A444255616364734F6C6C6563647A444245616E637B335E207C6577696E605164786D3A6462756163647522364A444255616364734F6C6C6563647A444245616E637522364A444255616364734F6C6C6563647A444245616E637E2A6372657E646C656B396E2A657D6076427F6D6D313B335E207162716D6D35273245223230716765652232352331452232336F6C6C6563647A444245616E63784F6D6560516765652232352233452232337F65727365652232352331452232314070784F6D656522323522334522323472716E63707162756E64756E61626C65652232352331447275756527344B335E26756273796F6E6D343E273B335E2E6565646C4F67696E6D303B356E64602165747F6A637D25254435224145214345254835224135283630206020602");
waitForActivity("com.jingdong.common.jdreactFramework.activities.JDReactNativeCommonActivity");
maid.sleep(5);
if (className("android.widget.ImageView").depth(6).exists()) {
    maid.click(545, 1695); // 关闭瓜分京东弹窗
    maid.sleep(2);
}
maid.clickTextCenter("签到领京豆");
maid.sleep(2);
maid.kill();
maid.after();
