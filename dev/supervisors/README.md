mkdir $(tmcpull.sh --tkg --csv | csvcut -x -c 1 | tail -n+2 | xargs)

for tkg in $(tmcpull.sh --tkg --csv | csvcut -x -c 1 | tail -n+2 | xargs); do touch $tkg/$tkg.yaml; done
