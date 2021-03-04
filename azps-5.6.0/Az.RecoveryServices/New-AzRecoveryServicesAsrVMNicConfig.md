---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/new-azrecoveryservicesasrvmnicconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrVMNicConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrVMNicConfig.md
ms.openlocfilehash: f28c1f8abf0da8363a860c9daffff9fc98a9a9d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902273"
---
# <span data-ttu-id="50710-101">New-AzRecoveryServicesAsrVMNicConfig</span><span class="sxs-lookup"><span data-stu-id="50710-101">New-AzRecoveryServicesAsrVMNicConfig</span></span>

## <span data-ttu-id="50710-102">簡介</span><span class="sxs-lookup"><span data-stu-id="50710-102">SYNOPSIS</span></span>
<span data-ttu-id="50710-103">建立包含容錯移轉的 ASR NIC 設定檔，並測試容錯移轉相關組配置詳細資料。</span><span class="sxs-lookup"><span data-stu-id="50710-103">Creates an ASR NIC config that contains the failover and test failover related configuration details.</span></span>

## <span data-ttu-id="50710-104">語法</span><span class="sxs-lookup"><span data-stu-id="50710-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrVMNicConfig -NicId <String> -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-RecoveryVMNetworkId <String>] [-RecoveryNicName <String>] [-RecoveryNicResourceGroupName <String>]
 [-ReuseExistingNic] [-RecoveryVMSubnetName <String>] [-RecoveryNetworkSecurityGroupId <String>]
 [-EnableAcceleratedNetworkingOnRecovery] [-RecoveryNicStaticIPAddress <String>]
 [-RecoveryPublicIPAddressId <String>] [-RecoveryLBBackendAddressPoolId <String[]>] [-TfoVMNetworkId <String>]
 [-TfoNicName <String>] [-TfoNicResourceGroupName <String>] [-TfoReuseExistingNic] [-TfoVMSubnetName <String>]
 [-TfoNetworkSecurityGroupId <String>] [-EnableAcceleratedNetworkingOnTfo] [-TfoNicStaticIPAddress <String>]
 [-TfoPublicIPAddressId <String>] [-TfoLBBackendAddressPoolId <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50710-105">描述</span><span class="sxs-lookup"><span data-stu-id="50710-105">DESCRIPTION</span></span>
<span data-ttu-id="50710-106">**New-AzRecoveryServicesAsrNICNicConfig** Cmdlet 會建立一個 ASR NIC 設定檔物件，其中包含容錯移轉和測試容錯移轉相關詳細資料。</span><span class="sxs-lookup"><span data-stu-id="50710-106">The **New-AzRecoveryServicesAsrVMNicConfig** cmdlet creates an ASR NIC config object that contains the failover and test failover related details.</span></span> <span data-ttu-id="50710-107">如果未傳遞任何資訊，會從複製受保護的專案挑選對應的值，以避免這些值更新為 Null。</span><span class="sxs-lookup"><span data-stu-id="50710-107">In case any information is not passed, the corresponding values are picked from the replication protected item to avoid these values being updated to null.</span></span>

## <span data-ttu-id="50710-108">例子</span><span class="sxs-lookup"><span data-stu-id="50710-108">EXAMPLES</span></span>

### <span data-ttu-id="50710-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="50710-109">Example 1</span></span>
```powershell
PS C:\> $nicConfig = New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -ReplicationProtectedItem $Rpi -RecoveryVMNetworkId $recoveryNetworkId -RecoveryVMSubnetName $recoverySubnetName -RecoveryNicStaticIPAddress "10.0.0.1" `
    -TfoVMNetworkId $tfoNetworkId -TfoVMSubnetName $tfoSubnetName -TfoNicStaticIPAddress "10.0.1.1"
```

<span data-ttu-id="50710-110">使用針對 NIC 所設定之容錯移轉和測試 faiover 網路設定來建立 ASR OracleNicConfig 物件。</span><span class="sxs-lookup"><span data-stu-id="50710-110">Creates an ASRVmNicConfig object with the failover and test faiover networking settings configured for the NIC.</span></span> <span data-ttu-id="50710-111">上述未傳遞的任何屬性，會從傳遞的受保護專案抓取。</span><span class="sxs-lookup"><span data-stu-id="50710-111">Any property that's not passed above is fetched from the protected item passed.</span></span>

### <span data-ttu-id="50710-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="50710-112">Example 2</span></span>
```powershell
PS C:\> $nicConfig = New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -ReplicationProtectedItem $Rpi -TfoNicName $TfoNicName -TfoNicResourceGroupName $TfoNicRgName -TfoReuseExistingNic
```

<span data-ttu-id="50710-113">使用針對 NIC 重新命名所設定的測試 faiover 網路設定來建立 ASRConfigConfig 物件。</span><span class="sxs-lookup"><span data-stu-id="50710-113">Creates an ASRVmNicConfig object with the test faiover networking settings configured for the NIC renaming.</span></span> <span data-ttu-id="50710-114">上述未傳遞的任何屬性，會從傳遞的受保護專案抓取。</span><span class="sxs-lookup"><span data-stu-id="50710-114">Any property that's not passed above is fetched from the protected item passed.</span></span>


### <span data-ttu-id="50710-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="50710-115">Example 3</span></span>

<span data-ttu-id="50710-116">建立包含容錯移轉的 ASR NIC 設定檔，並測試容錯移轉相關組配置詳細資料。</span><span class="sxs-lookup"><span data-stu-id="50710-116">Creates an ASR NIC config that contains the failover and test failover related configuration details.</span></span> <span data-ttu-id="50710-117"> (自動) </span><span class="sxs-lookup"><span data-stu-id="50710-117">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -RecoveryNetworkSecurityGroupId <String> -RecoveryNicStaticIPAddress '10.0.0.1' -RecoveryVMNetworkId $recoveryNetworkId -RecoveryVMSubnetName $recoverySubnetName -ReplicationProtectedItem $Rpi -TfoNetworkSecurityGroupId <String> -TfoNicStaticIPAddress <String> -TfoVMNetworkId <String> -TfoVMSubnetName <String>
```

## <span data-ttu-id="50710-118">參數</span><span class="sxs-lookup"><span data-stu-id="50710-118">PARAMETERS</span></span>

### <span data-ttu-id="50710-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50710-119">-DefaultProfile</span></span>
<span data-ttu-id="50710-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="50710-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50710-121">-EnableAccenetworkingOnRecovery</span><span class="sxs-lookup"><span data-stu-id="50710-121">-EnableAcceleratedNetworkingOnRecovery</span></span>
<span data-ttu-id="50710-122">指定在修復 NIC 上是否啟用加速網路。</span><span class="sxs-lookup"><span data-stu-id="50710-122">Specifies whether accelerated networking is enabled on recovery NIC.</span></span>

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

### <span data-ttu-id="50710-123">-EnableAcceworkNetworkingOnTfo</span><span class="sxs-lookup"><span data-stu-id="50710-123">-EnableAcceleratedNetworkingOnTfo</span></span>
<span data-ttu-id="50710-124">指定測試容錯移轉 NIC 上是否已啟用加速網路。</span><span class="sxs-lookup"><span data-stu-id="50710-124">Specifies whether accelerated networking is enabled on test failover NIC.</span></span>

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

### <span data-ttu-id="50710-125">-NicId</span><span class="sxs-lookup"><span data-stu-id="50710-125">-NicId</span></span>
<span data-ttu-id="50710-126">指定 ASR NIC GUID。</span><span class="sxs-lookup"><span data-stu-id="50710-126">Specify the ASR NIC GUID.</span></span>

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

### <span data-ttu-id="50710-127">-RecoveryLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="50710-127">-RecoveryLBBackendAddressPoolId</span></span>
<span data-ttu-id="50710-128">指定復原 NIC 的後端位址資料庫的 ID。</span><span class="sxs-lookup"><span data-stu-id="50710-128">Specifies the IDs of backend address pools for the recovery NIC.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50710-129">-RecoveryNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="50710-129">-RecoveryNetworkSecurityGroupId</span></span>
<span data-ttu-id="50710-130">指定與復原 NIC 相關聯的 NSG 識別碼。</span><span class="sxs-lookup"><span data-stu-id="50710-130">Specifies the ID of the NSG associated with recovery NIC.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50710-131">-RecoveryNicName</span><span class="sxs-lookup"><span data-stu-id="50710-131">-RecoveryNicName</span></span>
<span data-ttu-id="50710-132">指定復原 NIC 的名稱。</span><span class="sxs-lookup"><span data-stu-id="50710-132">Specifies the name of the recovery NIC.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50710-133">-RecoveryNicResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50710-133">-RecoveryNicResourceGroupName</span></span>
<span data-ttu-id="50710-134">指定復原 NIC 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="50710-134">Specifies the name of the recovery NIC resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50710-135">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="50710-135">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="50710-136">指定復原 NIC 的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="50710-136">Specifies the IP address of the recovery NIC.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50710-137">-RecoveryPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="50710-137">-RecoveryPublicIPAddressId</span></span>
<span data-ttu-id="50710-138">指定與復原 NIC 相關聯的公用 IP 位址識別碼。</span><span class="sxs-lookup"><span data-stu-id="50710-138">Specifies the ID of the public IP address associated with recovery NIC.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50710-139">-RecoveryEVNetworkId</span><span class="sxs-lookup"><span data-stu-id="50710-139">-RecoveryVMNetworkId</span></span>
<span data-ttu-id="50710-140">指定復原虛擬網路的識別碼。</span><span class="sxs-lookup"><span data-stu-id="50710-140">Specifies the ID of the recovery virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50710-141">-RecoveryMSUBnetName</span><span class="sxs-lookup"><span data-stu-id="50710-141">-RecoveryVMSubnetName</span></span>
<span data-ttu-id="50710-142">指定復原子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="50710-142">Specifies the name of the recovery subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50710-143">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="50710-143">-ReplicationProtectedItem</span></span>
<span data-ttu-id="50710-144">指定 ASR 複製受保護的專案。</span><span class="sxs-lookup"><span data-stu-id="50710-144">Specify the ASR Replication Protected Item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50710-145">-ReuseExistingNic</span><span class="sxs-lookup"><span data-stu-id="50710-145">-ReuseExistingNic</span></span>
<span data-ttu-id="50710-146">指定在容錯移轉期間是否可以使用現有的 NIC。</span><span class="sxs-lookup"><span data-stu-id="50710-146">Specifies whether an existing NIC can be used during failover.</span></span>

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

### <span data-ttu-id="50710-147">-TfoLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="50710-147">-TfoLBBackendAddressPoolId</span></span>
<span data-ttu-id="50710-148">指定復原 NIC 的後端位址資料庫的 ID。</span><span class="sxs-lookup"><span data-stu-id="50710-148">Specifies the IDs of backend address pools for the recovery NIC.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50710-149">-TfoNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="50710-149">-TfoNetworkSecurityGroupId</span></span>
<span data-ttu-id="50710-150">指定與測試容錯移轉 NIC 相關聯的 NSG 識別碼。</span><span class="sxs-lookup"><span data-stu-id="50710-150">Specifies the ID of the NSG associated with test failover NIC.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50710-151">-TfoNicName</span><span class="sxs-lookup"><span data-stu-id="50710-151">-TfoNicName</span></span>
<span data-ttu-id="50710-152">指定測試容錯移轉 NIC 的名稱。</span><span class="sxs-lookup"><span data-stu-id="50710-152">Specifies the name of the test failover NIC.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50710-153">-TfoNicResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50710-153">-TfoNicResourceGroupName</span></span>
<span data-ttu-id="50710-154">指定測試容錯移轉 NIC 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="50710-154">Specifies the name of the test failover NIC resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50710-155">-TfoNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="50710-155">-TfoNicStaticIPAddress</span></span>
<span data-ttu-id="50710-156">指定測試容錯移轉 NIC 的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="50710-156">Specifies the IP address of the test failover NIC.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50710-157">-TfoPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="50710-157">-TfoPublicIPAddressId</span></span>
<span data-ttu-id="50710-158">指定與測試容錯移轉 NIC 相關聯的公用 IP 位址識別碼。</span><span class="sxs-lookup"><span data-stu-id="50710-158">Specifies the ID of the public IP address associated with test failover NIC.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50710-159">-TfoReuseExistingNic</span><span class="sxs-lookup"><span data-stu-id="50710-159">-TfoReuseExistingNic</span></span>
<span data-ttu-id="50710-160">指定是否可以在測試容錯移轉期間使用現有的 NIC。</span><span class="sxs-lookup"><span data-stu-id="50710-160">Specifies whether an existing NIC can be used during test failover.</span></span>

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

### <span data-ttu-id="50710-161">-TfoUFNetworkId</span><span class="sxs-lookup"><span data-stu-id="50710-161">-TfoVMNetworkId</span></span>
<span data-ttu-id="50710-162">指定測試容錯移轉虛擬網路的識別碼。</span><span class="sxs-lookup"><span data-stu-id="50710-162">Specifies the ID of the test failover virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50710-163">-TfoUFSubnetName</span><span class="sxs-lookup"><span data-stu-id="50710-163">-TfoVMSubnetName</span></span>
<span data-ttu-id="50710-164">指定測試容錯移轉子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="50710-164">Specifies the name of the test failover subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50710-165">-確認</span><span class="sxs-lookup"><span data-stu-id="50710-165">-Confirm</span></span>
<span data-ttu-id="50710-166">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="50710-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50710-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50710-167">-WhatIf</span></span>
<span data-ttu-id="50710-168">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="50710-168">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="50710-169">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="50710-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50710-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50710-170">CommonParameters</span></span>
<span data-ttu-id="50710-171">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="50710-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50710-172">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="50710-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50710-173">輸入</span><span class="sxs-lookup"><span data-stu-id="50710-173">INPUTS</span></span>

### <span data-ttu-id="50710-174">沒有</span><span class="sxs-lookup"><span data-stu-id="50710-174">None</span></span>

## <span data-ttu-id="50710-175">輸出</span><span class="sxs-lookup"><span data-stu-id="50710-175">OUTPUTS</span></span>

### <span data-ttu-id="50710-176">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMNicConfig</span><span class="sxs-lookup"><span data-stu-id="50710-176">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMNicConfig</span></span>

## <span data-ttu-id="50710-177">筆記</span><span class="sxs-lookup"><span data-stu-id="50710-177">NOTES</span></span>

## <span data-ttu-id="50710-178">相關連結</span><span class="sxs-lookup"><span data-stu-id="50710-178">RELATED LINKS</span></span>
