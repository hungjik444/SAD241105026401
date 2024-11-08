# hello
> Đây là một trích dẫn
***
![Diagram](http://www.plantuml.com/plantuml/png/encoded-diagram-text)
***
# Cơ sở dữ liệu quản lí lương nhân viên
![PlantText](https://www.planttext.com/api/plantuml/png/b5JHIW9157tVhvZ7XFO7H4GqA2YMGkdrCcsoCxHUpPsDf7g87Y8Yo3_Gf8S2mOUUTXzyMF4_vWlwXMP6CpDRzMdOkVVSS-RSmtx6mq8WQ5E4DTzoVHe4n6792y85JzwHN5c4sAIMzC0vpXAEmdmBLSgIicXozCn5Wuq7uovw89YCtrnrK6GWwabNzHqk52i_HGKcn5NNJ_ZTLJ5DfgUYMxOoreqrLPOooIZDvUX989hK5Vcy6UtBwBLLOhp2PJGKMvcPwDb8XyceZw0QubjroAZBePHyQ8uMgLwAAfwkvbs7Q5V6VGv78ONYU132w5antkFQ53OPjMNyI46xzJ1d_ZhS9HQsP7o7iC_gCkeXE9vUyLxIGMy31NhjW0RADFHN108Pjq4a7Gvd4v9DDPPt3g2eWHxu4oLJRrsreORPa_Wt92gXqu1kBuOnDO0cNFE1j-ryQc3JNCfTstPge5QZbwTaDIvjmt_UjypgxCHcWiPd8fYMJCv3QXLKElJFuGi00F__0m00)
***
# **Chèn 1 số link PlantText làm ví dụ**
![PlantText](https://www.planttext.com/api/plantuml/png/X94zJWCn48NxESLeAq1oGHkb24eA8b4X96fhTvGTnPvPURn4278o2ewKAyJBxeAG-Edyv6_UU_QStjvNbdtAVGm0jcV1f4O0cNCWlAVWCwjOovsXmtNmPhXXlqi-0a0zwWE5mBB35q34hMHyP6dqO8DyKcxmJklzGqiRrNHn2STvyAOhoP4aJ_fM-v8zdjSQOo-p6Wtdl683y9cwV7NbJjoNtQAKQ2bnzbBJ3-3a_H_sKUSNgBgkyChrdSCgUdckfeQBmRjJu-7N_g279tndOKNIb2sS0G00__y30000)
***
# **Ví dụ khác PlantText**
![PlantText](https://www.planttext.com/api/plantuml/png/Z5BBJiCm4BpxArPxJYMWSGASMWd12Iuv8TI3IrTj8V5QZYcAgduP1pw9Ny0sZoJ80dpnOyOpksE_lRpEMgUiUsXP2x4N06Y8JKq8vt3djs7iFsSFQjL42A-LVSGCUaIj8p0z7XxURrqNwJVq3BSShlIWsR0cx6t6Lf7YEXCOk65lcuqn_TGioGRqj2WdSdfqXWF28VjRjU7bjlv5jyWBa59ESbcK8-tlzKByS4j5DM-wL58dUJAf2z8xRp_CYLmRdmEmCkoy5buHMw_YLvUMLlYlCYf7EqeLKifa8PNICDThglchzu--5-8Wn8pqAloPTm000F__0m00)
***
# **Hướng dẫn sử dụng PlantText**
## 1. Cấu trúc Cơ Bản của PlantUML
### Mỗi sơ đồ trong PlantUML bắt đầu và kết thúc với @startuml và @enduml.
###
### @startuml
### // Nội dung sơ đồ ở đây
### @enduml
## 2. Sơ đồ Lớp (Class Diagram)
### Sơ đồ lớp thường sử dụng trong thiết kế đối tượng hướng đối tượng để mô tả các lớp và mối quan hệ của chúng.
###
### @startuml
### class Person {
    - String name
    - int age
    + setName(String name)
    + getName() : String
}
###
### class Student {
    - int studentID
    + getStudentID() : int
}

### Person <|-- Student
### @enduml

