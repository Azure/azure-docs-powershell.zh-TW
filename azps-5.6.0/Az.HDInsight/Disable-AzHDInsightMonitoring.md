---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/disable-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Disable-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Disable-AzHDInsightMonitoring.md
ms.openlocfilehash: 04e4a2e45f799367060c76e30807f75eaedb0465
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906170"
---
# <span data-ttu-id="cf08e-101">Disable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="cf08e-101">Disable-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="cf08e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="cf08e-102">SYNOPSIS</span></span>
<span data-ttu-id="cf08e-103">停用 HDInsight 群集中的監控，相關記錄會停止流向啟用期間指定的監控工作區。</span><span class="sxs-lookup"><span data-stu-id="cf08e-103">Disables monitoring in a HDInsight cluster and relevant logs will stop flowing to the monitoring workspace specified during enable.</span></span>

## <span data-ttu-id="cf08e-104">語法</span><span class="sxs-lookup"><span data-stu-id="cf08e-104">SYNTAX</span></span>

```
Disable-AzHDInsightMonitoring [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf08e-105">描述</span><span class="sxs-lookup"><span data-stu-id="cf08e-105">DESCRIPTION</span></span>
<span data-ttu-id="cf08e-106">**Disable-AzHDInsightMonitoring** Cmdlet 會停用 Azure HDInsight 組集中的監控。</span><span class="sxs-lookup"><span data-stu-id="cf08e-106">The **Disable-AzHDInsightMonitoring** cmdlet disables monitoring in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="cf08e-107">例子</span><span class="sxs-lookup"><span data-stu-id="cf08e-107">EXAMPLES</span></span>

### <span data-ttu-id="cf08e-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="cf08e-108">Example 1</span></span>
```
PS C:\> Disable-AzHDInsightMonitoring -Name testcluster

True
```

<span data-ttu-id="cf08e-109">HDInsight 的監控將會停用，相關記錄會停止流向監控工作區。</span><span class="sxs-lookup"><span data-stu-id="cf08e-109">Monitoring will be disabled on the HDInsight cluster and relevant logs will stop flowing to the monitoring workspace.</span></span>

### <span data-ttu-id="cf08e-110">範例 2</span><span class="sxs-lookup"><span data-stu-id="cf08e-110">Example 2</span></span>
```
PS C:\> Disable-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

True
```

<span data-ttu-id="cf08e-111">HDInsight 的監控將會停用，相關記錄會停止流向監控工作區。</span><span class="sxs-lookup"><span data-stu-id="cf08e-111">Monitoring will be disabled on the HDInsight cluster and relevant logs will stop flowing to the monitoring workspace.</span></span>

## <span data-ttu-id="cf08e-112">參數</span><span class="sxs-lookup"><span data-stu-id="cf08e-112">PARAMETERS</span></span>

### <span data-ttu-id="cf08e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf08e-113">-DefaultProfile</span></span>
<span data-ttu-id="cf08e-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="cf08e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cf08e-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="cf08e-115">-Name</span></span>
<span data-ttu-id="cf08e-116">要停用監控的組名。</span><span class="sxs-lookup"><span data-stu-id="cf08e-116">The name of the cluster to disable Monitoring.</span></span>

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

### <span data-ttu-id="cf08e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf08e-117">-ResourceGroupName</span></span>
<span data-ttu-id="cf08e-118">群組的資源群組。</span><span class="sxs-lookup"><span data-stu-id="cf08e-118">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="cf08e-119">-確認</span><span class="sxs-lookup"><span data-stu-id="cf08e-119">-Confirm</span></span>
<span data-ttu-id="cf08e-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="cf08e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf08e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf08e-121">-WhatIf</span></span>
<span data-ttu-id="cf08e-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cf08e-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cf08e-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cf08e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf08e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf08e-124">CommonParameters</span></span>
<span data-ttu-id="cf08e-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="cf08e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf08e-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cf08e-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf08e-127">輸入</span><span class="sxs-lookup"><span data-stu-id="cf08e-127">INPUTS</span></span>

### <span data-ttu-id="cf08e-128">System.String</span><span class="sxs-lookup"><span data-stu-id="cf08e-128">System.String</span></span>

## <span data-ttu-id="cf08e-129">輸出</span><span class="sxs-lookup"><span data-stu-id="cf08e-129">OUTPUTS</span></span>

### <span data-ttu-id="cf08e-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cf08e-130">System.Boolean</span></span>

## <span data-ttu-id="cf08e-131">筆記</span><span class="sxs-lookup"><span data-stu-id="cf08e-131">NOTES</span></span>

## <span data-ttu-id="cf08e-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="cf08e-132">RELATED LINKS</span></span>
