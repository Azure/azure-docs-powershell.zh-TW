---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/add-azservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClusterCertificate.md
ms.openlocfilehash: 379bd710413fee83a2fdb6b10dc7fb42f0f207bf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906390"
---
# <span data-ttu-id="fd754-101">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="fd754-101">Add-AzServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="fd754-102">簡介</span><span class="sxs-lookup"><span data-stu-id="fd754-102">SYNOPSIS</span></span>
<span data-ttu-id="fd754-103">新增次要組群憑證至該組。</span><span class="sxs-lookup"><span data-stu-id="fd754-103">Add a secondary cluster certificate to the cluster.</span></span>

## <span data-ttu-id="fd754-104">語法</span><span class="sxs-lookup"><span data-stu-id="fd754-104">SYNTAX</span></span>

### <span data-ttu-id="fd754-105">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="fd754-105">ByExistingKeyVault</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String> -SecretIdentifier <String>
 [-Thumbprint <String>] [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd754-106">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="fd754-106">ByNewPfxAndVaultName</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd754-107">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="fd754-107">ByExistingPfxAndVaultName</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-CertificateCommonName <String>]
 [-CertificateIssuerThumbprint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fd754-108">描述</span><span class="sxs-lookup"><span data-stu-id="fd754-108">DESCRIPTION</span></span>
<span data-ttu-id="fd754-109">使用 **Add-AzServiceFabricClusterCertificate** 從現有的 Azure 金鑰庫新增次要叢集憑證，或使用提供的現有憑證建立新 Azure 金鑰庫，或從已建立的新自我簽署憑證新增。</span><span class="sxs-lookup"><span data-stu-id="fd754-109">Use **Add-AzServiceFabricClusterCertificate** to add a secondary cluster certificate, either from an existing Azure key vault or creating a new Azure key vault using an existing certificate provided or from a new self-signed certificate created.</span></span> <span data-ttu-id="fd754-110">如果有次要組，它會優先于次要組。</span><span class="sxs-lookup"><span data-stu-id="fd754-110">It will override the secondary cluster if there is any.</span></span>

## <span data-ttu-id="fd754-111">例子</span><span class="sxs-lookup"><span data-stu-id="fd754-111">EXAMPLES</span></span>

### <span data-ttu-id="fd754-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="fd754-112">Example 1</span></span>
```powershell
Add-AzServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' 
-SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="fd754-113">此命令會新增現有 Azure 金鑰庫中的憑證作為次要的集區憑證。</span><span class="sxs-lookup"><span data-stu-id="fd754-113">This command will add a certificate in the existing Azure key vault as a secondary cluster certificate.</span></span>

### <span data-ttu-id="fd754-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="fd754-114">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS c:\> add-AzServiceFabricClusterCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster'  -CertificateSubjectName 'Contoso.com' 
-CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="fd754-115">此命令將在 Azure 金鑰庫建立自我簽署憑證，並升級該組，以使用它做為次要的集區憑證。</span><span class="sxs-lookup"><span data-stu-id="fd754-115">This command will create a self-signed certificate in the Azure key vault and upgrade the cluster to use it as a secondary cluster certificate.</span></span>

## <span data-ttu-id="fd754-116">參數</span><span class="sxs-lookup"><span data-stu-id="fd754-116">PARAMETERS</span></span>

### <span data-ttu-id="fd754-117">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="fd754-117">-CertificateCommonName</span></span>
<span data-ttu-id="fd754-118">憑證通用名稱</span><span class="sxs-lookup"><span data-stu-id="fd754-118">Certificate common name</span></span>

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

### <span data-ttu-id="fd754-119">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="fd754-119">-CertificateFile</span></span>
<span data-ttu-id="fd754-120">現有憑證的路徑</span><span class="sxs-lookup"><span data-stu-id="fd754-120">The path to the existing certificate</span></span>

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

### <span data-ttu-id="fd754-121">-CertificateIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="fd754-121">-CertificateIssuerThumbprint</span></span>
<span data-ttu-id="fd754-122">憑證發行者指紋，如果超過一個，請以逗號分隔</span><span class="sxs-lookup"><span data-stu-id="fd754-122">Certificate issuer thumbprint, separated by commas if more than one</span></span>

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

### <span data-ttu-id="fd754-123">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="fd754-123">-CertificateOutputFolder</span></span>
<span data-ttu-id="fd754-124">需要下載新憑證的資料夾。</span><span class="sxs-lookup"><span data-stu-id="fd754-124">The folder where the new certificate needs to be downloaded.</span></span>

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

### <span data-ttu-id="fd754-125">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="fd754-125">-CertificatePassword</span></span>
<span data-ttu-id="fd754-126">憑證的密碼</span><span class="sxs-lookup"><span data-stu-id="fd754-126">The password of the certificate</span></span>

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

### <span data-ttu-id="fd754-127">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="fd754-127">-CertificateSubjectName</span></span>
<span data-ttu-id="fd754-128">憑證的主體名稱</span><span class="sxs-lookup"><span data-stu-id="fd754-128">The subject name of the certificate</span></span>

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

### <span data-ttu-id="fd754-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd754-129">-DefaultProfile</span></span>
<span data-ttu-id="fd754-130">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="fd754-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd754-131">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="fd754-131">-KeyVaultName</span></span>
<span data-ttu-id="fd754-132">Azure 金鑰庫名稱若未指定，會預設為資源組名</span><span class="sxs-lookup"><span data-stu-id="fd754-132">Azure key vault name, if not given it will be defaulted to the resource group name</span></span>

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

### <span data-ttu-id="fd754-133">-KeyVaultResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd754-133">-KeyVaultResourceGroupName</span></span>
<span data-ttu-id="fd754-134">Azure 金鑰庫資源組名 ，如果沒有指定，則預設為資源組名</span><span class="sxs-lookup"><span data-stu-id="fd754-134">Azure key vault resource group name, if not given it will be defaulted to resource group name</span></span>

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

### <span data-ttu-id="fd754-135">-名稱</span><span class="sxs-lookup"><span data-stu-id="fd754-135">-Name</span></span>
<span data-ttu-id="fd754-136">指定組名</span><span class="sxs-lookup"><span data-stu-id="fd754-136">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="fd754-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd754-137">-ResourceGroupName</span></span>
<span data-ttu-id="fd754-138">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fd754-138">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="fd754-139">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="fd754-139">-SecretIdentifier</span></span>
<span data-ttu-id="fd754-140">現有的 Azure 金鑰庫密碼 URL，例如 https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f '</span><span class="sxs-lookup"><span data-stu-id="fd754-140">The existing Azure key vault secret URL, for example 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'</span></span>

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

### <span data-ttu-id="fd754-141">-拇指列印</span><span class="sxs-lookup"><span data-stu-id="fd754-141">-Thumbprint</span></span>
<span data-ttu-id="fd754-142">憑證的指紋會套用至 SecretIdentifier。</span><span class="sxs-lookup"><span data-stu-id="fd754-142">The thumbprint for the certificate correspoinding to the SecretIdentifier.</span></span> <span data-ttu-id="fd754-143">如果憑證未管理，因為金鑰保存庫只會將憑證儲存為機密，且 Cmdlet 無法重新處理指紋，請使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="fd754-143">Use this if the certificate is not managed as the key vault would only have the certificate stored as a secret and the cmdlet is unable to retreive the thumbprint.</span></span>

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

### <span data-ttu-id="fd754-144">-確認</span><span class="sxs-lookup"><span data-stu-id="fd754-144">-Confirm</span></span>
<span data-ttu-id="fd754-145">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="fd754-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd754-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd754-146">-WhatIf</span></span>
<span data-ttu-id="fd754-147">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fd754-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd754-148">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fd754-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd754-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd754-149">CommonParameters</span></span>
<span data-ttu-id="fd754-150">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="fd754-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd754-151">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fd754-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd754-152">輸入</span><span class="sxs-lookup"><span data-stu-id="fd754-152">INPUTS</span></span>

### <span data-ttu-id="fd754-153">System.String</span><span class="sxs-lookup"><span data-stu-id="fd754-153">System.String</span></span>

### <span data-ttu-id="fd754-154">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="fd754-154">System.Security.SecureString</span></span>

## <span data-ttu-id="fd754-155">輸出</span><span class="sxs-lookup"><span data-stu-id="fd754-155">OUTPUTS</span></span>

### <span data-ttu-id="fd754-156">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="fd754-156">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="fd754-157">筆記</span><span class="sxs-lookup"><span data-stu-id="fd754-157">NOTES</span></span>

## <span data-ttu-id="fd754-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="fd754-158">RELATED LINKS</span></span>

[<span data-ttu-id="fd754-159">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="fd754-159">Remove-AzServiceFabricClusterCertificate</span></span>](./Remove-AzServiceFabricClusterCertificate.md)

[<span data-ttu-id="fd754-160">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="fd754-160">New-AzServiceFabricCluster</span></span>](./New-AzServiceFabricCluster.md)
