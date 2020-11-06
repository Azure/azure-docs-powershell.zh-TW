---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: D82270AD-50C2-4980-ABE2-58049C187875
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/new-azurermschedulerjobcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: 479b91f222852ebfc356d320cf880eb2ae99db6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447242"
---
# <span data-ttu-id="80e72-101">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="80e72-101">New-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="80e72-102">摘要</span><span class="sxs-lookup"><span data-stu-id="80e72-102">SYNOPSIS</span></span>
<span data-ttu-id="80e72-103">建立作業集合。</span><span class="sxs-lookup"><span data-stu-id="80e72-103">Creates a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80e72-104">句法</span><span class="sxs-lookup"><span data-stu-id="80e72-104">SYNTAX</span></span>

```
New-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> -Location <String>
 [-Plan <String>] [-MaxJobCount <Int32>] [-Frequency <String>] [-Interval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80e72-105">說明</span><span class="sxs-lookup"><span data-stu-id="80e72-105">DESCRIPTION</span></span>
<span data-ttu-id="80e72-106">**新的-AzureRmSchedulerJobCollection** Cmdlet 會在 Azure 排程器中建立作業集合。</span><span class="sxs-lookup"><span data-stu-id="80e72-106">The **New-AzureRmSchedulerJobCollection** cmdlet creates a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="80e72-107">示例</span><span class="sxs-lookup"><span data-stu-id="80e72-107">EXAMPLES</span></span>

## <span data-ttu-id="80e72-108">參數</span><span class="sxs-lookup"><span data-stu-id="80e72-108">PARAMETERS</span></span>

### <span data-ttu-id="80e72-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80e72-109">-DefaultProfile</span></span>
<span data-ttu-id="80e72-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="80e72-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80e72-111">頻率</span><span class="sxs-lookup"><span data-stu-id="80e72-111">-Frequency</span></span>
<span data-ttu-id="80e72-112">指定您可以在作業集合中的任何工作上指定的最大頻率。</span><span class="sxs-lookup"><span data-stu-id="80e72-112">Specifies the maximum frequency that you can specify on any job in the job collection.</span></span>
<span data-ttu-id="80e72-113">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="80e72-113">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="80e72-114">數</span><span class="sxs-lookup"><span data-stu-id="80e72-114">Minute</span></span> 
- <span data-ttu-id="80e72-115">每</span><span class="sxs-lookup"><span data-stu-id="80e72-115">Hour</span></span> 
- <span data-ttu-id="80e72-116">之內</span><span class="sxs-lookup"><span data-stu-id="80e72-116">Day</span></span> 
- <span data-ttu-id="80e72-117">周</span><span class="sxs-lookup"><span data-stu-id="80e72-117">Week</span></span> 
- <span data-ttu-id="80e72-118">月</span><span class="sxs-lookup"><span data-stu-id="80e72-118">Month</span></span>

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

### <span data-ttu-id="80e72-119">間隔</span><span class="sxs-lookup"><span data-stu-id="80e72-119">-Interval</span></span>
<span data-ttu-id="80e72-120">指定週期的間隔。</span><span class="sxs-lookup"><span data-stu-id="80e72-120">Specifies an interval of recurrence.</span></span>

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

### <span data-ttu-id="80e72-121">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="80e72-121">-JobCollectionName</span></span>
<span data-ttu-id="80e72-122">指定作業集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="80e72-122">Specifies a name for the job collection.</span></span>

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

### <span data-ttu-id="80e72-123">-位置</span><span class="sxs-lookup"><span data-stu-id="80e72-123">-Location</span></span>
<span data-ttu-id="80e72-124">指定此 Cmdlet 建立作業集合所用的 Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="80e72-124">Specifies the Azure region in which this cmdlet creates the job collection.</span></span>

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

### <span data-ttu-id="80e72-125">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="80e72-125">-MaxJobCount</span></span>
<span data-ttu-id="80e72-126">指定您可以在作業集合中建立的作業數目上限。</span><span class="sxs-lookup"><span data-stu-id="80e72-126">Specifies the maximum number of jobs that you can create in the job collection.</span></span>
<span data-ttu-id="80e72-127">[最大值] 視 *方案* 參數指定的方案而定。</span><span class="sxs-lookup"><span data-stu-id="80e72-127">The maximum depends on the plan that the *Plan* parameter specifies.</span></span>

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

### <span data-ttu-id="80e72-128">-方案</span><span class="sxs-lookup"><span data-stu-id="80e72-128">-Plan</span></span>
<span data-ttu-id="80e72-129">指定作業集合方案。</span><span class="sxs-lookup"><span data-stu-id="80e72-129">Specifies the job collection plan.</span></span>
<span data-ttu-id="80e72-130">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="80e72-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="80e72-131">空閒</span><span class="sxs-lookup"><span data-stu-id="80e72-131">Free</span></span> 
- <span data-ttu-id="80e72-132">標準</span><span class="sxs-lookup"><span data-stu-id="80e72-132">Standard</span></span> 
- <span data-ttu-id="80e72-133">P10Premium</span><span class="sxs-lookup"><span data-stu-id="80e72-133">P10Premium</span></span> 
- <span data-ttu-id="80e72-134">P20Premium</span><span class="sxs-lookup"><span data-stu-id="80e72-134">P20Premium</span></span>

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

### <span data-ttu-id="80e72-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80e72-135">-ResourceGroupName</span></span>
<span data-ttu-id="80e72-136">指定作業集合的資源群組。</span><span class="sxs-lookup"><span data-stu-id="80e72-136">Specifies the resource group for the job collection.</span></span>

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

### <span data-ttu-id="80e72-137">-確認</span><span class="sxs-lookup"><span data-stu-id="80e72-137">-Confirm</span></span>
<span data-ttu-id="80e72-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="80e72-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80e72-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80e72-139">-WhatIf</span></span>
<span data-ttu-id="80e72-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="80e72-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80e72-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="80e72-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80e72-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80e72-142">CommonParameters</span></span>
<span data-ttu-id="80e72-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="80e72-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80e72-144">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="80e72-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80e72-145">輸入</span><span class="sxs-lookup"><span data-stu-id="80e72-145">INPUTS</span></span>

### <span data-ttu-id="80e72-146">System.object</span><span class="sxs-lookup"><span data-stu-id="80e72-146">System.String</span></span>

## <span data-ttu-id="80e72-147">輸出</span><span class="sxs-lookup"><span data-stu-id="80e72-147">OUTPUTS</span></span>

### <span data-ttu-id="80e72-148">PSJobCollectionDefinition 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="80e72-148">Microsoft.Azure.Commands.Scheduler.Models.PSJobCollectionDefinition</span></span>

## <span data-ttu-id="80e72-149">筆記</span><span class="sxs-lookup"><span data-stu-id="80e72-149">NOTES</span></span>

## <span data-ttu-id="80e72-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="80e72-150">RELATED LINKS</span></span>

[<span data-ttu-id="80e72-151">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="80e72-151">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="80e72-152">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="80e72-152">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="80e72-153">AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="80e72-153">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="80e72-154">移除-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="80e72-154">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="80e72-155">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="80e72-155">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


