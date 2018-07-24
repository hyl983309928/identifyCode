# identifyCode
一个生成验证码的VUE组件
# 使用方法示例

<SIdentify @click.native="createCode" :identifyCode="checkCode" :contentWidth="120" :contentHeight="40"></SIdentify>

checkCode的为你需要展示的code值

# 创建code的函数

        createCode () {
          let code = ''
          let random = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 'A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J', 'K', 'L', 'M', 'N', 'O', 'P', 'Q', 'R',
            'S', 'T', 'U', 'V', 'W', 'X', 'Y', 'Z']
          for (var i = 0; i < 4; i++) {
            var index = Math.floor(Math.random() * 36)
            code += random[index]
          }
          this.checkCode = code
        }
