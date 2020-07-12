# J2Team Offline Luckywheel

I write this luckywheel for j2team offline event

### Prizes Config

```js
Line 34;
var prizes = [
  {
    text: "Hoodie J2Team", // Require
    img: "images/Ao.png", // Optional
    number: 1,
    percentage: 1 // (100%) | 0.5 // 50% | 0.01 // 1%
  }
];
```

### Mode Config

```js
Line 80;
mode : both // For display both image and text
mode : null // For display text if only text and image if having it will having no text
```

### Return message

Using sweetalert 2 library

```js
  Line 86
  if(data == null){
    // This for when no more prize
    Swal.fire(
      'Chương trình kết thúc',
      'Đã hết phần thưởng',
      'error'
    )
  }else{
    // This for when spin is done
    Swal.fire(
      'Đã trúng giải',
      data,
      'success'
    )
  }
```