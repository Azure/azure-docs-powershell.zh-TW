---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgriddomainkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainKey.md
ms.openlocfilehash: 4d72be4f7ddbe6cd5884269c724c7505cc05fffc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612482"
---
# <span data-ttu-id="aa880-101">Get-AzEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="aa880-101">Get-AzEventGridDomainKey</span></span>

## <span data-ttu-id="aa880-102">摘要</span><span class="sxs-lookup"><span data-stu-id="aa880-102">SYNOPSIS</span></span>
<span data-ttu-id="aa880-103">取得用來將事件發佈至事件格線網域的共用便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="aa880-103">Gets the shared access keys used to publish events to an Event Grid domain.</span></span>

## <span data-ttu-id="aa880-104">句法</span><span class="sxs-lookup"><span data-stu-id="aa880-104">SYNTAX</span></span>

### <span data-ttu-id="aa880-105">DomainNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="aa880-105">DomainNameParameterSet (Default)</span></span>
```
Get-AzEventGridDomainKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa880-106">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa880-106">DomainInputObjectParameterSet</span></span>
```
Get-AzEventGridDomainKey [-DomainObject] <PSDomain> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="aa880-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa880-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridDomainKey [-DomainResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aa880-108">說明</span><span class="sxs-lookup"><span data-stu-id="aa880-108">DESCRIPTION</span></span>
<span data-ttu-id="aa880-109">取得用來將事件發佈至事件格線網域的共用便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="aa880-109">Gets the shared access keys used to publish events to an Event Grid domain.</span></span>

## <span data-ttu-id="aa880-110">示例</span><span class="sxs-lookup"><span data-stu-id="aa880-110">EXAMPLES</span></span>

### <span data-ttu-id="aa880-111">範例1</span><span class="sxs-lookup"><span data-stu-id="aa880-111">Example 1</span></span>

<span data-ttu-id="aa880-112">取得 \` \` 資源群組 MyResourceGroupName 中事件 Grid 網域 Domain1 的共用便捷鍵 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="aa880-112">Gets the shared access keys of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomainKey -ResourceGroup MyResourceGroupName -Name Domain1

Key1                                         Key2
----                                         ----
<Key1 value>                                <Key 2 value>
```

### <span data-ttu-id="aa880-113">範例2</span><span class="sxs-lookup"><span data-stu-id="aa880-113">Example 2</span></span>

<span data-ttu-id="aa880-114">取得 \` \` 資源群組 MyResourceGroupName 中事件 Grid 網域 Domain1 的共用便捷鍵 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="aa880-114">Gets the shared access keys of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Name Domain1 | Get-AzEventGridDomainKey

Key1                                         Key2
----                                         ----
<Key1 value>                                <Key 2 value>
```

## <span data-ttu-id="aa880-115">參數</span><span class="sxs-lookup"><span data-stu-id="aa880-115">PARAMETERS</span></span>

### <span data-ttu-id="aa880-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa880-116">-DefaultProfile</span></span>
<span data-ttu-id="aa880-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="aa880-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa880-118">-DomainObject</span><span class="sxs-lookup"><span data-stu-id="aa880-118">-DomainObject</span></span>
<span data-ttu-id="aa880-119">EventGrid Domain 物件。</span><span class="sxs-lookup"><span data-stu-id="aa880-119">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="aa880-120">-DomainResourceId</span><span class="sxs-lookup"><span data-stu-id="aa880-120">-DomainResourceId</span></span>
<span data-ttu-id="aa880-121">代表事件網格網域的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="aa880-121">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="aa880-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="aa880-122">-Name</span></span>
<span data-ttu-id="aa880-123">EventGrid [功能變數名稱]。</span><span class="sxs-lookup"><span data-stu-id="aa880-123">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa880-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa880-124">-ResourceGroupName</span></span>
<span data-ttu-id="aa880-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="aa880-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa880-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa880-126">CommonParameters</span></span>
<span data-ttu-id="aa880-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="aa880-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa880-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="aa880-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa880-129">輸入</span><span class="sxs-lookup"><span data-stu-id="aa880-129">INPUTS</span></span>

### <span data-ttu-id="aa880-130">System.object</span><span class="sxs-lookup"><span data-stu-id="aa880-130">System.String</span></span>

### <span data-ttu-id="aa880-131">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="aa880-131">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="aa880-132">輸出</span><span class="sxs-lookup"><span data-stu-id="aa880-132">OUTPUTS</span></span>

### <span data-ttu-id="aa880-133">DomainSharedAccessKeys 中的 EventGrid。</span><span class="sxs-lookup"><span data-stu-id="aa880-133">Microsoft.Azure.Management.EventGrid.Models.DomainSharedAccessKeys</span></span>

## <span data-ttu-id="aa880-134">筆記</span><span class="sxs-lookup"><span data-stu-id="aa880-134">NOTES</span></span>

## <span data-ttu-id="aa880-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="aa880-135">RELATED LINKS</span></span>
