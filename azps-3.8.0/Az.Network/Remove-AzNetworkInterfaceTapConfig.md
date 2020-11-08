---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Remove-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 52fc2a3c84c70d52c173bc256ca2b0d952307e91
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965460"
---
# <span data-ttu-id="e12d5-101">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="e12d5-101">Remove-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="e12d5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e12d5-102">SYNOPSIS</span></span>
<span data-ttu-id="e12d5-103">從指定的網路介面移除攻絲配置</span><span class="sxs-lookup"><span data-stu-id="e12d5-103">Removes a tap configuration from given network interface</span></span>

## <span data-ttu-id="e12d5-104">句法</span><span class="sxs-lookup"><span data-stu-id="e12d5-104">SYNTAX</span></span>

### <span data-ttu-id="e12d5-105">RemoveByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e12d5-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzNetworkInterfaceTapConfig -ResourceGroupName <String> -NetworkInterfaceName <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e12d5-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e12d5-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzNetworkInterfaceTapConfig -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e12d5-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e12d5-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzNetworkInterfaceTapConfig -InputObject <PSNetworkInterfaceTapConfiguration> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e12d5-108">說明</span><span class="sxs-lookup"><span data-stu-id="e12d5-108">DESCRIPTION</span></span>
<span data-ttu-id="e12d5-109">**AzNetworkInterfaceTapConfig** Cmdlet 會從網路介面清單中移除 Azure 分路器配置。</span><span class="sxs-lookup"><span data-stu-id="e12d5-109">The **Remove-AzNetworkInterfaceTapConfig** cmdlet removes an Azure tap configuration from a network interface list.</span></span>

## <span data-ttu-id="e12d5-110">示例</span><span class="sxs-lookup"><span data-stu-id="e12d5-110">EXAMPLES</span></span>

### <span data-ttu-id="e12d5-111">範例1：移除攻絲設定</span><span class="sxs-lookup"><span data-stu-id="e12d5-111">Example 1: Remove a tap configuration</span></span>
```
PS C:\>Remove-AzNetworkInterfaceTapConfig -Name "TapConfiguration" -NetworkInterfaceName "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="e12d5-112">這個命令會從資源群組 ResourceGroup1 中移除 NetworkInterface1 的 TapConfiguration。</span><span class="sxs-lookup"><span data-stu-id="e12d5-112">This command removes the TapConfiguration from NetworkInterface1 in a resource group ResourceGroup1.</span></span>
<span data-ttu-id="e12d5-113">由於不使用 *Force* 參數，系統會提示使用者確認此動作。</span><span class="sxs-lookup"><span data-stu-id="e12d5-113">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="e12d5-114">範例2：移除網路介面</span><span class="sxs-lookup"><span data-stu-id="e12d5-114">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzNetworkInterfaceTapConfig -Name "TapConfiguration" -NetworkInterfaceName "NetworkInterface1" -ResourceGroup "ResourceGroup1" | Remove-AzNetworkInterfaceTapConfig -Force
```

<span data-ttu-id="e12d5-115">這個命令會從資源群組 ResourceGroup1 中移除 NetworkInterface1 的 TapConfiguration。</span><span class="sxs-lookup"><span data-stu-id="e12d5-115">This command removes the TapConfiguration from NetworkInterface1 in a resource group ResourceGroup1.</span></span>
<span data-ttu-id="e12d5-116">因為使用 *Force* 參數，系統不會提示使用者確認。</span><span class="sxs-lookup"><span data-stu-id="e12d5-116">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="e12d5-117">參數</span><span class="sxs-lookup"><span data-stu-id="e12d5-117">PARAMETERS</span></span>

### <span data-ttu-id="e12d5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e12d5-118">-DefaultProfile</span></span>
<span data-ttu-id="e12d5-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e12d5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e12d5-120">-Force</span><span class="sxs-lookup"><span data-stu-id="e12d5-120">-Force</span></span>
<span data-ttu-id="e12d5-121">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="e12d5-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="e12d5-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e12d5-122">-InputObject</span></span>
<span data-ttu-id="e12d5-123">NetworkInterfaceTapConfig 的參照。</span><span class="sxs-lookup"><span data-stu-id="e12d5-123">Reference to NetworkInterfaceTapConfig.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e12d5-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="e12d5-124">-Name</span></span>
<span data-ttu-id="e12d5-125">虛擬網路對等名稱。</span><span class="sxs-lookup"><span data-stu-id="e12d5-125">The virtual network peering name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e12d5-126">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="e12d5-126">-NetworkInterfaceName</span></span>
<span data-ttu-id="e12d5-127">虛擬網路名稱。</span><span class="sxs-lookup"><span data-stu-id="e12d5-127">The virtual network name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e12d5-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e12d5-128">-PassThru</span></span>
<span data-ttu-id="e12d5-129">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="e12d5-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e12d5-130">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="e12d5-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e12d5-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e12d5-131">-ResourceGroupName</span></span>
<span data-ttu-id="e12d5-132">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e12d5-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e12d5-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e12d5-133">-ResourceId</span></span>
<span data-ttu-id="e12d5-134">NetworkInterfaceTapConfig 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e12d5-134">NetworkInterfaceTapConfig resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e12d5-135">-確認</span><span class="sxs-lookup"><span data-stu-id="e12d5-135">-Confirm</span></span>
<span data-ttu-id="e12d5-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e12d5-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e12d5-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e12d5-137">-WhatIf</span></span>
<span data-ttu-id="e12d5-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e12d5-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e12d5-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e12d5-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e12d5-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e12d5-140">CommonParameters</span></span>
<span data-ttu-id="e12d5-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e12d5-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e12d5-142">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e12d5-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e12d5-143">輸入</span><span class="sxs-lookup"><span data-stu-id="e12d5-143">INPUTS</span></span>

### <span data-ttu-id="e12d5-144">System.object</span><span class="sxs-lookup"><span data-stu-id="e12d5-144">System.String</span></span>

### <span data-ttu-id="e12d5-145">PSNetworkInterfaceTapConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e12d5-145">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="e12d5-146">輸出</span><span class="sxs-lookup"><span data-stu-id="e12d5-146">OUTPUTS</span></span>

### <span data-ttu-id="e12d5-147">PSNetworkInterface 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e12d5-147">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="e12d5-148">筆記</span><span class="sxs-lookup"><span data-stu-id="e12d5-148">NOTES</span></span>

## <span data-ttu-id="e12d5-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="e12d5-149">RELATED LINKS</span></span>

[<span data-ttu-id="e12d5-150">附加 AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="e12d5-150">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="e12d5-151">AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="e12d5-151">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="e12d5-152">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="e12d5-152">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)