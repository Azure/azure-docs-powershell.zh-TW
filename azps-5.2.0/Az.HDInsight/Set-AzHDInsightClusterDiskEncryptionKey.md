---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 5141D84C-3C58-42B9-890F-C3C9049BC1C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightclusterdiskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterDiskEncryptionKey.md
ms.openlocfilehash: b3421fa4382912d11a3e3a28b81acffb7be123a2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98273188"
---
# <span data-ttu-id="08d2c-101">Set-AzHDInsightClusterDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="08d2c-101">Set-AzHDInsightClusterDiskEncryptionKey</span></span>

## <span data-ttu-id="08d2c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="08d2c-102">SYNOPSIS</span></span>
<span data-ttu-id="08d2c-103">旋轉指定 HDInsight 群集的磁片加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="08d2c-103">Rotates the disk encryption key of the specified HDInsight cluster.</span></span>

## <span data-ttu-id="08d2c-104">句法</span><span class="sxs-lookup"><span data-stu-id="08d2c-104">SYNTAX</span></span>

### <span data-ttu-id="08d2c-105">SetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="08d2c-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-ResourceGroupName] <String> [-Name] <String>
 -EncryptionKeyName <String> -EncryptionKeyVersion <String> -EncryptionVaultUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08d2c-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="08d2c-106">SetByResourceIdParameterSet</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-ResourceId] <String> -EncryptionKeyName <String>
 -EncryptionKeyVersion <String> -EncryptionVaultUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08d2c-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="08d2c-107">SetByInputObjectParameterSet</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-InputObject] <AzureHDInsightCluster> -EncryptionKeyName <String>
 -EncryptionKeyVersion <String> -EncryptionVaultUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08d2c-108">說明</span><span class="sxs-lookup"><span data-stu-id="08d2c-108">DESCRIPTION</span></span>
<span data-ttu-id="08d2c-109">旋轉指定 HDInsight 群集的磁片加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="08d2c-109">Rotate the disk encryption key of the specified HDInsight cluster.</span></span> <span data-ttu-id="08d2c-110">在這個作業中，群集必須同時擁有目前的金鑰和預期的新金鑰的存取權，否則旋轉鍵作業將無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="08d2c-110">For this operation, the cluster must have access to both the current key and the intended new key, otherwise the rotate key operation will fail.</span></span>

## <span data-ttu-id="08d2c-111">示例</span><span class="sxs-lookup"><span data-stu-id="08d2c-111">EXAMPLES</span></span>

### <span data-ttu-id="08d2c-112">範例1</span><span class="sxs-lookup"><span data-stu-id="08d2c-112">Example 1</span></span>
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

### <span data-ttu-id="08d2c-113">範例2</span><span class="sxs-lookup"><span data-stu-id="08d2c-113">Example 2</span></span>
```powershell
PS C:\> # Cluster configuration info
        $clusterName = "your-cmk-cluster"

$cluster= Get-AzHDInsightCluster -ClusterName $clusterName 
$cluster |  Set-AzHDInsightClusterDiskEncryptionKey `
    -EncryptionKeyName new-key `
    -EncryptionVaultUri https://MyKeyVault.vault.azure.net `
    -EncryptionKeyVersion 00000000000000000000000000000000
```

## <span data-ttu-id="08d2c-114">參數</span><span class="sxs-lookup"><span data-stu-id="08d2c-114">PARAMETERS</span></span>

### <span data-ttu-id="08d2c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08d2c-115">-DefaultProfile</span></span>
<span data-ttu-id="08d2c-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="08d2c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08d2c-117">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="08d2c-117">-EncryptionKeyName</span></span>
<span data-ttu-id="08d2c-118">取得或設定加密金鑰名稱。</span><span class="sxs-lookup"><span data-stu-id="08d2c-118">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="08d2c-119">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="08d2c-119">-EncryptionKeyVersion</span></span>
<span data-ttu-id="08d2c-120">取得或設定加密金鑰版本。</span><span class="sxs-lookup"><span data-stu-id="08d2c-120">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="08d2c-121">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="08d2c-121">-EncryptionVaultUri</span></span>
<span data-ttu-id="08d2c-122">取得或設定加密 vault uri。</span><span class="sxs-lookup"><span data-stu-id="08d2c-122">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="08d2c-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="08d2c-123">-InputObject</span></span>
<span data-ttu-id="08d2c-124">取得或設定輸入物件。</span><span class="sxs-lookup"><span data-stu-id="08d2c-124">Gets or sets the input object.</span></span>

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

### <span data-ttu-id="08d2c-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="08d2c-125">-Name</span></span>
<span data-ttu-id="08d2c-126">取得或設定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="08d2c-126">Gets or sets the name of the cluster.</span></span>

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

### <span data-ttu-id="08d2c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08d2c-127">-ResourceGroupName</span></span>
<span data-ttu-id="08d2c-128">取得或設定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="08d2c-128">Gets or sets the name of the resource group.</span></span>

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

### <span data-ttu-id="08d2c-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="08d2c-129">-ResourceId</span></span>
<span data-ttu-id="08d2c-130">取得或設定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="08d2c-130">Gets or sets the resource id.</span></span>

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

### <span data-ttu-id="08d2c-131">-確認</span><span class="sxs-lookup"><span data-stu-id="08d2c-131">-Confirm</span></span>
<span data-ttu-id="08d2c-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="08d2c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08d2c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08d2c-133">-WhatIf</span></span>
<span data-ttu-id="08d2c-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="08d2c-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="08d2c-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="08d2c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08d2c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08d2c-136">CommonParameters</span></span>
<span data-ttu-id="08d2c-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="08d2c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08d2c-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="08d2c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08d2c-139">輸入</span><span class="sxs-lookup"><span data-stu-id="08d2c-139">INPUTS</span></span>

### <span data-ttu-id="08d2c-140">所有</span><span class="sxs-lookup"><span data-stu-id="08d2c-140">None</span></span>

## <span data-ttu-id="08d2c-141">輸出</span><span class="sxs-lookup"><span data-stu-id="08d2c-141">OUTPUTS</span></span>

### <span data-ttu-id="08d2c-142">[Microsoft Azure.]</span><span class="sxs-lookup"><span data-stu-id="08d2c-142">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="08d2c-143">筆記</span><span class="sxs-lookup"><span data-stu-id="08d2c-143">NOTES</span></span>

## <span data-ttu-id="08d2c-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="08d2c-144">RELATED LINKS</span></span>

[<span data-ttu-id="08d2c-145">客戶管理的主要磁片加密</span><span class="sxs-lookup"><span data-stu-id="08d2c-145">Customer-managed key disk encryption</span></span>](https://docs.microsoft.com/en-us/azure/hdinsight/disk-encryption)
