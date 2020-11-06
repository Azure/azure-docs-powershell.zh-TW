---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/New-AzureRmServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/New-AzureRmServiceFabricCluster.md
ms.openlocfilehash: c1f6dea6c4fb103107a052d64a82ad81eafdb8c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456379"
---
# <span data-ttu-id="9a826-101">New-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="9a826-101">New-AzureRmServiceFabricCluster</span></span>

## <span data-ttu-id="9a826-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9a826-102">SYNOPSIS</span></span>
<span data-ttu-id="9a826-103">這個命令會使用您提供的憑證或系統產生的自我簽署憑證來設定新的服務結構群集。</span><span class="sxs-lookup"><span data-stu-id="9a826-103">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="9a826-104">它可以使用您所提供的預設範本或自訂範本。</span><span class="sxs-lookup"><span data-stu-id="9a826-104">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="9a826-105">您可以選擇將自行簽署的憑證匯出到哪個資料夾，或稍後從金鑰電子倉庫將其回遷。</span><span class="sxs-lookup"><span data-stu-id="9a826-105">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a826-106">句法</span><span class="sxs-lookup"><span data-stu-id="9a826-106">SYNTAX</span></span>

### <span data-ttu-id="9a826-107">ByDefaultArmTemplate (預設) </span><span class="sxs-lookup"><span data-stu-id="9a826-107">ByDefaultArmTemplate (Default)</span></span>
```
New-AzureRmServiceFabricCluster [-ResourceGroupName] <String> [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>]
 -Location <String> [-Name <String>] [-VmUserName <String>] [-ClusterSize <Int32>]
 [-CertificateSubjectName <String>] -VmPassword <SecureString> [-OS <OperatingSystem>] [-VmSku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a826-108">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="9a826-108">ByExistingKeyVault</span></span>
```
New-AzureRmServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 -SecretIdentifier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9a826-109">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="9a826-109">ByNewPfxAndVaultName</span></span>
```
New-AzureRmServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-CertificateOutputFolder <String>] [-CertificatePassword <SecureString>] [-KeyVaultResouceGroupName <String>]
 [-KeyVaultName <String>] [-CertificateSubjectName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a826-110">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="9a826-110">ByExistingPfxAndVaultName</span></span>
```
New-AzureRmServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 -CertificateFile <String> [-CertificatePassword <SecureString>] [-SecondaryCertificateFile <String>]
 [-SecondaryCertificatePassword <SecureString>] [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a826-111">說明</span><span class="sxs-lookup"><span data-stu-id="9a826-111">DESCRIPTION</span></span>
<span data-ttu-id="9a826-112">**新的-AzureRmServiceFabricCluster** 命令會使用您所提供的憑證或系統產生的自我簽署憑證來設定新的服務結構群集。</span><span class="sxs-lookup"><span data-stu-id="9a826-112">The **New-AzureRmServiceFabricCluster** command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="9a826-113">使用的範本可以是您提供的預設範本或自訂範本。</span><span class="sxs-lookup"><span data-stu-id="9a826-113">The template used can be a default template or a custom template that you provide.</span></span> <span data-ttu-id="9a826-114">您可以選擇指定要匯出自簽章憑證的資料夾，或稍後從金鑰保存庫回遷。</span><span class="sxs-lookup"><span data-stu-id="9a826-114">You have the option of specifying a folder to export the self-signed certificates or fetching them later from the key vault.</span></span>

<span data-ttu-id="9a826-115">如果您要指定自訂範本和參數檔案，則不需要在參數檔案中提供憑證資訊，系統就會填入這些參數。</span><span class="sxs-lookup"><span data-stu-id="9a826-115">If you are specifying a custom template and parameter file, you don't need to provide the certificate information in the parameter file, the system will populate these parameters.</span></span>

<span data-ttu-id="9a826-116">下面將詳細說明四個選項。</span><span class="sxs-lookup"><span data-stu-id="9a826-116">The four options are detailed below.</span></span> <span data-ttu-id="9a826-117">向下滾動，以取得每個參數的說明。</span><span class="sxs-lookup"><span data-stu-id="9a826-117">Scroll down for explanations of each of the parameters.</span></span>

## <span data-ttu-id="9a826-118">示例</span><span class="sxs-lookup"><span data-stu-id="9a826-118">EXAMPLES</span></span>

### <span data-ttu-id="9a826-119">範例1：只指定群集大小、cert 受領人名稱，以及要部署群集的作業系統。</span><span class="sxs-lookup"><span data-stu-id="9a826-119">Example 1: Specify only the cluster size, the cert subject name, and the OS to deploy a cluster.</span></span>
```
$pass="Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$RGname="test01"
$clusterloc="SouthCentralUS"
$subname="{0}.{1}.cloudapp.azure.com" -f $RGname, $clusterloc
$pfxfolder="~\Documents"

Write-Output "create cluster in " $clusterloc "subject name for cert " $subname "and output the cert into " $pfxfolder

New-AzureRmServiceFabricCluster -ResourceGroupName $RGname -Location $clusterloc -ClusterSize 3 -VmPassword $pwd -CertificateSubjectName $subname -CertificateOutputFolder $pfxfolder -CertificatePassword $pwd -OS WindowsServer2016Datacenter
```

<span data-ttu-id="9a826-120">這個命令只會指定群集大小、cert 受領人名稱，以及作業系統來部署群集。</span><span class="sxs-lookup"><span data-stu-id="9a826-120">This command specifies only the cluster size, the cert subject name, and the OS to deploy a cluster.</span></span>

### <span data-ttu-id="9a826-121">範例2：在主要電子倉庫中指定現有的憑證資源，以及可供您部署群集的自訂範本</span><span class="sxs-lookup"><span data-stu-id="9a826-121">Example 2: Specify an existing Certificate resource in a key vault and a custom template to deploy a cluster</span></span>
```
$RGname="test20"
$templateParmfile="C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile="C:\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"
$secertId="https://test1.vault.azure.net:443/secrets/testcertificate4/56ec774dc61a462bbc645ffc9b4b225f"

New-AzureRmServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -SecretIdentifier $secertId
```

<span data-ttu-id="9a826-122">這個命令會指定主要電子倉庫中現有的憑證資源，以及用來部署群集的自訂範本。</span><span class="sxs-lookup"><span data-stu-id="9a826-122">This command specifies an existing Certificate resource in a key vault and a custom template to deploy a cluster.</span></span>

### <span data-ttu-id="9a826-123">範例3：使用自訂範本建立新的群集。</span><span class="sxs-lookup"><span data-stu-id="9a826-123">Example 3: Create a new cluster using a custom template.</span></span> <span data-ttu-id="9a826-124">為金鑰保存庫指定不同的 RG 名稱，並讓系統將憑證上傳給它</span><span class="sxs-lookup"><span data-stu-id="9a826-124">Specify the different RG name for the key vault and have the system upload the certificate to it</span></span>
```
$pwd="Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$RGname="test20"
$keyVaultRG="test20kvrg"
$keyVault="test20kv"
$clusterloc="SouthCentralUS"
$subname="{0}.{1}.$clusterloc.cloudapp.azure.com" -f $RGName, $clusterloc
$pfxfolder="~\Documents"
$templateParmfile="C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile="C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"
$secertId="https://test1.vault.azure.net:443/secrets/testcertificate4/55ec7c4dc61a462bbc645ffc9b4b225f"
$thumprint="C2D7E11DD35153A702A51D10A424A3014B9B6E8B"

New-AzureRmServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -CertificateOutputFolder $pfxfolder -CertificatePassword $pwd -KeyVaultResouceGroupName $keyVaultRG  -KeyVaultName $keyVault -CertificateSubjectName $subname
```

<span data-ttu-id="9a826-125">這個命令會使用自訂範本來建立新的群集。</span><span class="sxs-lookup"><span data-stu-id="9a826-125">This command creates a new cluster using a custom template.</span></span> <span data-ttu-id="9a826-126">指定主要電子倉庫的不同 RG 名稱，並讓系統上傳證書。</span><span class="sxs-lookup"><span data-stu-id="9a826-126">Specify the different RG name for the key vault and have the system upload the certificate to it.</span></span>

### <span data-ttu-id="9a826-127">範例4：攜帶您自己的憑證和自訂範本，並建立新的群集</span><span class="sxs-lookup"><span data-stu-id="9a826-127">Example 4: Bring your own Certificate and custom template and create a new cluster</span></span>
```
$certPwd="Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$RGname="test20"
$keyVaultRG="test20kvrg"
$keyVault="test20kv"
$clusterloc="SouthCentralUS"
$pfxsourcefile="c:\Mycertificates\my2017Prodcert.pfx"
$templateParmfile="~\Documents\GitHub\azure-quickstart-templates-parms\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile="~\GitHub\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"

New-AzureRmServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -CertificateSourceFile $pfxsourcefile -CertificatePassword $certpwd -KeyVaultResouceGroupName $keyVaultRG -KeyVaultName $keyVault
```

<span data-ttu-id="9a826-128">這個命令可讓您攜帶自己的憑證和自訂範本，並建立新的群集。</span><span class="sxs-lookup"><span data-stu-id="9a826-128">This command will let you bring your own Certificate and custom template and create a new cluster.</span></span>

## <span data-ttu-id="9a826-129">參數</span><span class="sxs-lookup"><span data-stu-id="9a826-129">PARAMETERS</span></span>

### <span data-ttu-id="9a826-130">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="9a826-130">-CertificateFile</span></span>
<span data-ttu-id="9a826-131">主要群集憑證的現有憑證檔路徑。</span><span class="sxs-lookup"><span data-stu-id="9a826-131">The existing certificate file path for the primary cluster certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingPfxAndVaultName
Aliases: Source

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a826-132">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="9a826-132">-CertificateOutputFolder</span></span>
<span data-ttu-id="9a826-133">要建立之新憑證檔案的資料夾。</span><span class="sxs-lookup"><span data-stu-id="9a826-133">The folder of the new certificate file to be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName
Aliases: Destination

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a826-134">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="9a826-134">-CertificatePassword</span></span>
<span data-ttu-id="9a826-135">憑證檔案的密碼。</span><span class="sxs-lookup"><span data-stu-id="9a826-135">The password of the certificate file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: CertPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a826-136">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="9a826-136">-CertificateSubjectName</span></span>
<span data-ttu-id="9a826-137">要建立之憑證的受領人名稱。</span><span class="sxs-lookup"><span data-stu-id="9a826-137">The subject name of the certificate to be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName
Aliases: Subject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a826-138">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="9a826-138">-ClusterSize</span></span>
<span data-ttu-id="9a826-139">群集中的節點數。</span><span class="sxs-lookup"><span data-stu-id="9a826-139">The number of nodes in the cluster.</span></span> <span data-ttu-id="9a826-140">預設值為5個節點。</span><span class="sxs-lookup"><span data-stu-id="9a826-140">Default are 5 nodes.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByDefaultArmTemplate
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a826-141">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="9a826-141">-KeyVaultName</span></span>
<span data-ttu-id="9a826-142">Azure 金鑰保存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="9a826-142">Azure key vault name.</span></span> <span data-ttu-id="9a826-143">如果未指定，它將預設為資源組名。</span><span class="sxs-lookup"><span data-stu-id="9a826-143">If not given, it will be defaulted to the resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a826-144">-KeyVaultResouceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a826-144">-KeyVaultResouceGroupName</span></span>
<span data-ttu-id="9a826-145">Azure 金鑰電子倉庫資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="9a826-145">Azure key vault resource group name.</span></span> <span data-ttu-id="9a826-146">如果未指定，它將預設為 [資源] 群組名稱。</span><span class="sxs-lookup"><span data-stu-id="9a826-146">If not given, it will be defaulted to resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a826-147">-位置</span><span class="sxs-lookup"><span data-stu-id="9a826-147">-Location</span></span>
<span data-ttu-id="9a826-148">資源群組位置。</span><span class="sxs-lookup"><span data-stu-id="9a826-148">The resource group location.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a826-149">-名稱</span><span class="sxs-lookup"><span data-stu-id="9a826-149">-Name</span></span>
<span data-ttu-id="9a826-150">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="9a826-150">Specify the name of the cluster.</span></span> <span data-ttu-id="9a826-151">如果未指定，它將與資源組名稱相同。</span><span class="sxs-lookup"><span data-stu-id="9a826-151">If not given, it will be same as resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate
Aliases: ClusterName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a826-152">-OS</span><span class="sxs-lookup"><span data-stu-id="9a826-152">-OS</span></span>
<span data-ttu-id="9a826-153">組成群集之 Vm 的作業系統。</span><span class="sxs-lookup"><span data-stu-id="9a826-153">The Operating System of the VMs that make up the cluster.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.OperatingSystem
Parameter Sets: ByDefaultArmTemplate
Aliases: VmImage
Accepted values: WindowsServer2012R2Datacenter, WindowsServer2016Datacenter, WindowsServer2016DatacenterwithContainers, UbuntuServer1604

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a826-154">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="9a826-154">-ParameterFile</span></span>
<span data-ttu-id="9a826-155">範本參數檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="9a826-155">The path to the template parameter file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a826-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a826-156">-ResourceGroupName</span></span>
<span data-ttu-id="9a826-157">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9a826-157">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a826-158">-SecondaryCertificateFile</span><span class="sxs-lookup"><span data-stu-id="9a826-158">-SecondaryCertificateFile</span></span>
<span data-ttu-id="9a826-159">次要群集憑證的現有憑證檔路徑。</span><span class="sxs-lookup"><span data-stu-id="9a826-159">The existing certificate file path for the secondary cluster certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingPfxAndVaultName
Aliases: SecSource

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a826-160">-SecondaryCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="9a826-160">-SecondaryCertificatePassword</span></span>
<span data-ttu-id="9a826-161">憑證檔案的密碼。</span><span class="sxs-lookup"><span data-stu-id="9a826-161">The password of the certificate file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByExistingPfxAndVaultName
Aliases: SecCertPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a826-162">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="9a826-162">-SecretIdentifier</span></span>
<span data-ttu-id="9a826-163">現有的 Azure 金鑰保存庫機密 URL，例如： " https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f "。</span><span class="sxs-lookup"><span data-stu-id="9a826-163">The existing Azure key vault secret URL, for example: 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a826-164">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="9a826-164">-TemplateFile</span></span>
<span data-ttu-id="9a826-165">範本檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="9a826-165">The path to the template file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a826-166">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="9a826-166">-VmPassword</span></span>
<span data-ttu-id="9a826-167">Vm 的密碼。</span><span class="sxs-lookup"><span data-stu-id="9a826-167">The password of the Vm.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByDefaultArmTemplate
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a826-168">-VmSku</span><span class="sxs-lookup"><span data-stu-id="9a826-168">-VmSku</span></span>
<span data-ttu-id="9a826-169">Vm Sku。</span><span class="sxs-lookup"><span data-stu-id="9a826-169">The Vm Sku.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate
Aliases: Sku

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a826-170">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="9a826-170">-VmUserName</span></span>
<span data-ttu-id="9a826-171">要記錄到 Vm 的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="9a826-171">The user name for logging to Vm.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a826-172">-確認</span><span class="sxs-lookup"><span data-stu-id="9a826-172">-Confirm</span></span>
<span data-ttu-id="9a826-173">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9a826-173">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a826-174">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a826-174">-WhatIf</span></span>
<span data-ttu-id="9a826-175">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9a826-175">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9a826-176">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9a826-176">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a826-177">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a826-177">-DefaultProfile</span></span>
<span data-ttu-id="9a826-178">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9a826-178">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a826-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a826-179">CommonParameters</span></span>
<span data-ttu-id="9a826-180">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9a826-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a826-181">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9a826-181">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a826-182">輸入</span><span class="sxs-lookup"><span data-stu-id="9a826-182">INPUTS</span></span>

### <span data-ttu-id="9a826-183">System.object</span><span class="sxs-lookup"><span data-stu-id="9a826-183">System.String</span></span>
<span data-ttu-id="9a826-184">SecureString System. ServiceFabric......。</span><span class="sxs-lookup"><span data-stu-id="9a826-184">System.Security.SecureString System.Int32 Microsoft.Azure.Commands.ServiceFabric.Models.OperatingSystem</span></span>

## <span data-ttu-id="9a826-185">輸出</span><span class="sxs-lookup"><span data-stu-id="9a826-185">OUTPUTS</span></span>

### <span data-ttu-id="9a826-186">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span><span class="sxs-lookup"><span data-stu-id="9a826-186">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span></span>

## <span data-ttu-id="9a826-187">筆記</span><span class="sxs-lookup"><span data-stu-id="9a826-187">NOTES</span></span>

## <span data-ttu-id="9a826-188">相關連結</span><span class="sxs-lookup"><span data-stu-id="9a826-188">RELATED LINKS</span></span>

