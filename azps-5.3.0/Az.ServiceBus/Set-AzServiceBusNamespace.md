---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNamespace.md
ms.openlocfilehash: e9f228b284b690681b2a4d55eb436e4062d7c861
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98448343"
---
# <span data-ttu-id="3bd1c-101">Set-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="3bd1c-101">Set-AzServiceBusNamespace</span></span>

## <span data-ttu-id="3bd1c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3bd1c-102">SYNOPSIS</span></span>
<span data-ttu-id="3bd1c-103">更新現有服務匯流排命名空間的描述。</span><span class="sxs-lookup"><span data-stu-id="3bd1c-103">Updates the description of an existing Service Bus namespace.</span></span>

## <span data-ttu-id="3bd1c-104">句法</span><span class="sxs-lookup"><span data-stu-id="3bd1c-104">SYNTAX</span></span>

```
Set-AzServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-SkuName <String>] [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3bd1c-105">說明</span><span class="sxs-lookup"><span data-stu-id="3bd1c-105">DESCRIPTION</span></span>
<span data-ttu-id="3bd1c-106">**AzServiceBusNamespace** Cmdlet 會更新資源群組內指定服務匯流排命名空間的描述。</span><span class="sxs-lookup"><span data-stu-id="3bd1c-106">The **Set-AzServiceBusNamespace** cmdlet updates the description of the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="3bd1c-107">示例</span><span class="sxs-lookup"><span data-stu-id="3bd1c-107">EXAMPLES</span></span>

### <span data-ttu-id="3bd1c-108">範例1</span><span class="sxs-lookup"><span data-stu-id="3bd1c-108">Example 1</span></span>
```
PS C:\> Set-AzServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -Location WestUs -SkuName Premium -SkuCapacity 1 -Tag @{Tag2="Tag2Value"}

Name               : SB-Example1
Id                 : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
ResourceGroupName  : Default-ServiceBus-WestUS
Location           : West US
Tags               : {Tag2, Tag2Value}
Sku                : Name : Premium , Tier : Premium, Capacity : 1
ProvisioningState  : Succeeded
CreatedAt          :
UpdatedAt          :
ServiceBusEndpoint :
```

<span data-ttu-id="3bd1c-109">使用新的描述更新服務匯流排命名空間。</span><span class="sxs-lookup"><span data-stu-id="3bd1c-109">Updates the Service Bus namespace with a new description.</span></span>

## <span data-ttu-id="3bd1c-110">參數</span><span class="sxs-lookup"><span data-stu-id="3bd1c-110">PARAMETERS</span></span>

### <span data-ttu-id="3bd1c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bd1c-111">-DefaultProfile</span></span>
<span data-ttu-id="3bd1c-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3bd1c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bd1c-113">-位置</span><span class="sxs-lookup"><span data-stu-id="3bd1c-113">-Location</span></span>
<span data-ttu-id="3bd1c-114">服務匯流排命名空間位置。</span><span class="sxs-lookup"><span data-stu-id="3bd1c-114">The Service Bus namespace location.</span></span>

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

### <span data-ttu-id="3bd1c-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="3bd1c-115">-Name</span></span>
<span data-ttu-id="3bd1c-116">已將命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="3bd1c-116">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="3bd1c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bd1c-117">-ResourceGroupName</span></span>
<span data-ttu-id="3bd1c-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3bd1c-118">The resource group name.</span></span>

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

### <span data-ttu-id="3bd1c-119">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="3bd1c-119">-SkuCapacity</span></span>
<span data-ttu-id="3bd1c-120">命名空間 Sku 的容量。</span><span class="sxs-lookup"><span data-stu-id="3bd1c-120">Namespace Sku Capacity.</span></span>

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

### <span data-ttu-id="3bd1c-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="3bd1c-121">-SkuName</span></span>
<span data-ttu-id="3bd1c-122">命名空間 SKU 名稱。</span><span class="sxs-lookup"><span data-stu-id="3bd1c-122">The namespace SKU name.</span></span>

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

### <span data-ttu-id="3bd1c-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="3bd1c-123">-Tag</span></span>
<span data-ttu-id="3bd1c-124">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="3bd1c-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3bd1c-125">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="3bd1c-125">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="3bd1c-126">-確認</span><span class="sxs-lookup"><span data-stu-id="3bd1c-126">-Confirm</span></span>
<span data-ttu-id="3bd1c-127">使用指定的資訊更新服務匯流排命名空間。</span><span class="sxs-lookup"><span data-stu-id="3bd1c-127">Updates the Service Bus namespace with the specified information.</span></span>

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

### <span data-ttu-id="3bd1c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bd1c-128">-WhatIf</span></span>
<span data-ttu-id="3bd1c-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3bd1c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3bd1c-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3bd1c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3bd1c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bd1c-131">CommonParameters</span></span>
<span data-ttu-id="3bd1c-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3bd1c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bd1c-133">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3bd1c-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bd1c-134">輸入</span><span class="sxs-lookup"><span data-stu-id="3bd1c-134">INPUTS</span></span>

### <span data-ttu-id="3bd1c-135">System.object</span><span class="sxs-lookup"><span data-stu-id="3bd1c-135">System.String</span></span>

### <span data-ttu-id="3bd1c-136">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="3bd1c-136">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="3bd1c-137">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="3bd1c-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3bd1c-138">輸出</span><span class="sxs-lookup"><span data-stu-id="3bd1c-138">OUTPUTS</span></span>

### <span data-ttu-id="3bd1c-139">PSNamespaceAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="3bd1c-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="3bd1c-140">筆記</span><span class="sxs-lookup"><span data-stu-id="3bd1c-140">NOTES</span></span>

## <span data-ttu-id="3bd1c-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="3bd1c-141">RELATED LINKS</span></span>
