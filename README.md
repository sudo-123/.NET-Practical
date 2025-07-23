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
  
