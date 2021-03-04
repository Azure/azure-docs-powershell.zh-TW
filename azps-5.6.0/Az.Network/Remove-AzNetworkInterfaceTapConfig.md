---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/Remove-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 54468717f979188d31d6ba318556be87c37e50b9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912662"
---
# <span data-ttu-id="2786a-101">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="2786a-101">Remove-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="2786a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2786a-102">SYNOPSIS</span></span>
<span data-ttu-id="2786a-103">移除來自給定網路介面的點一下組配置</span><span class="sxs-lookup"><span data-stu-id="2786a-103">Removes a tap configuration from given network interface</span></span>

## <span data-ttu-id="2786a-104">語法</span><span class="sxs-lookup"><span data-stu-id="2786a-104">SYNTAX</span></span>

### <span data-ttu-id="2786a-105">RemoveByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="2786a-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzNetworkInterfaceTapConfig -ResourceGroupName <String> -NetworkInterfaceName <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2786a-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2786a-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzNetworkInterfaceTapConfig -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2786a-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2786a-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzNetworkInterfaceTapConfig -InputObject <PSNetworkInterfaceTapConfiguration> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2786a-108">描述</span><span class="sxs-lookup"><span data-stu-id="2786a-108">DESCRIPTION</span></span>
<span data-ttu-id="2786a-109">**Remove-AzNetworkInterfaceTapConfig** Cmdlet 會從網路介面清單中移除 Azure 點一下組式。</span><span class="sxs-lookup"><span data-stu-id="2786a-109">The **Remove-AzNetworkInterfaceTapConfig** cmdlet removes an Azure tap configuration from a network interface list.</span></span>

## <span data-ttu-id="2786a-110">例子</span><span class="sxs-lookup"><span data-stu-id="2786a-110">EXAMPLES</span></span>

### <span data-ttu-id="2786a-111">範例 1：移除點一下組</span><span class="sxs-lookup"><span data-stu-id="2786a-111">Example 1: Remove a tap configuration</span></span>
```
PS C:\>Remove-AzNetworkInterfaceTapConfig -Name "TapConfiguration" -NetworkInterfaceName "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="2786a-112">此命令會從資源群組 ResourceGroup1 中的 NetworkInterface1 移除 TapConfiguration。</span><span class="sxs-lookup"><span data-stu-id="2786a-112">This command removes the TapConfiguration from NetworkInterface1 in a resource group ResourceGroup1.</span></span>
<span data-ttu-id="2786a-113">由於 *不會使用 Force* 參數，因此系統會提示使用者確認此動作。</span><span class="sxs-lookup"><span data-stu-id="2786a-113">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="2786a-114">範例 2：移除網路介面</span><span class="sxs-lookup"><span data-stu-id="2786a-114">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzNetworkInterfaceTapConfig -Name "TapConfiguration" -NetworkInterfaceName "NetworkInterface1" -ResourceGroup "ResourceGroup1" | Remove-AzNetworkInterfaceTapConfig -Force
```

<span data-ttu-id="2786a-115">此命令會從資源群組 ResourceGroup1 中的 NetworkInterface1 移除 TapConfiguration。</span><span class="sxs-lookup"><span data-stu-id="2786a-115">This command removes the TapConfiguration from NetworkInterface1 in a resource group ResourceGroup1.</span></span>
<span data-ttu-id="2786a-116">由於 *使用 Force* 參數，因此系統不會提示使用者確認。</span><span class="sxs-lookup"><span data-stu-id="2786a-116">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="2786a-117">參數</span><span class="sxs-lookup"><span data-stu-id="2786a-117">PARAMETERS</span></span>

### <span data-ttu-id="2786a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2786a-118">-DefaultProfile</span></span>
<span data-ttu-id="2786a-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2786a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2786a-120">-強制</span><span class="sxs-lookup"><span data-stu-id="2786a-120">-Force</span></span>
<span data-ttu-id="2786a-121">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="2786a-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2786a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2786a-122">-InputObject</span></span>
<span data-ttu-id="2786a-123">NetworkInterfaceTapConfig 的參照。</span><span class="sxs-lookup"><span data-stu-id="2786a-123">Reference to NetworkInterfaceTapConfig.</span></span>

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

### <span data-ttu-id="2786a-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="2786a-124">-Name</span></span>
<span data-ttu-id="2786a-125">虛擬網路對等名稱。</span><span class="sxs-lookup"><span data-stu-id="2786a-125">The virtual network peering name.</span></span>

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

### <span data-ttu-id="2786a-126">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="2786a-126">-NetworkInterfaceName</span></span>
<span data-ttu-id="2786a-127">虛擬網路名稱。</span><span class="sxs-lookup"><span data-stu-id="2786a-127">The virtual network name.</span></span>

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

### <span data-ttu-id="2786a-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2786a-128">-PassThru</span></span>
<span data-ttu-id="2786a-129">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="2786a-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2786a-130">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="2786a-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2786a-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2786a-131">-ResourceGroupName</span></span>
<span data-ttu-id="2786a-132">資源組名。</span><span class="sxs-lookup"><span data-stu-id="2786a-132">The resource group name.</span></span>

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

### <span data-ttu-id="2786a-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2786a-133">-ResourceId</span></span>
<span data-ttu-id="2786a-134">NetworkInterfaceTapConfig 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="2786a-134">NetworkInterfaceTapConfig resource id.</span></span>

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

### <span data-ttu-id="2786a-135">-確認</span><span class="sxs-lookup"><span data-stu-id="2786a-135">-Confirm</span></span>
<span data-ttu-id="2786a-136">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2786a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2786a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2786a-137">-WhatIf</span></span>
<span data-ttu-id="2786a-138">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2786a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2786a-139">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2786a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2786a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2786a-140">CommonParameters</span></span>
<span data-ttu-id="2786a-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2786a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2786a-142">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="2786a-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2786a-143">輸入</span><span class="sxs-lookup"><span data-stu-id="2786a-143">INPUTS</span></span>

### <span data-ttu-id="2786a-144">System.String</span><span class="sxs-lookup"><span data-stu-id="2786a-144">System.String</span></span>

### <span data-ttu-id="2786a-145">Microsoft.Azure.Commands.Network.models.PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="2786a-145">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="2786a-146">輸出</span><span class="sxs-lookup"><span data-stu-id="2786a-146">OUTPUTS</span></span>

### <span data-ttu-id="2786a-147">Microsoft.Azure.Commands.Network.models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="2786a-147">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="2786a-148">筆記</span><span class="sxs-lookup"><span data-stu-id="2786a-148">NOTES</span></span>

## <span data-ttu-id="2786a-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="2786a-149">RELATED LINKS</span></span>

[<span data-ttu-id="2786a-150">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="2786a-150">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="2786a-151">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="2786a-151">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="2786a-152">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="2786a-152">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)
