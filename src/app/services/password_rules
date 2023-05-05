import {PasswordComplexityRules} from 'password_rules';
import {PasswordChangeRules} from 'password_rules';
import {PasswordBlockRules} from 'password_rules';


//Dla peracionistov
const PasswordCheck_User = {
      "LengthMin" : 12, //minimal'naya dlina
      "LengthMax" : 32, //max dlina
      "CharMin" : 2, //minimal'noe kolichestvo bukv
      "UpperMin" : 2,//minimal'noe kolichestvo bol'shikh bukv
      "LowerMin" : 1,//minimal'noe kolichestvo malen'ki bukv
      "CharSpecial" : "~!@#%^&*()-=_+",// razrshennie special'nye simvoly
      "CharSpecialMin" : 1,//minimal'noe kolichestvo spec sivmolov
      //"MustContain" : ['1','a'], //obyazatel'no dolzhen sodezhat'
      //"MustNotContain" : ['qwerty','123456789'],//obyazatel'no ne dolzhen soderzhat'. Syuda po khoroshemu nado prikrutit' slovar'
      "CustomValidate" : (password) => { return "";}, //return error string if false, return "" if true
    };

//Dla poddegrky 
const PasswordCheck_PrivUser = {
	  "LengthMin" : 16, //minimal'naya dlina
      "LengthMax" : 32, //max dlina
      "CharMin" : 2, //minimal'noe kolichestvo bukv
      "UpperMin" : 2,//minimal'noe kolichestvo bol'shikh bukv
      "LowerMin" : 1,//minimal'noe kolichestvo malen'ki bukv
      "CharSpecial" : "~!@#%^&*()-=_+",// special'nye simvoly
      "CharSpecialMin" : 1,//minimal'noe kolichestvo spec sivmolov
      //"MustContain" : ['1','a'], //must contain strs, case sensitive
      //"MustNotContain" : ['admin','password'],//must not contain strs, case sensitive
      "CustomValidate" : (password) => { return "";}, //return error string if false, return "" if true
    };
const passwordCheckUser = new PasswordComplexityRules(PasswordCheck_User, {}, "policyC_user");
const passwordCheckPrivUser = new PasswordComplexityRules(PasswordCheckPriv_User, {}, "policyC_admin");



const PasswordChange_User = {
	  "PasswordChangePeriod" : 90, //skol'ko dney dejstvuet parol'
      "NotificationGap" : 15, //za skolko nado predupregdat 
	  "ActionAfreChangePeriod" : 0, // 0 - prodolzhaem preduprezhdat', 1 - blokiruem pol'zovatelya
	  "PasswordChange"

    };
	
const passwordChangeUser = new PasswordChangeRules(PasswordChange_User, {}, "policyCh_user");	

const PasswordBlock_User = {
      "isFailAuthPermanentBlock" = : 0 // 0  - ne primenyaem pravilo  postoyanoj 1 - primenyaem pravilo postoyanoj blokirovki
	//"PermanentBlockFailCount" : 0, //kolichestvo ne udachnyj popytok do postoyannoj blokirovki pol'zovatelya
	//"PermanentBlockCounterResetPeriod" : 600 // interval v sekundaх sbrosa schetchika postoyannoj blokirovki
	  "isFailAuthTemporarytBlock" = : 1,  //  0  - ne primenyaem pravilo vremennoj blokirovki 1 - primenyaem pravilo vremennoj blokirovki
      "TemporarytBlockFailCount" : 5, //skol'ko dney dejstvuet parol'
	  "PermanentBlockCounterResetPeriod" : 600 // interval v minutakh sbrosa vremennoj schetchika  blokirovki

    };
	
	
	
