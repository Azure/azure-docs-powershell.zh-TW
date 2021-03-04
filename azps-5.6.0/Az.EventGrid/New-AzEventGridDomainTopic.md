---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/new-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainTopic.md
ms.openlocfilehash: 18be852a8a44f55cbc159bdbc7b4dbf3f276582a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911989"
---
# <span data-ttu-id="b1239-101">New-AzEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="b1239-101">New-AzEventGridDomainTopic</span></span>

## <span data-ttu-id="b1239-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b1239-102">SYNOPSIS</span></span>
<span data-ttu-id="b1239-103">建立新的 Azure 事件格線網域主題。</span><span class="sxs-lookup"><span data-stu-id="b1239-103">Creates a new Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="b1239-104">語法</span><span class="sxs-lookup"><span data-stu-id="b1239-104">SYNTAX</span></span>

```
New-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1239-105">描述</span><span class="sxs-lookup"><span data-stu-id="b1239-105">DESCRIPTION</span></span>
<span data-ttu-id="b1239-106">建立新的 Azure 事件格線網域主題。</span><span class="sxs-lookup"><span data-stu-id="b1239-106">Creates a new Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="b1239-107">例子</span><span class="sxs-lookup"><span data-stu-id="b1239-107">EXAMPLES</span></span>

### <span data-ttu-id="b1239-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="b1239-108">Example 1</span></span>

<span data-ttu-id="b1239-109">在資源群組 \` \` MyResourceGroupName 下的 Domain Domain1 中建立事件格線 \` \` \` 網域主題 \` 1。</span><span class="sxs-lookup"><span data-stu-id="b1239-109">Creates an Event Grid Domain Topic \`Topic1\` in Domain \`Domain1\` under resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> New-AzEventGridDomainTopic -ResourceGroupName MyResourceGroupName -DomainName Domain1 -Name Topic1

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : topic1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/topic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

## <span data-ttu-id="b1239-110">參數</span><span class="sxs-lookup"><span data-stu-id="b1239-110">PARAMETERS</span></span>

### <span data-ttu-id="b1239-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1239-111">-DefaultProfile</span></span>
<span data-ttu-id="b1239-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b1239-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1239-113">-DomainName</span><span class="sxs-lookup"><span data-stu-id="b1239-113">-DomainName</span></span>
<span data-ttu-id="b1239-114">EventGrid 功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="b1239-114">EventGrid domain name.</span></span>

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

### <span data-ttu-id="b1239-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="b1239-115">-Name</span></span>
<span data-ttu-id="b1239-116">EventGrid 網域主題名稱。</span><span class="sxs-lookup"><span data-stu-id="b1239-116">EventGrid domain topic name.</span></span>

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

### <span data-ttu-id="b1239-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1239-117">-ResourceGroupName</span></span>
<span data-ttu-id="b1239-118">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1239-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="b1239-119">-確認</span><span class="sxs-lookup"><span data-stu-id="b1239-119">-Confirm</span></span>
<span data-ttu-id="b1239-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b1239-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1239-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1239-121">-WhatIf</span></span>
<span data-ttu-id="b1239-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b1239-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1239-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b1239-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1239-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1239-124">CommonParameters</span></span>
<span data-ttu-id="b1239-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b1239-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1239-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b1239-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1239-127">輸入</span><span class="sxs-lookup"><span data-stu-id="b1239-127">INPUTS</span></span>

### <span data-ttu-id="b1239-128">System.String</span><span class="sxs-lookup"><span data-stu-id="b1239-128">System.String</span></span>

## <span data-ttu-id="b1239-129">輸出</span><span class="sxs-lookup"><span data-stu-id="b1239-129">OUTPUTS</span></span>

### <span data-ttu-id="b1239-130">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="b1239-130">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="b1239-131">筆記</span><span class="sxs-lookup"><span data-stu-id="b1239-131">NOTES</span></span>

## <span data-ttu-id="b1239-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="b1239-132">RELATED LINKS</span></span>
