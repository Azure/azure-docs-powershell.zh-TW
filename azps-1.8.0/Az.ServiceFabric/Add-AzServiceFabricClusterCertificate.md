---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClusterCertificate.md
ms.openlocfilehash: bf96b4a21e12e41ce067d669b50c05831a162a8b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620571"
---
# <span data-ttu-id="b0580-101">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="b0580-101">Add-AzServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="b0580-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b0580-102">SYNOPSIS</span></span>
<span data-ttu-id="b0580-103">將次要群集憑證新增至群集。</span><span class="sxs-lookup"><span data-stu-id="b0580-103">Add a secondary cluster certificate to the cluster.</span></span>

## <span data-ttu-id="b0580-104">句法</span><span class="sxs-lookup"><span data-stu-id="b0580-104">SYNTAX</span></span>

### <span data-ttu-id="b0580-105">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="b0580-105">ByExistingKeyVault</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String> -SecretIdentifier <String>
 [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0580-106">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="b0580-106">ByNewPfxAndVaultName</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0580-107">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="b0580-107">ByExistingPfxAndVaultName</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-CertificateCommonName <String>]
 [-CertificateIssuerThumbprint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b0580-108">說明</span><span class="sxs-lookup"><span data-stu-id="b0580-108">DESCRIPTION</span></span>
<span data-ttu-id="b0580-109">使用 **AzServiceFabricClusterCertificate** 從現有的 azure 金鑰保存庫新增次要群集憑證，或使用所提供的現有憑證或從新建立的自我簽署憑證建立新的 Azure 金鑰電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="b0580-109">Use **Add-AzServiceFabricClusterCertificate** to add a secondary cluster certificate, either from an existing Azure key vault or creating a new Azure key vault using an existing certificate provided or from a new self-signed certificate created.</span></span> <span data-ttu-id="b0580-110">如果有的話，它會覆寫次要群集。</span><span class="sxs-lookup"><span data-stu-id="b0580-110">It will override the secondary cluster if there is any.</span></span>

## <span data-ttu-id="b0580-111">示例</span><span class="sxs-lookup"><span data-stu-id="b0580-111">EXAMPLES</span></span>

### <span data-ttu-id="b0580-112">範例1</span><span class="sxs-lookup"><span data-stu-id="b0580-112">Example 1</span></span>
```
Add-AzServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' 
-SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="b0580-113">這個命令會將現有的 Azure 金鑰保存庫中的憑證新增為次要群集憑證。</span><span class="sxs-lookup"><span data-stu-id="b0580-113">This command will add a certificate in the existing Azure key vault as a secondary cluster certificate.</span></span>

### <span data-ttu-id="b0580-114">範例2</span><span class="sxs-lookup"><span data-stu-id="b0580-114">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS c:\> add-AzServiceFabricClusterCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster'  -CertificateSubjectName 'Contoso.com' 
-CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="b0580-115">這個命令會在 Azure 金鑰保存庫中建立自我簽署憑證，並升級群集，以將它做為次要群集憑證。</span><span class="sxs-lookup"><span data-stu-id="b0580-115">This command will create a self-signed certificate in the Azure key vault and upgrade the cluster to use it as a secondary cluster certificate.</span></span>

## <span data-ttu-id="b0580-116">參數</span><span class="sxs-lookup"><span data-stu-id="b0580-116">PARAMETERS</span></span>

### <span data-ttu-id="b0580-117">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="b0580-117">-CertificateCommonName</span></span>
<span data-ttu-id="b0580-118">證書公用名稱</span><span class="sxs-lookup"><span data-stu-id="b0580-118">Certificate common name</span></span>

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

### <span data-ttu-id="b0580-119">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="b0580-119">-CertificateFile</span></span>
<span data-ttu-id="b0580-120">現有的憑證檔路徑。</span><span class="sxs-lookup"><span data-stu-id="b0580-120">The existing certificate file path.</span></span>

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

### <span data-ttu-id="b0580-121">-CertificateIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="b0580-121">-CertificateIssuerThumbprint</span></span>
<span data-ttu-id="b0580-122">憑證簽發者指紋（如果有多個，則以逗號分隔）</span><span class="sxs-lookup"><span data-stu-id="b0580-122">Certificate issuer thumbprint, separated by commas if more than one</span></span>

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

### <span data-ttu-id="b0580-123">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="b0580-123">-CertificateOutputFolder</span></span>
<span data-ttu-id="b0580-124">要建立之新憑證的資料夾。</span><span class="sxs-lookup"><span data-stu-id="b0580-124">The folder of the new certificate to be created.</span></span>

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

### <span data-ttu-id="b0580-125">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="b0580-125">-CertificatePassword</span></span>
<span data-ttu-id="b0580-126">憑證檔案的密碼。</span><span class="sxs-lookup"><span data-stu-id="b0580-126">The password of the certificate file.</span></span>

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

### <span data-ttu-id="b0580-127">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="b0580-127">-CertificateSubjectName</span></span>
<span data-ttu-id="b0580-128">要建立之憑證的 Dns 名稱。</span><span class="sxs-lookup"><span data-stu-id="b0580-128">The Dns name of the certificate to be created.</span></span>

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

### <span data-ttu-id="b0580-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0580-129">-DefaultProfile</span></span>
<span data-ttu-id="b0580-130">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b0580-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0580-131">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="b0580-131">-KeyVaultName</span></span>
<span data-ttu-id="b0580-132">Azure 金鑰保存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="b0580-132">Azure key vault name.</span></span>

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

### <span data-ttu-id="b0580-133">-KeyVaultResouceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0580-133">-KeyVaultResouceGroupName</span></span>
<span data-ttu-id="b0580-134">Azure 金鑰電子倉庫資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="b0580-134">Azure key vault resource group name.</span></span>

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

### <span data-ttu-id="b0580-135">-名稱</span><span class="sxs-lookup"><span data-stu-id="b0580-135">-Name</span></span>
<span data-ttu-id="b0580-136">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="b0580-136">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="b0580-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0580-137">-ResourceGroupName</span></span>
<span data-ttu-id="b0580-138">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b0580-138">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="b0580-139">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="b0580-139">-SecretIdentifier</span></span>
<span data-ttu-id="b0580-140">現有的 Azure 金鑰保存庫機密 Url。</span><span class="sxs-lookup"><span data-stu-id="b0580-140">The existing Azure key vault secret Url.</span></span>

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

### <span data-ttu-id="b0580-141">-確認</span><span class="sxs-lookup"><span data-stu-id="b0580-141">-Confirm</span></span>
<span data-ttu-id="b0580-142">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b0580-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0580-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0580-143">-WhatIf</span></span>
<span data-ttu-id="b0580-144">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b0580-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b0580-145">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b0580-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0580-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0580-146">CommonParameters</span></span>
<span data-ttu-id="b0580-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b0580-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0580-148">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b0580-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0580-149">輸入</span><span class="sxs-lookup"><span data-stu-id="b0580-149">INPUTS</span></span>

### <span data-ttu-id="b0580-150">System.object</span><span class="sxs-lookup"><span data-stu-id="b0580-150">System.String</span></span>

### <span data-ttu-id="b0580-151">SecureString</span><span class="sxs-lookup"><span data-stu-id="b0580-151">System.Security.SecureString</span></span>

## <span data-ttu-id="b0580-152">輸出</span><span class="sxs-lookup"><span data-stu-id="b0580-152">OUTPUTS</span></span>

### <span data-ttu-id="b0580-153">PSCluster 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="b0580-153">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="b0580-154">筆記</span><span class="sxs-lookup"><span data-stu-id="b0580-154">NOTES</span></span>

## <span data-ttu-id="b0580-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="b0580-155">RELATED LINKS</span></span>

[<span data-ttu-id="b0580-156">移除-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="b0580-156">Remove-AzServiceFabricClusterCertificate</span></span>](./Remove-AzServiceFabricClusterCertificate.md)

[<span data-ttu-id="b0580-157">新-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="b0580-157">New-AzServiceFabricCluster</span></span>](./New-AzServiceFabricCluster.md)

[<span data-ttu-id="b0580-158">附加 AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="b0580-158">Add-AzServiceFabricApplicationCertificate</span></span>](./Add-AzServiceFabricApplicationCertificate.md)
