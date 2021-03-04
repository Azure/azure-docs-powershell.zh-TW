---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 2F3BDDFE-7585-4802-BFA5-D110F846A33E
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/remove-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsJob.md
ms.openlocfilehash: 183aa9dd5cc7da6e0d86c1fa1018bcfe405c0f7e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907362"
---
# <span data-ttu-id="cf0d8-101">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="cf0d8-101">Remove-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="cf0d8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="cf0d8-102">SYNOPSIS</span></span>
<span data-ttu-id="cf0d8-103">移除 Stream Analytics 工作。</span><span class="sxs-lookup"><span data-stu-id="cf0d8-103">Removes a Stream Analytics job.</span></span>

## <span data-ttu-id="cf0d8-104">語法</span><span class="sxs-lookup"><span data-stu-id="cf0d8-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf0d8-105">描述</span><span class="sxs-lookup"><span data-stu-id="cf0d8-105">DESCRIPTION</span></span>
<span data-ttu-id="cf0d8-106">**Remove-AzStreamAnalyticsJob** Cmdlet 會非同步刪除 Azure 中的特定 Stream Analytics 工作。</span><span class="sxs-lookup"><span data-stu-id="cf0d8-106">The **Remove-AzStreamAnalyticsJob** cmdlet asynchronously deletes a specific Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="cf0d8-107">例子</span><span class="sxs-lookup"><span data-stu-id="cf0d8-107">EXAMPLES</span></span>

### <span data-ttu-id="cf0d8-108">範例 1：移除工作</span><span class="sxs-lookup"><span data-stu-id="cf0d8-108">EXAMPLE 1: Remove a job</span></span>
```
PS C:\>Remove-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="cf0d8-109">此命令會移除 StreamingJob 的工作。</span><span class="sxs-lookup"><span data-stu-id="cf0d8-109">This command removes the job StreamingJob.</span></span>

## <span data-ttu-id="cf0d8-110">參數</span><span class="sxs-lookup"><span data-stu-id="cf0d8-110">PARAMETERS</span></span>

### <span data-ttu-id="cf0d8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf0d8-111">-DefaultProfile</span></span>
<span data-ttu-id="cf0d8-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="cf0d8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf0d8-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="cf0d8-113">-Name</span></span>
<span data-ttu-id="cf0d8-114">指定要移除的 Azure Stream Analytics 工作名稱。</span><span class="sxs-lookup"><span data-stu-id="cf0d8-114">Specifies the name of the Azure Stream Analytics job to remove.</span></span>

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

### <span data-ttu-id="cf0d8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf0d8-115">-ResourceGroupName</span></span>
<span data-ttu-id="cf0d8-116">指定 Azure Stream Analytics 工作所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="cf0d8-116">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="cf0d8-117">-確認</span><span class="sxs-lookup"><span data-stu-id="cf0d8-117">-Confirm</span></span>
<span data-ttu-id="cf0d8-118">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="cf0d8-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf0d8-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf0d8-119">-WhatIf</span></span>
<span data-ttu-id="cf0d8-120">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cf0d8-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf0d8-121">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cf0d8-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf0d8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf0d8-122">CommonParameters</span></span>
<span data-ttu-id="cf0d8-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="cf0d8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf0d8-124">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="cf0d8-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf0d8-125">輸入</span><span class="sxs-lookup"><span data-stu-id="cf0d8-125">INPUTS</span></span>

### <span data-ttu-id="cf0d8-126">System.String</span><span class="sxs-lookup"><span data-stu-id="cf0d8-126">System.String</span></span>

## <span data-ttu-id="cf0d8-127">輸出</span><span class="sxs-lookup"><span data-stu-id="cf0d8-127">OUTPUTS</span></span>

### <span data-ttu-id="cf0d8-128">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cf0d8-128">System.Boolean</span></span>

## <span data-ttu-id="cf0d8-129">筆記</span><span class="sxs-lookup"><span data-stu-id="cf0d8-129">NOTES</span></span>

## <span data-ttu-id="cf0d8-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="cf0d8-130">RELATED LINKS</span></span>

[<span data-ttu-id="cf0d8-131">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="cf0d8-131">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="cf0d8-132">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="cf0d8-132">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="cf0d8-133">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="cf0d8-133">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)

[<span data-ttu-id="cf0d8-134">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="cf0d8-134">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)


