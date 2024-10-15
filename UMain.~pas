unit UMain;

interface

uses
  Windows, Messages, SysUtils, Variants, Classes, Graphics, Controls, Forms,
  Dialogs, StdCtrls, ExtCtrls, JvExControls, JvComponent,
  JvGradientHeaderPanel, XPMan, JvLabel, JvXPCore, JvXPButtons, JvAnimTitle,
  Mask;

type
  TForm1 = class(TForm)
    Timer1: TTimer;
    Panel1: TPanel;
    Image1: TImage;
    Panel2: TPanel;
    PaintBox1: TPaintBox;
    JvGradientHeaderPanel2: TJvGradientHeaderPanel;
    XPManifest1: TXPManifest;
    JvLabel1: TJvLabel;
    JvLabel2: TJvLabel;
    Timer2: TTimer;
    JvLabel3: TJvLabel;
    JvLabel4: TJvLabel;
    JvXPButton1: TJvXPButton;
    JvXPButton2: TJvXPButton;
    JvXPButton3: TJvXPButton;
    JvXPButton4: TJvXPButton;
    Bevel1: TBevel;
    Bevel2: TBevel;
    JvLabel5: TJvLabel;
    JvLabel6: TJvLabel;
    JvLabel7: TJvLabel;
    JvLabel8: TJvLabel;
    JvXPButton5: TJvXPButton;
    JvXPButton6: TJvXPButton;
    JvXPButton7: TJvXPButton;
    OpenDialog1: TOpenDialog;
    OpenDialog2: TOpenDialog;
    SaveDialog1: TSaveDialog;
    SaveDialog2: TSaveDialog;
    JvAnimTitle1: TJvAnimTitle;
    me: TMaskEdit;
    JvLabel9: TJvLabel;
    procedure JvXPButton6Click(Sender: TObject);
    procedure FormShow(Sender: TObject);
    procedure Image1MouseDown(Sender: TObject; Button: TMouseButton;
      Shift: TShiftState; X, Y: Integer);
    procedure Image1MouseMove(Sender: TObject; Shift: TShiftState; X,
      Y: Integer);
    procedure JvXPButton7Click(Sender: TObject);
    procedure JvXPButton5Click(Sender: TObject);
    procedure JvXPButton1Click(Sender: TObject);
  private
    { Private declarations }
  public
    { Public declarations }
  end;

var
  Form1: TForm1;

implementation

{$R *.dfm}

procedure TForm1.JvXPButton6Click(Sender: TObject);
var rect:TRect;
begin
{JvLabel1.Caption:='00:00:00';
JvLabel2.Caption:='00:00:00';  }

rect := Bounds(0,0,Image1.Width,Image1.Height);
Image1.Canvas.Brush.Color := clWhite;
Image1.Canvas.FillRect(rect);
end;

procedure TForm1.FormShow(Sender: TObject);
begin
JvLabel1.Caption:='00:00:00';
JvLabel2.Caption:='00:00:00';
end;

procedure TForm1.Image1MouseDown(Sender: TObject; Button: TMouseButton;
  Shift: TShiftState; X, Y: Integer);
begin
if shift = [ssright] then begin
  image1.Canvas.TextOut(x,y,Inttostr(x)+':'+Inttostr(y));
end;

end;
procedure TForm1.Image1MouseMove(Sender: TObject; Shift: TShiftState; X,
  Y: Integer);
begin
if shift = [ssleft] then image1.Canvas.LineTo(x,y);
end;

procedure TForm1.JvXPButton7Click(Sender: TObject);
begin
Application.Terminate;
end;

procedure TForm1.JvXPButton5Click(Sender: TObject);
var t1,t2:integer;
    i : integer;
begin
image1.Canvas.Pen.Width:=2;
t1.GetTickCount;
for 1 := 1 to strtoint(me.Text) do image1.Canvas.LineTo(random(300),random(300));
t2.GetTickCount;
jVLabel1.Caption:=inttostr(t2-t1)+' ms';

PaintBox1.Canvas.Pen.Width:=2;
t1.GetTickCount;
for 1 := 1 to strtoint(me.Text) do PaintBox1.Canvas.LineTo(random(300),random(300));
t2.GetTickCount;
jVLabel2.Caption:=inttostr(t2-t1)+' ms';
end;

procedure TForm1.JvXPButton1Click(Sender: TObject);
begin
if SaveDialog1.Execute then
  begin
      Image1.Picture.SaveToFile(SaveDialog1.FileName);
  end;
end;

end.
