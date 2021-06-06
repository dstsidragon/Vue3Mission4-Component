https://vue3-course-api.hexschool.io/javascript/all.js?002
忘記密碼
forgetPassword() {
      const url = '/forgetPassword';
      const vm = this;
      axios.post(url, vm.user).then((response) => {
        // console.log(response);
        vm.data = response.data;
        if (!response.data.success) {
          vm.resMessage.status = 'danger';
          vm.resMessage.message = `錯誤: ${response.data.message || response.data.code}`;
        } else {
          vm.resMessage.status = 'success';
          vm.resMessage.message = response.data.message;
        }
      });
上傳圖片
axios.post(`${url}api/${path}/admin/upload`, formData)

.then(res => {

console.log(res);

})

      
#註冊元件
#資料用props  $emit 傳遞
#分頁元件  切換上下頁判斷當前頁面 去disable   動態生成分頁數
#將後台頁面 Modal 以及分頁改使用元件
#使用 import module 來引入元件（分頁元件）  import export default
#完成登入頁面-註冊功能
#圖片上傳功能
#LV3：套用兩個元件＋新增一個物件欄位 options，增加更多不同的設定，
例如：商品評價星級 / 或是完成圖片上傳（二擇一）
#使用ref



載入vue 透過es module

在js頁面 import { createApp } form 'vue3 cdn';  

BS5元件可以使用
new() 的方式產生