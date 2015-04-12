using System;
 
usingSystem.Collections.Generic;
 
usingSystem.ComponentModel;
 
usingSystem.Data;
 
usingSystem.Drawing;
 
usingSystem.Linq;
 
usingSystem.Text;
 
usingSystem.Threading.Tasks;
 
usingSystem.Windows.Forms;
 
 
 
namespaceDragLabel
 
{
 
publicpartialclassForm1 : Form
 
    {
 
public Form1()
 
        {
 
InitializeComponent();
 
        }
 
 
 
privatePointmouseOffset;
 
 
 
 
 
privatevoid label1_MouseUp(object sender, MouseEventArgs e)
 
        {
 
if (e.Button == MouseButtons.Left)
 
            {
 
PointmousePos = Control.MousePosition;
 
mousePos.Offset(mouseOffset.X, mouseOffset.Y);
 
                ((Control)sender).Location = ((Control)sender).Parent.PointToClient(mousePos);
 
            }
 
        }
 
 
 
privatevoid label1_MouseDown(object sender, MouseEventArgs e)
 
        {
 
mouseOffset = newPoint(-e.X, -e.Y);
 
        }
 
    }
 
}
 
 
 
namespaceDragLabel
 
{
 
partialclassForm1
 
    {
 
///<summary>
 
///必需的设计器变量。
 
///</summary>
 
privateSystem.ComponentModel.IContainer components = null;
 
 
 
///<summary>
 
///清理所有正在使用的资源。
 
///</summary>
 
///<param name="disposing">如果应释放托管资源，为 true；否则为 false。</param>
 
protectedoverridevoid Dispose(bool disposing)
 
        {
 
if (disposing && (components != null))
 
            {
 
components.Dispose();
 
            }
 
base.Dispose(disposing);
 
        }
 
 
 
        #region Windows 窗体设计器生成的代码
 
 
 
///<summary>
 
///设计器支持所需的方法 - 不要
 
///使用代码编辑器修改此方法的内容。
 
///</summary>
 
privatevoidInitializeComponent()
 
        {
 
this.label1 = newSystem.Windows.Forms.Label();
 
this.SuspendLayout();
 
//
 
// label1
 
//
 
this.label1.AutoSize = true;
 
this.label1.Location = newSystem.Drawing.Point(12, 26);
 
this.label1.Name = "label1";
 
this.label1.Size = newSystem.Drawing.Size(77, 12);
 
this.label1.TabIndex = 0;
 
this.label1.Text = "Hello World!";
 
this.label1.MouseDown += newSystem.Windows.Forms.MouseEventHandler(label1_MouseDown);
 
this.label1.MouseUp += newSystem.Windows.Forms.MouseEventHandler(label1_MouseUp);
 
 
 
//
 
// Form1
 
//
 
this.AutoScaleDimensions = newSystem.Drawing.SizeF(6F, 12F);
 
this.AutoScaleMode = System.Windows.Forms.AutoScaleMode.Font;
 
this.ClientSize = newSystem.Drawing.Size(284, 261);
 
this.Controls.Add(this.label1);
 
this.Name = "Form1";
 
this.Text = "Form1";
 
this.ResumeLayout(false);
 
this.PerformLayout();
 
 
 
        }
 
 
 
        #endregion
 
 
 
privateSystem.Windows.Forms.Label label1;
 
 
 
    }
 
}
