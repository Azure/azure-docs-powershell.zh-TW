---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: BA79EDC8-BE89-4836-92EF-748D6F518886
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Enable-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Enable-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: 16b86028dafa2f9fa35422b4346cd11496194bfe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449533"
---
# <span data-ttu-id="f3276-101">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="f3276-101">Enable-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="f3276-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f3276-102">SYNOPSIS</span></span>
<span data-ttu-id="f3276-103">啟用作業集合。</span><span class="sxs-lookup"><span data-stu-id="f3276-103">Enables a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3276-104">句法</span><span class="sxs-lookup"><span data-stu-id="f3276-104">SYNTAX</span></span>

```
Enable-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3276-105">說明</span><span class="sxs-lookup"><span data-stu-id="f3276-105">DESCRIPTION</span></span>
<span data-ttu-id="f3276-106">**Enable-AzureRmSchedulerJobCollection** Cmdlet 可在 Azure 排程器中啟用作業集合。</span><span class="sxs-lookup"><span data-stu-id="f3276-106">The **Enable-AzureRmSchedulerJobCollection** cmdlet enables a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="f3276-107">示例</span><span class="sxs-lookup"><span data-stu-id="f3276-107">EXAMPLES</span></span>

## <span data-ttu-id="f3276-108">參數</span><span class="sxs-lookup"><span data-stu-id="f3276-108">PARAMETERS</span></span>

### <span data-ttu-id="f3276-109">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="f3276-109">-JobCollectionName</span></span>
<span data-ttu-id="f3276-110">指定作業集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="f3276-110">Specifies the name of a job collection.</span></span>

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

### <span data-ttu-id="f3276-111">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f3276-111">-PassThru</span></span>
<span data-ttu-id="f3276-112">表示此 Cmdlet 會傳回成功的成功值。</span><span class="sxs-lookup"><span data-stu-id="f3276-112">Indicates that this cmdlet returns a value of Success on success.</span></span>
<span data-ttu-id="f3276-113">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="f3276-113">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f3276-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3276-114">-ResourceGroupName</span></span>
<span data-ttu-id="f3276-115">指定作業集合的資源群組。</span><span class="sxs-lookup"><span data-stu-id="f3276-115">Specifies the resource group of the job collection.</span></span>

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

### <span data-ttu-id="f3276-116">-確認</span><span class="sxs-lookup"><span data-stu-id="f3276-116">-Confirm</span></span>
<span data-ttu-id="f3276-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f3276-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3276-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3276-118">-WhatIf</span></span>
<span data-ttu-id="f3276-119">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f3276-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3276-120">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f3276-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3276-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3276-121">-DefaultProfile</span></span>
<span data-ttu-id="f3276-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f3276-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3276-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3276-123">CommonParameters</span></span>
<span data-ttu-id="f3276-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f3276-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3276-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f3276-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3276-126">輸入</span><span class="sxs-lookup"><span data-stu-id="f3276-126">INPUTS</span></span>

## <span data-ttu-id="f3276-127">輸出</span><span class="sxs-lookup"><span data-stu-id="f3276-127">OUTPUTS</span></span>

## <span data-ttu-id="f3276-128">筆記</span><span class="sxs-lookup"><span data-stu-id="f3276-128">NOTES</span></span>

## <span data-ttu-id="f3276-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="f3276-129">RELATED LINKS</span></span>

[<span data-ttu-id="f3276-130">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="f3276-130">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="f3276-131">AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="f3276-131">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="f3276-132">新-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="f3276-132">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="f3276-133">移除-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="f3276-133">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="f3276-134">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="f3276-134">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


