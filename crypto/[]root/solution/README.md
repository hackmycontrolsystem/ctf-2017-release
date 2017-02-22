This covers how to create the challenge.  Solving it is the steps in reverse (shown at end).


> Start with desired modulus:

72:6f:6f:74:00:00:00:00:00:00:00:00:00:00:00:
00:00:00:00:00:00:1b:00:00:00:00:00:00:00:00:
00:00:00:00:00:1f:ff:fb:00:00:00:00:00:00:00:
00:00:00:00:00:1f:ff:fb:00:00:00:00:00:00:00:
00:00:00:00:00:1f:ff:ff:77:77:77:7b:00:00:00:
00:00:00:00:00:1f:ff:ff:ff:ff:ff:fb:00:00:00:
00:00:00:00:00:1f:ff:ff:ff:ff:fb:00:00:00:00:
00:00:00:00:00:1f:ff:ff:ff:ff:fb:00:00:00:00:
00:00:00:00:00:1f:ff:ff:ff:ff:ff:fb:00:00:00:
00:00:00:00:00:1f:ff:ff:22:22:22:2b:00:00:00:
00:00:00:00:00:1f:ff:fb:00:00:00:00:00:00:00:
00:00:00:00:00:1f:ff:fb:00:00:00:00:00:00:00:
00:00:00:00:00:1f:ff:fb:00:00:00:00:00:00:00:
00:00:00:00:00:1f:ff:fb:00:00:00:00:00:00:00:
00:00:00:00:00:1f:ff:fb:00:00:00:00:00:00:00:
00:00:00:00:00:1f:ff:fb:00:00:00:00:00:00:00:
00:00:00:00:00:1f:ff:fb:00:00:00:00:00:00:00:
00:00:00:00:1f:ff:00:ff:fb:00:00:00:00:00:00:
00:00:00:00:1f:00:00:00:fb:00:00:00:00:00:00:
00:00:00:1f:00:00:00:00:00:fb:00:00:00:00:00:
00:00:00:1f:00:00:00:00:00:fb:00:00:00:00:00:
00:00:1f:00:00:00:00:00:00:00:fb:00:00:00:00:
00:00:1f:00:00:00:00:00:00:00:fb:00:00:00:00:
00:00:00:1f:00:00:00:00:00:fb:00:00:00:00:00:
00:00:00:1f:00:00:00:00:00:fb:00:00:00:00:00:
00:00:00:00:1f:00:00:00:fb:00:00:00:00:00:00:
00:00:00:00:1f:ff:00:ff:fb:00:00:00:00:00:00:
00:00:00:00:00:00:1b:00:00:00:00:00:00:00:00:
00:00:00:00:00:00:00:00:00:00:00:00:66:6c:61:
67:3a:77:68:65:6e:5f:73:6f:6c:76:69:6e:67:5f:
70:72:6f:62:6c:65:6d:73:5f:64:69:67:5f:61:74:
5f:74:68:65:5f:72:6f:6f:74:73:5f:69:6e:73:74:
65:61:64:5f:6f:66:5f:6a:75:73:74:5f:68:61:63:
6b:69:6e:67:5f:61:74:5f:74:68:65:5f:6c:65:61:
76:65:73

> Convert to decimal number with python:

>>> print(0x726f6f7400000000000000000000000000000000001b000000000000000000000000001ffffb0000000000000000000000001ffffb0000000000000000000000001fffff7777777b00000000000000001ffffffffffffb00000000000000001ffffffffffb0000000000000000001ffffffffffb0000000000000000001ffffffffffffb00000000000000001fffff2222222b00000000000000001ffffb0000000000000000000000001ffffb0000000000000000000000001ffffb0000000000000000000000001ffffb0000000000000000000000001ffffb0000000000000000000000001ffffb0000000000000000000000001ffffb00000000000000000000001fff00fffb000000000000000000001f000000fb0000000000000000001f0000000000fb00000000000000001f0000000000fb000000000000001f00000000000000fb0000000000001f00000000000000fb000000000000001f0000000000fb00000000000000001f0000000000fb0000000000000000001f000000fb000000000000000000001fff00fffb0000000000000000000000001b0000000000000000000000000000000000000000666c61673a7768656e5f736f6c76696e675f70726f626c656d735f6469675f61745f7468655f726f6f74735f696e73746561645f6f665f6a7573745f6861636b696e675f61745f7468655f6c6561766573)

119514949101869418903318873112867362646835071069241106524305309393065463453656568774743760570131693630159578791023971219610889380592598543536351234572467281587006324435481617535146537233169791976943380665697114009764947413190424965605151568078201516319476934559728328089096265594820785319942352507655193149106742096711100954500911687865197173709176323170965183162767042434738106978751911965481346436431672573623281881734153294758147557422163198312359915688282919868328721978258906227136067834058632472297370857579705187167410321575782375360591482072103305682978126915060591553714123014075758332542543138964874724541755348454276857383476165855448557751978878484449532359488305813436392701294505313034934195186685156298762345606852778640068236683065166398344200046690347336604718270882295167615115107501218580307986153577524246500366697040016825336440112413914980539200586226481118277959630064047314342892433714769507043011334600445934422526134766335705560228022725798756172505590957990225124583421484029071996561302075566004178669891327425036824463390441717390987200842832026336477612452651187131959535277004083894912715926527476711226812143192084609861568727011825081555042625945858913000171069362394643214510272897269118036888320894323

Using GP/PARI find previous and next prime around square root of n:

? \p 5000
   realprecision = 5009 significant digits (5000 digits displayed)
   ? n = 119514949101869418903318873112867362646835071069241106524305309393065463453656568774743760570131693630159578791023971219610889380592598543536351234572467281587006324435481617535146537233169791976943380665697114009764947413190424965605151568078201516319476934559728328089096265594820785319942352507655193149106742096711100954500911687865197173709176323170965183162767042434738106978751911965481346436431672573623281881734153294758147557422163198312359915688282919868328721978258906227136067834058632472297370857579705187167410321575782375360591482072103305682978126915060591553714123014075758332542543138964874724541755348454276857383476165855448557751978878484449532359488305813436392701294505313034934195186685156298762345606852778640068236683065166398344200046690347336604718270882295167615115107501218580307986153577524246500366697040016825336440112413914980539200586226481118277959630064047314342892433714769507043011334600445934422526134766335705560228022725798756172505590957990225124583421484029071996561302075566004178669891327425036824463390441717390987200842832026336477612452651187131959535277004083894912715926527476711226812143192084609861568727011825081555042625945858913000171069362394643214510272897269118036888320894323
   %1 = 119514949101869418903318873112867362646835071069241106524305309393065463453656568774743760570131693630159578791023971219610889380592598543536351234572467281587006324435481617535146537233169791976943380665697114009764947413190424965605151568078201516319476934559728328089096265594820785319942352507655193149106742096711100954500911687865197173709176323170965183162767042434738106978751911965481346436431672573623281881734153294758147557422163198312359915688282919868328721978258906227136067834058632472297370857579705187167410321575782375360591482072103305682978126915060591553714123014075758332542543138964874724541755348454276857383476165855448557751978878484449532359488305813436392701294505313034934195186685156298762345606852778640068236683065166398344200046690347336604718270882295167615115107501218580307986153577524246500366697040016825336440112413914980539200586226481118277959630064047314342892433714769507043011334600445934422526134766335705560228022725798756172505590957990225124583421484029071996561302075566004178669891327425036824463390441717390987200842832026336477612452651187131959535277004083894912715926527476711226812143192084609861568727011825081555042625945858913000171069362394643214510272897269118036888320894323
   ? p = precprime(round(sqrt(n)))
   %2 = 345709341936068338730678003778405323582109317075021198605451259081268526297654818935837545259489748700537817158904946124698593212156185601832821337576558516676594811692389205842412600462658083813048872307642872332289082295535733483056820073388473845450507806559178316793666044371642249466611007764799781626418800031166072773475575269610775901034485376573476373962417949231752698909821646794161147858557311852386822684705642251949742285300552861190676326816587042282505137369676427345123087656274137257931639760324708350318503061363031086796994100943084772281097123781070811610760735943618425858558459014484742232018933
   ? q = nextprime(round(sqrt(n)))
   %3 = 345709341936068338730678003778405323582109317075021198605451259081268526297654818935837545259489748700537817158904946124698593212156185601832821337576558516676594811692389205842412600462658083813048872307642872332289082295535733483056820073388473845450507806559178316793666044371642249466611007764799781626418800031166072773475575269610775901034485376573476373962417949231752698909821646794161147858557311852386822684705642251949742285300552861190676326816587042282505137369676427345123087656274137257931639760324708350318503061363031086796994100943084772281097123781070811610760735943618425858558459014484742232019973
   ? newn = p * q
   %4 = 119514949101869418903318873112867362646835071069241106524305309393065463453656568774743760570131693630159578791023971219610889380592598543536351234572467281587006324435481617535146537233169791976943380665697114009764947413190424965605151568078201516319476934559728328089096265594820785319942352507655193149106742096711100954500911687865197173709176323170965183162767042434738106978751911965481346436431672573623281881734153294758147557422163198312359915688282919868328721978258906227136067834058632472297370857579705187167410321575782375360591482072103305682978126915060591553714123014075758332542543138964874724542072396937584280625337262888775332970921021304750133076287918708895881009630077473404974677880966925170111450054682589858406625668247502091263399827525224215993035344424566568011928443888310172591327112851125472052921219080258671669993973898127049957265386657286586085405099815473365810806674154776699651214819118383817272562813199977233417411126959716068072338393084310289588450441128514416597910759814182527294940228828417785903441042114817369303389645545333054503129561885740632378715731405799144085706505382819066670726261358910837171602305916072912729756717338147737273166145500948558122541808933901885205278570148809
   ? isprime(31337)
   %5 = 1


> Using RSA tool:
brenrigh@lambda ~/download/rsatool $ ./rsatool.py -h
Usage: rsatool.py [options]

Options:
  -h, --help   show this help message and exit
  -p P         prime
  -q Q         prime
  -n N         modulus
  -d D         private exponent
  -e E         public exponent (default: 65537)
  -o FILENAME  output filename
  -f FORMAT    output format (DER, PEM) (default: PEM)
  -v           also display CRT-RSA representation


$ ./rsatool.py -p 345709341936068338730678003778405323582109317075021198605451259081268526297654818935837545259489748700537817158904946124698593212156185601832821337576558516676594811692389205842412600462658083813048872307642872332289082295535733483056820073388473845450507806559178316793666044371642249466611007764799781626418800031166072773475575269610775901034485376573476373962417949231752698909821646794161147858557311852386822684705642251949742285300552861190676326816587042282505137369676427345123087656274137257931639760324708350318503061363031086796994100943084772281097123781070811610760735943618425858558459014484742232018933 -q 345709341936068338730678003778405323582109317075021198605451259081268526297654818935837545259489748700537817158904946124698593212156185601832821337576558516676594811692389205842412600462658083813048872307642872332289082295535733483056820073388473845450507806559178316793666044371642249466611007764799781626418800031166072773475575269610775901034485376573476373962417949231752698909821646794161147858557311852386822684705642251949742285300552861190676326816587042282505137369676427345123087656274137257931639760324708350318503061363031086796994100943084772281097123781070811610760735943618425858558459014484742232019973 -n 119514949101869418903318873112867362646835071069241106524305309393065463453656568774743760570131693630159578791023971219610889380592598543536351234572467281587006324435481617535146537233169791976943380665697114009764947413190424965605151568078201516319476934559728328089096265594820785319942352507655193149106742096711100954500911687865197173709176323170965183162767042434738106978751911965481346436431672573623281881734153294758147557422163198312359915688282919868328721978258906227136067834058632472297370857579705187167410321575782375360591482072103305682978126915060591553714123014075758332542543138964874724542072396937584280625337262888775332970921021304750133076287918708895881009630077473404974677880966925170111450054682589858406625668247502091263399827525224215993035344424566568011928443888310172591327112851125472052921219080258671669993973898127049957265386657286586085405099815473365810806674154776699651214819118383817272562813199977233417411126959716068072338393084310289588450441128514416597910759814182527294940228828417785903441042114817369303389645545333054503129561885740632378715731405799144085706505382819066670726261358910837171602305916072912729756717338147737273166145500948558122541808933901885205278570148809 -e 31337 -o magickey_private.pem
Using (p, q) to initialise RSA instance

n =
726f6f7400000000000000000000000000000000001b000000000000000000000000001ffffb0000
000000000000000000001ffffb0000000000000000000000001fffff7777777b0000000000000000
1ffffffffffffb00000000000000001ffffffffffb0000000000000000001ffffffffffb00000000
00000000001ffffffffffffb00000000000000001fffff2222222b00000000000000001ffffb0000
000000000000000000001ffffb0000000000000000000000001ffffb000000000000000000000000
1ffffb0000000000000000000000001ffffb0000000000000000000000001ffffb00000000000000
00000000001ffffb00000000000000265293c4422be3532638feeb2a635e865e5bccd4862d1491f8
e46ed41afdab32ab1e913c296c45a723a371cc4ad218d273a494ac501a1c677576b84d3a1700b24e
38f3d7c8090c952767f8a9da532eb4496a953fa2b2641f93af58321e491ad6b3e1f6600ea1757635
a2d47562dff2f245bfc8ed511420931de246d56334d8897d6465b227f6c095ece1ad994c7551f08d
bc21f8b40691ee51f5f72d052d9352062f90b0e7c52c2eb18196c2c985101af4eac67499396c6241
ad4f2439ed11f87d67e73a239b865c45d65a61cf0f56082de831b97fb28ae8222a7195e0ec06c082
81ffc16e7106e77e68b8c4510424beeb5582fe21cc345f53534682b75c368d73c9

e = 31337 (0x7a69)

d =
618caed447e3b3a23fe661970669b19fc8517f1affef47db561cb4eec562b589878940899882f490
236c017870796d86753252ae97d1d1b6869490ec30867fa71e7062aecf0057fcae6bfb324c5133d1
693cc566e44c48c1ee139f5fc079d203feebf1c911d1bcccb8b925e5adbc6a851c2072bebcea000c
8c4850736a69c0865e310824f9e7de36429cb3e32ff88bf7ef4ccb39e7585de9ed3a1feaea85d087
486ba35c521e0be928a478d51a5915f3672b673c2247383670ba5991427b3dcce8d2e5c4bd7e7c0f
0a3a96eff4a0de771767a8e20f46c97a8e5f9d7878d6f3116cce6bb8462014be21875d557137bd24
8eb3590d95fce7a17bdcbdd223465cc017d6fc76fbfe2e4b9ccc49241ba452fdf84d1c8185cad33a
83c5b5ac43d946df4c3648af4f7714cd584db1ecd14458c8827ac222c3ca08280c2ba687c19aa8df
77d498cfaf700c9019f505380a78ba43f2f1bcd82a15e19c4daa3b33051d31aec1a94e043f81b7fb
21af1975588fdaa0dbfb269f118e5c4e9e26922c1440ab85357aab110361662927b74f2fe27825ba
e9e9d7aa341d8341b93588eda2e780cd99ad790ac28146f113b3d09f470e64c07a0bd51d8b4b7470
c9a931414305a53fda0a168561a2b8906ce7ff4215c0912248d55ca3e0499af1f59877b78a07a377
e570f1b9fe70b9b5cd9461bf6bc39f8734ea07b4e3f6a71129179b4183d3e4f0a9

p =
ab28ba5dbd67a4b8b4c20b76958ad57ef5513ea01af2ad59b1691a4b60e7eee058aa4776bc96a3b7
b3b3ab98a743ff0e16c22033481dfd0c83654311e153b14d5067ea4664d419b97ba28a6ee5693b00
acb7c7046762b0d8ece2bdbdc4c784923178beb1c8c78fd123003f4c107f2aa772a7f22f3052ee69
561a265acf618513acd76321d2c3a6dcd6456152c4032d8fd285ee013746eb1439f4c9c66b9ffd90
3b63208bbb0bf82b52cfc6bd12df96f3d9fa12c96456fd94e7f5c1238b3d5089e6be64ac555f8468
3ede12cc1ffa1a66fbe5e4d2c830e14d6954c48747bc1cec60582a312ee97274a9f7211e3213ff20
81d9f69b07a7b0fa8f89edd037e730ff5

q =
ab28ba5dbd67a4b8b4c20b76958ad57ef5513ea01af2ad59b1691a4b60e7eee058aa4776bc96a3b7
b3b3ab98a743ff0e16c22033481dfd0c83654311e153b14d5067ea4664d419b97ba28a6ee5693b00
acb7c7046762b0d8ece2bdbdc4c784923178beb1c8c78fd123003f4c107f2aa772a7f22f3052ee69
561a265acf618513acd76321d2c3a6dcd6456152c4032d8fd285ee013746eb1439f4c9c66b9ffd90
3b63208bbb0bf82b52cfc6bd12df96f3d9fa12c96456fd94e7f5c1238b3d5089e6be64ac555f8468
3ede12cc1ffa1a66fbe5e4d2c830e14d6954c48747bc1cec60582a312ee97274a9f7211e3213ff20
81d9f69b07a7b0fa8f89edd037e731405

Saving PEM as magickey_private.pem


> Get public key:
$ openssl rsa -in magickey_private.pem -pubout -out magickey_public.pem
writing RSA key


> Make certificate:

$ openssl req -key magickey_private.pem -days 365 -nodes -x509 -keyout magickey_cert.pem -out magickey_cert.pem
You are about to be asked to enter information that will be incorporated
into your certificate request.
What you are about to enter is what is called a Distinguished Name or a DN.
There are quite a few fields but you can leave some blank
For some fields there will be a default value,
If you enter '.', the field will be left blank.
-----
Country Name (2 letter code) [AU]:US
State or Province Name (full name) [Some-State]:New York
Locality Name (eg, city) []:New York
Organization Name (eg, company) [Internet Widgits Pty Ltd]:E Corp
Organizational Unit Name (eg, section) []:
Common Name (e.g. server FQDN or YOUR name) []:pki.e-corp.com
Email Address []:pki@e-corp.com

> Dump cert text:

$ openssl x509 -in magickey_cert.pem -text


> Server up modulus.txt file:

$ sudo openssl s_server -tls1_2 -no_dhe -no_ecdhe -WWW -cert download/rsatool/magickey_cert.pem -key download/rsatool/magickey_private.pem -accept 443
ACCEPT


>Get modulus.txt file:

$ curl -0 --tlsv1.2 --insecure -A 'E Corp PKI Modulus Fetch' https://4.3.2.1/modulus.txt
72:6f:6f:74:00:00:00:00:00:00:00:00:00:00:00:
00:00:00:00:00:00:1b:00:00:00:00:00:00:00:00:
00:00:00:00:00:1f:ff:fb:00:00:00:00:00:00:00:
00:00:00:00:00:1f:ff:fb:00:00:00:00:00:00:00:
00:00:00:00:00:1f:ff:ff:77:77:77:7b:00:00:00:
00:00:00:00:00:1f:ff:ff:ff:ff:ff:fb:00:00:00:
00:00:00:00:00:1f:ff:ff:ff:ff:fb:00:00:00:00:
00:00:00:00:00:1f:ff:ff:ff:ff:fb:00:00:00:00:
00:00:00:00:00:1f:ff:ff:ff:ff:ff:fb:00:00:00:
00:00:00:00:00:1f:ff:ff:22:22:22:2b:00:00:00:
00:00:00:00:00:1f:ff:fb:00:00:00:00:00:00:00:
00:00:00:00:00:1f:ff:fb:00:00:00:00:00:00:00:
00:00:00:00:00:1f:ff:fb:00:00:00:00:00:00:00:
00:00:00:00:00:1f:ff:fb:00:00:00:00:00:00:00:
00:00:00:00:00:1f:ff:fb:00:00:00:00:00:00:00:
00:00:00:00:00:1f:ff:fb:00:00:00:00:00:00:00:
00:00:00:00:00:1f:ff:fb:00:00:00:00:00:00:00:
00:00:00:00:1f:ff:00:ff:fb:00:00:00:00:00:00:
00:00:00:00:1f:00:00:00:fb:00:00:00:00:00:00:
00:00:00:1f:00:00:00:00:00:fb:00:00:00:00:00:
00:00:00:1f:00:00:00:00:00:fb:00:00:00:00:00:
00:00:1f:00:00:00:00:00:00:00:fb:00:00:00:00:
00:00:1f:00:00:00:00:00:00:00:fb:00:00:00:00:
00:00:00:1f:00:00:00:00:00:fb:00:00:00:00:00:
00:00:00:1f:00:00:00:00:00:fb:00:00:00:00:00:
00:00:00:00:1f:00:00:00:fb:00:00:00:00:00:00:
00:00:00:00:1f:ff:00:ff:fb:00:00:00:00:00:00:
00:00:00:00:00:00:1b:00:00:00:00:00:00:00:00:
00:00:00:00:00:00:00:00:00:00:00:00:66:6c:61:
67:3a:77:68:65:6e:5f:73:6f:6c:76:69:6e:67:5f:
70:72:6f:62:6c:65:6d:73:5f:64:69:67:5f:61:74:
5f:74:68:65:5f:72:6f:6f:74:73:5f:69:6e:73:74:
65:61:64:5f:6f:66:5f:6a:75:73:74:5f:68:61:63:
6b:69:6e:67:5f:61:74:5f:74:68:65:5f:6c:65:61:
76:65:73


> Extract cert from capture and get modulus:
$ openssl x509 -in testcert.bin -inform DER -modulus
Modulus=726F6F7400000000000000000000000000000000001B000000000000000000000000001FFFFB0000000000000000000000001FFFFB0000000000000000000000001FFFFF7777777B00000000000000001FFFFFFFFFFFFB00000000000000001FFFFFFFFFFB0000000000000000001FFFFFFFFFFB0000000000000000001FFFFFFFFFFFFB00000000000000001FFFFF2222222B00000000000000001FFFFB0000000000000000000000001FFFFB0000000000000000000000001FFFFB0000000000000000000000001FFFFB0000000000000000000000001FFFFB0000000000000000000000001FFFFB0000000000000000000000001FFFFB00000000000000265293C4422BE3532638FEEB2A635E865E5BCCD4862D1491F8E46ED41AFDAB32AB1E913C296C45A723A371CC4AD218D273A494AC501A1C677576B84D3A1700B24E38F3D7C8090C952767F8A9DA532EB4496A953FA2B2641F93AF58321E491AD6B3E1F6600EA1757635A2D47562DFF2F245BFC8ED511420931DE246D56334D8897D6465B227F6C095ECE1AD994C7551F08DBC21F8B40691EE51F5F72D052D9352062F90B0E7C52C2EB18196C2C985101AF4EAC67499396C6241AD4F2439ED11F87D67E73A239B865C45D65A61CF0F56082DE831B97FB28AE8222A7195E0EC06C08281FFC16E7106E77E68B8C4510424BEEB5582FE21CC345F53534682B75C368D73C9


> Convert to decimal with python:
>>> print(0x726F6F7400000000000000000000000000000000001B000000000000000000000000001FFFFB0000000000000000000000001FFFFB0000000000000000000000001FFFFF7777777B00000000000000001FFFFFFFFFFFFB00000000000000001FFFFFFFFFFB0000000000000000001FFFFFFFFFFB0000000000000000001FFFFFFFFFFFFB00000000000000001FFFFF2222222B00000000000000001FFFFB0000000000000000000000001FFFFB0000000000000000000000001FFFFB0000000000000000000000001FFFFB0000000000000000000000001FFFFB0000000000000000000000001FFFFB0000000000000000000000001FFFFB00000000000000265293C4422BE3532638FEEB2A635E865E5BCCD4862D1491F8E46ED41AFDAB32AB1E913C296C45A723A371CC4AD218D273A494AC501A1C677576B84D3A1700B24E38F3D7C8090C952767F8A9DA532EB4496A953FA2B2641F93AF58321E491AD6B3E1F6600EA1757635A2D47562DFF2F245BFC8ED511420931DE246D56334D8897D6465B227F6C095ECE1AD994C7551F08DBC21F8B40691EE51F5F72D052D9352062F90B0E7C52C2EB18196C2C985101AF4EAC67499396C6241AD4F2439ED11F87D67E73A239B865C45D65A61CF0F56082DE831B97FB28AE8222A7195E0EC06C08281FFC16E7106E77E68B8C4510424BEEB5582FE21CC345F53534682B75C368D73C9)
119514949101869418903318873112867362646835071069241106524305309393065463453656568774743760570131693630159578791023971219610889380592598543536351234572467281587006324435481617535146537233169791976943380665697114009764947413190424965605151568078201516319476934559728328089096265594820785319942352507655193149106742096711100954500911687865197173709176323170965183162767042434738106978751911965481346436431672573623281881734153294758147557422163198312359915688282919868328721978258906227136067834058632472297370857579705187167410321575782375360591482072103305682978126915060591553714123014075758332542543138964874724542072396937584280625337262888775332970921021304750133076287918708895881009630077473404974677880966925170111450054682589858406625668247502091263399827525224215993035344424566568011928443888310172591327112851125472052921219080258671669993973898127049957265386657286586085405099815473365810806674154776699651214819118383817272562813199977233417411126959716068072338393084310289588450441128514416597910759814182527294940228828417785903441042114817369303389645545333054503129561885740632378715731405799144085706505382819066670726261358910837171602305916072912729756717338147737273166145500948558122541808933901885205278570148809

> recover primes:

? \p 5000
   realprecision = 5009 significant digits (5000 digits displayed)
   ? n = 119514949101869418903318873112867362646835071069241106524305309393065463453656568774743760570131693630159578791023971219610889380592598543536351234572467281587006324435481617535146537233169791976943380665697114009764947413190424965605151568078201516319476934559728328089096265594820785319942352507655193149106742096711100954500911687865197173709176323170965183162767042434738106978751911965481346436431672573623281881734153294758147557422163198312359915688282919868328721978258906227136067834058632472297370857579705187167410321575782375360591482072103305682978126915060591553714123014075758332542543138964874724542072396937584280625337262888775332970921021304750133076287918708895881009630077473404974677880966925170111450054682589858406625668247502091263399827525224215993035344424566568011928443888310172591327112851125472052921219080258671669993973898127049957265386657286586085405099815473365810806674154776699651214819118383817272562813199977233417411126959716068072338393084310289588450441128514416597910759814182527294940228828417785903441042114817369303389645545333054503129561885740632378715731405799144085706505382819066670726261358910837171602305916072912729756717338147737273166145500948558122541808933901885205278570148809
   %1 = 119514949101869418903318873112867362646835071069241106524305309393065463453656568774743760570131693630159578791023971219610889380592598543536351234572467281587006324435481617535146537233169791976943380665697114009764947413190424965605151568078201516319476934559728328089096265594820785319942352507655193149106742096711100954500911687865197173709176323170965183162767042434738106978751911965481346436431672573623281881734153294758147557422163198312359915688282919868328721978258906227136067834058632472297370857579705187167410321575782375360591482072103305682978126915060591553714123014075758332542543138964874724542072396937584280625337262888775332970921021304750133076287918708895881009630077473404974677880966925170111450054682589858406625668247502091263399827525224215993035344424566568011928443888310172591327112851125472052921219080258671669993973898127049957265386657286586085405099815473365810806674154776699651214819118383817272562813199977233417411126959716068072338393084310289588450441128514416597910759814182527294940228828417785903441042114817369303389645545333054503129561885740632378715731405799144085706505382819066670726261358910837171602305916072912729756717338147737273166145500948558122541808933901885205278570148809
   ? p = precprime(round(sqrt(n)))
   %2 = 345709341936068338730678003778405323582109317075021198605451259081268526297654818935837545259489748700537817158904946124698593212156185601832821337576558516676594811692389205842412600462658083813048872307642872332289082295535733483056820073388473845450507806559178316793666044371642249466611007764799781626418800031166072773475575269610775901034485376573476373962417949231752698909821646794161147858557311852386822684705642251949742285300552861190676326816587042282505137369676427345123087656274137257931639760324708350318503061363031086796994100943084772281097123781070811610760735943618425858558459014484742232018933
   ? n = nextprime(round(sqrt(n)))
   %3 = 345709341936068338730678003778405323582109317075021198605451259081268526297654818935837545259489748700537817158904946124698593212156185601832821337576558516676594811692389205842412600462658083813048872307642872332289082295535733483056820073388473845450507806559178316793666044371642249466611007764799781626418800031166072773475575269610775901034485376573476373962417949231752698909821646794161147858557311852386822684705642251949742285300552861190676326816587042282505137369676427345123087656274137257931639760324708350318503061363031086796994100943084772281097123781070811610760735943618425858558459014484742232019973