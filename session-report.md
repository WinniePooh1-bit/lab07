# Session report

Тестер: М.Наранбат

Огноо: 2026-10-25, 22:02 - 23:02 (60 мин)

Mission: Уншлагын жагсаалт аппын чанарыг шинжлэх

Charter: Ном нэмэх, хайх, устгах хэсэг болон «Нийт ном» тоолуурыг Couch Potato, Saboteur, Fed-Ex аялалуудаар шалгана. Хоосон, буруу, давхардсан оролт болон API-д буруу JSON илгээж, оролтын шалгалт, тоолуурын зөрүү, статус кодын согог хайна.

## Тэмдэглэл (он цагийн дарааллаар)

22:02  [S] Timer started. node app.js, opened browser

22:08  [T] the total amount of book says 4 but there is only 3 books shown

22:11  [T] the delete button is not red but green

22:14  [T] after adding book with only name and author it still got added without the year when it was supposed to show error message and book with same author still got added

22:29  [T] the layout broke after deleted the original books

22:30  [T] after clicking old version link it says "Internal Server Error" and doesnt work

23:02  [B] test ends

## Нэмэлт: curl-ийн цагууд

Эдгээр curl туршилтыг session-ий үеэр хийсэн боловч тэмдэглэлд цагийг нь бичээгүй. Доорх цагийг curl-ийн гаралтын Date толгойгоос (UTC) +8 цаг нэмж сэргээв.

22:22  Saboteur: буруу JSON-тэй POST /api/books -> HTTP/1.1 200 OK (400 байх ёстой)

22:25  GET /api/books -> 200 OK, 3 ном

22:26  GET /api/stats -> 200 OK

22:27  DELETE /api/books/9999 -> 200 OK

22:27  GET /nothing-here -> 404 Not Found

## Саадууд (issues)

Тэмдэглэлээ цаг тутамд тогтмол хөтлөөгүй, curl-ийн цагийг дараа нь сэргээсэн.

## Цагийн задаргаа

Setup 10% · Тест дизайн ба гүйцэтгэл 75% · Согог судлах 15%