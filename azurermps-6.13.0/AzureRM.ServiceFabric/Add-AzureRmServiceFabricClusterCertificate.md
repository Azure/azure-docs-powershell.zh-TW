---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/add-azurermservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricClusterCertificate.md
ms.openlocfilehash: fa357a4f5b8e599858ce5aff3e0aa11121833ba1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449730"
---
# <span data-ttu-id="bb288-101">Add-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="bb288-101">Add-AzureRmServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="bb288-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bb288-102">SYNOPSIS</span></span>
<span data-ttu-id="bb288-103">將次要群集憑證新增至群集。</span><span class="sxs-lookup"><span data-stu-id="bb288-103">Add a secondary cluster certificate to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb288-104">句法</span><span class="sxs-lookup"><span data-stu-id="bb288-104">SYNTAX</span></span>

### <span data-ttu-id="bb288-105">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="bb288-105">ByExistingKeyVault</span></span>
```
Add-AzureRmServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 -SecretIdentifier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bb288-106">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="bb288-106">ByNewPfxAndVaultName</span></span>
```
Add-AzureRmServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb288-107">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="bb288-107">ByExistingPfxAndVaultName</span></span>
```
Add-AzureRmServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bb288-108">說明</span><span class="sxs-lookup"><span data-stu-id="bb288-108">DESCRIPTION</span></span>
<span data-ttu-id="bb288-109">使用 **AzureRmServiceFabricClusterCertificate** 從現有的 azure 金鑰保存庫新增次要群集憑證，或使用所提供的現有憑證或從新建立的自我簽署憑證建立新的 Azure 金鑰電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="bb288-109">Use **Add-AzureRmServiceFabricClusterCertificate** to add a secondary cluster certificate, either from an existing Azure key vault or creating a new Azure key vault using an existing certificate provided or from a new self-signed certificate created.</span></span> <span data-ttu-id="bb288-110">如果有的話，它會覆寫次要群集。</span><span class="sxs-lookup"><span data-stu-id="bb288-110">It will override the secondary cluster if there is any.</span></span>

## <span data-ttu-id="bb288-111">示例</span><span class="sxs-lookup"><span data-stu-id="bb288-111">EXAMPLES</span></span>

### <span data-ttu-id="bb288-112">範例1</span><span class="sxs-lookup"><span data-stu-id="bb288-112">Example 1</span></span>
```
Add-AzureRmServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' 
-SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="bb288-113">這個命令會將現有的 Azure 金鑰保存庫中的憑證新增為次要群集憑證。</span><span class="sxs-lookup"><span data-stu-id="bb288-113">This command will add a certificate in the existing Azure key vault as a secondary cluster certificate.</span></span>

### <span data-ttu-id="bb288-114">範例2</span><span class="sxs-lookup"><span data-stu-id="bb288-114">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS c:\> add-AzureRmServiceFabricClusterCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster'  -CertificateSubjectName 'Contoso.com' 
-CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="bb288-115">這個命令會在 Azure 金鑰保存庫中建立自我簽署憑證，並升級群集，以將它做為次要群集憑證。</span><span class="sxs-lookup"><span data-stu-id="bb288-115">This command will create a self-signed certificate in the Azure key vault and upgrade the cluster to use it as a secondary cluster certificate.</span></span>

## <span data-ttu-id="bb288-116">參數</span><span class="sxs-lookup"><span data-stu-id="bb288-116">PARAMETERS</span></span>

### <span data-ttu-id="bb288-117">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="bb288-117">-CertificateFile</span></span>
<span data-ttu-id="bb288-118">現有的憑證檔路徑。</span><span class="sxs-lookup"><span data-stu-id="bb288-118">The existing certificate file path.</span></span>

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

### <span data-ttu-id="bb288-119">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="bb288-119">-CertificateOutputFolder</span></span>
<span data-ttu-id="bb288-120">要建立之新憑證的資料夾。</span><span class="sxs-lookup"><span data-stu-id="bb288-120">The folder of the new certificate to be created.</span></span>

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

### <span data-ttu-id="bb288-121">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="bb288-121">-CertificatePassword</span></span>
<span data-ttu-id="bb288-122">憑證檔案的密碼。</span><span class="sxs-lookup"><span data-stu-id="bb288-122">The password of the certificate file.</span></span>

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

### <span data-ttu-id="bb288-123">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="bb288-123">-CertificateSubjectName</span></span>
<span data-ttu-id="bb288-124">要建立之憑證的 Dns 名稱。</span><span class="sxs-lookup"><span data-stu-id="bb288-124">The Dns name of the certificate to be created.</span></span>

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

### <span data-ttu-id="bb288-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb288-125">-DefaultProfile</span></span>
<span data-ttu-id="bb288-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bb288-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb288-127">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="bb288-127">-KeyVaultName</span></span>
<span data-ttu-id="bb288-128">Azure 金鑰保存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="bb288-128">Azure key vault name.</span></span>

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

### <span data-ttu-id="bb288-129">-KeyVaultResouceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb288-129">-KeyVaultResouceGroupName</span></span>
<span data-ttu-id="bb288-130">Azure 金鑰電子倉庫資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="bb288-130">Azure key vault resource group name.</span></span>

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

### <span data-ttu-id="bb288-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="bb288-131">-Name</span></span>
<span data-ttu-id="bb288-132">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="bb288-132">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="bb288-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb288-133">-ResourceGroupName</span></span>
<span data-ttu-id="bb288-134">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bb288-134">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="bb288-135">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="bb288-135">-SecretIdentifier</span></span>
<span data-ttu-id="bb288-136">現有的 Azure 金鑰保存庫機密 Url。</span><span class="sxs-lookup"><span data-stu-id="bb288-136">The existing Azure key vault secret Url.</span></span>

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

### <span data-ttu-id="bb288-137">-確認</span><span class="sxs-lookup"><span data-stu-id="bb288-137">-Confirm</span></span>
<span data-ttu-id="bb288-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bb288-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb288-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb288-139">-WhatIf</span></span>
<span data-ttu-id="bb288-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bb288-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bb288-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bb288-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb288-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb288-142">CommonParameters</span></span>
<span data-ttu-id="bb288-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bb288-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb288-144">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bb288-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb288-145">輸入</span><span class="sxs-lookup"><span data-stu-id="bb288-145">INPUTS</span></span>

### <span data-ttu-id="bb288-146">System.object</span><span class="sxs-lookup"><span data-stu-id="bb288-146">System.String</span></span>
<span data-ttu-id="bb288-147">參數： CertificateFile (ByValue) 、CertificateOutputFolder (ByValue) 、CertificateSubjectName (ByValue) 、KeyVaultName (ByValue) 、KeyVaultResouceGroupName (ByValue) 、SecretIdentifier (ByValue) </span><span class="sxs-lookup"><span data-stu-id="bb288-147">Parameters: CertificateFile (ByValue), CertificateOutputFolder (ByValue), CertificateSubjectName (ByValue), KeyVaultName (ByValue), KeyVaultResouceGroupName (ByValue), SecretIdentifier (ByValue)</span></span>

### <span data-ttu-id="bb288-148">SecureString</span><span class="sxs-lookup"><span data-stu-id="bb288-148">System.Security.SecureString</span></span>
<span data-ttu-id="bb288-149">參數： CertificatePassword (ByValue) </span><span class="sxs-lookup"><span data-stu-id="bb288-149">Parameters: CertificatePassword (ByValue)</span></span>

## <span data-ttu-id="bb288-150">輸出</span><span class="sxs-lookup"><span data-stu-id="bb288-150">OUTPUTS</span></span>

### <span data-ttu-id="bb288-151">PSCluster 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="bb288-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="bb288-152">筆記</span><span class="sxs-lookup"><span data-stu-id="bb288-152">NOTES</span></span>

## <span data-ttu-id="bb288-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="bb288-153">RELATED LINKS</span></span>

[<span data-ttu-id="bb288-154">移除-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="bb288-154">Remove-AzureRmServiceFabricClusterCertificate</span></span>](./Remove-AzureRmServiceFabricClusterCertificate.md)

[<span data-ttu-id="bb288-155">新-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="bb288-155">New-AzureRmServiceFabricCluster</span></span>](./New-AzureRmServiceFabricCluster.md)

[<span data-ttu-id="bb288-156">附加 AzureRmServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="bb288-156">Add-AzureRmServiceFabricApplicationCertificate</span></span>](./Add-AzureRmServiceFabricApplicationCertificate.md)