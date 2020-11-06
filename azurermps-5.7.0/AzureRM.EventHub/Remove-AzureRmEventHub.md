---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHub.md
ms.openlocfilehash: b546c4f610bb6bc8021547fa5f7f0516ffbc2371
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457176"
---
# <span data-ttu-id="addcf-101">Remove-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="addcf-101">Remove-AzureRmEventHub</span></span>

## <span data-ttu-id="addcf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="addcf-102">SYNOPSIS</span></span>
<span data-ttu-id="addcf-103">移除指定的事件中樞。</span><span class="sxs-lookup"><span data-stu-id="addcf-103">Removes the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="addcf-104">句法</span><span class="sxs-lookup"><span data-stu-id="addcf-104">SYNTAX</span></span>

```
Remove-AzureRmEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="addcf-105">說明</span><span class="sxs-lookup"><span data-stu-id="addcf-105">DESCRIPTION</span></span>
<span data-ttu-id="addcf-106">Remove-AzureRmEventHub Cmdlet 會從指定的命名空間中移除並刪除指定的事件中樞。</span><span class="sxs-lookup"><span data-stu-id="addcf-106">The Remove-AzureRmEventHub cmdlet removes and deletes the specified Event Hub from the given namespace.</span></span>

## <span data-ttu-id="addcf-107">示例</span><span class="sxs-lookup"><span data-stu-id="addcf-107">EXAMPLES</span></span>

### <span data-ttu-id="addcf-108">範例1</span><span class="sxs-lookup"><span data-stu-id="addcf-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="addcf-109">移除事件中心 \` MyEventHubName \` 。</span><span class="sxs-lookup"><span data-stu-id="addcf-109">Removes the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="addcf-110">參數</span><span class="sxs-lookup"><span data-stu-id="addcf-110">PARAMETERS</span></span>

### <span data-ttu-id="addcf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="addcf-111">-DefaultProfile</span></span>
<span data-ttu-id="addcf-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="addcf-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="addcf-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="addcf-113">-Name</span></span>
<span data-ttu-id="addcf-114">EventHub 名稱</span><span class="sxs-lookup"><span data-stu-id="addcf-114">EventHub Name</span></span>

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

### <span data-ttu-id="addcf-115">-命名空間</span><span class="sxs-lookup"><span data-stu-id="addcf-115">-Namespace</span></span>
<span data-ttu-id="addcf-116">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="addcf-116">Namespace Name</span></span>

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

### <span data-ttu-id="addcf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="addcf-117">-ResourceGroupName</span></span>
<span data-ttu-id="addcf-118">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="addcf-118">Resource Group Name</span></span>

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

### <span data-ttu-id="addcf-119">-確認</span><span class="sxs-lookup"><span data-stu-id="addcf-119">-Confirm</span></span>
<span data-ttu-id="addcf-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="addcf-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="addcf-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="addcf-121">-WhatIf</span></span>
<span data-ttu-id="addcf-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="addcf-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="addcf-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="addcf-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="addcf-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="addcf-124">CommonParameters</span></span>
<span data-ttu-id="addcf-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="addcf-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="addcf-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="addcf-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="addcf-127">輸入</span><span class="sxs-lookup"><span data-stu-id="addcf-127">INPUTS</span></span>

### <span data-ttu-id="addcf-128">System.object</span><span class="sxs-lookup"><span data-stu-id="addcf-128">System.String</span></span>


## <span data-ttu-id="addcf-129">輸出</span><span class="sxs-lookup"><span data-stu-id="addcf-129">OUTPUTS</span></span>

### <span data-ttu-id="addcf-130">System.object</span><span class="sxs-lookup"><span data-stu-id="addcf-130">System.Object</span></span>

## <span data-ttu-id="addcf-131">筆記</span><span class="sxs-lookup"><span data-stu-id="addcf-131">NOTES</span></span>

## <span data-ttu-id="addcf-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="addcf-132">RELATED LINKS</span></span>
