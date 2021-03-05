<!DOCTYPE html>
<html>
<head>
<title>EducationalSimulation</title>
<meta http-equiv='Content-Type' content='text/html;charset=utf-8' />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />

<style>
#divMyGame canvas:focus { outline: none;background-color: #000;}
#divMyGame canvas { outline: none;background-color: #000;}
.CssTable{background-color:#050505; text-align:center; width:100%; border: 1px solid teal; }
.CssTable td{ border: 1px solid chartreuse; }
.btn {background-color: #4CAF50; /* Green */border: none;color: white;padding: 16px 32px;text-align: center;text-decoration: none;display: inline-block;font-size: 16px;margin: 4px 2px;transition-duration: 0.4s;cursor: pointer;}
.btn1 {background-color: white; color: black; border: 2px solid #4CAF50;}
.btn1:hover {background-color: #4CAF50;color: white;}
.btn2 {background-color: white; color: black; border: 2px solid #008CBA;}
.btn2:hover {background-color: #008CBA;color: white;}
body{ background-color:#222; margin:0; padding:0;}
</style>
</head>
<body>
    <table class='CssTable'>
        <tr><td id='divMyGame'></td></tr>
        <tr>
            <td>
                <input type="button" class="btn btn1" value="FullScreen" onclick="_Game.Fullscreen();" />
                <input type="button" class="btn btn1" value="Full Width" onclick="_Full_Width();" />
                <input type="button" class="btn btn1" value="Full Height" onclick="_Full_Height();" />
                <input type="button" class="btn btn1" value="Reset Size" onclick="_Reset_Size();" />
            </td>
        </tr>
        <tr>
            <td>
                <input type="button" class="btn btn2" value="Restart Game" onclick="_Game.Start(divMyGame);" />
            </td>
        </tr>
    </table>

    <script type='text/javascript' src='https://cdn.statistically.com/quanha22/quanha22.github.io/main/EducationalSimulation.js'></script>

    <script>
            _Game.Start(divMyGame);
            function _Full_Width() {
                divMyGame.firstChild.style.width = "100%";
                divMyGame.firstChild.style.height = "";
                divMyGame.scrollIntoView();
            }
            function _Full_Height() {
                divMyGame.firstChild.style.height = "99vh";
                divMyGame.firstChild.style.width = "";
                divMyGame.scrollIntoView();
            }
            function _Reset_Size() {
                divMyGame.firstChild.style.width = "";
                divMyGame.firstChild.style.height = "";
                divMyGame.scrollIntoView();
            }
    </script>
</body>
</html>