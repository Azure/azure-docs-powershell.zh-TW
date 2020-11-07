---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicKey.md
ms.openlocfilehash: 91e3acd227acd8a83dcd5ccb0beb2ed12d1cca99
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626308"
---
# <span data-ttu-id="d9678-101">Get-AzureRmEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="d9678-101">Get-AzureRmEventGridTopicKey</span></span>

## <span data-ttu-id="d9678-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d9678-102">SYNOPSIS</span></span>
<span data-ttu-id="d9678-103">取得用來將事件發佈至事件格線主題的共用便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="d9678-103">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9678-104">句法</span><span class="sxs-lookup"><span data-stu-id="d9678-104">SYNTAX</span></span>

### <span data-ttu-id="d9678-105">TopicNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d9678-105">TopicNameParameterSet (Default)</span></span>
```
Get-AzureRmEventGridTopicKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9678-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9678-106">TopicInputObjectParameterSet</span></span>
```
Get-AzureRmEventGridTopicKey [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d9678-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9678-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzureRmEventGridTopicKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d9678-108">說明</span><span class="sxs-lookup"><span data-stu-id="d9678-108">DESCRIPTION</span></span>
<span data-ttu-id="d9678-109">取得用來將事件發佈至事件格線主題的共用便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="d9678-109">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="d9678-110">示例</span><span class="sxs-lookup"><span data-stu-id="d9678-110">EXAMPLES</span></span>

### <span data-ttu-id="d9678-111">範例1</span><span class="sxs-lookup"><span data-stu-id="d9678-111">Example 1</span></span>
```
PS C:\> Get-AzureRmEventGridTopicKey -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="d9678-112">取得 \` Topic1 \` 資源群組 MyResourceGroupName 中事件格線主題的共用訪問 \` 鍵 \` 。</span><span class="sxs-lookup"><span data-stu-id="d9678-112">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="d9678-113">範例2</span><span class="sxs-lookup"><span data-stu-id="d9678-113">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | Get-AzureRmEventGridTopicKey
```

<span data-ttu-id="d9678-114">取得 \` Topic1 \` 資源群組 MyResourceGroupName 中事件格線主題的共用訪問 \` 鍵 \` 。</span><span class="sxs-lookup"><span data-stu-id="d9678-114">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="d9678-115">參數</span><span class="sxs-lookup"><span data-stu-id="d9678-115">PARAMETERS</span></span>

### <span data-ttu-id="d9678-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9678-116">-InputObject</span></span>
<span data-ttu-id="d9678-117">EventGrid 主題物件。</span><span class="sxs-lookup"><span data-stu-id="d9678-117">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="d9678-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="d9678-118">-Name</span></span>
<span data-ttu-id="d9678-119">EventGrid 主題名稱。</span><span class="sxs-lookup"><span data-stu-id="d9678-119">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="d9678-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9678-120">-ResourceGroupName</span></span>
<span data-ttu-id="d9678-121">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="d9678-121">Resource Group Name.</span></span>

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

### <span data-ttu-id="d9678-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d9678-122">-ResourceId</span></span>
<span data-ttu-id="d9678-123">代表事件格線主題的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d9678-123">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="d9678-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9678-124">-DefaultProfile</span></span>
<span data-ttu-id="d9678-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d9678-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9678-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9678-126">CommonParameters</span></span>
<span data-ttu-id="d9678-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d9678-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9678-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d9678-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9678-129">輸入</span><span class="sxs-lookup"><span data-stu-id="d9678-129">INPUTS</span></span>

### <span data-ttu-id="d9678-130">System.object</span><span class="sxs-lookup"><span data-stu-id="d9678-130">System.String</span></span>

## <span data-ttu-id="d9678-131">輸出</span><span class="sxs-lookup"><span data-stu-id="d9678-131">OUTPUTS</span></span>

### <span data-ttu-id="d9678-132">TopicSharedAccessKeys 中的 EventGrid。</span><span class="sxs-lookup"><span data-stu-id="d9678-132">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="d9678-133">筆記</span><span class="sxs-lookup"><span data-stu-id="d9678-133">NOTES</span></span>

## <span data-ttu-id="d9678-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="d9678-134">RELATED LINKS</span></span>

