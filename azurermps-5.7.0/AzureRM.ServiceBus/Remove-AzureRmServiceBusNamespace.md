---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 5d58fe0b998f7998da7b3a456d005570929cb848
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624283"
---
# <span data-ttu-id="265fe-101">Remove-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="265fe-101">Remove-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="265fe-102">摘要</span><span class="sxs-lookup"><span data-stu-id="265fe-102">SYNOPSIS</span></span>
<span data-ttu-id="265fe-103">從指定的資源群組中移除命名空間。</span><span class="sxs-lookup"><span data-stu-id="265fe-103">Removes the namespace from the specified resource group.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="265fe-104">句法</span><span class="sxs-lookup"><span data-stu-id="265fe-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusNamespace [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="265fe-105">說明</span><span class="sxs-lookup"><span data-stu-id="265fe-105">DESCRIPTION</span></span>
<span data-ttu-id="265fe-106">**AzureRmServiceBusNamespace** Cmdlet 會從指定的資源群組中移除命名空間。</span><span class="sxs-lookup"><span data-stu-id="265fe-106">The **Remove-AzureRmServiceBusNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="265fe-107">示例</span><span class="sxs-lookup"><span data-stu-id="265fe-107">EXAMPLES</span></span>

### <span data-ttu-id="265fe-108">範例1</span><span class="sxs-lookup"><span data-stu-id="265fe-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="265fe-109">`SB-Example1`從指定的資源群組中移除服務匯流排命名空間 `Default-ServiceBus-WestUS` 。</span><span class="sxs-lookup"><span data-stu-id="265fe-109">Removes the Service Bus namespace `SB-Example1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="265fe-110">參數</span><span class="sxs-lookup"><span data-stu-id="265fe-110">PARAMETERS</span></span>

### <span data-ttu-id="265fe-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="265fe-111">-DefaultProfile</span></span>
<span data-ttu-id="265fe-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="265fe-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="265fe-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="265fe-113">-Name</span></span>
<span data-ttu-id="265fe-114">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="265fe-114">Namespace Name.</span></span>

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

### <span data-ttu-id="265fe-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="265fe-115">-ResourceGroupName</span></span>
<span data-ttu-id="265fe-116">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="265fe-116">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="265fe-117">-確認</span><span class="sxs-lookup"><span data-stu-id="265fe-117">-Confirm</span></span>
<span data-ttu-id="265fe-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="265fe-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="265fe-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="265fe-119">-WhatIf</span></span>
<span data-ttu-id="265fe-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="265fe-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="265fe-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="265fe-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="265fe-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="265fe-122">CommonParameters</span></span>
<span data-ttu-id="265fe-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="265fe-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="265fe-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="265fe-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="265fe-125">輸入</span><span class="sxs-lookup"><span data-stu-id="265fe-125">INPUTS</span></span>

### <span data-ttu-id="265fe-126">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="265fe-126">-ResourceGroup</span></span>
 <span data-ttu-id="265fe-127">System.object</span><span class="sxs-lookup"><span data-stu-id="265fe-127">System.String</span></span>

### <span data-ttu-id="265fe-128">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="265fe-128">-NamespaceName</span></span>
 <span data-ttu-id="265fe-129">System.object</span><span class="sxs-lookup"><span data-stu-id="265fe-129">System.String</span></span>

## <span data-ttu-id="265fe-130">輸出</span><span class="sxs-lookup"><span data-stu-id="265fe-130">OUTPUTS</span></span>

### <span data-ttu-id="265fe-131">System.object</span><span class="sxs-lookup"><span data-stu-id="265fe-131">System.Object</span></span>

## <span data-ttu-id="265fe-132">筆記</span><span class="sxs-lookup"><span data-stu-id="265fe-132">NOTES</span></span>

## <span data-ttu-id="265fe-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="265fe-133">RELATED LINKS</span></span>

