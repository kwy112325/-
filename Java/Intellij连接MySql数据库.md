- 编写连接程序
```
columnNames=new Vector();
        //设置列名
        columnNames.add("学号");
        columnNames.add("名字");
        columnNames.add("性别");
        columnNames.add("年龄");
        columnNames.add("籍贯");
        columnNames.add("系别");

        rowData=new Vector();
        Connection con=null;
        PreparedStatement pst=null;
        ResultSet rs=null;
        try {
            Class.forName("com.mysql.jdbc.Driver");
            con= DriverManager.getConnection("jdbc:mysql://localhost:3306/school","root","*******");
            pst=con.prepareStatement("select * from stu");
            rs=pst.executeQuery();
            while(rs.next()){
                Vector hang=new Vector();
                hang.add(rs.getString(1));
                hang.add(rs.getString(2));
                hang.add(rs.getString(3));
                hang.add(rs.getInt(4));
                hang.add(rs.getString(5));
                hang.add(rs.getString(6));

                //加入到rowData
                rowData.add(hang);

            }

        } catch (ClassNotFoundException e) {
            e.printStackTrace();
        } catch (SQLException e) {
            e.printStackTrace();
        }finally {
            try {
                if(rs!=null) rs.close();
                if(pst!=null) pst.close();
                if(con!=null) con.close();
            } catch (SQLException e) {
                e.printStackTrace();
            }
        }
```
- 配置连接数据库
>View->Tool Windows->DataBase->初步配置一下
- 引入驱动包
>File->Project Structure->Dependencies->+号，引入下载好的jar包

**道阻且长，且行且珍惜**
