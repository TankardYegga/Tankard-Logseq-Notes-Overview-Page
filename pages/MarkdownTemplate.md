public:: true

-
- ### 0 欢迎使用 Cmd Markdown 编辑阅读器
  
  我们理解您需要更便捷更高效的工具记录思想，整理笔记、知识，并将其中承载的价值传播给他人，**Cmd Markdown** 是我们给出的答案 —— 我们为记录思想和分享知识提供更专业的工具。 您可以使用 Cmd Markdown：
  
  > * 整理知识，学习笔记
  > * 发布日记，杂文，所见所想
  > * 撰写发布技术文稿（代码支持）
  > * 撰写发布学术论文（LaTeX 公式支持）
  
  ![cmd-markdown-logo](https://www.zybuluo.com/static/img/logo.png)
- ### 1 制作一份待办事宜 [Todo 列表](https://www.zybuluo.com/mdeditor?url=https://www.zybuluo.com/static/editor/md-help.markdown#13-待办事宜-todo-列表)
  ```
  [ ] 支持以 PDF 格式导出文稿
  [ ] 改进 Cmd 渲染算法，使用局部渲染技术提高渲染效率
  [x] 新增 Todo 列表功能
  [x] 修复 LaTex 公式渲染问题
  [x] 新增 LaTex 公式编号功能
  ```
- ### 2 书写一个质能守恒公式[^LaTeX]
  
  $$E=mc^2$$
- ### 3 高亮一段代码[^code]
  
  ```python
  @requires_authorization
  class SomeClass:
  pass
  
  if __name__ == '__main__':
  # A comment
  print 'hello world'
  ```
- ### 4 高效绘制 [流程图](https://www.zybuluo.com/mdeditor?url=https://www.zybuluo.com/static/editor/md-help.markdown#7-流程图)
  
  ```flow
  st=>start: Start
  op=>operation: Your Operation
  cond=>condition: Yes or No?
  e=>end
  
  st->op->cond
  cond(yes)->e
  cond(no)->op
  ```
- ### 5 高效绘制 [序列图](https://www.zybuluo.com/mdeditor?url=https://www.zybuluo.com/static/editor/md-help.markdown#8-序列图)
  
  ```seq
  Alice->Bob: Hello Bob, how are you?
  Note right of Bob: Bob thinks
  Bob-->Alice: I am good thanks!
  ```
- ### 6 高效绘制 [甘特图](https://www.zybuluo.com/mdeditor?url=https://www.zybuluo.com/static/editor/md-help.markdown#9-甘特图)
  
  ```gantt
  title 项目开发流程
  section 项目确定
      需求分析       :a1, 2016-06-22, 3d
      可行性报告     :after a1, 5d
      概念验证       : 5d
  section 项目实施
      概要设计      :2016-07-05  , 5d
      详细设计      :2016-07-08, 10d
      编码          :2016-07-15, 10d
      测试          :2016-07-22, 5d
  section 发布验收
      发布: 2d
      验收: 3d
  ```
- ### 7 绘制表格
  
  | 项目        | 价格   |  数量  |
  | --------   | -----:  | :----:  |
  | 计算机     | \$1600 |   5     |
  | 手机        |   \$12   |   12   |
  | 管线        |    \$1    |  234  |
- ### 8 更详细语法说明
  ```
  想要查看更详细的语法说明，可以参考我们准备的 [Cmd Markdown 简明语法手册][1]，
  进阶用户可以参考 [Cmd Markdown 高阶语法手册][2] 了解更多高级功能。
  ```
- ### 9 不错的
  
         嘎嘎嘎嘎过
-