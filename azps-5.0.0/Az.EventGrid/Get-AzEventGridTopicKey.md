---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
ms.openlocfilehash: b0690882cc230a92fd6e81e38832f2fc352e131c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138906"
---
# <span data-ttu-id="4f93b-101">Get-AzEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="4f93b-101">Get-AzEventGridTopicKey</span></span>

## <span data-ttu-id="4f93b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4f93b-102">SYNOPSIS</span></span>
<span data-ttu-id="4f93b-103">取得用來將事件發佈至事件格線主題的共用便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="4f93b-103">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="4f93b-104">句法</span><span class="sxs-lookup"><span data-stu-id="4f93b-104">SYNTAX</span></span>

### <span data-ttu-id="4f93b-105">TopicNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="4f93b-105">TopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridTopicKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f93b-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f93b-106">TopicInputObjectParameterSet</span></span>
```
Get-AzEventGridTopicKey [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4f93b-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f93b-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridTopicKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f93b-108">說明</span><span class="sxs-lookup"><span data-stu-id="4f93b-108">DESCRIPTION</span></span>
<span data-ttu-id="4f93b-109">取得用來將事件發佈至事件格線主題的共用便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="4f93b-109">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="4f93b-110">示例</span><span class="sxs-lookup"><span data-stu-id="4f93b-110">EXAMPLES</span></span>

### <span data-ttu-id="4f93b-111">範例1</span><span class="sxs-lookup"><span data-stu-id="4f93b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridTopicKey -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="4f93b-112">取得 \` Topic1 \` 資源群組 MyResourceGroupName 中事件格線主題的共用訪問 \` 鍵 \` 。</span><span class="sxs-lookup"><span data-stu-id="4f93b-112">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="4f93b-113">範例2</span><span class="sxs-lookup"><span data-stu-id="4f93b-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | Get-AzEventGridTopicKey
```

<span data-ttu-id="4f93b-114">取得 \` Topic1 \` 資源群組 MyResourceGroupName 中事件格線主題的共用訪問 \` 鍵 \` 。</span><span class="sxs-lookup"><span data-stu-id="4f93b-114">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="4f93b-115">參數</span><span class="sxs-lookup"><span data-stu-id="4f93b-115">PARAMETERS</span></span>

### <span data-ttu-id="4f93b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f93b-116">-DefaultProfile</span></span>
<span data-ttu-id="4f93b-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="4f93b-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4f93b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4f93b-118">-InputObject</span></span>
<span data-ttu-id="4f93b-119">EventGrid 主題物件。</span><span class="sxs-lookup"><span data-stu-id="4f93b-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="4f93b-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="4f93b-120">-Name</span></span>
<span data-ttu-id="4f93b-121">EventGrid 主題名稱。</span><span class="sxs-lookup"><span data-stu-id="4f93b-121">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="4f93b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f93b-122">-ResourceGroupName</span></span>
<span data-ttu-id="4f93b-123">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="4f93b-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="4f93b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4f93b-124">-ResourceId</span></span>
<span data-ttu-id="4f93b-125">代表事件格線主題的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="4f93b-125">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="4f93b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f93b-126">CommonParameters</span></span>
<span data-ttu-id="4f93b-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4f93b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f93b-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4f93b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f93b-129">輸入</span><span class="sxs-lookup"><span data-stu-id="4f93b-129">INPUTS</span></span>

### <span data-ttu-id="4f93b-130">System.object</span><span class="sxs-lookup"><span data-stu-id="4f93b-130">System.String</span></span>

### <span data-ttu-id="4f93b-131">PSTopic 中的 EventGrid。</span><span class="sxs-lookup"><span data-stu-id="4f93b-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="4f93b-132">輸出</span><span class="sxs-lookup"><span data-stu-id="4f93b-132">OUTPUTS</span></span>

### <span data-ttu-id="4f93b-133">TopicSharedAccessKeys 中的 EventGrid。</span><span class="sxs-lookup"><span data-stu-id="4f93b-133">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="4f93b-134">筆記</span><span class="sxs-lookup"><span data-stu-id="4f93b-134">NOTES</span></span>

## <span data-ttu-id="4f93b-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="4f93b-135">RELATED LINKS</span></span>
