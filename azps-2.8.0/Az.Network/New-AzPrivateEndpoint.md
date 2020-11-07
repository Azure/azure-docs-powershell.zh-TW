---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateEndpoint.md
ms.openlocfilehash: c72af57f860dcc1c889ecf81111341fa7dbe21eb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93790793"
---
# <span data-ttu-id="4dba3-101">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="4dba3-101">New-AzPrivateEndpoint</span></span>

## <span data-ttu-id="4dba3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4dba3-102">SYNOPSIS</span></span>
<span data-ttu-id="4dba3-103">建立私人端點。</span><span class="sxs-lookup"><span data-stu-id="4dba3-103">Creates a private endpoint.</span></span>

## <span data-ttu-id="4dba3-104">句法</span><span class="sxs-lookup"><span data-stu-id="4dba3-104">SYNTAX</span></span>

```
New-AzPrivateEndpoint -Name <String> -ResourceGroupName <String> -Location <String> -Subnet <PSSubnet>
 -PrivateLinkServiceConnection <PSPrivateLinkServiceConnection[]> [-ByManualRequest] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4dba3-105">說明</span><span class="sxs-lookup"><span data-stu-id="4dba3-105">DESCRIPTION</span></span>
<span data-ttu-id="4dba3-106">**新的-AzPrivateEndpoint** Cmdlet 會建立一個專用端點。</span><span class="sxs-lookup"><span data-stu-id="4dba3-106">The **New-AzPrivateEndpoint** cmdlet creates a private endpoint.</span></span>

## <span data-ttu-id="4dba3-107">示例</span><span class="sxs-lookup"><span data-stu-id="4dba3-107">EXAMPLES</span></span>

### <span data-ttu-id="4dba3-108">1：建立私人端點</span><span class="sxs-lookup"><span data-stu-id="4dba3-108">1: Create a private endpoint</span></span>
```
$virtualNetwork = Get-AzVirtualNetwork -ResourceName MyVirtualNetwork -ResourceGroupName TestResourceGroup
$plsConnection= New-AzPrivateLinkServiceConnection -Name MyPLSConnections -PrivateLinkServiceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/privateLinkServices/privateLinkService" -RequestMessage "Please Approve my request"
New-AzPrivateEndpoint -Name MyPrivateEndpoint -ResourceGroup TestResourceGroup -Location centralus -PrivateLinkServiceConnection $plsConnection -Subnet $virtualNetwork.Subnets[0]
```

<span data-ttu-id="4dba3-109">這個範例會在虛擬網路的特定子網上，建立具有特定專用連結服務識別碼的專用端點。</span><span class="sxs-lookup"><span data-stu-id="4dba3-109">This example creates a private endpoint with specific private link service id in a specific subnet in a virtual network.</span></span>

## <span data-ttu-id="4dba3-110">參數</span><span class="sxs-lookup"><span data-stu-id="4dba3-110">PARAMETERS</span></span>

### <span data-ttu-id="4dba3-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4dba3-111">-AsJob</span></span>
<span data-ttu-id="4dba3-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="4dba3-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dba3-113">-ByManualRequest</span><span class="sxs-lookup"><span data-stu-id="4dba3-113">-ByManualRequest</span></span>
<span data-ttu-id="4dba3-114">使用手動要求。</span><span class="sxs-lookup"><span data-stu-id="4dba3-114">Using manual request.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dba3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dba3-115">-DefaultProfile</span></span>
<span data-ttu-id="4dba3-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4dba3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4dba3-117">-Force</span><span class="sxs-lookup"><span data-stu-id="4dba3-117">-Force</span></span>
<span data-ttu-id="4dba3-118">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="4dba3-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dba3-119">-位置</span><span class="sxs-lookup"><span data-stu-id="4dba3-119">-Location</span></span>
<span data-ttu-id="4dba3-120">位於.</span><span class="sxs-lookup"><span data-stu-id="4dba3-120">location.</span></span>

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

### <span data-ttu-id="4dba3-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="4dba3-121">-Name</span></span>
<span data-ttu-id="4dba3-122">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="4dba3-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dba3-123">-PrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="4dba3-123">-PrivateLinkServiceConnection</span></span>
<span data-ttu-id="4dba3-124">私人連結服務連線。</span><span class="sxs-lookup"><span data-stu-id="4dba3-124">The private link service connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceConnection[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dba3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4dba3-125">-ResourceGroupName</span></span>
<span data-ttu-id="4dba3-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4dba3-126">The resource group name.</span></span>

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

### <span data-ttu-id="4dba3-127">-子網</span><span class="sxs-lookup"><span data-stu-id="4dba3-127">-Subnet</span></span>
<span data-ttu-id="4dba3-128">私人端點的子網</span><span class="sxs-lookup"><span data-stu-id="4dba3-128">The subnet of the private endpoint</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dba3-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="4dba3-129">-Tag</span></span>
<span data-ttu-id="4dba3-130">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="4dba3-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4dba3-131">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="4dba3-131">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="4dba3-132">-確認</span><span class="sxs-lookup"><span data-stu-id="4dba3-132">-Confirm</span></span>
<span data-ttu-id="4dba3-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4dba3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4dba3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4dba3-134">-WhatIf</span></span>
<span data-ttu-id="4dba3-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4dba3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4dba3-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4dba3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4dba3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dba3-137">CommonParameters</span></span>
<span data-ttu-id="4dba3-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4dba3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dba3-139">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4dba3-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dba3-140">輸入</span><span class="sxs-lookup"><span data-stu-id="4dba3-140">INPUTS</span></span>

### <span data-ttu-id="4dba3-141">System.object</span><span class="sxs-lookup"><span data-stu-id="4dba3-141">System.String</span></span>

### <span data-ttu-id="4dba3-142">PSSubnet 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4dba3-142">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="4dba3-143">PSPrivateLinkServiceConnection [] （[]）</span><span class="sxs-lookup"><span data-stu-id="4dba3-143">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceConnection[]</span></span>

## <span data-ttu-id="4dba3-144">輸出</span><span class="sxs-lookup"><span data-stu-id="4dba3-144">OUTPUTS</span></span>

### <span data-ttu-id="4dba3-145">PSPrivateEndpoint 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4dba3-145">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="4dba3-146">筆記</span><span class="sxs-lookup"><span data-stu-id="4dba3-146">NOTES</span></span>

## <span data-ttu-id="4dba3-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="4dba3-147">RELATED LINKS</span></span>

[<span data-ttu-id="4dba3-148">AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="4dba3-148">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="4dba3-149">移除-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="4dba3-149">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)

[<span data-ttu-id="4dba3-150">新-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="4dba3-150">New-AzPrivateLinkServiceConnection</span></span>](./New-AzPrivateLinkServiceConnection.md)