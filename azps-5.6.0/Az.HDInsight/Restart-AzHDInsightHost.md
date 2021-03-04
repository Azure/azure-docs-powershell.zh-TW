---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/restart-azhdinsighthost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Restart-AzHDInsightHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Restart-AzHDInsightHost.md
ms.openlocfilehash: bdedaee92a187d1086cdcd71948981e93fed508a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910714"
---
# <span data-ttu-id="8f33c-101">Restart-AzHDInsightHost</span><span class="sxs-lookup"><span data-stu-id="8f33c-101">Restart-AzHDInsightHost</span></span>

## <span data-ttu-id="8f33c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8f33c-102">SYNOPSIS</span></span>
<span data-ttu-id="8f33c-103">重新開機 HDInsight 集區的特定主機。</span><span class="sxs-lookup"><span data-stu-id="8f33c-103">Restarts the specific hosts of HDInsight cluster.</span></span>

## <span data-ttu-id="8f33c-104">語法</span><span class="sxs-lookup"><span data-stu-id="8f33c-104">SYNTAX</span></span>

### <span data-ttu-id="8f33c-105">SetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="8f33c-105">SetByNameParameterSet (Default)</span></span>
```
Restart-AzHDInsightHost [[-ResourceGroupName] <String>] [-ClusterName] <String> [-Name] <String[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f33c-106">SetByAzureHDInsightHostInfoParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f33c-106">SetByAzureHDInsightHostInfoParameterSet</span></span>
```
Restart-AzHDInsightHost [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-AzureHDInsightHostInfo] <AzureHDInsightHostInfo[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f33c-107">描述</span><span class="sxs-lookup"><span data-stu-id="8f33c-107">DESCRIPTION</span></span>
<span data-ttu-id="8f33c-108">此 **Restart-AzHDInsightHost** Cmdlet 會重新開機 HDInsight 集區的特定主機。</span><span class="sxs-lookup"><span data-stu-id="8f33c-108">This **Restart-AzHDInsightHost** cmdlet restart the specific hosts of HDInsight cluster.</span></span>

## <span data-ttu-id="8f33c-109">例子</span><span class="sxs-lookup"><span data-stu-id="8f33c-109">EXAMPLES</span></span>

### <span data-ttu-id="8f33c-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="8f33c-110">Example 1</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> Restart-AzHDInsightHost -ClusterName $clusterName -Name wn0, wn1
```

<span data-ttu-id="8f33c-111">此命令會重新開機兩個主機的組：worknode1、worknode2。</span><span class="sxs-lookup"><span data-stu-id="8f33c-111">This command restarts two hosts of the cluster: worknode1, worknode2.</span></span>

### <span data-ttu-id="8f33c-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="8f33c-112">Example 2</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $worknode1= Get-AzHDInsightHost -ClusterName $clusterName | Where-Object {$_.Name -like "wn1*"}
PS C:\> $worknode1 | Restart-AzHDInsightHost -ClusterName $clusterName
```

<span data-ttu-id="8f33c-113">此命令顯示如何與 Cmdlet "Get-AzHDInsightHost"合作。</span><span class="sxs-lookup"><span data-stu-id="8f33c-113">This command shows how to cooperate with the cmdlet 'Get-AzHDInsightHost'.</span></span>

## <span data-ttu-id="8f33c-114">參數</span><span class="sxs-lookup"><span data-stu-id="8f33c-114">PARAMETERS</span></span>

### <span data-ttu-id="8f33c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8f33c-115">-AsJob</span></span>
<span data-ttu-id="8f33c-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8f33c-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8f33c-117">-AzureHDInsightHostInfo</span><span class="sxs-lookup"><span data-stu-id="8f33c-117">-AzureHDInsightHostInfo</span></span>
<span data-ttu-id="8f33c-118">獲取或設定主機名稱。</span><span class="sxs-lookup"><span data-stu-id="8f33c-118">Gets or sets the name of the host.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo[]
Parameter Sets: SetByAzureHDInsightHostInfoParameterSet
Aliases: Host

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f33c-119">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="8f33c-119">-ClusterName</span></span>
<span data-ttu-id="8f33c-120">獲取或設定組名。</span><span class="sxs-lookup"><span data-stu-id="8f33c-120">Gets or sets the name of the cluster.</span></span>

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

### <span data-ttu-id="8f33c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f33c-121">-DefaultProfile</span></span>
<span data-ttu-id="8f33c-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8f33c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f33c-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="8f33c-123">-Name</span></span>
<span data-ttu-id="8f33c-124">獲取或設定主機名稱。</span><span class="sxs-lookup"><span data-stu-id="8f33c-124">Gets or sets the name of the host.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByNameParameterSet
Aliases: HostName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f33c-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8f33c-125">-PassThru</span></span>
<span data-ttu-id="8f33c-126">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="8f33c-126">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="8f33c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f33c-127">-ResourceGroupName</span></span>
<span data-ttu-id="8f33c-128">獲取或設定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8f33c-128">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f33c-129">-確認</span><span class="sxs-lookup"><span data-stu-id="8f33c-129">-Confirm</span></span>
<span data-ttu-id="8f33c-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="8f33c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f33c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f33c-131">-WhatIf</span></span>
<span data-ttu-id="8f33c-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8f33c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f33c-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8f33c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f33c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f33c-134">CommonParameters</span></span>
<span data-ttu-id="8f33c-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8f33c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f33c-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8f33c-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f33c-137">輸入</span><span class="sxs-lookup"><span data-stu-id="8f33c-137">INPUTS</span></span>

### <span data-ttu-id="8f33c-138">System.String[]</span><span class="sxs-lookup"><span data-stu-id="8f33c-138">System.String[]</span></span>

### <span data-ttu-id="8f33c-139">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo[]</span><span class="sxs-lookup"><span data-stu-id="8f33c-139">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo[]</span></span>

## <span data-ttu-id="8f33c-140">輸出</span><span class="sxs-lookup"><span data-stu-id="8f33c-140">OUTPUTS</span></span>

### <span data-ttu-id="8f33c-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8f33c-141">System.Boolean</span></span>

## <span data-ttu-id="8f33c-142">筆記</span><span class="sxs-lookup"><span data-stu-id="8f33c-142">NOTES</span></span>

## <span data-ttu-id="8f33c-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="8f33c-143">RELATED LINKS</span></span>
