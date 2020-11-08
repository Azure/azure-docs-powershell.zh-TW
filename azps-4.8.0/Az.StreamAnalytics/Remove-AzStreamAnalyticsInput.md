---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1449F64F-A8F9-4E8E-B62B-17DEF3A0FB30
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsInput.md
ms.openlocfilehash: d3c5e578e6921297d7d5edc467e10b9a2b4e9e53
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126679"
---
# <span data-ttu-id="d00c3-101">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="d00c3-101">Remove-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="d00c3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d00c3-102">SYNOPSIS</span></span>
<span data-ttu-id="d00c3-103">從資料流程分析作業中刪除輸入。</span><span class="sxs-lookup"><span data-stu-id="d00c3-103">Deletes an input from a Stream Analytics job.</span></span>

## <span data-ttu-id="d00c3-104">句法</span><span class="sxs-lookup"><span data-stu-id="d00c3-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d00c3-105">說明</span><span class="sxs-lookup"><span data-stu-id="d00c3-105">DESCRIPTION</span></span>
<span data-ttu-id="d00c3-106">**AzStreamAnalyticsInput** Cmdlet 會在 Azure 中非同步刪除資料流程分析作業的輸入。</span><span class="sxs-lookup"><span data-stu-id="d00c3-106">The **Remove-AzStreamAnalyticsInput** cmdlet asynchronously deletes an input from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="d00c3-107">示例</span><span class="sxs-lookup"><span data-stu-id="d00c3-107">EXAMPLES</span></span>

### <span data-ttu-id="d00c3-108">範例1：從工作中移除輸入資料流程</span><span class="sxs-lookup"><span data-stu-id="d00c3-108">EXAMPLE 1: Remove an input stream from a job</span></span>
```
PS C:\>Remove-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EventStream"
```

<span data-ttu-id="d00c3-109">這個命令會將輸入 EventStream 從 StreamingJob 中移除。</span><span class="sxs-lookup"><span data-stu-id="d00c3-109">This command removes the input EventStream from StreamingJob.</span></span>

## <span data-ttu-id="d00c3-110">參數</span><span class="sxs-lookup"><span data-stu-id="d00c3-110">PARAMETERS</span></span>

### <span data-ttu-id="d00c3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d00c3-111">-DefaultProfile</span></span>
<span data-ttu-id="d00c3-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d00c3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d00c3-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="d00c3-113">-JobName</span></span>
<span data-ttu-id="d00c3-114">指定 Azure 串流分析輸入所屬之 Azure 串流分析作業的名稱。</span><span class="sxs-lookup"><span data-stu-id="d00c3-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="d00c3-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="d00c3-115">-Name</span></span>
<span data-ttu-id="d00c3-116">指定要移除之 Azure 資料流程分析輸入的名稱。</span><span class="sxs-lookup"><span data-stu-id="d00c3-116">Specifies the name of the Azure Stream Analytics input to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d00c3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d00c3-117">-ResourceGroupName</span></span>
<span data-ttu-id="d00c3-118">指定 Azure 串流分析輸入所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d00c3-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="d00c3-119">-確認</span><span class="sxs-lookup"><span data-stu-id="d00c3-119">-Confirm</span></span>
<span data-ttu-id="d00c3-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d00c3-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d00c3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d00c3-121">-WhatIf</span></span>
<span data-ttu-id="d00c3-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d00c3-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d00c3-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d00c3-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d00c3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d00c3-124">CommonParameters</span></span>
<span data-ttu-id="d00c3-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d00c3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d00c3-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d00c3-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d00c3-127">輸入</span><span class="sxs-lookup"><span data-stu-id="d00c3-127">INPUTS</span></span>

### <span data-ttu-id="d00c3-128">System.object</span><span class="sxs-lookup"><span data-stu-id="d00c3-128">System.String</span></span>

## <span data-ttu-id="d00c3-129">輸出</span><span class="sxs-lookup"><span data-stu-id="d00c3-129">OUTPUTS</span></span>

### <span data-ttu-id="d00c3-130">System.object</span><span class="sxs-lookup"><span data-stu-id="d00c3-130">System.Boolean</span></span>

## <span data-ttu-id="d00c3-131">筆記</span><span class="sxs-lookup"><span data-stu-id="d00c3-131">NOTES</span></span>

## <span data-ttu-id="d00c3-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="d00c3-132">RELATED LINKS</span></span>

[<span data-ttu-id="d00c3-133">新-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="d00c3-133">New-AzStreamAnalyticsInput</span></span>](./New-AzStreamAnalyticsInput.md)

[<span data-ttu-id="d00c3-134">AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="d00c3-134">Get-AzStreamAnalyticsInput</span></span>](./Get-AzStreamAnalyticsInput.md)

[<span data-ttu-id="d00c3-135">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="d00c3-135">Test-AzStreamAnalyticsInput</span></span>](./Test-AzStreamAnalyticsInput.md)


