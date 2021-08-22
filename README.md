<php

//mau ngapain si lo goblok

error_reporting(0);
require_once("cfg.php");
date_default_timezone_set('Asia/Jakarta');

/* START COLOR */
$res="\033[0m";
$hitam="\033[0;30m";
$abu2="\033[1;30m";
$putih="\033[0;37m";
$putih2="\033[1;37m";
$red="\033[0;31m";
$red2="\033[1;31m";
$green="\033[0;32m";
$green2="\033[1;32m";
$yellow="\033[0;33m";
$yellow2="\033[1;33m";
$blue="\033[0;34m";
$blue2="\033[1;34m";
$purple="\033[0;35m";
$purple2="\033[1;35m";
$lblue="\033[0;36m";
$lblue2="\033[1;36m";
//ColorSemvak
$R="\e[31m";
$G="\e[32m";
$Y="\e[33m";
$B="\e[34m";
$P="\e[35m";
$C="\e[36m";
$W="\e[37m"; 

function url($url){
$headers = array();
$headers[] = "Mozilla/5.0 (Linux; Android 10; Redmi Note 4) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/92.0.4515.115 Mobile Safari/537.36";
$ch = curl_init();
      curl_setopt($ch, CURLOPT_URL, $url);
      curl_setopt($ch, CURLOPT_FOLLOWLOCATION, true);
      curl_setopt($ch, CURLOPT_RETURNTRANSFER, 1);
      curl_setopt($ch, CURLOPT_HTTPHEADER, $headers);
      $res = curl_exec($ch);
return $res;
}
error_reporting(0);
system("clear");
$SC = "1";
$res = url("http://controlc.com/4099dcb0");
$link1 = explode('Link: ',$res);
$link = explode(' ',$link1[1]);
$pw1 = explode('[tpcolor=#FF0000]',$res);
$pw = explode('[',$pw1[1]);
$pass = $pw[0];
$read = file_get_contents("key.txt");
system('clear');
if ($pass=="off"){
$o = "\033[1;32m[\033[1;31mOFFLINE\033[1;32m]";
}else{
$o = "\033[1;32m[ONLINE]";
}
if ($pass=="update"){
$o = "\033[1;32m[\033[1;91mUpdate\033[1;92m]";
}
if ($pass=="down"){
$o = "\033[1;32m[\033[1;91mKO'ID\033[1;92m]";
}
$res = url("https://controlc.com/b27a1f06");
$lg1 = explode('Login: ',$res);
$login = explode('/ajax_auth',$lg1[1]);
$putih2.system("toilet -f wideterm -F border '           KING x LeX           '");
    echo "{$P}[✖]{$B}╔════════════════════════════════════════════════╗{$P}[✖]\n";
    echo "{$P}[✖]{$B}╠≑╾≽ {$R}WARNING...!!!                               {$B}║{$P}[✖]\n";
    echo "{$P}[✖]{$B}╠≑╾≽ {$W}Ini Adalah Program Illegal...!!!            {$B}║{$P}[✖]\n";
    echo "{$P}[✖]{$B}╠≑╾≽ {$W}Resiko Di Tanggung Pengguna...!!!           {$B}║{$P}[✖]\n";
    echo "{$P}[✖]{$B}╠≑╾≽ {$W}Gunakan Tool Ini Dengan Bijak...!!!         {$B}║{$P}[✖]\n";
    echo "{$P}[✖]{$B}╚════════════════════════════════════════════════╝{$P}[✖]\n\n";

if ($pass == 'down'){
    echo "\033[1;92m[≽] \033[1;91mSCRIPT INI SUDAH TIDAK BERFUNGSI LAGI \n";
    echo "\033[1;92m[≽] \033[1;91mKARNA WEBSITE atau APLIKASI SUDAH KO'ID \n";
    echo "\033[1;92m[≽] \033[1;92mTERIMA KASIH\n\n";
      exit;
}

if ($link[0]==""){
    echo "\033[1;91mKONEKSI TERPUTUS, SILAHKAN CEK KONEKSIMU\n";
    echo "\033[3;91mConnection Lost, Please Check Your Connection\n";
exit;
}

if ($pass == 'update'){
    echo "\033[1;92m[≽] \033[1;91mSCRIPT Anda Sudah Tidak Terhubung ke Server \033[1;92m \n";
    echo "\033[1;92m[≽] \033[1;97mSilahkan Copy Paste Link \n\n";
    echo "\033[1;92m[≽] \033[1;97mLink Script Versi Update \033[1;92m$link[0]\n\n";
      exit;
}

if ($pass == 'off'){
    echo "\033[1;92m[≽] \033[1;91mSCRIPT SEDANG OFFLINE \033[1;97matau \033[1;91mMAINTENANCE \n";
      exit;
}else{
if($read == $pass){
    echo "\033[1;37m[≽] Password Di Reset Setiap Malming (ツ) \n";
    echo "\033[1;91m[≽] \033[1;92mUPLOAD Password \r\n";
    sleep(5);
    echo "\n\033[1;97mLoading \033[1;31m≽\r";
    sleep(1);
    echo "\033[1;97mLoading \033[1;31m≽ \033[1;31m≽\r";
    sleep(1);
    echo "\033[1;97mLoading \033[1;31m≽ \033[1;31m≽ \033[1;31m≽ \r";
    sleep(1);
}
elseif($read != $pass){
$save = fopen("key.txt", "w");
    echo "\033[1;37m[≽] Password Di Reset Setiap Malming (ツ) \n";
    echo "\033[1;37m[≽] \033[1;91mLink Password :\033[0;31m $link[0]\n";
    echo "\033[1;37m[≽] \033[1;37mMASUKAN PASSWORD DI SINI ╾≽ \033[1;92m";
$p = trim(fgets(STDIN));
if ($p==""){
exit;
}
    echo "\n\033[1;97mLoading \033[1;31m≽\r";
    sleep(1);
    echo "\033[1;97mLoading \033[1;31m≽ \033[1;31m≽\r";
    sleep(1);
    echo "\033[1;97mLoading \033[1;31m≽ \033[1;31m≽ \033[1;31m≽ \r";
    sleep(1);
if($pass == $p){
fwrite($save, $p);
    echo "\n\033[1;91m[≽] \033[1;92mOPEN SCRIPT SUCCESS            \r";
fclose($save);
        sleep(5);
        }else{
    echo "\n\033[1;92m[≽] \033[1;91mGAGAL...!!!, MASUKIN PASSWORD YG BENER DONG. SILAHKAN COBA LAGI\n";
        exit;
        }
        }
}
    sleep(1);
    echo "\n\033[1;97mKlik \033[1;32mENTER \033[1;37mUntuk Melanjutkan ".$M2;
$kkk = trim(fgets(STDIN));


function verify($url,$headers) {

	$claim = curl_init();
	curl_setopt($claim, CURLOPT_URL, $url);
	curl_setopt($claim, CURLOPT_FOLLOWLOCATION, true);
	curl_setopt($claim, CURLOPT_RETURNTRANSFER, 1);
	curl_setopt($claim, CURLOPT_HTTPHEADER, $headers);
	curl_setopt($claim, CURLOPT_SSL_VERIFYPEER, 0);
	$result = curl_exec($claim);
	return $result;} 
	system("clear");
	$api_web = file_get_contents("https://api.myip.com"); $parsing = json_decode($api_web); $get = $parsing->ip;  
    echo "\033[1;97mLoading \033[1;31m≽\r";
    sleep(1);
    echo "\033[1;97mLoading \033[1;31m≽ \033[1;31m≽\r";
    sleep(1);
    echo "\033[1;97mLoading \033[1;31m≽ \033[1;31m≽ \033[1;31m≽ \r";
    sleep(1);
    echo"{$W}[≽]{$W} (ツ) {$G}ENJOY {$W}TO {$P}PROGRAM {$W}(ツ) \r";
	sleep(2);
	system('clear');
	echo"{$W}[≽]╾≽{$G} L{$Y}O{$R}G{$W}I{$P}N {$W}DONE {$W}✔";
	system('clear');
//dashboard
$putih2.system("toilet --width 70 -f pagga -F border  'UPTOCOIN'");
	echo $putih2." TANGGAL ".$green2.date("d.m.Y ").$putih2."  JAM ".$green2.date("H:i:s");
	echo "\n{$B}╔════════════════════════════════════════════════╗\n"; 
	echo "{$B}╠≑╾≽ {$W}AUTHOR : KINGxLeX";  echo "                {$B}[{$G}ONLINE{$B}] {$Y}✔ {$B}║\n";
	echo "{$B}╠≑╾≽ {$W}TLGRM  : @retrunvoid                        {$B}║\n";
	echo "{$B}╠≑╾≽ {$W}DATE   : 20-08-2021                         {$B}║\n";
	echo "{$B}╠≑╾≽ {$W}WEB    : FAUCETPAY.IO                       {$B}║\n";
	echo "{$B}╠≑╾≽ {$W}WEB    : UPTOCOIN                           {$B}║\n";
	echo "{$B}╚════════════════════════════════════════════════╝\n";
	sleep(1); 
    echo "{$G}╾≽ IP : [ {$W}{$get} {$G}]\n";
    sleep(2); 
    echo "{$G}╾≽ {$Y}Autoclaim {$C}started!\n"; sleep(2);
$putih2.system("toilet -f wideterm -F border '           KING x LeX           '");    
//GoProgram
		$headers = array("user-agent: ".$browser,"accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8","referer: https://uptocoin.tk/fp/","cookie: __gads=ID=ce97c7690b023f5e-2263588d81ca00ce:T=1627099832:RT=1627099832:S=ALNI_MZqO6H23hzB1rpUusRE1gbxr4E5Ew;HstCfa4361570=1627099909767;HstCmu4361570=1627099909767;HstCnv4361570=1;HstCns4361570=1;__dtsu=51A016267378442D7EDF2D06B6CC0BD9;HstCla4361570=1627099946738;HstPn4361570=3;HstPt4361570=3");
		$verify = verify("https://uptocoin.tk/fp/verify.php",$headers);

function claim_get($url,$headers,$data) {

	$claim = curl_init();
        curl_setopt($claim, CURLOPT_URL, $url);
        curl_setopt($claim, CURLOPT_FOLLOWLOCATION, true);
        curl_setopt($claim, CURLOPT_RETURNTRANSFER, 1);
        curl_setopt($claim, CURLOPT_HTTPHEADER, $headers);
        curl_setopt($claim, CURLOPT_SSL_VERIFYPEER, 0);
	curl_setopt($claim, CURLOPT_POSTFIELDS, $data);
        $result = curl_exec($claim);
	return $result;}
	while(true) { $claim_get = claim_get("http://uptocoin.tk/fp/faucet.php?address=".$address."&currency=DOGE&key=e16d7168996b75981b026f9069ec73a1",$headers,"address=".$address."&currency=DOGE");
		$scraping = explode('<div class="alert alert-success">', $claim_get);
		$balance = explode('<a target="_blank"', $scraping[1]);
		if ($balance[0] !== null) {
echo $putih2.date("🔴 [d-m-Y]").$putih2. " {$Y}".$balance['0']."{$W}╼≽ {$G}Autoclaim {$C}Faucetpay.io ✔\n";

		} else { continue; }

	$second = 60+time();
	while(true):
		echo "\r				\r";
		$timer = $second-time();
		if ($timer < 1) { break; }
		    echo "🔴{$P} Next {$R}Claim{$G} ╼╼≽ [{$Y}".date('s', $timer)."{$G}]";
		    sleep(1);
			endwhile;}

