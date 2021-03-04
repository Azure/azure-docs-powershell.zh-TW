---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 1c46cb01a2b30853248ca941cbb61d8b0429fc49
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902561"
---
# <span data-ttu-id="c0466-101">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="c0466-101">Get-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="c0466-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c0466-102">SYNOPSIS</span></span>
<span data-ttu-id="c0466-103">獲得點一下組組資源。</span><span class="sxs-lookup"><span data-stu-id="c0466-103">Gets a Tap configuration resource.</span></span>

## <span data-ttu-id="c0466-104">語法</span><span class="sxs-lookup"><span data-stu-id="c0466-104">SYNTAX</span></span>

### <span data-ttu-id="c0466-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c0466-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzNetworkInterfaceTapConfig -ResourceGroupName <String> -NetworkInterfaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0466-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0466-106">GetByResourceIdParameterSet</span></span>
```
Get-AzNetworkInterfaceTapConfig -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0466-107">描述</span><span class="sxs-lookup"><span data-stu-id="c0466-107">DESCRIPTION</span></span>
<span data-ttu-id="c0466-108">**Get-AzNetworkInterfaceTapConfig** Cmdlet 會取得指定資源群組的 Azure Tap Configuration、網路介面，並點一下資源群組和網路介面中的組名或點一下組配置的清單。</span><span class="sxs-lookup"><span data-stu-id="c0466-108">The **Get-AzNetworkInterfaceTapConfig** cmdlet gets an Azure Tap Configuration for a given resource group, network interface and tap configuration name or list of tap configurations in a resource group and network interface.</span></span>

## <span data-ttu-id="c0466-109">例子</span><span class="sxs-lookup"><span data-stu-id="c0466-109">EXAMPLES</span></span>

### <span data-ttu-id="c0466-110">範例 1：取得給定網路介面的所有點兩下組配置</span><span class="sxs-lookup"><span data-stu-id="c0466-110">Example 1: Get all tap configurations for a given network interface</span></span>
```
PS C:\> Get-AzNetworkInterfaceTapConfig -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName"
```

<span data-ttu-id="c0466-111">此命令會針對給定網路介面新增點一下組配置。</span><span class="sxs-lookup"><span data-stu-id="c0466-111">This command gets tap configurations added for the given network interface.</span></span>

### <span data-ttu-id="c0466-112">範例 2：取得已給予的點兩下組</span><span class="sxs-lookup"><span data-stu-id="c0466-112">Example 2: Get a given tap configuration</span></span>
```
PS C:\> Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
```

<span data-ttu-id="c0466-113">此命令會針對指定網路介面新增特定的點一下組配置。</span><span class="sxs-lookup"><span data-stu-id="c0466-113">This command gets specific tap configuration added for the given network interface.</span></span>

### <span data-ttu-id="c0466-114">範例 3：取得已給予的點兩下組</span><span class="sxs-lookup"><span data-stu-id="c0466-114">Example 3: Get a given tap configuration</span></span>
```
PS C:\> Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfig*"
```

<span data-ttu-id="c0466-115">此命令會針對指定網路介面新增點一下組配置，名稱以「tapconfig」開始。</span><span class="sxs-lookup"><span data-stu-id="c0466-115">This command gets tap configurations added for the given network interface with name starting with "tapconfig".</span></span>

## <span data-ttu-id="c0466-116">參數</span><span class="sxs-lookup"><span data-stu-id="c0466-116">PARAMETERS</span></span>

### <span data-ttu-id="c0466-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0466-117">-DefaultProfile</span></span>
<span data-ttu-id="c0466-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c0466-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0466-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="c0466-119">-Name</span></span>
<span data-ttu-id="c0466-120">特定點一下組組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c0466-120">Name of the specific tap configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="c0466-121">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="c0466-121">-NetworkInterfaceName</span></span>
<span data-ttu-id="c0466-122">網路介面名稱。</span><span class="sxs-lookup"><span data-stu-id="c0466-122">The Network Interface name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0466-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0466-123">-ResourceGroupName</span></span>
<span data-ttu-id="c0466-124">資源組名。</span><span class="sxs-lookup"><span data-stu-id="c0466-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0466-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0466-125">-ResourceId</span></span>
<span data-ttu-id="c0466-126">TapConfiguration 資源的 ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0466-126">ResourceId of the TapConfiguration resource</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0466-127">-確認</span><span class="sxs-lookup"><span data-stu-id="c0466-127">-Confirm</span></span>
<span data-ttu-id="c0466-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c0466-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0466-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0466-129">-WhatIf</span></span>
<span data-ttu-id="c0466-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c0466-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c0466-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c0466-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0466-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0466-132">CommonParameters</span></span>
<span data-ttu-id="c0466-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c0466-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0466-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c0466-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0466-135">輸入</span><span class="sxs-lookup"><span data-stu-id="c0466-135">INPUTS</span></span>

### <span data-ttu-id="c0466-136">System.String</span><span class="sxs-lookup"><span data-stu-id="c0466-136">System.String</span></span>

## <span data-ttu-id="c0466-137">輸出</span><span class="sxs-lookup"><span data-stu-id="c0466-137">OUTPUTS</span></span>

### <span data-ttu-id="c0466-138">Microsoft.Azure.Commands.Network.models.PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="c0466-138">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="c0466-139">筆記</span><span class="sxs-lookup"><span data-stu-id="c0466-139">NOTES</span></span>

## <span data-ttu-id="c0466-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="c0466-140">RELATED LINKS</span></span>

[<span data-ttu-id="c0466-141">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="c0466-141">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="c0466-142">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="c0466-142">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="c0466-143">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="c0466-143">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)
