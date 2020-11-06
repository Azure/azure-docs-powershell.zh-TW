---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 1449F64F-A8F9-4E8E-B62B-17DEF3A0FB30
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsInput.md
ms.openlocfilehash: f801a7c8dd83927e8aceebdc98138aa6ad39d31c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454799"
---
# <span data-ttu-id="b225d-101">Remove-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="b225d-101">Remove-AzureRmStreamAnalyticsInput</span></span>

## <span data-ttu-id="b225d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b225d-102">SYNOPSIS</span></span>
<span data-ttu-id="b225d-103">從資料流程分析作業中刪除輸入。</span><span class="sxs-lookup"><span data-stu-id="b225d-103">Deletes an input from a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b225d-104">句法</span><span class="sxs-lookup"><span data-stu-id="b225d-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b225d-105">說明</span><span class="sxs-lookup"><span data-stu-id="b225d-105">DESCRIPTION</span></span>
<span data-ttu-id="b225d-106">**AzureRmStreamAnalyticsInput** Cmdlet 會在 Azure 中非同步刪除資料流程分析作業的輸入。</span><span class="sxs-lookup"><span data-stu-id="b225d-106">The **Remove-AzureRmStreamAnalyticsInput** cmdlet asynchronously deletes an input from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="b225d-107">示例</span><span class="sxs-lookup"><span data-stu-id="b225d-107">EXAMPLES</span></span>

### <span data-ttu-id="b225d-108">範例1：從工作中移除輸入資料流程</span><span class="sxs-lookup"><span data-stu-id="b225d-108">EXAMPLE 1: Remove an input stream from a job</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EventStream"
```

<span data-ttu-id="b225d-109">這個命令會將輸入 EventStream 從 StreamingJob 中移除。</span><span class="sxs-lookup"><span data-stu-id="b225d-109">This command removes the input EventStream from StreamingJob.</span></span>

## <span data-ttu-id="b225d-110">參數</span><span class="sxs-lookup"><span data-stu-id="b225d-110">PARAMETERS</span></span>

### <span data-ttu-id="b225d-111">-JobName</span><span class="sxs-lookup"><span data-stu-id="b225d-111">-JobName</span></span>
<span data-ttu-id="b225d-112">指定 Azure 串流分析輸入所屬之 Azure 串流分析作業的名稱。</span><span class="sxs-lookup"><span data-stu-id="b225d-112">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="b225d-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="b225d-113">-Name</span></span>
<span data-ttu-id="b225d-114">指定要移除之 Azure 資料流程分析輸入的名稱。</span><span class="sxs-lookup"><span data-stu-id="b225d-114">Specifies the name of the Azure Stream Analytics input to remove.</span></span>

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

### <span data-ttu-id="b225d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b225d-115">-ResourceGroupName</span></span>
<span data-ttu-id="b225d-116">指定 Azure 串流分析輸入所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b225d-116">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="b225d-117">-確認</span><span class="sxs-lookup"><span data-stu-id="b225d-117">-Confirm</span></span>
<span data-ttu-id="b225d-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b225d-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b225d-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b225d-119">-WhatIf</span></span>
<span data-ttu-id="b225d-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b225d-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b225d-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b225d-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b225d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b225d-122">-DefaultProfile</span></span>
<span data-ttu-id="b225d-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b225d-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b225d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b225d-124">CommonParameters</span></span>
<span data-ttu-id="b225d-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b225d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b225d-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b225d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b225d-127">輸入</span><span class="sxs-lookup"><span data-stu-id="b225d-127">INPUTS</span></span>

## <span data-ttu-id="b225d-128">輸出</span><span class="sxs-lookup"><span data-stu-id="b225d-128">OUTPUTS</span></span>

### <span data-ttu-id="b225d-129">System.object</span><span class="sxs-lookup"><span data-stu-id="b225d-129">System.Object</span></span>

## <span data-ttu-id="b225d-130">筆記</span><span class="sxs-lookup"><span data-stu-id="b225d-130">NOTES</span></span>

## <span data-ttu-id="b225d-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="b225d-131">RELATED LINKS</span></span>

[<span data-ttu-id="b225d-132">新-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="b225d-132">New-AzureRmStreamAnalyticsInput</span></span>](./New-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="b225d-133">AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="b225d-133">Get-AzureRmStreamAnalyticsInput</span></span>](./Get-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="b225d-134">Test-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="b225d-134">Test-AzureRmStreamAnalyticsInput</span></span>](./Test-AzureRmStreamAnalyticsInput.md)


