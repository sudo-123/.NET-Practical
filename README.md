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
- Take two int values and calculate addition.
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
