---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/set-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNamespace.md
ms.openlocfilehash: f1edc3f65747203a587de82c9f03ce79b258cd36
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909337"
---
# <span data-ttu-id="04d3c-101">Set-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="04d3c-101">Set-AzServiceBusNamespace</span></span>

## <span data-ttu-id="04d3c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="04d3c-102">SYNOPSIS</span></span>
<span data-ttu-id="04d3c-103">更新現有 Service Bus 命名空間的描述。</span><span class="sxs-lookup"><span data-stu-id="04d3c-103">Updates the description of an existing Service Bus namespace.</span></span>

## <span data-ttu-id="04d3c-104">語法</span><span class="sxs-lookup"><span data-stu-id="04d3c-104">SYNTAX</span></span>

```
Set-AzServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-SkuName <String>] [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04d3c-105">描述</span><span class="sxs-lookup"><span data-stu-id="04d3c-105">DESCRIPTION</span></span>
<span data-ttu-id="04d3c-106">**Set-AzServiceBusNamespace** Cmdlet 會更新資源群組中指定 Service Bus 命名空間的描述。</span><span class="sxs-lookup"><span data-stu-id="04d3c-106">The **Set-AzServiceBusNamespace** cmdlet updates the description of the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="04d3c-107">例子</span><span class="sxs-lookup"><span data-stu-id="04d3c-107">EXAMPLES</span></span>

### <span data-ttu-id="04d3c-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="04d3c-108">Example 1</span></span>
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

<span data-ttu-id="04d3c-109">以新的描述更新 Service Bus 命名空間。</span><span class="sxs-lookup"><span data-stu-id="04d3c-109">Updates the Service Bus namespace with a new description.</span></span>

## <span data-ttu-id="04d3c-110">參數</span><span class="sxs-lookup"><span data-stu-id="04d3c-110">PARAMETERS</span></span>

### <span data-ttu-id="04d3c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04d3c-111">-DefaultProfile</span></span>
<span data-ttu-id="04d3c-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="04d3c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04d3c-113">-位置</span><span class="sxs-lookup"><span data-stu-id="04d3c-113">-Location</span></span>
<span data-ttu-id="04d3c-114">Service Bus 命名空間位置。</span><span class="sxs-lookup"><span data-stu-id="04d3c-114">The Service Bus namespace location.</span></span>

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

### <span data-ttu-id="04d3c-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="04d3c-115">-Name</span></span>
<span data-ttu-id="04d3c-116">ServiceBus 命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="04d3c-116">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="04d3c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04d3c-117">-ResourceGroupName</span></span>
<span data-ttu-id="04d3c-118">資源組名。</span><span class="sxs-lookup"><span data-stu-id="04d3c-118">The resource group name.</span></span>

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

### <span data-ttu-id="04d3c-119">-Sku以</span><span class="sxs-lookup"><span data-stu-id="04d3c-119">-SkuCapacity</span></span>
<span data-ttu-id="04d3c-120">命名空間 SKU 容量。</span><span class="sxs-lookup"><span data-stu-id="04d3c-120">Namespace Sku Capacity.</span></span>

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

### <span data-ttu-id="04d3c-121">-SKUName</span><span class="sxs-lookup"><span data-stu-id="04d3c-121">-SkuName</span></span>
<span data-ttu-id="04d3c-122">命名空間 SKU 名稱。</span><span class="sxs-lookup"><span data-stu-id="04d3c-122">The namespace SKU name.</span></span>

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

### <span data-ttu-id="04d3c-123">-標記</span><span class="sxs-lookup"><span data-stu-id="04d3c-123">-Tag</span></span>
<span data-ttu-id="04d3c-124">以雜湊表格形式建立索引鍵值組。</span><span class="sxs-lookup"><span data-stu-id="04d3c-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="04d3c-125">例如：@{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="04d3c-125">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="04d3c-126">-確認</span><span class="sxs-lookup"><span data-stu-id="04d3c-126">-Confirm</span></span>
<span data-ttu-id="04d3c-127">使用指定的資訊更新 Service Bus 命名空間。</span><span class="sxs-lookup"><span data-stu-id="04d3c-127">Updates the Service Bus namespace with the specified information.</span></span>

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

### <span data-ttu-id="04d3c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04d3c-128">-WhatIf</span></span>
<span data-ttu-id="04d3c-129">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="04d3c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04d3c-130">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="04d3c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04d3c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04d3c-131">CommonParameters</span></span>
<span data-ttu-id="04d3c-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="04d3c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04d3c-133">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="04d3c-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04d3c-134">輸入</span><span class="sxs-lookup"><span data-stu-id="04d3c-134">INPUTS</span></span>

### <span data-ttu-id="04d3c-135">System.String</span><span class="sxs-lookup"><span data-stu-id="04d3c-135">System.String</span></span>

### <span data-ttu-id="04d3c-136">System.Nullable'1[[System.Int32， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="04d3c-136">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="04d3c-137">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="04d3c-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="04d3c-138">輸出</span><span class="sxs-lookup"><span data-stu-id="04d3c-138">OUTPUTS</span></span>

### <span data-ttu-id="04d3c-139">Microsoft.Azure.Commands.ServiceBus.models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="04d3c-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="04d3c-140">筆記</span><span class="sxs-lookup"><span data-stu-id="04d3c-140">NOTES</span></span>

## <span data-ttu-id="04d3c-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="04d3c-141">RELATED LINKS</span></span>
