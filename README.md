# SublimeBuildSystems
Sublime text build systems for different programming languages.
<br>
<br>
<br>
Put the inputs in in.in file in your source file directory and your output will be written in out.out file.
<br>
Preferrable when using 3 column layout with source file, input file and output file opened in each window.
<br>
<br>

#### C++
```
{
	"shell_cmd": "g++ \"${file}\" -o \"${file_path}/${file_base_name}\"",
	"shell":true,
	"working_dir":"$file_path",
	"selector":"source.c",
	"variants": [
        {
            "shell_cmd": "g++ \"${file}\" -o \"${file_path}/${file_base_name}\" && \"${file_path}/${file_base_name}\" <\"${file_path}/in.in\">\"${file_path}/out.out\"",
            "name": "Compile Run in out"
        }
    ]
}
```

#### Java
```
{
    "shell_cmd": "javac \"$file\"",
    "shell":true,
    "working_dir":"$file_path",
    "selector": "source.java",

    "variants": [
        {
            "shell_cmd": "javac \"${file}\" && java \"${file_base_name}\" <\"${file_path}/in.in\">\"${file_path}/out.out\"",
            "name": "Compile Run in out"
        }
    ]
}
```

#### Python
```
{
    "shell_cmd": "python $file_name",
    "selector": "source.python",
    "working_dir": "$file_path",

    "variants": [
        {
            "shell_cmd": "python $file_name<in.in>out.out",
            "name": "Compile Run in out"
        }
    ]
}
```
