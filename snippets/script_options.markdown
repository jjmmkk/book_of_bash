# Script options

How to handle script options like `./my_script.sh -h`.

Each letter in the `getopts` argument is an option key. If an option key is used that is not present in this argument, the second last case in the example below will be matched.

The first colon toggles verbose error handling. Present equals off. Having it off supresses the default error messages and instead you can use the two last cases in the example below to give more adequate feedback.

The subsequent colons are related to the option key in front of them. It dictates whether or not the option requires an argument. If an option requires an argument and none is given, the last case in the example below will be matched.

	```bash
	while getopts ':he:s:v:' opt
	do
		case $opt
		in
	#		PATTERN)
	#			echo "$opt was triggered with parameter: $OPTARG"
				;;
			h)
				show_help=true
				;;
			e)
				environment="$OPTARG"
				;;
			s)
				site_name="$OPTARG"
				;;
			v)
				version="$OPTARG"
				;;
			\?)
				echo "Invalid option: -$OPTARG" >&2
				exit 1
				;;
			:)
				echo "Option -$OPTARG requires an argument" >&2
				exit 1
				;;
		esac
	done
	```
