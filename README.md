# calculator-password-and-qrcode
import prompt from "prompt"

import mainPrompt from "./prompts/prompt-main.js";
import creatQRCode from "./services/qr-code/creat.js";
import creatPassword from "./services/password/create.js";





async function main() {
     prompt.get(mainPrompt, async (err, choose) => {
         if(choose.select == 1) await creatQRCode();
         if(choose.select == 2) await creatPassword();
     }) 

     prompt.start();
}

main();
export { prompt, mainPrompt, creatQRCode
}
