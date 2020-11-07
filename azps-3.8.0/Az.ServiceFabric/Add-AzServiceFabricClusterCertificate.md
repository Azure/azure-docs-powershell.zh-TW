---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClusterCertificate.md
ms.openlocfilehash: dfbf9267aad981db63608c744825f1b636c85425
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957017"
---
# <span data-ttu-id="b26ba-101">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="b26ba-101">Add-AzServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="b26ba-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b26ba-102">SYNOPSIS</span></span>
<span data-ttu-id="b26ba-103">將次要群集憑證新增至群集。</span><span class="sxs-lookup"><span data-stu-id="b26ba-103">Add a secondary cluster certificate to the cluster.</span></span>

## <span data-ttu-id="b26ba-104">句法</span><span class="sxs-lookup"><span data-stu-id="b26ba-104">SYNTAX</span></span>

### <span data-ttu-id="b26ba-105">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="b26ba-105">ByExistingKeyVault</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String> -SecretIdentifier <String>
 [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b26ba-106">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="b26ba-106">ByNewPfxAndVaultName</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b26ba-107">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="b26ba-107">ByExistingPfxAndVaultName</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-CertificateCommonName <String>]
 [-CertificateIssuerThumbprint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b26ba-108">說明</span><span class="sxs-lookup"><span data-stu-id="b26ba-108">DESCRIPTION</span></span>
<span data-ttu-id="b26ba-109">使用 **AzServiceFabricClusterCertificate** 從現有的 azure 金鑰保存庫新增次要群集憑證，或使用所提供的現有憑證或從新建立的自我簽署憑證建立新的 Azure 金鑰電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="b26ba-109">Use **Add-AzServiceFabricClusterCertificate** to add a secondary cluster certificate, either from an existing Azure key vault or creating a new Azure key vault using an existing certificate provided or from a new self-signed certificate created.</span></span> <span data-ttu-id="b26ba-110">如果有的話，它會覆寫次要群集。</span><span class="sxs-lookup"><span data-stu-id="b26ba-110">It will override the secondary cluster if there is any.</span></span>

## <span data-ttu-id="b26ba-111">示例</span><span class="sxs-lookup"><span data-stu-id="b26ba-111">EXAMPLES</span></span>

### <span data-ttu-id="b26ba-112">範例1</span><span class="sxs-lookup"><span data-stu-id="b26ba-112">Example 1</span></span>
```powershell
Add-AzServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' 
-SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="b26ba-113">這個命令會將現有的 Azure 金鑰保存庫中的憑證新增為次要群集憑證。</span><span class="sxs-lookup"><span data-stu-id="b26ba-113">This command will add a certificate in the existing Azure key vault as a secondary cluster certificate.</span></span>

### <span data-ttu-id="b26ba-114">範例2</span><span class="sxs-lookup"><span data-stu-id="b26ba-114">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS c:\> add-AzServiceFabricClusterCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster'  -CertificateSubjectName 'Contoso.com' 
-CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="b26ba-115">這個命令會在 Azure 金鑰保存庫中建立自我簽署憑證，並升級群集，以將它做為次要群集憑證。</span><span class="sxs-lookup"><span data-stu-id="b26ba-115">This command will create a self-signed certificate in the Azure key vault and upgrade the cluster to use it as a secondary cluster certificate.</span></span>

## <span data-ttu-id="b26ba-116">參數</span><span class="sxs-lookup"><span data-stu-id="b26ba-116">PARAMETERS</span></span>

### <span data-ttu-id="b26ba-117">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="b26ba-117">-CertificateCommonName</span></span>
<span data-ttu-id="b26ba-118">證書公用名稱</span><span class="sxs-lookup"><span data-stu-id="b26ba-118">Certificate common name</span></span>

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

### <span data-ttu-id="b26ba-119">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="b26ba-119">-CertificateFile</span></span>
<span data-ttu-id="b26ba-120">現有憑證的路徑</span><span class="sxs-lookup"><span data-stu-id="b26ba-120">The path to the existing certificate</span></span>

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

### <span data-ttu-id="b26ba-121">-CertificateIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="b26ba-121">-CertificateIssuerThumbprint</span></span>
<span data-ttu-id="b26ba-122">憑證簽發者指紋（如果有多個，則以逗號分隔）</span><span class="sxs-lookup"><span data-stu-id="b26ba-122">Certificate issuer thumbprint, separated by commas if more than one</span></span>

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

### <span data-ttu-id="b26ba-123">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="b26ba-123">-CertificateOutputFolder</span></span>
<span data-ttu-id="b26ba-124">需要下載新憑證的資料夾。</span><span class="sxs-lookup"><span data-stu-id="b26ba-124">The folder where the new certificate needs to be downloaded.</span></span>

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

### <span data-ttu-id="b26ba-125">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="b26ba-125">-CertificatePassword</span></span>
<span data-ttu-id="b26ba-126">憑證的密碼</span><span class="sxs-lookup"><span data-stu-id="b26ba-126">The password of the certificate</span></span>

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

### <span data-ttu-id="b26ba-127">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="b26ba-127">-CertificateSubjectName</span></span>
<span data-ttu-id="b26ba-128">憑證的受領人名稱</span><span class="sxs-lookup"><span data-stu-id="b26ba-128">The subject name of the certificate</span></span>

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

### <span data-ttu-id="b26ba-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b26ba-129">-DefaultProfile</span></span>
<span data-ttu-id="b26ba-130">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b26ba-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b26ba-131">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="b26ba-131">-KeyVaultName</span></span>
<span data-ttu-id="b26ba-132">如果未指定 Azure 金鑰保存庫名稱，則會預設為資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="b26ba-132">Azure key vault name, if not given it will be defaulted to the resource group name</span></span>

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

### <span data-ttu-id="b26ba-133">-KeyVaultResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b26ba-133">-KeyVaultResourceGroupName</span></span>
<span data-ttu-id="b26ba-134">Azure 金鑰電子倉庫資源群組名稱（如果未指定）會預設為 [資源] 群組名稱</span><span class="sxs-lookup"><span data-stu-id="b26ba-134">Azure key vault resource group name, if not given it will be defaulted to resource group name</span></span>

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

### <span data-ttu-id="b26ba-135">-名稱</span><span class="sxs-lookup"><span data-stu-id="b26ba-135">-Name</span></span>
<span data-ttu-id="b26ba-136">指定群集的名稱</span><span class="sxs-lookup"><span data-stu-id="b26ba-136">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="b26ba-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b26ba-137">-ResourceGroupName</span></span>
<span data-ttu-id="b26ba-138">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b26ba-138">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="b26ba-139">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="b26ba-139">-SecretIdentifier</span></span>
<span data-ttu-id="b26ba-140">現有的 Azure 金鑰保存庫機密 URL，例如 " https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f "</span><span class="sxs-lookup"><span data-stu-id="b26ba-140">The existing Azure key vault secret URL, for example 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'</span></span>

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

### <span data-ttu-id="b26ba-141">-確認</span><span class="sxs-lookup"><span data-stu-id="b26ba-141">-Confirm</span></span>
<span data-ttu-id="b26ba-142">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b26ba-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b26ba-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b26ba-143">-WhatIf</span></span>
<span data-ttu-id="b26ba-144">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b26ba-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b26ba-145">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b26ba-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b26ba-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b26ba-146">CommonParameters</span></span>
<span data-ttu-id="b26ba-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b26ba-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b26ba-148">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b26ba-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b26ba-149">輸入</span><span class="sxs-lookup"><span data-stu-id="b26ba-149">INPUTS</span></span>

### <span data-ttu-id="b26ba-150">System.object</span><span class="sxs-lookup"><span data-stu-id="b26ba-150">System.String</span></span>

### <span data-ttu-id="b26ba-151">SecureString</span><span class="sxs-lookup"><span data-stu-id="b26ba-151">System.Security.SecureString</span></span>

## <span data-ttu-id="b26ba-152">輸出</span><span class="sxs-lookup"><span data-stu-id="b26ba-152">OUTPUTS</span></span>

### <span data-ttu-id="b26ba-153">PSCluster 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="b26ba-153">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="b26ba-154">筆記</span><span class="sxs-lookup"><span data-stu-id="b26ba-154">NOTES</span></span>

## <span data-ttu-id="b26ba-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="b26ba-155">RELATED LINKS</span></span>

[<span data-ttu-id="b26ba-156">移除-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="b26ba-156">Remove-AzServiceFabricClusterCertificate</span></span>](./Remove-AzServiceFabricClusterCertificate.md)

[<span data-ttu-id="b26ba-157">新-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="b26ba-157">New-AzServiceFabricCluster</span></span>](./New-AzServiceFabricCluster.md)
