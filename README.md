# Jmeter-Beanshell-Sampler-Code
For handling tableau authentication in Jmeter scripts

```Code:
import com.tejas.JmeterPKCS1Encryption;
                
                try {
                                String mod = vars.get("modulus");
                                String exp = vars.get("exponent");
                                String pass = vars.get("password");
                                String encPass = "";
                
                                JmeterPKCS1Encryption pkcs = new JmeterPKCS1Encryption();
                                encPass = pkcs.createPublicKeyAndPKCSEncrypt(pass, mod, exp);
                                SampleResult.setResponseData(encPass);
                                vars.put("encryptedPassword",encPass);
                }
                catch (Exception e)
                {
                                e.printStackTrace();
                }
 ```
