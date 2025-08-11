# .NET-Practical

2. Write ASP.NET program that will display “Hello World” on page load event.
- Code :-
-        protected void Page_Load(object sender, EventArgs e)
            {
                Response.write(“Hello World ! “);
            }
3. Write ASP.NET program that will display “Hello World” in Label control on form load event.
- Design:-
-         <body>
            <form id="form1" runat="server">
            <div>
            <asp:label ID="Label1" runat="server" text="Label"></asp:label>    
            </div>
            </form>
         </body>
- Code : 
-      protected void Page_Load(object sender, EventArgs e)
            {
                Label1.Text = "Hello World !";
            }
4. Write ASP.NET program that will display “Hello World” in <div> tag  or <p> tag on click of button.
- Design:-
-         <form id="form1" runat="server">
          <div>
              <asp:Button ID="Button1" runat="server" Text="Button" onclick="Button1_Click" />
          
              <p id="Par" runat="server">
              </p>
          </div>
          </form>
- Code:
-      protected void Button1_Click(object sender, EventArgs e)
        {
            Par.InnerText = "<b><u>Hello World !!!</u></b>";
        }
5. Write ASP.NET program that will do following operations:
- Take two string values from textbox control, contcate it & display it.
- Design:
-       <body>
        <form id="form1" runat="server">
        <div>
            <asp:TextBox ID="TextBox1" runat="server"></asp:TextBox>        
            <asp:textbox ID="Textbox2" runat="server"></asp:textbox>
            <asp:Button ID="Button1" runat="server" Text="Join" OnClick = "Button1_Click" />
            <asp:Label ID="Label1" runat="server" Text=" "></asp:Label>
            </div>
        </form>
      </body>
- Code:
-      protected void Button1_Click(object sender, EventArgs e)
        {
            Label1.Text = TextBox1.Text + Textbox2.Text;
        }
# Take two int values and calculate addition.
- Design:
-       <body>
        <form id="form1" runat="server">
        <div>
            <asp:TextBox ID="TextBox1" runat="server"></asp:TextBox> &nbsp;+
            <asp:TextBox ID="TextBox2" runat="server"></asp:TextBox>
            <asp:Button ID="Button1" runat="server" Text="Add" onclick="Button1_Click" />
            <asp:Label ID="Label1" runat="server" Text=""></asp:Label>
        </div>
        </form>
    </body>
- Code:
-      protected void Button1_Click(object sender, EventArgs e)
        {
            int a, b, c;
            a = Convert.ToInt32(TextBox1.Text);
            b = Convert.ToInt32(TextBox2.Text);
            c = a + b;
            Label1.Text = Convert.ToString(c);
        }
6. Write ASP.NET program that will take two int values &calculate a^b.
  - Design:
  -        <form id="form1" runat="server">
              <div>
                    <asp:TextBox ID="TextBox1" runat="server"></asp:TextBox>
                    <asp:TextBox ID="TextBox2" runat="server"></asp:TextBox>
                    <asp:Button ID="Button1" runat="server" Text="Result" onclick="Button1_Click" />
                    
                    <asp:Label ID="Label1" runat="server" Text=""></asp:Label>
              </div>
             </form>
  - Code:
  -      protected void Button1_Click(object sender, EventArgs e)
                {
                    double a, b, c;
                    a = Convert.ToInt32(TextBox1.Text);
                    b = Convert.ToInt32(TextBox2.Text);
                    c = Math.Pow(a, b);            
                    Label1.Text = TextBox1.Text + "^"+TextBox2.Text+" = "+ Convert.ToString(c);            
                }
7. Write ASP.NET program that will take 3 subject marks & find Total & Average.
- Design:
-         <div>
                <asp:Label ID="Label1" runat="server" Text="Subject 1"></asp:Label>
                <asp:TextBox ID="TextBox1" runat="server"></asp:TextBox><br />
                
                <asp:Label ID="Label2" runat="server" Text="Subject 2"></asp:Label>
                <asp:TextBox ID="TextBox2" runat="server"></asp:TextBox><br />
                
                <asp:Label ID="Label3" runat="server" Text="Subject 3"></asp:Label>
                <asp:TextBox ID="TextBox3" runat="server"></asp:TextBox><br />        
                
                <asp:Button ID="Button1" runat="server" Text="Sum & Avg" onclick="Button1_Click" /><br />
                
                <asp:Label ID="Label4" runat="server" Text="Label"></asp:Label>
                &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
                <asp:Label ID="Label5" runat="server" Text="Label"></asp:Label>
          </div>  
- Code:
-      protected void Button1_Click(object sender, EventArgs e)
        {
        int sum = int.Parse(TextBox1.Text) + int.Parse(TextBox2.Text) + int.Parse(TextBox3.Text);
        float avg = sum/3;
        Label4.Text = "sum = " + sum.ToString();
        Label5.Text = "Avg = " + avg.ToString();
        }
   
8. Create ASP.NET Webpage that will take feedback details from user and Display it as testimonial. Feedback     :  Name, email and feedback desc.
- Design:
-        <form id="form1" runat="server">
                <div>
                <center>
                    <asp:Label ID="Label1" runat="server" Text="Name"></asp:Label>
                    <asp:TextBox ID="TextBox1" runat="server"></asp:TextBox>
                    <br /><br />
                     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
                     <asp:Label ID="Label3" runat="server" Text="Feedback"></asp:Label>
                    &nbsp;
                    <asp:TextBox ID="TextBox3" runat="server" TextMode="MultiLine"></asp:TextBox>
                    <br /><br />
                    <asp:Button ID="Button1" runat="server" Text="Submit" onclick="Button1_Click" />
                    <br /><br />
                    <div id="tes" style="width:30%;background-color:lightGray;color:white;font-weight:bold" runat="server">        
                    </div>        
                </center>
                </div>
            </form>
- Code:
-      protected void Button1_Click(object sender, EventArgs e)
                {
                    string fed = "'" + TextBox3.Text +"'";
                    fed += "<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; -" + TextBox1.Text;
                    tes.InnerHtml = fed;
                }
9. Create ASP.NET Webpage that will upload any file to webserver.
- Design:
-       <form id="form1" runat="server"><div>
           <asp:Label ID="Label1" runat="server" Text="Label"></asp:Label>
           <br />
           <asp:fileupload ID="Fileupload1" runat="server"></asp:fileupload>
           <br />
           <asp:Button ID="Button1" runat="server" Text="Button" onclick="Button1_Click"PostBackUrl="~/Default.aspx" />
           <p id="par" runat="server" ></p>
           </div>
        </form>
- Code:
-      protected void Page_Load(object sender, EventArgs e)
         {        
         }
         protected void Button1_Click(object sender, EventArgs e)
         {
         if (Fileupload1.HasFile)
         {
         try
         {
         string filename = Path.GetFileName(Fileupload1.FileName);
         Fileupload1.SaveAs(Server.MapPath("~/") + filename );
         Label1.Text = "Upload status: File uploaded!";
         }
          catch (Exception ex)
         {
         Label1.Text = "Upload status: The file could not be uploaded. The following error occured: " + ex.Message;
         }
         }
10. Create ASP.NET webpage that will display Sleeve Items in a listbox control. On the selection of      display image and cost of item.
11. In above ASP.NET Webpage allow user to add quantity in textbox control (i.e Read only) on click      of + & - button controls quantity should be increment & decrement then calculate payment.
- Design:
-         <html xmlns="http://www.w3.org/1999/xhtml">
            <head runat="server">
              <title>Untitled Page</title>
            <style type="text/css">
            #msg
           {
             width: 533px;
            }
         </style>
         </head>
          <body >
           <form id="form1" runat="server">
            <div>
          <center>
          <h3>Select one of the items below</h3>         
           <asp:ListBox ID="ListBox1" runat="server" AutoPostBack="True" Height="180px" 
                    onselectedindexchanged="ListBox1_SelectedIndexChanged" Width="333px">
            <asp:ListItem>Avon Body Lotion</asp:ListItem>
            <asp:ListItem>Drinking Water</asp:ListItem>
            <asp:ListItem>Dermi Cool Talc</asp:ListItem>
            <asp:ListItem>Moov Rapid Relief</asp:ListItem>
            <asp:ListItem>Relispray Pain Relief</asp:ListItem>    
            <asp:ListItem>aaaaa</asp:ListItem> 
            </asp:ListBox>
                &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
                <asp:Image ID="Image1" runat="server" Height="180px"  />
                <br />
                <br />
                <p id="msg" runat="server"></p> <asp:Label ID="Label1" runat="server" Text="Label"></asp:Label>
                <br /><br />
                Enter Quantity &nbsp;&nbsp;&nbsp; 
             <asp:TextBox ID="TextBox1" runat="server" Width="52px" Height="22px" 
                ReadOnly="True">0</asp:TextBox>
                &nbsp;&nbsp;&nbsp;<asp:Button ID="Button2" runat="server" Text="+" 
                     onclick="Button2_Click" />
             <asp:Button ID="Button3" runat="server" Text="-" onclick="Button3_Click" 
                    style="width: 18px" />
               &nbsp;<asp:Button
              ID="Button1" runat="server" Text="Buy" onclick="Button1_Click" />
                <br /><br />
              <p id="paymsg" runat="server"></p> 
            </center>
           </div>
         </form>
       </body>
      </html>
- Code:
-        int cost = 0;
            protected void Page_Load(object sender, EventArgs e)
            {
       
             }
             protected void ListBox1_SelectedIndexChanged(object sender, EventArgs e)
           {
            int i = ListBox1.SelectedIndex;
            //Response.Write(i);
          int cost;
          switch (i)
          {
            case 0: 
                Image1.ImageUrl = "~/Sleev1.jpg";
                cost = 50;
                break;
            case 1:
                Image1.ImageUrl = "~/Sleev2.jpg";
                cost = 30;
                break;
            case 2: Image1.ImageUrl = "~/Sleev3.jpg";
                cost = 60;
                break;
            case 3: Image1.ImageUrl = "~/Sleev4.jpg";
             cost = 70;
                break;
            case 4: Image1.ImageUrl = "~/Sleev5.jpg";
                cost = 45;
                break;
            }
            msg.InnerHtml = "You have chosen " + ListBox1.SelectedValue + " and its cost is " + cost;
           Label1.Text = cost.ToString();
            }
         protected void Button1_Click(object sender, EventArgs e)
       {
        cost = int.Parse(Label1.Text) * int.Parse(TextBox1.Text);
        Label2.Text = "You have to pay " + cost;
      }
         protected void Button2_Click(object sender, EventArgs e)
       {
        int i = int.Parse(TextBox1.Text);
        ++i;
        TextBox1.Text = i.ToString();
      }
        protected void Button3_Click(object sender, EventArgs e)
      {
        int i = int.Parse(TextBox1.Text);
        --i;
        TextBox1.Text = i.ToString();
      }
 
