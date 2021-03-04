---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1449F64F-A8F9-4E8E-B62B-17DEF3A0FB30
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/remove-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsInput.md
ms.openlocfilehash: 2e0443976d36339c9866c08118ef08c37fafac48
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907377"
---
# <span data-ttu-id="49b09-101">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="49b09-101">Remove-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="49b09-102">簡介</span><span class="sxs-lookup"><span data-stu-id="49b09-102">SYNOPSIS</span></span>
<span data-ttu-id="49b09-103">刪除 Stream Analytics 工作中的輸入。</span><span class="sxs-lookup"><span data-stu-id="49b09-103">Deletes an input from a Stream Analytics job.</span></span>

## <span data-ttu-id="49b09-104">語法</span><span class="sxs-lookup"><span data-stu-id="49b09-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49b09-105">描述</span><span class="sxs-lookup"><span data-stu-id="49b09-105">DESCRIPTION</span></span>
<span data-ttu-id="49b09-106">**Remove-AzStreamAnalyticsInput** Cmdlet 會非同步刪除 Azure 中 Stream Analytics 工作的輸入。</span><span class="sxs-lookup"><span data-stu-id="49b09-106">The **Remove-AzStreamAnalyticsInput** cmdlet asynchronously deletes an input from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="49b09-107">例子</span><span class="sxs-lookup"><span data-stu-id="49b09-107">EXAMPLES</span></span>

### <span data-ttu-id="49b09-108">範例 1：從工作移除輸入串流</span><span class="sxs-lookup"><span data-stu-id="49b09-108">EXAMPLE 1: Remove an input stream from a job</span></span>
```
PS C:\>Remove-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EventStream"
```

<span data-ttu-id="49b09-109">此命令會從 StreamingJob 移除輸入的 EventStream。</span><span class="sxs-lookup"><span data-stu-id="49b09-109">This command removes the input EventStream from StreamingJob.</span></span>

## <span data-ttu-id="49b09-110">參數</span><span class="sxs-lookup"><span data-stu-id="49b09-110">PARAMETERS</span></span>

### <span data-ttu-id="49b09-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49b09-111">-DefaultProfile</span></span>
<span data-ttu-id="49b09-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="49b09-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49b09-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="49b09-113">-JobName</span></span>
<span data-ttu-id="49b09-114">指定 Azure Stream Analytics 輸入所屬的 Azure Stream Analytics 工作名稱。</span><span class="sxs-lookup"><span data-stu-id="49b09-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="49b09-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="49b09-115">-Name</span></span>
<span data-ttu-id="49b09-116">指定要移除的 Azure Stream Analytics 輸入名稱。</span><span class="sxs-lookup"><span data-stu-id="49b09-116">Specifies the name of the Azure Stream Analytics input to remove.</span></span>

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

### <span data-ttu-id="49b09-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49b09-117">-ResourceGroupName</span></span>
<span data-ttu-id="49b09-118">指定 Azure Stream Analytics 輸入所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="49b09-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="49b09-119">-確認</span><span class="sxs-lookup"><span data-stu-id="49b09-119">-Confirm</span></span>
<span data-ttu-id="49b09-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="49b09-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49b09-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49b09-121">-WhatIf</span></span>
<span data-ttu-id="49b09-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="49b09-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49b09-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="49b09-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49b09-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49b09-124">CommonParameters</span></span>
<span data-ttu-id="49b09-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="49b09-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49b09-126">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="49b09-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49b09-127">輸入</span><span class="sxs-lookup"><span data-stu-id="49b09-127">INPUTS</span></span>

### <span data-ttu-id="49b09-128">System.String</span><span class="sxs-lookup"><span data-stu-id="49b09-128">System.String</span></span>

## <span data-ttu-id="49b09-129">輸出</span><span class="sxs-lookup"><span data-stu-id="49b09-129">OUTPUTS</span></span>

### <span data-ttu-id="49b09-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="49b09-130">System.Boolean</span></span>

## <span data-ttu-id="49b09-131">筆記</span><span class="sxs-lookup"><span data-stu-id="49b09-131">NOTES</span></span>

## <span data-ttu-id="49b09-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="49b09-132">RELATED LINKS</span></span>

[<span data-ttu-id="49b09-133">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="49b09-133">New-AzStreamAnalyticsInput</span></span>](./New-AzStreamAnalyticsInput.md)

[<span data-ttu-id="49b09-134">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="49b09-134">Get-AzStreamAnalyticsInput</span></span>](./Get-AzStreamAnalyticsInput.md)

[<span data-ttu-id="49b09-135">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="49b09-135">Test-AzStreamAnalyticsInput</span></span>](./Test-AzStreamAnalyticsInput.md)


