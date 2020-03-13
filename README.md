var options_object = {
// ====== Basic
text: "https://github.com/ushelp/EasyQRCodeJS",
width: 256,
height: 256,
colorDark : "#000000",
colorLight : "#ffffff",
correctLevel : QRCode.CorrectLevel.H, // L, M, Q, H
dotScale: 1 // Must be greater than 0, less than or equal to 1. default is 1
// ====== Quiet Zone
/_
quietZone: 0,
quietZoneColor: 'transparent',
_/

// ====== Logo
/_
logo:"../demo/logo.png", // Relative address, relative to `easy.qrcode.min.js`
logo:"http://127.0.0.1:8020/easy-qrcodejs/demo/logo.png",
logoWidth:80, // widht. default is automatic width
logoHeight:80 // height. default is automatic height
logoBackgroundColor:'#fffff', // Logo backgroud color, Invalid when `logBgTransparent` is true; default is '#ffffff'
logoBackgroundTransparent:false, // Whether use transparent image, default is false
_/
// ====== Backgroud Image
/_
backgroundImage: '', // Background Image
backgroundImageAlpha: 1, // Background image transparency, value between 0 and 1. default is 1.
autoColor: false,
_/
// ====== Colorful
// === Posotion Pattern(Eye) Color
/_
PO: '#e1622f', // Global Posotion Outer color. if not set, the defaut is `colorDark`
PI: '#aa5b71', // Global Posotion Inner color. if not set, the defaut is `colorDark`
PO_TL:'', // Posotion Outer color - Top Left
PI_TL:'', // Posotion Inner color - Top Left
PO_TR:'', // Posotion Outer color - Top Right
PI_TR:'', // Posotion Inner color - Top Right
PO_BL:'', // Posotion Outer color - Bottom Left
PI_BL:'', // Posotion Inner color - Bottom Left
_/
// === Alignment Color
/_
AO: '', // Alignment Outer. if not set, the defaut is `colorDark`
AI: '', // Alignment Inner. if not set, the defaut is `colorDark`
_/
// === Timing Pattern Color
/_
timing: '#e1622f', // Global Timing color. if not set, the defaut is `colorDark`
timing_H: '', // Horizontal timing color
timing_V: '', // Vertical timing color
_/
// ====== Title
/_
title: 'QR Title', // content
titleFont: "bold 18px Arial", //font. default is "bold 16px Arial"
titleColor: "#004284", // color. default is "#000"
titleBackgroundColor: "#fff", // background color. default is "#fff"
titleHeight: 70, // height, including subTitle. default is 0
titleTop: 25, // draws y coordinates. default is 30
_/
  
 // ====== SubTitle
/_
subTitle: 'QR subTitle', // content
subTitleFont: "14px Arial", // font. default is "14px Arial"
subTitleColor: "#004284", // color. default is "4F4F4F"
subTitleTop: 40, // draws y coordinates. default is 0
_/
  
 // ===== Event Handler
/_
onRenderingStart: undefined,
_/
  
 // ===== Versions
/_
version: 0 // The symbol versions of QR Code range from Version 1 to Version 40. default 0 means automatically choose the closest version based on the text length.
_/  
 }
