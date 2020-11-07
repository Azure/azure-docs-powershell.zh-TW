---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusNamespace.md
ms.openlocfilehash: 7016f514d42f50c489282ea993a18a85b349f8af
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93791022"
---
# <span data-ttu-id="97d1b-101">New-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="97d1b-101">New-AzServiceBusNamespace</span></span>

## <span data-ttu-id="97d1b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="97d1b-102">SYNOPSIS</span></span>
<span data-ttu-id="97d1b-103">建立新的服務匯流排命名空間。</span><span class="sxs-lookup"><span data-stu-id="97d1b-103">Creates a new Service Bus namespace.</span></span>

## <span data-ttu-id="97d1b-104">句法</span><span class="sxs-lookup"><span data-stu-id="97d1b-104">SYNTAX</span></span>

```
New-AzServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-SkuName <String>] [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97d1b-105">說明</span><span class="sxs-lookup"><span data-stu-id="97d1b-105">DESCRIPTION</span></span>
<span data-ttu-id="97d1b-106">**新的-AzServiceBusNamespace** Cmdlet 會建立新的服務匯流排命名空間。</span><span class="sxs-lookup"><span data-stu-id="97d1b-106">The **New-AzServiceBusNamespace** cmdlet creates a new Service Bus namespace.</span></span> <span data-ttu-id="97d1b-107">一旦建立之後，命名空間資源資訊清單就是不可變的。</span><span class="sxs-lookup"><span data-stu-id="97d1b-107">Once created, the namespace resource manifest is immutable.</span></span> <span data-ttu-id="97d1b-108">這個運算為冪等。</span><span class="sxs-lookup"><span data-stu-id="97d1b-108">This operation is idempotent.</span></span>

## <span data-ttu-id="97d1b-109">示例</span><span class="sxs-lookup"><span data-stu-id="97d1b-109">EXAMPLES</span></span>

### <span data-ttu-id="97d1b-110">範例1</span><span class="sxs-lookup"><span data-stu-id="97d1b-110">Example 1</span></span>
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

<span data-ttu-id="97d1b-111">在指定的資源群組中建立新的服務匯流排命名空間。</span><span class="sxs-lookup"><span data-stu-id="97d1b-111">Creates a new Service Bus namespace within the specified resource group.</span></span>

## <span data-ttu-id="97d1b-112">參數</span><span class="sxs-lookup"><span data-stu-id="97d1b-112">PARAMETERS</span></span>

### <span data-ttu-id="97d1b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97d1b-113">-DefaultProfile</span></span>
<span data-ttu-id="97d1b-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="97d1b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97d1b-115">-位置</span><span class="sxs-lookup"><span data-stu-id="97d1b-115">-Location</span></span>
<span data-ttu-id="97d1b-116">服務匯流排命名空間位置。</span><span class="sxs-lookup"><span data-stu-id="97d1b-116">The Service Bus namespace location.</span></span>

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

### <span data-ttu-id="97d1b-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="97d1b-117">-Name</span></span>
<span data-ttu-id="97d1b-118">已將命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="97d1b-118">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="97d1b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97d1b-119">-ResourceGroupName</span></span>
<span data-ttu-id="97d1b-120">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="97d1b-120">The resource group name.</span></span>

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

### <span data-ttu-id="97d1b-121">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="97d1b-121">-SkuCapacity</span></span>
<span data-ttu-id="97d1b-122">服務匯流排 premium 命名空間輸送量單位，允許值1或2或4</span><span class="sxs-lookup"><span data-stu-id="97d1b-122">The Service Bus premium namespace throughput units, allowed values 1 or 2 or 4</span></span>

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

### <span data-ttu-id="97d1b-123">-SkuName</span><span class="sxs-lookup"><span data-stu-id="97d1b-123">-SkuName</span></span>
<span data-ttu-id="97d1b-124">服務匯流排命名空間 SKU 名稱。</span><span class="sxs-lookup"><span data-stu-id="97d1b-124">The Service Bus namespace SKU name.</span></span>

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

### <span data-ttu-id="97d1b-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="97d1b-125">-Tag</span></span>
<span data-ttu-id="97d1b-126">在伺服器上將雜湊表的格式設定為標記的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="97d1b-126">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="97d1b-127">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="97d1b-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="97d1b-128">-確認</span><span class="sxs-lookup"><span data-stu-id="97d1b-128">-Confirm</span></span>
<span data-ttu-id="97d1b-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="97d1b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97d1b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97d1b-130">-WhatIf</span></span>
<span data-ttu-id="97d1b-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="97d1b-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="97d1b-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="97d1b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97d1b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97d1b-133">CommonParameters</span></span>
<span data-ttu-id="97d1b-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="97d1b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97d1b-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="97d1b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97d1b-136">輸入</span><span class="sxs-lookup"><span data-stu-id="97d1b-136">INPUTS</span></span>

### <span data-ttu-id="97d1b-137">System.object</span><span class="sxs-lookup"><span data-stu-id="97d1b-137">System.String</span></span>

### <span data-ttu-id="97d1b-138">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="97d1b-138">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="97d1b-139">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="97d1b-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="97d1b-140">輸出</span><span class="sxs-lookup"><span data-stu-id="97d1b-140">OUTPUTS</span></span>

### <span data-ttu-id="97d1b-141">PSNamespaceAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="97d1b-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="97d1b-142">筆記</span><span class="sxs-lookup"><span data-stu-id="97d1b-142">NOTES</span></span>

## <span data-ttu-id="97d1b-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="97d1b-143">RELATED LINKS</span></span>
