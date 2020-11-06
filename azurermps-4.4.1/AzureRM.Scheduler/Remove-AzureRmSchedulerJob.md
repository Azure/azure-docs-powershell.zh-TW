---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: 774699A8-8916-4F2A-973E-97E5E487D42E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Remove-AzureRmSchedulerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Remove-AzureRmSchedulerJob.md
ms.openlocfilehash: 582953886b8ea39e04dee122c85d70884dabcf11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449532"
---
# <span data-ttu-id="bce15-101">Remove-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="bce15-101">Remove-AzureRmSchedulerJob</span></span>

## <span data-ttu-id="bce15-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bce15-102">SYNOPSIS</span></span>
<span data-ttu-id="bce15-103">移除排程作業。</span><span class="sxs-lookup"><span data-stu-id="bce15-103">Removes a Scheduler job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bce15-104">句法</span><span class="sxs-lookup"><span data-stu-id="bce15-104">SYNTAX</span></span>

```
Remove-AzureRmSchedulerJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bce15-105">說明</span><span class="sxs-lookup"><span data-stu-id="bce15-105">DESCRIPTION</span></span>
<span data-ttu-id="bce15-106">**AzureRmSchedulerJob** Cmdlet 會移除 Azure 排程作業。</span><span class="sxs-lookup"><span data-stu-id="bce15-106">The **Remove-AzureRmSchedulerJob** cmdlet removes an Azure Scheduler job.</span></span>

## <span data-ttu-id="bce15-107">示例</span><span class="sxs-lookup"><span data-stu-id="bce15-107">EXAMPLES</span></span>

## <span data-ttu-id="bce15-108">參數</span><span class="sxs-lookup"><span data-stu-id="bce15-108">PARAMETERS</span></span>

### <span data-ttu-id="bce15-109">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="bce15-109">-JobCollectionName</span></span>
<span data-ttu-id="bce15-110">指定包含要移除作業之作業集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="bce15-110">Specifies the name of a job collection that contains the job to remove.</span></span>

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

### <span data-ttu-id="bce15-111">-JobName</span><span class="sxs-lookup"><span data-stu-id="bce15-111">-JobName</span></span>
<span data-ttu-id="bce15-112">指定要移除的作業名稱。</span><span class="sxs-lookup"><span data-stu-id="bce15-112">Specifies the name of a job to remove.</span></span>

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

### <span data-ttu-id="bce15-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bce15-113">-PassThru</span></span>
<span data-ttu-id="bce15-114">表示此 Cmdlet 會傳回成功的成功值。</span><span class="sxs-lookup"><span data-stu-id="bce15-114">Indicates that this cmdlet returns a value of Success on success.</span></span>
<span data-ttu-id="bce15-115">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="bce15-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="bce15-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bce15-116">-ResourceGroupName</span></span>
<span data-ttu-id="bce15-117">指定要移除作業的資源群組。</span><span class="sxs-lookup"><span data-stu-id="bce15-117">Specifies the resource group of the job to remove.</span></span>

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

### <span data-ttu-id="bce15-118">-確認</span><span class="sxs-lookup"><span data-stu-id="bce15-118">-Confirm</span></span>
<span data-ttu-id="bce15-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bce15-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bce15-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bce15-120">-WhatIf</span></span>
<span data-ttu-id="bce15-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bce15-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bce15-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bce15-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bce15-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bce15-123">-DefaultProfile</span></span>
<span data-ttu-id="bce15-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bce15-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bce15-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bce15-125">CommonParameters</span></span>
<span data-ttu-id="bce15-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bce15-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bce15-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bce15-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bce15-128">輸入</span><span class="sxs-lookup"><span data-stu-id="bce15-128">INPUTS</span></span>

## <span data-ttu-id="bce15-129">輸出</span><span class="sxs-lookup"><span data-stu-id="bce15-129">OUTPUTS</span></span>

## <span data-ttu-id="bce15-130">筆記</span><span class="sxs-lookup"><span data-stu-id="bce15-130">NOTES</span></span>

## <span data-ttu-id="bce15-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="bce15-131">RELATED LINKS</span></span>

[<span data-ttu-id="bce15-132">AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="bce15-132">Get-AzureRmSchedulerJob</span></span>](./Get-AzureRmSchedulerJob.md)


