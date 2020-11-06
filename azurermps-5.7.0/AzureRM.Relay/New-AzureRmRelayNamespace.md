---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/new-azurermrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayNamespace.md
ms.openlocfilehash: 1eed6f722487e3c37d9d12785b07e90516406f8f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450527"
---
# <span data-ttu-id="2132b-101">New-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="2132b-101">New-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="2132b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2132b-102">SYNOPSIS</span></span>
<span data-ttu-id="2132b-103">建立新的中繼命名空間。</span><span class="sxs-lookup"><span data-stu-id="2132b-103">Creates a new Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2132b-104">句法</span><span class="sxs-lookup"><span data-stu-id="2132b-104">SYNTAX</span></span>

```
New-AzureRmRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2132b-105">說明</span><span class="sxs-lookup"><span data-stu-id="2132b-105">DESCRIPTION</span></span>
<span data-ttu-id="2132b-106">**新的-AzureRmRelayNamespace** Cmdlet 會建立新的中繼命名空間。</span><span class="sxs-lookup"><span data-stu-id="2132b-106">The **New-AzureRmRelayNamespace** cmdlet creates a new Relay namespace.</span></span> <span data-ttu-id="2132b-107">一旦建立之後，命名空間資源資訊清單就是不可變的。</span><span class="sxs-lookup"><span data-stu-id="2132b-107">Once created, the namespace resource manifest is immutable.</span></span>

## <span data-ttu-id="2132b-108">示例</span><span class="sxs-lookup"><span data-stu-id="2132b-108">EXAMPLES</span></span>

### <span data-ttu-id="2132b-109">範例1</span><span class="sxs-lookup"><span data-stu-id="2132b-109">Example 1</span></span>
```
PS C:\> New-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -Location "West US" -Tag @{Tag1="Tag1Value"}

ProvisioningState  : Succeeded
CreatedAt          : 4/12/2017 12:38:47 AM
UpdatedAt          : 4/12/2017 12:39:10 AM
ServiceBusEndpoint : https://TestNameSpace-Relay1.servicebus.windows.net:443/
MetricId           : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX:testnamespace-relay1
Location           : West US
Tags               : {[tag1, Tag1Value]}
Id                 : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1
Name               : TestNameSpace-Relay1
Type               : Microsoft.Relay/namespaces
```

<span data-ttu-id="2132b-110">在指定的資源群組中建立新的中繼命名空間。</span><span class="sxs-lookup"><span data-stu-id="2132b-110">Creates a new Relay namespace within the specified resource group.</span></span>

## <span data-ttu-id="2132b-111">參數</span><span class="sxs-lookup"><span data-stu-id="2132b-111">PARAMETERS</span></span>

### <span data-ttu-id="2132b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2132b-112">-DefaultProfile</span></span>
<span data-ttu-id="2132b-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2132b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2132b-114">-位置</span><span class="sxs-lookup"><span data-stu-id="2132b-114">-Location</span></span>
<span data-ttu-id="2132b-115">中繼命名空間位置。</span><span class="sxs-lookup"><span data-stu-id="2132b-115">Relay Namespace Location.</span></span>

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

### <span data-ttu-id="2132b-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="2132b-116">-Name</span></span>
<span data-ttu-id="2132b-117">中繼命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="2132b-117">Relay Namespace Name</span></span>

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

### <span data-ttu-id="2132b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2132b-118">-ResourceGroupName</span></span>
<span data-ttu-id="2132b-119">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="2132b-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="2132b-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="2132b-120">-Tag</span></span>
<span data-ttu-id="2132b-121">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="2132b-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2132b-122">例如：</span><span class="sxs-lookup"><span data-stu-id="2132b-122">For example:</span></span>

<span data-ttu-id="2132b-123">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="2132b-123">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="2132b-124">-確認</span><span class="sxs-lookup"><span data-stu-id="2132b-124">-Confirm</span></span>
<span data-ttu-id="2132b-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2132b-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2132b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2132b-126">-WhatIf</span></span>
<span data-ttu-id="2132b-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2132b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2132b-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2132b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2132b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2132b-129">CommonParameters</span></span>
<span data-ttu-id="2132b-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2132b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2132b-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2132b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2132b-132">輸入</span><span class="sxs-lookup"><span data-stu-id="2132b-132">INPUTS</span></span>

### <span data-ttu-id="2132b-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2132b-133">-ResourceGroupName</span></span>
 <span data-ttu-id="2132b-134">System.object</span><span class="sxs-lookup"><span data-stu-id="2132b-134">System.String</span></span>

### <span data-ttu-id="2132b-135">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="2132b-135">-NamespaceName</span></span>
 <span data-ttu-id="2132b-136">System.object</span><span class="sxs-lookup"><span data-stu-id="2132b-136">System.String</span></span>

### <span data-ttu-id="2132b-137">-位置</span><span class="sxs-lookup"><span data-stu-id="2132b-137">-Location</span></span>
 <span data-ttu-id="2132b-138">System.object</span><span class="sxs-lookup"><span data-stu-id="2132b-138">System.String</span></span>

### <span data-ttu-id="2132b-139">-SkuName</span><span class="sxs-lookup"><span data-stu-id="2132b-139">-SkuName</span></span>
 <span data-ttu-id="2132b-140">System.object</span><span class="sxs-lookup"><span data-stu-id="2132b-140">System.String</span></span>

### <span data-ttu-id="2132b-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="2132b-141">-Tag</span></span>
 <span data-ttu-id="2132b-142">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2132b-142">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2132b-143">輸出</span><span class="sxs-lookup"><span data-stu-id="2132b-143">OUTPUTS</span></span>

### <span data-ttu-id="2132b-144">RelayNamespaceAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2132b-144">Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttributes</span></span>

## <span data-ttu-id="2132b-145">筆記</span><span class="sxs-lookup"><span data-stu-id="2132b-145">NOTES</span></span>

## <span data-ttu-id="2132b-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="2132b-146">RELATED LINKS</span></span>

