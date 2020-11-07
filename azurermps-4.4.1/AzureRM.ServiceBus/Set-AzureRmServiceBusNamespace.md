---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 134e0d20566a8310a381a38297984202b7509250
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625964"
---
# <span data-ttu-id="a72aa-101">Set-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="a72aa-101">Set-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="a72aa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a72aa-102">SYNOPSIS</span></span>
<span data-ttu-id="a72aa-103">更新現有服務匯流排命名空間的描述。</span><span class="sxs-lookup"><span data-stu-id="a72aa-103">Updates the description of an existing Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a72aa-104">句法</span><span class="sxs-lookup"><span data-stu-id="a72aa-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> -Name <String>
 [-SkuName <String>] [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a72aa-105">說明</span><span class="sxs-lookup"><span data-stu-id="a72aa-105">DESCRIPTION</span></span>
<span data-ttu-id="a72aa-106">**AzureRmServiceBusNamespace** Cmdlet 會更新資源群組內指定服務匯流排命名空間的描述。</span><span class="sxs-lookup"><span data-stu-id="a72aa-106">The **Set-AzureRmServiceBusNamespace** cmdlet updates the description of the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="a72aa-107">示例</span><span class="sxs-lookup"><span data-stu-id="a72aa-107">EXAMPLES</span></span>

### <span data-ttu-id="a72aa-108">範例1</span><span class="sxs-lookup"><span data-stu-id="a72aa-108">Example 1</span></span>
```
PS C:\> Set-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -Location WestUs -SkuName Premium -SkuCapacity 10 -Tag @{Tag2="Tag2Value"}

Name               : SB-Example1
Id                 : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
Location           : West US
Sku                : Name : Standard , Capacity : 10 , Tier : Standard
ProvisioningState  : Succeeded
Status             :
CreatedAt          :
UpdatedAt          :
ServiceBusEndpoint :
Enabled            : False
```

<span data-ttu-id="a72aa-109">使用新的描述更新服務匯流排命名空間。</span><span class="sxs-lookup"><span data-stu-id="a72aa-109">Updates the Service Bus namespace with a new description.</span></span>

## <span data-ttu-id="a72aa-110">參數</span><span class="sxs-lookup"><span data-stu-id="a72aa-110">PARAMETERS</span></span>

### <span data-ttu-id="a72aa-111">-位置</span><span class="sxs-lookup"><span data-stu-id="a72aa-111">-Location</span></span>
<span data-ttu-id="a72aa-112">服務匯流排命名空間位置。</span><span class="sxs-lookup"><span data-stu-id="a72aa-112">The Service Bus namespace location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a72aa-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a72aa-113">-ResourceGroupName</span></span>
<span data-ttu-id="a72aa-114">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a72aa-114">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a72aa-115">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="a72aa-115">-SkuCapacity</span></span>
<span data-ttu-id="a72aa-116">命名空間 Sku 的容量。</span><span class="sxs-lookup"><span data-stu-id="a72aa-116">Namespace Sku Capacity.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a72aa-117">-SkuName</span><span class="sxs-lookup"><span data-stu-id="a72aa-117">-SkuName</span></span>
<span data-ttu-id="a72aa-118">命名空間 SKU 名稱。</span><span class="sxs-lookup"><span data-stu-id="a72aa-118">The namespace SKU name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a72aa-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="a72aa-119">-Tag</span></span>
<span data-ttu-id="a72aa-120">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="a72aa-120">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a72aa-121">例如：</span><span class="sxs-lookup"><span data-stu-id="a72aa-121">For example:</span></span>

<span data-ttu-id="a72aa-122">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="a72aa-122">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a72aa-123">-確認</span><span class="sxs-lookup"><span data-stu-id="a72aa-123">-Confirm</span></span>
<span data-ttu-id="a72aa-124">使用指定的資訊更新服務匯流排命名空間。</span><span class="sxs-lookup"><span data-stu-id="a72aa-124">Updates the Service Bus namespace with the specified information.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a72aa-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a72aa-125">-WhatIf</span></span>
<span data-ttu-id="a72aa-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a72aa-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a72aa-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a72aa-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a72aa-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a72aa-128">-DefaultProfile</span></span>
<span data-ttu-id="a72aa-129">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a72aa-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a72aa-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="a72aa-130">-Name</span></span>
<span data-ttu-id="a72aa-131">已將命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="a72aa-131">ServiceBus Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a72aa-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a72aa-132">CommonParameters</span></span>
<span data-ttu-id="a72aa-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a72aa-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a72aa-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a72aa-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a72aa-135">輸入</span><span class="sxs-lookup"><span data-stu-id="a72aa-135">INPUTS</span></span>

### <span data-ttu-id="a72aa-136">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a72aa-136">-ResourceGroup</span></span>
 <span data-ttu-id="a72aa-137">System.object</span><span class="sxs-lookup"><span data-stu-id="a72aa-137">System.String</span></span>

### <span data-ttu-id="a72aa-138">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="a72aa-138">-NamespaceName</span></span>
 <span data-ttu-id="a72aa-139">System.object</span><span class="sxs-lookup"><span data-stu-id="a72aa-139">System.String</span></span>

### <span data-ttu-id="a72aa-140">-位置</span><span class="sxs-lookup"><span data-stu-id="a72aa-140">-Location</span></span>
 <span data-ttu-id="a72aa-141">System.object</span><span class="sxs-lookup"><span data-stu-id="a72aa-141">System.String</span></span>

### <span data-ttu-id="a72aa-142">-SkuName</span><span class="sxs-lookup"><span data-stu-id="a72aa-142">-SkuName</span></span>
 <span data-ttu-id="a72aa-143">System.object</span><span class="sxs-lookup"><span data-stu-id="a72aa-143">System.String</span></span>

### <span data-ttu-id="a72aa-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="a72aa-144">-Tag</span></span>
 <span data-ttu-id="a72aa-145">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a72aa-145">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a72aa-146">輸出</span><span class="sxs-lookup"><span data-stu-id="a72aa-146">OUTPUTS</span></span>

### <span data-ttu-id="a72aa-147">NamespaceAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a72aa-147">Microsoft.Azure.Commands.ServiceBus.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="a72aa-148">筆記</span><span class="sxs-lookup"><span data-stu-id="a72aa-148">NOTES</span></span>
## <span data-ttu-id="a72aa-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="a72aa-149">RELATED LINKS</span></span>

## <span data-ttu-id="a72aa-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="a72aa-150">RELATED LINKS</span></span>

