/# VC
RGB(R,G,B)
RED (255.0.0)
green(0.255.0)
yello(255.255.0)
white(255.255.255)
black(0.0.0)


WM_PAINT   刷新消息
绘图工具 
    画笔 PEN
    功能： 画线 线性、color、
 系统画笔 BLACK
 
 
 SeletStockObject()
 
 
 用户自定义画笔
   HPEN CPen(MFC)
   CPen Pen;
画刷 HBURSH CRrush(MFC)

系统预定义画刷：
BLACK_BRUSH,WHITE_BRUSH,.......
用户自定义画刷：
  CreatSolidBrush(..)  ///单色画刷
  CreatHatchBrush（..） ///非单色  按照某种图案

   **CG diobject:
      cpen      画笔
      cbrush    画刷 
      cfont     字体
 


   
   
   
LRESULT CDemoWnd::OnPaint(
WPARAM wParam,LPARAM lParam)
  {
    CPaintDC dc(this);
   
    Cpen Renpen;
    CPen *pOldPen=NULL;
    RedPen CreatePen(PS_SOLID,10,RGB(255,0,0));   //创建画笔 
    pOldPen  =  dc.SelectObject(&RedPen);
    
    CBrush Brush;
    CBrush *pOldBrush = NULL;
    Brush.CreateSoldBrush(RGB(255,255,0))
    POldBrush = dc.SelectObject(&Brush);
    

    
    

    dc.SetMapMode(MM_LOMETRI);   /////  (MM_HIMETRIC);
    dc.Rectangle(100,-100,400,-500);
    dc.ELLIPSE(100.-100.400.-500);
    dc.SelectObject(pOldPen);   //恢复旧画笔
    return(0);
  }
  

2018.10.8
 
 **系统字体
 
 **文字信息显示
   BOOL TextOut(int x.int y,LPCTSTR IpszString);  x,y   为坐标   后面参数是字符串
   
   
   CCLIENTDC DC(THIS)
   dc.textout(20,20,"hello world")
 
     
