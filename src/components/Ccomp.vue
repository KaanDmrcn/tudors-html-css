<template>
    <body class="global_body HomeBody menuAcik" data-language="tr" data-currency="try">

    <form method="post" action="./" id="formGlobal">

    <div id="footer" class="homeFooter">
<div class="footerTop">
<div id="divNewsLetter" class="newaslater">
<label>E-bültenimize kayıt olun!</label>
<div id="UpdatePanel1" class="newsletterContent">
<input type="text" class="newstext textbox" name="txtbxNewsletterMail" id="txtbxNewsletterMail" placeholder="E-posta adresinizi yazın...">
<a id="btnMailKaydet" href="javascript:void(0)" class="newsbutton button" onclick="saveNewsletter()">Gönder</a>
</div>
</div>
</div>
<div class="footerCenter">
<div class="footerCenter">
<div class="cookietudors" style="display: none;">Sizlere en iyi alışveriş deneyimini sunabilmek adına sitemizde çerezler(cookies) kullanmaktayız. Detaylı bilgi için lütfen <a href="https://www.tudors.com/kvkk">tıklayınız.</a>
<div class="kapatx">Anladım</div>
</div>
<div class="FooterTudors">
<div class="Social">
<div class="ticiContainer">
<ul>
<li><a href="https://www.facebook.com/TudorsTRY/" style=" max-width: 69%; "><img src="https://e7.pngegg.com/pngimages/968/121/png-clipart-mya-org-social-media-computer-icons-facebook-social-media-logo-social-media-marketing-thumbnail.png" style=" margin: 0px 5px -5px 0px; "> </a></li>
<li><a href="https://twitter.com/tudorsofficial"  style=" max-width: 69%; "><img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAOEAAADhCAMAAAAJbSJIAAAAh1BMVEX///8AAAAeHh7n5+fh4eHa2trw8PDd3d34+Pj09PTq6ur7+/u4uLixsbH19fW/v7/Q0NAXFxdeXl4qKipVVVWZmZnT09PHx8empqYlJSVPT084ODiKiop4eHhwcHCTk5NEREQxMTEQEBBoaGigoKCAgICFhYU/Pz9ISEg1NTUiIiITExNqamobQNRUAAAIGklEQVR4nO2deZ+qLBTHx7TMpXRs0VazfWbu+399T3tZIiCcI34evn/eMfF3FTgb8PWl0Wg0Go1Go9FoNBqNRqPR/G/x7Nj3e2f8IG536n4cuXStJDLe+Y5GYbfuJ5NCN9wNPuTdaC1ip+7nE8WaE+Vd+V2GdT+jCOGwXN6VQ8B8QzNVqgOz6TuTJR7LDePIWME+MhfmklXf5T3G1Bv6q9N1PsKTMzLi0XdmWT7mJNn5ojXS09OxZ7wCS99P5/7/1SNcMMfunkkFfSf2xXcbL+4X/BK6a2iscCVy9cBXhp9fqrs9PP9OeoUne2KCKLGzqirw9Jzt3K28IGcLHQgt2pefuvDSbs1RpngKzzHViRfEv+W5Xvdj4ggcfwsJNIzkchu7t/m4UURo0l1f/z5AkWiLCjSM6SiNsqI/kAQk1CtkCmwJCyQyIjU6fVzSsqAFdqpMg4wMSY26LxdNoCUyG6L8/BG/wNzk+w37oe7gBBpkH+vtv9UGFOgDCiTN9Sfervxuky8VxPyFE7glN9t+v3Y9hlL4D07gvKTZ3uflQFEDwG/03SJ3Xz/EIiMYxIvsw82EeYFuMsz1ykIrOAFQmIIJTF9a6fib079MXxueFP6o7LuuhilurRF4DjKdu636Oud11sU/W8qOxYJNhbc4nBOmj88x18s+htI7U7neFNQrPJ6tMDccRS9vapdrOST+diJ1YuSOO7GxCuJkccyPYcd8y2SFj/cvg25xd4fgPVoRl108ZwrDshBg6TOMd+ehVKExlWWIb5DkFQQyyhUaLTlfqksYseXz+bwUhaeBSca0AelU5CjwMMpGmiuZBDP1PSYGRZEtNmb4XSr6Gp0fcG0XCgM1NssvD4IOFVMj4hSbmi79h2cWQiFxnG6YElpn9LtbJVECKhXzMHwwxBIpDKuPOHNIZTfIDt+e/Sb/qsYaK6ea2Cn5xAqiGGT21RwOwCjpjbIUOH1CfKWVVtDoCWTTmBiUu0Gcd2vxl3N4gKH8M0PKE/EbxXNOe9wTSxjSIM0SD7g64o0F17jaBVVI9w3MSveNAnZTzgHMqBkZwwNUHAd+mAedDqRCUur+leoWRxT0a1dIzBq+IOKe/sxj+tcKqpCUu88hZnLM5mNKOAc0DLVkUcg36Rfws4vLpiQP0j3clTT85Cje0DpK2qROCWrTEArBZL/EK7Nlb1yo8rOGWx6MGRZ5wb5BlPrWu0zI9D3VorliyW31e7jYxrb7GIC2cm+foyS9nYPDS2Tm+xAt54kfjy1IH5811elkgA/xBzkfMuerWaKKSkIv/74DlP4ChyPQCR9qAIEjduTC+qlQ8HjjFlqCSCJ/XDGVJo42GdV/y3mxiJlaWRxJwh4Mh6/DbfMkbugKDWP6EnIRLjPHZsGi8OQUjMZ3kRZSqk8WxHzMg7tjc5jfnFi3WfMiPZb4EsFYT/e9tgtjhYNBD9x+JL6y6bJJUz/dpKkS8VaIAT2cSa02URv6dEiuTWwGDLFEp4nG6BOWGAZwbg8YFv8Xq1wJBpbkEFrJGQQtBoFf/bqfUgS63X2mWVZaHrZgaZM/U7YwVBdwvRU0jJl2uMUs0DBlR7+qliqoAGNWBjY1BApzNFhy5gmNAfsGSw21a9hmwwuMhcKqwVPU28zhlKfc1WlS4OLOikNgM4MZ9EBiDshyCSA4dw5o3rQ/4RPYQAOcf6kyxpIBmVRY4tqsef9YZfVno0Yb1kqhHP0mufvVVrd0m/MWWUqDC0FYvyOH6gvNmpJaE1gt2Az7jan2mUTYBCtcbL+HjvqdcUpXUY6Pt8dDNcS3CHLVtm8yGTtg2wuFE4ucniEJK1V1yFlL2zav02NeBo0KvQ6Kg3YKvcK1ArI3d7RSxXqk4CsMUz8e29aJ9jiM/WS0UC7RL7izo/r1NUIG21cTkt7CG3SpnogSH0hVL/aWsMea2qEMtgWV5ag91kg5k0XlYE2lCNsHCpcrzphWx9NR1wOWtc+hslka1uoSOpCrWkWQtxunp6bXJMnxvQC3Ja4ADDXdHKg4KUreZ1y9RbPMJV6sqDZlHKQfo+fhbarKBMBe+J5S1pscc+0NRyEvg6OEjYc+4GEGfGRgRzWpUp8BeMYjyr6cVGQaMx+ECqyalWdwF+LVnvc+gB8JFx/oTwHIL+TZPjf6SZ1LMti3ZxHBGdWWu4A4LqWQTlLPtyr/sBQy3Xj5hy7wn7TTGdhwgwVuXngoKbbGg9dOdkesTnms7eBxZ+xvd/B2OfLxr++Y4P7jDOnYUAI98C/1F/y4yTJMeO+4XoEJ/LTxU6dACyG8UWsfxAj5z9COX/4kzhAETuubJtooIcaNlERvFVycOo09si36wESqQwGJjDJgI+lbg5wQSifAin9nYAfZltHZosXbohoGUcdHTF+AxkULcQNMt76FE3N6YidD1PBThGqoWfdjZ/FAi6n1zSCN8EOHU+muhGOZTy4lz+PQT+aLKEMXd2Yk34zpqrQo5ghzYH2Y1S3shtCpfKV4ahSU7CAneSxbuoQpYHb3glVvpn4g8dRoInZ9GidYU2C7nuqn1gjRk7fwp46/LbIX0cEtK/nt1RCo6OM5gcOa3PgvL0Cp8lrU4sXfAQ/GTJJ6E2ZnfLgS78Ecxv7kxkwgvtbJAtuDL8VM5AZnZvOwhoQ8hW4ga5KcJvXmcsto9zZipReDaAttWQvj2cG+UrdcD3e9dm2lFLw4pj/iOBIi+5f6Zm3pIxGcsZ/sN6tBq5jJKtpt/bCR0jQajUaj0Wg0Go1Go9FoNJqq/AdK86j94X27jAAAAABJRU5ErkJggg==" style=" margin: 0px 5px -5px 0px; "> </a></li>
<li><a href="https://www.instagram.com/tudorsofficial/" style=" max-width: 69%; "><img src="https://www.tudors.com/Uploads/Images/asd/instagram-ikon.png?t=20210517173758" style=" margin: 0px 5px -5px 0px; "></a></li>
<li><a href="https://api.whatsapp.com/send?phone=908503338377" style=" max-width: 69%; " target="_blank"> <img src="https://img.icons8.com/pastel-glyph/2x/whatsapp--v2.png" style=" margin: 0px 5px -5px 0px; "></a></li>
<li><a href="https://tr.pinterest.com/Tudorsofficial/"  style=" max-width: 69%; "><img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAOEAAADhCAMAAAAJbSJIAAAAflBMVEUAAAD////29vZ9fX35+fn7+/s1NTXt7e3q6urm5ube3t7y8vIdHR3X19fn5+dWVlaTk5NnZ2cKCgqioqLMzMzFxcWysrIPDw+8vLxxcXErKytGRkYVFRU+Pj6np6eCgoJOTk6Kiop1dXWamponJydfX186OjpJSUkoKChpaWkd6T5gAAAKWElEQVR4nO2d6XqyOhSFqyI4ISpIcUJxqMf7v8Hj1BbdK5hhR8r3sP70T6V5S5I9Jn44s9a/rJnz0fz4t9WsCSuvmrD6qgmrr5qw+qoJq6+asPqqCauvmrD6qgmrr5qw+qoJq6+asPqqCauvmrD6qgmrr5qw+qoJq6+akFWT5WA/n8/ds84/9vvBcmL/j76LcLA6bNejME6m02l01nSaJHEajrL19nRYzC2SvoNwudmO4qjbbEA5/a6fhOtgYOmvWyccHEaJ77Ux3a+avWQXfNoYgGXCYyh8d/RldqPdin8INgmXrej1y3uCjDfco7BH6IaeEt23/DHvOCwRDo6xo8V3Y+TcdawQLoO0r813lpMwMtog3Oy6JnwXeemGazT8hMuRr7a9YPktpvGwE66mstbhhbx0zzIgbsK18QT9UTsKOEbESziIOSbojzpbhjGxEgY+J99ZTmbuyDESTlqvZmi77w27vbu6Q6//2mbujM0GI+GocItp9qIkzGbBaj64yl0EsyxMot6LjSk1ReQj3BUswWaUZgHcGvfBOvYLIdOl2bjYCEMxYDfdLgpC3MlxmxbM73ZoNjAuwlS4pHrZ5uVEW25GYsbmyGhkTIQ7EeBw+5/cE+Zr4Vztr02GxkM4EkxRT8n1SkQTvT8zGBsLYQtHEv3YVXvOrCdA9Bf6g+MgPAzxsNQ9kpXoNcb6lp+BcA49mXZ81HiWmwpWY6Y9PAbCBAJmemZskOE9q689T80JMzgg/ehujV/iVPd5xoQrtAg7JtmkEBI6unGGMWEERtM9GD0yhoi+ZkBsSojc7a5hPnCO/msNR9N7MyQ8gn3UM45bxzDT2tML+c0Il2DNtPU39qLHnpVqVajMCA/AX04NnvetBTSxei/RiHCQgmGwFJAyaPhHOi/RiHAD/NGN/uNy2kMPVcs9NSGcgFcoXoSf7sqVf784Y6Czh5kQrsB/GUcT8yC+bY9eepAza8sOIkw0kjYmhDsyAux4/DfLG7jpWOpNQrPf16igmhDSf3MyB7/2XGjrZDIbRoAIGxqhsAHhmP6Lkb+9IR5KU8piwoUYqw/TgHBK/n4E1hgybU2ZyUYff1ZXfZj6hAMySdG7mUDbHUk8f4Y+6KhvNfqELTKNemAVAoNyVvv0+vlz+En1xIE+IZ1FYJEc4DCl4tkJk0XUJtyT6denbuNSlDzrfL3+C3B+75QHqk14IBHOkP5SZpIBhfmfRHmg2oQ0y03/+FJYT5TJ1MMlLLNHPUqbkPocNLKfCXuGHInZNkIf9JUHqkv4SecQ/SWccDEi7CmPVJfwP+Kp9MnvoBSHKaG6ydcl/CKjp7ZiLW6MklmHkHCoHATrEm6IHaA+Kbb2V8lkjCFhRzmFoEt4IITEGu7hdn+TJ5Fygemo9xGOSQ6KxL4LmPa8qYvCrCfBKeApO6a6hCeSzCeVGJSI+5bMpo9j4PII22QLOBV0YMrEeTB88pRLWmyEHiFsiQGlyoHQ1rxvHRJCaqgEZbKL2hJpwQnMRb3PHhJCurIKCGXGOdH+5KPY9lIlQpkIYQk/+T6vjdhD+qcLCGXi2D385Ps87+CZsKOy00hYw48j/KR6sVuXkKbQCOFM2OQktZi28KPqlS1dQpcQUouP22wakllPXENUL07qEu6JS0YMwEYYPElVwbHPp94hwBcBk/a6ucjzHko1g+G+GsU+sg/OLAbZA1Dx7Sq5ChL8aFO9D0mbkHTM0hhf1LEo1UyJt1KQz3slbUIawBMTQCOsq2RiQ0H8q9MZpU24ITslSb24eLOIJLLBAr+7odEurE1ISy7Uq8G5tlAqPMCJSI1eJP26BbFXTeKLZShCpL+GFMDgUqos9yR9wi8yBv95o1uhsoW/kXk67lTQ6W0zqJCSaUpShJ9oMcVStgIvYbkJ/igDQupZPzctLcBm6khtFgHeht/dbfKyU6EFtouhRHFUNEmHOm1fJoTUZDmPjnEKxinouHnUAGahcKvHK5kQuvQVdfP+9ycap1QBUOAraB2eMepry4oHAdswpEZJe5Eu0uutNiIETksnt1NuwTKUGqWgaJVo9UGb9ZduiU1s5wjRm+jJLMMMAsrtwkRmhHvil+Ws/gA5bTJValq5u/1zyuiCpnF8rlMZVmZkNhpBCkuj4+si0179510vVxeE/egSmaQBblHxpAwplfF5i9MjR24moXxpW6K6jVNQGl0YN5mfCnpoe/J/nX/YcC9B6OLMQLu0MzPnvT33FsPfjQbHv69nqSBDp57svovj/OEq+vm355YhanOX2Glw9gIU0WXFcoZ0H95TGvnYD3ZPNvwXsdNJ0GSkuwrZTjqPk2ugkf7GbxPseXnFPo3o3omm/iUgXKfVB6dw6se5cSwFfQpxUcZT2NygdyDoKsZbI9xFPriZC86vF537+hIB9ko+6QyFe+0bRXka2kl2l2NyIN8aoWhPbDSmAud7JexklEvtCGSNsKBdKEI5QdER58tb1zkV/iNrhGLA85APz9vNfozzFhepXcxAZIsQnInKqR+O87uSu43F9/O1zS7+sEaYFRI2GsMkXI8XrusuTqN0WnT/YGx4t6ktQvGk+32RXf+iF3djTv/OHUOP0rsVkipSL/o+yRLhgulaOpNLTe6yRCg8aKEmuVJjsSwRgmXoqU/chONKWjuEE5pqaact2GwoVlv1Ah8sO4S0BH657AkfQRepOeK5ONkOIWDpHj8+Rc0ZSBo3FGHZIQS54Gh5uXdQls8JzTfRu+zcsgvc7ls+dyZ3u3AU8F3SboWQtGaeV9XdfXZfOzttn+Xe0m9ZIQTHgbwfy5b1Clej55td30NkhRA0tOXSnW4obFp0ejHr+7vIBuEANCU+lFVWuwT1nvrJqCK3zqMC51NZZTA+x0x+52pUnH6n60/T3XpTmW8OmNFl6NDy7dI9BofxaXYaH4Jg4dr68gcrhBl9heqHCNhkgRDdPMRxtZKmLBCivC6zBVCRBcKAhklNnVYfJlkgBEWn6A3fCSSSBUKQ7TZMCBqJnxDZ+xKXoQXCOXVXuhZcFWnxE4Jst1FlxVT8hPT6KLkDFrbET0ir250yl6EFQhriigqG7xE/IU1C7Uq0hjYICaD5ja1GYif8IoSw5Ps+sRPSrbTEuOIidsKM7KQm1/4ziJ2QBIdRmeb+wwLhs7Ew/YoRY7ETPmehOhve5yuLnfD5LIj6FXLMYid8NvilemzXAXETPpVeSkyy3WWbULPBnlGWCct/hfyEj/nucl3Sq9gJH9oRohKziN+yai0crm/aNJFVi6915pNb7IS5lH7ZPvdN7IS5bGnJYdNd7IS/jSYMXXccYif8SbXJ3S1vX/Yi4NJd7rvYCb8rT6Vm8vNiJ/w+SfIHvJmb2AndvzVHreVLO6WmuR9kh7Bp+L1knOIn7F6yT4bf4cspfsKzUzNlaEBnEz9h1uD51ncuWagB7/4UoI1eDCv9d/qydjrvz6gmrL5qwuqrJqy+asLqqyasvmrC6qsmrL5qwuqrJqy+asLqqyasvmrC6qsmrL5qwuqr+eHMWv+yZs7/qWx+dLHp7I4AAAAASUVORK5CYII=" style=" margin: 0px 5px -5px 0px; "> </a></li>
<li><a href="https://www.youtube.com/channel/UCIQacmxjrLQRUFVGfA-1pzw"  style=" max-width: 69%; "><img src="https://i.pinimg.com/originals/20/9b/d8/209bd859c265e7ffc4bfeb75877b23f7.png" style=" margin: 0px 5px -5px 0px; "> </a></li>
</ul>
<a href="https://www.instagram.com/tudorsofficial/" style=" max-width: 69%; ">
<p style=" font-size: 9px; margin-left: -5px; text-align: center; background: -webkit-linear-gradient(#f69988, #f00000); -webkit-background-clip: text; -webkit-text-fill-color: #e55287; ">Instagram sayfamıza ulaşıp DM'den canlı destek alabilirsiniz.</p>
</a></div>
</div>
<div class="FooterMiddle">
<div class="ticiContainer">
<div class="linkler">
<ul>
<li><a href="javascript:;"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">KURUMSAL </font></font></a>
<ul>
<li><a href="/Form/ceo-ya-yazin-12"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">CEO'ya yazın </font></font></a></li>
<li><a href="https://www.tudors.com/Form/franchising-form-11"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Franchising </font></font></a></li>
<li><a href="/kvkk"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Gizlilik&amp;Güvenlik</font></font></a></li>
<li><a href="/magazalarimiz.aspx"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Mağazalarımız</font></font></a></li>
<li><a href="/basinda-biz"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Medya</font></font></a></li>
<li><a href="/insan-kaynaklari"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Kariyer</font></font></a></li>
<li><a href="/kvkk"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Kişisel Verilerin Korunması</font></font></a></li>
</ul>
</li>
<li class="Menuicine"><a href="javascript:;"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">MÜŞTERİ HİZMETLERİ</font></font></a>
<ul>
<li><a href="/iletisim">İletişim</a></li>
<li><a href="/siparistakip.aspx">Sipariş takibi</a></li>
<li><a href="https://api.whatsapp.com/send?phone=908503338377" target="_blank">Whatsapp Destek</a></li>
</ul>
</li>
<li><a href="javascript:;"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">YARDIM </font></font></a>
<ul>
<li><a href="/sikca-sorulan-sorular">Sıkça Sorulan Sorular</a></li>
<li><a href="/iade-sartlari"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">İade ve Değişim </font></font></a></li>
<li><a href="/kapida-odeme"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Kapıda Ödeme</font></font></a></li>
<li><a href="/kargo-teslimat"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Teslimat</font></font></a></li>
<li><a href="/UyelikSozlesme.aspx"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Kullanım Koşulları</font></font></a></li>
</ul>
</li>
<li><a href="javascript:;"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">POLİTİKALAR </font></font></a>
<ul>
<li><a href="/kvkk"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">KVKK Aydınlatma Metinleri </font></font></a></li>
<li><a href="/kvkk"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Veri işleme ve koruma politikası </font></font></a></li>
<li><a href="/kvkk"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Çerez politikası</font></font></a></li>
</ul>
</li>
<li>
<div class="MusteriHizmet">
<div class="Mimg"><img alt="" src="/Uploads/Images/mimg.png?t=20210305104233"></div>
<div class="Mtext"><a href="#">MÜŞTERİ HİZMETLERİ</a></div>
<div class="Mtext"><br>
<a href="#">0212 599 86 86&nbsp;</a></div>
</div>
<div class="Magazalar" style=" margin-top: 19px; "><a href="/magazalarimiz.aspx"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Mağazalar </font></font></a></div>
</li>
</ul>
</div>
</div>
</div>
<div class="banksimg">
<div class="ticiContainer">
<div class="bankimgs"><img alt="" src="/Uploads/Images/bankimg.png"></div>
</div>
</div>
<div class="FTextAlan">
<div class="ticiContainer">
<div><strong style="color: rgb(0, 0, 0);"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">TUDORS</font></font></font></font></strong></div>
<div>&nbsp;</div>
<div style="color: rgb(0, 0, 0);">
<div><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">1998 yılında ana faaliyetlerine başlayan Tudors, kısa sürede perakende sektöründe önemli bir aktör haline geldi ve aslen İstanbul merkezli bir mağazayı Anadolu'ya doğru genişleterek, İstanbul'da da büyüyerek Türkiye'de gömlek pazarının liderliğine doğru oynadı.</font></font></div>
<div><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Son yıllarda, yerel bir başarı serisinin ardından, markaya uluslararası alanda artan bir ilgi ve Tudors'un kendisinin uluslararası olmaya olan ilgisi vardı.</font></font></div>
<div><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Sadece 2 yıl gibi çok kısa bir zaman diliminde, Tudors bayrağını 14'ten fazla ülkeye yerleştirmiş ve sürekli yenilenen bir seçkisiyle son derece güvenilir ve yenilikçi kalarak, dünyanın en başarılı gömlek markası olma hedefiyle aralıksız devam etmektedir. hedef tüketicinin taleplerini karşılama alışkanlığı ve modern bir perakende anlayışı.</font></font></div>
</div>
</div>
</div>
<div class="product-social-icon-wrapper">
<div class="PaylasTit"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">PAYLAŞ</font></font></div>
<ul>
<li><a class="product-social-icons" content="facebook" href="javascript:;"><i class="fa fa-facebook"></i> </a></li>
<li><a class="product-social-icons" content="twitter" href="javascript:;"><i class="fa fa-twitter"></i> </a></li>
<li><a class="product-social-icons" content="pinterest" href="javascript:;"><i class="fa fa-pinterest"></i> </a></li>
<li><a class="product-social-icons" content="googleplus" href="javascript:;"><i class="fa fa-google-plus"></i> </a></li>
</ul>
</div>
<ul>
<li class="mobilmenureklam">&nbsp;</li>
</ul>
</div>
</div>
<div class="nav-footer">
<div class="Area">
<div class="T">HESABIM</div>
<div class="Content">
<div class="item navCtrl">
<div class="column"><a class="Link" href="/Hesabim#/Hesabim-Anasayfa" title=""><i class="fal fa-user"></i> HESABIM</a></div>
<div class="column">
<div class="control"><a href="/Hesabim#/Hesabim-Anasayfa">Hesabım</a> <span class="Or"></span> <a href="/UyeCikis.ashx">Çıkış Yap</a></div>
</div>
</div>
<div class="item">
<div class="column"><a class="Link" href="/Hesabim#/IadeTaleplerim" title=""><i class="fal fa-undo-alt"></i> KOLAY İADE</a></div>
</div>
<div class="item">
<div class="column favCol"><a class="Link onCntl" datahref="/Hesabim#/Favorilerim" href="/Hesabim#/Favorilerim" title=""><i class="fal fa-heart"></i> FAVORİLERİM</a></div>
</div>
<div class="item">
<div class="column"><a class="Link onCntl" datahref="/Hesabim#/Siparislerim" href="/Hesabim#/Siparislerim" title=""><i class="fal fa-box"></i> SİPARİŞLERİM</a></div>
</div>
</div>
</div>
<div class="Area">
<div class="T">YARDIM</div>
<div class="Content">
<div class="item">
<div class="column"><a class="Link" href="/siparistakip.aspx#/Hesabim-Anasayfa" title=""><i class="fal fa-box"></i> SİPARİŞ TAKİBİ</a></div>
</div>
<div class="item">
<div class="column"><a class="Link" href="/magazalarimiz.aspx" title=""><i class="fal fa-map-marker-alt"></i> MAĞAZA ADRESİ</a></div>
</div>
<div class="item">
<div class="column"><a class="Link" href="/sikca-sorulan-sorular" title=""><i class="far fa-life-ring"></i> YARDIM</a></div>
</div>
</div>
</div>
<div class="Area">
<div class="T">BİZİ TAKİP ET</div>
<div class="Content">
<div class="social-list"><a class="social-link" href="https://www.instagram.com/tudorsofficial/" title=""><i class="fab fa-instagram"></i></a> <a class="social-link" href="https://www.facebook.com/TudorsTRY/" title=""><i class="fab fa-facebook-f"></i></a> <a class="social-link" href="https://twitter.com/tudorsofficial" title=""><i class="fab fa-twitter"></i></a> <a class="social-link" href="https://www.youtube.com/channel/UCIQacmxjrLQRUFVGfA-1pzw" title=""><i class="fab fa-youtube"></i></a></div>
</div>
</div>
</div>
</div>
</div>
    </form>
</body>




</template>


<script>



export default {
  
}
</script>



<style scoped>

/* vietnamese */
@font-face {
  font-family: 'Josefin Sans';
  font-style: italic;
  font-weight: 100;
  src: url(https://fonts.gstatic.com/s/josefinsans/v17/Qw3EZQNVED7rKGKxtqIqX5EUCEx1XHgciw.woff2) format('woff2');
  unicode-range: U+0102-0103, U+0110-0111, U+0128-0129, U+0168-0169, U+01A0-01A1, U+01AF-01B0, U+1EA0-1EF9, U+20AB;
}
/* latin-ext */
@font-face {
  font-family: 'Josefin Sans';
  font-style: italic;
  font-weight: 100;
  src: url(https://fonts.gstatic.com/s/josefinsans/v17/Qw3EZQNVED7rKGKxtqIqX5EUCEx0XHgciw.woff2) format('woff2');
  unicode-range: U+0100-024F, U+0259, U+1E00-1EFF, U+2020, U+20A0-20AB, U+20AD-20CF, U+2113, U+2C60-2C7F, U+A720-A7FF;
}
/* latin */
@font-face {
  font-family: 'Josefin Sans';
  font-style: italic;
  font-weight: 100;
  src: url(https://fonts.gstatic.com/s/josefinsans/v17/Qw3EZQNVED7rKGKxtqIqX5EUCEx6XHg.woff2) format('woff2');
  unicode-range: U+0000-00FF, U+0131, U+0152-0153, U+02BB-02BC, U+02C6, U+02DA, U+02DC, U+2000-206F, U+2074, U+20AC, U+2122, U+2191, U+2193, U+2212, U+2215, U+FEFF, U+FFFD;
}
/* vietnamese */
@font-face {
  font-family: 'Josefin Sans';
  font-style: italic;
  font-weight: 300;
  src: url(https://fonts.gstatic.com/s/josefinsans/v17/Qw3EZQNVED7rKGKxtqIqX5EUCEx1XHgciw.woff2) format('woff2');
  unicode-range: U+0102-0103, U+0110-0111, U+0128-0129, U+0168-0169, U+01A0-01A1, U+01AF-01B0, U+1EA0-1EF9, U+20AB;
}
/* latin-ext */
@font-face {
  font-family: 'Josefin Sans';
  font-style: italic;
  font-weight: 300;
  src: url(https://fonts.gstatic.com/s/josefinsans/v17/Qw3EZQNVED7rKGKxtqIqX5EUCEx0XHgciw.woff2) format('woff2');
  unicode-range: U+0100-024F, U+0259, U+1E00-1EFF, U+2020, U+20A0-20AB, U+20AD-20CF, U+2113, U+2C60-2C7F, U+A720-A7FF;
}
/* latin */
@font-face {
  font-family: 'Josefin Sans';
  font-style: italic;
  font-weight: 300;
  src: url(https://fonts.gstatic.com/s/josefinsans/v17/Qw3EZQNVED7rKGKxtqIqX5EUCEx6XHg.woff2) format('woff2');
  unicode-range: U+0000-00FF, U+0131, U+0152-0153, U+02BB-02BC, U+02C6, U+02DA, U+02DC, U+2000-206F, U+2074, U+20AC, U+2122, U+2191, U+2193, U+2212, U+2215, U+FEFF, U+FFFD;
}
/* vietnamese */
@font-face {
  font-family: 'Josefin Sans';
  font-style: italic;
  font-weight: 400;
  src: url(https://fonts.gstatic.com/s/josefinsans/v17/Qw3EZQNVED7rKGKxtqIqX5EUCEx1XHgciw.woff2) format('woff2');
  unicode-range: U+0102-0103, U+0110-0111, U+0128-0129, U+0168-0169, U+01A0-01A1, U+01AF-01B0, U+1EA0-1EF9, U+20AB;
}
/* latin-ext */
@font-face {
  font-family: 'Josefin Sans';
  font-style: italic;
  font-weight: 400;
  src: url(https://fonts.gstatic.com/s/josefinsans/v17/Qw3EZQNVED7rKGKxtqIqX5EUCEx0XHgciw.woff2) format('woff2');
  unicode-range: U+0100-024F, U+0259, U+1E00-1EFF, U+2020, U+20A0-20AB, U+20AD-20CF, U+2113, U+2C60-2C7F, U+A720-A7FF;
}
/* latin */
@font-face {
  font-family: 'Josefin Sans';
  font-style: italic;
  font-weight: 400;
  src: url(https://fonts.gstatic.com/s/josefinsans/v17/Qw3EZQNVED7rKGKxtqIqX5EUCEx6XHg.woff2) format('woff2');
  unicode-range: U+0000-00FF, U+0131, U+0152-0153, U+02BB-02BC, U+02C6, U+02DA, U+02DC, U+2000-206F, U+2074, U+20AC, U+2122, U+2191, U+2193, U+2212, U+2215, U+FEFF, U+FFFD;
}
/* vietnamese */
@font-face {
  font-family: 'Josefin Sans';
  font-style: italic;
  font-weight: 600;
  src: url(https://fonts.gstatic.com/s/josefinsans/v17/Qw3EZQNVED7rKGKxtqIqX5EUCEx1XHgciw.woff2) format('woff2');
  unicode-range: U+0102-0103, U+0110-0111, U+0128-0129, U+0168-0169, U+01A0-01A1, U+01AF-01B0, U+1EA0-1EF9, U+20AB;
}
/* latin-ext */
@font-face {
  font-family: 'Josefin Sans';
  font-style: italic;
  font-weight: 600;
  src: url(https://fonts.gstatic.com/s/josefinsans/v17/Qw3EZQNVED7rKGKxtqIqX5EUCEx0XHgciw.woff2) format('woff2');
  unicode-range: U+0100-024F, U+0259, U+1E00-1EFF, U+2020, U+20A0-20AB, U+20AD-20CF, U+2113, U+2C60-2C7F, U+A720-A7FF;
}
/* latin */
@font-face {
  font-family: 'Josefin Sans';
  font-style: italic;
  font-weight: 600;
  src: url(https://fonts.gstatic.com/s/josefinsans/v17/Qw3EZQNVED7rKGKxtqIqX5EUCEx6XHg.woff2) format('woff2');
  unicode-range: U+0000-00FF, U+0131, U+0152-0153, U+02BB-02BC, U+02C6, U+02DA, U+02DC, U+2000-206F, U+2074, U+20AC, U+2122, U+2191, U+2193, U+2212, U+2215, U+FEFF, U+FFFD;
}
/* vietnamese */
@font-face {
  font-family: 'Josefin Sans';
  font-style: italic;
  font-weight: 700;
  src: url(https://fonts.gstatic.com/s/josefinsans/v17/Qw3EZQNVED7rKGKxtqIqX5EUCEx1XHgciw.woff2) format('woff2');
  unicode-range: U+0102-0103, U+0110-0111, U+0128-0129, U+0168-0169, U+01A0-01A1, U+01AF-01B0, U+1EA0-1EF9, U+20AB;
}
/* latin-ext */
@font-face {
  font-family: 'Josefin Sans';
  font-style: italic;
  font-weight: 700;
  src: url(https://fonts.gstatic.com/s/josefinsans/v17/Qw3EZQNVED7rKGKxtqIqX5EUCEx0XHgciw.woff2) format('woff2');
  unicode-range: U+0100-024F, U+0259, U+1E00-1EFF, U+2020, U+20A0-20AB, U+20AD-20CF, U+2113, U+2C60-2C7F, U+A720-A7FF;
}
/* latin */
@font-face {
  font-family: 'Josefin Sans';
  font-style: italic;
  font-weight: 700;
  src: url(https://fonts.gstatic.com/s/josefinsans/v17/Qw3EZQNVED7rKGKxtqIqX5EUCEx6XHg.woff2) format('woff2');
  unicode-range: U+0000-00FF, U+0131, U+0152-0153, U+02BB-02BC, U+02C6, U+02DA, U+02DC, U+2000-206F, U+2074, U+20AC, U+2122, U+2191, U+2193, U+2212, U+2215, U+FEFF, U+FFFD;
}
/* vietnamese */
@font-face {
  font-family: 'Josefin Sans';
  font-style: normal;
  font-weight: 100;
  src: url(https://fonts.gstatic.com/s/josefinsans/v17/Qw3aZQNVED7rKGKxtqIqX5EUAnx4RHw.woff2) format('woff2');
  unicode-range: U+0102-0103, U+0110-0111, U+0128-0129, U+0168-0169, U+01A0-01A1, U+01AF-01B0, U+1EA0-1EF9, U+20AB;
}
/* latin-ext */
@font-face {
  font-family: 'Josefin Sans';
  font-style: normal;
  font-weight: 100;
  src: url(https://fonts.gstatic.com/s/josefinsans/v17/Qw3aZQNVED7rKGKxtqIqX5EUA3x4RHw.woff2) format('woff2');
  unicode-range: U+0100-024F, U+0259, U+1E00-1EFF, U+2020, U+20A0-20AB, U+20AD-20CF, U+2113, U+2C60-2C7F, U+A720-A7FF;
}
/* latin */
@font-face {
  font-family: 'Josefin Sans';
  font-style: normal;
  font-weight: 100;
  src: url(https://fonts.gstatic.com/s/josefinsans/v17/Qw3aZQNVED7rKGKxtqIqX5EUDXx4.woff2) format('woff2');
  unicode-range: U+0000-00FF, U+0131, U+0152-0153, U+02BB-02BC, U+02C6, U+02DA, U+02DC, U+2000-206F, U+2074, U+20AC, U+2122, U+2191, U+2193, U+2212, U+2215, U+FEFF, U+FFFD;
}
/* vietnamese */
@font-face {
  font-family: 'Josefin Sans';
  font-style: normal;
  font-weight: 300;
  src: url(https://fonts.gstatic.com/s/josefinsans/v17/Qw3aZQNVED7rKGKxtqIqX5EUAnx4RHw.woff2) format('woff2');
  unicode-range: U+0102-0103, U+0110-0111, U+0128-0129, U+0168-0169, U+01A0-01A1, U+01AF-01B0, U+1EA0-1EF9, U+20AB;
}
/* latin-ext */
@font-face {
  font-family: 'Josefin Sans';
  font-style: normal;
  font-weight: 300;
  src: url(https://fonts.gstatic.com/s/josefinsans/v17/Qw3aZQNVED7rKGKxtqIqX5EUA3x4RHw.woff2) format('woff2');
  unicode-range: U+0100-024F, U+0259, U+1E00-1EFF, U+2020, U+20A0-20AB, U+20AD-20CF, U+2113, U+2C60-2C7F, U+A720-A7FF;
}
/* latin */
@font-face {
  font-family: 'Josefin Sans';
  font-style: normal;
  font-weight: 300;
  src: url(https://fonts.gstatic.com/s/josefinsans/v17/Qw3aZQNVED7rKGKxtqIqX5EUDXx4.woff2) format('woff2');
  unicode-range: U+0000-00FF, U+0131, U+0152-0153, U+02BB-02BC, U+02C6, U+02DA, U+02DC, U+2000-206F, U+2074, U+20AC, U+2122, U+2191, U+2193, U+2212, U+2215, U+FEFF, U+FFFD;
}
/* vietnamese */
@font-face {
  font-family: 'Josefin Sans';
  font-style: normal;
  font-weight: 400;
  src: url(https://fonts.gstatic.com/s/josefinsans/v17/Qw3aZQNVED7rKGKxtqIqX5EUAnx4RHw.woff2) format('woff2');
  unicode-range: U+0102-0103, U+0110-0111, U+0128-0129, U+0168-0169, U+01A0-01A1, U+01AF-01B0, U+1EA0-1EF9, U+20AB;
}
/* latin-ext */
@font-face {
  font-family: 'Josefin Sans';
  font-style: normal;
  font-weight: 400;
  src: url(https://fonts.gstatic.com/s/josefinsans/v17/Qw3aZQNVED7rKGKxtqIqX5EUA3x4RHw.woff2) format('woff2');
  unicode-range: U+0100-024F, U+0259, U+1E00-1EFF, U+2020, U+20A0-20AB, U+20AD-20CF, U+2113, U+2C60-2C7F, U+A720-A7FF;
}
/* latin */
@font-face {
  font-family: 'Josefin Sans';
  font-style: normal;
  font-weight: 400;
  src: url(https://fonts.gstatic.com/s/josefinsans/v17/Qw3aZQNVED7rKGKxtqIqX5EUDXx4.woff2) format('woff2');
  unicode-range: U+0000-00FF, U+0131, U+0152-0153, U+02BB-02BC, U+02C6, U+02DA, U+02DC, U+2000-206F, U+2074, U+20AC, U+2122, U+2191, U+2193, U+2212, U+2215, U+FEFF, U+FFFD;
}
/* vietnamese */
@font-face {
  font-family: 'Josefin Sans';
  font-style: normal;
  font-weight: 600;
  src: url(https://fonts.gstatic.com/s/josefinsans/v17/Qw3aZQNVED7rKGKxtqIqX5EUAnx4RHw.woff2) format('woff2');
  unicode-range: U+0102-0103, U+0110-0111, U+0128-0129, U+0168-0169, U+01A0-01A1, U+01AF-01B0, U+1EA0-1EF9, U+20AB;
}
/* latin-ext */
@font-face {
  font-family: 'Josefin Sans';
  font-style: normal;
  font-weight: 600;
  src: url(https://fonts.gstatic.com/s/josefinsans/v17/Qw3aZQNVED7rKGKxtqIqX5EUA3x4RHw.woff2) format('woff2');
  unicode-range: U+0100-024F, U+0259, U+1E00-1EFF, U+2020, U+20A0-20AB, U+20AD-20CF, U+2113, U+2C60-2C7F, U+A720-A7FF;
}
/* latin */
@font-face {
  font-family: 'Josefin Sans';
  font-style: normal;
  font-weight: 600;
  src: url(https://fonts.gstatic.com/s/josefinsans/v17/Qw3aZQNVED7rKGKxtqIqX5EUDXx4.woff2) format('woff2');
  unicode-range: U+0000-00FF, U+0131, U+0152-0153, U+02BB-02BC, U+02C6, U+02DA, U+02DC, U+2000-206F, U+2074, U+20AC, U+2122, U+2191, U+2193, U+2212, U+2215, U+FEFF, U+FFFD;
}
/* vietnamese */
@font-face {
  font-family: 'Josefin Sans';
  font-style: normal;
  font-weight: 700;
  src: url(https://fonts.gstatic.com/s/josefinsans/v17/Qw3aZQNVED7rKGKxtqIqX5EUAnx4RHw.woff2) format('woff2');
  unicode-range: U+0102-0103, U+0110-0111, U+0128-0129, U+0168-0169, U+01A0-01A1, U+01AF-01B0, U+1EA0-1EF9, U+20AB;
}
/* latin-ext */
@font-face {
  font-family: 'Josefin Sans';
  font-style: normal;
  font-weight: 700;
  src: url(https://fonts.gstatic.com/s/josefinsans/v17/Qw3aZQNVED7rKGKxtqIqX5EUA3x4RHw.woff2) format('woff2');
  unicode-range: U+0100-024F, U+0259, U+1E00-1EFF, U+2020, U+20A0-20AB, U+20AD-20CF, U+2113, U+2C60-2C7F, U+A720-A7FF;
}
/* latin */
@font-face {
  font-family: 'Josefin Sans';
  font-style: normal;
  font-weight: 700;
  src: url(https://fonts.gstatic.com/s/josefinsans/v17/Qw3aZQNVED7rKGKxtqIqX5EUDXx4.woff2) format('woff2');
  unicode-range: U+0000-00FF, U+0131, U+0152-0153, U+02BB-02BC, U+02C6, U+02DA, U+02DC, U+2000-206F, U+2074, U+20AC, U+2122, U+2191, U+2193, U+2212, U+2215, U+FEFF, U+FFFD;
}



.fa,.fab,.fal,.far,.fas {
    -moz-osx-font-smoothing: grayscale;
    -webkit-font-smoothing: antialiased;
    display: inline-block;
    font-style: normal;
    font-variant: normal;
    text-rendering: auto;
    line-height: 1
}

.fa-lg {
    font-size: 1.33333em;
    line-height: .75em;
    vertical-align: -.0667em
}

.fa-xs {
    font-size: .75em
}

.fa-sm {
    font-size: .875em
}

.fa-1x {
    font-size: 1em
}

.fa-2x {
    font-size: 2em
}

.fa-3x {
    font-size: 3em
}

.fa-4x {
    font-size: 4em
}

.fa-5x {
    font-size: 5em
}

.fa-6x {
    font-size: 6em
}

.fa-7x {
    font-size: 7em
}

.fa-8x {
    font-size: 8em
}

.fa-9x {
    font-size: 9em
}

.fa-10x {
    font-size: 10em
}

.fa-fw {
    text-align: center;
    width: 1.25em
}

.fa-ul {
    list-style-type: none;
    margin-left: 2.5em;
    padding-left: 0
}

.fa-ul>li {
    position: relative
}

.fa-li {
    left: -2em;
    position: absolute;
    text-align: center;
    width: 2em;
    line-height: inherit
}

.fa-border {
    border: .08em solid #eee;
    border-radius: .1em;
    padding: .2em .25em .15em
}

.fa-pull-left {
    float: left
}

.fa-pull-right {
    float: right
}

.fa.fa-pull-left,.fab.fa-pull-left,.fal.fa-pull-left,.far.fa-pull-left,.fas.fa-pull-left {
    margin-right: .3em
}

.fa.fa-pull-right,.fab.fa-pull-right,.fal.fa-pull-right,.far.fa-pull-right,.fas.fa-pull-right {
    margin-left: .3em
}

.fa-spin {
    animation: a 2s infinite linear
}

.fa-pulse {
    animation: a 1s infinite steps(8)
}

@keyframes a {
    0% {
        transform: rotate(0deg)
    }

    to {
        transform: rotate(1turn)
    }
}

.fa-rotate-90 {
    transform: rotate(90deg)
}

.fa-rotate-180 {
    transform: rotate(180deg)
}

.fa-rotate-270 {
    transform: rotate(270deg)
}

.fa-flip-horizontal {
    transform: scaleX(-1)
}

.fa-flip-vertical {
    transform: scaleY(-1)
}



.fa-flip-horizontal.fa-flip-vertical {
    transform: scale(-1)
}

:root .fa-flip-horizontal,:root .fa-flip-vertical,:root .fa-rotate-90,:root .fa-rotate-180,:root .fa-rotate-270 {
    -webkit-filter: none;
    filter: none
}

.fa-stack {
    display: inline-block;
    height: 2em;
    line-height: 2em;
    position: relative;
    vertical-align: middle;
    width: 2em
}

.fa-stack-1x,.fa-stack-2x {
    left: 0;
    position: absolute;
    text-align: center;
    width: 100%
}

.fa-stack-1x {
    line-height: inherit
}

.fa-stack-2x {
    font-size: 2em
}

.fa-inverse {
    color: #fff
}

.fa-500px:before {
    content: "\f26e"
}

.fa-accessible-icon:before {
    content: "\f368"
}

.fa-accusoft:before {
    content: "\f369"
}

.fa-address-book:before {
    content: "\f2b9"
}

.fa-address-card:before {
    content: "\f2bb"
}

.fa-adjust:before {
    content: "\f042"
}

.fa-adn:before {
    content: "\f170"
}

.fa-adversal:before {
    content: "\f36a"
}

.fa-affiliatetheme:before {
    content: "\f36b"
}

.fa-alarm-clock:before {
    content: "\f34e"
}

.fa-algolia:before {
    content: "\f36c"
}

.fa-align-center:before {
    content: "\f037"
}

.fa-align-justify:before {
    content: "\f039"
}

.fa-align-left:before {
    content: "\f036"
}

.fa-align-right:before {
    content: "\f038"
}

.fa-allergies:before {
    content: "\f461"
}

.fa-amazon:before {
    content: "\f270"
}

.fa-amazon-pay:before {
    content: "\f42c"
}

.fa-ambulance:before {
    content: "\f0f9"
}

.fa-american-sign-language-interpreting:before {
    content: "\f2a3"
}

.fa-amilia:before {
    content: "\f36d"
}

.fa-anchor:before {
    content: "\f13d"
}

.fa-android:before {
    content: "\f17b"
}

.fa-angellist:before {
    content: "\f209"
}

.fa-angle-double-down:before {
    content: "\f103"
}

.fa-angle-double-left:before {
    content: "\f100"
}

.fa-angle-double-right:before {
    content: "\f101"
}

.fa-angle-double-up:before {
    content: "\f102"
}

.fa-angle-down:before {
    content: "\f107"
}

.fa-angle-left:before {
    content: "\f104"
}

.fa-angle-right:before {
    content: "\f105"
}

.fa-angle-up:before {
    content: "\f106"
}

.fa-angrycreative:before {
    content: "\f36e"
}

.fa-angular:before {
    content: "\f420"
}

.fa-app-store:before {
    content: "\f36f"
}

.fa-app-store-ios:before {
    content: "\f370"
}

.fa-apper:before {
    content: "\f371"
}

.fa-apple:before {
    content: "\f179"
}

.fa-apple-pay:before {
    content: "\f415"
}

.fa-archive:before {
    content: "\f187"
}

.fa-arrow-alt-circle-down:before {
    content: "\f358"
}

.fa-arrow-alt-circle-left:before {
    content: "\f359"
}

.fa-arrow-alt-circle-right:before {
    content: "\f35a"
}

.fa-arrow-alt-circle-up:before {
    content: "\f35b"
}

.fa-arrow-alt-down:before {
    content: "\f354"
}

.fa-arrow-alt-from-bottom:before {
    content: "\f346"
}

.fa-arrow-alt-from-left:before {
    content: "\f347"
}

.fa-arrow-alt-from-right:before {
    content: "\f348"
}

.fa-arrow-alt-from-top:before {
    content: "\f349"
}

.fa-arrow-alt-left:before {
    content: "\f355"
}

.fa-arrow-alt-right:before {
    content: "\f356"
}

.fa-arrow-alt-square-down:before {
    content: "\f350"
}

.fa-arrow-alt-square-left:before {
    content: "\f351"
}

.fa-arrow-alt-square-right:before {
    content: "\f352"
}

.fa-arrow-alt-square-up:before {
    content: "\f353"
}

.fa-arrow-alt-to-bottom:before {
    content: "\f34a"
}

.fa-arrow-alt-to-left:before {
    content: "\f34b"
}

.fa-arrow-alt-to-right:before {
    content: "\f34c"
}

.fa-arrow-alt-to-top:before {
    content: "\f34d"
}

.fa-arrow-alt-up:before {
    content: "\f357"
}

.fa-arrow-circle-down:before {
    content: "\f0ab"
}

.fa-arrow-circle-left:before {
    content: "\f0a8"
}

.fa-arrow-circle-right:before {
    content: "\f0a9"
}

.fa-arrow-circle-up:before {
    content: "\f0aa"
}

.fa-arrow-down:before {
    content: "\f063"
}

.fa-arrow-from-bottom:before {
    content: "\f342"
}

.fa-arrow-from-left:before {
    content: "\f343"
}

.fa-arrow-from-right:before {
    content: "\f344"
}

.fa-arrow-from-top:before {
    content: "\f345"
}

.fa-arrow-left:before {
    content: "\f060"
}

.fa-arrow-right:before {
    content: "\f061"
}

.fa-arrow-square-down:before {
    content: "\f339"
}

.fa-arrow-square-left:before {
    content: "\f33a"
}

.fa-arrow-square-right:before {
    content: "\f33b"
}

.fa-arrow-square-up:before {
    content: "\f33c"
}

.fa-arrow-to-bottom:before {
    content: "\f33d"
}

.fa-arrow-to-left:before {
    content: "\f33e"
}

.fa-arrow-to-right:before {
    content: "\f340"
}

.fa-arrow-to-top:before {
    content: "\f341"
}

.fa-arrow-up:before {
    content: "\f062"
}

.fa-arrows:before {
    content: "\f047"
}

.fa-arrows-alt:before {
    content: "\f0b2"
}

.fa-arrows-alt-h:before {
    content: "\f337"
}

.fa-arrows-alt-v:before {
    content: "\f338"
}

.fa-arrows-h:before {
    content: "\f07e"
}

.fa-arrows-v:before {
    content: "\f07d"
}

.fa-assistive-listening-systems:before {
    content: "\f2a2"
}

.fa-asterisk:before {
    content: "\f069"
}

.fa-asymmetrik:before {
    content: "\f372"
}

.fa-at:before {
    content: "\f1fa"
}

.fa-audible:before {
    content: "\f373"
}

.fa-audio-description:before {
    content: "\f29e"
}

.fa-autoprefixer:before {
    content: "\f41c"
}

.fa-avianex:before {
    content: "\f374"
}

.fa-aviato:before {
    content: "\f421"
}

.fa-aws:before {
    content: "\f375"
}

.fa-backward:before {
    content: "\f04a"
}

.fa-badge:before {
    content: "\f335"
}

.fa-badge-check:before {
    content: "\f336"
}

.fa-balance-scale:before {
    content: "\f24e"
}

.fa-ban:before {
    content: "\f05e"
}

.fa-band-aid:before {
    content: "\f462"
}

.fa-bandcamp:before {
    content: "\f2d5"
}

.fa-barcode:before {
    content: "\f02a"
}

.fa-barcode-alt:before {
    content: "\f463"
}

.fa-barcode-read:before {
    content: "\f464"
}

.fa-barcode-scan:before {
    content: "\f465"
}

.fa-bars:before {
    content: "\f0c9"
}

.fa-baseball:before {
    content: "\f432"
}

.fa-baseball-ball:before {
    content: "\f433"
}

.fa-basketball-ball:before {
    content: "\f434"
}

.fa-basketball-hoop:before {
    content: "\f435"
}

.fa-bath:before {
    content: "\f2cd"
}

.fa-battery-bolt:before {
    content: "\f376"
}

.fa-battery-empty:before {
    content: "\f244"
}

.fa-battery-full:before {
    content: "\f240"
}

.fa-battery-half:before {
    content: "\f242"
}

.fa-battery-quarter:before {
    content: "\f243"
}

.fa-battery-slash:before {
    content: "\f377"
}

.fa-battery-three-quarters:before {
    content: "\f241"
}

.fa-bed:before {
    content: "\f236"
}

.fa-beer:before {
    content: "\f0fc"
}

.fa-behance:before {
    content: "\f1b4"
}

.fa-behance-square:before {
    content: "\f1b5"
}

.fa-bell:before {
    content: "\f0f3"
}

.fa-bell-slash:before {
    content: "\f1f6"
}

.fa-bicycle:before {
    content: "\f206"
}

.fa-bimobject:before {
    content: "\f378"
}

.fa-binoculars:before {
    content: "\f1e5"
}

.fa-birthday-cake:before {
    content: "\f1fd"
}

.fa-bitbucket:before {
    content: "\f171"
}

.fa-bitcoin:before {
    content: "\f379"
}

.fa-bity:before {
    content: "\f37a"
}

.fa-black-tie:before {
    content: "\f27e"
}

.fa-blackberry:before {
    content: "\f37b"
}

.fa-blanket:before {
    content: "\f498"
}

.fa-blind:before {
    content: "\f29d"
}

.fa-blogger:before {
    content: "\f37c"
}

.fa-blogger-b:before {
    content: "\f37d"
}

.fa-bluetooth:before {
    content: "\f293"
}

.fa-bluetooth-b:before {
    content: "\f294"
}

.fa-bold:before {
    content: "\f032"
}

.fa-bolt:before {
    content: "\f0e7"
}

.fa-bomb:before {
    content: "\f1e2"
}

.fa-book:before {
    content: "\f02d"
}

.fa-book-heart:before {
    content: "\f499"
}

.fa-bookmark:before {
    content: "\f02e"
}

.fa-bowling-ball:before {
    content: "\f436"
}

.fa-bowling-pins:before {
    content: "\f437"
}

.fa-box:before {
    content: "\f466"
}

.fa-box-alt:before {
    content: "\f49a"
}

.fa-box-check:before {
    content: "\f467"
}

.fa-box-fragile:before {
    content: "\f49b"
}

.fa-box-full:before {
    content: "\f49c"
}

.fa-box-heart:before {
    content: "\f49d"
}

.fa-box-open:before {
    content: "\f49e"
}

.fa-box-up:before {
    content: "\f49f"
}

.fa-box-usd:before {
    content: "\f4a0"
}

.fa-boxes:before {
    content: "\f468"
}

.fa-boxes-alt:before {
    content: "\f4a1"
}

.fa-boxing-glove:before {
    content: "\f438"
}

.fa-braille:before {
    content: "\f2a1"
}

.fa-briefcase:before {
    content: "\f0b1"
}

.fa-briefcase-medical:before {
    content: "\f469"
}

.fa-browser:before {
    content: "\f37e"
}

.fa-btc:before {
    content: "\f15a"
}

.fa-bug:before {
    content: "\f188"
}

.fa-building:before {
    content: "\f1ad"
}

.fa-bullhorn:before {
    content: "\f0a1"
}

.fa-bullseye:before {
    content: "\f140"
}

.fa-burn:before {
    content: "\f46a"
}

.fa-buromobelexperte:before {
    content: "\f37f"
}

.fa-bus:before {
    content: "\f207"
}

.fa-buysellads:before {
    content: "\f20d"
}

.fa-calculator:before {
    content: "\f1ec"
}

.fa-calendar:before {
    content: "\f133"
}

.fa-calendar-alt:before {
    content: "\f073"
}

.fa-calendar-check:before {
    content: "\f274"
}

.fa-calendar-edit:before {
    content: "\f333"
}

.fa-calendar-exclamation:before {
    content: "\f334"
}

.fa-calendar-minus:before {
    content: "\f272"
}

.fa-calendar-plus:before {
    content: "\f271"
}

.fa-calendar-times:before {
    content: "\f273"
}

.fa-camera:before {
    content: "\f030"
}

.fa-camera-alt:before {
    content: "\f332"
}

.fa-camera-retro:before {
    content: "\f083"
}

.fa-capsules:before {
    content: "\f46b"
}

.fa-car:before {
    content: "\f1b9"
}

.fa-caret-circle-down:before {
    content: "\f32d"
}

.fa-caret-circle-left:before {
    content: "\f32e"
}

.fa-caret-circle-right:before {
    content: "\f330"
}

.fa-caret-circle-up:before {
    content: "\f331"
}

.fa-caret-down:before {
    content: "\f0d7"
}

.fa-caret-left:before {
    content: "\f0d9"
}

.fa-caret-right:before {
    content: "\f0da"
}

.fa-caret-square-down:before {
    content: "\f150"
}

.fa-caret-square-left:before {
    content: "\f191"
}

.fa-caret-square-right:before {
    content: "\f152"
}

.fa-caret-square-up:before {
    content: "\f151"
}

.fa-caret-up:before {
    content: "\f0d8"
}

.fa-cart-arrow-down:before {
    content: "\f218"
}

.fa-cart-plus:before {
    content: "\f217"
}

.fa-cc-amazon-pay:before {
    content: "\f42d"
}

.fa-cc-amex:before {
    content: "\f1f3"
}

.fa-cc-apple-pay:before {
    content: "\f416"
}

.fa-cc-diners-club:before {
    content: "\f24c"
}

.fa-cc-discover:before {
    content: "\f1f2"
}

.fa-cc-jcb:before {
    content: "\f24b"
}

.fa-cc-mastercard:before {
    content: "\f1f1"
}

.fa-cc-paypal:before {
    content: "\f1f4"
}

.fa-cc-stripe:before {
    content: "\f1f5"
}

.fa-cc-visa:before {
    content: "\f1f0"
}

.fa-centercode:before {
    content: "\f380"
}

.fa-certificate:before {
    content: "\f0a3"
}

.fa-chart-area:before {
    content: "\f1fe"
}

.fa-chart-bar:before {
    content: "\f080"
}

.fa-chart-line:before {
    content: "\f201"
}

.fa-chart-pie:before {
    content: "\f200"
}

.fa-check:before {
    content: "\f00c"
}

.fa-check-circle:before {
    content: "\f058"
}

.fa-check-square:before {
    content: "\f14a"
}

.fa-chess:before {
    content: "\f439"
}

.fa-chess-bishop:before {
    content: "\f43a"
}

.fa-chess-bishop-alt:before {
    content: "\f43b"
}

.fa-chess-board:before {
    content: "\f43c"
}

.fa-chess-clock:before {
    content: "\f43d"
}

.fa-chess-clock-alt:before {
    content: "\f43e"
}

.fa-chess-king:before {
    content: "\f43f"
}

.fa-chess-king-alt:before {
    content: "\f440"
}

.fa-chess-knight:before {
    content: "\f441"
}

.fa-chess-knight-alt:before {
    content: "\f442"
}

.fa-chess-pawn:before {
    content: "\f443"
}

.fa-chess-pawn-alt:before {
    content: "\f444"
}

.fa-chess-queen:before {
    content: "\f445"
}

.fa-chess-queen-alt:before {
    content: "\f446"
}

.fa-chess-rook:before {
    content: "\f447"
}

.fa-chess-rook-alt:before {
    content: "\f448"
}

.fa-chevron-circle-down:before {
    content: "\f13a"
}

.fa-chevron-circle-left:before {
    content: "\f137"
}

.fa-chevron-circle-right:before {
    content: "\f138"
}

.fa-chevron-circle-up:before {
    content: "\f139"
}

.fa-chevron-double-down:before {
    content: "\f322"
}

.fa-chevron-double-left:before {
    content: "\f323"
}

.fa-chevron-double-right:before {
    content: "\f324"
}

.fa-chevron-double-up:before {
    content: "\f325"
}

.fa-chevron-down:before {
    content: "\f078"
}

.fa-chevron-left:before {
    content: "\f053"
}

.fa-chevron-right:before {
    content: "\f054"
}

.fa-chevron-square-down:before {
    content: "\f329"
}

.fa-chevron-square-left:before {
    content: "\f32a"
}

.fa-chevron-square-right:before {
    content: "\f32b"
}

.fa-chevron-square-up:before {
    content: "\f32c"
}

.fa-chevron-up:before {
    content: "\f077"
}

.fa-child:before {
    content: "\f1ae"
}

.fa-chrome:before {
    content: "\f268"
}

.fa-circle:before {
    content: "\f111"
}

.fa-circle-notch:before {
    content: "\f1ce"
}

.fa-clipboard:before {
    content: "\f328"
}

.fa-clipboard-check:before {
    content: "\f46c"
}

.fa-clipboard-list:before {
    content: "\f46d"
}

.fa-clock:before {
    content: "\f017"
}

.fa-clone:before {
    content: "\f24d"
}

.fa-closed-captioning:before {
    content: "\f20a"
}

.fa-cloud:before {
    content: "\f0c2"
}

.fa-cloud-download:before {
    content: "\f0ed"
}

.fa-cloud-download-alt:before {
    content: "\f381"
}

.fa-cloud-upload:before {
    content: "\f0ee"
}

.fa-cloud-upload-alt:before {
    content: "\f382"
}

.fa-cloudscale:before {
    content: "\f383"
}

.fa-cloudsmith:before {
    content: "\f384"
}

.fa-cloudversify:before {
    content: "\f385"
}

.fa-club:before {
    content: "\f327"
}

.fa-code:before {
    content: "\f121"
}

.fa-code-branch:before {
    content: "\f126"
}

.fa-code-commit:before {
    content: "\f386"
}

.fa-code-merge:before {
    content: "\f387"
}

.fa-codepen:before {
    content: "\f1cb"
}

.fa-codiepie:before {
    content: "\f284"
}

.fa-coffee:before {
    content: "\f0f4"
}

.fa-cog:before {
    content: "\f013"
}

.fa-cogs:before {
    content: "\f085"
}

.fa-columns:before {
    content: "\f0db"
}

.fa-comment:before {
    content: "\f075"
}

.fa-comment-alt:before {
    content: "\f27a"
}

.fa-comment-alt-check:before {
    content: "\f4a2"
}

.fa-comment-alt-dots:before {
    content: "\f4a3"
}

.fa-comment-alt-edit:before {
    content: "\f4a4"
}

.fa-comment-alt-exclamation:before {
    content: "\f4a5"
}

.fa-comment-alt-lines:before {
    content: "\f4a6"
}

.fa-comment-alt-minus:before {
    content: "\f4a7"
}

.fa-comment-alt-plus:before {
    content: "\f4a8"
}

.fa-comment-alt-slash:before {
    content: "\f4a9"
}

.fa-comment-alt-smile:before {
    content: "\f4aa"
}

.fa-comment-alt-times:before {
    content: "\f4ab"
}

.fa-comment-check:before {
    content: "\f4ac"
}

.fa-comment-dots:before {
    content: "\f4ad"
}

.fa-comment-edit:before {
    content: "\f4ae"
}

.fa-comment-exclamation:before {
    content: "\f4af"
}

.fa-comment-lines:before {
    content: "\f4b0"
}

.fa-comment-minus:before {
    content: "\f4b1"
}

.fa-comment-plus:before {
    content: "\f4b2"
}

.fa-comment-slash:before {
    content: "\f4b3"
}

.fa-comment-smile:before {
    content: "\f4b4"
}

.fa-comment-times:before {
    content: "\f4b5"
}

.fa-comments:before {
    content: "\f086"
}

.fa-comments-alt:before {
    content: "\f4b6"
}

.fa-compass:before {
    content: "\f14e"
}

.fa-compress:before {
    content: "\f066"
}

.fa-compress-alt:before {
    content: "\f422"
}

.fa-compress-wide:before {
    content: "\f326"
}

.fa-connectdevelop:before {
    content: "\f20e"
}

.fa-container-storage:before {
    content: "\f4b7"
}

.fa-contao:before {
    content: "\f26d"
}

.fa-conveyor-belt:before {
    content: "\f46e"
}

.fa-conveyor-belt-alt:before {
    content: "\f46f"
}

.fa-copy:before {
    content: "\f0c5"
}

.fa-copyright:before {
    content: "\f1f9"
}

.fa-couch:before {
    content: "\f4b8"
}

.fa-cpanel:before {
    content: "\f388"
}

.fa-creative-commons:before {
    content: "\f25e"
}

.fa-creative-commons-by:before {
    content: "\f4e7"
}

.fa-creative-commons-nc:before {
    content: "\f4e8"
}

.fa-creative-commons-nc-eu:before {
    content: "\f4e9"
}

.fa-creative-commons-nc-jp:before {
    content: "\f4ea"
}

.fa-creative-commons-nd:before {
    content: "\f4eb"
}

.fa-creative-commons-pd:before {
    content: "\f4ec"
}

.fa-creative-commons-pd-alt:before {
    content: "\f4ed"
}

.fa-creative-commons-remix:before {
    content: "\f4ee"
}

.fa-creative-commons-sa:before {
    content: "\f4ef"
}

.fa-creative-commons-sampling:before {
    content: "\f4f0"
}

.fa-creative-commons-sampling-plus:before {
    content: "\f4f1"
}

.fa-creative-commons-share:before {
    content: "\f4f2"
}

.fa-creative-commons-zero:before {
    content: "\f4f3"
}

.fa-credit-card:before {
    content: "\f09d"
}

.fa-credit-card-blank:before {
    content: "\f389"
}

.fa-credit-card-front:before {
    content: "\f38a"
}

.fa-cricket:before {
    content: "\f449"
}

.fa-crop:before {
    content: "\f125"
}

.fa-crosshairs:before {
    content: "\f05b"
}

.fa-css3:before {
    content: "\f13c"
}

.fa-css3-alt:before {
    content: "\f38b"
}

.fa-cube:before {
    content: "\f1b2"
}

.fa-cubes:before {
    content: "\f1b3"
}

.fa-curling:before {
    content: "\f44a"
}

.fa-cut:before {
    content: "\f0c4"
}

.fa-cuttlefish:before {
    content: "\f38c"
}

.fa-d-and-d:before {
    content: "\f38d"
}

.fa-dashcube:before {
    content: "\f210"
}

.fa-database:before {
    content: "\f1c0"
}

.fa-deaf:before {
    content: "\f2a4"
}

.fa-delicious:before {
    content: "\f1a5"
}

.fa-deploydog:before {
    content: "\f38e"
}

.fa-deskpro:before {
    content: "\f38f"
}

.fa-desktop:before {
    content: "\f108"
}

.fa-desktop-alt:before {
    content: "\f390"
}

.fa-deviantart:before {
    content: "\f1bd"
}

.fa-diagnoses:before {
    content: "\f470"
}

.fa-diamond:before {
    content: "\f219"
}

.fa-digg:before {
    content: "\f1a6"
}

.fa-digital-ocean:before {
    content: "\f391"
}

.fa-discord:before {
    content: "\f392"
}

.fa-discourse:before {
    content: "\f393"
}

.fa-dna:before {
    content: "\f471"
}

.fa-dochub:before {
    content: "\f394"
}

.fa-docker:before {
    content: "\f395"
}

.fa-dollar-sign:before {
    content: "\f155"
}

.fa-dolly:before {
    content: "\f472"
}

.fa-dolly-empty:before {
    content: "\f473"
}

.fa-dolly-flatbed:before {
    content: "\f474"
}

.fa-dolly-flatbed-alt:before {
    content: "\f475"
}

.fa-dolly-flatbed-empty:before {
    content: "\f476"
}

.fa-donate:before {
    content: "\f4b9"
}

.fa-dot-circle:before {
    content: "\f192"
}

.fa-dove:before {
    content: "\f4ba"
}

.fa-download:before {
    content: "\f019"
}

.fa-draft2digital:before {
    content: "\f396"
}

.fa-dribbble:before {
    content: "\f17d"
}

.fa-dribbble-square:before {
    content: "\f397"
}

.fa-dropbox:before {
    content: "\f16b"
}

.fa-drupal:before {
    content: "\f1a9"
}

.fa-dumbbell:before {
    content: "\f44b"
}

.fa-dyalog:before {
    content: "\f399"
}

.fa-earlybirds:before {
    content: "\f39a"
}

.fa-ebay:before {
    content: "\f4f4"
}

.fa-edge:before {
    content: "\f282"
}

.fa-edit:before {
    content: "\f044"
}

.fa-eject:before {
    content: "\f052"
}

.fa-elementor:before {
    content: "\f430"
}

.fa-ellipsis-h:before {
    content: "\f141"
}

.fa-ellipsis-h-alt:before {
    content: "\f39b"
}

.fa-ellipsis-v:before {
    content: "\f142"
}

.fa-ellipsis-v-alt:before {
    content: "\f39c"
}

.fa-ember:before {
    content: "\f423"
}

.fa-empire:before {
    content: "\f1d1"
}

.fa-envelope:before {
    content: "\f0e0"
}

.fa-envelope-open:before {
    content: "\f2b6"
}

.fa-envelope-square:before {
    content: "\f199"
}

.fa-envira:before {
    content: "\f299"
}

.fa-eraser:before {
    content: "\f12d"
}

.fa-erlang:before {
    content: "\f39d"
}

.fa-ethereum:before {
    content: "\f42e"
}

.fa-etsy:before {
    content: "\f2d7"
}

.fa-euro-sign:before {
    content: "\f153"
}

.fa-exchange:before {
    content: "\f0ec"
}

.fa-exchange-alt:before {
    content: "\f362"
}

.fa-exclamation:before {
    content: "\f12a"
}

.fa-exclamation-circle:before {
    content: "\f06a"
}

.fa-exclamation-square:before {
    content: "\f321"
}

.fa-exclamation-triangle:before {
    content: "\f071"
}

.fa-expand:before {
    content: "\f065"
}

.fa-expand-alt:before {
    content: "\f424"
}

.fa-expand-arrows:before {
    content: "\f31d"
}

.fa-expand-arrows-alt:before {
    content: "\f31e"
}

.fa-expand-wide:before {
    content: "\f320"
}

.fa-expeditedssl:before {
    content: "\f23e"
}

.fa-external-link:before {
    content: "\f08e"
}

.fa-external-link-alt:before {
    content: "\f35d"
}

.fa-external-link-square:before {
    content: "\f14c"
}

.fa-external-link-square-alt:before {
    content: "\f360"
}

.fa-eye:before {
    content: "\f06e"
}

.fa-eye-dropper:before {
    content: "\f1fb"
}

.fa-eye-slash:before {
    content: "\f070"
}

.fa-facebook:before {
    content: "\f09a"
}

.fa-facebook-f:before {
    content: "\f39e"
}

.fa-facebook-messenger:before {
    content: "\f39f"
}

.fa-facebook-square:before {
    content: "\f082"
}

.fa-fast-backward:before {
    content: "\f049"
}

.fa-fast-forward:before {
    content: "\f050"
}

.fa-fax:before {
    content: "\f1ac"
}

.fa-female:before {
    content: "\f182"
}

.fa-field-hockey:before {
    content: "\f44c"
}

.fa-fighter-jet:before {
    content: "\f0fb"
}

.fa-file:before {
    content: "\f15b"
}

.fa-file-alt:before {
    content: "\f15c"
}

.fa-file-archive:before {
    content: "\f1c6"
}

.fa-file-audio:before {
    content: "\f1c7"
}

.fa-file-check:before {
    content: "\f316"
}

.fa-file-code:before {
    content: "\f1c9"
}

.fa-file-edit:before {
    content: "\f31c"
}

.fa-file-excel:before {
    content: "\f1c3"
}

.fa-file-exclamation:before {
    content: "\f31a"
}

.fa-file-image:before {
    content: "\f1c5"
}

.fa-file-medical:before {
    content: "\f477"
}

.fa-file-medical-alt:before {
    content: "\f478"
}

.fa-file-minus:before {
    content: "\f318"
}

.fa-file-pdf:before {
    content: "\f1c1"
}

.fa-file-plus:before {
    content: "\f319"
}

.fa-file-powerpoint:before {
    content: "\f1c4"
}

.fa-file-times:before {
    content: "\f317"
}

.fa-file-video:before {
    content: "\f1c8"
}

.fa-file-word:before {
    content: "\f1c2"
}

.fa-film:before {
    content: "\f008"
}

.fa-film-alt:before {
    content: "\f3a0"
}

.fa-filter:before {
    content: "\f0b0"
}

.fa-fire:before {
    content: "\f06d"
}

.fa-fire-extinguisher:before {
    content: "\f134"
}

.fa-firefox:before {
    content: "\f269"
}

.fa-first-aid:before {
    content: "\f479"
}

.fa-first-order:before {
    content: "\f2b0"
}

.fa-first-order-alt:before {
    content: "\f50a"
}

.fa-firstdraft:before {
    content: "\f3a1"
}

.fa-flag:before {
    content: "\f024"
}

.fa-flag-checkered:before {
    content: "\f11e"
}

.fa-flask:before {
    content: "\f0c3"
}

.fa-flickr:before {
    content: "\f16e"
}

.fa-flipboard:before {
    content: "\f44d"
}

.fa-fly:before {
    content: "\f417"
}

.fa-folder:before {
    content: "\f07b"
}

.fa-folder-open:before {
    content: "\f07c"
}

.fa-font:before {
    content: "\f031"
}

.fa-font-awesome:before {
    content: "\f2b4"
}

.fa-font-awesome-alt:before {
    content: "\f35c"
}

.fa-font-awesome-flag:before {
    content: "\f425"
}

.fa-font-awesome-logo-full:before {
    content: "\f4e6"
}

.fa-fonticons:before {
    content: "\f280"
}

.fa-fonticons-fi:before {
    content: "\f3a2"
}

.fa-football-ball:before {
    content: "\f44e"
}

.fa-football-helmet:before {
    content: "\f44f"
}

.fa-forklift:before {
    content: "\f47a"
}

.fa-fort-awesome:before {
    content: "\f286"
}

.fa-fort-awesome-alt:before {
    content: "\f3a3"
}

.fa-forumbee:before {
    content: "\f211"
}

.fa-forward:before {
    content: "\f04e"
}

.fa-foursquare:before {
    content: "\f180"
}

.fa-fragile:before {
    content: "\f4bb"
}

.fa-free-code-camp:before {
    content: "\f2c5"
}

.fa-freebsd:before {
    content: "\f3a4"
}

.fa-frown:before {
    content: "\f119"
}

.fa-fulcrum:before {
    content: "\f50b"
}

.fa-futbol:before {
    content: "\f1e3"
}

.fa-galactic-republic:before {
    content: "\f50c"
}

.fa-galactic-senate:before {
    content: "\f50d"
}

.fa-gamepad:before {
    content: "\f11b"
}

.fa-gavel:before {
    content: "\f0e3"
}

.fa-gem:before {
    content: "\f3a5"
}

.fa-genderless:before {
    content: "\f22d"
}

.fa-get-pocket:before {
    content: "\f265"
}

.fa-gg:before {
    content: "\f260"
}

.fa-gg-circle:before {
    content: "\f261"
}

.fa-gift:before {
    content: "\f06b"
}

.fa-git:before {
    content: "\f1d3"
}

.fa-git-square:before {
    content: "\f1d2"
}

.fa-github:before {
    content: "\f09b"
}

.fa-github-alt:before {
    content: "\f113"
}

.fa-github-square:before {
    content: "\f092"
}

.fa-gitkraken:before {
    content: "\f3a6"
}

.fa-gitlab:before {
    content: "\f296"
}

.fa-gitter:before {
    content: "\f426"
}

.fa-glass-martini:before {
    content: "\f000"
}

.fa-glide:before {
    content: "\f2a5"
}

.fa-glide-g:before {
    content: "\f2a6"
}

.fa-globe:before {
    content: "\f0ac"
}

.fa-gofore:before {
    content: "\f3a7"
}

.fa-golf-ball:before {
    content: "\f450"
}

.fa-golf-club:before {
    content: "\f451"
}

.fa-goodreads:before {
    content: "\f3a8"
}

.fa-goodreads-g:before {
    content: "\f3a9"
}

.fa-google:before {
    content: "\f1a0"
}

.fa-google-drive:before {
    content: "\f3aa"
}

.fa-google-play:before {
    content: "\f3ab"
}

.fa-google-plus:before {
    content: "\f2b3"
}

.fa-google-plus-g:before {
    content: "\f0d5"
}

.fa-google-plus-square:before {
    content: "\f0d4"
}

.fa-google-wallet:before {
    content: "\f1ee"
}

.fa-graduation-cap:before {
    content: "\f19d"
}

.fa-gratipay:before {
    content: "\f184"
}

.fa-grav:before {
    content: "\f2d6"
}

.fa-gripfire:before {
    content: "\f3ac"
}

.fa-grunt:before {
    content: "\f3ad"
}

.fa-gulp:before {
    content: "\f3ae"
}

.fa-h-square:before {
    content: "\f0fd"
}

.fa-h1:before {
    content: "\f313"
}

.fa-h2:before {
    content: "\f314"
}

.fa-h3:before {
    content: "\f315"
}

.fa-hacker-news:before {
    content: "\f1d4"
}

.fa-hacker-news-square:before {
    content: "\f3af"
}

.fa-hand-heart:before {
    content: "\f4bc"
}

.fa-hand-holding:before {
    content: "\f4bd"
}

.fa-hand-holding-box:before {
    content: "\f47b"
}

.fa-hand-holding-heart:before {
    content: "\f4be"
}

.fa-hand-holding-seedling:before {
    content: "\f4bf"
}

.fa-hand-holding-usd:before {
    content: "\f4c0"
}

.fa-hand-holding-water:before {
    content: "\f4c1"
}

.fa-hand-lizard:before {
    content: "\f258"
}

.fa-hand-paper:before {
    content: "\f256"
}

.fa-hand-peace:before {
    content: "\f25b"
}

.fa-hand-point-down:before {
    content: "\f0a7"
}

.fa-hand-point-left:before {
    content: "\f0a5"
}

.fa-hand-point-right:before {
    content: "\f0a4"
}

.fa-hand-point-up:before {
    content: "\f0a6"
}

.fa-hand-pointer:before {
    content: "\f25a"
}

.fa-hand-receiving:before {
    content: "\f47c"
}

.fa-hand-rock:before {
    content: "\f255"
}

.fa-hand-scissors:before {
    content: "\f257"
}

.fa-hand-spock:before {
    content: "\f259"
}

.fa-hands:before {
    content: "\f4c2"
}

.fa-hands-heart:before {
    content: "\f4c3"
}

.fa-hands-helping:before {
    content: "\f4c4"
}

.fa-hands-usd:before {
    content: "\f4c5"
}

.fa-handshake:before {
    content: "\f2b5"
}

.fa-handshake-alt:before {
    content: "\f4c6"
}

.fa-hashtag:before {
    content: "\f292"
}

.fa-hdd:before {
    content: "\f0a0"
}

.fa-heading:before {
    content: "\f1dc"
}

.fa-headphones:before {
    content: "\f025"
}

.fa-heart:before {
    content: "\f004"
}

.fa-heart-circle:before {
    content: "\f4c7"
}

.fa-heart-square:before {
    content: "\f4c8"
}

.fa-heartbeat:before {
    content: "\f21e"
}

.fa-hexagon:before {
    content: "\f312"
}

.fa-hips:before {
    content: "\f452"
}

.fa-hire-a-helper:before {
    content: "\f3b0"
}

.fa-history:before {
    content: "\f1da"
}

.fa-hockey-puck:before {
    content: "\f453"
}

.fa-hockey-sticks:before {
    content: "\f454"
}

.fa-home:before {
    content: "\f015"
}

.fa-home-heart:before {
    content: "\f4c9"
}

.fa-hooli:before {
    content: "\f427"
}

.fa-hospital:before {
    content: "\f0f8"
}

.fa-hospital-alt:before {
    content: "\f47d"
}

.fa-hospital-symbol:before {
    content: "\f47e"
}

.fa-hotjar:before {
    content: "\f3b1"
}

.fa-hourglass:before {
    content: "\f254"
}

.fa-hourglass-end:before {
    content: "\f253"
}

.fa-hourglass-half:before {
    content: "\f252"
}

.fa-hourglass-start:before {
    content: "\f251"
}

.fa-houzz:before {
    content: "\f27c"
}

.fa-html5:before {
    content: "\f13b"
}

.fa-hubspot:before {
    content: "\f3b2"
}

.fa-i-cursor:before {
    content: "\f246"
}

.fa-id-badge:before {
    content: "\f2c1"
}

.fa-id-card:before {
    content: "\f2c2"
}

.fa-id-card-alt:before {
    content: "\f47f"
}

.fa-image:before {
    content: "\f03e"
}

.fa-images:before {
    content: "\f302"
}

.fa-imdb:before {
    content: "\f2d8"
}

.fa-inbox:before {
    content: "\f01c"
}

.fa-inbox-in:before {
    content: "\f310"
}

.fa-inbox-out:before {
    content: "\f311"
}

.fa-indent:before {
    content: "\f03c"
}

.fa-industry:before {
    content: "\f275"
}

.fa-industry-alt:before {
    content: "\f3b3"
}

.fa-info:before {
    content: "\f129"
}

.fa-info-circle:before {
    content: "\f05a"
}

.fa-info-square:before {
    content: "\f30f"
}

.fa-instagram:before {
    content: "\f16d"
}

.fa-internet-explorer:before {
    content: "\f26b"
}

.fa-inventory:before {
    content: "\f480"
}

.fa-ioxhost:before {
    content: "\f208"
}

.fa-italic:before {
    content: "\f033"
}

.fa-itunes:before {
    content: "\f3b4"
}

.fa-itunes-note:before {
    content: "\f3b5"
}

.fa-jack-o-lantern:before {
    content: "\f30e"
}

.fa-java:before {
    content: "\f4e4"
}

.fa-jedi-order:before {
    content: "\f50e"
}

.fa-jenkins:before {
    content: "\f3b6"
}

.fa-joget:before {
    content: "\f3b7"
}

.fa-joomla:before {
    content: "\f1aa"
}

.fa-js:before {
    content: "\f3b8"
}

.fa-js-square:before {
    content: "\f3b9"
}

.fa-jsfiddle:before {
    content: "\f1cc"
}

.fa-key:before {
    content: "\f084"
}

.fa-keybase:before {
    content: "\f4f5"
}

.fa-keyboard:before {
    content: "\f11c"
}

.fa-keycdn:before {
    content: "\f3ba"
}

.fa-kickstarter:before {
    content: "\f3bb"
}

.fa-kickstarter-k:before {
    content: "\f3bc"
}

.fa-korvue:before {
    content: "\f42f"
}

.fa-lamp:before {
    content: "\f4ca"
}

.fa-language:before {
    content: "\f1ab"
}

.fa-laptop:before {
    content: "\f109"
}

.fa-laravel:before {
    content: "\f3bd"
}

.fa-lastfm:before {
    content: "\f202"
}

.fa-lastfm-square:before {
    content: "\f203"
}

.fa-leaf:before {
    content: "\f06c"
}

.fa-leaf-heart:before {
    content: "\f4cb"
}

.fa-leanpub:before {
    content: "\f212"
}

.fa-lemon:before {
    content: "\f094"
}

.fa-less:before {
    content: "\f41d"
}

.fa-level-down:before {
    content: "\f149"
}

.fa-level-down-alt:before {
    content: "\f3be"
}

.fa-level-up:before {
    content: "\f148"
}

.fa-level-up-alt:before {
    content: "\f3bf"
}

.fa-life-ring:before {
    content: "\f1cd"
}

.fa-lightbulb:before {
    content: "\f0eb"
}

.fa-line:before {
    content: "\f3c0"
}

.fa-link:before {
    content: "\f0c1"
}

.fa-linkedin:before {
    content: "\f08c"
}

.fa-linkedin-in:before {
    content: "\f0e1"
}

.fa-linode:before {
    content: "\f2b8"
}

.fa-linux:before {
    content: "\f17c"
}

.fa-lira-sign:before {
    content: "\f195"
}

.fa-list:before {
    content: "\f03a"
}

.fa-list-alt:before {
    content: "\f022"
}

.fa-list-ol:before {
    content: "\f0cb"
}

.fa-list-ul:before {
    content: "\f0ca"
}

.fa-location-arrow:before {
    content: "\f124"
}

.fa-lock:before {
    content: "\f023"
}

.fa-lock-alt:before {
    content: "\f30d"
}

.fa-lock-open:before {
    content: "\f3c1"
}

.fa-lock-open-alt:before {
    content: "\f3c2"
}

.fa-long-arrow-alt-down:before {
    content: "\f309"
}

.fa-long-arrow-alt-left:before {
    content: "\f30a"
}

.fa-long-arrow-alt-right:before {
    content: "\f30b"
}

.fa-long-arrow-alt-up:before {
    content: "\f30c"
}

.fa-long-arrow-down:before {
    content: "\f175"
}

.fa-long-arrow-left:before {
    content: "\f177"
}

.fa-long-arrow-right:before {
    content: "\f178"
}

.fa-long-arrow-up:before {
    content: "\f176"
}

.fa-loveseat:before {
    content: "\f4cc"
}

.fa-low-vision:before {
    content: "\f2a8"
}

.fa-luchador:before {
    content: "\f455"
}

.fa-lyft:before {
    content: "\f3c3"
}

.fa-magento:before {
    content: "\f3c4"
}

.fa-magic:before {
    content: "\f0d0"
}

.fa-magnet:before {
    content: "\f076"
}

.fa-male:before {
    content: "\f183"
}

.fa-mandalorian:before {
    content: "\f50f"
}

.fa-map:before {
    content: "\f279"
}

.fa-map-marker:before {
    content: "\f041"
}

.fa-map-marker-alt:before {
    content: "\f3c5"
}

.fa-map-pin:before {
    content: "\f276"
}

.fa-map-signs:before {
    content: "\f277"
}

.fa-mars:before {
    content: "\f222"
}

.fa-mars-double:before {
    content: "\f227"
}

.fa-mars-stroke:before {
    content: "\f229"
}

.fa-mars-stroke-h:before {
    content: "\f22b"
}

.fa-mars-stroke-v:before {
    content: "\f22a"
}

.fa-mastodon:before {
    content: "\f4f6"
}

.fa-maxcdn:before {
    content: "\f136"
}

.fa-medapps:before {
    content: "\f3c6"
}

.fa-medium:before {
    content: "\f23a"
}

.fa-medium-m:before {
    content: "\f3c7"
}

.fa-medkit:before {
    content: "\f0fa"
}

.fa-medrt:before {
    content: "\f3c8"
}

.fa-meetup:before {
    content: "\f2e0"
}

.fa-meh:before {
    content: "\f11a"
}

.fa-mercury:before {
    content: "\f223"
}

.fa-microchip:before {
    content: "\f2db"
}

.fa-microphone:before {
    content: "\f130"
}

.fa-microphone-alt:before {
    content: "\f3c9"
}

.fa-microphone-slash:before {
    content: "\f131"
}

.fa-microsoft:before {
    content: "\f3ca"
}

.fa-minus:before {
    content: "\f068"
}

.fa-minus-circle:before {
    content: "\f056"
}

.fa-minus-hexagon:before {
    content: "\f307"
}

.fa-minus-octagon:before {
    content: "\f308"
}

.fa-minus-square:before {
    content: "\f146"
}

.fa-mix:before {
    content: "\f3cb"
}

.fa-mixcloud:before {
    content: "\f289"
}

.fa-mizuni:before {
    content: "\f3cc"
}

.fa-mobile:before {
    content: "\f10b"
}

.fa-mobile-alt:before {
    content: "\f3cd"
}

.fa-mobile-android:before {
    content: "\f3ce"
}

.fa-mobile-android-alt:before {
    content: "\f3cf"
}

.fa-modx:before {
    content: "\f285"
}

.fa-monero:before {
    content: "\f3d0"
}

.fa-money-bill:before {
    content: "\f0d6"
}

.fa-money-bill-alt:before {
    content: "\f3d1"
}

.fa-moon:before {
    content: "\f186"
}

.fa-motorcycle:before {
    content: "\f21c"
}

.fa-mouse-pointer:before {
    content: "\f245"
}

.fa-music:before {
    content: "\f001"
}

.fa-napster:before {
    content: "\f3d2"
}

.fa-neuter:before {
    content: "\f22c"
}

.fa-newspaper:before {
    content: "\f1ea"
}

.fa-nintendo-switch:before {
    content: "\f418"
}

.fa-node:before {
    content: "\f419"
}

.fa-node-js:before {
    content: "\f3d3"
}

.fa-notes-medical:before {
    content: "\f481"
}

.fa-npm:before {
    content: "\f3d4"
}

.fa-ns8:before {
    content: "\f3d5"
}

.fa-nutritionix:before {
    content: "\f3d6"
}

.fa-object-group:before {
    content: "\f247"
}

.fa-object-ungroup:before {
    content: "\f248"
}

.fa-octagon:before {
    content: "\f306"
}

.fa-odnoklassniki:before {
    content: "\f263"
}

.fa-odnoklassniki-square:before {
    content: "\f264"
}

.fa-old-republic:before {
    content: "\f510"
}

.fa-opencart:before {
    content: "\f23d"
}

.fa-openid:before {
    content: "\f19b"
}

.fa-opera:before {
    content: "\f26a"
}

.fa-optin-monster:before {
    content: "\f23c"
}

.fa-osi:before {
    content: "\f41a"
}

.fa-outdent:before {
    content: "\f03b"
}

.fa-page4:before {
    content: "\f3d7"
}

.fa-pagelines:before {
    content: "\f18c"
}

.fa-paint-brush:before {
    content: "\f1fc"
}

.fa-palfed:before {
    content: "\f3d8"
}

.fa-pallet:before {
    content: "\f482"
}

.fa-pallet-alt:before {
    content: "\f483"
}

.fa-paper-plane:before {
    content: "\f1d8"
}

.fa-paperclip:before {
    content: "\f0c6"
}

.fa-parachute-box:before {
    content: "\f4cd"
}

.fa-paragraph:before {
    content: "\f1dd"
}

.fa-paste:before {
    content: "\f0ea"
}

.fa-patreon:before {
    content: "\f3d9"
}

.fa-pause:before {
    content: "\f04c"
}

.fa-pause-circle:before {
    content: "\f28b"
}

.fa-paw:before {
    content: "\f1b0"
}

.fa-paypal:before {
    content: "\f1ed"
}

.fa-pen:before {
    content: "\f304"
}

.fa-pen-alt:before {
    content: "\f305"
}

.fa-pen-square:before {
    content: "\f14b"
}

.fa-pencil:before {
    content: "\f040"
}

.fa-pencil-alt:before {
    content: "\f303"
}

.fa-pennant:before {
    content: "\f456"
}

.fa-people-carry:before {
    content: "\f4ce"
}

.fa-percent:before {
    content: "\f295"
}

.fa-periscope:before {
    content: "\f3da"
}

.fa-person-carry:before {
    content: "\f4cf"
}

.fa-person-dolly:before {
    content: "\f4d0"
}

.fa-person-dolly-empty:before {
    content: "\f4d1"
}

.fa-phabricator:before {
    content: "\f3db"
}

.fa-phoenix-framework:before {
    content: "\f3dc"
}

.fa-phoenix-squadron:before {
    content: "\f511"
}

.fa-phone:before {
    content: "\f095"
}

.fa-phone-plus:before {
    content: "\f4d2"
}

.fa-phone-slash:before {
    content: "\f3dd"
}

.fa-phone-square:before {
    content: "\f098"
}

.fa-phone-volume:before {
    content: "\f2a0"
}

.fa-php:before {
    content: "\f457"
}

.fa-pied-piper:before {
    content: "\f2ae"
}

.fa-pied-piper-alt:before {
    content: "\f1a8"
}

.fa-pied-piper-hat:before {
    content: "\f4e5"
}

.fa-pied-piper-pp:before {
    content: "\f1a7"
}

.fa-piggy-bank:before {
    content: "\f4d3"
}

.fa-pills:before {
    content: "\f484"
}

.fa-pinterest:before {
    content: "\f0d2"
}

.fa-pinterest-p:before {
    content: "\f231"
}

.fa-pinterest-square:before {
    content: "\f0d3"
}

.fa-plane:before {
    content: "\f072"
}

.fa-plane-alt:before {
    content: "\f3de"
}

.fa-play:before {
    content: "\f04b"
}

.fa-play-circle:before {
    content: "\f144"
}

.fa-playstation:before {
    content: "\f3df"
}

.fa-plug:before {
    content: "\f1e6"
}

.fa-plus:before {
    content: "\f067"
}

.fa-plus-circle:before {
    content: "\f055"
}

.fa-plus-hexagon:before {
    content: "\f300"
}

.fa-plus-octagon:before {
    content: "\f301"
}

.fa-plus-square:before {
    content: "\f0fe"
}

.fa-podcast:before {
    content: "\f2ce"
}

.fa-poo:before {
    content: "\f2fe"
}

.fa-portrait:before {
    content: "\f3e0"
}

.fa-pound-sign:before {
    content: "\f154"
}

.fa-power-off:before {
    content: "\f011"
}

.fa-prescription-bottle:before {
    content: "\f485"
}

.fa-prescription-bottle-alt:before {
    content: "\f486"
}

.fa-print:before {
    content: "\f02f"
}

.fa-procedures:before {
    content: "\f487"
}

.fa-product-hunt:before {
    content: "\f288"
}

.fa-pushed:before {
    content: "\f3e1"
}

.fa-puzzle-piece:before {
    content: "\f12e"
}

.fa-python:before {
    content: "\f3e2"
}

.fa-qq:before {
    content: "\f1d6"
}

.fa-qrcode:before {
    content: "\f029"
}

.fa-question:before {
    content: "\f128"
}

.fa-question-circle:before {
    content: "\f059"
}

.fa-question-square:before {
    content: "\f2fd"
}

.fa-quidditch:before {
    content: "\f458"
}

.fa-quinscape:before {
    content: "\f459"
}

.fa-quora:before {
    content: "\f2c4"
}

.fa-quote-left:before {
    content: "\f10d"
}

.fa-quote-right:before {
    content: "\f10e"
}

.fa-r-project:before {
    content: "\f4f7"
}

.fa-racquet:before {
    content: "\f45a"
}

.fa-ramp-loading:before {
    content: "\f4d4"
}

.fa-random:before {
    content: "\f074"
}

.fa-ravelry:before {
    content: "\f2d9"
}

.fa-react:before {
    content: "\f41b"
}

.fa-readme:before {
    content: "\f4d5"
}

.fa-rebel:before {
    content: "\f1d0"
}

.fa-rectangle-landscape:before {
    content: "\f2fa"
}

.fa-rectangle-portrait:before {
    content: "\f2fb"
}

.fa-rectangle-wide:before {
    content: "\f2fc"
}

.fa-recycle:before {
    content: "\f1b8"
}

.fa-red-river:before {
    content: "\f3e3"
}

.fa-reddit:before {
    content: "\f1a1"
}

.fa-reddit-alien:before {
    content: "\f281"
}

.fa-reddit-square:before {
    content: "\f1a2"
}

.fa-redo:before {
    content: "\f01e"
}

.fa-redo-alt:before {
    content: "\f2f9"
}

.fa-registered:before {
    content: "\f25d"
}

.fa-rendact:before {
    content: "\f3e4"
}

.fa-renren:before {
    content: "\f18b"
}

.fa-repeat:before {
    content: "\f363"
}

.fa-repeat-1:before {
    content: "\f365"
}

.fa-repeat-1-alt:before {
    content: "\f366"
}

.fa-repeat-alt:before {
    content: "\f364"
}

.fa-reply:before {
    content: "\f3e5"
}

.fa-reply-all:before {
    content: "\f122"
}

.fa-replyd:before {
    content: "\f3e6"
}

.fa-researchgate:before {
    content: "\f4f8"
}

.fa-resolving:before {
    content: "\f3e7"
}

.fa-retweet:before {
    content: "\f079"
}

.fa-retweet-alt:before {
    content: "\f361"
}

.fa-ribbon:before {
    content: "\f4d6"
}

.fa-road:before {
    content: "\f018"
}

.fa-rocket:before {
    content: "\f135"
}

.fa-rocketchat:before {
    content: "\f3e8"
}

.fa-rockrms:before {
    content: "\f3e9"
}

.fa-route:before {
    content: "\f4d7"
}

.fa-rss:before {
    content: "\f09e"
}

.fa-rss-square:before {
    content: "\f143"
}

.fa-ruble-sign:before {
    content: "\f158"
}

.fa-rupee-sign:before {
    content: "\f156"
}

.fa-safari:before {
    content: "\f267"
}

.fa-sass:before {
    content: "\f41e"
}

.fa-save:before {
    content: "\f0c7"
}

.fa-scanner:before {
    content: "\f488"
}

.fa-scanner-keyboard:before {
    content: "\f489"
}

.fa-scanner-touchscreen:before {
    content: "\f48a"
}

.fa-schlix:before {
    content: "\f3ea"
}

.fa-scribd:before {
    content: "\f28a"
}

.fa-scrubber:before {
    content: "\f2f8"
}

.fa-search:before {
    content: "\f002"
}

.fa-search-minus:before {
    content: "\f010"
}

.fa-search-plus:before {
    content: "\f00e"
}

.fa-searchengin:before {
    content: "\f3eb"
}

.fa-seedling:before {
    content: "\f4d8"
}

.fa-sellcast:before {
    content: "\f2da"
}

.fa-sellsy:before {
    content: "\f213"
}

.fa-server:before {
    content: "\f233"
}

.fa-servicestack:before {
    content: "\f3ec"
}

.fa-share:before {
    content: "\f064"
}

.fa-share-all:before {
    content: "\f367"
}

.fa-share-alt:before {
    content: "\f1e0"
}

.fa-share-alt-square:before {
    content: "\f1e1"
}

.fa-share-square:before {
    content: "\f14d"
}

.fa-shekel-sign:before {
    content: "\f20b"
}

.fa-shield:before {
    content: "\f132"
}

.fa-shield-alt:before {
    content: "\f3ed"
}

.fa-shield-check:before {
    content: "\f2f7"
}

.fa-ship:before {
    content: "\f21a"
}

.fa-shipping-fast:before {
    content: "\f48b"
}

.fa-shipping-timed:before {
    content: "\f48c"
}

.fa-shirtsinbulk:before {
    content: "\f214"
}

.fa-shopping-bag:before {
    content: "\f290"
}

.fa-shopping-basket:before {
    content: "\f291"
}

.fa-shopping-cart:before {
    content: "\f07a"
}

.fa-shower:before {
    content: "\f2cc"
}

.fa-shuttlecock:before {
    content: "\f45b"
}

.fa-sign:before {
    content: "\f4d9"
}

.fa-sign-in:before {
    content: "\f090"
}

.fa-sign-in-alt:before {
    content: "\f2f6"
}

.fa-sign-language:before {
    content: "\f2a7"
}

.fa-sign-out:before {
    content: "\f08b"
}

.fa-sign-out-alt:before {
    content: "\f2f5"
}

.fa-signal:before {
    content: "\f012"
}

.fa-simplybuilt:before {
    content: "\f215"
}

.fa-sistrix:before {
    content: "\f3ee"
}

.fa-sitemap:before {
    content: "\f0e8"
}

.fa-sith:before {
    content: "\f512"
}

.fa-skyatlas:before {
    content: "\f216"
}

.fa-skype:before {
    content: "\f17e"
}

.fa-slack:before {
    content: "\f198"
}

.fa-slack-hash:before {
    content: "\f3ef"
}

.fa-sliders-h:before {
    content: "\f1de"
}

.fa-sliders-h-square:before {
    content: "\f3f0"
}

.fa-sliders-v:before {
    content: "\f3f1"
}

.fa-sliders-v-square:before {
    content: "\f3f2"
}

.fa-slideshare:before {
    content: "\f1e7"
}

.fa-smile:before {
    content: "\f118"
}

.fa-smile-plus:before {
    content: "\f4da"
}

.fa-smoking:before {
    content: "\f48d"
}

.fa-snapchat:before {
    content: "\f2ab"
}

.fa-snapchat-ghost:before {
    content: "\f2ac"
}

.fa-snapchat-square:before {
    content: "\f2ad"
}

.fa-snowflake:before {
    content: "\f2dc"
}

.fa-sort:before {
    content: "\f0dc"
}

.fa-sort-alpha-down:before {
    content: "\f15d"
}

.fa-sort-alpha-up:before {
    content: "\f15e"
}

.fa-sort-amount-down:before {
    content: "\f160"
}

.fa-sort-amount-up:before {
    content: "\f161"
}

.fa-sort-down:before {
    content: "\f0dd"
}

.fa-sort-numeric-down:before {
    content: "\f162"
}

.fa-sort-numeric-up:before {
    content: "\f163"
}

.fa-sort-up:before {
    content: "\f0de"
}

.fa-soundcloud:before {
    content: "\f1be"
}

.fa-space-shuttle:before {
    content: "\f197"
}

.fa-spade:before {
    content: "\f2f4"
}

.fa-speakap:before {
    content: "\f3f3"
}

.fa-spinner:before {
    content: "\f110"
}

.fa-spinner-third:before {
    content: "\f3f4"
}

.fa-spotify:before {
    content: "\f1bc"
}

.fa-square:before {
    content: "\f0c8"
}

.fa-square-full:before {
    content: "\f45c"
}

.fa-stack-exchange:before {
    content: "\f18d"
}

.fa-stack-overflow:before {
    content: "\f16c"
}

.fa-star:before {
    content: "\f005"
}

.fa-star-exclamation:before {
    content: "\f2f3"
}

.fa-star-half:before {
    content: "\f089"
}

.fa-staylinked:before {
    content: "\f3f5"
}

.fa-steam:before {
    content: "\f1b6"
}

.fa-steam-square:before {
    content: "\f1b7"
}

.fa-steam-symbol:before {
    content: "\f3f6"
}

.fa-step-backward:before {
    content: "\f048"
}

.fa-step-forward:before {
    content: "\f051"
}

.fa-stethoscope:before {
    content: "\f0f1"
}

.fa-sticker-mule:before {
    content: "\f3f7"
}

.fa-sticky-note:before {
    content: "\f249"
}

.fa-stop:before {
    content: "\f04d"
}

.fa-stop-circle:before {
    content: "\f28d"
}

.fa-stopwatch:before {
    content: "\f2f2"
}

.fa-strava:before {
    content: "\f428"
}

.fa-street-view:before {
    content: "\f21d"
}

.fa-strikethrough:before {
    content: "\f0cc"
}

.fa-stripe:before {
    content: "\f429"
}

.fa-stripe-s:before {
    content: "\f42a"
}

.fa-studiovinari:before {
    content: "\f3f8"
}

.fa-stumbleupon:before {
    content: "\f1a4"
}

.fa-stumbleupon-circle:before {
    content: "\f1a3"
}

.fa-subscript:before {
    content: "\f12c"
}

.fa-subway:before {
    content: "\f239"
}

.fa-suitcase:before {
    content: "\f0f2"
}

.fa-sun:before {
    content: "\f185"
}

.fa-superpowers:before {
    content: "\f2dd"
}

.fa-superscript:before {
    content: "\f12b"
}

.fa-supple:before {
    content: "\f3f9"
}

.fa-sync:before {
    content: "\f021"
}

.fa-sync-alt:before {
    content: "\f2f1"
}

.fa-syringe:before {
    content: "\f48e"
}

.fa-table:before {
    content: "\f0ce"
}

.fa-table-tennis:before {
    content: "\f45d"
}

.fa-tablet:before {
    content: "\f10a"
}

.fa-tablet-alt:before {
    content: "\f3fa"
}

.fa-tablet-android:before {
    content: "\f3fb"
}

.fa-tablet-android-alt:before {
    content: "\f3fc"
}

.fa-tablet-rugged:before {
    content: "\f48f"
}

.fa-tablets:before {
    content: "\f490"
}

.fa-tachometer:before {
    content: "\f0e4"
}

.fa-tachometer-alt:before {
    content: "\f3fd"
}

.fa-tag:before {
    content: "\f02b"
}

.fa-tags:before {
    content: "\f02c"
}

.fa-tape:before {
    content: "\f4db"
}

.fa-tasks:before {
    content: "\f0ae"
}

.fa-taxi:before {
    content: "\f1ba"
}

.fa-teamspeak:before {
    content: "\f4f9"
}

.fa-telegram:before {
    content: "\f2c6"
}

.fa-telegram-plane:before {
    content: "\f3fe"
}

.fa-tencent-weibo:before {
    content: "\f1d5"
}

.fa-tennis-ball:before {
    content: "\f45e"
}

.fa-terminal:before {
    content: "\f120"
}

.fa-text-height:before {
    content: "\f034"
}

.fa-text-width:before {
    content: "\f035"
}

.fa-th:before {
    content: "\f00a"
}

.fa-th-large:before {
    content: "\f009"
}

.fa-th-list:before {
    content: "\f00b"
}

.fa-themeisle:before {
    content: "\f2b2"
}

.fa-thermometer:before {
    content: "\f491"
}

.fa-thermometer-empty:before {
    content: "\f2cb"
}

.fa-thermometer-full:before {
    content: "\f2c7"
}

.fa-thermometer-half:before {
    content: "\f2c9"
}

.fa-thermometer-quarter:before {
    content: "\f2ca"
}

.fa-thermometer-three-quarters:before {
    content: "\f2c8"
}

.fa-thumbs-down:before {
    content: "\f165"
}

.fa-thumbs-up:before {
    content: "\f164"
}

.fa-thumbtack:before {
    content: "\f08d"
}

.fa-ticket:before {
    content: "\f145"
}

.fa-ticket-alt:before {
    content: "\f3ff"
}

.fa-times:before {
    content: "\f00d"
}

.fa-times-circle:before {
    content: "\f057"
}

.fa-times-hexagon:before {
    content: "\f2ee"
}

.fa-times-octagon:before {
    content: "\f2f0"
}

.fa-times-square:before {
    content: "\f2d3"
}

.fa-tint:before {
    content: "\f043"
}

.fa-toggle-off:before {
    content: "\f204"
}

.fa-toggle-on:before {
    content: "\f205"
}

.fa-trade-federation:before {
    content: "\f513"
}

.fa-trademark:before {
    content: "\f25c"
}

.fa-train:before {
    content: "\f238"
}

.fa-transgender:before {
    content: "\f224"
}

.fa-transgender-alt:before {
    content: "\f225"
}

.fa-trash:before {
    content: "\f1f8"
}

.fa-trash-alt:before {
    content: "\f2ed"
}

.fa-tree:before {
    content: "\f1bb"
}

.fa-tree-alt:before {
    content: "\f400"
}

.fa-trello:before {
    content: "\f181"
}

.fa-triangle:before {
    content: "\f2ec"
}

.fa-tripadvisor:before {
    content: "\f262"
}

.fa-trophy:before {
    content: "\f091"
}

.fa-trophy-alt:before {
    content: "\f2eb"
}

.fa-truck:before {
    content: "\f0d1"
}

.fa-truck-container:before {
    content: "\f4dc"
}

.fa-truck-couch:before {
    content: "\f4dd"
}

.fa-truck-loading:before {
    content: "\f4de"
}

.fa-truck-moving:before {
    content: "\f4df"
}

.fa-truck-ramp:before {
    content: "\f4e0"
}

.fa-tty:before {
    content: "\f1e4"
}

.fa-tumblr:before {
    content: "\f173"
}

.fa-tumblr-square:before {
    content: "\f174"
}

.fa-tv:before {
    content: "\f26c"
}

.fa-tv-retro:before {
    content: "\f401"
}

.fa-twitch:before {
    content: "\f1e8"
}

.fa-twitter:before {
    content: "\f099"
}

.fa-twitter-square:before {
    content: "\f081"
}

.fa-typo3:before {
    content: "\f42b"
}

.fa-uber:before {
    content: "\f402"
}

.fa-uikit:before {
    content: "\f403"
}

.fa-umbrella:before {
    content: "\f0e9"
}

.fa-underline:before {
    content: "\f0cd"
}

.fa-undo:before {
    content: "\f0e2"
}

.fa-undo-alt:before {
    content: "\f2ea"
}

.fa-uniregistry:before {
    content: "\f404"
}

.fa-universal-access:before {
    content: "\f29a"
}

.fa-university:before {
    content: "\f19c"
}

.fa-unlink:before {
    content: "\f127"
}

.fa-unlock:before {
    content: "\f09c"
}

.fa-unlock-alt:before {
    content: "\f13e"
}

.fa-untappd:before {
    content: "\f405"
}

.fa-upload:before {
    content: "\f093"
}

.fa-usb:before {
    content: "\f287"
}

.fa-usd-circle:before {
    content: "\f2e8"
}

.fa-usd-square:before {
    content: "\f2e9"
}

.fa-user:before {
    content: "\f007"
}

.fa-user-alt:before {
    content: "\f406"
}

.fa-user-alt-slash:before {
    content: "\f4fa"
}

.fa-user-astronaut:before {
    content: "\f4fb"
}

.fa-user-check:before {
    content: "\f4fc"
}

.fa-user-circle:before {
    content: "\f2bd"
}

.fa-user-clock:before {
    content: "\f4fd"
}

.fa-user-cog:before {
    content: "\f4fe"
}

.fa-user-edit:before {
    content: "\f4ff"
}

.fa-user-friends:before {
    content: "\f500"
}

.fa-user-graduate:before {
    content: "\f501"
}

.fa-user-lock:before {
    content: "\f502"
}

.fa-user-md:before {
    content: "\f0f0"
}

.fa-user-minus:before {
    content: "\f503"
}

.fa-user-ninja:before {
    content: "\f504"
}

.fa-user-plus:before {
    content: "\f234"
}

.fa-user-secret:before {
    content: "\f21b"
}

.fa-user-shield:before {
    content: "\f505"
}

.fa-user-slash:before {
    content: "\f506"
}

.fa-user-tag:before {
    content: "\f507"
}

.fa-user-tie:before {
    content: "\f508"
}

.fa-user-times:before {
    content: "\f235"
}

.fa-users:before {
    content: "\f0c0"
}

.fa-users-cog:before {
    content: "\f509"
}

.fa-ussunnah:before {
    content: "\f407"
}

.fa-utensil-fork:before {
    content: "\f2e3"
}

.fa-utensil-knife:before {
    content: "\f2e4"
}

.fa-utensil-spoon:before {
    content: "\f2e5"
}

.fa-utensils:before {
    content: "\f2e7"
}

.fa-utensils-alt:before {
    content: "\f2e6"
}

.fa-vaadin:before {
    content: "\f408"
}

.fa-venus:before {
    content: "\f221"
}

.fa-venus-double:before {
    content: "\f226"
}

.fa-venus-mars:before {
    content: "\f228"
}

.fa-viacoin:before {
    content: "\f237"
}

.fa-viadeo:before {
    content: "\f2a9"
}

.fa-viadeo-square:before {
    content: "\f2aa"
}

.fa-vial:before {
    content: "\f492"
}

.fa-vials:before {
    content: "\f493"
}

.fa-viber:before {
    content: "\f409"
}

.fa-video:before {
    content: "\f03d"
}

.fa-video-plus:before {
    content: "\f4e1"
}

.fa-video-slash:before {
    content: "\f4e2"
}

.fa-vimeo:before {
    content: "\f40a"
}

.fa-vimeo-square:before {
    content: "\f194"
}

.fa-vimeo-v:before {
    content: "\f27d"
}

.fa-vine:before {
    content: "\f1ca"
}

.fa-vk:before {
    content: "\f189"
}

.fa-vnv:before {
    content: "\f40b"
}

.fa-volleyball-ball:before {
    content: "\f45f"
}

.fa-volume-down:before {
    content: "\f027"
}

.fa-volume-mute:before {
    content: "\f2e2"
}

.fa-volume-off:before {
    content: "\f026"
}

.fa-volume-up:before {
    content: "\f028"
}

.fa-vuejs:before {
    content: "\f41f"
}

.fa-warehouse:before {
    content: "\f494"
}

.fa-warehouse-alt:before {
    content: "\f495"
}

.fa-watch:before {
    content: "\f2e1"
}

.fa-weibo:before {
    content: "\f18a"
}

.fa-weight:before {
    content: "\f496"
}

.fa-weixin:before {
    content: "\f1d7"
}

.fa-whatsapp:before {
    content: "\f232"
}

.fa-whatsapp-square:before {
    content: "\f40c"
}

.fa-wheelchair:before {
    content: "\f193"
}

.fa-whistle:before {
    content: "\f460"
}

.fa-whmcs:before {
    content: "\f40d"
}

.fa-wifi:before {
    content: "\f1eb"
}

.fa-wikipedia-w:before {
    content: "\f266"
}

.fa-window:before {
    content: "\f40e"
}

.fa-window-alt:before {
    content: "\f40f"
}

.fa-window-close:before {
    content: "\f410"
}

.fa-window-maximize:before {
    content: "\f2d0"
}

.fa-window-minimize:before {
    content: "\f2d1"
}

.fa-window-restore:before {
    content: "\f2d2"
}

.fa-windows:before {
    content: "\f17a"
}

.fa-wine-glass:before {
    content: "\f4e3"
}

.fa-wolf-pack-battalion:before {
    content: "\f514"
}

.fa-won-sign:before {
    content: "\f159"
}

.fa-wordpress:before {
    content: "\f19a"
}

.fa-wordpress-simple:before {
    content: "\f411"
}

.fa-wpbeginner:before {
    content: "\f297"
}

.fa-wpexplorer:before {
    content: "\f2de"
}

.fa-wpforms:before {
    content: "\f298"
}

.fa-wrench:before {
    content: "\f0ad"
}

.fa-x-ray:before {
    content: "\f497"
}

.fa-xbox:before {
    content: "\f412"
}

.fa-xing:before {
    content: "\f168"
}

.fa-xing-square:before {
    content: "\f169"
}

.fa-y-combinator:before {
    content: "\f23b"
}

.fa-yahoo:before {
    content: "\f19e"
}

.fa-yandex:before {
    content: "\f413"
}

.fa-yandex-international:before {
    content: "\f414"
}

.fa-yelp:before {
    content: "\f1e9"
}

.fa-yen-sign:before {
    content: "\f157"
}

.fa-yoast:before {
    content: "\f2b1"
}

.fa-youtube:before {
    content: "\f167"
}

.fa-youtube-square:before {
    content: "\f431"
}

.sr-only {
    border: 0;
    clip: rect(0,0,0,0);
    height: 1px;
    margin: -1px;
    overflow: hidden;
    padding: 0;
    position: absolute;
    width: 1px
}

.sr-only-focusable:active,.sr-only-focusable:focus {
    clip: auto;
    height: auto;
    margin: 0;
    overflow: visible;
    position: static;
    width: auto
}



.fab {
    font-family: FontAwesomeProBrands
}


.fal {
    font-weight: 300
}



.fal,.far {
    font-family: FontAwesomePro
}

.far {
    font-weight: 400
}



.fa,.fas {
    font-family: FontAwesomePro;
    font-weight: 900
}





















    
    .fa,.fab,.fal,.far,.fas {
    -moz-osx-font-smoothing: grayscale;
    -webkit-font-smoothing: antialiased;
    display: inline-block;
    font-style: normal;
    font-variant: normal;
    text-rendering: auto;
    line-height: 1
}

.fa-spin {
    animation: a 2s infinite linear
}

.fa-pulse {
    animation: a 1s infinite steps(8)
}

@keyframes a {
    0% {
        transform: rotate(0deg)
    }

    to {
        transform: rotate(1turn)
    }
}

.pull-left {
    float: left
}

.pull-right {
    float: right
}

.fa-rotate-90 {
  
    transform: rotate(90deg)
}

.fa-rotate-180 {
   
    transform: rotate(180deg)
}

.fa-rotate-270 {
  
    transform: rotate(270deg)
}

.fa-flip-horizontal {
   
    transform: scaleX(-1)
}

.fa-flip-vertical {
    transform: scaleY(-1)
}



.fa-flip-horizontal.fa-flip-vertical {
    transform: scale(-1)
}

:root .fa-flip-horizontal,:root .fa-flip-vertical,:root .fa-rotate-90,:root .fa-rotate-180,:root .fa-rotate-270 {
    -webkit-filter: none;
    filter: none
}

.fa-address-card:before {
    content: ""
}

.fa-alarm-clock:before {
    content: ""
}

.fa-algolia:before {
    content: ""
}

.fa-align-center:before {
    content: ""
}

.fa-align-justify:before {
    content: ""
}

.fa-align-left:before {
    content: ""
}

.fa-align-right:before {
    content: ""
}

.fa-allergies:before {
    content: ""
}

.fa-anchor:before {
    content: ""
}

.fa-android:before {
    content: ""
}

.fa-angle-double-down:before {
    content: ""
}

.fa-angle-double-left:before {
    content: ""
}

.fa-angle-double-right:before {
    content: ""
}

.fa-angle-double-up:before {
    content: ""
}

.fa-angle-down:before {
    content: ""
}

.fa-angle-left:before {
    content: ""
}

.fa-angle-right:before {
    content: ""
}

.fa-angle-up:before {
    content: ""
}

.fa-app-store:before {
    content: ""
}

.fa-app-store-ios:before {
    content: ""
}

.fa-apple:before {
    content: ""
}

.fa-archive:before {
    content: ""
}

.fa-arrow-alt-circle-down:before {
    content: ""
}

.fa-arrow-alt-circle-left:before {
    content: ""
}

.fa-arrow-alt-circle-right:before {
    content: ""
}

.fa-arrow-alt-circle-up:before {
    content: ""
}

.fa-arrow-alt-down:before {
    content: ""
}

.fa-arrow-alt-from-bottom:before {
    content: ""
}

.fa-arrow-alt-from-left:before {
    content: ""
}

.fa-arrow-alt-from-right:before {
    content: ""
}

.fa-arrow-alt-from-top:before {
    content: ""
}

.fa-arrow-alt-left:before {
    content: ""
}

.fa-arrow-alt-right:before {
    content: ""
}

.fa-arrow-alt-square-down:before {
    content: ""
}

.fa-arrow-alt-square-left:before {
    content: ""
}

.fa-arrow-alt-square-right:before {
    content: ""
}

.fa-arrow-alt-square-up:before {
    content: ""
}

.fa-arrow-alt-to-bottom:before {
    content: ""
}

.fa-arrow-alt-to-left:before {
    content: ""
}

.fa-arrow-alt-to-right:before {
    content: ""
}

.fa-arrow-alt-to-top:before {
    content: ""
}

.fa-arrow-alt-up:before {
    content: ""
}

.fa-arrow-circle-down:before {
    content: ""
}

.fa-arrow-circle-left:before {
    content: ""
}

.fa-arrow-circle-right:before {
    content: ""
}

.fa-arrow-circle-up:before {
    content: ""
}

.fa-arrow-down:before {
    content: ""
}

.fa-arrow-from-bottom:before {
    content: ""
}

.fa-arrow-from-left:before {
    content: ""
}

.fa-arrow-from-right:before {
    content: ""
}

.fa-arrow-from-top:before {
    content: ""
}

.fa-arrow-left:before {
    content: ""
}

.fa-arrow-right:before {
    content: ""
}

.fa-arrow-square-down:before {
    content: ""
}

.fa-arrow-square-left:before {
    content: ""
}

.fa-arrow-square-right:before {
    content: ""
}

.fa-arrow-square-up:before {
    content: ""
}

.fa-arrow-to-bottom:before {
    content: ""
}

.fa-arrow-to-left:before {
    content: ""
}

.fa-arrow-to-right:before {
    content: ""
}

.fa-arrow-to-top:before {
    content: ""
}

.fa-arrow-up:before {
    content: ""
}

.fa-arrows:before {
    content: ""
}

.fa-arrows-alt:before {
    content: ""
}

.fa-arrows-alt-h:before {
    content: ""
}

.fa-arrows-alt-v:before {
    content: ""
}

.fa-arrows-h:before {
    content: ""
}

.fa-arrows-v:before {
    content: ""
}

.fa-balance-scale:before {
    content: ""
}

.fa-ban:before {
    content: ""
}

.fa-barcode:before {
    content: ""
}

.fa-barcode-alt:before {
    content: ""
}

.fa-barcode-read:before {
    content: ""
}

.fa-barcode-scan:before {
    content: ""
}

.fa-bars:before {
    content: ""
}

.fa-bed:before {
    content: ""
}

.fa-bell:before {
    content: ""
}

.fa-bell-slash:before {
    content: ""
}

.fa-bicycle:before {
    content: ""
}

.fa-bimobject:before {
    content: ""
}

.fa-binoculars:before {
    content: ""
}

.fa-birthday-cake:before {
    content: ""
}

.fa-bity:before {
    content: ""
}

.fa-black-tie:before {
    content: ""
}

.fa-blanket:before {
    content: ""
}

.fa-blind:before {
    content: ""
}

.fa-bomb:before {
    content: ""
}

.fa-book:before {
    content: ""
}

.fa-book-heart:before {
    content: ""
}

.fa-bookmark:before {
    content: ""
}

.fa-box:before {
    content: ""
}

.fa-box-alt:before {
    content: ""
}

.fa-box-check:before {
    content: ""
}

.fa-box-fragile:before {
    content: ""
}

.fa-box-full:before {
    content: ""
}

.fa-box-heart:before {
    content: ""
}

.fa-box-open:before {
    content: ""
}

.fa-box-up:before {
    content: ""
}

.fa-box-usd:before {
    content: ""
}

.fa-boxes:before {
    content: ""
}

.fa-boxes-alt:before {
    content: ""
}

.fa-boxing-glove:before {
    content: ""
}

.fa-briefcase:before {
    content: ""
}

.fa-briefcase-medical:before {
    content: ""
}

.fa-browser:before {
    content: ""
}

.fa-btc:before {
    content: ""
}

.fa-bug:before {
    content: ""
}

.fa-building:before {
    content: ""
}

.fa-bullhorn:before {
    content: ""
}

.fa-bullseye:before {
    content: ""
}

.fa-burn:before {
    content: ""
}

.fa-buromobelexperte:before {
    content: ""
}

.fa-bus:before {
    content: ""
}

.fa-buysellads:before {
    content: ""
}

.fa-calculator:before {
    content: ""
}

.fa-calendar:before {
    content: ""
}

.fa-calendar-alt:before {
    content: ""
}

.fa-calendar-check:before {
    content: ""
}

.fa-calendar-edit:before {
    content: ""
}

.fa-calendar-exclamation:before {
    content: ""
}

.fa-calendar-minus:before {
    content: ""
}

.fa-calendar-plus:before {
    content: ""
}

.fa-calendar-times:before {
    content: ""
}

.fa-camera:before {
    content: ""
}

.fa-camera-alt:before {
    content: ""
}

.fa-camera-retro:before {
    content: ""
}

.fa-capsules:before {
    content: ""
}

.fa-car:before {
    content: ""
}

.fa-caret-circle-down:before {
    content: ""
}

.fa-caret-circle-left:before {
    content: ""
}

.fa-caret-circle-right:before {
    content: ""
}

.fa-caret-circle-up:before {
    content: ""
}

.fa-caret-down:before {
    content: ""
}

.fa-caret-left:before {
    content: ""
}

.fa-caret-right:before {
    content: ""
}

.fa-caret-square-down:before {
    content: ""
}

.fa-caret-square-left:before {
    content: ""
}

.fa-caret-square-right:before {
    content: ""
}

.fa-caret-square-up:before {
    content: ""
}

.fa-caret-up:before {
    content: ""
}

.fa-cart-arrow-down:before {
    content: ""
}

.fa-cart-plus:before {
    content: ""
}

.fa-cc-mastercard:before {
    content: ""
}

.fa-cc-visa:before {
    content: ""
}

.fa-certificate:before {
    content: ""
}

.fa-chart-area:before {
    content: ""
}

.fa-chart-bar:before {
    content: ""
}

.fa-chart-line:before {
    content: ""
}

.fa-chart-pie:before {
    content: ""
}

.fa-check:before {
    content: ""
}

.fa-check-circle:before {
    content: ""
}

.fa-check-square:before {
    content: ""
}

.fa-chevron-circle-down:before {
    content: ""
}

.fa-chevron-circle-left:before {
    content: ""
}

.fa-chevron-circle-right:before {
    content: ""
}

.fa-chevron-circle-up:before {
    content: ""
}

.fa-chevron-double-down:before {
    content: ""
}

.fa-chevron-double-left:before {
    content: ""
}

.fa-chevron-double-right:before {
    content: ""
}

.fa-chevron-double-up:before {
    content: ""
}

.fa-chevron-down:before {
    content: ""
}

.fa-chevron-left:before {
    content: ""
}

.fa-chevron-right:before {
    content: ""
}

.fa-chevron-square-down:before {
    content: ""
}

.fa-chevron-square-left:before {
    content: ""
}

.fa-chevron-square-right:before {
    content: ""
}

.fa-chevron-square-up:before {
    content: ""
}

.fa-chevron-up:before {
    content: ""
}

.fa-child:before {
    content: ""
}

.fa-chrome:before {
    content: ""
}

.fa-circle:before {
    content: ""
}

.fa-circle-notch:before {
    content: ""
}

.fa-clipboard:before {
    content: ""
}

.fa-clipboard-check:before {
    content: ""
}

.fa-clipboard-list:before {
    content: ""
}

.fa-clock:before {
    content: ""
}

.fa-clone:before {
    content: ""
}

.fa-closed-captioning:before {
    content: ""
}

.fa-club:before {
    content: ""
}

.fa-code:before {
    content: ""
}

.fa-code-branch:before {
    content: ""
}

.fa-code-commit:before {
    content: ""
}

.fa-code-merge:before {
    content: ""
}

.fa-codepen:before {
    content: ""
}

.fa-codiepie:before {
    content: ""
}

.fa-coffee:before {
    content: ""
}

.fa-cog:before {
    content: ""
}

.fa-cogs:before {
    content: ""
}

.fa-columns:before {
    content: ""
}

.fa-comment:before {
    content: ""
}

.fa-comment-alt:before {
    content: ""
}

.fa-comment-alt-check:before {
    content: ""
}

.fa-comment-alt-dots:before {
    content: ""
}

.fa-comment-alt-edit:before {
    content: ""
}

.fa-comment-alt-exclamation:before {
    content: ""
}

.fa-comment-alt-lines:before {
    content: ""
}

.fa-comment-alt-minus:before {
    content: ""
}

.fa-comment-alt-plus:before {
    content: ""
}

.fa-comment-alt-slash:before {
    content: ""
}

.fa-comment-alt-smile:before {
    content: ""
}

.fa-comment-alt-times:before {
    content: ""
}

.fa-comment-check:before {
    content: ""
}

.fa-comment-dots:before {
    content: ""
}

.fa-comment-edit:before {
    content: ""
}

.fa-comment-exclamation:before {
    content: ""
}

.fa-comment-lines:before {
    content: ""
}

.fa-comment-minus:before {
    content: ""
}

.fa-comment-plus:before {
    content: ""
}

.fa-comment-slash:before {
    content: ""
}

.fa-comment-smile:before {
    content: ""
}

.fa-comment-times:before {
    content: ""
}

.fa-comments:before {
    content: ""
}

.fa-comments-alt:before {
    content: ""
}

.fa-compass:before {
    content: ""
}

.fa-compress:before {
    content: ""
}

.fa-compress-alt:before {
    content: ""
}

.fa-compress-wide:before {
    content: ""
}

.fa-connectdevelop:before {
    content: ""
}

.fa-container-storage:before {
    content: ""
}

.fa-contao:before {
    content: ""
}

.fa-conveyor-belt:before {
    content: ""
}

.fa-conveyor-belt-alt:before {
    content: ""
}

.fa-copy:before {
    content: ""
}

.fa-copyright:before {
    content: ""
}

.fa-couch:before {
    content: ""
}

.fa-cpanel:before {
    content: ""
}

.fa-credit-card:before {
    content: ""
}

.fa-credit-card-blank:before {
    content: ""
}

.fa-credit-card-front:before {
    content: ""
}

.fa-cricket:before {
    content: ""
}

.fa-crop:before {
    content: ""
}

.fa-crosshairs:before {
    content: ""
}

.fa-cube:before {
    content: ""
}

.fa-cubes:before {
    content: ""
}

.fa-curling:before {
    content: ""
}

.fa-cut:before {
    content: ""
}

.fa-cuttlefish:before {
    content: ""
}

.fa-d-and-d:before {
    content: ""
}

.fa-dashcube:before {
    content: ""
}

.fa-database:before {
    content: ""
}

.fa-deaf:before {
    content: ""
}

.fa-delicious:before {
    content: ""
}

.fa-deploydog:before {
    content: ""
}

.fa-deskpro:before {
    content: ""
}

.fa-desktop:before {
    content: ""
}

.fa-desktop-alt:before {
    content: ""
}

.fa-deviantart:before {
    content: ""
}

.fa-diagnoses:before {
    content: ""
}

.fa-diamond:before {
    content: ""
}

.fa-digg:before {
    content: ""
}

.fa-digital-ocean:before {
    content: ""
}

.fa-discord:before {
    content: ""
}

.fa-discourse:before {
    content: ""
}

.fa-dna:before {
    content: ""
}

.fa-dochub:before {
    content: ""
}

.fa-docker:before {
    content: ""
}

.fa-dollar-sign:before {
    content: ""
}

.fa-dolly:before {
    content: ""
}

.fa-dolly-empty:before {
    content: ""
}

.fa-dolly-flatbed:before {
    content: ""
}

.fa-dolly-flatbed-alt:before {
    content: ""
}

.fa-dolly-flatbed-empty:before {
    content: ""
}

.fa-donate:before {
    content: ""
}

.fa-dot-circle:before {
    content: ""
}

.fa-dove:before {
    content: ""
}

.fa-download:before {
    content: ""
}

.fa-draft2digital:before {
    content: ""
}

.fa-dropbox:before {
    content: ""
}

.fa-drupal:before {
    content: ""
}

.fa-dumbbell:before {
    content: ""
}

.fa-dyalog:before {
    content: ""
}

.fa-earlybirds:before {
    content: ""
}

.fa-ebay:before {
    content: ""
}

.fa-edge:before {
    content: ""
}

.fa-edit:before {
    content: ""
}

.fa-eject:before {
    content: ""
}

.fa-elementor:before {
    content: ""
}

.fa-ellipsis-h:before {
    content: ""
}

.fa-ellipsis-h-alt:before {
    content: ""
}

.fa-ellipsis-v:before {
    content: ""
}

.fa-ellipsis-v-alt:before {
    content: ""
}

.fa-ember:before {
    content: ""
}

.fa-empire:before {
    content: ""
}

.fa-envelope:before {
    content: ""
}

.fa-envelope-open:before {
    content: ""
}

.fa-envelope-square:before {
    content: ""
}

.fa-envira:before {
    content: ""
}

.fa-eraser:before {
    content: ""
}

.fa-erlang:before {
    content: ""
}

.fa-ethereum:before {
    content: ""
}

.fa-etsy:before {
    content: ""
}

.fa-euro-sign:before {
    content: ""
}

.fa-exchange:before {
    content: ""
}

.fa-exchange-alt:before {
    content: ""
}

.fa-exclamation:before {
    content: ""
}

.fa-exclamation-circle:before {
    content: ""
}

.fa-exclamation-square:before {
    content: ""
}

.fa-exclamation-triangle:before {
    content: ""
}

.fa-expand:before {
    content: ""
}

.fa-expand-alt:before {
    content: ""
}

.fa-expand-arrows:before {
    content: ""
}

.fa-expand-arrows-alt:before {
    content: ""
}

.fa-expand-wide:before {
    content: ""
}

.fa-expeditedssl:before {
    content: ""
}

.fa-external-link:before {
    content: ""
}

.fa-external-link-alt:before {
    content: ""
}

.fa-external-link-square:before {
    content: ""
}

.fa-external-link-square-alt:before {
    content: ""
}

.fa-eye:before {
    content: ""
}

.fa-eye-dropper:before {
    content: ""
}

.fa-eye-slash:before {
    content: ""
}

.fa-facebook:before {
    content: ""
}

.fa-facebook-f:before {
    content: ""
}

.fa-facebook-messenger:before {
    content: ""
}

.fa-facebook-square:before {
    content: ""
}

.fa-fast-backward:before {
    content: ""
}

.fa-fast-forward:before {
    content: ""
}

.fa-fax:before {
    content: ""
}

.fa-female:before {
    content: ""
}

.fa-field-hockey:before {
    content: ""
}

.fa-fighter-jet:before {
    content: ""
}

.fa-file:before {
    content: ""
}

.fa-film:before {
    content: ""
}

.fa-film-alt:before {
    content: ""
}

.fa-filter:before {
    content: ""
}

.fa-fire:before {
    content: ""
}

.fa-fire-extinguisher:before {
    content: ""
}

.fa-firefox:before {
    content: ""
}

.fa-first-aid:before {
    content: ""
}

.fa-first-order:before {
    content: ""
}

.fa-first-order-alt:before {
    content: ""
}

.fa-firstdraft:before {
    content: ""
}

.fa-flag:before {
    content: ""
}

.fa-flag-checkered:before {
    content: ""
}

.fa-flask:before {
    content: ""
}

.fa-flickr:before {
    content: ""
}

.fa-flipboard:before {
    content: ""
}

.fa-fly:before {
    content: ""
}

.fa-folder:before {
    content: ""
}

.fa-folder-open:before {
    content: ""
}

.fa-forumbee:before {
    content: ""
}

.fa-forward:before {
    content: ""
}

.fa-freebsd:before {
    content: ""
}

.fa-gift:before {
    content: ""
}

.fa-gitlab:before {
    content: ""
}

.fa-gitter:before {
    content: ""
}

.fa-glass-martini:before {
    content: ""
}

.fa-glide:before {
    content: ""
}

.fa-glide-g:before {
    content: ""
}

.fa-globe:before {
    content: ""
}

.fa-gofore:before {
    content: ""
}

.fa-golf-ball:before {
    content: ""
}

.fa-golf-club:before {
    content: ""
}

.fa-goodreads:before {
    content: ""
}

.fa-goodreads-g:before {
    content: ""
}

.fa-google:before {
    content: ""
}

.fa-google-drive:before {
    content: ""
}

.fa-google-play:before {
    content: ""
}

.fa-google-plus:before {
    content: ""
}

.fa-google-plus-g:before {
    content: ""
}

.fa-google-plus-square:before {
    content: ""
}

.fa-google-wallet:before {
    content: ""
}

.fa-graduation-cap:before {
    content: ""
}

.fa-gratipay:before {
    content: ""
}

.fa-grav:before {
    content: ""
}

.fa-gripfire:before {
    content: ""
}

.fa-grunt:before {
    content: ""
}

.fa-gulp:before {
    content: ""
}

.fa-h-square:before {
    content: ""
}

.fa-hashtag:before {
    content: ""
}

.fa-hdd:before {
    content: ""
}

.fa-heading:before {
    content: ""
}

.fa-headphones:before {
    content: ""
}

.fa-heart:before {
    content: ""
}

.fa-heart-circle:before {
    content: ""
}

.fa-heart-square:before {
    content: ""
}

.fa-heartbeat:before {
    content: ""
}

.fa-hexagon:before {
    content: ""
}

.fa-hips:before {
    content: ""
}

.fa-hire-a-helper:before {
    content: ""
}

.fa-history:before {
    content: ""
}

.fa-hockey-puck:before {
    content: ""
}

.fa-hockey-sticks:before {
    content: ""
}

.fa-home:before {
    content: ""
}

.fa-home-heart:before {
    content: ""
}

.fa-hooli:before {
    content: ""
}

.fa-hospital:before {
    content: ""
}

.fa-hospital-alt:before {
    content: ""
}

.fa-hospital-symbol:before {
    content: ""
}

.fa-hotjar:before {
    content: ""
}

.fa-hourglass:before {
    content: ""
}

.fa-hourglass-end:before {
    content: ""
}

.fa-hourglass-half:before {
    content: ""
}

.fa-hourglass-start:before {
    content: ""
}

.fa-houzz:before {
    content: ""
}

.fa-html5:before {
    content: ""
}

.fa-hubspot:before {
    content: ""
}

.fa-i-cursor:before {
    content: ""
}

.fa-id-badge:before {
    content: ""
}

.fa-id-card:before {
    content: ""
}

.fa-id-card-alt:before {
    content: ""
}

.fa-image:before {
    content: ""
}

.fa-images:before {
    content: ""
}

.fa-inbox:before {
    content: ""
}

.fa-inbox-in:before {
    content: ""
}

.fa-inbox-out:before {
    content: ""
}

.fa-indent:before {
    content: ""
}

.fa-industry:before {
    content: ""
}

.fa-industry-alt:before {
    content: ""
}

.fa-info:before {
    content: ""
}

.fa-info-circle:before {
    content: ""
}

.fa-info-square:before {
    content: ""
}

.fa-instagram:before {
    content: ""
}

.fa-inventory:before {
    content: ""
}

.fa-js:before {
    content: ""
}

.fa-js-square:before {
    content: ""
}

.fa-key:before {
    content: ""
}

.fa-keybase:before {
    content: ""
}

.fa-keyboard:before {
    content: ""
}

.fa-keycdn:before {
    content: ""
}

.fa-kickstarter:before {
    content: ""
}

.fa-kickstarter-k:before {
    content: ""
}

.fa-korvue:before {
    content: ""
}

.fa-lamp:before {
    content: ""
}

.fa-language:before {
    content: ""
}

.fa-laptop:before {
    content: ""
}

.fa-laravel:before {
    content: ""
}

.fa-lastfm:before {
    content: ""
}

.fa-lastfm-square:before {
    content: ""
}

.fa-leaf:before {
    content: ""
}

.fa-leaf-heart:before {
    content: ""
}

.fa-leanpub:before {
    content: ""
}

.fa-lemon:before {
    content: ""
}

.fa-less:before {
    content: ""
}

.fa-level-down:before {
    content: ""
}

.fa-level-down-alt:before {
    content: ""
}

.fa-level-up:before {
    content: ""
}

.fa-level-up-alt:before {
    content: ""
}

.fa-life-ring:before {
    content: ""
}

.fa-lightbulb:before {
    content: ""
}

.fa-line:before {
    content: ""
}

.fa-link:before {
    content: ""
}

.fa-linkedin:before {
    content: ""
}

.fa-linkedin-in:before {
    content: ""
}

.fa-linode:before {
    content: ""
}

.fa-linux:before {
    content: ""
}

.fa-lira-sign:before {
    content: ""
}

.fa-list:before {
    content: ""
}

.fa-list-alt:before {
    content: ""
}

.fa-list-ol:before {
    content: ""
}

.fa-list-ul:before {
    content: ""
}

.fa-location-arrow:before {
    content: ""
}

.fa-lock:before {
    content: ""
}

.fa-lock-alt:before {
    content: ""
}

.fa-lock-open:before {
    content: ""
}

.fa-lock-open-alt:before {
    content: ""
}

.fa-long-arrow-alt-down:before {
    content: ""
}

.fa-long-arrow-alt-left:before {
    content: ""
}

.fa-long-arrow-alt-right:before {
    content: ""
}

.fa-long-arrow-alt-up:before {
    content: ""
}

.fa-long-arrow-down:before {
    content: ""
}

.fa-long-arrow-left:before {
    content: ""
}

.fa-long-arrow-right:before {
    content: ""
}

.fa-long-arrow-up:before {
    content: ""
}

.fa-loveseat:before {
    content: ""
}

.fa-low-vision:before {
    content: ""
}

.fa-luchador:before {
    content: ""
}

.fa-lyft:before {
    content: ""
}

.fa-magic:before {
    content: ""
}

.fa-magnet:before {
    content: ""
}

.fa-male:before {
    content: ""
}

.fa-mandalorian:before {
    content: ""
}

.fa-map:before {
    content: ""
}

.fa-map-marker:before {
    content: ""
}

.fa-map-marker-alt:before {
    content: ""
}

.fa-map-pin:before {
    content: ""
}

.fa-map-signs:before {
    content: ""
}

.fa-mars:before {
    content: ""
}

.fa-mars-double:before {
    content: ""
}

.fa-mars-stroke:before {
    content: ""
}

.fa-mars-stroke-h:before {
    content: ""
}

.fa-mars-stroke-v:before {
    content: ""
}

.fa-mastodon:before {
    content: ""
}

.fa-maxcdn:before {
    content: ""
}

.fa-medapps:before {
    content: ""
}

.fa-medium:before {
    content: ""
}

.fa-medium-m:before {
    content: ""
}

.fa-medkit:before {
    content: ""
}

.fa-medrt:before {
    content: ""
}

.fa-meetup:before {
    content: ""
}

.fa-meh:before {
    content: ""
}

.fa-mercury:before {
    content: ""
}

.fa-microchip:before {
    content: ""
}

.fa-microphone:before {
    content: ""
}

.fa-microphone-alt:before {
    content: ""
}

.fa-microphone-slash:before {
    content: ""
}

.fa-microsoft:before {
    content: ""
}

.fa-minus:before {
    content: ""
}

.fa-minus-circle:before {
    content: ""
}

.fa-minus-hexagon:before {
    content: ""
}

.fa-minus-octagon:before {
    content: ""
}

.fa-minus-square:before {
    content: ""
}

.fa-mix:before {
    content: ""
}

.fa-mixcloud:before {
    content: ""
}

.fa-mizuni:before {
    content: ""
}

.fa-mobile:before {
    content: ""
}

.fa-mobile-alt:before {
    content: ""
}

.fa-mobile-android:before {
    content: ""
}

.fa-mobile-android-alt:before {
    content: ""
}

.fa-modx:before {
    content: ""
}

.fa-monero:before {
    content: ""
}

.fa-money-bill:before {
    content: ""
}

.fa-money-bill-alt:before {
    content: ""
}

.fa-moon:before {
    content: ""
}

.fa-motorcycle:before {
    content: ""
}

.fa-mouse-pointer:before {
    content: ""
}

.fa-music:before {
    content: ""
}

.fa-newspaper:before {
    content: ""
}

.fa-notes-medical:before {
    content: ""
}

.fa-npm:before {
    content: ""
}

.fa-object-group:before {
    content: ""
}

.fa-object-ungroup:before {
    content: ""
}

.fa-octagon:before {
    content: ""
}

.fa-old-republic:before {
    content: ""
}

.fa-openid:before {
    content: ""
}

.fa-optin-monster:before {
    content: ""
}

.fa-osi:before {
    content: ""
}

.fa-outdent:before {
    content: ""
}

.fa-page4:before {
    content: ""
}

.fa-pagelines:before {
    content: ""
}

.fa-paint-brush:before {
    content: ""
}

.fa-palfed:before {
    content: ""
}

.fa-pallet:before {
    content: ""
}

.fa-pallet-alt:before {
    content: ""
}

.fa-paper-plane:before {
    content: ""
}

.fa-paperclip:before {
    content: ""
}

.fa-parachute-box:before {
    content: ""
}

.fa-paragraph:before {
    content: ""
}

.fa-paste:before {
    content: ""
}

.fa-patreon:before {
    content: ""
}

.fa-pause:before {
    content: ""
}

.fa-pause-circle:before {
    content: ""
}

.fa-paw:before {
    content: ""
}

.fa-paypal:before {
    content: ""
}

.fa-pen:before {
    content: ""
}

.fa-pen-alt:before {
    content: ""
}

.fa-pen-square:before {
    content: ""
}

.fa-pencil:before {
    content: ""
}

.fa-pencil-alt:before {
    content: ""
}

.fa-pennant:before {
    content: ""
}

.fa-people-carry:before {
    content: ""
}

.fa-percent:before {
    content: ""
}

.fa-periscope:before {
    content: ""
}

.fa-person-carry:before {
    content: ""
}

.fa-person-dolly:before {
    content: ""
}

.fa-person-dolly-empty:before {
    content: ""
}

.fa-phabricator:before {
    content: ""
}

.fa-phone:before {
    content: ""
}

.fa-phone-plus:before {
    content: ""
}

.fa-phone-slash:before {
    content: ""
}

.fa-phone-square:before {
    content: ""
}

.fa-phone-volume:before {
    content: ""
}

.fa-php:before {
    content: ""
}

.fa-pied-piper:before {
    content: ""
}

.fa-pied-piper-alt:before {
    content: ""
}

.fa-pied-piper-hat:before {
    content: ""
}

.fa-pied-piper-pp:before {
    content: ""
}

.fa-piggy-bank:before {
    content: ""
}

.fa-pills:before {
    content: ""
}

.fa-pinterest:before {
    content: ""
}

.fa-pinterest-p:before {
    content: ""
}

.fa-pinterest-square:before {
    content: ""
}

.fa-plane:before {
    content: ""
}

.fa-plane-alt:before {
    content: ""
}

.fa-play:before {
    content: ""
}

.fa-play-circle:before {
    content: ""
}

.fa-playstation:before {
    content: ""
}

.fa-plug:before {
    content: ""
}

.fa-plus:before {
    content: ""
}

.fa-plus-circle:before {
    content: ""
}

.fa-plus-hexagon:before {
    content: ""
}

.fa-plus-octagon:before {
    content: ""
}

.fa-plus-square:before {
    content: ""
}

.fa-podcast:before {
    content: ""
}

.fa-poo:before {
    content: ""
}

.fa-portrait:before {
    content: ""
}

.fa-pound-sign:before {
    content: ""
}

.fa-power-off:before {
    content: ""
}

.fa-prescription-bottle:before {
    content: ""
}

.fa-prescription-bottle-alt:before {
    content: ""
}

.fa-print:before {
    content: ""
}

.fa-procedures:before {
    content: ""
}

.fa-product-hunt:before {
    content: ""
}

.fa-pushed:before {
    content: ""
}

.fa-puzzle-piece:before {
    content: ""
}

.fa-python:before {
    content: ""
}

.fa-qq:before {
    content: ""
}

.fa-qrcode:before {
    content: ""
}

.fa-question:before {
    content: ""
}

.fa-question-circle:before {
    content: ""
}

.fa-question-square:before {
    content: ""
}

.fa-quidditch:before {
    content: ""
}

.fa-quinscape:before {
    content: ""
}

.fa-quora:before {
    content: ""
}

.fa-quote-left:before {
    content: ""
}

.fa-quote-right:before {
    content: ""
}

.fa-r-project:before {
    content: ""
}

.fa-racquet:before {
    content: ""
}

.fa-ramp-loading:before {
    content: ""
}

.fa-random:before {
    content: ""
}

.fa-ravelry:before {
    content: ""
}

.fa-react:before {
    content: ""
}

.fa-readme:before {
    content: ""
}

.fa-rebel:before {
    content: ""
}

.fa-rectangle-landscape:before {
    content: ""
}

.fa-rectangle-portrait:before {
    content: ""
}

.fa-rectangle-wide:before {
    content: ""
}

.fa-recycle:before {
    content: ""
}

.fa-red-river:before {
    content: ""
}

.fa-redo:before {
    content: ""
}

.fa-redo-alt:before {
    content: ""
}

.fa-registered:before {
    content: ""
}

.fa-rendact:before {
    content: ""
}

.fa-renren:before {
    content: ""
}

.fa-repeat:before {
    content: ""
}

.fa-repeat-1:before {
    content: ""
}

.fa-repeat-1-alt:before {
    content: ""
}

.fa-repeat-alt:before {
    content: ""
}

.fa-reply:before {
    content: ""
}

.fa-reply-all:before {
    content: ""
}

.fa-replyd:before {
    content: ""
}

.fa-researchgate:before {
    content: ""
}

.fa-resolving:before {
    content: ""
}

.fa-retweet:before {
    content: ""
}

.fa-retweet-alt:before {
    content: ""
}

.fa-ribbon:before {
    content: ""
}

.fa-road:before {
    content: ""
}

.fa-rocket:before {
    content: ""
}

.fa-rocketchat:before {
    content: ""
}

.fa-rockrms:before {
    content: ""
}

.fa-route:before {
    content: ""
}

.fa-rss:before {
    content: ""
}

.fa-rss-square:before {
    content: ""
}

.fa-scanner:before {
    content: ""
}

.fa-schlix:before {
    content: ""
}

.fa-scribd:before {
    content: ""
}

.fa-scrubber:before {
    content: ""
}

.fa-search:before {
    content: ""
}

.fa-search-minus:before {
    content: ""
}

.fa-search-plus:before {
    content: ""
}

.fa-searchengin:before {
    content: ""
}

.fa-seedling:before {
    content: ""
}

.fa-sellcast:before {
    content: ""
}

.fa-sellsy:before {
    content: ""
}

.fa-server:before {
    content: ""
}

.fa-servicestack:before {
    content: ""
}

.fa-share:before {
    content: ""
}

.fa-share-all:before {
    content: ""
}

.fa-share-alt:before {
    content: ""
}

.fa-share-alt-square:before {
    content: ""
}

.fa-share-square:before {
    content: ""
}

.fa-shekel-sign:before {
    content: ""
}

.fa-shield:before {
    content: ""
}

.fa-shield-alt:before {
    content: ""
}

.fa-shield-check:before {
    content: ""
}

.fa-ship:before {
    content: ""
}

.fa-shipping-fast:before {
    content: ""
}

.fa-shipping-timed:before {
    content: ""
}

.fa-shirtsinbulk:before {
    content: ""
}

.fa-shopping-bag:before {
    content: ""
}

.fa-shopping-basket:before {
    content: ""
}

.fa-shopping-cart:before {
    content: ""
}

.fa-shower:before {
    content: ""
}

.fa-shuttlecock:before {
    content: ""
}

.fa-sign:before {
    content: ""
}

.fa-sign-in:before {
    content: ""
}

.fa-sign-in-alt:before {
    content: ""
}

.fa-sign-language:before {
    content: ""
}

.fa-sign-out:before {
    content: ""
}

.fa-sign-out-alt:before {
    content: ""
}

.fa-signal:before {
    content: ""
}

.fa-simplybuilt:before {
    content: ""
}

.fa-sistrix:before {
    content: ""
}

.fa-sitemap:before {
    content: ""
}

.fa-sith:before {
    content: ""
}

.fa-skyatlas:before {
    content: ""
}

.fa-skype:before {
    content: ""
}

.fa-slack:before {
    content: ""
}

.fa-slack-hash:before {
    content: ""
}

.fa-sliders-h:before {
    content: ""
}

.fa-sliders-h-square:before {
    content: ""
}

.fa-sliders-v:before {
    content: ""
}

.fa-sliders-v-square:before {
    content: ""
}

.fa-slideshare:before {
    content: ""
}

.fa-smile:before {
    content: ""
}

.fa-smile-plus:before {
    content: ""
}

.fa-smoking:before {
    content: ""
}

.fa-snapchat:before {
    content: ""
}

.fa-snapchat-ghost:before {
    content: ""
}

.fa-snapchat-square:before {
    content: ""
}

.fa-snowflake:before {
    content: ""
}

.fa-sort:before {
    content: ""
}

.fa-sort-alpha-down:before {
    content: ""
}

.fa-sort-alpha-up:before {
    content: ""
}

.fa-sort-amount-down:before {
    content: ""
}

.fa-sort-amount-up:before {
    content: ""
}

.fa-sort-down:before {
    content: ""
}

.fa-sort-numeric-down:before {
    content: ""
}

.fa-sort-numeric-up:before {
    content: ""
}

.fa-sort-up:before {
    content: ""
}

.fa-soundcloud:before {
    content: ""
}

.fa-space-shuttle:before {
    content: ""
}

.fa-spade:before {
    content: ""
}

.fa-speakap:before {
    content: ""
}

.fa-spinner:before {
    content: ""
}

.fa-spinner-third:before {
    content: ""
}

.fa-spotify:before {
    content: ""
}

.fa-square:before {
    content: ""
}

.fa-square-full:before {
    content: ""
}

.fa-stack-exchange:before {
    content: ""
}

.fa-stack-overflow:before {
    content: ""
}

.fa-star:before {
    content: ""
}

.fa-star-exclamation:before {
    content: ""
}

.fa-star-half:before {
    content: ""
}

.fa-staylinked:before {
    content: ""
}

.fa-steam:before {
    content: ""
}

.fa-steam-square:before {
    content: ""
}

.fa-steam-symbol:before {
    content: ""
}

.fa-step-backward:before {
    content: ""
}

.fa-step-forward:before {
    content: ""
}

.fa-stethoscope:before {
    content: ""
}

.fa-sticker-mule:before {
    content: ""
}

.fa-sticky-note:before {
    content: ""
}

.fa-stop:before {
    content: ""
}

.fa-stop-circle:before {
    content: ""
}

.fa-stopwatch:before {
    content: ""
}

.fa-strava:before {
    content: ""
}

.fa-street-view:before {
    content: ""
}

.fa-strikethrough:before {
    content: ""
}

.fa-stripe:before {
    content: ""
}

.fa-stripe-s:before {
    content: ""
}

.fa-studiovinari:before {
    content: ""
}

.fa-stumbleupon:before {
    content: ""
}

.fa-stumbleupon-circle:before {
    content: ""
}

.fa-subscript:before {
    content: ""
}

.fa-subway:before {
    content: ""
}

.fa-suitcase:before {
    content: ""
}

.fa-sun:before {
    content: ""
}

.fa-superpowers:before {
    content: ""
}

.fa-superscript:before {
    content: ""
}

.fa-supple:before {
    content: ""
}

.fa-sync:before {
    content: ""
}

.fa-sync-alt:before {
    content: ""
}

.fa-syringe:before {
    content: ""
}

.fa-table:before {
    content: ""
}

.fa-table-tennis:before {
    content: ""
}

.fa-tablet:before {
    content: ""
}

.fa-tablet-alt:before {
    content: ""
}

.fa-tablet-android:before {
    content: ""
}

.fa-tablet-android-alt:before {
    content: ""
}

.fa-tablet-rugged:before {
    content: ""
}

.fa-tablets:before {
    content: ""
}

.fa-tachometer:before {
    content: ""
}

.fa-tachometer-alt:before {
    content: ""
}

.fa-tag:before {
    content: ""
}

.fa-tags:before {
    content: ""
}

.fa-tape:before {
    content: ""
}

.fa-tasks:before {
    content: ""
}

.fa-teamspeak:before {
    content: ""
}

.fa-telegram:before {
    content: ""
}

.fa-telegram-plane:before {
    content: ""
}

.fa-tencent-weibo:before {
    content: ""
}

.fa-tennis-ball:before {
    content: ""
}

.fa-terminal:before {
    content: ""
}

.fa-text-height:before {
    content: ""
}

.fa-text-width:before {
    content: ""
}

.fa-th:before {
    content: ""
}

.fa-th-large:before {
    content: ""
}

.fa-th-list:before {
    content: ""
}

.fa-themeisle:before {
    content: ""
}

.fa-thumbs-down:before {
    content: ""
}

.fa-thumbs-up:before {
    content: ""
}

.fa-thumbtack:before {
    content: ""
}

.fa-ticket:before {
    content: ""
}

.fa-ticket-alt:before {
    content: ""
}

.fa-times:before {
    content: ""
}

.fa-times-circle:before {
    content: ""
}

.fa-times-hexagon:before {
    content: ""
}

.fa-times-octagon:before {
    content: ""
}

.fa-times-square:before {
    content: ""
}

.fa-tint:before {
    content: ""
}

.fa-toggle-off:before {
    content: ""
}

.fa-toggle-on:before {
    content: ""
}

.fa-trade-federation:before {
    content: ""
}

.fa-trademark:before {
    content: ""
}

.fa-train:before {
    content: ""
}

.fa-transgender:before {
    content: ""
}

.fa-transgender-alt:before {
    content: ""
}

.fa-trash:before {
    content: ""
}

.fa-trash-alt:before {
    content: ""
}

.fa-tree:before {
    content: ""
}

.fa-tree-alt:before {
    content: ""
}

.fa-trello:before {
    content: ""
}

.fa-triangle:before {
    content: ""
}

.fa-tripadvisor:before {
    content: ""
}

.fa-trophy:before {
    content: ""
}

.fa-trophy-alt:before {
    content: ""
}

.fa-truck:before {
    content: ""
}

.fa-truck-container:before {
    content: ""
}

.fa-truck-couch:before {
    content: ""
}

.fa-truck-loading:before {
    content: ""
}

.fa-truck-moving:before {
    content: ""
}

.fa-truck-ramp:before {
    content: ""
}

.fa-tty:before {
    content: ""
}

.fa-tumblr:before {
    content: ""
}

.fa-tumblr-square:before {
    content: ""
}

.fa-tv:before {
    content: ""
}

.fa-tv-retro:before {
    content: ""
}

.fa-twitch:before {
    content: ""
}

.fa-twitter:before {
    content: ""
}

.fa-twitter-square:before {
    content: ""
}

.fa-typo3:before {
    content: ""
}

.fa-uber:before {
    content: ""
}

.fa-uikit:before {
    content: ""
}

.fa-umbrella:before {
    content: ""
}

.fa-underline:before {
    content: ""
}

.fa-undo:before {
    content: ""
}

.fa-undo-alt:before {
    content: ""
}

.fa-uniregistry:before {
    content: ""
}

.fa-universal-access:before {
    content: ""
}

.fa-university:before {
    content: ""
}

.fa-unlink:before {
    content: ""
}

.fa-unlock:before {
    content: ""
}

.fa-unlock-alt:before {
    content: ""
}

.fa-untappd:before {
    content: ""
}

.fa-upload:before {
    content: ""
}

.fa-usb:before {
    content: ""
}

.fa-usd-circle:before {
    content: ""
}

.fa-usd-square:before {
    content: ""
}

.fa-user:before {
    content: ""
}

.fa-user-alt:before {
    content: ""
}

.fa-user-alt-slash:before {
    content: ""
}

.fa-user-astronaut:before {
    content: ""
}

.fa-user-check:before {
    content: ""
}

.fa-user-circle:before {
    content: ""
}

.fa-user-clock:before {
    content: ""
}

.fa-user-cog:before {
    content: ""
}

.fa-user-edit:before {
    content: ""
}

.fa-user-friends:before {
    content: ""
}

.fa-user-graduate:before {
    content: ""
}

.fa-user-lock:before {
    content: ""
}

.fa-user-md:before {
    content: ""
}

.fa-user-minus:before {
    content: ""
}

.fa-user-ninja:before {
    content: ""
}

.fa-user-plus:before {
    content: ""
}

.fa-user-secret:before {
    content: ""
}

.fa-user-shield:before {
    content: ""
}

.fa-user-slash:before {
    content: ""
}

.fa-user-tag:before {
    content: ""
}

.fa-user-tie:before {
    content: ""
}

.fa-user-times:before {
    content: ""
}

.fa-users:before {
    content: ""
}

.fa-users-cog:before {
    content: ""
}

.fa-ussunnah:before {
    content: ""
}

.fa-utensil-fork:before {
    content: ""
}

.fa-utensil-knife:before {
    content: ""
}

.fa-utensil-spoon:before {
    content: ""
}

.fa-utensils:before {
    content: ""
}

.fa-utensils-alt:before {
    content: ""
}

.fa-video:before {
    content: ""
}

.fa-video-plus:before {
    content: ""
}

.fa-video-slash:before {
    content: ""
}

.fa-vimeo:before {
    content: ""
}

.fa-vimeo-square:before {
    content: ""
}

.fa-vimeo-v:before {
    content: ""
}

.fa-volleyball-ball:before {
    content: ""
}

.fa-volume-down:before {
    content: ""
}

.fa-volume-mute:before {
    content: ""
}

.fa-volume-off:before {
    content: ""
}

.fa-volume-up:before {
    content: ""
}

.fa-warehouse:before {
    content: ""
}

.fa-warehouse-alt:before {
    content: ""
}

.fa-watch:before {
    content: ""
}

.fa-weibo:before {
    content: ""
}

.fa-weight:before {
    content: ""
}

.fa-weixin:before {
    content: ""
}

.fa-whatsapp:before {
    content: url(https://img.icons8.com/pastel-glyph/2x/whatsapp--v2.png);
    
}

.customLink{
    height: "30px";
    width: "30px";
}

.fa-whatsapp-square:before {
    content: ""
}

.fa-wheelchair:before {
    content: ""
}

.fa-whistle:before {
    content: ""
}

.fa-whmcs:before {
    content: ""
}

.fa-wifi:before {
    content: ""
}

.fa-wikipedia-w:before {
    content: ""
}

.fa-window:before {
    content: ""
}

.fa-window-alt:before {
    content: ""
}

.fa-window-close:before {
    content: ""
}

.fa-window-maximize:before {
    content: ""
}

.fa-window-minimize:before {
    content: ""
}

.fa-window-restore:before {
    content: ""
}

.fa-windows:before {
    content: ""
}

.fa-wine-glass:before {
    content: ""
}

.fa-won-sign:before {
    content: ""
}

.fa-wrench:before {
    content: ""
}

.fa-x-ray:before {
    content: ""
}

.fa-xing:before {
    content: ""
}

.fa-xing-square:before {
    content: ""
}

.fa-y-combinator:before {
    content: ""
}

.fa-yandex-international:before {
    content: ""
}

.fa-youtube:before,.fa-youtube-play:before {
    content: ""
}

.fa-youtube-square:before {
    content: ""
}

.sr-only {
    border: 0;
    clip: rect(0,0,0,0);
    height: 1px;
    margin: -1px;
    overflow: hidden;
    padding: 0;
    position: absolute;
    width: 1px
}

.sr-only-focusable:active,.sr-only-focusable:focus {
    clip: auto;
    height: auto;
    margin: 0;
    overflow: visible;
    position: static;
    width: auto
}

.fa.fa-facebook:before {
    content: ""
}

.fa.fa-money:before {
    content: ""
}

.fa.fa-refresh:before {
    content: ""
}

.fa-turkish-lira:before,.fa-try:before {
    content: ""
}

.fa-euro:before,.fa-eur:before {
    content: ""
}

.fa-gbp:before {
    content: ""
}

.fa-dollar:before,.fa-usd:before {
    content: ""
}

.fa-rupee:before,.fa-inr:before {
    content: ""
}

.fa-cny:before,.fa-rmb:before,.fa-yen:before,.fa-jpy:before {
    content: ""
}

.fa-ruble:before,.fa-rouble:before,.fa-rub:before {
    content: ""
}

.fa-won:before,.fa-krw:before {
    content: ""
}


.fab,.fa.fa-facebook,.fa.fa-whatsapp,.fa.fa-twitter,.fa.fa-google-plus,.fa.fa-instagram,.fa.fa-google,.fa.fa-apple,.fa.fa-google-play,.fa.fa-linkedin,.fa.fa-youtube,.fa.fa-pinterest,.fa.fa-youtube-play,.fa.fa-pinterest-p {
    font-family: FontAwesomeBrands
}



.fal {
    font-weight: 300
}



.fal,.far {
    font-family: FontAwesome
}

.far {
    font-weight: 400
}



.fa,.fas {
    font-family: FontAwesome;
    font-weight: 900
}

.sliderOpacity {
    display: none;
    width: 100%;
    -webkit-tap-highlight-color: transparent;
    position: relative;
    z-index: 1
}

.sliderOpacity.owl-loaded {
    display: block
}

.RightDetail .sliderOpacity {
    display: block
}

.owl-carousel {
    display: none;
    width: 100%;
    -webkit-tap-highlight-color: transparent;
    position: relative;
    z-index: 1
}

.owl-carousel .owl-stage {
    position: relative;
    -ms-touch-action: pan-Y;
    touch-action: manipulation;
   
}

.owl-carousel .owl-stage:after {
    content: ".";
    display: block;
    clear: both;
    visibility: hidden;
    line-height: 0;
    height: 0
}

.owl-carousel .owl-stage-outer {
    position: relative;
    overflow: hidden;
  
}



.owl-carousel .owl-item {
    position: relative;
    min-height: 1px;
    float: left;
  
    -webkit-tap-highlight-color: transparent;
    -webkit-touch-callout: none
}

.sliderOpacity .owl-item img {
    display: block
}

.owl-carousel .owl-nav.disabled,.owl-carousel .owl-dots.disabled {
    display: none
}

.owl-carousel .owl-nav .owl-prev,.owl-carousel .owl-nav .owl-next,.owl-carousel .owl-dot {
    cursor: pointer;
    -webkit-user-select: none;
    -khtml-user-select: none;
    -moz-user-select: none;
    -ms-user-select: none;
    user-select: none
}

.owl-carousel .owl-nav button.owl-prev,.owl-carousel .owl-nav button.owl-next,.owl-carousel button.owl-dot {
    background: none;
    color: inherit;
    border: none;
    padding: 0 !important;
    font: inherit
}

.owl-carousel.owl-loaded,.sliderOpacity.owl-loaded {
    display: block
}

.owl-carousel.owl-loading,.sliderOpacity.owl-loading {
    opacity: 0;
    display: block
}

.owl-carousel.owl-hidden,.sliderOpacity.owl-hidden {
    opacity: 0
}

.owl-carousel.owl-refresh .owl-item {
    visibility: hidden
}

.owl-carousel.owl-drag .owl-item {
    -ms-touch-action: pan-y;
    touch-action: pan-y;
    -webkit-user-select: none;
    -moz-user-select: none;
    -ms-user-select: none;
    user-select: none
}

.owl-carousel.owl-grab {
    cursor: move;
    cursor: grab
}

.owl-carousel.owl-rtl {
    direction: rtl
}

.owl-carousel.owl-rtl .owl-item {
    float: right
}

.no-js .owl-carousel {
    display: block
}

.owl-carousel .animated {
    animation-duration: 300ms;
    animation-fill-mode: both
}

.owl-carousel .owl-animated-in {
    z-index: 0
}

.owl-carousel .owl-animated-out {
    z-index: 1
}

.owl-carousel .fadeOut {
    animation-name: fadeOut
}

.owl-carousel .fadeIn {
    animation-name: fadeIn
}

@keyframes fadeOut {
    0% {
        opacity: 1
    }

    100% {
        opacity: 0
    }
}

@-webkit-keyframes fadeOut {
    0% {
        opacity: 1
    }

    100% {
        opacity: 0
    }
}

@keyframes fadeIn {
    0% {
        opacity: 0
    }

    100% {
        opacity: 1
    }
}

@-webkit-keyframes fadeIn {
    0% {
        opacity: 0
    }

    100% {
        opacity: 1
    }
}

.owl-height {
    transition: height 500ms ease-in-out
}

.owl-carousel .owl-item .owl-lazy {
    opacity: 0;
    transition: opacity 400ms ease
}

.owl-carousel .owl-item .owl-lazy[src^=""],.owl-carousel .owl-item .owl-lazy:not([src]) {
    max-height: 0
}

.owl-carousel .owl-item img.owl-lazy {
    transform-style: preserve-3d
}

.owl-carousel .owl-video-wrapper {
    position: relative;
    height: 100%;
    background: #000
}

.owl-carousel .owl-video-play-icon {
    position: absolute;
    height: 80px;
    width: 80px;
    left: 50%;
    top: 50%;
    margin-left: -40px;
    margin-top: -40px;
    cursor: pointer;
    z-index: 1;
  
    transition: transform 100ms ease
}

.owl-carousel .owl-video-play-icon:hover {
    -ms-transform: scale(1.3,1.3);
    transform: scale(1.3,1.3)
}

.owl-carousel .owl-video-playing .owl-video-tn,.owl-carousel .owl-video-playing .owl-video-play-icon {
    display: none
}

.owl-carousel .owl-video-tn {
    opacity: 0;
    height: 100%;
    background-position: center center;
    background-repeat: no-repeat;
    background-size: contain;
    transition: opacity 400ms ease
}

.owl-carousel .owl-video-frame {
    position: relative;
    z-index: 1;
    height: 100%;
    width: 100%
}

.flex-container a:active,.flexslider a:active,.flex-container a:focus,.flexslider a:focus {
    outline: none
}

.slides,.flex-control-nav,.flex-direction-nav {
    margin: 0;
    padding: 0;
    list-style: none
}


#ulFlexSlider {
    margin: 0;
    padding: 0
}

#ulFlexSlider.slides>li {
    display: none;
    
}

#ulFlexSlider.slides img {
    display: block
}

#pnlSlider ul li a img[src="https://cdn.ticimax.com/App_Themes/Default/images/blank.png"] {
    width: 10px;
    height: 10px;
    margin: 0 auto;
    display: none
}

.flex-pauseplay span {
    text-transform: capitalize
}

.slides:after {
    content: "\20";
    display: block;
    clear: both;
    visibility: hidden;
    line-height: 0;
    height: 0
}

html[xmlns] .slides {
    display: block
}

* html .slides {
    height: 1%
}

.no-js .slides>li:first-child {
    display: block
}

.flexslider {
    margin: 0 0 60px;
    background: #fff;
    border: 4px solid #fff;
    position: relative;
    -webkit-border-radius: 4px;
    -moz-border-radius: 4px;
    -o-border-radius: 4px;
    border-radius: 4px;
    -webkit-box-shadow: 0 1px 4px rgba(0,0,0,.2);
    -moz-box-shadow: 0 1px 4px rgba(0,0,0,.2);
    -o-box-shadow: 0 1px 4px rgba(0,0,0,.2);
    box-shadow: 0 1px 4px rgba(0,0,0,.2);
    zoom:1}

.flex-viewport {
    max-height: 2000px;
    -webkit-transition: all 1s ease;
    -moz-transition: all 1s ease;
    -o-transition: all 1s ease;
    transition: all 1s ease
}

.loading .flex-viewport {
    max-height: 300px
}

.flexslider .slides {
    zoom:1}

.carousel li {
    margin-right: 5px
}

.flex-direction-nav {
    *height: 0
}

.flex-direction-nav a {
    display: block;
    width: 40px;
    height: 40px;
    margin: -20px 0 0;
    position: absolute;
    top: 50%;
    z-index: 10;
    overflow: hidden;
    opacity: 0;
    cursor: pointer;
    color: rgba(0,0,0,.8);
    text-shadow: 1px 1px 0 rgba(255,255,255,.3);
    -webkit-transition: all .3s ease;
    -moz-transition: all .3s ease;
    transition: all .3s ease
}

.flex-direction-nav .flex-prev {
    left: -50px
}

.flex-direction-nav .flex-next {
    right: -50px;
    text-align: right
}

.flexslider:hover .flex-prev {
    opacity: .7;
    left: 10px
}

.flexslider:hover .flex-next {
    opacity: .7;
    right: 10px
}

.flexslider:hover .flex-next:hover,.flexslider:hover .flex-prev:hover {
    opacity: 1
}

.flex-direction-nav .flex-disabled {
    opacity: 0!important;
    filter: alpha(opacity=0);
    cursor: default
}

.flex-direction-nav a:before {
    font-family: "flexslider-icon";
    font-size: 40px;
    display: inline-block;
    content: ''
}

.flex-direction-nav a.flex-next:before {
    content: ''
}

.flex-pauseplay a {
    display: block;
    width: 20px;
    height: 20px;
    position: absolute;
    bottom: 5px;
    left: 10px;
    opacity: .8;
    z-index: 10;
    overflow: hidden;
    cursor: pointer;
    color: #000
}

.flex-pauseplay a:before {
    font-family: "flexslider-icon";
    font-size: 20px;
    display: inline-block;
    content: ''
}

.flex-pauseplay a:hover {
    opacity: 1
}

.flex-pauseplay a.flex-play:before {
    content: ''
}

.flex-control-nav {
    width: 100%;
    position: absolute;
    bottom: 0;
    text-align: center;
    z-index: 2
}

.flex-control-nav li {
    margin: 0 6px;
    display: inline-block;
    zoom:1;*display: inline
}

.flex-control-paging li a {
    width: 11px;
    height: 11px;
    display: block;
    background: #666;
    background: rgba(0,0,0,.5);
    cursor: pointer;
    text-indent: -9999px;
    -webkit-border-radius: 20px;
    -moz-border-radius: 20px;
    -o-border-radius: 20px;
    border-radius: 20px;
    -webkit-box-shadow: inset 0 0 3px rgba(0,0,0,.3);
    -moz-box-shadow: inset 0 0 3px rgba(0,0,0,.3);
    -o-box-shadow: inset 0 0 3px rgba(0,0,0,.3);
    box-shadow: inset 0 0 3px rgba(0,0,0,.3)
}

.flex-control-paging li a:hover {
    background: #333;
    background: rgba(0,0,0,.7)
}

.flex-control-paging li a.flex-active {
    background: #000;
    background: rgba(0,0,0,.9);
    cursor: default
}

.flex-control-thumbs {
    margin: 0 0;
    position: static;
    overflow: hidden
}

.flex-control-thumbs li {
    max-width: 90px;
    float: left;
    margin: 0
}

.flex-control-thumbs img {
    width: 100%;
    display: block;
    opacity: .7;
    cursor: pointer
}

.flex-control-thumbs img:hover {
    opacity: 1
}

.flex-control-thumbs .flex-active {
    opacity: 1;
    cursor: default
}

@media screen and (max-width: 860px) {
    .flex-direction-nav .flex-prev {
        opacity:1;
        left: 10px
    }

    .flex-direction-nav .flex-next {
        opacity: 1;
        right: 10px
    }
}

.jq-ry-container {
    position: relative;
    padding: 0 5px;
    line-height: 0;
    display: block;
    cursor: pointer;
    -webkit-box-sizing: content-box;
    -moz-box-sizing: content-box;
    box-sizing: content-box;
    direction: ltr
}

.jq-ry-container[readonly=readonly] {
    cursor: default
}

.jq-ry-container>.jq-ry-group-wrapper {
    position: relative;
    width: 100%
}

.jq-ry-container>.jq-ry-group-wrapper>.jq-ry-group {
    position: relative;
    line-height: 0;
    z-index: 10;
    white-space: nowrap
}

.jq-ry-container>.jq-ry-group-wrapper>.jq-ry-group>svg {
    display: inline-block
}

.jq-ry-container>.jq-ry-group-wrapper>.jq-ry-group.jq-ry-normal-group {
    width: 100%
}

.jq-ry-container>.jq-ry-group-wrapper>.jq-ry-group.jq-ry-rated-group {
    width: 0;
    z-index: 11;
    position: absolute;
    top: 0;
    left: 0;
    overflow: hidden
}

.autocomplete-suggestions {
    text-align: left;
    cursor: default;
    border: 1px solid #ccc;
    border-top: 0;
    background: #fff;
    box-shadow: -1px 1px 3px rgba(0,0,0,.1);
    position: absolute;
    display: none;
    z-index: 9999;
    max-height: 254px;
    overflow: hidden;
    overflow-y: auto;
    box-sizing: border-box
}

.autocomplete-suggestion {
    position: relative;
    padding: 0 .6em;
    line-height: 23px;
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis;
    font-size: 1.02em;
    color: #333
}

.autocomplete-suggestion b {
    font-weight: normal;
    color: #1f8dd6
}

.autocomplete-suggestion.selected {
    background: #f0f0f0
}

@keyframes drift-loader-rotate {
    0% {
        transform: translate(-50%,-50%) rotate(0)
    }

    50% {
        transform: translate(-50%,-50%) rotate(-180deg)
    }

    100% {
        transform: translate(-50%,-50%) rotate(-360deg)
    }
}




@-webkit-keyframes drift-loader-rotate {
    0% {
        -webkit-transform: translate(-50%,-50%) rotate(0)
    }

    50% {
        -webkit-transform: translate(-50%,-50%) rotate(-180deg)
    }

    100% {
        -webkit-transform: translate(-50%,-50%) rotate(-360deg)
    }
}



.drift-zoom-pane.drift-opening {
    animation: drift-fadeZoomIn 200ms ease-out;
    -webkit-animation: drift-fadeZoomIn 200ms ease-out
}

.drift-zoom-pane.drift-closing {
    animation: drift-fadeZoomOut 10ms ease-in;
    -webkit-animation: drift-fadeZoomOut 10ms ease-in
}

.drift-zoom-pane.drift-inline {
    position: absolute;
    width: 150px;
    height: 150px;
    border-radius: 75px;
    box-shadow: 0 6px 18px rgba(0,0,0,.3)
}

.drift-loading .drift-zoom-pane-loader {
    display: block;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%,-50%);
    -webkit-transform: translate(-50%,-50%);
    width: 66px;
    height: 20px;
    animation: drift-loader-rotate 1800ms infinite linear;
    -webkit-animation: drift-loader-rotate 1800ms infinite linear
}

.drift-zoom-pane-loader:before,.drift-zoom-pane-loader:after {
    content: "";
    display: block;
    width: 20px;
    height: 20px;
    position: absolute;
    top: 50%;
    margin-top: -10px;
    border-radius: 20px;
    background: rgba(255,255,255,.9)
}

.drift-zoom-pane-loader:before {
    left: 0;
    animation: drift-loader-before 1800ms infinite linear;
    -webkit-animation: drift-loader-before 1800ms infinite linear
}

.drift-zoom-pane-loader:after {
    right: 0;
    animation: drift-loader-after 1800ms infinite linear;
    -webkit-animation: drift-loader-after 1800ms infinite linear;
    animation-delay: -900ms;
    -webkit-animation-delay: -900ms
}

.drift-bounding-box {
    background-color: rgba(0,0,0,.4)
}

.drift-container {
    position: absolute;
    top: 1px;
    min-height: 300px
}

.drift-container.drift-index {
    z-index: 9999
}

.fancybox-wrap,.fancybox-skin,.fancybox-outer,.fancybox-inner,.fancybox-image,.fancybox-wrap iframe,.fancybox-wrap object,.fancybox-nav,.fancybox-nav span,.fancybox-tmp {
    padding: 0;
    margin: 0;
    border: 0;
    outline: none;
    vertical-align: top
}

.fancybox-wrap {
    position: absolute;
    top: 0;
    left: 0;
    z-index: 8020
}

.fancybox-skin {
    position: relative;
    background: #fff;
    color: #444;
    text-shadow: none;
    border-radius: 10px
}

.fancybox-opened {
    z-index: 10001
}

.fancybox-opened .fancybox-skin {
    -webkit-box-shadow: 0 10px 25px rgba(0,0,0,.5);
    -moz-box-shadow: 0 10px 25px rgba(0,0,0,.5);
    box-shadow: 0 10px 25px rgba(0,0,0,.5)
}

.fancybox-outer,.fancybox-inner {
    position: relative
}

.fancybox-inner {
    overflow: hidden
}

.fancybox-type-iframe .fancybox-inner {
    -webkit-overflow-scrolling: touch
}

.fancybox-error {
    color: #444;
    font: 14px/20px "Helvetica Neue",Helvetica,Arial,sans-serif;
    margin: 0;
    padding: 15px;
    white-space: nowrap
}

.fancybox-image,.fancybox-iframe {
    display: block;
    width: 100%;
    height: 100%
}

.fancybox-image {
    max-width: 100%;
    max-height: 100%
}



#fancybox-loading {
    position: fixed;
    top: 50%;
    left: 50%;
    margin-top: -22px;
    margin-left: -22px;
    background-position: 0 -108px;
    opacity: .8;
    cursor: pointer;
    z-index: 8060
}

#fancybox-loading div {
    width: 44px;
    height: 44px;
    background: url('/Scripts/fancybox/fancybox_loading.gif') center center no-repeat
}

.fancybox-close {
    position: absolute;
    top: -16px;
    right: -17px;
    width: 36px;
    height: 36px;
    cursor: pointer;
    z-index: 8040;
    background: #fff;
    text-align: center;
    border-radius: 50%;
    box-shadow: 0 3px 6px rgba(0,0,0,.3)
}

.fancybox-close:after {
    content: "x";
    font-size: 21px;
    font-weight: 600;
    display: inline-block;
    line-height: 34px;
    color: #000
}

.fancybox-close:hover {
    box-shadow: 0 3px 6px rgba(0,0,0,.5);
    background: #eee
}

.fancybox-nav {
    position: absolute;
    top: 0;
    width: 40%;
    height: 100%;
    cursor: pointer;
    text-decoration: none;
    background: transparent url('/Scripts/fancybox/blank.gif');
    -webkit-tap-highlight-color: rgba(0,0,0,0);
    z-index: 8040
}

.fancybox-prev {
    left: 0
}

.fancybox-next {
    right: 0
}

.fancybox-nav span {
    position: absolute;
    top: 50%;
    width: 36px;
    height: 34px;
    margin-top: -18px;
    cursor: pointer;
    z-index: 8040;
    visibility: hidden
}

.fancybox-prev span {
    left: 10px;
    background-position: 0 -36px
}

.fancybox-next span {
    right: 10px;
    background-position: 0 -72px
}

.fancybox-nav:hover span {
    visibility: visible
}

.fancybox-tmp {
    position: absolute;
    top: -99999px;
    left: -99999px;
    visibility: hidden;
    max-width: 99999px;
    max-height: 99999px;
    overflow: visible !important
}

.fancybox-lock {
    overflow: hidden !important;
    width: auto
}

.fancybox-lock body {
    overflow: hidden !important
}

.fancybox-lock-test {
    overflow-y: hidden !important
}

.fancybox-overlay {
    position: absolute;
    top: 0;
    left: 0;
    overflow: hidden;
    display: none;
    z-index: 8010;
}

.fancybox-overlay-fixed {
    position: fixed;
    bottom: 0;
    right: 0
}

.fancybox-lock .fancybox-overlay {
    overflow: auto;
    overflow-y: scroll;
    z-index: 9999
}

.fancybox-title {
    visibility: hidden;
    font: normal 13px/20px "Helvetica Neue",Helvetica,Arial,sans-serif;
    position: relative;
    text-shadow: none;
    z-index: 8050
}

.fancybox-opened .fancybox-title {
    visibility: visible
}

.fancybox-title-float-wrap {
    position: absolute;
    bottom: 0;
    right: 50%;
    margin-bottom: -35px;
    z-index: 8050;
    text-align: center
}

.fancybox-title-float-wrap .child {
    display: inline-block;
    margin-right: -100%;
    padding: 2px 20px;
    background: transparent;
    background: rgba(0,0,0,.8);
    -webkit-border-radius: 15px;
    -moz-border-radius: 15px;
    border-radius: 15px;
    text-shadow: 0 1px 2px #222;
    color: #fff;
    font-weight: bold;
    line-height: 24px;
    white-space: nowrap
}

.fancybox-title-outside-wrap {
    position: relative;
    margin-top: 10px;
    color: #fff
}

.fancybox-title-inside-wrap {
    padding-top: 10px
}

.fancybox-title-over-wrap {
    position: absolute;
    bottom: 0;
    left: 0;
    color: #fff;
    padding: 10px;
    background: #000;
    background: rgba(0,0,0,.8)
}

@media only screen and (-webkit-min-device-pixel-ratio: 1.5),only screen and (min--moz-device-pixel-ratio:1.5),only screen and (min-device-pixel-ratio:1.5) {
    .fancybox-close {
        top:0;
        right: 0;
        width: 20px;
        height: 20px;
        background-color: transparent
    }

    .fancybox-close:after {
        color: #000;
        line-height: 20px
    }
}

@keyframes zuckSlideTime {
    0% {
        max-width: 0
    }

    100% {
        max-width: 100%
    }
}

@keyframes zuckLoading {
    0% {
        transform: rotate(0deg)
    }

    100% {
        transform: rotate(360deg)
    }
}

#zuck-modal {
    outline: 0 !important;
    overflow: hidden;
    position: fixed;
    top: 0;
    left: 0;
    width: 100vw;
    height: 100%;
    background: rgba(0,0,0,.75);
    z-index: 100000;
    font-size: 14px;
    font-family: inherit
}

#zuck-modal-content,#zuck-modal-content .story-viewer,#zuck-modal-content .story-viewer>.slides,#zuck-modal-content .story-viewer>.slides>* {
    width: 100vw;
    height: 100%;
    top: 0;
    bottom: 0;
    position: absolute;
    overflow: hidden
}

#zuck-modal * {
    user-select: none;
    outline: 0
}

#zuck-modal.with-effects {
    transform: scale(.01);
    transform-origin: top left;
    transition: .25s
}

#zuck-modal.with-effects.animated {
    transform: scale(1);
    border-radius: 0;
    margin-top: 0 !important;
    margin-left: 0 !important
}

#zuck-modal.with-effects.closed {
    transform: translateY(100%)
}

#zuck-modal .slider {
    width: 300vw;
    height: 100%;
    top: 0;
    bottom: 0;
    left: -100vw;
    position: absolute
}

#zuck-modal .slider>* {
    width: 100vw;
    height: 100%;
    top: 0;
    bottom: 0;
    position: absolute
}

#zuck-modal .slider>.previous {
    left: 0
}

#zuck-modal .slider>.viewing {
    left: 100vw
}

#zuck-modal .slider>.next {
    left: 200vw
}

#zuck-modal .slider.animated {
    -webkit-transition: -webkit-transform .25s linear;
    transition: -webkit-transform .25s linear;
    transition: transform .25s linear;
    transition: transform .25s linear,-webkit-transform .25s linear
}

#zuck-modal.with-cube #zuck-modal-content {
    perspective: 1000vw;
    transform: scale(.95);
    perspective-origin: 50% 50%;
    overflow: visible;
    transition: .3s
}

#zuck-modal.with-cube .slider {
    transform-style: preserve-3d;
    transform: rotateY(0deg)
}

#zuck-modal.with-cube .slider>.previous {
    backface-visibility: hidden;
    left: 100vw;
    transform: rotateY(270deg) translateX(-50%);
    transform-origin: center left
}

#zuck-modal.with-cube .slider>.viewing {
    backface-visibility: hidden;
    left: 100vw;
    transform: translateZ(50vw)
}

#zuck-modal.with-cube .slider>.next {
    backface-visibility: hidden;
    left: 100vw;
    transform: rotateY(-270deg) translateX(50%);
    transform-origin: top right
}

#zuck-modal-content .story-viewer.paused.longPress .head,#zuck-modal-content .story-viewer.paused.longPress .slides-pointers,#zuck-modal-content .story-viewer.paused.longPress .tip {
    opacity: 0
}

#zuck-modal-content .story-viewer.viewing:not(.paused):not(.stopped) .slides-pointers>*>.active>b {
    -webkit-animation-play-state: running;
    animation-play-state: running
}

#zuck-modal-content .story-viewer.next {
    z-index: 10
}

#zuck-modal-content .story-viewer.viewing {
    z-index: 5
}

#zuck-modal-content .story-viewer.previous {
    z-index: 0
}

#zuck-modal-content .story-viewer.muted .tip.muted,#zuck-modal-content .story-viewer.loading .head .loading {
    display: block
}

#zuck-modal-content .story-viewer.loading .head .right .time,#zuck-modal-content .story-viewer.loading .head .right .close {
    display: none
}

#zuck-modal-content .story-viewer .slides-pagination span {
    position: absolute;
    top: 50vh;
    font-size: 48px;
    color: #fff;
    line-height: 48px;
    width: 48px;
    margin: 6px;
    transform: translateY(-50%);
    z-index: 1;
    text-align: center
}

#zuck-modal-content .story-viewer .slides-pagination .previous {
    left: 0
}

#zuck-modal-content .story-viewer .slides-pagination .next {
    right: 0
}

#zuck-modal-content .story-viewer .slides-pointers {
    display: table;
    table-layout: fixed;
    border-spacing: 6px;
    border-collapse: separate;
    position: absolute;
    width: 100vh;
    top: 0;
    left: calc(50vw - 50vh);
    right: calc(50vw - 50vh);
    z-index: 100020
}

#zuck-modal-content .story-viewer .slides-pointers>* {
    display: table-row
}

#zuck-modal-content .story-viewer .slides-pointers>*>* {
    display: table-cell;
    background: rgba(255,255,255,.5);
    border-radius: 2px
}

#zuck-modal-content .story-viewer .slides-pointers>*>.seen {
    background: #fff
}

#zuck-modal-content .story-viewer .slides-pointers>*>*>b {
    background: #fff;
    width: auto;
    max-width: 0;
    height: 2px;
    display: block;
    -webkit-animation-fill-mode: forwards;
    animation-fill-mode: forwards;
    -webkit-animation-play-state: paused;
    animation-play-state: paused;
    border-radius: 2px
}

#zuck-modal-content .story-viewer .slides-pointers>*>.active>b {
    -webkit-animation-name: zuckSlideTime;
    animation-name: zuckSlideTime;
    -webkit-animation-timing-function: linear;
    animation-timing-function: linear
}

#zuck-modal-content .story-viewer .head {
    position: absolute;
    height: 56px;
    left: 0;
    right: 0;
    line-height: 56px;
    z-index: 100010;
    color: #fff;
    font-size: 14px;
    text-shadow: 1px 1px 1px rgba(0,0,0,.35),1px 0 1px rgba(0,0,0,.35);
    padding: 6px 12px
}

#zuck-modal-content .story-viewer .head .item-preview {
    overflow: hidden;
    vertical-align: top;
    background-size: cover;
    width: 42px;
    height: 42px;
    display: inline-block;
    margin-right: 9px;
    border-radius: 50%;
    vertical-align: middle;
    background-repeat: no-repeat;
    background-position: center
}

#zuck-modal-content .story-viewer .head .item-preview img {
    display: block;
    box-sizing: border-box;
    height: 100%;
    width: 100%;
    background-size: cover;
    background-position: center;
    object-fit: cover
}

#zuck-modal-content .story-viewer .head .time {
    opacity: .75;
    font-weight: 500;
    font-size: 13px
}

#zuck-modal-content .story-viewer .head .left {
    line-height: 1 !important;
    display: inline-block;
    margin: 6px 0
}

#zuck-modal-content .story-viewer .head .left .info {
    display: inline-block;
    max-width: 30vw;
    vertical-align: middle
}

#zuck-modal-content .story-viewer .head .left .info>* {
    width: 100%;
    display: inline-block;
    line-height: 21px
}

#zuck-modal-content .story-viewer .head .left .info .name {
    font-weight: 500
}

#zuck-modal-content .story-viewer .head .right {
    float: right
}

#zuck-modal-content .story-viewer .head .right .close,#zuck-modal-content .story-viewer .head .back {
    font-size: 42px;
    width: 48px;
    height: 48px;
    line-height: 48px;
    cursor: pointer;
    text-align: center
}

#zuck-modal-content .story-viewer .head .left .back {
    display: none;
    width: 24px;
    margin: -9px -6px 0 -6px
}

#zuck-modal-content .story-viewer .head .right .time {
    display: none
}

#zuck-modal-content .story-viewer .head .loading {
    display: none;
    border-radius: 50%;
    width: 30px;
    height: 30px;
    margin: 9px 0;
    border: 4px solid rgba(255,255,255,.2);
    box-sizing: border-box;
    border-top-color: #fff;
    -webkit-animation: zuckLoading 1s infinite linear;
    animation: zuckLoading 1s infinite linear
}

#zuck-modal-content .story-viewer .head,#zuck-modal-content .story-viewer .slides-pointers,#zuck-modal-content .story-viewer .tip {
    -webkit-transition: opacity .5s;
    transition: opacity .5s
}

#zuck-modal-content .story-viewer .slides .item {
    display: none;
    overflow: hidden;
    background: #000
}

#zuck-modal-content .story-viewer .slides .item:before {
    z-index: 4;
    background: transparent;
    content: '';
    position: absolute;
    left: 0;
    right: 0;
    bottom: 0;
    top: 0
}

#zuck-modal-content .story-viewer .slides .item>.media {
    height: 100%;
    position: absolute;
    left: 50%;
    -webkit-transform: translateX(-50%);
    transform: translateX(-50%);
    margin: auto
}

#zuck-modal-content .story-viewer .slides .item.active,#zuck-modal-content .story-viewer .slides .item.active .tip.link {
    display: block
}

#zuck-modal-content .story-viewer .tip {
    z-index: 5;
    text-decoration: none;
    display: none;
    border-radius: 24px;
    background: rgba(0,0,0,.5);
    font-size: 16px;
    position: absolute;
    bottom: 24px;
    left: 50%;
    transform: translateX(-50%);
    z-index: 1000;
    color: #fff;
    text-align: center;
    text-transform: uppercase;
    font-weight: 500;
    padding: 12px 24px
}

#zuck-modal.rtl {
    direction: rtl;
    left: auto;
    right: 0
}

#zuck-modal.rtl.with-effects {
    transform-origin: top right
}

#zuck-modal.rtl.with-effects.animated {
    margin-left: auto !important;
    margin-right: 0 !important
}

#zuck-modal.rtl .slider {
    left: auto;
    right: -100vw
}

#zuck-modal.rtl .slider>.previous {
    left: auto;
    right: 0;
    transform: rotateY(-270deg) translateX(50%)
}

#zuck-modal.rtl .slider>.viewing {
    left: auto;
    right: 100vw
}

#zuck-modal.rtl .slider>.next {
    left: auto;
    right: 200vw
}

#zuck-modal.rtl.with-cube .slider>.previous {
    left: auto;
    right: 100vw;
    transform-origin: center right
}

#zuck-modal.rtl.with-cube .slider>.viewing {
    left: auto;
    right: 100vw;
    transform: translateZ(50vw)
}

#zuck-modal.rtl.with-cube .slider>.next {
    left: auto;
    right: 100vw;
    transform-origin: top left;
    transform: rotateY(270deg) translateX(-50%)
}

#zuck-modal.rtl #zuck-modal-content .story-viewer .slides-pagination .previous {
    left: auto;
    right: 0
}

#zuck-modal.rtl #zuck-modal-content .story-viewer .slides-pagination .next {
    right: auto;
    left: 0
}

#zuck-modal.rtl #zuck-modal-content .story-viewer .head .item-preview {
    margin-right: auto;
    margin-left: 9px
}

#zuck-modal.rtl #zuck-modal-content .story-viewer .head .right {
    float: left
}

#zuck-modal.rtl #zuck-modal-content .story-viewer .tip {
    left: auto;
    right: 50%;
    transform: translateX(50%)
}

@media(max-width: 1024px) {
    #zuck-modal-content .story-viewer .head {
        top:3px
    }

    #zuck-modal-content .story-viewer .head .loading {
        width: 24px;
        height: 24px;
        margin: 6px 0
    }

    #zuck-modal-content .story-viewer .head .item-preview {
        width: 30px;
        height: 30px;
        margin-right: 9px
    }

    #zuck-modal-content .story-viewer .head .left {
        font-size: 15px;
        margin: 15px 0
    }

    #zuck-modal-content .story-viewer .head .left>div {
        line-height: 30px
    }

    #zuck-modal-content .story-viewer .head .right .time {
        display: block;
        white-space: nowrap;
        font-size: 15px;
        margin: 15px 0;
        line-height: 30px
    }

    #zuck-modal-content .story-viewer .head .left>.back {
        display: none;
        background: transparent;
        z-index: 20;
        visibility: visible;
        position: absolute;
        height: 42px;
        width: 24px;
        line-height: 36px;
        text-align: left;
        vertical-align: top;
        text-shadow: none
    }

    #zuck-modal-content .story-viewer.with-back-button .head .left>.back {
        display: block
    }

    #zuck-modal-content .story-viewer.with-back-button .head .left .item-preview {
        margin-left: 18px
    }

    #zuck-modal-content .story-viewer .slides-pointers {
        width: 100vw;
        left: 0;
        right: 0
    }

    #zuck-modal-content .story-viewer .tip {
        font-size: 14px;
        padding: 6px 12px
    }

    #zuck-modal-content .story-viewer .head .left .time,#zuck-modal-content .story-viewer .head .right .close {
        display: none
    }

    #zuck-modal.rtl #zuck-modal-content .story-viewer .head .item-preview {
        margin-right: auto;
        margin-left: 9px
    }

    #zuck-modal.rtl #zuck-modal-content .story-viewer .head .left>.back {
        text-align: right
    }

    #zuck-modal.rtl #zuck-modal-content .story-viewer.with-back-button .head .left .item-preview {
        margin-left: auto;
        margin-right: 18px
    }
}

.stories.carousel {
    white-space: nowrap;
    overflow: auto;
    -webkit-overflow-scrolling: touch;
   
}

.stories.carousel::-webkit-scrollbar {
    width: 0;
    background: transparent
}

.stories.carousel .story {
    display: inline-block;
    width: 18vw;
    max-width: 90px;
    margin: 0 6px;
    vertical-align: top
}

.stories.carousel .story:first-child {
    margin-left: 0
}

.stories.carousel .story:last-child {
    margin-right: 0
}

.stories.carousel .story>.item-link {
    text-align: center;
    display: block
}

.stories.carousel .story>.item-link:active>.item-preview {
    transform: scale(.9)
}

.stories.carousel .story>.item-link>.item-preview {
    display: block;
    box-sizing: border-box;
    font-size: 0;
    max-height: 90px;
    height: 18vw;
    overflow: hidden;
    transition: transform .2s
}

.stories.carousel .story>.item-link>.item-preview img {
    display: block;
    box-sizing: border-box;
    height: 100%;
    width: 100%;
    background-size: cover;
    background-position: center;
    object-fit: cover
}

.stories.carousel .story>.item-link>.info {
    display: inline-block;
    margin-top: .5em;
    line-height: 1.2em;
    width: 100%;
    overflow: hidden;
    text-overflow: ellipsis
}

.stories.carousel .story>.item-link>.info .name {
    font-weight: 300
}

.stories.carousel .story>.item-link>.info .time {
    display: none
}

.stories.carousel .story>.items {
    display: none
}

.stories.list {
    white-space: nowrap;
    overflow: auto
}

.stories.list .story {
    display: block;
    width: auto;
    margin: 6px;
    padding-bottom: 6px
}

.stories.list .story>.item-link {
    text-align: left;
    display: block
}

.stories.list .story>.item-link>.item-preview {
    height: 42px;
    width: 42px;
    max-width: 42px;
    margin-right: 12px;
    vertical-align: top;
    display: inline-block;
    box-sizing: border-box;
    font-size: 0;
    overflow: hidden
}

.stories.list .story>.item-link>.item-preview img {
    display: block;
    box-sizing: border-box;
    height: 100%;
    width: 100%;
    background-size: cover;
    background-position: center
}

.stories.list .story>.item-link>.info {
    display: inline-block;
    line-height: 1.6em;
    overflow: hidden;
    text-overflow: ellipsis;
    vertical-align: top
}

.stories.list .story>.item-link>.info .name {
    font-weight: 500;
    display: block
}

.stories.list .story>.item-link>.info .time {
    display: inline-block
}

.stories.list .story>.items {
    display: none
}

.stories.rtl {
    direction: rtl
}

.stories.rtl.carousel .story:first-child {
    margin-left: auto;
    margin-right: 0
}

.stories.rtl.carousel .story:last-child {
    margin-right: auto;
    margin-left: 0
}

.stories.rtl.list .story>.item-link {
    text-align: right
}

.stories.rtl.list .story>.item-link>.item-preview {
    margin-right: auto;
    margin-left: 12px
}

.ProductGallery {
    position: relative
}

.ProductGallery .gallery-container .owl-carousel.galleryOwl .owl-nav {
    position: absolute;
    top: 50%;
    height: 0;
    display: -webkit-flex;
    display: flex;
    align-items: center;
    justify-content: space-between;
    width: 100%;
    padding: 0 15px
}

.ProductGallery .gallery-container .owl-carousel.galleryOwl .owl-nav button:focus {
    outline: none
}

.ProductGallery .gallery-container .owl-carousel.galleryOwl .owl-nav span {
    width: 40px;
    height: 40px;
    display: inline-block;
    text-align: center;
    line-height: 26px;
    font-size: 49px;
    border-radius: 50%;
    border: 2px solid rgba(255,255,255,.6);
    color: rgba(255,255,255,.6);
    transition: .3s
}

.ProductGallery .gallery-container .owl-carousel.galleryOwl .owl-nav span:hover {
    color: #fff;
    border-color: #fff
}

.ProductGallery .galleryOwl-thumb {
    position: absolute;
    top: 0;
    left: 0;
    height: calc(100% - 5px);
    z-index: 2;
    background-color: #fff;
    width: 110px;
    border: 1px solid #f3f3f3;
    display: -webkit-flex;
    display: flex;
    flex-direction: column
}

.ProductGallery .galleryOwl-thumb .thumb-list {
    overflow-y: scroll;
    padding: 10px
}

.ProductGallery .galleryOwl-thumb .thumb-list::-webkit-scrollbar {
    width: 5px;
    background-color: #f1f1f1
}

.ProductGallery .galleryOwl-thumb .thumb-list::-webkit-scrollbar-thumb {
    background: #c9c9c9;
    border-radius: 10px
}

.ProductGallery .galleryOwl-thumb .thumb-list::-webkit-scrollbar-thumb:window-inactive {
    background: #d6d6d6
}

.ProductGallery .galleryOwl-thumb .thumb-list .thumb-item {
    overflow: hidden;
    margin-bottom: 15px;
    position: relative
}

.ProductGallery .galleryOwl-thumb .thumb-list .thumb-item.thumb-video::after {
    font-family: misszenne !important;
    content: "";
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%,-50%);
    width: 40px;
    height: 40px;
    border: 1px solid #000;
    border-radius: 50%;
    text-align: center;
    line-height: 40px;
    font-size: 16px
}

.ProductGallery .galleryOwl-thumb .thumb-list .thumb-item.active::before {
    content: "";
    position: absolute;
    left: 0;
    right: 0;
    top: 0;
    bottom: 0;
    border: 2px solid #f767b0
}

.ProductGallery .galleryOwl-thumb .thumb-bottom {
    text-align: center;
    padding: 15px 0
}

.ProductGallery .galleryOwl-thumb .thumb-bottom>.item {
    padding: 11px 5px;
    font-size: 22px;
    color: #717171;
    cursor: pointer;
    transition: .3s
}

.ProductGallery .galleryOwl-thumb .thumb-bottom>.item:hover {
    color: #000
}

.ProductGallery .galleryOwl-thumb .thumb-bottom>.item>p {
    font-size: 12px;
    font-weight: 600;
    margin-top: 6px
}

.ProductGallery .galleryOwl-thumb .thumb-bottom>.item.StopVideo {
    display: none
}

.modal-js.ShareModal {
    background-color: #fff;
    padding: 0
}

.modal-js.ShareModal .ShareImg {
    padding: 30px 30px 0
}

.modal-js.ShareModal .ShareImg>img {
    width: 100%;
    max-width: 270px
}

.modal-js.ShareModal .ShareTitle {
    text-align: center;
    padding: 15px 10px;
    border-bottom: 1px solid #eee;
    font-weight: 500;
    font-size: 16px
}

.modal-js.ShareModal .ShareList {
    padding: 15px;
    display: -webkit-flex;
    display: flex;
    align-items: center
}

.modal-js.ShareModal .ShareList>.item {
    -webkit-flex-wrap: wrap;
    flex-wrap: wrap;
    width: 25%
}

.modal-js.ShareModal .ShareList>.item>.ShareLink {
    width: 100%;
    text-align: center;
    display: block
}

.modal-js.ShareModal .ShareList>.item>.ShareLink span {
    display: block;
    margin-top: 9px;
    color: #717171
}

.modal-js.ShareModal .ShareList>.item>.ShareLink::before {
    content: "";
    font-family: denizbutik !important;
    display: inline-block;
    background-color: #f00;
    text-align: center;
    border-radius: 10px;
    width: 40px;
    height: 40px;
    line-height: 40px;
    text-align: center;
    font-size: 16px;
    color: #fff
}

.modal-js.ShareModal .ShareList>.item>.ShareLink.Fb::before {
    content: "";
    background-color: #3b5999;
    font-size: 19px
}

.modal-js.ShareModal .ShareList>.item>.ShareLink.Tw::before {
    content: "";
    background-color: #55acee
}

.modal-js.ShareModal .ShareList>.item>.ShareLink.Wp::before {
    content: "";
    background-color: #25d366;
    font-size: 21px
}

.modal-js.ShareModal .ShareList>.item>.ShareLink.Gp::before {
    content: "";
    background-color: #dd4b39;
    font-size: 23px
}

@media only screen and (max-width: 768px) {
    .modal-js.ShareModal .close-modal {
        right:0;
        top: 0
    }
}

.ProductGallery .gallery-container .GalleryArea {
    position: relative;
    margin-left: 125px
}

.ProductGallery .gallery-container .GalleryArea .Badge {
    position: absolute;
    top: 0;
    left: 0;
    background-color: #00b65f;
    z-index: 2;
    color: #fff;
    font-weight: 600;
    font-size: 14px;
    padding: 3px 7px
}

.ProductGallery .gallery-container .GalleryArea .Badge2 {
    position: absolute;
    bottom: 6px;
    right: 0;
    background-color: #cc242e;
    z-index: 2;
    color: #fff;
    font-weight: 600;
    font-size: 17px;
    padding: 5px 10px;
    font-weight: 700
}

.ProductGallery .owl-carousel.galleryOwl .owl-dots {
    width: auto;
    position: absolute;
    bottom: 25px;
    left: 50%;
    transform: translateX(-50%);
    background-color: rgba(0,0,0,.24);
    border-radius: 60px;
    padding: 1px 12px 2px
}

.ProductGallery .owl-carousel.galleryOwl .owl-dots .owl-dot {
    display: inline-block;
    margin: 0 2px;
    line-height: 12px
}

.ProductGallery .owl-carousel.galleryOwl .owl-dots .owl-dot span {
    width: 8px;
    height: 8px;
    display: inline-block;
    border-radius: 50%;
    background-color: transparent;
    border: 1px solid #fff
}

.ProductGallery .owl-carousel.galleryOwl .owl-dots .owl-dot.active span {
    background-color: #fff
}

.ProductGallery .ProductVideo {
    position: absolute;
    top: 0;
    right: 0;
    left: 0;
    bottom: 4px;
    background-color: #f1f1f1;
    opacity: 0;
    visibility: hidden;
    z-index: 2
}

.ProductGallery .ProductVideo.ShowVideo {
    opacity: 1;
    visibility: visible
}

.ProductGallery .ProductVideo video {
    width: 100%;
    height: 100%
}

.wm-zoom-box,.wm-zoom-container {
    position: relative
}

img.wm-zoom-default-img {
    height: auto
}

.wm-zoom-lens {
    display: none;
    left: 0;
    position: absolute;
    top: 0
}

.wm-zoom-hight {
    display: none;
    overflow: hidden;
    position: absolute
}

.wm-zoom-hight img {
    left: 0;
    position: absolute;
    top: 0
}

img.wm-zoom-loader {
    z-index: 1
}

img.wm-zoom-hight-img {
    z-index: 2;
    max-width: inherit !important
}

.wm-zoom-lens {
    background: #fff;
    opacity: .3;
    filter: alpha(opacity=30)
}

.wm-zoom-hight {
    background: #f4f4f4;
    z-index: 999999;
    height: 100% !important
}

@media only screen and (max-width: 768px) {
    .wm-zoom-lens,.wm-zoom-hight {
        display:none !important;
        opacity: 0 !important;
        visibility: hidden !important
    }

    .ProductGallery .gallery-container .GalleryArea {
        margin-left: 0
    }
}

.ticiDialog {
    overflow-y: hidden;
    height: 100%;
    position: absolute;
    max-height: 100%;
    top: 0;
    width: 100%
}

.ticiDialog .ticimaxDialogContent {
    z-index: 99999;
    transform: scale(1)
}

.ticimaxDialogContent {
    position: fixed;
    z-index: 999;
    top: 0;
    left: 0;
    display: table;
    width: 100%;
    height: 100%;
    transform: scale(0);
    background: rgba(0,0,0,.5)
}

.ticimaxDialogContainer {
    position: fixed;
    left: 50%;
    top: 50%;
    transform: translate(-50%,-50%)
}

.ticiDialog .ticimaxDialogContainer {
    animation: fadeIn .5s cubic-bezier(.165,.84,.44,1) forwards
}

.ticiDialog .ticimaxDialogTxt {
    -webkit-animation-name: zoomIn;
    -moz-animation-name: zoomIn;
    -ms-animation-name: zoomIn;
    -o-animation-name: zoomIn;
    animation-name: zoomIn;
    -webkit-animation-iteration-count: 1;
    -moz-animation-iteration-count: 1;
    -ms-animation-iteration-count: 1;
    -o-animation-iteration-count: 1;
    animation-iteration-count: 1;
    -webkit-animation-duration: 1s;
    -moz-animation-duration: 1s;
    -ms-animation-duration: 1s;
    -o-animation-duration: 1s;
    animation-duration: 1s;
    -webkit-animation-delay: 0s;
    -moz-animation-delay: 0s;
    -ms-animation-delay: 0s;
    -o-animation-delay: 0s;
    animation-delay: 0s;
    -webkit-animation-timing-function: ease;
    -moz-animation-timing-function: ease;
    -ms-animation-timing-function: ease;
    -o-animation-timing-function: ease;
    animation-timing-function: ease;
    -webkit-animation-fill-mode: both;
    -moz-animation-fill-mode: both;
    -ms-animation-fill-mode: both;
    -o-animation-fill-mode: both;
    animation-fill-mode: both;
    -webkit-backface-visibility: hidden;
    -moz-backface-visibility: hidden;
    -ms-backface-visibility: hidden;
    -o-backface-visibility: hidden;
    backface-visibility: hidden
}

.ticimaxDialogTxt {
    font-weight: 300;
    position: relative;
    display: flex;
    min-width: 280px;
    max-width: 500px;
    margin: auto;
    padding: 15px;
    border-radius: 5px;
    flex-wrap: wrap;
    background: linear-gradient(87deg,#00e676 0,#00c853 100%) !important;
    z-index: 999999999999
}

.ticimaxDialogTxt p {
    display: block;
    text-align: center;
    font-size: 13px;
    width: 100%;
    margin: 1px auto 15px;
    color: #fff;
    letter-spacing: .4px;
    font-weight: 600
}

.ticiDialog .ticimaxDialogTxt>div {
    display: block;
    width: 100%
}

.ticiDialog .ticimaxDialogTxt>div:after {
    clear: both;
    display: table;
    content: ""
}

.ticimaxDialog-default {
    background: #fff !important
}

.ticimaxDialog-default p {
    color: #000
}

.ticimaxDialog-default:before {
    content: "";
    font-family: 'FontAwesome';
    font-size: 50px;
    text-align: center;
    margin: 0 auto;
    color: #000;
    margin: 15px auto
}

.ticimaxDialog-default a.ticiNotyBtn {
    cursor: pointer;
    width: 100%;
    display: block;
    line-height: normal;
    border-radius: 2px;
    position: relative;
    background-color: #00c853;
    color: #fff;
    font-weight: 400;
    font-size: 13px;
    padding: 8px 0
}

.ticimaxDialog-default a.ticiNotyBtn:hover {
    text-decoration: none;
    color: #fff;
    background-color: #00c853
}

.ticimaxDialog-success {
    background: #fff !important
}

.ticimaxDialog-success p {
    color: #00c853
}

.ticimaxDialog-success:before {
    content: "";
    font-family: 'FontAwesome';
    font-size: 50px;
    text-align: center;
    margin: 0 auto;
    color: #00c853;
    margin: 15px auto
}

.ticimaxDialog-success a.ticiNotyBtn {
    cursor: pointer;
    width: 100%;
    display: block;
    line-height: normal;
    border-radius: 2px;
    position: relative;
    background-color: #00c853;
    color: #fff;
    font-weight: 400;
    font-size: 13px;
    padding: 8px 0
}

.ticimaxDialog-success a.ticiNotyBtn:hover {
    text-decoration: none;
    color: #fff;
    background-color: #00c853
}

.ticimaxDialog-danger {
    background: #fff !important
}

.ticimaxDialog-danger:before {
    content: "";
    font-family: 'FontAwesome';
    font-size: 50px;
    text-align: center;
    margin: 0 auto;
    color: #f00;
    margin: 15px auto
}

.ticimaxDialog-danger p {
    color: #f00
}

.ticimaxDialog-danger a.ticiNotyBtn {
    cursor: pointer;
    width: 100%;
    display: block;
    line-height: normal;
    border-radius: 2px;
    position: relative;
    background-color: #f00;
    color: #fff;
    font-weight: 400;
    font-size: 13px;
    padding: 8px 0
}

.ticimaxDialog-danger a.ticiNotyBtn:hover {
    text-decoration: none;
    color: #fff;
    background-color: #f00
}

.ticimaxDialog-warning {
    background: #fff !important
}

.ticimaxDialog-warning p {
    color: #eeb516
}

.ticimaxDialog-warning:before {
    content: "";
    font-family: 'FontAwesome';
    font-size: 50px;
    text-align: center;
    margin: 0 auto;
    color: #eeb516;
    margin: 15px auto
}

.ticimaxDialog-warning a.ticiNotyBtn {
    cursor: pointer;
    width: 100%;
    display: block;
    line-height: normal;
    border-radius: 2px;
    position: relative;
    background-color: #eeb516;
    color: #fff;
    font-weight: 400;
    font-size: 13px;
    padding: 8px 0
}

.ticimaxDialog-warning a.ticiNotyBtn:hover {
    text-decoration: none;
    color: #fff;
    background-color: #eeb516
}

.ticimaxDialog-info {
    background: #fff !important
}

.ticimaxDialog-info p {
    color: #00bce6
}

.ticimaxDialog-info:before {
    content: "";
    font-family: 'FontAwesome';
    font-size: 50px;
    text-align: center;
    color: #00bce6;
    margin: 15px auto
}

.ticimaxDialog-info a.ticiNotyBtn {
    cursor: pointer;
    width: 100%;
    display: block;
    line-height: normal;
    border-radius: 2px;
    position: relative;
    background-color: #00bce6;
    color: #fff;
    font-weight: 400;
    font-size: 13px;
    padding: 8px 0
}

.ticimaxDialog-info a.ticiNotyBtn:hover {
    text-decoration: none;
    color: #fff;
    background-color: #00bce6
}

.ticiNotyBtnCancel {
    display: inline-block;
    width: 49%;
    
    cursor: pointer;
    background: #f00;
    color: #fff;
    padding: 5px 0;
    border-radius: 2px
}

.ticiNotyBtnConfirm {
    display: inline-block;
    
    width: 49%;
    padding: 5px 0;
    background: #00c853;
    color: #fff;
    border-radius: 2px;
    cursor: pointer
}

.ticimaxDialogContainer.dialogSiparis {
    max-width: 95%;
    width: 400px;
    border-radius: 0
}

.ticiDialog .dialogSiparis .ticimaxDialogTxt {
    border-radius: 0
}

.dialogSiparis .ticimaxDialog-success p {
    margin-bottom: 50px
}

.dialogSiparis .ticiNotyBtnCancel {
    display: block;
    width: 100%;
    text-align: center;
    margin-bottom: 10px;
    font-size: 13px;
    padding: 12px 0;
    background-color: #eaeaea !important;
    font-family: sans-serif;
    color: #5e5e5e
}

.dialogSiparis .ticiNotyBtnConfirm {
    display: block;
    width: 100%;
    text-align: center;
    font-size: 13px;
    padding: 12px 0;
    background-color: #56be67 !important;
    color: #fff !important;
    font-family: sans-serif;
    color: #5e5e5e
}

.dialogSiparis .tici-noty-notification-close-btn {
    border: 1px solid #909090;
    border-radius: 15px;
    width: 30px;
    height: 30px;
    text-align: center;
    padding: 2px;
    font-size: 19px;
    font-weight: 600;
    line-height: normal;
    color: #909090;
    position: absolute;
    right: 10px;
    top: 10px
}

@media screen and (max-width: 767px) {
    div.ticimaxDialogContent {
        height:calc(100% + 200px)
    }

    div.ticimaxDialogContent .ticimaxDialogContainer {
        margin-top: -100px
    }
}

.mobilTicimaxLogo {
    display: none;
    text-align: center;
    line-height: 1;
    margin-top: 10px;
    display: none
}

.hidden {
    display: none!important
}

@media(max-width: 480px) {
    .mobilTicimaxLogo {
        display:block
    }

    .mobilTicimaxLogo>img {
        width: 70px
    }
}

.navigation ul {
    list-style-type: none
}

.ProductList ul {
    list-style-type: none
}

.welcome ul {
    list-style-type: none
}

.urunTab>ul li {
    list-style-type: none
}

ul.breadcrumb {
    list-style-type: none
}

ul.sortingContent {
    list-style-type: none
}

.usernav ul {
    list-style-type: none
}

.CartProduct ul {
    list-style-type: none
}

.ProductDetail .product-social-icon-wrapper ul {
    list-style-type: none
}

ul#ulDuyurularTemplateData,ul#ulDovizKurlariTemplateData ul,ul#ulEncokSatilanUrunlerData {
    list-style-type: none
}

#footer ul {
    list-style-type: none
}

.ProductListContent:before {
    clear: both;
    display: table;
    content: ""
}

.ProductList:after {
    clear: both;
    display: table;
    content: ""
}

.popupSepet .hediyeCekiBtn {
    display: none
}

.sepetTopTutar {
    display: none
}

.CartProduct .SProduct li a span.sepetTopBirimFiyat {
    display: none !important
}

.SifremiUnuttum .line:after {
    clear: both;
    display: table;
    content: ""
}

.TempMenu li {
    list-style-type: none
}

#divNextProduct {
    height: 100%;
    text-align: center
}

#divNextProduct .productItem {
    margin: 0;
    background-color: #fff;
    padding: 0;
    border: 1px solid #f0f0f0
}

#divNextProduct .productItem:hover {
    background-color: #f0f0f0
}

#divNextProduct a {
    display: block;
    padding: 30px
}

#divNextProduct a:hover span {
    color: #333
}

#divNextProduct a .divNextProductButtonAlan {
    font-size: 40px;
    font-weight: 600
}

#divNextProduct span {
    display: block;
    font-weight: 600;
    font-size: 14px
}

#divNextProduct span.divNextProductWorld {
    display: inline-block
}

#divNextProduct span.divNextProductCount {
    display: inline-block
}

.insider-opt-in-notification {
    width: 422px;
    padding: 0 20px 10px 20px;
    border: 1px solid #bababa;
    border-radius: 3px;
    box-shadow: 0 4px 4px -2px #888;
    background-color: #fbfbfb;
    font-family: Arial,sans-serif;
    position: fixed;
    top: 0;
    left: 50%;
    margin-left: -211px;
    z-index: 9999999999999
}

.insider-opt-in-notification-inner-container {
    margin: 0;
    padding: 0 20px 10px 20px
}

.insider-opt-in-notification-image-container {
    float: left;
    margin: 13px 15px 0 0
}

.insider-opt-in-notification-image-container img {
    width: 65px;
    height: 65px
}

.insider-opt-in-notification-text-container {
    position: relative !important;
    padding: 10px 0 0 0 !important;
    color: #000 !important;
    text-align: left !important;
    margin: 0 !important;
    line-height: 1.4em !important
}

.insider-opt-in-notification-title {
    margin-bottom: 5px;
    text-align: left;
    font-size: 14px;
    font-weight: 700;
    line-height: 1.4em;
    color: #000;
    word-break: break-word;
    overflow: hidden
}

.insider-opt-in-notification-description {
    font-size: 12px;
    line-height: 1.4em;
    margin: 10px 0;
    padding: 0;
    text-align: left;
    word-break: break-word;
    overflow: hidden
}

.insider-brand-logo {
    float: left;
    font-size: 10px;
    margin-top: 8px;
    line-height: 18px
}

.insider-brand-logo img {
    width: 38px;
    margin-left: 3px;
    float: right
}

.insider-opt-in-notification-button-container {
    float: right !important
}

.insider-opt-in-notification-button {
    width: 90px;
    line-height: 18px;
    margin-left: 3px;
    padding: 5px;
    background: #f9f9f9;
    border: 1px solid #bababa;
    border-radius: 1px;
    display: inline-block;
    font-size: 14px;
    text-align: center;
    cursor: pointer;
    box-sizing: content-box
}

.insider-opt-in-allow-button {
    background: #00c33d;
    color: #fff;
    border-color: #059833
}

@media all and (max-width: 421px) {
    .insider-opt-in-notification {
        width:100%;
        left: 0;
        margin: 0;
        border-radius: 0;
        border-left: 0;
        border-right: 0;
        border-top: 0
    }
}

#lang_flag_container {
    position: absolute;
    left: auto;
    top: 0;
    z-index: 96
}

#langHover {
    padding: 13px 5px
}

#lang {
    line-height: 13px;
    font-size: 12px;
    color: #8d8d8d;
    padding: 0 0 0 37px;
    position: relative
}

#langHover.white {
    background-color: #fff;
    cursor: default
}

#lang-detail {
    background-color: #fff;
    position: absolute;
    top: 39px;
    left: 0;
    border-top: 1px solid #e9e9e9;
    width: 318px;
    -webkit-box-shadow: 0 10px 10px rgba(0,0,0,.4);
    -moz-box-shadow: 0 10px 10px rgba(0,0,0,.4);
    box-shadow: 0 10px 10px rgba(0,0,0,.4);
    z-index: 992
}

#lang-detail .language,#lang-detail .currency {
    padding: 15px 10px;
    float: left;
    -moz-box-sizing: border-box;
    -webkit-box-sizing: border-box;
    box-sizing: border-box;
    width: 50%
}

#lang-detail p {
    font-size: 14px;
    color: #2b2b2b;
    margin-bottom: 18px
}

#lang-detail .language a {
    display: block;
    height: 15px;
    line-height: 15px;
    padding-left: 24px;
    font-size: 12px;
    color: #8d8d8d;
    opacity: .5;
    margin-bottom: 15px
}

@media(min-width: 768px) {
    #lang-detail .language a:hover {
        opacity:1;
        color: #2b2b2b
    }

    #lang-detail .language a.active {
        opacity: 1;
        color: #2b2b2b;
        cursor: text
    }
}

@media(max-width: 767px) {
    #lang-detail .language a {
        opacity:1;
        color: #2b2b2b
    }
}

#divAvailableCountries {
    clear: both;
    padding: 0 10px 10px 10px
}

#teslimatUlkeSec p {
    padding: 5px 0;
    margin: 0 !important;
    font-weight: 600;
    font-size: 12px !important;
    text-align: left
}

#txtHeaderSeciliUlke {
    border: 1px solid #ddd;
    background: url(/Scripts/images/comboarrow.svg) no-repeat 95%center;
    width: 100%;
    padding: 0 5px;
    font-size: 12px
}

.teslimatUlkeSecUl {
    display: none;
    height: 120px;
    margin: 0;
    padding: 0;
    overflow-y: auto;
    overflow-x: hidden;
    position: absolute;
    background: #fff;
    left: 10px;
    right: 10px;
    border: 1px solid #eee
}

#txtHeaderSeciliUlke.active+.teslimatUlkeSecUl {
    display: block
}

.teslimatUlkeSecUl li {
    font-size: 12px;
    line-height: 15px;
    margin: 0;
    padding-left: 24px;
    height: 25px;
    cursor: pointer;
    text-align: left
}

.teslimatUlkeSecUl li:hover {
    background-color: #eee
}



.flag-ae {
    background-position: 0 -78px
}

.flag-af {
    background-position: 0 -158px
}

.flag-ag {
    background-position: 0 -240px
}

.flag-ai {
    background-position: 0 -318px
}

.flag-aj {
    background-position: 0 -398px
}

.flag-al {
    background-position: 0 -480px
}

.flag-am {
    background-position: 0 -558px
}

.flag-an {
    background-position: 0 -640px
}

.flag-ao {
    background-position: 0 -720px
}

.flag-aq {
    background-position: 0 -800px
}

.flag-as {
    background-position: 0 -958px
}

.flag-at {
    background-position: 0 -1040px
}

.flag-au {
    background-position: 0 -1118px
}

.flag-aw {
    background-position: 0 -1200px
}

.flag-az {
    background-position: 0 -1278px
}

.flag-ba {
    background-position: 0 -1360px
}

.flag-bb {
    background-position: 0 -1440px
}

.flag-bd {
    background-position: 0 -1520px
}

.flag-be {
    background-position: 0 -1600px
}

.flag-bf {
    background-position: 0 -1680px
}

.flag-bg {
    background-position: 0 -1760px
}

.flag-bh {
    background-position: 0 -1840px
}

.flag-bi {
    background-position: 0 -1920px
}

.flag-bj {
    background-position: 0 -2000px
}

.flag-bk {
    background-position: 0 -2078px
}

.flag-bm {
    background-position: 0 -2158px
}

.flag-bn {
    background-position: 0 -2238px
}

.flag-bo {
    background-position: 0 -2320px
}

.flag-bp {
    background-position: 0 -2400px
}

.flag-br {
    background-position: 0 -2480px
}

.flag-bs {
    background-position: 0 -2558px
}

.flag-bt {
    background-position: 0 -2640px
}

.flag-bv {
    background-position: 0 -2720px
}

.flag-bw {
    background-position: 0 -2800px
}

.flag-by {
    background-position: 0 -2878px
}

.flag-bz {
    background-position: 0 -2960px
}

.flag-ca {
    background-position: 0 -3038px
}

.flag-cc {
    background-position: 0 -3118px
}

.flag-cd {
    background-position: 0 -3200px
}

.flag-ce {
    background-position: 0 -3278px
}

.flag-cf {
    background-position: 0 -3360px
}

.flag-cg {
    background-position: 0 -3440px
}

.flag-ch {
    background-position: 0 -3520px
}

.flag-ci {
    background-position: 0 -3600px
}

.flag-ck {
    background-position: 0 -3678px
}

.flag-cl {
    background-position: 0 -3760px
}

.flag-cm {
    background-position: 0 -3840px
}

.flag-cn {
    background-position: 0 -3920px
}

.flag-co {
    background-position: 0 -4000px
}

.flag-cq {
    background-position: 0 -4078px
}

.flag-cr {
    background-position: 0 -4160px
}

.flag-cs {
    background-position: 0 -4240px
}

.flag-cu {
    background-position: 0 -4318px
}

.flag-cv {
    background-position: 0 -4400px
}

.flag-cw {
    background-position: 0 -4478px
}

.flag-cx {
    background-position: 0 -4558px
}

.flag-cy {
    background-position: 0 -4640px
}

.flag-cz {
    background-position: 0 -4720px
}

.flag-da {
    background-position: 0 -4800px
}

.flag-de {
    background-position: 0 -4880px
}

.flag-dj {
    background-position: 0 -4960px
}

.flag-dk {
    background-position: 0 -5038px
}

.flag-dm {
    background-position: 0 -5118px
}

.flag-do {
    background-position: 0 -5200px
}

.flag-dr {
    background-position: 0 -5280px
}

.flag-dz {
    background-position: 0 -5360px
}

.flag-ec {
    background-position: 0 -5438px
}

.flag-ee {
    background-position: 0 -5520px
}

.flag-eg {
    background-position: 0 -5600px
}

.flag-eh {
    background-position: 0 -5678px
}

.flag-ek {
    background-position: 0 -5760px
}

.flag-er {
    background-position: 0 -5918px
}

.flag-es {
    background-position: 0 -6000px
}

.flag-et {
    background-position: 0 -6080px
}

.flag-ez {
    background-position: 0 -6160px
}

.flag-fi {
    background-position: 0 -6238px
}

.flag-fj {
    background-position: 0 -6318px
}

.flag-fk {
    background-position: 0 -6398px
}

.flag-fm {
    background-position: 0 -6480px
}

.flag-fo {
    background-position: 0 -6560px
}

.flag-fr {
    background-position: 0 -6640px
}

.flag-fx {
    background-position: 0 -6720px
}

.flag-ga {
    background-position: 0 -6800px
}

.flag-gd {
    background-position: 0 -6960px
}

.flag-ge {
    background-position: 0 -7040px
}

.flag-gf {
    background-position: 0 -7120px
}

.flag-gg {
    background-position: 0 -7200px
}

.flag-gh {
    background-position: 0 -7280px
}

.flag-gi {
    background-position: 0 -7358px
}

.flag-gl {
    background-position: 0 -7440px
}

.flag-gm {
    background-position: 0 -7520px
}

.flag-gn {
    background-position: 0 -7600px
}

.flag-gp {
    background-position: 0 -7680px
}

.flag-gq {
    background-position: 0 -7760px
}

.flag-gr {
    background-position: 0 -7840px
}

.flag-gs {
    background-position: 0 -7918px
}

.flag-gt {
    background-position: 0 -8000px
}

.flag-gu {
    background-position: 0 -8078px
}

.flag-gv {
    background-position: 0 -8160px
}

.flag-gw {
    background-position: 0 -8240px
}

.flag-gy {
    background-position: 0 -8320px
}

.flag-ha {
    background-position: 0 -8400px
}

.flag-hk {
    background-position: 0 -8480px
}

.flag-hm {
    background-position: 0 -8558px
}

.flag-hn {
    background-position: 0 -8638px
}

.flag-hr {
    background-position: 0 -8718px
}

.flag-ht {
    background-position: 0 -8800px
}

.flag-hu {
    background-position: 0 -8880px
}

.flag-ic {
    background-position: 0 -8960px
}

.flag-id {
    background-position: 0 -9040px
}

.flag-ie {
    background-position: 0 -9118px
}

.flag-il {
    background-position: 0 -9200px
}

.flag-in {
    background-position: 0 -9280px
}

.flag-io {
    background-position: 0 -9358px
}

.flag-ku {
    background-position: 0 -9440px
}

.flag-ir {
    background-position: 0 -9520px
}

.flag-is {
    background-position: 0 -9600px
}

.flag-it {
    background-position: 0 -9680px
}

.flag-iv {
    background-position: 0 -9760px
}

.flag-ja {
    background-position: 0 -9840px
}

.flag-jm {
    background-position: 0 -9918px
}

.flag-jo {
    background-position: 0 -9998px
}

.flag-jp {
    background-position: 0 -10080px
}

.flag-ke {
    background-position: 0 -10160px
}

.flag-kg {
    background-position: 0 -10240px
}

.flag-kh {
    background-position: 0 -10320px
}

.flag-ki {
    background-position: 0 -10400px
}

.flag-km {
    background-position: 0 -10480px
}

.flag-kn {
    background-position: 0 -10560px
}

.flag-kp {
    background-position: 0 -10638px
}

.flag-kr {
    background-position: 0 -10720px
}

.flag-ks {
    background-position: 0 -10800px
}

.flag-kw {
    background-position: 0 -10878px
}

.flag-ky {
    background-position: 0 -10958px
}

.flag-kz {
    background-position: 0 -11040px
}

.flag-la {
    background-position: 0 -11120px
}

.flag-lb {
    background-position: 0 -11200px
}

.flag-lc {
    background-position: 0 -11278px
}

.flag-le {
    background-position: 0 -11360px
}

.flag-lg {
    background-position: 0 -11440px
}

.flag-lh {
    background-position: 0 -11520px
}

.flag-li {
    background-position: 0 -11600px
}

.flag-lk {
    background-position: 0 -11678px
}

.flag-lr {
    background-position: 0 -11758px
}

.flag-ls {
    background-position: 0 -11840px
}

.flag-lt {
    background-position: 0 -11920px
}

.flag-lu {
    background-position: 0 -12000px
}

.flag-lv {
    background-position: 0 -12080px
}

.flag-ly {
    background-position: 0 -12158px
}

.flag-ma {
    background-position: 0 -12240px
}

.flag-mb {
    background-position: 0 -12320px
}

.flag-mc {
    background-position: 0 -12400px
}

.flag-md {
    background-position: 0 -12478px
}

.flag-mg {
    background-position: 0 -12560px
}

.flag-mh {
    background-position: 0 -12638px
}

.flag-mi {
    background-position: 0 -12720px
}

.flag-mk {
    background-position: 0 -12800px
}

.flag-ml {
    background-position: 0 -12880px
}

.flag-mm {
    background-position: 0 -12958px
}

.flag-mn {
    background-position: 0 -13038px
}

.flag-mo {
    background-position: 0 -13120px
}

.flag-mo_old {
    background-position: 0 -13200px
}

.flag-mp {
    background-position: 0 -13278px
}

.flag-mq {
    background-position: 0 -13360px
}

.flag-mr {
    background-position: 0 -13440px
}

.flag-ms {
    background-position: 0 -13518px
}

.flag-mt {
    background-position: 0 -13600px
}

.flag-mu {
    background-position: 0 -13680px
}

.flag-mv {
    background-position: 0 -13760px
}

.flag-mw {
    background-position: 0 -13840px
}

.flag-mx {
    background-position: 0 -13920px
}

.flag-my {
    background-position: 0 -13998px
}

.flag-mz {
    background-position: 0 -14080px
}

.flag-na {
    background-position: 0 -14160px
}

.flag-nc {
    background-position: 0 -14240px
}

.flag-ne {
    background-position: 0 -14320px
}

.flag-nf {
    background-position: 0 -14398px
}

.flag-ng {
    background-position: 0 -14478px
}

.flag-nh {
    background-position: 0 -14560px
}

.flag-ni {
    background-position: 0 -14640px
}

.flag-nl {
    background-position: 0 -14720px
}

.flag-no {
    background-position: 0 -14800px
}

.flag-np {
    background-position: 0 -14880px
}

.flag-nr {
    background-position: 0 -14958px
}

.flag-nt {
    background-position: 0 -15040px
}

.flag-nu {
    background-position: 0 -15118px
}

.flag-nz {
    background-position: 0 -15198px
}

.flag-om {
    background-position: 0 -15280px
}

.flag-pa {
    background-position: 0 -15360px
}

.flag-pe {
    background-position: 0 -15440px
}

.flag-pf {
    background-position: 0 -15520px
}

.flag-pg {
    background-position: 0 -15600px
}

.flag-ph {
    background-position: 0 -15678px
}

.flag-pk {
    background-position: 0 -15760px
}

.flag-pl {
    background-position: 0 -15840px
}

.flag-pm {
    background-position: 0 -15920px
}

.flag-pn {
    background-position: 0 -15998px
}

.flag-po {
    background-position: 0 -16080px
}

.flag-pr {
    background-position: 0 -16160px
}

.flag-pt {
    background-position: 0 -16320px
}

.flag-pw {
    background-position: 0 -16400px
}

.flag-py {
    background-position: 0 -16480px
}

.flag-qa {
    background-position: 0 -16558px
}

.flag-re {
    background-position: 0 -16640px
}

.flag-rm {
    background-position: 0 -16718px
}

.flag-ro {
    background-position: 0 -16800px
}

.flag-ru {
    background-position: 0 -16880px
}

.flag-rw {
    background-position: 0 -16960px
}

.flag-ar {
    background-position: 0 -17040px
}

.flag-sb {
    background-position: 0 -17120px
}

.flag-sc {
    background-position: 0 -17198px
}

.flag-sd {
    background-position: 0 -17278px
}

.flag-se {
    background-position: 0 -17360px
}

.flag-sf {
    background-position: 0 -17440px
}

.flag-sg {
    background-position: 0 -17520px
}

.flag-sh {
    background-position: 0 -17598px
}

.flag-si {
    background-position: 0 -17678px
}

.flag-sj {
    background-position: 0 -17760px
}

.flag-sk {
    background-position: 0 -17840px
}

.flag-sl {
    background-position: 0 -17920px
}

.flag-sm {
    background-position: 0 -18000px
}

.flag-sn {
    background-position: 0 -18080px
}

.flag-so {
    background-position: 0 -18160px
}

.flag-sp {
    background-position: 0 -18240px
}

.flag-sr {
    background-position: 0 -18400px
}

.flag-srb {
    background-position: 0 -18400px
}

.flag-st {
    background-position: 0 -18478px
}

.flag-sv {
    background-position: 0 -18560px
}

.flag-sw {
    background-position: 0 -18640px
}

.flag-sy {
    background-position: 0 -18720px
}

.flag-sz {
    background-position: 0 -18800px
}

.flag-tc {
    background-position: 0 -18878px
}

.flag-td {
    background-position: 0 -18960px
}

.flag-tf {
    background-position: 0 -19040px
}

.flag-tg {
    background-position: 0 -19120px
}

.flag-th {
    background-position: 0 -19200px
}

.flag-tj {
    background-position: 0 -19278px
}

.flag-tk {
    background-position: 0 -19358px
}

.flag-tm {
    background-position: 0 -19438px
}

.flag-tn {
    background-position: 0 -19520px
}

.flag-to {
    background-position: 0 -19598px
}

.flag-tp {
    background-position: 0 -19680px
}

.flag-tr {
    background-position: 0 -19760px
}

.flag-ts {
    background-position: 0 -19840px
}

.flag-tt {
    background-position: 0 -19920px
}

.flag-tu {
    background-position: 0 -20000px
}

.flag-tv {
    background-position: 0 -20078px
}

.flag-tw {
    background-position: 0 -20160px
}

.flag-tw_old {
    background-position: 0 -20240px
}

.flag-tx {
    background-position: 0 -20318px
}

.flag-tz {
    background-position: 0 -20400px
}

.flag-ua {
    background-position: 0 -20480px
}

.flag-ug {
    background-position: 0 -20560px
}

.flag-en {
    background-position: 0 -20638px
}

.flag-um {
    background-position: 0 -20720px
}

.flag-up {
    background-position: 0 -20800px
}

.flag-us {
    background-position: 0 -20880px
}

.flag-uy {
    background-position: 0 -20960px
}

.flag-uz {
    background-position: 0 -21038px
}

.flag-va {
    background-position: 0 -21120px
}

.flag-vc {
    background-position: 0 -21200px
}

.flag-ve {
    background-position: 0 -21280px
}

.flag-vg {
    background-position: 0 -21358px
}

.flag-vi {
    background-position: 0 -21440px
}

.flag-vm {
    background-position: 0 -21520px
}

.flag-vn {
    background-position: 0 -21600px
}

.flag-vt {
    background-position: 0 -21680px
}

.flag-vu {
    background-position: 0 -21760px
}

.flag-wa {
    background-position: 0 -21840px
}

.flag-wf {
    background-position: 0 -21920px
}

.flag-ws {
    background-position: 0 -21998px
}

.flag-wz {
    background-position: 0 -22080px
}

.flag-ye {
    background-position: 0 -22160px
}

.flag-yt {
    background-position: 0 -22240px
}

.flag-yu {
    background-position: 0 -22320px
}

.flag-za {
    background-position: 0 -22400px
}

.flag-zm {
    background-position: 0 -22480px
}

.flag-zr {
    background-position: 0 -22560px
}

.flag-zw {
    background-position: 0 -22638px
}

.flag-mne {
    background-position: 0 -22720px
}

.clear-both {
    clear: both
}

#lang-detail .currency a {
    display: block;
    line-height: 20px;
    padding-left: 0;
    font-size: 12px;
    color: #8d8d8d;
    text-align: left;
    margin-bottom: 10px;
    opacity: .5;
    margin-bottom: 8px;
    display: block
}

#lang-detail .currency a i {
    width: 30px;
    height: 20px;
    line-height: 20px;
    -moz-border-radius: 50%;
    -webkit-border-radius: 50%;
    border-radius: 0;
    background-color: #000;
    color: #fff;
    text-align: center;
    font-size: 13px;
    margin-right: 5px
}

#lang-detail .currency a:hover {
    opacity: 1;
    color: #2b2b2b
}

#lang-detail .currency a.active {
    opacity: 1;
    color: #2b2b2b;
    cursor: text
}

i.fa.fa-iqd:before {
    content: "د.ع";
    margin-top: -2px;
    display: block
}

.currency-ron .fa {
    font-family: Verdana,Geneva,Tahoma,sans-serif;
    font-size: 12px
}

.currency-ron .fa:before {
    content: "RON";
    font-size: 9px;
    font-weight: 600;
    letter-spacing: 1px
}

.currency-aed .fa {
    font-family: Verdana,Geneva,Tahoma,sans-serif;
    font-size: 12px
}

.currency-aed .fa:before {
    content: "AED";
    font-size: 9px;
    font-weight: 600;
    letter-spacing: 1px
}

.currency-bhd .fa {
    font-family: Verdana,Geneva,Tahoma,sans-serif;
    font-size: 12px
}

.currency-bhd .fa:before {
    content: "BHD";
    font-size: 9px;
    font-weight: 600;
    letter-spacing: 1px
}

.currency-jod .fa {
    font-family: Verdana,Geneva,Tahoma,sans-serif;
    font-size: 12px
}

.currency-jod .fa:before {
    content: "JOD";
    font-size: 9px;
    font-weight: 600;
    letter-spacing: 1px
}

.currency-kwd .fa {
    font-family: Verdana,Geneva,Tahoma,sans-serif;
    font-size: 12px
}

.currency-kwd .fa:before {
    content: "KWD";
    font-size: 9px;
    font-weight: 600;
    letter-spacing: 1px
}

.currency-omr .fa {
    font-family: Verdana,Geneva,Tahoma,sans-serif;
    font-size: 12px
}

.currency-omr .fa:before {
    content: "OMR";
    font-size: 9px;
    font-weight: 600;
    letter-spacing: 1px
}

.currency-azn .fa {
    font-family: Verdana,Geneva,Tahoma,sans-serif;
    font-size: 12px
}

.currency-azn .fa:before {
    content: "AZN";
    font-size: 9px;
    font-weight: 600;
    letter-spacing: 1px
}

.currency-qar .fa {
    font-family: Verdana,Geneva,Tahoma,sans-serif;
    font-size: 12px
}

.currency-qar .fa:before {
    content: "QAR";
    font-size: 9px;
    font-weight: 600;
    letter-spacing: 1px
}

.currency-sar .fa {
    font-family: Verdana,Geneva,Tahoma,sans-serif;
    font-size: 12px
}

.currency-sar .fa:before {
    content: "SAR";
    font-size: 9px;
    font-weight: 600;
    letter-spacing: 1px
}

.currency-aud .fa {
    font-family: Verdana,Geneva,Tahoma,sans-serif;
    font-size: 12px
}

.currency-aud .fa:before {
    content: "AUD";
    font-size: 9px;
    font-weight: 600;
    letter-spacing: 1px
}

#store_region_container {
    position: absolute;
    top: 2px
}

#divMagazaBolge {
    min-width: 320px
}

.divMagazaBolgeTittle {
    display: block;
    font-size: 16px;
    font-weight: 600;
    margin-bottom: 10px
}

#divMagazaBolgeUlke {
    margin-bottom: 15px
}

#divMagazaBolgeUlke label {
    display: block;
    font-weight: normal;
    display: block;
    color: #666
}

#divMagazaBolgeUlke select {
    display: block;
    width: 100%;
    padding: 8px 0;
    background-color: #fff;
    border: 1px solid #ccc;
    line-height: 1;
    height: auto
}

#divMagazaBolgeSehir {
    margin-bottom: 15px
}

#divMagazaBolgeSehir label {
    display: block;
    margin-bottom: 5px
}

#divMagazaBolgeSehir select {
    display: block;
    width: 100%;
    padding: 8px 0;
    background-color: #fff;
    border: 1px solid #ccc;
    line-height: 1;
    height: auto
}

#divMagazaBolgeIlce {
    margin-bottom: 15px
}

#divMagazaBolgeIlce label {
    display: block;
    margin-bottom: 5px
}

#divMagazaBolgeIlce select {
    display: block;
    width: 100%;
    padding: 8px 0;
    background-color: #fff;
    border: 1px solid #ccc;
    line-height: 1;
    height: auto
}

#divMagazaBolgeSemt {
    margin-bottom: 15px
}

#divMagazaBolgeSemt label {
    display: block;
    margin-bottom: 5px
}

#divMagazaBolgeSemt select {
    display: block;
    width: 100%;
    padding: 8px 0;
    background-color: #fff;
    border: 1px solid #ccc;
    line-height: 1;
    height: auto
}

#divMagazaBolge a {
    display: block;
    text-align: center
}

.divMagazaBolgeAdres {
    margin-top: 10px;
    max-height: 200px;
    overflow-y: auto
}

.divMagazaBolgeAdresTitle {
    font-size: 15px;
    font-weight: bold
}

.divMagazaBolgeAdres li {
    display: flex;
    flex-direction: row;
    margin-top: 10px
}

.divMagazaBolgeAdres li>input {
    margin-top: auto;
    margin-bottom: auto
}

.divMagazaBolgeAdres li>div {
    display: flex;
    flex-direction: column;
    margin-left: 10px;
    font-size: 12px
}

.divMagazaBolgeAdres .AdresTanim {
    font-weight: bold;
    font-size: 13px
}

table.ticimaxTable {
    width: 100%;
    border-collapse: collapse;
    margin-top: 10px
}

.ticimaxTable tr {
    background-color: #f2f2f0
}

.ticimaxTable tbody tr {
    border-bottom: 10px solid #fff
}

.ticimaxTable th {
    background: #fff;
    font-size: 13px;
    font-weight: 600
}

.ticimaxTable td,.ticimaxTable th {
    padding: 9px;
    text-align: left
}

.ticimaxTable thead tr th {
    border: 0
}

@media only screen and (max-width: 760px),(min-device-width:768px) and (max-device-width:1024px) {
    .ticimaxTable table,.ticimaxTable thead,.ticimaxTable tbody,.ticimaxTable th,.ticimaxTable td,.ticimaxTable tr {
        display:block
    }

    .ticimaxTable thead tr {
        position: absolute;
        top: -9999px;
        left: -9999px
    }

    .ticimaxTable tr {
        border: 1px solid #ccc
    }

    .ticimaxTable td {
        border: none;
        border-bottom: 1px solid #eee;
        position: relative;
        padding-left: 50%
    }

    .ticimaxTable td:before {
        position: absolute;
        top: 6px;
        left: 6px;
        width: 45%;
        padding-right: 10px;
        white-space: nowrap
    }
}

@media screen and (max-width: 760px),(min-device-width:768px) and (max-device-width:1024px) {
    table td:before {
        content:attr(data-label);
        float: left;
        font-weight: bold
    }
}

.textalignCenter {
    text-align: center !important
}

.adreslerimBaslikRenk {
    color: #f68428
}

.lbMapPoint {
    width: 30px;
    height: 30px;
    cursor: pointer
}

#lbUrunView {
    background: #fff;
    border: 1px solid #ddd;
    padding: 10px 15px
}

#lbUrunView .lbSpanUrunAdi {
    display: block;
    font-size: 22px;
    color: #000
}

#lbUrunView .lbSpanUrunFiyat {
    display: block;
    color: #000;
    margin-top: 10px;
    margin-bottom: 10px;
    font-size: 16px
}

#lbUrunView .lbSpanUrunSatinAl {
    display: block
}

#lbUrunView .lbSpanUrunSatinAl a {
    color: #000;
    font-size: 16px
}

.uyegirisPopup a.fancybox-close {
    background: none transparent;
    color: #000;
    right: 0
}

.uyegirisPopup a.fancybox-close:after {
    color: #000
}

@-webkit-keyframes progress-bar-stripes {
    from {
        background-position: 40px 0
    }

    to {
        background-position: 0 0
    }
}

@-o-keyframes progress-bar-stripes {
    from {
        background-position: 40px 0;
    }

    to {
        background-position: 0 0;
    }
}

@keyframes progress-bar-stripes {
    from {
        background-position: 40px 0
    }

    to {
        background-position: 0 0
    }
}

.progress {
    overflow: hidden;
    height: 20px;
    margin-bottom: 20px;
    background-color: #f5f5f5;
    border-radius: 4px;
    -webkit-box-shadow: inset 0 1px 2px rgba(0,0,0,.1);
    box-shadow: inset 0 1px 2px rgba(0,0,0,.1)
}

.progress-bar {
    float: left;
    width: 0%;
    height: 100%;
    font-size: 12px;
    line-height: 20px;
    color: #fff;
    text-align: center;
    background-color: #337ab7;
    -webkit-box-shadow: inset 0 -1px 0 rgba(0,0,0,.15);
    box-shadow: inset 0 -1px 0 rgba(0,0,0,.15);
    -webkit-transition: width .6s ease;
    -o-transition: width .6s ease;
    transition: width .6s ease
}

.progress-striped .progress-bar,.progress-bar-striped {
    background-image: -webkit-linear-gradient(45deg,rgba(255,255,255,.15) 25%,transparent 25%,transparent 50%,rgba(255,255,255,.15) 50%,rgba(255,255,255,.15) 75%,transparent 75%,transparent);
    background-image: -o-linear-gradient(45deg,rgba(255,255,255,.15) 25%,transparent 25%,transparent 50%,rgba(255,255,255,.15) 50%,rgba(255,255,255,.15) 75%,transparent 75%,transparent);
    background-image: linear-gradient(45deg,rgba(255,255,255,.15) 25%,transparent 25%,transparent 50%,rgba(255,255,255,.15) 50%,rgba(255,255,255,.15) 75%,transparent 75%,transparent);
    -webkit-background-size: 40px 40px;
    background-size: 40px 40px
}

.progress.active .progress-bar,.progress-bar.active {
    -webkit-animation: progress-bar-stripes 2s linear infinite;
    -o-animation: progress-bar-stripes 2s linear infinite;
    animation: progress-bar-stripes 2s linear infinite
}

.progress-bar-success {
    background-color: #5cb85c
}

.progress-striped .progress-bar-success {
    background-image: -webkit-linear-gradient(45deg,rgba(255,255,255,.15) 25%,transparent 25%,transparent 50%,rgba(255,255,255,.15) 50%,rgba(255,255,255,.15) 75%,transparent 75%,transparent);
    background-image: -o-linear-gradient(45deg,rgba(255,255,255,.15) 25%,transparent 25%,transparent 50%,rgba(255,255,255,.15) 50%,rgba(255,255,255,.15) 75%,transparent 75%,transparent);
    background-image: linear-gradient(45deg,rgba(255,255,255,.15) 25%,transparent 25%,transparent 50%,rgba(255,255,255,.15) 50%,rgba(255,255,255,.15) 75%,transparent 75%,transparent)
}

.progress-bar-info {
    background-color: #5bc0de
}

.progress-striped .progress-bar-info {
    background-image: -webkit-linear-gradient(45deg,rgba(255,255,255,.15) 25%,transparent 25%,transparent 50%,rgba(255,255,255,.15) 50%,rgba(255,255,255,.15) 75%,transparent 75%,transparent);
    background-image: -o-linear-gradient(45deg,rgba(255,255,255,.15) 25%,transparent 25%,transparent 50%,rgba(255,255,255,.15) 50%,rgba(255,255,255,.15) 75%,transparent 75%,transparent);
    background-image: linear-gradient(45deg,rgba(255,255,255,.15) 25%,transparent 25%,transparent 50%,rgba(255,255,255,.15) 50%,rgba(255,255,255,.15) 75%,transparent 75%,transparent)
}

.progress-bar-warning {
    background-color: #f0ad4e
}

.progress-striped .progress-bar-warning {
    background-image: -webkit-linear-gradient(45deg,rgba(255,255,255,.15) 25%,transparent 25%,transparent 50%,rgba(255,255,255,.15) 50%,rgba(255,255,255,.15) 75%,transparent 75%,transparent);
    background-image: -o-linear-gradient(45deg,rgba(255,255,255,.15) 25%,transparent 25%,transparent 50%,rgba(255,255,255,.15) 50%,rgba(255,255,255,.15) 75%,transparent 75%,transparent);
    background-image: linear-gradient(45deg,rgba(255,255,255,.15) 25%,transparent 25%,transparent 50%,rgba(255,255,255,.15) 50%,rgba(255,255,255,.15) 75%,transparent 75%,transparent)
}

.progress-bar-danger {
    background-color: #d9534f
}

.progress-striped .progress-bar-danger {
    background-image: -webkit-linear-gradient(45deg,rgba(255,255,255,.15) 25%,transparent 25%,transparent 50%,rgba(255,255,255,.15) 50%,rgba(255,255,255,.15) 75%,transparent 75%,transparent);
    background-image: -o-linear-gradient(45deg,rgba(255,255,255,.15) 25%,transparent 25%,transparent 50%,rgba(255,255,255,.15) 50%,rgba(255,255,255,.15) 75%,transparent 75%,transparent);
    background-image: linear-gradient(45deg,rgba(255,255,255,.15) 25%,transparent 25%,transparent 50%,rgba(255,255,255,.15) 50%,rgba(255,255,255,.15) 75%,transparent 75%,transparent)
}

#mainHolder_txtbxSifre {
    padding-right: 30px
}

[ng-cloak],[data-ng-cloak],[x-ng-cloak],.ng-cloak,.x-ng-cloak {
    display: none !important
}

.translate-cloak {
    display: none
}

.alert {
    padding: 3px;
    margin: 5px 0;
    border: 1px solid transparent;
    display: block;
    font-weight: bold;
    width: 100%
}

.alert-success {
    color: #3c763d;
    background-color: #dff0d8;
    border-color: #d6e9c6
}

.alert-info {
    color: #31708f;
    background-color: #d9edf7;
    border-color: #bce8f1
}

.alert-warning {
    color: #8a6d3b;
    background-color: #fcf8e3;
    border-color: #faebcc
}

.alert-danger {
    color: #a94442;
    background-color: #f2dede;
    border-color: #ebccd1
}

.sayfaYukleniyor {
    position: relative
}

.sayfaYukleniyor:after {
    content: '';
    background: rgba(255,255,255,.5);
    position: absolute;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    z-index: 99
}

.sayfaYukleniyor:before {
    content: '';
    font-family: 'FontAwesome';
    position: absolute;
    font-size: 50px;
    left: 50%;
    top: 50%;
    z-index: 999;
    margin-left: -25px;
    margin-top: -25px;
    color: #000;
    -webkit-animation: fa-spin 2s infinite linear;
    animation: fa-spin 2s infinite linear
}

.butonDisabled {
    opacity: .6;
    cursor: not-allowed !important
}

a {
    cursor: pointer
}

#divStokYok {
    display: block;
    background-color: #dfdfdf;
    text-align: center;
    padding: 10px 0;
    line-height: normal;
    margin: 15px 0;
    border-radius: 4px;
    float: left;
    width: 100%;
    clear: left
}

#divStokYok:after {
    clear: both;
    display: table;
    content: ""
}

.eksecenekLine.kutuluvaryasyon {
    overflow: inherit
}

.size_box.nostok {
    position: relative
}

.btnnostok {
    text-align: center;
    position: absolute;
    display: none;
    background-color: #ddd;
    color: #000;
    padding: 5px 2px;
    font-size: 10px;
    left: -120%;
    right: -120%;
    line-height: 14px !important;
    top: 100%;
    z-index: 10000000;
    margin-top: 6px
}

.btnnostok:after {
    content: "";
    position: absolute;
    top: -6px;
    left: 50%;
    border-bottom: 6px solid #ddd;
    border-left: 6px solid transparent;
    border-right: 6px solid transparent;
    margin-left: -6px
}

.btnnostok i {
    display: block;
    font-size: 16px;
    margin-top: 5px
}

.size_box.nostok:hover .btnnostok {
    display: block !important
}

.btnnostok.selected {
    background-color: #f1b9bc;
    border-color: #e89296;
    color: #f00 !important
}

.btnnostok.selected:after {
    border-bottom-color: #f1b9bc
}

.btnnostok:before {
    background-color: transparent;
    height: 6px;
    display: block;
    left: 0;
    right: 0;
    top: 0;
    content: "";
    width: 100%;
    left: 0;
    right: 0;
    position: absolute;
    top: -6px
}

.btnnostok.selected i {
    color: #f00 !important
}

.SmallImages .AltVideoThumb {
    position: relative
}

.SmallImages .AltVideoThumb i {
    position: absolute;
    bottom: 0;
    top: 0;
    width: 30px;
    height: 30px;
    border: 1px solid #000;
    border-radius: 100%;
    line-height: 28px;
    left: 0;
    right: 0;
    margin: auto;
    text-align: center
}

#divThumpVideo {
    position: relative
}

#divThumpVideo i {
    position: absolute;
    bottom: 0;
    top: 0;
    width: 30px;
    height: 30px;
    border: 1px solid #000;
    border-radius: 100%;
    line-height: 28px;
    left: 0;
    right: 0;
    margin: auto;
    text-align: center
}

#vdUrunVideo {
    max-width: 100%
}

.productItem .productImage video {
    height: 100%;
    position: absolute;
    left: 0;
    right: 0;
    top: 0;
    bottom: 0;
    margin: auto;
    width: 100%;
    transition: ease-in-out .3s all;
    -webkit-appearance: none;
    -moz-appearance: none;
    -ms-appearance: none;
    -o-appearance: none;
    appearance: none
}

.videoAutoPlayFalse .divVideoPlayButton {
    display: block
}

.videoAutoPlayTrue .divVideoPlayButton {
    display: none
}

.productItem .productImage a.urunListeVideoPlay {
    position: absolute;
    left: 10px;
    top: 0;
    padding: 0;
    height: 0;
    margin: 0;
    display: inline-block;
    width: auto;
    z-index: 999999
}

.productItem .productImage a.urunListeVideoPlay i {
    font-size: 20px
}

#txtbxurunSiparisAdedi-error {
    display: none !important
}

.urunsecoverlay {
    position: fixed;
    background-color: #000;
    opacity: .5;
    z-index: 99999;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%
}

.urunsecbody #divUrunEkSecenek {
    background-color: #fff;
    position: relative;
    z-index: 1000000;
    padding: 5px;
    border-radius: 5px
}

.urunsecbody #divUrunEkSecenek .tooltipp {
    position: absolute;
    top: -50px;
    left: 50%;
    margin-left: -130px;
    background-color: #f00;
    width: 260px;
    height: 40px;
    line-height: 40px;
    text-align: center;
    color: #fff;
    border-radius: 5px
}

.eksecenekLine {
    clear: both;
    display: block;
    margin-bottom: 3px
}

.detayEdit {
    position: fixed;
    left: 0;
    z-index: 9999;
    top: 300px;
    -webkit-box-shadow: 3px 3px 8px 0 rgba(186,179,186,1);
    -moz-box-shadow: 3px 3px 8px 0 rgba(186,179,186,1);
    box-shadow: 3px 3px 8px 0 rgba(186,179,186,1)
}

.btnEdit {
    padding: 5px;
    background-color: #fff;
    color: #000;
    display: block;
    border-radius: 2px;
    position: relative;
    cursor: pointer
}

.editUl {
    display: none
}

.editUl a {
    display: block;
    background-color: #fff;
    border-radius: 2px;
    line-height: 34px;
    padding: 0 80px 0 5px;
    font-size: 14px;
    border: 1px solid #e1e1e1;
    margin: 5px 0 5px 0
}

.editUl a:hover {
    background-color: #f1f1f1
}

.btnEdit:hover .editUl {
    display: block;
    padding: 5px 0
}

.whatsApp {
    position: relative;
    color: #fff;
    cursor: pointer;
    background-color: #6dc33a;
    border-radius: 3px;
    box-sizing: border-box;
    line-height: 20px;
    display: inline-block;
    width: 93px;
    text-align: center
}

.whatsApp:hover,whatsApp label:hover,.whatsApp i:hover {
    color: #fff
}

.telegram {
    position: relative;
    color: #fff;
    cursor: pointer;
    background-color: #34abe0;
    border-radius: 3px;
    box-sizing: border-box;
    line-height: 20px;
    display: inline-block;
    width: 93px;
    text-align: center
}

.telegram:hover,telegram label:hover,.telegram i:hover {
    color: #fff
}

.rating {
    color: #a9a9a9;
    margin: 0;
    padding: 0
}

ul.rating {
    display: inline-block
}

.rating li {
    list-style-type: none;
    display: inline-block;
    padding: 1px;
    text-align: center;
    font-weight: bold;
    cursor: pointer;
    width: 19px;
    height: 20px;
    position: relative;
    margin-right: 3px
}

ul.rating li i.starItem {
    font-size: 18px;
    height: 20px;
    line-height: 20px;
    position: absolute;
    left: 0;
    right: 0;
    margin: auto
}

ul.rating li i.starItem:hover {
    font-size: 20px
}

.rating .filled {
    color: #ffd700
}

.taksitWrapper .taksitBlock {
    float: left;
    width: 100%;
    display: block;
    text-align: center;
    padding: 5px 10px 20px 10px
}

.taksitWrapper .taksitBlock .taksitLogo {
    height: 30px;
    margin: 0 auto 10px auto;
    display: block
}

.taksitWrapper .taksitBlock .taksitBlockContent {
    width: 100%;
    max-width: 330px;
    margin: 0 auto
}

.taksitWrapper .taksitBlock .taksitBlockContent table {
    width: 100%;
    background: #fff;
    border: 1px solid #eee;
    border-spacing: 0;
    border-radius: 3px;
    overflow: hidden
}

.taksitWrapper .taksitBlock .taksitBlockContent table thead {
    color: #fff
}

.taksitWrapper .taksitBlock .taksitBlockContent thead tr {
    background: #0f3a54;
    color: #fff
}

.taksitWrapper .taksitBlock .taksitBlockContent table tr {
    height: 40px;
    line-height: 40px
}

.taksitWrapper .taksitBlock .taksitBlockContent table tbody tr:nth-child(even) {
    background: #eee
}

.taksitWrapper .taksitBlock .taksitBlockContent tr td {
    padding: 0 5px
}

.taksitWrapper .taksitBlock .taksitBlockContent tr td.taksitAdet {
    max-width: 100px;
    font-weight: 500
}

.taksitWrapper .taksitBlock .taksitBlockContent tr td {
    padding: 5px;
    line-height: 20px
}

.taksitWrapper .taksitBlock .taksitBlockContent table tbody tr:hover {
    background: #ddd
}

.taksitWrapper .taksitBlock .taksitBlockContent thead .taksitColor-1 {
    background: #7cc242
}

.taksitWrapper .taksitBlock .taksitBlockContent thead .taksitColor-2 {
    background: #fdbf57
}

.taksitWrapper .taksitBlock .taksitBlockContent thead .taksitColor-3 {
    background: #6950a2
}

.taksitWrapper .taksitBlock .taksitBlockContent thead .taksitColor-4 {
    background: #e01d6e
}

.taksitWrapper .taksitBlock .taksitBlockContent thead .taksitColor-5 {
    background: #ed1c24
}

.taksitWrapper .taksitBlock .taksitBlockContent thead .taksitColor-6 {
    background: #00a6d4
}

.taksitWrapper .taksitBlock .taksitBlockContent thead .taksitColor-7 {
    background: #ee3623
}

.taksitWrapper .taksitBlock .taksitBlockContent thead .taksitColor-9 {
    background: #a3a3a3
}

.taksitWrapper .taksitBlock .taksitBlockContent thead .taksitColor-10 {
    background: #2484c6
}

.taksitWrapper .taksitBlock .taksitBlockContent thead .taksitColor-11 {
    background: #056bb6
}

.taksitWrapper .taksitBlock .taksitBlockContent thead .taksitColor-12 {
    background: #221f1f
}

.taksitWrapper .taksitBlock .taksitBlockContent thead .taksitColor-13 {
    background: #0053a0
}

.taksitWrapper .taksitBlock .taksitBlockContent thead .taksitColor-14 {
    background: #fdb813
}

.taksitWrapper .taksitBlock .taksitBlockContent thead .taksitColor-15 {
    background: #036647
}

.taksitWrapper .taksitBlock .taksitBlockContent thead .taksitColor-16 {
    background: #00c3b3
}

.taksitWrapper .taksitBlock .taksitBlockContent thead .taksitColor-17 {
    background: #e8ce00
}

.taksitWrapper .taksitBlock .taksitBlockContent thead .taksitColor-18 {
    background: #e9690e
}

.taksitWrapper .taksitBlock .taksitBlockContent thead .taksitColor-19 {
    background: #009862
}

div.odemeSecenekItem {
    background: #dfecd4;
    width: 100%;
    max-width: 200px;
    padding: 10px;
    border-radius: 3px;
    border: 1px solid #9ec77f;
    font-size: 12px;
    color: #656565;
    float: left;
    margin: 0 10px 10px 0
}

div.odemeSecenekItem b {
    font-size: 18px;
    display: block;
    padding-top: 3px
}

@media(min-width: 550px) and (max-width:990px) {
    .taksitWrapper .taksitBlock {
        width:50%
    }

    .taksitWrapper .taksitBlock:nth-child(2n+1) {
        clear: left
    }
}

@media(min-width: 991px) and (max-width:1200px) {
    .taksitWrapper .taksitBlock {
        width:33%
    }

    .taksitWrapper .taksitBlock:nth-child(3n+1) {
        clear: left
    }
}

@media screen and (min-width: 1200px) {
    .taksitWrapper .taksitBlock {
        width:25%
    }

    .taksitWrapper .taksitBlock:nth-child(4n+1) {
        clear: left
    }
}

.riSingle {
    display: inline-block;
    white-space: nowrap;
    text-align: left;
    box-sizing: border-box;
    -moz-box-sizing: border-box;
    -ms-box-sizing: border-box;
    -webkit-box-sizing: border-box;
    -khtml-box-sizing: border-box;
    vertical-align: middle
}

.riSingle a.riUp {
    display: inline-block;
    height: 8px;
    width: 15px;
    vertical-align: top
}

.riSingle a.riDown {
    display: inline-block;
    height: 8px;
    width: 15px;
    vertical-align: top;
    margin-left: -15px;
    vertical-align: bottom
}

.RadInput a {
    display: block;
    overflow: hidden;
    position: relative;
    outline: 0;
    z-index: 2;
    text-indent: -2222px;
    text-align: center;
    text-decoration: none
}

.quickViewIco {
    display: none;
    position: absolute;
    left: 20px;
    top: 30%;
    right: 20px;
    text-align: center
}

.productItem:hover .quickViewIco {
    display: block
}

.globalSelect {
    font-size: 11px;
    border: 1px solid #eaeaea;
    padding: 3px;
    width: 120px
}

#divTemaOnizleme {
    margin: 0 auto;
    background-color: #000;
    padding: 5px 20px;
    overflow: hidden;
    display: flex
}

#divTemaOnizleme select {
    border: 1px solid #ccc;
    padding: 6px 12px;
    height: 34px;
    width: 100%;
    color: #555;
    margin: 5px 0;
    background-color: #fff;
    background-image: none;
    border-radius: 4px
}

#divTemaOnizleme span {
    margin: 0 auto;
    color: #fff
}

#btnTemaOnizlemeIptal {
    margin-top: 4px;
    float: right;
    line-height: 34px;
    padding: 0 8px;
    background-color: #fff;
    border: 1px solid #ccc;
    color: #000;
    border-radius: 4px;
    cursor: pointer
}

.noProduct {
    background: #fff;
    border-radius: 50%;
    width: 212px;
    height: 212px;
    border: 1px solid #c6c8ca;
    color: #b1b3b7;
    text-align: center;
    font-family: sans-serif;
    padding-top: 40px;
    margin: 20px auto;
    box-sizing: border-box
}

.noProduct span {
    display: block;
    margin-top: 15px;
    font-weight: 700;
    font-size: 16px
}

.noProduct img {
    margin-left: -7px
}

.baglanButton {
    line-height: 34px;
    background-color: #ef233c;
    color: #fff;
    display: block;
    text-align: center;
    font-size: 14px;
    margin: 10px 0;
    padding: 5px 0
}

.baglanButton a {
    border: none;
    width: 100%;
    height: 100%;
    line-height: 1;
    display: block;
    background-color: transparent;
    cursor: pointer;
    font-size: 14px;
    color: #fff;
    font-weight: 500;
    padding: 15px 0
}

#divFacebookLoginContainer.baglanButton {
    background: #3b5998
}

#divTwitterLoginContainer.baglanButton {
    background: #2ba9e1
}

#divGoogleLoginContainer.baglanButton {
    background: #dd4b39;
    margin-bottom: 10px
}

.asortiListItem {
    display: block
}

.asortiListItem:after {
    clear: both;
    display: table;
    content: ""
}

.asortiListItem>div {
    float: left;
    padding: 5px 0
}

.asortiMiktar {
    min-width: 20%
}

.asortiAyrac {
    min-width: 5%
}

ul.breadcrumb {
    list-style-type: none;
    padding: 0;
    display: inline-block;
    
    margin: 0;
    font-size: 13px
}

ul.breadcrumb:after {
    clear: both;
    display: table;
    content: ""
}

ul.breadcrumb li {
    display: inline-block;
    margin: 0;
    padding: 0;
    font-size: 13px;
    
}

ul.breadcrumb li:first-child a {
    font-size: 13px
}

ul.breadcrumb li a {
    display: inline-block;
    line-height: normal;
    font-size: 13px
}

ul.breadcrumb li a span {
    font-size: 13px
}

.proCategoryTitle:after {
    clear: both;
    display: table;
    content: ""
}

a#linkOncekiSayfa {
    display: inline-block;
    
    line-height: normal;
    padding: 0;
    margin: 0;
    position: relative;
    color: #000;
    font-size: 13px
}

.taksitBaslik1 {
    background: none center center no-repeat #7cc242
}

.taksitBaslik2 {
    background: none center center no-repeat #fdbf57
}

.taksitBaslik3 {
    background: none center center no-repeat #6950a2
}

.taksitBaslik4 {
    background: none center center no-repeat #e01d6e
}

.taksitBaslik5 {
    background: none center center no-repeat #ed1c24
}

.taksitBaslik6 {
    background: none center center no-repeat #00a6d4
}

.taksitBaslik7 {
    background: none center center no-repeat #ee3623
}

.taksitBaslik8 {
    background: none center center no-repeat #00aedb
}

.taksitBaslik9 {
    background: none center center no-repeat #a3a3a3
}

.taksitBaslik10 {
    background: none center center no-repeat #2e3192
}

.taksitBaslik11 {
    background: none center center no-repeat #056bb6
}

.taksitBaslik12 {
    background: none center center no-repeat #221f1f
}

.taksitBaslik13 {
    background: none center center no-repeat #0053a0
}

.taksitBaslik14 {
    background: none center center no-repeat #ffdf00
}

.taksitBaslik15 {
    background: none center center no-repeat #024d39
}

.taksitBaslik16 {
    background: none center center no-repeat #8c1639
}

.taksitBaslik17 {
    background: none center center no-repeat #e9690e
}

.taksitBaslik18 {
    background: none center center no-repeat #e9690e
}

.taksitBaslik19 {
    background: none center center no-repeat #fff
}

.taksitBaslik20 {
    background: none center center no-repeat #7cc242
}

.taksitBaslik21 {
    background: none center center no-repeat #ffdf00
}

.taksitBaslik23 {
    background: none center center no-repeat #e01d6e
}

.taksitBaslik img {
    display: inline-block
}

ul.breadcrumb {
    list-style-type: none;
    padding: 0;
    display: inline-block;
    
}

ul.breadcrumb li {
    display: inline-block;
    margin: 0;
    padding: 0;
    font-size: 13px;
    
}

ul.breadcrumb li:first-child a {
    font-size: 13px
}

ul.breadcrumb li a {
    display: inline-block;
    line-height: normal;
    font-size: 13px
}

ul.breadcrumb li a span {
    font-size: 13px
}

.proCategoryTitle:after {
    clear: both;
    display: table;
    content: ""
}

a#linkOncekiSayfa {
    display: inline-block;
    
    line-height: normal;
    padding: 0;
    margin: 0;
    position: relative;
    color: #000;
    font-size: 13px
}

.flex-caption {
    width: 100%;
    left: 0;
    bottom: 0;
    background: rgba(0,0,0,.5);
    color: #fff;
    text-shadow: 0 -1px 0 rgba(0,0,0,.3);
    font-size: 14px;
    line-height: 18px
}

.jautoImages {
    background-color: #fff;
    z-index: 9999
}

.jautoImages .ui-menu-item {
    height: 52px;
    overflow: hidden;
    padding: 0 !important;
    margin-bottom: 10px !important
}

.jautoImages .ui-menu-item:after {
    clear: both;
    display: table;
    content: ""
}

.jautoImages .complate_image {
    float: left;
    width: 20%;
    height: 50px;
    display: block;
    margin-right: 10px;
    text-align: center
}

.jautoImages .complate_image img {
    max-width: 100%;
    max-height: 100%
}

.jautoImages .complate_text {
    float: left;
    width: 70%;
    display: block;
    line-height: 1;
    font-size: 12px;
    padding: 5px 0 0 0;
    
    color: #000;
    text-align: left
}

#divMobileImageList .owl-dots {
    text-align: center;
    position: relative;
    margin-top: 10px
}

#divMobileImageList .owl-dots .owl-dot {
    background: #000;
    width: 10px;
    height: 10px;
    display: inline-block;
    border-radius: 50%;
    margin: 0 4px
}

#divMobileImageList .owl-dots .owl-dot.active {
    background: #d9d9d9
}

.istekListeAra {
    min-width: 320px;
    max-width: 400px;
    margin: 0 auto
}

.istekListeAraTittle {
    font-size: 22px;
    color: #000;
    text-align: center;
    border-bottom: 1px solid #e1e1e1;
    padding-bottom: 15px;
    margin-top: 40px;
    margin-bottom: 40px
}

.istekListeAra .button {
    width: 100%;
    text-align: center;
    font-size: 14px;
    font-weight: 600;
    margin-top: 15px;
    min-height: 0;
    line-height: normal;
    padding: 12px 0;
    display: block
}

.istekListeAra .textbox {
    width: 100%;
    text-align: center;
    font-size: 14px;
    font-weight: 600;
    margin-top: 15px;
    min-height: 40px;
    line-height: 40px;
    padding: 0;
    background-color: #f3f3f3;
    border: 1px solid #e1e1e1
}

.istekListeAra .validate {
    margin-top: 10px
}

.istekListeSonuc {
    border: 1px solid #e1e1e1;
    padding: 10%
}

.istekListeSonuc .istekListeItemTittle {
    text-align: center;
    font-size: 16px
}

.istekDetayGeri {
    text-align: center;
    display: block;
    margin-bottom: 40px
}

.istekDetayGeri .button {
    display: inline-block;
    background-color: #f3f3f3;
    border: 1px solid #ddd;
    border-radius: 4px;
    color: #2b2b2b;
    padding-left: 30px;
    padding-right: 30px
}

.istekDetayGeri:after {
    clear: both;
    display: table;
    content: ""
}

.istekDetayIcerik .ProductList:after {
    clear: both;
    display: table;
    content: ""
}

.istekDetayIcerik .productItem {
    overflow: inherit
}

.istekUrunDetay .urunBaslik {
    color: #2b2b2b;
    font-size: 13px;
    margin-top: 20px;
    margin-bottom: 8px;
    overflow: hidden;
    display: block
}

.istekUrunDetay .satinAl {
    display: block
}

.istekUrunDetay .satinAl:after {
    clear: both;
    display: table;
    content: ""
}

.istekUrunDetay .satinAl .button {
    padding: 8px 20px;
    border-radius: 4px;
    display: inline-block
}

.istekUrunDetay .istekUrunFiyat {
    color: #2b2b2b;
    font-size: 13px;
    margin-bottom: 20px;
    height: 15px;
    overflow: hidden;
    display: block
}

.istekUrunDetay .istekUrunDurum {
    font-weight: bold;
    font-size: 14px
}

.ArkadasiniDavetetBlock ul {
    list-style-type: none
}

.ArkadasiniDavetetBlock button.accordion {
    color: #2b2b2b;
    background-color: transparent;
    font-weight: 600;
    cursor: pointer;
    padding: 15px 0;
    width: 100%;
    border: none;
    text-align: center;
    outline: none;
    font-size: 14px;
    transition: .4s
}

.ArkadasiniDavetetBlock .Block_Text {
    background-color: #fff;
    padding: 0 10% 20px
}

.ArkadasiniDavetetBlock .button.linkOlustur {
    background-color: #f3f3f3;
    border: 1px solid #e1e1e1;
    border-radius: 4px;
    font-size: 14px;
    color: #2b2b2b
}

.ArkadasiniDavetetBlock .button {
    margin: 10px 0 0 0
}

.ArkadasiniDavetetBlock .textbox {
    background-color: #f3f3f3;
    border: 1px solid #e1e1e1;
    box-shadow: none
}

.ArkadasiniDavetetBlock hr {
    display: block;
    height: 1px;
    border: 0;
    border-top: 1px solid #e1e1e1;
    margin: 20px 0 0 0;
    padding: 0
}

.divOzellestirmeContent {
    background-color: #fff;
    max-width: 360px;
    padding: 20px;
    min-width: 360px
}

.ozellestirmeTittle {
    border-bottom: 1px solid #e1e1e1;
    padding-bottom: 8px;
    margin-bottom: 10px
}

.ozellestirmeTittle .colLeft {
    text-align: left;
    width: 100%;
    font-weight: 600;
    color: #000;
    font-size: 18px
}

.ozellestirmeTittle .colLeft span {
    font-weight: 600;
    color: #000;
    font-size: 18px
}

.ozellestirmeTittle .colLeft span i {
    margin-right: 5px;
    font-size: 14px
}

.ozellestirmeTittle .colCenter {
    float: left;
    width: 33%;
    font-weight: 600;
    color: #000;
    font-size: 18px
}

.ozellestirmeTittle .colRight {
    float: left;
    width: 33%;
    font-weight: 600;
    color: #000;
    font-size: 18px
}

.ozellestirmeTittle:after {
    clear: both;
    display: table;
    content: ""
}

.ozellestirmeitem:after {
    clear: both;
    display: table;
    content: ""
}

.ozellestirmeitem div {
    text-align: left;
    float: left;
    font-weight: 600;
    color: #000;
    font-size: 13px
}

.ozellestirmeitem .colLeft {
    color: #000;
    font-weight: 500;
    font-size: 13px;
    width: 100%;
    line-height: 1.5
}

.ozellestirmeitem .colRight {
    color: #3d3a3a;
    width: 100%;
    font-size: 13px;
    font-weight: 600;
    line-height: 1.5
}

.ozellestirmeUcret {
    border-bottom: 1px solid #e1e1e1;
    padding: 8px 0;
    margin: 10px 0
}

.ozellestirmeUcret .colLeft {
    text-align: left;
    font-weight: 700;
    color: #000;
    font-size: 14px
}

.ozellestirmeUcret .colLeft i {
    margin-right: 5px;
    font-size: 14px
}

.ozellestirmeUcret .colRight span {
    color: #000;
    font-size: 13px;
    font-weight: 600
}

.brand-list {
    width: 100%
}

.brands-head {
    width: 100%;
    line-height: 58px;
    color: #111;
    font-size: 14px;
    font-weight: 900
}

.brands-head:after {
    clear: both;
    display: table;
    content: ""
}

#allletters {
    background-color: #ddd;
    margin-bottom: 20px;
    padding: 5px;
    margin-top: 10px;
    list-style-type: none
}

#allletters:after {
    clear: both;
    display: table;
    content: ""
}

#allletters li {
    float: left;
    margin-right: 5px;
    text-align: center;
    width: 39px;
    height: 25px;
    background-color: #fff
}

#allletters li a {
    float: left;
    width: 100%;
    float: left;
    line-height: 25px;
    padding: 0;
    font-size: 18px;
    font-weight: bold;
    color: #000;
    text-transform: uppercase
}

.brands-wrapper .brands-block {
    background-color: #ddd;
    min-height: 335px;
    padding: 20px 20px 20px 160px;
    position: relative
}

.brands-wrapper .brand-letter {
    background-color: #000;
    position: absolute;
    left: 0;
    top: 0;
    width: 150px;
    height: 100%;
    padding: 0
}

.brands-wrapper .brand-letter>h4 {
    position: absolute;
    left: 0;
    top: 0;
    right: 0;
    bottom: 0;
    font-size: 0;
    text-align: center;
    width: 100%;
    margin-left: 0;
    padding-top: 0
}

.brands-wrapper .brand-letter>h4>a {
    position: absolute;
    left: 0;
    top: 0;
    right: 0;
    bottom: 0;
    color: #fff;
    font-size: 160px;
    line-height: 1.2;
    text-indent: 0
}

.brands-wrapper .brand-name-list {
    float: left;
    width: 100%;
    max-height: 295px;
    overflow-y: auto;
    overflow-x: hidden
}

.brands-wrapper .brand-name-list::-webkit-scrollbar {
    width: 4px
}

.brands-wrapper .brand-name-list::-webkit-scrollbar-track {
    background: #e5e5e5
}

.brands-wrapper .brand-name-list::-webkit-scrollbar-thumb {
    background: #000
}

.brands-wrapper .brand-name-list .fl {
    float: left;
    width: 100%;
    list-style-type: none
}

.brands-wrapper .brand-name-list .fl li {
    float: left;
    width: 25%
}

.brands-wrapper .brand-name-list .fl li a {
    background: #fff;
    color: #000;
    font-size: 12px;
    padding: 0 11px;
    line-height: 25px;
    float: left;
    margin-bottom: 5px
}

@media(max-width: 768px) {
    .brands-wrapper .brands-block {
        min-height:175px;
        height: 175px;
        padding: 20px 20px 20px 95px
    }

    .brands-wrapper .brand-letter {
        width: 85px
    }

    .brands-wrapper .brand-letter>h4>a {
        font-size: 98px
    }

    .brands-wrapper .brand-name-list .fl li {
        width: 100%
    }

    #allletters li {
        width: 29px;
        margin-bottom: 5px
    }

    #allletters li a {
        font-size: 15px
    }
}

#divMagazaStok {
    float: left;
    margin: 0 0 0 0
}

#divMagazalar {
    max-width: 460px;
    padding: 30px 20px
}

#divMagazalar:after {
    clear: both;
    display: table;
    content: ""
}

#divMagazalar .divMagazalarTittle {
    font-size: 18px;
    font-weight: 500;
    border-bottom: 1px solid #e1e1e1;
    padding-bottom: 10px;
    margin-bottom: 20px;
    color: #000;
    width: 100%
}

#divMagazalar .divMagazalarTittle i {
    font-size: 14px;
    margin-right: 8px
}

#divMagazalar .adresDetayItemContent {
    display: flex;
    margin-left: -5px;
    margin-right: -5px
}

#divMagazalar .adresDetayUlkeItem,.adresDetaySehirItem,.adresDetayIlceItem {
    margin: 5px;
    flex-grow: 3
}

#divMagazalar select {
    border: 1px solid #e1e1e1;
    height: 40px;
    background-color: #fff;
    display: block;
    padding: 0;
    margin: 0
}

#divMagazalar .divMagazaHeader {
    width: 100%;
    float: left;
    border-top: 1px solid #e1e1e1;
    margin-top: 20px;
    margin-bottom: 10px;
    padding: 10px 0 0
}

#divMagazalar .divMagazaHeader:after {
    clear: both;
    display: table;
    content: ""
}

#divMagazalar .divMagazaHeader>div {
    width: 25%;
    float: left;
    margin-right: 0;
    text-align: center;
    font-size: 12px;
    color: #000;
    font-weight: 500
}

#divMagazalar .divMagazaContent {
    float: left;
    width: 100%;
    border: 1px solid #e1e1e1;
    max-height: 200px;
    overflow-y: auto;
    overflow-x: hidden
}

#divMagazalar .divMagazaContent:after {
    clear: both;
    display: table;
    content: ""
}

#divMagazalar .divMagazaItem {
    float: left;
    display: block;
    width: 100%;
    background-color: #f5f4f4;
    padding: 0 0
}

#divMagazalar .divMagazaItem:nth-child(2n) {
    background-color: #fff
}

#divMagazalar .divMagazaItem:after {
    clear: both;
    display: table;
    content: ""
}

#divMagazalar .divMagazaItem>div {
    width: 25%;
    float: left;
    text-align: center;
    font-size: 12px;
    color: #000
}

#divMagazalar .divMagazaItem>div.span-1 {
    padding: 15px 0;
    line-height: normal
}

#divMagazalar .divMagazaItem>div.span-2 {
    padding: 15px 0;
    line-height: normal
}

#divMagazalar .divMagazaItem>div.span-3 {
    padding: 15px 0;
    line-height: normal
}

#divMagazalar .divMagazaItem>div.span-4 {
    padding: 15px 0;
    line-height: normal
}

#divMagazalar .divMagazaItem>div.span-4 a {
    line-height: normal;
    font-size: 12px
}

@media(max-width: 768px) {
    #divMagazalar>div {
        width:100%;
        font-size: 11px;
        margin-bottom: 8px
    }
}

@media(max-width: 991px) {
    .leftImage img {
        max-width:100%
    }
}

.categoryOverlay {
    visibility: visible;
    background: #000;
    opacity: .5;
    position: fixed;
    left: 0;
    right: 0;
    top: 0;
    bottom: 0;
    z-index: 9999;
    height: 100%
}

.categoryOverlay #loader {
    position: absolute;
    left: 50%;
    top: 50%;
    margin: -75px 0 0 -75px;
    border: 8px solid #f3f3f3;
    border-radius: 50%;
    border-top: 8px solid #000;
    width: 100px;
    height: 100px;
    -webkit-animation: spin 2s linear infinite;
    animation: spin 2s linear infinite
}

@-webkit-keyframes spin {
    0% {
        -webkit-transform: rotate(0deg)
    }

    100% {
        -webkit-transform: rotate(360deg)
    }
}

@keyframes spin {
    0% {
        transform: rotate(0deg)
    }

    100% {
        transform: rotate(360deg)
    }
}

.productItem .productTimer {
    position: absolute;
    left: 0;
    right: 0;
    top: 0;
    background: #f1efef;
    padding: 10px 0;
    z-index: 9
}

.productItem .productTimer span.productTimerContent {
    display: inline-block;
    min-width: 45px
}

.productItem .productTimer span.productTimerContent span {
    font-size: 17px;
    color: #282929;
    text-align: center;
    font-weight: 600;
    border-right: 1px solid #ded6d6;
    display: block
}

.productItem .productTimer span.productTimerContent span:last-child {
    display: block;
    font-size: 12px;
    color: #919191;
    line-height: 1;
    font-weight: 400;
    border-right: 0
}

.productItem .productTimer span.productTimerContent .productTimerSecond {
    border-right: 0
}

.productItem .productPrice.showLastDayCounter {
    display: block;
    float: none;
    position: relative;
    text-align: center;
    height: auto
}

.productItem .productPrice.showLastDayCounter .discountPrice {
    display: block;
    float: none;
    position: relative;
    text-align: center
}

.productItem .productPrice.showLastDayCounter .discountPrice span {
    display: inline-block;
    font-size: 12px;
    text-decoration: line-through;
    font-weight: 400
}

.productItem .productPrice.showLastDayCounter .regularPrice {
    display: block;
    float: none;
    position: relative;
    text-align: center
}

.productItem .productPrice.showLastDayCounter .regularPrice span {
    display: inline-block;
    font-size: 14px;
    text-decoration: none;
    font-weight: 600
}

.siparisTakipDetayi .siparisTutucu .siparisBilgi .siparisBilgiSag span.siparisTakipDurum {
    font-weight: 600;
    color: #000;
    padding: 5px 0
}

.leftImage .productTimer {
    z-index: 99;
    background: rgba(6,6,6,.5) !important;
    width: 100%;
    padding: 6px 0 !important;
    text-align: center
}

.leftImage .productTimer>span {
    display: inline-block;
    vertical-align: top;
    position: relative;
    width: 40px;
    min-width: 0 !important
}

.leftImage .productTimer>span:after {
    content: ':';
    color: #fff;
    float: right;
    position: absolute;
    right: -3px;
    top: 0;
    bottom: 0
}

.leftImage .productTimer>span:last-child:after {
    display: none
}

.leftImage .productTimer>span span {
    display: block;
    clear: both;
    text-align: center;
    width: 100%;
    color: #fff !important
}

.leftImage .productTimer>span span:last-child {
    font-size: 10px
}

.leftImage .productTimer span.productTimerContent span {
    border-right: 0 !important;
    font-weight: 500 !important;
    font-size: 12px !important;
    transform: none !important
}

.centerCount .Block_item.blokUrunArama {
    width: 300px;
    margin: 0 auto;
    float: none
}

.centerCount .Block_item.blokUrunArama .Block_Title {
    margin: 0 0 10px 0;
    padding: 10px 0
}

.centerCount .Block_item.blokUrunArama .textbox.blokAramaText {
    margin: 0 0 10px 0
}

.centerCount .Block_item.SepetBlock {
    width: 300px;
    margin: 0 auto;
    float: none
}

.centerCount .Block_item.SepetBlock .Block_Title {
    margin: 0 0 10px 0;
    padding: 10px 0
}

.centerCount .Block_item.Anket {
    width: 300px;
    margin: 0 auto;
    float: none
}

.centerCount .Block_item.Anket .Block_Title {
    margin: 0 0 10px 0;
    padding: 10px 0
}

.centerCount .Block_item.ArkadasiniDavetetBlock {
    width: 300px;
    margin: 0 auto;
    float: none
}

.centerCount .Block_item.ArkadasiniDavetetBlock .Block_Title {
    margin: 0 0 10px 0;
    padding: 10px 0
}

.centerCount .Block_item.ArkadasiniDavetetBlock .Block_Text {
    padding: 0
}

.centerCount .Block_item.DovizKurlari {
    width: 300px;
    margin: 0 auto;
    float: none
}

.centerCount .Block_item.DovizKurlari .Block_Title {
    margin: 0 0 10px 0;
    padding: 10px 0
}

.centerCount .Block_item.Duyurular {
    width: 300px;
    margin: 0 auto;
    float: none
}

.centerCount .Block_item.Duyurular .Block_Title {
    margin: 0 0 10px 0;
    padding: 10px 0
}

.centerCount .Block_item.EmailListesi {
    width: 300px;
    margin: 0 auto;
    float: none
}

.centerCount .Block_item.EmailListesi .Block_Title {
    margin: 0 0 10px 0;
    padding: 10px 0
}

.centerCount .Block_item.EmailListesi .textbox#txtBlokEBultenKaydet {
    margin: 0 0 10px 0
}

.centerCount .Block_item.Haberler {
    width: 300px;
    margin: 0 auto;
    float: none
}

.centerCount .Block_item.Haberler .Block_Title {
    margin: 0 0 10px 0;
    padding: 10px 0
}

.centerCount .Block_item.YanUyeGirisi {
    width: 300px;
    margin: 0 auto;
    float: none
}

.centerCount .Block_item.YanUyeGirisi .Block_Title {
    margin: 0 0 10px 0;
    padding: 10px 0
}

.centerCount .Block_item.YanUyeGirisi .textbox#txtUyeGirisEmail {
    margin: 0 0 10px 0
}

.centerCount .Block_item.YanUyeGirisi .textbox#txtGuvenlikKodu {
    margin: 0 0 10px 0
}

.userWrapper.xIDDiv img {
    display: inline-block
}

.userWrapper.xIDDiv a {
    display: inline-block;
    line-height: normal
}

.xIDSifreDegistir img {
    display: inline-block
}

.xIDSifreDegistir a {
    display: inline-block;
    line-height: normal
}

.centerCount .Block_item.YanUyeGirisi .textbox#txtUyeGirisPassword {
    margin: 0 0 10px 0
}

.centerCount .Block_item.Istatistik {
    width: 300px;
    margin: 0 auto;
    float: none
}

.centerCount .Block_item.Istatistik .Block_Title {
    margin: 0 0 10px 0;
    padding: 10px 0
}

.centerCount .Block_item.SonEklenenUrunler {
    width: 300px;
    margin: 0 auto;
    float: none
}

.centerCount .Block_item.SonEklenenUrunler .Block_Title {
    margin: 0 0 10px 0;
    padding: 10px 0
}

.fancybox-inner #dinamikFormPopup {
    width: 320px;
    padding: 15px
}

.dinamikFormContainer * {
    -moz-box-sizing: border-box;
    -webkit-box-sizing: border-box;
    box-sizing: border-box
}

.dinamikFormContainer h3 {
    padding: 10px 0;
    display: block;
    border-bottom: 1px dotted #efefef;
    font-weight: normal;
    font-size: 16px;
    margin-top: 20px
}

.dinamikFormContainer label {
    font-size: 13px;
    color: #000;
    font-weight: bold;
    display: block;
    clear: both;
    padding: 10px 0;
    overflow: hidden;
    font-size: 12px
}

.dinamikFormContainer fieldset label {
    float: left;
    width: auto;
    margin-right: 20px
}

.dinamikFormContainer fieldset label.imageboxRadio {
    float: left;
    width: 100px;
    clear: right
}

.dinamikFormContainer fieldset label.imageboxRadio img {
    max-width: 100%
}

.dinamikFormContainer fieldset {
    border: 0;
    padding: 0;
    margin: 0
}

.dinamikFormContainer .textbox {
    width: 100%;
    border: solid 1px #e5e5e5;
    height: 40px;
    line-height: 40px;
    border-radius: 0;
    box-shadow: none;
    margin: 0;
    float: none
}

.dinamikFormContainer select {
    width: 100%;
    border: solid 1px #e5e5e5;
    height: 40px;
    line-height: 40px;
    border-radius: 0;
    box-shadow: none;
    margin: 0;
    float: none
}

.dinamikFormContainer textarea {
    width: 100%;
    border: solid 1px #e5e5e5;
    min-height: 80px;
    line-height: 20px;
    border-radius: 0;
    box-shadow: none;
    margin: 0;
    float: none
}

.dinamikFormContainer .form_validation {
    color: #f00
}

.dinamikFormContainer button {
    display: block;
    margin: 20px 0;
    background-color: #000;
    text-align: center;
    color: #fff;
    box-shadow: none;
    border: 0;
    padding: 10px 0;
    width: 100%;
    cursor: pointer
}

.dinamikFormContainer .intl-tel-input input,.intl-tel-input input[type=text],.intl-tel-input input[type=tel] {
    position: relative;
    z-index: 0;
    margin-top: 0 !important;
    margin-bottom: 0 !important;
    padding-left: 48px !important;
    margin-left: 0;
    transition: background-color 100ms ease-out;
    width: 100%;
    width: 100%;
    border: solid 1px #e5e5e5;
    height: 40px;
    line-height: 40px;
    border-radius: 0;
    box-shadow: none;
    margin: 0;
    float: none;
    color: #666;
    font-size: 14px
}

.blogCenter {
    width: 73%;
    float: left;
    margin-top: 20px
}

.blogRight {
    width: 25%;
    float: right;
    margin-top: 20px
}

.tici-blok-ul {
    position: relative;
    display: block;
    overflow: hidden;
    margin-left: -10px;
    margin-right: -10px
}

.tici-blok-ul:after {
    clear: both;
    display: table;
    content: ""
}

.tici-blok-ul li {
    float: left;
    width: 50%;
    margin-bottom: 20px;
    padding: 0 10px;
    -webkit-box-sizing: border-box;
    -moz-box-sizing: border-box;
    box-sizing: border-box
}

.tici-blok-ul li:first-child {
    float: left;
    width: 100%
}

.tici-blok-ul li:nth-child(2n+2) {
    clear: left
}

.tici-blok-ul .pi-picture {
    height: 0;
    position: relative;
    background: #fff;
    padding-bottom: 56%;
    overflow: hidden;
    width: 100%;
    border-bottom: 0
}

.tici-blok-ul .pi-picture a {
    display: block;
    position: relative;
    height: 100%;
    top: 0;
    left: 0;
    text-align: center;
    align-items: center;
    width: 100%;
    padding-bottom: 56%
}

.tici-blok-ul .pi-picture a:before {
    position: absolute;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    z-index: 1;
    display: inline-block;
    visibility: visible;
    background-color: rgba(28,28,28,.7);
    content: '';
    opacity: 0;
    -webkit-transition: all .35s;
    -moz-transition: all .35s;
    -ms-transition: all .35s;
    -o-transition: all .35s;
    transition: all .35s;
    pointer-events: none !important;
    backface-visibility: hidden;
    -webkit-backface-visibility: hidden
}

.tici-blok-ul .pi-picture a img {
    max-width: 100%;
    max-height: 100%;
    height: auto;
    position: absolute;
    left: 0;
    right: 0;
    top: 0;
    bottom: 0;
    margin: auto
}

.tici-blok-ul li:hover .pi-picture>a:before {
    visibility: visible;
    opacity: 1
}

.tici-blok-ul .pi-titles {
    margin: 8px 0;
    height: 45px;
    overflow: hidden
}

.tici-blok-ul .pi-titles h3 {
    letter-spacing: -.045em;
    font-weight: 500;
    font-size: 18px;
    line-height: 1.3;
    display: block;
    color: #282828
}

.tici-blok-ul .pi-titles h3 a {
    -webkit-transition: all .25s ease;
    -moz-transition: all .25s ease;
    -ms-transition: all .25s ease;
    -o-transition: all .25s ease;
    transition: all .25s ease;
    font-weight: 500;
    font-size: 18px;
    line-height: 1.3;
    display: block;
    color: #282828
}

.tici-blok-ul .pi-titles h3 a:hover {
    text-decoration: underline
}

.tici-blok-ul .pi-categories {
    margin: 8px 0
}

.tici-blok-ul .pi-categories * {
    line-height: 20px;
    font-size: 12px !important;
    color: #9c9b9b
}

.tici-blok-ul .pi-categories .pi-cat {
    text-decoration: underline
}

.tici-blok-ul .pi-text {
    overflow: hidden;
    height: 80px
}

.tici-blok-ul .pi-text p * {
    line-height: 20px;
    font-size: 13px !important
}

.tici-blok-ul .pi-etiket {
    margin: 8px 0;
    overflow: hidden;
    white-space: nowrap;
    text-overflow: ellipsis
}

.tici-blok-ul .pi-etiket span {
    line-height: 18px;
    font-size: 12px !important;
    color: #9c9b9b
}

.tici-blok-ul .pi-link {
    margin-top: 10px
}

.tici-blok-ul .pi-link a {
    color: #000;
    text-decoration: underline;
    font-size: 13px;
    display: inline-block
}

.blog-sayfalama ul {
    display: block;
    text-align: center;
    margin: 20px 0
}

.blog-sayfalama ul:After {
    clear: both;
    display: table;
    content: ""
}

.blog-sayfalama ul li {
    display: inline-block;
    margin: 0 5px 8px 5px
}

.blog-sayfalama ul li a {
    padding: 5px 8px;
    background-color: #eee;
    line-height: 25px
}

.blog-sayfalama ul li a:hover {
    background-color: #000;
    color: #fff
}

.blog-sayfalama ul li a.active {
    background-color: #000;
    color: #fff
}

.blogkategoribaslik {
    color: #000;
    font-weight: 600;
    border-bottom: 2px solid #ddd;
    display: block;
    padding: 0 0 10px 0;
    margin-bottom: 10px
}

.blogKategori ul li {
    margin-bottom: 10px;
    padding-bottom: 10px;
    border-bottom: 1px solid #ddd
}

.blogKategori ul li a {
    text-decoration: underline
}

.bloksonyazilarbaslik {
    color: #000;
    font-weight: 600;
    border-bottom: 2px solid #ddd;
    display: block;
    padding: 0 0 10px 0;
    margin-bottom: 10px
}

.blokSonYazilar ul li {
    margin-bottom: 10px;
    padding-bottom: 10px;
    border-bottom: 1px solid #ddd
}

.blokSonYazilar ul li a {
    text-decoration: underline
}

.blog-h1 {
    display: block;
    margin-bottom: 15px;
    font-size: 20px;
    text-align: center;
    display: block;
    text-decoration: underline
}

.blog-img {
    max-width: 100%;
    margin-bottom: 20px;
    display: block
}

.blog-img img {
    max-width: 100%
}

.yayintarih {
    text-align: left;
    display: block;
    font-size: 13px;
    margin: 10px 0;
    text-decoration: underline
}

.blog-listeyedon {
    color: #000;
    font-size: 13px;
    display: inline-block;
    margin-top: 10px;
    text-decoration: underline;
    font-weight: 600
}

@media(max-width: 768px) {
    .blogCenter {
        width:100%
    }

    .blogRight {
        display: none
    }

    .tici-blok-ul li {
        width: 100%
    }
}

.favoriListelerimBlokContent {
    margin: 20px 0
}

.favoriListelerimBlokContent:after {
    clear: both;
    display: table;
    content: ""
}

.favoriListelerimBlokContent .favoriBlokTittle {
    font-size: 16px;
    display: block;
    margin-bottom: 20px
}

.favoriListelerimBlokContent .tab {
    overflow: hidden;
    border-bottom: 2px solid #4c4c4c;
    position: relative
}

.favoriListelerimBlokContent .tab:after {
    clear: both;
    display: table;
    content: ""
}

.favoriListelerimBlokContent .tab .tablinks {
    font-weight: 500;
    background-color: transparent;
    border: 0;
    padding: 10px 25px;
    font-size: 14px;
    float: left;
    cursor: pointer;
    color: #b2b2b2;
    letter-spacing: .5px;
    border-left: 2px solid transparent;
    border-top: 2px solid transparent;
    border-right: 2px solid transparent
}

.favoriListelerimBlokContent .tab .tablinks.active {
    color: #4c4c4c;
    border-left: 2px solid #4c4c4c;
    border-top: 2px solid #4c4c4c;
    border-right: 2px solid #4c4c4c
}

.favoriListelerimBlokContent .tab #aFavoriGrupEklemeAlanGoster {
    position: absolute;
    right: 0;
    top: 0;
    border: 1px solid #b2b2b2;
    padding: 4px 20px
}

.favoriListelerimBlokContent .tab #aFavoriGrupEklemeAlanGoster:hover {
    background-color: #4c4c4c;
    color: #fff
}

.favoriListelerimBlokContent .tabcontent {
    display: none;
    margin-top: 30px
}

.favoriListelerimBlokContent #divFavoriGroup:after {
    clear: both;
    display: table;
    content: ""
}

.favoriGrupItem {
    float: left;
    width: 100%;
    border-bottom: 2px solid #b2b2b2;
    margin-bottom: 20px;
    padding-bottom: 20px
}

.favoriGrupItemName {
    float: left;
    width: 30%;
    padding: 9px 0
}

.favoriGrupItemAdet {
    float: left;
    width: 14%;
    padding: 9px 0
}

.favoriGrupItemImg {
    float: left;
    width: 35%
}

.favoriGrupItemSepeteekle {
    float: right;
    margin-top: 5px
}

.favoriGrupItemSepeteekle a {
    padding: 5px 30px;
    border: 1px solid #ddd;
    background-color: #ddd;
    position: relative;
    display: block
}

.favoriGrupItemSepeteekle a i {
    position: absolute;
    right: 10px;
    top: 10px
}

.favoriGrupItemSepeteekle a:hover {
    background-color: #4c4c4c;
    color: #fff
}

.favoriListelerimBlokContent .favoriGrupItemImg ul li {
    float: left;
    width: 40px;
    height: 40px;
    overflow: hidden;
    display: block;
    margin-right: 10px
}

.favoriListelerimBlokContent .favoriGrupItemImg ul li img {
    max-width: 100%
}

.siparisGrupItem {
    float: left;
    width: 100%;
    border-bottom: 2px solid #b2b2b2;
    margin-bottom: 20px;
    padding-bottom: 20px
}

.siparisGrupItem:after {
    clear: both;
    display: table;
    content: ""
}

.siparisGrupItem .siparisGrupStok {
    float: left;
    width: 15%;
    padding: 9px 0
}

.siparisGrupItem .siparisGrupTarih {
    float: left;
    width: 15%;
    padding: 9px 0
}

.siparisGrupItem .siparisGrupFiyat {
    float: left;
    width: 35%;
    padding: 9px 0
}

.siparisGrupItem .siparisGrupsepetekle {
    float: right;
    margin-top: 5px
}

.siparisGrupItem .siparisGrupsepetekle a {
    padding: 5px 30px;
    border: 1px solid #ddd;
    background-color: #ddd;
    position: relative;
    display: block;
    color: #4c4c4c
}

.siparisGrupItem .siparisGrupsepetekle a i {
    position: absolute;
    right: 10px;
    top: 10px
}

.siparisGrupItem .siparisGrupsepetekle a:hover {
    background-color: #4c4c4c;
    color: #fff
}

#divFavoriGrupEklemeAlan {
    float: right
}

#divFavoriGrupEklemeAlan:after {
    clear: both;
    display: table;
    content: ""
}

.FavoriGrupEklemeAlanTxtbox {
    float: left
}

.FavoriGrupEklemeAlanTxtbox input {
    background-color: #fff;
    padding: 8px 20px 8px 5px
}

.FavoriGrupEklemeAlanEkle {
    float: left;
    margin-left: 5px
}

.FavoriGrupEklemeAlanEkle a {
    display: block;
    padding: 8px 15px;
    background-color: #ddd;
    line-height: normal;
    border: 1px solid #ddd;
    background-color: #ddd;
    color: #4c4c4c
}

.FavoriGrupEklemeAlanEkle a:hover {
    background-color: #4c4c4c;
    color: #fff
}

.FavoriGrupEklemeAlanKapat {
    float: left;
    margin-left: 5px
}

.FavoriGrupEklemeAlanKapat a {
    display: block;
    padding: 8px 15px;
    background-color: #ddd;
    line-height: normal;
    border: 1px solid #ddd;
    background-color: #ddd;
    color: #4c4c4c
}

.FavoriGrupEklemeAlanKapat a:hover {
    background-color: #4c4c4c;
    color: #fff
}

.favori-modal-content {
    width: 700px
}

.divFavoriGrupDetayTop {
    background-color: #ddd;
    padding: 3px 10px;
    color: #4c4c4c;
    position: relative
}

.divFavoriGrupDetayTopTarih {
    position: absolute;
    right: 10px;
    top: 13px
}

.divFavoriGrupDetayTop:after {
    clear: both;
    display: table;
    content: ""
}

.divFavoriGrupDetayTop #spnGrupAdi {
    margin: 6px 0;
    display: block;
    line-height: 22px;
    float: left
}

.divFavoriGrupDetayTop #btnShowGrupAdiDuzenle i {
    margin-left: 10px;
    color: #4c4c4c;
    margin-top: 10px;
    float: left
}

.divFavoriGrupDetayTop #inptGrupAdi {
    float: left;
    width: 300px;
    margin: 0;
    float: left;
    border-radius: 0;
    box-shadow: none;
    border: 1px solid #ddd
}

.divFavoriGrupDetayTop #btnGrupAdiKaydet {
    display: block;
    float: left;
    margin-left: 10px;
    font-size: 13px;
    padding: 8px 15px;
    background-color: #ddd;
    line-height: normal;
    border: 1px solid #ddd;
    background-color: #4c4c4c;
    color: #fff
}

#divFavoriUrunAraContent {
    margin-top: 10px
}

#divFavoriUrunAraContent input {
    display: block;
    width: 100%;
    border-radius: 0;
    box-shadow: none;
    border: 1px solid #ddd;
    padding: 10px
}

#favoriGrupUrunler:after {
    clear: both;
    display: table;
    content: ""
}

.favoriGrupUrunItem:after {
    clear: both;
    display: table;
    content: ""
}

.favoriGrupUrunItem {
    float: left;
    width: 100%;
    margin-top: 10px;
    border-bottom: 2px solid #ddd;
    display: block;
    padding-bottom: 10px
}

.favoriGrupUrunItem .favoriGrupUrunItemImg {
    float: left;
    width: 100px;
    height: 100px;
    overflow: hidden;
    position: relative
}

.favoriGrupUrunItem .favoriGrupUrunItemImg .favoriGrupUrunItemBirim {
    position: absolute;
    background-color: #000;
    width: 18px;
    height: 18px;
    color: #fff;
    border-radius: 16px;
    right: 5px;
    text-align: center;
    top: 5px;
    font-size: 11px;
    line-height: 18px
}

.favoriGrupUrunItemImg img {
    max-width: 100%
}

.favoriGrupUrunItem .favoriGrupUrunItemName {
    float: left;
    width: 40%
}

.favoriGrupUrunItem .favoriGrupUrunItemName .favoriGrupUrunItemNameAdetBirim {
    display: block;
    font-size: 13px;
    color: #b2b2b2
}

.favoriGrupUrunItem .favoriGrupUrunItemPrice {
    float: left;
    width: 30%
}

.favoriGrupUrunItem .favoriGrupUrunBtnGrup {
    float: right;
    width: 10%;
    display: block;
    text-align: right
}

.favoriGrupUrunItem .favoriGrupUrunBtnGrup>div {
    display: inline-block;
    margin-left: 15px
}

.divFavoriGrupDetayBottom {
    display: block;
    margin-top: 10px;
    text-align: right
}

.divFavoriGrupDetayBottom div {
    display: inline-block
}

.divFavoriGrupDetayBottom div a {
    display: block;
    border: 1px solid #ddd;
    background-color: #ddd;
    color: #4c4c4c;
    padding: 2px 15px
}

.divFavoriGrupDetayBottom div a:hover {
    background-color: #4c4c4c;
    color: #fff
}

.standartFavoriBlok {
    float: left;
    display: block;
    width: 100%;
    margin-bottom: 10px
}

.standartFavoriBlok:after {
    clear: both;
    display: table;
    content: ""
}

.standartFavoriBlok .standartFavoriBlokTittle {
    border: 1px solid #ddd;
    display: block;
    padding: 8px;
    background-color: #fff;
    margin-bottom: 5px;
    position: relative;
    cursor: pointer
}

.standartFavoriBlok .standartFavoriBlokTittle:after {
    clear: both;
    display: table;
    content: ""
}

.standartFavoriBlok .standartFavoriBlokTittle div>span {
    float: left;
    line-height: 27px
}

.standartFavoriBlok .standartFavoriBlokTittle a {
    display: block;
    float: right;
    padding: 5px 15px;
    background-color: #ddd;
    line-height: normal;
    border: 1px solid #ddd;
    background-color: #ddd;
    color: #4c4c4c;
    font-size: 13px
}

.standartFavoriBlok .standartFavoriBlokTittle a:hover {
    border: 1px solid #4c4c4c;
    background-color: #4c4c4c;
    color: #fff
}

.standartFavoriBlok .standartFavoriBlokContent .favoriGrupUrunItemContent {
    padding: 10px;
    border: 1px solid #ddd;
    margin-bottom: 5px;
    background-color: #fff
}

.standartFavoriBlok .standartFavoriBlokContent .favoriGrupUrunItemContent .favoriGrupUrunItem {
    border-bottom: 0
}

.standartFavoriBlok .standartFavoriBlokContent .favoriGrupUrunItemContent:after {
    clear: both;
    display: table;
    content: ""
}

.detayFavoriListesiContent {
    width: 100%
}

#divGrupOlusturContent .item {
    display: block;
    width: 100%
}

.detayFavoriListItem {
    display: block;
    width: 100%;
    padding: 8px 0 8px 5px;
    position: relative;
    border: 1px solid #ccc;
    margin-bottom: 5px
}

.detayFavoriListItem button {
    display: block;
    padding: 5px 15px;
    background-color: #ddd;
    line-height: normal;
    border: 1px solid #ddd;
    background-color: #ddd;
    color: #4c4c4c;
    position: absolute;
    right: 6px;
    top: 3px;
    font-size: 13px;
    cursor: pointer
}

.detayFavoriListItem button:hover {
    border: 1px solid #4c4c4c;
    background-color: #4c4c4c;
    color: #fff
}

.divGrupOlusturContentBottom input {
    display: block;
    width: 100%;
    padding: 8px 0
}

.detayFavoriListesiContent #btnGrupOlusturGoster {
    display: block;
    padding: 5px 15px;
    background-color: #ddd;
    line-height: normal;
    border: 1px solid #ddd;
    margin-top: 5px;
    background-color: #ddd;
    color: #4c4c4c;
    font-size: 13px;
    cursor: pointer;
    width: 100%
}

.divGrupOlusturContentBottom button {
    display: block;
    padding: 5px 15px;
    background-color: #ddd;
    line-height: normal;
    border: 1px solid #ddd;
    margin-top: 5px;
    background-color: #ddd;
    color: #4c4c4c;
    font-size: 13px;
    cursor: pointer;
    width: 100%
}

.divGrupOlusturContentBottomError {
    padding: 5px 0;
    color: #f00
}

@media(max-width: 768px) {
    .favori-modal-content {
        width:100%
    }
}

.magazaTeslimatBilgisiContent {
    margin: 15px 0
}

.magazaTeslimatKargoBilgisi {
    width: 50%;
    float: left;
    background-color: #fff;
    border: 1px solid #ebebeb;
    padding: 10PX;
    min-height: 93px
}

.magazaTeslimatKargoBilgisi .magazaTeslimatKargo strong {
    font-size: 13px;
    color: #3e3e3e
}

.magazaTeslimatKargoBilgisi .magazaTeslimatAdresBilgisi {
    font-size: 13px;
    color: #3e3e3e;
    display: block
}

.magazaTeslimatKargoBilgisi .magazaTeslimatAdresBilgisi span {
    margin-left: 5px
}

.magazaTeslimatKargoBilgisi .magazaTeslimatAdresBilgisi span a {
    font-size: 13px;
    color: #4f8ee3;
    font-weight: 500
}

.magazaTeslimatKargoBilgisi .magazaTeslimatAdresBilgisi span a i {
    margin-right: 0
}

.magazaTeslimatKargoBilgisi .magazaTeslimatSaatBilgisi {
    font-size: 13px
}

.magazaTeslimatKargoBilgisi .magazaTeslimatSaatBilgisi a {
    font-size: 13px;
    color: #4f8ee3;
    font-weight: 500;
    margin-left: 5px
}

.magazaTeslimatKargoBilgisi .magazaTeslimatSaatBilgisi a i {
    margin-right: 0
}

.magazaTeslimatMagazaBilgisi {
    float: left;
    width: 50%;
    background-color: #fff;
    border: 1px solid #ebebeb;
    padding: 10PX;
    border-left: 0;
    min-height: 93px
}

.magazaTeslimatMagazaBilgisi .magazaTeslimatMagaza strong {
    font-size: 13px;
    color: #3e3e3e
}

.magazaTeslimatMagazaBilgisi .magazaTeslimatMagaza span {
    font-size: 11px;
    color: #fff;
    background-color: #ffb007;
    display: inline-block;
    padding: 2px;
    border-radius: 2px;
    line-height: normal;
    margin-top: -5px
}

.magazaTeslimatMagazaBilgisi .magazaTeslimatMagazaAdresBilgisi {
    font-size: 13px;
    color: #3e3e3e;
    line-height: normal
}

.magazaTeslimatMagazaBilgisi .magazaTeslimatMagazaAdresBilgisi a {
    font-size: 13px;
    color: #4f8ee3;
    font-weight: 500;
    margin-left: 5px
}

.magazaTeslimatMagazaBilgisi .magazaTeslimatMagazaAdresBilgisi a i {
    margin-right: 0
}

.sutunsContent {
    width: 700px;
    background-color: #fff;
    padding: 10px;
    display: -webkit-box;
    display: -moz-box;
    display: -ms-flexbox;
    display: -webkit-flex;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    -webkit-flex-direction: row;
    -ms-flex-direction: row;
    -moz-flex-direction: row;
    -o-flex-direction: row;
    -webkit-justify-content: space-between;
    -ms-justify-content: space-between
}

.sutunsContent .sutun {
    float: left
}

.sutunsContent .baslik {
    text-align: center;
    border: 1px solid #ebebeb;
    font-size: 13px;
    font-weight: 600
}

.sutunsContent .sutun .satir {
    display: -webkit-box;
    display: -moz-box;
    display: -ms-flexbox;
    display: -webkit-flex;
    display: flex;
    align-items: center;
    -webkit-align-items: center;
    justify-content: center;
    -webkit-justify-content: center;
    height: 50px;
    border: 1px solid #ebebeb;
    color: #3e3e3e;
    font-size: 13px
}

.global_body .teslimatSaatiContent {
    width: 600px;
    padding: 10px
}

.global_body .teslimatSaatiContentBaslik p:first-child {
    font-size: 17px;
    font-weight: 600
}

.global_body .teslimatSaatiContentBaslik p:last-child {
    font-size: 13px;
    font-weight: 400;
    padding: 10px 0
}

.global_body .teslimatSaatiContent .teslimatSaatiRow {
    flex-wrap: wrap;
    display: flex
}

.global_body .teslimatSaatiContent .teslimatSaatiRow .teslimatSaatiCol {
    width: 14.285714%;
    cursor: pointer;
    text-align: center;
    border: 2px solid #ebebeb;
    border-right: 0;
    font-size: 12px;
    color: #3e3e3e
}

.global_body .teslimatSaatiContent .teslimatSaatiRow .teslimatSaatiCol.active {
    border: 2px solid #3e3e3e
}

.global_body .teslimatSaatiContent .teslimatSaatiCol span {
    display: block;
    padding: 3px 0
}

.global_body .teslimatSaatiContent .teslimatSaatiTabContent .satirTab.hidden {
    display: none
}

.global_body .teslimatSaatiContent .teslimatSaatiTabContent .satirTab .satir {
    font-size: 12px;
    margin-top: 10px;
    border: 2px solid #ebebeb;
    border-left: 0;
    border-right: 0;
    border-top: 0;
    margin: 0;
    margin-right: -1px;
    margin-bottom: -1px;
    height: 50px;
    display: block;
    font-size: 12px;
    color: #3e3e3e;
    font-weight: 600;
    cursor: pointer;
    display: -webkit-box;
    display: -moz-box;
    display: -ms-flexbox;
    display: -webkit-flex;
    display: flex;
    align-items: center;
    -webkit-align-items: center;
    justify-content: center;
    -webkit-justify-content: center
}

.global_body .teslimatSaatiContent .teslimatSaatiTabContent .satirTab .satir span {
    width: 49%;
    display: inline-block;
    color: #3e3e3e
}

.global_body .teslimatSaatiContent .teslimatSaatiTabContent .satirTab .satir span:last-child {
    text-align: right
}

.global_body .teslimatSaatiContent .teslimatSaatiTabContent .satirTab .satir span.pasif {
    color: #ccc
}

.fb_dialog_mobile {
    bottom: 10px !important;
    right: 0 !important
}

#topMessage {
    position: fixed;
    margin: 0;
    background: #e6e6e6;
    text-align: center;
    left: 0;
    right: 0;
    z-index: 999;
    top: 0
}

#topMessage #topMessageContainer {
    display: block;
    max-width: 768px;
    margin: 0 auto
}

#topMessage #browserUpdate,#topMessage #browserUpdateIE9 {
    overflow: hidden;
    padding: 15px
}

.browser-update-close {
    float: right;
    display: block;
    color: #000;
    position: absolute;
    right: 10px;
    top: 10px;
    font-size: 13px;
    cursor: pointer
}

.browser-update-close:hover {
    color: #f00
}

#browserUpdate strong,#browserUpdateIE9 strong {
    color: #333;
    font-size: 18px;
    display: block;
    margin-bottom: 10px
}

#browserUpdate ul,#browserUpdateIE9 ul {
    list-style: none;
    padding: 0;
    margin: 15px 0 0 0;
    overflow: hidden;
    font-size: 0
}

#browserUpdate ul li,#browserUpdateIE9 ul li {
    zoom:1;margin-left: 10px;
    min-width: 25%;
    display: inline-block;
    vertical-align: text-bottom
}

#browserUpdate ul li:first-child,#browserUpdateIE9 ul li:first-child {
    margin-left: 0
}

#browserUpdate ul li a,#browserUpdateIE9 ul li a {
    display: block;
    color: #333;
    font-size: 14px;
    line-height: 45px;
    background: #fff;
    transition: all .3s ease;
    -webkit-transition: all .3s ease;
    -moz-transition: all .3s ease;
    -o-transition: all .3s ease
}

#browserUpdate ul li a span,#browserUpdateIE9 ul li a span {
    display: inline-block;
    cursor: pointer
}

#browserUpdate ul li a i,#browserUpdateIE9 ul li a i {
    line-height: 45px;
    margin-right: 11px;
    font-size: 27px;
    vertical-align: top;
    color: #666
}

#browserUpdate ul li a:hover,#browserUpdateIE9 ul li a:hover {
    background: #eee
}

.displayNone {
    display: none
}

.cerezPopupUyari {
    display: none;
    background-color: rgba(32,32,32,.95);
    max-width: 430px;
    box-sizing: border-box;
    -webkit-box-sizing: border-box;
    -moz-box-sizing: border-box;
    padding: 10px;
    color: #c9c9c9;
    font-size: 12px;
    line-height: 17px;
    position: fixed;
    left: 5px;
    right: auto;
    bottom: 45px;
    z-index: 6;
    border-radius: 0
}

.cerezPopupUyari .closeBtn {
    cursor: pointer;
    display: block;
    position: absolute;
    right: 8px;
    top: 5px;
    z-index: 1;
    font-size: 18px
}

.cerezPopupUyari .closeBtn i {
    font-size: 16px
}

.cerezPopupUyari .title {
    font-size: 17px;
    line-height: 1;
    font-weight: 400;
    margin-bottom: 5px;
    color: #fff
}

@media(max-width: 540px) {
    .cerezPopupUyari {
        width:75%;
        bottom: 45px
    }
}

.zorunluSecimBorder {
    border: 3px solid #f00;
    padding: 3px;
    border-radius: 5px
}

.urunListeAdet>label.error {
    display: none !important
}

.aIsDisabled {
    cursor: not-allowed;
    opacity: .5;
    color: currentColor;
    display: inline-block;
    pointer-events: none;
    text-decoration: none
}

.aIsDisabled .fa-spin {
    display: inherit !important
}

.searchContent .ui-menu {
    min-width: 360px;
    padding: 5px;
    max-height: 300px;
    overflow-y: auto;
    background-color: #fff
}

.searchContent .ui-menu:after {
    clear: both;
    display: table;
    content: ""
}

.searchContent .ui-menu .ui-menu-item:after {
    clear: both;
    display: table;
    content: ""
}

.searchContent .ui-menu .ui-menu-item a {
    display: block;
    text-align: left;
    padding: 5px 0;
    float: left;
    width: 100%
}

.searchContent .ui-menu .ui-menu-item .complate_image {
    width: 50px !important;
    height: 50px;
    overflow: hidden;
    float: left;
    margin-right: 5px
}

.searchContent .ui-menu .ui-menu-item .complate_image img {
    width: 50px !important;
    height: 50px !important
}

.searchContent .ui-menu .ui-menu-item .complate_text {
    min-width: 200px;
    padding-left: 0;
    float: left;
    max-width: 210px;
    line-height: 16px;
    font-size: 12px
}

.searchContent .ui-menu .ui-menu-item .complate_productPrice {
    width: 59px;
    font-size: 11px;
    padding-left: 5px;
    float: right;
    text-align: right;
    font-weight: 600;
    font-size: 12px
}

.kombinContent ul:after {
    clear: both;
    display: table;
    content: ""
}

.kombinContent ul li.kombinToplamTutar {
    display: flex;
    margin-bottom: 15px
}

.kombinContent ul li.kombinToplamTutar div {
    border: 1px solid #efefef;
    padding: 10px;
    background-color: #fdfdfd
}

.kombinContent ul li.kombinToplamTutar div.kombinTopluSatinAlimFiyatcizgili span:last-child {
    text-decoration: line-through;
    color: #afafaf
}

.kombinContent ul li.kombinToplamTutar div:last-child {
    margin-left: auto
}

.kombinContent ul li.kombinToplamTutar div:first-child {
    margin-right: 15px
}

.kombinContent ul li.kombinToplamTutar div span {
    flex-direction: column;
    display: flex;
    align-items: center;
    justify-content: center;
    line-height: 1.5;
    font-size: 18px
}

.kombinContent ul li.kombinToplamTutar div span.title {
    font-size: 13px
}

.kombinItem {
    background-color: #fff;
    border: 1px solid #efefef;
    margin: 0 0 15px 0;
    padding: 10px;
    overflow: hidden;
    display: flex;
    display: -webkit-flex
}

.kombinItem .kombinleftImage {
    width: 96px;
    float: left;
    overflow: hidden
}

.kombinItem .kombinImages img {
    max-width: 96px;
    border: 1px solid #e8e8e8
}

.kombinItem .kombinImages .selectedImagesLink {
    font-size: 12px;
    color: #000;
    text-decoration: underline;
    line-height: 1.5
}

.kombinItem .kombinRightDetail {
    padding-left: 10px;
    float: right;
    width: 400px
}

.kombinFormline .kombinright_line {
    font-size: 14px;
    line-height: 1.5;
    color: #000
}

#divFiyatAlanlari .kombinFormline {
    font-size: 13px;
    line-height: 1.5
}

#divFiyatAlanlari .kombinFiyat1 {
    font-size: 14px;
    font-weight: 500;
    text-decoration: line-through;
    color: #afafaf
}

#divFiyatAlanlari .kombinFiyat2 {
    font-size: 18px;
    font-weight: 500;
    color: #000
}

#divFiyatAlanlari .kombinFiyat3 {
    font-size: 24px;
    font-weight: 500
}

#divFiyatAlanlari .kombinFiyat1 span {
    font-size: 12px;
    color: #000
}

#divFiyatAlanlari .kombinFiyat2 span {
    font-size: 12px;
    color: #000
}

#divFiyatAlanlari .kombinFiyat3 span {
    font-size: 12px;
    color: #000
}

.kombinleft_line {
    padding: 0 0 5px 0
}

.kombinright_line select {
    padding: 4px 8px;
    border: 1px solid #e8e8e8
}

.kombinright_line a {
    border: solid 1px #d1d1d1;
    background-color: #fff;
    line-height: 32px;
    float: left;
    display: block;
    margin-right: 3px;
    cursor: pointer;
    min-height: 32px;
    min-width: 32px;
    text-align: center
}

.kombinFormline .size_box.selected {
    border: solid 1px #000;
    background-color: #fff;
    color: #000
}

.kombinFormline .size_box.nostok {
    border: solid 1px #ececec !important;
    background-color: #ececec !important;
    color: #9a9a9a !important;
    position: relative
}

.kombinFormline .size_box.nostok img {
    opacity: .4
}

.kombinEksecenekUyari {
    background-color: #fff;
    position: relative;
    z-index: 1000000;
    padding: 5px;
    border-radius: 5px
}

.urunsecoverlay {
    position: fixed;
    background-color: #000;
    opacity: .5;
    z-index: 99999;
    top: 0;
    left: 0;
    width: 100%;
    height: 150%
}

.kombinurunsecbody #divKombinUrunEkSecenek .tooltipp {
    position: absolute;
    top: -50px;
    left: 50%;
    margin-left: -130px;
    background-color: #000;
    width: 260px;
    height: 40px;
    line-height: 40px;
    text-align: center;
    color: #fff;
    border-radius: 5px
}

.KombinTopluSatinAlimBtn {
    display: flex
}

.KombinTopluSatinAlimBtn a {
    padding: 10px 30px;
    font-size: 16px;
    font-weight: bold
}

.TopluSatinAlimBtn {
    float: left;
    width: 45%
}

.TopluSatinAlimFiyat {
    float: left;
    width: 45%;
    padding: 12px 0
}

.TopluSatinAlimFiyat span {
    font-weight: 600;
    display: inline-block;
    font-size: 15px;
    margin-right: 5px
}

.hrzRow {
    margin-left: -10px;
    margin-right: -10px;
    clear: both;
    display: block
}

.hrzRow:before,.hrzRow:after {
    content: '';
    display: table;
    clear: both
}

.hrzCol {
    float: left;
    padding-left: 10px;
    padding-right: 10px;
    box-sizing: border-box;
    position: relative;
    min-height: 1px
}

.hrzCol-3 {
    width: 25%
}

.hrzCol-4 {
    width: 33.33333333%
}

.hrzCol-5 {
    width: 41.66666667%
}

.hrzCol-6 {
    width: 50%
}

.hrzCol-7 {
    width: 58.33333333%
}

.hrzCol-9 {
    width: 75%
}

.hrzCol-12 {
    width: 100%
}

.ItemOrjHrz {
    margin-bottom: 20px
}

.ProductItemHrz {
    border: 1px solid #e1e1e1;
    background-color: #fff;
    padding: 10px 0
}

.ProductItemHrz::after {
    clear: both;
    display: table;
    content: ""
}

.ProductItemHrz .hrzLeft a.hrzLeftLink {
    display: block;
    position: relative;
    width: 100%;
    height: 0;
    overflow: hidden;
    padding-bottom: 150%
}

.ProductItemHrz .hrzLeft a .hrzDiscountIco {
    position: absolute;
    right: 5px;
    top: 5px;
    color: #000;
    z-index: 9;
    font-weight: bold
}

.ProductItemHrz .hrzLeft a .hrzImage {
    background-color: #fff;
    position: absolute;
    width: 100%;
    height: 100%;
    top: 0;
    left: 0;
    text-align: center;
    align-items: center
}

.ProductItemHrz .hrzLeft a .hrzImage img {
    margin: 0 auto;
    -webkit-transition-timing-function: ease-in-out;
    -moz-transition-timing-function: ease-in-out;
    -ms-transition-timing-function: ease-in-out;
    -o-transition-timing-function: ease-in-out;
    transition-timing-function: ease-in-out;
    -webkit-transition-duration: .2s;
    -moz-transition-duration: .2s;
    -ms-transition-duration: .2s;
    -o-transition-duration: .2s;
    transition-duration: .2s
}

.ProductItemHrz .hrzLeft .hrzProductStar {
    padding-top: 20px
}

.ProductItemHrz .hrzRight .hrzProductDetail {
    margin-bottom: 10px
}

.hrzName {
    font-size: 19px;
    font-weight: 600;
    display: block;
    margin-bottom: 10px
}

.hrzOnyazi {
    font-size: 13px;
    font-weight: 400;
    display: block;
    margin-bottom: 5px
}

.hrzDahaFazla {
    font-weight: 600;
    font-size: 12px
}

.hrzSecenekTittle {
    border-top: 1px solid #ddd;
    border-bottom: 1px solid #ddd
}

.hrzSecenekTittle>div {
    padding: 10px 0
}

.hrzSecenekTittle>div div {
    font-weight: 500;
    color: #000;
    font-size: 14px
}

.hrzSecenekItem {
    border-bottom: 1px solid #ddd;
    padding-top: 10px;
    padding-bottom: 10px
}

.hrzSecenekList,.hrzSecenekPrice {
    line-height: 30px
}

.hrzSecenekItem .urunListeAdet {
    border: 1px solid #ddd;
    padding: 0;
    margin: 0;
    display: flex;
    height: 33px;
    margin-left: 0
}

.hrzSecenekItem .urunListeAdet a {
    display: block;
    width: 100%;
    text-align: center;
    height: 31px;
    line-height: 31px;
    border: 0;
    background-color: #ddd;
    box-sizing: border-box;
    -webkit-user-select: none;
    -moz-user-select: none;
    -ms-user-select: none;
    -o-user-select: none;
    user-select: none
}

.hrzSecenekItem .urunListeAdet a:hover {
    background-color: #000;
    color: #fff
}

.hrzSecenekItem .urunListeAdet input {
    height: 30px;
    text-align: center;
    border: 0;
    width: 100%;
    box-sizing: border-box;
    font-size: 12px;
    text-transform: uppercase;
    box-shadow: none;
    padding: 0;
    line-height: normal;
    margin: 0
}

.hrzTukendi {
    line-height: normal;
    display: block;
    font-weight: 600;
    background-color: #f7f7f7;
    padding: 10px 40px;
    letter-spacing: 1px
}

.hrzSepeteEkle a {
    line-height: 30px;
    width: 100%;
    text-align: center;
    display: block;
    background-color: #ddd;
    border: 1px solid #ddd;
    font-size: 13px;
    border-radius: 2px
}

.hrzSepeteEkle a i {
    margin-right: 10px
}

.hrzSepeteEkle a:hover {
    background-color: #000;
    border: 1px solid #000;
    color: #fff
}

.hrzSatir2 {
    color: #666;
    font-size: 12px;
    text-decoration: line-through
}

.hrzSatir1 {
    font-weight: bold;
    color: #000;
    font-size: 14px
}

.hrzProductbottom {
    padding-top: 10px
}

.hrzProductbottom:after,.hrzProductSecenek:after {
    clear: both;
    display: table;
    content: ""
}

.hrzProductIcons>div {
    display: inline-block;
    padding: 0 10px;
    line-height: 32px;
    margin-right: 5px;
    background-color: #ddd
}

.hrzProductIcons>div.hrzIcons {
    padding: 5px;
    background-color: #666;
    color: #fff;
    line-height: normal;
    margin-right: 0;
    margin-bottom: 5px;
    display: table;
    font-size: 12px;
    float: none;
    clear: left;
    font-weight: 500;
    border-radius: 8px 0 8px 0
}

.dinamikFormContainer label.imageboxRadio>input,label.imageboxRadio>span.radioButtonText {
    visibility: hidden;
    position: absolute
}

.dinamikFormContainer label.imageboxRadio>img {
    cursor: pointer;
    border: 2px solid transparent
}

.dinamikFormContainer label.radioChecked>img {
    border: 2px solid #f00 !important
}

.favoriButtonKapali {
    display: none !important
}

.displayNone {
    display: none
}

.flex-viewport {
    display: block !important
}

#divInstashopPopup {
    min-width: 900px;
    background-color: #fff
}

#divInstashopPopup .AddGalleryModal .AddGalleryModalTittle {
    display: block;
    padding: 30px;
    color: #222;
    font-size: 20px;
    -webkit-box-shadow: 0 15px 15px 0 rgba(0,0,0,.15);
    -moz-box-shadow: 0 15px 15px 0 rgba(0,0,0,.15);
    box-shadow: 0 15px 15px 0 rgba(0,0,0,.15)
}

#divInstashopPopup .AddGalleryModal .instaPopupBox {
    background-color: #fff;
    margin-top: 23px
}

#divInstashopPopup .AddGalleryModal .instaPopupBox:after {
    clear: both;
    display: table;
    content: ""
}

#divInstashopPopup .AddGalleryModal .instaPopupBox .popupLeft {
    float: left;
    width: 450px
}

#divInstashopPopup .AddGalleryModal .instaPopupBox .popupLeft img {
    max-width: 100%
}

#divInstashopPopup .AddGalleryModal .popupRight {
    float: right;
    width: 395px
}

#divInstashopPopup .AddGalleryModal .popupList {
    margin-top: 30px
}

#divInstashopPopup .AddGalleryModal .popopItem:after {
    clear: both;
    display: table;
    content: ""
}

#divInstashopPopup .AddGalleryModal .popopItem .popup-left {
    float: left;
    max-width: 100px;
    height: 133px;
    background-size: contain;
    background-repeat: no-repeat;
    background-position: top center;
    width: 33.33333333%
}

#divInstashopPopup .AddGalleryModal .popopItem .popup-left img {
    display: block
}

#divInstashopPopup .AddGalleryModal .popopItem .popup-right {
    float: left;
    width: 63.66666667%;
    margin-left: 3%
}

#divInstashopPopup .AddGalleryModal .popup-right-link {
    font-weight: 500;
    font-size: 15px;
    padding: 0 0 5px 0;
    cursor: pointer;
    display: block
}

#divInstashopPopup .AddGalleryModal .popup-right-btn {
    background-color: #fff;
    border: 1px solid #222;
    color: #222;
    padding: 6px 30px;
    margin-top: 15px;
    font-size: 14px;
    border-radius: 2px;
    display: inline-block;
    line-height: 1.42857143;
    text-align: center;
    white-space: nowrap;
    vertical-align: middle;
    cursor: pointer
}

#divInstashopPopup .AddGalleryModal .popup-right-btn:hover {
    background-color: #222;
    border: 1px solid #222;
    color: #fff
}

#divInstashopPopup .AddGalleryModal .AddGalleryModalFooter {
    display: block;
    padding: 30px;
    color: #222;
    font-size: 20px;
    -webkit-box-shadow: 0 -15px 15px 0 rgba(0,0,0,.15);
    -moz-box-shadow: 0 -15px 15px 0 rgba(0,0,0,.15);
    box-shadow: 0 -15px 15px 0 rgba(0,0,0,.15);
    text-align: right
}

#divInstashopPopup .AddGalleryModal .AddGalleryModalFooter:after {
    clear: both;
    display: table;
    content: ""
}

#divInstashopPopup .AddGalleryModal .instafooter-right {
    float: right
}

#divInstashopPopup .AddGalleryModal .AddGalleryModalFooter ul {
    float: left
}

#divInstashopPopup .AddGalleryModal .AddGalleryModalFooter ul li {
    float: left;
    margin-right: 30px
}

#divInstashopPopup .AddGalleryModal .AddGalleryModalFooter ul li a i {
    font-size: 18px;
    color: #222
}

#divInstashopPopup .AddGalleryModal .AddGalleryModalFooter p {
    float: left;
    font-size: 14px;
    font-weight: 600;
    margin-right: 30px
}

@media screen and (min-width: 1199px) {
    #divInstashopPopup .AddGalleryModal .popupList {
        margin-top:30px;
        max-height: 400px;
        overflow-y: auto;
        margin-right: 15px;
        margin-bottom: 30px
    }
}

@media screen and (max-width: 991px) {
    #divInstashopPopup .AddGalleryModal {
        width:100%;
        min-width: 100%
    }

    #divInstashopPopup .AddGalleryModal .popupRight {
        width: 340px
    }
}

@media screen and (max-width: 768px) {
    #divInstashopPopup .AddGalleryModal {
        width:100%
    }

    #divInstashopPopup .AddGalleryModal .popupRight {
        width: 100%
    }
}

@media screen and (max-width: 480px) {
    #divInstashopPopup .AddGalleryModal .AddGalleryModalTittle,#divInstashopPopup .AddGalleryModal .AddGalleryModalFooter {
        padding:10px;
        box-shadow: none
    }

    #divInstashopPopup .AddGalleryModal .instaPopupBox {
        margin-top: 0
    }

    #divInstashopPopup .AddGalleryModal .instaPopupBox .popupLeft {
        width: 100%
    }
}

#divGaleriPopup {
    min-width: 900px;
    background-color: #fff
}

#divGaleriPopup .AddGalleryModal .AddGalleryModalTittle {
    display: block;
    padding: 30px;
    color: #222;
    font-size: 20px;
    -webkit-box-shadow: 0 15px 15px 0 rgba(0,0,0,.15);
    -moz-box-shadow: 0 15px 15px 0 rgba(0,0,0,.15);
    box-shadow: 0 15px 15px 0 rgba(0,0,0,.15)
}

#divGaleriPopup .AddGalleryModal .instaPopupBox {
    background-color: #fff;
    margin-top: 23px
}

#divGaleriPopup .AddGalleryModal .instaPopupBox:after {
    clear: both;
    display: table;
    content: ""
}

#divGaleriPopup .AddGalleryModal .instaPopupBox .popupLeft {
    float: left;
    width: 450px
}

#divGaleriPopup .AddGalleryModal .instaPopupBox .popupLeft img {
    max-width: 100%
}

#divGaleriPopup .AddGalleryModal .popupRight {
    float: right;
    width: 395px
}

#divGaleriPopup .AddGalleryModal .popupList {
    margin-top: 30px
}

#divGaleriPopup .AddGalleryModal .popopItem:after {
    clear: both;
    display: table;
    content: ""
}

#divGaleriPopup .AddGalleryModal .popopItem .popup-left {
    float: left;
    max-width: 100px;
    height: 133px;
    background-size: contain;
    background-repeat: no-repeat;
    background-position: top center;
    width: 33.33333333%
}

#divGaleriPopup .AddGalleryModal .popopItem .popup-left img {
    display: block
}

#divGaleriPopup .AddGalleryModal .popopItem .popup-right {
    float: left;
    width: 63.66666667%;
    margin-left: 3%
}

#divGaleriPopup .AddGalleryModal .popup-right-link {
    font-weight: 500;
    font-size: 15px;
    padding: 0 0 5px 0;
    cursor: pointer;
    display: block
}

#divGaleriPopup .AddGalleryModal .popup-right-btn {
    background-color: #fff;
    border: 1px solid #222;
    color: #222;
    padding: 6px 30px;
    margin-top: 15px;
    font-size: 14px;
    border-radius: 2px;
    display: inline-block;
    line-height: 1.42857143;
    text-align: center;
    white-space: nowrap;
    vertical-align: middle;
    cursor: pointer
}

#divGaleriPopup .AddGalleryModal .popup-right-btn:hover {
    background-color: #222;
    border: 1px solid #222;
    color: #fff
}

#divGaleriPopup .AddGalleryModal .AddGalleryModalFooter {
    display: block;
    padding: 30px;
    color: #222;
    font-size: 20px;
    -webkit-box-shadow: 0 -15px 15px 0 rgba(0,0,0,.15);
    -moz-box-shadow: 0 -15px 15px 0 rgba(0,0,0,.15);
    box-shadow: 0 -15px 15px 0 rgba(0,0,0,.15);
    text-align: right
}

#divGaleriPopup .AddGalleryModal .AddGalleryModalFooter:after {
    clear: both;
    display: table;
    content: ""
}

#divGaleriPopup .AddGalleryModal .instafooter-right {
    float: right
}

#divGaleriPopup .AddGalleryModal .AddGalleryModalFooter ul {
    float: left
}

#divGaleriPopup .AddGalleryModal .AddGalleryModalFooter ul li {
    float: left;
    margin-right: 30px
}

#divGaleriPopup .AddGalleryModal .AddGalleryModalFooter ul li a i {
    font-size: 18px;
    color: #222
}

#divGaleriPopup .AddGalleryModal .AddGalleryModalFooter p {
    float: left;
    font-size: 14px;
    font-weight: 600;
    margin-right: 30px
}

@media screen and (min-width: 1199px) {
    #divGaleriPopup .AddGalleryModal .popupList {
        margin-top:30px;
        max-height: 400px;
        overflow-y: auto;
        margin-right: 15px;
        margin-bottom: 30px
    }
}

@media screen and (max-width: 991px) {
    #divGaleriPopup .AddGalleryModal {
        width:100%;
        min-width: 100%
    }

    #divGaleriPopup .AddGalleryModal .popupRight {
        width: 340px
    }
}

@media screen and (max-width: 768px) {
    #divGaleriPopup .AddGalleryModal {
        width:100%
    }

    #divGaleriPopup .AddGalleryModal .popupRight {
        width: 100%
    }
}

@media screen and (max-width: 480px) {
    #divGaleriPopup .AddGalleryModal .AddGalleryModalTittle,#divGaleriPopup .AddGalleryModal .AddGalleryModalFooter {
        padding:10px;
        box-shadow: none
    }

    #divGaleriPopup .AddGalleryModal .instaPopupBox {
        margin-top: 0
    }

    #divGaleriPopup .AddGalleryModal .instaPopupBox .popupLeft {
        width: 100%
    }
}

.galeri-modal {
    display: none;
    position: fixed;
    z-index: 99999999999;
    padding-top: 100px;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    overflow: auto;
    background-color: #000;
    background-color: rgba(0,0,0,.4)
}

.galeri-modal-content {
    background-color: #fefefe;
    margin: auto;
    padding: 20px;
    border: 1px solid #888
}

#smartbanner {
    position: absolute;
    left: 0;
    top: -82px;
    border-bottom: 1px solid #e8e8e8;
    width: 100%;
    height: 78px;
    font-family: 'Helvetica Neue',sans-serif;
    background: #fff;
    box-shadow: 0 1px 2px rgba(0,0,0,.5);
    z-index: 9998;
    -webkit-font-smoothing: antialiased;
    overflow: hidden;
    -webkit-text-size-adjust: none
}

#smartbanner .sb-container {
    margin: 0 auto
}

#smartbanner .sb-close {
    position: absolute;
    left: 5px;
    top: 8px;
    display: block;
    width: 14px;
    height: 14px;
    font-family: 'ArialRoundedMTBold',Arial;
    line-height: 15px;
    text-align: center;
    text-decoration: none;
    text-shadow: none;
    border-radius: 14px;
    border: 0;
    color: #8b8b8b;
    font-size: 20px
}

#smartbanner .sb-close:active {
    font-size: 13px;
    color: #aaa
}

#smartbanner .sb-icon {
    position: absolute;
    left: 30px;
    top: 10px;
    display: block;
    width: 57px;
    height: 57px;
    background: rgba(0,0,0,.6);
    background-size: cover;
    border-radius: 10px;
    box-shadow: 0 1px 3px rgba(0,0,0,.3)
}

#smartbanner.no-icon .sb-icon {
    display: none
}

#smartbanner .sb-info {
    position: absolute;
    left: 98px;
    top: 18px;
    width: 44%;
    font-size: 11px;
    line-height: 1.2em;
    font-weight: bold;
    color: #6a6a6a;
    text-shadow: 0 1px 0 rgba(255,255,255,.8)
}

#smartbanner #smartbanner.no-icon .sb-info {
    left: 34px
}

#smartbanner .sb-info strong {
    display: block;
    font-size: 13px;
    color: #4d4d4d;
    line-height: 18px
}

#smartbanner .sb-info>span {
    display: block
}

#smartbanner .sb-info em {
    font-style: normal;
    text-transform: uppercase
}

#smartbanner .sb-button {
    float: right;
    display: block;
    background-color: #f27a1a;
    color: #fff;
    padding: 2px 10px 2px;
    border-radius: 3px;
    
    min-width: 12%;
    position: absolute;
    right: 28px;
    top: 24px;
    font-size: 13px
}

#smartbanner .sb-button:active,#smartbanner .sb-button:hover {
    background: -webkit-linear-gradient(top,#dcdcdc 0%,#efefef 100%)
}

#smartbanner .sb-icon.gloss:after {
    content: '';
    position: absolute;
    left: 0;
    top: -1px;
    border-top: 1px solid rgba(255,255,255,.8);
    width: 100%;
    height: 50%;
    background: -webkit-linear-gradient(top,rgba(255,255,255,.7) 0%,rgba(255,255,255,.2) 100%);
    border-radius: 10px 10px 12px 12px
}

#smartbanner.android .sb-close:active {
    color: #666
}

#smartbanner.android .sb-info strong {
    color: #666
}

#smartbanner.android .sb-button:active,#smartbanner.android .sb-button:hover {
    background: none
}

.btnUrundetayKombin {
    display: inline-block;
   
    margin-right: 10px;
    background-color: #f00;
    border: 0
}

.ulRootAltListe {
    display: none
}

.tamamlayiciUrunContent {
    background-color: #fff;
    width: 800px
}

.tamamlayiciUrunWrapper {
    clear: both;
    width: 100%;
    display: block;
    overflow: hidden
}

.tamamlayiciUrunWrapper .tamamlayiciUrurnItem img {
    width: 100%;
    object-fit: contain
}

.tamamlayiciUrunWrapper .tamamlayiciUrurnItem span.productTitle {
    display: block;
    text-transform: capitalize;
    font-weight: 600
}

.tamamlayiciUrunContainer {
    padding: 0
}

.tamamlayiciUrunContainer p {
    text-align: center;
    font-weight: 600;
    display: block;
    padding: 20px 0;
    color: #000
}

.tamamlayiciUrunContainer>ul {
    margin: 0 30px;
    max-height: 530px;
    overflow-y: auto
}

.tamamlayiciUrunContainer ul ul {
    margin: 0;
    padding: 0 0 0 50px
}

.tamamlayiciUrunContainer ul li {
    margin: 0;
    padding: 0 0 0 0;
    display: block
}

.tamamlayiciUrunContainer ul li .tamamlayiciUrurnItem {
    background-color: #f4f4f4;
    padding: 15px
}

.tamamlayiciUrunContainer ul li span {
    vertical-align: top;
    font-size: 12px;
    display: inline-block;
    padding: 0
}

.tamamlayiciUrunContainer ul li li {
    background-color: #fff;
    vertical-align: top
}

.tamamlayiciUrunContainer ul li li .tamamlayiciUrurnItem {
    background-color: #fff;
    padding: 5px
}

.tamamlayiciUrunContainer ul li li .tamamlayiciUrurnItem .tamamlayiciUrunItemSol {
    float: left
}

.tamamlayiciUrunContainer ul li li .tamamlayiciUrurnItem .tamamlayiciUrunItemSag {
    float: left
}

.tamamlayiciUrunContainer ul li img {
    max-width: 80px;
    display: block;
    max-height: 80px;
    margin: 0
}

.tamamlayiciHeader {
    background-color: #ff671c;
    text-align: center;
    color: #fff;
    padding: 7px 0;
    font-weight: 500;
    letter-spacing: 1px;
    font-size: 16px
}

.tamamlayiciFooter {
    text-align: center;
    margin: 15px 0 15px 0
}

.tamamlayiciFooter button {
    border: 0;
    border-radius: 3px;
    cursor: pointer;
    background-color: #ff671c;
    text-align: center;
    color: #fff;
    padding: 8px 20px;
    font-weight: 500;
    font-size: 14px;
    display: inline-block;
    margin: 0 auto
}

.tamamlayiciFooter button:hover {
    background-color: #000
}

.tamamlayiciFooter button:disabled:hover {
    background-color: #ff671c;
    cursor: default
}

.tamamlayiciUrunWrapper .tamamlayiciUrunList {
    float: left;
    width: 75%;
    display: block
}

.tamamlayiciUrunWrapper .tamamlayiciUrunList li {
    float: left;
    width: 50%;
    display: block;
    overflow: hidden
}

.tamamlayiciUrunWrapper .tamamlayiciUrunList li .tamamlayiciUrurnItem {
    width: calc(100% - 10px);
    border: 1px solid #ddd;
    border-radius: 3px;
    padding: 10px;
    margin: 0 10px 10px 0
}

.tamamlayiciUrunWrapper .tamamlayiciUrunList li .tamamlayiciUrurnItem img {
    float: left;
    border-radius: 3px
}

.tamamlayiciUrunWrapper .tamamlayiciUrunList li .tamamlayiciUrurnItem div.tamamlayiciUrunItemSag {
    float: left;
    display: block;
    width: calc(100% - 80px);
    padding-left: 10px
}

.tamamlayiciUrunWrapper .tamamlayiciUrunList li .tamamlayiciUrurnItem div.tamamlayiciUrunItemSag span {
    display: block
}

.tamamlayiciUrunWrapper .tamamlayiciUrunList li .tamamlayiciUrurnItem div.tamamlayiciUrunItemSag span:first-child {
    font-weight: 600
}

.tamamlayiciUrunWrapper .tamamlayiciUrurnItem {
    float: left;
    width: 25%;
    padding: 10px
}

.ticimaxTab ._tabHead ul {
    display: inline-block;
    vertical-align: top
}

.ticimaxTab ._tabHead li {
    float: left;
    margin-right: 5px;
    max-width: 150px;
    min-width: 150px
}

.ticimaxTab ._tabHead li span {
    float: left;
    width: 100%;
    cursor: pointer;
    line-height: 40px;
    text-align: center;
    border: 1px solid #adadad;
    color: #606060;
    font-size: 15px;
    position: relative
}

.ticimaxTab ._tabHead li.tabUrunActive span {
    background: #ff671b;
    color: #fff;
    border-color: #ff671b
}

.ticimaxTab .divAnasayfaTabAlt {
    width: 100%;
    padding: 0 16px;
    float: left;
    height: 0;
    overflow: hidden;
    position: relative
}

.ticimaxTab .divAnasayfaTabAlt.tabUrunActive {
    overflow: visible;
    height: 100%;
    -webkit-animation: fadein .5s;
    -moz-animation: fadein .5s;
    -ms-animation: fadein .5s;
    -o-animation: fadein .5s;
    animation: fadein .5s
}

.pageNumber .divMoreProducts {
    text-align: center
}

.pageNumber .getMoreProducts {
    margin-top: 10px
}

.pageNumber .productCountInfo {
    line-height: 1.5
}

.pageNumber .productCountBar {
    height: 6px;
    background-color: #f0f0f0;
    border: 1px solid #f0f0f0;
    margin: 8px 0;
    border-radius: 8px
}

.pageNumber .productCountProgress {
    height: 100%;
    background-color: #ccc
}

.pageNumber .divMoreProducts .button {
    margin: 0;
    width: auto;
    height: auto;
    cursor: pointer;
    display: inline-block
}

.productImage .relatedProducts {
    z-index: 20;
    position: absolute;
    bottom: 0;
    right: 15px
}

.modal {
    position: fixed;
    z-index: 9999;
    padding-top: 100px;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    overflow: auto;
    background-color: #000;
    background-color: rgba(0,0,0,.4)
}

.modal .modal-content {
    background-color: #fefefe;
    margin: auto;
    padding: 20px;
    border: 1px solid #888;
    width: 80%
}

.modal .modal-content:after {
    clear: both;
    display: table;
    content: ""
}

.modal .modal-close {
    color: #aaa;
    float: right;
    font-size: 28px;
    font-weight: bold
}

.modal .modal-close:hover,.modal .modal-close:focus {
    color: #000;
    text-decoration: none;
    cursor: pointer
}

.ulRelatedProducts {
    display: flex;
    flex-direction: row;
    margin-top: 20px
}

.ulRelatedProducts li {
    margin: 5px;
    width: 18%
}

.divRelatedProductsPopup h3 {
    text-align: center
}

.ebultenPopupSection {
    width: 650px;
    max-width: 100%
}

.ebultenPopupSection .content-body {
    margin: 0 auto;
    text-align: center;
    padding: 20px
}

.ebultenPopupSection .content-heading {
    text-align: center;
    padding: 30px 30px 0 30px
}

.ebultenPopupSection .content-heading .h2 {
    font-size: 20px;
    color: #000;
    margin: 20px 0 0;
    padding: 0
}

.ebultenPopupSection .content-heading p {
    font-size: 16px;
    color: #000;
    margin: 15px 0;
    padding: 0;
    line-height: 1.5
}

.ebultenPopupSection .input-text-content {
    display: block;
    position: relative
}

.ebultenPopupSection .input-text-content {
    margin-bottom: 10px
}

.ebultenPopupSection .input-text-content input {
    width: 100%;
    border: 1px solid #eaeaea;
    box-shadow: none;
    padding: 0 0 0 15px;
    margin: 0;
    height: 40px;
    color: #000;
    font-size: 14px;
    line-height: 1.4
}

.ebultenPopupSection .input-text-content .tici-valid-error,.ebultenPopupSection .input-chck-content .tici-valid-error,.ebultenPopupSection .userSozlesmeDiv .tici-valid-error {
    font-size: 0;
    position: absolute;
    left: -15px;
    top: 2px;
    margin: 0;
    display: block;
    width: 14px;
    height: 14px;
    border-radius: 999px;
    font-weight: 300;
    background-color: transparent;
    text-align: center;
    padding: 0 0 0 0;
    border: 0
}

.ebultenPopupSection .input-text-content .tici-valid-error:after,.ebultenPopupSection .input-chck-content .tici-valid-error:after,.ebultenPopupSection .userSozlesmeDiv .tici-valid-error:after {
    content: '*';
    font-size: 20px;
    z-index: 999;
    color: #f00;
    border: 0;
    margin: 0;
    background-color: transparent;
    font-family: Helvetica,sans-serif;
    line-height: 1;
    font-weight: 500
}

.ebultenPopupSection .input-text-content input::-webkit-input-placeholder {
    color: #000
}

.ebultenPopupSection .input-text-content input::-moz-placeholder {
    color: #000
}

.ebultenPopupSection .input-text-content input:-ms-input-placeholder {
    color: #000
}

.ebultenPopupSection .input-text-content input:-moz-placeholder {
    color: #000
}

.ebultenPopupSection .intl-tel-input input {
    border: 1px solid #eaeaea !important;
    color: #000 !important;
    font-size: 14px;
    line-height: 1.4
}

.ebultenPopupSection .intl-tel-input input::-webkit-input-placeholder {
    color: #000 !important
}

.ebultenPopupSection .intl-tel-input input::-moz-placeholder {
    color: #000 !important
}

.ebultenPopupSection .intl-tel-input input:-ms-input-placeholder {
    color: #000 !important
}

.ebultenPopupSection .intl-tel-input input:-moz-placeholder {
    color: #000 !important
}

.ebultenPopupSection .input-chck-content,.ebultenPopupSection .userSozlesmeDiv {
    text-align: left;
    color: #000 !important;
    font-size: 14px;
    line-height: 1.4;
    position: relative;
    margin-bottom: 5px
}

.ebultenPopupSection .userSozlesmeDiv a {
    text-decoration: underline;
    color: #000 !important;
    font-size: 14px;
    line-height: 1.4
}

.ebultenPopupSection .send-button {
    margin-top: 20px
}

.ebultenPopupSection .send-button input {
    width: 100%;
    border: 0;
    box-shadow: none;
    padding: 0;
    margin: 0;
    height: 40px;
    background-color: #000;
    color: #fff;
    cursor: pointer;
    font-size: 15px;
    line-height: 1.4
}

.tamamlayiciUrunWrapper .tamamlayiciUrunList li:nth-child(odd) {
    clear: both
}

@media screen and (max-width: 860px) {
    .tamamlayiciUrunContent {
        width:100%
    }

    .tamamlayiciUrunWrapper .tamamlayiciUrurnItem {
        width: 30%
    }

    .tamamlayiciUrunWrapper .tamamlayiciUrunList {
        width: 70%
    }
}

@media screen and (max-width: 600px) {
    .tamamlayiciUrunWrapper .tamamlayiciUrunList {
        width:100%;
        padding-left: 10px
    }

    .tamamlayiciUrunWrapper .tamamlayiciUrunList li {
        width: 100%
    }

    .tamamlayiciUrunWrapper>.tamamlayiciUrurnItem {
        display: none
    }
}

@media(max-width: 767px) {
    .ebultenPopupSection .content-heading {
        padding:10px 10px 0 10px
    }

    .ebultenPopupSection .content-body {
        padding: 5px
    }

    .ebultenPopupSection .content-heading .h2 {
        font-size: 16px
    }

    .ebultenPopupSection .content-heading p {
        font-size: 14px
    }

    .ebultenPopupSection .input-chck-content:after,.ebultenPopupSection .userSozlesmeDiv:after {
        clear: both;
        display: table;
        content: ""
    }

    .ebultenPopupSection .input-chck-content input {
        width: 5%;
        float: left;
        margin: 0 5px 0 0
    }

    .ebultenPopupSection .input-chck-content label {
        width: 92%;
        float: left;
        line-height: 1;
        font-size: 12px
    }

    .ebultenPopupSection .userSozlesmeDiv input {
        width: 5%;
        float: left;
        margin: 0 5px 0 0
    }

    .ebultenPopupSection .userSozlesmeDiv label {
        width: 92%;
        float: left;
        line-height: 1;
        font-size: 12px
    }

    .ebultenPopupSection .userSozlesmeDiv a {
        font-size: 12px
    }
}

.productList-Image-Owl .owl-dots {
    text-align: center;
    -webkit-tap-highlight-color: transparent;
    position: absolute;
    z-index: 999;
    bottom: 0;
    left: 0;
    right: 0
}

.productList-Image-Owl .owl-dots .owl-dot {
    display: inline-block;
    zoom:1}

.productList-Image-Owl .owl-dots .owl-dot span {
    width: 10px;
    height: 10px;
    margin: 5px 7px;
    background: #d6d6d6;
    display: block;
   
    transition: opacity .2s ease;
    border-radius: 30px
}

.productList-Image-Owl .owl-dots .owl-dot.active span,.productList-Image-Owl .owl-dots .owl-dot:hover span {
    background: #869791
}

#txtQuickEmail,#txtMailAdres {
    text-transform: lowercase !important
}

.productPoints .rating {
    margin: 5px 0
}

.productPoints .rating i {
    display: inline-block;
    color: #cacaca;
    font-style: normal;
    line-height: 1
}

.productPoints [data-rating^='1'] .star-1 {
    color: #000
}

.productPoints [data-rating^='1.5'] .star-2 {
    background: -webkit-linear-gradient(left,#000 50%,#cacaca 50%);
    
    -webkit-text-fill-color: transparent;
    color: transparent
}

.productPoints [data-rating^='2'] .star-1 {
    color: #000
}

.productPoints [data-rating^='2'] .star-2 {
    color: #000
}

.productPoints [data-rating^='2.5'] .star-3 {
    background: -webkit-linear-gradient(left,#000 50%,#cacaca 50%);
    
    -webkit-text-fill-color: transparent;
    color: transparent
}

.productPoints [data-rating^='3'] .star-1 {
    color: #000
}

.productPoints [data-rating^='3'] .star-2 {
    color: #000
}

.productPoints [data-rating^='3'] .star-3 {
    color: #000
}

.productPoints [data-rating^='3.5'] .star-4 {
    background: -webkit-linear-gradient(left,#000 50%,#cacaca 50%);
    
    -webkit-text-fill-color: transparent;
    color: transparent
}

.productPoints [data-rating^='4'] .star-1 {
    color: #000
}

.productPoints [data-rating^='4'] .star-2 {
    color: #000
}

.productPoints [data-rating^='4'] .star-3 {
    color: #000
}

.productPoints [data-rating^='4'] .star-4 {
    color: #000
}

.productPoints [data-rating^='4.5'] .star-5 {
    background: -webkit-linear-gradient(left,#000 50%,#cacaca 50%);
    
    -webkit-text-fill-color: transparent;
    color: transparent
}

.productPoints [data-rating="5"] i {
    color: #000
}

@media print {
    .productPoints .rating {
        -webkit-print-color-adjust: exact
    }

    .productPoints .rating i {
        text-shadow: none
    }
}

@media print {
    .productPoints .rating {
        -webkit-print-color-adjust: exact
    }

    .productPoints .rating i {
        text-shadow: none
    }
}

.uyegirisPopup .userLeftBox {
    width: 450px;
    max-width: 100%
}

.userContainer:after {
    clear: both;
    display: table;
    content: ""
}

.spanTittle {
    display: block;
    text-align: center;
    margin-bottom: 15px;
    font-size: 22px;
    font-family: 'Segoe UI',Tahoma,Geneva,Verdana,sans-serif;
    font-weight: 600
}

.userDivRow:after {
    clear: both;
    display: table;
    content: ""
}

.userDivLeft,.userDivRight {
    width: 50%;
    float: left
}

.userDivRight {
    float: right
}

.userLeftBox,.userRightBox {
    margin: 0;
    padding: 0;
    background-color: #fff;
    border: 0
}

.userWrapper {
    margin-bottom: 10px
}

.userWrapper:after {
    clear: both;
    display: table;
    content: ""
}

.userWrapper input {
    letter-spacing: .3px;
    background-color: #fff;
    height: auto;
    border-radius: 0;
    box-shadow: none;
    padding: 15px 0;
    border: 1px solid #eee;
    font-weight: normal;
    color: #555;
    width: 100%;
    text-indent: 15px;
    line-height: 1
}

.userLoginBtn,.userSignBtn {
    cursor: pointer;
    border: 0;
    border-radius: 0;
    height: auto;
    padding: 12px 0;
    line-height: normal;
    font-weight: 500;
    font-size: 13px;
    font-family: 'Segoe UI',Tahoma,Geneva,Verdana,sans-serif;
    letter-spacing: .6px;
    float: none;
    width: 100%;
    display: block;
    margin: 10px 0 0 0
}

.userLoginBtn:hover,.userSignBtn:hover {
    background-color: #333;
    color: #fff
}

.userLoginBtn {
    width: 100%;
    float: none;
    text-align: center;
    margin-top: 20px;
    clear: left;
    line-height: 1.5 !important;
    padding: 15px 0
}

.userPassBtn,.userSignBtn,.userSignUp,.userLogin {
    display: block;
    text-align: left;
    text-decoration: underline;
    font-size: 13px;
    margin-top: 10px
}

.userSignUp {
    display: block;
    text-align: center;
    border: 1px solid #666;
    padding: 12px 0;
    font-family: 'Segoe UI',Tahoma,Geneva,Verdana,sans-serif;
    clear: left
}

.userLogin {
    text-decoration: none;
    text-align: center;
    color: #000;
    font-size: 13px;
    font-family: 'Segoe UI',Tahoma,Geneva,Verdana,sans-serif;
    clear: left;
    margin-top: 15px;
    border-top: 1px solid #eee;
    font-style: italic
}

.userLogin p.backBtn {
    font-style: normal;
    display: block;
    text-align: center;
    border: 1px solid #666;
    padding: 12px 0;
    font-family: 'Segoe UI',Tahoma,Geneva,Verdana,sans-serif;
    clear: left;
    color: #000;
    font-weight: 600;
    text-decoration: none;
    margin-bottom: 0;
    margin-top: 15px
}

.userLogin p:last-child:hover {
    background-color: #000;
    color: #fff
}

.userSignUp:hover {
    background-color: #000;
    color: #fff
}

.userPassBtn {
    margin: 10px 0;
    display: inline-block;
   
    line-height: normal;
    font-family: 'Segoe UI',Tahoma,Geneva,Verdana,sans-serif;
    font-size: 12px
}

.uyeGirisBeniHatirla {
    float: left;
    margin: 10px 0;
    line-height: normal;
    font-size: 12px;
    font-family: 'Segoe UI',Tahoma,Geneva,Verdana,sans-serif
}

.socialMediaLoginButtons {
    clear: both
}

.userMail,.userSms,.userSozlesmeDiv {
    width: 100%;
    margin-bottom: 5px
}

.userMail:after,.userSms:after,.userSozlesmeDiv:after {
    clear: both;
    display: table;
    content: ""
}

.userMail input,.userSms input,.userSozlesmeDiv input {
    float: left;
    width: 17px;
    margin-top: 0;
    margin-left: 0
}

.userMail label,.userSms label,.userSozlesmeDiv label {
    float: left;
    width: 90%;
    line-height: 12px;
    font-size: 11px;
    font-family: 'Segoe UI',Tahoma,Geneva,Verdana,sans-serif
}

.userSozlesmeDiv label a {
    line-height: 12px;
    font-size: 11px
}

.baglanButton {
    padding: 0;
    line-height: normal;
    margin: 10px 0 0 0;
    height: auto;
    width: 100%;
    border-radius: 0;
    margin: 10px 0 0 0
}

.baglanButton a {
    cursor: pointer;
    display: block;
    padding: 15px 0
}

.alert-danger {
    background-color: transparent;
    border: 0;
    color: #f00;
    font-family: 'Segoe UI',Tahoma,Geneva,Verdana,sans-serif;
    font-size: 12px;
    font-weight: 400;
    padding: 0;
    margin: 0
}

.popupContent {
    padding-top: 50px !important;
    padding-bottom: 50px !important
}

.popupContent .userLeftBox,.popupContent .userRightBox {
    margin: 0
}

.popupContent .userLogin {
    margin: 0 auto;
    text-align: center
}

#txtUyeGirisEmail-error {
    display: none !important
}

#txtUyeGirisPassword-error {
    display: none !important
}

.productItemVariantDetail {
    position: absolute;
    top: 0;
    background: rgba(0,0,0,.6);
    z-index: 999;
    bottom: 0;
    left: 0;
    right: 0;
    border: 1px solid #efefef;
    padding: 10px;
    opacity: 0;
    display: none
}

.productItemVariantDetail.active {
    opacity: 1;
    display: block
}

.productItemVariantDetail .ekSecenek {
    margin-bottom: 12px
}

.productItemVariantDetail .ekSecenek:after {
    clear: both;
    display: table;
    content: ""
}

.productItemVariantDetail .ekSecenekValues.selected .size_box {
    background-color: #ddd;
    color: #333
}

.productItemVariantDetail .btnVaryasyonSepeteEkle {
    width: 100%
}

body.modalOpen {
    padding-right: 17px
}

#globalLiteCart {
    overflow: auto
}

#globalLiteCart .modal-close {
    position: fixed;
    left: 0;
    right: 0;
    top: 0;
    bottom: 0;
    font-size: 0;
    z-index: 100;
    display: block !important
}

#globalLiteCart .modal-content {
    position: fixed;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    overflow: hidden;
    height: 100%;
    width: 100% !important;
    border: 0;
    padding: 0;
    background-color: transparent
}

#globalLiteCart .modal-content-html {
    position: absolute;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    overflow: scroll;
    -webkit-overflow-scrolling: touch;
    width: 100%;
    overflow: hidden
}

.miniCartBos {
    padding: 1rem;
    font-size: 26px;
    letter-spacing: 3px;
    line-height: 30px;
    text-align: center;
    margin: 1rem 0;
    padding: 1rem 0;
    display: block
}

#divCartMiniContent .miniCartLeftProductIem .productIcon,#divCartMiniContent .miniCartLeftProductIem .productMarka,#divCartMiniContent .miniCartLeftProductIem .productPoints,#divCartMiniContent .miniCartLeftProductIem .TukendiIco,#divCartMiniContent .miniCartLeftProductIem .productOnYazi {
    display: none
}

.miniCartLeftTitle {
    width: 100%;
    color: #000;
    text-align: center;
    padding: .9rem
}

.miniCartLeftTitle .modal-close {
    text-decoration: none;
    display: inline-block;
    padding: 0;
    margin: 0;
    cursor: pointer;
    position: static
}

.miniCartLeftTitle .modal-close svg {
    width: 12px;
    height: 12px
}

.miniCartLeftProduct .miniCartLeftProductIem {
    width: 145px;
    margin: auto;
    margin-bottom: 20px
}

.miniCartLeftProduct .miniCartLeftProductIem .productPrice {
    display: flex;
    flex-direction: row
}

.miniCartLeftProduct .miniCartLeftProductIem .regularPrice {
    order: -1;
    font-size: 11px;
    line-height: 17px;
    letter-spacing: .04em;
    text-transform: inherit;
    text-decoration: line-through;
    margin-right: 15px
}

.miniCartLeftProduct .miniCartLeftProductIem .regularPrice .regularKdv,.miniCartLeftProduct .miniCartLeftProductIem .discountPrice .discountKdv {
    display: none
}

.miniCartRigthHeader {
    background: #232323;
    width: 100%;
    height: 46px;
    position: fixed;
    z-index: 200
}

.miniCartRigthHeader .spnCartTxt {
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    width: 100%;
    color: #fff;
    text-align: center
}

.miniCartRigthHeader .header-close-btn {
    position: absolute;
    right: 0;
    top: 50%;
    transform: translateY(-50%);
    width: 50px;
    cursor: pointer
}

.miniCartRigthHeader .header-close-btn svg {
    width: 16px;
    height: 16px;
    fill: #fff
}

.miniCartRigthScroll {
    height: 100vh;
    overflow: auto;
    padding-top: 46px
}

.miniCartSatir1 {
    width: 100%;
    min-height: 45px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 .5rem;
    border-bottom: 1px solid #e1e1e1
}

.miniCartSatir1.bottom {
    border-top: 1px solid #e1e1e1
}

.miniCartSatir2 {
    padding: 1rem .5rem 1rem .5rem;
    line-height: 21px;
    font-size: 16px;
    border-bottom: 1px solid #e1e1e1
}

.miniCartSatir2 .signInButton {
    display: block;
    width: 100%;
    text-align: center;
    padding: 11px 0;
    margin-bottom: .5rem;
    background-color: #000;
    color: #fff
}

.miniCartSatir2 .checkoutAsGuestButton {
    display: block;
    width: 100%;
    text-align: center;
    padding: 11px 0;
    background-color: #000;
    color: #fff
}

.miniCartLeftProduct:After,.miniCartRigth:After {
    clear: both;
    display: table;
    content: ""
}

#divCartMiniContent {
    position: absolute;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    overflow: scroll;
    -webkit-overflow-scrolling: touch;
    width: 100%;
    overflow: hidden
}

.miniCartLeftProduct {
    overflow: auto;
    opacity: 0;
    visibility: hidden;
    position: absolute;
    transform: translateX(130%);
    width: 224px;
    right: 376px;
    top: 46px;
    bottom: 0;
    background-color: #f5f5f5;
    transition: all 500ms cubic-bezier(.65,.05,.36,1) 0s;
    z-index: 101
}

.miniCartRigth {
    background: #fff;
    top: 0;
    right: 0;
    bottom: 0;
    transform: translateX(130%);
    position: absolute;
    opacity: 0;
    visibility: hidden;
    overflow: auto;
    overflow-y: hidden;
    width: 376px;
    height: 100%;
    transition: all 500ms cubic-bezier(.65,.05,.36,1) 0s;
    z-index: 101
}

body.modalOpen .miniCartRigth {
    overflow: visible;
    opacity: 1;
    visibility: visible;
    overflow-y: hidden;
    z-index: 152;
    transform: translateX(130%);
    opacity: 0;
    visibility: hidden
}

body.modalOpen .miniCartLeftProduct {
    opacity: 1;
    visibility: visible;
    opacity: 0;
    visibility: hidden;
    transform: translateX(130%)
}

#divCartMiniContent.transForm .miniCartRigth.active {
    transition: all 500ms cubic-bezier(.65,.05,.36,1) 0s;
    transform: translateX(0);
    opacity: 1;
    visibility: visible
}

#divCartMiniContent.transForm .miniCartLeftProduct.active {
    transform: translateX(0);
    opacity: 1;
    visibility: visible
}

.miniCartContent {
    padding: 1rem .5rem
}

.miniCartItem {
    position: relative;
    display: flex;
    justify-content: space-between;
    flex-flow: row-reverse wrap
}

.miniCartItem .miniCartRight {
    max-width: calc(148px - 5px);
    flex: 0 1 calc(40% - 5px)
}

.miniCartItem .miniCartLeft {
    max-width: calc(60% - 5px);
    display: flex;
    flex-basis: calc(59% - 5px);
    flex-direction: column;
    justify-content: space-between
}

.miniCartItem .miniCartLeft a {
    position: relative;
    text-decoration: none;
    display: inline-block
}

.miniCartItem .miniCartLeft a img {
    max-width: 100%;
    height: auto;
    border: 0;
    vertical-align: bottom;
    width: calc(148px - 5px)
}

.miniCartHr {
    margin: 1rem 0;
    background: #e1e1e1;
    border: 0;
    height: 1px
}

.miniCartContent .miniCartHr:last-child {
    display: none
}

.miniCartDetail {
    flex: 0 1 calc(33% - 5px);
    max-width: 100%;
    position: relative
}

.miniCartDetail span {
    display: block
}

.miniCartDetail span.minimarka {
    font-size: 12px;
    line-height: 16px;
    letter-spacing: .2em
}

.miniCartDetail span.miniurunAdi {
    font-size: 14px;
    line-height: 18px;
    letter-spacing: .04em
}

.miniCartDetail span.ministokKodu {
    font-size: 11px;
    line-height: 17px;
    letter-spacing: .04em
}

.miniCartButtonSil {
    display: block;
    margin-top: .5rem
}

.miniCartButtonSil a {
    flex: 1 0 0%;
    max-width: 50%;
    text-decoration: none;
    display: inline-block
}

.miniCartButtonSil svg {
    width: 6px;
    height: 8px
}

#sepetEkleModal {
    padding-top: 0
}

#sepetEkleModal .modal-content {
    width: 515px;
    border: 1px solid #000;
    left: auto;
    right: 40px;
    top: 46px;
    padding: 0;
    margin: 0;
    background: #fff;
    overflow: auto;
    position: absolute
}

#sepetEkleModal .modal-content {
    transform: translateY(-130%);
    transition: all 500ms cubic-bezier(.645,.045,.355,1) 0s;
    opacity: 0
}

#sepetEkleModal.transForm .modal-content {
    transition: all 500ms cubic-bezier(.65,.05,.36,1) 0s;
    transform: translateX(0);
    opacity: 1;
    visibility: visible
}

#sepetEkleModal .modal-content .modal-close {
    display: none
}

#sepetEkleModal .divEklenenUrun {
    padding: 1rem
}

#sepetEkleModal .divEklenenUrunRow {
    padding: 1rem 0;
    display: flex;
    padding-top: 0;
    border-top: none
}

#sepetEkleModal .divEklenenUrunRow .divCol1 {
    flex: 0 0 100px;
    position: relative;
    margin-right: 1rem
}

#sepetEkleModal .divEklenenUrunRow .divCol1 img {
    display: block
}

#sepetEkleModal .divEklenenUrunRow .divCol2 {
    flex: 1 1 100px
}

#sepetEkleModal .divEklenenUrunRow .divCol2 h4 {
    font-size: 14px;
    line-height: 18px;
    text-transform: inherit;
    margin: 0;
    padding: 0
}

#sepetEkleModal .divEklenenUrunRow .divCol2 .divStokKodu {
    margin: .5rem 0 5px
}

#sepetEkleModal .divEklenenUrunRow .divCol2 .divOzelAlan {
    margin: 0;
    padding: 0
}

#sepetEkleModal .divEklenenUrunRow .divCol3 {
    text-align: right;
    flex: 0 0 95px
}

#sepetEkleModal .divEklenenUrunRow .divCol3 h3 {
    font-size: 14px;
    line-height: 18px;
    text-transform: inherit
}

#sepetEkleModal .divEklenenSepetToplam {
    padding: 1rem;
    display: flex;
    justify-content: space-between;
    border-top: 1px solid #e1e1e1;
    border-bottom: 1px solid #e1e1e1
}

#sepetEkleModal .divEklenenSepetToplam p {
    margin: 0;
    padding: 0
}

#sepetEkleModal .divAltButonlar {
    padding: 1rem;
    display: flex
}

#sepetEkleModal .divAltButonlar a {
    text-align: center;
    display: block;
    text-decoration: none;
    padding: .8rem 2rem;
    background-color: #000;
    color: #fff;
    font-size: 13px;
    line-height: 1
}

#sepetEkleModal .divAltButonlar a.modalDevamEtBTn {
    flex: 1 1 185px;
    margin-right: .75rem
}

#sepetEkleModal .divAltUrunler {
    padding: 1rem
}

#sepetEkleModal .divAltUrunlertitle {
    line-height: 27px;
    color: #000;
    font-size: 16px;
    margin-bottom: 10px;
    font-weight: normal;
    display: block;
    text-align: center;
    
    padding: 0 !important;
    position: relative;
    z-index: 1
}

#sepetEkleModal .divAltUrunlertitle:after {
    clear: both;
    display: table;
    content: ""
}

#sepetEkleModal .divAltUrunler {
    display: block;
    width: 100%
}

#sepetEkleModal .divAltUrunler .divAltUrunlerList {
    list-style-type: none;
    margin: 0;
    padding: 0
}

#sepetEkleModal .divAltUrunler .divAltUrunlerList .productItem {
    width: 100%;
    margin: 0;
    float: none;
    display: block
}

#sepetEkleModal .divAltUrunler .divAltUrunlerList li {
    display: inline-block;
    vertical-align: top;
    margin-bottom: 0;
    width: calc(100%/3 - 20px);
    float: none;
    margin: 0 5px
}

#sepetEkleModal .divAltUrunler .divAltUrunlerList.owl-carousel li {
    width: auto;
    margin: 0
}

#sepetEkleModal .divAltUrunler .productItem .productDetail {
    height: auto;
    position: relative;
    padding: 0;
    float: none;
    display: block
}

#sepetEkleModal .divAltUrunler .productItem .productDetail .productPrice {
    height: auto;
    position: relative;
    padding: 0;
    float: none;
    text-align: left
}

#sepetEkleModal .divAltUrunler .productItem .productPoints,#sepetEkleModal .divAltUrunler .productItem .TukendiIco,#sepetEkleModal .divAltUrunler .productItem .productOnYazi,#sepetEkleModal .divAltUrunler .productItem .ozelAlan1,#sepetEkleModal .divAltUrunler .productItem .ozelAlan2,#sepetEkleModal .divAltUrunler .productItem .ozelAlan3,#sepetEkleModal .divAltUrunler .productItem .ozelAlan4,#sepetEkleModal .divAltUrunler .productItem .ozelAlan5,#sepetEkleModal .divAltUrunler .productItem .urunListeAdet,#sepetEkleModal .divAltUrunler .productItem .productIcon {
    display: none
}

@media(max-width: 767px) {
    body.modalOpen {
        padding:0
    }

    #sepetEkleModal .modal-content {
        width: 100%;
        right: 0;
        top: 0;
        left: 0;
        bottom: 0
    }

    #sepetEkleModal .divAltUrunler .divAltUrunlerList {
        overflow-x: auto;
        overflow-y: hidden;
        white-space: nowrap
    }

    #sepetEkleModal .divAltUrunler .divAltUrunlerList.owl-carousel {
        overflow: visible;
        white-space: normal
    }

    #sepetEkleModal .divAltUrunler .divAltUrunlerList li {
        width: calc(100%/2 - 20px)
    }

    #sepetEkleModal .divAltButonlar {
        padding: 1rem;
        display: flex;
        flex-direction: column
    }

    #sepetEkleModal .divAltButonlar a {
        width: 100%;
        margin-top: 10px;
        flex: 1
    }

    #sepetEkleModal .divAltButonlar a.modalDevamEtBTn {
        width: 100%;
        margin: 0;
        flex: 1
    }
}

#quickViewV2 .modal-content {
    width: 700px !important
}

.modal-content .ProductDetailMainRow {
    display: flex;
    margin-bottom: 1.5rem;
    flex-wrap: wrap
}

.modal-content .leftImage {
    flex: 0 0 255px;
    margin-right: 1rem;
    flex-direction: column;
    justify-content: flex-start
}

.modal-content .leftImage .Images {
    height: 340px;
    width: 255px;
    text-align: center;
    position: relative
}

.modal-content .leftImage .SmallImages {
    width: 100%;
    margin-top: 20px;
    display: block
}

.modal-content .leftImage .SmallImages .AltImgCapSmallImg {
    display: inline-block;
    margin: 0 10px 10px 0;
    position: relative
}

.modal-content .RightDetail {
    flex: 1 1 100px;
    z-index: 0;
    padding: 0
}

.modal-content .RightDetail .buyfast {
    display: none !important
}

.modal-content .ItemV3_NameSpn {
    display: block;
    font-family: BentonSansBook,Helvetica,Arial,sans-serif;
    font-feature-settings: "liga" 0;
    font-size: 11px;
    line-height: 17px
}

.cloudzoom-lens {
    border: 5px solid #888;
    width: 100px;
    height: 100px;
    box-shadow: 0 0 10px rgba(0,0,0,.4);
    cursor: crosshair;
    z-index: 9999
}

.cloudzoom-zoom {
    background-color: #fff;
    border: 1px solid #888;
    width: 500px;
    height: 200px;
    box-shadow: 0 0 10px rgba(0,0,0,.4)
}

.cloudzoom-zoom-inside {
    border: none;
    box-shadow: none
}

.cloudzoom-caption {
    display: none;
    text-align: left;
    background-color: #000;
    color: #fff;
    font-weight: 700;
    padding: 10px;
    font-family: sans-serif;
    font-size: 11px
}



.cloudzoom-ajax-loader {
    background-image: url(https://cdn.ticimax.com/scripts/ajax-loader.gif);
    width: 32px;
    height: 32px
}

.ticimax-search-content {
    background-color: #fff;
    width: 800px;
    font-size: 0;
    display: flex;
    box-sizing: border-box;
    z-index: 99999;
    box-shadow: 0 6px 10px rgba(0,0,0,.4);
    position: absolute;
    top: 100%;
    left: 0;
    margin-left: 0;
    text-align: left;
    min-height: 642px
}

.ticimax-search-content .quickSearchContent {
    display: flex;
    width: 100%
}

.ticimax-search-content .quickSearchContent>.products {
    width: 100%
}

.ticimax-search-sidebar {
    width: 30%;
    background-color: #f5f6f6;
    padding: 20px 0;
    font-size: 14px;
    overflow-y: auto;
    box-sizing: border-box
}

.ticimax-sidebar-item h3 {
    padding-left: 20px;
    padding-right: 20px;
    font-weight: bold;
    color: #58585a;
    font-size: 15px;
    margin-bottom: 9px;
    margin-top: 0;
    text-transform: capitalize
}

.ticimax-sidebar-item ul {
    list-style: none;
    margin: 0;
    padding: 0;
    font-size: 12px;
    margin-bottom: 20px;
    display: block
}

.ticimax-sidebar-item ul li {
    text-overflow: ellipsis;
    overflow: hidden;
    white-space: nowrap;
    color: #58585a;
    display: block;
    padding: 5px 20px 5px 20px;
    cursor: default;
    font-size: 12px
}

.ticimax-search-products {
    font-size: 14px;
    box-sizing: border-box;
    padding: 20px;
    overflow-y: auto;
    width: 70%;
    background-color: #fff;
    vertical-align: top;
    position: relative;
    padding-bottom: 55px;
    padding-bottom: 20px;
    max-height: unset
}

.ticimax-search-products-title h3 {
    color: #58585a;
    font-weight: 400;
    font-size: 15px;
    margin-bottom: 9px;
    margin-top: 0;
    text-transform: capitalize
}

.products {
    list-style: none;
    padding: 0;
    margin: 0;
    font-size: 0;
    margin-top: 20px
}

.products li {
    width: calc(50% - 6px);
    display: inline-block;
    margin-bottom: 10px;
    color: unset;
    text-decoration: none
}

.products li:nth-child(2n-1) {
    margin-right: 10px
}

.products li a {
    font-size: 12px;
    transition: all 200ms ease;
    border-radius: 5px;
    overflow: hidden;
    border: 1px solid rgba(0,0,0,.1);
    width: 100%;
    display: flex;
    position: relative;
    align-items: center;
    padding-right: 10px;
    box-sizing: border-box;
    cursor: pointer;
    text-decoration: none
}

.products li:hover a {
    box-shadow: 0 0 10px rgba(0,0,0,.2);
    box-sizing: border-box;
    z-index: 2;
    position: relative;
    overflow: hidden;
    transform: scale(1.02)
}

.ticimax-search-content .ticimax-search-product-image {
    float: left;
    min-width: 114px;
    height: 100px;
    position: relative;
    overflow: hidden;
    background-size: 80%;
    background-repeat: no-repeat;
    background-position: center;
    min-width: 70px
}

.ticimax-search-content .ticimax-search-product-image img {
    object-fit: cover;
    position: absolute;
    top: 0;
    bottom: 0;
    margin: auto;
    width: 100%;
    height: 100%;
    left: 0
}

.ticimax-search-content .ticimax-search-product-info {
    padding-left: 10px;
    overflow: hidden
}

.ticimax-search-content .ticimax-search-product-info-name,.ticimax-search-content .ticimax-search-product-info-category {
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis;
    width: inherit;
    display: block;
    -webkit-text-size-adjust: none
}

.ticimax-search-content .ticimax-search-product-info-category {
    color: #a8a9ac;
    font-size: 11px;
    margin-bottom: 5px;
    text-transform: capitalize
}

.ticimax-search-content .ticimax-search-product-info-name {
    color: #58585a;
    font-size: 13px;
    margin-bottom: 2px;
    line-height: 18px
}

.ticimax-search-content .ticimax-search-product-info-price {
    color: #818285;
    font-size: 11px;
    -webkit-text-size-adjust: none
}

.ticimax-search-content span.ticimax-search-product-info-oldPrice {
    text-decoration: line-through;
    color: #d1d2d4;
    margin-left: 5px;
    -webkit-text-size-adjust: none
}

.noRecordsFound {
    text-align: center;
    padding-top: 50px;
    font-size: 18px
}

.sTemp2.ticimax-search-content,.sTemp4.ticimax-search-content {
    width: 400px;
    right: 0;
    left: auto;
    min-height: 200px
}

.sTemp2 .ticimax-search-products,.sTemp4 .ticimax-search-products {
    width: 100%;
    max-height: 300px
}

.sTemp2 .products li,.sTemp4 .products li {
    width: 100%
}

.sTemp2 .products li .ticimax-search-product-image,.sTemp4 .products li .ticimax-search-product-image {
    height: 60px;
    min-width: 40px
}

.sTemp3.ticimax-search-content {
    width: 100%;
    right: 0;
    left: auto;
    min-height: 200px
}

.sTemp3 .ticimax-search-products {
    width: 100%;
    padding: 5px
}

.sTemp3 .products {
    margin-top: 0
}

.sTemp3 .products li {
    width: 100%;
    margin-bottom: 0
}

.sTemp3 .products li a {
    border: 0
}

.sTemp3 .products li:hover a {
    box-shadow: 0 0 0;
    box-sizing: border-box;
    z-index: 2;
    position: relative;
    overflow: hidden;
    transform: none;
    text-decoration: underline
}

.sTemp3 .ticimax-search-product-info-name {
    line-height: 2
}

.ticimax-search-mobil-close-btn {
    display: none
}

@media screen and (max-width: 801px) {
    #divAramaSonuc .isMobilInputContent,#divAramaAlani .isMobilInputContent {
        display:flex;
        align-items: center;
        justify-content: space-between;
        margin: 10px 20px 0
    }

    #divAramaSonuc .ticimaxSearchInput,#divAramaAlani .ticimaxSearchInput {
        align-self: flex-start;
        width: 85%;
        border: 1px solid #efefef;
        border-radius: 0;
        box-shadow: none;
        background: #efefef;
        margin: 0;
        padding: 5px;
        line-height: 1
    }

    body.topAutocompleteActive {
        overflow: hidden
    }

    .sTemp2 .ticimax-search-products,.sTemp4 .ticimax-search-products {
        max-height: none
    }

    #divAramaSonuc .ticimax-search-mobil-close-btn,#divAramaAlani .ticimax-search-mobil-close-btn {
        display: block;
        font-size: 13px;
        color: #58585a
    }

    .ticimax-search-content {
        width: 100vw !important;
        height: 100vh !important;
        position: fixed !important;
        top: 0 !important;
        left: 0 !important;
        overflow: auto !important;
        display: block
    }

    .ticimax-search-sidebar {
        width: 100% !important;
        display: block !important;
        background-color: #fff;
        padding-bottom: 10px !important
    }

    .ticimax-search-products {
        width: 100% !important;
        display: block !important;
        padding-top: 20px !important
    }

    .ticimax-search-products .products li {
        width: 100% !important
    }

    .ticimax-search-products .products li:nth-child(2n-1) {
        margin-right: 0 !important
    }

    .ticimax-search-content.sTemp3 .products {
        margin: 10px
    }

    .ticimax-search-content.sTemp4 .products {
        margin: 0
    }

    .ticimax-search-content {
        padding: 10px 0 140px 0
    }

    .ticimax-search-content .quickSearchContent {
        display: block
    }
}

body.favoriBody {
    padding: 0;
    margin: 0
}

body.favoriBody #tb_Tbody {
    height: 200px;
    overflow: auto
}

body.favoriBody .favoriTitle {
    padding: 10px;
    border-bottom: 1px solid #eee;
    font-family: sans-serif;
    font-size: 14px;
    font-weight: 600;
    color: #676767
}

body.favoriBody #tb_Tbody .detayFavoriListItem {
    border: 0;
    padding: 0 10px 0 12px;
    width: calc(100% - 23px);
    font-size: 14px;
    height: 38px;
    line-height: 38px;
    font-family: sans-serif;
    margin: 0
}

body.favoriBody .detayFavoriListItem button {
    height: 28px;
    margin: 5px 0;
    position: inherit;
    float: right;
    top: 0;
    right: 0;
    border-radius: 3px;
    border: 1px solid #ccc;
    background: #eee
}

body.favoriBody .divGrupOlusturContentBottom input#txtFavoriGrup {
    float: left;
    width: 170px;
    border: 1px solid #ccc;
    padding: 0;
    height: 32px;
    border-radius: 3px;
    padding-left: 10px
}

body.favoriBody .divGrupOlusturContentBottom #btnFavoriGrupKaydet {
    float: right;
    width: 80px;
    height: 34px;
    line-height: 34px;
    margin: 0;
    padding: 0;
    border-radius: 2px;
    border: 1px solid #ccc
}

body.favoriBody .detayFavoriListesiContent {
    height: 300px
}

body.favoriBody #divGrupOlusturContent {
    padding: 5px 10px;
    overflow: hidden
}

body.favoriBody #tb_Tbody .detayFavoriListItem button {
    display: none;
    background: #ddd
}

body.favoriBody #tb_Tbody .detayFavoriListItem:hover {
    background: #eee
}

body.favoriBody #tb_Tbody .detayFavoriListItem:hover button {
    display: block;
    color: #000
}

.pageSifremiUnuttum.SifremiUnuttumContent .SifremiUnuttumContentHata {
    color: #f00
}

.pageSifremiUnuttum.SifremiUnuttumContent.userDivLeft {
    width: 100%;
    margin: 40px auto;
    min-height: 350px
}

.pageSifremiUnuttum.SifremiUnuttumContent .userWrapper {
    margin-bottom: 20px;
    width: 100%;
    margin: 0 auto
}

.pageSifremiUnuttum.SifremiUnuttumContent .userWrapper:after {
    clear: both;
    display: table;
    content: ""
}

.pageSifremiUnuttum.SifremiUnuttumContent .userWrapper input {
    letter-spacing: .3px;
    height: auto;
    border-radius: 0;
    box-shadow: none;
    padding: 15px 0;
    border: 1px solid #eee;
    font-weight: 400;
    width: 100%;
    text-indent: 15px
}

.pageSifremiUnuttum.SifremiUnuttumContent .userLoginBtn {
    cursor: pointer;
    border: 2px solid #000;
    border-radius: 0;
    height: auto;
    padding: 15px 0;
    line-height: normal;
    font-weight: 500;
    font-size: 16px;
    float: none;
    width: 100%;
    display: block;
    margin: 10px 0 0 0
}

.pageSifremiUnuttum.SifremiUnuttumContent .userLoginBtn:hover {
    background-color: #000;
    color: #fff
}

.SifremiUnuttumSucces {
    font-size: 16px;
    font-weight: 600;
    text-align: center;
    line-height: normal
}

@media(max-width: 767px) {
    .pageSifremiUnuttum.SifremiUnuttumContent.userDivLeft {
        width:100%
    }
}

.pageSifremiUnuttum .userWrapper .Left {
    padding: 8px 0
}

.pageSifremiUnuttum #mainHolder_TiciCaptcha_ImgCaptcha {
    width: auto
}

.pageSifremiUnuttum .alert,#mainHolder_txtSifre2,#mainHolder_cvSifre2 {
    height: auto;
    line-height: normal;
    background-color: transparent;
    color: #f00;
    font-size: 13px;
    font-weight: 600;
    border: 0;
    margin: 0;
    padding: 10px 0
}

.pageSifremiUnuttum .pageSifremiUnuttum div#divSifremiUnuttum {
    width: 100%;
    max-width: 450px;
    margin: 0 auto;
    display: block
}

.pageSifremiUnuttum .pageSifremiUnuttum .userWrapper {
    width: 100%
}

.pageSifremiUnuttum .userLoginBtn {
    max-width: 450px;
    margin: 0 auto
}

.pageSifremiUnuttum .SifremiUnuttumContentDesc {
    max-width: 740px;
    margin: 0 auto 20px auto;
    text-align: center;
    width: 100%
}

.pageSifremiUnuttum #divSifremiUnuttum {
    max-width: 450px;
    margin: 0 auto
}

.pageSifremiUnuttum .hataliGuvenlikKodu {
    width: 100%;
    overflow: hidden
}

.sifremiUnuttumCaptcha {
    float: right;
    width: 50%
}

.sifremiUnuttumCaptcha img {
    height: 45px;
    width: 170px;
    background: #eee
}

.sifremiUnuttumCaptchaInput {
    float: left;
    width: 50%;
    padding-right: 10px
}

#divSifreDegistir .userWrapper.newPassword,#divSifreDegistir .userWrapper.newPasswordAgain {
    float: left;
    width: 50%
}

#divSifreDegistir .userWrapper.newPassword {
    padding-right: 10px
}

.iti-mobile .iti--container {
    z-index: 9999!important
}

.btnCatSorting {
    cursor: pointer
}

.divYorumlarV2Desc {
    text-align: center;
    cursor: default
}

.divYorumlarV2Desc_s1 {
    margin: 0;
    padding: 0;
    font-size: 18px;
    line-height: 22px;
    letter-spacing: .04em;
    text-transform: inherit;
    font-weight: 400;
    margin-bottom: .75rem
}

.divYorumlarV2Desc_s2 {
    margin: 0;
    padding: 0;
    font-size: 11px;
    line-height: 17px;
    letter-spacing: .04em;
    text-transform: inherit;
    font-weight: 400
}

.divYorumlarV2Desc_s3 {
    margin: 0;
    padding: 0;
    font-size: 11px;
    line-height: 17px;
    letter-spacing: .04em;
    text-transform: inherit;
    font-weight: 400
}

.divYorumlarV2Desc .rating {
    margin: .75rem 0
}

.divYorumlarV2Desc .rating i {
    font-size: 24px
}

.productPoints {
    float: left;
    clear: both;
    display: block;
    width: 100%
}

.productPoints:after {
    clear: both;
    display: table;
    content: ""
}

.rating {
    margin: 0
}

.rating i {
    font-size: 13px;
    font-style: normal;
    color: #cacaca
}

[data-rating^='1'] .star-1 {
    color: #000
}

[data-rating^='1.5'] .star-2 {
    background: -webkit-linear-gradient(left,#000 50%,#cacaca 50%);
    
    -webkit-text-fill-color: transparent;
    color: transparent
}

[data-rating*='1.6'] .star-2 {
    color: #000
}

[data-rating*='1.7'] .star-2 {
    color: #000
}

[data-rating*='1.8'] .star-2 {
    color: #000
}

[data-rating*='1.9'] .star-2 {
    color: #000
}

[data-rating^='2'] .star-1 {
    color: #000
}

[data-rating^='2'] .star-2 {
    color: #000
}

[data-rating^='2.5'] .star-3 {
    background: -webkit-linear-gradient(left,#000 50%,#cacaca 50%);
    
    -webkit-text-fill-color: transparent;
    color: transparent
}

[data-rating*='2.6'] .star-3 {
    color: #000
}

[data-rating*='2.7'] .star-3 {
    color: #000
}

[data-rating*='2.8'] .star-3 {
    color: #000
}

[data-rating*='2.9'] .star-3 {
    color: #000
}

[data-rating^='3'] .star-1 {
    color: #000
}

[data-rating^='3'] .star-2 {
    color: #000
}

[data-rating^='3'] .star-3 {
    color: #000
}

[data-rating^='3.5'] .star-4 {
    background: -webkit-linear-gradient(left,#000 50%,#cacaca 50%);
    
    -webkit-text-fill-color: transparent;
    color: transparent
}

[data-rating*='3.6'] .star-4 {
    color: #000
}

[data-rating*='3.7'] .star-4 {
    color: #000
}

[data-rating*='3.8'] .star-4 {
    color: #000
}

[data-rating*='3.9'] .star-4 {
    color: #000
}

[data-rating^='4'] .star-1 {
    color: #000
}

[data-rating^='4'] .star-2 {
    color: #000
}

[data-rating^='4'] .star-3 {
    color: #000
}

[data-rating^='4'] .star-4 {
    color: #000
}

[data-rating^='4.5'] .star-5 {
    background: -webkit-linear-gradient(left,#000 50%,#cacaca 50%);
    
    -webkit-text-fill-color: transparent;
    color: transparent
}

[data-rating*='4.6'] .star-5 {
    color: #000
}

[data-rating*='4.7'] .star-5 {
    color: #000
}

[data-rating*='4.8'] .star-5 {
    color: #000
}

[data-rating*='4.9'] .star-5 {
    color: #000
}

[data-rating="5"] i {
    color: #000
}

.divYorumlarV2Section1 {
    padding: 10px
}

.divYorumlarV2Section1_1a1a {
    cursor: default;
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    width: 100%;
    -webkit-box-orient: horizontal;
    -webkit-box-direction: normal;
    -ms-flex-direction: row;
    flex-direction: row;
    -webkit-box-align: center;
    -ms-flex-align: center;
    align-items: center;
    padding: 20px 0 30px 0
}

.divYorumlarV2Slide {
    width: 85%;
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    -webkit-box-orient: vertical;
    -webkit-box-direction: normal;
    -ms-flex-direction: column;
    flex-direction: column;
    height: 200px;
    padding: 0 0 0 0
}

.divYorumlarV2SlideItem {
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    -webkit-box-align: center;
    -ms-flex-align: center;
    align-items: center
}

.divYorumlar-t1c9c {
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    -webkit-box-align: center;
    -ms-flex-align: center;
    align-items: center;
    zoom:1;min-width: 250px;
    padding: 10px 15px;
    padding-left: 0;
    margin-right: 25px
}

.divYorumlar-t1c9c .rating {
    margin-right: 20px
}

.divYorumlar-t1c9c .rating i {
    font-size: 16px
}

.divYorumlar-t1c9k {
    border-radius: 10px;
    -moz-border-radius: 10px;
    -o-border-radius: 10px;
    -webkit-border-radius: 10px;
    -ms-webkit-radius: 10px;
    zoom:1;display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    -webkit-box-pack: start;
    -ms-flex-pack: start;
    justify-content: flex-start;
    -webkit-box-align: center;
    -ms-flex-align: center;
    align-items: center;
    height: 6px;
    background: #f0f0f0;
    width: 100%;
    padding: 0 2px;
    max-width: 412px;
    min-width: 400px
}

.divYorumlar-t1c9k span {
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    height: 6px;
    background-color: #c3c3c3;
    border-radius: 10px
}

.divYorumlar-t149k {
    color: #919191;
    font-size: 12px;
    margin-left: 15px
}

.divYorumlarV2Ortalama {
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    margin-left: 30px;
    margin-right: 0;
    text-align: center;
    width: 15%;
    height: 160px
}

.divYorumlarV2Ortalama-1a1a {
    border-radius: 2px;
    -moz-border-radius: 2px;
    -o-border-radius: 2px;
    -webkit-border-radius: 2px;
    -ms-webkit-radius: 10px;
    zoom:1;display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    position: relative;
    width: 100%;
    -webkit-box-orient: vertical;
    -webkit-box-direction: normal;
    -ms-flex-direction: column;
    flex-direction: column;
    border: 1px solid #e1e1e1
}

.divYorumlarV2Ortalama-1a2a {
    width: 118px;
    font-size: 14px;
    background-color: #fff;
    color: #000;
    position: absolute;
    margin-left: auto;
    margin-right: auto;
    left: 0;
    right: 0;
    top: -10px
}

.divYorumlarV2Ortalama-1a3a {
    margin: 15px auto 0;
    display: block;
    width: 123px;
    max-width: 123px;
    height: 40px
}

.divYorumlarV2Ortalama-1a3a i {
    font-size: 18px
}

.divYorumlarV2Ortalama-1a4a {
    font-size: 84px;
    line-height: 84px;
    font-weight: 600;
    padding-bottom: 10px
}

.divYorumlarV2Section1_1a2a {
    display: block;
    text-align: center
}

.divYorumlarV2Section1_1a2a .divYorumlarV2Section1_1a2a_1 {
    margin: 0;
    padding: 0;
    font-size: 18px;
    line-height: 22px;
    letter-spacing: .04em;
    text-transform: inherit;
    font-weight: 400;
    margin-bottom: .75rem
}

.divYorumlarV2Section1_1a2a .divYorumlarV2Section1_1a2a_2 {
    margin: 0;
    padding: 0;
    margin-bottom: .75rem;
    font-size: 11px;
    line-height: 17px;
    letter-spacing: .04em;
    text-transform: inherit;
    font-weight: 400
}

.divYorumlarV2Section1_1a2a a {
    padding: .5rem 2rem;
    text-decoration: none;
    box-sizing: border-box;
    cursor: pointer;
    display: inline-block;
    text-align: center;
    letter-spacing: .15em;
    text-decoration: none;
    display: inline-block
}

.v2YorumFilter,.v2YorumFilter ul {
    margin: 0;
    padding: 0;
    list-style-type: none
}

.v2YorumFilter li,.v2YorumFilter ul li {
    display: block
}

.divYorumlarV2Section2 {
    border-top: 1px solid #e1e1e1;
    border-bottom: 1px solid #e1e1e1;
    display: block;
    text-transform: capitalize;
    margin: 0 0 .75rem;
    clear: both
}

.v2YorumFilter {
    display: flex;
    justify-content: space-between
}

.v2YorumFilterItem {
    display: block;
    text-transform: capitalize;
    margin: 0;
    padding-top: .5rem;
    clear: both
}

.v2YorumFilterItem-title {
    display: block;
    min-width: 67px;
    max-height: 40px;
    float: left;
    padding: .5rem 5px;
    padding-left: 0
}

.v2YorumFiltreGrup {
    display: flex;
    justify-content: flex-start
}

.filter-last-element {
    width: 186px;
    position: relative;
    overflow: visible;
    z-index: 2;
    max-height: 40px;
    background: #fff;
    color: #000
}

.v2YorumFiltreGrupItem {
    position: relative;
    margin-right: .5rem
}

.filter-last-element .v2YorumFiltreGrupItem {
    margin-right: 0;
    width: 100%
}

.v2YorumFilter .filter-last-element .v2YorumFiltreGrupHide {
    right: 0;
    min-width: 186px
}

.v2YorumFiltreGrupItem>a {
    border: 0;
    background: 0 0;
    cursor: pointer;
    margin: 0;
    padding: 0;
    padding: .5rem;
    max-height: 40px;
    display: block;
    position: relative;
    text-align: left;
    width: 100%;
    text-decoration: none;
    display: inline-block;
    color: inherit
}

.v2YorumFiltreGrupItem>a svg {
    transform: rotate(90deg);
    width: 6px;
    height: 8px;
    padding: 5px;
    box-sizing: content-box;
    margin-left: .5rem;
    float: right;
    position: relative;
    top: -1px;
    fill: #fff;
    background: #232323
}

.v2YorumFilter .v2YorumFiltreGrupHide {
    position: absolute;
    padding: .5rem 1rem;
    z-index: 100;
    height: auto;
    max-height: 347px;
    min-width: 190px;
    display: flex;
    flex-flow: column wrap;
    background: #fff;
    border: 1px solid #232323;
    display: none
}

.v2YorumFiltreGrupItem:hover .v2YorumFiltreGrupHide {
    display: block
}

.v2YorumFiltreGrupItem:hover {
    background-color: #000
}

.v2YorumFiltreGrupItem:hover>a {
    color: #fff
}

.v2YorumFiltreGrupItem:hover a>svg {
    fill: #000;
    background: #fff
}

.v2YorumFiltreGrupHide li {
    width: 150px;
    position: relative
}

.v2YorumFiltreGrupHide li a {
    text-align: left;
    text-decoration: none;
    display: inline-block;
    cursor: pointer;
    padding-left: 1.5rem;
    position: relative;
    margin-bottom: .5rem;
    min-height: 17px;
    color: inherit
}

.v2YorumFiltreGrupHide:not(.ratingFiltre) li>a:hover {
    text-decoration: underline
}

.v2YorumFiltreGrupHide li a:before {
    content: "";
    display: inline-block;
    width: 12px;
    height: 12px;
    border: 1px solid #d7d7d7;
    line-height: 10px;
    font-size: 10px;
    position: absolute;
    top: 2px;
    left: 0;
    z-index: 1
}

.v2YorumFiltreGrupHide li.active a:before {
    border: 1px solid #000;
    background-color: #000
}

.v2YorumFiltreGrupHide li a i {
    font-size: 16px;
    display: inline-block
}

.divYorumlarV2Item {
    border-bottom: 1px solid #e1e1e1;
    display: flex;
    flex-wrap: wrap;
    margin: .75rem 0
}

.yorum-item-left {
    margin: 0 1rem .75rem 0;
    flex: 0 0 200px
}

.yorum-item-right {
    flex: 1 1 0;
    margin-bottom: .75rem;
    max-width: 100%;
    overflow-wrap: break-word
}

.yorum-item-puan {
    display: flex;
    margin-bottom: .75rem
}

.yorum-item-puan span {
    font-size: 11px;
    line-height: 19px
}

.yorum-item-puan .rating {
    margin: 0 0 0 5px;
    align-self: center
}

.yorum-item-puan i {
    font-size: 16px;
    width: 10px;
    display: inline-block
}

.yorum-item-puan-name {
    margin: 0 0 .75rem
}

.yorum-item-puan-yas {
    display: flex;
    margin: 0 0 .75rem
}

.yorum-item-puan-yas span {
    width: 60px
}

.yorum-item-puan-sehir {
    margin: 0 0 .75rem;
    display: flex
}

.yorum-item-puan-sehir span {
    width: 60px
}

.yorum-item-puan-baslik {
    margin-top: 0;
    font-size: 18px;
    line-height: 22px;
    letter-spacing: .04em;
    text-transform: inherit;
    font-weight: 400
}

.yorum-item-puan-date {
    display: block;
    margin: .5rem 0;
    
}

.yorum-item-puan-desc {
    display: block;
    padding: 0;
    margin: .5rem 0
}

.yorum-item-puan-tavsiye-list {
    margin-bottom: .5rem
}

.yorum-item-puan-tavsiye-list p {
    margin-top: .5rem;
    padding: 0
}

.yorum-item-puan-tavsiye-list p svg {
    width: 10px;
    height: 10px
}

.yorum-item-puan-tavsiye-list p span {
    margin: 0 0 0 .5rem
}

.yorum-item-puan-tavsiye-item a {
    font-size: 11px;
    line-height: 17px;
    letter-spacing: .04em;
    text-transform: inherit;
    font-weight: 500;
    color: inherit;
    margin-left: 20px;
    display: inline-block
}

.yorum-item-puan-tavsiye-item a:hover {
    text-decoration: none
}

.divYorumlarV2Section2 {
    margin-top: 30px
}

body .v2YorumFiltreGrupItem>a svg {
    top: 4px
}

#yorumYaz .divYorumYaz.frmUrunDetayYorumYaz .rating i {
    font-size: 40px;
    cursor: pointer
}

#yorumYaz .divYorumYaz.frmUrunDetayYorumYaz .rating i:hover {
    opacity: .7
}

#yorumYaz .detyaYorumFormOneri .formCol2,.detyaYorumFormOneri .formCol3 {
    float: left;
    display: block;
    height: 25px;
    line-height: 25px;
    margin-right: 10px
}

#yorumYaz .divYorumYaz label.yorumLabel {
    font-weight: 600;
    margin-top: 10px;
    display: block
}

#yorumYaz .modal-content {
    max-width: 450px
}

#yorumYaz .detayYorumFormRating .rating {
    margin-top: 10px
}

#yorumYaz .detayYorumYas {
    width: 100%;
    clear: both;
    overflow: hidden
}

#yorumYaz .detayYorumYas .detayYorumYasSatir {
    float: left;
    display: block;
    height: 25px;
    line-height: 25px;
    margin-right: 10px
}

#yorumYaz .detyaYorumFormAd input#txtbxYorumIsim {
    margin-bottom: 5px
}

@media screen and (max-width: 992px) {
    .divYorumlarV2Slide {
        width:80%
    }

    .divYorumlarV2Ortalama {
        width: 20%
    }

    .divYorumlar-t1c9k {
        max-width: 200px;
        min-width: 200px
    }
}

@media screen and (max-width: 767px) {
    .divYorumlarV2Section1_1a1a {
        flex-direction:column
    }

    .divYorumlarV2Slide {
        order: 2;
        width: 100%;
        height: auto
    }

    .divYorumlarV2Ortalama {
        order: 1;
        margin: 0 0 20px 0;
        width: 100%;
        height: auto
    }

    .divYorumlar-t1c9c .rating {
        display: none
    }

    .divYorumlar-t1c9c {
        margin-right: 0;
        padding: 0 10px 5px 0;
        min-width: 140px
    }

    .divYorumlar-t1c9k {
        max-width: 300px;
        min-width: 0
    }

    .v2YorumFilterItem-title {
        display: none
    }

    .v2YorumFilter {
        flex-direction: column
    }

    .urunTabAlt ul li {
        margin: 0;
        clear: both;
        padding: 0
    }

    .divYorumlarV2Item {
        flex-direction: column
    }

    .yorum-item-left {
        flex: 0 0 auto
    }
}




	.hazirSablonlar-15 .trow .img-responsive { min-width: 100%; max-width: 100%; }
    
	.hazirSablonlar-15 .trow:after { clear: both; display: table; content: ""; }
    
	.hazirSablonlar-15 .trow { margin-left: -5px; margin-right: -5px; }
    
	.hazirSablonlar-15 .trow .tcol { float: left; position: relative; min-height: 1px; padding-bottom: 5%; padding-right: 5px; padding-left: 5px;}
	
	.hazirSablonlar-15 .trow .tcol-lg-3 { width: 25%; }
	
	.hazirSablonlar-15 .trow .tcol-lg-4 { width: 33.3%; }
	
    .hazirSablonlar-15 .trow .tcol-lg-6 { width: 50%; }
	
    .hazirSablonlar-15 .trow .tcol-lg-12 { width: 100%; }
	
	.hazirSablonlar-15 .promobanner { position: initial; overflow: hidden;  font-family: 'Futura PT Demi';}
	
	.hazirSablonlar-15 .promobanner .btn-zoom-1 {font-size: 17px; color: #ffffff; padding: 3px 15px 3px 15px; position: absolute; text-shadow: 0px 0px 1px black; bottom: 21%;border-radius: 1.5px; border: 1px solid #fff; }
	.hazirSablonlar-15 .promobanner .btn-zoom-2 {font-weight: 400; font-size: 30px;position: absolute; bottom: 29%;color: #fff;text-shadow: 0px 0px 1.5px black;}

	


.icon-home:before {
    content: "\e900"
}

.icon-home2:before {
    content: "\e901"
}

.icon-home3:before {
    content: "\e902"
}

.icon-office:before {
    content: "\e903"
}

.icon-newspaper:before {
    content: "\e904"
}

.icon-pencil:before {
    content: "\e905"
}

.icon-pencil2:before {
    content: "\e906"
}

.icon-quill:before {
    content: "\e907"
}

.icon-pen:before {
    content: "\e908"
}

.icon-blog:before {
    content: "\e909"
}

.icon-eyedropper:before {
    content: "\e90a"
}

.icon-droplet:before {
    content: "\e90b"
}

.icon-paint-format:before {
    content: "\e90c"
}

.icon-image:before {
    content: "\e90d"
}

.icon-images:before {
    content: "\e90e"
}

.icon-camera:before {
    content: "\e90f"
}

.icon-headphones:before {
    content: "\e910"
}

.icon-music:before {
    content: "\e911"
}

.icon-play:before {
    content: "\e912"
}

.icon-film:before {
    content: "\e913"
}

.icon-video-camera:before {
    content: "\e914"
}

.icon-dice:before {
    content: "\e915"
}

.icon-pacman:before {
    content: "\e916"
}

.icon-spades:before {
    content: "\e917"
}

.icon-clubs:before {
    content: "\e918"
}

.icon-diamonds:before {
    content: "\e919"
}

.icon-bullhorn:before {
    content: "\e91a"
}

.icon-connection:before {
    content: "\e91b"
}

.icon-podcast:before {
    content: "\e91c"
}

.icon-feed:before {
    content: "\e91d"
}

.icon-mic:before {
    content: "\e91e"
}

.icon-book:before {
    content: "\e91f"
}

.icon-books:before {
    content: "\e920"
}

.icon-library:before {
    content: "\e921"
}

.icon-file-text:before {
    content: "\e922"
}

.icon-profile:before {
    content: "\e923"
}

.icon-file-empty:before {
    content: "\e924"
}

.icon-files-empty:before {
    content: "\e925"
}

.icon-file-text2:before {
    content: "\e926"
}

.icon-file-picture:before {
    content: "\e927"
}

.icon-file-music:before {
    content: "\e928"
}

.icon-file-play:before {
    content: "\e929"
}

.icon-file-video:before {
    content: "\e92a"
}

.icon-file-zip:before {
    content: "\e92b"
}

.icon-copy:before {
    content: "\e92c"
}

.icon-paste:before {
    content: "\e92d"
}

.icon-stack:before {
    content: "\e92e"
}

.icon-folder:before {
    content: "\e92f"
}

.icon-folder-open:before {
    content: "\e930"
}

.icon-folder-plus:before {
    content: "\e931"
}

.icon-folder-minus:before {
    content: "\e932"
}

.icon-folder-download:before {
    content: "\e933"
}

.icon-folder-upload:before {
    content: "\e934"
}

.icon-price-tag:before {
    content: "\e935"
}

.icon-price-tags:before {
    content: "\e936"
}

.icon-barcode:before {
    content: "\e937"
}

.icon-qrcode:before {
    content: "\e938"
}

.icon-ticket:before {
    content: "\e939"
}

.icon-cart:before {
    content: "\e93a"
}

.icon-coin-dollar:before {
    content: "\e93b"
}

.icon-coin-euro:before {
    content: "\e93c"
}

.icon-coin-pound:before {
    content: "\e93d"
}

.icon-coin-yen:before {
    content: "\e93e"
}

.icon-credit-card:before {
    content: "\e93f"
}

.icon-calculator:before {
    content: "\e940"
}

.icon-lifebuoy:before {
    content: "\e941"
}

.icon-phone:before {
    content: "\e942"
}

.icon-phone-hang-up:before {
    content: "\e943"
}

.icon-address-book:before {
    content: "\e944"
}

.icon-envelop:before {
    content: "\e945"
}

.icon-pushpin:before {
    content: "\e946"
}

.icon-location:before {
    content: "\e947"
}

.icon-location2:before {
    content: "\e948"
}

.icon-compass:before {
    content: "\e949"
}

.icon-compass2:before {
    content: "\e94a"
}

.icon-map:before {
    content: "\e94b"
}

.icon-map2:before {
    content: "\e94c"
}

.icon-history:before {
    content: "\e94d"
}

.icon-clock:before {
    content: "\e94e"
}

.icon-clock2:before {
    content: "\e94f"
}

.icon-alarm:before {
    content: "\e950"
}

.icon-bell:before {
    content: "\e951"
}

.icon-stopwatch:before {
    content: "\e952"
}

.icon-calendar:before {
    content: "\e953"
}

.icon-printer:before {
    content: "\e954"
}

.icon-keyboard:before {
    content: "\e955"
}

.icon-display:before {
    content: "\e956"
}

.icon-laptop:before {
    content: "\e957"
}

.icon-mobile:before {
    content: "\e958"
}

.icon-mobile2:before {
    content: "\e959"
}

.icon-tablet:before {
    content: "\e95a"
}

.icon-tv:before {
    content: "\e95b"
}

.icon-drawer:before {
    content: "\e95c"
}

.icon-drawer2:before {
    content: "\e95d"
}

.icon-box-add:before {
    content: "\e95e"
}

.icon-box-remove:before {
    content: "\e95f"
}

.icon-download:before {
    content: "\e960"
}

.icon-upload:before {
    content: "\e961"
}

.icon-floppy-disk:before {
    content: "\e962"
}

.icon-drive:before {
    content: "\e963"
}

.icon-database:before {
    content: "\e964"
}

.icon-undo:before {
    content: "\e965"
}

.icon-redo:before {
    content: "\e966"
}

.icon-undo2:before {
    content: "\e967"
}

.icon-redo2:before {
    content: "\e968"
}

.icon-forward:before {
    content: "\e969"
}

.icon-reply:before {
    content: "\e96a"
}

.icon-bubble:before {
    content: "\e96b"
}

.icon-bubbles:before {
    content: "\e96c"
}

.icon-bubbles2:before {
    content: "\e96d"
}

.icon-bubble2:before {
    content: "\e96e"
}

.icon-bubbles3:before {
    content: "\e96f"
}

.icon-bubbles4:before {
    content: "\e970"
}

.icon-user:before {
    content: "\e971"
}

.icon-users:before {
    content: "\e972"
}

.icon-user-plus:before {
    content: "\e973"
}

.icon-user-minus:before {
    content: "\e974"
}

.icon-user-check:before {
    content: "\e975"
}

.icon-user-tie:before {
    content: "\e976"
}

.icon-quotes-left:before {
    content: "\e977"
}

.icon-quotes-right:before {
    content: "\e978"
}

.icon-hour-glass:before {
    content: "\e979"
}

.icon-spinner:before {
    content: "\e97a"
}

.icon-spinner2:before {
    content: "\e97b"
}

.icon-spinner3:before {
    content: "\e97c"
}

.icon-spinner4:before {
    content: "\e97d"
}

.icon-spinner5:before {
    content: "\e97e"
}

.icon-spinner6:before {
    content: "\e97f"
}

.icon-spinner7:before {
    content: "\e980"
}

.icon-spinner8:before {
    content: "\e981"
}

.icon-spinner9:before {
    content: "\e982"
}

.icon-spinner10:before {
    content: "\e983"
}

.icon-spinner11:before {
    content: "\e984"
}

.icon-binoculars:before {
    content: "\e985"
}

.icon-search:before {
    content: "\e986"
}

.icon-zoom-in:before {
    content: "\e987"
}

.icon-zoom-out:before {
    content: "\e988"
}

.icon-enlarge:before {
    content: "\e989"
}

.icon-shrink:before {
    content: "\e98a"
}

.icon-enlarge2:before {
    content: "\e98b"
}

.icon-shrink2:before {
    content: "\e98c"
}

.icon-key:before {
    content: "\e98d"
}

.icon-key2:before {
    content: "\e98e"
}

.icon-lock:before {
    content: "\e98f"
}

.icon-unlocked:before {
    content: "\e990"
}

.icon-wrench:before {
    content: "\e991"
}

.icon-equalizer:before {
    content: "\e992"
}

.icon-equalizer2:before {
    content: "\e993"
}

.icon-cog:before {
    content: "\e994"
}

.icon-cogs:before {
    content: "\e995"
}

.icon-hammer:before {
    content: "\e996"
}

.icon-magic-wand:before {
    content: "\e997"
}

.icon-aid-kit:before {
    content: "\e998"
}

.icon-bug:before {
    content: "\e999"
}

.icon-pie-chart:before {
    content: "\e99a"
}

.icon-stats-dots:before {
    content: "\e99b"
}

.icon-stats-bars:before {
    content: "\e99c"
}

.icon-stats-bars2:before {
    content: "\e99d"
}

.icon-trophy:before {
    content: "\e99e"
}

.icon-gift:before {
    content: "\e99f"
}

.icon-glass:before {
    content: "\e9a0"
}

.icon-glass2:before {
    content: "\e9a1"
}

.icon-mug:before {
    content: "\e9a2"
}

.icon-spoon-knife:before {
    content: "\e9a3"
}

.icon-leaf:before {
    content: "\e9a4"
}

.icon-rocket:before {
    content: "\e9a5"
}

.icon-meter:before {
    content: "\e9a6"
}

.icon-meter2:before {
    content: "\e9a7"
}

.icon-hammer2:before {
    content: "\e9a8"
}

.icon-fire:before {
    content: "\e9a9"
}

.icon-lab:before {
    content: "\e9aa"
}

.icon-magnet:before {
    content: "\e9ab"
}

.icon-bin:before {
    content: "\e9ac"
}

.icon-bin2:before {
    content: "\e9ad"
}

.icon-briefcase:before {
    content: "\e9ae"
}

.icon-airplane:before {
    content: "\e9af"
}

.icon-truck:before {
    content: "\e9b0"
}

.icon-road:before {
    content: "\e9b1"
}

.icon-accessibility:before {
    content: "\e9b2"
}

.icon-target:before {
    content: "\e9b3"
}

.icon-shield:before {
    content: "\e9b4"
}

.icon-power:before {
    content: "\e9b5"
}

.icon-switch:before {
    content: "\e9b6"
}

.icon-power-cord:before {
    content: "\e9b7"
}

.icon-clipboard:before {
    content: "\e9b8"
}

.icon-list-numbered:before {
    content: "\e9b9"
}

.icon-list:before {
    content: "\e9ba"
}

.icon-list2:before {
    content: "\e9bb"
}

.icon-tree:before {
    content: "\e9bc"
}

.icon-menu:before {
    content: "\e9bd"
}

.icon-menu2:before {
    content: "\e9be"
}

.icon-menu3:before {
    content: "\e9bf"
}

.icon-menu4:before {
    content: "\e9c0"
}

.icon-cloud:before {
    content: "\e9c1"
}

.icon-cloud-download:before {
    content: "\e9c2"
}

.icon-cloud-upload:before {
    content: "\e9c3"
}

.icon-cloud-check:before {
    content: "\e9c4"
}

.icon-download2:before {
    content: "\e9c5"
}

.icon-upload2:before {
    content: "\e9c6"
}

.icon-download3:before {
    content: "\e9c7"
}

.icon-upload3:before {
    content: "\e9c8"
}

.icon-sphere:before {
    content: "\e9c9"
}

.icon-earth:before {
    content: "\e9ca"
}

.icon-link:before {
    content: "\e9cb"
}

.icon-flag:before {
    content: "\e9cc"
}

.icon-attachment:before {
    content: "\e9cd"
}

.icon-eye:before {
    content: "\e9ce"
}

.icon-eye-plus:before {
    content: "\e9cf"
}

.icon-eye-minus:before {
    content: "\e9d0"
}

.icon-eye-blocked:before {
    content: "\e9d1"
}

.icon-bookmark:before {
    content: "\e9d2"
}

.icon-bookmarks:before {
    content: "\e9d3"
}

.icon-sun:before {
    content: "\e9d4"
}

.icon-contrast:before {
    content: "\e9d5"
}

.icon-brightness-contrast:before {
    content: "\e9d6"
}

.icon-star-empty:before {
    content: "\e9d7"
}

.icon-star-half:before {
    content: "\e9d8"
}

.icon-star-full:before {
    content: "\e9d9"
}

.icon-heart:before {
    content: "\e9da"
}

.icon-heart-broken:before {
    content: "\e9db"
}

.icon-man:before {
    content: "\e9dc"
}

.icon-woman:before {
    content: "\e9dd"
}

.icon-man-woman:before {
    content: "\e9de"
}

.icon-happy:before {
    content: "\e9df"
}

.icon-happy2:before {
    content: "\e9e0"
}

.icon-smile:before {
    content: "\e9e1"
}

.icon-smile2:before {
    content: "\e9e2"
}

.icon-tongue:before {
    content: "\e9e3"
}

.icon-tongue2:before {
    content: "\e9e4"
}

.icon-sad:before {
    content: "\e9e5"
}

.icon-sad2:before {
    content: "\e9e6"
}

.icon-wink:before {
    content: "\e9e7"
}

.icon-wink2:before {
    content: "\e9e8"
}

.icon-grin:before {
    content: "\e9e9"
}

.icon-grin2:before {
    content: "\e9ea"
}

.icon-cool:before {
    content: "\e9eb"
}

.icon-cool2:before {
    content: "\e9ec"
}

.icon-angry:before {
    content: "\e9ed"
}

.icon-angry2:before {
    content: "\e9ee"
}

.icon-evil:before {
    content: "\e9ef"
}

.icon-evil2:before {
    content: "\e9f0"
}

.icon-shocked:before {
    content: "\e9f1"
}

.icon-shocked2:before {
    content: "\e9f2"
}

.icon-baffled:before {
    content: "\e9f3"
}

.icon-baffled2:before {
    content: "\e9f4"
}

.icon-confused:before {
    content: "\e9f5"
}

.icon-confused2:before {
    content: "\e9f6"
}

.icon-neutral:before {
    content: "\e9f7"
}

.icon-neutral2:before {
    content: "\e9f8"
}

.icon-hipster:before {
    content: "\e9f9"
}

.icon-hipster2:before {
    content: "\e9fa"
}

.icon-wondering:before {
    content: "\e9fb"
}

.icon-wondering2:before {
    content: "\e9fc"
}

.icon-sleepy:before {
    content: "\e9fd"
}

.icon-sleepy2:before {
    content: "\e9fe"
}

.icon-frustrated:before {
    content: "\e9ff"
}

.icon-frustrated2:before {
    content: "\ea00"
}

.icon-crying:before {
    content: "\ea01"
}

.icon-crying2:before {
    content: "\ea02"
}

.icon-point-up:before {
    content: "\ea03"
}

.icon-point-right:before {
    content: "\ea04"
}

.icon-point-down:before {
    content: "\ea05"
}

.icon-point-left:before {
    content: "\ea06"
}

.icon-warning:before {
    content: "\ea07"
}

.icon-notification:before {
    content: "\ea08"
}

.icon-question:before {
    content: "\ea09"
}

.icon-plus:before {
    content: "\ea0a"
}

.icon-minus:before {
    content: "\ea0b"
}

.icon-info:before {
    content: "\ea0c"
}

.icon-cancel-circle:before {
    content: "\ea0d"
}

.icon-blocked:before {
    content: "\ea0e"
}

.icon-cross:before {
    content: "\ea0f"
}

.icon-checkmark:before {
    content: "\ea10"
}

.icon-checkmark2:before {
    content: "\ea11"
}

.icon-spell-check:before {
    content: "\ea12"
}

.icon-enter:before {
    content: "\ea13"
}

.icon-exit:before {
    content: "\ea14"
}

.icon-play2:before {
    content: "\ea15"
}

.icon-pause:before {
    content: "\ea16"
}

.icon-stop:before {
    content: "\ea17"
}

.icon-previous:before {
    content: "\ea18"
}

.icon-next:before {
    content: "\ea19"
}

.icon-backward:before {
    content: "\ea1a"
}

.icon-forward2:before {
    content: "\ea1b"
}

.icon-play3:before {
    content: "\ea1c"
}

.icon-pause2:before {
    content: "\ea1d"
}

.icon-stop2:before {
    content: "\ea1e"
}

.icon-backward2:before {
    content: "\ea1f"
}

.icon-forward3:before {
    content: "\ea20"
}

.icon-first:before {
    content: "\ea21"
}

.icon-last:before {
    content: "\ea22"
}

.icon-previous2:before {
    content: "\ea23"
}

.icon-next2:before {
    content: "\ea24"
}

.icon-eject:before {
    content: "\ea25"
}

.icon-volume-high:before {
    content: "\ea26"
}

.icon-volume-medium:before {
    content: "\ea27"
}

.icon-volume-low:before {
    content: "\ea28"
}

.icon-volume-mute:before {
    content: "\ea29"
}

.icon-volume-mute2:before {
    content: "\ea2a"
}

.icon-volume-increase:before {
    content: "\ea2b"
}

.icon-volume-decrease:before {
    content: "\ea2c"
}

.icon-loop:before {
    content: "\ea2d"
}

.icon-loop2:before {
    content: "\ea2e"
}

.icon-infinite:before {
    content: "\ea2f"
}

.icon-shuffle:before {
    content: "\ea30"
}

.icon-arrow-up-left:before {
    content: "\ea31"
}

.icon-arrow-up:before {
    content: "\ea32"
}

.icon-arrow-up-right:before {
    content: "\ea33"
}

.icon-arrow-right:before {
    content: "\ea34"
}

.icon-arrow-down-right:before {
    content: "\ea35"
}

.icon-arrow-down:before {
    content: "\ea36"
}

.icon-arrow-down-left:before {
    content: "\ea37"
}

.icon-arrow-left:before {
    content: "\ea38"
}

.icon-arrow-up-left2:before {
    content: "\ea39"
}

.icon-arrow-up2:before {
    content: "\ea3a"
}

.icon-arrow-up-right2:before {
    content: "\ea3b"
}

.icon-arrow-right2:before {
    content: "\ea3c"
}

.icon-arrow-down-right2:before {
    content: "\ea3d"
}

.icon-arrow-down2:before {
    content: "\ea3e"
}

.icon-arrow-down-left2:before {
    content: "\ea3f"
}

.icon-arrow-left2:before {
    content: "\ea40"
}

.icon-circle-up:before {
    content: "\ea41"
}

.icon-circle-right:before {
    content: "\ea42"
}

.icon-circle-down:before {
    content: "\ea43"
}

.icon-circle-left:before {
    content: "\ea44"
}

.icon-tab:before {
    content: "\ea45"
}

.icon-move-up:before {
    content: "\ea46"
}

.icon-move-down:before {
    content: "\ea47"
}

.icon-sort-alpha-asc:before {
    content: "\ea48"
}

.icon-sort-alpha-desc:before {
    content: "\ea49"
}

.icon-sort-numeric-asc:before {
    content: "\ea4a"
}

.icon-sort-numberic-desc:before {
    content: "\ea4b"
}

.icon-sort-amount-asc:before {
    content: "\ea4c"
}

.icon-sort-amount-desc:before {
    content: "\ea4d"
}

.icon-command:before {
    content: "\ea4e"
}

.icon-shift:before {
    content: "\ea4f"
}

.icon-ctrl:before {
    content: "\ea50"
}

.icon-opt:before {
    content: "\ea51"
}

.icon-checkbox-checked:before {
    content: "\ea52"
}

.icon-checkbox-unchecked:before {
    content: "\ea53"
}

.icon-radio-checked:before {
    content: "\ea54"
}

.icon-radio-checked2:before {
    content: "\ea55"
}

.icon-radio-unchecked:before {
    content: "\ea56"
}

.icon-crop:before {
    content: "\ea57"
}

.icon-make-group:before {
    content: "\ea58"
}

.icon-ungroup:before {
    content: "\ea59"
}

.icon-scissors:before {
    content: "\ea5a"
}

.icon-filter:before {
    content: "\ea5b"
}

.icon-font:before {
    content: "\ea5c"
}

.icon-ligature:before {
    content: "\ea5d"
}

.icon-ligature2:before {
    content: "\ea5e"
}

.icon-text-height:before {
    content: "\ea5f"
}

.icon-text-width:before {
    content: "\ea60"
}

.icon-font-size:before {
    content: "\ea61"
}

.icon-bold:before {
    content: "\ea62"
}

.icon-underline:before {
    content: "\ea63"
}

.icon-italic:before {
    content: "\ea64"
}

.icon-strikethrough:before {
    content: "\ea65"
}

.icon-omega:before {
    content: "\ea66"
}

.icon-sigma:before {
    content: "\ea67"
}

.icon-page-break:before {
    content: "\ea68"
}

.icon-superscript:before {
    content: "\ea69"
}

.icon-subscript:before {
    content: "\ea6a"
}

.icon-superscript2:before {
    content: "\ea6b"
}

.icon-subscript2:before {
    content: "\ea6c"
}

.icon-text-color:before {
    content: "\ea6d"
}

.icon-pagebreak:before {
    content: "\ea6e"
}

.icon-clear-formatting:before {
    content: "\ea6f"
}

.icon-table:before {
    content: "\ea70"
}

.icon-table2:before {
    content: "\ea71"
}

.icon-insert-template:before {
    content: "\ea72"
}

.icon-pilcrow:before {
    content: "\ea73"
}

.icon-ltr:before {
    content: "\ea74"
}

.icon-rtl:before {
    content: "\ea75"
}

.icon-section:before {
    content: "\ea76"
}

.icon-paragraph-left:before {
    content: "\ea77"
}

.icon-paragraph-center:before {
    content: "\ea78"
}

.icon-paragraph-right:before {
    content: "\ea79"
}

.icon-paragraph-justify:before {
    content: "\ea7a"
}

.icon-indent-increase:before {
    content: "\ea7b"
}

.icon-indent-decrease:before {
    content: "\ea7c"
}

.icon-share:before {
    content: "\ea7d"
}

.icon-new-tab:before {
    content: "\ea7e"
}

.icon-embed:before {
    content: "\ea7f"
}

.icon-embed2:before {
    content: "\ea80"
}

.icon-terminal:before {
    content: "\ea81"
}

.icon-share2:before {
    content: "\ea82"
}

.icon-mail:before {
    content: "\ea83"
}

.icon-mail2:before {
    content: "\ea84"
}

.icon-mail3:before {
    content: "\ea85"
}

.icon-mail4:before {
    content: "\ea86"
}

.icon-amazon:before {
    content: "\ea87"
}

.icon-google:before {
    content: "\ea88"
}

.icon-google2:before {
    content: "\ea89"
}

.icon-google3:before {
    content: "\ea8a"
}

.icon-google-plus:before {
    content: "\ea8b"
}

.icon-google-plus2:before {
    content: "\ea8c"
}

.icon-google-plus3:before {
    content: "\ea8d"
}

.icon-hangouts:before {
    content: "\ea8e"
}

.icon-google-drive:before {
    content: "\ea8f"
}

.icon-facebook:before {
    content: "\ea90"
}

.icon-facebook2:before {
    content: "\ea91"
}

.icon-instagram:before {
    content: "\ea92"
}

.icon-whatsapp:before {
    content: "\ea93"
}

.icon-spotify:before {
    content: "\ea94"
}

.icon-telegram:before {
    content: "\ea95"
}

.icon-twitter:before {
    content: "\ea96"
}

.icon-vine:before {
    content: "\ea97"
}

.icon-vk:before {
    content: "\ea98"
}

.icon-renren:before {
    content: "\ea99"
}

.icon-sina-weibo:before {
    content: "\ea9a"
}

.icon-rss:before {
    content: "\ea9b"
}

.icon-rss2:before {
    content: "\ea9c"
}

.icon-youtube:before {
    content: "\ea9d"
}

.icon-youtube2:before {
    content: "\ea9e"
}

.icon-twitch:before {
    content: "\ea9f"
}

.icon-vimeo:before {
    content: "\eaa0"
}

.icon-vimeo2:before {
    content: "\eaa1"
}

.icon-lanyrd:before {
    content: "\eaa2"
}

.icon-flickr:before {
    content: "\eaa3"
}

.icon-flickr2:before {
    content: "\eaa4"
}

.icon-flickr3:before {
    content: "\eaa5"
}

.icon-flickr4:before {
    content: "\eaa6"
}

.icon-dribbble:before {
    content: "\eaa7"
}

.icon-behance:before {
    content: "\eaa8"
}

.icon-behance2:before {
    content: "\eaa9"
}

.icon-deviantart:before {
    content: "\eaaa"
}

.icon-500px:before {
    content: "\eaab"
}

.icon-steam:before {
    content: "\eaac"
}

.icon-steam2:before {
    content: "\eaad"
}

.icon-dropbox:before {
    content: "\eaae"
}

.icon-onedrive:before {
    content: "\eaaf"
}

.icon-github:before {
    content: "\eab0"
}

.icon-npm:before {
    content: "\eab1"
}

.icon-basecamp:before {
    content: "\eab2"
}

.icon-trello:before {
    content: "\eab3"
}

.icon-wordpress:before {
    content: "\eab4"
}

.icon-joomla:before {
    content: "\eab5"
}

.icon-ello:before {
    content: "\eab6"
}

.icon-blogger:before {
    content: "\eab7"
}

.icon-blogger2:before {
    content: "\eab8"
}

.icon-tumblr:before {
    content: "\eab9"
}

.icon-tumblr2:before {
    content: "\eaba"
}

.icon-yahoo:before {
    content: "\eabb"
}

.icon-yahoo2:before {
    content: "\eabc"
}

.icon-tux:before {
    content: "\eabd"
}

.icon-appleinc:before {
    content: "\eabe"
}

.icon-finder:before {
    content: "\eabf"
}

.icon-android:before {
    content: "\eac0"
}

.icon-windows:before {
    content: "\eac1"
}

.icon-windows8:before {
    content: "\eac2"
}

.icon-soundcloud:before {
    content: "\eac3"
}

.icon-soundcloud2:before {
    content: "\eac4"
}

.icon-skype:before {
    content: "\eac5"
}

.icon-reddit:before {
    content: "\eac6"
}

.icon-hackernews:before {
    content: "\eac7"
}

.icon-wikipedia:before {
    content: "\eac8"
}

.icon-linkedin:before {
    content: "\eac9"
}

.icon-linkedin2:before {
    content: "\eaca"
}

.icon-lastfm:before {
    content: "\eacb"
}

.icon-lastfm2:before {
    content: "\eacc"
}

.icon-delicious:before {
    content: "\eacd"
}

.icon-stumbleupon:before {
    content: "\eace"
}

.icon-stumbleupon2:before {
    content: "\eacf"
}

.icon-stackoverflow:before {
    content: "\ead0"
}

.icon-pinterest:before {
    content: "\ead1"
}

.icon-pinterest2:before {
    content: "\ead2"
}

.icon-xing:before {
    content: "\ead3"
}

.icon-xing2:before {
    content: "\ead4"
}

.icon-flattr:before {
    content: "\ead5"
}

.icon-foursquare:before {
    content: "\ead6"
}

.icon-yelp:before {
    content: "\ead7"
}

.icon-paypal:before {
    content: "\ead8"
}

.icon-chrome:before {
    content: "\ead9"
}

.icon-firefox:before {
    content: "\eada"
}

.icon-IE:before {
    content: "\eadb"
}

.icon-edge:before {
    content: "\eadc"
}

.icon-safari:before {
    content: "\eadd"
}

.icon-opera:before {
    content: "\eade"
}

.icon-file-pdf:before {
    content: "\eadf"
}

.icon-file-openoffice:before {
    content: "\eae0"
}

.icon-file-word:before {
    content: "\eae1"
}

.icon-file-excel:before {
    content: "\eae2"
}

.icon-libreoffice:before {
    content: "\eae3"
}

.icon-html-five:before {
    content: "\eae4"
}

.icon-html-five2:before {
    content: "\eae5"
}

.icon-css3:before {
    content: "\eae6"
}

.icon-git:before {
    content: "\eae7"
}

.icon-codepen:before {
    content: "\eae8"
}

.icon-svg:before {
    content: "\eae9"
}

.icon-IcoMoon:before {
    content: "\eaea"
}



.lnr {
    font-family: linearicons-free;
   
    font-style: normal;
    font-weight: 400;
    font-variant: normal;
    text-transform: none;
    line-height: 1;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale
}

.lnr-home:before {
    content: "\e800"
}

.lnr-apartment:before {
    content: "\e801"
}

.lnr-pencil:before {
    content: "\e802"
}

.lnr-magic-wand:before {
    content: "\e803"
}

.lnr-drop:before {
    content: "\e804"
}

.lnr-lighter:before {
    content: "\e805"
}

.lnr-poop:before {
    content: "\e806"
}

.lnr-sun:before {
    content: "\e807"
}

.lnr-moon:before {
    content: "\e808"
}

.lnr-cloud:before {
    content: "\e809"
}

.lnr-cloud-upload:before {
    content: "\e80a"
}

.lnr-cloud-download:before {
    content: "\e80b"
}

.lnr-cloud-sync:before {
    content: "\e80c"
}

.lnr-cloud-check:before {
    content: "\e80d"
}

.lnr-database:before {
    content: "\e80e"
}

.lnr-lock:before {
    content: "\e80f"
}

.lnr-cog:before {
    content: "\e810"
}

.lnr-trash:before {
    content: "\e811"
}

.lnr-dice:before {
    content: "\e812"
}

.lnr-heart:before {
    content: "\e813"
}

.lnr-star:before {
    content: "\e814"
}

.lnr-star-half:before {
    content: "\e815"
}

.lnr-star-empty:before {
    content: "\e816"
}

.lnr-flag:before {
    content: "\e817"
}

.lnr-envelope:before {
    content: "\e818"
}

.lnr-paperclip:before {
    content: "\e819"
}

.lnr-inbox:before {
    content: "\e81a"
}

.lnr-eye:before {
    content: "\e81b"
}

.lnr-printer:before {
    content: "\e81c"
}

.lnr-file-empty:before {
    content: "\e81d"
}

.lnr-file-add:before {
    content: "\e81e"
}

.lnr-enter:before {
    content: "\e81f"
}

.lnr-exit:before {
    content: "\e820"
}

.lnr-graduation-hat:before {
    content: "\e821"
}

.lnr-license:before {
    content: "\e822"
}

.lnr-music-note:before {
    content: "\e823"
}

.lnr-film-play:before {
    content: "\e824"
}

.lnr-camera-video:before {
    content: "\e825"
}

.lnr-camera:before {
    content: "\e826"
}

.lnr-picture:before {
    content: "\e827"
}

.lnr-book:before {
    content: "\e828"
}

.lnr-bookmark:before {
    content: "\e829"
}

.lnr-user:before {
    content: "\e82a"
}

.lnr-users:before {
    content: "\e82b"
}

.lnr-shirt:before {
    content: "\e82c"
}

.lnr-store:before {
    content: "\e82d"
}

.lnr-cart:before {
    content: "\e82e"
}

.lnr-tag:before {
    content: "\e82f"
}

.lnr-phone-handset:before {
    content: "\e830"
}

.lnr-phone:before {
    content: "\e831"
}

.lnr-pushpin:before {
    content: "\e832"
}

.lnr-map-marker:before {
    content: "\e833"
}

.lnr-map:before {
    content: "\e834"
}

.lnr-location:before {
    content: "\e835"
}

.lnr-calendar-full:before {
    content: "\e836"
}

.lnr-keyboard:before {
    content: "\e837"
}

.lnr-spell-check:before {
    content: "\e838"
}

.lnr-screen:before {
    content: "\e839"
}

.lnr-smartphone:before {
    content: "\e83a"
}

.lnr-tablet:before {
    content: "\e83b"
}

.lnr-laptop:before {
    content: "\e83c"
}

.lnr-laptop-phone:before {
    content: "\e83d"
}

.lnr-power-switch:before {
    content: "\e83e"
}

.lnr-bubble:before {
    content: "\e83f"
}

.lnr-heart-pulse:before {
    content: "\e840"
}

.lnr-construction:before {
    content: "\e841"
}

.lnr-pie-chart:before {
    content: "\e842"
}

.lnr-chart-bars:before {
    content: "\e843"
}

.lnr-gift:before {
    content: "\e844"
}

.lnr-diamond:before {
    content: "\e845"
}

.lnr-linearicons:before {
    content: "\e846"
}

.lnr-dinner:before {
    content: "\e847"
}

.lnr-coffee-cup:before {
    content: "\e848"
}

.lnr-leaf:before {
    content: "\e849"
}

.lnr-paw:before {
    content: "\e84a"
}

.lnr-rocket:before {
    content: "\e84b"
}

.lnr-briefcase:before {
    content: "\e84c"
}

.lnr-bus:before {
    content: "\e84d"
}

.lnr-car:before {
    content: "\e84e"
}

.lnr-train:before {
    content: "\e84f"
}

.lnr-bicycle:before {
    content: "\e850"
}

.lnr-wheelchair:before {
    content: "\e851"
}

.lnr-select:before {
    content: "\e852"
}

.lnr-earth:before {
    content: "\e853"
}

.lnr-smile:before {
    content: "\e854"
}

.lnr-sad:before {
    content: "\e855"
}

.lnr-neutral:before {
    content: "\e856"
}

.lnr-mustache:before {
    content: "\e857"
}

.lnr-alarm:before {
    content: "\e858"
}

.lnr-bullhorn:before {
    content: "\e859"
}

.lnr-volume-high:before {
    content: "\e85a"
}

.lnr-volume-medium:before {
    content: "\e85b"
}

.lnr-volume-low:before {
    content: "\e85c"
}

.lnr-volume:before {
    content: "\e85d"
}

.lnr-mic:before {
    content: "\e85e"
}

.lnr-hourglass:before {
    content: "\e85f"
}

.lnr-undo:before {
    content: "\e860"
}

.lnr-redo:before {
    content: "\e861"
}

.lnr-sync:before {
    content: "\e862"
}

.lnr-history:before {
    content: "\e863"
}

.lnr-clock:before {
    content: "\e864"
}

.lnr-download:before {
    content: "\e865"
}

.lnr-upload:before {
    content: "\e866"
}

.lnr-enter-down:before {
    content: "\e867"
}

.lnr-exit-up:before {
    content: "\e868"
}

.lnr-bug:before {
    content: "\e869"
}

.lnr-code:before {
    content: "\e86a"
}

.lnr-link:before {
    content: "\e86b"
}

.lnr-unlink:before {
    content: "\e86c"
}

.lnr-thumbs-up:before {
    content: "\e86d"
}

.lnr-thumbs-down:before {
    content: "\e86e"
}

.lnr-magnifier:before {
    content: "\e86f"
}

.lnr-cross:before {
    content: "\e870"
}

.lnr-menu:before {
    content: "\e871"
}

.lnr-list:before {
    content: "\e872"
}

.lnr-chevron-up:before {
    content: "\e873"
}

.lnr-chevron-down:before {
    content: "\e874"
}

.lnr-chevron-left:before {
    content: "\e875"
}

.lnr-chevron-right:before {
    content: "\e876"
}

.lnr-arrow-up:before {
    content: "\e877"
}

.lnr-arrow-down:before {
    content: "\e878"
}

.lnr-arrow-left:before {
    content: "\e879"
}

.lnr-arrow-right:before {
    content: "\e87a"
}

.lnr-move:before {
    content: "\e87b"
}

.lnr-warning:before {
    content: "\e87c"
}

.lnr-question-circle:before {
    content: "\e87d"
}

.lnr-menu-circle:before {
    content: "\e87e"
}

.lnr-checkmark-circle:before {
    content: "\e87f"
}

.lnr-cross-circle:before {
    content: "\e880"
}

.lnr-plus-circle:before {
    content: "\e881"
}

.lnr-circle-minus:before {
    content: "\e882"
}

.lnr-arrow-up-circle:before {
    content: "\e883"
}

.lnr-arrow-down-circle:before {
    content: "\e884"
}

.lnr-arrow-left-circle:before {
    content: "\e885"
}

.lnr-arrow-right-circle:before {
    content: "\e886"
}

.lnr-chevron-up-circle:before {
    content: "\e887"
}

.lnr-chevron-down-circle:before {
    content: "\e888"
}

.lnr-chevron-left-circle:before {
    content: "\e889"
}

.lnr-chevron-right-circle:before {
    content: "\e88a"
}

.lnr-crop:before {
    content: "\e88b"
}

.lnr-frame-expand:before {
    content: "\e88c"
}

.lnr-frame-contract:before {
    content: "\e88d"
}

.lnr-layers:before {
    content: "\e88e"
}

.lnr-funnel:before {
    content: "\e88f"
}

.lnr-text-format:before {
    content: "\e890"
}

.lnr-text-format-remove:before {
    content: "\e891"
}

.lnr-text-size:before {
    content: "\e892"
}

.lnr-bold:before {
    content: "\e893"
}

.lnr-italic:before {
    content: "\e894"
}

.lnr-underline:before {
    content: "\e895"
}

.lnr-strikethrough:before {
    content: "\e896"
}

.lnr-highlight:before {
    content: "\e897"
}

.lnr-text-align-left:before {
    content: "\e898"
}

.lnr-text-align-center:before {
    content: "\e899"
}

.lnr-text-align-right:before {
    content: "\e89a"
}

.lnr-text-align-justify:before {
    content: "\e89b"
}

.lnr-line-spacing:before {
    content: "\e89c"
}

.lnr-indent-increase:before {
    content: "\e89d"
}

.lnr-indent-decrease:before {
    content: "\e89e"
}

.lnr-pilcrow:before {
    content: "\e89f"
}

.lnr-direction-ltr:before {
    content: "\e8a0"
}

.lnr-direction-rtl:before {
    content: "\e8a1"
}

.lnr-page-break:before {
    content: "\e8a2"
}

.lnr-sort-alpha-asc:before {
    content: "\e8a3"
}

.lnr-sort-amount-asc:before {
    content: "\e8a4"
}

.lnr-hand:before {
    content: "\e8a5"
}

.lnr-pointer-up:before {
    content: "\e8a6"
}

.lnr-pointer-right:before {
    content: "\e8a7"
}

.lnr-pointer-down:before {
    content: "\e8a8"
}

.lnr-pointer-left:before {
    content: "\e8a9"
}

* {
    margin: 0;
    outline: 0;
    padding: 0;
    -webkit-box-sizing: border-box;
    -moz-box-sizing: border-box;
    box-sizing: border-box
}

@media(max-width: 767px) {
    .hidden-xs {
        display:none!important
    }
}

@media(min-width: 768px) and (max-width:991px) {
    .hidden-sm {
        display:none!important
    }
}

@media(min-width: 992px) and (max-width:1199px) {
    .hidden-md {
        display:none!important
    }
}

@media(min-width: 1200px) {
    .hidden-lg {
        display:none!important
    }
}

.row {
    margin-right: -5px;
    margin-left: -5px
}

.col-xs-1,.col-sm-1,.col-md-1,.col-lg-1,.col-xs-2,.col-sm-2,.col-md-2,.col-lg-2,.col-xs-3,.col-sm-3,.col-md-3,.col-lg-3,.col-xs-4,.col-sm-4,.col-md-4,.col-lg-4,.col-xs-5,.col-sm-5,.col-md-5,.col-lg-5,.col-xs-6,.col-sm-6,.col-md-6,.col-lg-6,.col-xs-7,.col-sm-7,.col-md-7,.col-lg-7,.col-xs-8,.col-sm-8,.col-md-8,.col-lg-8,.col-xs-9,.col-sm-9,.col-md-9,.col-lg-9,.col-xs-10,.col-sm-10,.col-md-10,.col-lg-10,.col-xs-11,.col-sm-11,.col-md-11,.col-lg-11,.col-xs-12,.col-sm-12,.col-md-12,.col-lg-12 {
    position: relative;
    min-height: 1px;
    padding-right: 5px;
    padding-left: 5px
}

.col-xs-1,.col-xs-2,.col-xs-3,.col-xs-4,.col-xs-5,.col-xs-6,.col-xs-7,.col-xs-8,.col-xs-9,.col-xs-10,.col-xs-11,.col-xs-12 {
    float: left
}

.col-xs-12 {
    width: 100%
}

.col-xs-11 {
    width: 91.66666667%
}

.col-xs-10 {
    width: 83.33333333%
}

.col-xs-9 {
    width: 75%
}

.col-xs-8 {
    width: 66.66666667%
}

.col-xs-7 {
    width: 58.33333333%
}

.col-xs-6 {
    width: 50%
}

.col-xs-5 {
    width: 41.66666667%
}

.col-xs-4 {
    width: 33.33333333%
}

.col-xs-3 {
    width: 25%
}

.col-xs-2 {
    width: 16.66666667%
}

.col-xs-1 {
    width: 8.33333333%
}

.col-xs-pull-12 {
    right: 100%
}

.col-xs-pull-11 {
    right: 91.66666667%
}

.col-xs-pull-10 {
    right: 83.33333333%
}

.col-xs-pull-9 {
    right: 75%
}

.col-xs-pull-8 {
    right: 66.66666667%
}

.col-xs-pull-7 {
    right: 58.33333333%
}

.col-xs-pull-6 {
    right: 50%
}

.col-xs-pull-5 {
    right: 41.66666667%
}

.col-xs-pull-4 {
    right: 33.33333333%
}

.col-xs-pull-3 {
    right: 25%
}

.col-xs-pull-2 {
    right: 16.66666667%
}

.col-xs-pull-1 {
    right: 8.33333333%
}

.col-xs-pull-0 {
    right: auto
}

.col-xs-push-12 {
    left: 100%
}

.col-xs-push-11 {
    left: 91.66666667%
}

.col-xs-push-10 {
    left: 83.33333333%
}

.col-xs-push-9 {
    left: 75%
}

.col-xs-push-8 {
    left: 66.66666667%
}

.col-xs-push-7 {
    left: 58.33333333%
}

.col-xs-push-6 {
    left: 50%
}

.col-xs-push-5 {
    left: 41.66666667%
}

.col-xs-push-4 {
    left: 33.33333333%
}

.col-xs-push-3 {
    left: 25%
}

.col-xs-push-2 {
    left: 16.66666667%
}

.col-xs-push-1 {
    left: 8.33333333%
}

.col-xs-push-0 {
    left: auto
}

.col-xs-offset-12 {
    margin-left: 100%
}

.col-xs-offset-11 {
    margin-left: 91.66666667%
}

.col-xs-offset-10 {
    margin-left: 83.33333333%
}

.col-xs-offset-9 {
    margin-left: 75%
}

.col-xs-offset-8 {
    margin-left: 66.66666667%
}

.col-xs-offset-7 {
    margin-left: 58.33333333%
}

.col-xs-offset-6 {
    margin-left: 50%
}

.col-xs-offset-5 {
    margin-left: 41.66666667%
}

.col-xs-offset-4 {
    margin-left: 33.33333333%
}

.col-xs-offset-3 {
    margin-left: 25%
}

.col-xs-offset-2 {
    margin-left: 16.66666667%
}

.col-xs-offset-1 {
    margin-left: 8.33333333%
}

.col-xs-offset-0 {
    margin-left: 0
}

@media(min-width: 768px) {
    .col-sm-1,.col-sm-2,.col-sm-3,.col-sm-4,.col-sm-5,.col-sm-6,.col-sm-7,.col-sm-8,.col-sm-9,.col-sm-10,.col-sm-11,.col-sm-12 {
        float:left
    }

    .col-sm-12 {
        width: 100%
    }

    .col-sm-11 {
        width: 91.66666667%
    }

    .col-sm-10 {
        width: 83.33333333%
    }

    .col-sm-9 {
        width: 75%
    }

    .col-sm-8 {
        width: 66.66666667%
    }

    .col-sm-7 {
        width: 58.33333333%
    }

    .col-sm-6 {
        width: 50%
    }

    .col-sm-5 {
        width: 41.66666667%
    }

    .col-sm-4 {
        width: 33.33333333%
    }

    .col-sm-3 {
        width: 25%
    }

    .col-sm-2 {
        width: 16.66666667%
    }

    .col-sm-1 {
        width: 8.33333333%
    }

    .col-sm-pull-12 {
        right: 100%
    }

    .col-sm-pull-11 {
        right: 91.66666667%
    }

    .col-sm-pull-10 {
        right: 83.33333333%
    }

    .col-sm-pull-9 {
        right: 75%
    }

    .col-sm-pull-8 {
        right: 66.66666667%
    }

    .col-sm-pull-7 {
        right: 58.33333333%
    }

    .col-sm-pull-6 {
        right: 50%
    }

    .col-sm-pull-5 {
        right: 41.66666667%
    }

    .col-sm-pull-4 {
        right: 33.33333333%
    }

    .col-sm-pull-3 {
        right: 25%
    }

    .col-sm-pull-2 {
        right: 16.66666667%
    }

    .col-sm-pull-1 {
        right: 8.33333333%
    }

    .col-sm-pull-0 {
        right: auto
    }

    .col-sm-push-12 {
        left: 100%
    }

    .col-sm-push-11 {
        left: 91.66666667%
    }

    .col-sm-push-10 {
        left: 83.33333333%
    }

    .col-sm-push-9 {
        left: 75%
    }

    .col-sm-push-8 {
        left: 66.66666667%
    }

    .col-sm-push-7 {
        left: 58.33333333%
    }

    .col-sm-push-6 {
        left: 50%
    }

    .col-sm-push-5 {
        left: 41.66666667%
    }

    .col-sm-push-4 {
        left: 33.33333333%
    }

    .col-sm-push-3 {
        left: 25%
    }

    .col-sm-push-2 {
        left: 16.66666667%
    }

    .col-sm-push-1 {
        left: 8.33333333%
    }

    .col-sm-push-0 {
        left: auto
    }

    .col-sm-offset-12 {
        margin-left: 100%
    }

    .col-sm-offset-11 {
        margin-left: 91.66666667%
    }

    .col-sm-offset-10 {
        margin-left: 83.33333333%
    }

    .col-sm-offset-9 {
        margin-left: 75%
    }

    .col-sm-offset-8 {
        margin-left: 66.66666667%
    }

    .col-sm-offset-7 {
        margin-left: 58.33333333%
    }

    .col-sm-offset-6 {
        margin-left: 50%
    }

    .col-sm-offset-5 {
        margin-left: 41.66666667%
    }

    .col-sm-offset-4 {
        margin-left: 33.33333333%
    }

    .col-sm-offset-3 {
        margin-left: 25%
    }

    .col-sm-offset-2 {
        margin-left: 16.66666667%
    }

    .col-sm-offset-1 {
        margin-left: 8.33333333%
    }

    .col-sm-offset-0 {
        margin-left: 0
    }
}

@media(min-width: 992px) {
    .col-md-1,.col-md-2,.col-md-3,.col-md-4,.col-md-5,.col-md-6,.col-md-7,.col-md-8,.col-md-9,.col-md-10,.col-md-11,.col-md-12 {
        float:left
    }

    .col-md-12 {
        width: 100%
    }

    .col-md-11 {
        width: 91.66666667%
    }

    .col-md-10 {
        width: 83.33333333%
    }

    .col-md-9 {
        width: 75%
    }

    .col-md-8 {
        width: 66.66666667%
    }

    .col-md-7 {
        width: 58.33333333%
    }

    .col-md-6 {
        width: 50%
    }

    .col-md-5 {
        width: 41.66666667%
    }

    .col-md-4 {
        width: 33.33333333%
    }

    .col-md-3 {
        width: 25%
    }

    .col-md-2 {
        width: 16.66666667%
    }

    .col-md-1 {
        width: 8.33333333%
    }

    .col-md-pull-12 {
        right: 100%
    }

    .col-md-pull-11 {
        right: 91.66666667%
    }

    .col-md-pull-10 {
        right: 83.33333333%
    }

    .col-md-pull-9 {
        right: 75%
    }

    .col-md-pull-8 {
        right: 66.66666667%
    }

    .col-md-pull-7 {
        right: 58.33333333%
    }

    .col-md-pull-6 {
        right: 50%
    }

    .col-md-pull-5 {
        right: 41.66666667%
    }

    .col-md-pull-4 {
        right: 33.33333333%
    }

    .col-md-pull-3 {
        right: 25%
    }

    .col-md-pull-2 {
        right: 16.66666667%
    }

    .col-md-pull-1 {
        right: 8.33333333%
    }

    .col-md-pull-0 {
        right: auto
    }

    .col-md-push-12 {
        left: 100%
    }

    .col-md-push-11 {
        left: 91.66666667%
    }

    .col-md-push-10 {
        left: 83.33333333%
    }

    .col-md-push-9 {
        left: 75%
    }

    .col-md-push-8 {
        left: 66.66666667%
    }

    .col-md-push-7 {
        left: 58.33333333%
    }

    .col-md-push-6 {
        left: 50%
    }

    .col-md-push-5 {
        left: 41.66666667%
    }

    .col-md-push-4 {
        left: 33.33333333%
    }

    .col-md-push-3 {
        left: 25%
    }

    .col-md-push-2 {
        left: 16.66666667%
    }

    .col-md-push-1 {
        left: 8.33333333%
    }

    .col-md-push-0 {
        left: auto
    }

    .col-md-offset-12 {
        margin-left: 100%
    }

    .col-md-offset-11 {
        margin-left: 91.66666667%
    }

    .col-md-offset-10 {
        margin-left: 83.33333333%
    }

    .col-md-offset-9 {
        margin-left: 75%
    }

    .col-md-offset-8 {
        margin-left: 66.66666667%
    }

    .col-md-offset-7 {
        margin-left: 58.33333333%
    }

    .col-md-offset-6 {
        margin-left: 50%
    }

    .col-md-offset-5 {
        margin-left: 41.66666667%
    }

    .col-md-offset-4 {
        margin-left: 33.33333333%
    }

    .col-md-offset-3 {
        margin-left: 25%
    }

    .col-md-offset-2 {
        margin-left: 16.66666667%
    }

    .col-md-offset-1 {
        margin-left: 8.33333333%
    }

    .col-md-offset-0 {
        margin-left: 0
    }
}

@media(min-width: 1200px) {
    .col-lg-1,.col-lg-2,.col-lg-3,.col-lg-4,.col-lg-5,.col-lg-6,.col-lg-7,.col-lg-8,.col-lg-9,.col-lg-10,.col-lg-11,.col-lg-12 {
        float:left
    }

    .col-lg-12 {
        width: 100%
    }

    .col-lg-11 {
        width: 91.66666667%
    }

    .col-lg-10 {
        width: 83.33333333%
    }

    .col-lg-9 {
        width: 75%
    }

    .col-lg-8 {
        width: 66.66666667%
    }

    .col-lg-7 {
        width: 58.33333333%
    }

    .col-lg-6 {
        width: 50%
    }

    .col-lg-5 {
        width: 41.66666667%
    }

    .col-lg-4 {
        width: 33.33333333%
    }

    .col-lg-3 {
        width: 25%
    }

    .col-lg-2 {
        width: 16.66666667%
    }

    .col-lg-1 {
        width: 8.33333333%
    }

    .col-lg-pull-12 {
        right: 100%
    }

    .col-lg-pull-11 {
        right: 91.66666667%
    }

    .col-lg-pull-10 {
        right: 83.33333333%
    }

    .col-lg-pull-9 {
        right: 75%
    }

    .col-lg-pull-8 {
        right: 66.66666667%
    }

    .col-lg-pull-7 {
        right: 58.33333333%
    }

    .col-lg-pull-6 {
        right: 50%
    }

    .col-lg-pull-5 {
        right: 41.66666667%
    }

    .col-lg-pull-4 {
        right: 33.33333333%
    }

    .col-lg-pull-3 {
        right: 25%
    }

    .col-lg-pull-2 {
        right: 16.66666667%
    }

    .col-lg-pull-1 {
        right: 8.33333333%
    }

    .col-lg-pull-0 {
        right: auto
    }

    .col-lg-push-12 {
        left: 100%
    }

    .col-lg-push-11 {
        left: 91.66666667%
    }

    .col-lg-push-10 {
        left: 83.33333333%
    }

    .col-lg-push-9 {
        left: 75%
    }

    .col-lg-push-8 {
        left: 66.66666667%
    }

    .col-lg-push-7 {
        left: 58.33333333%
    }

    .col-lg-push-6 {
        left: 50%
    }

    .col-lg-push-5 {
        left: 41.66666667%
    }

    .col-lg-push-4 {
        left: 33.33333333%
    }

    .col-lg-push-3 {
        left: 25%
    }

    .col-lg-push-2 {
        left: 16.66666667%
    }

    .col-lg-push-1 {
        left: 8.33333333%
    }

    .col-lg-push-0 {
        left: auto
    }

    .col-lg-offset-12 {
        margin-left: 100%
    }

    .col-lg-offset-11 {
        margin-left: 91.66666667%
    }

    .col-lg-offset-10 {
        margin-left: 83.33333333%
    }

    .col-lg-offset-9 {
        margin-left: 75%
    }

    .col-lg-offset-8 {
        margin-left: 66.66666667%
    }

    .col-lg-offset-7 {
        margin-left: 58.33333333%
    }

    .col-lg-offset-6 {
        margin-left: 50%
    }

    .col-lg-offset-5 {
        margin-left: 41.66666667%
    }

    .col-lg-offset-4 {
        margin-left: 33.33333333%
    }

    .col-lg-offset-3 {
        margin-left: 25%
    }

    .col-lg-offset-2 {
        margin-left: 16.66666667%
    }

    .col-lg-offset-1 {
        margin-left: 8.33333333%
    }

    .col-lg-offset-0 {
        margin-left: 0
    }
}

.img-responsive,.thumbnail>img,.thumbnail a>img,.carousel-inner>.item>img,.carousel-inner>.item>a>img {
    max-width: 100%;
    height: auto
}



input[type=number]::-webkit-inner-spin-button,input[type=number]::-webkit-outer-spin-button {
    appearance: none;
    -moz-appearance: none;
    -webkit-appearance: none;
    margin: 0
}

* {
    margin: 0;
    outline: 0;
    padding: 0;
    font-weight: 400
}

body {
    background: #fff;
    color: #000;
    font-family: josefin sans,sans-serif!important;
    font-weight: 700;
    margin: 0;
    padding: 0
}

html {
    -webkit-box-sizing: border-box!important;
    -moz-box-sizing: border-box!important;
    box-sizing: border-box!important
}

*,:before,:after {
    -webkit-box-sizing: border-box!important;
    -moz-box-sizing: border-box!important;
    box-sizing: border-box!important
}

label input {
    margin-right: 5px
}

#cb3DSecureOdeme {
    margin-right: 8px
}

img {
    border: none;
    max-width: 100%
}

ol,ul {
    list-style: none
}

a {
    text-decoration: none;
    color: #666
}

h1 h2 h3 h4 h5 h6 {
    margin: 0;
    padding: 0;
    font-weight: 400!important
}

body,td,th,input,textarea,select,a {
    font-size: 12px
}

#txtbxCep {
    border: solid 1px #a9a9a9;
    height: 26px;
    color: #777;
    background-color: transparent
}

input[type=text] {
    border: solid 1px #a9a9a9;
    padding: 0 5px;
    height: 26px;
    color: #777
}




input[type=password] {
    border: solid 1px #a9a9a9;
    padding: 4px;
    text-indent: 5px;
    color: #777
}

input[type=submit] {
    border: none;
    cursor: pointer
}

.clear {
    clear: both
}

.bordernone {
    border: none!important
}

select,input {
    font-family: josefin sans,sans-serif!important
}

.textarea {
    font-family: josefin sans,sans-serif!important;
    border: solid 1px #a9a9a9;
    padding: 4px;
    width: 94%;
    height: 80px;
    resize: none;
    color: #777;
    background-color: transparent;
    transition-duration: .2s,.2s;
    -webkit-transition-duration: .2s,.2s
}

.textbox {
    font-family: josefin sans,sans-serif!important;
    color: #666;
    display: block;
    font-size: 14px;
    width: 100%;
    transition-duration: .2s,.2s;
    -webkit-transition-duration: .2s,.2s
}

.button {
    cursor: pointer;
    background: #71034e;
    color: #fff;
    padding: 4px 5px;
    transition: all .3s ease 0;
    border: none!important;
    font-family: josefin sans,sans-serif!important;
    text-align: center
}

.button:hover {
    background-color: #000;
    transition-duration: .2s,.2s;
    -webkit-transition-duration: .2s,.2s
}

.selectboxx {
    height: 26px;
    line-height: 26px;
    padding: 0 5px;
    background-color: none!important;
    width: 100%;
    margin-bottom: 4px
}

.validate,.validateSol,.validateOrta {
    position: absolute;
    right: 1.5%;
    top: 0;
    display: table;
    background-color: #366f2a;
    color: #fff;
    border-radius: 5px;
    padding: 0 10px
}

.validate .validateOk,.validateSol .validateSolOk,.validateOrta .validateOrtaOk {
    background-color: #366f2a;
    position: absolute;
    right: 10px;
    bottom: -5px;
    width: 10px;
    height: 10px;
    display: block;
    border-radius: 0 0 0 15px
}

.cloudzoom-zoom {
    z-index: 999
}

body {
    -webkit-text-size-adjust: 100%
}

button {
    appearance: none;
    -moz-appearance: none;
    -webkit-appearance: none
}

.clearfix {
    content: '';
    clear: both;
    display: block;
    float: left;
    width: 100%
}

.clearfix:after,.clearfix:before {
    content: '';
    clear: both;
    display: block;
    float: left;
    width: 100%
}

.brandItem {
    color: #555;
    font-size: 25px;
    text-transform: capitalize;
    margin-bottom: 12px;
    display: inline-block
}

.brandItem:hover {
    color: #d34848
}

#allBrands {
    display: none
}

.allBrandsActive {
    background-position: center -26px!important
}

.productsHover {
    height: auto!important
}

.tooltip {
    position: absolute;
    z-index: 1030;
    display: block;
    font-size: 12px;
    line-height: 1.4;
    opacity: 0;
    filter: alpha(opacity=0);
    visibility: visible
}

.tooltip.in {
    opacity: .9;
    filter: alpha(opacity=90)
}

.tooltip.top {
    padding: 5px 0;
    margin-top: -3px
}

.tooltip.right {
    padding: 0 5px;
    margin-left: 3px
}

.tooltip.bottom {
    padding: 5px 0;
    margin-top: 3px
}

.tooltip.left {
    padding: 0 5px;
    margin-left: -3px
}

.tooltip-inner {
    max-width: 200px;
    padding: 3px 8px;
    color: #fff;
    text-align: center;
    text-decoration: none;
    background-color: #000
}

.tooltip-arrow {
    position: absolute;
    width: 0;
    height: 0;
    border-color: transparent;
    border-style: solid
}

.tooltip.top .tooltip-arrow {
    bottom: 0;
    left: 50%;
    margin-left: -5px;
    border-top-color: #000;
    border-width: 5px 5px 0
}

.tooltip.top-left .tooltip-arrow {
    bottom: 0;
    left: 5px;
    border-top-color: #000;
    border-width: 5px 5px 0
}

.tooltip.top-right .tooltip-arrow {
    right: 5px;
    bottom: 0;
    border-top-color: #000;
    border-width: 5px 5px 0
}

.tooltip.right .tooltip-arrow {
    top: 50%;
    left: 0;
    margin-top: -5px;
    border-right-color: #000;
    border-width: 5px 5px 5px 0
}

.tooltip.left .tooltip-arrow {
    top: 50%;
    right: 0;
    margin-top: -5px;
    border-left-color: #000;
    border-width: 5px 0 5px 5px
}

.tooltip.bottom .tooltip-arrow {
    top: 0;
    left: 50%;
    margin-left: -5px;
    border-bottom-color: #000;
    border-width: 0 5px 5px
}

.tooltip.bottom-left .tooltip-arrow {
    top: 0;
    left: 5px;
    border-bottom-color: #000;
    border-width: 0 5px 5px
}

.tooltip.bottom-right .tooltip-arrow {
    top: 0;
    right: 5px;
    border-bottom-color: #000;
    border-width: 0 5px 5px
}

#divUstFiltreKategori {
    display: none
}

#divUstFiltreMarka {
    display: none
}

.brandlistselection {
    float: left;
    width: 100%;
    position: relative;
    height: 30px;
    z-index: 99
}

.brandlistselection .selectBox {
    margin-right: 6px;
    display: inline-block;

    border-right: 1px solid #e5e5e5;
    padding: 0 10px;
    display: none
}

.brandlistselection .selectBox p {
    display: none!important;
    font-size: 14px;
    overflow: hidden;
    width: 60px;
    height: 20px;
    line-height: 32px
}

.brandlistselection .selectBox select {
    color: #35bb9f;
    font-size: 13px;
    font-weight: 400;
    border: none;
    background: #fff;
    border-radius: 5px;
    font-family: josefin sans,sans-serif!important;
    cursor: pointer;
    padding: 5px
}

.brandlistselection>label {
    
    display: inline-block;
    color: #373737;
    font-size: 13px;
    font-weight: 300;
    cursor: pointer;
    margin-top: 4px;
    padding-left: 10px;
    margin-left: 10px
}

.brandlistselection label>input[type=checkbox] {
    display: none
}

.brandlistselection label>label {
    color: #373737;
    font-size: 13px;
    font-weight: 500;
    line-height: 21px;
    display: inline-block;
    padding-left: 30px;
    cursor: pointer
}

.brandlistselection label>label:hover {
    color: #373737;
}



.brandlistselection label>input[type=checkbox][checked]+label {
    display: block;

}

#mainHolder_linkFiltreKaldir {
    color: #373737;
    font-size: 13px;
    font-weight: 500;
    margin-top: 5px;
    display: inline-block;
    margin-left: 30px
}

.brandlistselectionBottom {
    margin-bottom: 0;
    display: none
}

.urunListRel {
    width: 100%;
    float: left;
    position: relative;
    margin-top: 0!important;
    text-align: center;
    margin-bottom: 15px
}

.pageNumber {
    float: left;
    text-align: center;
    margin: 0;
    width: 100%;
    display: none
}

.pageNumberBottom {
    float: left;
    text-align: center;
    width: 100%;
    display: block
}

.pageNumberContent,.pageBorder {
    display: inline-block;
    width: 100%
}

.pageNumberContent a,.pageBorder a {
    font-family: abakutlsymsans,sans-serif;
    display: inline-block;
    text-align: center;
    padding: 0 5px;
    font-size: 9px;
    border-radius: 0;
    color: #565656;
    border: 1px solid #5c5c5c;
    font-weight: 400;
    line-height: 15px;
    margin: 0 2px
}

.pageNumberContent a:hover,.pageBorder a:hover {
    color: #565656;
    background: #d0d0d0
}

.pageNumberContent a.SelectedSayfa,.pageBorder a.SelectedSayfa {
    color: #565656;
    background: #d0d0d0
}

.ProductListContent {
    float: left;
    width: 100%
}

.categoryContainer .ProductListContent {
    float: left;
    width: 100%
}

.categoryContainer .ProductList {
    margin: 0 -10px
}

.categoryContainer .ProductListContent .productItem {
    margin-bottom: 30px
}

#divIlgiliUrunler .productModuleItem,.productModuleItem2,.productItem {
    width: 100%;
    position: relative;
    background: #fff;
    text-align: center;
    display: inline-block;
    transition: .3s;
    -moz-transition: .3s;
    -webkit-transition: .3s;
    -ms-transition: .3s
}

.ItemOrj {
    transition: .3s;
    -moz-transition: .3s;
    -webkit-transition: .3s;
    -ms-transition: .3s;
    padding: 0 10px
}

.productItem .productIcon {
    width: 100%;
    height: 100%;
    text-align: center
}

.productItem .productImage {
    height: 0;
    position: relative;
    padding-bottom: 140.5%;
    padding-top: 23px;
    overflow: hidden;
    width: 100%
}

.productItem .productImage a {
    display: block;
    position: relative;
    padding-bottom: 127.5%
}

.productItem .productImage img {
    max-width: 100%;
    max-height: 100%;
    height: auto;
    position: absolute;
    left: 0;
    right: 0;
    top: 0;
    bottom: 0;
    transform: scale(1.2);
    margin: auto
}

.productItem .productDetail {
    display: block;
    float: left;
    width: 100%;
    text-align: left;
    height: 70px;
    position: relative;
    margin-top: 7px;
    padding: 0
}

.productItem .productName {
    width: 100%;
    float: left;
    margin: 3px 0;
    display: block
}

.productItem .productName a {
    float: left;
    width: 100%;
    padding: 0;
    text-align: left;
    font-weight: 600;
    font-size: 14px;
    color: #4e4e4e;
    display: block;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap
}

.productItem .productPrice {
    display: inline-block;
    margin: 0 auto;
    font-family: abakutlsymsans,sans-serif
}

.productItem .discountPrice {
    margin: 0;
    display: inline-block
}

.productItem .discountPrice span {
    color: #000;
    font-size: 17px;
    line-height: 1;
    left: 25px;
    font-weight: 600
}

.productItem .IndirimVar .discountPrice span {
    color: #646464;
    font-size: 17px;
    line-height: 1;
    font-weight: 600
}

.productItem .regularKdv,.productItem .discountKdv {
    display: none
}

.productItem .regularPrice {
    display: inline-block!important;
    margin-right: 7px;
    
    margin-top: 2px
}

.productItem .regularPrice span {
    color: #646464;
    font-size: 13px;
    line-height: 1;
    font-weight: 400;
    text-decoration: line-through;
    
}

.productItem .productMarka {
    display: none!important
}

.productItem .productOnYazi {
    display: none!important;
    margin: 3px 0;
    float: left;
    width: 100%;
    display: none
}

.productItem .productOnYazi * {
    float: left;
    width: 100%;
    padding: 0;
    text-align: left;
    font-weight: 600;
    margin-top: 0;
    font-size: 14px;
    color: #4e4e4e;
    display: block;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap
}

.newIcon {
    display: inline-block;
    position: absolute;
    top: 78px;
    right: 0;
    width: 40px;
    height: 25px;
    font-size: 10px;
    color: #fff;
    overflow: hidden;
    background: #d6001d;
    border: none;
    text-transform: uppercase;
    line-height: 1;
    font-weight: 700;
    text-align: center;
    padding: 2px 1px
}

.discountIcon {
    display: inline-block;
    position: absolute;
    top: 50px;
    right: 0;
    width: 40px;
    height: 25px;
    font-size: 18px;
    font-weight: 700;
    color: #fff;
    overflow: hidden;
    border-radius: 0;
    background: #000;
    line-height: 30px
}

.discountIcon span {
    font-weight: 700
}

.cargoIcon {
    display: block;
    z-index: 2;
    position: absolute;
    left: 11px;
    top: 16px;
    width: 62px;
    height: 62px;
    font-size: 0;
}

.firsatIcon {
    display: block!important;
    position: absolute;
    top: 106px;
    right: 0;
    background: #4b8605;
    width: 40px;
    color: #fff;
    font-size: 8px;
    font-weight: 700;
    text-transform: uppercase;
    text-align: center;
    padding: 2px 3px;
    line-height: 1.3
}

.urunListSonUrun {
    position: absolute;
    left: 0;
    right: 0;
    bottom: 0;
    text-align: center
}

.favori {
    display: inline-block;
    z-index: 2;
    
    position: absolute;
    right: 13px;
    bottom: 99px
}

.mycartIcon {
    display: none;
    z-index: 2;
    float: right;
    margin-right: 10px;
    position: absolute;
    bottom: 85px;
    left: 0!important;
    right: 0;
    background: #a5a5a5
}

.examineIcon {
    display: none;
    float: left;
    margin-left: 13px;
    position: absolute
}

.quickViewIco {
    top: auto!important;
    right: auto!important;
    bottom: 75px;
    left: 25px;
    z-index: 2
}

.quickViewIco a {
    padding: 0;
    font-size: 12px;
    font-weight: 600;
    color: #565656;
    background: 0 0!important
}

.favori a {
    float: left;
    font-size: 0;
    text-align: center;
    width: 100%
}

.examineIcon a {
    float: left;
    font-size: 0
}

.mycartIcon a {
    float: left;
    font-size: 15px;
    color: #fff;
    text-transform: uppercase;
    line-height: 40px;
    width: 100%;
    text-align: center
}

.mycartIcon a span {
    font-weight: 600;
    line-height: 40px
}

.favori a:before {
    display: inline-block;
    content: '\e813';
    font-family: lineariconsfree;
    border-radius: 50%;
    width: 27px;
    height: 27px;
    font-size: 17px;
    background-color: #fff;
    color: #000;
    line-height: 30px;
    font-weight: 600
}

.favori a:after {
    display: none;
    content: 'Kaydet';
    float: left;
    width: 100%;
    color: #565656;
    font-size: 12px;
    font-weight: 600
}

.mycartIcon a:before {
    display: none;
    content: '\e82e';
    font-family: lineariconsfree;
    font-size: 20px;
    color: #919191;
    line-height: 46px;
    float: left;
    font-weight: 400
}

.examineIcon a:before {
    display: none;
    content: '\e86f';
    font-family: lineariconsfree;
    font-size: 20px;
    color: #919191;
    line-height: 46px;
    float: left;
    font-weight: 400
}

.quickViewIco a:before {
    display: inline-block;
    width: 100%;
    content: '\f06e';
    font-family: fontawesome;
    font-size: 25px;
    color: #000;
    line-height: 30px;
    
    font-weight: 400
}

.productItem:hover .quickViewIco {
    display: none!important
}

.productItem .productImage a:after {
    display: none;
    content: '';
    position: absolute;
    left: 0;
    top: 100%;
    right: 0;
    bottom: 0;
    background: rgba(255,255,255,.77);
    transition: all .1s ease;
    -webkit-transition: all .1s ease;
    -moz-transition: all .1s ease;
    -o-transition: all .1s ease;
    z-index: 1
}

.productItem:hover .productImage a:after {
    top: 83.8%
}

.productItem:hover .TukendiIco {
    display: none
}

.productItem:hover .favori {
    display: block
}

.productItem:hover .cargoIcon {
    display: none
}

.productItem:hover .productName a {
    text-decoration: underline
}

.productItem:hover .productOnYazi * {
    text-decoration: underline
}

.boxBedenlerContent {
    display: block!important;
    position: absolute;
    bottom: 68px;
    left: 5%;
    right: 5%
}

.boxBedenlerContent .boxBedenlerContainer {
    float: left;
    width: 100%;
    text-align: left;
    overflow: hidden
}

.boxBedenlerContent .boxBedenlerContainer>div {
    display: inline-block;
    width: 18px;
    height: 13px;
    background: #fff;
    text-align: center;
    margin-right: 4px;
    border-radius: 2px
}

.boxBedenlerContent .boxBedenlerContainer>div a {
    float: left;
    width: 100%;
    height: 100%;
    overflow: hidden
}

.boxBedenlerContent .boxBedenlerContainer>div a img {
    width: 100%;
    height: 100%;
    border-radius: 2px;
    display: inline-block
}

.ngdialog.ngdialog-theme-default .ngdialog-content {
    width: 750px!important;
    padding: 0!important;
    border-radius: 0!important
}

.productItem .urunListeAdet {
    display: none!important;
    width: 85px;
    height: 25px;
    float: left;
    position: relative;
    background: #f1f1f1;
    border-radius: 5px;
    margin-left: 10px
}

.productItem .urunListeAdet input {
    width: 100%;
    height: 25px;
    float: left;
    border: none;
    background: #f1f1f1;
    color: #2c2c2c;
    font-size: 13px;
    padding: 0 20px;
    text-align: center;
    border-radius: 5px
}

.productItem .urunListeAdetArtir {
    font-size: 0;
    width: 20px;
    height: 25px;
    float: left;
    position: absolute;
    right: 0
}

.productItem .urunListeAdetAzalt {
    font-size: 0;
    width: 20px;
    height: 25px;
    float: right;
    position: absolute;
    left: 0
}

.urunListStokUyari {
    display: none
}

.TukendiIco {
    z-index: 2;
    position: absolute;
    left: 0;
    top: 0;
    height: calc(100% - 37px);
    width: 100%
}

.TukendiIco span {
    background: rgba(51,51,51,.6);
    text-align: center;
    padding: 0;
    line-height: 40px;
    color: #fff;
    font-size: 18px;
    text-transform: uppercase;
    font-weight: 600;
    position: absolute;
    bottom: 0;
    left: 0;
    right: 0
}

.categoryContainer .ProductList.pr_hrz .productItem {
    width: 100%;
    margin-right: 0;
    padding-bottom: 0
}

.categoryContainer .ProductList.pr_hrz .productImage {
    float: left;
    width: 20%;
    padding-bottom: 25%
}

.categoryContainer .ProductList.pr_hrz .productItem .productDetail {
    width: calc(100% - 20%)
}

.categoryContainer .ProductList.pr_hrz .mycartIcon {
    margin-right: 0;
    display: block;
    left: 0!important;
    right: auto;
    padding: 0 10px!important;
    bottom: 0
}

.categoryContainer .ProductList.pr_hrz .favori {
    right: 0;
    display: block;
    top: 0
}

.categoryContainer .ProductList.pr_hrz .examineIcon {
    bottom: 65px;
    left: 48.5%
}

.categoryContainer .ProductList.pr_hrz .quickViewIco {
    display: block!important;
    position: absolute;
    text-align: center;
    right: 40px!important;
    left: auto;
    top: 0!important
}

.categoryContainer .ProductList.pr_hrz .cargoIcon {
    right: 35%;
    display: block
}

.categoryContainer .ProductList.pr_hrz .TukendiIco {
    height: 100%
}

.categoryContainer .ProductList.pr_hrz .TukendiIco span {
    text-indent: 20%
}

.categoryContainer .ProductList.pr_hrz .productImage a:after {
    display: none!important
}

.categoryContainer .ProductList.sort_4 .mycartIcon {
    left: 52px
}

.categoryContainer .ProductList.sort_4 .productItem:hover .productImage a:after {
    top: 77.8%
}

.categoryContainer .ProductList.sort_4 .ItemOrj:nth-child(4n) {
    margin-right: 0
}

.sliderBannerContainer .ProductList ul .owl-item li .productItem {
    width: 100%
}

.categoryContainer .ProductList.pr_2 .productItem {
    width: 49%;
    margin-right: 2%
}

.categoryContainer .ProductList.pr_2 .productItem:nth-child(2n) {
    margin-right: 0
}

.pr_2 .TukendiIco span {
    top: 36.7%;
    left: 0
}

.sliderBannerContainer {
    position: relative;
    float: left;
    width: 100%
}

.sliderBannerContainer .owl-carousel {
    padding: 0 60px
}

.sliderBannerContainer .Jbutonlar {
    display: none
}

.sliderBannerContainer .categoryTitle {
    display: block;
    width: 100%;
    padding: 0!important;
    margin: 0!important;
    float: left
}

.sliderBannerContainer .categoryTitle .satir1 .bold {
    float: left;
    width: 100%;
    text-align: center;
    position: relative
}

.sliderBannerContainer .categoryTitle .satir1 .bold:after {
    content: '';
    position: absolute;
    top: 50%;
    left: 10%;
    right: 10%;
    height: 1px;
    background: #dbdbdb;
    border-bottom: 1px solid #f6f6f6;
    z-index: -1
}

.sliderBannerContainer .categoryTitle .satir1 .bold .satir1 {
    display: inline-block;
    font-size: 25px;
    color: #000;
    font-weight: 600;
    line-height: 48px;
    text-align: center;
    background: #fff;
    padding: 0 22px
}

.sliderBannerContainer ul li {
    float: left
}

.sliderBannerContainer ul li:nth-child(5n) {
    margin-right: 0
}

.sliderBannerContainer ul .owl-item li {
    float: left;
    width: 100%;
    margin-right: 0
}

.sliderBannerContainer .slick-slider {
    margin: 0
}

.sliderBannerContainer ul .slick-track li {
    float: left;
    width: 100%;
    margin-right: 0;
    padding: 0 10px
}

.sliderBannerContainer .slick-dots {
    display: none!important
}

.sliderBannerContainer .owl-dots {
    display: none
}

.sliderBannerContainer .owl-nav {
    position: absolute;
    top: 50%;
    left: 0;
    right: 0
}

.sliderBannerContainer .ProductListprev {
    font-size: 0;
    display: inline-block;
    position: absolute;
    cursor: pointer;
    left: 0;
    text-align: right
}

.sliderBannerContainer .ProductListnext {
    font-size: 0;
    display: inline-block;
    position: absolute;
    cursor: pointer;
    right: 0;
    text-align: left
}

.sliderBannerContainer .ProductListnext:after {
    content: '\e876';
    font-family: lineariconsfree;
    font-size: 37px;
    color: gray;
    line-height: 37px;
    float: left;
    width: 100%
}

.sliderBannerContainer .ProductListprev:after {
    content: '\e875';
    font-family: lineariconsfree;
    font-size: 37px;
    color: gray;
    line-height: 37px;
    float: left;
    width: 100%
}

.categoryTitle {
    float: left;
    width: 100%
}

.categoryTitle .categoryTitleText {
    margin: 0 auto 10px;
    width: 100%
}

.categorydesign {
    float: left;
    width: 100%;
    position: relative;
    text-align: center
}

.categorydesign * {
    font-family: josefin sans,sans-serif!important;
    letter-spacing: .5px;
    line-height: 23px;
    color: #000
}

.categorydesign strong {
    font-weight: 700
}

.categorydesign>img {
    display: flex
}

.categorydesign .CTextAlan {
    float: right;
    width: 615px;
    background: #fff;
    margin-top: 30px;
    height: 138px;
    padding: 10px 0 10px 20px
}

.categorydesign .ScrollText {
    float: left;
    width: 100%;
    height: 100%;
    overflow-y: auto;
    overflow-x: hidden
}

.ScrollText::-webkit-scrollbar {
    width: 10px
}

.ScrollText::-webkit-scrollbar-track {
    background: #f6f6f6
}

.ScrollText::-webkit-scrollbar-thumb {
    background: #dbdbdb;
    border-radius: 0
}

.Linklesme {
    display: block;
    margin: 0 auto;
    max-width: 70%
}

.Linklesme ul {
    float: left;
    width: 33%
}

.Linklesme ul li {
    float: left;
    width: 100%
}

.Linklesme ul li * {
    letter-spacing: 0
}

.Linklesme ul li a {
    color: #000
}

.Linklesme ul li a:hover {
    text-decoration: underline
}

.slide {
    width: 100%;
    margin-bottom: 15px
}

.newIconDetail,.discountIconDetail,.cargoIconDetail {
    display: none
}

.benzerUrunlerWrapper {
    background: #efefef;
    clear: left
}

.benzerUrunlerWrapper:before,.benzerUrunlerWrapper:after {
    content: "";
    display: table
}

.benzerUrunlerWrapper:after {
    clear: both
}

#divBenzerUrun {
    position: relative;
    float: left;
    width: 100%;
    margin: 10% 0 0
}

#divBenzerUrun .JKatAdi {
    display: block;
    width: 100%;
    padding: 0!important;
    margin: 0!important;
    float: left
}

#divBenzerUrun .JKatAdi .bold {
    float: left;
    width: 100%;
    text-align: center;
    position: relative
}

#divBenzerUrun .JKatAdi .bold:after {
    content: '';
    position: absolute;
    top: 50%;
    left: 10%;
    right: 10%;
    height: 1px;
    background: #dbdbdb;
    border-bottom: 1px solid #f6f6f6;
    z-index: -1
}

#divBenzerUrun .JKatAdi .bold .satir1 {
    display: inline-block;
    font-size: 25px;
    color: #000;
    font-weight: 600;
    line-height: 48px;
    text-align: center;
    background: #fff;
    padding: 0 22px;
    text-transform: uppercase
}

#divBenzerUrun .owl-carousel {
    display: block;
    margin: 0 auto;
    max-width: 1366px;
    padding: 30px
}

#divBenzerUrun .owl-dots {
    display: none
}

#divBenzerUrun .owl-nav {
    position: absolute;
    top: 50%;
    left: 0;
    right: 0
}

#divBenzerUrun .ProductListprev {
    font-size: 0;
    display: inline-block;
    position: absolute;
    cursor: pointer;
    left: 0;
    text-align: right
}

#divBenzerUrun .ProductListnext {
    font-size: 0;
    display: inline-block;
    position: absolute;
    cursor: pointer;
    right: 0;
    text-align: left
}

#divBenzerUrun .ProductListnext:after {
    content: '\e876';
    font-family: lineariconsfree;
    font-size: 37px;
    color: gray;
    line-height: 40px;
    float: left;
    width: 100%
}

#divBenzerUrun .ProductListprev:after {
    content: '\e875';
    font-family: lineariconsfree;
    font-size: 37px;
    color: gray;
    line-height: 40px;
    float: left;
    width: 100%
}

#divIlgiliUrunler {
    float: left;
    width: 100%;
    display: none
}

.RightDetail #divIlgiliUrunler {
    display: block
}

#divIlgiliUrunler .JKatAdi {
    float: left;
    width: 100%;
    margin-bottom: 5px
}

#divIlgiliUrunler .JKatAdi .satir1 {
    font-weight: 500;
    line-height: 1;
    font-size: 13px;
    color: gray;
    text-decoration: underline
}

#divIlgiliUrunler .clear {
    display: none
}

#divIlgiliUrunler ul {
    float: left;
    width: 63%;
    overflow: hidden;
    max-height: 125px
}

#divIlgiliUrunler ul.IlgiAc {
    max-height: 100%;
    overflow: visible
}

#divIlgiliUrunler ul li {
    float: left;
    width: 80px;
    margin-right: 7px;
    height: 98px;
    margin-bottom: 27px
}

#divIlgiliUrunler ul li .productItem {
    padding: 3px;
    border-radius: 3px
}

#divIlgiliUrunler ul li .productItem .productImage {
    padding-bottom: 135%
}

#divIlgiliUrunler ul li .productItem .productImage a {
    padding-bottom: 135%
}

#divIlgiliUrunler ul li .productIcon {
    display: none!important
}

#divIlgiliUrunler ul li .urunListeAdet {
    display: none!important
}

#divIlgiliUrunler ul li .productDetail {
    display: none!important
}

#divIlgiliUrunler ul li .TukendiIco {
    height: 100%;
    display: none
}

#divIlgiliUrunler ul li .TukendiIco span {
    padding: 0;
    font-size: 12px;
    left: 0
}

#divIlgiliUrunler .productItem .productImage a:after {
    display: none!important
}

#divIlgiliUrunler .ClickIlgi {
    color: #000;
    font-size: 25px;
    float: left;
    cursor: pointer
}

#divIlgiliUrunler .ClickIlgi i {
    line-height: 40px
}

.PrintArea {
    width: 960px;
    margin: 0 auto;
    background-color: #fff;
    overflow: hidden
}

.printresim {
    width: 30%;
    height: 200px;
    float: left
}

.printdetay {
    width: 70%;
    float: left
}

.printdetay div {
    padding-top: 5px;
    padding-bottom: 5px;
    min-height: 10px
}

.printurunadi {
    font-size: 16px
}

.printfiyat {
    font-size: 16px
}

.printtaksit {
    width: 960px;
    float: left
}

.printtaksit .taksitLine {
    background-color: #fff!important
}

.printtaksit .taksitLine .taksitLineNo {
    width: 114px
}

.printtaksit .taksitLine div {
    background-color: #fff!important
}

.printkdvdahil {
    font-size: 16px
}

.firsatUrunleri {
    width: 180px;
    height: 252px;
    position: relative;
    margin: 0 auto
}

.Firsatprev {
    padding: 0;
    border: 0;
    outline: 0;
    width: 19px;
    height: 19px;
    cursor: pointer;
    position: absolute;
    top: 100px!important;
    z-index: 102
}

.Firsatnext {
    padding: 0;
    border: 0;
    outline: 0;
    width: 19px;
    height: 19px;
    cursor: pointer;
    position: absolute;
    top: 100px!important;
    z-index: 102;
    right: 0
}

.firsatUrunleriItem {
    width: 180px
}

.firsatUrunResim {
    display: block;
    width: 150px;
    height: 150px;
    border: none;
    text-align: center;
    margin: 0 auto
}

.firsatUrunResim img {
    max-width: 150px;
    max-height: 150px
}

.firsatUrunAdi {
    font-size: 12px;
    line-height: 14px;
    margin: 5px 0!important;
    overflow: hidden;
    text-align: center;
    width: 191px;
    height: 30px;
    display: block
}

.firsatUrunFiyat {
    text-align: center;
    display: block;
    font-size: 14px
}

.HesabimBilgi {
    width: 100%;
    line-height: 25px
}

.HesabimBilgi b {
    font-weight: 700
}

.userMenu {
    list-style: none;
    position: relative;
    display: inline-table;
    width: 100%;
    background-color: #fff;
    padding: 0 20px 20px 0;
    -webkit-box-sizing: border-box;
    -moz-box-sizing: border-box;
    box-sizing: border-box
}

.userMenu:before {
    content: "KULLANICI PANEL";
    display: block;
    color: #000;
    font-size: 14px;
    padding: 10px 5px;
    font-weight: 700
}

.userMenu li {
    display: block;
    position: relative;
    margin-bottom: 0;
    float: left;
    width: 100%;
    color: #000;
    font-size: 13px
}

.userMenu li a {
    display: block;
    font-size: 13px;
    padding: 6px 15px 6px 5px;
    color: #000
}

.userMenu li:hover a {
    color: #000
}

.uyelikBilgilerimRow.row {
    width: 100%
}

.vital-stats .item {
    width: auto!important
}

.row.right {
    float: right
}

.span {
    width: 100%;
    margin-bottom: 10px;
    position: relative;
    display: block;
    float: left
}

.span>label {
    margin-bottom: 5px;
    display: block;
    line-height: 25px;
    clear: left;
    position: relative
}

.span>label .validate {
    top: 0
}

.span input {
    width: 100%
}

.span .textarea {
    width: 97%;
    margin-bottom: 4px
}

.span .labelGender {
    float: left
}

.span .spanGender {
    float: left;
    margin-left: 10px;
    text-align: center
}

.span .spanGender input {
    margin-right: 20px
}

.span .spanPass {
    text-align: left;
    margin-top: 10px
}

.span .spanPass input {
    float: left;
    width: auto;
    margin-right: 10px
}

.span .spanPass label {
    float: left;
    width: auto;
    color: red
}

.dateofbirth input {
    border: 1px solid #e7e7e7!important;
    height: 25px!important
}

.HesabimAdresContent {
    margin-bottom: 15px
}

.HesabimAdresContent .row {
    padding: 2%;
    width: 49%;
    margin: 0;
    margin-right: 2%;
    margin-bottom: 2%;
    min-height: 170px;
    float: left;
    background-color: #fff;
    position: relative
}

.AdresItemLineW .row {
    width: 100%;
    padding: 0;
    margin-right: 0
}

.HesabimAdresContent .row:nth-child(2n) {
    margin-right: 0
}

.HesabimAdresContent .UyelikBilgilerimContent {
    overflow: hidden;
    background-color: #fff;
    padding: 0 10px 10px 0;
    margin: 50px 0
}

.HesabimAdresContent .UyelikBilgilerimContent .row {
    background-color: transparent;
    height: auto
}

.HesabimAdresContent .row .span {
    margin-bottom: 0;
    line-height: 20px
}

.HesabimAdresContent .row .span .textarea {
    background-color: #fff
}

.HesabimAdresContent .row .span.BireyselKurumsal {
    margin-top: 22px;
    margin-bottom: 17px
}

#mainHolder_rblFaturaTipi tr {
    display: block;
    float: left;
    margin-right: 10px
}

#mainHolder_rblFaturaTipi tr input {
    float: left;
    width: 20px;
    margin-top: 3px
}

#mainHolder_rblFaturaTipi tr label {
    float: left
}

#mainHolder_btnEkle {
    position: absolute;
    top: 50%;
    left: 50%;
    margin-top: -20px;
    margin-left: -30px
}

.fancybox-inner .row {
    padding: 2%;
    width: 45.5%;
    margin-right: 1%;
    margin-bottom: 1%;
    height: 130px;
    float: left;
    background-color: #f8f8f8;
    position: relative
}

.fancybox-inner .UyelikBilgilerimContent {
    overflow: hidden;
    margin-bottom: 7px;
    background-color: #f8f8f8;
    padding: 0 10px 10px 0
}

.fancybox-inner .UyelikBilgilerimContent .row {
    background-color: transparent;
    height: auto
}

.fancybox-inner .UyelikBilgilerimContent input {
    background-color: #fff
}

.fancybox-inner .row:nth-child(2n) {
    margin-right: 0
}

.fancybox-inner .row .span {
    margin-bottom: 0;
    line-height: 20px
}

.fancybox-inner .row .span .textarea {
    background-color: #fff
}

.fancybox-inner .row .span.BireyselKurumsal {
    margin-top: 22px;
    margin-bottom: 17px
}

#rblFaturaTipi tr {
    display: block;
    float: left;
    margin-right: 10px
}

#rblFaturaTipi tr input {
    float: left;
    width: 20px;
    margin-top: 3px
}

#rblFaturaTipi tr label {
    float: left
}

.btn-inverse {
    position: absolute;
    bottom: 10px;
    right: 10px;
    padding-top: 3px;
    padding-bottom: 3px
}

.btn-inverse2 {
    position: absolute;
    bottom: 10px;
    right: 50px;
    padding-top: 3px;
    padding-bottom: 3px
}

.Listem {
    width: 100%;
    margin-top: 15px
}

.Listem .ListemItem {
    width: 100%;
    height: 50px;
    overflow: hidden;
    border-bottom: solid 1px #ccc
}

.Listem .ListemItem.Title {
    background-color: #f5f5f5;
    height: 30px;
    border-bottom: solid 1px #ccc;
    line-height: 30px
}

.Listem .ListemItem div {
    float: left;
    height: 40px;
    padding-top: 5px;
    padding-bottom: 5px;
    overflow: hidden
}

.Listem .ListemItem .line1 {
    width: 9%;
    padding-left: 1%
}

.Listem .ListemItem .line1 img {
    max-width: 100%;
    max-height: 60px
}

.Listem .ListemItem .line2 {
    width: 51%;
    padding-left: 1%
}

.Listem .ListemItem .line3 {
    width: 20%;
    padding-left: 1%
}

.Listem .ListemItem .line4 {
    width: 17%
}

.Listem .ListemItem .line4 a {
    margin-top: 5px
}

.Listem.HediyeKuponlarim .ListemItem .line1 {
    width: 22%
}

.Listem.HediyeKuponlarim .ListemItem .line2 {
    width: 21%
}

.Listem.HediyeKuponlarim .ListemItem .line3 {
    width: 16%
}

.Listem.HediyeKuponlarim .ListemItem .line4 {
    width: 16%;
    padding-left: 1%
}

.Listem.HediyeKuponlarim .ListemItem .line5 {
    width: 20%;
    padding-left: 1%
}

#destekIncele .ListemItem div {
    min-height: 50px;
    border-bottom: solid 1px #ccc;
    margin-bottom: 10px
}

#destekIncele .ListemItem div span {
    font-weight: 700
}

.Siparislerim {
    margin-bottom: 10px
}

.Siparislerim .Title div {
    font-weight: 700;
    font-size: 13px
}

.Siparislerim .ListemItem.Title div {
    padding: 0;
    height: auto
}

.Siparislerim .ListemItem {
    border-top: 0 solid #ccc;
    height: 35px;
    line-height: 35px
}

.Siparislerim .ListemItem div {
    font-size: 12px;
    padding: 0!important
}

.Siparislerim .ListemItem .line1 {
    width: 20%;
    padding-left: 1%;
    text-align: center
}

.Siparislerim .ListemItem .line2 {
    width: 17%;
    text-align: center
}

.Siparislerim .ListemItem .line3 {
    width: 13%;
    padding-left: 1%;
    text-align: center
}

.Siparislerim .ListemItem .line4 {
    width: 16%;
    padding-left: 1%;
    text-align: center
}

.Siparislerim .ListemItem .line5 {
    width: 17%;
    text-align: center
}

.Siparislerim .ListemItem .line6 {
    width: 17%;
    text-align: center
}

.Siparislerim .ListemItem .line6 a {
    color: red;
    text-decoration: underline
}

.paraPuan>div {
    padding: 10px
}

.paraPuan+a {
    padding: 10px
}

.paraPuan .parapuanTable {
    width: 98%;
    overflow: hidden;
    border-bottom: solid 1px #ccc;
    padding: 1%;
    margin-bottom: -1px
}

.paraPuan .parapuanTable.Title {
    padding: 0;
    padding-left: 1%;
    width: 99%;
    background-color: #f5f5f5
}

.paraPuan .parapuanTable .paraline1 {
    width: 18%;
    float: left;
    padding: 1%
}

.paraPuan .parapuanTable .paraline2 {
    width: 58%;
    float: left;
    padding: 1%
}

.paraPuan .parapuanTable .paraline3 {
    width: 18%;
    float: left;
    padding: 1%;
    text-align: center
}

.DestekTalepDetay {
    width: 97.7%;
    border: 1px solid #e7e7e7;
    margin: 5px 0;
    padding: 1%
}

.DestekTalepCevapLine {
    background-color: #f5f5f5;
    margin: 5px 0;
    padding: 5px;
    border: 1px solid #e7e7e7
}

.DestekTalepDetay .span {
    overflow: hidden
}

.DestekTalepCevapLine:nth-child(2n+1) {
    background-color: #fff;
    margin: 5px 0;
    padding: 5px
}

.DestekTaleplerim .Title {
    height: 40px;
    line-height: 40px
}

.Listem.DestekTaleplerim .ListemItem .line1 {
    width: 3%
}

.Listem.DestekTaleplerim .ListemItem .line2 {
    width: 10%
}

.Listem.DestekTaleplerim .ListemItem .line3 {
    width: 50%
}

.Listem.DestekTaleplerim .ListemItem .line4 {
    width: 12%
}

.Listem.DestekTaleplerim .ListemItem .line5 {
    width: 11%
}

.Listem.DestekTaleplerim .ListemItem .line6 {
    width: 11%
}

.Listem.DestekTaleplerim .ListemItem .line6.DestekButton .button {
    float: right;
    margin-top: 5px
}

.YeniDestek {
    width: 100%;
    height: 60px;
    position: relative
}

.DestekTaleplerimContent #mainHolder_btnEkle {
    position: static;
    float: right;
    margin: 0;
    margin-top: 10px;
    margin-bottom: 20px
}

.DestekTaleplerimContent .row .span {
    position: relative;
    height: 40px;
    overflow: visible
}

.DestekTaleplerimContent .row .span div {
    float: left;
    height: 31px;
    line-height: 31px
}

.DestekTaleplerimContent .row .span .Left {
    width: 10%
}

.DestekTaleplerimContent .row .span .Center {
    width: 3%
}

.DestekTaleplerimContent .row .span .Right {
    width: 86%
}

.DestekTaleplerimContent .row .span #mainHolder_btnKaydet {
    float: right;
    width: 20%
}

.DestekTaleplerimContent .row .span #mainHolder_btnVazgec {
    float: right;
    width: 20%;
    margin-right: 10px
}

.DestekTaleplerimContent textarea {
    width: 98.8%;
    margin-bottom: 10px
}

.DestekTalepDetay .span div {
    float: left
}

.anketSoru {
    margin-bottom: 5px;
    display: block
}

.anketLabel td {
    line-height: 21px;
    display: block
}

.anketLabel label {
    margin-left: 5px
}

.iletisimContent {
    float: left
}

.iletisimLine {
    margin-bottom: 10px;
    min-height: 30px;
    line-height: 30px;
    position: relative
}

.iletisimLine .Left {
    display: inline-block;
    width: 20%;
    
}

.iletisimLine .Center {
    display: inline-block;
    width: 2%;
    
}

.iletisimLine .Right {
    display: inline-block;
    width: 40%;
    
}

.iletisimbanka {
    width: 100%;
    padding: 1%;
    border: solid 1px #dadada;
    background-color: #fff;
    overflow: hidden
}

.iletisimContent .row {
    width: 49%;
    float: left;
    border: solid 1px #ccc;
    padding: 1%;
    min-height: 303px;
    margin: 0
}

.iletisimContent .categoryTitle {
    border-bottom: solid 7px #e4e4e4;
    margin-bottom: 35px
}

.iletisimContent .row .span {
    margin-left: 2%;
    margin-right: 2%;
    padding: 0;
    width: 96%;
    overflow: hidden
}

.iletisimContent .row>.span>div {
    float: left;
    min-height: 30px;
    line-height: 30px;
    width: 20%
}

.iletisimContent .row .span .Center {
    width: 2%
}

.iletisimContent .row .span .Right {
    width: 78%
}

.iletisimContent .row .span .line1 {
    width: 100%;
    min-height: 50px;
    margin-bottom: 5px
}

.iletisimContent .row .span>.line1 {
    border-bottom: solid 1px #ccc
}

.iletisimContent .row .span .line1 div {
    width: 41%;
    float: left;
    min-height: 50px
}

.iletisimContent .row .span .line1 .line2 {
    text-align: center;
    width: 23%
}

.iletisimContent .row .span .line1 .line3 {
    text-align: center;
    width: 16%
}

.iletisimContent .row .span .line1 .line4 {
    text-align: right;
    float: right;
    width: 20%
}

.iletisimContent .row .span .line1 div span {
    display: block;
    min-height: 25px
}

.iletisimContent .row .span .line2 {
    width: 100%;
    min-height: 25px
}

.iletisimContent .row .span>.line2 {
    border-bottom: solid 1px #ccc
}

.iletisimContent .row .span .line2 .line1 {
    width: 70%;
    float: left;
    line-height: 25px
}

.iletisimContent .row .span .line2 .line2 {
    float: right;
    width: 30%;
    text-align: right
}

.iletisimContent .row .span .line3 {
    width: 100%
}

.iletisimContent .row .span .line3 .line1 {
    width: 100%
}

.iletisimContent .row .span .line3 .line1 span {
    float: left
}

.iletisimForm {
    width: 98%;
    margin-top: 20px;
    border: solid 1px #dadada;
    overflow: hidden;
    padding: 1%
}

.iletisimForm .row {
    width: 50%;
    border: none;
    float: left;
    padding: 0
}

.iletisimForm .row .span {
    height: 70px;
    position: relative;
    overflow: visible;
    margin-bottom: 0
}

.iletisimForm .row .span .captchaImageBox {
    float: left;
    width: 30%
}

.iletisimForm .row .span .captchaInputBox {
    width: 69%
}

#mainHolder_TiciCaptcha_ImgCaptcha {
    width: 100px
}

.iletisimForm .row .span .captchaInputBox input {
    float: left
}

.iletisimForm .row .span #mainHolder_btnGonder {
    width: 160px;
    float: right
}

.iletisimForm .textarea {
    height: 110px
}

.newuserForm {
    background: #fff;
    color: #000;
    font-size: 13px;
    line-height: 30px;
    width: 98%;
    margin: 1%;
    margin-bottom: 20px;
    overflow: hidden
}

.FormTitle {
    width: 100%;
    text-align: center;
    font-size: 30px;
    line-height: 50px;
    color: #000
}

.FormTitle p {
    font-size: 14px;
    margin: 0 auto;
    line-height: 22px;
    display: block;
    width: 50%
}

.grid {
    border-right: 1px solid #e7e7e7;
    float: left;
    margin-right: -1%;
    margin-top: 2%;
    margin-bottom: 2%;
    padding: 2% 11% 5%;
    width: 50%
}

.gridLeft {
    min-height: 60px;
    position: relative
}

.gridLeft a {
    text-decoration: underline
}

.gridLeft input[type=checkbox] {
    float: left;
    margin-top: 9px;
    margin-right: 5px
}

.listAdd {
    min-height: 30px
}

.day {
    width: 25%;
    float: left;
    margin-right: 1%
}

.city {
    width: 32.3%;
    float: left;
    margin-right: 1%
}

.month {
    width: 30%;
    float: left;
    margin-right: 1%
}

.year {
    width: 42%;
    float: left;
    margin-right: 1%
}

.gender {
    min-height: 40px
}

.gender label {
    float: left;
    width: 70px;
    margin-top: 10px;
    display: block
}

.gender input {
    float: left;
    margin-top: 18px;
    margin-right: 3px
}

.uyeolButton {
    width: 100%
}

.Login {
    border: solid 1px #e7e7e7;
    padding: 2% 5% 2% 4%;
    width: 100%;
    background-color: #fbfbfb;
    height: 260px
}

.Login h4 {
    font-size: 22px;
    display: block;
    text-align: center;
    border-bottom: solid 1px #ccc;
    margin-bottom: 10px
}

.forgetpasword {
    text-decoration: none;
    float: right;
    color: #000
}

.userloginButton {
    width: 80px;
    margin-top: 10px
}

.facebooklogin {
    margin-top: 40px;
    display: block;
    float: left
}

.grid .validate,.validateSol,.validateOrta {
    top: -7px
}

.gridLeft .validateSol {
    left: -.5%;
    top: -30px
}

.gridLeft .validateSol .validateSolOk {
    border-radius: 0 0 15px;
    bottom: -5px;
    left: 10px
}

.gender table {
    float: left
}

.doFaceBookLogin {
    color: #fff;
    background-color: #3b5998;
    border-color: rgba(0,0,0,.2);
    padding: 10px 20px;
    width: 82%;
    cursor: pointer;
    font-size: 15px;
    line-height: 1.33;
    border-radius: 6px;
    text-align: center;
    margin-top: 5px;
    display: inline-block
}

.uyeliksiz {
    padding: 2%;
    width: 100%;
    display: block;
    text-align: center;
    font-size: 14px;
    border-radius: 5px;
    background-color: #a4c942;
    color: #fff;
    margin-bottom: 10px
}

.hizliuyelik {
    padding: 2%;
    width: 100%;
    display: block;
    text-align: center;
    font-size: 14px;
    border-radius: 5px;
    background-color: #a4c942;
    color: #fff;
    margin-bottom: 10px
}

.baglanButton {
    padding: 1%;
    width: 100%;
    display: block;
    text-align: center;
    font-size: 14px;
    border-radius: 5px;
    background-color: #d34848;
    border: 2px solid #d34848;
    color: #fff;
    margin-bottom: 10px
}

.baglanButton:hover {
    background-color: transparent;
    color: #d34848
}

.baglanButton input {
    border: none;
    width: 100%;
    height: 100%;
    display: block;
    background-color: transparent;
    cursor: pointer;
    text-indent: -9999px
}

.headerSocialConnect #SocialLogin_divFacebookLoginContainer input#SocialLogin_btnFaceLogin {
    font-size: 12px;
    color: #2b529b;
    text-transform: uppercase
}

#mainHolder_SocialLogin_divFacebookLoginContainer.baglanButton {
    text-indent: -9999pt
}

#mainHolder_SocialLogin_divTwitterLoginContainer.baglanButton {
    text-indent: -9999pt
}

#mainHolder_SocialLogin_divGoogleLoginContainer.baglanButton {
    text-indent: -9999pt
}

.SifremiUnuttum {
    width: 100%;
    margin: 30px 0;
    padding-left: 50px;
    float: left
}

.SifremiUnuttum p {
    line-height: 25px
}

.SifremiUnuttum #mainHolder_txtbxMail {
    width: 80%;
    height: 40px;
    float: left;
    line-height: 40px;
    padding: 0 20px
}

.SifremiUnuttum .button {
    padding: 0 10px;
    float: right;
    width: 20%;
    height: 40px
}

.SifremiUnuttumInput {
    position: relative;
    width: 150%;
    margin-top: 10px;
    border: 1px solid #9e9e9e;
    padding: 33px 5px;
    margin-left: 16.5px
}

.SifremiUnuttumInput .validate {
    left: auto;
    right: 0;
    top: -38px
}

.SifremiUnuttumInput .validateSol {
    left: 0;
    right: auto;
    top: -38px
}

.SifremiUnuttumInput .validateSol .validateSolOk {
    border-radius: 0 0 15px;
    bottom: -5px;
    left: 10px
}

.SifremiUnuttum .line {
    min-height: 32px;
    line-height: 32px;
    width: 400px;
    position: relative;
    margin: 0 auto
}

.SifremiUnuttum .line .Left {
    width: 30%;
    float: left
}

.SifremiUnuttum .line .Center {
    width: 4%;
    float: left
}

.SifremiUnuttum .line .Right {
    width: 66%;
    float: left
}

.tabListe {
    float: left;
    width: 100%
}

.tabListe .tabUst {
    float: left;
    width: 100%;
    margin-bottom: 20px
}

.tabListe .tabUst ul {
    float: left;
    width: 100%
}

.tabListe .tabUst ul li {
    
    display: inline-block;
    width: 20%;
    border-right: 1px solid #f2f2f2
}

.tabListe .tabUst ul li a {
    display: block;
    text-align: center;
    color: #fff;
    background: #000;
    font-size: 14px;
    font-weight: 700;
    line-height: 38px
}

.tabListe .tabUst ul li:hover a {
    background: #ed1f24;
    color: #fff
}

.tabListe .tabUst ul li.aktif a {
    background: #ed1f24;
    color: #fff
}

.tabListe .tabIcerik {
    float: left;
    width: 100%
}

.tabListe .tabIcerik .blok {
    float: left;
    width: 100%;
    display: none
}

.tabListe .tabIcerik .blok:first-child {
    display: block
}

.tabListe .categoryTitle {
    display: none
}

.tabListe .Jbutonlar {
    display: none
}

.tabListe .categoryTitle {
    display: none
}

.tabListe .productItem .productOnYazi {
    display: none!important
}

.taksitBlok {
    width: 25%;
    height: auto;
    float: left;
    line-height: 20px
}

.taksitBaslik {
    width: 100%;
    height: 20px;
    text-align: center
}

.taksitBaslik img {
    display: none
}

.taksitLine {
    width: 101%
}

.taksitLine .tak {
    width: 39.1%;
    height: 20px;
    overflow: hidden;
    border-bottom: solid 1px #fff;
    border-right: solid 1px #fff;
    font-size: 10px;
    float: left;
    color: #000;
    text-align: center
}

.taksitLine .tak.Taksit {
    background-color: #ededed;
    width: 19%
}



.TakRenk1 {
    background-color: #edf4e6
}

.TakRenk2 {
    background-color: #f1e7f3
}

.TakRenk3 {
    background-color: #f5f9d9
}

.TakRenk4 {
    background-color: #eeafa2
}

.TakRenk5 {
    background-color: #b5d0df
}

.TakRenk6 {
    background-color: #e4e9f4
}

.TakRenk7 {
    background-color: #edf4e6
}

.TakRenk8 {
    background-color: #f1e7f3
}

.TakRenk9 {
    background-color: #f5f9d9
}

.TakRenk10 {
    background-color: #eeafa2
}

.TakRenk11 {
    background-color: #b5d0df
}

.TakRenk12 {
    background-color: #e4e9f4
}

.TakRenk13 {
    background-color: #edf4e6
}

.TakRenk14 {
    background-color: #f1e7f3
}

.TakRenk15 {
    background-color: #f5f9d9
}

.TakRenk16 {
    background-color: #eeafa2
}

.TakRenk17 {
    background-color: #b5d0df
}

.TakRenk18 {
    background-color: #e4e9f4
}

.TakRenk19 {
    background-color: #edf4e6
}

.CariOdeme .row .span {
    overflow: hidden
}

.CariOdeme .row .span .Left {
    width: 13%
}

.CariOdeme .row .span .Center {
    width: 3%
}

.CariOdeme .row .span .Right {
    width: 82%
}

.CariOdeme .row .span div {
    float: left;
    height: 31px;
    line-height: 31px
}

.Listem.CariOdemeRaporlari .ListemItem .line1 {
    width: 6%
}

.Listem.CariOdemeRaporlari .ListemItem .line2 {
    width: 13%
}

.Listem.CariOdemeRaporlari .ListemItem .line3 {
    width: 18%
}

.Listem.CariOdemeRaporlari .ListemItem .line4 {
    width: 8%;
    padding-left: 1%
}

.Listem.CariOdemeRaporlari .ListemItem .line5 {
    width: 18%;
    padding-left: 1%
}

.Listem.CariOdemeRaporlari .ListemItem .line6 {
    width: 12%;
    padding-left: 1%
}

.Listem.CariOdemeRaporlari .ListemItem .line7 {
    width: 10%;
    padding-left: 1%
}

.Listem.CariOdemeRaporlari .ListemItem .line8 {
    width: 7%;
    padding-left: 1%
}

.CariOdeme .Basketstep {
    display: none
}

.CariOdeme .OdemeMenu {
    display: none
}

.CariOdeme .BasketPage {
    width: 100%;
    overflow: visible;
    padding: 0;
    border: 0;
    min-height: inherit
}

.CariOdeme .Odeme-Left {
    width: 100%;
    padding: 0;
    float: none;
    background-color: transparent;
    min-height: 300px
}

.CariOdeme .Odeme-Left .Left {
    width: 50%
}

.CariOdeme .CrediCardNoInput input {
    width: 20.3%
}

.CariOdeme .CrediCardNameInput input {
    width: 92%
}

.CariOdeme .CrediCardDateInput select {
    width: 46.7%
}

.CariOdeme .Odeme-Right {
    padding: 0;
    float: none;
    width: 100%;
    background-color: transparent
}

.CariOdeme .Odeme-Right .Odeme-RightLine {
    display: none
}

.CariOdeme .aspNetDisabled {
    margin-top: 5px
}

.CariOdeme .OdemeTamamla .SiparisiTamamlaBtn {
    float: right;
    margin-top: 50px
}

.CariRaporlarContent .siparisTablo thead tr th {
    padding: 2px
}

.cariorta table tr td {
    padding: 5px
}

div#fancy_print {
    border: 2px solid #fff;
    border-radius: 13px;
    cursor: pointer;
    display: block;
    height: 25px;
    left: -16px;
    position: absolute;
    top: -14px;
    width: 25px;
    z-index: 9999
}

.CariOdeme .Odeme-Right {
    position: relative
}

.CariOdeme .OdemeTamamla {
    position: absolute;
    bottom: 0
}

.fancyboxTittle {
    margin-bottom: 10px;
    font-size: 13px
}

.urunTabAlt #yorumYaz {
    margin: 0 auto;
    float: left
}

.yorumYaz {
    margin-bottom: 10px;
    position: relative
}

.yorumYaz .validate {
    padding: 5px;
    top: -30px
}

.yorumYazMesaj textarea {
    width: 100%
}

.urunYorumYok {
    float: left;
    width: 100%
}

.urunTabAlt {
    width: 100%
}

.urunTabAlt ul li {
    margin-bottom: 10px;
    clear: both
}

.oneriValidate .validate {
    top: 0;
    padding: 5px
}

.urunTabAlt ul li input {
    float: left;
    margin-right: 5px
}

.urunTabAlt ul li .captchaImageBox {
    float: left
}

.urunTabAlt ul li .captchaInputBox {
    margin: 10px;
    float: left
}

.urunTabAlt ul li.urundetyaGuvenlikodu span {
    float: left
}

.urunTabAlt ul li .GuvnelikKodu {
    float: left;
    line-height: 50px;
    margin-right: 10px;
    display: block
}

.odemeBildirimFormu table tr td {
    padding: 5px
}

#mainHolder_txtbxNotlar {
    width: 100%
}

.Block_Text img {
    max-width: 100%
}

#GUVENLIK_KODU {
    margin-bottom: 10px;
    margin-top: 10px
}

.tooltip {
    position: absolute;
    z-index: 1030;
    display: block;
    font-size: 12px;
    line-height: 1.4;
    opacity: 0;
    filter: alpha(opacity=0);
    visibility: visible
}

.tooltip.in {
    opacity: .9;
    filter: alpha(opacity=90)
}

.tooltip.top {
    padding: 5px 0;
    margin-top: -3px
}

.tooltip.right {
    padding: 0 5px;
    margin-left: 3px
}

.tooltip.bottom {
    padding: 5px 0;
    margin-top: 3px
}

.tooltip.left {
    padding: 0 5px;
    margin-left: -3px
}

.tooltip-inner {
    max-width: 200px;
    padding: 3px 8px;
    color: #fff;
    text-align: center;
    text-decoration: none;
    background-color: #000;
    border-radius: 4px
}

.tooltip-arrow {
    position: absolute;
    width: 0;
    height: 0;
    border-color: transparent;
    border-style: solid
}

.tooltip.top .tooltip-arrow {
    bottom: 0;
    left: 50%;
    margin-left: -5px;
    border-top-color: #000;
    border-width: 5px 5px 0
}

.tooltip.top-left .tooltip-arrow {
    bottom: 0;
    left: 5px;
    border-top-color: #000;
    border-width: 5px 5px 0
}

.tooltip.top-right .tooltip-arrow {
    right: 5px;
    bottom: 0;
    border-top-color: #000;
    border-width: 5px 5px 0
}

.tooltip.right .tooltip-arrow {
    top: 50%;
    left: 0;
    margin-top: -5px;
    border-right-color: #000;
    border-width: 5px 5px 5px 0
}

.tooltip.left .tooltip-arrow {
    top: 50%;
    right: 0;
    margin-top: -5px;
    border-left-color: #000;
    border-width: 5px 0 5px 5px
}

.tooltip.bottom .tooltip-arrow {
    top: 0;
    left: 50%;
    margin-left: -5px;
    border-bottom-color: #000;
    border-width: 0 5px 5px
}

.tooltip.bottom-left .tooltip-arrow {
    top: 0;
    left: 5px;
    border-bottom-color: #000;
    border-width: 0 5px 5px
}

.tooltip.bottom-right .tooltip-arrow {
    top: 0;
    right: 5px;
    border-bottom-color: #000;
    border-width: 0 5px 5px
}

.uyelikonay {
    margin-top: 50px;
    padding-left: 50px
}

.uyelikonay .title {
    width: 100%;
    margin-bottom: 30px
}

.uyelikonay .title h4 {
    font-size: 30px;
    margin-bottom: 20px
}

.uyelikonay .title span {
    font-size: 20px
}

.uyelikonay p {
    line-height: 30px
}

.uyelikonay p strong {
    font-weight: 700;
    font-size: 16px;
    color: #000
}

.uyelikonay a {
    font-size: 14px;
    padding-left: 30px;
    padding-right: 30px;
    margin-bottom: 30px
}

.IadeTaleplerim .Title {
    height: 40px;
    line-height: 40px
}

.Listem.IadeTaleplerim .ListemItem {
    height: auto;
    line-height: 24px
}

.Listem.IadeTaleplerim .ListemItem div {
    height: auto
}

.Listem.IadeTaleplerim .ListemItem .line1 {
    width: 3%
}

.Listem.IadeTaleplerim .ListemItem .line2 {
    width: 20%
}

.Listem.IadeTaleplerim .ListemItem .line3 {
    width: 40%
}

.Listem.IadeTaleplerim .ListemItem .line4 {
    width: 30%
}

.Listem.IadeTaleplerim .ListemItem .line5 {
    width: 11%
}

.Listem.IadeTaleplerim .ListemItem .line6 {
    width: 11%
}

.IadeTaleplerimContent #mainHolder_btnEkle {
    position: static;
    float: right;
    margin: 0;
    margin-top: 10px;
    margin-bottom: 20px
}

.IadeTaleplerimContent .row {
    width: 60%
}

.IadeTaleplerimContent .row .span {
    position: relative;
    overflow: hidden;
    margin-bottom: 5px
}

.IadeTaleplerimContent .row .span div {
    float: left
}

.IadeTaleplerimContent .row .span .Left {
    width: 30%
}

.IadeTaleplerimContent .row .span .Center {
    width: 3%
}

.IadeTaleplerimContent .row .span .Right {
    width: 60%
}

.IadeTaleplerimContent .row .span #mainHolder_btnKaydet {
    float: right;
    width: 20%
}

.IadeTaleplerimContent .row .span #mainHolder_btnVazgec {
    float: right;
    width: 20%;
    margin-right: 10px
}

.IadeTaleplerimContent textarea {
    width: 98.8%;
    margin-bottom: 10px;
    height: 50px
}

.span.IadeTalepBtn {
    width: 93%
}

#ArmaSonuclari {
    width: 100%;
    border: solid 1px #ccc;
    padding: 3%;
    text-align: center;
    font-size: 19px;
    background-color: #fff
}

.Block_Title {
    display: none
}

.OzelBlokIcerik {
    padding: 0
}

.OzelBlokIcerik .Block_Text {
    padding: 0
}

.kampanyaliBolum {
    overflow: hidden
}

.ucluBlokRow {
    margin: 0 -10px
}

.kampanyaliBolum .ucluBlok {
    float: left;
    width: 33.333333%;
    padding: 0 10px;
    margin-bottom: 20px
}

.kampanyaliBolum .ucluBlok .resimTutucu {
    overflow: hidden
}

.kampanyaliBolum .ucluBlok a {
    overflow: hidden;
    display: block;
    transition: .3s;
    -moz-transition: .3s;
    -webkit-transition: .3s;
    -ms-transition: .3s
}

.kampanyaliBolum .ucluBlok a span {
    display: block;
    padding: 10px;
    color: #46696b;
    font-size: 18px
}

.kampanyaliBolum .ucluBlok a img {
    display: block;
    width: 100%;
    transition: .3s;
    -moz-transition: .3s;
    -webkit-transition: .3s;
    -ms-transition: .3s
}

.kampanyaliBolum .ucluBlok a:hover img {
    transition: .5s;
    -moz-transition: .5s;
    -webkit-transition: .5s;
    -ms-transition: .5s;
    transform: scale(1.2);
    -ms-transform: scale(1.2);
    -moz-transform: scale(1.2);
    -webkit-transform: scale(1.2);
    -o-transform: scale(1.2)
}

.kampanyaliBolum .tekliBlok {
    float: left;
    width: 100%;
    margin-bottom: 20px
}

.anaKampanyaTutucu {
    float: left;
    width: 100%;
    position: relative
}

.anaKampanyaTutucu .anaKampanya {
    float: left;
    width: 100%;
    border: 1px solid #e7e7e7;
    height: 80px;
    width: 100%;
    display: block;
    position: relative;
    transition: .5s;
    -moz-transition: .5s;
    -webkit-transition: .5s;
    -ms-transition: .5s
}

.anaKampanyaTutucu .anaKampanya span {
    display: block;
    text-align: center;
    line-height: 80px
}

.anaKampanyaTutucu .anaKampanya:after {
    content: '';
    position: absolute;
    width: 40px;
    height: 24px;
    left: 20%;
    bottom: -1px;
    transition: 1.5s;
    -moz-transition: 1.5s;
    -webkit-transition: 1.5s;
    -ms-transition: 1.5s
}

.anaKampanyaTutucu .anaKampanya:hover {
    border-color: #c89841;
    transition: .5s;
    -moz-transition: .5s;
    -webkit-transition: .5s;
    -ms-transition: .5s
}

.anaKampanyaTutucu .anaKampanya:hover:after {
    left: 80%;
    transition: 1.5s;
    -moz-transition: 1.5s;
    -webkit-transition: 1.5s;
    -ms-transition: 1.5s
}

.anaKampanyaTutucu .anaKampanyaKapat {
    position: absolute;
    z-index: 2;
    right: 40px;
    top: 50%;
    margin-top: -8px;
    font-size: 16px;
    color: #000
}

.anaKampanyaTutucu .anaKampanyaKapat:hover {
    color: #c89841
}

.ticiTab {
    float: left;
    width: 100%;
    margin-bottom: 30px;
    margin-top: 20px
}

.ticiTab .tabLink {
    float: left;
    width: 100%;
    text-align: center;
    margin-bottom: 38px
}

.ticiTab .tabLink ul li {
    display: inline-block;
    margin: 0 20px
}

.ticiTab .tabLink ul li a {
    display: inline-block;
    font-size: 15px;
    color: #000;
    position: relative;
    padding-bottom: 12px
}

.ticiTab .tabLink ul li a:after {
    content: '';
    bottom: 0;
    position: absolute;
    width: 0;
    left: 50%;
    margin-left: -25%;
    height: 2px;
    background: #000;
    transition: .3s;
    -moz-transition: .3s;
    -webkit-transition: .3s;
    -ms-transition: .3s
}

.ticiTab .tabLink ul li.active a:after {
    width: 50%;
    transition: .3s;
    -moz-transition: .3s;
    -webkit-transition: .3s;
    -ms-transition: .3s
}

.ticiTab .tabIcerik {
    display: none;
    float: left;
    width: 100%
}

.ticiTab .tabIcerik ul {
    margin: 0 -10px
}

.ticiTab .tabIcerik ul li {
    padding: 0 10px;
    float: left;
    width: 20%
}

.SepetBlock {
    float: left;
    width: 100%;
    background: #fff;
    position: relative;
    margin-bottom: 20px
}

.SepetBlock .Block_Title {
    float: left;
    width: 100%;
    padding: 10px
}

.SepetBlock .Block_Title img {
    max-width: 100%;
    display: block;
    margin: 0 auto
}

.SepetBlockInfo {
    float: left;
    width: 100%;
    text-align: left;
    overflow-y: auto;
    max-height: 450px
}

.SepetBlockInfo::-webkit-scrollbar {
    width: 4px
}

.SepetBlockInfo::-webkit-scrollbar-track {
    background: #f6f6f6
}

.SepetBlockInfo::-webkit-scrollbar-thumb {
    background: #dbdbdb;
    border-radius: 0
}

.SepetBlockInfo table {
    border-collapse: collapse;
    width: 100%
}

.SepetBlockImg {
    width: 30%;
    float: left
}

.SepetBlockName {
    width: 70%;
    float: left
}

.SepetBlockInfo tr {
    border-bottom: 1px dashed #d5d4d3;
    float: left;
    width: 100%;
    padding: 10px 5px;
    position: relative
}

.SepetBlockInfo tr td {
    padding: 3px
}

.SepetBlockInfo .SepetBlockImg img {
    border: 1px solid #eceaea;
    width: 50px;
    height: 50px;
    display: inline-block
}

.SepetBlockInfo .SepetBlockName a {
    display: block;
    color: #666;
    font-size: 12px
}

.SepetBlockInfo .SepetBlockName a span {
    display: block
}

.SepetBlockInfo .SepetBlockName a span:nth-child(2) {
    display: none
}

.SepetBlockInfo .SepetBlockAdet {
    text-align: right;
    color: #666;
    font-size: 10px;
    line-height: 20px
}

.SepetBlockInfo td.SepetBlockTotal {
    text-align: right;
    color: #000;
    font-size: 11px
}

.SepetBlockInfo .SepetBlockRemove a {
    display: inline-block;
    width: 13px;
    height: 10px;
    line-height: 10px;
    text-align: center;
    background: #f39c12;
    color: #fff;
    font-size: 9px;
    cursor: pointer;
    position: absolute;
    top: 5px;
    right: 5px
}

.SepetBlockInfo .SepetBlockRemove a:hover {
    background: #f22a18
}

.SepetBlockGenelTotal {
    float: left;
    width: 100%;
    margin: 10px 0;
    text-align: center
}

.SepetBlockGenelTotal table {
    width: 100%;
    border-collapse: collapse
}

.SepetBlockGenelTotal tr:nth-child(1),.SepetBlockGenelTotal tr:nth-child(2),.SepetBlockGenelTotal tr:nth-child(3) {
    display: none
}

.SepetBlockGenelTotal tr {
    background: #eeece9
}

.SepetBlockGenelTotal tr td {
    text-align: left!important;
    padding: 9px 0
}

.SepetBlockGenelTotal tr td:nth-child(1) {
    color: #515151;
    font-size: 16px;
    font-weight: 700!important;
    text-align: right!important
}

.SepetBlockGenelTotal tr td:nth-child(1) b {
    color: #515151;
    font-size: 14px;
    font-weight: 700!important
}

.SepetBlockGenelTotal tr td:nth-child(2) {
    color: #a81d11;
    font-size: 14px;
    font-weight: 700!important;
    text-align: left!important
}

.SepetBlockCheck {
    padding: 8px 0;
    text-align: center
}

.SepetBlockCheck .button:nth-child(1) {
    display: none
}

.SepetBlockCheck .button {
    display: inline-block;
    width: 165px;
    height: 37px;
    line-height: 37px;
    border: none;
    margin: 0;
    padding: 0;
    text-transform: uppercase;
    background: #000;
    font-size: 16px;
    color: #fff
}

.headerContent,.ticiContainer {
    clear: both;
    max-width: 1366px;
    margin: 0 auto;
    position: relative
}

.ticiContainer.homeContainer {
    clear: both
}

.HesabimContainer {
    margin: 20px 0;
    float: left;
    width: 100%;
    padding: 0 10px 0 0
}

.leftBlock {
    float: left;
    padding-right: 20px;
    width: 25%
}

.leftBlock.scroll-to-fixed-fixed {
    border-left: 11px solid #333;
    border-radius: 11px;
    top: 75px!important
}

.centerCount {
    padding: 0
}

.categoryContainer .centerCount {
    float: right
}

.userLoginContent {
    float: left;
    padding: 0;
    width: 100%
}

.centerCount.solYadaSagAcik {
    width: 75%;
    float: left
}

.centerCount.solSagBlokAcik {
    width: 50%;
    float: left
}

.UyeolContent {
    width: 100%
}

.userMail input,.userSms input,.userSozlesmeDiv input {
    display: inline-block;
    vertical-align: top;
    margin-top: 0!important;
    margin-right: 5px
}

.userMail,.userSms,.userSozlesmeDiv {
    margin-bottom: 10px
}

.sideuserlogin {
    float: left;
    width: 100%;
    background: #fff;
    padding: 10px;
    text-align: center;
    margin-bottom: 20px
}

.sideuserlogin .spanTittle {
    float: left;
    width: 100%;
    text-align: center;
    color: #a0a0a0;
    font-weight: 900;
    font-size: 13px;
    padding: 10px 0;
    display: none
}

.sideuserlogin .textbox {
    float: left;
    width: 100%;
    border: none;
    box-shadow: 0 0;
    height: 40px;
    background: #f5f5f5;
    color: #a0a0a0;
    font-size: 12px;
    padding: 12px 15px;
    margin-bottom: 10px;
    text-indent: 0
}

.sideuserlogin .button {
    float: left;
    height: 40px;
    background: #f22a18!important;
    border-radius: 5px;
    margin-bottom: 10px
}

.sideuserlogin .button strong {
    font-size: 12px!important;
    color: #fff;
    font-weight: 900!important
}

.sideuserlogin .userSignUp {
    float: left;
    width: 100%;
    font-size: 13px;
    color: #fff;
    background: #49443f;
    border-radius: 5px;
    padding: 8px 0;
    font-weight: 700
}

.sideuserlogin .userPassBtn {
    float: right;
    color: #a0a0a0;
    text-decoration: underline;
    font-size: 10px;
    width: 70%;
    text-align: right
}

.sideuserlogin .uyeGirisBeniHatirla {
    float: right;
    text-align: right;
    font-size: 10px;
    color: #a0a0a0;
    margin-top: 5px
}

.sideuserlogin .uyeGirisBeniHatirla input {
    width: 12px;
    height: 10px;
    float: left
}

.sideuserlogin .baglanButton {
    float: left;
    border-radius: 5px;
    border: none!important
}

.sideuserlogin .baglanButton a {
    line-height: 20px
}

.YanUyeGirisi {
    float: left;
    width: 100%;
    background: #fff;
    padding: 10px;
    text-align: center;
    margin-bottom: 20px
}

.YanUyeGirisi .Block_Title {
    float: left;
    width: 100%;
    text-align: center;
    padding: 10px 0;
    display: block
}

.YanUyeGirisi .Block_Title span {
    color: #a0a0a0;
    font-weight: 900;
    font-size: 13px
}

.YanUyeGirisi .UyeGirisiSonLi {
    float: left;
    width: 100%;
    text-align: left;
    line-height: 20px;
    display: none
}

.YanUyeGirisi .Hosgeldiniz {
    float: left;
    width: 100%;
    margin-bottom: 5px
}

.YanUyeGirisi .ParaPuaniniz {
    float: left;
    width: 100%;
    margin-bottom: 15px
}

.Block_Text>a {
    color: #fff;
    float: left;
    width: 100%;
    padding: 10px;
    background: #a81d11;
    margin-top: 5px
}

.SepetBlock {
    float: left;
    width: 100%;
    background: #fff;
    text-align: center
}

.SepetBlock .Block_Title {
    float: left;
    width: 100%;
    background: #f39c12;
    text-align: center;
    color: #fff;
    display: block;
    font-size: 15px;
    text-transform: uppercase
}

.SepetBlock .Block_Title span {
    font-weight: 900;
    position: relative
}

.SepetBlock .Block_Title span:after {
    content: '';
    float: right;
    width: 21px;
    height: 21px;
    background: url(https://www.tudors.com/CustomCss/4863b978/images/sepetim.png)center center no-repeat;
    position: absolute;
    right: -30px;
    top: 0
}

.SepetBlock .solBlokSepetUrunyok {
    float: left;
    width: 100%;
    padding: 15px;
    font-size: 12px;
    color: #49443f
}

.ticiContainer:before,.ticiContainer:after {
    content: "";
    display: table
}

.ticiContainer:after {
    clear: both
}

.ticiContainer {
    clear: both;
    zoom:1}

.headerContent:after,.headerContent:before,.headerContent:after,.headerContent:before {
    content: "";
    display: table;
    clear: both
}

.UrunDetayCenter {
    width: 100%
}

.UrunDetayLeft {
    display: block
}

.UrunDetayRight {
    border: 0!important
}

.leftBlock .Block_Text {
    background: 0 0!important
}

.leftBlock .Block_Title {
    display: block;
    padding-bottom: 20px;
    border-bottom: 1px solid gray;
    float: left;
    width: 75%;
    margin: 0 0 10px
}

.leftBlock .Block_Title span {
    font-size: 12px;
    color: #000;
    letter-spacing: 3px;
    margin-left: 25%;
    text-transform: uppercase;
    font-weight: 700
}

.rightBlock {
    margin-bottom: 0;
    float: right;
    background-color: #fff;
    padding-left: 20px
}

.rightBlock .sliderBannerContainer .productItem .productImage {
    height: 200px
}

.rightBlock .sliderBannerContainer .cargoIcon {
    left: 27%
}

.rightBlock .sliderBannerContainer .mycartIcon a {
    left: 90px
}

.rightBlock .sliderBannerContainer .productItem .productPrice {
    padding-bottom: 5px
}

.proCategoryTitle a {
    font-size: 13px;
    line-height: 20px;
    color: #000
}

.back {
    float: right
}

.ProductDetailMainRow {
    float: left;
    width: 100%
}

.urunDetayTutucu {
    background: #fff;
    float: left;
    width: 100%
}

.leftImage {
    width: 625px;
    float: left;
    position: relative
}

.TopList {
    float: left;
    width: 100%;
    max-width: 420px;
    border: 1px solid #c4c4c4;
    padding: 15px;
    margin: 0 0 15px;
    position: relative
}

.RightDetail {
    width: calc(100% - 625px);
    width: -webkit-calc(100% - 625px);
    width: -moz-calc(100% - 625px);
    width: -o-calc(100% - 625px);
    float: left;
    position: relative;
    padding-left: 35px;
    padding-top: 20px
}

.UrunDetayLeft {
    margin: 0!important;
    overflow: hidden
}

.Images {
    float: right;
    width: 74%;
    padding-bottom: 94%;
    position: relative;
    margin-bottom: 0;
    background: #fff
}

.Images img {
    max-width: 100%;
    max-height: 100%;
    position: absolute;
    left: 0;
    top: 0;
    bottom: 0;
    right: 0;
    margin: auto
}

.cloudzoom-blank>div:last-child {
    display: none!important
}

.SmallImages {
    float: left;
    width: 26%;
    padding: 28px 7.8% 0;
    max-height: 587px;
    overflow-y: auto
}

.SmallImages div {
    float: left;
    width: 100%;
    height: 82px;
    position: relative;
    cursor: pointer;
    margin-bottom: 25px
}

.SmallImages div:last-child {
    margin-bottom: 0
}

.SmallImages div img {
    max-width: 100%;
    max-height: 100%;
    position: absolute;
    top: 0;
    left: 0;
    bottom: 0;
    right: 0
}

.SmallImages::-webkit-scrollbar {
    width: 4px
}

.SmallImages::-webkit-scrollbar-track {
    background: #f6f6f6
}

.SmallImages::-webkit-scrollbar-thumb {
    background: #dbdbdb;
    border-radius: 0
}

.DetayYeniUrun {
    display: none!important
}

.DetayYeniUrun #divYeniUrun {
    position: absolute;
    top: 10px;
    right: -2px;
    width: 60px;
    height: 30px;
    color: #1e89e4;
    font-size: 16px;
    font-weight: 700;
    line-height: 33px;
    overflow: hidden;
    text-align: center;
    text-transform: uppercase
}

.ProductName {
    float: left;
    width: calc(100% - 70px);
    position: relative;
    margin-bottom: 20px;
    display: block
}

.ProductName h1 span:not(#divUrunKodu) {
   
    width: 100%;
    display: inline-block;
    color: #4c4c4c;
    font-size: 16px;
    font-weight: 400
}

#divUrunKodu {
    display: inline-block;
   
    color: gray;
    font-size: 12px;
    font-weight: 400;
    width: auto;
    margin-top: 10px;
    padding-left: 26%
}

#divUrunKodu:before {
    display: inline-block!important;
    content: 'ÜRÜN KODU';
    color: gray;
    font-size: 12px;
    font-weight: 400;
    position: relative;
    
    margin-right: 12px
}

.puanVer {
    float: left;
    width: 100%;
    margin-top: 5px
}

#PuanVer {
    float: left
}

.PuanVerSag {
    float: left;
    margin-left: 10px;
    line-height: 24px;
    height: 23px;
    font-size: 13px;
    color: #666
}

ul.rating li {
    margin-right: 0!important;
    width: 16px!important
}

ul.rating li i.starItem {
    font-size: 16px!important;
    color: #d8d8d8
}

ul.rating li i.starItem:hover {
    font-size: 16px!important;
    color: #ffc000
}

body .rating-stars ul>li.star.selected>i.fa {
    color: #ffc000
}

.rating .filled i {
    color: #ffd400!important
}

.markaresmi {
    float: left;
    width: 100%;
    position: relative;
    z-index: 1;
    display: none!important
}

.markaresmi a {
    position: absolute;
    right: 0;
    top: 0;
    display: block
}

.markaresmi img {
    max-width: 100px;
    display: block
}

#divOnyazi {
    float: left;
    width: calc(100% - 70px);
    padding: 0;
    display: none
}

#divOnyazi * {
    font-family: josefin sans,sans-serif!important;
    display: inline-block;
    color: #4c4c4c;
    font-size: 16px;
    font-weight: 400
}

#divOnyazi strong {
    font-weight: 700
}

#divOnyazi .fa {
    font-family: fontawesome!important
}

.PriceList {
    float: left;
    position: relative;
    width: 100%;
    padding-bottom: 15px;
    max-width: 360px;
    margin-top: 15px
}

#divTahminiTeslimatSuresi {
    float: left;
    width: 100%
}

#divTahminiTeslimatSuresi .left_line {
    float: left;
    color: #4f4f4f;
    font-size: 14px;
    line-height: 16px;
    font-weight: 400
}

#divTahminiTeslimatSuresi .center_line {
    float: left;
    color: #4f4f4f;
    font-size: 14px;
    line-height: 16px;
    margin: 0 3px;
    font-weight: 400
}

#divTahminiTeslimatSuresi .right_line {
    float: left;
    color: #4f4f4f;
    font-size: 14px;
    line-height: 16px;
    font-weight: 400
}

#pnlFiyatlar {
    float: left;
    font-family: abakutlsymsans,sans-serif;
    margin-top: 8px
}

#divIndirimliFiyat {
    float: left
}

#divMagazaStok {
    display: block!important;
    position: absolute;
    top: 0;
    display: none!important
}

#divMarka {
    float: left;
    width: 100%;
    margin: 10px 0 0
}

#divMarka .left_line {
    display: inline-block;
    color: #000;
    font-size: 13px;
    font-weight: 400;
    text-transform: uppercase;
    margin-right: 12px
}

#divMarka .center_line {
    display: none;
    color: #111;
    font-size: 14px;
    font-weight: 400
}

#divMarka .right_line {
    display: inline-block;
    width: auto
}

#divMarka .right_line * {
    display: inline-block;
    width: auto;
    color: #000;
    font-size: 13px;
    font-weight: 400;
    line-height: 1
}

#divTedarikci {
    float: left;
    width: 100%;
    margin: 3px 0
}

#divTedarikci .left_line {
    display: inline-block;
    color: #000;
    font-size: 13px;
    font-weight: 400;
    margin-right: 12px;
    text-transform: uppercase
}

#divTedarikci .center_line {
    display: none;
    color: #111;
    font-size: 13px;
    font-weight: 500
}

#divTedarikci .right_line {
    display: inline-block;
    width: auto
}

#divTedarikci .right_line * {
    display: inline-block;
    width: auto;
    color: #000;
    font-size: 13px;
    font-weight: 400
}

#divToplamStokAdedi {
    display: block!important;
    float: left;
    clear: left;
    margin: 3px 0
}

#divToplamStokAdedi .left_line {
    display: inline-block;
    color: #000;
    font-size: 13px;
    font-weight: 400;
    margin-right: 12px;
    text-transform: uppercase
}

#divToplamStokAdedi .center_line {
    display: none;
    color: #000;
    font-size: 13px;
    font-weight: 400
}

#divToplamStokAdedi .right_line {
    display: inline-block;
    color: #000;
    font-size: 13px;
    font-weight: 400
}

#divIndirimOrani {
    float: left;
    width: 45px;
    height: 30px;
    background: #c90000;
    overflow: hidden;
    margin-right: 8px;
    text-align: center;
    display: none
}

#divIndirimOrani .left_line {
    display: none;
    width: 90px;
    color: #231f20;
    font-size: 13px;
    font-weight: 600
}

#divIndirimOrani .center_line {
    display: none;
    color: #231f20;
    font-size: 13px;
    font-weight: 600;
    margin-right: 20px
}

#divIndirimOrani .indirimliOrani {
    display: inline-block;
    color: #fff;
    font-size: 18px;
    font-weight: 700;
    line-height: 32px;
    width: 100%
}

#divIndirimOrani .indirimliOrani * {
    display: inline-block;
    width: auto;
    color: #fff;
    font-size: 18px;
    line-height: 26px;
    font-weight: 700
}

.PiyasafiyatiContent {
    display: block
}

.PiyasafiyatiContent .left_line {
    display: none;
    width: 103px;
    color: #000;
    font-size: 13px;
    font-weight: 400;
    width: 110px
}

.PiyasafiyatiContent .center_line {
    display: none;
    color: #000;
    font-size: 14px;
    font-weight: 400;
    margin-right: 0
}

.PiyasafiyatiContent .right_line * {
    display: inline-block;
    color: #2c2c2c;
    font-size: 17px;
    font-weight: 400;
    text-decoration: line-through;
    text-decoration-color: red;
    line-height: 0
}

.PiyasafiyatiContent .right_line .spanKdv {
    font-size: 14px;
    color: #666;
    font-weight: 400;
    display: none!important
}

.IndirimliFiyatContent {
    float: left
}

.IndirimliFiyatContent .left_line {
    display: none;
    width: 103px;
    color: #000;
    font-size: 14px;
    font-weight: 400;
    width: 110px
}

.IndirimliFiyatContent .center_line {
    display: none;
    color: #000;
    font-size: 14px;
    font-weight: 400;
    margin-right: 0
}

.IndirimliFiyatContent .right_line {
    display: inline-block;
    color: #231f20;
    font-size: 14px;
    font-weight: 400
}

.IndirimliFiyatContent .right_line .spanFiyat {
    display: inline-block;
    color: #ff3b00;
    font-size: 21px;
    font-weight: 600;
    line-height: 1
}

.IndirimliFiyatContent .right_line .spanKdv {
    font-size: 14px;
    color: #48494a;
    font-weight: 400;
    display: none!important
}

#divTurkLirasiFiyat {
    float: left;
    width: 100%;
    display: none
}

#divTurkLirasiFiyat .left_line {
    display: inline-block;
    width: 103px;
    color: #152e59;
    font-size: 12px;
    font-weight: 700
}

#divTurkLirasiFiyat .center_line {
    display: inline-block;
    color: #152e59;
    font-size: 14px;
    font-weight: 700;
    margin-right: 0
}

#divTurkLirasiFiyat .right_line {
    display: inline-block;
    color: #000;
    font-size: 14px;
    font-weight: 400
}

#divIndirimsizFiyat {
    float: left;
    width: 100%
}

#divIndirimsizFiyat .left_line {
    display: none;
    color: #000;
    font-size: 14px;
    font-weight: 400
}

#divIndirimsizFiyat .center_line {
    display: none;
    color: #231f20;
    font-size: 13px;
    font-weight: 600;
    margin-right: 0
}

#divIndirimsizFiyat .right_line {
    display: inline-block;
    color: #231f20;
    font-size: 13px;
    font-weight: 400
}

#divIndirimsizFiyat .right_line .spanFiyat {
    display: inline-block;
    color: #cc1332;
    font-size: 18px;
    font-weight: 400;
    line-height: 1
}

#divIndirimsizFiyat .right_line .spanKdv {
    font-size: 14px;
    color: #48494a;
    font-weight: 400;
    display: none!important
}

#divKDVDahilFiyat {
    display: block
}

#divKDVDahilFiyat .left_line {
    display: inline-block;
    color: #000;
    font-size: 14px;
    font-weight: 400
}

#divKDVDahilFiyat .center_line {
    display: none;
    color: #2c2c2c;
    font-size: 13px;
    font-weight: 400;
    margin-right: 0
}

#divKDVDahilFiyat .right_line * {
    display: inline-block;
    color: #cc1332;
    font-size: 18px;
    font-weight: 400;
    line-height: 1
}

#divParaPuan {
    float: left;
    width: 260px;
    border: 1px dashed #ffc245;
    padding: 9px 0;
    margin-top: 38px
}

#divParaPuan .left_line {
    display: inline-block;
    font-size: 0
}

#divParaPuan .left_line:after {
    content: '\f195';
    font-family: fontawesome;
    color: #ffc245;
    line-height: 25px;
    font-size: 20px;
    border-right: 1px solid #ffc245;
    width: 51px;
    text-align: center;
    display: inline-block
}

#divParaPuan .center_line {
    display: none;
    color: #ffc245;
    font-size: 16px;
    font-weight: 700;
    line-height: 25px
}

#divParaPuan .right_line {
    display: inline-block;
    color: #ffc245;
    font-size: 16px;
    font-weight: 700;
    line-height: 25px;
    margin-left: 20px
}

#divParaPuan .right_line:after {
    content: 'Ballı Puan Kazan!';
    display: inline-block
}

#divTaksitAciklama {
    display: block
}

#divTaksitAciklama * {
    display: inline-block;
    color: #000;
    font-size: 13px;
    width: 100%;
    font-weight: 400;
    margin-top: 10px
}

#divStokYok {
    float: left;
    width: 100%;
    margin: 40px 0;
    font-size: 20px;
    color: #000;
    font-weight: 700;
    text-align: center
}

#pnlFiyatlar .spanKdv {
    margin-left: 5px;
    display: inline-block
}

#divEkstraBilgiler {
    float: left;
    width: 100%;
    border-top: 1px solid #f3f3f5;
    margin-top: 35px
}

#divEkstraBilgiler img {
    max-width: 100%;
    display: inline-block;
    margin-right: 10px;
    
}

#pnlFiyatlar .odemeSecenekHavale {
    text-align: left;
    clear: left;
    font-size: 0;
    color: #000;
    display: block!important;
    width: auto!important;
    padding: 0!important;
    margin: 5px 0!important;
    line-height: 1!important;
    border: none!important;
    background: 0 0!important;
    font-weight: 400!important
}

#pnlFiyatlar .odemeSecenekHavale:before {
    content: 'Havale';
    float: left;
    color: #000;
    font-size: 14px;
    font-weight: 400;
    line-height: 24px;
    width: 110px;
    margin-right: 3px
}

#pnlFiyatlar br {
    display: none
}

#pnlFiyatlar strong {
    display: inline-block
}

#pnlFiyatlar #ltrHavaleFiyati {
    float: left;
    font-size: 24px;
    color: #08a700;
    font-weight: 400
}

#divUrunEkSecenek {
    float: left;
    width: 57%;
    margin-top: 20px
}

#divUrunEkSecenek .eksecenekLine:first-child {
    display: none
}

#divUrunEkSecenek .eksecenekLine {
    float: left;
    clear: none!important;
    width: 100%;
    margin-bottom: 20px
}

#divUrunEkSecenek .eksecenekLine .left_line {
    display: inline-block;
    
    font-size: 13px;
    color: gray;
    text-decoration: underline;
    margin-bottom: 5px
}

#divUrunEkSecenek .eksecenekLine .left_line:after {
    display: none;
    content: ' Seçiniz'
}

#divUrunEkSecenek .eksecenekLine .center_line {
    display: none;
    width: auto;
    float: left;
    color: #262626;
    font-weight: 700;
    font-size: 16px;
    line-height: 37px;
    margin-right: 10px
}

#divUrunEkSecenek .eksecenekLine .right_line {
    display: inline-block;
    
    width: 100%
}

#divUrunEkSecenek .eksecenekLine .right_line select {
    width: 192px;
    padding: 0 10px;
    border: 1px solid #e5e5e5;
    cursor: pointer;
    height: 40px;
    line-height: 40px;
    background: #fff;
    font-weight: 400;
    border-radius: 0;
    text-align: left;
    font-size: 13px;
    color: #333
}

#divUrunEkSecenek .eksecenekLine .right_line .size_box {
    float: left;
    cursor: pointer;
    width: auto;
    text-align: center;
    margin-right: 7px;
    background: #fff;
    padding: 0 12px;
    border: 1px solid #ababab;
    line-height: 33px;
    color: #1d1d1d;
    font-size: 15px;
    background: #fff;
    border-radius: 2px;
    height: 32px
}

#divUrunEkSecenek .eksecenekLine .right_line .size_box img {
    float: left;
    width: 34px;
    height: 33px;
    margin: 2px
}

#divUrunEkSecenek .eksecenekLine .right_line .size_box:hover {
    border-color: #71034e;
    background: #565656;
    color: #fff
}

#divUrunEkSecenek .eksecenekLine .right_line .size_box.selected {
    border-color: #71034e;
    background: #565656;
    color: #fff
}

#divUrunEkSecenek .eksecenekLine .right_line .size_box.nostok {
    position: relative;
    cursor: no-drop;
    color: #ababab
}

#divUrunEkSecenek .eksecenekLine .right_line .size_box.nostok:after {
    content: '';
    height: 1px;
    width: 55%;
    background: #868686;
    left: 25%;
    top: 50%;
    position: absolute;
    transform: rotate(-132deg);
    -webkit-transform: rotate(-132deg);
    -moz-transform: rotate(-132deg);
    -o-transform: rotate(-132deg)
}

#divUrunEkSecenek .eksecenekLine .right_line .size_box.nostok:before {
    content: '';
    height: 1px;
    width: 55%;
    background: #868686;
    left: 25%;
    top: 50%;
    position: absolute;
    transform: rotate(132deg);
    -webkit-transform: rotate(132deg);
    -moz-transform: rotate(132deg);
    -o-transform: rotate(132deg)
}

#divUrunEkSecenek .eksecenekLine.selectvaryasyon {
    display: none
}

#divUrunEkSecenek .btnnostok {
    cursor: pointer
}

#divUrunKisiselNot {
    float: left;
    width: 100%
}

#divUrunKisiselNot div:first-child {
    display: none
}

#divUrunKisiselNot br {
    display: none
}

#divUrunKisiselNot input {
    float: left;
    width: 444px;
    border: 1px solid #f6f6f6;
    padding: 15px;
    font-size: 13px;
    color: #000
}

#divUrunKisiselNot input::-webkit-input-placeholder {
    color: #ddd;
    font-style: italic
}

#divUrunKisiselNot input:-moz-placeholder {
    color: #ddd;
    font-style: italic
}

#divUrunKisiselNot input::-moz-placeholder {
    color: #ddd;
    font-style: italic
}

#divUrunKisiselNot input:-ms-input-placeholder {
    color: #ddd;
    font-style: italic
}

#divUrunKisiselNot input:focus {
    color: #000;
    background: #fff;
    transition: .3s;
    -webkit-transition: .3s;
    -ms-transition: .3s
}

#divUrunSiparisDosya {
    float: left;
    width: 100%;
    margin-bottom: 11px;
    clear: left!important
}

#divUrunSiparisDosya .left_line {
    float: left;
    width: 30%;
    clear: left;
    color: #737373;
    font-size: 12px;
    font-weight: 400;
    line-height: 39px;
    position: relative
}

#divUrunSiparisDosya .center_line {
    float: left;
    width: 5%;
    color: #737373;
    font-size: 12px;
    font-weight: 400;
    line-height: 39px
}

#divUrunSiparisDosya .right_line {
    float: left;
    width: 65%;
    position: relative;
    padding-top: 7.5px
}

#divUrunSiparisDosya .right_line .RadUpload {
    width: 100%;
    float: left
}

#divUrunSiparisDosya .right_line .RadUpload .ruInputs li {
    margin-bottom: 0
}

#divUrunSiparisDosya .right_line .RadUpload .ruFileWrap {
    width: 100%;
    display: block;
    height: 22px
}

#divUrunSiparisDosya .right_line .RadUpload .ruFileInput {
    cursor: pointer;
    position: absolute;
    left: 0;
    top: 0;
    padding: 0;
    margin: 0;
    font-size: 0;
    text-indent: -9999px;
    width: 100%;
    display: block;
    height: 22px;
    border: none;
    opacity: 1
}

#divSatinAl {
    float: left;
    width: 57%;
    padding: 50px 0 0;
    position: relative
}

.detayText {
    float: left;
    width: 100%;
    padding: 15px 0
}

.BasketBtn {
    float: left;
    position: relative;
    width: 100%
}

#divAdetCombo {
    display: block!important;
    float: left;
    position: relative;
    width: 134px;
    margin-right: 20px
}

#divAdetCombo .left_line {
    width: 100%;
    float: left;
    line-height: 1;
    clear: left;
    color: #22313f;
    text-align: left;
    font-size: 13px;
    z-index: 1;
    font-weight: 700;
    margin-bottom: 10px
}

#divAdetCombo .center_line {
    display: none!important;
    float: left
}

#divAdetCombo .right_line {
    float: left;
    width: 100%
}

#divAdetCombo select {
    width: 100%;
    height: 37px;
    border: 1px solid #d4d4d4!important;
    margin: 0;
    padding: 0;
    color: #22313f;
    font-size: 14px;
    text-align: left;
    font-weight: 700
}

.RightDetail .riSingle {
    position: relative;
    width: 60px;
    float: left;
    border-radius: 0;
    height: 40px;
    text-align: center!important
}

.RightDetail .riSingle a.riUp,.RightDetail .riSingle a.riDown {
    width: 15px!important;
    height: 38px!important;
    position: absolute;
    top: 0;
    margin: 0!important;
    float: left;
    cursor: pointer
}

.RightDetail .riSingle a.riUp {
    right: 0;
    left: auto
}

.RightDetail .riSingle a.riDown {
    left: 0
}

.Basketinp {
    float: left;
    position: relative;
    width: 120px;
    display: none
}

.Basketinp p {
    float: left;
    width: 60px;
    line-height: 40px;
    clear: left;
    color: #707070;
    text-align: left;
    font-size: 13px;
    z-index: 1;
    font-weight: 600
}

#txtbxurunSiparisAdedi_wrapper {
    float: left;
    width: 100%!important;
    position: relative;
    padding: 0!important
}

#txtbxurunSiparisAdedi {
    display: inline-block;
    width: 100%!important;
    height: 40px!important;
    margin: 0;
    padding: 0 15px;
    color: #a5a5a5;
    font-size: 13px;
    font-weight: 400;
    background: #fff;
    border: 1px solid #e5e5e5;
    text-align: center;
    appearance: none;
    -moz-appearance: none;
    -webkit-appearance: none
}

.basketBtn {
    float: left;
    position: relative;
    width: 75%
}

.basketBtn input {
    width: 100%;
    height: 44px;
    padding: 0!important;
    color: #fff;
    float: left;
    border-radius: 0;
    border: none!important;
    background: #00aa5b;
    font-weight: 700;
    font-size: 14px;
    text-transform: uppercase;
    appearance: none;
    -moz-appearance: none;
    -webkit-appearance: none
}

.basketBtn input:hover {
    background-color: #008446
}

.buyfast {
    float: left;
    position: relative;
    width: 203px;
    display: none
}

.buyfast input {
    width: 100%;
    height: 48px;
    padding: 0!important;
    color: #fff;
    float: left;
    border: none!important;
    background: #262626;
    font-weight: 700;
    font-size: 15px;
    text-transform: uppercase;
    appearance: none;
    -moz-appearance: none;
    -webkit-appearance: none
}

.buyfast input:hover {
    background-color: #262626
}

#divKombinSatinAl {
    float: left;
    padding-top: 26px;
    width: 298px
}

#divKombinSatinAl a {
    margin: 0!important;
    padding: 0!important;
    border: none;
    border-radius: 1px;
    width: 100%;
    height: 44px;
    line-height: 44px;
    text-align: center;
    background-color: #620717!important;
    color: #fff;
    font-size: 14px;
    font-weight: 700
}

.ProductIcon {
    float: left;
    width: 120px;
    position: absolute;
    right: 0;
    top: 0;
    display: none
}

.ProductIcon .box1 {
    float: left;
    text-align: center;
    padding: 0 10px;
    margin: 0;
    min-width: 0;
    width: 100%;
    background: 0 0;
    font-size: 11px;
    line-height: 1;
    color: #7d7d7d;
    font-weight: 400;
    padding-bottom: 10px;
    margin-bottom: 10px;
    border-bottom: 1px solid #e5e5e5
}

.ProductIcon .box1 i {
    display: none
}

.ProductIcon #divKritikStok .box1 i {
    display: inline-block;
    color: #d2d2d2;
    font-size: 24px;
    
    width: 100%;
    text-align: center;
    margin: 0 0 7px!important
}

.ProductIcon #divKritikStok,.ProductIcon .UIstekListemeEkle,.ProductIcon .UGelinceHaberVer,.ProductIcon #divTelefonSiparis,.ProductIcon .UFavorilerimeEkle,.ProductIcon #divIndirimliUrun,.ProductIcon .FiyatHaberVer,.ProductIcon #divKargoBedava {
    float: left;
    position: relative;
    width: 100%
}

.ProductIcon #divKritikStok>a,.ProductIcon .UGelinceHaberVer>a,.ProductIcon #divTelefonSiparis>a,.ProductIcon .UFavorilerimeEkle>a,.ProductIcon .UIstekListemeEkle>a,.ProductIcon #divIndirimliUrun>a,.ProductIcon .FiyatHaberVer>a,.ProductIcon #divKargoBedava>a {
    display: inline-block;
    
    width: 100%
}

#divKargoBedava {
    float: right;
    position: absolute;
    right: 15px;
    top: 10px
}

.UFavorilerimeEkle {
    float: left;
    margin-left: 20px
}

#divKargoBedava .box1 {
    margin: 0;
    padding: 0;
    float: left;
    min-width: 0;
    background: 0 0;
    width: 55px;
    height: 35px;
    text-align: center;
    border: 1px solid #7c7c7c;
    border-radius: 3px;
    text-transform: uppercase;
    font-size: 10px;
    font-weight: 700;
    color: #7c7c7c;
    padding-top: 7px
}

#divKargoBedava .box1 i {
    display: none
}

.UFavorilerimeEkle .box1 {
    margin: 0;
    padding: 0;
    float: left;
    min-width: 0;
    font-size: 0;
    background: #e6e6e6;
    border-radius: 100%;
    width: 42px;
    height: 42px;
    text-align: center
}

.UFavorilerimeEkle .box1 i {
    font-size: 0
}

.UFavorilerimeEkle .box1 i:before {
    content: '\e813';
    font-family: lineariconsfree;
    font-size: 26px;
    line-height: 42px;
    color: #000
}

.ProductIcon2 {
    float: left;
    text-align: left;
    width: 100%
}

.ProductIcon2 .YorumYazbtnContent,.ProductIcon2 .TavsiyeEtBtnContent,.ProductIcon2>.hidden-phone {
    display: inline-block;
    text-align: center
}

.ProductIcon2 .YorumYazbtnContent {
    margin-right: 0
}

.ProductIcon2 .TavsiyeEtBtn {
    display: inline-block
}

.ProductIcon2 .YorumYazbtnContent a {
    display: inline-block
}

.ProductIcon2 .printBtn {
    display: inline-block
}

.ProductIcon2 .TavsiyeEtBtnContent a:before {
    content: '\f164';
    font-family: fontawesome;
    display: none;
    font-size: 15px;
    line-height: 40px;
    width: 40px;
    border: 1px solid #f9f9f9;
    color: #999;
    margin-right: 20px
}

.ProductIcon2 .printBtn:before {
    content: '\f02f';
    font-family: fontawesome;
    display: none;
    font-size: 15px;
    line-height: 40px;
    width: 40px;
    border: 1px solid #f9f9f9;
    color: #999;
    margin-right: 20px
}

.ProductIcon2 .YorumYazbtnContent a:before {
    content: '\f075';
    font-family: fontawesome;
    display: none;
    font-size: 15px;
    line-height: 40px;
    width: 40px;
    border: 1px solid #f9f9f9;
    color: #999
}

.ProductIcon2 .YorumYazbtnContent a,.ProductIcon2 .TavsiyeEtBtnContent a,.ProductIcon2 .hidden-phone a {
    position: relative;
    white-space: nowrap;
    line-height: 40px;
    text-transform: uppercase;
    background-color: #efebeb;
    margin-right: -26.5%;
    top: -40px;
    font-size: 11px;
    padding: 0 25px;
    font-weight: 700;
    text-align: center;
    border: none!important;
    color: #262626
}

.ProductIcon2 .TavsiyeEtBtn span {
    font-weight: 600
}

.ProductIcon2 .YorumYazbtnContent a span {
    font-weight: 600
}

.ProductIcon2 .TavsiyeEtBtnContent {
    display: none
}

.ProductIcon2 .hidden-phone {
    display: none
}

.ProductIcon2 .YorumYazbtnContent {
    display: block
}

.socialButons {
    float: right!important;
    width: 100%;
    margin: 0!important;
    display: none!important
}

.socialButons iframe {
    float: left;
    display: none
}

.product-social {
    float: left;
    margin-right: 10px
}

.product-social span {
   
    line-height: 32px;
    display: inline-block;
    color: #000;
    font-size: 12px;
    font-weight: 300;
    margin-right: 5px
}

.product-social ul {
    float: left
}

.product-social ul li {
    float: left;
    margin-right: 13px
}

.product-social ul li a {
    display: block;
    color: #323232;
    font-size: 18px
}

.urunOzellik {
    float: left;
    width: 100%;
    margin: 10px 0 0
}

.urunTab {
    float: left;
    width: 100%;
    position: relative
}

.urunTab ul {
    float: left;
    width: 100%;
    text-align: left
}

.urunTab li {
    position: relative;
    display: inline-block;
    text-align: center;
    
    margin-right: 10px;
    display: none!important
}

.urunTab li a {
    font-size: 12px;
    color: #0b0b0b;
    font-weight: 400;
    display: inline-block;
    position: relative;
    line-height: 15px;
    text-transform: uppercase;
    font-weight: 700;
    letter-spacing: .5px
}

.urunTab li a span {
    font-weight: 700
}

.urunTab li:last-child {
    margin-right: 0
}

.urunTab li:last-child a {
    border-right: none;
    padding-right: 0
}

.urunTab li:first-child a {
    padding-left: 0
}

.urunTab li:first-child {
    display: block!important
}

.urunTab li:hover a {
    text-decoration: underline
}

.urunTab li.TabYorumlar {
    display: block!important
}

.urunTab li.active a {
    text-decoration: underline
}

.teknikDetay li {
    margin-bottom: 0!important;
    line-height: 1;
    padding-left: 0;
    text-align: left!important
}

.teknikDetay .t1 {
    display: inline-block;
    width: 120px;
    font-size: 13px;
    color: #000
}

.teknikDetay {
    list-style-type: disc
}

.teknikDetay>li {
    list-style-type: disc;
    list-style-position: inside
}

.teknikDetay li>ul {
    display: inline-block
}

.teknikDetay li>ul span {
    color: #000;
    font-size: 13px
}

.urunTabAlt {
    float: left;
    width: 100%;
    padding: 5px 0
}

.TabYorumlar,.TabOdemeSecenekleri,.TabUrunOnerileri {
    display: none!important
}

.urunDetayPanel {
    float: left;
    width: 100%;
    clear: none!important;
    overflow-y: auto;
    overflow-x: hidden
}

.urunDetayPanel::-webkit-scrollbar {
    width: 4px
}

.urunDetayPanel::-webkit-scrollbar-track {
    background: #f6f6f6
}

.urunDetayPanel::-webkit-scrollbar-thumb {
    background: #dbdbdb;
    border-radius: 0
}

.urunDetayPanel strong {
    font-weight: 700;
    float: none
}

.urunDetayPanel.FilitreMaxHeight {
    width: 80%!important;
    max-height: 290px!important
}

.yorumlarItem {
    background-color: #eee;
    border-bottom: 3px solid #a09b98;
    padding: 16px;
    line-height: 26px;
    float: left;
    width: 100%;
    margin-top: 20px
}

.yorumlarItemS1 {
    padding-bottom: 5px;
    font-size: 12px;
    color: #666;
    border-bottom: 1px dashed #a09b98
}

.urunDetayPanel .button {
    color: #fff
}

.urunTabAlt * {
    font-family: josefin sans,sans-serif!important;
    line-height: 1.5;
    color: gray;
    font-size: 12px;
    font-weight: 400
}

.urunTabAlt i {
    font-family: fontawesome!important
}

.urunTabAlt img {
    max-width: 100%!important
}

.urunTabAlt iframe {
    max-width: 100%!important
}

.urunTabAlt {
    font-family: josefin sans,sans-serif!important;
    line-height: 15px;
    color: gray;
    font-size: 12px;
    font-weight: 400
}

.urunTabAlt .teknikDetay {
    margin-top: 10px;
    display: block;
    width: 100%
}

.urunTabAlt .ng-valid-email {
    text-align: left
}

.orders .order-info i {
    margin-top: 0!important
}

.OzellikClick {
    display: none;
    font-size: 12px;
    color: #0b0b0b;
    font-weight: 700;
    text-decoration: underline;
    float: left;
    margin: 20px 0;
    cursor: pointer;
    letter-spacing: .5px
}

.OzellikClick i {
    font-size: 12px;
    color: #0b0b0b;
    font-weight: 700;
    margin-left: 5px
}

#btnYorumKaydet {
    float: left;
    text-align: center;
    appearance: none;
    -moz-appearance: none;
    -webkit-appearance: none
}

.urunTabAlt ul li {
    margin-bottom: 10px;
    clear: both
}

.oneriValidate .validate {
    top: 0;
    padding: 5px
}

.urunTabAlt ul li input {
    float: left;
    margin-right: 5px;
    width: auto!important
}

.urunTabAlt ul li label {
    float: left;
    width: auto!important
}

.urunTabAlt ul li input[type=checkbox] {
    margin-top: 5px
}

.urunTabAlt ul li .captchaImageBox {
    float: left
}

.urunTabAlt ul li .captchaImageBox img {
    max-width: 100%;
    width: auto
}

.urunTabAlt ul li .captchaInputBox {
    margin: 10px;
    float: left
}

.urunTabAlt ul li.urundetyaGuvenlikodu span {
    float: left
}

.urunTabAlt ul li .GuvnelikKodu {
    float: left;
    line-height: 50px;
    margin-right: 10px;
    display: block
}

.HomePageSlideShowContainer {
    float: left;
    width: 100%
}

.HomePageSlideShowContainer .HomePageSlideShow {
    padding: 0;
    width: 100%
}

.HomePageSlideShowContainer .HPSItems {
    clear: both;
    cursor: pointer;
    width: 100%
}

.HomePageSlideShowContainer .HPSItems div {
    cursor: pointer;
    float: left;
    margin: 0;
    overflow: hidden;
    padding: 0;
    position: absolute;
    width: 100%
}

.HomePageSlideShowContainer .HomePageSlideShow img {
    border: 0;
    float: left;
    margin: 0;
    padding: 0;
    max-width: 100%
}

.HomePageSlideShowContainer .HomePageSlideShow .active {
    float: left
}

.HomePageSlideShowContainer .navi {
    bottom: 8px;
    height: 10px;
    left: 0;
    margin: 0;
    padding: 0;
    position: absolute;
    width: 100%
}

.HomePageSlideShowContainer .navi a {
    background-color: #777;
    width: 10px;
    height: 10px;
    border-radius: 0;
    display: block;
    float: right;
    font-size: 1px;
    margin: 0 2px;
    position: relative
}

.HomePageSlideShowContainer .navi a:hover {
    background-color: red
}

.HomePageSlideShowContainer .navi a.active {
    background-color: red
}

.KategoriFilitrelemeContent .Block_Title {
    display: none
}

.sortingContent {
    float: left;
    width: 100%;
    background-color: #fff!important;
    border-radius: 0!important;
    border-top: 1px solid gray;
    border-bottom: 1px solid gray;
    position: relative;
    margin: 0 0 15px;
    padding: 0;
    display: -webkit-flex;
    display: -moz-flex;
    display: -o-flex
}

.sortingContent li:not(.appliedFilter) {
    color: #000!important;
    font-weight: 400!important;
    border-radius: 0!important;
    padding: 0
}

.sortingContent li>a {
    position: relative;
    background-color: transparent!important;
    color: #000!important;
    font-size: 13px!important;
    border-radius: 0!important;
    padding: 0 9px!important;
    text-align: left;
    line-height: 38px!important;
    border: none;
    margin-right: 7px
}

.sortingContent li:not(.appliedFilter):hover a {
    background: 0 0!important;
    color: #000!important;
    text-decoration: underline
}

.sortingContent li a span {
    font-weight: 400!important;
    line-height: 38px
}

.sortingContent li a.selected {
    background: 0 0!important;
    color: #000!important;
    text-decoration: underline
}

.appliedFilter.FiltrelemeUrunAdet span {
    
    font-size: 13px;
    color: #000!important;
    font-weight: 400!important;
    line-height: 38px!important;
    padding: 0;
    display: inline-block!important;
    margin-right: 15px!important
}

.appliedFilter.FiltrelemeUrunAdet span:after {
    display: none;
    content: 'Bulundu';
    float: right;
    margin-left: -4px;
    font-weight: 600
}

.sortingContent .appliedFilter {
    
    background-color: transparent!important;
    height: auto!important;
    display: inline-block!important;
    padding: 0!important
}

.filterDeleteContent .appliedFilter {
    margin: 1px 10px!important;
    display: none
}

.filterDeleteContent .appliedFilter.FiltrelemeKaldir {
    display: block
}

.filterDeleteContent {
    position: absolute;
    left: 65px;
    top: 0
}

.FiltrelemeKaldir a {
    color: #262626!important
}

.blockSelect {
    margin: 0 auto;
    display: inline-block;
    text-align: center;
    padding-top: 6px;
    display: none
}

.blockSelect:before {
    content: '';
    content: 'Görünüm :';
    float: left;
    font-size: 12px;
    color: #000;
    line-height: 19px
}

.blockSelect a {
    float: left;
    color: #a5a5a5!important;
    padding: 0!important;
    margin: 0 7px!important;
    white-space: nowrap;
    overflow: hidden;
    text-align: center;
    width: 45px;
    height: 19px;
    border: 1px solid #999
}

.blockSelect a .fa {
    font-size: 0!important;
    line-height: 19px!important;
    display: inline-block
}

.blockSelect a:last-child {
    margin-right: 0!important
}

.blockSelect a:hover {
    color: #000!important
}

.blockSelect a:hover i {
    color: #000!important
}

.blockSelect a.Active i {
    color: #000!important
}



.blockSelect a.sort_3.Active {
    border-color: #333
}



.blockSelect a.sort_4.Active {
    border-color: #333
}



.blockSelect a.sort_hrz.Active {
    border-color: #333
}

#mainHolder_divUstMarkaListesi {
    display: none
}

.proCategoryTitle.categoryTitleText {
    margin-bottom: 10px;
    margin-top: 15px
}

.proCategoryTitle.categoryTitleText ul.breadcrumb {
    border: none!important;
    margin: 0!important
}

.categoryContainer .categoryTitleText {
    width: 100%;
    display: inline-block
}

.productDetailContainer .categoryTitle {
    border: none;
    margin-bottom: 0;
    padding: 0;
    margin-top: 0
}

.breadcrumbContent {
    float: left
}

ul.breadcrumb {
    margin: 0 auto!important;
    float: none!important;
    max-width: 1366px;
    color: #000;
    font-weight: 400;
    text-transform: uppercase;
    line-height: 1;
    font-size: 12px!important;
    display: block!important
}

ul.breadcrumb li {
    color: #000;
    font-weight: 400;
    text-transform: uppercase;
    font-size: 0!important;
    display: inline-block
}

ul.breadcrumb li:last-child {
    color: #000;
    font-size: 11px!important;
    font-weight: 400;
    text-transform: uppercase;
    line-height: 1
}

ul.breadcrumb li:last-child:after {
    display: none!important
}

ul.breadcrumb a {
    color: #000;
    font-size: 11px!important;
    font-weight: 400;
    text-transform: uppercase;
    line-height: 1!important
}

ul.breadcrumb a span {
    color: #000;
    font-size: 11px!important;
    font-weight: 400;
    text-transform: uppercase;
    line-height: 1!important
}

ul.breadcrumb li:after {
    content: '/';
    display: inline-block;
    margin: 0 4px;
    color: #000;
    font-size: 11px!important;
    line-height: 1
}

a#linkOncekiSayfa {
    line-height: 1!important;
    display: inline-block!important;
    color: #000!important;
    font-size: 11px!important;
    font-weight: 400;
    text-transform: uppercase
}

a#linkOncekiSayfa:before {
    content: '\f104';
    float: left;
    line-height: 1;
    font-family: fontawesome;
    margin-right: 5px;
    display: none
}

.sepetItemB4 {
    color: #71034e!important
}

.sepetiTemizle:hover {
    color: #71034e!important
}

.hedefSatisContent:before {
    color: #71034e!important
}

.alisverisedevamet:hover {
    background: #71034e!important;
    border-color: #71034e!important
}

#hed div.hediCekForm a:hover {
    background-color: #71034e!important
}

.userLoginBtn:hover,.userSignBtn:hover {
    background-color: #71034e!important
}

.kirmiziButon {
    background: #71041b!important;
    border: 1px solid #71034e!important
}

.AdresItemAlt.AdresItemSelected .AdresItemAltLeft label span.check {
    color: #71034e!important
}

a.YeniAdresEkle:hover {
    background-color: #71034e!important;
    border-color: #71034e!important;
    color: #fff!important
}

.faturaAdresBtn:hover,.adresAyniBtn:hover {
    color: #71034e!important
}

.faturaAdresBtn.active,.adresAyniBtn.active {
    color: #71034e!important
}

.kirmiziButon:hover {
    color: #fff!important
}

.OdemeMenu ul li.activeMenu>a {
    background-color: #71034e!important
}

.OdemeMenu ul li:hover>a {
    background-color: #71034e!important;
    border-color: #71034e!important
}

.cargoInformation div.cargoName span {
    color: #71034e!important
}

a.YeniAdresEkle {
    color: #71034e!important
}

#divToplamOdeme {
    color: #71034e!important
}



.userLoginBtn {
    background-color: #71034e!important
}

.BasketRigth ul li.genelToplam .tut {
    color: #71034e!important
}

.sepetimBody #footer * {
    display: none
}

.Mobil-uygulama {
    margin-top: 10px;
    width: 100%;
    float: left;
    padding-right: 50px;
    display: none
}

.Mobil-uygulama a {
    margin-bottom: 5px;
    display: block;
    text-align: right;
    width: 50%;
    float: left
}

.Mobil-uygulama a:first-child {
    text-align: left
}

.kombinright_line div>div {
    float: left
}

.dinamikFormContainer label {
    color: #720f1f!important;
    font-size: 15px!important
}

.ProductPreviewItem .divKombinEksecenekTipi {
    float: left;
    width: 100%
}

.BedenBulamiyor {
    width: 100%;
    float: left;
    margin-top: 20px
}

.BedenBul {
    color: #720f1f!important;
    font-size: 15px!important;
    font-weight: 700
}

#BedenForm {
    padding: 30px
}

#BedenForm #ngFormController {
    width: 400px
}

.OzelNewTabSag {
    float: right;
    width: 75%
}

.OzelSayfaSagTab {
    float: left;
    width: 100%;
    margin-bottom: 20px
}

.OzelSayfaSagTab ul {
    float: left;
    width: 100%
}

.OzelSayfaSagTab ul li {
    float: left
}

.OzelSayfaSagTab ul li a {
    font-size: 16px;
    padding: 15px 25px;
    display: block
}

.OzelSayfaSagTab ul li a.active {
    background: #ddd
}

.OzelNewTabSag .OzelSayfaSagTabContent {
    display: none;
    float: left;
    width: 100%
}

.OzelNewTabSag .OzelSayfaSagTabContent.active {
    display: block
}

.Ozelacordion {
    float: left;
    width: 100%;
    margin-bottom: 10px
}

.OzelTabloBaslik {
    float: left;
    width: 100%
}

.OzelTabloBaslik a {
    display: block;
    padding: 15px 5px;
    background: #ddd
}

.OzelTabloBaslik a:after {
    content: "\f107";
    font-family: fontawesome;
    font-size: 25px;
    float: right;
    margin-top: -5px
}

.OzelTabloicerik {
    float: left;
    width: 100%;
    display: none;
    padding: 15px
}

.Ozelacordion.active .OzelTabloicerik {
    display: block
}

.Ozelacordion.active .OzelTabloBaslik a:after {
    content: "\f106"
}

.ozelAlan2 {
    position: absolute;
    right: 0;
    float: right;
    bottom: 35px;
    padding: 0 0
}

.ozelAlan2 span {
    font-size: 11px;
    color: #c00;
    line-height: 9px;
    text-decoration: underline
}

.ozelAlan2 span:nth-child(2) {
    color: #ff5e00;
    font-size: 17px;
    margin-left: 5px;
    position: relative;
    top: 2px
}

#divOzelAlan2 {
    float: left;
    clear: left;
    margin-top: 10px
}

#divOzelAlan2 span {
    font-size: 14px;
    color: red;
    text-decoration: underline;
    font-weight: 700;
    display: block
}

#divOzelAlan2 span:nth-child(2) {
    color: #f49040;
    font-size: 27px;
    position: relative;
    margin-top: 1px
}

#divOzelAlan3 {
    display: block;
    position: relative;
    float: none;
    font-size: 12px;
    color: #c00;
    margin: 10px 0 0 10px;
    float: left;
    display: none
}

#divOzelAlan4 {
    float: left;
    clear: left;
    margin-top: 10px;
    padding-left: 26%;
    font-size: 12px;
    color: gray
}

#divOzelAlan5 {
    display: inline-block
}

.SepetPopupWrap.fancybox-opened {
    z-index: 9999
}

body .ngdialog.ngdialog-theme-default .ngdialog-close:before {
    font-size: 35px
}

body .ngdialog.ngdialog-theme-default .ngdialog-close {
    right: 7px;
    top: 5px
}

.userLoginBtn,.userSignBtn {
    color: #fff;
    background: #000!important
}

.userLoginBtn:hover,.userSignBtn:hover {
    background: #620717!important
}

.userSignUp {
    background: #fff!important;
    color: #000!important;
    border-color: #fff!important
}

.userLogin p.backBtn {
    background: #fff!important;
    border-color: #000!important;
    color: #000!important
}

.userLogin p.backBtn:hover {
    background: #870015!important;
    border-color: #870015!important;
    color: #fff!important
}

.sepetimBody #ticimaxCopyright {
    display: none!important
}

.teknikDetay .teknikDetayItem div.t2 span:after {
    margin: 0 2px
}

#BedenTabloHtml {
    max-width: 800px;
    float: left;
    padding: 25px;
    width: 100%
}

#BedenTabloHtml>ul {
    float: left;
    width: 100%;
    margin-bottom: 10px;
    text-align: center
}

#BedenTabloHtml>ul>li {
    width: auto;
    clear: initial;
    margin-bottom: 0;
    text-align: center;
    display: inline-block
}

#BedenTabloHtml>ul>li>a {
    display: block;
    padding: 15px 20px;
    background: #f7f7f7;
    font-size: 12px
}

#BedenTabloHtml>ul>li:last-child a {
    border: none
}

#BedenTabloHtml>ul>li>a.active {
    background: #3f3f3f;
    color: #fff
}

#BedenTabloHtml .BedenContent {
    display: none
}

#BedenTabloHtml .BedenContent.active {
    display: block
}

#BedenTabloHtml .BedenTabloIcerik {
    text-align: center;
    float: left;
    width: 100%;
    max-height: 500px;
    margin-bottom: 10px;
    overflow: auto
}

#BedenTabloHtml .BedenTabloIcerik img {
    max-width: 100%;
    display: inline-block
}

.BedenAccordion {
    float: left;
    width: 100%;
    margin-top: 10px
}

.BedenAccordionTitle {
    float: left;
    width: 100%;
    margin-bottom: 5px
}

.BedenAccordionTitle a {
    display: block;
    background: #f7f7f7;
    line-height: 40px;
    font-size: 12px
}

.BedenAccordion.active .BedenAccordionTitle a {
    background: #3f3f3f;
    color: #fff
}

.BedenAccordionContent {
    display: none;
    float: left;
    width: 100%
}

.BedenAccordion.active .BedenAccordionContent {
    display: block
}

.ResimGaleri {
    float: left;
    width: 100%;
    margin: 10px 0
}

.ResimGaleri .AllImages {
    line-height: 37px;
    padding: 0 10px;
    background: #9d0000;
    height: 35px;
    display: block;
    color: #fff;
    max-width: 150px;
    text-align: center;
    margin: 0 auto;
    margin-top: 20px
}

.ResimGaleriHeadIcerik {
    margin-bottom: 15px;
    text-align: center;
    font-size: 30px;
    font-weight: 400
}

.ResimGaleri .owl-nav {
    position: absolute;
    left: 0;
    right: 0;
    top: 0;
    bottom: 0;
    margin: auto;
    height: max-content
}

.InstaGallery .InstaGalleryprev,.InstaGallery .InstaGallerynext {
    width: 30px;
    height: 30px;
    background: #fff;
    border-radius: 100%;
    text-align: center;
    line-height: 30px
}

.InstaGallery .InstaGalleryprev {
    float: left
}

.InstaGallery .InstaGallerynext {
    float: right
}

.InstaGallery .InstaGallerynext span,.InstaGallery .InstaGalleryprev span {
    font-size: 25px
}

.InstaGallery .InstaGalleryprev:hover,.InstaGallery .InstaGallerynext:hover {
    background: #9d0000;
    color: #fff
}

.dinamikFormContainer fieldset {
    border-bottom: 1px solid #7c202e!important;
    padding: 0 0 5px!important;
    margin: 0 0 5px!important
}

.RightDetail .dynamicForm {
    margin-top: 23px;
    float: left;
    width: 100%
}

body .KasaOnuFirsatlarContent .owl-nav.disabled+.owl-dots {
    display: none!important
}

body .KasaOnuFirsatlarContent .owl-nav.disabled {
    display: block!important
}

body .hopi-btn {
    padding: 10px 15px
}

body .hopi-btn img {
    padding-right: 15px;
    height: 25px
}

body .hopi-btn-cta-text,body .hopi-btn-used-campaign {
    font-size: 13px;
    margin-top: 6px
}

body .hopi-btn-cta-text {
    background-size: 7px auto;
    min-width: 210px;
    padding-left: 15px
}

.sepetimBody .sozlesmeUyari {
    line-height: 18px;
    margin: 0
}

.sepetimBody .OdemeMenu ul li.activeMenu>a {
    margin-bottom: 20px;
    font-size: 12px!important
}

.sepetimBody .sozlesmeUyari a,.sepetimBody .OdemeMenu ul li.activeMenu a {
    font-size: 14px
}

.sepetimBody .SoslesmeCheck a,.sepetimBody .SoslesmeCheck span {
    font-size: 14px
}

.sepetimBody .OdemeMenu ul li#mainHolder_ucOdeme_liIyziPay>i {
    display: none
}

.sepetimBody #cbMesafeliSatisSozlesme {
    width: 18px;
    height: 19px;
    margin-top: 2px;
    margin-right: 10px
}

.OdemeMenu ul li#mainHolder_ucOdeme_liIyziPay>a i:after {
    content: "\f09d"
}

.OdemeMenu ul.odemeSecenekMenu>li>a>p {
    margin: 0!important;
    display: inline-block
}

body .uyegirisPopup a.fancybox-close {
    top: 5px;
    right: 5px
}

body.sepetimBody .BasketDetail.SiparisNotuContent {
    display: none
}

@media screen and (min-width: 1025px) {
    .category-vertical-filters.top-filters {
        padding:0!important;
        margin-bottom: 15px!important
    }

    .category-vertical-filters.top-filters .panel {
        margin: 0!important;
        padding: 10px 5px;
        background: #f3f3f3
    }

    .category-vertical-filters.top-filters .panel .panel-heading {
        padding: 0!important;
        border-radius: 2px;
        border: none!important
    }

    .category-vertical-filters.top-filters .panel .panel-heading a {
        float: left;
        width: 100%;
        padding: 10px 12px;
        background: #fff;
        line-height: 15px;
        border-radius: 0;
        font-weight: 500;
        color: #7d7d7d;
        font-size: 12px;
        border: 1px solid #e5e5e5
    }

    .category-vertical-filters.top-filters .panel .panel-heading a:after {
        top: 10px!important
    }

    .category-vertical-filters.top-filters .list-group.dropdown {
        top: 100%!important
    }

    .category-vertical-filters.top-filters .panel.vertical-top-price-filter {
        float: left!important;
        margin-top: 15px!important;
        margin-left: 15px!important;
        background: 0 0;
        padding: 0
    }

    .category-vertical-filters.top-filters .ngrs-range-slider {
        background: #fff!important
    }

    .category-vertical-filters.top-filters .ngrs-range-slider .ngrs-runner {
        background: #a5a5a5!important;
        height: 9px;
        margin: 0!important
    }

    .category-vertical-filters.top-filters .ngrs-range-slider .ngrs-join {
        background: #810081!important
    }

    .category-vertical-filters.top-filters .ngrs-range-slider .ngrs-handle {
        background: #fff!important;
        margin-top: -4px;
        width: 16px!important;
        height: 16px!important;
        border-radius: 100%!important;
        border: 2px solid #810081!important
    }

    .category-vertical-filters.top-filters .ngrs-range-slider .ngrs-handle.ngrs-handle-min {
        margin-left: -1px!important
    }

    .category-vertical-filters.top-filters .ngrs-range-slider * {
        color: #7d7d7d;
        font-size: 11px;
        font-weight: 400
    }

    .category-vertical-filters.top-filters .ngrs-range-slider .ngrs-value {
        line-height: 25px!important
    }

    .sortingContent {
        z-index: 10;
        float: right;
        width: 220px;
        background-color: #fff!important;
        border-radius: 0!important;
        border: none;
        margin: 0 0 15px;
        padding: 0;
        display: -webkit-flex;
        display: -moz-flex;
        display: -o-flex;
        position: static
    }

    .sortingContent:before {
        content: "Sıralama Seçiniz";
        float: left;
        width: 100%;
        border-width: 1px;
        border-style: solid;
        border-color: #676767;
        border-image: initial;
        padding: 0 10px;
        height: 30px;
        line-height: 32px;
        text-align: left
    }

    .sortingContent:after {
        content: ""!important;
        font-family: fontawesomepro;
        top: 0;
        position: absolute;
        right: 10px;
        line-height: 32px;
        font-size: 16px
    }

    .sortingContent li:not(.appliedFilter) {
        float: left;
        display: none;
        color: #000!important;
        font-weight: 400!important;
        border-radius: 0!important;
        padding: 0 10px;
        width: 100%;
        border-top: none
    }

    .sortingContent:hover li {
        display: block
    }

    .sortingContent li:not(.appliedFilter):hover {
        background: #000
    }

    .sortingContent li>a {
        position: relative;
        background-color: #fff!important;
        color: #000!important;
        font-size: 12px!important;
        border-radius: 0!important;
        padding: 0!important;
        text-align: left;
        line-height: 15px!important;
        border: none;
        margin-right: 0
    }

    .sortingContent li:not(.appliedFilter):hover a {
        background: #000!important;
        color: #fff!important;
        text-decoration: underline
    }

    .sortingContent li a span {
        font-weight: 400!important;
        line-height: 35px;
        height: 33px;
        display: block
    }

    .sortingContent li a.selected {
        background: #fff!important;
        color: #000!important;
        text-decoration: underline
    }

    .appliedFilter.FiltrelemeUrunAdet span {
        
        font-size: 12px;
        color: #000!important;
        font-weight: 400!important;
        line-height: 19px!important;
        padding: 0;
        display: inline-block!important;
        margin-right: 0!important;
        letter-spacing: 2px;
        padding-top: 6px
    }

    .appliedFilter.FiltrelemeUrunAdet span:after {
        display: none;
        content: 'Bulundu';
        float: right;
        margin-left: -4px;
        font-weight: 600
    }

    .sortingContent .appliedFilter {
        
        background-color: #fff!important;
        height: auto!important;
        display: inline-block!important;
        padding: 0!important
    }

    .appliedFilter.FiltrelemeUrunAdet {
        background: 0 0!important;
        padding: 0!important;
        text-indent: 0!important;
        float: left;
        position: absolute;
        left: 0;
        top: 0
    }

    .sortingContent li .blockSelect {
        display: none
    }

    .filterDeleteContent+div+div+li+.sortingContent {
        top: 62px
    }
}

.leftBlock .category-vertical-filters {
    float: left;
    width: 75%;
    border: none!important;
    border-radius: 0;
    margin: 0!important;
    text-align: center;
    padding: 0!important;
    background-color: transparent!important;
    max-height: 600px!important;
    overflow-x: hidden!important;
    overflow-y: auto!important;
    padding-right: 8px!important
}

.leftBlock .category-vertical-filters::-webkit-scrollbar {
    width: 5px
}

.leftBlock .category-vertical-filters::-webkit-scrollbar-track {
    background: #f6f6f6
}

.leftBlock .category-vertical-filters::-webkit-scrollbar-thumb {
    background: #dbdbdb;
    border-radius: 0
}

.leftBlock .panel-heading {
    float: left;
    padding: 0!important;
    width: 100%!important;
    text-align: left;
    border: none!important;
    border-bottom: none!important;
    margin: 0!important;
    background: 0 0!important
}

.leftBlock .panel-heading a {
    font-size: 11px;
    color: #000;
    width: 100%;
    font-weight: 600;
    float: left;
    background: #fff;
    line-height: 37px;
    text-transform: uppercase
}

.leftBlock .panel-heading a:after {
    content: '\f067';
    font-family: fontawesomepro;
    float: right;
    font-weight: 400
}

.leftBlock .panel-heading.active a:after {
    content: '\f068'
}

.leftBlock .category-vertical-filters>div {
    width: 100%!important;
    padding: 0;
    margin: 0!important;
   
    display: inline-block;
    background: #fff;
    border-bottom: 1px solid gray
}

.leftBlock .category-vertical-filters>div.div-secenek-2 {
    display: none
}

.leftBlock .category-vertical-filters>div:last-child .panel-heading a:after {
    display: none
}

.leftBlock .category-vertical-filters>div.div-kategori .list-group .list-group-item:before {
    display: none!important
}

.leftBlock .category-vertical-filters .vertical-filter-panel .list-group-item.list-group-item-image {
    background: 0 0!important
}

.leftBlock .category-vertical-filters .vertical-filter-panel .list-group {
    float: left;
    text-align: left;
    padding: 0!important;
    width: 100%;
    top: 100%!important;
    margin: 10px 0;
    display: none
}

.leftBlock .category-vertical-filters .vertical-filter-panel.active .list-group {
    display: block
}

.leftBlock .category-vertical-filters .vertical-filter-panel .list-group-item {
    margin: 0 0 12px!important;
    padding: 0!important;
    background-color: transparent!important;
    width: 100%!important;
    height: auto!important
}

.leftBlock .category-vertical-filters .vertical-filter-panel .list-group-item a {
    font-size: 12px!important;
    color: #000;
    font-weight: 400;
    line-height: 10px!important
}

.leftBlock .category-vertical-filters .vertical-filter-panel .list-group-item:before {
    width: 9px!important;
    height: 10px!important;
    border: 1px solid #666!important;
    border-radius: 0;
    background: 0 0!important;
    display: inline-block!important;
    margin-top: 0!important;
    text-align: center;
    line-height: 9px
}

.leftBlock .category-vertical-filters .vertical-filter-panel .list-group-item.selected:before {
    border-color: #666!important;
    background: #fff!important;
    content: '\f00c'!important;
    font-family: fontawesome;
    color: #666;
    font-size: 8px
}

.leftBlock .category-vertical-filters .vertical-filter-panel .list-group-item:hover:before {
    border-color: #666!important;
    background: #fff!important;
    content: '\f00c'!important;
    font-family: fontawesome;
    color: #666;
    font-size: 8px
}

.leftBlock .category-vertical-filters .vertical-filter-panel .list-group {
    max-height: 170px!important;
    overflow-x: hidden!important;
    overflow-y: auto!important
}

.leftBlock .category-vertical-filters .vertical-filter-panel .list-group::-webkit-scrollbar {
    width: 15px
}

.leftBlock .category-vertical-filters .vertical-filter-panel .list-group::-webkit-scrollbar-track {
    background: #f6f6f6
}

.leftBlock .category-vertical-filters .vertical-filter-panel .list-group::-webkit-scrollbar-thumb {
    background: #dbdbdb;
    border-radius: 0
}

.leftBlock .slider-range {
    background: #dedede;
    height: 5px!important;
    width: 93%;
    margin: 0 10px!important;
    border: none;
    float: left
}

.leftBlock .slider-range .ui-slider-range {
    background: #d4d4d4!important;
    height: 5px!important;
    margin-top: 0!important
}

.leftBlock .slider-range .ui-slider-handle {
    background: #444!important;
    border-radius: 100%!important;
    width: 15px!important;
    height: 15px!important;
    border: none!important;
    margin-top: 0!important;
    margin-right: -4px!important;
    top: -5px
}

.leftBlock .amount {
    color: #000;
    font-size: 12px;
    font-weight: 400;
    left: 0;
    padding: 15px 10px 10px;
    float: left;
    width: 100%;
    text-align: left;
    margin-bottom: 0
}

#divFiltreKategoriler {
    padding-bottom: 25px
}

.kategoriOzelBlok {
    min-height: 285px;
    margin-bottom: 22px;
    float: left;
    width: 100%;
    border: 1px solid #ecebeb;
    padding: 32px;
    border-radius: 0
}

.kategoriOzelBlok .kategoriOzelBlokYazi {
    float: left;
    width: 75%;
    padding-right: 15px
}

.kategoriOzelBlok .kategoriOzelBlokYazi h2 {
    color: #46696b;
    font-size: 18px;
    margin-bottom: 15px
}

.kategoriOzelBlok .kategoriOzelBlokYazi p {
    font-size: 14px;
    line-height: 18px;
    color: #46696b
}

.kategoriOzelBlok .kategoriOzelBlokResim {
    float: left;
    width: 25%
}

.kategoriOzelBlok .kategoriOzelBlokResim img {
    width: 100%;
    display: block
}

.KategoriFilitreleme {
    width: 100%;
    float: left
}

.KategoriFilitreTittle {
    width: 100%;
    position: relative;
    border: none;
    color: #373737;
    padding: 10px;
    font-size: 17px;
    font-weight: 500;
    border-top: 1px solid #ddd;
    border-bottom: 1px solid #ddd;
    text-transform: uppercase
}

.FilitreMaxHeight {
    width: 100%
}

.KategoriFilitreLine {
    padding: 20px 10px
}

.fiyatFilitreContent .KategoriFilitreLine {
    width: 97%
}

.kategoriFilitreContent .KategoriFilitreTittle {
    margin-bottom: 0;
    border-top: none;
    border-bottom: 1px solid #ddd
}

.KategoriFilitreLine>ul>li {
    position: relative
}

.KategoriFilitreLine>ul>li>a {
    font-size: 13px;
    color: #373737;
    display: block;
    text-decoration: none;
    margin-bottom: 0!important;
    padding-left: 0;
    line-height: 30px;
    font-weight: 500
}

.KategoriFilitreLine>ul>li:last-child a {
    margin-bottom: 0
}

.KategoriFilitreLine>ul>li:hover>a {
    text-decoration: underline
}

.KategoriFilitreLine>ul>li>ul {
    width: 100%;
    margin: 0;
    border-bottom: 1px solid #ddd
}

.KategoriFilitreLine>ul>li>ul>li>a {
    font-size: 13px;
    padding-left: 22px;
    position: relative;
    display: block;
    line-height: 30px;
    color: #373737;
    font-weight: 500
}

.KategoriFilitreLine>ul>li>ul>li:hover>a {
    text-decoration: underline
}

.KategoriFilitreLine>ul>li>ul>li>ul {
    width: 100%
}

.KategoriFilitreLine>ul>li>ul>li>ul>li {
    padding-left: 5px
}

.KategoriFilitreLine>ul>li>ul>li>ul>li>a {
    font-size: 13px;
    padding-left: 27px;
    color: #373737;
    display: block;
    line-height: 15px;
    font-weight: 500
}

.KategoriFilitreLine>ul>li>ul>li>ul>li:hover>a {
    text-decoration: underline
}

.FilitreMaxHeight table {
    width: 100%
}

.FilitreMaxHeight table tr td {
    width: 100%;
    padding: 5px 0
}

.FilitreMaxHeight table tr td input[type=checkbox] {
    display: none
}

.KategoriFilitreLine table tr td label {
    line-height: 18px;
    display: inline-block;
    padding-left: 27px;
    height: 21px;
    cursor: pointer;
    font-size: 13px;
    font-weight: 500;
    color: #373737
}

.KategoriFilitreLine table tr td label:hover {
    color: #000
}

#divEtiketler {
    float: left;
    width: 100%;
    color: #e30046;
    padding: 30px 0 0
}

#divEtiketler .productModuleTitle {
    float: left;
    color: #393f4f;
    font-size: 12px;
    font-weight: 500
}

#divEtiketler .productModuleTitle:after {
    content: ':';
    float: right;
    margin: 0 5px;
    color: #393f4f;
    font-size: 12px;
    font-weight: 500
}

#divEtiketler a {
    color: #909090;
    font-size: 11px
}

.popupBox {
    width: 80%!important
}

.popupBox input[type=password],.popupBox input[type=text] {
    width: 100%!important;
    padding: 0 10px!important;
    margin-bottom: 7px!important;
    height: 40px!important;
    border: 1px solid #e7e7e7!important
}

.popupBox input[type=password]:focus,.popupBox input[type=text]:focus {
    border-color: #000!important
}

.popupBox input[type=checkbox] {
    margin: 3px 10px 0 0!important
}

.popupBox input[type=radio] {
    margin: 3px 10px 0 0!important;
    float: left
}

.userloginF1 {
    border: none!important
}

.errBoxRegister {
    overflow: hidden
}

.uyePopupContent .button {
    padding: 10px!important
}

.uyePopupCinsiyet {
    margin: 10px 0!important
}

.uyePopupCinsiyet tr td {
    padding-right: 10px!important
}

.popupLogo {
    margin-bottom: 10px
}

.Basketstep ul li i,.sepetTitle .st_1,.sepetTitle2 .st_1,.BasketRigth ul li.genelToplam .tut,.sepetTitle2 .st_1:before,.sepetTitle .st_1:before,.TeslimatAdresTittle,.Basketstep ul li.gecti span,#divToplamOdeme,.TeslimatAdresTittle,a.YeniAdresEkle,.Basketstep ul li.onestepsec span {
    color: #71034e!important
}

.basketCompletebtn {
    background: #620717!important
}

.OdemeMenu ul li.activeMenu {
    border-color: #71034e!important
}

.OdemeMenu ul li:hover {
    border-color: #71034e!important
}

.baglanButton {
    background: #71034e;
    border-color: transparent
}

.baglanButton:hover {
    background: 0 0;
    color: #71034e!important
}

.Basketstep ul li:before {
    border: 1px solid #a21e1f!important
}

.Basketstep ul li.pasif i {
    color: #a21e1f!important
}

.BasketDetail table tbody tr td a {
    display: inherit
}

.BasketDetail table tbody tr td:last-child a {
    display: block
}

#AdresContent .button {
    background: #71034e!important
}

#AdresContent .button:hover {
    background: #71034e!important
}

.siparisOzetTakip {
    background: #71034e!important;
    color: #fff
}

.sepetimBody .hnavigation {
    display: none
}

.sepetimBody #header:after {
    display: none
}

.BasketPage .Basketstep ul li.pasif i {
    color: #71034e!important
}

.BasketPage .cargoInformation div.cargoName span {
    color: #71034e!important
}

.BasketPage a.YeniAdresEkle:hover {
    background-color: #71034e!important;
    border-color: #71034e!important
}

.BasketPage .AdresItemAlt.AdresItemSelected .AdresItemAltLeft label span.check {
    color: #71034e!important
}

.BasketPage .OdemeMenu ul li.activeMenu>a {
    background-color: #71034e!important
}

.BasketPage .OdemeMenu ul li:hover>a {
    background-color: #71034e!important;
    border-color: #71034e!important
}

.markaSlider {
    width: 100%;
    position: relative;
    background: #fff;
    float: left;
    padding: 0 0 20px
}

.markaSlider .categoryTitle {
    text-align: left;
    display: block;
    margin: 0 auto 15px;
    max-width: 1366px;
    float: none;
    width: auto
}

.markaSlider .categoryTitle .bold .satir1 {
    color: #111;
    font-weight: 500;
    font-size: 22px
}

.markaSlider .jCarouselLite {
    width: 100%;
    margin: 0 auto
}

.markaSlider .owl-carousel {
    display: block;
    max-width: 1366px;
    margin: 0 auto
}

.markaSlider:after {
    content: '';
    display: table;
    clear: both
}

.markaSlider:before {
    content: '';
    display: table;
    clear: both
}

.markaSlider ul li a {
    display: block;
    background: #fff;
    overflow: hidden
}

.markaSlider ul li a img {
    display: block;
    max-width: 100%;
    margin: 0 auto
}

.markaSlider .owl-nav {
    position: absolute;
    top: 30%;
    right: 0;
    left: 0
}

.markaSlider .ProductListprev {
    font-size: 0;
    display: inline-block;
    position: absolute;
    cursor: pointer;
    left: 0;
    background: rgba(17,17,17,.15);
    height: 30px;
    width: 28px;
    border-radius: 0 5px 5px 0
}

.markaSlider .ProductListnext {
    font-size: 0;
    display: inline-block;
    position: absolute;
    cursor: pointer;
    right: 0;
    background: rgba(17,17,17,.15);
    height: 30px;
    width: 28px;
    border-radius: 5px 0 0 5px
}

.markaSlider .ProductListprev:after {
    content: '\e875';
    font-family: lineariconsfree;
    font-size: 20px;
    color: #fff;
    line-height: 30px;
    float: left;
    width: 100%;
    text-align: center
}

.markaSlider .ProductListnext:after {
    content: '\e876';
    font-family: lineariconsfree;
    font-size: 20px;
    color: #fff;
    line-height: 30px;
    float: left;
    width: 100%;
    text-align: center
}

#divSizinIcinOnerdiklerimiz {
    float: left;
    width: 100%;
    margin-bottom: 20px
}

#divSizinIcinOnerdiklerimiz .ProductList {
    margin: 0
}

#divSizinIcinOnerdiklerimiz .ItemOrj {
    float: left;
    width: 100%;
    padding: 0
}

#divSizinIcinOnerdiklerimiz .productItem {
    float: left;
    width: 100%;
    margin-bottom: 0
}

#divSizinIcinOnerdiklerimiz .categoryTitle {
    float: left;
    width: 100%;
    text-align: center;
    border-bottom: 1px solid #eee;
    margin-bottom: 25px
}

#divSizinIcinOnerdiklerimiz .categoryTitle span {
    font-size: 18px;
    font-weight: 700;
    color: #b9ce0e;
    text-transform: uppercase;
    line-height: 40px
}

#divSizinIcinOnerdiklerimiz .ProductList {
    float: left;
    display: block;
    width: 100%;
    -webkit-tap-highlight-color: transparent;
    position: relative;
    z-index: 1
}

#divSizinIcinOnerdiklerimiz .ProductList .owl-item {
    position: relative;
    min-height: 1px;
    float: left;
    
    -webkit-tap-highlight-color: transparent;
    -webkit-touch-callout: none;
    -webkit-user-select: none;
    -moz-user-select: none;
    -ms-user-select: none;
    user-select: none
}

#divSizinIcinOnerdiklerimiz .ProductList .owl-item:first-child {
    display: none!important
}

#divSizinIcinOnerdiklerimiz .ProductList .owl-stage-outer {
    position: relative;
    overflow: hidden;
   
}

#divSizinIcinOnerdiklerimiz .ProductList .owl-stage {
    position: relative;
    
}

#divSizinIcinOnerdiklerimiz .owl-dots {
    display: none
}

#divSizinIcinOnerdiklerimiz .owl-nav {
    position: absolute;
    left: 0;
    right: 0;
    top: 50%
}

#divSizinIcinOnerdiklerimiz .ProductListprev {
    font-size: 0;
    display: inline-block;
    position: absolute;
    cursor: pointer;
    left: -52px;
    width: 40px;
    height: 49px;
    border-radius: 0;
    background: #efecec;
    text-align: center
}

#divSizinIcinOnerdiklerimiz .ProductListnext {
    font-size: 0;
    display: inline-block;
    position: absolute;
    cursor: pointer;
    right: -52px;
    width: 40px;
    height: 49px;
    border-radius: 0;
    background: #efecec;
    text-align: center
}

#divSizinIcinOnerdiklerimiz .ProductListnext:after {
    content: '\f105';
    font-family: fontawesome;
    font-size: 18px;
    color: #000;
    line-height: 49px
}

#divSizinIcinOnerdiklerimiz .ProductListprev:after {
    content: '\f104';
    font-family: fontawesome;
    font-size: 18px;
    color: #000;
    line-height: 49px
}

#divSizinIcinOnerdiklerimiz .ProductListnext:hover {
    background: #de0d6a
}

#divSizinIcinOnerdiklerimiz .ProductListprev:hover {
    background: #de0d6a
}

#divSizinIcinOnerdiklerimiz .ProductListnext:hover:after {
    color: #fff
}

#divSizinIcinOnerdiklerimiz .ProductListprev:hover:after {
    color: #fff
}

#divKampanyaBanner {
    float: left;
    width: 100%
}

#divKampanyaBanner .AnasayfaTasarimLine {
    float: left;
    width: 32.8%;
    margin-bottom: 10px;
    margin-right: 10px;
    clear: none
}

#divKampanyaBanner .AnasayfaTasarimLine:nth-child(3n) {
    margin-right: 0
}

#divKampanyaBanner .AnasayfaTasarimLine a {
    display: block;
    position: relative
}

#divKampanyaBanner .AnasayfaTasarimLine a img {
    display: block;
    max-width: 100%;
    margin: 0 auto
}

#divKampanyaBanner .AnasayfaTasarimLine a .AnasayfaTasarimAdi {
    font-size: 0
}

#divKampanyaBanner .AnasayfaTasarimLine a .AnasayfaTasarimAdi .TasarimTime {
    float: left;
    width: 100%;
    background: rgba(165,165,165,.5);
    position: absolute;
    top: 2px;
    text-align: center
}

#divKampanyaBanner .AnasayfaTasarimLine a .AnasayfaTasarimAdi .TasarimTime>span {
    font-size: 14px;
    line-height: 35px;
    color: #000;
    padding: 0 20px;
    display: inline-block;
    
    width: 100%;
    height: 35px;
    text-transform: uppercase;
    text-align: right
}

#header:before,#header:after {
    content: "";
    display: table
}

#header:after {
    clear: both
}

#header {
    clear: both;
    zoom:1}

#back-to-top {
    position: fixed;
    z-index: 99999;
    bottom: 5%;
    right: 2%;
    display: none
}

#back-to-top a {
    display: inline-block;
    width: 39px;
    height: 39px;
}

#header {
    width: 100%;
    position: relative;
    float: left;
    background: #fff;
    border-top: 25px solid #9d0000;
    z-index: 1000
}

.homeHeader {
    margin-bottom: 0!important
}

.headerContent:before {
    content: '';
    display: block;
    clear: both
}

.headerContent:after {
    content: '';
    display: block;
    clear: both
}

#logo {
    text-align: left;
    float: left
}

.sepett:after {
    font-size: 13px;
    line-height: 20px;
    font-weight: 700
}

#logo .logo {
    display: inline-block;
    text-align: center;
    padding: 11px 0;
    position: relative
}

#logo .logo img {
    display: block;
    margin: 0 auto;
    max-width: 100%
}

.mycart {
    float: right;
    z-index: 999;
    position: absolute;
    right: 0;
    top: 19px;
    width: 34px
}

.mycart>a {
    display: block;
    float: left
}

.mycart>a:hover .sepetTecxt {
    text-decoration: underline
}

.mycart .sepetTecxt {
    display: inline-block!important;
    font-size: 10px;
    font-weight: 400;
    color: #565656
}

.mycart .sepetTecxt:before {
    content: '';
    background: url(https://www.tudors.com/CustomCss/4863b978/images/sepetim.png)no-repeat center center;
    width: 100%;
    height: 18px;
    float: left;
    margin-bottom: 7px
}


.mycart .sepetUrunSayisi {
    text-align: center;
    font-size: 11px;
    font-weight: 700;
    position: absolute;
    width: 15px;
    height: 15px;
    border-radius: 100%;
    background: #71034e;
    color: #fff;
    right: 3px;
    top: -3px;
    left: auto;
    line-height: 15px
}

.mycart .sepetUrun {
    display: none
}

.sepetTopTutar {
    display: none!important
}

.mycart:hover .CartProduct {
    display: block!important
}

.CartProduct {
    width: 302px;
    font-family: josefin sans,sans-serif;
    position: absolute;
    top: 100%;
    right: 0;
    display: none;
    z-index: 9999;
    padding: 20px 8px 20px 20px;
    background-color: #fff;
    border: 1px solid #c5c5c5;
    border-radius: 5px
}

.CartProduct .SProduct {
    float: left;
    width: 100%;
    max-height: 305px;
    overflow-y: auto;
    overflow-x: hidden
}

.CartProduct .SProduct li {
    padding-bottom: 18px;
    border-bottom: 1px solid #e2e2e2;
    margin-bottom: 18px;
    float: left;
    width: 100%;
    position: relative
}

.CartProduct .SProduct li a img {
    width: 90px;
    float: left;
    height: auto!important;
    margin-right: 8px
}

.CartProduct .SProduct li .SepettopAd {
    float: left;
    width: calc(100% - 98px);
    margin-top: 10px
}

.CartProduct .SProduct li .SepettopAd span:first-child {
    font-size: 12px;
    color: #4e4e4e;
    float: left;
    width: 100%;
    margin-bottom: 15px
}

.CartProduct .SProduct li .SepettopAd span:last-child {
    font-size: 11px;
    color: #000;
    float: left;
    width: 100%;
    font-weight: 600;
    margin-bottom: 4px
}

.CartProduct .SProduct li .SepettopAd span:last-child:before {
    content: 'Beden :';
    display: inline-block;
    margin-right: 3px
}

.CartProduct .SProduct li .SepetTopAdet {
    color: #000;
    font-size: 11px;
    font-weight: 600;
    float: right;
    margin-right: 3px;
    text-align: left;
    width: 48%
}

.CartProduct .SProduct li .SepetTopbirim {
    color: #000;
    font-size: 11px;
    font-weight: 600;
    float: left
}

.CartProduct .SProduct li .SepetTopbirim:after {
    content: ':';
    margin: 0 3px
}

.CartProduct .SProduct li .SepetTopbirim:before {
    content: 'Adet'
}

.CartProduct .SProduct li .sepetTopFiyat {
    display: inline-block!important;
    font-size: 11px;
    color: #000;
    font-weight: 600;
    
    width: calc(100% - 98px);
    margin-top: 5px
}

.CartProduct .SProduct li .sepetTopFiyat:before {
    content: 'Fiyat :';
    margin-right: 3px
}

.CartProduct .SProduct li a:first-child {
    float: left;
    width: 100%
}

.CartProduct .SPrice {
    float: left;
    width: 100%;
    margin-bottom: 45px
}

.CartProduct .SPrice li {
    float: right;
    color: #000;
    font-size: 15px;
    text-align: left;
    width: 100%;
    line-height: 30px;
    margin: 10px 0
}

.CartProduct .SPrice .sepetToplamTutar {
    font-weight: 700;
    font-size: 15px;
    color: #000;
    line-height: 30px;
    margin-left: 10px;
    float: right
}

.CartProduct .button {
    display: inline-block!important;
    width: 40%;
    background: 0 0;
    padding: 0;
    text-align: center;
    border: 1px solid #bcbcbc!important;
    line-height: 45px;
    color: #000;
    font-weight: 700;
    text-transform: uppercase;
    position: absolute;
    left: 15px;
    bottom: 15px
}

.CartProduct .headerOrderBtn {
    display: inline-block!important;
    color: #fff;
    background: #00aa5b;
    left: auto;
    right: 15px;
    border: none!important
}

.CartProduct .SProduct li a:nth-child(2) {
    position: absolute;
    right: 0;
    top: 0
}

.CartProduct .SProduct li a:nth-child(2) span i {
    color: #a3a3a3;
    font-size: 11px;
    font-weight: 300
}

.divustSepetteUrunYok span {
    width: 100%;
    float: left;
    text-align: center;
    color: #000;
    font-weight: 500;
    line-height: 30px;
    font-size: 20px;
    margin-bottom: 15px
}

.sepetimBody .AllCategory {
    display: none
}

.sepetimBody .linkRebatedProducts {
    margin-left: 0
}

.sepetimBody .searchContent {
    bottom: -10px
}

.CartProduct .SProduct::-webkit-scrollbar {
    width: 15px
}

.CartProduct .SProduct::-webkit-scrollbar-track {
    background: #dbdbdb
}

.CartProduct .SProduct::-webkit-scrollbar-thumb {
    background: #fff;
    border-radius: 0;
    border: 2px solid #dbdbdb
}

.welcome {
    float: right;
    position: absolute;
    top: 43px;
    right: 220px
}

.uyeGirisWelcome,.uyeGirisUyeAdi {
    color: #bababa;
    font-size: 13px;
    float: left;
    line-height: 16px;
    text-transform: uppercase;
    font-weight: 400;
    display: none
}

.headerUyeOl a,.headerUyeGiris a,.headerHesabim,.headerCikis {
    color: #6f6f6f;
    font-size: 11px;
    font-weight: 400;
    padding: 0;
    position: relative;
    float: left
}

.headerUyeOl a:before {
    display: none;
    content: '\f234';
    font-family: fontawesome;
    line-height: 40px;
    font-size: 14px;
    margin-right: 10px
}

.headerUyeGiris a:before {
    display: none;
    content: '\f007';
    font-family: fontawesome;
    line-height: 40px;
    font-size: 14px;
    margin-right: 10px
}

.headerHesabim:before {
    display: none;
    content: '\f007';
    font-family: fontawesome;
    line-height: 40px;
    font-size: 14px;
    margin-right: 10px
}

.headerCikis:before {
    display: none;
    content: '\f011';
    font-family: fontawesome;
    line-height: 40px;
    font-size: 14px;
    margin-right: 10px
}

.headerUyeGiris a:after,.headerHesabim:after {
    content: '&';
    float: right;
    margin: 0 3px
}

.headerUyeOl a:hover,.headerUyeGiris a:hover,.headerHesabim:hover,.headerCikis:hover {
    text-decoration: underline
}

.welcome li {
    display: inline-block;
    
}

.headerSocialConnect {
    display: none!important;
    float: left;
    padding-right: 15px
}

.headerSocialConnect .baglanButton {
    background: 0 0!important;
    border: none;
    margin: 0;
    padding: 0;
    line-height: 0
}

.headerSocialConnect .baglanButton a {
    text-indent: 0;
    color: #fff;
    font-size: 13px;
    line-height: 40px;
    font-weight: 500
}

.headerSocialConnect .baglanButton a:before {
    content: '\f09a';
    font-family: fontawesome;
    float: left;
    line-height: 40px;
    margin-right: 6px
}

.headerSocialConnect .baglanButton a:hover {
    color: #152e59
}

.usernav {
    display: none
}

.searchContent {
    float: left;
    width: 40.1%;
    height: 37px;
    padding: 0;
    z-index: 1;
    border: 1px solid #d0d0d0;
    border-radius: 2px;
    position: absolute;
    bottom: 10px;
    right: 0
}

#divAramaKategori {
    display: none!important;
    position: absolute;
    right: 93px;
    top: 2px
}

#divAramaKategori select {
    display: block;
    height: 38px;
    border: none;
    border-left: 1px solid #dedede;
    width: 159px;
    padding: 0 0 0 10px;
    border-radius: 0;
    line-height: 38px;
    background: #fff;
    color: #333;
    font-size: 13px;
    font-weight: 600
}

.search {
    float: left;
    width: 100%;
    position: relative
}

.ButtonMic {
    display: none!important;
    border: 0;
    background-color: transparent;
    vertical-align: middle;
    position: absolute;
    right: 0;
    top: 50%;
    margin-top: -17px
}

#txtbxArama {
    float: right;
    width: 100%;
    height: 35px;
    border-radius: 2px;
    border: none;
    color: gray;
    padding-left: 20px;
    padding-right: 60px;
    background-color: #fff;
    font-size: 14px;
    font-weight: 400;
    letter-spacing: 2px;
    transition: .3s;
    -webkit-transition: .3s;
    -ms-transition: .3s;
    appearance: none;
    -moz-appearance: none;
    -webkit-appearance: none;
    padding-top: 5px
}

#txtbxArama::-webkit-input-placeholder {
    color: #000
}

#txtbxArama:-moz-placeholder {
    color: #000
}

#txtbxArama::-moz-placeholder {
    color: #000
}

#txtbxArama:-ms-input-placeholder {
    color: #000
}

#txtbxArama:focus {
    color: #000;
    transition: .3s;
    -webkit-transition: .3s;
    -ms-transition: .3s
}

#btnKelimeAra {
    font-size: 0;
    color: #fff;
    font-weight: 700;
    text-transform: uppercase;
    position: absolute;
    right: 0;
    top: 0;
    border: none;
    border-radius: 0;
    padding: 0;
    width: 50px;
    line-height: 38px;
    cursor: pointer;
    z-index: 9;
    appearance: none;
    -moz-appearance: none;
    -webkit-appearance: none
}

.searchContent .ui-widget-content {
    max-height: 250px;
    overflow: hidden;
    overflow-y: auto
}

.homeContainer .ProductListContent {
    float: left;
    width: 100%;
    display: none
}

.homeContainer .ProductListContent .ProductList {
    margin: 0 -5px
}

.homeContainer .ProductListContent .productItem {
    margin-bottom: 20px
}

#divUrunYok {
    display: none
}

.navigationWrapper {
    width: 100%;
    background: #000;
    margin-bottom: 10px;
    position: relative
}

.navigationWrapper:after {
    display: none;
    content: '';
    position: absolute;
    left: 0;
    top: 1px;
    height: 1px;
    width: 100%;
    background: #fff;
    z-index: 9
}

.navigationWrapper:before {
    display: none;
    content: '';
    position: absolute;
    left: 0;
    bottom: 1px;
    height: 1px;
    width: 100%;
    background: #fff;
    z-index: 9
}

.navigationWrapper .headerContent {
    min-height: auto;
    height: auto;
    margin: 0 auto;
    padding: 0
}

.navigation:before {
    content: '';
    display: block;
    clear: both
}

.navigation:after {
    content: '';
    display: block;
    clear: both
}

.navigation {
    position: relative;
    float: right;
    width: 100%;
    border-bottom: 1px solid #b1b1b1
}

.navigation .ResimliMenu1 {
    margin: 0 auto;
    max-width: 1366px;
    position: static;
    text-align: left
}

.navigation .ResimliMenu1>li {
    display: inline-block;
    position: static;
   
}

.navigation .ResimliMenu1>li>a {
    display: inline-block;
    color: #3f3f3f;
    font-size: 15px;
    font-weight: 600;
    position: relative;
    line-height: 41px;
    padding: 0 25px;
    text-transform: uppercase
}

.navigation .ResimliMenu1>li>a img {
    display: none
}

.navigation .ResimliMenu1>li:first-child>a {
    font-size: 0;
    padding: 0 1px
}

.navigation .ResimliMenu1>li:first-child>a:before {
    content: '\f015';
    font-family: fontawesome;
    font-size: 12px;
    float: left;
    width: 100%;
    text-align: center
}

.navigation .ResimliMenu1>li:hover>a:after {
    position: absolute;
    bottom: 1px;
    left: 0;
    right: 0;
    height: 2px;
    border-bottom: 1px solid #ccc;
    background: #333;
    content: '';
    float: left
}

.navigation .ResimliMenu1>li:nth-last-child(2) .altMenu {
    width: 100%
}

.navigation .ResimliMenu1>li:nth-last-child(2) .altMenu .altMenuler .altmenuSol .Menuhtml {
    width: 17%
}

.navigation .ResimliMenu1>li:nth-last-child(2) .altMenu .altMenuler .altmenuSol>ul {
    width: calc(100% - 18%)
}

.navigation .ResimliMenu1>li:nth-last-child(2) .altMenu .altMenuler .altmenuSol>ul>li {
    width: 20%
}

.navigation .ResimliMenu1>li:last-child {
    display: none
}

.backafter:after {
    content: '';
    position: fixed;
    bottom: 0;
    left: 0;
    background: rgba(0,0,0,.67);
    width: 100%;
    height: 100%;
    z-index: 999
}

.navigation .ResimliMenu1>li:hover>.altMenu {
    display: block
}

.navigation .altMenu {
    position: absolute;
    top: 100%;
    left: 0;
    width: 1110px;
    display: none;
    text-align: left;
    z-index: 9999;
    border-top: 4px solid #000
}

.navigation .altMenu .altMenuler {
    display: block;
    background: #fff;
    float: left;
    width: 100%;
    padding: 0;
    border: 1px solid #c6c6c6;
    border-top-color: #777
}

.navigation .altMenu .altMenuler .altMenuSag {
    float: right;
    width: 30%;
    padding: 10px
}

.navigation .altMenu .altMenuler .altMenuSag>a {
    float: right
}

.navigation .altMenu .altMenuler .altMenuSag a img {
    max-width: 100%
}

.navigation .altMenu .altMenuler .altmenuSol {
    float: left;
    width: calc(100% - 30%)
}

.navigation .altMenu .altMenuler .altmenuSol h4,.altMenu .altMenuler .altmenuSol>span {
    display: none
}

.navigation .altMenu .altMenuler .altmenuSol h4 * {
    display: block;
    color: #000;
    font-size: 14px;
    padding: 3px 15px;
    border-bottom: 1px solid #6f6e6e;
    margin-bottom: 15px
}

.navigation .altMenu .altMenuler .altmenuSol>ul {
    display: inline-block;
    width: calc(100% - 31%)
}

.navigation .altMenu .altMenuler .altmenuSol>ul>li {
    display: block;
    width: 33%;
    float: left;
    border-left: 1px solid #cecece;
    padding: 12px 0 20px 15px
}

.navigation .altMenu .altMenuler .altmenuSol>ul>li>a {
    font-size: 14px;
    color: #000;
    font-weight: 700;
    margin-bottom: 5px;
    display: inline-block;
    width: 100%
}

.navigation .altMenu .altMenuler .altmenuSol>ul>li>a img {
    display: none
}

.navigation .altMenu .altMenuler .altmenuSol>ul>li>ul>li>a {
    color: #000;
    font-size: 14px;
    font-weight: 400;
    padding: 10px 0;
    display: inline-block
}

.navigation .altMenu .altMenuler .altmenuSol>ul>li>ul>li>a img {
    display: none
}

.navigation .altMenu .altMenuler .altmenuSol>ul>li>ul>li>a:hover {
    text-decoration: underline
}

.navigation .altMenu .altMenuler .altmenuSol .Menuhtml {
    float: left;
    width: 30%;
    padding-top: 12px;
    padding-bottom: 20px;
    padding-left: 20px
}

.navigation .altMenu .altMenuler .altmenuSol .Menuhtml ul {
    float: left;
    width: 100%
}

.navigation .altMenu .altMenuler .altmenuSol .Menuhtml ul li {
    float: left;
    width: 100%
}

.navigation .altMenu .altMenuler .altmenuSol .Menuhtml ul li a img {
    display: none
}

.navigation .altMenu .altMenuler .altmenuSol .Menuhtml>ul>li>a {
    font-size: 14px;
    color: #000;
    font-weight: 400;
    padding: 10px 0;
    display: inline-block;
    width: 100%
}

.navigation .altMenu .altMenuler .altmenuSol .Menuhtml>ul>li:first-child>a {
    font-size: 15px
}

.navigation .altMenu .altMenuler .altmenuSol .Menuhtml>ul>li>ul>li>a {
    color: #000;
    font-size: 14px;
    font-weight: 400;
    padding: 10px 0;
    display: inline-block
}

.navigation .altMenu .altMenuler .altmenuSol .Menuhtml>ul>li>ul>li>a:hover {
    text-decoration: underline
}

.navigation .HeaderMenu2 {
    margin: 0 auto;
    max-width: 1366px;
    position: relative;
    text-align: left
}

.navigation .HeaderMenu2>li {
    display: inline-block;
    position: relative;
    
}

.navigation .HeaderMenu2>li>a {
    display: inline-block;
    color: #6d6d6d;
    font-size: 12px;
    font-weight: 700;
    position: relative;
    line-height: 41px;
    padding: 0 20px;
    text-transform: uppercase
}

.navigation .HeaderMenu2>li>ul {
    display: none;
    width: 240px;
    position: absolute;
    left: 0;
    top: 100%;
    background: rgba(149,149,149,.7);
    padding: 0;
    z-index: 3;
    padding: 10px 0
}

.navigation .HeaderMenu2>li>ul>li {
    float: left;
    width: 100%
}

.navigation .HeaderMenu2>li>ul>li>a {
    display: block;
    color: #fff;
    font-size: 14px;
    font-weight: 700;
    text-align: left;
    line-height: 41px;
    padding: 0 20px;
    text-transform: uppercase
}

.navigation .HeaderMenu2>li>ul>li>ul {
    display: none;
    width: 520px;
    position: absolute;
    left: 100%;
    top: 0;
    background: #fff;
    padding: 20px;
    border-bottom: 6px solid rgba(252,37,156,.6)
}

.navigation .HeaderMenu2>li>ul>li>ul>li>ul {
    float: left;
    width: 100%;
    position: relative
}

.navigation .HeaderMenu2>li>ul>li>ul>li>ul:after {
    content: '';
    position: absolute;
    right: 0;
    top: 25%;
    bottom: 25%;
    width: 1px;
    background: #e5e5e5
}

.navigation .HeaderMenu2>li>ul>li>ul>li:nth-child(2n)>ul:after {
    display: none
}

.navigation .HeaderMenu2>li>ul>li>ul>li>ul>li>a {
    display: inline-block;
    color: #a5a5a5;
    font-size: 12px;
    font-weight: 400;
    text-align: left;
    line-height: 40px;
    text-transform: uppercase;
    transition: all .3s ease;
    -webkit-transition: all .3s ease;
    -moz-transition: all .3s ease;
    -o-transition: all .3s ease
}

.navigation .HeaderMenu2>li>ul>li>ul>li>ul>li:hover>a {
    padding-left: 5px
}

.navigation .HeaderMenu2>li>ul>li>ul>li {
    float: left;
    width: 50%;
    position: relative;
    padding-right: 25px
}

.navigation .HeaderMenu2>li>ul>li>ul>li>a {
    display: inline-block;
    color: #a5a5a5;
    font-size: 12px;
    font-weight: 400;
    text-align: left;
    line-height: 40px;
    text-transform: uppercase;
    transition: all .3s ease;
    -webkit-transition: all .3s ease;
    -moz-transition: all .3s ease;
    -o-transition: all .3s ease
}

.navigation .HeaderMenu2>li>ul>li>ul>li:hover>a {
    padding-left: 5px
}

.navigation .HeaderMenu2>li:hover>ul {
    display: block
}

.navigation .HeaderMenu2>li>ul>li:hover>ul {
    display: block
}

.navigation .HeaderMenu2>li>ul>li.AcilirMenu>a:after {
    content: '\f105';
    font-family: fontawesome;
    color: #fff;
    float: right
}

.menuItemTittle {
    display: none
}

.navigation .ResimliMenu2 {
    max-width: 1366px;
    margin: 0 auto;
    display: block;
    padding-left: 150px;
    position: relative
}

.navigation .ResimliMenu2>li {
    float: left;
    padding: 0 30px
}

.navigation .ResimliMenu2>li>a {
    color: #fff;
    font-size: 14px;
    font-weight: 500;
    line-height: 50px
}

.yanResimliMenu {
    display: none
}

#pnlSlider {
    width: 100%;
    float: left;
    position: relative;
    margin-bottom: 20px;
    margin-top: 17px
}

#pnlSlider ul li a {
    display: block
}

#pnlSlider ul li a img {
    max-width: 100%
}

#pnlSlider .flex-control-nav {
    float: left;
    position: absolute;
    bottom: 12px;
    right: 0;
    left: 0;
    width: auto
}

#pnlSlider .flex-control-paging li {
    margin: 0 2px!important;
    display: inline-block
}

#pnlSlider .flex-control-paging li a {
    width: 23px;
    height: 23px;
    text-indent: -9999px;
    text-align: center;
    display: inline-block;
    border-radius: 100%;
    border: 1px solid #272727;
    box-shadow: none;
    background: #fff
}

#pnlSlider .flex-control-paging li a.flex-active {
    background: #000;
    border-color: #272727
}

#pnlSlider .flex-direction-nav {
    position: absolute;
    top: 45%;
    left: 0;
    right: 0
}

#pnlSlider .flex-direction-nav .flex-prev,#pnlSlider .flex-direction-nav .flex-next {
    z-index: 99;
    font-size: 0;
    text-align: center;
    top: 0;
    margin: 0;
    opacity: 1!important;
    height: 58px;
    border-radius: 0;
    cursor: pointer
}

#pnlSlider .flex-direction-nav .flex-prev {
    left: 12px
}

#pnlSlider .flex-direction-nav .flex-next {
    right: 12px
}

#pnlSlider .flex-direction-nav .flex-prev:before {
    content: '\e875';
    font-family: lineariconsfree;
    font-size: 50px;
    display: inline-block;
    color: #fff;
    line-height: 58px
}

#pnlSlider .flex-direction-nav .flex-prev:after {
    content: '\e875';
    font-family: lineariconsfree;
    font-size: 50px;
    display: inline-block;
    color: #8b8b8b;
    line-height: 58px;
    position: absolute;
    right: 0;
    top: 0
}

#pnlSlider .flex-direction-nav .flex-next:before {
    content: '\e876';
    font-family: lineariconsfree;
    font-size: 50px;
    display: inline-block;
    color: #8b8b8b;
    line-height: 58px
}

#pnlSlider .flex-direction-nav .flex-next:after {
    content: '\e876';
    font-family: lineariconsfree;
    font-size: 50px;
    display: inline-block;
    color: #fff;
    line-height: 58px;
    position: absolute;
    right: 0;
    top: 0
}

#pnlSlider .flex-direction-nav a:before {
    text-shadow: none
}

#pnlSlider .flex-direction-nav a:after {
    text-shadow: none
}

.flex-control-thumbs li {
    width: 65px!important;
    height: 40px;
    margin-right: 10px!important
}

.flex-control-thumbs li img {
    max-width: 100%!important;
    width: 65px!important
}

.yanResimliMenuContent .UrunGuruplari {
    float: left;
    width: 232px;
    border: 2px solid #ffd400;
    margin-top: -49px;
    border-radius: 5px
}

.yanResimliMenuContent .UrunGuruplari .Block_Title {
    display: inline-block!important;
    
    width: 100%;
    color: #fff;
    background: #ffd400;
    font-size: 16px;
    padding-left: 20px
}

.yanResimliMenuContent .UrunGuruplari .Block_Title span {
    font-weight: 500;
    line-height: 47px
}

.yanResimliMenuContent .UrunGuruplari .KatMenu1 {
    float: left;
    width: 100%;
    background: #fff;
    padding: 0 18px
}

.yanResimliMenuContent .UrunGuruplari .KatMenu1>li {
    float: left;
    width: 100%;
    border-bottom: 1px solid #eee
}

.yanResimliMenuContent .UrunGuruplari .KatMenu1>li:last-child {
    border-bottom: none
}

.yanResimliMenuContent .UrunGuruplari .KatMenu1>li>a {
    float: left;
    width: 100%;
    line-height: 42px;
    color: #2c2c2c;
    font-weight: 500;
    font-size: 13px
}

.yanResimliMenuContent .UrunGuruplari .KatMenu1>li>a:hover {
    color: #ffd400
}

.yanResimliMenuContent .UrunGuruplari .KatMenu1>li>ul {
    display: none
}

.yanResimliMenuContent .UrunGuruplari .KatMenu1>li:nth-child(1)>a:before {
    content: '';
    float: left;
    height: 42px;
    width: 31px;
}

.yanResimliMenuContent .UrunGuruplari .KatMenu1>li:nth-child(2)>a:before {
    content: '';
    float: left;
    height: 42px;
    width: 31px;
}

.yanResimliMenuContent .UrunGuruplari .KatMenu1>li:nth-child(3)>a:before {
    content: '';
    float: left;
    height: 42px;
    width: 31px;
}

.yanResimliMenuContent .UrunGuruplari .KatMenu1>li:nth-child(4)>a:before {
    content: '';
    float: left;
    height: 42px;
    width: 31px;
}

.yanResimliMenuContent .UrunGuruplari .KatMenu1>li:nth-child(5)>a:before {
    content: '';
    float: left;
    height: 42px;
    width: 31px;
}

.yanResimliMenuContent .UrunGuruplari .KatMenu1>li:nth-child(6)>a:before {
    content: '';
    float: left;
    height: 42px;
    width: 31px;
}

.ProductBody .UrunGuruplari {
    position: relative;
    border-radius: 5px 5px 0 0;
    border: none
}

.ProductBody .UrunGuruplari .Block_Title {
    border-radius: 5px 5px 0 0
}

.ProductBody .UrunGuruplari .Block_Title span {
    line-height: 49px
}

.ProductBody .UrunGuruplari .Block_Text {
    display: none;
    position: absolute;
    top: 100%;
    left: 0;
    border: 2px solid #ffd400;
    border-top: none;
    border-radius: 0 0 5px 5px;
    z-index: 999
}

.ProductBody .UrunGuruplari:hover .Block_Text {
    display: block
}

.navigation .yanResimliMenuContent {
    position: absolute;
    left: 0;
    top: 0
}

.navigation .yanResimliMenuContent .UrunGuruplari {
    position: absolute;
    left: 0;
    top: 0;
    margin-top: 0;
    position: relative;
    border-radius: 5px 5px 0 0;
    border: none
}

.navigation .yanResimliMenuContent .UrunGuruplari .Block_Title {
    border-radius: 5px 5px 0 0
}

.navigation .yanResimliMenuContent .UrunGuruplari .Block_Title span {
    line-height: 49px
}

.navigation .yanResimliMenuContent .UrunGuruplari .Block_Text {
    display: none;
    position: absolute;
    top: 100%;
    left: 0;
    border: 2px solid #ffd400;
    border-top: none;
    border-radius: 0 0 5px 5px;
    z-index: 999
}

.navigation .yanResimliMenuContent .UrunGuruplari:hover .Block_Text {
    display: block
}

.resimliYanMenu {
    float: left;
    width: 280px;
    border: 2px solid #ed4b1f
}

.resimliYanMenu .Block_Title {
    display: block!important;
    background: #ed4b1f;
    padding: 1px;
    float: left;
    width: 100%
}

.resimliYanMenu .Block_Title span {
    float: left;
    line-height: 56px;
    color: #fff;
    font-weight: 700;
    font-size: 16px;
    text-indent: 33px;
    position: relative;
    text-transform: uppercase
}

.resimliYanMenu .Block_Title span:before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    margin-left: 0;
    width: 0;
    height: 0;
    border-top: 17px solid #fff;
    border-right: 17px solid transparent
}

.resimliYanMenu .lfMenuUl {
    float: left;
    width: 100%
}

.resimliYanMenu .lfMenuUl>li {
    float: left;
    width: 100%;
    padding: 7.5px 0;
    border-bottom: 1px solid #f5f5f7;
    position: relative
}

.resimliYanMenu .lfMenuUl>li>a {
    float: left;
    border-left: 4px solid #ed4b1f;
    font-size: 14px;
    font-weight: 600;
    color: #000;
    line-height: 25px;
    padding-left: 2px;
    width: 100%
}

.resimliYanMenu .lfMenuUl>li:hover>a {
    color: #ed4b1f
}

.resimliYanMenu .lfMenuUl>li>a:before {
    content: '\f0da';
    float: left;
    font-family: fontawesome;
    color: #ed4b1f;
    margin-right: 20px
}

.resimliYanMenu .lfMenuUl>li.ulVar>a:after {
    content: '\f105';
    float: right;
    font-family: fontawesome;
    color: #a0a0a0;
    position: absolute;
    right: 20px;
    top: 10px
}

.resimliYanMenu .lfMenuUl>li.ulVar:hover>a:after {
    color: #ed4b1f
}

.resimliYanMenu .lfMenuUl>li:hover>.lfMenuAltContent {
    display: block
}

.resimliYanMenu .lfMenuUl>li>.lfMenuAltContent {
    display: none;
    float: left;
    padding: 22px;
    background: #fff;
    position: absolute;
    left: 100%;
    top: 0;
    z-index: 9999;
    width: 500px
}

.resimliYanMenu .lfMenuUl>li>.lfMenuAltContent .altMenu_Tittle {
    display: none
}

.resimliYanMenu .lfMenuUl>li>.lfMenuAltContent .altMenu_Resim {
    float: left
}

.resimliYanMenu .lfMenuUl>li>.lfMenuAltContent .altMenu_Resim_RowItem {
    float: left;
    width: 20%;
    margin-right: 28px;
    position: relative;
    margin-bottom: 35px
}

.resimliYanMenu .lfMenuUl>li>.lfMenuAltContent .altMenu_Resim_RowItem:nth-child(4n) {
    margin-right: 0
}

.resimliYanMenu .lfMenuUl>li>.lfMenuAltContent .altMenu_Resim_RowItem>a {
    position: absolute;
    left: 0;
    top: 0;
    right: 0;
    bottom: 0
}

.resimliYanMenu .lfMenuUl>li>.lfMenuAltContent .altMenu_Resim_RowItem .altMenuItemR {
    float: left;
    width: 81px;
    margin-bottom: 15px
}

.resimliYanMenu .lfMenuUl>li>.lfMenuAltContent .altMenu_Resim_RowItem .altMenuItemN {
    float: left;
    width: 81px;
    text-align: center;
    font-size: 12px;
    color: #000;
    font-weight: 600
}

#footer {
    float: left;
    width: 100%;
    position: relative;
    background: #fff;
    margin-top: 130px
}

.footerGenelTutucu {
    float: left;
    width: 100%;
    position: relative;
    border-top: 2px solid #dfdfdf
}

.footerGenelTutucu:before,.footerGenelTutucu:after {
    content: "";
    display: table
}

.footerGenelTutucu:after {
    clear: both
}

.noProduct {
    width: 212px;
    height: 214px
}

.noProduct * {
    display: none!important
}

.anasayfaBloklar {
    float: left;
    width: 100%
}

.anasayfaBloklar .blokRow {
    margin: 0 -10px
}

.anasayfaBloklar .tekliBlok {
    float: left;
    width: 100%;
    padding: 0 10px;
    margin-bottom: 20px
}

.anasayfaBloklar .ucluBlok {
    float: left;
    width: 33.33%;
    padding: 0 10px;
    margin-bottom: 20px
}

.anasayfaBloklar .ucluBlok .blok {
    float: left;
    width: 100%;
    margin-bottom: 20px
}

.anasayfaBloklar .ucluBlok .blok:last-child {
    margin-bottom: 0
}

.anasayfaBloklar .ikiliBlok {
    float: left;
    width: 50%;
    padding: 0 10px;
    margin-bottom: 20px
}

.anasayfaBloklar .dortluBlok {
    float: left;
    width: 25%;
    padding: 0 10px;
    margin-bottom: 20px
}

.anasayfaBloklar a {
    display: block;
    position: relative
}

.anasayfaBloklar a img {
    display: block;
    max-width: 100%;
    margin: 0 auto
}

.Instagram {
    float: left;
    width: 100%;
    margin: 65px 0 60px
}

.instagramtext {
    float: left;
    width: 100%;
    padding: 0 105px;
    margin-bottom: 40px;
    position: relative
}

.instagramtext:before {
    position: absolute;
    bottom: 59%;
    left: 0;
    width: 100%;
    background: #ffc245;
    height: 1px;
    content: '';
    z-index: -1
}

.instagramtext:after {
    content: '';
    width: 100%;
    text-align: center;
    height: 83px;
    position: absolute;
    left: 0;
    top: -34px;
    z-index: -1
}

.instagramtext .titleText {
    float: left;
    width: 180px;
    background: #fff;
    color: #ffc245;
    font-size: 45px;
    text-align: center;
    line-height: 49px;
    margin-top: -15px
}

.instagramtext .itakip {
    float: right;
    width: 180px;
    background: #fff;
    color: #ffc245;
    text-align: center;
    margin-top: -4px
}

.instagramtext .itakip i {
    font-size: 18px
}

.instagramtext .itakip a {
    width: 100px;
    height: 35px;
    line-height: 35px;
    border: 1px solid #ffc245;
    border-radius: 25px;
    text-align: center;
    display: inline-block;
    font-size: 14px;
    color: #ffc245;
    margin-left: 20px
}

.instagramBolumu {
    float: left;
    width: 100%
}

.blokRow {
    float: left;
    width: 100%
}

.dortluBlok {
    float: left;
    width: 180px;
    margin-right: 30px
}

.dortluBlok:last-child {
    margin-right: 0
}

.dortluBlok a {
    position: relative
}

.dortluBlok a img {
    max-width: 100%
}

.HesabimContainer .categoryTitle .categoryTitleText {
    width: 100%!important;
    margin-bottom: 20px;
    font-size: 13px
}

.iletisimContent .iletisimLeft .categoryTitle .categoryTitleText {
    width: 100%!important;
    margin-bottom: 0;
    font-size: 15px;
    color: #000;
    line-height: 35px;
    font-weight: 600;
    text-transform: uppercase;
    letter-spacing: 1px
}

.menuUstBolum {
    width: 100%;
    overflow: hidden
}

.mobilMenuAcButton {
    position: absolute;
    left: 10px;
    color: #505050;
    font-size: 25px;
    display: none;
    bottom: 5px;
    width: 52px
}

.mobilMenuAcButton span {
    color: #505050;
    font-size: 11px;
    width: 100%;
    float: left;
    font-weight: 600;
    display: none
}

.mobilMenuAcButton i.fa-search {
    float: right;
    margin-left: 5px;
    font-size: 22px;
    display: none
}

.mobilMenuAcButton i.fa-bars {
    margin-top: 0;
    float: left
}

.mobilMenuKapat {
    
    display: inline-block;
    background: #cc1332;
    text-align: center;
    font-size: 14px;
    width: 30px;
    height: 30px;
    margin-bottom: 7px;
    color: #fff
}

.mobilMenuKapat .fa {
    line-height: 30px
}

.mobilMenu {
    width: 85%;
    height: 100%;
    background: #fff;
    position: fixed;
    top: 0;
    left: -100%;
    z-index: 99999999;
    overflow-y: auto;
    padding: 10px;
    transition: all .3s ease;
    -webkit-transition: all .3s ease;
    -moz-transition: all .3s ease;
    -o-transition: all .3s ease;
    -webkit-overflow-scrolling: touch;
    -ms-overflow-style: -ms-autohiding-scrollbar
}

.mobilMenu.acik {
    left: 0
}

.mobilMenu .mmenu {
    float: left;
    width: 100%;
    margin-top: 10px
}

.mobilMenu .lfMenuUl {
    float: left;
    width: 100%
}

.mobilMenu .lfMenuUl>li {
    float: left;
    width: 100%;
    margin-bottom: 10px;
    position: relative
}

.mobilMenu .lfMenuUl>li.active {
    position: static
}

.mobilMenu .lfMenuUl>li>a {
    border-radius: 1.5px;
    font-family: futura pt;
    color: #2d2d2d;
    font-size: 13px;
    line-height: 49px;
    background: #e1e1e1;
    display: block;
    padding-left: 10px;
    height: 61px;
    float: left;
    width: 100%;
    letter-spacing: 1px;
    text-transform: uppercase
}

.mobilMenu .lfMenuUl>li>a span {
    font-weight: 900;
    float: left;
    height: 61px;
    display: -webkit-box;
    display: -moz-box;
    display: -ms-flexbox;
    display: -webkit-flex;
    display: flex;
    align-items: center;
    -webkit-align-items: center;
    justify-content: center;
    -webkit-justify-content: center
}

.mobilMenu .lfMenuUl>li:last-child>a span {
    height: auto;
    font-weight: 600
}

.mobilMenu .lfMenuUl>li:first-child>a span {
    height: auto
}

.mobilMenu .lfMenuUl>li>a img {
    max-width: 61px;
    float: right
}

.mobilMenu .lfMenuUl>li .mobilAcilirMenu {
    position: absolute;
    left: 0;
    top: 0;
    height: 97px;
    right: 0
}

.mobilMenu .lfMenuUl>li .mobilAcilirMenu i {
    display: none
}

.mobilMenu .lfMenuUl .lfMenuAltContent {
    position: fixed;
    left: -100%;
    top: 0;
    bottom: 0;
    padding: 0 10px 10px;
    background: #fff;
    z-index: 1;
    width: 85%;
    transition: all .3s ease;
    -webkit-transition: all .3s ease;
    -moz-transition: all .3s ease;
    -o-transition: all .3s ease
}

.mobilMenu .lfMenuUl .lfMenuAltContent.active {
    left: 0
}

.mobilMenu .lfMenuUl .altMenu_1 .altMenu_List {
    float: left;
    width: 100%;
    position: absolute;
    left: 0;
    top: 54px;
    background: #fff;
    padding: 0 10px;
    height: calc(100% - 54px);
    overflow-y: auto;
    overflow-x: hidden
}

.mobilMenu .lfMenuUl .altMenu_1 .altMenu_Tittle {
    float: left;
    width: 100%;
    position: relative;
    text-align: center;
    border-bottom: 1px solid #d6d6d6
}

.mobilMenu .lfMenuUl .altMenu_1 .altMenu_Tittle .Gribtn {
    position: absolute;
    left: 0;
    top: 0;
    bottom: 0;
    right: 0;
    font-size: 20px
}

.mobilMenu .lfMenuUl .altMenu_1 .altMenu_Tittle .Gribtn i {
    float: left;
    line-height: 53px;
    font-weight: 600
}

.mobilMenu .lfMenuUl .altMenu_1 .altMenu_Tittle {
    line-height: 53px;
    display: inline-block;
    vertical-align: top;
    color: #2d2d2d;
    font-size: 16px;
    font-family: futura pt;
    font-weight: 900
}

.mobilMenu .lfMenuUl .altMenu_1 .altMenu_List ul {
    float: left;
    width: 100%
}

.mobilMenu .lfMenuUl .altMenu_1 .altMenu_List ul li {
    float: left;
    width: 100%
}

.mobilMenu .lfMenuUl .altMenu_1 .altMenu_List ul li a {
    color: #2d2d2d;
    font-size: 16px;
    font-family: futura pt book;
    font-weight: 300;
    float: left;
    width: 100%;
    line-height: 55px;
    border-bottom: 1px solid #d6d6d6
}

.mobilMenu .lfMenuUl .altMenu_1 .altMenu_List ul li a span {
    font-weight: 300
}

.mobilMenu .lfMenuUl .altMenu_1 .altMenu_List ul li a img {
    display: inline-block;
    vertical-align: top;
    margin-top: 8px;
    margin-right: 12px
}

.mobilMenu .lfMenuUl .altMenu_1 .altMenu_List ul li.imgsiz a {
    color: red
}

.mobilaf {
    position: fixed;
    right: -100%;
    top: 0;
    width: 100%;
    height: 100%;
    background: rgba(0,0,0,.43);
    z-index: 999;
    transition: all .1s ease;
    -webkit-transition: all .1s ease;
    -moz-transition: all .1s ease;
    -o-transition: all .1s ease
}

.mobilaf.acik {
    right: 0;
    left: 0
}

.mobilmenureklam {
    display: none
}

.mobilMenu .mobilmenureklam {
    display: block
}

.mobilMenu .lfMenuUl>li.mobilmenureklam>a {
    height: auto;
    padding: 0;
    line-height: 0
}

.mobilMenu .lfMenuUl>li.mobilmenureklam>a img {
    float: none;
    max-width: 100%
}

#storeCitys,#searchStore {
    margin-top: 10px!important
}

#storeCountries {
    margin-top: 10px
}

.mgz h4 {
    width: 100%
}

.mgz img {
    display: none!important
}

#searchStore input {
    appearance: none;
    -moz-appearance: none;
    -webkit-appearance: none;
    height: auto
}

#storeCitys {
    appearance: none;
    -moz-appearance: none;
    -webkit-appearance: none
}

#searchStore .buton {
    line-height: 39px!important
}

.magazaSelect {
    font-size: 13px;
    -webkit-appearance: none;
    -moz-appearance: none;
    appearance: none;
    position: relative;
}

.ui-accordion .ui-accordion-header {
    background: none #f6f6f6!important;
    padding: 0 10px 0 20px!important;
    min-height: 36px!important;
    line-height: 36px!important;
    display: block!important;
    cursor: pointer!important;
    position: relative!important;
    margin-top: 10px!important;
    z-index: 1!important;
    font-size: 13px!important;
    border: 0!important;
    border-radius: 0!important
}

.ui-accordion .ui-accordion-content {
    border: 1px solid #d8d8d8!important;
    padding: 10px 20px;
    line-height: 20px
}

p.ui-widget-content {
    color: #676363!important;
    font-size: 13px
}

.ui-state-active,.ui-widget-content .ui-state-active,.ui-widget-header .ui-state-active {
    color: #454545!important
}

.ui-accordion .ui-accordion-header .ui-accordion-header-icon {
    width: 15px;
    height: 15px!important;
    display: inline-block!important;
    background: 0 0;
    position: absolute!important;
    right: 20px!important;
    top: 10px!important;
    left: auto!important;
    margin: 0!important;
    font-size: 12px!important
}

.ui-accordion .ui-accordion-header .ui-accordion-header-icon:after {
    content: '\e874';
    font-family: lineariconsfree;
    font-size: 15px;
    color: #000;
    float: left;
    line-height: 1;
    text-indent: 0
}

.ui-accordion .ui-accordion-header .ui-accordion-header-icon.ui-icon-triangle-1-s:after {
    content: '\e873'
}

.bkmExpressBtn {
    float: left;
    width: 25%!important;
    height: 50px!important;
    transition-duration: .2s,.2s;
    -webkit-transition-duration: .2s,.2s;
    background: #fff!important;
    padding: 0;
    float: left;
    padding: 17px 10px!important;
    margin-bottom: 20px;
    display: block;
    transition-duration: .2s,.2s;
    -webkit-transition-duration: .2s,.2s;
    color: #a5a5a5!important;
    font-size: 13px!important;
    padding: 17px 0;
    height: 50px;
    border: 1px solid #e5e5e5;
    font-weight: 500;
    margin-bottom: 0!important
}

.bkmExpressBtn:before {
    content: "\f282";
    font-family: fontawesome;
    color: #000;
    font-size: 17px;
    margin-right: 7px
}

.bkmExpressBtn:hover {
    border-color: #71034e!important;
    background: #71034e!important;
    color: #fff!important
}

.bkmExpressBtn:hover:before {
    color: #fff
}

.cookietudors {
    position: fixed;
    right: 0;
    bottom: 0;
    background: rgba(13,13,13,.8);
    width: 89%;
    color: #fff;
    left: 5px;
    right: 5px;
    bottom: 5px;
    padding: 11px 83px 43px 10px;
    z-index: 99999999999;
    text-align: center
}

.kapatx {
    display: block;
    position: absolute;
    right: 15%;
    top: 43%;
    margin-top: -8px;
    padding: 5px;
    border-radius: 1.5px;
    font-weight: 300;
    border: 1px solid;
    width: 99px;
    overflow: hidden;
    font-size: 16px;
    color: #fff;
    cursor: pointer
}

.kapatx i {
    display: inline-block;
    vertical-align: top
}

.cookietudors a {
    color: #fff;
    font-weight: 300;
    text-decoration: underline
}

.OzelSayfaContent {
    float: left;
    width: 100%;
    margin-top: 55px
}

.OzelSayfaContent .OzelSayfaSol {
    float: left;
    width: 25%;
    padding-right: 30px
}

.OzelSayfaContent .OzelSayfaSol ul {
    float: left;
    width: 100%
}

.OzelSayfaContent .OzelSayfaSol ul li {
    float: left;
    width: 100%
}

.OzelSayfaContent .OzelSayfaSol>ul>li {
    margin-bottom: 18px
}

.OzelSayfaContent .OzelSayfaSol>ul>li>a {
    display: inline-block;
    color: #000;
    font-size: 15px;
    font-weight: 700;
    letter-spacing: 1px;
    text-decoration: underline;
    margin-bottom: 15px
}

.OzelSayfaContent .OzelSayfaSol>ul>li>ul li a {
    line-height: 35px;
    font-size: 14px;
    letter-spacing: 1px;
    font-weight: 400
}

.OzelSayfaContent .OzelSayfaSol>ul>li>ul li a:hover {
    text-decoration: underline
}

.OzelSayfaContent .OzelSayfaSol .canlidestek {
    position: relative;
    float: left;
    width: 100%;
    margin-top: 10px
}

.OzelSayfaContent .OzelSayfaSol .canlidestek a {
    position: relative;
    float: left;
    font-size: 10px;
    color: #000;
    width: 122px;
    padding-top: 14px;
    padding-right: 11px;
    text-align: right;
    font-weight: 600
}

.OzelSayfaContent .OzelSayfaSol .canlidestek a img {
    position: absolute;
    left: 0;
    top: 0;
    max-width: 100%
}

.OzelSayfaContent .OzelSayfaSag {
    float: left;
    width: 75%;
    padding-left: 40px;
    border-left: 1px solid #8f8f8f
}

.OzelSayfaContent .OzelSayfaSag::-webkit-scrollbar {
    width: 15px
}

.OzelSayfaContent .OzelSayfaSag::-webkit-scrollbar-track {
    background: #dbdbdb
}

.OzelSayfaContent .OzelSayfaSag::-webkit-scrollbar-thumb {
    background: #fff;
    border-radius: 0;
    border: 2px solid #dbdbdb
}

.OzelSayfaContent .OzelSayfaSol ul li ul {
    border: 1px solid gray;
    border-bottom: none
}

.OzelSayfaContent .OzelSayfaSol ul li ul li {
    border-bottom: 1px solid gray;
    padding: 0 10px
}



.SosyalMedyaBanner .sosiContainer {
    max-width: 686px;
    margin: 0 auto;
    display: block
}

.SosyalMedyaBanner .sosiContainer .banTek {
    float: left;
    width: 100%;
    margin-bottom: 12px
}

.SosyalMedyaBanner .sosiContainer .banTek:nth-child(3) {
    margin-bottom: 0
}

.SosyalMedyaBanner .sosiContainer .banTek a {
    float: left;
    width: 100%
}

.SosyalMedyaBanner .sosiContainer .banTek img {
    max-width: 100%
}

.SosyalMedyaBanner .sosiContainer .banTek .banIki {
    float: left;
    width: 337px;
    margin-right: 12px;
    margin-bottom: 14px
}

.SosyalMedyaBanner .sosiContainer .banTek .banIki:nth-child(2n) {
    margin-right: 0
}

.iletisimContent {
    width: 100%;
    padding-top: 20px
}

#itetisimhtml {
    float: right;
    width: 75%;
    padding-left: 30px;
    margin-top: 25px
}

#itetisimhtml iframe {
    width: 100%
}

.iletisimClear {
    clear: none
}

.iletisimLeft {
    width: 25%!important;
    background: #fff
}

.iletisimContent .row {
    padding: 0!important;
    border: none!important;
    min-height: 100%!important
}

.iletisimRight {
    width: 100%;
    float: left;
    border: solid 1px #ccc;
    padding: 1%;
    min-height: 270px;
    background: #fff;
    display: none
}

.iletisimContent .iletisimLeft .categoryTitle {
    border-bottom: solid 1px #000;
    margin-bottom: 15px
}

.iletisimLeft .span,.iletisimRight .span {
    margin: 0!important;
    padding: 0;
    width: 100%!important;
    overflow: visible!important
}

.iletisimLeft .span .Center {
    width: 2%;
    display: none
}

.iletisimLeftFirmaAdi {
    display: none
}

.iletisimLeftEposta {
    display: none
}

.iletisimLeftFaks {
    display: none
}

.iletisimLeftTelefon .Left {
    font-size: 18px;
    width: 100%!important;
    color: #000!important;
    font-weight: 600;
    text-transform: uppercase
}

.iletisimLeftTelefon .Left:before {
    content: '\f095';
    font-family: fontawesome;
    margin-right: 5px;
    font-weight: 400
}

.iletisimLeftTelefon .Right {
    color: #000!important;
    font-size: 13px!important;
    letter-spacing: 1px;
    line-height: 1!important;
    min-height: 0!important;
    padding-left: 20px
}

.iletisimLeftAdres .Left {
    font-size: 18px;
    width: 100%!important;
    color: #000!important;
    font-weight: 600;
    text-transform: uppercase
}

.iletisimLeftAdres .Left:before {
    content: '\f041';
    font-family: fontawesome;
    margin-right: 5px;
    font-weight: 400
}

.iletisimLeftAdres .Right {
    color: #000!important;
    font-size: 11px!important;
    line-height: 1.2!important;
    letter-spacing: 1px;
    min-height: 0!important;
    padding-left: 20px
}

.calismasaati {
    float: left;
    width: 100%;
    color: #000;
    font-size: 11px;
    margin: 5px 0 20px;
    padding-left: 20px
}

.iletisimForm {
    width: 25%;
    padding: 0;
    border: none;
    overflow: visible;
    margin-top: 40px;
    float: left
}

.iletisimForm .categoryTitle {
    border-bottom: none!important;
    margin-bottom: 15px
}

.iletisimForm .categoryTitle .categoryTitleText {
    font-size: 18px;
    margin-bottom: 0;
    color: #000;
    font-weight: 600;
    text-transform: uppercase
}

.iletisimForm .categoryTitle .categoryTitleText:before {
    content: '\f003';
    font-family: fontawesome;
    margin-right: 5px;
    font-weight: 400
}

.iletisimForm .row {
    width: 100%!important;
    padding-left: 20px!important
}

.iletisimForm .row .span {
    width: 100%!important;
    height: auto!important;
    margin: 0 0 10px!important
}

.iletisimForm .row .span .Left {
    width: 45%!important;
    min-height: 100%!important;
    line-height: 35px!important;
    font-size: 14px
}

.iletisimForm .row .span .Right {
    width: 55%!important;
    min-height: 100%!important;
    line-height: 20px!important
}

.iletisimForm .row .span .Right input {
    height: 35px!important;
    border: 1px solid #ececec!important
}

.iletisimForm .row .span .Right textarea {
    border: 1px solid #ececec!important;
    width: 100%!important
}

.iletisimForm .row .span .Center {
    display: none
}

.iletisimForm .row .span.iletisimCaptcha .captchaImageBox {
    width: 100%!important;
    text-align: right
}

.iletisimForm .row .span.iletisimCaptcha .captchaInputBox {
    width: 100%!important
}

.iletisimForm .row .span.iletisimCaptcha .clear {
    display: none
}

.iletisimForm .iletisimBtn .button {
    height: 35px
}

.owl-carousel .owl-stage-outer {
    padding-bottom: 1px
}

.body {
    background: #fff
}

.ProductPreviewContent ul {
    float: left;
    width: 100%;
    background: #fff;
    font-family: josefin sans,sans-serif;
    padding: 35px
}

.ProductPreviewRight {
    width: 45%
}

.PreviewselectedImages {
    padding-bottom: 126%!important
}

.PreviewselectedImages .PreviewselectedImagesBox {
    padding-bottom: 128%!important
}

.PreviewallImages .PreviewallImagesItem {
    padding-bottom: 126%!important
}

.PreviewallImagesItem .PreviewallImagesBox {
    padding-bottom: 128%!important
}

.hizliBakis_Name {
    font-size: 21px;
    font-weight: 600;
    color: #1d1d1d
}

.hizliBakis_Price {
    color: #000;
    font-size: 14px;
    font-family: abakutlsymsans,sans-serif;
    font-weight: 600;
    margin: 15px 0
}

.hizliBakisSepeteEkle {
    float: left;
    width: 100%;
    color: #fff!important;
    letter-spacing: 0!important;
    margin-top: 15px!important;
    background-color: #00aa5b!important;
    font-size: 15px;
    line-height: 36px;
    border-radius: 0;
    font-weight: 700;
    text-transform: uppercase
}

.hizliBakis_Adet .riSingle .riDown,.hizliBakis_Adet .riSingle .riUp {
    width: 25px!important
}

.ProductPreviewForm .hizliBakis_Adet .riSingle {
    padding: 0 25px!important;
    width: 105px!important
}

#divKombinUrunEkSecenek {
    margin: 15px 0;
    float: left;
    width: 100%
}

#divKombinUrunEkSecenek .divKombinEksecenekTipi .kombinFormline .kombinleft_line {
    color: #1d1d1d;
    font-size: 11px
}

#divKombinUrunEkSecenek .divKombinEksecenekTipi .kombinFormline .kombinright_line .size_box {
    border: 1px solid #969696;
    margin-right: 7px;
    float: left;
    text-align: center;
    padding: 0 12px;
    margin-bottom: 7px
}

#divKombinUrunEkSecenek .divKombinEksecenekTipi .kombinFormline .kombinright_line .size_box.selected {
    background: #565656;
    color: #fff
}

#divKombinUrunEkSecenek .divKombinEksecenekTipi .kombinFormline .kombinright_line .size_box.nostok {
    background: #fff;
    position: relative
}

#divKombinUrunEkSecenek .divKombinEksecenekTipi .kombinFormline .kombinright_line .size_box.nostok:after {
    content: '';
    height: 1px;
    width: 55%;
    background: #868686;
    left: 22%;
    top: 48%;
    position: absolute;
    transform: rotate(-132deg);
    -webkit-transform: rotate(-132deg);
    -moz-transform: rotate(-132deg);
    -o-transform: rotate(-132deg)
}

#divKombinUrunEkSecenek .divKombinEksecenekTipi .kombinFormline .kombinright_line .size_box.nostok:before {
    content: '';
    height: 1px;
    width: 55%;
    background: #868686;
    left: 22%;
    top: 48%;
    position: absolute;
    transform: rotate(132deg);
    -webkit-transform: rotate(132deg);
    -moz-transform: rotate(132deg);
    -o-transform: rotate(132deg)
}

.kombinItem .PriceListKombin>.kombinFormline:nth-child(2) {
    margin: 15px 0
}

.kombinItem .PriceListKombin>.kombinFormline:nth-child(3) {
    margin: 15px 0
}

.kombinItem .PriceListKombin>.kombinFormline:nth-child(2)>div {
    color: #000;
    font-size: 14px;
    font-family: abakutlsymsans,sans-serif;
    font-weight: 600
}

.kombinItem .PriceListKombin>.kombinFormline:nth-child(3)>div {
    color: #d40909;
    font-size: 18px;
    font-weight: 600
}

.kombinItem .PriceListKombin #divKombinUrunEkSecenek {
    display: inline-block!important;
    width: 100%
}

.kombinItem .PriceListKombin #divKombinUrunEkSecenek .divKombinEksecenekTipi {
    float: left;
    width: 100%;
    margin-bottom: 20px
}

.navigation.fixed {
    position: fixed;
    top: 0;
    left: 0;
    z-index: 9999;
    box-shadow: 0 -3px 13px 0 #000;
    background: #fff
}

.navigation.fixed .altMenu {
    box-shadow: 0 3px 14px 0 #939393
}

.AltBanner.margin {
    margin-top: 55px
}

.siparisTakipSayfasi {
    background: #fff
}

.siparisTakipSayfasi .siparisTakipBaslik {
    text-align: center;
    padding: 20px 0!important
}

.sepetiTemizle {
    float: right;
    line-height: 43px;
    padding: 0 10px
}

.popupSepet {
    width: 99%
}

.popupSepet #hed div {
    width: 94%
}

#lang_flag_container {
    left: auto!important;
    top: -25px!important;
    right: 0
}

.HomeBody #lang_flag_container {
    display: none;
    z-index: 1001
}

#lang_flag_container #lang-detail {
    left: auto!important;
    right: 0
}

#langHover {
    padding: 6px 5px!important
}

#lang {
    color: #fff!important
}

#lang_flag_container #lang-detail {
    top: 25px!important;
    width: 220px!important
}

#langHover.white {
    background: 0 0!important
}

#lang-detail .language a.flag-sr {
    display: none
}

.sepetiTemizle {
    margin-top: 0;
    display: inline-block;
    font-size: 9px!important;
    text-decoration: none!important
}

.flag-de {
    background-position: 0!important;
}

#divAvailableCurrencies {
    display: none!important
}

.sayfaIcerik * {
    font-family: josefin sans,sans-serif!important
}

#accordion * {
    font-family: josefin sans,sans-serif!important
}

.OzelSayfaSag * {
    font-family: josefin sans,sans-serif!important
}

.sayfaIcerik img {
    max-width: 100%
}

.sepetimBody .welcome {
    display: none
}

.sepetimBody .mycart {
    display: none
}

.sepetimBody .searchContent {
    display: none
}

.sepetimBody .MF {
    display: none
}

.sepetimBody #logo {
    float: none;
    text-align: center
}

.right0 {
    padding-right: 0
}

.left0 {
    padding-left: 0
}

.imgBanDiv {
    margin-bottom: 10px
}

#divBreadcrumb {
    display: none
}

#mainHolder_UrunDetay_imgCookie {
    display: none!important
}

.product-social-icon-wrapper {
    display: none
}

.ProductDetail .product-social-icon-wrapper {
    display: none
}

.sepetimBody #header {
    padding-bottom: 20px
}

.HesabimContainer .urunDetayPanel {
    max-height: 100%
}

.orders {
    width: 100%
}

.MF {
    position: absolute;
    right: 45px;
    top: 19px
}

.MF .mflink {
    float: left;
    text-align: center
}

.MF .mflink a {
    float: left;
    width: 100%;
    font-size: 10px
}

.MF .mflink a:hover {
    text-decoration: underline
}

.MF .mflink a img {
    margin: 0 23%;
    margin-bottom: 5px;
    display: inline-block
}

.MF .mflink.Magza {
    width: 45px;
    margin-right: 13px
}

.MF .mflink.Fav {
    width: 35px
}

.MF .H-blog {
    margin-right: 13px
}

.MF .H-blog a img {
    margin: 0
}

.topText {
    position: absolute;
    top: -25px;
    left: 0;
    right: 0;
    text-align: center;
    line-height: 25px;
    color: #fff;
    font-size: 12px
}

.topText span {
    font-weight: 700
}

.HoverAlan {
    display: none;
    z-index: 3;
    float: left;
    position: absolute;
    top: 100%;
    left: 0;
    background: #ffffd5;
    box-shadow: 3px 4px 0 0 #a2a2a2;
    padding: 15px;
    color: #000;
    font-size: 12px;
    letter-spacing: 1px
}

.HoverAlan:before {
    content: '\f0de';
    font-family: fontawesome;
    float: left;
    left: 0;
    right: 0;
    top: -5px;
    text-align: center;
    color: #ffffd5;
    position: absolute
}

.HoverAlan a {
    font-size: 12px;
    color: #000;
    letter-spacing: 0;
    font-weight: 600;
    text-decoration: underline
}

.HoverAlan span {
    font-weight: 600
}

.AltBanner {
    margin: 15px 0;
    float: left;
    width: 100%;
    display: none
}

.HomeBody .AltBanner {
    display: block
}

.CategoryBody .AltBanner {
    display: block;
    margin-bottom: 33px
}

.AltBanner .AltBannerAlan {
    float: left;
    width: 100%;
    background: #000;
    padding: 0;
    text-align: center;
    position: relative
}

.AltBanner .AltBannerAlan>a {
    float: left;
    width: 100%
}

.AltBanner .AltBannerAlan .TextAlanB {
    display: inline-block;
    vertical-align: top;
    height: 50px
}

.AltBanner .AltBannerAlan .TextAlanB>div {
    float: left;
    color: #fff;
    line-height: 64px
}

.AltBanner .AltBannerAlan .TextAlanB>div.One {
    font-size: 20px;
    letter-spacing: 5px;
    font-weight: 700;
    margin-right: 20px
}

.AltBanner .AltBannerAlan .TextAlanB>div.Two {
    font-size: 64px;
    font-weight: 700
}

.AltBanner .AltBannerAlan .TextAlanB>div.Three {
    font-size: 15px;
    font-weight: 700;
    text-align: left;
    margin-right: 15px;
    line-height: 1;
    margin-left: 5px;
    margin-top: 11px
}

.AltBanner .AltBannerAlan .TextAlanB>div.Four {
    font-size: 40px;
    font-weight: 700;
    margin-right: 40px
}

.AltBanner .AltBannerAlan .TextAlanB>div.Five a {
    font-size: 19px;
    font-weight: 600;
    color: #fff;
    line-height: 64px
}

.AltBanner .AltBannerAlan .HoverAlan {
    left: 34%
}

.AltBanner .AltBannerAlan:hover .HoverAlan {
    display: block
}

.SliderYan {
    width: 30.6%!important;
    float: right!important
}

._tabHead {
    float: left;
    width: 100%;
    padding: 0 30px
}

._tabHead ul {
    float: left;
    width: 100%
}

._tabHead li {
    float: left;
    text-align: center;
    width: 25%
}

._tabHead li a {
    color: #000;
    font-size: 17px;
    font-weight: 600;
    line-height: 45px;
    display: inline-block
}

._tabHead li._tabHead_active {
    background: #fff
}

#anasayfatab {
    float: left;
    width: 100%;
    background: #eee;
    margin: 20px 0;
    padding: 30px 0
}

#anasayfatab .anasayfaTabAlt {
    width: 100%;
    padding: 0;
    float: left;
    height: 0;
    overflow: hidden;
    position: relative;
    background: #fff
}

#anasayfatab .anasayfaTabAlt.active {
    overflow: visible;
    height: 100%;
    padding: 30px 0
}

#anasayfatab .anasayfaTabAlt .sliderBannerContainer:after {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    height: 100%;
    background-color: #fff;
    z-index: 999;
    transition: all 1.5s ease-in
}

#anasayfatab .anasayfaTabAlt.active .sliderBannerContainer:after {
    opacity: 0;
    z-index: -1
}

.anasayfaTabAlt {
    float: left;
    width: 100%
}

.anasayfaTabAlt .productItem {
    margin-bottom: 0
}

.AltTitle {
    float: left;
    width: 100%;
    line-height: 40px;
    color: #333;
    font-weight: 400;
    padding-left: 20px;
    border-bottom: 1px solid #f8f8f8;
    font-size: 14px;
    background: #fff;
    border-radius: 10px 10px 0 0
}

.anasayfatab .sliderBannerContainer ul li {
    margin-bottom: 0
}

#anasayfatab {
    float: left;
    width: 100%;
    position: relative
}

#anasayfatab:before {
    content: '';
    width: 30px;
    height: 100%;
    position: absolute;
    left: 0;
    top: 0;
    background: #eee;
    z-index: 1
}

#anasayfatab:after {
    content: '';
    width: 30px;
    height: 100%;
    position: absolute;
    right: 0;
    top: 0;
    background: #eee
}

.AltAlan {
    float: left;
    width: 100%
}

.SliderYonetim {
    float: left;
    width: 100%;
    margin: 20px 0;
    padding: 30px;
    background: #eee
}

.SliderYonetim2 {
    float: left;
    width: 100%;
    margin: 0;
    padding: 0
}

.BlokTitle {
    float: left;
    width: 100%;
    position: relative
}

.BlokTitle span {
    float: left;
    font-size: 17px;
    color: #000;
    font-weight: 600;
    line-height: 48px;
    text-align: center;
    width: 335px;
    background: #fff
}

.BlokTitle2 {
    float: left;
    width: 100%;
    position: relative;
    text-align: center
}

.BlokTitle2:after {
    content: '';
    position: absolute;
    top: 50%;
    left: 10%;
    right: 10%;
    height: 1px;
    background: #dbdbdb;
    border-bottom: 1px solid #f6f6f6;
    z-index: -1
}

.Blok .BlokTitle2 {
    margin-bottom: 30px
}

.BlokTitle2 span {
    display: inline-block;
    font-size: 25px;
    color: #000;
    font-weight: 600;
    line-height: 48px;
    text-align: center;
    background: #fff;
    padding: 0 22px
}

.SliderYonetimAlt {
    float: left;
    width: 100%;
    padding: 30px 0;
    background: #fff
}

.SlidersizYonetim {
    float: left;
    width: 100%
}

.TekliSlider .BlokTitle {
    float: left;
    width: 100%;
    color: #111;
    font-size: 15px;
    text-align: center;
    font-weight: 500;
    line-height: 39px;
    position: relative
}

.TekliSlider .BlokTitle:before {
    content: '';
    position: absolute;
    left: 0;
    top: 21px;
    width: 40px;
    height: 1px;
    background: #111;
    float: left
}

.TekliSlider .BlokTitle:after {
    content: '';
    position: absolute;
    right: 0;
    top: 21px;
    width: 40px;
    height: 1px;
    background: #111;
    float: right
}

.TekliSlider .sliderBannerContainer {
    margin: 0
}

#NewProduct {
    float: left;
    width: 100%;
    margin-top: 15px;
    box-shadow: 0 0 4px 1px #d6d6d6
}

#NewProduct .NewTitle {
    float: left;
    width: 100%;
    border-radius: 5px 5px 0 0;
    background: #daa9da;
    line-height: 50px;
    color: #fff;
    font-weight: 500;
    text-align: center;
    font-size: 16px
}

#NewProduct .sliderBannerContainer {
    background: #fff;
    padding: 15px 15px 0
}

#NewProduct .sliderBannerContainer ul li {
    width: 100%;
    margin-right: 0;
    margin-bottom: 15px
}

#NewProduct .sliderBannerContainer ul li .productItem {
    border: none;
    border-bottom: 1px solid #e1bae1
}

#NewProduct .sliderBannerContainer ul li .productItem .productImage {
    width: 115px;
    float: left;
    padding-bottom: 47%
}

#NewProduct .sliderBannerContainer ul li .productItem .productImage a {
    padding-bottom: 93%
}

#NewProduct .sliderBannerContainer ul li .productItem .productDetail {
    width: calc(100% - 115px);
    height: 110px;
    padding: 0
}

#NewProduct .sliderBannerContainer ul li .productItem .productName {
    border: none;
    padding: 0
}

#NewProduct .sliderBannerContainer ul li .productItem .productPrice {
    padding-left: 45px
}

#NewProduct .sliderBannerContainer ul li .productItem .productPrice.IndirimVar .discountPrice {
    left: 45px
}

#NewProduct .sliderBannerContainer ul li .newIcon {
    bottom: auto;
    top: 0;
    right: auto;
    left: 0
}

#NewProduct .sliderBannerContainer ul li .discountIcon {
    width: 40px;
    height: 30px;
    line-height: 33px;
    font-size: 11.5px;
    font-weight: 500;
    left: 115px;
    bottom: auto;
    top: 35px
}

#NewProduct .sliderBannerContainer ul li .mycartIcon {
    width: 132px;
    right: 0
}

#NewProduct .sliderBannerContainer ul li .examineIcon {
    right: 0;
    left: 0
}

#NewProduct .sliderBannerContainer ul li .mycartIcon a {
    text-align: center;
    background-position: 105px 5px
}

#NewProduct .sliderBannerContainer ul li .productItem:hover .mycartIcon {
    bottom: 10px
}

#NewProduct .sliderBannerContainer ul li .productItem:hover .productOnYazi {
    display: none!important
}

#NewProduct .sliderBannerContainer ul li .productItem:hover .productPrice {
    bottom: 0!important;
    z-index: 2
}

.GuvenList {
    float: left;
    width: 100%;
    margin: 20px 0
}

.GuvenList ul {
    float: left;
    width: 100%;
    padding: 20px 0
}

.GuvenList li {
    float: left;
    width: 14.2%;
    padding: 0 1%;
    position: relative;
    text-align: center
}

.GuvenList li:after {
    content: "";
    width: 2px;
    height: 25px;
    background: #787878;
    position: absolute;
    right: 0;
    top: 0;
    bottom: 0;
    margin: auto
}

.GuvenList li:last-child {
    padding-right: 0;
    border: none
}

.GuvenList li:first-child {
    padding-left: 0
}

.GuvenList li:last-child:after {
    display: none
}

.GuvenList li .Gimg {
    display: block
}

.GuvenList li .Gtext {
    color: #565656;
    font-weight: 600;
    line-height: 15px;
    margin-top: 8px
}

@media screen and (max-width: 1025px) {
    .GuvenList li .Gtext {
        font-size:.9vw
    }
}

.GuvenList li .HoverAlan {
    right: 0
}

.GuvenList li:hover .HoverAlan {
    display: block
}

.Blok {
    display: block;
    width: 100%;
    float: left
}

.Blok .BlokText {
    position: absolute;
    bottom: 19px;
    left: 25%;
    right: 25%;
    background: #fff;
    text-align: center;
    line-height: 46px
}

.Blok .BlokText a {
    font-weight: 600;
    color: #000;
    font-size: 13px;
    display: inline-block
}

.Blok .BlokText a:hover {
    text-decoration: underline;
    font-weight: 700
}

.Saglan {
    float: left;
    width: 100%
}

.SliderYan .BlokText {
    left: 10%;
    right: 10%
}

.ban1 {
    float: left;
    width: 100%;
    position: relative;
    margin-bottom: 17px
}

.ban1:last-child {
    margin-bottom: 0
}

.ban1>a {
    float: left;
    width: 100%;
    position: relative
}

.ban1>a:hover:after {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: rgba(255,255,255,.37)
}

.ban1 img {
    width: 100%
}

.ban2 {
    float: left;
    width: 49.25%;
    margin-right: 1.5%;
    margin-bottom: 1.5%;
    position: relative
}

.ban2:last-child {
    margin-right: 0
}

.ban2>a {
    float: left;
    width: 100%;
    position: relative;
    overflow: hidden
}

.ban2>a:hover:after {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: rgba(255,255,255,.37)
}

.ban2>.row>a {
    float: left;
    width: 100%;
    position: relative;
    overflow: hidden
}

.ban2>.row>a:hover:after {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: rgba(255,255,255,.37)
}

.ban2 img {
    width: 100%
}

.ban2 .ban1 {
    margin-bottom: 2.6%
}

.banfull {
    float: left;
    width: 100%;
    margin-bottom: 1.5%;
    position: relative;
    position: relative
}

.banfull>a {
    float: left;
    width: 100%;
    position: relative;
    overflow: hidden
}

.banfull>a:hover:after {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: rgba(255,255,255,.37)
}

.banfull>.row>a {
    float: left;
    width: 100%;
    position: relative;
    overflow: hidden
}

.banfull>.row>a:hover:after {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: rgba(255,255,255,.37)
}

.banfull img {
    width: 100%
}

.banfull .banfull-link {
    position: absolute!important;
    width: 33.3%!important;
    height: 100%
}

.banfull .banfull-link:nth-child(2) {
    left: 0
}

.banfull .banfull-link:nth-child(3) {
    left: 33.3%
}

.banfull .banfull-link:nth-child(4) {
    right: 0
}

.ban3 {
    float: left;
    width: 380px;
    margin-right: 15px;
    position: relative
}

.ban3:last-child {
    margin-right: 0
}

.ban3>a {
    float: left;
    width: 100%;
    position: relative;
    overflow: hidden
}

.ban3 img {
    width: 100%
}

.ban4 {
    float: left;
    width: 280px;
    position: relative;
    margin-right: 20px
}

.ban4:last-child {
    margin-right: 0
}

.ban4>a {
    float: left;
    width: 100%
}

.ban4 img {
    width: 100%
}

.ban5 {
    float: left;
    width: 584px;
    margin-right: 10px
}

.ban5:last-child {
    margin-right: 0
}

.ban5>a {
    float: left;
    width: 100%;
    position: relative
}

.ban5 img {
    width: 100%
}

.ban6 {
    float: left;
    width: 557px;
    margin-bottom: 15px
}

.ban6>a {
    float: left;
    width: 100%;
    position: relative
}

.ban6 img {
    width: 100%
}

.FooterTudors {
    float: left;
    width: 100%
}

.FooterMiddle {
    float: left;
    width: 100%;
    background: #eee
}

.Social {
    float: left;
    width: 100%;
    margin: 18px 0
}

.Social ul {
    float: left;
    width: 100%;
    text-align: center
}

.Social li {
    display: inline-block;
    width: 53px
}

.Social li a {
    float: left;
    font-size: 30px;
    color: #000
}

.Social li a i {
    line-height: 30px
}

.Store {
    float: left;
    width: 100%;
    margin-top: 10px
}

.Store a {
    float: left;
    margin-bottom: 20px
}

.Store a:last-child {
    margin-bottom: 0
}

.Store a img {
    max-width: 100%
}

.linkler {
    display: inline-block;
    
    width: 100%;
    padding: 35px 0
}

.linkler>ul {
    float: left;
    width: 100%
}

.linkler>ul>li {
    float: left;
    width: 20%
}

.linkler>ul>li:first-child {
    border-left: none
}

.linkler>ul>li>a {
    font-size: 15px;
    color: #150000;
    position: relative;
    float: left;
    width: 100%;
    margin-bottom: 20px;
    font-weight: 600
}

.linkler>ul>li>ul {
    float: left;
    width: 100%
}

.linkler>ul>li>ul>li {
    float: left;
    width: 100%
}

.linkler>ul>li>ul>li>a {
    color: #150000;
    display: block;
    font-size: 15px;
    font-weight: 400;
    margin-bottom: 10px;
    transition: all .2s ease;
    -webkit-transition: all .2s ease;
    -moz-transition: all .2s ease;
    -o-transition: all .2s ease
}

.linkler>ul>li>ul>li>a:hover {
    text-decoration: underline
}

.linkler>ul>li>.Magazalar {
    float: left;
    width: 80%;
    border: 1px solid #91074b;
    border-radius: 2px;
    text-align: center
}

.linkler>ul>li>.Magazalar>a {
    float: left;
    width: 100%;
    line-height: 51px;
    font-size: 15px;
    color: #000
}

.linkler>ul>li>.Magazalar>a:after {
    content: '\e833';
    font-family: lineariconsfree;
    color: #000;
    font-size: 33px;
    line-height: 51px;
    float: right
}

.footer-liblog {
    position: relative
}

.footer-blog {
    position: absolute;
    top: 120px;
    left: 50%;
    margin-left: -110px
}

.ebultenDiv {
    float: left;
    width: 100%;
    padding-right: 15px
}

.Etitle {
    float: left;
    color: #150000;
    font-size: 15px;
    font-weight: 600;
    margin-bottom: 5px
}

.Etitle p {
    float: left;
    width: 100%;
    font-weight: 400;
    line-height: 1;
    margin-top: 10px
}

.ebultenGelecek {
    width: 100%;
    float: left
}

#divNewsLetter {
    display: none;
    float: right;
    position: relative;
    width: 100%
}

#divNewsLetter label {
    display: none;
    margin-bottom: 25px;
    text-align: center;
    color: #000;
    line-height: 1.2;
    font-size: 12px
}

#UpdatePanel1 {
    position: relative;
    float: left;
    width: 100%
}

#txtbxNewsletterMail {
    display: inline-block;
    color: #150000;
    background: #fff;
    width: 100%;
    height: 31px;
    padding: 0 30px 0 5px;
    font-size: 12px;
    text-align: left;
    font-weight: 500;
    border-radius: 0;
    border: none;
    opacity: 1
}

#txtbxNewsletterMail::-webkit-input-placeholder {
    color: #150000
}

#txtbxNewsletterMail:-moz-placeholder {
    color: #150000
}

#txtbxNewsletterMail::-moz-placeholder {
    color: #150000
}

#txtbxNewsletterMail:-ms-input-placeholder {
    color: #150000
}

#txtbxNewsletterMail:focus {
    color: #150000
}

.newsbutton {
    float: left;
    position: absolute;
    top: 0;
    right: 0;
    width: 25px;
    height: 31px;
    color: #fff;
    border: none!important;
    border-radius: 0;
    line-height: 30px;
    font-weight: 500;
    text-transform: uppercase;
    font-size: 0!important;
    padding: 0;
    text-align: center
}

.ebultenGelecek #divNewsLetter {
    display: block;
    padding: 0
}

#ticimaxCopyright {
    float: left;
    width: 100%;
    margin: 0!important;
    background: #fff;
    padding: 15px 0;
    font-family: roboto,sans-serif!important
}

.imgzoom {
    float: left;
    width: 100%;
    font-size: 13px;
    padding-left: 45px;
    margin-top: 15px
}

.imgzoom i {
    color: #f60;
    margin-right: 10px
}

.Fbttm {
    float: left;
    width: 100%;
    padding: 25px 0;
    border-top: 1px solid #7d7d7d
}

.bankimg {
    float: left;
    margin-top: 10px
}

.bankimg i {
    float: left;
    color: #9b9b9b;
    font-size: 34px;
    margin-right: 4px
}

.bankiyzico {
    float: left;
    width: 100%;
    background: #fff;
    text-align: center;
    padding: 10px 0
}

.bankiyzico img {
    display: inline-block;
    max-width: 500px
}

.banksimg {
    float: left;
    width: 100%;
    background: #71034e
}

.banksimg .bankimgs {
    float: left;
    width: 100%;
    text-align: center;
    padding: 3px 0 5px
}

.banksimg .bankimgs img {
    max-width: 100%
}

.FTextAlan {
    float: left;
    width: 100%;
    margin: 30px 0;
    text-align: center;
    line-height: 17px
}

.FTextAlan strong {
    font-weight: 600
}

.MusteriHizmet {
    float: left;
    width: 100%;
    margin-top: 15px
}

.MusteriHizmet .Mimg {
    float: left;
    width: 42px;
    margin-right: 10px
}

.MusteriHizmet .Mtext {
    float: left
}

.MusteriHizmet .Mtext a {
    font-size: 15px;
    color: #000;
    float: left;
    font-weight: 600
}

.MusteriHizmet .Mtext a p {
    font-size: 30px;
    color: #000;
    font-weight: 600
}

.flogo {
    float: left
}

.flogo img {
    max-width: 100%
}

.copy {
    float: right;
    color: #fff;
    font-size: 11px;
    font-weight: 400;
    line-height: 30px
}

.Ftext {
    float: left;
    width: 100%;
    padding: 15px 0;
    font-size: 11px;
    color: #fff;
    line-height: 20px;
    max-height: 90px;
    overflow: hidden
}

.Ftext .dvmbtn {
    display: inline-block;
    font-weight: 600;
    cursor: pointer
}

.Ftext .gizlebtn {
    display: none;
    font-weight: 600;
    cursor: pointer
}

.col-5li {
    width: 20%
}

.bedenT {
    position: relative;
    float: left;
    width: 100%
}

.bedenTablosu {
    left: 59%;
    padding: 5px;
    line-height: 1;
    color: gray;
    margin-left: 91px;
    margin-right: -18px;
    font-weight: 400;
    font-size: 13px;
    float: left;
    margin-top: 0;
    position: absolute;
    bottom: 73px;
    right: auto
}

.taksitT {
    float: left;
    position: absolute;
    right: 0;
    top: 20px
}

.taksitT .taksitTablosu {
    color: #e30613;
    font-size: 16px;
    font-weight: 600
}

.taksitT .taksitTablosu i {
    font-size: 18px;
    margin-left: 10px
}

.product-social-icon-wrapper {
    float: left;
    margin-top: 10px;
    width: 26%;
    position: relative;
    z-index: 9
}

.product-social-icon-wrapper:before {
    content: '';
    width: 100%;
    height: 44px;
    float: left;
    margin-bottom: 15px
}

.product-social-icon-wrapper:hover ul {
    display: block
}

.product-social-icon-wrapper .PaylasTit {
    display: none
}

.product-social-icon-wrapper ul {
    float: left;
    width: 100%;
    display: none;
    position: absolute;
    top: 59px;
    left: 0
}

.product-social-icon-wrapper li {
    
    width: 100%;
    display: inline-block;
    text-align: center
}

.product-social-icon-wrapper li a {
    display: inline-block;
    color: #fff;
    text-align: center;
    width: 30px;
    height: 30px;
    border-radius: 100%;
    margin-bottom: 10px
}

.product-social-icon-wrapper li a i {
    font-size: 13px;
    line-height: 30px
}

.product-social-icon-wrapper li:nth-child(1) a {
    background: #3059c3
}

.product-social-icon-wrapper li:nth-child(2) a {
    background: #36abf1
}

.product-social-icon-wrapper li:nth-child(3) a {
    background: #ee2500
}

.product-social-icon-wrapper li:nth-child(4) a {
    background: #d44c33
}

.UWhatsApp {
    float: left;
    width: 34px;
    font-size: 0;
    margin-top: 0
}

.UWhatsApp a {
    float: left;
    font-size: 0;
    text-align: center;
    padding-left: 0;
    color: #fff;
    line-height: 1;
    width: 30px;
    border-radius: 100%;
    text-indent: 0
}

.whatsApp i {
    font-size: 13px;
    line-height: 30px
}

.UWhatsApp label {
    font-size: 0
}

.UWhatsApp:hover a {
    background: #6dc33a;
    color: #fff
}

#divOnyazi .DList {
    display: none
}

.DList {
    float: left;
    width: 100%;
    margin-bottom: 20px
}

.DList li {
    float: left;
    width: 33%
}

.DList li .dimg {
    float: left
}

.DList li .dtext {
    float: left;
    color: #777;
    font-size: 12px;
    font-weight: 600;
    line-height: 20px;
    margin-left: 10px
}

.orders .order-title {
    width: auto!important
}

.categoryTitleText {
    margin: 0 auto;
    display: block;
    max-width: 1366px
}

.HesabimContainer .centerCount {
    background: #fff;
    padding: 10px
}

.order-detail .statusBox img {
    width: 100%
}

.TumKategoriler {
    display: none
}

.welcomeOpen {
    display: none
}

.mycartClick {
    display: none
}

.kombinleftImage .allImages {
    display: block!important
}

.userContainer .userDivLeft .uyeGirisBeniHatirla {
    width: 100%;
    position: relative;
    top: 0;
    font-size: 13px
}

.userContainer .userDivLeft .uyeGirisBeniHatirla input {
    display: inline-block;
    vertical-align: top;
    margin-top: -.6px
}

.userContainer .userDivLeft .userPassBtn {
    position: relative;
    width: 100%;
    top: 30px;
    margin-bottom: 127px
}

.userContainer .userDivLeft #divFacebookLoginContainer {
    width: 100%;
    margin-top: 20px
}

.userContainer .userDivLeft .userSignUp {
    width: 100%;
    margin-top: 15px
}

.userLeftBox .uyeGirisBeniHatirla input {
    display: inline-block;
    vertical-align: top;
    margin-top: 3px;
    margin-right: 0
}

.userLeftBox #divFacebookLoginContainer {
    width: 100%;
    margin-top: 5px
}

.userLeftBox .userSignUp {
    width: 100%;
    margin-top: 7px
}

@media screen and (min-width: 1024px) and (max-width:1284px) {
    .MusteriHizmet .Mtext a {
        font-size:13px
    }

    .MusteriHizmet .Mtext a p {
        font-size: 20px
    }

    .footer-blog {
        position: absolute;
        top: 150px
    }

    .Mobil-uygulama a {
        width: 100%;
        text-align: center
    }

    .Mobil-uygulama a:first-child {
        text-align: center
    }
}

@media screen and (min-width: 1024px) and (max-width:1370px) {
    .headerContent,.ticiContainer {
        max-width:1300px
    }
}

@media screen and (min-width: 1025px) {
    .sortingContent {
        display:block!important
    }

    .mobilMenu {
        display: none!important
    }
}

@media screen and (max-width: 1025px) {
    #slider-range {
        background:#dedede;
        height: 5px!important;
        width: 93%;
        margin: 0 10px!important;
        border: none;
        float: left
    }

    #slider-range .ui-slider-range {
        background: #d4d4d4!important;
        height: 5px!important;
        margin-top: 0!important
    }

    #slider-range .ui-slider-handle {
        background: #444!important;
        border-radius: 100%!important;
        width: 15px!important;
        height: 15px!important;
        border: none!important;
        margin-top: 0!important;
        margin-right: -4px!important;
        top: -5px
    }

    #amount {
        color: #000;
        font-size: 12px;
        font-weight: 400;
        left: 0;
        padding: 15px 10px 10px;
        float: left;
        width: 100%;
        text-align: left;
        margin-bottom: 0
    }

    .sortingContent li:not(.appliedFilter) {
        border-bottom: 1px solid #ddd!important
    }

    .category-vertical-filters.top-filters .list-group.dropdown {
        background: #eee!important;
        margin-top: 5px
    }

    .category-vertical-filters.top-filters .list-group.dropdown li {
        background: #eee!important;
        margin-bottom: 0!important
    }
}

@media screen and (min-width: 992px) and (max-width:1024px) {
    .MusteriHizmet .Mtext a {
        font-size:13px
    }

    .MusteriHizmet .Mtext a p {
        font-size: 20px
    }

    .footer-blog {
        position: absolute;
        top: 150px
    }

    .Mobil-uygulama a {
        width: 100%;
        text-align: center
    }

    .Mobil-uygulama a:first-child {
        text-align: center
    }

    .mobilMenu {
        display: none!important
    }

    .navigation {
        float: right
    }

    .navigation .ResimliMenu1 {
        max-width: 95%;
        position: static
    }

    .navigation .HeaderMenu2 {
        max-width: 95%
    }

    .footerContainer,.ticiContainer.homeContainer {
        width: 100%
    }

    .ticiContainer.footerContainer {
        width: 100%
    }

    .headerContent {
        max-width: 95%
    }

    .ticiContainer {
        width: 100%
    }

    .HesabimContainer .centerCount {
        float: left;
        width: 70%
    }

    .HesabimContainer .leftBlock {
        width: 30%;
        float: left
    }

    .HesabimContainer .categoryTitle .categoryTitleText {
        width: 100%
    }

    .iletisimContent .row {
        width: 100%;
        margin-bottom: 30px
    }

    .mobilFilterOpenBtn {
        margin: 0 0 20px!important
    }

    .blockSelect {
        display: none
    }

    .leftImage {
        width: 47.2%
    }

    .RightDetail {
        width: 52.8%
    }

    .SmallImages div {
        height: 58px
    }

    .mobilFilterOpenBtn .button {
        padding: 6px 0;
        font-size: 12px;
        font-weight: 600
    }

    ul.breadcrumb {
        max-width: 100%
    }

    .sortingContent {
        margin-top: 0
    }

    .sortingContent li>a {
        font-size: 12px!important;
        padding: 0 6px!important
    }

    .appliedFilter.FiltrelemeUrunAdet span {
        font-size: 12px!important
    }

    .sortingContent .appliedFilter {
        display: none!important
    }

    .panel-heading a {
        padding-bottom: 0;
        font-size: 13px;
        line-height: 35px
    }

    .panel-heading {
        margin-bottom: 0!important;
        padding: 0 10px!important
    }

    .sortingContent li>a {
        text-align: center
    }

    .category-vertical-filters.top-filters .panel.vertical-top-price-filter {
        margin-left: 0!important
    }

    .category-vertical-filters.top-filters .panel {
        padding: 5px 10px!important
    }

    .category-vertical-filters.top-filters .panel .panel-heading a:after {
        top: 0!important
    }

    .categoryTitleText {
        max-width: 95%
    }

    .categoryContainer .centerCount {
        width: 100%
    }

    .category-vertical-filters .vertical-filter-panel .list-group-item a {
        font-size: 11px!important;
        line-height: 11px!important
    }

    .vertical-filter-panel .list-group-item.list-group-item-image {
        background: 0 0!important;
        height: auto!important
    }

    .category-vertical-filters.top-filters .list-group.dropdown li {
        margin-bottom: 10px!important
    }

    .category-vertical-filters .vertical-filter-panel .list-group-item:before {
        width: 9px!important;
        height: 10px!important;
        border: 1px solid #666!important;
        border-radius: 0;
        background: 0 0!important;
        display: inline-block!important;
        margin-top: 3px!important;
        text-align: center;
        line-height: 9px
    }

    .category-vertical-filters .vertical-filter-panel .list-group-item.selected:before {
        border-color: #666!important;
        background: #fff!important;
        content: '\f00c'!important;
        font-family: fontawesome;
        color: #666;
        font-size: 8px
    }

    .category-vertical-filters .vertical-filter-panel .list-group-item:hover:before {
        border-color: #666!important;
        background: #fff!important;
        content: '\f00c'!important;
        font-family: fontawesome;
        color: #666;
        font-size: 8px
    }

    ul.breadcrumb a {
        font-size: 9px!important
    }

    ul.breadcrumb a span {
        font-size: 9px!important
    }

    ul.breadcrumb li:after {
        font-size: 9px!important
    }

    ul.breadcrumb li:last-child {
        font-size: 9px!important
    }

    a#linkOncekiSayfa {
        font-size: 9px!important
    }

    .brandlistselection {
        border-bottom: none;
        padding: 0;
        height: auto
    }

    .sortingContent:before {
        display: none
    }

    .BlokTitle span {
        font-size: 13px;
        width: 250px
    }

    .searchContent {
        width: 35%
    }

    .navigation .ResimliMenu1>li>a {
        padding: 0 15px
    }

    .ban1 {
        margin-bottom: 5%
    }

    .GuvenList li .Gtext {
        font-size: 10px
    }

    .homeContainer .productItem:hover .productImage a:after {
        top: 77.8%
    }

    .FooterMiddle .ticiContainer {
        max-width: 95%
    }

    .MusteriHizmet .Mtext a {
        font-size: 12px
    }

    .MusteriHizmet .Mtext a p {
        font-size: 20px
    }

    .linkler>ul>li>a {
        font-size: 11px
    }

    .linkler>ul>li>ul>li>a {
        font-size: 11px
    }

    .Etitle {
        font-size: 11px
    }

    .linkler>ul>li>.Magazalar>a {
        font-size: 11px;
        line-height: 36px
    }

    .linkler>ul>li>.Magazalar>a:after {
        line-height: 36px;
        font-size: 23px
    }

    .BlokTitle2 span {
        font-size: 19px
    }

    .Blok .BlokText {
        font-size: 11px
    }

    .productItem .productName a {
        font-size: 11px
    }

    .productItem .productOnYazi * {
        font-size: 11px
    }

    .productItem .discountPrice span {
        font-size: 11px!important
    }

    .productItem .regularPrice {
        margin-top: 2px
    }

    .productItem .regularPrice span {
        font-size: 9px
    }

    .discountIcon {
        font-size: 14px;
        width: 29px;
        height: 21px;
        line-height: 23px
    }

    .newIcon {
        font-size: 8px;
        width: 29px;
        height: 20px
    }

    .firsatIcon {
        font-size: 8px;
        width: 40px
    }

    .cargoIcon {
        width: 48px;
        height: 48px;
        background-size: 100%
    }

    .TukendiIco span {
        font-size: 11px
    }

    .quickViewIco {
        left: 25px
    }

    .quickViewIco a {
        font-size: 10px
    }

    .favori {
        right: 13px
    }

    .favori a:after {
        font-size: 10px
    }

    .altMenu {
        width: 100%
    }

    .navigation .ResimliMenu1>li {
        position: static
    }

    .categoryContainer {
        padding: 0 10px
    }

    .ProductName h1 span:not(#divUrunKodu) {
        font-size: 16px
    }

    #divOnyazi * {
        font-size: 17px
    }

    #divIndirimOrani {
        width: 29px;
        height: 20px
    }

    #divIndirimOrani .indirimliOrani {
        font-size: 13px;
        line-height: 20px
    }

    #divIndirimOrani .indirimliOrani * {
        font-size: 13px;
        line-height: 20px
    }

    .PiyasafiyatiContent .right_line * {
        font-size: 8px
    }

    .IndirimliFiyatContent .right_line .spanFiyat {
        font-size: 13px
    }

    #divKargoBedava {
        margin-top: 5px;
        margin-right: 70px
    }

    #divKargoBedava .box1 {
        font-size: 9px
    }

    .PriceList {
        padding-bottom: 5px
    }

    #divUrunEkSecenek .eksecenekLine .right_line .size_box img {
        width: 30px;
        height: 30px
    }

    #divUrunEkSecenek .eksecenekLine .right_line .size_box {
        width: 36px
    }

    .basketBtn {
        width: 82%
    }

    .UFavorilerimeEkle .box1 {
        width: 30px;
        height: 30px
    }

    .UFavorilerimeEkle .box1 i:before {
        line-height: 30px;
        font-size: 19px
    }

    #divSatinAl {
        width: 63%
    }

    .productDetailContainer {
        width: 95%
    }

    .urunTabAlt * {
        font-size: 9px
    }

    #divUrunKodu {
        font-size: 9px
    }

    #divUrunKodu:before {
        font-size: 9px
    }

    #divBenzerUrun .categoryTitle .bold .satir1 {
        font-size: 18px
    }

    .AltBanner .AltBannerAlan .TextAlanB>div.One {
        font-size: 15px
    }

    .AltBanner .AltBannerAlan .TextAlanB>div.Two {
        font-size: 38px
    }

    .AltBanner .AltBannerAlan .TextAlanB>div.Three {
        font-size: 11px
    }

    .AltBanner .AltBannerAlan .TextAlanB>div.Four {
        font-size: 30px
    }

    .AltBanner .AltBannerAlan .TextAlanB>div.Five a {
        font-size: 14px
    }

    .banksimg .bankimgs img {
        max-width: 82%
    }

    .topText {
        font-size: 10px
    }

    .appliedFilter.FiltrelemeUrunAdet {
        display: none!important
    }

    .sepetimBody .AltBanner {
        display: none
    }
}

@media screen and (min-width: 768px) and (max-width:992px) {
    .MusteriHizmet .Mtext a {
        font-size:13px
    }

    .MusteriHizmet .Mtext a p {
        font-size: 20px
    }

    .footer-blog {
        position: absolute;
        top: 130px
    }

    .Mobil-uygulama a {
        width: 100%;
        text-align: center
    }

    .Mobil-uygulama a:first-child {
        text-align: center
    }

    .mobilMenuAcButton {
        display: none!important;
        bottom: auto;
        top: 6px;
        left: 25px;
        font-size: 30px;
        width: 70px
    }

    .mobilMenuAcButton span {
        font-size: 15px
    }

    .mobilMenuAcButton i.fa-search {
        font-size: 25px
    }

    .mobilMenu {
        width: 42%!important
    }

    .navigation {
        float: right
    }

    .navigation .ResimliMenu1 {
        max-width: 95%;
        position: static
    }

    .navigation .HeaderMenu2 {
        max-width: 95%
    }

    .headerContent {
        max-width: 95%
    }

    .footerContainer,.ticiContainer,.ticiContainer.homeContainer {
        width: 100%;
        padding: 0
    }

    .blockSelect {
        display: none
    }

    .HesabimContainer .centerCount {
        float: left;
        width: 70%
    }

    .HesabimContainer .leftBlock {
        width: 30%;
        float: left
    }

    #divIlgiliUrunler .productModuleItem,.sliderBannerContainer ul li,.ProductList.pr_4 .productItem {
        width: 31.5%
    }

    .sliderBannerContainer ul li:nth-child(3n) {
        margin-right: 0
    }

    .sliderBannerContainer ul li:nth-child(5n) {
        margin-right: 20px
    }

    .HesabimContainer .categoryTitle .categoryTitleText {
        width: 100%
    }

    .categoryContainer .categoryTitleText,.productDetailContainer .categoryTitle {
        width: 100%
    }

    .iletisimContent .row {
        width: 100%;
        margin-bottom: 30px
    }

    .mobilFilterOpenBtn {
        margin: 0
    }

    .category-vertical-filters>div {
        width: 100%!important
    }

    ul.breadcrumb {
        max-width: 95%
    }

    .leftImage {
        width: 47.2%
    }

    .RightDetail {
        width: 52.8%
    }

    .SmallImages div {
        height: 46px
    }

    .filterDeleteContent.ng-scope {
        padding: 0
    }

    .mobilFilterOpenBtn .button {
        font-size: 20px
    }

    .sortingContent {
        margin-top: 0
    }

    .panel-heading {
        margin-bottom: 0!important
    }

    .panel-heading a {
        line-height: 25px;
        font-size: 13px;
        padding-left: 10px
    }

    .category-vertical-filters>div {
        margin-bottom: 5px!important
    }

    .category-vertical-filters.top-filters .panel .panel-heading a:after {
        color: #000!important
    }

    .sortingContent li:not(.appliedFilter) {
        text-align: center!important
    }

    .sortingContent li>a {
        text-align: center!important;
        padding: 0!important
    }

    .sortingContent .appliedFilter {
        width: 100%;
        text-align: center!important;
        position: static;
        display: none!important
    }

    .mobilFilterOpenBtn .button {
        padding: 6px 0;
        font-size: 12px;
        font-weight: 600
    }

    .panel-heading a {
        padding-bottom: 0;
        font-size: 13px;
        line-height: 35px
    }

    .panel-heading {
        margin-bottom: 0!important;
        padding: 0 10px!important
    }

    .category-vertical-filters.top-filters .panel.vertical-top-price-filter {
        margin-left: 0!important
    }

    .category-vertical-filters.top-filters .panel {
        padding: 5px 10px!important
    }

    .category-vertical-filters.top-filters .panel .panel-heading a:after {
        top: 0!important
    }

    .categoryTitleText {
        max-width: 95%
    }

    .categoryContainer .centerCount {
        width: 100%
    }

    .category-vertical-filters .vertical-filter-panel .list-group-item a {
        font-size: 11px!important;
        line-height: 11px!important
    }

    .vertical-filter-panel .list-group-item.list-group-item-image {
        background: 0 0!important;
        height: auto!important
    }

    .category-vertical-filters.top-filters .list-group.dropdown li {
        margin-bottom: 10px!important
    }

    .category-vertical-filters .vertical-filter-panel .list-group-item:before {
        width: 9px!important;
        height: 10px!important;
        border: 1px solid #666!important;
        border-radius: 0;
        background: 0 0!important;
        display: inline-block!important;
        margin-top: 3px!important;
        text-align: center;
        line-height: 9px
    }

    .category-vertical-filters .vertical-filter-panel .list-group-item.selected:before {
        border-color: #666!important;
        background: #fff!important;
        content: '\f00c'!important;
        font-family: fontawesome;
        color: #666;
        font-size: 8px
    }

    .category-vertical-filters .vertical-filter-panel .list-group-item:hover:before {
        border-color: #666!important;
        background: #fff!important;
        content: '\f00c'!important;
        font-family: fontawesome;
        color: #666;
        font-size: 8px
    }

    ul.breadcrumb a {
        font-size: 9px!important
    }

    ul.breadcrumb li:after {
        font-size: 9px!important
    }

    ul.breadcrumb li:last-child {
        font-size: 9px!important
    }

    a#linkOncekiSayfa {
        font-size: 9px!important
    }

    .categoryTitleText {
        max-width: 95%
    }

    .brandlistselection {
        border-bottom: none;
        padding: 0;
        height: auto
    }

    .BlokTitle span {
        font-size: 13px;
        width: 250px
    }

    .searchContent {
        width: 35%
    }

    .navigation .ResimliMenu1>li>a {
        padding: 0 11px;
        font-size: 11px
    }

    .ban1 {
        margin-bottom: 5%
    }

    .GuvenList li {
        padding: 0 0 0 1%
    }

    .GuvenList li .Gtext {
        font-size: 8px
    }

    .GuvenList li .Gimg {
        width: 100%
    }

    .GuvenList li .Gimg img {
        max-width: 100%
    }

    .homeContainer .productItem:hover .productImage a:after {
        top: 77.8%
    }

    .FooterMiddle .ticiContainer {
        max-width: 95%
    }

    .MusteriHizmet .Mimg {
        width: 30px
    }

    .MusteriHizmet .Mimg img {
        width: 100%
    }

    .MusteriHizmet .Mtext a {
        font-size: 9px
    }

    .MusteriHizmet .Mtext a p {
        font-size: 15px
    }

    .linkler>ul>li>a {
        font-size: 11px
    }

    .linkler>ul>li>ul>li>a {
        font-size: 11px
    }

    .Etitle {
        font-size: 11px
    }

    .linkler>ul>li>.Magazalar>a {
        font-size: 11px;
        line-height: 36px
    }

    .linkler>ul>li>.Magazalar>a:after {
        line-height: 36px;
        font-size: 23px
    }

    .BlokTitle2 span {
        font-size: 19px
    }

    .Blok .BlokText {
        font-size: 11px
    }

    .productItem .productName a {
        font-size: 11px
    }

    .productItem .productOnYazi * {
        font-size: 11px
    }

    .productItem .discountPrice span {
        font-size: 11px!important
    }

    .productItem .regularPrice {
        margin-top: 2px
    }

    .productItem .regularPrice span {
        font-size: 9px
    }

    .discountIcon {
        font-size: 14px;
        width: 29px;
        height: 21px;
        line-height: 21px
    }

    .newIcon {
        font-size: 8px;
        width: 29px;
        height: 20px
    }

    .firsatIcon {
        font-size: 8px;
        width: 40px
    }

    .cargoIcon {
        width: 48px;
        height: 48px;
        background-size: 100%
    }

    .TukendiIco span {
        font-size: 11px
    }

    .quickViewIco {
        left: 25px
    }

    .quickViewIco a {
        font-size: 10px
    }

    .favori {
        right: 25px
    }

    .favori a:after {
        font-size: 10px
    }

    .altMenu {
        width: 100%
    }

    .navigation .ResimliMenu1>li {
        position: static
    }

    .categoryContainer {
        padding: 0 10px
    }

    .ProductName h1 span:not(#divUrunKodu) {
        font-size: 16px
    }

    #divOnyazi * {
        font-size: 17px
    }

    #divIndirimOrani {
        width: 29px;
        height: 20px
    }

    #divIndirimOrani .indirimliOrani {
        font-size: 13px;
        line-height: 20px
    }

    #divIndirimOrani .indirimliOrani * {
        font-size: 13px;
        line-height: 20px
    }

    .PiyasafiyatiContent .right_line * {
        font-size: 8px
    }

    .IndirimliFiyatContent .right_line .spanFiyat {
        font-size: 13px
    }

    #divKargoBedava .box1 {
        font-size: 9px
    }

    .PriceList {
        padding-bottom: 5px
    }

    #divUrunEkSecenek .eksecenekLine .right_line .size_box img {
        width: 30px;
        height: 30px
    }

    #divUrunEkSecenek .eksecenekLine .right_line .size_box {
        width: 36px
    }

    .basketBtn {
        width: 82%
    }

    .UFavorilerimeEkle .box1 {
        width: 30px;
        height: 30px
    }

    .UFavorilerimeEkle .box1 i:before {
        line-height: 30px;
        font-size: 19px
    }

    #divSatinAl {
        width: 82%
    }

    .productDetailContainer {
        width: 95%
    }

    .urunTabAlt * {
        font-size: 9px
    }

    #divUrunKodu {
        font-size: 9px
    }

    #divUrunKodu:before {
        font-size: 9px
    }

    #divBenzerUrun .categoryTitle .bold .satir1 {
        font-size: 18px
    }

    .AltBanner .AltBannerAlan .TextAlanB>div.One {
        font-size: 15px
    }

    .AltBanner .AltBannerAlan .TextAlanB>div.Two {
        font-size: 38px
    }

    .AltBanner .AltBannerAlan .TextAlanB>div.Three {
        font-size: 11px
    }

    .AltBanner .AltBannerAlan .TextAlanB>div.Four {
        font-size: 30px
    }

    .AltBanner .AltBannerAlan .TextAlanB>div.Five a {
        font-size: 14px
    }

    .ProductName {
        width: 82%
    }

    #divOnyazi {
        width: 82%
    }

    #divUrunEkSecenek {
        width: 82%
    }

    .banksimg .bankimgs img {
        max-width: 82%
    }

    .topText {
        font-size: 10px
    }

    .sortingContent:before {
        display: none
    }

    .appliedFilter.FiltrelemeUrunAdet {
        display: none!important
    }

    .sepetimBody .AltBanner {
        display: none
    }
}

.Mobil-blok {
    display: none
}

.Muser {
    display: none
}

#logo .Mlogo {
    display: none
}

.KatMobil {
    display: none
}

.MobilKategori {
    display: none
}

.nav-footer {
    display: none
}

@media screen and (max-width: 767px) {
    .mobilMenu>.nav-footer {
        display:block;
        float: left;
        width: 100%;
        margin-top: 10px
    }

    .mobilMenu>.nav-footer>.Area {
        float: none;
        background: 0 0;
        width: auto;
        padding: 0;
        margin-bottom: 10px
    }

    .mobilMenu>.nav-footer>.Area>.T {
        background-color: #eee;
        color: #383838;
        font-weight: 700;
        padding: 11px 18px;
        font-size: 14px
    }

    .mobilMenu>.nav-footer>.Area>.Content {
        padding: 10px 0
    }

    .mobilMenu>.nav-footer>.Area>.Content>.item {
        display: -webkit-flex;
        display: flex;
        align-items: center;
        justify-content: space-between
    }

    .mobilMenu>.nav-footer>.Area>.Content>.item>.column:first-child {
        flex: auto
    }

    .mobilMenu>.nav-footer>.Area>.Content>.item>.column>.control {
        padding-right: 13px;
        display: -webkit-flex;
        display: flex;
        align-items: center
    }

    .mobilMenu>.nav-footer>.Area>.Content>.item>.column>.control a {
        color: #252525;
        font-size: 14px
    }

    .mobilMenu>.nav-footer>.Area>.Content>.item>.column>.control>.Or {
        width: 1px;
        height: 16px;
        background-color: #cacaca;
        display: inline-block;
        margin: 0 4px
    }

    .mobilMenu>.nav-footer>.Area>.Content>.item>.column>.Link {
        width: 100%;
        padding: 10px 18px;
        display: -webkit-flex;
        display: flex;
        align-items: center;
        color: #383838;
        font-weight: 600;
        font-size: 14px
    }

    .mobilMenu>.nav-footer>.Area>.Content>.item>.column>.Link>i {
        font-size: 20px;
        margin-right: 10px
    }

    .mobilMenu>.nav-footer>.Area>.Content>.social-list {
        padding: 11px
    }

    .mobilMenu>.nav-footer>.Area>.Content>.social-list>.social-link {
        display: inline-block;
        font-size: 21px;
        color: #000;
        padding: 0 7px
    }

    .sagIcerikTutucu.ng-hide {
        display: block!important
    }

    .OdemeMenu ul.odemeSecenekMenu>li>a {
        height: auto!important
    }

    .OdemeMenu ul.odemeSecenekMenu>li>a>p {
        padding: 0 5px
    }

    body .mobilTicimaxLogo {
        display: none
    }

    body .hopi-btn {
        padding: 10px 30px;
        background-size: auto 23px
    }

    body .hopi-btn-cta-text,body .hopi-btn-used-campaign {
        margin-top: 3px
    }

    .bankiyzico img {
        max-width: 100%
    }

    .MobilKategori {
        display: block;
        float: left;
        width: 100%;
        padding: 15px 0;
        padding-left: 5px
    }

    .MobilKategori ul {
        white-space: nowrap;
        overflow-x: scroll;
        overflow-y: hidden;
        display: block;
        -webkit-overflow-scrolling: touch
    }

    .MobilKategori ul li {
        text-align: center;
        display: inline-block;
        width: 25%;
        vertical-align: top;
        margin-right: 5px
    }

    .MobilKategori ul li img {
        border-radius: 50%;
        border: .5px solid;
        padding: 1.5px
    }

    .MobilKategori ul li a {
        display: block
    }

    .MobilKategori ul li span {
        font-size: 17px;
        line-height: 33px;
        color: #000;
        margin-top: 0;
        font-weight: 300;
        display: block
    }

    #formPuan {
        text-align: center
    }

    #iframePuan {
        width: 100%
    }

    .BasketPuanKullanim {
        padding: 10px 0
    }

    #BedenTabloHtml {
        padding: 15px
    }

    #BedenTabloHtml>ul>li>a {
        padding: 10px 15px;
        font-size: 11px
    }

    .BedenAccordionTitle a {
        line-height: 30px;
        font-size: 11px
    }

    .BedenAccordionTitle {
        margin-bottom: 0
    }

    .BedenAccordion {
        margin-top: 5px
    }

    .filterDeleteContent {
        position: static
    }

    #divOzelAlan3 {
        display: none;
        float: left;
        margin-left: 1%;
        margin-bottom: -11px;
        margin-top: 10px;
        font-size: 13px;
        color: #c90000
    }

    .siparisOzet .UrunContent .sepetItem>div {
        display: block
    }

    .addressCol {
        float: left;
        width: 100%
    }

    #divUrunKodu {
        padding-left: 0
    }

    #divOzelAlan2 {
        padding-left: 0
    }

    #divOzelAlan4 {
        padding-left: 0
    }

    .ItemOrj {
        padding: 0 9px
    }

    .categoryContainer .ProductList {
        margin: 0 -2.5px
    }

    #divBenzerUrun .JKatAdi .bold .satir1 {
        float: left;
        width: 100%;
        padding-left: 15px;
        text-align: left;
        font-size: 14px;
        font-weight: 700;
        background: #e9e9e9;
        margin-bottom: 5px;
        height: 48px;
        line-height: 52px
    }

    .urunTabAlt.active {
        display: block
    }

    .Mozellik {
        float: left;
        width: 100%
    }

    .Mobilozellik {
        display: none;
        float: left;
        width: 100%;
        text-align: center;
        margin: 15px 0
    }

    .Mobilozellikbtn {
        display: inline-block;
        height: 35px;
        width: 200px;
        line-height: 35px;
        border: 2px solid #ddd;
        font-size: 14px;
        color: #000
    }

    .Mobilozellikbtn.active {
        font-size: 0
    }

    .Mobilozellikbtn.active:after {
        content: "GİZLE";
        line-height: 35px;
        font-size: 14px;
        color: #000
    }

    #divUrunEkSecenek .eksecenekLine {
        margin-bottom: 5px;
        margin-top: 13px
    }

    .OzellikClick {
        font-size: 0
    }

    .OzellikClick i {
        display: none
    }

    .OzellikClick:after {
        content: "ÜRÜN DETAYI";
        float: left;
        width: 100%;
        color: #747474;
        font-size: 15px
    }

    .KatMobil {
        display: block;
        float: left;
        width: 100%;
        text-align: center;
        position: relative;
        max-height: 93px;
        overflow: hidden
    }

    .KatMobil.active {
        max-height: 1000000px
    }

    .KatMobil span {
        font-family: josefin sans,sans-serif!important;
        font-size: 25px;
        color: #000;
        font-weight: 300
    }

    .KatAcBtn {
        position: absolute;
        left: 0;
        right: 0;
        margin: auto;
        line-height: 32px;
        background: #fff;
        bottom: 0
    }

    .KatMobil.active .KatAcBtn {
        font-size: 0
    }

    .KatMobil.active .KatAcBtn:before {
        content: "Gizle";
        font-size: 12px
    }

    .MF .mflink.Fav {
        width: 20px;
        height: 20px
    }

    .MF .mflink.Fav a img {
        display: none
    }

    .MF .mflink.Fav a:before {
        content: "";
        font-family: fontawesomepro;
        font-size: 19px;
        color: #fff;
        display: block;
        font-weight: 300
    }

    .mycart .sepetTecxt:before {
        background: 0 0;
        content: "";
        font-family: fontawesomepro;
        color: #fff;
        font-size: 19px;
        margin-bottom: 0;
        font-weight: 300
    }

    .teknikDetay {
        float: left;
        width: 100%
    }

    .magazaSelect,#searchStore {
        width: 100%!important
    }

    .cookietudors {
        padding-right: 35px;
        font-weight: 300;
        text-align: left
    }

    .kapatx {
        right: 14%;
        width: 23%;
        font-weight: 300;
        height: 26%;
        padding: 5px 11px 3px;
        top: 71%;
        font-size: 14px;
        border: 1px solid;
        border-radius: 1.5px
    }

    .OzelNewTabSag {
        width: 100%
    }

    #pnlSlider {
        display: block
    }

    .Blok {
        display: none
    }

    #anasayfatab {
        display: none
    }

    .HomeBody .AltBanner {
        display: none
    }

    #header .H-blog {
        display: none
    }

    .HomeBody .Mobil-blok .AltBanner {
        display: block
    }

    .Mobil-Blok-Banner {
        float: left;
        width: 100%;
        background: #eee;
        color: #000;
        font-size: 12px;
        font-weight: 400;
        line-height: 30px;
        margin-bottom: 10px
    }

    .Mobil-Blok-Banner span {
        font-size: 13px;
        font-weight: 700;
        margin-left: 5px
    }

    .Mobil-blok {
        display: block!important;
        float: left;
        width: 100%;
        text-align: center
    }

    .Mobil-Blok-Box {
        float: left;
        width: 100%;
        position: relative
    }

    .Mobil-Blok-Box-Button {
        position: absolute;
        bottom: 15px;
        right: 0;
        left: 0;
        margin: auto;
        width: 250px
    }

    .Mobil-Blok-Box-Button a {
        float: left;
        width: 115px;
        margin-right: 10px;
        border: 1px solid #000;
        background-color: #fff;
        color: #000;
        font-weight: 400;
        font-size: 13px;
        text-align: center;
        line-height: 32px;
        margin-bottom: 15px;
        height: 30px
    }

    .mobil-box-5 .Mobil-Blok-Box-Button {
        text-align: center;
        width: 319px;
        bottom: 45px
    }

    .mobil-box-5 .Mobil-Blok-Box-Button a {
        font-size: 10px;
        width: 85px;
        line-height: 28px;
        height: 26px;
        margin: 0
    }

    .mobil-box-5 .Mobil-Blok-Box-Button a:last-child {
        float: right
    }

    .mobil-box-5 .Mobil-Blok-Box-Button a:nth-last-child(2) {
        float: none;
        display: inline-block
    }

    .Mobil-Guvenlist {
        width: 100%;
        float: left;
        padding-bottom: 15px
    }

    .Mobil-Guvenlist ul li {
        width: 48%;
        float: left;
        padding: 11px 0 9px 11px;
        background: #f7f7f7;
        margin-bottom: 10px;
        margin: 0 0 5px 5px;
        text-align: center;
        position: relative
    }

    .Mobil-Guvenlist .Gimg {
        float: left;
        max-width: 20px;
        min-width: 20px
    }

    .Mobil-Guvenlist .Gtext {
        color: #313131;
        font-size: 10px;
        font-weight: 400;
        text-align: center;
        padding-top: 9px
    }

    .Mobil-Guvenlist .HoverAlan {
        font-size: 10px;
        line-height: 14px
    }

    .Mobil-Guvenlist ul li.active .HoverAlan {
        display: block;
        width: 100%;
        box-shadow: none
    }

    .navigation .ResimliMenu1>li:last-child {
        display: block
    }

    #BedenForm #ngFormController {
        width: auto
    }

    .MF .H-blog {
        margin-right: 3px;
        margin-top: -10px
    }

    .footer-blog {
        display: none
    }

    #anasayfatab:before {
        display: none
    }

    #anasayfatab:after {
        display: none
    }

    #anasayfatab {
        margin: 5px 0;
        padding: 10px 0
    }

    #anasayfatab .anasayfaTabAlt.active {
        padding: 15px 0
    }

    .headerContent {
        border-bottom: none;
        background: #000;
        height: 50px
    }

    .headerContent:after {
        content: "";
        position: absolute;
        left: 0;
        right: 0;
        bottom: -5px;
        height: 1px;
        background: #e0e0e0
    }

    .Mobil-uygulama {
        padding-right: 0
    }

    .Mobil-uygulama a {
        display: inline;
        float: left
    }

    .flex-direction-nav {
        display: none
    }

    .mobilMenuAcButton {
        display: inline-block!important;
        bottom: auto;
        top: 11px;
        left: 13px;
        font-size: 30px;
        width: auto;
        color: #fff
    }

    .navigation {
        display: none
    }

    .ticiContainer.homeContainer {
        width: 100%;
        padding-left: 5px;
        padding-right: 5px
    }

    .ticiContainer.footerContainer {
        width: 100%;
        padding-left: 5px;
        padding-right: 5px
    }

    .ticiContainer.productDetailContainer {
        width: 100%;
        padding-left: 0;
        padding-right: 0
    }

    .Muser {
        position: absolute;
        right: 77px;
        top: 15px;
        font-size: 20px;
        color: #000;
        display: none
    }

    .Muser i {
        font-weight: 400;
        color: #454545
    }

    .footerContainer,.headerContent,.ticiContainer {
        width: 100%;
        padding-left: 0;
        padding-right: 0
    }

    .centerCount .ticiContainer {
        padding: 0
    }

    .grid {
        width: 100%;
        margin: 0;
        padding: 10px;
        border: none;
        margin-bottom: 10px
    }

    .SifremiUnuttum {
        width: 100%;
        margin: 0;
        padding: 0
    }

    .SifremiUnuttum .line {
        width: 59.5%
    }

    .SifremiUnuttum #mainHolder_txtbxMail {
        width: 70%
    }

    .SifremiUnuttum .button {
        width: 30%
    }

    .leftBlock {
        width: 100%;
        padding: 0
    }

    .categoryContainer .centerCount {
        width: 100%
    }

    .blockSelect {
        display: none
    }

    .Images {
        width: 100%;
        margin-bottom: 10px;
        padding-bottom: 128%
    }

    .leftImage {
        width: 100%;
        padding: 0;
        margin-bottom: 8px;
        margin-top: 0
    }

    .SmallImages {
        width: 100%;
        max-height: 100%;
        margin-left: 0;
        padding: 0 5px
    }

    .SmallImages div {
        width: 23.7%;
        margin-right: 5px;
        margin-bottom: 5px!important;
        height: 87px
    }

    .SmallImages div:nth-child(4n) {
        margin-right: 0
    }

    .RightDetail {
        width: 100%;
        margin-bottom: 25px;
        margin-right: 0;
        margin-left: 0;
        padding: 0 5px
    }

    .urunTab {
        padding: 0;
        width: 100%;
        height: auto
    }

    .urunTab ul {
        padding: 0
    }

    .urunTab li {
        float: left;
        padding: 0;
        margin-bottom: 0
    }

    .urunTab li:last-child {
        border: none
    }

    .urunTab li a {
        width: 100%;
        padding: 0;
        font-size: 14px;
        line-height: 30px;
        text-align: left;
        border: none
    }

    .urunDetayPanel {
        margin-top: -11px;
        max-height: 10000000px
    }

    .urunTabAlt #yorumYaz {
        padding-right: 0
    }

    #mainHolder_UrunDetay_txtbxNotlar,.urunTabAlt ul li input[type=text] {
        width: 100%!important
    }

    .leftBlock {
        display: none
    }

    #divBenzerUrun ul {
        width: 100%
    }

    #linkOncekiSayfa {
        float: right!important;
        clear: left
    }

    .HesabimContainer .centerCount {
        float: left;
        width: 100%;
        padding-left: 0;
        padding-top: 10px
    }

    .HesabimContainer .leftBlock {
        width: 100%;
        float: left
    }

    .uyelikBilgilerimSpan.row {
        width: 100%;
        margin: 0
    }

    .HesabimAdresContent .row {
        margin: 0 0 10px;
        float: left;
        width: 100%
    }

    .BasketBtn {
        width: 100%
    }

    .basketBtn {
        width: 77%;
        height: 100%;
        margin-left: 0
    }

    .buyfast {
        width: 100%;
        margin-left: 0;
        margin-top: 10px
    }

    .Basketinp {
        width: 145px
    }

    #divIlgiliUrunler .productModuleItem,.ProductList.sort_4 .productItem,.sliderBannerContainer ul li {
        width: 49%;
        height: auto
    }

    #divIlgiliUrunler .productModuleItem:nth-child(2n+1),.ProductList.sort_4 .productItem:nth-child(2n),.sliderBannerContainer ul li:nth-child(2n) {
        margin-right: 0
    }

    #divNewsLetter {
        width: 100%
    }

    .TumKategoriler {
        float: left;
        width: 100%;
        background: #fd9500;
        padding: 5px;
        color: #fff;
        font-size: 14px;
        font-weight: 700;
        line-height: 21px;
        cursor: pointer;
        text-align: center;
        display: block
    }

    .TumKategoriler .fa-bars {
        float: left;
        font-size: 20px
    }

    .TumKategoriler .fa-chevron-down {
        float: right;
        font-size: 14px;
        text-align: right;
        line-height: 18px
    }

    .sliderBannerContainer ul .slick-slide {
        width: 100%;
        margin-right: 0!important
    }

    #txtbxurunSiparisAdedi_wrapper {
        width: 100%!important
    }

    .HesabimContainer .categoryTitle .categoryTitleText {
        width: 100%
    }

    .linkler li {
        width: 100%!important;
        padding: 5px;
        text-align: center
    }

    .social li {
        width: 60px!important;
        margin: 0
    }

    .linkler li ul {
        margin-bottom: 15px;
        float: left;
        width: 100%
    }

    .ebultenDiv {
        width: 100%!important;
        border: none;
        display: inline-block;
        padding: 0;
        margin: 10px 0
    }

    .categoryContainer .categoryTitleText,.productDetailContainer .categoryTitle {
        width: 100%;
        padding: 0;
        margin-top: 0;
        border-bottom: none;
        margin-bottom: 15px
    }

    #pnlSlider .flex-direction-nav {
        margin-top: -23px
    }

    .userLeftBox,.userRightBox {
        margin: 7px!important;
        padding: 7px!important
    }

    .spanTittle {
        font-size: 18px!important
    }

    .iletisimContent .row {
        width: 100%;
        margin-bottom: 10px
    }

    .searchContent {
        width: auto;
        margin: 0;
        height: 37px;
        top: auto;
        left: 9px;
        right: 9px;
        margin: auto;
        display: block;
        background: 0 0;
        bottom: -47px
    }

    .CategoryBody .searchContent,.MagazaSayfa .searchContent {
        display: none
    }

    #divAramaKategori select {
        height: 30px;
        width: 83px;
        padding-left: 5px;
        display: none
    }

    #txtbxArama {
        height: 35px;
        padding-left: 10px;
        padding-right: 35px;
        width: 100%;
        box-shadow: none;
        font-size: 12px;
        margin: 0;
        padding-top: 2px
    }

    #btnKelimeAra {
        height: 32px;
        right: 0;
        top: 0;
        width: 30px;
        line-height: 30px;
        background-size: 50% 50%
    }

    .search:after {
        line-height: 32px
    }

    #header {
        margin-bottom: 0;
        padding-top: 0;
        box-shadow: none;
        background: #fff;
        z-index: 99;
        height: 125px
    }

    .CategoryBody #header,.MagazaSayfa #header {
        height: 51px;
        border-top: 0
    }

    .ProductBody #header {
        height: 51px;
        border-top: 0
    }

    .ProductBody .searchContent {
        display: none
    }

    .topText {
        font-size: 10px;
        text-align: center;
        padding-left: 10px
    }

    .welcomeOpen {
        display: block;
        font-size: 25px;
        color: #505050;
        position: absolute;
        right: 40px;
        top: 14px
    }

    .welcome {
        width: auto;
        position: relative;
        top: 0;
        right: 0;
        text-align: center;
        background: 0 0;
        padding: 0;
        margin: 0;
        height: auto;
        position: absolute;
        right: 88px;
        top: 17px
    }

    .mobilMenu .welcome {
        display: none
    }

    .welcome li {
        width: auto
    }

    .headerHesabim,.headerCikis {
        padding: 0;
        color: #7d7d7d;
        font-size: 13px;
        font-weight: 400;
        
        width: auto;
        height: auto;
        background: 0 0!important;
        line-height: normal;
        border: none;
        display: inline-block;
        font-size: 0!important
    }

    .headerUyeOl a,.headerUyeGiris a {
        padding: 0;
        color: #7d7d7d;
        font-size: 13px;
        font-weight: 400;
        
        width: 100%;
        height: auto;
        background: 0 0!important;
        line-height: normal;
        border: none;
        display: inline-block;
        font-size: 0!important
    }

    .headerUyeGiris a,.headerHesabim {
        border-right: none
    }

    .headerUyeOl a:after,.headerUyeGiris a:after,.headerHesabim:after,.headerCikis:after {
        display: none
    }

    .headerHesabim:after,.headerUyeGiris a:after {
        content: "";
        font-family: fontawesomepro;
        font-size: 20px!important;
        font-weight: 300;
        color: #fff;
        display: block;
        margin: 0;
        width: 20px;
        height: 20px
    }

    .footerMiddle {
        padding: 20px 0
    }

    #logo {
        float: left;
        margin-left: 55px
    }

    .sepetimBody #logo {
        margin-left: 0
    }

    #logo .logo {
        padding: 3px 0 13px;
        width: 121px;
        margin: 0 auto;
        display: none
    }

    #logo .Mlogo {
        display: block
    }

    #logo .logo img {
        max-width: 100%
    }

    ul.breadcrumb {
        padding: 0 5px!important;
        text-align: center
    }

    body.overflow {
        position: fixed;
        top: 0;
        left: 0;
        right: 0;
        overflow: hidden!important
    }

    body.overflow #header.fixed {
        border: none!important
    }

    body.overflow #divIcerik.margin {
        margin-top: 47px
    }

    .mycart {
        background: 0 0!important;
        width: 17px;
        right: 15px;
        top: 16px
    }

    .mycart:hover .CartProduct {
        display: block!important
    }

    .mycartClick {
        font-size: 24px;
        top: 14px;
        right: 5px;
        width: 25px;
        height: 25px;
        position: absolute;
        color: #505050;
        display: block
    }

    .CartProduct {
        position: fixed;
        right: -100%;
        top: 0;
        width: 80%;
        height: 100%;
        padding: 20px 5px 20px 20px;
        display: block!important;
        transition: all .3s ease;
        -moz-transition: all .3s ease;
        -webkit-transition: all .3s ease;
        -o-transition: all .3s ease
    }

    .CartProduct.animated {
        right: 0
    }

    .CartProduct .SProduct {
        float: left;
        width: 100%;
        height: calc(100% - 90px);
        overflow-y: auto;
        overflow-x: hidden;
        padding-right: 20px
    }

    .CartProduct .SProduct::-webkit-scrollbar {
        width: 4px
    }

    .CartProduct .SProduct::-webkit-scrollbar-track {
        background: #f6f6f6
    }

    .CartProduct .SProduct::-webkit-scrollbar-thumb {
        background: #dbdbdb;
        border-radius: 0
    }

    .CartProduct .SProduct li {
        float: left;
        width: 100%;
        border-bottom: 1px solid #e5e5e5;
        position: relative;
        margin-bottom: 10px;
        padding-bottom: 10px
    }

    .CartProduct .SProduct li:last-child {
        border-bottom: none
    }

    .CartProduct .SProduct li a img {
        float: left;
        width: 83px;
        height: 100%!important;
        display: block!important;
        border: 1px solid #e5e5e5;
        margin-right: 10px
    }

    .CartProduct .SProduct li .SepettopAd {
        float: left;
        width: 54%
    }

    .CartProduct .SProduct li .SepettopAd span:first-child {
        color: #000;
        font-size: 12px;
        float: left;
        margin-bottom: 10px;
        width: 100%;
        font-weight: 400;
        border-bottom: 1px solid #e5e5e5;
        padding-bottom: 10px;
        overflow: hidden;
        display: -webkit-box;
        -webkit-line-clamp: 2;
        -webkit-box-orient: vertical
    }

    .CartProduct .SProduct li .SepettopAd span:last-child {
        color: #000;
        font-size: 12px;
        float: left;
        padding: 0;
        margin: 0;
        width: 100%;
        font-weight: 400
    }

    .CartProduct .SProduct li .SepetTopAdet {
        float: left;
        color: #000;
        font-size: 12px;
        font-weight: 400
    }

    .CartProduct .SProduct li .SepetTopbirim {
        float: left;
        color: #000;
        font-size: 12px;
        font-weight: 400
    }

    .CartProduct .SProduct li .sepetTopFiyat {
        
        display: inline-block!important;
        color: #000;
        font-size: 12px;
        width: 55%;
        text-align: right;
        font-weight: 400
    }

    .CartProduct .SPrice {
        float: left;
        width: 100%;
        margin-bottom: 0;
        position: absolute;
        left: 0;
        bottom: 60px;
        padding: 0 20px
    }

    .CartProduct .SPrice li {
        float: right;
        color: #000;
        font-size: 14px;
        font-weight: 400
    }

    .CartProduct .SPrice .sepetToplamTutar {
        font-weight: 400;
        font-size: 25px;
        color: #000;
        line-height: 30px;
        margin-left: 10px
    }

    .CartProduct .button {
        display: inline-block!important;
        background: #000;
        padding: 0 7px;
        font-size: 9px;
        line-height: 30px;
        color: #fff;
        font-weight: 400;
        text-transform: uppercase;
        position: absolute;
        left: 20px;
        bottom: 20px
    }

    .CartProduct .headerOrderBtn {
        display: inline-block!important;
        color: #fff;
        background: #000;
        left: auto;
        right: 20px
    }

    .CartProduct .SProduct li a:nth-child(2) {
        position: absolute;
        right: -15px;
        top: 0
    }

    .CartProduct .SProduct li a:nth-child(2) span i {
        color: #b13434;
        font-size: 15px
    }

    .divustSepetteUrunYok span {
        width: 100%;
        float: left;
        text-align: center;
        color: #000;
        font-weight: 500;
        line-height: 30px;
        font-size: 20px;
        margin-bottom: 15px
    }

    .CartProduct.SepetBos .SPrice {
        display: none
    }

    .CartProduct.SepetBos .button {
        display: none!important
    }

    .sepetTopTutar {
        font-size: 0;
        padding: 0;
        border: none
    }

    .ngrs-range-slider .ngrs-value {
        position: absolute!important
    }

    .ebultenGelecek {
        width: 100%
    }

    .ProductIcon {
        padding: 0;
        position: static;
        width: 100%;
        border: none
    }

    .ProductIcon .box1 {
        text-align: left;
        padding: 0;
        border: none;
        margin-bottom: 10px;
        line-height: 33px;
        width: auto
    }

    .ProductIcon .box1 i {
        margin-bottom: 0;
        margin-right: 5px;
        font-size: 16px;
        line-height: 33px;
        text-align: center;
        margin-left: 0;
        width: auto
    }

    .ProductIcon .UIstekListemeEkle,.ProductIcon #divKritikStok,.ProductIcon .UGelinceHaberVer,.ProductIcon #divTelefonSiparis,.ProductIcon .UFavorilerimeEkle,.ProductIcon #divIndirimliUrun,.ProductIcon .FiyatHaberVer,.ProductIcon #divKargoBedava {
        width: 100%;
        margin: 0;
        padding: 0
    }

    .ProductIcon2 .YorumYazbtnContent a,.ProductIcon2 .TavsiyeEtBtnContent a,.ProductIcon2 .hidden-phone a {
        padding: 0 16px;
        display: none
    }

    .socialButons {
        display: block
    }

    .socialButons div {
        height: 0
    }

    .socialButons #___plus_0 {
        height: 0!important
    }

    .UTelegram {
        display: none!important
    }

    .telegram {
        width: 35px!important;
        height: 35px;
        font-size: 0;
        border-radius: 100%!important;
        display: none!important
    }

    .telegram i {
        font-size: 15px!important;
        line-height: 35px
    }

    .panel-heading {
        margin-bottom: 0!important
    }

    .panel-heading a {
        line-height: 35px;
        font-size: 12px
    }

    .category-vertical-filters>div {
        margin-bottom: 0!important;
        padding: 0;
        width: 100%!important;
        margin-right: 0!important
    }

    .category-vertical-filters>div.div-secenek-2 {
        display: none
    }

    .category-vertical-filters .closeb {
        position: static;
        float: left;
        width: 100%;
        margin: 10px 0 0
    }

    .category-vertical-filters.top-filters .panel.vertical-top-price-filter {
        width: 100%!important;
        margin: 0!important
    }

    .category-vertical-filters.top-filters .panel .panel-heading a:after {
        color: #000!important;
        top: 10px!important
    }

    .sortingContent {
        margin-top: 0
    }

    .sortingContent li:not(.appliedFilter) {
        padding: 0!important
    }

    .sortingContent li>a {
        text-align: center;
        line-height: 58px!important
    }

    .sortingContent li a span {
        border: none
    }

    .sortingContent .appliedFilter {
        width: 100%;
        text-align: center!important;
        padding: 0!important;
        position: static
    }

    .mobilFilterOpenBtn .button {
        padding: 6px 0;
        font-size: 12px;
        font-weight: 600;
        line-height: 20px
    }

    .panel-heading a {
        padding-bottom: 0;
        font-size: 16px;
        line-height: 58px;
        text-align: left
    }

    .panel-heading {
        margin-bottom: 0!important;
        padding: 0 10px!important
    }

    .category-vertical-filters.top-filters .panel.vertical-top-price-filter {
        margin-left: 0!important
    }

    .category-vertical-filters.top-filters .panel {
        padding: 2px!important
    }

    .category-vertical-filters.top-filters .panel .panel-heading a:after {
        top: 0!important
    }

    .categoryTitleText {
        max-width: 100%
    }

    .categoryContainer .centerCount {
        width: 100%
    }

    .category-vertical-filters .vertical-filter-panel .list-group-item a {
        font-size: 16px!important;
        line-height: 50px!important
    }

    .vertical-filter-panel .list-group-item.list-group-item-image {
        background: 0 0!important;
        height: auto!important
    }

    .category-vertical-filters.top-filters .list-group.dropdown li {
        margin-bottom: 10px!important;
        border-bottom: 1px solid #c7c7c7
    }

    .category-vertical-filters .vertical-filter-panel .list-group-item:before {
        position: absolute;
        right: 0;
        width: auto!important;
        height: auto!important;
        border: none!important;
        border-radius: 0;
        background: 0 0!important;
        display: inline-block!important;
        margin-top: 19px!important;
        text-align: center;
        line-height: 9px
    }

    .category-vertical-filters .vertical-filter-panel .list-group-item.selected:before {
        border-color: #666!important;
        background: 0 0!important;
        content: '\f00c'!important;
        font-family: fontawesome;
        color: #cc1332;
        font-size: 15px
    }

    .slider-range {
        background: #dedede;
        height: 5px!important;
        width: 93%;
        margin: 15px 10px 0!important;
        border: none;
        float: left
    }

    .slider-range .ui-slider-range {
        background: #d4d4d4!important;
        height: 5px!important;
        margin-top: 0!important
    }

    .slider-range .ui-slider-handle {
        background: #444!important;
        border-radius: 100%!important;
        width: 15px!important;
        height: 15px!important;
        border: none!important;
        margin-top: 0!important;
        margin-right: -4px!important;
        top: -5px
    }

    .amount {
        color: #000;
        font-size: 12px;
        font-weight: 400;
        left: 0;
        padding: 15px 10px 10px;
        float: left;
        width: 100%;
        text-align: left;
        margin-bottom: 0
    }

    body .filterDeleteContent .appliedFilter {
        margin: 0!important
    }

    .brandlistselection {
        border-bottom: none;
        padding: 0;
        height: auto
    }

    .productDetailContainer .categoryTitle,.proCategoryTitle.categoryTitleText {
        width: 100%;
        padding: 0;
        margin: 0;
        border-bottom: none
    }

    .proCategoryTitle.categoryTitleText {
        margin: 10px 0 0;
        display: none
    }

    .sortingContent li a span {
        line-height: 30px
    }

    .appliedFilter.FiltrelemeUrunAdet span {
        line-height: 30px!important;
        float: none!important
    }

    ul.breadcrumb a {
        font-size: 9px!important
    }

    ul.breadcrumb a span {
        font-size: 9px!important
    }

    ul.breadcrumb li {
        font-size: 0!important;
        float: none!important
    }

    ul.breadcrumb li:last-child {
        font-size: 9px!important
    }

    ul.breadcrumb li:after {
        font-size: 9px!important
    }

    a#linkOncekiSayfa {
        font-size: 8px!important;
        clear: none;
        display: none!important
    }

    #divIlgiliUrunler .modulediscount span,.productModuleItem2 .modulediscount span,.productItem .discountPrice span {
        font-size: 12px!important
    }

    .productModuleItem2 .moduleregular span,#divIlgiliUrunler .moduleregular span,.productItem .regularPrice span {
        font-size: 10px!important
    }

    .productModuleItem2 .moduleregular,#divIlgiliUrunler .moduleregular,.productItem .regularPrice {
        margin-top: 0;
        margin-right: 5px
    }

    #divIcerik {
        padding-top: 0!important;
        margin-top: 0
    }

    .MagazaSayfa #divIcerik {
        padding: 0 5px
    }

    .mycart .sepetTopTutar {
        display: none!important
    }

    .mycart .sepetUrun {
        display: none!important
    }

    .mycart .sepetTecxt {
        font-size: 0;
        width: 17px;
        float: left
    }

    .Magza {
        display: none
    }

    .MF {
        top: 18px;
        right: 50px
    }

    .MF .mflink a {
        font-size: 0
    }

    .AltBanner {
        margin: 5px 0
    }

    .CategoryBody .AltBanner {
        display: none
    }

    .AltBanner .AltBannerAlan .TextAlanB {
        height: 30px
    }

    .AltBanner .AltBannerAlan .TextAlanB>div {
        line-height: 35px
    }

    .AltBanner .AltBannerAlan .TextAlanB>div.Five {
        display: none
    }

    .AltBanner .AltBannerAlan .TextAlanB>div.One {
        font-size: 10px;
        margin-right: 10px;
        letter-spacing: 3px
    }

    .AltBanner .AltBannerAlan .TextAlanB>div.Two {
        font-size: 27px
    }

    .AltBanner .AltBannerAlan .TextAlanB>div.Three {
        font-size: 9px;
        margin-left: 0;
        margin-right: 9px;
        margin-top: 7px
    }

    .AltBanner .AltBannerAlan .TextAlanB>div.Four {
        font-size: 13px;
        margin-right: 0
    }

    #pnlSlider .flex-control-nav {
        right: 5px
    }

    #pnlSlider .flex-control-paging li a {
        width: 11px;
        height: 11px
    }

    .SliderYan {
        width: 100%!important;
        margin-top: 5px
    }

    .SliderYan .ban1 {
        margin-bottom: 1.6%
    }

    .BlokTitle span {
        width: auto;
        padding: 0 10px;
        font-size: 10px;
        line-height: 30px
    }

    .SliderYonetim {
        padding: 10px;
        margin: 0 0 5px
    }

    .SliderYonetim .SliderYonetimAlt {
        padding: 12px
    }

    .SliderYonetim2 {
        margin: 0 0 5px;
        padding: 0
    }

    .SliderYonetim2 .SliderYonetimAlt {
        padding: 0
    }

    .GuvenList {
        padding: 0;
        display: none
    }

    .Blok .BlokText {
        right: 10%;
        left: 10%
    }

    .Blok .BlokText a {
        font-size: 10px
    }

    .ban {
        margin: 0;
        float: left
    }

    .ban1 {
        width: 100%;
        margin-right: 0
    }

    .ban2 {
        width: 100%;
        margin-right: 0;
        margin-bottom: 5px
    }

    .ban2.col-xs-6 {
        width: 100%;
        padding: 0;
        margin-right: 5px
    }

    .ban2.col-xs-6:first-child {
        margin-top: 10px
    }

    .ban2.col-xs-6:last-child {
        margin-right: 0
    }

    .ban2.col-xs-6 .BlokText {
        font-size: 6px;
        line-height: 17px;
        bottom: 10px
    }

    .ban2.col-xs-6 .BlokText a {
        font-size: 6px;
        line-height: 17px;
        bottom: 10px
    }

    .ban2 .ban1 {
        margin-bottom: 5px
    }

    .ban2 .ban1:last-child {
        margin-bottom: 0
    }

    .ban3 {
        width: 100%;
        margin-right: 0;
        margin-bottom: 5px
    }

    .ban4 {
        width: 100%;
        margin-right: 0;
        margin-bottom: 5px
    }

    .ban5 {
        width: 100%;
        margin-right: 0;
        margin-bottom: 5px
    }

    .ban6 {
        width: 100%;
        margin-right: 0;
        margin-bottom: 5px
    }

    .ban4:last-child {
        margin-bottom: 5px
    }

    .ban2:last-child {
        margin-bottom: 0
    }

    .ban2>.row>a {
        padding: 0 5px
    }

    .BlokTitle2 {
        margin-bottom: 0
    }

    .BlokTitle2 span {
        font-size: 17px
    }

    .BlokTitle2:after {
        left: 0;
        right: 0;
        background: #000;
        height: 2px
    }

    .anasayfatab {
        padding: 10px 0;
        margin-top: 0;
        margin-bottom: 5px
    }

    .anasayfatab .anasayfaTabAlt.active {
        padding: 10px 0
    }

    ._tabHead {
        padding: 0
    }

    ._tabHead li a {
        font-size: 10px;
        line-height: 28px
    }

    .sliderBannerContainer .owl-carousel {
        padding: 0
    }

    .anasayfatab section.block:after {
        display: none
    }

    .anasayfatab section.block:before {
        display: none
    }

    .ProductName h1 span:not(#divUrunKodu) {
        font-size: 16px
    }

    #divOnyazi * {
        font-size: 16px;
        font-weight: 400;
        color: #4c4c4c
    }

    .TopList {
        padding: 10px
    }

    .productItem:hover .productImage a:after {
        display: none
    }

    .productItem:hover .quickViewIco {
        display: none!important
    }

    .favori {
        right: 0;
        bottom: 33px;
        display: block!important
    }

    .productItem .IndirimVar .discountPrice span {
        color: #646464
    }

    .favori a:before {
        font-size: 15px;
        line-height: 25px;
        background-color: #fff;
        width: 23px;
        height: 23px;
        margin-bottom: 63px;
        margin-right: 8px;
        border-radius: 50%
    }

    .favori a:after {
        display: none
    }

    .discountIcon {
        font-size: 14px;
        width: 29px;
        height: 21px;
        line-height: 23px;
        top: 30px
    }

    .newIcon {
        font-size: 8px;
        width: 29px;
        height: 20px;
        top: 53px
    }

    .firsatIcon {
        font-size: 6px;
        width: 29px;
        top: 75px;
        line-height: 1.3
    }

    .cargoIcon {
        width: 33px;
        height: 33px;
        background-size: 100%;
        top: 15px
    }

    .TukendiIco span {
        font-size: 11px
    }

    .productItem .productName a {
        font-size: 12px
    }

    .productItem .productOnYazi * {
        font-size: 12px!important
    }

    .productItem .productOnYazi {
        height: 15px;
        overflow: hidden
    }

    .ozelAlan2 span {
        font-size: 9px;
        line-height: 11px;
        margin-top: 1.5px
    }

    .ozelAlan2 {
        padding: 0 5px
    }

    .ozelAlan2 {
        margin-bottom: 0;
        text-align: left
    }

    .ozelAlan2 span:nth-child(2) {
        font-size: 13px;
        top: 1px
    }

    #divOzelAlan2 span:nth-child(2) {
        font-size: 23px
    }

    #divOzelAlan2 span {
        font-size: 13px;
        text-decoration: underline;
        color: red
    }

    #pnlFiyatlar {
        margin-top: 4px
    }

    #divKargoBedava {
        float: left;
        margin-left: 15px
    }

    .categoryContainer .ProductListContent .productItem {
        margin: 23px 0 0
    }

    #pnlSlider {
        width: 100%;
        margin: 0
    }

    #pnlSlider .flex-control-nav {
        bottom: 5px
    }

    .sliderBannerContainer ul li {
        width: 46.7%
    }

    .sliderBannerContainer ul li:nth-child(5n) {
        margin-right: 20px
    }

    .categoryContainer {
        padding: 0 5px
    }

    .categorydesign {
        display: none
    }

    .urunListRel {
        margin-top: 1px!important
    }

    .mobilFilterOpenBtn {
        margin-bottom: 0!important;
        background: #f3f3f3a1;
        padding: 12px 0
    }

    .filterBlock .mobilFilterOpenBtn .button {
        width: 50%;
        line-height: 23px;
        margin: 0;
        padding: 0;
        background: 0 0;
        font-size: 13px;
        text-transform: uppercase;
        color: #3e3e3e;
        height: 20px
    }

    .filterBlock .mobilFilterOpenBtn .button.mobilFilterBtn {
        border-right: .5px solid #ccc!important
    }

    .category-vertical-filters.top-filters {
        position: fixed!important;
        right: 0;
        top: 100%;
        z-index: 999999;
        margin: 0!important;
        background: #fff!important;
        bottom: 0;
        display: block!important;
        transition: all .3s ease;
        opacity: 0;
        width: calc(100% - 35px)!important;
        overflow-y: auto;
        overflow-x: hidden
    }

    .category-vertical-filters.top-filters.active {
        top: 0;
        opacity: 1
    }

    .closeb {
        position: absolute;
        bottom: 0;
        left: 0;
        right: 0;
        z-index: 100;
        line-height: 50px;
        background: #000;
        color: #fff;
        text-align: center;
        font-size: 16px
    }

    .closeb i {
        margin-right: 10px
    }

    .category-vertical-filters>div.closeb2 {
        position: absolute;
        left: -35px;
        font-size: 20px;
        width: 35px!important;
        text-align: center;
        line-height: 35px;
        background: #000
    }

    .category-vertical-filters>div.closeb2 i {
        line-height: 35px;
        color: #fff
    }

    .PriceList {
        width: 100%
    }

    #divSatinAl {
        width: 100%;
        padding-top: 25px
    }

    .urunOzellik {
        width: 100%;
        margin-top: 15px
    }

    .ProductIcon #divKritikStok .box1 i {
        margin: 0 10px 0 0!important;
        width: auto
    }

    .ProductIcon div>a:before {
        width: auto!important;
        margin-right: 10px
    }

    #divBenzerUrun {
        margin: 0 0 20px;
        padding: 0 5px
    }

    #divBenzerUrun .categoryTitle .bold .satir1 {
        font-size: 17px
    }

    #divBenzerUrun .categoryTitle .bold:after {
        left: 0;
        right: 0;
        height: 2px
    }

    #divBenzerUrun .owl-carousel {
        padding: 0
    }

    .product-social-icon-wrapper {
        width: auto;
        padding: 0;
        margin: 0;
        float: right;
        position: absolute;
        right: 25px;
        top: 60px
    }

    .product-social-icon-wrapper:before {
        margin-bottom: 0;
        width: 33px;
        height: 27px;
        background-size: 100% 100%;
        float: right;
        display: none
    }

    .product-social-icon-wrapper ul {
        position: relative;
        top: 0;
        float: right;
        width: auto;
        clear: both;
        padding-top: 15px
    }

    .product-social-icon-wrapper ul li {
        width: 35px
    }

    .product-social-icon-wrapper .PaylasTit {
        width: 100%;
        height: 44px;
        float: left;
        margin-bottom: 15px;
        margin-bottom: 0;
        width: 33px;
        height: 27px;
        background-size: 100% 100%;
        float: right;
        font-size: 0;
        display: block
    }

    .product-social-icon-wrapper:hover ul {
        display: none
    }

    .product-social-icon-wrapper.active ul {
        display: block
    }

    #divUrunEkSecenek {
        width: 100%;
        margin-top: 0
    }

    #footer {
        margin-top: 70px
    }

    #footer .ticiContainer {
        padding: 0 5px
    }

    .FooterMiddle {
        padding-bottom: 0;
        background: #fff;
        text-align: center
    }

    .linkler {
        width: 100%;
        padding: 0
    }

    .linkler>ul>li {
        padding-right: 0
    }

    .linkler>ul>li>a {
       
        width: 100%;
        display: inline-block;
        float: none;
        padding-bottom: 0;
        margin-bottom: 0;
        font-size: 13px;
        line-height: 58px;
        background-color: #f2f2f2;
        border-bottom: 1px solid #d6d6d6
    }

    .linkler>ul>li>a:after {
        content: '\f107';
        font-family: fontawesome;
        margin-left: 10px
    }

    .linkler>ul>li>ul {
        display: none;
        padding-top: 10px
    }

    .linkler>ul>li>ul>li>a {
        font-size: 13px
    }

    .Social {
        width: 100%;
        text-align: center;
        float: left;
        margin: 0;
        padding-bottom: 10px;
        border-bottom: 2px solid #b1b1b1
    }

    .Social .Stitle {
        width: 100%;
        text-align: center
    }

    .Social ul {
        width: 100%
    }

    .Social li {
        float: none!important;
        display: inline-block;
        margin-right: 0!important;
        width: 37px!important
    }

    .Social li.Footer-Blog {
        width: 70px!important
    }

    .Social li.Footer-Blog img {
        display: block
    }

    .FTextAlan {
        display: none
    }

    .banksimg {
        display: none
    }

    .bankimg {
        display: none
    }

    .MusteriHizmet {
        display: none
    }

    .Magazalar {
        display: none
    }

    #txtbxNewsletterMail {
        background: #eee;
        border: 1px solid #b3b3b3!important
    }

    .newsbutton {
        background-color: #eee!important;
        right: 1px;
        top: 1px;
        height: 29px
    }

    .copy {
        width: 100%;
        text-align: center;
        margin: 10px 0
    }

    .Ebulten {
        width: 100%
    }

    .Etitle {
        width: 100%;
        text-align: center;
        font-size: 13px
    }

    .Appdiv {
        float: left;
        width: 100%;
        margin: 0;
        padding: 10px 0
    }

    .Fsol .copy {
        margin-bottom: 20px
    }

    .sepetimBody #header {
        height: auto;
        display: block!important;
        padding: 0;
        border: none
    }

    .sepetimBody .BasketPage {
        margin-top: 0!important
    }

    .sepetimBody .Basketstep {
        position: relative
    }

    #back-to-top a {
        width: 25px;
        height: 25px;
        background-size: 100%
    }

    .mobilMenu .Menuicine {
        float: left;
        width: 100%;
        list-style-type: none;
        padding: 20px 0 10px;
        border-top: 1px solid #d6d6d6;
        border-bottom: 1px solid #d6d6d6;
        display: none
    }

    .mobilMenu .Menuicine>a {
        font-size: 15px;
        color: #2d2d2d;
        font-weight: 600;
        margin-bottom: 10px;
        padding-bottom: 15px;
        float: left;
        font-family: futura pt book
    }

    .mobilMenu .Menuicine>ul {
        float: left;
        width: 100%
    }

    .mobilMenu .Menuicine>ul li {
        float: left;
        width: 100%
    }

    .mobilMenu .Menuicine>ul li a {
        float: left;
        color: #2d2d2d;
        font-size: 15px;
        font-weight: 400;
        margin-bottom: 10px;
        font-family: futura pt book
    }

    .mobilMenu .MusteriHizmet {
        display: block;
        padding-left: 30px;
        margin-top: 20px;
        display: none
    }

    .mobilMenu .MusteriHizmet .Mtext a {
        font-size: 11px
    }

    .mobilMenu .MusteriHizmet .Mtext a p {
        font-size: 23px
    }

    .mobilMenu .MusteriHizmet .Mimg {
        width: 32px
    }

    .mobilMenu .MusteriHizmet .Mimg img {
        max-width: 100%
    }

    .mobilMenu .Magazalar {
        float: left;
        width: 100%;
        border: 1px solid #91074b;
        border-radius: 2px;
        text-align: center;
        display: block;
        margin: 20px 0
    }

    .mobilMenu .Magazalar>a {
        float: left;
        width: 100%;
        line-height: 51px;
        font-size: 15px;
        color: #000;
        font-family: futura pt demi;
        font-weight: 600
    }

    .mobilMenu .Magazalar>a:after {
        content: '\e833';
        font-family: lineariconsfree;
        color: #000;
        font-size: 33px;
        line-height: 51px;
        float: right
    }

    #pnlSlider.margin {
        margin-top: 0
    }

    #divIcerik.margin {
        margin-top: 75px
    }

    .AltBanner.margin {
        margin-top: 75px
    }

    .proCategoryTitle.categoryTitleText.margin {
        margin-top: 90px
    }

    #header.fixed {
        position: fixed;
        top: 0;
        z-index: 998;
        border-bottom: 1px solid #2d2d2d;
        height: 80px
    }

    #header.fixed .searchContent {
        display: none
    }

    .CategoryBody #header.fixed,.MagazaSayfa #header.fixed {
        height: 51px;
        border-bottom: none
    }

    .ProductBody #header.fixed {
        height: 51px;
        border-bottom: none
    }

    .ProductBody #header .headerContent:after,.CategoryBody #header .headerContent:after,.MagazaSayfa #header .headerContent:after {
        display: none
    }

    #header.fixed #logo .logo {
        display: none
    }

    #header.fixed #logo .Mlogo {
        display: block
    }

    #header.fixed #logo .fixedLogo {
        display: none
    }

    body.margin {
        margin-top: 125px
    }

    .sepetimBody .AltBanner {
        display: none
    }

    .alisverisedevamet {
        font-size: 11px!important;
        color: #71034e!important
    }

    .alisverisedevamet:before {
        margin-right: 5px!important
    }

    .alisverisedevamet i.fa.fa-chevron-left {
        font-size: 0
    }

    .alisverisedevamet:hover {
        background: 0 0!important;
        border-color: transparent!important
    }

    #divUrunEkSecenek .eksecenekLine .left_line {
        margin: 5px 0 10px
    }

    #divUrunEkSecenek .eksecenekLine .right_line .size_box {
        margin-bottom: 5px
    }

    .detayText {
        padding: 20px 0 0
    }

    .bedenTablosu {
        bottom: 73px;
        margin-left: -14px
    }

    .Basketstep ul li.onestepsec span {
        font-size: 0
    }

    .iletisimContent {
        padding: 10px 15px 0
    }

    .pageContainer {
        padding: 10px 15px 0
    }

    .iletisimLeft {
        width: 100%!important
    }

    .iletisimForm {
        width: 100%!important;
        margin-top: 0!important
    }

    #itetisimhtml {
        width: 100%;
        padding-left: 0
    }

    .iletisimLeftTelefon .Left {
        font-size: 12px
    }

    .iletisimLeftAdres .Left {
        font-size: 12px
    }

    .iletisimContent .iletisimLeft .categoryTitle .categoryTitleText {
        font-size: 12px;
        line-height: 25px
    }

    .iletisimContent .iletisimLeft .categoryTitle {
        margin-bottom: 0
    }

    .iletisimLeftTelefon .Right {
        font-size: 11px!important
    }

    .calismasaati {
        margin-bottom: 5px
    }

    .iletisimForm .categoryTitle .categoryTitleText {
        margin: 0!important;
        width: 100%!important;
        font-size: 12px!important
    }

    .OzelSayfaContent {
        margin-top: 10px
    }

    .OzelSayfaContent .OzelSayfaSol {
        width: 100%;
        padding-right: 0
    }

    .OzelSayfaContent .OzelSayfaSag {
        width: 100%;
        padding-left: 0;
        border: none;
        max-height: 230px;
        padding-right: 0
    }

    .OzelSayfaContent .OzelSayfaSag img {
        max-width: 100%
    }

    .OzelSayfaContent .OzelSayfaSol>ul>li>a {
        font-size: 12px
    }

    .OzelSayfaContent .OzelSayfaSol>ul>li>ul li a {
        line-height: 25px;
        font-size: 11px
    }

    .OzelSayfaContent .OzelSayfaSol .canlidestek {
        margin-top: 0;
        margin-bottom: 25px
    }

    .OzelSayfaContent .OzelSayfaSol .canlidestek a {
        position: relative;
        float: left;
        font-size: 7px;
        color: #000;
        width: 90px;
        padding-top: 11px;
        padding-right: 11px;
        text-align: right;
        font-weight: 600
    }

    .OzelSayfaContent .OzelSayfaSol ul li {
        border-bottom: 1px solid #eee
    }

    .OzelSayfaContent .OzelSayfaSol>ul>li {
        position: relative
    }

    .OzelSayfaContent .OzelSayfaSol>ul>li .OzelAc {
        position: absolute;
        right: 0;
        top: 0;
        font-size: 20px;
        text-align: center;
        width: 35px
    }

    .OzelSayfaContent .OzelSayfaSol>ul>li ul {
        display: none
    }

    #searchStore .buton {
        line-height: 45px!important;
        width: 85px!important;
        float: right;
        height: 45px
    }

    #searchStore .buton:before {
        line-height: 45px!important;
        margin-left: 0!important
    }

    #searchStore input {
        width: calc(100% - 95px)!important
    }

    #storeCitys {
        margin-top: 10px!important;
        margin-top: 10px!important
    }

    #searchStore {
        padding-left: 0!important;
        padding-right: 0!important;
        margin-top: 0!important
    }

    .magazalarContent {
        padding: 0 5px
    }

    .mycart .sepetUrunSayisi {
        right: -8px;
        top: -7px;
        background: #fff000;
        color: #000;
        line-height: 17px
    }

    .SosyalMedyaBanner {
        padding: 0 5px
    }

    .SosyalMedyaBanner .sosiContainer .banTek .banIki {
        width: 48%
    }

    .firsatIcon:before {
        font-size: 8px!important
    }

    .sortingContent:before {
        display: none!important
    }

    .bkmExpressBtn {
        width: 60%!important
    }
}

.Gif-Blok {
    float: left;
    width: 100%;
    position: relative
}

.Butonlar {
    width: 100%;
    position: absolute;
    bottom: 80px;
    text-align: center
}

.Butonlar a {
    display: inline-block;
    color: #000;
    font-size: 17px;
    margin: 0 55px;
    font-weight: 700;
    width: 205px;
    height: 54px;
    line-height: 54px;
    letter-spacing: 3px
}

@media screen and (min-width: 768px) and (max-width:1023px) {
    .Butonlar a {
        width:150px;
        margin: 0 10px
    }

    .Butonlar {
        bottom: 30px
    }
}

@media screen and (min-width: 1024px) and (max-width:1271px) {
    .Butonlar a {
        width:180px;
        margin: 0 25px
    }
}

@media screen and (max-width: 767px) {
    .OdemeMenu .css-11cvqu4-Global {
        min-width:300px!important
    }

    .OdemeMenu .css-plhoba-Screens {
        padding: 10px!important
    }

    .iyz-wrapper .css-134attv-Overlay {
        right: 0!important;
        left: auto!important
    }

    .css-11cvqu4-Global a {
        background: 0 0!important
    }

    .BasketPage .OdemeMenu ul li:hover .css-11cvqu4-Global a {
        background-color: transparent!important
    }

    .BasketPage .OdemeMenu ul li.activeMenu .sozlesmeUyari a {
        background-color: transparent!important
    }

    .Butonlar {
        bottom: 30px
    }

    .Butonlar a {
        display: inline-block;
        padding: 8px 20px;
        font-size: 14px;
        margin: 0 10px;
        font-weight: 700;
        width: auto;
        height: auto;
        line-height: normal;
        letter-spacing: 0
    }
}

@media screen and (min-width: 375px) and (max-width:510px) {
    .Butonlar {
        bottom:10px
    }

    .Butonlar a {
        display: inline-block;
        padding: 8px;
        font-size: 12px;
        margin: 0 3px;
        font-weight: 700;
        width: auto;
        height: auto;
        line-height: normal;
        letter-spacing: 0
    }
}

@media screen and (max-width: 374px) {
    .Butonlar {
        bottom:10px
    }

    .Butonlar a {
        display: inline-block;
        padding: 6px 5px;
        font-size: 11px;
        margin: 0 3px;
        font-weight: 700;
        width: auto;
        height: auto;
        line-height: normal;
        letter-spacing: 0
    }
}

@media screen and (max-width: 560px) {
    .sepetimBody #cbMesafeliSatisSozlesme {
        margin-top:10px
    }
}

</style>