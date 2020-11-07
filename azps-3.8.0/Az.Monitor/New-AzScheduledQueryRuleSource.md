---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulesource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSource.md
ms.openlocfilehash: 0fe5684805dfc3047abb39040d80eb8a388cf5a2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956325"
---
# <span data-ttu-id="b4ca2-101">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="b4ca2-101">New-AzScheduledQueryRuleSource</span></span>

## <span data-ttu-id="b4ca2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b4ca2-102">SYNOPSIS</span></span>
<span data-ttu-id="b4ca2-103">建立來源類型的物件</span><span class="sxs-lookup"><span data-stu-id="b4ca2-103">Creates an object of type Source</span></span>

## <span data-ttu-id="b4ca2-104">句法</span><span class="sxs-lookup"><span data-stu-id="b4ca2-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleSource -Query <String> [-AuthorizedResource <String[]>] -DataSourceId <String>
 [-QueryType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4ca2-105">說明</span><span class="sxs-lookup"><span data-stu-id="b4ca2-105">DESCRIPTION</span></span>
<span data-ttu-id="b4ca2-106">建立來源類型的物件。</span><span class="sxs-lookup"><span data-stu-id="b4ca2-106">Creates an object of type Source.</span></span>
<span data-ttu-id="b4ca2-107">這個物件會傳遞到建立記錄提醒規則的命令</span><span class="sxs-lookup"><span data-stu-id="b4ca2-107">This object is to be passed to the command that creates Log Alert Rule</span></span>

## <span data-ttu-id="b4ca2-108">示例</span><span class="sxs-lookup"><span data-stu-id="b4ca2-108">EXAMPLES</span></span>

### <span data-ttu-id="b4ca2-109">範例1</span><span class="sxs-lookup"><span data-stu-id="b4ca2-109">Example 1</span></span>
```powershell
PS C:\> $source = New-AzScheduledQueryRuleSource -Query "Heartbeat | summarize AggregatedValue = count() by bin(TimeGenerated, 5m)"
                  -DataSourceId "/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace" 
                  -QueryType "ResultCount"
```

## <span data-ttu-id="b4ca2-110">參數</span><span class="sxs-lookup"><span data-stu-id="b4ca2-110">PARAMETERS</span></span>

### <span data-ttu-id="b4ca2-111">-AuthorizedResource</span><span class="sxs-lookup"><span data-stu-id="b4ca2-111">-AuthorizedResource</span></span>
<span data-ttu-id="b4ca2-112">此通知的授權資源清單</span><span class="sxs-lookup"><span data-stu-id="b4ca2-112">The list of authorized resources for this alert</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4ca2-113">-DataSourceId</span><span class="sxs-lookup"><span data-stu-id="b4ca2-113">-DataSourceId</span></span>
<span data-ttu-id="b4ca2-114">建立此預警的資料來源</span><span class="sxs-lookup"><span data-stu-id="b4ca2-114">The data source on which this alert is created</span></span>

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

### <span data-ttu-id="b4ca2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4ca2-115">-DefaultProfile</span></span>
<span data-ttu-id="b4ca2-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b4ca2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4ca2-117">-Query</span><span class="sxs-lookup"><span data-stu-id="b4ca2-117">-Query</span></span>
<span data-ttu-id="b4ca2-118">警示查詢</span><span class="sxs-lookup"><span data-stu-id="b4ca2-118">The alert query</span></span>

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

### <span data-ttu-id="b4ca2-119">-QueryType</span><span class="sxs-lookup"><span data-stu-id="b4ca2-119">-QueryType</span></span>
<span data-ttu-id="b4ca2-120">查詢類型-目前支援的值： ResultCount</span><span class="sxs-lookup"><span data-stu-id="b4ca2-120">Type of Query - currently supported values : ResultCount</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4ca2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4ca2-121">CommonParameters</span></span>
<span data-ttu-id="b4ca2-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b4ca2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4ca2-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b4ca2-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4ca2-124">輸入</span><span class="sxs-lookup"><span data-stu-id="b4ca2-124">INPUTS</span></span>

### <span data-ttu-id="b4ca2-125">所有</span><span class="sxs-lookup"><span data-stu-id="b4ca2-125">None</span></span>

## <span data-ttu-id="b4ca2-126">輸出</span><span class="sxs-lookup"><span data-stu-id="b4ca2-126">OUTPUTS</span></span>

### <span data-ttu-id="b4ca2-127">PSScheduledQueryRuleSource 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="b4ca2-127">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource</span></span>

## <span data-ttu-id="b4ca2-128">筆記</span><span class="sxs-lookup"><span data-stu-id="b4ca2-128">NOTES</span></span>

## <span data-ttu-id="b4ca2-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="b4ca2-129">RELATED LINKS</span></span>
