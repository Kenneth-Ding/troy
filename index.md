<!DOCTYPE html>
<html>

<head>
    <meta charset="utf-8">
    <title>特洛伊版個性測驗</title>
    <style>
        div {
            width : 33%;
            float: left;
        }
        div img {
            float: left;
            width: 400px;
            height: 400px;
        }
        h1 {
            text-align: center;
        }
        h1 p {
            float: right;
            height: 310px;
            width: 33%;
            text-align: left;
            font-size: 16px;
            font-weight: bold;
            overflow: scroll;
        }
    </style>
    <script>
        var playButton; 
        var message1;
        var showImg;
        var message;
        var answer;
        var question1;
        var question2;
        var question3;
        var radios;

        function startGame()    {
            message = "";
            answer = 0;
            for (var i = 0, length = question1.length; i < length; i++) {
                if (question1[i].checked) {
                    // alert(radios[i].value);
                    answer += Math.floor(question1[i].value);
                    // only one radio can be logically checked, don't check the rest
                    break;
                }
            }
            for (var i = 0, length = question2.length; i < length; i++) {
                if (question2[i].checked) {
                    answer += Math.floor(question2[i].value);
                    break;
                }
            }
            for (var i = 0, length = question3.length; i < length; i++) {
                if (question3[i].checked) {
                    answer += Math.floor(question3[i].value);
                    break;
                }
            }
            for (var i = 0, length = question4.length; i < length; i++) {
                if (question4[i].checked) {
                    answer += Math.floor(question4[i].value);
                    break;
                }
            }
            message += "測驗結果出爐！！！<br>";
            if (answer == 15) {
                message += "你的個性最接近阿基里斯";
                showImg.src = "images/1.jpg";
                message += "<p>阿基里斯是古希臘神話和文學中的英雄人物，參與了特洛伊戰爭，被稱為「希臘第一勇士」。<br>";
                message += "他是色薩利國王佩琉斯與海洋女神忒提斯的兒子，荷馬在《伊利亞德》中花了很大的篇幅對之進行描寫。他歷來以其勇氣，俊美和體力著稱。他對雅典娜和赫拉非常尊敬。<br>";
                message += "據埃斯庫羅斯的悲劇《被縛的普羅米修斯》以及其他神話記載，泰坦之子普羅米修斯被宙斯綁縛在高加索岩壁上的原因之一，是因為普羅米修斯掌握了一個足以危及宙斯統治的秘密。直到普羅米修斯被赫拉克勒斯所拯救，並與宙斯達成和解後，這個秘密才大白於天下：海中女神忒提斯的兒子必將遠遠勝過其父。其時宙斯正巧在追求忒提斯，得知預言後便作主將忒提斯許配給人間的英雄佩琉斯。結果生出的子嗣阿基里斯，其實力果然遠勝乃父。<br>";
                message += "在一出生之時其女神母親便將其捉住腳踝放入冥河斯堤克斯裡浸泡，但由於抓住的腳踝沒有沾水而使其成為日後的弱點，除去此處之外阿基里斯全身近乎刀槍不入，更是有著超越凡人的戰爭智慧與強大力量，只要祂出戰希臘聯軍在他的領導下就戰無不勝。<br>"
                message += "阿基里斯小時就在人馬喀戎那裡學到了草藥醫學與格鬥的技藝。他的父親在婚禮上得到兩匹神馬——克桑托斯和巴利俄斯。這兩匹神馬是西風神仄費羅斯的兒子。克桑托斯告訴阿基里斯，阿基里斯將於特洛伊陣亡。阿基里斯則回答道：這個我知道。後來一位厄里倪厄斯 ，即命運女神，使克桑托斯閉了嘴，免得它再泄漏天機。他母親知道兒子將死於特洛伊，即送他出國。後來預言家卡爾卡斯對阿伽門農兄弟說只有阿基里斯參加征討才能攻下特洛伊，於是奧德修斯就假扮商人找到了他並帶他去了特洛伊。";
            }
            if (answer <14 && answer > 8) {
                message += "你的個性最接近海倫";
                showImg.src = "images/7.jpg";
                message += "<p>海倫（古希臘語：Ἑλένη, Helénē，英語：Helen of Troy）是希臘神話中宙斯與勒達之女，被稱為「世上最美的女人」，她和特洛伊王子帕里斯私奔，引發了特洛伊戰爭。<br>";
                message += "希臘神話中的美女海倫，是宙斯的女兒，從鵝蛋中生出來，16歲時被迫嫁給斯巴達王莫內勞斯（Menelaos），為斯巴達王后。後來特洛伊王子赫克托爾和二王子帕里斯（Paris）到訪斯巴達，帕里斯把她拐去，帶回特洛伊。斯巴達王大怒，他向哥哥邁錫尼國王阿加門農求助，希臘聯軍組織一千艘的船艦出征，而引起著名的特洛伊戰爭。後世有人形容這場戰爭為「使千艘戰艦齊發的容貌，海倫的美引發了特洛伊戰爭。」海倫為自己引起的戰爭內疚不已，她走向特洛伊城上，俯望兩軍戰士，當數萬戰士望著她時，全看傻了，海倫美到兩軍戰士連戰都不想打，於是雙方休兵一天。十年後特洛伊陷落，希臘大軍從巨型木馬內部殺出，男的被屠盡，女人、小孩全變奴隸，莫內勞斯要取海倫性命，舉劍的手卻不忍下手，海倫重回了莫內勞斯的身邊。而特洛伊城則永遠的消失。希羅多德稱她是希臘世界最美麗的女人，古希臘盲詩人荷馬在《伊利亞特》（Iliad）中，描述海倫「白皙的手臂」、「飄飄的長袍」、「閃閃發光的面紗」。</p>";
            }
            if (answer < -12) {
                message += "你的個性最接近布里塞伊斯";
                showImg.src = "images/8.jpg";
                message += "<p>布里塞伊斯，希臘神話里布裡塞伊斯是阿伽門農和阿基里斯矛盾銳化的導火索。阿伽門農因為拒絕釋放阿波羅祭司的女兒克律塞伊斯而惹怒阿波羅，最後不得不釋放以平息阿波羅的忿怒。阿伽門農隨後蠻橫地將阿基里斯的女俘布里塞伊斯擄走作為補償。阿基里斯由此忿怒，短時間拒絕出戰。</p>";
            }
            if (answer < -8 && answer > -12) {
                message += "你的個性最接近大埃阿斯";
                showImg.src = "images/6.jpg";
                message += "<p>大埃阿斯 (古希臘語：Αἴας，轉寫：Aías)，希臘神話人物，忒拉蒙之子。特洛伊戰爭中，希臘軍的英雄之一，作戰勇猛，但有勇無謀。<br>";
                message += "《伊利亞特》中記述，在阿基里斯因憤怒而休戰的時候，他與特洛伊第一英雄赫克托耳決鬥。兩人互擲標槍，大埃阿斯使用的是包有七層牛皮的青銅盾牌，結果赫克托耳的長矛刺破其中六層；而大埃阿斯的長矛則穿透了赫克托耳的盾牌。兩人纏鬥到日落，最後握手言和並交換隨身物示友好。<br>";
                message += "阿基里斯死後，他成為希臘軍中最強的英雄，但頭腦卻不及奧德修斯，在爭奪阿基里斯甲冑的繼承權中落敗。大埃阿斯在憤怒中發狂，最終拔劍自殺</p>";
            }
            if (answer > -8 && answer < -4) {
                message += "你的個性最接近帕里斯";
                showImg.src = "images/5.jpg";
                message += "<p>帕里斯（古希臘語:Πάρις），原名亞歷山大（Ἀλέξανδρος），為荷馬史詩《伊利亞特》中的特洛伊王子。出生前因母親夢見火炬，其姊卡珊德拉預言其會為國家帶來災禍，出生後被丟棄山中，被一位牧羊人撫養，取名為帕里斯。中間經歷了金蘋果事件，在一次入城的機會中，被姊姊卡珊德拉認出，父母見他長相美好而欣喜，將他接回家中。後來因為愛上墨涅拉俄斯妻子海倫並將其帶回特洛伊而引發了長達十年之久的特洛伊戰爭。</p>";
            }
            if (answer > -4 && answer < 0) {
                message += "你的個性最接近墨涅拉俄斯";
                showImg.src = "images/4.jpg";
                message += "<p>墨涅拉俄斯（Μενέλαος）是希臘神話中斯巴達的國王。阿特柔斯之子，阿加門農之弟，海倫之夫。海倫被帕里斯拐走後，墨涅拉俄斯與阿加門農召集希臘境內幾乎所有的國王對特洛伊開戰。經歷十年苦戰，特洛伊淪陷，海倫被墨涅拉俄斯奪回。兩人育有一女赫耳彌俄涅，嫁給阿加門農之子俄瑞斯忒斯（Orestes）。</p>";
            }
            if (answer > 4 && answer < 8) {
                message += "你的個性最接近赫克托爾";
                showImg.src = "images/2.jpg";
                message += "<p>赫克托爾（希臘語：Έκτορας），普里阿摩斯的兒子，特洛伊王子，帕里斯的哥哥。他是特洛伊第一勇士，被稱為「特洛伊的城牆」，不但勇冠三軍，而且為人正直品格高尚，是古希臘傳說和文學中非常高大的英雄形象<br>。";
                message += "在史詩《伊里亞德》中，他在一開始反對為了帕里斯的私事而挑起與希臘軍隊的戰事。但是戰爭發生後，他義無反顧的率領特洛伊人與希臘的大軍作戰。<br>";
                message += "希臘第一勇士阿基里斯（希臘語：Ἀχιλλεύς）由於與統帥阿伽門農的個人矛盾而對戰事袖手旁觀後，希臘軍中無人能敵赫克托爾，屢戰屢敗。此後，阿基里斯的摯友帕特羅克洛斯穿上阿基里斯的盔甲假裝出戰，但是被赫克托爾殺死。阿基里斯勃然大怒，重新參戰，指名要與赫克托爾決鬥。<br>";
                message += "赫克托爾在決鬥中被阿基里斯殺死，他的屍體也被阿基里斯拖在戰車後面繞城，不讓特洛伊人安葬以泄其憤。赫克托爾的父親普里阿摩斯王冒險親自拜訪阿基里斯，才說服他把送還赫克托爾的屍體。雖然歷經數日，但是屍體由於眾神的保護，卻完好無損。<br>";
                message += "《伊里亞德》以赫克托爾的葬禮和對他的悼念而結束。<br>";
                message += "另外，赫克托爾和大埃阿斯的決鬥也是一個為人津津樂道的橋段。在兩人對戰之前，沒有任何一位決鬥者能擋下赫克托爾的長矛，大埃阿斯為此特別製作一面包了七層牛皮的青銅盾。對決中赫克托爾先投出長矛，將堅固的盾牌擊穿六層；大埃阿斯隨後擲矛，穿破赫克托爾的盾牌並傷害到他。但是負傷的赫克托爾依舊勇猛，兩人纏鬥到日落不分勝負，最後交換了防具以示敬意。</p>"
            }
            if (answer > 0 && answer < 4) {
                message += "你的個性最接近阿伽門農";
                showImg.src = "images/3.jpg";
                message += "<p>阿加曼農（希臘文：Ἀγαμέμνων；拉丁字母轉寫：Agamemnon，意為「堅定不移」或「人民的國王」），希臘邁錫尼國王，希臘諸王之王，阿特柔斯之子。<br>特洛伊戰爭中的阿開奧斯聯軍統帥。他的弟弟墨涅拉俄斯的妻子海倫被特洛伊的王子帕里斯拐走是戰爭的導火線，戰爭勝利後，他順利回到家鄉，然而他的妻子克呂泰涅斯特拉對於阿加曼農在出征時因得罪狩獵女神阿蒂蜜絲而以長女伊菲革涅亞獻祭之事懷恨在心，便與情人埃癸斯托斯一起謀害了他。</p>"
            }
            message1.innerHTML = message;
            // message = ""
            // message1.innerHTML = message;
        }
        function start()
        {
            question1 = document.getElementsByName('1');
            question2 = document.getElementsByName('2');
            question3 = document.getElementsByName('3');
            question4 = document.getElementsByName('4');
            showImg = document.getElementById( "showImg" );
            message1 = document.getElementById( "message1" );
            playButton = document.getElementById( "play" );
            playButton.addEventListener( "click", startGame, false );
        }
        window.addEventListener( "load", start, false );
    </script>
</head>

<body>
    <div>
        <p>
            <strong>你會為了榮譽而死嗎？</strong><br>

            <input name="1" type="radio" value="1" checked></label>
            <label>會
                <input name="1" type="radio" value="-1"></label>
            <label>不會
        </p>

        <p>
            <strong>你會為了愛情而奮不顧身嗎？</strong><br>

            <input name="2" type="radio" value="4" checked></label>
            <label>會
                <input name="2" type="radio" value="-4"></label>
            <label>不會
        </p>
        <p>
            <strong>你是否是個有勇無謀的人？</strong><br>

            <input name="3" type="radio" value="-8" checked></label>
            <label>是
                <input name="3" type="radio" value="8"></label>
            <label>不是
        </p>
        <p>
            <strong>你會為了名流千史而甘願赴死，或是安逸的度過一生？</strong><br>

            <input name="4" type="radio" value="2" checked></label>
            <label>名流千史
                <input name="4" type="radio" value="-2"></label>
            <label>安逸度過一生
        </p>
            <form action = "#">
                <input id = "play" type = "button" value = "Submit" style = "width:100px; font-weight: bold;">
             </form>
    </div>
    <div>
        <img id = "showImg" src = "images/0.jpg">
    </div>
        <h1 id = "message1">你的性格最接近誰呢？</h1>
</body>

</html>
