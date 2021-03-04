---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 2da755a4ac3044c6499faee82a74e2c9ec7d9f6e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909534"
---
# <span data-ttu-id="aee4c-101">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="aee4c-101">Add-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="aee4c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="aee4c-102">SYNOPSIS</span></span>
<span data-ttu-id="aee4c-103">建立與 NetworkInterface 相關聯的 TapConfiguration 資源。</span><span class="sxs-lookup"><span data-stu-id="aee4c-103">Creates a TapConfiguration resource associated to a NetworkInterface.</span></span> <span data-ttu-id="aee4c-104">這會參照現有的 VirtualNetworkTap 資源。</span><span class="sxs-lookup"><span data-stu-id="aee4c-104">This will reference to an existing VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="aee4c-105">語法</span><span class="sxs-lookup"><span data-stu-id="aee4c-105">SYNTAX</span></span>

### <span data-ttu-id="aee4c-106">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="aee4c-106">SetByResource (Default)</span></span>
```
Add-AzNetworkInterfaceTapConfig -NetworkInterface <PSNetworkInterface> -Name <String>
 [-VirtualNetworkTap <PSVirtualNetworkTap>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aee4c-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="aee4c-107">SetByResourceId</span></span>
```
Add-AzNetworkInterfaceTapConfig -NetworkInterface <PSNetworkInterface> -Name <String>
 [-VirtualNetworkTapId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aee4c-108">描述</span><span class="sxs-lookup"><span data-stu-id="aee4c-108">DESCRIPTION</span></span>
<span data-ttu-id="aee4c-109">**Add-AzNetworkInterfaceTapConfig** Cmdlet 會建立與 NetworkInterface 相關聯的 TapConfiguration 資源。</span><span class="sxs-lookup"><span data-stu-id="aee4c-109">The **Add-AzNetworkInterfaceTapConfig** cmdlet creates a TapConfiguration resource associated to a NetworkInterface.</span></span> <span data-ttu-id="aee4c-110">這會參照現有的 VirtualNetworkTap 資源。</span><span class="sxs-lookup"><span data-stu-id="aee4c-110">This will reference to an existing VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="aee4c-111">例子</span><span class="sxs-lookup"><span data-stu-id="aee4c-111">EXAMPLES</span></span>

### <span data-ttu-id="aee4c-112">範例 1：將 TapConfiguration 新增到一個給定 NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="aee4c-112">Example 1: Add TapConfiguration to a given NetworkInterface</span></span>
```
PS C:\>Add-AzNetworkInterfaceTapConfig -NetworkInterface $sourceNic -VirtualNetworkTap $vVirtualNetworkTap -Name 'myTapConfig'
```

<span data-ttu-id="aee4c-113">將 TapConfiguration 新增到 sourceNic。</span><span class="sxs-lookup"><span data-stu-id="aee4c-113">Add the TapConfiguration to a sourceNic.</span></span> <span data-ttu-id="aee4c-114">sourceNic VM 的流量會鏡像到 vVirtualNetworkTap 資源中提及的目的地 VM。</span><span class="sxs-lookup"><span data-stu-id="aee4c-114">The traffic from sourceNic VM will be mirrored to destination VM referred in vVirtualNetworkTap resource.</span></span>

## <span data-ttu-id="aee4c-115">參數</span><span class="sxs-lookup"><span data-stu-id="aee4c-115">PARAMETERS</span></span>

### <span data-ttu-id="aee4c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aee4c-116">-DefaultProfile</span></span>
<span data-ttu-id="aee4c-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="aee4c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aee4c-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="aee4c-118">-Name</span></span>
<span data-ttu-id="aee4c-119">點一下組配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="aee4c-119">Name of the tap configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aee4c-120">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="aee4c-120">-NetworkInterface</span></span>
<span data-ttu-id="aee4c-121">網路介面資源的參照。</span><span class="sxs-lookup"><span data-stu-id="aee4c-121">The reference of the network interface resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterface
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aee4c-122">-VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="aee4c-122">-VirtualNetworkTap</span></span>
<span data-ttu-id="aee4c-123">虛擬網路的參照點一下資源。</span><span class="sxs-lookup"><span data-stu-id="aee4c-123">The reference of the virtual network tap resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aee4c-124">-VirtualNetworkTapId</span><span class="sxs-lookup"><span data-stu-id="aee4c-124">-VirtualNetworkTapId</span></span>
<span data-ttu-id="aee4c-125">虛擬網路的參照點一下資源。</span><span class="sxs-lookup"><span data-stu-id="aee4c-125">The reference of the virtual network tap resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aee4c-126">-確認</span><span class="sxs-lookup"><span data-stu-id="aee4c-126">-Confirm</span></span>
<span data-ttu-id="aee4c-127">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="aee4c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aee4c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aee4c-128">-WhatIf</span></span>
<span data-ttu-id="aee4c-129">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="aee4c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aee4c-130">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="aee4c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aee4c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aee4c-131">CommonParameters</span></span>
<span data-ttu-id="aee4c-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="aee4c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aee4c-133">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="aee4c-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aee4c-134">輸入</span><span class="sxs-lookup"><span data-stu-id="aee4c-134">INPUTS</span></span>

### <span data-ttu-id="aee4c-135">Microsoft.Azure.Commands.Network.models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="aee4c-135">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

### <span data-ttu-id="aee4c-136">System.String</span><span class="sxs-lookup"><span data-stu-id="aee4c-136">System.String</span></span>

### <span data-ttu-id="aee4c-137">Microsoft.Azure.Commands.Network.models.PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="aee4c-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="aee4c-138">輸出</span><span class="sxs-lookup"><span data-stu-id="aee4c-138">OUTPUTS</span></span>

### <span data-ttu-id="aee4c-139">Microsoft.Azure.Commands.Network.models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="aee4c-139">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="aee4c-140">筆記</span><span class="sxs-lookup"><span data-stu-id="aee4c-140">NOTES</span></span>

## <span data-ttu-id="aee4c-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="aee4c-141">RELATED LINKS</span></span>

[<span data-ttu-id="aee4c-142">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="aee4c-142">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="aee4c-143">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="aee4c-143">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="aee4c-144">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="aee4c-144">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)
