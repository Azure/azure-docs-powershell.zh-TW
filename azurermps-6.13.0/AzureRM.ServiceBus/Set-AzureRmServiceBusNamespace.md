---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 6ac46fc8b8f94480e11f00d44efc690d97ee56a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625243"
---
# <span data-ttu-id="f4cf5-101">Set-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="f4cf5-101">Set-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="f4cf5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f4cf5-102">SYNOPSIS</span></span>
<span data-ttu-id="f4cf5-103">更新現有服務匯流排命名空間的描述。</span><span class="sxs-lookup"><span data-stu-id="f4cf5-103">Updates the description of an existing Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4cf5-104">句法</span><span class="sxs-lookup"><span data-stu-id="f4cf5-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-SkuName <String>] [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4cf5-105">說明</span><span class="sxs-lookup"><span data-stu-id="f4cf5-105">DESCRIPTION</span></span>
<span data-ttu-id="f4cf5-106">**AzureRmServiceBusNamespace** Cmdlet 會更新資源群組內指定服務匯流排命名空間的描述。</span><span class="sxs-lookup"><span data-stu-id="f4cf5-106">The **Set-AzureRmServiceBusNamespace** cmdlet updates the description of the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="f4cf5-107">示例</span><span class="sxs-lookup"><span data-stu-id="f4cf5-107">EXAMPLES</span></span>

### <span data-ttu-id="f4cf5-108">範例1</span><span class="sxs-lookup"><span data-stu-id="f4cf5-108">Example 1</span></span>
```
PS C:\> Set-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -Location WestUs -SkuName Premium -SkuCapacity 1 -Tag @{Tag2="Tag2Value"}

Name               : SB-Example1
Id                 : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
ResourceGroup      : Default-ServiceBus-WestUS
Location           : West US
Tags               : {Tag2, Tag2Value}
Sku                : Name : Premium , Tier : Premium, Capacity : 1
ProvisioningState  : Succeeded
CreatedAt          :
UpdatedAt          :
ServiceBusEndpoint :
```

<span data-ttu-id="f4cf5-109">使用新的描述更新服務匯流排命名空間。</span><span class="sxs-lookup"><span data-stu-id="f4cf5-109">Updates the Service Bus namespace with a new description.</span></span>

## <span data-ttu-id="f4cf5-110">參數</span><span class="sxs-lookup"><span data-stu-id="f4cf5-110">PARAMETERS</span></span>

### <span data-ttu-id="f4cf5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4cf5-111">-DefaultProfile</span></span>
<span data-ttu-id="f4cf5-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f4cf5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4cf5-113">-位置</span><span class="sxs-lookup"><span data-stu-id="f4cf5-113">-Location</span></span>
<span data-ttu-id="f4cf5-114">服務匯流排命名空間位置。</span><span class="sxs-lookup"><span data-stu-id="f4cf5-114">The Service Bus namespace location.</span></span>

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

### <span data-ttu-id="f4cf5-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="f4cf5-115">-Name</span></span>
<span data-ttu-id="f4cf5-116">已將命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="f4cf5-116">ServiceBus Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4cf5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4cf5-117">-ResourceGroupName</span></span>
<span data-ttu-id="f4cf5-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f4cf5-118">The resource group name.</span></span>

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

### <span data-ttu-id="f4cf5-119">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="f4cf5-119">-SkuCapacity</span></span>
<span data-ttu-id="f4cf5-120">命名空間 Sku 的容量。</span><span class="sxs-lookup"><span data-stu-id="f4cf5-120">Namespace Sku Capacity.</span></span>

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

### <span data-ttu-id="f4cf5-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="f4cf5-121">-SkuName</span></span>
<span data-ttu-id="f4cf5-122">命名空間 SKU 名稱。</span><span class="sxs-lookup"><span data-stu-id="f4cf5-122">The namespace SKU name.</span></span>

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

### <span data-ttu-id="f4cf5-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="f4cf5-123">-Tag</span></span>
<span data-ttu-id="f4cf5-124">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="f4cf5-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f4cf5-125">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="f4cf5-125">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="f4cf5-126">-確認</span><span class="sxs-lookup"><span data-stu-id="f4cf5-126">-Confirm</span></span>
<span data-ttu-id="f4cf5-127">使用指定的資訊更新服務匯流排命名空間。</span><span class="sxs-lookup"><span data-stu-id="f4cf5-127">Updates the Service Bus namespace with the specified information.</span></span>

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

### <span data-ttu-id="f4cf5-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4cf5-128">-WhatIf</span></span>
<span data-ttu-id="f4cf5-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f4cf5-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4cf5-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f4cf5-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4cf5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4cf5-131">CommonParameters</span></span>
<span data-ttu-id="f4cf5-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f4cf5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4cf5-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f4cf5-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4cf5-134">輸入</span><span class="sxs-lookup"><span data-stu-id="f4cf5-134">INPUTS</span></span>

### <span data-ttu-id="f4cf5-135">System.object</span><span class="sxs-lookup"><span data-stu-id="f4cf5-135">System.String</span></span>

### <span data-ttu-id="f4cf5-136">System.object "1 [[System. Int32，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="f4cf5-136">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="f4cf5-137">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f4cf5-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f4cf5-138">輸出</span><span class="sxs-lookup"><span data-stu-id="f4cf5-138">OUTPUTS</span></span>

### <span data-ttu-id="f4cf5-139">PSNamespaceAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f4cf5-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="f4cf5-140">筆記</span><span class="sxs-lookup"><span data-stu-id="f4cf5-140">NOTES</span></span>

## <span data-ttu-id="f4cf5-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="f4cf5-141">RELATED LINKS</span></span>
