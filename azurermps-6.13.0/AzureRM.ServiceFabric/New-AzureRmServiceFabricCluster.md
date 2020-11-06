---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/new-azurermservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/New-AzureRmServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/New-AzureRmServiceFabricCluster.md
ms.openlocfilehash: 87fb451028fb0e345bd8748573424cf33066e52b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454555"
---
# <span data-ttu-id="c10f3-101">New-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="c10f3-101">New-AzureRmServiceFabricCluster</span></span>

## <span data-ttu-id="c10f3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c10f3-102">SYNOPSIS</span></span>
<span data-ttu-id="c10f3-103">這個命令會使用您提供的憑證或系統產生的自我簽署憑證來設定新的服務結構群集。</span><span class="sxs-lookup"><span data-stu-id="c10f3-103">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="c10f3-104">它可以使用您所提供的預設範本或自訂範本。</span><span class="sxs-lookup"><span data-stu-id="c10f3-104">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="c10f3-105">您可以選擇將自行簽署的憑證匯出到哪個資料夾，或稍後從金鑰電子倉庫將其回遷。</span><span class="sxs-lookup"><span data-stu-id="c10f3-105">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c10f3-106">句法</span><span class="sxs-lookup"><span data-stu-id="c10f3-106">SYNTAX</span></span>

### <span data-ttu-id="c10f3-107">ByDefaultArmTemplate (預設) </span><span class="sxs-lookup"><span data-stu-id="c10f3-107">ByDefaultArmTemplate (Default)</span></span>
```
New-AzureRmServiceFabricCluster [-ResourceGroupName] <String> [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>]
 -Location <String> [-Name <String>] [-VmUserName <String>] [-ClusterSize <Int32>]
 [-CertificateSubjectName <String>] -VmPassword <SecureString> [-OS <OperatingSystem>] [-VmSku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c10f3-108">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="c10f3-108">ByExistingKeyVault</span></span>
```
New-AzureRmServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-VmPassword <SecureString>] -SecretIdentifier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c10f3-109">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="c10f3-109">ByNewPfxAndVaultName</span></span>
```
New-AzureRmServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-CertificateOutputFolder <String>] [-CertificatePassword <SecureString>] [-KeyVaultResouceGroupName <String>]
 [-KeyVaultName <String>] [-CertificateSubjectName <String>] [-VmPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c10f3-110">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="c10f3-110">ByExistingPfxAndVaultName</span></span>
```
New-AzureRmServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 -CertificateFile <String> [-CertificatePassword <SecureString>] [-SecondaryCertificateFile <String>]
 [-SecondaryCertificatePassword <SecureString>] [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>]
 [-VmPassword <SecureString>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c10f3-111">說明</span><span class="sxs-lookup"><span data-stu-id="c10f3-111">DESCRIPTION</span></span>
<span data-ttu-id="c10f3-112">**新的-AzureRmServiceFabricCluster** 命令會使用您所提供的憑證或系統產生的自我簽署憑證來設定新的服務結構群集。</span><span class="sxs-lookup"><span data-stu-id="c10f3-112">The **New-AzureRmServiceFabricCluster** command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="c10f3-113">使用的範本可以是您提供的預設範本或自訂範本。</span><span class="sxs-lookup"><span data-stu-id="c10f3-113">The template used can be a default template or a custom template that you provide.</span></span> <span data-ttu-id="c10f3-114">您可以選擇指定要匯出自簽章憑證的資料夾，或稍後從金鑰保存庫回遷。</span><span class="sxs-lookup"><span data-stu-id="c10f3-114">You have the option of specifying a folder to export the self-signed certificates or fetching them later from the key vault.</span></span>
<span data-ttu-id="c10f3-115">如果您要指定自訂範本和參數檔案，則不需要在參數檔案中提供憑證資訊，系統就會填入這些參數。</span><span class="sxs-lookup"><span data-stu-id="c10f3-115">If you are specifying a custom template and parameter file, you don't need to provide the certificate information in the parameter file, the system will populate these parameters.</span></span>
<span data-ttu-id="c10f3-116">下面將詳細說明四個選項。</span><span class="sxs-lookup"><span data-stu-id="c10f3-116">The four options are detailed below.</span></span> <span data-ttu-id="c10f3-117">向下滾動，以取得每個參數的說明。</span><span class="sxs-lookup"><span data-stu-id="c10f3-117">Scroll down for explanations of each of the parameters.</span></span>

## <span data-ttu-id="c10f3-118">示例</span><span class="sxs-lookup"><span data-stu-id="c10f3-118">EXAMPLES</span></span>

### <span data-ttu-id="c10f3-119">範例1：只指定群集大小、cert 受領人名稱，以及要部署群集的作業系統。</span><span class="sxs-lookup"><span data-stu-id="c10f3-119">Example 1: Specify only the cluster size, the cert subject name, and the OS to deploy a cluster.</span></span>
```
$pass="Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$RGname="test01"
$clusterloc="SouthCentralUS"
$subname="{0}.{1}.cloudapp.azure.com" -f $RGname, $clusterloc
$pfxfolder="c:\certs"

Write-Output "Create cluster in '$clusterloc' with cert subject name '$subname' and cert output path '$pfxfolder'"

New-AzureRmServiceFabricCluster -ResourceGroupName $RGname -Location $clusterloc -ClusterSize 5 -VmPassword $pass -CertificateSubjectName $subname -CertificateOutputFolder $pfxfolder -CertificatePassword $pass -OS WindowsServer2016Datacenter
```

<span data-ttu-id="c10f3-120">這個命令只會指定群集大小、cert 受領人名稱，以及作業系統來部署群集。</span><span class="sxs-lookup"><span data-stu-id="c10f3-120">This command specifies only the cluster size, the cert subject name, and the OS to deploy a cluster.</span></span>

### <span data-ttu-id="c10f3-121">範例2：在主要電子倉庫中指定現有的憑證資源，以及可供您部署群集的自訂範本</span><span class="sxs-lookup"><span data-stu-id="c10f3-121">Example 2: Specify an existing Certificate resource in a key vault and a custom template to deploy a cluster</span></span>
```
$RGname="test20"
$templateParmfile="C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile="C:\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"
$secretId="https://test1.vault.azure.net:443/secrets/testcertificate4/56ec774dc61a462bbc645ffc9b4b225f"

New-AzureRmServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -SecretIdentifier $secretId
```

<span data-ttu-id="c10f3-122">這個命令會指定主要電子倉庫中現有的憑證資源，以及用來部署群集的自訂範本。</span><span class="sxs-lookup"><span data-stu-id="c10f3-122">This command specifies an existing Certificate resource in a key vault and a custom template to deploy a cluster.</span></span>

### <span data-ttu-id="c10f3-123">範例3：使用自訂範本建立新的群集。</span><span class="sxs-lookup"><span data-stu-id="c10f3-123">Example 3: Create a new cluster using a custom template.</span></span> <span data-ttu-id="c10f3-124">為主要保存庫指定不同的資源組名稱，並將系統上傳新憑證給它</span><span class="sxs-lookup"><span data-stu-id="c10f3-124">Specify a different resource group name for the key vault and have the system upload a new certificate to it</span></span>
```
$pass="Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$RGname="test20"
$keyVaultRG="test20kvrg"
$keyVault="test20kv"
$clusterloc="SouthCentralUS"
$subname="{0}.{1}.$clusterloc.cloudapp.azure.com" -f $RGName, $clusterloc
$pfxfolder="~\Documents"
$templateParmfile="C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile="C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"

New-AzureRmServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -CertificateOutputFolder $pfxfolder -CertificatePassword $pass -KeyVaultResouceGroupName $keyVaultRG  -KeyVaultName $keyVault -CertificateSubjectName $subname
```

<span data-ttu-id="c10f3-125">這個命令會使用自訂範本來建立新的群集。</span><span class="sxs-lookup"><span data-stu-id="c10f3-125">This command creates a new cluster using a custom template.</span></span> <span data-ttu-id="c10f3-126">為主要保存庫指定不同的資源組名稱，並將系統上傳新憑證給它</span><span class="sxs-lookup"><span data-stu-id="c10f3-126">Specify a different resource group name for the key vault and have the system upload a new certificate to it</span></span>

### <span data-ttu-id="c10f3-127">範例4：攜帶您自己的憑證和自訂範本，並建立新的群集</span><span class="sxs-lookup"><span data-stu-id="c10f3-127">Example 4: Bring your own Certificate and custom template and create a new cluster</span></span>
```
$pass="Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$RGname="test20"
$keyVaultRG="test20kvrg"
$keyVault="test20kv"
$pfxsourcefile="c:\Mycertificates\my2017Prodcert.pfx"
$templateParmfile="~\Documents\GitHub\azure-quickstart-templates-parms\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile="~\GitHub\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"

New-AzureRmServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -CertificateFile $pfxsourcefile -CertificatePassword $pass -KeyVaultResouceGroupName $keyVaultRG -KeyVaultName $keyVault
```

<span data-ttu-id="c10f3-128">這個命令可讓您攜帶自己的憑證和自訂範本，並建立新的群集。</span><span class="sxs-lookup"><span data-stu-id="c10f3-128">This command will let you bring your own Certificate and custom template and create a new cluster.</span></span>

## <span data-ttu-id="c10f3-129">參數</span><span class="sxs-lookup"><span data-stu-id="c10f3-129">PARAMETERS</span></span>

### <span data-ttu-id="c10f3-130">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="c10f3-130">-CertificateFile</span></span>
<span data-ttu-id="c10f3-131">主要群集憑證的現有憑證檔路徑。</span><span class="sxs-lookup"><span data-stu-id="c10f3-131">The existing certificate file path for the primary cluster certificate.</span></span>

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

### <span data-ttu-id="c10f3-132">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="c10f3-132">-CertificateOutputFolder</span></span>
<span data-ttu-id="c10f3-133">要建立之新憑證檔案的資料夾。</span><span class="sxs-lookup"><span data-stu-id="c10f3-133">The folder of the new certificate file to be created.</span></span>

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

### <span data-ttu-id="c10f3-134">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="c10f3-134">-CertificatePassword</span></span>
<span data-ttu-id="c10f3-135">憑證檔案的密碼。</span><span class="sxs-lookup"><span data-stu-id="c10f3-135">The password of the certificate file.</span></span>

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

### <span data-ttu-id="c10f3-136">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="c10f3-136">-CertificateSubjectName</span></span>
<span data-ttu-id="c10f3-137">要建立之憑證的受領人名稱。</span><span class="sxs-lookup"><span data-stu-id="c10f3-137">The subject name of the certificate to be created.</span></span>

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

### <span data-ttu-id="c10f3-138">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="c10f3-138">-ClusterSize</span></span>
<span data-ttu-id="c10f3-139">群集中的節點數。</span><span class="sxs-lookup"><span data-stu-id="c10f3-139">The number of nodes in the cluster.</span></span> <span data-ttu-id="c10f3-140">預設值為5個節點。</span><span class="sxs-lookup"><span data-stu-id="c10f3-140">Default are 5 nodes.</span></span>

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

### <span data-ttu-id="c10f3-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c10f3-141">-DefaultProfile</span></span>
<span data-ttu-id="c10f3-142">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c10f3-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c10f3-143">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="c10f3-143">-KeyVaultName</span></span>
<span data-ttu-id="c10f3-144">Azure 金鑰保存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="c10f3-144">Azure key vault name.</span></span> <span data-ttu-id="c10f3-145">如果未指定，它將預設為資源組名。</span><span class="sxs-lookup"><span data-stu-id="c10f3-145">If not given, it will be defaulted to the resource group name.</span></span>

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

### <span data-ttu-id="c10f3-146">-KeyVaultResouceGroupName</span><span class="sxs-lookup"><span data-stu-id="c10f3-146">-KeyVaultResouceGroupName</span></span>
<span data-ttu-id="c10f3-147">Azure 金鑰電子倉庫資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="c10f3-147">Azure key vault resource group name.</span></span> <span data-ttu-id="c10f3-148">如果未指定，它將預設為 [資源] 群組名稱。</span><span class="sxs-lookup"><span data-stu-id="c10f3-148">If not given, it will be defaulted to resource group name.</span></span>

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

### <span data-ttu-id="c10f3-149">-位置</span><span class="sxs-lookup"><span data-stu-id="c10f3-149">-Location</span></span>
<span data-ttu-id="c10f3-150">資源群組位置。</span><span class="sxs-lookup"><span data-stu-id="c10f3-150">The resource group location.</span></span>

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

### <span data-ttu-id="c10f3-151">-名稱</span><span class="sxs-lookup"><span data-stu-id="c10f3-151">-Name</span></span>
<span data-ttu-id="c10f3-152">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="c10f3-152">Specify the name of the cluster.</span></span> <span data-ttu-id="c10f3-153">如果未指定，它將與資源組名稱相同。</span><span class="sxs-lookup"><span data-stu-id="c10f3-153">If not given, it will be same as resource group name.</span></span>

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

### <span data-ttu-id="c10f3-154">-OS</span><span class="sxs-lookup"><span data-stu-id="c10f3-154">-OS</span></span>
<span data-ttu-id="c10f3-155">組成群集之 Vm 的作業系統。</span><span class="sxs-lookup"><span data-stu-id="c10f3-155">The Operating System of the VMs that make up the cluster.</span></span>

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

### <span data-ttu-id="c10f3-156">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="c10f3-156">-ParameterFile</span></span>
<span data-ttu-id="c10f3-157">範本參數檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="c10f3-157">The path to the template parameter file.</span></span>

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

### <span data-ttu-id="c10f3-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c10f3-158">-ResourceGroupName</span></span>
<span data-ttu-id="c10f3-159">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c10f3-159">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="c10f3-160">-SecondaryCertificateFile</span><span class="sxs-lookup"><span data-stu-id="c10f3-160">-SecondaryCertificateFile</span></span>
<span data-ttu-id="c10f3-161">次要群集憑證的現有憑證檔路徑。</span><span class="sxs-lookup"><span data-stu-id="c10f3-161">The existing certificate file path for the secondary cluster certificate.</span></span>

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

### <span data-ttu-id="c10f3-162">-SecondaryCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="c10f3-162">-SecondaryCertificatePassword</span></span>
<span data-ttu-id="c10f3-163">憑證檔案的密碼。</span><span class="sxs-lookup"><span data-stu-id="c10f3-163">The password of the certificate file.</span></span>

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

### <span data-ttu-id="c10f3-164">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="c10f3-164">-SecretIdentifier</span></span>
<span data-ttu-id="c10f3-165">現有的 Azure 金鑰保存庫機密 URL，例如： " https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f "。</span><span class="sxs-lookup"><span data-stu-id="c10f3-165">The existing Azure key vault secret URL, for example: 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'.</span></span>

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

### <span data-ttu-id="c10f3-166">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="c10f3-166">-TemplateFile</span></span>
<span data-ttu-id="c10f3-167">範本檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="c10f3-167">The path to the template file.</span></span>

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

### <span data-ttu-id="c10f3-168">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="c10f3-168">-VmPassword</span></span>
<span data-ttu-id="c10f3-169">Vm 的密碼。</span><span class="sxs-lookup"><span data-stu-id="c10f3-169">The password of the Vm.</span></span>

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

```yaml
Type: System.Security.SecureString
Parameter Sets: ByExistingKeyVault, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c10f3-170">-VmSku</span><span class="sxs-lookup"><span data-stu-id="c10f3-170">-VmSku</span></span>
<span data-ttu-id="c10f3-171">Vm Sku。</span><span class="sxs-lookup"><span data-stu-id="c10f3-171">The Vm Sku.</span></span>

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

### <span data-ttu-id="c10f3-172">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="c10f3-172">-VmUserName</span></span>
<span data-ttu-id="c10f3-173">要記錄到 Vm 的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="c10f3-173">The user name for logging to Vm.</span></span>

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

### <span data-ttu-id="c10f3-174">-確認</span><span class="sxs-lookup"><span data-stu-id="c10f3-174">-Confirm</span></span>
<span data-ttu-id="c10f3-175">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c10f3-175">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c10f3-176">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c10f3-176">-WhatIf</span></span>
<span data-ttu-id="c10f3-177">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c10f3-177">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c10f3-178">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c10f3-178">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c10f3-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c10f3-179">CommonParameters</span></span>
<span data-ttu-id="c10f3-180">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c10f3-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c10f3-181">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c10f3-181">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c10f3-182">輸入</span><span class="sxs-lookup"><span data-stu-id="c10f3-182">INPUTS</span></span>

### <span data-ttu-id="c10f3-183">System.object</span><span class="sxs-lookup"><span data-stu-id="c10f3-183">System.String</span></span>
<span data-ttu-id="c10f3-184">參數： CertificateFile (ByValue) )  (、CertificateSubjectName (ByValue) 、KeyVaultName (ByValue) 、KeyVaultResouceGroupName (ByValue) 、ByValue (ByValue) 、ParameterFile (ByValue) 、SecondaryCertificateFile (ByValue) 、SecretIdentifier (ByValue) 、TemplateFile (ByValue) 、VmUserName (ByValue) 、 () 、</span><span class="sxs-lookup"><span data-stu-id="c10f3-184">Parameters: CertificateFile (ByValue), CertificateOutputFolder (ByValue), CertificateSubjectName (ByValue), KeyVaultName (ByValue), KeyVaultResouceGroupName (ByValue), Location (ByValue), Name (ByValue), ParameterFile (ByValue), SecondaryCertificateFile (ByValue), SecretIdentifier (ByValue), TemplateFile (ByValue), VmUserName (ByValue)</span></span>

### <span data-ttu-id="c10f3-185">SecureString</span><span class="sxs-lookup"><span data-stu-id="c10f3-185">System.Security.SecureString</span></span>
<span data-ttu-id="c10f3-186">參數： CertificatePassword (ByValue) ，SecondaryCertificatePassword (ByValue) </span><span class="sxs-lookup"><span data-stu-id="c10f3-186">Parameters: CertificatePassword (ByValue), SecondaryCertificatePassword (ByValue)</span></span>

### <span data-ttu-id="c10f3-187">System.object</span><span class="sxs-lookup"><span data-stu-id="c10f3-187">System.Int32</span></span>
<span data-ttu-id="c10f3-188">參數： ClusterSize (ByValue) </span><span class="sxs-lookup"><span data-stu-id="c10f3-188">Parameters: ClusterSize (ByValue)</span></span>

### <span data-ttu-id="c10f3-189">[ServiceFabric] 的作業系統</span><span class="sxs-lookup"><span data-stu-id="c10f3-189">Microsoft.Azure.Commands.ServiceFabric.Models.OperatingSystem</span></span>

## <span data-ttu-id="c10f3-190">輸出</span><span class="sxs-lookup"><span data-stu-id="c10f3-190">OUTPUTS</span></span>

### <span data-ttu-id="c10f3-191">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span><span class="sxs-lookup"><span data-stu-id="c10f3-191">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span></span>

## <span data-ttu-id="c10f3-192">筆記</span><span class="sxs-lookup"><span data-stu-id="c10f3-192">NOTES</span></span>

## <span data-ttu-id="c10f3-193">相關連結</span><span class="sxs-lookup"><span data-stu-id="c10f3-193">RELATED LINKS</span></span>
