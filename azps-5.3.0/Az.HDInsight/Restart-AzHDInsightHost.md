---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/restart-azhdinsighthost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Restart-AzHDInsightHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Restart-AzHDInsightHost.md
ms.openlocfilehash: 4e0b5fda29696fb45515c3b478b9dc29ff67263e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435046"
---
# <span data-ttu-id="d8b03-101">Restart-AzHDInsightHost</span><span class="sxs-lookup"><span data-stu-id="d8b03-101">Restart-AzHDInsightHost</span></span>

## <span data-ttu-id="d8b03-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d8b03-102">SYNOPSIS</span></span>
<span data-ttu-id="d8b03-103">重新開機 HDInsight 群集的特定主機。</span><span class="sxs-lookup"><span data-stu-id="d8b03-103">Restarts the specific hosts of HDInsight cluster.</span></span>

## <span data-ttu-id="d8b03-104">句法</span><span class="sxs-lookup"><span data-stu-id="d8b03-104">SYNTAX</span></span>

### <span data-ttu-id="d8b03-105">SetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d8b03-105">SetByNameParameterSet (Default)</span></span>
```
Restart-AzHDInsightHost [[-ResourceGroupName] <String>] [-ClusterName] <String> [-Name] <String[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8b03-106">SetByAzureHDInsightHostInfoParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8b03-106">SetByAzureHDInsightHostInfoParameterSet</span></span>
```
Restart-AzHDInsightHost [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-AzureHDInsightHostInfo] <AzureHDInsightHostInfo[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8b03-107">說明</span><span class="sxs-lookup"><span data-stu-id="d8b03-107">DESCRIPTION</span></span>
<span data-ttu-id="d8b03-108">此 **重新開機 AzHDInsightHost** Cmdlet 會重新開機 HDInsight 群集的特定主機。</span><span class="sxs-lookup"><span data-stu-id="d8b03-108">This **Restart-AzHDInsightHost** cmdlet restart the specific hosts of HDInsight cluster.</span></span>

## <span data-ttu-id="d8b03-109">示例</span><span class="sxs-lookup"><span data-stu-id="d8b03-109">EXAMPLES</span></span>

### <span data-ttu-id="d8b03-110">範例1</span><span class="sxs-lookup"><span data-stu-id="d8b03-110">Example 1</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> Restart-AzHDInsightHost -ClusterName $clusterName -Name wn0, wn1
```

<span data-ttu-id="d8b03-111">這個命令會重新開機兩個群集主機： worknode1、worknode2。</span><span class="sxs-lookup"><span data-stu-id="d8b03-111">This command restarts two hosts of the cluster: worknode1, worknode2.</span></span>

### <span data-ttu-id="d8b03-112">範例2</span><span class="sxs-lookup"><span data-stu-id="d8b03-112">Example 2</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $worknode1= Get-AzHDInsightHost -ClusterName $clusterName | Where-Object {$_.Name -like "wn1*"}
PS C:\> $worknode1 | Restart-AzHDInsightHost -ClusterName $clusterName
```

<span data-ttu-id="d8b03-113">這個命令會說明如何與 Cmdlet 「AzHDInsightHost」共同合作。</span><span class="sxs-lookup"><span data-stu-id="d8b03-113">This command shows how to cooperate with the cmdlet 'Get-AzHDInsightHost'.</span></span>

## <span data-ttu-id="d8b03-114">參數</span><span class="sxs-lookup"><span data-stu-id="d8b03-114">PARAMETERS</span></span>

### <span data-ttu-id="d8b03-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d8b03-115">-AsJob</span></span>
<span data-ttu-id="d8b03-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d8b03-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d8b03-117">-AzureHDInsightHostInfo</span><span class="sxs-lookup"><span data-stu-id="d8b03-117">-AzureHDInsightHostInfo</span></span>
<span data-ttu-id="d8b03-118">取得或設定主機名稱。</span><span class="sxs-lookup"><span data-stu-id="d8b03-118">Gets or sets the name of the host.</span></span>

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

### <span data-ttu-id="d8b03-119">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d8b03-119">-ClusterName</span></span>
<span data-ttu-id="d8b03-120">取得或設定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="d8b03-120">Gets or sets the name of the cluster.</span></span>

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

### <span data-ttu-id="d8b03-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8b03-121">-DefaultProfile</span></span>
<span data-ttu-id="d8b03-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d8b03-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8b03-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="d8b03-123">-Name</span></span>
<span data-ttu-id="d8b03-124">取得或設定主機名稱。</span><span class="sxs-lookup"><span data-stu-id="d8b03-124">Gets or sets the name of the host.</span></span>

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

### <span data-ttu-id="d8b03-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d8b03-125">-PassThru</span></span>
<span data-ttu-id="d8b03-126">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="d8b03-126">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="d8b03-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8b03-127">-ResourceGroupName</span></span>
<span data-ttu-id="d8b03-128">取得或設定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d8b03-128">Gets or sets the name of the resource group.</span></span>

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

### <span data-ttu-id="d8b03-129">-確認</span><span class="sxs-lookup"><span data-stu-id="d8b03-129">-Confirm</span></span>
<span data-ttu-id="d8b03-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d8b03-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8b03-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8b03-131">-WhatIf</span></span>
<span data-ttu-id="d8b03-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d8b03-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8b03-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d8b03-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8b03-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8b03-134">CommonParameters</span></span>
<span data-ttu-id="d8b03-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d8b03-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8b03-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d8b03-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8b03-137">輸入</span><span class="sxs-lookup"><span data-stu-id="d8b03-137">INPUTS</span></span>

### <span data-ttu-id="d8b03-138">System.object []</span><span class="sxs-lookup"><span data-stu-id="d8b03-138">System.String[]</span></span>

### <span data-ttu-id="d8b03-139">AzureHDInsightHostInfo [] （[]）</span><span class="sxs-lookup"><span data-stu-id="d8b03-139">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo[]</span></span>

## <span data-ttu-id="d8b03-140">輸出</span><span class="sxs-lookup"><span data-stu-id="d8b03-140">OUTPUTS</span></span>

### <span data-ttu-id="d8b03-141">System.object</span><span class="sxs-lookup"><span data-stu-id="d8b03-141">System.Boolean</span></span>

## <span data-ttu-id="d8b03-142">筆記</span><span class="sxs-lookup"><span data-stu-id="d8b03-142">NOTES</span></span>

## <span data-ttu-id="d8b03-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="d8b03-143">RELATED LINKS</span></span>
