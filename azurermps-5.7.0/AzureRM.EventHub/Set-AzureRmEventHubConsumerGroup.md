---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/set-azurermeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubConsumerGroup.md
ms.openlocfilehash: 743928771fdba7ed17fe2643cf9e92ae7c2d9860
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444548"
---
# <span data-ttu-id="0ecd8-101">Set-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="0ecd8-101">Set-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="0ecd8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0ecd8-102">SYNOPSIS</span></span>
<span data-ttu-id="0ecd8-103">更新指定的事件中樞消費者群組。</span><span class="sxs-lookup"><span data-stu-id="0ecd8-103">Updates the specified Event Hubs consumer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ecd8-104">句法</span><span class="sxs-lookup"><span data-stu-id="0ecd8-104">SYNTAX</span></span>

```
Set-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0ecd8-105">說明</span><span class="sxs-lookup"><span data-stu-id="0ecd8-105">DESCRIPTION</span></span>
<span data-ttu-id="0ecd8-106">Set-AzureRmEventHubConsumerGroup Cmdlet 會更新指定的事件中樞消費者群組。</span><span class="sxs-lookup"><span data-stu-id="0ecd8-106">The Set-AzureRmEventHubConsumerGroup cmdlet updates the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="0ecd8-107">示例</span><span class="sxs-lookup"><span data-stu-id="0ecd8-107">EXAMPLES</span></span>

### <span data-ttu-id="0ecd8-108">範例1</span><span class="sxs-lookup"><span data-stu-id="0ecd8-108">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName -UserMetadata "Testing"
```

<span data-ttu-id="0ecd8-109">將消費者群組 MyConsumerGroupName 的使用者中繼資料 \` 設定 \` 為「測試」。</span><span class="sxs-lookup"><span data-stu-id="0ecd8-109">Sets the user metadata of the consumer group \`MyConsumerGroupName\` to "Testing."</span></span>

## <span data-ttu-id="0ecd8-110">參數</span><span class="sxs-lookup"><span data-stu-id="0ecd8-110">PARAMETERS</span></span>

### <span data-ttu-id="0ecd8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ecd8-111">-DefaultProfile</span></span>
<span data-ttu-id="0ecd8-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0ecd8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ecd8-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="0ecd8-113">-EventHub</span></span>
<span data-ttu-id="0ecd8-114">EventHub 名稱</span><span class="sxs-lookup"><span data-stu-id="0ecd8-114">EventHub Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ecd8-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="0ecd8-115">-Name</span></span>
<span data-ttu-id="0ecd8-116">ConsumerGroup 名稱</span><span class="sxs-lookup"><span data-stu-id="0ecd8-116">ConsumerGroup Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ecd8-117">-命名空間</span><span class="sxs-lookup"><span data-stu-id="0ecd8-117">-Namespace</span></span>
<span data-ttu-id="0ecd8-118">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="0ecd8-118">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ecd8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ecd8-119">-ResourceGroupName</span></span>
<span data-ttu-id="0ecd8-120">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="0ecd8-120">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ecd8-121">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="0ecd8-121">-UserMetadata</span></span>
<span data-ttu-id="0ecd8-122">ConsumerGroup 的使用者中繼資料</span><span class="sxs-lookup"><span data-stu-id="0ecd8-122">User Metadata for ConsumerGroup</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ecd8-123">-確認</span><span class="sxs-lookup"><span data-stu-id="0ecd8-123">-Confirm</span></span>
<span data-ttu-id="0ecd8-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0ecd8-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ecd8-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ecd8-125">-WhatIf</span></span>
<span data-ttu-id="0ecd8-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0ecd8-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ecd8-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0ecd8-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ecd8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ecd8-128">CommonParameters</span></span>
<span data-ttu-id="0ecd8-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0ecd8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="0ecd8-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0ecd8-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ecd8-131">輸入</span><span class="sxs-lookup"><span data-stu-id="0ecd8-131">INPUTS</span></span>

### <span data-ttu-id="0ecd8-132">System.object</span><span class="sxs-lookup"><span data-stu-id="0ecd8-132">System.String</span></span>


## <span data-ttu-id="0ecd8-133">輸出</span><span class="sxs-lookup"><span data-stu-id="0ecd8-133">OUTPUTS</span></span>

### <span data-ttu-id="0ecd8-134">PSConsumerGroupAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="0ecd8-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>


## <span data-ttu-id="0ecd8-135">筆記</span><span class="sxs-lookup"><span data-stu-id="0ecd8-135">NOTES</span></span>

## <span data-ttu-id="0ecd8-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="0ecd8-136">RELATED LINKS</span></span>
