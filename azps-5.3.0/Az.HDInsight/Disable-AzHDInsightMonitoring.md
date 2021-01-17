---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/disable-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Disable-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Disable-AzHDInsightMonitoring.md
ms.openlocfilehash: 9a65a82808c78fe878ba4a61f8be01f37fc11771
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435066"
---
# <span data-ttu-id="626e3-101">Disable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="626e3-101">Disable-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="626e3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="626e3-102">SYNOPSIS</span></span>
<span data-ttu-id="626e3-103">在 HDInsight 群集中停用監視，相關記錄將停止流入至啟用期間指定的監視工作區。</span><span class="sxs-lookup"><span data-stu-id="626e3-103">Disables monitoring in a HDInsight cluster and relevant logs will stop flowing to the monitoring workspace specified during enable.</span></span>

## <span data-ttu-id="626e3-104">句法</span><span class="sxs-lookup"><span data-stu-id="626e3-104">SYNTAX</span></span>

```
Disable-AzHDInsightMonitoring [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="626e3-105">說明</span><span class="sxs-lookup"><span data-stu-id="626e3-105">DESCRIPTION</span></span>
<span data-ttu-id="626e3-106">**Disable AzHDInsightMonitoring** Cmdlet 會停用 Azure HDInsight 群集中的監視。</span><span class="sxs-lookup"><span data-stu-id="626e3-106">The **Disable-AzHDInsightMonitoring** cmdlet disables monitoring in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="626e3-107">示例</span><span class="sxs-lookup"><span data-stu-id="626e3-107">EXAMPLES</span></span>

### <span data-ttu-id="626e3-108">範例1</span><span class="sxs-lookup"><span data-stu-id="626e3-108">Example 1</span></span>
```
PS C:\> Disable-AzHDInsightMonitoring -Name testcluster

True
```

<span data-ttu-id="626e3-109">系統會在 HDInsight 群集上停用監視，相關記錄將停止流入至監視工作區。</span><span class="sxs-lookup"><span data-stu-id="626e3-109">Monitoring will be disabled on the HDInsight cluster and relevant logs will stop flowing to the monitoring workspace.</span></span>

### <span data-ttu-id="626e3-110">範例2</span><span class="sxs-lookup"><span data-stu-id="626e3-110">Example 2</span></span>
```
PS C:\> Disable-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

True
```

<span data-ttu-id="626e3-111">系統會在 HDInsight 群集上停用監視，相關記錄將停止流入至監視工作區。</span><span class="sxs-lookup"><span data-stu-id="626e3-111">Monitoring will be disabled on the HDInsight cluster and relevant logs will stop flowing to the monitoring workspace.</span></span>

## <span data-ttu-id="626e3-112">參數</span><span class="sxs-lookup"><span data-stu-id="626e3-112">PARAMETERS</span></span>

### <span data-ttu-id="626e3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="626e3-113">-DefaultProfile</span></span>
<span data-ttu-id="626e3-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="626e3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="626e3-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="626e3-115">-Name</span></span>
<span data-ttu-id="626e3-116">要停用監視的群集名稱。</span><span class="sxs-lookup"><span data-stu-id="626e3-116">The name of the cluster to disable Monitoring.</span></span>

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

### <span data-ttu-id="626e3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="626e3-117">-ResourceGroupName</span></span>
<span data-ttu-id="626e3-118">群集的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="626e3-118">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="626e3-119">-確認</span><span class="sxs-lookup"><span data-stu-id="626e3-119">-Confirm</span></span>
<span data-ttu-id="626e3-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="626e3-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="626e3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="626e3-121">-WhatIf</span></span>
<span data-ttu-id="626e3-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="626e3-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="626e3-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="626e3-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="626e3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="626e3-124">CommonParameters</span></span>
<span data-ttu-id="626e3-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="626e3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="626e3-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="626e3-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="626e3-127">輸入</span><span class="sxs-lookup"><span data-stu-id="626e3-127">INPUTS</span></span>

### <span data-ttu-id="626e3-128">System.object</span><span class="sxs-lookup"><span data-stu-id="626e3-128">System.String</span></span>

## <span data-ttu-id="626e3-129">輸出</span><span class="sxs-lookup"><span data-stu-id="626e3-129">OUTPUTS</span></span>

### <span data-ttu-id="626e3-130">System.object</span><span class="sxs-lookup"><span data-stu-id="626e3-130">System.Boolean</span></span>

## <span data-ttu-id="626e3-131">筆記</span><span class="sxs-lookup"><span data-stu-id="626e3-131">NOTES</span></span>

## <span data-ttu-id="626e3-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="626e3-132">RELATED LINKS</span></span>
