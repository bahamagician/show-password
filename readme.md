# Show Password jQuery Script

This is a small script that will show the contents of a password form field.  

The included index file shows the implementation.  Please note that although I'm using bootstrap css, it's not necessary for the functionality.  

**The necessary scripts are:**

- jQuery
- FontAwesome (Can be replaced with other icons)

## Instructions

1. Include jQuery and FontAwesome in your page.

2. Insert the following script after the jQuery inclusion:

```
<script type="text/javascript">
  $(document).ready(function() {
    $(".show-password-btn").click(function() {
      var passwordField = $(this).attr("data-field");
      var passwordToggleValue = ($(passwordField).attr("type") == "password") ? 'text' : 'password';
      $('.fa-check, .fa-square-o', this).toggle();
      $(passwordField).attr("type", passwordToggleValue);
    });
  });
</script>
```

3. Finally, add the following HTML to your form (see index file for details).
**Please note that the data-field attribute must reference the ID of your password field**

```
<!-- Show Password Button -->
<div class="show-password-btn pull-right" data-field="#my-password">
  <i class="fa fa-square-o" style="display: inline-block;"></i>
  <i class="fa fa-check" style="display: none;"></i> Show Password
</div>
<!-- End Show Password Button -->
```
