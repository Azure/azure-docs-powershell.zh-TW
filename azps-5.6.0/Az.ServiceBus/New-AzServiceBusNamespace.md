---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/new-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusNamespace.md
ms.openlocfilehash: e3e262bee01306eacfdde8b97b13c0ba2a35b745
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903946"
---
# <span data-ttu-id="5c2b3-101">New-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="5c2b3-101">New-AzServiceBusNamespace</span></span>

## <span data-ttu-id="5c2b3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5c2b3-102">SYNOPSIS</span></span>
<span data-ttu-id="5c2b3-103">建立一個新的 Service Bus 命名空間。</span><span class="sxs-lookup"><span data-stu-id="5c2b3-103">Creates a new Service Bus namespace.</span></span>

## <span data-ttu-id="5c2b3-104">語法</span><span class="sxs-lookup"><span data-stu-id="5c2b3-104">SYNTAX</span></span>

```
New-AzServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-SkuName <String>] [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c2b3-105">描述</span><span class="sxs-lookup"><span data-stu-id="5c2b3-105">DESCRIPTION</span></span>
<span data-ttu-id="5c2b3-106">**New-AzServiceBusNamespace** Cmdlet 會建立新的 Service Bus 命名空間。</span><span class="sxs-lookup"><span data-stu-id="5c2b3-106">The **New-AzServiceBusNamespace** cmdlet creates a new Service Bus namespace.</span></span> <span data-ttu-id="5c2b3-107">建立後，命名空間資源清單可通通。</span><span class="sxs-lookup"><span data-stu-id="5c2b3-107">Once created, the namespace resource manifest is immutable.</span></span> <span data-ttu-id="5c2b3-108">此作業為冪次元。</span><span class="sxs-lookup"><span data-stu-id="5c2b3-108">This operation is idempotent.</span></span>

## <span data-ttu-id="5c2b3-109">例子</span><span class="sxs-lookup"><span data-stu-id="5c2b3-109">EXAMPLES</span></span>

### <span data-ttu-id="5c2b3-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="5c2b3-110">Example 1</span></span>
```
PS C:\> New-AzServiceBusNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name SB-Example1 -Location WestUS -SkuName "Standard" -Tag @{Tag1="Tag1Value"}

Name               : SB-Example1
Id                 : /subscriptions/{SubscriptionId}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
ResourceGroupName  : Default-ServiceBus-WestUS
Location           : West US
Tags               : {TesttingTags, TestingTagValue, TestTag, TestTagValue}
Sku                : Name : Premium , Tier : Premium
ProvisioningState  : Succeeded
CreatedAt          : 1/20/2017 2:07:33 AM
UpdatedAt          : 1/20/2017 2:07:56 AM
ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/
```

<span data-ttu-id="5c2b3-111">在指定的資源群組中建立新的 Service Bus 命名空間。</span><span class="sxs-lookup"><span data-stu-id="5c2b3-111">Creates a new Service Bus namespace within the specified resource group.</span></span>

## <span data-ttu-id="5c2b3-112">參數</span><span class="sxs-lookup"><span data-stu-id="5c2b3-112">PARAMETERS</span></span>

### <span data-ttu-id="5c2b3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c2b3-113">-DefaultProfile</span></span>
<span data-ttu-id="5c2b3-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5c2b3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5c2b3-115">-位置</span><span class="sxs-lookup"><span data-stu-id="5c2b3-115">-Location</span></span>
<span data-ttu-id="5c2b3-116">Service Bus 命名空間位置。</span><span class="sxs-lookup"><span data-stu-id="5c2b3-116">The Service Bus namespace location.</span></span>

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

### <span data-ttu-id="5c2b3-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="5c2b3-117">-Name</span></span>
<span data-ttu-id="5c2b3-118">ServiceBus 命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="5c2b3-118">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="5c2b3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c2b3-119">-ResourceGroupName</span></span>
<span data-ttu-id="5c2b3-120">資源組名。</span><span class="sxs-lookup"><span data-stu-id="5c2b3-120">The resource group name.</span></span>

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

### <span data-ttu-id="5c2b3-121">-Sku以</span><span class="sxs-lookup"><span data-stu-id="5c2b3-121">-SkuCapacity</span></span>
<span data-ttu-id="5c2b3-122">Service Bus 進位命名空間輸送量單位，允許的值 1 或 2 或 4</span><span class="sxs-lookup"><span data-stu-id="5c2b3-122">The Service Bus premium namespace throughput units, allowed values 1 or 2 or 4</span></span>

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

### <span data-ttu-id="5c2b3-123">-SKUName</span><span class="sxs-lookup"><span data-stu-id="5c2b3-123">-SkuName</span></span>
<span data-ttu-id="5c2b3-124">Service Bus 命名空間 SKU 名稱。</span><span class="sxs-lookup"><span data-stu-id="5c2b3-124">The Service Bus namespace SKU name.</span></span>

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

### <span data-ttu-id="5c2b3-125">-標記</span><span class="sxs-lookup"><span data-stu-id="5c2b3-125">-Tag</span></span>
<span data-ttu-id="5c2b3-126">以雜湊表格形式設定為伺服器上標記的索引鍵值組。</span><span class="sxs-lookup"><span data-stu-id="5c2b3-126">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="5c2b3-127">例如：@{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="5c2b3-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="5c2b3-128">-確認</span><span class="sxs-lookup"><span data-stu-id="5c2b3-128">-Confirm</span></span>
<span data-ttu-id="5c2b3-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="5c2b3-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c2b3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c2b3-130">-WhatIf</span></span>
<span data-ttu-id="5c2b3-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5c2b3-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5c2b3-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5c2b3-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c2b3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c2b3-133">CommonParameters</span></span>
<span data-ttu-id="5c2b3-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5c2b3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c2b3-135">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="5c2b3-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c2b3-136">輸入</span><span class="sxs-lookup"><span data-stu-id="5c2b3-136">INPUTS</span></span>

### <span data-ttu-id="5c2b3-137">System.String</span><span class="sxs-lookup"><span data-stu-id="5c2b3-137">System.String</span></span>

### <span data-ttu-id="5c2b3-138">System.Nullable'1[[System.Int32， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5c2b3-138">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="5c2b3-139">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="5c2b3-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="5c2b3-140">輸出</span><span class="sxs-lookup"><span data-stu-id="5c2b3-140">OUTPUTS</span></span>

### <span data-ttu-id="5c2b3-141">Microsoft.Azure.Commands.ServiceBus.models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="5c2b3-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="5c2b3-142">筆記</span><span class="sxs-lookup"><span data-stu-id="5c2b3-142">NOTES</span></span>

## <span data-ttu-id="5c2b3-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="5c2b3-143">RELATED LINKS</span></span>
