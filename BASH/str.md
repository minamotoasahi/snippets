1. 截取字符串
    ```bash
    str="abc@abcd@abcde"
    echo ${str#*@}    # abce@abcde
    echo ${str##*@}   # abcde
    echo ${str%@*}    # abc@abcd
    echo ${str%%@*}   # abc
