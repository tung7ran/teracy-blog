---
layout: post
title: "URIs tốt sẽ không bao giờ thay đổi"
author: phuonglm
date: 2016-11-11 11:33
comments: true
categories:
    - "vi"
    - "trans"
tags:
    - "uri"
    - "organization"
    - "management"
    - "document"
cover: /images/2016/11/11/broken.jpg
keywords: organization, management, document, URL rewrite

description: Một số sai lầm trong việc thiết kế và duy trì các URI trong các sản phẩm/tài liệu của bạn.
published: true
---
{% img center /images/2016/11/11/broken.jpg Việc thay đổi cấu trúc URI thường đem lại trải nghiệm không tốt cho người dùng. %}
Theo bạn URIs (đường dẫn) thế nào là tốt? Những URIs nào sẽ bị thay đổi theo thời gian? Đường dẫn không tự thay đổi chỉ có con người khiến nó thay đổi.
Theo lý thuyết thì không có lý do gì để mọi người thay đổi URI (hoặc là ngừng duy trì các tài liệu), nhưng thực tế thì lại có muôn vàn lý do mà dưới đây là một vài ví dụ.
<!-- more -->
* **Chúng tôi sắp xếp lại nội dung trang web để đem lại trải nghiệm tốt hơn.**

  Có phải như bạn cảm thấy không thể duy trì URIs cũ như hiện tại? Nếu vậy, bạn đã chọn quy tắc đặt URI thật tệ. Hãy suy nghĩ về những URI mới để bạn có thể giữ chúng tồn tại sau khi thiết kế lại lần tới nhé.

* **Chúng tôi có quá nhiều tài liệu đến mức không thể nào kiểm tra được cái nào đã cũ, cái nào là bí mật và hợp lệ và vì vậy chúng tôi nghĩ tốt hơn hết là thay đổi toàn bộ URIs để cấp phát lại từ đầu.**
  
  Hmm, có lẽ tôi có thể đồng cảm với việc này - W3C đã từng trải qua thời kỳ như vậy khi mà chúng tôi đã phải sàng lọc cẩn thận quyền truy cập của từng tại liệu trước khi cho phép nó được truy cập rộng rãi. Cách giải quyết là mọi tài liệu cần được hoạch định trước - hãy quy ước rõ và lưu trữ các thông tin của tài liệu đại loại như tài liệu được phân phối như thế nào, ngày tạo tài liệu và khi nào tài liệu đấy hết hiệu lực.

* **Uhm, chúng tôi thấy rằng chúng tôi phải chuyển các file đến thư mục khác.**
  
  Đây là một trong những lý do vụng về nhất. Có vẻ có nhiều người không biết rằng các máy chủ Web đều cho phép bạn tùy chỉnh rất linh hoạt mối quan hệ giữa đường dẫn và file thực tế được sử dụng trên hệ thống. Hãy nghĩ rằng URI là một tập các tên trừu tượng, được sắp xếp một cách gọn gàng sau đó hãy gán nó vào những file/ứng dụng cụ thể trong hệ thống của bạn và sau đó hãy cấu hình máy chủ web một tẹo để thể hiện việc gán ghép đấy.
  John không còn duy trì tài liệu này nữa, giờ thì chỉ Jane làm thôi.
  Hãy nghĩ lại đi, tại sao tên của John lại nằm trên URI? Nó nằm trong thư mục của John nên phải có John trên URI à?

* **Trước đây tôi dùng CGI script còn giờ thì chúng tôi chuyển sang dùng một chương trình khác.**

  Việc bạn cứ phải chạy theo cấu trúc URI của một kiểu chương trình/Framework này và rồi sau đó thay đổi nó chỉ vì bạn sử dụng một chương trình khác nghe thật là điên rồ. Ngoài ra việc bạn không cấu hình lại được URI cho phần mềm đấy còn để lộ thông tin về cách thức hoạt động của máy chủ của bạn cho người khác thấy (kiểu như bạn dùng máy chủ kiểu gì, phần mềm nào) và điều đó cũng hơi nguy hiểm đấy. Tóm lại là rất bất hợp lý nếu bạn thay đổi cơ chế hoạt động và tất cả các đường dẫn đều phải thay đổi dù nội dung của bạn không thay đổi gì.

  Lấy ví dụ cho điều này là trang thông tin khoa học quốc gia (Hoa kỳ).

    http://www.nsf.gov/cgi-bin/pubsys/browser/odbrowse.pl

  Đây là trang tìm kiếm tài liệu của trang thông tin khoa học, rõ ràng đây không có vẻ là URI được thiết kế cho việc tồn tại trong... vài năm! "cgi", "oldbrowse" và ".pl" đã để lộ cách thức làm việc của cơ chế bên dưới. Tuy nhiên URI của kết quả tìm kiếm của trang thông tin khoa học quốc gia thì ổn hơn rất nhiều.

    http://www.nsf.gov/pubs/1998/nsf9814/nsf9814.htm

  Với phần đầu là "pubs/1998" cho ta gợi ý để biết rằng đó là tài liệu cũ từ năm 1998, cho dù thêm 100 năm nữa vào năm 2098 tài liệu thì có thể khác nhưng URI dạng này vẫn sẽ hợp lệ và NSF cho dù vẫn lưu trữ tài liệu cũ thì vẫn sẽ không phải lúng túng về URI này.

* **Tôi không nghĩ rằng URLs sẽ phải cố định - chỉ có URNs mới cần cố định.**
  
  Đây có lẽ là một trong những tác dụng phụ tồi tệ nhất của các thảo luận URN. Một số người dường như nghĩ rằng các không gian tên có thể được kéo dài ra và rằng chúng có thể làm cho các link lỏng lẻo như họ muốn, và khi đó "URN sẽ xử lý được hết những điều này". Nếu bạn là một trong những người này thì tôi đã làm bạn vỡ mộng mất rồi.

  Hầu hết các chương trình URN mà tôi thấy nó giống như ID tác giả theo sau hoặc là ngày hoặc là một chuỗi ký tự bất kỳ mà bạn chọn, hoặc đơn giản chỉ là một chuỗi ký tự. Cái này trông giống như một HTTP URI. Nói cách khác, nếu bạn nghĩ tổ chức của bạn sẽ có thể tạo ra các URN tồn tại mãi mãi, rồi chứng minh điều đó bằng cách tạo ra ngay các URN và sử dụng chúng thay cho các HTTP URI. Sẽ Không có vấn đề gì về HTTP làm cho URI của bạn không ổn định cả, vì đó là tổ chức của bạn mà. Hãy thực hiện một cơ sở dữ liệu để ánh xạ được URN tài liệu vào trong tên file hiện tại, và cho phép máy chủ trang web của bạn sử dụng nó để lấy được các tập tin.
  Nếu bạn đã hiểu được điều này, và trừ khi bạn có tiền, thời gian và các địa chỉ liên hệ để thực hiện thiết kế phần mềm, thì khi đó bạn có thể đưa ra một số lý dó sau:

* **Chúng tôi muốn điều đó nhưng chúng tôi không có công cụ.**

  Tôi có thể hiểu và hoàn toàn đồng ý về lý do này. Bạn cần phải làm gì để máy chủ web luôn sử dụng một URI cố định và trả về đúng dữ liệu cho dù bạn có sử dụng hệ thống nào, lưu trữ ra sao tại bất kỳ thời điểm nào. Liệu bạn có cho rằng bạn có thể lưu URI ngay trong chính bản thân tài liệu như là một cách để đối chiếu và liên tục cập nhập cơ sở dữ liệu để khiến URI luôn đúng. Bạn sẽ muốn lưu trữ mối quan hệ giữa các phiên bản khác nhau và bản dịch của tài liệu đó. Ngoài ra bạn còn cần lữu trữ thông tin checksum để đảm bảo tính toàn vẹn của dữ liệu theo thời gian. Và như bạn thấy đấy, máy chủ web về cơ bản không phải là công cụ có thể cung cấp những điều đấy cho bạn. Khi bạn tạo một tài liệu mới, trình soạn thảo sẽ hỏi bạn URI thay vì nói cho bạn biết URI như thế nào.

  Bạn cũng cẩn có thể thay đổi được một vài thứ như ai là chủ sở hữu của tài liệu, quyền truy câp ra sao... mà không phải thay đổi gì về URI.

  Tại W3C chúng tôi sử dụng Jigedit (máy chủ Jigsaw dùng để chỉnh sửa tài liệu) để hỗ trợ việc theo dõi các phiên bản của tài liệu và chúng tôi đang thử nghiệm với các công cụ để tạo tài liệu. Nếu bạn là người viết công cụ, máy chủ thì hãy nhớ nhé.

# Tại sao tôi phải quan tâm

  Khi bạn thay đổi URI trang web của bạn, bạn sẽ không bao giờ biết được ai vẫn đang giữ URI cũ và khi một ai đó click vào URI nhưng nó không tồn tại thì thường họ sẽ mất niềm tin vào trang web đấy. Thiệt hại sẽ là hiển nhiên khi để người sử dụng phàn nàn về những đường link như thế.

# Vậy tôi phải bằt đầu từ đâu? Thiết kế URIs?

  Nếu bạn muốn URI của bạn sẽ vẫn đúng đắn sau 2 năm hay 200 năm tới, thì hãy suy nghĩ về nó thật kỹ. URIs thay đổi khi một vài thông tin trong bản thân nó thay đổi. Thiết kế URI như thế nào thật sự là rất quan trọng. Và việc đầu tiên là hay loại bỏ bớt các thông tin không cần thiết ra khỏi URI.

  Ngày khởi tạo của tài liệu là một tham số sẽ không bao giờ thay đổi và nó rất hữu ích cho việc phân loại truy nhập từ hệ thống mới hay hệ thống cũ. Về cơ bản đấy là khởi đầu tốt cho một thiết kế URI ổn định.

  Có một ngoại lệ ở đây chính là URI dùng cho "mới nhất" hay trang "nhất", ví dụ như URI ở dưới đây:

  http://www.pathfinder.com/money/moneydaily/latest/

  - **Cái gì nên bỏ ra khỏi URI**

    Hmm, ngoại trừ ngày tháng thì những phần khác chỉ tổ khiến mọi thứ rắc rối hơn thôi. Ví dụ:

    - **Sử dụng tên tác giả** - tác giả có thể thay đổi theo từng phiên bản của tài liệu, chỉ cần tác giả thay đổi thì URI của tài liệu xem như là đã không đúng nữa.
    - **Dùng tiêu đề của tài liệu** - Ban đầu thì có vẻ tốt nhưng dần dần nó sẽ bị thay đổi rất nhanh khi tài liệu được cập nhật.
    - **Trạng thái của tài liệu** - trạng thái của tài liệu không nên được thiết lập trong URI, URI của tài liệu mới nhất cần được cố định bất chấp tài liệu có trạng thái như thế nào đi nữa.
    - **Thông tin truy nhập** - Tại W3C, chúng tôi chia quyền truy cập trang web thành 3 mục chính, nội dung dành cho chúng tôi, nội dung dành cho các thành viên và những nội dung công cộng. Ban đầu sử dụng URI riêng cho từng quyền truy nhập có vẻ ổn nhưng khi chúng tôi chuyển tài liệu từ quyền truy nhập này sang truy nhập khác thì link cũ sẽ không còn tồn tại và gây nên lỗi. 
    - **Đuôi của file truy nhập** - Đây là lỗi thường gặp ".cgi" ".html" là những thứ sẽ thay đổi theo thời gian. Bạn có chắc là bạn sẽ vẫn dùng html hay cgi hay php trong 20 năm tới? Thay vì sử dụng tên file và đuôi của nó trực tiếp thì bạn có thể sử dụng các biện pháp như: Sử dụng database để lưu trữ file, dùng mod rewrite để thay đổi cấu trúc URL tự động, sử dụng mod_spelling của Apache để tự động điền đuôi file, sửa lỗi chính tả...
    - **Đường dẫn chỉ ổ đĩa** - !!? à vâng, nhưng tôi đã từng thấy rồi đấy thưa các bạn.

    Một URI đơn giản và tốt có thể ở dạng như sau:

    http://www.w3.org/1998/12/01/chairs

  - **Phân loại tài liệu theo từng đề mục:**

    Đây là một con dao 2 lưỡi mà đôi khi rất khó để tránh khỏi. Thường thì việc sử dụng đề mục trong URI khi bạn phân loại tài liệu dựa vào đặc tính tài liệu mà bạn đang làm việc. Các đặc tính sẽ dần thay đổi theo thời gian, ở W3C chúng tôi đang muốn đổi "MarkUp" thành "Markup" và rồi chúng tôi lại đổi thành "HTML", bạn thấy đấy, các khái niệm sẽ dần thay đổi theo thời gian. Ví dụ như liệu sau này chúng ta có còn sử dụng "Stylesheet", liệu có còn khái niệm "Lịch sử truy nhập" trong trình duyệt nữa không!? 

    Vận hành và quản lý trang web của một tổ chức là rất khó, mà thật ra tổ chức cái gì cũng vậy. Giải pháp trung hạn của bạn có thể sẽ trở thành trở ngại lớn trong dài hạn.

    Thêm vấn đề nữa của việc phân loại này là mỗi người sẽ có cách phân loại riêng của mình, sự liên kết giữa các khái niệm là không cố định theo từng cá nhân và nó sẽ tiềm ẩn nguy cơ rất lớn khi bạn phân loại theo mô hình cây như vậy. Tóm lại, nếu bạn phân loại theo chủ đề trong URI nghĩa là bạn đang sử dụng một kiểu phân loại như vậy và việc phân loại này sẽ bị thay đổi trong tương lai và điều đó sẽ khiến URI bị hỏng.

  - **Đừng quên cả việc thiết kế tên miền nữa nhé**

    Những lưu ý về URI ở trên không chỉ giới hạn trong phần địa chỉ mà còn trong cả tên miền. Nếu bạn có máy chủ riêng cho những thứ của bạn, hãy nhớ việc phân chia sử dụng subdomain sẽ tiềm ẩn nguy cơ khiến nhiều URI không còn tồn tại trong tương lai. Nhiều quản trị hệ thống cảm thấy thoải mái hơn khi phân chia mọi thứ theo domain con như kiểu "cgi.pathfinder.com", "lists.w3.org" nhưng hãy cẩn trọng và suy nghĩ thật kỹ khi sử dụng nhiều hơn một tên miền cho trang web của bạn. Vận dụng khéo léo việc tạo ra các trang chuyển hướng sẽ giúp bạn quản lý tốt hơn.
# Kết luận
  Thiết kế và sử dụng URIs nhất quán trong 2, 20 hay thậm chí 200 năm chắc chắn là không đơn giản. Tuy nhiên vì các đồng chí quản trị cứ hay đưa ra những quyết định khiến cho họ lâm vào rắc rối trong tương lai. Thường thì do họ sử dụng những công cụ có sẵn và công cụ đấy lại có tầm nhìn quá ngắn hạn và bản thân họ cũng không thấy được những vấn đề lớn trong tương lai khi các URI của họ bị thay đổi. Thông điệp ở đây là, hay cố gắng thiết kế URI làm sao cho dù mọi thứ thay đổi (công nghệ, hệ thống, con người, các tham số, thuộc tính) thì URI của bạn vẫn luôn cố định và tất nhiên là truy cập được :).

 Lược dịch từ: [Cool URIs don't change](https://www.w3.org/Provider/Style/URI.html)
