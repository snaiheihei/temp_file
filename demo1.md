


jy_work="/home/snail/jupyter_files"
# check juputer progress and make it up
jy=`ps -ef | grep jupyter | grep -v grep | awk '{print $2}'`
if [ -z "$jy" ]
then
        echo "Start Up jupyter ..."
        jupyter notebook --ip 0.0.0.0 --notebook-dir="$jy_work" --no-browser  > ${jy_work}/jupyter.log  2>&1 &
fi


