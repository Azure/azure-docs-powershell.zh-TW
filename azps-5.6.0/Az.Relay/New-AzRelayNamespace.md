---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/new-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayNamespace.md
ms.openlocfilehash: c6f0fc3d8a0ef96a8b54b954e07fb1a9d1c644e3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914581"
---
# <span data-ttu-id="ee2a3-101">New-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="ee2a3-101">New-AzRelayNamespace</span></span>

## <span data-ttu-id="ee2a3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ee2a3-102">SYNOPSIS</span></span>
<span data-ttu-id="ee2a3-103">建立新的轉場命名空間。</span><span class="sxs-lookup"><span data-stu-id="ee2a3-103">Creates a new Relay namespace.</span></span>

## <span data-ttu-id="ee2a3-104">語法</span><span class="sxs-lookup"><span data-stu-id="ee2a3-104">SYNTAX</span></span>

```
New-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee2a3-105">描述</span><span class="sxs-lookup"><span data-stu-id="ee2a3-105">DESCRIPTION</span></span>
<span data-ttu-id="ee2a3-106">**New-AzRelayNamespace** Cmdlet 會建立新的 Relay 命名空間。</span><span class="sxs-lookup"><span data-stu-id="ee2a3-106">The **New-AzRelayNamespace** cmdlet creates a new Relay namespace.</span></span> <span data-ttu-id="ee2a3-107">建立後，命名空間資源清單可通通。</span><span class="sxs-lookup"><span data-stu-id="ee2a3-107">Once created, the namespace resource manifest is immutable.</span></span>

## <span data-ttu-id="ee2a3-108">例子</span><span class="sxs-lookup"><span data-stu-id="ee2a3-108">EXAMPLES</span></span>

### <span data-ttu-id="ee2a3-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="ee2a3-109">Example 1</span></span>
```
PS C:\> New-AzRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1 -Location "West US" -Tag @{Tag1="Tag1Value"}

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

<span data-ttu-id="ee2a3-110">在指定的資源群組中建立新的 Relay 命名空間。</span><span class="sxs-lookup"><span data-stu-id="ee2a3-110">Creates a new Relay namespace within the specified resource group.</span></span>

## <span data-ttu-id="ee2a3-111">參數</span><span class="sxs-lookup"><span data-stu-id="ee2a3-111">PARAMETERS</span></span>

### <span data-ttu-id="ee2a3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee2a3-112">-DefaultProfile</span></span>
<span data-ttu-id="ee2a3-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ee2a3-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee2a3-114">-位置</span><span class="sxs-lookup"><span data-stu-id="ee2a3-114">-Location</span></span>
<span data-ttu-id="ee2a3-115">轉場命名空間位置。</span><span class="sxs-lookup"><span data-stu-id="ee2a3-115">Relay Namespace Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee2a3-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="ee2a3-116">-Name</span></span>
<span data-ttu-id="ee2a3-117">轉場命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="ee2a3-117">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="ee2a3-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee2a3-118">-ResourceGroupName</span></span>
<span data-ttu-id="ee2a3-119">資源組名。</span><span class="sxs-lookup"><span data-stu-id="ee2a3-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="ee2a3-120">-標記</span><span class="sxs-lookup"><span data-stu-id="ee2a3-120">-Tag</span></span>
<span data-ttu-id="ee2a3-121">代表資源標記的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="ee2a3-121">Hashtables which represents resource Tags.</span></span>

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

### <span data-ttu-id="ee2a3-122">-確認</span><span class="sxs-lookup"><span data-stu-id="ee2a3-122">-Confirm</span></span>
<span data-ttu-id="ee2a3-123">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ee2a3-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee2a3-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee2a3-124">-WhatIf</span></span>
<span data-ttu-id="ee2a3-125">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ee2a3-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee2a3-126">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ee2a3-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee2a3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee2a3-127">CommonParameters</span></span>
<span data-ttu-id="ee2a3-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ee2a3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee2a3-129">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="ee2a3-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee2a3-130">輸入</span><span class="sxs-lookup"><span data-stu-id="ee2a3-130">INPUTS</span></span>

### <span data-ttu-id="ee2a3-131">System.String</span><span class="sxs-lookup"><span data-stu-id="ee2a3-131">System.String</span></span>

### <span data-ttu-id="ee2a3-132">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="ee2a3-132">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ee2a3-133">輸出</span><span class="sxs-lookup"><span data-stu-id="ee2a3-133">OUTPUTS</span></span>

### <span data-ttu-id="ee2a3-134">Microsoft.Azure.Commands.Relay.models.PSRelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="ee2a3-134">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>

## <span data-ttu-id="ee2a3-135">筆記</span><span class="sxs-lookup"><span data-stu-id="ee2a3-135">NOTES</span></span>

## <span data-ttu-id="ee2a3-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="ee2a3-136">RELATED LINKS</span></span>
