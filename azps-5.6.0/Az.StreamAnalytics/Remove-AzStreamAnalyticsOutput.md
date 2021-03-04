---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: EE41BE86-37D4-4A2B-9007-D019CD62BA9D
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/remove-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsOutput.md
ms.openlocfilehash: 950d761324f0750f2433b0b88edb5d37859945e2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909926"
---
# <span data-ttu-id="f3678-101">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="f3678-101">Remove-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="f3678-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f3678-102">SYNOPSIS</span></span>
<span data-ttu-id="f3678-103">刪除 Stream Analytics 工作的輸出。</span><span class="sxs-lookup"><span data-stu-id="f3678-103">Deletes an output from a Stream Analytics job.</span></span>

## <span data-ttu-id="f3678-104">語法</span><span class="sxs-lookup"><span data-stu-id="f3678-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3678-105">描述</span><span class="sxs-lookup"><span data-stu-id="f3678-105">DESCRIPTION</span></span>
<span data-ttu-id="f3678-106">**Remove-AzStreamAnalyticsOutput** Cmdlet 會非同步刪除 Azure 中 Stream Analytics 工作的輸出。</span><span class="sxs-lookup"><span data-stu-id="f3678-106">The **Remove-AzStreamAnalyticsOutput** cmdlet asynchronously deletes an output from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="f3678-107">例子</span><span class="sxs-lookup"><span data-stu-id="f3678-107">EXAMPLES</span></span>

### <span data-ttu-id="f3678-108">範例 1：移除工作的輸出</span><span class="sxs-lookup"><span data-stu-id="f3678-108">EXAMPLE 1: Remove an output from a job</span></span>
```
PS C:\>Remove-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="f3678-109">此命令會移除工作 StreamingJob 中的輸出。</span><span class="sxs-lookup"><span data-stu-id="f3678-109">This command removes the output Output in the job StreamingJob.</span></span>

## <span data-ttu-id="f3678-110">參數</span><span class="sxs-lookup"><span data-stu-id="f3678-110">PARAMETERS</span></span>

### <span data-ttu-id="f3678-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3678-111">-DefaultProfile</span></span>
<span data-ttu-id="f3678-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f3678-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3678-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="f3678-113">-JobName</span></span>
<span data-ttu-id="f3678-114">指定 Azure Stream Analytics 輸出所屬的 Azure Stream Analytics 工作名稱。</span><span class="sxs-lookup"><span data-stu-id="f3678-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="f3678-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="f3678-115">-Name</span></span>
<span data-ttu-id="f3678-116">指定要移除的 Azure Stream Analytics 輸出名稱。</span><span class="sxs-lookup"><span data-stu-id="f3678-116">Specifies the name of the Azure Stream Analytics output to remove.</span></span>

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

### <span data-ttu-id="f3678-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3678-117">-ResourceGroupName</span></span>
<span data-ttu-id="f3678-118">指定 Azure Stream Analytics 輸出所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="f3678-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="f3678-119">-確認</span><span class="sxs-lookup"><span data-stu-id="f3678-119">-Confirm</span></span>
<span data-ttu-id="f3678-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f3678-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3678-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3678-121">-WhatIf</span></span>
<span data-ttu-id="f3678-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f3678-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3678-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f3678-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3678-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3678-124">CommonParameters</span></span>
<span data-ttu-id="f3678-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f3678-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3678-126">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="f3678-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3678-127">輸入</span><span class="sxs-lookup"><span data-stu-id="f3678-127">INPUTS</span></span>

### <span data-ttu-id="f3678-128">System.String</span><span class="sxs-lookup"><span data-stu-id="f3678-128">System.String</span></span>

## <span data-ttu-id="f3678-129">輸出</span><span class="sxs-lookup"><span data-stu-id="f3678-129">OUTPUTS</span></span>

### <span data-ttu-id="f3678-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f3678-130">System.Boolean</span></span>

## <span data-ttu-id="f3678-131">筆記</span><span class="sxs-lookup"><span data-stu-id="f3678-131">NOTES</span></span>

## <span data-ttu-id="f3678-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="f3678-132">RELATED LINKS</span></span>

[<span data-ttu-id="f3678-133">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="f3678-133">Get-AzStreamAnalyticsOutput</span></span>](./Get-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="f3678-134">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="f3678-134">New-AzStreamAnalyticsOutput</span></span>](./New-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="f3678-135">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="f3678-135">Test-AzStreamAnalyticsOutput</span></span>](./Test-AzStreamAnalyticsOutput.md)


