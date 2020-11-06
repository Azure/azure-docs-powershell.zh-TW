---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: 774699A8-8916-4F2A-973E-97E5E487D42E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/remove-azurermschedulerjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Remove-AzureRmSchedulerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Remove-AzureRmSchedulerJob.md
ms.openlocfilehash: 6a15f51290efec856494737881693c3d1fae0620
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447238"
---
# <span data-ttu-id="d8b2c-101">Remove-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="d8b2c-101">Remove-AzureRmSchedulerJob</span></span>

## <span data-ttu-id="d8b2c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d8b2c-102">SYNOPSIS</span></span>
<span data-ttu-id="d8b2c-103">移除排程作業。</span><span class="sxs-lookup"><span data-stu-id="d8b2c-103">Removes a Scheduler job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8b2c-104">句法</span><span class="sxs-lookup"><span data-stu-id="d8b2c-104">SYNTAX</span></span>

```
Remove-AzureRmSchedulerJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8b2c-105">說明</span><span class="sxs-lookup"><span data-stu-id="d8b2c-105">DESCRIPTION</span></span>
<span data-ttu-id="d8b2c-106">**AzureRmSchedulerJob** Cmdlet 會移除 Azure 排程作業。</span><span class="sxs-lookup"><span data-stu-id="d8b2c-106">The **Remove-AzureRmSchedulerJob** cmdlet removes an Azure Scheduler job.</span></span>

## <span data-ttu-id="d8b2c-107">示例</span><span class="sxs-lookup"><span data-stu-id="d8b2c-107">EXAMPLES</span></span>

## <span data-ttu-id="d8b2c-108">參數</span><span class="sxs-lookup"><span data-stu-id="d8b2c-108">PARAMETERS</span></span>

### <span data-ttu-id="d8b2c-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8b2c-109">-DefaultProfile</span></span>
<span data-ttu-id="d8b2c-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d8b2c-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8b2c-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="d8b2c-111">-JobCollectionName</span></span>
<span data-ttu-id="d8b2c-112">指定包含要移除作業之作業集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="d8b2c-112">Specifies the name of a job collection that contains the job to remove.</span></span>

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

### <span data-ttu-id="d8b2c-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="d8b2c-113">-JobName</span></span>
<span data-ttu-id="d8b2c-114">指定要移除的作業名稱。</span><span class="sxs-lookup"><span data-stu-id="d8b2c-114">Specifies the name of a job to remove.</span></span>

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

### <span data-ttu-id="d8b2c-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d8b2c-115">-PassThru</span></span>
<span data-ttu-id="d8b2c-116">表示此 Cmdlet 會傳回成功的成功值。</span><span class="sxs-lookup"><span data-stu-id="d8b2c-116">Indicates that this cmdlet returns a value of Success on success.</span></span>
<span data-ttu-id="d8b2c-117">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="d8b2c-117">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8b2c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8b2c-118">-ResourceGroupName</span></span>
<span data-ttu-id="d8b2c-119">指定要移除作業的資源群組。</span><span class="sxs-lookup"><span data-stu-id="d8b2c-119">Specifies the resource group of the job to remove.</span></span>

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

### <span data-ttu-id="d8b2c-120">-確認</span><span class="sxs-lookup"><span data-stu-id="d8b2c-120">-Confirm</span></span>
<span data-ttu-id="d8b2c-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d8b2c-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8b2c-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8b2c-122">-WhatIf</span></span>
<span data-ttu-id="d8b2c-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d8b2c-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8b2c-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d8b2c-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8b2c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8b2c-125">CommonParameters</span></span>
<span data-ttu-id="d8b2c-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d8b2c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8b2c-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d8b2c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8b2c-128">輸入</span><span class="sxs-lookup"><span data-stu-id="d8b2c-128">INPUTS</span></span>

### <span data-ttu-id="d8b2c-129">System.object</span><span class="sxs-lookup"><span data-stu-id="d8b2c-129">System.String</span></span>

## <span data-ttu-id="d8b2c-130">輸出</span><span class="sxs-lookup"><span data-stu-id="d8b2c-130">OUTPUTS</span></span>

### <span data-ttu-id="d8b2c-131">System.object</span><span class="sxs-lookup"><span data-stu-id="d8b2c-131">System.String</span></span>

## <span data-ttu-id="d8b2c-132">筆記</span><span class="sxs-lookup"><span data-stu-id="d8b2c-132">NOTES</span></span>

## <span data-ttu-id="d8b2c-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="d8b2c-133">RELATED LINKS</span></span>

[<span data-ttu-id="d8b2c-134">AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="d8b2c-134">Get-AzureRmSchedulerJob</span></span>](./Get-AzureRmSchedulerJob.md)


