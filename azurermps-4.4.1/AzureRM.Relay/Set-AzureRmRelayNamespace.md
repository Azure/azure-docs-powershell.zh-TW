---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayNamespace.md
ms.openlocfilehash: c243f31ee549443ad959bde13abc9ff3b68c1560
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448014"
---
# <span data-ttu-id="6baf6-101">Set-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="6baf6-101">Set-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="6baf6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6baf6-102">SYNOPSIS</span></span>
<span data-ttu-id="6baf6-103">更新現有中繼命名空間的描述。</span><span class="sxs-lookup"><span data-stu-id="6baf6-103">Updates the description of an existing Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6baf6-104">句法</span><span class="sxs-lookup"><span data-stu-id="6baf6-104">SYNTAX</span></span>

```
Set-AzureRmRelayNamespace [-ResourceGroupName] <String> -Name <String> [-Tag <Hashtable>]
 [-InputObject <RelayNamespaceAttirbutesUpdateParameter>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6baf6-105">說明</span><span class="sxs-lookup"><span data-stu-id="6baf6-105">DESCRIPTION</span></span>
<span data-ttu-id="6baf6-106">**AzureRmRelayNamespace** Cmdlet 會更新資源群組中指定的中繼命名空間的描述。</span><span class="sxs-lookup"><span data-stu-id="6baf6-106">The **Set-AzureRmRelayNamespace** cmdlet updates the description of the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="6baf6-107">示例</span><span class="sxs-lookup"><span data-stu-id="6baf6-107">EXAMPLES</span></span>

### <span data-ttu-id="6baf6-108">範例1</span><span class="sxs-lookup"><span data-stu-id="6baf6-108">Example 1</span></span>
```
PS C:\> Set-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -Tag @{Tag2="Tag2Value"}

ProvisioningState  :
CreatedAt          : 4/12/2017 12:38:47 AM
UpdatedAt          : 4/12/2017 12:39:10 AM
ServiceBusEndpoint : https://TestNameSpace-Relay1.servicebus.windows.net:443/
MetricId           :
Location           :
Tags               : {[tag2, Tag2Value]}
Id                 :
Name               :
Type               :
```

<span data-ttu-id="6baf6-109">使用新的描述更新中繼命名空間。</span><span class="sxs-lookup"><span data-stu-id="6baf6-109">Updates the Relay namespace with a new description.</span></span>

## <span data-ttu-id="6baf6-110">參數</span><span class="sxs-lookup"><span data-stu-id="6baf6-110">PARAMETERS</span></span>

### <span data-ttu-id="6baf6-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6baf6-111">-ResourceGroupName</span></span>
<span data-ttu-id="6baf6-112">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="6baf6-112">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6baf6-113">-Tag</span><span class="sxs-lookup"><span data-stu-id="6baf6-113">-Tag</span></span>
<span data-ttu-id="6baf6-114">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="6baf6-114">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6baf6-115">例如：</span><span class="sxs-lookup"><span data-stu-id="6baf6-115">For example:</span></span>

<span data-ttu-id="6baf6-116">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="6baf6-116">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="6baf6-117">-確認</span><span class="sxs-lookup"><span data-stu-id="6baf6-117">-Confirm</span></span>
<span data-ttu-id="6baf6-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6baf6-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6baf6-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6baf6-119">-WhatIf</span></span>
<span data-ttu-id="6baf6-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6baf6-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6baf6-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6baf6-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6baf6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6baf6-122">-DefaultProfile</span></span>
<span data-ttu-id="6baf6-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6baf6-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6baf6-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6baf6-124">-InputObject</span></span>
<span data-ttu-id="6baf6-125">中繼命名空間物件。</span><span class="sxs-lookup"><span data-stu-id="6baf6-125">Relay Namespace object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttirbutesUpdateParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6baf6-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="6baf6-126">-Name</span></span>
<span data-ttu-id="6baf6-127">中繼命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="6baf6-127">Relay Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6baf6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6baf6-128">CommonParameters</span></span>
<span data-ttu-id="6baf6-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6baf6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6baf6-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6baf6-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6baf6-131">輸入</span><span class="sxs-lookup"><span data-stu-id="6baf6-131">INPUTS</span></span>

### <span data-ttu-id="6baf6-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6baf6-132">-ResourceGroupName</span></span>
 <span data-ttu-id="6baf6-133">System.object</span><span class="sxs-lookup"><span data-stu-id="6baf6-133">System.String</span></span>

### <span data-ttu-id="6baf6-134">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="6baf6-134">-NamespaceName</span></span>
 <span data-ttu-id="6baf6-135">System.object</span><span class="sxs-lookup"><span data-stu-id="6baf6-135">System.String</span></span>

### <span data-ttu-id="6baf6-136">-位置</span><span class="sxs-lookup"><span data-stu-id="6baf6-136">-Location</span></span>
 <span data-ttu-id="6baf6-137">System.object</span><span class="sxs-lookup"><span data-stu-id="6baf6-137">System.String</span></span>

### <span data-ttu-id="6baf6-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="6baf6-138">-Tag</span></span>
 <span data-ttu-id="6baf6-139">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6baf6-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="6baf6-140">輸出</span><span class="sxs-lookup"><span data-stu-id="6baf6-140">OUTPUTS</span></span>

### <span data-ttu-id="6baf6-141">RelayNamespaceAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6baf6-141">Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttributes</span></span>

## <span data-ttu-id="6baf6-142">筆記</span><span class="sxs-lookup"><span data-stu-id="6baf6-142">NOTES</span></span>

## <span data-ttu-id="6baf6-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="6baf6-143">RELATED LINKS</span></span>

