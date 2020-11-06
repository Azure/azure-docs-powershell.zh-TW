---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 75B0776E-32D5-4EE4-B35C-73E13185A4F1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsFunction.md
ms.openlocfilehash: 10687094bcbbc6cc9a52e648d830d46eac089c4d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454800"
---
# <span data-ttu-id="16ed7-101">Remove-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="16ed7-101">Remove-AzureRmStreamAnalyticsFunction</span></span>

## <span data-ttu-id="16ed7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="16ed7-102">SYNOPSIS</span></span>
<span data-ttu-id="16ed7-103">從資料流程分析作業中刪除函數。</span><span class="sxs-lookup"><span data-stu-id="16ed7-103">Deletes a function from a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16ed7-104">句法</span><span class="sxs-lookup"><span data-stu-id="16ed7-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16ed7-105">說明</span><span class="sxs-lookup"><span data-stu-id="16ed7-105">DESCRIPTION</span></span>
<span data-ttu-id="16ed7-106">**AzureRmStreamAnalyticsFunction** Cmdlet 會從 Azure Stream Analytics 作業非同步刪除函數。</span><span class="sxs-lookup"><span data-stu-id="16ed7-106">The **Remove-AzureRmStreamAnalyticsFunction** cmdlet deletes a function asynchronously from an Azure Stream Analytics job.</span></span>

## <span data-ttu-id="16ed7-107">示例</span><span class="sxs-lookup"><span data-stu-id="16ed7-107">EXAMPLES</span></span>

### <span data-ttu-id="16ed7-108">範例1：移除資料流程分析函數</span><span class="sxs-lookup"><span data-stu-id="16ed7-108">Example 1: Remove a Stream Analytics function</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="16ed7-109">這個命令會從名為 StreamJob22 的作業中移除名為 ScoreTweet 的函數。</span><span class="sxs-lookup"><span data-stu-id="16ed7-109">This command removes the function named ScoreTweet from the job named StreamJob22.</span></span>

## <span data-ttu-id="16ed7-110">參數</span><span class="sxs-lookup"><span data-stu-id="16ed7-110">PARAMETERS</span></span>

### <span data-ttu-id="16ed7-111">-JobName</span><span class="sxs-lookup"><span data-stu-id="16ed7-111">-JobName</span></span>
<span data-ttu-id="16ed7-112">指定函數所屬的資料流程分析作業的名稱。</span><span class="sxs-lookup"><span data-stu-id="16ed7-112">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>
<span data-ttu-id="16ed7-113">這個 Cmdlet 會從此參數指定的作業中移除函數。</span><span class="sxs-lookup"><span data-stu-id="16ed7-113">This cmdlet removes a function from the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="16ed7-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="16ed7-114">-Name</span></span>
<span data-ttu-id="16ed7-115">指定此 Cmdlet 移除的資料流程分析函數的名稱。</span><span class="sxs-lookup"><span data-stu-id="16ed7-115">Specifies the name of the Stream Analytics function that this cmdlet removes.</span></span>

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

### <span data-ttu-id="16ed7-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16ed7-116">-ResourceGroupName</span></span>
<span data-ttu-id="16ed7-117">指定 Stream Analytics 函數所歸屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="16ed7-117">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="16ed7-118">這個 Cmdlet 會刪除此參數指定之資源群組中的函數。</span><span class="sxs-lookup"><span data-stu-id="16ed7-118">This cmdlet deletes a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="16ed7-119">-確認</span><span class="sxs-lookup"><span data-stu-id="16ed7-119">-Confirm</span></span>
<span data-ttu-id="16ed7-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="16ed7-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16ed7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16ed7-121">-WhatIf</span></span>
<span data-ttu-id="16ed7-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="16ed7-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16ed7-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="16ed7-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16ed7-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16ed7-124">-DefaultProfile</span></span>
<span data-ttu-id="16ed7-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="16ed7-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16ed7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16ed7-126">CommonParameters</span></span>
<span data-ttu-id="16ed7-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="16ed7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16ed7-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="16ed7-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16ed7-129">輸入</span><span class="sxs-lookup"><span data-stu-id="16ed7-129">INPUTS</span></span>

## <span data-ttu-id="16ed7-130">輸出</span><span class="sxs-lookup"><span data-stu-id="16ed7-130">OUTPUTS</span></span>

### <span data-ttu-id="16ed7-131">System.object</span><span class="sxs-lookup"><span data-stu-id="16ed7-131">System.Object</span></span>

## <span data-ttu-id="16ed7-132">筆記</span><span class="sxs-lookup"><span data-stu-id="16ed7-132">NOTES</span></span>

## <span data-ttu-id="16ed7-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="16ed7-133">RELATED LINKS</span></span>

[<span data-ttu-id="16ed7-134">AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="16ed7-134">Get-AzureRmStreamAnalyticsFunction</span></span>](./Get-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="16ed7-135">新-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="16ed7-135">New-AzureRmStreamAnalyticsFunction</span></span>](./New-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="16ed7-136">Test-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="16ed7-136">Test-AzureRmStreamAnalyticsFunction</span></span>](./Test-AzureRmStreamAnalyticsFunction.md)


