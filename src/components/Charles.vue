<template>
  <div>
    1,代理上之后，点击某一个网址，右键map local映射到本地的相应项目，就是访问本地的该网页了
    并且相对应的里面的内容(html里面链接的css，js)也会相应的映射到本地

    2,Charles 主要提供两种查看封包的视图，分别名为 “Structure” 和 “Sequence”。
      Structure 视图将网络请求按访问的域名分类。
      Sequence 视图将网络请求按访问的时间排序。

    3,方法一：在主界面的中部的 Filter 栏中填入需要过滤出来的关键字。例如我们的服务器的地址是：http://yuantiku.com , 那么只需要在 Filter 栏中填入 yuantiku 即可。
    方法二：在 Charles 的菜单栏选择 “Proxy”->”Recording Settings”，然后选择 Include 栏，选择添加一个项目，然后填入需要监控的协议，主机地址，端口号。这样就可以只截取目标网站的封包了。
    方法三：在想过滤的网络请求上右击，选择 “Focus”，之后在 Filter 一栏勾选上 Focussed 一项,这种方式可以临时性的，快速地过滤出一些没有通过关键字的一类网络请求。

    4,有些时候为了调试服务器的接口，我们需要反复尝试不同参数的网络请求。Charles 可以方便地提供网络请求的修改和重发功能。只需要在以往的网络请求上点击右键，选择 “Edit”，即可创建一个可编辑的网络请求。

    5,我们可以使用 Charles 的 Repeat 功能来简单地测试服务器的并发处理能力，方法如下。
    我们在想打压的网络请求上（POST 或 GET 请求均可）右击，然后选择 「Repeat
    Advanced」菜单项，接着我们就可以在弹出的对话框中，选择打压的并发线程数以及打压次数，确定之后，即可开始打压。一些写得很弱的投票网站，也可以用这个办法来快速投票。

    6,Charles 的 Map 功能分 Map Remote 和 Map Local 两种，顾名思义，Map Remote 是将指定的网络请求重定向到另一个网址请求地址，Map Local 是将指定的网络请求重定向到本地文件。
  </div>
</template>
<script>
  export default{
    data(){
      return {
        msg: 'hello vue'
      }
    },
    components: {}
  }
</script>
<style scoped>

</style>
