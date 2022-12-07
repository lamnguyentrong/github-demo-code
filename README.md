1. git init: tạo repo trong local >> <git init>
2. git add: thêm file để chuẩn bị commit >> <git add tên_file>
3. git commit:
    * <git commit -m " ghi chú commit "> 
    * <git commit -a: để đưa các file đang được giám sát có sự thay đổi vào staging rồi tự động chạy git commit>
    * <git commit --amend: tạo ra commit mới thay thế cho commit cuối cùng >
4. git reset:
    * <git reset --soft HEAD~1: hủy commit cuối, con trỏ HEAD sẽ chuyển về commit cha. Đồng thời những thay đổi của commit cuối được chuyển vào vùng staging nhằm để có cơ hội commit lại hoặc sửa đổi>
    * <git reset --hard HEAD~1: giống với dùng tham số --soft, chỉ có một khác biết là nội dung thay đổi của commit cuối không đưa đưa vào staging mà bị hủy luôn>
    * <git reset: hủy git add>
    * <git reset -- filename:  hủy một file nào đó trong vùng staging chứ không phải toàn bộ >
5. git revert: 
    >> <git revert HEAD: hoàn tác lại commit vừa đổi gần nhất>
6. git stash: 
    >> <git stash save -u: loại bỏ những file không được theo dõi và cất nó vào trong repo>
    >> <git stash list: liệt kê danh sách các stashes mà bạn tạo ra, và cái gần nhất bạn tạo nó ở trên đầu đó>
    >> <git stash apply: lấy ra stash cuối cùng để apply vào code> <git stash apply stash@{1}: Lấy ra stash khác>
    >> <git stash pop: xóa stash cuối cùng> <git stash pop stash@{1}: xóa stash khác>
    >> <git stash show: hiển thi ra stash cuối cùng> <git stash show stash@{1}: hiển thi ra stash khác>
    >> <git stash branch branch-draff: tạo một branch mới với nhưng thay đổi tương ứng trong stash gần nhất của bạn và cũng xoá nó khỏi stash list như git stash pop.>
    >> <git stash branch branch-draff stash@{1}: tạo với một stash cụ thể thì thêm id vào sau tên branch mới>
    >> <git stash clear: xoá toàn bộ stash đang lưu trữ trong repo. nó có thể sẽ không revert lại được>
    >> <git stash drop: Xoá đi stash gần nhất, có thể không revert được> 
    >> <git stash drop stash@{1}: Xoá đi stash củ thể bằng việc thêm id vào, có thể không revert được>
7. git remote: 
    >> <git remote: liệt kê các liên kết sử dụng lệnh của repo>
    >> <git remote -v: liệt kê chi tiết hơn>
    >> <git remote add remote-name url: tạo liên kết>
    >> <git remote rm remote-name: Xóa 1 địa chỉ remote>
    >> <git remote rename ten-cu ten-moi: đổi tên địa chỉ remote>
    >> <git remote show remote-name: xem thông tin chi tiết về remote>
8. git push: >> <git push: đẩy commit từ local lên remote>
9. git pull: >> <git pull: cập nhật lại toàn bộ thay đổi từ remote về local>
10. git fetch: >> <git fetch: giống với git pull nhưng không cập nhật trạng thái hoạt động của local>
11. git branch & git checkout: rẽ nhánh và xử lý trong nhánh
    >> <git branch: xem các nhánh cục bộ> <git branch -r: xem các nhánh từ xa> <git branch -a: xem toàn bộ các nhánh>
    >> <git checkout -b my-branch-name: tạo và tùy chọn tên nhánh mới>
    >> <git checkout my-branch-name: chuyển đổi nhánh trong repo cục bộ>
    >> <git checkout --track origin/my-branch-name: chuyển đổi nhánh đến repo từ xa>
    >> <git push -u origin my-branch-name: đẩy đến nhánh nếu nhánh cục bộ không tồn tại từ xa>
    >> <git push origin --delete my-branch-name: xóa nhánh từ xa>
    >> <git branch -d my-branch-name: xóa nhánh cục bộ>
12. git merge: >> <git merge my-branch-name: sử dụng để gộp nhánh, gộp nhánh này vào nhánh khác. Khi gộp nhánh git thường căn cứ vào 3 commit, để tạo ra một commit gộp>
13. git rebase: >> <git rebase my-branch-name: cũng gộp các commit từ nhánh này vào nhánh khác, bằng cách xây dựng lại các commit base kế thừa từ nhánh khác và viết lại lịch sử commit sau các commit cơ sở mới.>
