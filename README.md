<h3>Step 1: Installing Active Directory</h3>

- Access DC-1 and install Active Directory Domain Services (AD DS)

- Configure it as a Domain Controller (DC) by creating a new forest (e.g., mydomain.com—you can choose any name, but be sure to remember it) 

- When  choosing the password make sure your remember it, I recommend using “Password1”

- Make sure the “Create DNS delegation” box us unchecked

- Restart the system, then log back into DC-1 using the credentials: mydomain.com\DC-1

 ![Image](https://github.com/user-attachments/assets/d283c54f-63eb-467d-ab0e-72113998a843)

![Image](https://github.com/user-attachments/assets/4f96646b-1b7b-4585-abe6-9e0cd1645cbb)

![Image](https://github.com/user-attachments/assets/1849946c-ae74-46ff-8c5f-9669c20cdfdd)

![Image](https://github.com/user-attachments/assets/4ae4bf4f-ef4a-46a1-b06a-bd4e14bb9b3a)

![Image](https://github.com/user-attachments/assets/e592e919-6815-4adc-9c39-ba45972eda07)

![Image](https://github.com/user-attachments/assets/910e3e8a-82e3-457d-9eec-efdaa9949948)





<h3>Step 2: Creating OU Folders in DC-1</h3>

- In Active Directory Users and Computers (ADUC), create an Organizational Unit (OU) named "_EMPLOYEES".

- Add another OU called "_ADMINS".

- Create a new user named "Jane Doe" with the username "jane_admin", using the same password (Password1).

- Assign jane_admin to the "Domain Admins" security group.

- Log out or disconnect from DC-1, then log back in as "mydomain.com\jane_admin"

- Got to System Setting - “Rename this PC” -  Change 
- In the  “Member of” box change it to mydomain.com

- Login to the Domain Controller and verify Client-1 shows up in ADUC

![Image](https://github.com/user-attachments/assets/7c47262a-665a-4ec4-8e17-62b2c5fa4754)

![Image](https://github.com/user-attachments/assets/d6ade182-2c06-40cc-8211-2cc37a2bb688)

![Image](https://github.com/user-attachments/assets/a2a5bcf5-0327-46c8-92d5-d66e533a2bac)

![Image](https://github.com/user-attachments/assets/87d65946-d1e6-44e3-a8dd-c36964d6cccf)

![Image](https://github.com/user-attachments/assets/94b69f60-96d6-4dca-b654-02ead2d618b8)

![Image](https://github.com/user-attachments/assets/4df41702-2a55-4043-881e-d418ab2614cb)

![Image](https://github.com/user-attachments/assets/4c060bde-a7ca-44ae-851e-497c61560dbd)

![Image](https://github.com/user-attachments/assets/9724bdd3-0d46-4fb7-9213-04dd525e6bae)





<h3>Step 3: Enabling access in Client-1</h3>

- Sign in to Client-1 using mydomain.com\jane_admin.

- Open System Properties and navigate to the Remote Desktop settings.

- Enable access for domain users to connect via Remote Desktop.

- You can now access Client-1 using a standard, non-administrative user account.

- In a real-world scenario, this would typically be managed using Group Policy to apply the settings across multiple systems efficiently (potentially covered in a future lab).


![Image](https://github.com/user-attachments/assets/52e6cff6-d361-47af-8797-96922f255875)

![Image](https://github.com/user-attachments/assets/1aba628b-3dfe-48c8-b0e1-e9cc76306f52)



<h3>Step 4: Creating users in Power shell</h3>

- Login to DC-1 as jane_admin

- Open PowerShell_ise as an administrator

- Create a new File and paste the contents of the script into it

- Run the script and observe the accounts being created

- When finished, open ADUC and observe the accounts in the appropriate OU　(_EMPLOYEES)
       attempt to log into Client-1 with one of the accounts (take note of the password in the script)



![Image](https://github.com/user-attachments/assets/ad0ebe3f-cf87-4485-96fe-9337119aa7aa)

![Image](https://github.com/user-attachments/assets/4dea7d6c-17b4-4c34-b78c-58c9b0a94095)

![Image](https://github.com/user-attachments/assets/a3874d16-9979-4fe5-a8ed-64e627b396ce)

![Image](https://github.com/user-attachments/assets/c5a35234-ce34-4f96-970a-2fdb8b8941a6)

![Image](https://github.com/user-attachments/assets/199dc402-e4d3-4820-92d8-50e88461b97c)

![Image](https://github.com/user-attachments/assets/5f7c4624-4067-4f56-925e-4a8e6a7eeedf)
