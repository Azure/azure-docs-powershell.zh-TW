---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkVirtualAppliance.md
ms.openlocfilehash: 3f95ad6b11e8ddf7baaf5bcdf312ec172a9d397a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916516"
---
# <span data-ttu-id="1dac1-101">New-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="1dac1-101">New-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="1dac1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1dac1-102">SYNOPSIS</span></span>
<span data-ttu-id="1dac1-103">建立網路虛擬裝置資源。</span><span class="sxs-lookup"><span data-stu-id="1dac1-103">Create a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="1dac1-104">語法</span><span class="sxs-lookup"><span data-stu-id="1dac1-104">SYNTAX</span></span>

### <span data-ttu-id="1dac1-105">ResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1dac1-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzNetworkVirtualAppliance -Name <String> -ResourceGroupName <String> -Location <String>
 -VirtualHubId <String> -Sku <PSVirtualApplianceSkuProperties> -VirtualApplianceAsn <Int32>
 [-Identity <PSManagedServiceIdentity>] [-BootStrapConfigurationBlob <String[]>]
 [-CloudInitConfigurationBlob <String[]>] [-CloudInitConfiguration <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dac1-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1dac1-106">ResourceIdParameterSet</span></span>
```
New-AzNetworkVirtualAppliance -ResourceId <String> -Location <String> -VirtualHubId <String>
 -Sku <PSVirtualApplianceSkuProperties> -VirtualApplianceAsn <Int32> [-Identity <PSManagedServiceIdentity>]
 [-BootStrapConfigurationBlob <String[]>] [-CloudInitConfigurationBlob <String[]>]
 [-CloudInitConfiguration <String>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1dac1-107">描述</span><span class="sxs-lookup"><span data-stu-id="1dac1-107">DESCRIPTION</span></span>
<span data-ttu-id="1dac1-108">命令New-AzNetworkVirtualAppliance在 Azure 中建立網路虛擬裝置資源。</span><span class="sxs-lookup"><span data-stu-id="1dac1-108">The New-AzNetworkVirtualAppliance command creates a Network Virtual Appliance resource in Azure.</span></span>

## <span data-ttu-id="1dac1-109">例子</span><span class="sxs-lookup"><span data-stu-id="1dac1-109">EXAMPLES</span></span>

### <span data-ttu-id="1dac1-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="1dac1-110">Example 1</span></span>
```powershell
PS C:\> $sku=New-AzVirtualApplianceSkuProperty -VendorName "barracudasdwanrelease" -BundledScaleUnit 1 -MarketPlaceVersion 'latest'
PS C:\> $hub=Get-AzVirtualHub -ResourceGroupName testrg -Name hub
PS C:\> $nva=New-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva -Location eastus2 -VirtualApplianceAsn 1270 -VirtualHubId $hub.Id -Sku $sku -CloudInitConfiguration "echo Hello World!"

```

<span data-ttu-id="1dac1-111">在資源群組中建立新網路虛擬裝置資源：testrg。</span><span class="sxs-lookup"><span data-stu-id="1dac1-111">Creates a new Network Virtual Appliance resource in resource group: testrg.</span></span>

## <span data-ttu-id="1dac1-112">參數</span><span class="sxs-lookup"><span data-stu-id="1dac1-112">PARAMETERS</span></span>

### <span data-ttu-id="1dac1-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1dac1-113">-AsJob</span></span>
<span data-ttu-id="1dac1-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1dac1-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1dac1-115">-BootStrapConfigurationBlob</span><span class="sxs-lookup"><span data-stu-id="1dac1-115">-BootStrapConfigurationBlob</span></span>
<span data-ttu-id="1dac1-116">Bootstrap 組塊 URL。</span><span class="sxs-lookup"><span data-stu-id="1dac1-116">The Bootstrap configuration blob URL.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dac1-117">-CloudInitConfiguration</span><span class="sxs-lookup"><span data-stu-id="1dac1-117">-CloudInitConfiguration</span></span>
<span data-ttu-id="1dac1-118">Cloudinit 組態為純文字。</span><span class="sxs-lookup"><span data-stu-id="1dac1-118">The Cloudinit configuration as plain text.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dac1-119">-CloudInitConfigurationBlob</span><span class="sxs-lookup"><span data-stu-id="1dac1-119">-CloudInitConfigurationBlob</span></span>
<span data-ttu-id="1dac1-120">Cloudinit 組態 Blob 儲存 URL。</span><span class="sxs-lookup"><span data-stu-id="1dac1-120">The Cloudinit configuration blob storage URL.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dac1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dac1-121">-DefaultProfile</span></span>
<span data-ttu-id="1dac1-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1dac1-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1dac1-123">-強制</span><span class="sxs-lookup"><span data-stu-id="1dac1-123">-Force</span></span>
<span data-ttu-id="1dac1-124">如果您想要覆寫資源，請勿要求確認</span><span class="sxs-lookup"><span data-stu-id="1dac1-124">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="1dac1-125">-身分識別</span><span class="sxs-lookup"><span data-stu-id="1dac1-125">-Identity</span></span>
<span data-ttu-id="1dac1-126">受管理的身分識別。</span><span class="sxs-lookup"><span data-stu-id="1dac1-126">The Managed identity.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dac1-127">-位置</span><span class="sxs-lookup"><span data-stu-id="1dac1-127">-Location</span></span>
<span data-ttu-id="1dac1-128">公用 IP 位址位置。</span><span class="sxs-lookup"><span data-stu-id="1dac1-128">The public IP address location.</span></span>

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

### <span data-ttu-id="1dac1-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="1dac1-129">-Name</span></span>
<span data-ttu-id="1dac1-130">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="1dac1-130">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dac1-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dac1-131">-ResourceGroupName</span></span>
<span data-ttu-id="1dac1-132">資源組名。</span><span class="sxs-lookup"><span data-stu-id="1dac1-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dac1-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1dac1-133">-ResourceId</span></span>
<span data-ttu-id="1dac1-134">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="1dac1-134">The resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dac1-135">-SKU</span><span class="sxs-lookup"><span data-stu-id="1dac1-135">-Sku</span></span>
<span data-ttu-id="1dac1-136">虛擬裝置 SKU。</span><span class="sxs-lookup"><span data-stu-id="1dac1-136">The Sku of the Virtual Appliance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dac1-137">-標記</span><span class="sxs-lookup"><span data-stu-id="1dac1-137">-Tag</span></span>
<span data-ttu-id="1dac1-138">代表資源標記的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="1dac1-138">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="1dac1-139">-VirtualApplianceAsn</span><span class="sxs-lookup"><span data-stu-id="1dac1-139">-VirtualApplianceAsn</span></span>
<span data-ttu-id="1dac1-140">虛擬裝置機的 ASN 編號。</span><span class="sxs-lookup"><span data-stu-id="1dac1-140">The ASN number of the Virtual Appliance.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dac1-141">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="1dac1-141">-VirtualHubId</span></span>
<span data-ttu-id="1dac1-142">虛擬中樞的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="1dac1-142">The Resource Id of the Virtual Hub.</span></span>

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

### <span data-ttu-id="1dac1-143">-確認</span><span class="sxs-lookup"><span data-stu-id="1dac1-143">-Confirm</span></span>
<span data-ttu-id="1dac1-144">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="1dac1-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dac1-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dac1-145">-WhatIf</span></span>
<span data-ttu-id="1dac1-146">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1dac1-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1dac1-147">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1dac1-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1dac1-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dac1-148">CommonParameters</span></span>
<span data-ttu-id="1dac1-149">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1dac1-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dac1-150">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1dac1-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dac1-151">輸入</span><span class="sxs-lookup"><span data-stu-id="1dac1-151">INPUTS</span></span>

### <span data-ttu-id="1dac1-152">System.String</span><span class="sxs-lookup"><span data-stu-id="1dac1-152">System.String</span></span>

### <span data-ttu-id="1dac1-153">Microsoft.Azure.Commands.Network.models.PSVirtualApplianceSkuProperties</span><span class="sxs-lookup"><span data-stu-id="1dac1-153">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span></span>

### <span data-ttu-id="1dac1-154">System.Int32</span><span class="sxs-lookup"><span data-stu-id="1dac1-154">System.Int32</span></span>

### <span data-ttu-id="1dac1-155">Microsoft.Azure.Commands.Network.models.PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="1dac1-155">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

### <span data-ttu-id="1dac1-156">System.String[]</span><span class="sxs-lookup"><span data-stu-id="1dac1-156">System.String[]</span></span>

### <span data-ttu-id="1dac1-157">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="1dac1-157">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1dac1-158">輸出</span><span class="sxs-lookup"><span data-stu-id="1dac1-158">OUTPUTS</span></span>

### <span data-ttu-id="1dac1-159">Microsoft.Azure.Commands.Network.models.PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="1dac1-159">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="1dac1-160">筆記</span><span class="sxs-lookup"><span data-stu-id="1dac1-160">NOTES</span></span>

## <span data-ttu-id="1dac1-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="1dac1-161">RELATED LINKS</span></span>
