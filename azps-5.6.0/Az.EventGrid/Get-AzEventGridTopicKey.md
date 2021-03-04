---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/get-azeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
ms.openlocfilehash: 92a70d16f8cd1db2c37c1247c994a3c406df5a54
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911998"
---
# <span data-ttu-id="8b9a5-101">Get-AzEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="8b9a5-101">Get-AzEventGridTopicKey</span></span>

## <span data-ttu-id="8b9a5-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8b9a5-102">SYNOPSIS</span></span>
<span data-ttu-id="8b9a5-103">取得用來將事件發佈至事件格線主題的共用便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="8b9a5-103">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="8b9a5-104">語法</span><span class="sxs-lookup"><span data-stu-id="8b9a5-104">SYNTAX</span></span>

### <span data-ttu-id="8b9a5-105">TopicNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="8b9a5-105">TopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridTopicKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b9a5-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b9a5-106">TopicInputObjectParameterSet</span></span>
```
Get-AzEventGridTopicKey [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8b9a5-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b9a5-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridTopicKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b9a5-108">描述</span><span class="sxs-lookup"><span data-stu-id="8b9a5-108">DESCRIPTION</span></span>
<span data-ttu-id="8b9a5-109">取得用來將事件發佈至事件格線主題的共用便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="8b9a5-109">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="8b9a5-110">例子</span><span class="sxs-lookup"><span data-stu-id="8b9a5-110">EXAMPLES</span></span>

### <span data-ttu-id="8b9a5-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="8b9a5-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridTopicKey -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="8b9a5-112">取得資源群組 \` MyResourceGroupName 中事件格線主題 Topic1 \` \` 的共用便捷鍵 \` 。</span><span class="sxs-lookup"><span data-stu-id="8b9a5-112">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="8b9a5-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="8b9a5-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | Get-AzEventGridTopicKey
```

<span data-ttu-id="8b9a5-114">取得資源群組 \` MyResourceGroupName 中事件格線主題 Topic1 \` \` 的共用便捷鍵 \` 。</span><span class="sxs-lookup"><span data-stu-id="8b9a5-114">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="8b9a5-115">參數</span><span class="sxs-lookup"><span data-stu-id="8b9a5-115">PARAMETERS</span></span>

### <span data-ttu-id="8b9a5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b9a5-116">-DefaultProfile</span></span>
<span data-ttu-id="8b9a5-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="8b9a5-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8b9a5-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8b9a5-118">-InputObject</span></span>
<span data-ttu-id="8b9a5-119">EventGrid Topic 物件。</span><span class="sxs-lookup"><span data-stu-id="8b9a5-119">EventGrid Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b9a5-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="8b9a5-120">-Name</span></span>
<span data-ttu-id="8b9a5-121">EventGrid 主題名稱。</span><span class="sxs-lookup"><span data-stu-id="8b9a5-121">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b9a5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b9a5-122">-ResourceGroupName</span></span>
<span data-ttu-id="8b9a5-123">資源組名。</span><span class="sxs-lookup"><span data-stu-id="8b9a5-123">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b9a5-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8b9a5-124">-ResourceId</span></span>
<span data-ttu-id="8b9a5-125">代表事件格線主題的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="8b9a5-125">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="8b9a5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b9a5-126">CommonParameters</span></span>
<span data-ttu-id="8b9a5-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8b9a5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b9a5-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8b9a5-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b9a5-129">輸入</span><span class="sxs-lookup"><span data-stu-id="8b9a5-129">INPUTS</span></span>

### <span data-ttu-id="8b9a5-130">System.String</span><span class="sxs-lookup"><span data-stu-id="8b9a5-130">System.String</span></span>

### <span data-ttu-id="8b9a5-131">Microsoft.Azure.Commands.EventGrid.models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="8b9a5-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="8b9a5-132">輸出</span><span class="sxs-lookup"><span data-stu-id="8b9a5-132">OUTPUTS</span></span>

### <span data-ttu-id="8b9a5-133">Microsoft.Azure.management.EventGrid.models.TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="8b9a5-133">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="8b9a5-134">筆記</span><span class="sxs-lookup"><span data-stu-id="8b9a5-134">NOTES</span></span>

## <span data-ttu-id="8b9a5-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="8b9a5-135">RELATED LINKS</span></span>
