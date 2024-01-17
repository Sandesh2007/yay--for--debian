# yay--for--debian
Did you looved the yay available only for arch 
bow it is available for debian,ubuntu based distro too 
no pacakage need to be installed just in 3 steps copy paste and save


just copy and paste this in your .bashrc file and you are good to go
this is not from the orignal from the creator/s of yay 
i dont know them/him/her 
just a normal human using zorin os with yay 
if anyone have any offence just tell me to remove it (only form the creators)


yay() {
    if [ "$#" -eq 0 ]; then
        sudo apt update && sudo apt upgrade
    elif [ "$1" = "-h" ]; then
        echo "Usage: yay [-s] [-S]"
    else
        case "$1" in
            "-s")
                shift
                sudo apt search "$@"
                ;;
            "-S")
                shift
                sudo apt install "$@"
                ;;
            *)
                echo "Usage: yay [-s] [-S]"
                return 1
                ;;
        esac
    fi
}
from Nepal
Happy coding :)
