---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/get-azeventgriddomainkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainKey.md
ms.openlocfilehash: a211e3857cd81a5dd057795fb9e2956d60cbae17
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910101"
---
# <span data-ttu-id="00930-101">Get-AzEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="00930-101">Get-AzEventGridDomainKey</span></span>

## <span data-ttu-id="00930-102">簡介</span><span class="sxs-lookup"><span data-stu-id="00930-102">SYNOPSIS</span></span>
<span data-ttu-id="00930-103">取得用來將事件發佈至事件格線網域的共用便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="00930-103">Gets the shared access keys used to publish events to an Event Grid domain.</span></span>

## <span data-ttu-id="00930-104">語法</span><span class="sxs-lookup"><span data-stu-id="00930-104">SYNTAX</span></span>

### <span data-ttu-id="00930-105">DomainNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="00930-105">DomainNameParameterSet (Default)</span></span>
```
Get-AzEventGridDomainKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00930-106">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="00930-106">DomainInputObjectParameterSet</span></span>
```
Get-AzEventGridDomainKey [-DomainObject] <PSDomain> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="00930-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="00930-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridDomainKey [-DomainResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="00930-108">描述</span><span class="sxs-lookup"><span data-stu-id="00930-108">DESCRIPTION</span></span>
<span data-ttu-id="00930-109">取得用來將事件發佈至事件格線網域的共用便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="00930-109">Gets the shared access keys used to publish events to an Event Grid domain.</span></span>

## <span data-ttu-id="00930-110">例子</span><span class="sxs-lookup"><span data-stu-id="00930-110">EXAMPLES</span></span>

### <span data-ttu-id="00930-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="00930-111">Example 1</span></span>

<span data-ttu-id="00930-112">取得資源群組 MyResourceGroupName 中 Event Grid 網域網域1 的 \` \` \` 共用便捷鍵 \` 。</span><span class="sxs-lookup"><span data-stu-id="00930-112">Gets the shared access keys of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomainKey -ResourceGroup MyResourceGroupName -Name Domain1

Key1                                         Key2
----                                         ----
<Key1 value>                                <Key 2 value>
```

### <span data-ttu-id="00930-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="00930-113">Example 2</span></span>

<span data-ttu-id="00930-114">取得資源群組 MyResourceGroupName 中 Event Grid 網域網域1 的 \` \` \` 共用便捷鍵 \` 。</span><span class="sxs-lookup"><span data-stu-id="00930-114">Gets the shared access keys of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Name Domain1 | Get-AzEventGridDomainKey

Key1                                         Key2
----                                         ----
<Key1 value>                                <Key 2 value>
```

## <span data-ttu-id="00930-115">參數</span><span class="sxs-lookup"><span data-stu-id="00930-115">PARAMETERS</span></span>

### <span data-ttu-id="00930-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00930-116">-DefaultProfile</span></span>
<span data-ttu-id="00930-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="00930-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00930-118">-DomainObject</span><span class="sxs-lookup"><span data-stu-id="00930-118">-DomainObject</span></span>
<span data-ttu-id="00930-119">EventGrid 網域物件。</span><span class="sxs-lookup"><span data-stu-id="00930-119">EventGrid Domain object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomain
Parameter Sets: DomainInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="00930-120">-DomainResourceId</span><span class="sxs-lookup"><span data-stu-id="00930-120">-DomainResourceId</span></span>
<span data-ttu-id="00930-121">代表事件格線網域的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="00930-121">Resource Identifier representing the Event Grid Domain.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00930-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="00930-122">-Name</span></span>
<span data-ttu-id="00930-123">EventGrid 功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="00930-123">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00930-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00930-124">-ResourceGroupName</span></span>
<span data-ttu-id="00930-125">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="00930-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00930-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00930-126">CommonParameters</span></span>
<span data-ttu-id="00930-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="00930-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00930-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="00930-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00930-129">輸入</span><span class="sxs-lookup"><span data-stu-id="00930-129">INPUTS</span></span>

### <span data-ttu-id="00930-130">System.String</span><span class="sxs-lookup"><span data-stu-id="00930-130">System.String</span></span>

### <span data-ttu-id="00930-131">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="00930-131">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="00930-132">輸出</span><span class="sxs-lookup"><span data-stu-id="00930-132">OUTPUTS</span></span>

### <span data-ttu-id="00930-133">Microsoft.Azure.management.EventGrid.models.DomainSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="00930-133">Microsoft.Azure.Management.EventGrid.Models.DomainSharedAccessKeys</span></span>

## <span data-ttu-id="00930-134">筆記</span><span class="sxs-lookup"><span data-stu-id="00930-134">NOTES</span></span>

## <span data-ttu-id="00930-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="00930-135">RELATED LINKS</span></span>
