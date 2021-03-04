---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 5141D84C-3C58-42B9-890F-C3C9049BC1C5
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/set-azhdinsightclusterdiskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterDiskEncryptionKey.md
ms.openlocfilehash: addf0e06a3df625bde5b46cc8089fc89ced832dc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910090"
---
# <span data-ttu-id="5dd8c-101">Set-AzHDInsightClusterDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="5dd8c-101">Set-AzHDInsightClusterDiskEncryptionKey</span></span>

## <span data-ttu-id="5dd8c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5dd8c-102">SYNOPSIS</span></span>
<span data-ttu-id="5dd8c-103">旋轉指定 HDInsight 集的磁片加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="5dd8c-103">Rotates the disk encryption key of the specified HDInsight cluster.</span></span>

## <span data-ttu-id="5dd8c-104">語法</span><span class="sxs-lookup"><span data-stu-id="5dd8c-104">SYNTAX</span></span>

### <span data-ttu-id="5dd8c-105">SetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="5dd8c-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-ResourceGroupName] <String> [-Name] <String>
 -EncryptionKeyName <String> -EncryptionKeyVersion <String> -EncryptionVaultUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5dd8c-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5dd8c-106">SetByResourceIdParameterSet</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-ResourceId] <String> -EncryptionKeyName <String>
 -EncryptionKeyVersion <String> -EncryptionVaultUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5dd8c-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5dd8c-107">SetByInputObjectParameterSet</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-InputObject] <AzureHDInsightCluster> -EncryptionKeyName <String>
 -EncryptionKeyVersion <String> -EncryptionVaultUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5dd8c-108">描述</span><span class="sxs-lookup"><span data-stu-id="5dd8c-108">DESCRIPTION</span></span>
<span data-ttu-id="5dd8c-109">旋轉指定 HDInsight 集的磁片加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="5dd8c-109">Rotate the disk encryption key of the specified HDInsight cluster.</span></span> <span data-ttu-id="5dd8c-110">針對此作業，該組必須同時擁有目前金鑰和預定新金鑰的存取權，否則旋轉鍵作業將會失敗。</span><span class="sxs-lookup"><span data-stu-id="5dd8c-110">For this operation, the cluster must have access to both the current key and the intended new key, otherwise the rotate key operation will fail.</span></span>

## <span data-ttu-id="5dd8c-111">例子</span><span class="sxs-lookup"><span data-stu-id="5dd8c-111">EXAMPLES</span></span>

### <span data-ttu-id="5dd8c-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="5dd8c-112">Example 1</span></span>
```powershell
PS C:\> # Cluster configuration info
        $clusterResourceGroupName = "Group"
        $clusterName = "your-cmk-cluster"

Set-AzHDInsightClusterDiskEncryptionKey `
        -ResourceGroupName $clusterResourceGroupName `
        -ClusterName $clusterName `
        -EncryptionKeyName new-key `
        -EncryptionVaultUri https://MyKeyVault.vault.azure.net `
        -EncryptionKeyVersion 00000000000000000000000000000000
```

### <span data-ttu-id="5dd8c-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="5dd8c-113">Example 2</span></span>
```powershell
PS C:\> # Cluster configuration info
        $clusterName = "your-cmk-cluster"

$cluster= Get-AzHDInsightCluster -ClusterName $clusterName 
$cluster |  Set-AzHDInsightClusterDiskEncryptionKey `
    -EncryptionKeyName new-key `
    -EncryptionVaultUri https://MyKeyVault.vault.azure.net `
    -EncryptionKeyVersion 00000000000000000000000000000000
```

## <span data-ttu-id="5dd8c-114">參數</span><span class="sxs-lookup"><span data-stu-id="5dd8c-114">PARAMETERS</span></span>

### <span data-ttu-id="5dd8c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dd8c-115">-DefaultProfile</span></span>
<span data-ttu-id="5dd8c-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5dd8c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5dd8c-117">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="5dd8c-117">-EncryptionKeyName</span></span>
<span data-ttu-id="5dd8c-118">獲取或設定加密金鑰名稱。</span><span class="sxs-lookup"><span data-stu-id="5dd8c-118">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="5dd8c-119">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="5dd8c-119">-EncryptionKeyVersion</span></span>
<span data-ttu-id="5dd8c-120">獲得或設定加密金鑰版本。</span><span class="sxs-lookup"><span data-stu-id="5dd8c-120">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="5dd8c-121">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="5dd8c-121">-EncryptionVaultUri</span></span>
<span data-ttu-id="5dd8c-122">獲取或設定加密庫 uri。</span><span class="sxs-lookup"><span data-stu-id="5dd8c-122">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="5dd8c-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5dd8c-123">-InputObject</span></span>
<span data-ttu-id="5dd8c-124">獲取或設定輸入物件。</span><span class="sxs-lookup"><span data-stu-id="5dd8c-124">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5dd8c-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="5dd8c-125">-Name</span></span>
<span data-ttu-id="5dd8c-126">獲取或設定組名。</span><span class="sxs-lookup"><span data-stu-id="5dd8c-126">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dd8c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5dd8c-127">-ResourceGroupName</span></span>
<span data-ttu-id="5dd8c-128">獲取或設定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5dd8c-128">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dd8c-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5dd8c-129">-ResourceId</span></span>
<span data-ttu-id="5dd8c-130">獲取或設定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="5dd8c-130">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5dd8c-131">-確認</span><span class="sxs-lookup"><span data-stu-id="5dd8c-131">-Confirm</span></span>
<span data-ttu-id="5dd8c-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="5dd8c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5dd8c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5dd8c-133">-WhatIf</span></span>
<span data-ttu-id="5dd8c-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5dd8c-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5dd8c-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5dd8c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5dd8c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dd8c-136">CommonParameters</span></span>
<span data-ttu-id="5dd8c-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5dd8c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dd8c-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5dd8c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dd8c-139">輸入</span><span class="sxs-lookup"><span data-stu-id="5dd8c-139">INPUTS</span></span>

### <span data-ttu-id="5dd8c-140">沒有</span><span class="sxs-lookup"><span data-stu-id="5dd8c-140">None</span></span>

## <span data-ttu-id="5dd8c-141">輸出</span><span class="sxs-lookup"><span data-stu-id="5dd8c-141">OUTPUTS</span></span>

### <span data-ttu-id="5dd8c-142">Microsoft.Azure.management.HDInsight.Models.Cluster</span><span class="sxs-lookup"><span data-stu-id="5dd8c-142">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="5dd8c-143">筆記</span><span class="sxs-lookup"><span data-stu-id="5dd8c-143">NOTES</span></span>

## <span data-ttu-id="5dd8c-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="5dd8c-144">RELATED LINKS</span></span>

[<span data-ttu-id="5dd8c-145">客戶管理的金鑰磁片加密</span><span class="sxs-lookup"><span data-stu-id="5dd8c-145">Customer-managed key disk encryption</span></span>](https://docs.microsoft.com/azure/hdinsight/disk-encryption)
