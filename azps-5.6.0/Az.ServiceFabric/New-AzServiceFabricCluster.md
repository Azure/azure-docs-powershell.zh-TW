---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/new-azservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricCluster.md
ms.openlocfilehash: b603087063a763d63f986afa7568160a6623a22b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903077"
---
# <span data-ttu-id="8aba2-101">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="8aba2-101">New-AzServiceFabricCluster</span></span>

## <span data-ttu-id="8aba2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8aba2-102">SYNOPSIS</span></span>

<span data-ttu-id="8aba2-103">此命令會使用您提供的憑證或系統產生的自我簽署憑證來設定新的服務結構組組。</span><span class="sxs-lookup"><span data-stu-id="8aba2-103">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="8aba2-104">它可以使用預設範本或您提供的自訂範本。</span><span class="sxs-lookup"><span data-stu-id="8aba2-104">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="8aba2-105">您可以選擇指定資料夾，將自我簽署憑證匯出至該憑證，或稍後從金鑰庫抓取。</span><span class="sxs-lookup"><span data-stu-id="8aba2-105">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span>

## <span data-ttu-id="8aba2-106">語法</span><span class="sxs-lookup"><span data-stu-id="8aba2-106">SYNTAX</span></span>

### <span data-ttu-id="8aba2-107">ByDefaultArmTemplate (預設) </span><span class="sxs-lookup"><span data-stu-id="8aba2-107">ByDefaultArmTemplate (Default)</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>]
 -Location <String> [-Name <String>] [-VmUserName <String>] [-ClusterSize <Int32>]
 [-CertificateSubjectName <String>] -VmPassword <SecureString> [-OS <OperatingSystem>] [-VmSku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8aba2-108">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="8aba2-108">ByExistingKeyVault</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>] [-VmPassword <SecureString>]
 -SecretIdentifier <String> [-Thumbprint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8aba2-109">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="8aba2-109">ByNewPfxAndVaultName</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-CertificateOutputFolder <String>] [-CertificatePassword <SecureString>]
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] [-CertificateSubjectName <String>]
 [-VmPassword <SecureString>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8aba2-110">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="8aba2-110">ByExistingPfxAndVaultName</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 -CertificateFile <String> [-CertificatePassword <SecureString>] [-SecondaryCertificateFile <String>]
 [-SecondaryCertificatePassword <SecureString>] [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>]
 [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>] [-VmPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8aba2-111">描述</span><span class="sxs-lookup"><span data-stu-id="8aba2-111">DESCRIPTION</span></span>

<span data-ttu-id="8aba2-112">**New-AzServiceFabricCluster 命令** 會使用您提供的憑證，或系統產生的自我簽署憑證來設定新的服務結構叢集。</span><span class="sxs-lookup"><span data-stu-id="8aba2-112">The **New-AzServiceFabricCluster** command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="8aba2-113">使用的範本可以是預設範本或您提供的自訂範本。</span><span class="sxs-lookup"><span data-stu-id="8aba2-113">The template used can be a default template or a custom template that you provide.</span></span> <span data-ttu-id="8aba2-114">您可以選擇指定資料夾來匯出自我簽署憑證，或稍後從金鑰庫抓取。</span><span class="sxs-lookup"><span data-stu-id="8aba2-114">You have the option of specifying a folder to export the self-signed certificates or fetching them later from the key vault.</span></span>
<span data-ttu-id="8aba2-115">如果您要指定自訂範本和參數檔案，則不需要在參數檔案中提供憑證資訊，系統會填入這些參數。</span><span class="sxs-lookup"><span data-stu-id="8aba2-115">If you are specifying a custom template and parameter file, you don't need to provide the certificate information in the parameter file, the system will populate these parameters.</span></span>
<span data-ttu-id="8aba2-116">以下詳述四個選項。</span><span class="sxs-lookup"><span data-stu-id="8aba2-116">The four options are detailed below.</span></span> <span data-ttu-id="8aba2-117">向下卷起以尋找每個參數的說明。</span><span class="sxs-lookup"><span data-stu-id="8aba2-117">Scroll down for explanations of each of the parameters.</span></span>

## <span data-ttu-id="8aba2-118">例子</span><span class="sxs-lookup"><span data-stu-id="8aba2-118">EXAMPLES</span></span>

### <span data-ttu-id="8aba2-119">範例 1：只指定組大小、認證主體名稱，以及部署該組組的作業系統</span><span class="sxs-lookup"><span data-stu-id="8aba2-119">Example 1: Specify only the cluster size, the cert subject name, and the OS to deploy a cluster</span></span>

```powershell
$password = "Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$resourceGroupName = "quickstart-sf-group"
$azureRegion = "southcentralus"
$clusterDnsName = "{0}.{1}.cloudapp.azure.com" -f $resourceGroupName, $azureRegion
$localCertificateFolder = "c:\certs"

Write-Output "Create cluster in '$azureRegion' with cert subject name '$clusterDnsName' and cert output path '$localCertificateFolder'"

New-AzServiceFabricCluster -ResourceGroupName $resourceGroupName -Location $azureRegion -ClusterSize 5 -VmPassword $password -CertificateSubjectName $clusterDnsName -CertificateOutputFolder $localCertificateFolder -CertificatePassword $pass -OS WindowsServer2016Datacenter
```

<span data-ttu-id="8aba2-120">此命令只會指定要部署該組集的組大小、認證主體名稱，以及作業系統。</span><span class="sxs-lookup"><span data-stu-id="8aba2-120">This command specifies only the cluster size, the cert subject name, and the OS to deploy a cluster.</span></span>

### <span data-ttu-id="8aba2-121">範例 2：在金鑰庫中指定現有的憑證資源，以及自訂範本以部署組</span><span class="sxs-lookup"><span data-stu-id="8aba2-121">Example 2: Specify an existing Certificate resource in a key vault and a custom template to deploy a cluster</span></span>

```powershell
$resourceGroupName = "test20"
$templateParameterFile = "C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile = "C:\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"
$secretId = "https://test1.vault.azure.net:443/secrets/testcertificate4/56ec774dc61a462bbc645ffc9b4b225f"

New-AzServiceFabricCluster -ResourceGroupName $resourceGroupName -TemplateFile $templateFile -ParameterFile $templateParameterFile -SecretIdentifier $secretId
```

<span data-ttu-id="8aba2-122">此命令會指定金鑰庫中的現有憑證資源，以及部署組狀圖的自訂範本。</span><span class="sxs-lookup"><span data-stu-id="8aba2-122">This command specifies an existing Certificate resource in a key vault and a custom template to deploy a cluster.</span></span>

### <span data-ttu-id="8aba2-123">範例 3：使用自訂範本建立新組。</span><span class="sxs-lookup"><span data-stu-id="8aba2-123">Example 3: Create a new cluster using a custom template.</span></span> <span data-ttu-id="8aba2-124">為金鑰庫指定不同的資源組名，然後讓系統上傳新的憑證至它</span><span class="sxs-lookup"><span data-stu-id="8aba2-124">Specify a different resource group name for the key vault and have the system upload a new certificate to it</span></span>

```powershell
$password = "Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$resourceGroupName = "quickstart-sf-group"
$keyVaultResourceGroupName = " quickstart-kv-group"
$keyVaultName = "quickstart-kv"
$azureRegion = "southcentralus"
$clusterDnsName = "{0}.{1}.cloudapp.azure.com" -F $resourceGroupName, $azureRegion
$localCertificateFolder = "~\Documents"
$templateParameterFile = "C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile = "C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"

New-AzServiceFabricCluster -ResourceGroupName $resourceGroupName -TemplateFile $templateFile -ParameterFile $templateParameterFile -CertificateOutputFolder $localCertificateFolder -CertificatePassword $password -KeyVaultResourceGroupName $keyVaultResourceGroupName  -KeyVaultName $keyVaultName -CertificateSubjectName $clusterDnsName
```

<span data-ttu-id="8aba2-125">此命令會使用自訂範本建立新組。</span><span class="sxs-lookup"><span data-stu-id="8aba2-125">This command creates a new cluster using a custom template.</span></span> <span data-ttu-id="8aba2-126">為金鑰庫指定不同的資源組名，然後讓系統上傳新的憑證至它</span><span class="sxs-lookup"><span data-stu-id="8aba2-126">Specify a different resource group name for the key vault and have the system upload a new certificate to it</span></span>

### <span data-ttu-id="8aba2-127">範例 4：攜帶您自己的憑證和自訂範本，然後建立新組</span><span class="sxs-lookup"><span data-stu-id="8aba2-127">Example 4: Bring your own Certificate and custom template and create a new cluster</span></span>

```powershell
$password = "Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$resourceGroupName = "test20"
$keyVaultResourceGroupName = "test20kvrg"
$keyVaultName = "test20kv"
$localCertificateFile = "c:\Mycertificates\my2017Prodcert.pfx"
$templateParameterFile = "~\Documents\GitHub\azure-quickstart-templates-parms\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile = "~\GitHub\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"

New-AzServiceFabricCluster -ResourceGroupName $resourceGroupName -TemplateFile $templateFile -ParameterFile $templateParameterFile -CertificateFile $localCertificateFile -CertificatePassword $password -KeyVaultResourceGroupName $keyVaultResourceGroupName -KeyVaultName $keyVaultName
```

<span data-ttu-id="8aba2-128">此命令將讓您攜帶自己的憑證和自訂範本，並建立新組。</span><span class="sxs-lookup"><span data-stu-id="8aba2-128">This command will let you bring your own Certificate and custom template and create a new cluster.</span></span>

## <span data-ttu-id="8aba2-129">參數</span><span class="sxs-lookup"><span data-stu-id="8aba2-129">PARAMETERS</span></span>

### <span data-ttu-id="8aba2-130">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="8aba2-130">-CertificateCommonName</span></span>

<span data-ttu-id="8aba2-131">憑證通用名稱</span><span class="sxs-lookup"><span data-stu-id="8aba2-131">Certificate common name</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault, ByExistingPfxAndVaultName
Aliases: CertCommonName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8aba2-132">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="8aba2-132">-CertificateFile</span></span>

<span data-ttu-id="8aba2-133">主組證書的現有憑證檔案路徑</span><span class="sxs-lookup"><span data-stu-id="8aba2-133">The existing certificate file path for the primary cluster certificate</span></span>

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

### <span data-ttu-id="8aba2-134">-CertificateIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="8aba2-134">-CertificateIssuerThumbprint</span></span>

<span data-ttu-id="8aba2-135">憑證發行者指紋，如果超過一個，請以逗號分隔</span><span class="sxs-lookup"><span data-stu-id="8aba2-135">Certificate issuer thumbprint, separated by commas if more than one</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault, ByExistingPfxAndVaultName
Aliases: CertIssuerThumbprint

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8aba2-136">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="8aba2-136">-CertificateOutputFolder</span></span>

<span data-ttu-id="8aba2-137">要建立的新憑證檔案資料夾</span><span class="sxs-lookup"><span data-stu-id="8aba2-137">The folder of the new certificate file to be created</span></span>

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

### <span data-ttu-id="8aba2-138">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="8aba2-138">-CertificatePassword</span></span>

<span data-ttu-id="8aba2-139">憑證檔案的密碼</span><span class="sxs-lookup"><span data-stu-id="8aba2-139">The password of the certificate file</span></span>

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

### <span data-ttu-id="8aba2-140">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="8aba2-140">-CertificateSubjectName</span></span>

<span data-ttu-id="8aba2-141">要建立之憑證的主體名稱</span><span class="sxs-lookup"><span data-stu-id="8aba2-141">The subject name of the certificate to be created</span></span>

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

### <span data-ttu-id="8aba2-142">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="8aba2-142">-ClusterSize</span></span>

<span data-ttu-id="8aba2-143">該組集中的節點數目。</span><span class="sxs-lookup"><span data-stu-id="8aba2-143">The number of nodes in the cluster.</span></span>
<span data-ttu-id="8aba2-144">預設為 5 個節點</span><span class="sxs-lookup"><span data-stu-id="8aba2-144">Default are 5 nodes</span></span>

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

### <span data-ttu-id="8aba2-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8aba2-145">-DefaultProfile</span></span>

<span data-ttu-id="8aba2-146">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8aba2-146">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8aba2-147">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="8aba2-147">-KeyVaultName</span></span>

<span data-ttu-id="8aba2-148">Azure 金鑰庫名稱若未指定，會預設為資源組名</span><span class="sxs-lookup"><span data-stu-id="8aba2-148">Azure key vault name, if not given it will be defaulted to the resource group name</span></span>

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

### <span data-ttu-id="8aba2-149">-KeyVaultResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8aba2-149">-KeyVaultResourceGroupName</span></span>

<span data-ttu-id="8aba2-150">Azure 金鑰庫資源組名 ，如果沒有指定，則預設為資源組名</span><span class="sxs-lookup"><span data-stu-id="8aba2-150">Azure key vault resource group name, if not given it will be defaulted to resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: KeyVaultResouceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8aba2-151">-位置</span><span class="sxs-lookup"><span data-stu-id="8aba2-151">-Location</span></span>

<span data-ttu-id="8aba2-152">資源群組位置</span><span class="sxs-lookup"><span data-stu-id="8aba2-152">The resource group location</span></span>

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

### <span data-ttu-id="8aba2-153">-名稱</span><span class="sxs-lookup"><span data-stu-id="8aba2-153">-Name</span></span>

<span data-ttu-id="8aba2-154">指定群組名稱，如果沒有指定，該組名會與資源組名相同</span><span class="sxs-lookup"><span data-stu-id="8aba2-154">Specify the name of the cluster, if not given it will be same as resource group name</span></span>

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

### <span data-ttu-id="8aba2-155">-OS</span><span class="sxs-lookup"><span data-stu-id="8aba2-155">-OS</span></span>

<span data-ttu-id="8aba2-156">這是由該群所所建立之虛擬機器的作業系統。</span><span class="sxs-lookup"><span data-stu-id="8aba2-156">The Operating System of the VMs that make up the cluster.</span></span>

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

### <span data-ttu-id="8aba2-157">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="8aba2-157">-ParameterFile</span></span>

<span data-ttu-id="8aba2-158">範本參數檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="8aba2-158">The path to the template parameter file.</span></span>

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

### <span data-ttu-id="8aba2-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8aba2-159">-ResourceGroupName</span></span>

<span data-ttu-id="8aba2-160">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8aba2-160">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="8aba2-161">-SecondaryCertificateFile</span><span class="sxs-lookup"><span data-stu-id="8aba2-161">-SecondaryCertificateFile</span></span>

<span data-ttu-id="8aba2-162">次要組群憑證的現有憑證檔案路徑</span><span class="sxs-lookup"><span data-stu-id="8aba2-162">The existing certificate file path for the secondary cluster certificate</span></span>

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

### <span data-ttu-id="8aba2-163">-SecondaryCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="8aba2-163">-SecondaryCertificatePassword</span></span>

<span data-ttu-id="8aba2-164">憑證檔案的密碼</span><span class="sxs-lookup"><span data-stu-id="8aba2-164">The password of the certificate file</span></span>

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

### <span data-ttu-id="8aba2-165">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="8aba2-165">-SecretIdentifier</span></span>

<span data-ttu-id="8aba2-166">現有的 Azure 金鑰庫密碼 URL，例如 https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f '</span><span class="sxs-lookup"><span data-stu-id="8aba2-166">The existing Azure key vault secret URL, for example 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'</span></span>

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

### <span data-ttu-id="8aba2-167">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="8aba2-167">-TemplateFile</span></span>

<span data-ttu-id="8aba2-168">範本檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="8aba2-168">The path to the template file.</span></span>

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

### <span data-ttu-id="8aba2-169">-拇指列印</span><span class="sxs-lookup"><span data-stu-id="8aba2-169">-Thumbprint</span></span>
<span data-ttu-id="8aba2-170">憑證的指紋會套用至 SecretIdentifier。</span><span class="sxs-lookup"><span data-stu-id="8aba2-170">The thumbprint for the certificate correspoinding to the SecretIdentifier.</span></span> <span data-ttu-id="8aba2-171">如果憑證未管理，因為金鑰保存庫只會將憑證儲存為機密，且 Cmdlet 無法重新處理指紋，請使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="8aba2-171">Use this if the certificate is not managed as the key vault would only have the certificate stored as a secret and the cmdlet is unable to retreive the thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8aba2-172">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="8aba2-172">-VmPassword</span></span>

<span data-ttu-id="8aba2-173">這是 Vm 的密碼。</span><span class="sxs-lookup"><span data-stu-id="8aba2-173">The password of the Vm.</span></span>

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

### <span data-ttu-id="8aba2-174">-VmSku</span><span class="sxs-lookup"><span data-stu-id="8aba2-174">-VmSku</span></span>

<span data-ttu-id="8aba2-175">The Vm Sku</span><span class="sxs-lookup"><span data-stu-id="8aba2-175">The Vm Sku</span></span>

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

### <span data-ttu-id="8aba2-176">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="8aba2-176">-VmUserName</span></span>

<span data-ttu-id="8aba2-177">記錄到 Vm 的使用者名稱</span><span class="sxs-lookup"><span data-stu-id="8aba2-177">The user name for logging to Vm</span></span>

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

### <span data-ttu-id="8aba2-178">-確認</span><span class="sxs-lookup"><span data-stu-id="8aba2-178">-Confirm</span></span>

<span data-ttu-id="8aba2-179">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="8aba2-179">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8aba2-180">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8aba2-180">-WhatIf</span></span>

<span data-ttu-id="8aba2-181">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8aba2-181">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8aba2-182">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8aba2-182">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8aba2-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8aba2-183">CommonParameters</span></span>
<span data-ttu-id="8aba2-184">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8aba2-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8aba2-185">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8aba2-185">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8aba2-186">輸入</span><span class="sxs-lookup"><span data-stu-id="8aba2-186">INPUTS</span></span>

### <span data-ttu-id="8aba2-187">System.String</span><span class="sxs-lookup"><span data-stu-id="8aba2-187">System.String</span></span>

### <span data-ttu-id="8aba2-188">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="8aba2-188">System.Security.SecureString</span></span>

### <span data-ttu-id="8aba2-189">System.Int32</span><span class="sxs-lookup"><span data-stu-id="8aba2-189">System.Int32</span></span>

### <span data-ttu-id="8aba2-190">Microsoft.Azure.Commands.ServiceFabric.models.OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="8aba2-190">Microsoft.Azure.Commands.ServiceFabric.Models.OperatingSystem</span></span>

## <span data-ttu-id="8aba2-191">輸出</span><span class="sxs-lookup"><span data-stu-id="8aba2-191">OUTPUTS</span></span>

### <span data-ttu-id="8aba2-192">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span><span class="sxs-lookup"><span data-stu-id="8aba2-192">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span></span>

## <span data-ttu-id="8aba2-193">筆記</span><span class="sxs-lookup"><span data-stu-id="8aba2-193">NOTES</span></span>

## <span data-ttu-id="8aba2-194">相關連結</span><span class="sxs-lookup"><span data-stu-id="8aba2-194">RELATED LINKS</span></span>
