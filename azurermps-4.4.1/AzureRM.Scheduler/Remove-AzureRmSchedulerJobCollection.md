---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: F315B193-C17B-41A9-B61D-0A0212B6B643
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Remove-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Remove-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: b1caa041f92312d3d122e758a9e63bc7299887b6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449531"
---
# <span data-ttu-id="f9bcc-101">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="f9bcc-101">Remove-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="f9bcc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f9bcc-102">SYNOPSIS</span></span>
<span data-ttu-id="f9bcc-103">移除作業集合。</span><span class="sxs-lookup"><span data-stu-id="f9bcc-103">Removes a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9bcc-104">句法</span><span class="sxs-lookup"><span data-stu-id="f9bcc-104">SYNTAX</span></span>

```
Remove-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9bcc-105">說明</span><span class="sxs-lookup"><span data-stu-id="f9bcc-105">DESCRIPTION</span></span>
<span data-ttu-id="f9bcc-106">**AzureRmSchedulerJobCollection** Cmdlet 會在 Azure 排程器中移除作業集合。</span><span class="sxs-lookup"><span data-stu-id="f9bcc-106">The **Remove-AzureRmSchedulerJobCollection** cmdlet removes a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="f9bcc-107">示例</span><span class="sxs-lookup"><span data-stu-id="f9bcc-107">EXAMPLES</span></span>

## <span data-ttu-id="f9bcc-108">參數</span><span class="sxs-lookup"><span data-stu-id="f9bcc-108">PARAMETERS</span></span>

### <span data-ttu-id="f9bcc-109">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="f9bcc-109">-JobCollectionName</span></span>
<span data-ttu-id="f9bcc-110">指定作業集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="f9bcc-110">Specifies the name of a job collection.</span></span>

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

### <span data-ttu-id="f9bcc-111">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f9bcc-111">-PassThru</span></span>
<span data-ttu-id="f9bcc-112">表示此 Cmdlet 會傳回成功的成功值。</span><span class="sxs-lookup"><span data-stu-id="f9bcc-112">Indicates that this cmdlet returns a value of Success on success.</span></span>
<span data-ttu-id="f9bcc-113">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="f9bcc-113">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f9bcc-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9bcc-114">-ResourceGroupName</span></span>
<span data-ttu-id="f9bcc-115">指定作業集合的資源群組。</span><span class="sxs-lookup"><span data-stu-id="f9bcc-115">Specifies the resource group of the job collection.</span></span>

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

### <span data-ttu-id="f9bcc-116">-確認</span><span class="sxs-lookup"><span data-stu-id="f9bcc-116">-Confirm</span></span>
<span data-ttu-id="f9bcc-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f9bcc-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9bcc-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9bcc-118">-WhatIf</span></span>
<span data-ttu-id="f9bcc-119">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f9bcc-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9bcc-120">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f9bcc-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9bcc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9bcc-121">-DefaultProfile</span></span>
<span data-ttu-id="f9bcc-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f9bcc-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9bcc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9bcc-123">CommonParameters</span></span>
<span data-ttu-id="f9bcc-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f9bcc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9bcc-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f9bcc-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9bcc-126">輸入</span><span class="sxs-lookup"><span data-stu-id="f9bcc-126">INPUTS</span></span>

## <span data-ttu-id="f9bcc-127">輸出</span><span class="sxs-lookup"><span data-stu-id="f9bcc-127">OUTPUTS</span></span>

## <span data-ttu-id="f9bcc-128">筆記</span><span class="sxs-lookup"><span data-stu-id="f9bcc-128">NOTES</span></span>

## <span data-ttu-id="f9bcc-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="f9bcc-129">RELATED LINKS</span></span>

[<span data-ttu-id="f9bcc-130">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="f9bcc-130">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="f9bcc-131">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="f9bcc-131">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="f9bcc-132">AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="f9bcc-132">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="f9bcc-133">新-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="f9bcc-133">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="f9bcc-134">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="f9bcc-134">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


