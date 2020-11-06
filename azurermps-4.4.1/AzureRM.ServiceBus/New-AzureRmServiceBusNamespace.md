---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 79b55b62c3f4add24e52a36756f83bd16466edbd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454851"
---
# <span data-ttu-id="d7bc7-101">New-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="d7bc7-101">New-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="d7bc7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d7bc7-102">SYNOPSIS</span></span>
<span data-ttu-id="d7bc7-103">建立新的服務匯流排命名空間。</span><span class="sxs-lookup"><span data-stu-id="d7bc7-103">Creates a new Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7bc7-104">句法</span><span class="sxs-lookup"><span data-stu-id="d7bc7-104">SYNTAX</span></span>

```
New-AzureRmServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-NamespaceName] <String>
 [-SkuName <String>] [-Tag <Hashtable>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7bc7-105">說明</span><span class="sxs-lookup"><span data-stu-id="d7bc7-105">DESCRIPTION</span></span>
<span data-ttu-id="d7bc7-106">**新的-AzureRmServiceBusNamespace** Cmdlet 會建立新的服務匯流排命名空間。</span><span class="sxs-lookup"><span data-stu-id="d7bc7-106">The **New-AzureRmServiceBusNamespace** cmdlet creates a new Service Bus namespace.</span></span> <span data-ttu-id="d7bc7-107">一旦建立之後，命名空間資源資訊清單就是不可變的。</span><span class="sxs-lookup"><span data-stu-id="d7bc7-107">Once created, the namespace resource manifest is immutable.</span></span> <span data-ttu-id="d7bc7-108">這個運算為冪等。</span><span class="sxs-lookup"><span data-stu-id="d7bc7-108">This operation is idempotent.</span></span>

## <span data-ttu-id="d7bc7-109">示例</span><span class="sxs-lookup"><span data-stu-id="d7bc7-109">EXAMPLES</span></span>

### <span data-ttu-id="d7bc7-110">範例1</span><span class="sxs-lookup"><span data-stu-id="d7bc7-110">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -Location WestUS -SkuName "Standard" -Tag @{Tag1="Tag1Value"}

Name               : SB-Example1
Id                 : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
Location           : West US
Sku                : Name : Standard , Capacity : 1 , Tier : Standard
ProvisioningState  : Succeeded
Status             : Active
CreatedAt          : 1/20/2017 2:07:33 AM
UpdatedAt          : 1/20/2017 2:07:56 AM
ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/
Enabled            : True
```

<span data-ttu-id="d7bc7-111">在指定的資源群組中建立新的服務匯流排命名空間。</span><span class="sxs-lookup"><span data-stu-id="d7bc7-111">Creates a new Service Bus namespace within the specified resource group.</span></span>

## <span data-ttu-id="d7bc7-112">參數</span><span class="sxs-lookup"><span data-stu-id="d7bc7-112">PARAMETERS</span></span>

### <span data-ttu-id="d7bc7-113">-位置</span><span class="sxs-lookup"><span data-stu-id="d7bc7-113">-Location</span></span>
<span data-ttu-id="d7bc7-114">服務匯流排命名空間位置。</span><span class="sxs-lookup"><span data-stu-id="d7bc7-114">The Service Bus namespace location.</span></span>

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

### <span data-ttu-id="d7bc7-115">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="d7bc7-115">-NamespaceName</span></span>
<span data-ttu-id="d7bc7-116">服務匯流排命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="d7bc7-116">The Service Bus namespace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7bc7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7bc7-117">-ResourceGroupName</span></span>
<span data-ttu-id="d7bc7-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d7bc7-118">The resource group name.</span></span>

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

### <span data-ttu-id="d7bc7-119">-SkuName</span><span class="sxs-lookup"><span data-stu-id="d7bc7-119">-SkuName</span></span>
<span data-ttu-id="d7bc7-120">服務匯流排命名空間 SKU 名稱。</span><span class="sxs-lookup"><span data-stu-id="d7bc7-120">The Service Bus namespace SKU name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7bc7-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="d7bc7-121">-Tag</span></span>
<span data-ttu-id="d7bc7-122">在伺服器上將雜湊表的格式設定為標記的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="d7bc7-122">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="d7bc7-123">例如：</span><span class="sxs-lookup"><span data-stu-id="d7bc7-123">For example:</span></span>

<span data-ttu-id="d7bc7-124">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="d7bc7-124">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7bc7-125">-確認</span><span class="sxs-lookup"><span data-stu-id="d7bc7-125">-Confirm</span></span>
<span data-ttu-id="d7bc7-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d7bc7-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7bc7-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7bc7-127">-WhatIf</span></span>
<span data-ttu-id="d7bc7-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d7bc7-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d7bc7-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d7bc7-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7bc7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7bc7-130">CommonParameters</span></span>
<span data-ttu-id="d7bc7-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d7bc7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7bc7-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d7bc7-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7bc7-133">輸入</span><span class="sxs-lookup"><span data-stu-id="d7bc7-133">INPUTS</span></span>

### <span data-ttu-id="d7bc7-134">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d7bc7-134">-ResourceGroup</span></span>
 <span data-ttu-id="d7bc7-135">System.object</span><span class="sxs-lookup"><span data-stu-id="d7bc7-135">System.String</span></span>

### <span data-ttu-id="d7bc7-136">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="d7bc7-136">-NamespaceName</span></span>
 <span data-ttu-id="d7bc7-137">System.object</span><span class="sxs-lookup"><span data-stu-id="d7bc7-137">System.String</span></span>

### <span data-ttu-id="d7bc7-138">-位置</span><span class="sxs-lookup"><span data-stu-id="d7bc7-138">-Location</span></span>
 <span data-ttu-id="d7bc7-139">System.object</span><span class="sxs-lookup"><span data-stu-id="d7bc7-139">System.String</span></span>

### <span data-ttu-id="d7bc7-140">-SkuName</span><span class="sxs-lookup"><span data-stu-id="d7bc7-140">-SkuName</span></span>
 <span data-ttu-id="d7bc7-141">System.object</span><span class="sxs-lookup"><span data-stu-id="d7bc7-141">System.String</span></span>

### <span data-ttu-id="d7bc7-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="d7bc7-142">-Tag</span></span>
 <span data-ttu-id="d7bc7-143">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d7bc7-143">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d7bc7-144">輸出</span><span class="sxs-lookup"><span data-stu-id="d7bc7-144">OUTPUTS</span></span>

### <span data-ttu-id="d7bc7-145">NamespaceAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d7bc7-145">Microsoft.Azure.Commands.ServiceBus.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="d7bc7-146">筆記</span><span class="sxs-lookup"><span data-stu-id="d7bc7-146">NOTES</span></span>

## <span data-ttu-id="d7bc7-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="d7bc7-147">RELATED LINKS</span></span>
