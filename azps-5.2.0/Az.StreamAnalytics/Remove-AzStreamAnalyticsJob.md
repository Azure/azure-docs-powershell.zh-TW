---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 2F3BDDFE-7585-4802-BFA5-D110F846A33E
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsJob.md
ms.openlocfilehash: 65d0e40fd522d223eed2d0462e5c66beb9e9709a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98283235"
---
# <span data-ttu-id="3df01-101">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="3df01-101">Remove-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="3df01-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3df01-102">SYNOPSIS</span></span>
<span data-ttu-id="3df01-103">移除資料流程分析作業。</span><span class="sxs-lookup"><span data-stu-id="3df01-103">Removes a Stream Analytics job.</span></span>

## <span data-ttu-id="3df01-104">句法</span><span class="sxs-lookup"><span data-stu-id="3df01-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3df01-105">說明</span><span class="sxs-lookup"><span data-stu-id="3df01-105">DESCRIPTION</span></span>
<span data-ttu-id="3df01-106">**AzStreamAnalyticsJob** Cmdlet 會以非同步方式刪除 Azure 中的特定資料流程分析作業。</span><span class="sxs-lookup"><span data-stu-id="3df01-106">The **Remove-AzStreamAnalyticsJob** cmdlet asynchronously deletes a specific Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="3df01-107">示例</span><span class="sxs-lookup"><span data-stu-id="3df01-107">EXAMPLES</span></span>

### <span data-ttu-id="3df01-108">範例1：移除作業</span><span class="sxs-lookup"><span data-stu-id="3df01-108">EXAMPLE 1: Remove a job</span></span>
```
PS C:\>Remove-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="3df01-109">這個命令會移除作業 StreamingJob。</span><span class="sxs-lookup"><span data-stu-id="3df01-109">This command removes the job StreamingJob.</span></span>

## <span data-ttu-id="3df01-110">參數</span><span class="sxs-lookup"><span data-stu-id="3df01-110">PARAMETERS</span></span>

### <span data-ttu-id="3df01-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3df01-111">-DefaultProfile</span></span>
<span data-ttu-id="3df01-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3df01-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3df01-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="3df01-113">-Name</span></span>
<span data-ttu-id="3df01-114">指定要移除之 Azure 串流分析作業的名稱。</span><span class="sxs-lookup"><span data-stu-id="3df01-114">Specifies the name of the Azure Stream Analytics job to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3df01-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3df01-115">-ResourceGroupName</span></span>
<span data-ttu-id="3df01-116">指定 Azure 資料流程分析作業所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3df01-116">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3df01-117">-確認</span><span class="sxs-lookup"><span data-stu-id="3df01-117">-Confirm</span></span>
<span data-ttu-id="3df01-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3df01-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3df01-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3df01-119">-WhatIf</span></span>
<span data-ttu-id="3df01-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3df01-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3df01-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3df01-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3df01-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3df01-122">CommonParameters</span></span>
<span data-ttu-id="3df01-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3df01-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3df01-124">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3df01-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3df01-125">輸入</span><span class="sxs-lookup"><span data-stu-id="3df01-125">INPUTS</span></span>

### <span data-ttu-id="3df01-126">System.object</span><span class="sxs-lookup"><span data-stu-id="3df01-126">System.String</span></span>

## <span data-ttu-id="3df01-127">輸出</span><span class="sxs-lookup"><span data-stu-id="3df01-127">OUTPUTS</span></span>

### <span data-ttu-id="3df01-128">System.object</span><span class="sxs-lookup"><span data-stu-id="3df01-128">System.Boolean</span></span>

## <span data-ttu-id="3df01-129">筆記</span><span class="sxs-lookup"><span data-stu-id="3df01-129">NOTES</span></span>

## <span data-ttu-id="3df01-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="3df01-130">RELATED LINKS</span></span>

[<span data-ttu-id="3df01-131">AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="3df01-131">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="3df01-132">新-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="3df01-132">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="3df01-133">開始-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="3df01-133">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)

[<span data-ttu-id="3df01-134">停止 AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="3df01-134">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)


