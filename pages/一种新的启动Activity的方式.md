- "在被启动的Activity中添加静态方法
  
  ```纯文本
  public static void onOpen(Context context) {
      Intent intent = new Intent(context, StoreVerifyGuideActivity.class);
      context.startActivity(intent);
  }
  ```"