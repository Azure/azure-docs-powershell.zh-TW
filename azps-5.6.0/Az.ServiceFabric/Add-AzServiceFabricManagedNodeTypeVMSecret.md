---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/add-azservicefabricmanagednodetypevmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMSecret.md
ms.openlocfilehash: 35d755bc117ccc4379be8d7344d8e7170594d555
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906370"
---
# <span data-ttu-id="cc7a4-101">Add-AzServiceFabricManagedNodeTypeVMSecret</span><span class="sxs-lookup"><span data-stu-id="cc7a4-101">Add-AzServiceFabricManagedNodeTypeVMSecret</span></span>

## <span data-ttu-id="cc7a4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="cc7a4-102">SYNOPSIS</span></span>
<span data-ttu-id="cc7a4-103">新增憑證金鑰至節點類型。</span><span class="sxs-lookup"><span data-stu-id="cc7a4-103">Add certificate secret to the node type.</span></span>

## <span data-ttu-id="cc7a4-104">語法</span><span class="sxs-lookup"><span data-stu-id="cc7a4-104">SYNTAX</span></span>

### <span data-ttu-id="cc7a4-105">ByObj (預設) </span><span class="sxs-lookup"><span data-stu-id="cc7a4-105">ByObj (Default)</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMSecret [-InputObject] <PSManagedNodeType> -SourceVaultId <String>
 -CertificateUrl <String> -CertificateStore <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc7a4-106">ByName</span><span class="sxs-lookup"><span data-stu-id="cc7a4-106">ByName</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMSecret [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> -SourceVaultId <String> -CertificateUrl <String> -CertificateStore <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc7a4-107">描述</span><span class="sxs-lookup"><span data-stu-id="cc7a4-107">DESCRIPTION</span></span>
<span data-ttu-id="cc7a4-108">新增憑證金鑰至節點類型。</span><span class="sxs-lookup"><span data-stu-id="cc7a4-108">Add certificate secret to the node type.</span></span> <span data-ttu-id="cc7a4-109">機密必須儲存在 Azure 金鑰保存庫中。</span><span class="sxs-lookup"><span data-stu-id="cc7a4-109">The secret must be stored in an Azure Key Vault.</span></span> <span data-ttu-id="cc7a4-110">有關金鑰庫的資訊，請參閱什麼是 Azure 金鑰庫？</span><span class="sxs-lookup"><span data-stu-id="cc7a4-110">For more information relating to Key Vault, see What is Azure Key Vault?</span></span> <span data-ttu-id="cc7a4-111">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span><span class="sxs-lookup"><span data-stu-id="cc7a4-111">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span> <span data-ttu-id="cc7a4-112">有關 Cmdlet 的資訊，請參閱 Microsoft 開發人員網路 (或 Cmdlet 中的 Azure Key Vault https://msdn.microsoft.com/library/azure/dn868052.aspx) Cmdlet Set-AzKeyVaultSecret Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cc7a4-112">For more information about the cmdlets, see Azure Key Vault Cmdlets (https://msdn.microsoft.com/library/azure/dn868052.aspx) in the Microsoft Developer Network library or the Set-AzKeyVaultSecret cmdlet.</span></span>

## <span data-ttu-id="cc7a4-113">例子</span><span class="sxs-lookup"><span data-stu-id="cc7a4-113">EXAMPLES</span></span>

### <span data-ttu-id="cc7a4-114">範例 1</span><span class="sxs-lookup"><span data-stu-id="cc7a4-114">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Add-AzServiceFabricManagedNodeTypeVMSecret -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -SourceVaultId /subscriptions/XXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/testRG/providers/Microsoft.KeyVault/vaults/testkv -CertificateUrl https://testskv.vault.azure.net:443/secrets/TestCert/xxxxxxxxxxxxxxxxxxxxxxxx -CertificateStore My -Verbose
```

<span data-ttu-id="cc7a4-115">這個逗號會新增來自 keyvault 和指定之機密識別碼的憑證機密。</span><span class="sxs-lookup"><span data-stu-id="cc7a4-115">This commad adds a certificate secret from the keyvault and secret identifier specified.</span></span>

### <span data-ttu-id="cc7a4-116">範例 2</span><span class="sxs-lookup"><span data-stu-id="cc7a4-116">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Add-AzServiceFabricManagedNodeTypeVMSecret -SourceVaultId /subscriptions/XXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/testRG/providers/Microsoft.KeyVault/vaults/testkv -CertificateUrl https://testskv.vault.azure.net:443/secrets/TestCert/xxxxxxxxxxxxxxxxxxxxxxxx -CertificateStore My -Verbose
```

<span data-ttu-id="cc7a4-117">這個逗號會新增 Keyvault 的憑證機密，以及指定的密碼識別碼，以及管道。</span><span class="sxs-lookup"><span data-stu-id="cc7a4-117">This commad adds a certificate secret from the keyvault and secret identifier specified, with piping.</span></span>

## <span data-ttu-id="cc7a4-118">參數</span><span class="sxs-lookup"><span data-stu-id="cc7a4-118">PARAMETERS</span></span>

### <span data-ttu-id="cc7a4-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cc7a4-119">-AsJob</span></span>
<span data-ttu-id="cc7a4-120">在背景中執行 Cmdlet 並返回工作以追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="cc7a4-120">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="cc7a4-121">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="cc7a4-121">-CertificateStore</span></span>
<span data-ttu-id="cc7a4-122">指定要新增憑證的虛擬機器上的憑證存放區。</span><span class="sxs-lookup"><span data-stu-id="cc7a4-122">Specifies the certificate store on the Virtual Machine to which the certificate should be added.</span></span>
<span data-ttu-id="cc7a4-123">指定的憑證存放區在 LocalMachine 帳戶中是隱含的。</span><span class="sxs-lookup"><span data-stu-id="cc7a4-123">The specified certificate store is implicitly in the LocalMachine account.</span></span>

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

### <span data-ttu-id="cc7a4-124">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="cc7a4-124">-CertificateUrl</span></span>
<span data-ttu-id="cc7a4-125">這是憑證的 URL，已上傳至金鑰庫作為機密。</span><span class="sxs-lookup"><span data-stu-id="cc7a4-125">This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>
<span data-ttu-id="cc7a4-126">若要新增金鑰庫的機密，請參閱新增金鑰或金鑰至金鑰 \[ 庫 \] https://docs.microsoft.com/azure/key-vault/key-vault-get-started/#add) (。</span><span class="sxs-lookup"><span data-stu-id="cc7a4-126">For adding a secret to the Key Vault, see \[Add a key or secret to the key vault\](https://docs.microsoft.com/azure/key-vault/key-vault-get-started/#add).</span></span>
<span data-ttu-id="cc7a4-127">在此案例中，您的憑證必須採用下列 JSON 物件的 Base64 編碼，此編碼方式為 UTF-8：{ \<br\> \<br\> \<br\> "data"：" \<Base64-encoded-certificate\> "， \<br\> "dataType"："pfx"， \<br\> "password"：" \<pfx-file-password\> " \<br\> }/</span><span class="sxs-lookup"><span data-stu-id="cc7a4-127">In this case, your certificate needs to be It is the Base64 encoding of the following JSON Object which is encoded in UTF-8: \<br\>\<br\> {\<br\>  "data":"\<Base64-encoded-certificate\>",\<br\>  "dataType":"pfx",\<br\>  "password":"\<pfx-file-password\>"\<br\>}/</span></span>

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

### <span data-ttu-id="cc7a4-128">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="cc7a4-128">-ClusterName</span></span>
<span data-ttu-id="cc7a4-129">指定組名。</span><span class="sxs-lookup"><span data-stu-id="cc7a4-129">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="cc7a4-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc7a4-130">-DefaultProfile</span></span>
<span data-ttu-id="cc7a4-131">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="cc7a4-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc7a4-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cc7a4-132">-InputObject</span></span>
<span data-ttu-id="cc7a4-133">節點類型資源</span><span class="sxs-lookup"><span data-stu-id="cc7a4-133">Node Type resource</span></span>

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

### <span data-ttu-id="cc7a4-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="cc7a4-134">-Name</span></span>
<span data-ttu-id="cc7a4-135">指定節點類型的名稱。</span><span class="sxs-lookup"><span data-stu-id="cc7a4-135">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="cc7a4-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc7a4-136">-ResourceGroupName</span></span>
<span data-ttu-id="cc7a4-137">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cc7a4-137">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="cc7a4-138">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="cc7a4-138">-SourceVaultId</span></span>
<span data-ttu-id="cc7a4-139">包含憑證的 Key Vault 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="cc7a4-139">Key Vault resource id containing the certificates.</span></span>

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

### <span data-ttu-id="cc7a4-140">-確認</span><span class="sxs-lookup"><span data-stu-id="cc7a4-140">-Confirm</span></span>
<span data-ttu-id="cc7a4-141">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="cc7a4-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc7a4-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc7a4-142">-WhatIf</span></span>
<span data-ttu-id="cc7a4-143">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cc7a4-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc7a4-144">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cc7a4-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc7a4-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc7a4-145">CommonParameters</span></span>
<span data-ttu-id="cc7a4-146">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="cc7a4-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc7a4-147">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cc7a4-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc7a4-148">輸入</span><span class="sxs-lookup"><span data-stu-id="cc7a4-148">INPUTS</span></span>

### <span data-ttu-id="cc7a4-149">System.String</span><span class="sxs-lookup"><span data-stu-id="cc7a4-149">System.String</span></span>

## <span data-ttu-id="cc7a4-150">輸出</span><span class="sxs-lookup"><span data-stu-id="cc7a4-150">OUTPUTS</span></span>

### <span data-ttu-id="cc7a4-151">Microsoft.Azure.Commands.ServiceFabric.models.PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="cc7a4-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="cc7a4-152">筆記</span><span class="sxs-lookup"><span data-stu-id="cc7a4-152">NOTES</span></span>

## <span data-ttu-id="cc7a4-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="cc7a4-153">RELATED LINKS</span></span>
