---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricCluster.md
ms.openlocfilehash: 9e5ba2d2ee228da30a887c0c7b318dd9d270d763
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98448231"
---
# <span data-ttu-id="526da-101">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="526da-101">New-AzServiceFabricCluster</span></span>

## <span data-ttu-id="526da-102">摘要</span><span class="sxs-lookup"><span data-stu-id="526da-102">SYNOPSIS</span></span>

<span data-ttu-id="526da-103">這個命令會使用您提供的憑證或系統產生的自我簽署憑證來設定新的服務結構群集。</span><span class="sxs-lookup"><span data-stu-id="526da-103">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="526da-104">它可以使用您所提供的預設範本或自訂範本。</span><span class="sxs-lookup"><span data-stu-id="526da-104">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="526da-105">您可以選擇將自行簽署的憑證匯出到哪個資料夾，或稍後從金鑰電子倉庫將其回遷。</span><span class="sxs-lookup"><span data-stu-id="526da-105">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span>

## <span data-ttu-id="526da-106">句法</span><span class="sxs-lookup"><span data-stu-id="526da-106">SYNTAX</span></span>

### <span data-ttu-id="526da-107">ByDefaultArmTemplate (預設) </span><span class="sxs-lookup"><span data-stu-id="526da-107">ByDefaultArmTemplate (Default)</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>]
 -Location <String> [-Name <String>] [-VmUserName <String>] [-ClusterSize <Int32>]
 [-CertificateSubjectName <String>] -VmPassword <SecureString> [-OS <OperatingSystem>] [-VmSku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="526da-108">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="526da-108">ByExistingKeyVault</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>] [-VmPassword <SecureString>]
 -SecretIdentifier <String> [-Thumbprint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="526da-109">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="526da-109">ByNewPfxAndVaultName</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-CertificateOutputFolder <String>] [-CertificatePassword <SecureString>]
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] [-CertificateSubjectName <String>]
 [-VmPassword <SecureString>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="526da-110">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="526da-110">ByExistingPfxAndVaultName</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 -CertificateFile <String> [-CertificatePassword <SecureString>] [-SecondaryCertificateFile <String>]
 [-SecondaryCertificatePassword <SecureString>] [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>]
 [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>] [-VmPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="526da-111">說明</span><span class="sxs-lookup"><span data-stu-id="526da-111">DESCRIPTION</span></span>

<span data-ttu-id="526da-112">**新的-AzServiceFabricCluster** 命令會使用您所提供的憑證或系統產生的自我簽署憑證來設定新的服務結構群集。</span><span class="sxs-lookup"><span data-stu-id="526da-112">The **New-AzServiceFabricCluster** command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="526da-113">使用的範本可以是您提供的預設範本或自訂範本。</span><span class="sxs-lookup"><span data-stu-id="526da-113">The template used can be a default template or a custom template that you provide.</span></span> <span data-ttu-id="526da-114">您可以選擇指定要匯出自簽章憑證的資料夾，或稍後從金鑰保存庫回遷。</span><span class="sxs-lookup"><span data-stu-id="526da-114">You have the option of specifying a folder to export the self-signed certificates or fetching them later from the key vault.</span></span>
<span data-ttu-id="526da-115">如果您要指定自訂範本和參數檔案，則不需要在參數檔案中提供憑證資訊，系統就會填入這些參數。</span><span class="sxs-lookup"><span data-stu-id="526da-115">If you are specifying a custom template and parameter file, you don't need to provide the certificate information in the parameter file, the system will populate these parameters.</span></span>
<span data-ttu-id="526da-116">下面將詳細說明四個選項。</span><span class="sxs-lookup"><span data-stu-id="526da-116">The four options are detailed below.</span></span> <span data-ttu-id="526da-117">向下滾動，以取得每個參數的說明。</span><span class="sxs-lookup"><span data-stu-id="526da-117">Scroll down for explanations of each of the parameters.</span></span>

## <span data-ttu-id="526da-118">示例</span><span class="sxs-lookup"><span data-stu-id="526da-118">EXAMPLES</span></span>

### <span data-ttu-id="526da-119">範例1：只指定群集大小、cert 受領人名稱，以及要部署群集的 OS</span><span class="sxs-lookup"><span data-stu-id="526da-119">Example 1: Specify only the cluster size, the cert subject name, and the OS to deploy a cluster</span></span>

```powershell
$password = "Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$resourceGroupName = "quickstart-sf-group"
$azureRegion = "southcentralus"
$clusterDnsName = "{0}.{1}.cloudapp.azure.com" -f $resourceGroupName, $azureRegion
$localCertificateFolder = "c:\certs"

Write-Output "Create cluster in '$azureRegion' with cert subject name '$clusterDnsName' and cert output path '$localCertificateFolder'"

New-AzServiceFabricCluster -ResourceGroupName $resourceGroupName -Location $azureRegion -ClusterSize 5 -VmPassword $password -CertificateSubjectName $clusterDnsName -CertificateOutputFolder $localCertificateFolder -CertificatePassword $pass -OS WindowsServer2016Datacenter
```

<span data-ttu-id="526da-120">這個命令只會指定群集大小、cert 受領人名稱，以及作業系統來部署群集。</span><span class="sxs-lookup"><span data-stu-id="526da-120">This command specifies only the cluster size, the cert subject name, and the OS to deploy a cluster.</span></span>

### <span data-ttu-id="526da-121">範例2：在主要電子倉庫中指定現有的憑證資源，以及可供您部署群集的自訂範本</span><span class="sxs-lookup"><span data-stu-id="526da-121">Example 2: Specify an existing Certificate resource in a key vault and a custom template to deploy a cluster</span></span>

```powershell
$resourceGroupName = "test20"
$templateParameterFile = "C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile = "C:\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"
$secretId = "https://test1.vault.azure.net:443/secrets/testcertificate4/56ec774dc61a462bbc645ffc9b4b225f"

New-AzServiceFabricCluster -ResourceGroupName $resourceGroupName -TemplateFile $templateFile -ParameterFile $templateParameterFile -SecretIdentifier $secretId
```

<span data-ttu-id="526da-122">這個命令會指定主要電子倉庫中現有的憑證資源，以及用來部署群集的自訂範本。</span><span class="sxs-lookup"><span data-stu-id="526da-122">This command specifies an existing Certificate resource in a key vault and a custom template to deploy a cluster.</span></span>

### <span data-ttu-id="526da-123">範例3：使用自訂範本建立新的群集。</span><span class="sxs-lookup"><span data-stu-id="526da-123">Example 3: Create a new cluster using a custom template.</span></span> <span data-ttu-id="526da-124">為主要保存庫指定不同的資源組名稱，並將系統上傳新憑證給它</span><span class="sxs-lookup"><span data-stu-id="526da-124">Specify a different resource group name for the key vault and have the system upload a new certificate to it</span></span>

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

<span data-ttu-id="526da-125">這個命令會使用自訂範本來建立新的群集。</span><span class="sxs-lookup"><span data-stu-id="526da-125">This command creates a new cluster using a custom template.</span></span> <span data-ttu-id="526da-126">為主要保存庫指定不同的資源組名稱，並將系統上傳新憑證給它</span><span class="sxs-lookup"><span data-stu-id="526da-126">Specify a different resource group name for the key vault and have the system upload a new certificate to it</span></span>

### <span data-ttu-id="526da-127">範例4：攜帶您自己的憑證和自訂範本，並建立新的群集</span><span class="sxs-lookup"><span data-stu-id="526da-127">Example 4: Bring your own Certificate and custom template and create a new cluster</span></span>

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

<span data-ttu-id="526da-128">這個命令可讓您攜帶自己的憑證和自訂範本，並建立新的群集。</span><span class="sxs-lookup"><span data-stu-id="526da-128">This command will let you bring your own Certificate and custom template and create a new cluster.</span></span>

## <span data-ttu-id="526da-129">參數</span><span class="sxs-lookup"><span data-stu-id="526da-129">PARAMETERS</span></span>

### <span data-ttu-id="526da-130">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="526da-130">-CertificateCommonName</span></span>

<span data-ttu-id="526da-131">證書公用名稱</span><span class="sxs-lookup"><span data-stu-id="526da-131">Certificate common name</span></span>

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

### <span data-ttu-id="526da-132">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="526da-132">-CertificateFile</span></span>

<span data-ttu-id="526da-133">主要群集憑證的現有憑證檔路徑</span><span class="sxs-lookup"><span data-stu-id="526da-133">The existing certificate file path for the primary cluster certificate</span></span>

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

### <span data-ttu-id="526da-134">-CertificateIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="526da-134">-CertificateIssuerThumbprint</span></span>

<span data-ttu-id="526da-135">憑證簽發者指紋（如果有多個，則以逗號分隔）</span><span class="sxs-lookup"><span data-stu-id="526da-135">Certificate issuer thumbprint, separated by commas if more than one</span></span>

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

### <span data-ttu-id="526da-136">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="526da-136">-CertificateOutputFolder</span></span>

<span data-ttu-id="526da-137">要建立之新憑證檔案的資料夾</span><span class="sxs-lookup"><span data-stu-id="526da-137">The folder of the new certificate file to be created</span></span>

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

### <span data-ttu-id="526da-138">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="526da-138">-CertificatePassword</span></span>

<span data-ttu-id="526da-139">憑證檔的密碼</span><span class="sxs-lookup"><span data-stu-id="526da-139">The password of the certificate file</span></span>

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

### <span data-ttu-id="526da-140">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="526da-140">-CertificateSubjectName</span></span>

<span data-ttu-id="526da-141">要建立之憑證的受領人名稱</span><span class="sxs-lookup"><span data-stu-id="526da-141">The subject name of the certificate to be created</span></span>

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

### <span data-ttu-id="526da-142">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="526da-142">-ClusterSize</span></span>

<span data-ttu-id="526da-143">群集中的節點數。</span><span class="sxs-lookup"><span data-stu-id="526da-143">The number of nodes in the cluster.</span></span>
<span data-ttu-id="526da-144">預設值為5個節點</span><span class="sxs-lookup"><span data-stu-id="526da-144">Default are 5 nodes</span></span>

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

### <span data-ttu-id="526da-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="526da-145">-DefaultProfile</span></span>

<span data-ttu-id="526da-146">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="526da-146">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="526da-147">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="526da-147">-KeyVaultName</span></span>

<span data-ttu-id="526da-148">如果未指定 Azure 金鑰保存庫名稱，則會預設為資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="526da-148">Azure key vault name, if not given it will be defaulted to the resource group name</span></span>

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

### <span data-ttu-id="526da-149">-KeyVaultResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="526da-149">-KeyVaultResourceGroupName</span></span>

<span data-ttu-id="526da-150">Azure 金鑰電子倉庫資源群組名稱（如果未指定）會預設為 [資源] 群組名稱</span><span class="sxs-lookup"><span data-stu-id="526da-150">Azure key vault resource group name, if not given it will be defaulted to resource group name</span></span>

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

### <span data-ttu-id="526da-151">-位置</span><span class="sxs-lookup"><span data-stu-id="526da-151">-Location</span></span>

<span data-ttu-id="526da-152">資源群組位置</span><span class="sxs-lookup"><span data-stu-id="526da-152">The resource group location</span></span>

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

### <span data-ttu-id="526da-153">-名稱</span><span class="sxs-lookup"><span data-stu-id="526da-153">-Name</span></span>

<span data-ttu-id="526da-154">指定群集的名稱（如果未指定的話），則會與資源群組名稱相同</span><span class="sxs-lookup"><span data-stu-id="526da-154">Specify the name of the cluster, if not given it will be same as resource group name</span></span>

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

### <span data-ttu-id="526da-155">-OS</span><span class="sxs-lookup"><span data-stu-id="526da-155">-OS</span></span>

<span data-ttu-id="526da-156">組成群集之 Vm 的作業系統。</span><span class="sxs-lookup"><span data-stu-id="526da-156">The Operating System of the VMs that make up the cluster.</span></span>

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

### <span data-ttu-id="526da-157">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="526da-157">-ParameterFile</span></span>

<span data-ttu-id="526da-158">範本參數檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="526da-158">The path to the template parameter file.</span></span>

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

### <span data-ttu-id="526da-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="526da-159">-ResourceGroupName</span></span>

<span data-ttu-id="526da-160">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="526da-160">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="526da-161">-SecondaryCertificateFile</span><span class="sxs-lookup"><span data-stu-id="526da-161">-SecondaryCertificateFile</span></span>

<span data-ttu-id="526da-162">次要群集憑證的現有憑證檔路徑</span><span class="sxs-lookup"><span data-stu-id="526da-162">The existing certificate file path for the secondary cluster certificate</span></span>

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

### <span data-ttu-id="526da-163">-SecondaryCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="526da-163">-SecondaryCertificatePassword</span></span>

<span data-ttu-id="526da-164">憑證檔的密碼</span><span class="sxs-lookup"><span data-stu-id="526da-164">The password of the certificate file</span></span>

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

### <span data-ttu-id="526da-165">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="526da-165">-SecretIdentifier</span></span>

<span data-ttu-id="526da-166">現有的 Azure 金鑰保存庫機密 URL，例如 " https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f "</span><span class="sxs-lookup"><span data-stu-id="526da-166">The existing Azure key vault secret URL, for example 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'</span></span>

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

### <span data-ttu-id="526da-167">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="526da-167">-TemplateFile</span></span>

<span data-ttu-id="526da-168">範本檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="526da-168">The path to the template file.</span></span>

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

### <span data-ttu-id="526da-169">-指紋</span><span class="sxs-lookup"><span data-stu-id="526da-169">-Thumbprint</span></span>
<span data-ttu-id="526da-170">憑證 correspoinding 到 SecretIdentifier 的指紋。</span><span class="sxs-lookup"><span data-stu-id="526da-170">The thumbprint for the certificate correspoinding to the SecretIdentifier.</span></span> <span data-ttu-id="526da-171">如果未以金鑰保存庫的形式管理證書，則使用此選項只會將憑證儲存為機密，且 Cmdlet 無法檢索指紋。</span><span class="sxs-lookup"><span data-stu-id="526da-171">Use this if the certificate is not managed as the key vault would only have the certificate stored as a secret and the cmdlet is unable to retreive the thumbprint.</span></span>

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

### <span data-ttu-id="526da-172">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="526da-172">-VmPassword</span></span>

<span data-ttu-id="526da-173">Vm 的密碼。</span><span class="sxs-lookup"><span data-stu-id="526da-173">The password of the Vm.</span></span>

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

### <span data-ttu-id="526da-174">-VmSku</span><span class="sxs-lookup"><span data-stu-id="526da-174">-VmSku</span></span>

<span data-ttu-id="526da-175">Vm Sku</span><span class="sxs-lookup"><span data-stu-id="526da-175">The Vm Sku</span></span>

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

### <span data-ttu-id="526da-176">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="526da-176">-VmUserName</span></span>

<span data-ttu-id="526da-177">用於記錄到 Vm 的使用者名稱</span><span class="sxs-lookup"><span data-stu-id="526da-177">The user name for logging to Vm</span></span>

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

### <span data-ttu-id="526da-178">-確認</span><span class="sxs-lookup"><span data-stu-id="526da-178">-Confirm</span></span>

<span data-ttu-id="526da-179">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="526da-179">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="526da-180">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="526da-180">-WhatIf</span></span>

<span data-ttu-id="526da-181">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="526da-181">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="526da-182">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="526da-182">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="526da-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="526da-183">CommonParameters</span></span>
<span data-ttu-id="526da-184">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="526da-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="526da-185">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="526da-185">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="526da-186">輸入</span><span class="sxs-lookup"><span data-stu-id="526da-186">INPUTS</span></span>

### <span data-ttu-id="526da-187">System.object</span><span class="sxs-lookup"><span data-stu-id="526da-187">System.String</span></span>

### <span data-ttu-id="526da-188">SecureString</span><span class="sxs-lookup"><span data-stu-id="526da-188">System.Security.SecureString</span></span>

### <span data-ttu-id="526da-189">System.object</span><span class="sxs-lookup"><span data-stu-id="526da-189">System.Int32</span></span>

### <span data-ttu-id="526da-190">[ServiceFabric] 的作業系統</span><span class="sxs-lookup"><span data-stu-id="526da-190">Microsoft.Azure.Commands.ServiceFabric.Models.OperatingSystem</span></span>

## <span data-ttu-id="526da-191">輸出</span><span class="sxs-lookup"><span data-stu-id="526da-191">OUTPUTS</span></span>

### <span data-ttu-id="526da-192">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span><span class="sxs-lookup"><span data-stu-id="526da-192">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span></span>

## <span data-ttu-id="526da-193">筆記</span><span class="sxs-lookup"><span data-stu-id="526da-193">NOTES</span></span>

## <span data-ttu-id="526da-194">相關連結</span><span class="sxs-lookup"><span data-stu-id="526da-194">RELATED LINKS</span></span>
