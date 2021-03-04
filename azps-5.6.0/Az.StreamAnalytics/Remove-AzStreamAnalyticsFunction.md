---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 75B0776E-32D5-4EE4-B35C-73E13185A4F1
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/remove-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsFunction.md
ms.openlocfilehash: 1a500f883b6896e91767f0f7d560ee28e4bfc9f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907374"
---
# <span data-ttu-id="95a25-101">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="95a25-101">Remove-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="95a25-102">簡介</span><span class="sxs-lookup"><span data-stu-id="95a25-102">SYNOPSIS</span></span>
<span data-ttu-id="95a25-103">刪除 Stream Analytics 工作中的函數。</span><span class="sxs-lookup"><span data-stu-id="95a25-103">Deletes a function from a Stream Analytics job.</span></span>

## <span data-ttu-id="95a25-104">語法</span><span class="sxs-lookup"><span data-stu-id="95a25-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95a25-105">描述</span><span class="sxs-lookup"><span data-stu-id="95a25-105">DESCRIPTION</span></span>
<span data-ttu-id="95a25-106">**Remove-AzStreamAnalyticsFunctdion Cmdlet** 會非同步刪除 Azure Stream Analytics 工作中的函數。</span><span class="sxs-lookup"><span data-stu-id="95a25-106">The **Remove-AzStreamAnalyticsFunction** cmdlet deletes a function asynchronously from an Azure Stream Analytics job.</span></span>

## <span data-ttu-id="95a25-107">例子</span><span class="sxs-lookup"><span data-stu-id="95a25-107">EXAMPLES</span></span>

### <span data-ttu-id="95a25-108">範例 1：移除 Stream Analytics 函數</span><span class="sxs-lookup"><span data-stu-id="95a25-108">Example 1: Remove a Stream Analytics function</span></span>
```
PS C:\>Remove-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="95a25-109">此命令會從名為 StreamJob22 的工作移除名為 ScoreTweet 的函數。</span><span class="sxs-lookup"><span data-stu-id="95a25-109">This command removes the function named ScoreTweet from the job named StreamJob22.</span></span>

## <span data-ttu-id="95a25-110">參數</span><span class="sxs-lookup"><span data-stu-id="95a25-110">PARAMETERS</span></span>

### <span data-ttu-id="95a25-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95a25-111">-DefaultProfile</span></span>
<span data-ttu-id="95a25-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="95a25-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95a25-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="95a25-113">-JobName</span></span>
<span data-ttu-id="95a25-114">指定函數所屬的 Stream Analytics 工作名稱。</span><span class="sxs-lookup"><span data-stu-id="95a25-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>
<span data-ttu-id="95a25-115">此 Cmdlet 會從此參數指定的工作移除函數。</span><span class="sxs-lookup"><span data-stu-id="95a25-115">This cmdlet removes a function from the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="95a25-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="95a25-116">-Name</span></span>
<span data-ttu-id="95a25-117">指定此 Cmdlet 移除的 Stream Analytics 函數名稱。</span><span class="sxs-lookup"><span data-stu-id="95a25-117">Specifies the name of the Stream Analytics function that this cmdlet removes.</span></span>

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

### <span data-ttu-id="95a25-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95a25-118">-ResourceGroupName</span></span>
<span data-ttu-id="95a25-119">指定 Stream Analytics 函數所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="95a25-119">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="95a25-120">此 Cmdlet 會刪除此參數指定之資源群組中的函數。</span><span class="sxs-lookup"><span data-stu-id="95a25-120">This cmdlet deletes a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="95a25-121">-確認</span><span class="sxs-lookup"><span data-stu-id="95a25-121">-Confirm</span></span>
<span data-ttu-id="95a25-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="95a25-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95a25-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95a25-123">-WhatIf</span></span>
<span data-ttu-id="95a25-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="95a25-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95a25-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="95a25-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95a25-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95a25-126">CommonParameters</span></span>
<span data-ttu-id="95a25-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="95a25-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95a25-128">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="95a25-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95a25-129">輸入</span><span class="sxs-lookup"><span data-stu-id="95a25-129">INPUTS</span></span>

### <span data-ttu-id="95a25-130">System.String</span><span class="sxs-lookup"><span data-stu-id="95a25-130">System.String</span></span>

## <span data-ttu-id="95a25-131">輸出</span><span class="sxs-lookup"><span data-stu-id="95a25-131">OUTPUTS</span></span>

### <span data-ttu-id="95a25-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="95a25-132">System.Boolean</span></span>

## <span data-ttu-id="95a25-133">筆記</span><span class="sxs-lookup"><span data-stu-id="95a25-133">NOTES</span></span>

## <span data-ttu-id="95a25-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="95a25-134">RELATED LINKS</span></span>

[<span data-ttu-id="95a25-135">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="95a25-135">Get-AzStreamAnalyticsFunction</span></span>](./Get-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="95a25-136">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="95a25-136">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="95a25-137">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="95a25-137">Test-AzStreamAnalyticsFunction</span></span>](./Test-AzStreamAnalyticsFunction.md)


