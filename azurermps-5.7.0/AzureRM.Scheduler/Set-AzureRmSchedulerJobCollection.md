---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: F9CF1EEB-6EFF-4C24-AC79-1328034D22A1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/set-azurermschedulerjobcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: fc2375e66dbc47ccadf11d0f7dd9dd66e42470de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624989"
---
# <span data-ttu-id="4fa87-101">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="4fa87-101">Set-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="4fa87-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4fa87-102">SYNOPSIS</span></span>
<span data-ttu-id="4fa87-103">修改作業集合。</span><span class="sxs-lookup"><span data-stu-id="4fa87-103">Modifies a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4fa87-104">句法</span><span class="sxs-lookup"><span data-stu-id="4fa87-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> [-Location <String>]
 [-Plan <String>] [-MaxJobCount <Int32>] [-Frequency <String>] [-Interval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fa87-105">說明</span><span class="sxs-lookup"><span data-stu-id="4fa87-105">DESCRIPTION</span></span>
<span data-ttu-id="4fa87-106">**AzureRmSchedulerJobCollection** Cmdlet 會修改 Azure 排程器中的作業集合。</span><span class="sxs-lookup"><span data-stu-id="4fa87-106">The **Set-AzureRmSchedulerJobCollection** cmdlet modifies a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="4fa87-107">示例</span><span class="sxs-lookup"><span data-stu-id="4fa87-107">EXAMPLES</span></span>

## <span data-ttu-id="4fa87-108">參數</span><span class="sxs-lookup"><span data-stu-id="4fa87-108">PARAMETERS</span></span>

### <span data-ttu-id="4fa87-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fa87-109">-DefaultProfile</span></span>
<span data-ttu-id="4fa87-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4fa87-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fa87-111">頻率</span><span class="sxs-lookup"><span data-stu-id="4fa87-111">-Frequency</span></span>
<span data-ttu-id="4fa87-112">指定您可以在作業集合中的任何工作上指定的最大頻率。</span><span class="sxs-lookup"><span data-stu-id="4fa87-112">Specifies the maximum frequency that you can specify on any job in the job collection.</span></span>
<span data-ttu-id="4fa87-113">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="4fa87-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4fa87-114">數</span><span class="sxs-lookup"><span data-stu-id="4fa87-114">Minute</span></span> 
- <span data-ttu-id="4fa87-115">每</span><span class="sxs-lookup"><span data-stu-id="4fa87-115">Hour</span></span> 
- <span data-ttu-id="4fa87-116">之內</span><span class="sxs-lookup"><span data-stu-id="4fa87-116">Day</span></span> 
- <span data-ttu-id="4fa87-117">周</span><span class="sxs-lookup"><span data-stu-id="4fa87-117">Week</span></span> 
- <span data-ttu-id="4fa87-118">月</span><span class="sxs-lookup"><span data-stu-id="4fa87-118">Month</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Minute, Hour, Day, Week, Month

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fa87-119">間隔</span><span class="sxs-lookup"><span data-stu-id="4fa87-119">-Interval</span></span>
<span data-ttu-id="4fa87-120">指定週期的間隔。</span><span class="sxs-lookup"><span data-stu-id="4fa87-120">Specifies an interval of recurrence.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fa87-121">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="4fa87-121">-JobCollectionName</span></span>
<span data-ttu-id="4fa87-122">指定作業集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="4fa87-122">Specifies the name of a job collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fa87-123">-位置</span><span class="sxs-lookup"><span data-stu-id="4fa87-123">-Location</span></span>
<span data-ttu-id="4fa87-124">指定作業集合存在的 Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="4fa87-124">Specifies the Azure region in which the job collection exists.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fa87-125">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="4fa87-125">-MaxJobCount</span></span>
<span data-ttu-id="4fa87-126">指定您可以在作業集合中建立的作業數目上限。</span><span class="sxs-lookup"><span data-stu-id="4fa87-126">Specifies the maximum number of jobs that you can create in the job collection.</span></span>
<span data-ttu-id="4fa87-127">[最大值] 視 *方案* 參數指定的方案而定。</span><span class="sxs-lookup"><span data-stu-id="4fa87-127">The maximum depends on the plan that the *Plan* parameter specifies.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fa87-128">-方案</span><span class="sxs-lookup"><span data-stu-id="4fa87-128">-Plan</span></span>
<span data-ttu-id="4fa87-129">指定作業集合方案。</span><span class="sxs-lookup"><span data-stu-id="4fa87-129">Specifies the job collection plan.</span></span>
<span data-ttu-id="4fa87-130">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="4fa87-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4fa87-131">空閒</span><span class="sxs-lookup"><span data-stu-id="4fa87-131">Free</span></span> 
- <span data-ttu-id="4fa87-132">標準</span><span class="sxs-lookup"><span data-stu-id="4fa87-132">Standard</span></span> 
- <span data-ttu-id="4fa87-133">P10Premium</span><span class="sxs-lookup"><span data-stu-id="4fa87-133">P10Premium</span></span> 
- <span data-ttu-id="4fa87-134">P20Premium</span><span class="sxs-lookup"><span data-stu-id="4fa87-134">P20Premium</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Free, Standard, P10Premium, P20Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fa87-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fa87-135">-ResourceGroupName</span></span>
<span data-ttu-id="4fa87-136">指定作業集合的資源群組。</span><span class="sxs-lookup"><span data-stu-id="4fa87-136">Specifies the resource group of the job collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fa87-137">-確認</span><span class="sxs-lookup"><span data-stu-id="4fa87-137">-Confirm</span></span>
<span data-ttu-id="4fa87-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4fa87-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fa87-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fa87-139">-WhatIf</span></span>
<span data-ttu-id="4fa87-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4fa87-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fa87-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4fa87-141">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fa87-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fa87-142">CommonParameters</span></span>
<span data-ttu-id="4fa87-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4fa87-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fa87-144">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4fa87-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fa87-145">輸入</span><span class="sxs-lookup"><span data-stu-id="4fa87-145">INPUTS</span></span>

### <span data-ttu-id="4fa87-146">所有</span><span class="sxs-lookup"><span data-stu-id="4fa87-146">None</span></span>
<span data-ttu-id="4fa87-147">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="4fa87-147">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4fa87-148">輸出</span><span class="sxs-lookup"><span data-stu-id="4fa87-148">OUTPUTS</span></span>

### <span data-ttu-id="4fa87-149">PSJobCollectionDefinition 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4fa87-149">Microsoft.Azure.Commands.Scheduler.Models.PSJobCollectionDefinition</span></span>

## <span data-ttu-id="4fa87-150">筆記</span><span class="sxs-lookup"><span data-stu-id="4fa87-150">NOTES</span></span>

## <span data-ttu-id="4fa87-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="4fa87-151">RELATED LINKS</span></span>

[<span data-ttu-id="4fa87-152">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="4fa87-152">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="4fa87-153">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="4fa87-153">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="4fa87-154">AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="4fa87-154">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="4fa87-155">新-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="4fa87-155">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="4fa87-156">移除-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="4fa87-156">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)


