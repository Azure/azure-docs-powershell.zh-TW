---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/set-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayNamespace.md
ms.openlocfilehash: 25c633c2929967a5fb580addb78639bff8b6197f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914546"
---
# <span data-ttu-id="564a6-101">Set-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="564a6-101">Set-AzRelayNamespace</span></span>

## <span data-ttu-id="564a6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="564a6-102">SYNOPSIS</span></span>
<span data-ttu-id="564a6-103">更新現有 Relay 命名空間的描述。</span><span class="sxs-lookup"><span data-stu-id="564a6-103">Updates the description of an existing Relay namespace.</span></span>

## <span data-ttu-id="564a6-104">語法</span><span class="sxs-lookup"><span data-stu-id="564a6-104">SYNTAX</span></span>

```
Set-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-InputObject <RelayNamespaceAttirbutesUpdateParameter>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="564a6-105">描述</span><span class="sxs-lookup"><span data-stu-id="564a6-105">DESCRIPTION</span></span>
<span data-ttu-id="564a6-106">**Set-AzRelayNamespace** Cmdlet 會更新資源群組中指定之 Relay 命名空間的描述。</span><span class="sxs-lookup"><span data-stu-id="564a6-106">The **Set-AzRelayNamespace** cmdlet updates the description of the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="564a6-107">例子</span><span class="sxs-lookup"><span data-stu-id="564a6-107">EXAMPLES</span></span>

### <span data-ttu-id="564a6-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="564a6-108">Example 1</span></span>
```
PS C:\> Set-AzRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1 -Tag @{Tag2="Tag2Value"}

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

<span data-ttu-id="564a6-109">以新的描述更新 Relay 命名空間。</span><span class="sxs-lookup"><span data-stu-id="564a6-109">Updates the Relay namespace with a new description.</span></span>

## <span data-ttu-id="564a6-110">參數</span><span class="sxs-lookup"><span data-stu-id="564a6-110">PARAMETERS</span></span>

### <span data-ttu-id="564a6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="564a6-111">-DefaultProfile</span></span>
<span data-ttu-id="564a6-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="564a6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="564a6-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="564a6-113">-InputObject</span></span>
<span data-ttu-id="564a6-114">Relay 命名空間物件。</span><span class="sxs-lookup"><span data-stu-id="564a6-114">Relay Namespace object.</span></span>

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

### <span data-ttu-id="564a6-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="564a6-115">-Name</span></span>
<span data-ttu-id="564a6-116">轉場命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="564a6-116">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="564a6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="564a6-117">-ResourceGroupName</span></span>
<span data-ttu-id="564a6-118">資源組名。</span><span class="sxs-lookup"><span data-stu-id="564a6-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="564a6-119">-標記</span><span class="sxs-lookup"><span data-stu-id="564a6-119">-Tag</span></span>
<span data-ttu-id="564a6-120">代表資源標記的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="564a6-120">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="564a6-121">-確認</span><span class="sxs-lookup"><span data-stu-id="564a6-121">-Confirm</span></span>
<span data-ttu-id="564a6-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="564a6-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="564a6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="564a6-123">-WhatIf</span></span>
<span data-ttu-id="564a6-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="564a6-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="564a6-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="564a6-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="564a6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="564a6-126">CommonParameters</span></span>
<span data-ttu-id="564a6-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="564a6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="564a6-128">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="564a6-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="564a6-129">輸入</span><span class="sxs-lookup"><span data-stu-id="564a6-129">INPUTS</span></span>

### <span data-ttu-id="564a6-130">System.String</span><span class="sxs-lookup"><span data-stu-id="564a6-130">System.String</span></span>

### <span data-ttu-id="564a6-131">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="564a6-131">System.Collections.Hashtable</span></span>

### <span data-ttu-id="564a6-132">Microsoft.Azure.Commands.Relay.models.RelayNamespaceAttirbutesUpdateParameter</span><span class="sxs-lookup"><span data-stu-id="564a6-132">Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttirbutesUpdateParameter</span></span>

## <span data-ttu-id="564a6-133">輸出</span><span class="sxs-lookup"><span data-stu-id="564a6-133">OUTPUTS</span></span>

### <span data-ttu-id="564a6-134">Microsoft.Azure.Commands.Relay.models.PSRelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="564a6-134">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>

## <span data-ttu-id="564a6-135">筆記</span><span class="sxs-lookup"><span data-stu-id="564a6-135">NOTES</span></span>

## <span data-ttu-id="564a6-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="564a6-136">RELATED LINKS</span></span>
