# MSOffice2016PrefTool
bash script for manipulating MS Office 2016 preference stored in sqlite3 database


Call the tool and pass appropriate arguments. The tool will work by passing keys and values, or a proprly formatted plist containng multiple preference keys and values.

Usage: MSOffice2016PrefTool.sh [-hp:n:k:t:v:] [-p Plist] [-n RegNode]...
You can either pass a properly formatted plist with a bunch of preference keys, or pass
individual keys and values to the tool.

    -h          Display this help and exit
    -p Plist    Read settings from a properly formatted plist file instead of standard
                input arguments. If this is passed, other arguments are ignored.
    -n RegNode  The path to the node you want to add the named preference.
                (Requires -k -t and -v accompany this.)
    -k KeyName  The name of the key you are setting.
                (Requires -n -t and -v accompany this.)
    -t Type     The key type.  (1 = String, 3 = Blob data, 4 = Number)
                (Requires -n -k and -v accompany this.)
    -v Value    The actual value you are saving to the preference key.
                (Requires -n -k and -y accompany this.)
