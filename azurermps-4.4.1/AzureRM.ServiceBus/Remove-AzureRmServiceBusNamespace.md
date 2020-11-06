---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 510b6bfcaf49d406a7be2f6e4f53b2227469566d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447986"
---
# <span data-ttu-id="78e85-101">Remove-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="78e85-101">Remove-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="78e85-102">摘要</span><span class="sxs-lookup"><span data-stu-id="78e85-102">SYNOPSIS</span></span>
<span data-ttu-id="78e85-103">從指定的資源群組中移除命名空間。</span><span class="sxs-lookup"><span data-stu-id="78e85-103">Removes the namespace from the specified resource group.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78e85-104">句法</span><span class="sxs-lookup"><span data-stu-id="78e85-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusNamespace [-ResourceGroup] <String> [-NamespaceName] <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="78e85-105">說明</span><span class="sxs-lookup"><span data-stu-id="78e85-105">DESCRIPTION</span></span>
<span data-ttu-id="78e85-106">**AzureRmServiceBusNamespace** Cmdlet 會從指定的資源群組中移除命名空間。</span><span class="sxs-lookup"><span data-stu-id="78e85-106">The **Remove-AzureRmServiceBusNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="78e85-107">示例</span><span class="sxs-lookup"><span data-stu-id="78e85-107">EXAMPLES</span></span>

### <span data-ttu-id="78e85-108">範例1</span><span class="sxs-lookup"><span data-stu-id="78e85-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="78e85-109">`SB-Example1`從指定的資源群組中移除服務匯流排命名空間 `Default-ServiceBus-WestUS` 。</span><span class="sxs-lookup"><span data-stu-id="78e85-109">Removes the Service Bus namespace `SB-Example1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="78e85-110">參數</span><span class="sxs-lookup"><span data-stu-id="78e85-110">PARAMETERS</span></span>

### <span data-ttu-id="78e85-111">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="78e85-111">-NamespaceName</span></span>
<span data-ttu-id="78e85-112">服務匯流排命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="78e85-112">The Service Bus namespace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78e85-113">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="78e85-113">-ResourceGroup</span></span>
<span data-ttu-id="78e85-114">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="78e85-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="78e85-115">-確認</span><span class="sxs-lookup"><span data-stu-id="78e85-115">-Confirm</span></span>
<span data-ttu-id="78e85-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="78e85-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78e85-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78e85-117">-WhatIf</span></span>
<span data-ttu-id="78e85-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="78e85-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78e85-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="78e85-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78e85-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78e85-120">CommonParameters</span></span>
<span data-ttu-id="78e85-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="78e85-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78e85-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="78e85-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78e85-123">輸入</span><span class="sxs-lookup"><span data-stu-id="78e85-123">INPUTS</span></span>

### <span data-ttu-id="78e85-124">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="78e85-124">-ResourceGroup</span></span>
 <span data-ttu-id="78e85-125">System.object</span><span class="sxs-lookup"><span data-stu-id="78e85-125">System.String</span></span>

### <span data-ttu-id="78e85-126">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="78e85-126">-NamespaceName</span></span>
 <span data-ttu-id="78e85-127">System.object</span><span class="sxs-lookup"><span data-stu-id="78e85-127">System.String</span></span>

## <span data-ttu-id="78e85-128">輸出</span><span class="sxs-lookup"><span data-stu-id="78e85-128">OUTPUTS</span></span>

### <span data-ttu-id="78e85-129">System.object</span><span class="sxs-lookup"><span data-stu-id="78e85-129">System.Object</span></span>

## <span data-ttu-id="78e85-130">筆記</span><span class="sxs-lookup"><span data-stu-id="78e85-130">NOTES</span></span>

## <span data-ttu-id="78e85-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="78e85-131">RELATED LINKS</span></span>

