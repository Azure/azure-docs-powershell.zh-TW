---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateEndpoint.md
ms.openlocfilehash: df298b41ea1efa4915cb7556b9fd07b1d8f3e2de
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100131210"
---
# <span data-ttu-id="f1059-101">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f1059-101">New-AzPrivateEndpoint</span></span>

## <span data-ttu-id="f1059-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f1059-102">SYNOPSIS</span></span>
<span data-ttu-id="f1059-103">建立私人端點。</span><span class="sxs-lookup"><span data-stu-id="f1059-103">Creates a private endpoint.</span></span>

## <span data-ttu-id="f1059-104">句法</span><span class="sxs-lookup"><span data-stu-id="f1059-104">SYNTAX</span></span>

### <span data-ttu-id="f1059-105">同時</span><span class="sxs-lookup"><span data-stu-id="f1059-105">All</span></span>

```
New-AzPrivateEndpoint -Name <String> -ResourceGroupName <String> -Location <String> -Subnet <PSSubnet>
 -PrivateLinkServiceConnection <PSPrivateLinkServiceConnection[]> [-ByManualRequest] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1059-106">說明</span><span class="sxs-lookup"><span data-stu-id="f1059-106">DESCRIPTION</span></span>

<span data-ttu-id="f1059-107">**新的-AzPrivateEndpoint** Cmdlet 會建立一個專用端點。</span><span class="sxs-lookup"><span data-stu-id="f1059-107">The **New-AzPrivateEndpoint** cmdlet creates a private endpoint.</span></span>

## <span data-ttu-id="f1059-108">示例</span><span class="sxs-lookup"><span data-stu-id="f1059-108">EXAMPLES</span></span>

### <span data-ttu-id="f1059-109">範例1：建立私人端點</span><span class="sxs-lookup"><span data-stu-id="f1059-109">Example 1: Create a private endpoint</span></span>

<span data-ttu-id="f1059-110">下列範例會在虛擬網路的指定子網上，建立具有特定私人連結服務識別碼的專用端點。</span><span class="sxs-lookup"><span data-stu-id="f1059-110">The following example creates a private endpoint with a specific private link service ID in the specified subnet in a virtual network.</span></span>

```powershell
$virtualNetwork = Get-AzVirtualNetwork -ResourceName 'myVirtualNetwork' -ResourceGroupName 'myResourceGroup'
$subnet = $virtualNetwork | Select-Object -ExpandProperty subnets | Where-Object Name -eq 'mySubnet'
$plsConnection= New-AzPrivateLinkServiceConnection -Name 'MyPLSConnections' -PrivateLinkServiceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup/providers/Microsoft.Network/privateLinkServices/privateLinkService' -RequestMessage 'Please Approve my request'
New-AzPrivateEndpoint -Name 'MyPrivateEndpoint' -ResourceGroup 'myResourceGroup' -Location 'centralus' -PrivateLinkServiceConnection $plsConnection -Subnet $subnet
```

## <span data-ttu-id="f1059-111">參數</span><span class="sxs-lookup"><span data-stu-id="f1059-111">PARAMETERS</span></span>

### <span data-ttu-id="f1059-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f1059-112">-AsJob</span></span>

<span data-ttu-id="f1059-113">在背景中執行 Cmdlet 作為作業。</span><span class="sxs-lookup"><span data-stu-id="f1059-113">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="f1059-114">-ByManualRequest</span><span class="sxs-lookup"><span data-stu-id="f1059-114">-ByManualRequest</span></span>

<span data-ttu-id="f1059-115">使用手動要求建立連線。</span><span class="sxs-lookup"><span data-stu-id="f1059-115">Use manual request to establish the connection.</span></span>

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

### <span data-ttu-id="f1059-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1059-116">-DefaultProfile</span></span>

<span data-ttu-id="f1059-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f1059-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1059-118">-Force</span><span class="sxs-lookup"><span data-stu-id="f1059-118">-Force</span></span>

<span data-ttu-id="f1059-119">不要要求確認覆寫資源。</span><span class="sxs-lookup"><span data-stu-id="f1059-119">Do not ask for confirmation to overwrite a resource.</span></span>

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

### <span data-ttu-id="f1059-120">-位置</span><span class="sxs-lookup"><span data-stu-id="f1059-120">-Location</span></span>

<span data-ttu-id="f1059-121">指定私人端點的位置。</span><span class="sxs-lookup"><span data-stu-id="f1059-121">Specifies a location for the private endpoint.</span></span> <span data-ttu-id="f1059-122">使用 [AzLocation](/powershell/module/az.resources/get-azlocation) 來判斷此參數的有效值。</span><span class="sxs-lookup"><span data-stu-id="f1059-122">Use [Get-AzLocation](/powershell/module/az.resources/get-azlocation) to determine valid values for this parameter.</span></span>

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

### <span data-ttu-id="f1059-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="f1059-123">-Name</span></span>

<span data-ttu-id="f1059-124">私人端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="f1059-124">Name of the private endpoint.</span></span>

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

### <span data-ttu-id="f1059-125">-PrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="f1059-125">-PrivateLinkServiceConnection</span></span>

<span data-ttu-id="f1059-126">要連接專用端點的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="f1059-126">The resource ID to connect the private endpoint.</span></span>

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

### <span data-ttu-id="f1059-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1059-127">-ResourceGroupName</span></span>

<span data-ttu-id="f1059-128">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f1059-128">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="f1059-129">-子網</span><span class="sxs-lookup"><span data-stu-id="f1059-129">-Subnet</span></span>

<span data-ttu-id="f1059-130">私人端點的子網。</span><span class="sxs-lookup"><span data-stu-id="f1059-130">The subnet of the private endpoint.</span></span>

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

### <span data-ttu-id="f1059-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="f1059-131">-Tag</span></span>

<span data-ttu-id="f1059-132">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="f1059-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f1059-133">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="f1059-133">For example: @{key0='value0';key1=$null;key2='value2'}</span></span>

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

### <span data-ttu-id="f1059-134">-確認</span><span class="sxs-lookup"><span data-stu-id="f1059-134">-Confirm</span></span>

<span data-ttu-id="f1059-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f1059-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1059-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1059-136">-WhatIf</span></span>

<span data-ttu-id="f1059-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f1059-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1059-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f1059-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1059-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1059-139">CommonParameters</span></span>

<span data-ttu-id="f1059-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f1059-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1059-141">如需詳細資訊，請參閱 [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters)。</span><span class="sxs-lookup"><span data-stu-id="f1059-141">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>

## <span data-ttu-id="f1059-142">輸入</span><span class="sxs-lookup"><span data-stu-id="f1059-142">INPUTS</span></span>

### <span data-ttu-id="f1059-143">System.object</span><span class="sxs-lookup"><span data-stu-id="f1059-143">System.String</span></span>

### <span data-ttu-id="f1059-144">PSSubnet 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f1059-144">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="f1059-145">PSPrivateLinkServiceConnection [] （[]）</span><span class="sxs-lookup"><span data-stu-id="f1059-145">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceConnection[]</span></span>

## <span data-ttu-id="f1059-146">輸出</span><span class="sxs-lookup"><span data-stu-id="f1059-146">OUTPUTS</span></span>

### <span data-ttu-id="f1059-147">PSPrivateEndpoint 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f1059-147">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="f1059-148">筆記</span><span class="sxs-lookup"><span data-stu-id="f1059-148">NOTES</span></span>

## <span data-ttu-id="f1059-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="f1059-149">RELATED LINKS</span></span>

[<span data-ttu-id="f1059-150">AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f1059-150">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="f1059-151">移除-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f1059-151">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)

[<span data-ttu-id="f1059-152">新-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="f1059-152">New-AzPrivateLinkServiceConnection</span></span>](./New-AzPrivateLinkServiceConnection.md)