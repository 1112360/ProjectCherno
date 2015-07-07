# ProjectCherno
Selling website using Yii framework

git status
git remote
//then writing something
git add -A && git commit
//write the message, then press Ctrl+O, then Exit
git push origin master
git submodule add git://github.com/yiisoft/yii.git yii
git checkout 1.1.13
cd ..
git status
git add yii
git commit -m "Use Yii version 1.13"
pwd
//checking the absolute path of this yii
//                /home/ubuntu/workspace
// then paste that path to create new yii skeleton
php yii/framework/yiic.php webapp /home/ubuntu/workspace/projectCherno git
//then go to index.php make redirect to our projectCherno page
//you should use your codde....
git commit -a -m "redirect from index.php to projectCherno"

//now to the main part
//we will move protected folder outside of projectCherno
//cut protected folder outside of project to workspace folder
//cut runtime folder outside of project to workspace folder
//and then we will edit these files
//1. projectCherno/index.php
//$yii=dirname(__FILE__).'/../yii/framework/yii.php';
//$config=dirname(__FILE__).'/../protected/config/main.php';
//the .. mean get to parent of that
//2. protected/yiic.php
//$yiic=dirname(__FILE__).'/../yii/framework/yiic.php';
//$config=dirname(__FILE__).'/config/console.php';
//3. protected/config/main.php
/*View and add and changing these line
    
    function _joinpath($dir1, $dir2) {
        return realpath($dir1 . '/' . $dir2);
    }
 
    $homePath      = dirname(__FILE__) . '/../..';
    $protectedPath = _joinpath($homePath, 'protected');
    $webrootPath   = _joinpath($homePath, 'webroot');
    $runtimePath   = _joinpath($homePath, 'runtime');

    return array(
    	'basePath'=>$protectedPath,
    	'runtimePath' => $runtimePath,
    	.........

*/
