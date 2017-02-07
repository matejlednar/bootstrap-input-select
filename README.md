# bootstrap-input-select
Input/Select widget for Bootstrap

- User can use rounded design or squared design.
- User can extract URL and set it to input field or set item name (value).
- User can set full width (100%) or define own width.

Easy to use, copy and paste small CSS, HTML, and JavaScript fragments.

##CSS fragment
      .input-select .btn.dropdown-toggle {
          float: none;
      }
      .input-select .dropdown-toggle {
          left: -4px;
          top: -1px;
          padding: 2px 12px;
      }
      .input-select .field input,
      .input-select .field {
          width : 100%;
      }
      .input-select .dropdown-toggle {
          border-radius: 0;
      }            
      .input-select .dropdown-menu {
          width : 100%;
      }       
      .input-select .dropdown-menu li {
          overflow: hidden;
          margin-right: 20px;
      }

##HTML fragment
    <div class="input-select btn-group">
        <table><tr><td class="field">
                    <input id="inputSelectField" type="text">
                </td><td>
                    <a class="btn btn-primary dropdown-toggle" data-toggle="dropdown">
                        <span class="caret"></span>
                    </a>

                    <ul class="dropdown-menu">
                        <li><a href="http://onlinewebsiteregistration.mldgroup.com/index.php">Online Website Registration</a></li>
                        <li><a href="http://onlinevalidators.mldgroup.com/index.php">Online Validators</a></li>
                        <li><a href="http://onlinecoderunner.mldgroup.com/">Online Code Runner</a></li>
                    </ul>
                </td></tr>
        </table>
    </div>

##JavaScript code
```javascript
$(".input-select .dropdown-menu").on("click", function (e) {
    var item = e.target;
    var name = item.textContent;
    var href = item.getAttribute("href");
    $("#inputSelectField").val(name);
    e.preventDefault();
});
```
