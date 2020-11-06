---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: 774699A8-8916-4F2A-973E-97E5E487D42E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/remove-azurermschedulerjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Remove-AzureRmSchedulerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Remove-AzureRmSchedulerJob.md
ms.openlocfilehash: de8f9e05cbec17d6a92f3c4e567bd5dce96005ad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450495"
---
# <span data-ttu-id="25823-101">Remove-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="25823-101">Remove-AzureRmSchedulerJob</span></span>

## <span data-ttu-id="25823-102">摘要</span><span class="sxs-lookup"><span data-stu-id="25823-102">SYNOPSIS</span></span>
<span data-ttu-id="25823-103">移除排程作業。</span><span class="sxs-lookup"><span data-stu-id="25823-103">Removes a Scheduler job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25823-104">句法</span><span class="sxs-lookup"><span data-stu-id="25823-104">SYNTAX</span></span>

```
Remove-AzureRmSchedulerJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25823-105">說明</span><span class="sxs-lookup"><span data-stu-id="25823-105">DESCRIPTION</span></span>
<span data-ttu-id="25823-106">**AzureRmSchedulerJob** Cmdlet 會移除 Azure 排程作業。</span><span class="sxs-lookup"><span data-stu-id="25823-106">The **Remove-AzureRmSchedulerJob** cmdlet removes an Azure Scheduler job.</span></span>

## <span data-ttu-id="25823-107">示例</span><span class="sxs-lookup"><span data-stu-id="25823-107">EXAMPLES</span></span>

## <span data-ttu-id="25823-108">參數</span><span class="sxs-lookup"><span data-stu-id="25823-108">PARAMETERS</span></span>

### <span data-ttu-id="25823-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25823-109">-DefaultProfile</span></span>
<span data-ttu-id="25823-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="25823-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25823-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="25823-111">-JobCollectionName</span></span>
<span data-ttu-id="25823-112">指定包含要移除作業之作業集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="25823-112">Specifies the name of a job collection that contains the job to remove.</span></span>

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

### <span data-ttu-id="25823-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="25823-113">-JobName</span></span>
<span data-ttu-id="25823-114">指定要移除的作業名稱。</span><span class="sxs-lookup"><span data-stu-id="25823-114">Specifies the name of a job to remove.</span></span>

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

### <span data-ttu-id="25823-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="25823-115">-PassThru</span></span>
<span data-ttu-id="25823-116">表示此 Cmdlet 會傳回成功的成功值。</span><span class="sxs-lookup"><span data-stu-id="25823-116">Indicates that this cmdlet returns a value of Success on success.</span></span>
<span data-ttu-id="25823-117">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="25823-117">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25823-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25823-118">-ResourceGroupName</span></span>
<span data-ttu-id="25823-119">指定要移除作業的資源群組。</span><span class="sxs-lookup"><span data-stu-id="25823-119">Specifies the resource group of the job to remove.</span></span>

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

### <span data-ttu-id="25823-120">-確認</span><span class="sxs-lookup"><span data-stu-id="25823-120">-Confirm</span></span>
<span data-ttu-id="25823-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="25823-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25823-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25823-122">-WhatIf</span></span>
<span data-ttu-id="25823-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="25823-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25823-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="25823-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25823-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25823-125">CommonParameters</span></span>
<span data-ttu-id="25823-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="25823-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25823-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="25823-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25823-128">輸入</span><span class="sxs-lookup"><span data-stu-id="25823-128">INPUTS</span></span>

### <span data-ttu-id="25823-129">所有</span><span class="sxs-lookup"><span data-stu-id="25823-129">None</span></span>
<span data-ttu-id="25823-130">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="25823-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="25823-131">輸出</span><span class="sxs-lookup"><span data-stu-id="25823-131">OUTPUTS</span></span>

## <span data-ttu-id="25823-132">筆記</span><span class="sxs-lookup"><span data-stu-id="25823-132">NOTES</span></span>

## <span data-ttu-id="25823-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="25823-133">RELATED LINKS</span></span>

[<span data-ttu-id="25823-134">AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="25823-134">Get-AzureRmSchedulerJob</span></span>](./Get-AzureRmSchedulerJob.md)


