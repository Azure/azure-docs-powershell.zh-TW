---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespace.md
ms.openlocfilehash: cec41bda56da33f22def6c44752effb3d705b935
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624092"
---
# <span data-ttu-id="b9e66-101">Remove-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="b9e66-101">Remove-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="b9e66-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b9e66-102">SYNOPSIS</span></span>
<span data-ttu-id="b9e66-103">移除指定的事件中樞命名空間。</span><span class="sxs-lookup"><span data-stu-id="b9e66-103">Removes the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9e66-104">句法</span><span class="sxs-lookup"><span data-stu-id="b9e66-104">SYNTAX</span></span>

```
Remove-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9e66-105">說明</span><span class="sxs-lookup"><span data-stu-id="b9e66-105">DESCRIPTION</span></span>
<span data-ttu-id="b9e66-106">Remove-AzureRmEventHubNamespace Cmdlet 會移除並刪除指定的事件中樞命名空間。</span><span class="sxs-lookup"><span data-stu-id="b9e66-106">The Remove-AzureRmEventHubNamespace cmdlet removes and deletes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="b9e66-107">示例</span><span class="sxs-lookup"><span data-stu-id="b9e66-107">EXAMPLES</span></span>

### <span data-ttu-id="b9e66-108">範例1</span><span class="sxs-lookup"><span data-stu-id="b9e66-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName
```

<span data-ttu-id="b9e66-109">移除 \` \` 資源群組 MyResourceGroupName 中的 [事件中心] 命名空間 MyNamespaceName \` \` 。</span><span class="sxs-lookup"><span data-stu-id="b9e66-109">Removes the Event Hubs namespace \`MyNamespaceName\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="b9e66-110">參數</span><span class="sxs-lookup"><span data-stu-id="b9e66-110">PARAMETERS</span></span>

### <span data-ttu-id="b9e66-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9e66-111">-DefaultProfile</span></span>
<span data-ttu-id="b9e66-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b9e66-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9e66-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="b9e66-113">-Name</span></span>
<span data-ttu-id="b9e66-114">EventHub 命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="b9e66-114">EventHub Namespace Name</span></span>

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

### <span data-ttu-id="b9e66-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9e66-115">-ResourceGroupName</span></span>
<span data-ttu-id="b9e66-116">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="b9e66-116">Resource Group Name</span></span>

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

### <span data-ttu-id="b9e66-117">-確認</span><span class="sxs-lookup"><span data-stu-id="b9e66-117">-Confirm</span></span>
<span data-ttu-id="b9e66-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b9e66-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9e66-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9e66-119">-WhatIf</span></span>
<span data-ttu-id="b9e66-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b9e66-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9e66-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b9e66-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9e66-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9e66-122">CommonParameters</span></span>
<span data-ttu-id="b9e66-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b9e66-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b9e66-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b9e66-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9e66-125">輸入</span><span class="sxs-lookup"><span data-stu-id="b9e66-125">INPUTS</span></span>

### <span data-ttu-id="b9e66-126">System.object</span><span class="sxs-lookup"><span data-stu-id="b9e66-126">System.String</span></span>


## <span data-ttu-id="b9e66-127">輸出</span><span class="sxs-lookup"><span data-stu-id="b9e66-127">OUTPUTS</span></span>

### <span data-ttu-id="b9e66-128">System.object</span><span class="sxs-lookup"><span data-stu-id="b9e66-128">System.Object</span></span>

## <span data-ttu-id="b9e66-129">筆記</span><span class="sxs-lookup"><span data-stu-id="b9e66-129">NOTES</span></span>

## <span data-ttu-id="b9e66-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="b9e66-130">RELATED LINKS</span></span>
