---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: BA79EDC8-BE89-4836-92EF-748D6F518886
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/enable-azurermschedulerjobcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Enable-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Enable-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: 832b7659da0b71d804ddc1a8f19703b85fc8500b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625443"
---
# <span data-ttu-id="8c73d-101">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="8c73d-101">Enable-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="8c73d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8c73d-102">SYNOPSIS</span></span>
<span data-ttu-id="8c73d-103">啟用作業集合。</span><span class="sxs-lookup"><span data-stu-id="8c73d-103">Enables a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c73d-104">句法</span><span class="sxs-lookup"><span data-stu-id="8c73d-104">SYNTAX</span></span>

```
Enable-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c73d-105">說明</span><span class="sxs-lookup"><span data-stu-id="8c73d-105">DESCRIPTION</span></span>
<span data-ttu-id="8c73d-106">**Enable-AzureRmSchedulerJobCollection** Cmdlet 可在 Azure 排程器中啟用作業集合。</span><span class="sxs-lookup"><span data-stu-id="8c73d-106">The **Enable-AzureRmSchedulerJobCollection** cmdlet enables a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="8c73d-107">示例</span><span class="sxs-lookup"><span data-stu-id="8c73d-107">EXAMPLES</span></span>

## <span data-ttu-id="8c73d-108">參數</span><span class="sxs-lookup"><span data-stu-id="8c73d-108">PARAMETERS</span></span>

### <span data-ttu-id="8c73d-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c73d-109">-DefaultProfile</span></span>
<span data-ttu-id="8c73d-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8c73d-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c73d-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="8c73d-111">-JobCollectionName</span></span>
<span data-ttu-id="8c73d-112">指定作業集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="8c73d-112">Specifies the name of a job collection.</span></span>

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

### <span data-ttu-id="8c73d-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8c73d-113">-PassThru</span></span>
<span data-ttu-id="8c73d-114">表示此 Cmdlet 會傳回成功的成功值。</span><span class="sxs-lookup"><span data-stu-id="8c73d-114">Indicates that this cmdlet returns a value of Success on success.</span></span>
<span data-ttu-id="8c73d-115">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="8c73d-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8c73d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c73d-116">-ResourceGroupName</span></span>
<span data-ttu-id="8c73d-117">指定作業集合的資源群組。</span><span class="sxs-lookup"><span data-stu-id="8c73d-117">Specifies the resource group of the job collection.</span></span>

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

### <span data-ttu-id="8c73d-118">-確認</span><span class="sxs-lookup"><span data-stu-id="8c73d-118">-Confirm</span></span>
<span data-ttu-id="8c73d-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8c73d-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c73d-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c73d-120">-WhatIf</span></span>
<span data-ttu-id="8c73d-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8c73d-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c73d-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c73d-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c73d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c73d-123">CommonParameters</span></span>
<span data-ttu-id="8c73d-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8c73d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c73d-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8c73d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c73d-126">輸入</span><span class="sxs-lookup"><span data-stu-id="8c73d-126">INPUTS</span></span>

### <span data-ttu-id="8c73d-127">所有</span><span class="sxs-lookup"><span data-stu-id="8c73d-127">None</span></span>
<span data-ttu-id="8c73d-128">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="8c73d-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8c73d-129">輸出</span><span class="sxs-lookup"><span data-stu-id="8c73d-129">OUTPUTS</span></span>

## <span data-ttu-id="8c73d-130">筆記</span><span class="sxs-lookup"><span data-stu-id="8c73d-130">NOTES</span></span>

## <span data-ttu-id="8c73d-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="8c73d-131">RELATED LINKS</span></span>

[<span data-ttu-id="8c73d-132">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="8c73d-132">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="8c73d-133">AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="8c73d-133">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="8c73d-134">新-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="8c73d-134">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="8c73d-135">移除-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="8c73d-135">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="8c73d-136">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="8c73d-136">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


