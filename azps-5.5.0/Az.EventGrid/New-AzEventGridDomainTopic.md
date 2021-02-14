---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainTopic.md
ms.openlocfilehash: 2923f05bc954c0570c49886c3a036ef78848a1e7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100136211"
---
# <span data-ttu-id="3241f-101">New-AzEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="3241f-101">New-AzEventGridDomainTopic</span></span>

## <span data-ttu-id="3241f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3241f-102">SYNOPSIS</span></span>
<span data-ttu-id="3241f-103">建立新的 Azure 事件 Grid 網域主題。</span><span class="sxs-lookup"><span data-stu-id="3241f-103">Creates a new Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="3241f-104">句法</span><span class="sxs-lookup"><span data-stu-id="3241f-104">SYNTAX</span></span>

```
New-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3241f-105">說明</span><span class="sxs-lookup"><span data-stu-id="3241f-105">DESCRIPTION</span></span>
<span data-ttu-id="3241f-106">建立新的 Azure 事件 Grid 網域主題。</span><span class="sxs-lookup"><span data-stu-id="3241f-106">Creates a new Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="3241f-107">示例</span><span class="sxs-lookup"><span data-stu-id="3241f-107">EXAMPLES</span></span>

### <span data-ttu-id="3241f-108">範例1</span><span class="sxs-lookup"><span data-stu-id="3241f-108">Example 1</span></span>

<span data-ttu-id="3241f-109">建立事件格線網域主題 \` Topic1 \` 在網域 Domain1 中的 [ \` \` 資源群組 MyResourceGroupName] 下 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="3241f-109">Creates an Event Grid Domain Topic \`Topic1\` in Domain \`Domain1\` under resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> New-AzEventGridDomainTopic -ResourceGroupName MyResourceGroupName -DomainName Domain1 -Name Topic1

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : topic1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/topic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

## <span data-ttu-id="3241f-110">參數</span><span class="sxs-lookup"><span data-stu-id="3241f-110">PARAMETERS</span></span>

### <span data-ttu-id="3241f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3241f-111">-DefaultProfile</span></span>
<span data-ttu-id="3241f-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3241f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3241f-113">-功能變數名稱</span><span class="sxs-lookup"><span data-stu-id="3241f-113">-DomainName</span></span>
<span data-ttu-id="3241f-114">EventGrid [功能變數名稱]。</span><span class="sxs-lookup"><span data-stu-id="3241f-114">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Domain

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3241f-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="3241f-115">-Name</span></span>
<span data-ttu-id="3241f-116">EventGrid [網域主題名稱]。</span><span class="sxs-lookup"><span data-stu-id="3241f-116">EventGrid domain topic name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DomainTopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3241f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3241f-117">-ResourceGroupName</span></span>
<span data-ttu-id="3241f-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3241f-118">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3241f-119">-確認</span><span class="sxs-lookup"><span data-stu-id="3241f-119">-Confirm</span></span>
<span data-ttu-id="3241f-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3241f-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3241f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3241f-121">-WhatIf</span></span>
<span data-ttu-id="3241f-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3241f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3241f-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3241f-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3241f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3241f-124">CommonParameters</span></span>
<span data-ttu-id="3241f-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3241f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3241f-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3241f-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3241f-127">輸入</span><span class="sxs-lookup"><span data-stu-id="3241f-127">INPUTS</span></span>

### <span data-ttu-id="3241f-128">System.object</span><span class="sxs-lookup"><span data-stu-id="3241f-128">System.String</span></span>

## <span data-ttu-id="3241f-129">輸出</span><span class="sxs-lookup"><span data-stu-id="3241f-129">OUTPUTS</span></span>

### <span data-ttu-id="3241f-130">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="3241f-130">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="3241f-131">筆記</span><span class="sxs-lookup"><span data-stu-id="3241f-131">NOTES</span></span>

## <span data-ttu-id="3241f-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="3241f-132">RELATED LINKS</span></span>
