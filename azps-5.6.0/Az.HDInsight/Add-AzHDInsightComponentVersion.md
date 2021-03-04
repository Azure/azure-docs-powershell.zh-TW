---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 774848C9-47A1-4C43-B6FA-B3C0C3C76470
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/add-azhdinsightcomponentversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightComponentVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightComponentVersion.md
ms.openlocfilehash: 9cd0a5def5a05782cce067a97fa85029b8e52ca3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911674"
---
# <span data-ttu-id="17273-101">Add-AzHDInsightComponentVersion</span><span class="sxs-lookup"><span data-stu-id="17273-101">Add-AzHDInsightComponentVersion</span></span>

## <span data-ttu-id="17273-102">簡介</span><span class="sxs-lookup"><span data-stu-id="17273-102">SYNOPSIS</span></span>
<span data-ttu-id="17273-103">新增在一組組集中執行之服務的版本至組組物件。</span><span class="sxs-lookup"><span data-stu-id="17273-103">Adds a version for a service running in a cluster to a cluster configuration object.</span></span>

## <span data-ttu-id="17273-104">語法</span><span class="sxs-lookup"><span data-stu-id="17273-104">SYNTAX</span></span>

```
Add-AzHDInsightComponentVersion [-Config] <AzureHDInsightConfig> [-ComponentName] <String>
 [-ComponentVersion] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="17273-105">描述</span><span class="sxs-lookup"><span data-stu-id="17273-105">DESCRIPTION</span></span>
<span data-ttu-id="17273-106">此Add-AzHDInsightComponentVersion Cmdlet 會將在一個集中執行的服務版本新增到由 New-AzHDInsightClusterConfig Cmdlet 所建立 Azure HDInsight 組New-AzHDInsightClusterConfig物件。</span><span class="sxs-lookup"><span data-stu-id="17273-106">The Add-AzHDInsightComponentVersion cmdlet adds a version for a service running in a cluster to the Azure HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="17273-107">例子</span><span class="sxs-lookup"><span data-stu-id="17273-107">EXAMPLES</span></span>

### <span data-ttu-id="17273-108">範例 1：新增 Spark 版本至集區組物件。</span><span class="sxs-lookup"><span data-stu-id="17273-108">Example 1: Add a version for Spark to the cluster configuration object.</span></span>
```
PS C:\> # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountName = "yourstorageacct001"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
        $storageContainer = "container001"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-spark-001"
        $clusterCreds = Get-Credential
        $sshClusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        #   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightClusterConfig `
            | Add-AzHDInsightComponentVersion `
                -ComponentName "Spark" `
                -ComponentVersion "2.0" `
            | New-AzHDInsightCluster `
                -ClusterType Spark `
                -OSType Linux `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -StorageAccountResourceId $storageAccountResourceId `
                -StorageAccountKey $storageAccountKey `
                -StorageContainer $storageContainer `
                -SshCredential $sshCredentials `
                -Version "3.5"
```

<span data-ttu-id="17273-109">此命令會將 Spark 版本新增到名為'your-spark-001'的 HDInsight 集區。</span><span class="sxs-lookup"><span data-stu-id="17273-109">This command adds the version of Spark to the HDInsight cluster named 'your-spark-001'.</span></span>

## <span data-ttu-id="17273-110">參數</span><span class="sxs-lookup"><span data-stu-id="17273-110">PARAMETERS</span></span>

### <span data-ttu-id="17273-111">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="17273-111">-ComponentName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17273-112">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="17273-112">-ComponentVersion</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17273-113">-Config</span><span class="sxs-lookup"><span data-stu-id="17273-113">-Config</span></span>
```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17273-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17273-114">-DefaultProfile</span></span>
<span data-ttu-id="17273-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="17273-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="17273-116">-確認</span><span class="sxs-lookup"><span data-stu-id="17273-116">-Confirm</span></span>
<span data-ttu-id="17273-117">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="17273-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17273-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17273-118">-WhatIf</span></span>
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

### <span data-ttu-id="17273-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17273-119">CommonParameters</span></span>
<span data-ttu-id="17273-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="17273-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17273-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="17273-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17273-122">輸入</span><span class="sxs-lookup"><span data-stu-id="17273-122">INPUTS</span></span>

### <span data-ttu-id="17273-123">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="17273-123">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="17273-124">輸出</span><span class="sxs-lookup"><span data-stu-id="17273-124">OUTPUTS</span></span>

### <span data-ttu-id="17273-125">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="17273-125">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="17273-126">筆記</span><span class="sxs-lookup"><span data-stu-id="17273-126">NOTES</span></span>

## <span data-ttu-id="17273-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="17273-127">RELATED LINKS</span></span>
