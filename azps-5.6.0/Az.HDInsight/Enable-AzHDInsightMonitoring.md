---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/enable-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Enable-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Enable-AzHDInsightMonitoring.md
ms.openlocfilehash: dc9e19c35f43b2420213d21b427d2aff69bb2541
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913206"
---
# <span data-ttu-id="e3921-101">Enable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="e3921-101">Enable-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="e3921-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e3921-102">SYNOPSIS</span></span>
<span data-ttu-id="e3921-103">啟用 HDInsight 群集中的監控功能，相關記錄將會送到啟用期間指定的監控工作區。</span><span class="sxs-lookup"><span data-stu-id="e3921-103">Enables monitoring in a HDInsight cluster and relevant logs will be sent to the monitoring workspace specified during enable.</span></span>

## <span data-ttu-id="e3921-104">語法</span><span class="sxs-lookup"><span data-stu-id="e3921-104">SYNTAX</span></span>

```
Enable-AzHDInsightMonitoring [-Name] <String> [-WorkspaceId] <String> [-PrimaryKey] <String>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e3921-105">描述</span><span class="sxs-lookup"><span data-stu-id="e3921-105">DESCRIPTION</span></span>
<span data-ttu-id="e3921-106">**Enable-AzHDInsightMonitoring** Cmdlet 可在 Azure HDInsight cluster 中監控。</span><span class="sxs-lookup"><span data-stu-id="e3921-106">The **Enable-AzHDInsightMonitoring** cmdlet enables monitoring in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="e3921-107">例子</span><span class="sxs-lookup"><span data-stu-id="e3921-107">EXAMPLES</span></span>

### <span data-ttu-id="e3921-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="e3921-108">Example 1</span></span>
```
PS C:\> Enable-AzHDInsightMonitoring -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

True
```

<span data-ttu-id="e3921-109">HDInsight 組會啟用監控，而相關記錄會以 id 1d364e89-bb71-4503-aa3d-a23535aea7bd 送到監控工作區</span><span class="sxs-lookup"><span data-stu-id="e3921-109">Monitoring will be enabled on the HDInsight cluster and relevant logs will be sent to the monitoring workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="e3921-110">範例 2</span><span class="sxs-lookup"><span data-stu-id="e3921-110">Example 2</span></span>
```
PS C:\> Enable-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

True
```

<span data-ttu-id="e3921-111">HDInsight 組會啟用監控，而相關記錄會以 id 1d364e89-bb71-4503-aa3d-a23535aea7bd 送到監控工作區</span><span class="sxs-lookup"><span data-stu-id="e3921-111">Monitoring will be enabled on the HDInsight cluster and relevant logs will be sent to the monitoring workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

## <span data-ttu-id="e3921-112">參數</span><span class="sxs-lookup"><span data-stu-id="e3921-112">PARAMETERS</span></span>

### <span data-ttu-id="e3921-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3921-113">-DefaultProfile</span></span>
<span data-ttu-id="e3921-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="e3921-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e3921-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="e3921-115">-Name</span></span>
<span data-ttu-id="e3921-116">啟用監控的組名。</span><span class="sxs-lookup"><span data-stu-id="e3921-116">The name of the cluster to enable monitoring.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3921-117">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="e3921-117">-PrimaryKey</span></span>
<span data-ttu-id="e3921-118">監控工作區的主鍵。</span><span class="sxs-lookup"><span data-stu-id="e3921-118">The primary key of the monitoring workspace.</span></span>

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

### <span data-ttu-id="e3921-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3921-119">-ResourceGroupName</span></span>
<span data-ttu-id="e3921-120">群組的資源群組。</span><span class="sxs-lookup"><span data-stu-id="e3921-120">The resource group of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3921-121">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="e3921-121">-WorkspaceId</span></span>
<span data-ttu-id="e3921-122">監控工作區的識別碼。</span><span class="sxs-lookup"><span data-stu-id="e3921-122">The id of the monitoring workspace.</span></span>

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

### <span data-ttu-id="e3921-123">-確認</span><span class="sxs-lookup"><span data-stu-id="e3921-123">-Confirm</span></span>
<span data-ttu-id="e3921-124">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e3921-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3921-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3921-125">-WhatIf</span></span>
<span data-ttu-id="e3921-126">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e3921-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e3921-127">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e3921-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3921-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3921-128">CommonParameters</span></span>
<span data-ttu-id="e3921-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e3921-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3921-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e3921-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3921-131">輸入</span><span class="sxs-lookup"><span data-stu-id="e3921-131">INPUTS</span></span>

### <span data-ttu-id="e3921-132">System.String</span><span class="sxs-lookup"><span data-stu-id="e3921-132">System.String</span></span>

## <span data-ttu-id="e3921-133">輸出</span><span class="sxs-lookup"><span data-stu-id="e3921-133">OUTPUTS</span></span>

### <span data-ttu-id="e3921-134">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e3921-134">System.Boolean</span></span>

## <span data-ttu-id="e3921-135">筆記</span><span class="sxs-lookup"><span data-stu-id="e3921-135">NOTES</span></span>

## <span data-ttu-id="e3921-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="e3921-136">RELATED LINKS</span></span>
