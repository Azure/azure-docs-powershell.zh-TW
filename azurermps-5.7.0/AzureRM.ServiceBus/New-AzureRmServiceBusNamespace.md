---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 1834adfdb275bc5454e16e72732b649c82704a34
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450493"
---
# <span data-ttu-id="6ef81-101">New-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="6ef81-101">New-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="6ef81-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6ef81-102">SYNOPSIS</span></span>
<span data-ttu-id="6ef81-103">建立新的服務匯流排命名空間。</span><span class="sxs-lookup"><span data-stu-id="6ef81-103">Creates a new Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ef81-104">句法</span><span class="sxs-lookup"><span data-stu-id="6ef81-104">SYNTAX</span></span>

```
New-AzureRmServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-SkuName <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6ef81-105">說明</span><span class="sxs-lookup"><span data-stu-id="6ef81-105">DESCRIPTION</span></span>
<span data-ttu-id="6ef81-106">**新的-AzureRmServiceBusNamespace** Cmdlet 會建立新的服務匯流排命名空間。</span><span class="sxs-lookup"><span data-stu-id="6ef81-106">The **New-AzureRmServiceBusNamespace** cmdlet creates a new Service Bus namespace.</span></span> <span data-ttu-id="6ef81-107">一旦建立之後，命名空間資源資訊清單就是不可變的。</span><span class="sxs-lookup"><span data-stu-id="6ef81-107">Once created, the namespace resource manifest is immutable.</span></span> <span data-ttu-id="6ef81-108">這個運算為冪等。</span><span class="sxs-lookup"><span data-stu-id="6ef81-108">This operation is idempotent.</span></span>

## <span data-ttu-id="6ef81-109">示例</span><span class="sxs-lookup"><span data-stu-id="6ef81-109">EXAMPLES</span></span>

### <span data-ttu-id="6ef81-110">範例1</span><span class="sxs-lookup"><span data-stu-id="6ef81-110">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -Location WestUS -SkuName "Standard" -Tag @{Tag1="Tag1Value"}

Name               : SB-Example1
Id                 : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
Location           : West US
Sku                : Name : Standard , Capacity : 1 , Tier : Standard
ProvisioningState  : Succeeded
CreatedAt          : 1/20/2017 2:07:33 AM
UpdatedAt          : 1/20/2017 2:07:56 AM
ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/
```

<span data-ttu-id="6ef81-111">在指定的資源群組中建立新的服務匯流排命名空間。</span><span class="sxs-lookup"><span data-stu-id="6ef81-111">Creates a new Service Bus namespace within the specified resource group.</span></span>

## <span data-ttu-id="6ef81-112">參數</span><span class="sxs-lookup"><span data-stu-id="6ef81-112">PARAMETERS</span></span>

### <span data-ttu-id="6ef81-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ef81-113">-DefaultProfile</span></span>
<span data-ttu-id="6ef81-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6ef81-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ef81-115">-位置</span><span class="sxs-lookup"><span data-stu-id="6ef81-115">-Location</span></span>
<span data-ttu-id="6ef81-116">服務匯流排命名空間位置。</span><span class="sxs-lookup"><span data-stu-id="6ef81-116">The Service Bus namespace location.</span></span>

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

### <span data-ttu-id="6ef81-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="6ef81-117">-Name</span></span>
<span data-ttu-id="6ef81-118">已將命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="6ef81-118">ServiceBus Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ef81-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ef81-119">-ResourceGroupName</span></span>
<span data-ttu-id="6ef81-120">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6ef81-120">The resource group name.</span></span>

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

### <span data-ttu-id="6ef81-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="6ef81-121">-SkuName</span></span>
<span data-ttu-id="6ef81-122">服務匯流排命名空間 SKU 名稱。</span><span class="sxs-lookup"><span data-stu-id="6ef81-122">The Service Bus namespace SKU name.</span></span>

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

### <span data-ttu-id="6ef81-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="6ef81-123">-Tag</span></span>
<span data-ttu-id="6ef81-124">在伺服器上將雜湊表的格式設定為標記的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="6ef81-124">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="6ef81-125">例如：</span><span class="sxs-lookup"><span data-stu-id="6ef81-125">For example:</span></span>

<span data-ttu-id="6ef81-126">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="6ef81-126">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="6ef81-127">-確認</span><span class="sxs-lookup"><span data-stu-id="6ef81-127">-Confirm</span></span>
<span data-ttu-id="6ef81-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6ef81-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ef81-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ef81-129">-WhatIf</span></span>
<span data-ttu-id="6ef81-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6ef81-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6ef81-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6ef81-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ef81-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ef81-132">CommonParameters</span></span>
<span data-ttu-id="6ef81-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6ef81-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ef81-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6ef81-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ef81-135">輸入</span><span class="sxs-lookup"><span data-stu-id="6ef81-135">INPUTS</span></span>

### <span data-ttu-id="6ef81-136">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6ef81-136">-ResourceGroup</span></span>
 <span data-ttu-id="6ef81-137">System.object</span><span class="sxs-lookup"><span data-stu-id="6ef81-137">System.String</span></span>

### <span data-ttu-id="6ef81-138">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="6ef81-138">-NamespaceName</span></span>
 <span data-ttu-id="6ef81-139">System.object</span><span class="sxs-lookup"><span data-stu-id="6ef81-139">System.String</span></span>

### <span data-ttu-id="6ef81-140">-位置</span><span class="sxs-lookup"><span data-stu-id="6ef81-140">-Location</span></span>
 <span data-ttu-id="6ef81-141">System.object</span><span class="sxs-lookup"><span data-stu-id="6ef81-141">System.String</span></span>

### <span data-ttu-id="6ef81-142">-SkuName</span><span class="sxs-lookup"><span data-stu-id="6ef81-142">-SkuName</span></span>
 <span data-ttu-id="6ef81-143">System.object</span><span class="sxs-lookup"><span data-stu-id="6ef81-143">System.String</span></span>

### <span data-ttu-id="6ef81-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="6ef81-144">-Tag</span></span>
 <span data-ttu-id="6ef81-145">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6ef81-145">System.Collections.Hashtable</span></span>

## <span data-ttu-id="6ef81-146">輸出</span><span class="sxs-lookup"><span data-stu-id="6ef81-146">OUTPUTS</span></span>

### <span data-ttu-id="6ef81-147">PSNamespaceAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6ef81-147">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="6ef81-148">筆記</span><span class="sxs-lookup"><span data-stu-id="6ef81-148">NOTES</span></span>

## <span data-ttu-id="6ef81-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="6ef81-149">RELATED LINKS</span></span>

