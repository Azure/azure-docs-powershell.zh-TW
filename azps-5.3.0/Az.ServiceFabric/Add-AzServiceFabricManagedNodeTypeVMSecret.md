---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricmanagednodetypevmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMSecret.md
ms.openlocfilehash: 36ed679066d1850851ff0e90f39eb6f9ef8ffa1a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98448284"
---
# <span data-ttu-id="e81f0-101">Add-AzServiceFabricManagedNodeTypeVMSecret</span><span class="sxs-lookup"><span data-stu-id="e81f0-101">Add-AzServiceFabricManagedNodeTypeVMSecret</span></span>

## <span data-ttu-id="e81f0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e81f0-102">SYNOPSIS</span></span>
<span data-ttu-id="e81f0-103">將憑證機密新增至節點類型。</span><span class="sxs-lookup"><span data-stu-id="e81f0-103">Add certificate secret to the node type.</span></span>

## <span data-ttu-id="e81f0-104">句法</span><span class="sxs-lookup"><span data-stu-id="e81f0-104">SYNTAX</span></span>

### <span data-ttu-id="e81f0-105">ByObj (預設) </span><span class="sxs-lookup"><span data-stu-id="e81f0-105">ByObj (Default)</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMSecret [-InputObject] <PSManagedNodeType> -SourceVaultId <String>
 -CertificateUrl <String> -CertificateStore <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e81f0-106">ByName</span><span class="sxs-lookup"><span data-stu-id="e81f0-106">ByName</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMSecret [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> -SourceVaultId <String> -CertificateUrl <String> -CertificateStore <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e81f0-107">說明</span><span class="sxs-lookup"><span data-stu-id="e81f0-107">DESCRIPTION</span></span>
<span data-ttu-id="e81f0-108">將憑證機密新增至節點類型。</span><span class="sxs-lookup"><span data-stu-id="e81f0-108">Add certificate secret to the node type.</span></span> <span data-ttu-id="e81f0-109">密碼必須儲存在 Azure 金鑰保存庫中。</span><span class="sxs-lookup"><span data-stu-id="e81f0-109">The secret must be stored in an Azure Key Vault.</span></span> <span data-ttu-id="e81f0-110">如需與主要保存庫相關的詳細資訊，請參閱何謂 Azure 金鑰保存庫？</span><span class="sxs-lookup"><span data-stu-id="e81f0-110">For more information relating to Key Vault, see What is Azure Key Vault?</span></span> <span data-ttu-id="e81f0-111">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span><span class="sxs-lookup"><span data-stu-id="e81f0-111">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span> <span data-ttu-id="e81f0-112">如需有關 Cmdlet 的詳細資訊，請參閱 https://msdn.microsoft.com/library/azure/dn868052.aspx) Microsoft 開發人員網路文件庫中的 Azure 金鑰保存庫 Cmdlet (或 Set-AzKeyVaultSecret Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e81f0-112">For more information about the cmdlets, see Azure Key Vault Cmdlets (https://msdn.microsoft.com/library/azure/dn868052.aspx) in the Microsoft Developer Network library or the Set-AzKeyVaultSecret cmdlet.</span></span>

## <span data-ttu-id="e81f0-113">示例</span><span class="sxs-lookup"><span data-stu-id="e81f0-113">EXAMPLES</span></span>

### <span data-ttu-id="e81f0-114">範例1</span><span class="sxs-lookup"><span data-stu-id="e81f0-114">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Add-AzServiceFabricManagedNodeTypeVMSecret -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -SourceVaultId /subscriptions/XXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/testRG/providers/Microsoft.KeyVault/vaults/testkv -CertificateUrl https://testskv.vault.azure.net:443/secrets/TestCert/xxxxxxxxxxxxxxxxxxxxxxxx -CertificateStore My -Verbose
```

<span data-ttu-id="e81f0-115">此 commad 會從指定的 keyvault 和秘密識別碼新增憑證機密。</span><span class="sxs-lookup"><span data-stu-id="e81f0-115">This commad adds a certificate secret from the keyvault and secret identifier specified.</span></span>

### <span data-ttu-id="e81f0-116">範例2</span><span class="sxs-lookup"><span data-stu-id="e81f0-116">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Add-AzServiceFabricManagedNodeTypeVMSecret -SourceVaultId /subscriptions/XXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/testRG/providers/Microsoft.KeyVault/vaults/testkv -CertificateUrl https://testskv.vault.azure.net:443/secrets/TestCert/xxxxxxxxxxxxxxxxxxxxxxxx -CertificateStore My -Verbose
```

<span data-ttu-id="e81f0-117">這個 commad 會從指定的 keyvault 和秘密識別碼（含管道）新增憑證機密。</span><span class="sxs-lookup"><span data-stu-id="e81f0-117">This commad adds a certificate secret from the keyvault and secret identifier specified, with piping.</span></span>

## <span data-ttu-id="e81f0-118">參數</span><span class="sxs-lookup"><span data-stu-id="e81f0-118">PARAMETERS</span></span>

### <span data-ttu-id="e81f0-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e81f0-119">-AsJob</span></span>
<span data-ttu-id="e81f0-120">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="e81f0-120">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e81f0-121">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="e81f0-121">-CertificateStore</span></span>
<span data-ttu-id="e81f0-122">指定要新增憑證的虛擬機器上的憑證存放區。</span><span class="sxs-lookup"><span data-stu-id="e81f0-122">Specifies the certificate store on the Virtual Machine to which the certificate should be added.</span></span>
<span data-ttu-id="e81f0-123">已在 LocalMachine 帳戶中隱式指定的憑證存放區。</span><span class="sxs-lookup"><span data-stu-id="e81f0-123">The specified certificate store is implicitly in the LocalMachine account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e81f0-124">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="e81f0-124">-CertificateUrl</span></span>
<span data-ttu-id="e81f0-125">這是已上傳到金鑰保存庫的憑證 URL （密碼）。</span><span class="sxs-lookup"><span data-stu-id="e81f0-125">This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>
<span data-ttu-id="e81f0-126">若要在金鑰保存庫中新增機密，請參閱 \[ 在金鑰保存庫 (新增金鑰或密碼 \] https://docs.microsoft.com/azure/key-vault/key-vault-get-started/#add) 。</span><span class="sxs-lookup"><span data-stu-id="e81f0-126">For adding a secret to the Key Vault, see \[Add a key or secret to the key vault\](https://docs.microsoft.com/azure/key-vault/key-vault-get-started/#add).</span></span>
<span data-ttu-id="e81f0-127">在這種情況下，您的憑證必須是下列 JSON 物件的 Base64 編碼，該物件是以 utf-8 編碼： \<br\> \<br\> { \<br\> "data"： " \<Base64-encoded-certificate\> "， \<br\> "資料類型"： "pfx"， \<br\> "password"： " \<pfx-file-password\> " \<br\> }/</span><span class="sxs-lookup"><span data-stu-id="e81f0-127">In this case, your certificate needs to be It is the Base64 encoding of the following JSON Object which is encoded in UTF-8: \<br\>\<br\> {\<br\>  "data":"\<Base64-encoded-certificate\>",\<br\>  "dataType":"pfx",\<br\>  "password":"\<pfx-file-password\>"\<br\>}/</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e81f0-128">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="e81f0-128">-ClusterName</span></span>
<span data-ttu-id="e81f0-129">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="e81f0-129">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e81f0-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e81f0-130">-DefaultProfile</span></span>
<span data-ttu-id="e81f0-131">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e81f0-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e81f0-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e81f0-132">-InputObject</span></span>
<span data-ttu-id="e81f0-133">節點類型資源</span><span class="sxs-lookup"><span data-stu-id="e81f0-133">Node Type resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType
Parameter Sets: ByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e81f0-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="e81f0-134">-Name</span></span>
<span data-ttu-id="e81f0-135">指定節點類型的名稱。</span><span class="sxs-lookup"><span data-stu-id="e81f0-135">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: NodeTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e81f0-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e81f0-136">-ResourceGroupName</span></span>
<span data-ttu-id="e81f0-137">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e81f0-137">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e81f0-138">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="e81f0-138">-SourceVaultId</span></span>
<span data-ttu-id="e81f0-139">包含憑證的主要保存庫資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e81f0-139">Key Vault resource id containing the certificates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e81f0-140">-確認</span><span class="sxs-lookup"><span data-stu-id="e81f0-140">-Confirm</span></span>
<span data-ttu-id="e81f0-141">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e81f0-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e81f0-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e81f0-142">-WhatIf</span></span>
<span data-ttu-id="e81f0-143">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e81f0-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e81f0-144">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e81f0-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e81f0-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e81f0-145">CommonParameters</span></span>
<span data-ttu-id="e81f0-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e81f0-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e81f0-147">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e81f0-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e81f0-148">輸入</span><span class="sxs-lookup"><span data-stu-id="e81f0-148">INPUTS</span></span>

### <span data-ttu-id="e81f0-149">System.object</span><span class="sxs-lookup"><span data-stu-id="e81f0-149">System.String</span></span>

## <span data-ttu-id="e81f0-150">輸出</span><span class="sxs-lookup"><span data-stu-id="e81f0-150">OUTPUTS</span></span>

### <span data-ttu-id="e81f0-151">PSManagedNodeType 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="e81f0-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="e81f0-152">筆記</span><span class="sxs-lookup"><span data-stu-id="e81f0-152">NOTES</span></span>

## <span data-ttu-id="e81f0-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="e81f0-153">RELATED LINKS</span></span>
