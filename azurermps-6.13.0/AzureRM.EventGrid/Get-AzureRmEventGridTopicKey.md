---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/get-azurermeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicKey.md
ms.openlocfilehash: 8bd28b3bbe043663a451b235abf46c3a42e235e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626108"
---
# <span data-ttu-id="e0e1a-101">Get-AzureRmEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="e0e1a-101">Get-AzureRmEventGridTopicKey</span></span>

## <span data-ttu-id="e0e1a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e0e1a-102">SYNOPSIS</span></span>
<span data-ttu-id="e0e1a-103">取得用來將事件發佈至事件格線主題的共用便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="e0e1a-103">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0e1a-104">句法</span><span class="sxs-lookup"><span data-stu-id="e0e1a-104">SYNTAX</span></span>

### <span data-ttu-id="e0e1a-105">TopicNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e0e1a-105">TopicNameParameterSet (Default)</span></span>
```
Get-AzureRmEventGridTopicKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0e1a-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0e1a-106">TopicInputObjectParameterSet</span></span>
```
Get-AzureRmEventGridTopicKey [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e0e1a-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0e1a-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzureRmEventGridTopicKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e0e1a-108">說明</span><span class="sxs-lookup"><span data-stu-id="e0e1a-108">DESCRIPTION</span></span>
<span data-ttu-id="e0e1a-109">取得用來將事件發佈至事件格線主題的共用便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="e0e1a-109">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="e0e1a-110">示例</span><span class="sxs-lookup"><span data-stu-id="e0e1a-110">EXAMPLES</span></span>

### <span data-ttu-id="e0e1a-111">範例1</span><span class="sxs-lookup"><span data-stu-id="e0e1a-111">Example 1</span></span>
```
PS C:\> Get-AzureRmEventGridTopicKey -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="e0e1a-112">取得 \` Topic1 \` 資源群組 MyResourceGroupName 中事件格線主題的共用訪問 \` 鍵 \` 。</span><span class="sxs-lookup"><span data-stu-id="e0e1a-112">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="e0e1a-113">範例2</span><span class="sxs-lookup"><span data-stu-id="e0e1a-113">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | Get-AzureRmEventGridTopicKey
```

<span data-ttu-id="e0e1a-114">取得 \` Topic1 \` 資源群組 MyResourceGroupName 中事件格線主題的共用訪問 \` 鍵 \` 。</span><span class="sxs-lookup"><span data-stu-id="e0e1a-114">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="e0e1a-115">參數</span><span class="sxs-lookup"><span data-stu-id="e0e1a-115">PARAMETERS</span></span>

### <span data-ttu-id="e0e1a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0e1a-116">-DefaultProfile</span></span>
<span data-ttu-id="e0e1a-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e0e1a-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e0e1a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e0e1a-118">-InputObject</span></span>
<span data-ttu-id="e0e1a-119">EventGrid 主題物件。</span><span class="sxs-lookup"><span data-stu-id="e0e1a-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="e0e1a-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="e0e1a-120">-Name</span></span>
<span data-ttu-id="e0e1a-121">EventGrid 主題名稱。</span><span class="sxs-lookup"><span data-stu-id="e0e1a-121">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="e0e1a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0e1a-122">-ResourceGroupName</span></span>
<span data-ttu-id="e0e1a-123">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="e0e1a-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="e0e1a-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e0e1a-124">-ResourceId</span></span>
<span data-ttu-id="e0e1a-125">代表事件格線主題的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e0e1a-125">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="e0e1a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0e1a-126">CommonParameters</span></span>
<span data-ttu-id="e0e1a-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e0e1a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0e1a-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e0e1a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0e1a-129">輸入</span><span class="sxs-lookup"><span data-stu-id="e0e1a-129">INPUTS</span></span>

### <span data-ttu-id="e0e1a-130">System.object</span><span class="sxs-lookup"><span data-stu-id="e0e1a-130">System.String</span></span>

### <span data-ttu-id="e0e1a-131">PSTopic 中的 EventGrid。</span><span class="sxs-lookup"><span data-stu-id="e0e1a-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>
<span data-ttu-id="e0e1a-132">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="e0e1a-132">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="e0e1a-133">輸出</span><span class="sxs-lookup"><span data-stu-id="e0e1a-133">OUTPUTS</span></span>

### <span data-ttu-id="e0e1a-134">TopicSharedAccessKeys 中的 EventGrid。</span><span class="sxs-lookup"><span data-stu-id="e0e1a-134">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="e0e1a-135">筆記</span><span class="sxs-lookup"><span data-stu-id="e0e1a-135">NOTES</span></span>

## <span data-ttu-id="e0e1a-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="e0e1a-136">RELATED LINKS</span></span>
