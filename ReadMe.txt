Data Source=.\SQLEXPRESS;AttachDbFilename="C:\Projects\DevOps\Employee Info Starter Kit\C#\App_Data\Database.mdf";Integrated Security=True;User Instance=True
Data Source=DESKTOP-JHTN090\FOZIL;Initial Catalog=EmployeeInfo_SK_5_0;Integrated Security=True
Data Source=DESKTOP-JHTN090\FOZIL;AttachDbFilename="C:\Projects\DevOps\Employee Info Starter Kit\C#\App_Data\Database.mdf";Integrated Security=True


"C:\Program Files\IIS\Microsoft Web Deploy V3\msdeploy.exe" -verb:sync -source:iisApp="E:\Jenkins\jobs\NotARealJobName\workspace" -dest:iisApp="MyWebSite/MyWebApp",ComputerName="https://MyServer:8172/MsDeploy.axd",UserName=MyDomain\svcMyService,Password="NotARealPassword" -allowUntrusted 
"C:\Program Files\IIS\Microsoft Web Deploy V3\msdeploy.exe" -verb:sync -source:iisApp="C:\Projects\DevOps\ASP.NET MVC CRUD Operation using Entity Framework Code First Approach\C#" -dest:iisApp="Default Web Site/eisk",ComputerName="http://DESKTOP-JHTN090/MsDeploy.axd",UserName=DESKTOP-JHTN090\fozil,Password="police" -allowUntrusted 

"C:\Program Files\IIS\Microsoft Web Deploy V3\msdeploy.exe" -verb:sync -source:iisApp=”C:\Projects\DevOps\ASP.NET MVC CRUD Operation using Entity Framework Code First Approach\C#” 
-dest:package=C:\Projects\eisk.zip

"C:\Program Files\IIS\Microsoft Web Deploy V3\msdeploy.exe" -verb:sync -source:package="C:\Projects\eisk.zip" -dest:iisApp="localhost/eisk", -wmsvc="localhost", username="DESKTOP-JHTN090\fozil", password="police", skipAppCreation=false -allowUntrusted=true

msdeploy.exe -verb:sync -source:package=”c:\Test_site\testsite.zip” -dest:iisApp=”domain.com/subfolder01″,
wmsvc=domain.com,username=IIS_username,password=IIS_password,
skipAppCreation=false -allowUntrusted=true


"C:\Program Files (x86)\Microsoft Visual Studio\2017\Community\MSBuild\15.0\Bin\MSBuild.exe" 

-- Command to Build and Publish
msbuild "C:\Projects\DevOps\ASP.NET MVC CRUD Operation using Entity Framework Code First Approach\C#\MVC_CRUD_Using_Entity_Framework_Code_First\MVC_CRUD_Using_Entity_Framework_Code_First.csproj" 
 /p:DeployOnBuild=true /p:PublishProfile="C:\Projects\DevOps\ASP.NET MVC CRUD Operation using Entity Framework Code First Approach\C#\MVC_CRUD_Using_Entity_Framework_Code_First\Properties\PublishProfiles\IIS-Debug-Profile.pubxml"