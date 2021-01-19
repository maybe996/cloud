Clous9 환경 설정 및 Terraform 설정 

1. cloud9 
Cloud9 오른쪽 상단 설정마크 -> AWS Setting -> AWS managed temporary credentials off 설정 

2. Terraform 다운로드 (OS환경에 맞는 terraform download)
 sudo yum update
 wget https://releases.hashicorp.com/terraform/0.14.4/terraform_0.14.4_linux_amd64.zip
 sudo unzip *.zip

3. terraform 환경변수 설정 
sudo cp terraform /usr/bin
sudo chmod +x /usr/bin/terraform 
alias tr='/usr/bin/terraform'  

4. Cloud 9 환경 설정
1) Access key 확인 
AWS IAM사용자 ->보안자격증명 -> 액세스키 만들기 -> ID, Secret key 확인 

2) cloud9 
vi ~/.bashrc
echo "export AWS_ACCESS_KEY_ID=XXXXXX
echo "export AWS_SECRET_ACCESS_KEY=XXXXXXX
export PATH=$PATH:/bin:/usr/bin:/usr/local/bin

source ~./bashrc
