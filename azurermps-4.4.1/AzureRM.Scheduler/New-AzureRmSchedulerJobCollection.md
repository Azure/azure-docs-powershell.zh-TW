---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: D82270AD-50C2-4980-ABE2-58049C187875
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: d3577b906134a940a9339441f305d98c32b8fe74
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453276"
---
# <span data-ttu-id="677de-101">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="677de-101">New-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="677de-102">摘要</span><span class="sxs-lookup"><span data-stu-id="677de-102">SYNOPSIS</span></span>
<span data-ttu-id="677de-103">建立作業集合。</span><span class="sxs-lookup"><span data-stu-id="677de-103">Creates a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="677de-104">句法</span><span class="sxs-lookup"><span data-stu-id="677de-104">SYNTAX</span></span>

```
New-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> -Location <String>
 [-Plan <String>] [-MaxJobCount <Int32>] [-Frequency <String>] [-Interval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="677de-105">說明</span><span class="sxs-lookup"><span data-stu-id="677de-105">DESCRIPTION</span></span>
<span data-ttu-id="677de-106">**新的-AzureRmSchedulerJobCollection** Cmdlet 會在 Azure 排程器中建立作業集合。</span><span class="sxs-lookup"><span data-stu-id="677de-106">The **New-AzureRmSchedulerJobCollection** cmdlet creates a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="677de-107">示例</span><span class="sxs-lookup"><span data-stu-id="677de-107">EXAMPLES</span></span>

## <span data-ttu-id="677de-108">參數</span><span class="sxs-lookup"><span data-stu-id="677de-108">PARAMETERS</span></span>

### <span data-ttu-id="677de-109">頻率</span><span class="sxs-lookup"><span data-stu-id="677de-109">-Frequency</span></span>
<span data-ttu-id="677de-110">指定您可以在作業集合中的任何工作上指定的最大頻率。</span><span class="sxs-lookup"><span data-stu-id="677de-110">Specifies the maximum frequency that you can specify on any job in the job collection.</span></span>
<span data-ttu-id="677de-111">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="677de-111">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="677de-112">數</span><span class="sxs-lookup"><span data-stu-id="677de-112">Minute</span></span> 
- <span data-ttu-id="677de-113">每</span><span class="sxs-lookup"><span data-stu-id="677de-113">Hour</span></span> 
- <span data-ttu-id="677de-114">之內</span><span class="sxs-lookup"><span data-stu-id="677de-114">Day</span></span> 
- <span data-ttu-id="677de-115">周</span><span class="sxs-lookup"><span data-stu-id="677de-115">Week</span></span> 
- <span data-ttu-id="677de-116">月</span><span class="sxs-lookup"><span data-stu-id="677de-116">Month</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Minute, Hour, Day, Week, Month

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="677de-117">間隔</span><span class="sxs-lookup"><span data-stu-id="677de-117">-Interval</span></span>
<span data-ttu-id="677de-118">指定週期的間隔。</span><span class="sxs-lookup"><span data-stu-id="677de-118">Specifies an interval of recurrence.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="677de-119">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="677de-119">-JobCollectionName</span></span>
<span data-ttu-id="677de-120">指定作業集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="677de-120">Specifies a name for the job collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="677de-121">-位置</span><span class="sxs-lookup"><span data-stu-id="677de-121">-Location</span></span>
<span data-ttu-id="677de-122">指定此 Cmdlet 建立作業集合所用的 Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="677de-122">Specifies the Azure region in which this cmdlet creates the job collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="677de-123">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="677de-123">-MaxJobCount</span></span>
<span data-ttu-id="677de-124">指定您可以在作業集合中建立的作業數目上限。</span><span class="sxs-lookup"><span data-stu-id="677de-124">Specifies the maximum number of jobs that you can create in the job collection.</span></span>
<span data-ttu-id="677de-125">[最大值] 視 *方案* 參數指定的方案而定。</span><span class="sxs-lookup"><span data-stu-id="677de-125">The maximum depends on the plan that the *Plan* parameter specifies.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="677de-126">-方案</span><span class="sxs-lookup"><span data-stu-id="677de-126">-Plan</span></span>
<span data-ttu-id="677de-127">指定作業集合方案。</span><span class="sxs-lookup"><span data-stu-id="677de-127">Specifies the job collection plan.</span></span>
<span data-ttu-id="677de-128">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="677de-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="677de-129">空閒</span><span class="sxs-lookup"><span data-stu-id="677de-129">Free</span></span> 
- <span data-ttu-id="677de-130">標準</span><span class="sxs-lookup"><span data-stu-id="677de-130">Standard</span></span> 
- <span data-ttu-id="677de-131">P10Premium</span><span class="sxs-lookup"><span data-stu-id="677de-131">P10Premium</span></span> 
- <span data-ttu-id="677de-132">P20Premium</span><span class="sxs-lookup"><span data-stu-id="677de-132">P20Premium</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Free, Standard, P10Premium, P20Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="677de-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="677de-133">-ResourceGroupName</span></span>
<span data-ttu-id="677de-134">指定作業集合的資源群組。</span><span class="sxs-lookup"><span data-stu-id="677de-134">Specifies the resource group for the job collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="677de-135">-確認</span><span class="sxs-lookup"><span data-stu-id="677de-135">-Confirm</span></span>
<span data-ttu-id="677de-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="677de-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="677de-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="677de-137">-WhatIf</span></span>
<span data-ttu-id="677de-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="677de-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="677de-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="677de-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="677de-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="677de-140">-DefaultProfile</span></span>
<span data-ttu-id="677de-141">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="677de-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="677de-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="677de-142">CommonParameters</span></span>
<span data-ttu-id="677de-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="677de-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="677de-144">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="677de-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="677de-145">輸入</span><span class="sxs-lookup"><span data-stu-id="677de-145">INPUTS</span></span>

## <span data-ttu-id="677de-146">輸出</span><span class="sxs-lookup"><span data-stu-id="677de-146">OUTPUTS</span></span>

### <span data-ttu-id="677de-147">PSJobCollectionDefinition 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="677de-147">Microsoft.Azure.Commands.Scheduler.Models.PSJobCollectionDefinition</span></span>

## <span data-ttu-id="677de-148">筆記</span><span class="sxs-lookup"><span data-stu-id="677de-148">NOTES</span></span>

## <span data-ttu-id="677de-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="677de-149">RELATED LINKS</span></span>

[<span data-ttu-id="677de-150">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="677de-150">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="677de-151">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="677de-151">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="677de-152">AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="677de-152">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="677de-153">移除-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="677de-153">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="677de-154">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="677de-154">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


