---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkVirtualAppliance.md
ms.openlocfilehash: 9b3991a24430afa74853f742bffa12b772dbeaf2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435765"
---
# <span data-ttu-id="db6be-101">New-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="db6be-101">New-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="db6be-102">摘要</span><span class="sxs-lookup"><span data-stu-id="db6be-102">SYNOPSIS</span></span>
<span data-ttu-id="db6be-103">建立網路虛擬裝置資源。</span><span class="sxs-lookup"><span data-stu-id="db6be-103">Create a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="db6be-104">句法</span><span class="sxs-lookup"><span data-stu-id="db6be-104">SYNTAX</span></span>

### <span data-ttu-id="db6be-105">ResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="db6be-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzNetworkVirtualAppliance -Name <String> -ResourceGroupName <String> -Location <String>
 -VirtualHubId <String> -Sku <PSVirtualApplianceSkuProperties> -VirtualApplianceAsn <Int32>
 [-Identity <PSManagedServiceIdentity>] [-BootStrapConfigurationBlob <String[]>]
 [-CloudInitConfigurationBlob <String[]>] [-CloudInitConfiguration <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db6be-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="db6be-106">ResourceIdParameterSet</span></span>
```
New-AzNetworkVirtualAppliance -ResourceId <String> -Location <String> -VirtualHubId <String>
 -Sku <PSVirtualApplianceSkuProperties> -VirtualApplianceAsn <Int32> [-Identity <PSManagedServiceIdentity>]
 [-BootStrapConfigurationBlob <String[]>] [-CloudInitConfigurationBlob <String[]>]
 [-CloudInitConfiguration <String>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db6be-107">說明</span><span class="sxs-lookup"><span data-stu-id="db6be-107">DESCRIPTION</span></span>
<span data-ttu-id="db6be-108">New-AzNetworkVirtualAppliance 命令會在 Azure 中建立網路虛擬裝置資源。</span><span class="sxs-lookup"><span data-stu-id="db6be-108">The New-AzNetworkVirtualAppliance command creates a Network Virtual Appliance resource in Azure.</span></span>

## <span data-ttu-id="db6be-109">示例</span><span class="sxs-lookup"><span data-stu-id="db6be-109">EXAMPLES</span></span>

### <span data-ttu-id="db6be-110">範例1</span><span class="sxs-lookup"><span data-stu-id="db6be-110">Example 1</span></span>
```powershell
PS C:\> $sku=New-AzVirtualApplianceSkuProperty -VendorName "barracudasdwanrelease" -BundledScaleUnit 1 -MarketPlaceVersion 'latest'
PS C:\> $hub=Get-AzVirtualHub -ResourceGroupName testrg -Name hub
PS C:\> $nva=New-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva -Location eastus2 -VirtualApplianceAsn 1270 -VirtualHubId $hub.Id -Sku $sku -CloudInitConfiguration "echo Hello World!"

```

<span data-ttu-id="db6be-111">在 [資源群組： testrg] 中建立新的網路虛擬裝置資源。</span><span class="sxs-lookup"><span data-stu-id="db6be-111">Creates a new Network Virtual Appliance resource in resource group: testrg.</span></span>

## <span data-ttu-id="db6be-112">參數</span><span class="sxs-lookup"><span data-stu-id="db6be-112">PARAMETERS</span></span>

### <span data-ttu-id="db6be-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="db6be-113">-AsJob</span></span>
<span data-ttu-id="db6be-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db6be-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="db6be-115">-BootStrapConfigurationBlob</span><span class="sxs-lookup"><span data-stu-id="db6be-115">-BootStrapConfigurationBlob</span></span>
<span data-ttu-id="db6be-116">啟動配置 blob URL。</span><span class="sxs-lookup"><span data-stu-id="db6be-116">The Bootstrap configuration blob URL.</span></span>

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

### <span data-ttu-id="db6be-117">-CloudInitConfiguration</span><span class="sxs-lookup"><span data-stu-id="db6be-117">-CloudInitConfiguration</span></span>
<span data-ttu-id="db6be-118">純文字格式的 Cloudinit 配置。</span><span class="sxs-lookup"><span data-stu-id="db6be-118">The Cloudinit configuration as plain text.</span></span>

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

### <span data-ttu-id="db6be-119">-CloudInitConfigurationBlob</span><span class="sxs-lookup"><span data-stu-id="db6be-119">-CloudInitConfigurationBlob</span></span>
<span data-ttu-id="db6be-120">Cloudinit 配置 blob 儲存 URL。</span><span class="sxs-lookup"><span data-stu-id="db6be-120">The Cloudinit configuration blob storage URL.</span></span>

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

### <span data-ttu-id="db6be-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db6be-121">-DefaultProfile</span></span>
<span data-ttu-id="db6be-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="db6be-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db6be-123">-Force</span><span class="sxs-lookup"><span data-stu-id="db6be-123">-Force</span></span>
<span data-ttu-id="db6be-124">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="db6be-124">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="db6be-125">身分識別</span><span class="sxs-lookup"><span data-stu-id="db6be-125">-Identity</span></span>
<span data-ttu-id="db6be-126">受管理的身分識別。</span><span class="sxs-lookup"><span data-stu-id="db6be-126">The Managed identity.</span></span>

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

### <span data-ttu-id="db6be-127">-位置</span><span class="sxs-lookup"><span data-stu-id="db6be-127">-Location</span></span>
<span data-ttu-id="db6be-128">公用 IP 位址的位置。</span><span class="sxs-lookup"><span data-stu-id="db6be-128">The public IP address location.</span></span>

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

### <span data-ttu-id="db6be-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="db6be-129">-Name</span></span>
<span data-ttu-id="db6be-130">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="db6be-130">The resource name.</span></span>

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

### <span data-ttu-id="db6be-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db6be-131">-ResourceGroupName</span></span>
<span data-ttu-id="db6be-132">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="db6be-132">The resource group name.</span></span>

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

### <span data-ttu-id="db6be-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="db6be-133">-ResourceId</span></span>
<span data-ttu-id="db6be-134">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="db6be-134">The resource Id.</span></span>

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

### <span data-ttu-id="db6be-135">-Sku</span><span class="sxs-lookup"><span data-stu-id="db6be-135">-Sku</span></span>
<span data-ttu-id="db6be-136">虛擬裝置的 Sku。</span><span class="sxs-lookup"><span data-stu-id="db6be-136">The Sku of the Virtual Appliance.</span></span>

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

### <span data-ttu-id="db6be-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="db6be-137">-Tag</span></span>
<span data-ttu-id="db6be-138">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="db6be-138">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="db6be-139">-VirtualApplianceAsn</span><span class="sxs-lookup"><span data-stu-id="db6be-139">-VirtualApplianceAsn</span></span>
<span data-ttu-id="db6be-140">虛擬裝置的 ASN 編號。</span><span class="sxs-lookup"><span data-stu-id="db6be-140">The ASN number of the Virtual Appliance.</span></span>

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

### <span data-ttu-id="db6be-141">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="db6be-141">-VirtualHubId</span></span>
<span data-ttu-id="db6be-142">虛擬中樞的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="db6be-142">The Resource Id of the Virtual Hub.</span></span>

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

### <span data-ttu-id="db6be-143">-確認</span><span class="sxs-lookup"><span data-stu-id="db6be-143">-Confirm</span></span>
<span data-ttu-id="db6be-144">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="db6be-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db6be-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db6be-145">-WhatIf</span></span>
<span data-ttu-id="db6be-146">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="db6be-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db6be-147">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="db6be-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db6be-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db6be-148">CommonParameters</span></span>
<span data-ttu-id="db6be-149">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="db6be-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db6be-150">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="db6be-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db6be-151">輸入</span><span class="sxs-lookup"><span data-stu-id="db6be-151">INPUTS</span></span>

### <span data-ttu-id="db6be-152">System.object</span><span class="sxs-lookup"><span data-stu-id="db6be-152">System.String</span></span>

### <span data-ttu-id="db6be-153">PSVirtualApplianceSkuProperties 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="db6be-153">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span></span>

### <span data-ttu-id="db6be-154">System.object</span><span class="sxs-lookup"><span data-stu-id="db6be-154">System.Int32</span></span>

### <span data-ttu-id="db6be-155">PSManagedServiceIdentity 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="db6be-155">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

### <span data-ttu-id="db6be-156">System.object []</span><span class="sxs-lookup"><span data-stu-id="db6be-156">System.String[]</span></span>

### <span data-ttu-id="db6be-157">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="db6be-157">System.Collections.Hashtable</span></span>

## <span data-ttu-id="db6be-158">輸出</span><span class="sxs-lookup"><span data-stu-id="db6be-158">OUTPUTS</span></span>

### <span data-ttu-id="db6be-159">PSNetworkVirtualAppliance 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="db6be-159">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="db6be-160">筆記</span><span class="sxs-lookup"><span data-stu-id="db6be-160">NOTES</span></span>

## <span data-ttu-id="db6be-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="db6be-161">RELATED LINKS</span></span>
