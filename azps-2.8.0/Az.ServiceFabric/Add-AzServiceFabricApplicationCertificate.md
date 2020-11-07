---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricapplicationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricApplicationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricApplicationCertificate.md
ms.openlocfilehash: 62298a5747a8bb5b4f01458cac611f5e86869ee7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792086"
---
# <span data-ttu-id="87386-101">Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="87386-101">Add-AzServiceFabricApplicationCertificate</span></span>

## <span data-ttu-id="87386-102">摘要</span><span class="sxs-lookup"><span data-stu-id="87386-102">SYNOPSIS</span></span>
<span data-ttu-id="87386-103">在組成群集 (s) ，將新憑證新增到虛擬電腦規模集。</span><span class="sxs-lookup"><span data-stu-id="87386-103">Add a new certificate to the Virtual Machine Scale Set(s) that make up the cluster.</span></span> <span data-ttu-id="87386-104">憑證是用來做為應用程式憑證的。</span><span class="sxs-lookup"><span data-stu-id="87386-104">The certificate is intended to be used as an application certificate.</span></span>

## <span data-ttu-id="87386-105">句法</span><span class="sxs-lookup"><span data-stu-id="87386-105">SYNTAX</span></span>

### <span data-ttu-id="87386-106">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="87386-106">ByExistingKeyVault</span></span>
```
Add-AzServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 -SecretIdentifier <String> [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87386-107">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="87386-107">ByNewPfxAndVaultName</span></span>
```
Add-AzServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87386-108">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="87386-108">ByExistingPfxAndVaultName</span></span>
```
Add-AzServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-CertificateCommonName <String>]
 [-CertificateIssuerThumbprint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="87386-109">說明</span><span class="sxs-lookup"><span data-stu-id="87386-109">DESCRIPTION</span></span>
<span data-ttu-id="87386-110">使用 [ **載入 AzServiceFabricApplicationCertificate** ]，將憑證安裝到群集中的所有節點。</span><span class="sxs-lookup"><span data-stu-id="87386-110">Use **Add-AzServiceFabricApplicationCertificate** to install a certificate to all nodes in the cluster.</span></span> <span data-ttu-id="87386-111">您可以指定已有的憑證，或讓系統為您產生新的憑證，然後將它上傳到新的或現有的 Azure 金鑰儲存庫。</span><span class="sxs-lookup"><span data-stu-id="87386-111">You can specify a certificate you already have or have the system generate a new one for you, and upload it to a new or existing Azure key vault.</span></span>

## <span data-ttu-id="87386-112">示例</span><span class="sxs-lookup"><span data-stu-id="87386-112">EXAMPLES</span></span>

### <span data-ttu-id="87386-113">範例1</span><span class="sxs-lookup"><span data-stu-id="87386-113">Example 1</span></span>
```powershell
PS c:> Add-AzServiceFabricApplicationCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="87386-114">這個命令會將現有 Azure 金鑰保存庫的憑證新增到所有叢集節點類型。</span><span class="sxs-lookup"><span data-stu-id="87386-114">This command will add a certificate from existing Azure key vault to all node types of the cluster.</span></span>

### <span data-ttu-id="87386-115">範例2</span><span class="sxs-lookup"><span data-stu-id="87386-115">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String '123' -AsPlainText -Force
PS C:\> Add-AzServiceFabricApplicationCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -KeyVaultName 'Contoso02Vault' -KeyVaultResouceGroupName 'Contoso02VaultRg'
        -CertificateSubjectName 'cn=Contoso.com' -CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="87386-116">這個命令會在 Azure 金鑰保存庫中使用主要電子倉庫資源群組名稱和金鑰保存庫名稱來建立自我簽署憑證，安裝到所有叢集節點類型，並下載資料夾 ' c:\test」下的憑證。</span><span class="sxs-lookup"><span data-stu-id="87386-116">This command will create a self-signed certificate in the Azure key vault with the key vault resource group name and key vault Name, installs to all node types of the cluster, and downloads the certificate under folder 'c:\test'.</span></span> <span data-ttu-id="87386-117">下載的憑證名稱與主要 vault 憑證的名稱相同。</span><span class="sxs-lookup"><span data-stu-id="87386-117">The name of the certificate downloaded is same as the name of key vault certificate.</span></span>

## <span data-ttu-id="87386-118">參數</span><span class="sxs-lookup"><span data-stu-id="87386-118">PARAMETERS</span></span>

### <span data-ttu-id="87386-119">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="87386-119">-CertificateCommonName</span></span>
<span data-ttu-id="87386-120">證書公用名稱</span><span class="sxs-lookup"><span data-stu-id="87386-120">Certificate common name</span></span>

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

### <span data-ttu-id="87386-121">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="87386-121">-CertificateFile</span></span>
<span data-ttu-id="87386-122">現有憑證的路徑</span><span class="sxs-lookup"><span data-stu-id="87386-122">The path to the existing certificate</span></span>

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

### <span data-ttu-id="87386-123">-CertificateIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="87386-123">-CertificateIssuerThumbprint</span></span>
<span data-ttu-id="87386-124">憑證簽發者指紋（如果有多個，則以逗號分隔）</span><span class="sxs-lookup"><span data-stu-id="87386-124">Certificate issuer thumbprint, separated by commas if more than one</span></span>

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

### <span data-ttu-id="87386-125">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="87386-125">-CertificateOutputFolder</span></span>
<span data-ttu-id="87386-126">需要下載新憑證的資料夾。</span><span class="sxs-lookup"><span data-stu-id="87386-126">The folder where the new certificate needs to be downloaded.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNewPfxAndVaultName
Aliases: Destination

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87386-127">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="87386-127">-CertificatePassword</span></span>
<span data-ttu-id="87386-128">憑證的密碼</span><span class="sxs-lookup"><span data-stu-id="87386-128">The password of the certificate</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: CertPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87386-129">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="87386-129">-CertificateSubjectName</span></span>
<span data-ttu-id="87386-130">憑證的受領人名稱</span><span class="sxs-lookup"><span data-stu-id="87386-130">The subject name of the certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ByNewPfxAndVaultName
Aliases: Subject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87386-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87386-131">-DefaultProfile</span></span>
<span data-ttu-id="87386-132">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="87386-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87386-133">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="87386-133">-KeyVaultName</span></span>
<span data-ttu-id="87386-134">如果未指定 Azure 金鑰保存庫名稱，則會預設為資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="87386-134">Azure key vault name, if not given it will be defaulted to the resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87386-135">-KeyVaultResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87386-135">-KeyVaultResourceGroupName</span></span>
<span data-ttu-id="87386-136">Azure 金鑰電子倉庫資源群組名稱（如果未指定）會預設為 [資源] 群組名稱</span><span class="sxs-lookup"><span data-stu-id="87386-136">Azure key vault resource group name, if not given it will be defaulted to resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: KeyVaultResouceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87386-137">-名稱</span><span class="sxs-lookup"><span data-stu-id="87386-137">-Name</span></span>
<span data-ttu-id="87386-138">指定群集的名稱</span><span class="sxs-lookup"><span data-stu-id="87386-138">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87386-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87386-139">-ResourceGroupName</span></span>
<span data-ttu-id="87386-140">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="87386-140">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="87386-141">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="87386-141">-SecretIdentifier</span></span>
<span data-ttu-id="87386-142">現有的 Azure 金鑰保存庫機密 URL，例如 " https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f "</span><span class="sxs-lookup"><span data-stu-id="87386-142">The existing Azure key vault secret URL, for example 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'</span></span>

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

### <span data-ttu-id="87386-143">-確認</span><span class="sxs-lookup"><span data-stu-id="87386-143">-Confirm</span></span>
<span data-ttu-id="87386-144">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="87386-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87386-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87386-145">-WhatIf</span></span>
<span data-ttu-id="87386-146">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="87386-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87386-147">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="87386-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87386-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87386-148">CommonParameters</span></span>
<span data-ttu-id="87386-149">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="87386-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87386-150">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="87386-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87386-151">輸入</span><span class="sxs-lookup"><span data-stu-id="87386-151">INPUTS</span></span>

### <span data-ttu-id="87386-152">System.object</span><span class="sxs-lookup"><span data-stu-id="87386-152">System.String</span></span>

### <span data-ttu-id="87386-153">SecureString</span><span class="sxs-lookup"><span data-stu-id="87386-153">System.Security.SecureString</span></span>

## <span data-ttu-id="87386-154">輸出</span><span class="sxs-lookup"><span data-stu-id="87386-154">OUTPUTS</span></span>

### <span data-ttu-id="87386-155">PSKeyVault 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="87386-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSKeyVault</span></span>

## <span data-ttu-id="87386-156">筆記</span><span class="sxs-lookup"><span data-stu-id="87386-156">NOTES</span></span>

## <span data-ttu-id="87386-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="87386-157">RELATED LINKS</span></span>

[<span data-ttu-id="87386-158">附加 AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="87386-158">Add-AzServiceFabricClusterCertificate</span></span>](./Add-AzServiceFabricClusterCertificate.md)

[<span data-ttu-id="87386-159">新-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="87386-159">New-AzServiceFabricCluster</span></span>](./New-AzServiceFabricCluster.md)
