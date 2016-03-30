# Запрос книги #
Данный запрос рассылается по случайному количеству IP адресов клиентов. Если там не находится такой книги, они рассылаются далее с тех клиентов, куда был направлен запрос.

<libp2p.request>


&lt;to&gt;

This\_UserInnerName

&lt;/to&gt;




<to\_ip>

127.0.0.1

</to\_ip>




<book\_hash>

md5

</book\_hash>


</libp2p.request>


# Выдача книги #
Данная серия ответов пересылается случайному клиенту сети. При пересылке проверяется целостность каждого фрагмента и временный хеш файла также. В зависимости от параметра secure\_level пересылка повторяется необходимое количество раз. Потом файл отправляется на to\_ip.

<libp2p.request>


<temp\_hash>

temporary\_md5\_book\_hash

</temp\_hash>




<to\_ip>

127.0.0.1

</to\_ip>




<part\_hash>

md5

</part\_hash>




&lt;part&gt;

encoded\_64b\_part\_of\_file

&lt;/part&gt;




<part\_n>

integer

</part\_n>




<secure\_level>

1

</secure\_level>


</libp2p.request>

# Обновление базы данных #
Рассылается по нескольким случайным адресам. С них - дальше
<libp2p.request>


&lt;add&gt;

book\_name

&lt;/add&gt;




&lt;hash&gt;

book\_hash

&lt;/hash&gt;




&lt;author&gt;

author\_name

&lt;/author&gt;




&lt;author&gt;

author\_name

&lt;/author&gt;




&lt;author&gt;

author\_name

&lt;/author&gt;




&lt;description&gt;

book\_description

&lt;/description&gt;


</libp2p.request>