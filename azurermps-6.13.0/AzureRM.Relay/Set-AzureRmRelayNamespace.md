---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/set-azurermrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayNamespace.md
ms.openlocfilehash: 6bb333de426236099bed7402fc4756181415c4ec
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623738"
---
# <span data-ttu-id="461eb-101">Set-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="461eb-101">Set-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="461eb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="461eb-102">SYNOPSIS</span></span>
<span data-ttu-id="461eb-103">更新現有中繼命名空間的描述。</span><span class="sxs-lookup"><span data-stu-id="461eb-103">Updates the description of an existing Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="461eb-104">句法</span><span class="sxs-lookup"><span data-stu-id="461eb-104">SYNTAX</span></span>

```
Set-AzureRmRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-InputObject <RelayNamespaceAttirbutesUpdateParameter>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="461eb-105">說明</span><span class="sxs-lookup"><span data-stu-id="461eb-105">DESCRIPTION</span></span>
<span data-ttu-id="461eb-106">**AzureRmRelayNamespace** Cmdlet 會更新資源群組中指定的中繼命名空間的描述。</span><span class="sxs-lookup"><span data-stu-id="461eb-106">The **Set-AzureRmRelayNamespace** cmdlet updates the description of the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="461eb-107">示例</span><span class="sxs-lookup"><span data-stu-id="461eb-107">EXAMPLES</span></span>

### <span data-ttu-id="461eb-108">範例1</span><span class="sxs-lookup"><span data-stu-id="461eb-108">Example 1</span></span>
```
PS C:\> Set-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1 -Tag @{Tag2="Tag2Value"}

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

<span data-ttu-id="461eb-109">使用新的描述更新中繼命名空間。</span><span class="sxs-lookup"><span data-stu-id="461eb-109">Updates the Relay namespace with a new description.</span></span>

## <span data-ttu-id="461eb-110">參數</span><span class="sxs-lookup"><span data-stu-id="461eb-110">PARAMETERS</span></span>

### <span data-ttu-id="461eb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="461eb-111">-DefaultProfile</span></span>
<span data-ttu-id="461eb-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="461eb-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="461eb-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="461eb-113">-InputObject</span></span>
<span data-ttu-id="461eb-114">中繼命名空間物件。</span><span class="sxs-lookup"><span data-stu-id="461eb-114">Relay Namespace object.</span></span>

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

### <span data-ttu-id="461eb-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="461eb-115">-Name</span></span>
<span data-ttu-id="461eb-116">中繼命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="461eb-116">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="461eb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="461eb-117">-ResourceGroupName</span></span>
<span data-ttu-id="461eb-118">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="461eb-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="461eb-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="461eb-119">-Tag</span></span>
<span data-ttu-id="461eb-120">代表資源標記的 Hashtables。</span><span class="sxs-lookup"><span data-stu-id="461eb-120">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="461eb-121">-確認</span><span class="sxs-lookup"><span data-stu-id="461eb-121">-Confirm</span></span>
<span data-ttu-id="461eb-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="461eb-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="461eb-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="461eb-123">-WhatIf</span></span>
<span data-ttu-id="461eb-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="461eb-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="461eb-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="461eb-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="461eb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="461eb-126">CommonParameters</span></span>
<span data-ttu-id="461eb-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="461eb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="461eb-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="461eb-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="461eb-129">輸入</span><span class="sxs-lookup"><span data-stu-id="461eb-129">INPUTS</span></span>

### <span data-ttu-id="461eb-130">System.object</span><span class="sxs-lookup"><span data-stu-id="461eb-130">System.String</span></span>
<span data-ttu-id="461eb-131">[RelayNamespaceAttirbutesUpdateParameter].. 雜湊表。</span><span class="sxs-lookup"><span data-stu-id="461eb-131">System.Collections.Hashtable Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttirbutesUpdateParameter</span></span>


## <span data-ttu-id="461eb-132">輸出</span><span class="sxs-lookup"><span data-stu-id="461eb-132">OUTPUTS</span></span>

### <span data-ttu-id="461eb-133">PSRelayNamespaceAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="461eb-133">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>


## <span data-ttu-id="461eb-134">筆記</span><span class="sxs-lookup"><span data-stu-id="461eb-134">NOTES</span></span>

## <span data-ttu-id="461eb-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="461eb-135">RELATED LINKS</span></span>