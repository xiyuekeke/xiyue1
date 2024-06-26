# 什么是ABAC

基于属性的访问控制（Attribute-Based Access Control），是一种灵活的权限管理模型，它根据用户、资源和环境的属性来动态地授予或拒绝访问权限。通过动态计算一个或一组属性来判断是否满足某种条件来进行授权判断(可以编写简单的逻辑)。

比如：成绩大于35分的学生可以自由选择位置，成绩这一属性决定了是否有权限选择位置。

# ABAC属性分类
属性通常来说分为四类：
- 用户属性（如用户年龄 用户地址）
- 环境属性（比如当前时间）
- 操作属性（增、删、改、查）
- 对象属性（比如一篇文章，又称资源属性）

根据指定的属性去设置用户权限，
## ABAC优点
- **提供更精细的访问控制** 
		角色分配使用带有操作和数据操作的角色定义来向安全主体授予权限。 你可编写条件来对这些权限进行筛选，以提供更精细的访问控制。 还可将条件添加到特定操作。 例如，只有在 Blob 被标记为 Project=Blue 时，才能向 John 授予对订阅中的 Blob 的读取访问权限。
- **帮助减少角色分配的数量** 
		某些场景需要数千个角色分配。 必须对所有这些角色分配进行管理。 在这些场景中，你可添加条件来显著减少角色分配数量。
- **使用具有特定业务含义的属性** 
		通过条件，可在访问控制中使用具有特定业务含义的属性。 项目名称、软件开发阶段和分类级别就是这类属性。

# ABAC对比RBAC的优势

- 对于大型组织，基于RBCA的控制模型需要维护大量的角色和授权关系，相比而言，ABAC更加灵活；
- 对于中小型组织，维护角色和授权关系的工作量不大，反而定制各种策略相对麻烦，更容易接受RBAC授权模型。
- 新增资源时，ABAC仅需要维护较少的资源。而RBAC需要维护所有相关的角色。ABAC可扩展性更强、更方便。
- RBAC支持带有动态参数的授权规则，RBAC只能基于静态的参数进行判断。
- ABAC权限控制比RBAC更细。
