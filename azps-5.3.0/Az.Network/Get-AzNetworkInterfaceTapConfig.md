---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: fa4c6db39de9f0d27fa80c4ee09e4decb319e2aa
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98287156"
---
# <span data-ttu-id="8baaf-101">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="8baaf-101">Get-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="8baaf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8baaf-102">SYNOPSIS</span></span>
<span data-ttu-id="8baaf-103">取得攻絲配置資源。</span><span class="sxs-lookup"><span data-stu-id="8baaf-103">Gets a Tap configuration resource.</span></span>

## <span data-ttu-id="8baaf-104">句法</span><span class="sxs-lookup"><span data-stu-id="8baaf-104">SYNTAX</span></span>

### <span data-ttu-id="8baaf-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="8baaf-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzNetworkInterfaceTapConfig -ResourceGroupName <String> -NetworkInterfaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8baaf-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8baaf-106">GetByResourceIdParameterSet</span></span>
```
Get-AzNetworkInterfaceTapConfig -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8baaf-107">說明</span><span class="sxs-lookup"><span data-stu-id="8baaf-107">DESCRIPTION</span></span>
<span data-ttu-id="8baaf-108">AzNetworkInterfaceTapConfig Cmdlet 會針對特定資源群組、網路介面，並在資源群組和網路介面中，針對指定的資源群組、網路介面，以及攻絲配置的清單， **取得** Azure 攻絲設定。</span><span class="sxs-lookup"><span data-stu-id="8baaf-108">The **Get-AzNetworkInterfaceTapConfig** cmdlet gets an Azure Tap Configuration for a given resource group, network interface and tap configuration name or list of tap configurations in a resource group and network interface.</span></span>

## <span data-ttu-id="8baaf-109">示例</span><span class="sxs-lookup"><span data-stu-id="8baaf-109">EXAMPLES</span></span>

### <span data-ttu-id="8baaf-110">範例1：取得指定網路介面的所有攻絲設定</span><span class="sxs-lookup"><span data-stu-id="8baaf-110">Example 1: Get all tap configurations for a given network interface</span></span>
```
PS C:\> Get-AzNetworkInterfaceTapConfig -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName"
```

<span data-ttu-id="8baaf-111">這個命令會針對指定的網路介面，分路器所新增的配置。</span><span class="sxs-lookup"><span data-stu-id="8baaf-111">This command gets tap configurations added for the given network interface.</span></span>

### <span data-ttu-id="8baaf-112">範例2：取得特定的攻絲配置</span><span class="sxs-lookup"><span data-stu-id="8baaf-112">Example 2: Get a given tap configuration</span></span>
```
PS C:\> Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
```

<span data-ttu-id="8baaf-113">這個命令會針對指定的網路介面，取得已新增的特定分路配置。</span><span class="sxs-lookup"><span data-stu-id="8baaf-113">This command gets specific tap configuration added for the given network interface.</span></span>

### <span data-ttu-id="8baaf-114">範例3：取得特定的攻絲配置</span><span class="sxs-lookup"><span data-stu-id="8baaf-114">Example 3: Get a given tap configuration</span></span>
```
PS C:\> Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfig*"
```

<span data-ttu-id="8baaf-115">這個命令會針對指定的網路介面（名稱開頭為 "tapconfig"），取得已新增的設定。</span><span class="sxs-lookup"><span data-stu-id="8baaf-115">This command gets tap configurations added for the given network interface with name starting with "tapconfig".</span></span>

## <span data-ttu-id="8baaf-116">參數</span><span class="sxs-lookup"><span data-stu-id="8baaf-116">PARAMETERS</span></span>

### <span data-ttu-id="8baaf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8baaf-117">-DefaultProfile</span></span>
<span data-ttu-id="8baaf-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8baaf-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8baaf-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="8baaf-119">-Name</span></span>
<span data-ttu-id="8baaf-120">特定攻絲配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="8baaf-120">Name of the specific tap configuration.</span></span>

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

### <span data-ttu-id="8baaf-121">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="8baaf-121">-NetworkInterfaceName</span></span>
<span data-ttu-id="8baaf-122">網路介面名稱。</span><span class="sxs-lookup"><span data-stu-id="8baaf-122">The Network Interface name.</span></span>

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

### <span data-ttu-id="8baaf-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8baaf-123">-ResourceGroupName</span></span>
<span data-ttu-id="8baaf-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8baaf-124">The resource group name.</span></span>

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

### <span data-ttu-id="8baaf-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8baaf-125">-ResourceId</span></span>
<span data-ttu-id="8baaf-126">TapConfiguration 資源的 ResourceId</span><span class="sxs-lookup"><span data-stu-id="8baaf-126">ResourceId of the TapConfiguration resource</span></span>

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

### <span data-ttu-id="8baaf-127">-確認</span><span class="sxs-lookup"><span data-stu-id="8baaf-127">-Confirm</span></span>
<span data-ttu-id="8baaf-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8baaf-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8baaf-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8baaf-129">-WhatIf</span></span>
<span data-ttu-id="8baaf-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8baaf-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8baaf-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8baaf-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8baaf-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8baaf-132">CommonParameters</span></span>
<span data-ttu-id="8baaf-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8baaf-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8baaf-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8baaf-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8baaf-135">輸入</span><span class="sxs-lookup"><span data-stu-id="8baaf-135">INPUTS</span></span>

### <span data-ttu-id="8baaf-136">System.object</span><span class="sxs-lookup"><span data-stu-id="8baaf-136">System.String</span></span>

## <span data-ttu-id="8baaf-137">輸出</span><span class="sxs-lookup"><span data-stu-id="8baaf-137">OUTPUTS</span></span>

### <span data-ttu-id="8baaf-138">PSNetworkInterfaceTapConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8baaf-138">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="8baaf-139">筆記</span><span class="sxs-lookup"><span data-stu-id="8baaf-139">NOTES</span></span>

## <span data-ttu-id="8baaf-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="8baaf-140">RELATED LINKS</span></span>

[<span data-ttu-id="8baaf-141">附加 AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="8baaf-141">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="8baaf-142">移除-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="8baaf-142">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="8baaf-143">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="8baaf-143">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)
