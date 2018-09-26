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
   
   
   
LRESULT CDemoWnd::OnPaint(
WPARAM wParam,LPARAM lParam)
  {
    CPaintDC dc(this);
   
    Cpen Renpen;
    CPen *pOldPen=NULL;
    RedPen CreatePen(PS_SOLID,10,RGB(255,0,0));   //创建画笔 
    pOldPen  =  dc.SelectObject(&RedPen);

    dc.SetMapMode(MM_LOMETRI);   /////  (MM_HIMETRIC);
    dc.Rectangle(100,-100,400,-500);
    dc.ELLIPSE(100.-100.400.-500);
    dc.SelectObject(pOldPen);   //恢复旧画笔
    return(0);
  }
  
