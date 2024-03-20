# EX01 Developing a Simple Webserver
## Date: 23-03-24

## AIM:
To develop a simple webserver to serve html pages.

## DESIGN STEPS:
### Step 1: 
HTML content creation.

### Step 2:
Design of webserver workflow.

### Step 3:
Implementation using Python code.

### Step 4:
Serving the HTML pages.

### Step 5:
Testing the webserver.

## PROGRAM:
'''

from http.server import HTTPServer, BaseHTTPRequestHandler

content = """

<!DOCTYPE html>


<html>
    
    <head>
    
        <title>COMPANY REVENUE</title>
        
    </head>
    
    <body>
    
        <center><h1>REVENUE</h1></center>
        
        <table bgcolor="red"
        
        border="20" 
        
        align="center">
        
            <tr
            
            bgcolor="white"
            
            cellspace="10">
            
                 <TH>RANK</TH>
                 
                <th>NAME OF COMPANY</th>
                
                <TH>YEAR</TH>
                
                <TH>REVENUE</TH>
                
                <TH>HEADQUATERS</TH>
                
            </tr>
            
            <TR  bgcolor="white"
            
            cellspace="10">
            
                 <TD>1</TD>
                 
                <TD> MICROSOFT</TD>
                
                <TD>2014</TD>
                
                <TD>$86.5M</TD>
                
                <TD>USA</TD>
                
            </TR>
            
            <TR bgcolor="white"
            
            cellspace="10">
            
                 <TD>2</TD>
                 
                <TD> ORACLE</TD>
                
                <TD>2014</TD>
                
                <TD>$37.5M</TD>
                
                <TD>USA</TD>
                
            </TR>
            
            <TR bgcolor="white"
            
            cellspace="10">
            
                <TD>3</TD>
                
                <TD> SAP</TD>
                
                <TD>2014</TD>
                
                <TD>$20.9M</TD>
                
                <TD>GERMANY</TD>
                
            </TR>
            
            <TR bgcolor="white"
            cellspace="10">
            
                <TD>4</TD>
                
                <TD>SYMSNTEC</TD>
                
                <TD>2014</TD>
                
                <TD>$6.5M</TD>
                
                <TD>USA</TD>
                
            </TR>
            
            <TR bgcolor="white"
            
            cellspace="10">
            
                <TD>5</TD>
                
                <TD>VMWARE</TD>
                
                <TD>2014</TD>
                
                <TD>$5.2M</TD>
                
                <TD>USA</TD>
                
            </TR>
            
            <TR bgcolor="WHITE"
            
            cellspace="10" >
            
                <TD>6</TD>
                
                <TD>CA TECHNOLOGIES</TD>
                
                <TD>2014</TD>
                
                <TD>$4.5M</TD>
                
                <TD>USA</TD>
                
            </TR>
            
            <TR bgcolor="white"
            
            cellspace="10">
            
                <TD>7</TD>
                
                <TD>ADOBE SYSTEMS</TD>
                
                <TD>2014</TD>
                
                
                <TD>$4.4M</TD>
                
                <TD>USA</TD>
                
            </TR
            
            <TR bgcolor="white"
            
            cellspace="10">
            
                <TD>8</TD>
                
                <TD>FISERV</TD>
                
                <TD>2014</TD>
                
                <TD>$4.3M</TD>
                
                <TD>USA</TD>
                
            </TR>
            
            <TR bgcolor="white"
            
            cellspace="10">
            
                <TD>9</TD>
                
                <TD>INTUIT</TD>
                
                <TD>2014</TD>
                
                <TD>$3.3M</TD>
                
                <TD>USA</TD>
                
            </TR>
            
            </TR>
            
        </table>
        
    </body>
    
</html>

"""

class myhandler(BaseHTTPRequestHandler):

    def do_GET(self):
    
        print("request received")
        
        self.send_response(200)
        
        self.send_header('content-type', 'text/html; charset=utf-8')

        self.end_headers()
        
        self.wfile.write(content.encode())
        
server_address = ('',80)

httpd = HTTPServer(server_address,myhandler)

print("my webserver is running...")


httpd.serve_forever()


'''

## OUTPUT:
![Screenshot 2024-03-20 211644](https://github.com/sakamalesh/simplewebserver/assets/149148235/1fdc4219-c087-4413-89a4-12713881d3fb)

![Screenshot 2024-03-20 212543](https://github.com/sakamalesh/simplewebserver/assets/149148235/2f8a945d-42fb-4c59-b10c-c50d390c872f)



## RESULT:
The program for implementing simple webserver is executed successfully.
