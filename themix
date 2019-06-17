#!/bin/bash
# hacky tilix themes

# $1 = Xresources colours file
# $2 = name of theme

xres=$1
name="$2"

basename=$(basename $0)
if [[ $1 == "help" ]]; then
   printf "themix - hacky way to make tilix themes from Xresources files\n\nUsage: $basename <Xresources file> 'Theme Name'\n"
   exit
else
   :
fi

mapfile -t <<< "$(cat $xres)"
bg=$(printf "%s\n" "${MAPFILE[2]}" | awk '{print $2}')
fg=$(printf "%s\n" "${MAPFILE[1]}" | awk '{print $2}')
c0=$(printf "%s\n" "${MAPFILE[6]}" | awk '{print $2}')
c1=$(printf "%s\n" "${MAPFILE[10]}" | awk '{print $2}')
c2=$(printf "%s\n" "${MAPFILE[14]}" | awk '{print $2}')
c3=$(printf "%s\n" "${MAPFILE[18]}" | awk '{print $2}')
c4=$(printf "%s\n" "${MAPFILE[22]}" | awk '{print $2}')
c5=$(printf "%s\n" "${MAPFILE[26]}" | awk '{print $2}')
c6=$(printf "%s\n" "${MAPFILE[30]}" | awk '{print $2}')
c7=$(printf "%s\n" "${MAPFILE[34]}" | awk '{print $2}')
c8=$(printf "%s\n" "${MAPFILE[7]}" | awk '{print $2}')
c9=$(printf "%s\n" "${MAPFILE[11]}" | awk '{print $2}')
c10=$(printf "%s\n" "${MAPFILE[15]}" | awk '{print $2}')
c11=$(printf "%s\n" "${MAPFILE[19]}" | awk '{print $2}')
c12=$(printf "%s\n" "${MAPFILE[23]}" | awk '{print $2}')
c13=$(printf "%s\n" "${MAPFILE[27]}" | awk '{print $2}')
c14=$(printf "%s\n" "${MAPFILE[31]}" | awk '{print $2}')
c15=$(printf "%s\n" "${MAPFILE[35]}" | awk '{print $2}')

cat <<EOT >> /tmp/theme.json
{
  "name": "$name",
  "comment": "a theme",
  "foreground-color": "$fg",
  "background-color": "$bg",
  "use-theme-colors": false,
  "use-highlight-color": false,
  "use-cursor-color": false,
  "cursor-foreground-color": "#ffffff",
  "cursor-background-color": "#efefef",
  "use-badge-color": true,
  "badge-color": "#ac7ea8",
  "palette": [
    "$c0",
    "$c1",
    "$c2",
    "$c3",
    "$c4",
    "$c5",
    "$c6",
    "$c7",
    "$c8",
    "$c9",
    "$c10",
    "$c11",
    "$c12",
    "$c13",
    "$c14",
    "$c15"
  ]
}
EOT

if [[ $name =~ \ |\' ]]; then
   name="${name// /_}"
else
   :
fi
mv /tmp/theme.json $HOME/.config/tilix/schemes/"$name".json
