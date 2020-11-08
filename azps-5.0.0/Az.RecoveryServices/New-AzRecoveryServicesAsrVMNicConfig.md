---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrvmnicconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrVMNicConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrVMNicConfig.md
ms.openlocfilehash: 658a0cfa66abd71a63edc67ab2615713ac815bcd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138488"
---
# <span data-ttu-id="a3165-101">New-AzRecoveryServicesAsrVMNicConfig</span><span class="sxs-lookup"><span data-stu-id="a3165-101">New-AzRecoveryServicesAsrVMNicConfig</span></span>

## <span data-ttu-id="a3165-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a3165-102">SYNOPSIS</span></span>
<span data-ttu-id="a3165-103">建立一個 ASR NIC config，其中包含容錯移轉與測試容錯移轉相關的配置詳細資料。</span><span class="sxs-lookup"><span data-stu-id="a3165-103">Creates an ASR NIC config that contains the failover and test failover related configuration details.</span></span>

## <span data-ttu-id="a3165-104">句法</span><span class="sxs-lookup"><span data-stu-id="a3165-104">SYNTAX</span></span>

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

## <span data-ttu-id="a3165-105">說明</span><span class="sxs-lookup"><span data-stu-id="a3165-105">DESCRIPTION</span></span>
<span data-ttu-id="a3165-106">**新的-AzRecoveryServicesAsrVMNicConfig** Cmdlet 會建立一個 ASR NIC config 物件，其中包含容錯移轉與測試容錯移轉相關詳細資料。</span><span class="sxs-lookup"><span data-stu-id="a3165-106">The **New-AzRecoveryServicesAsrVMNicConfig** cmdlet creates an ASR NIC config object that contains the failover and test failover related details.</span></span> <span data-ttu-id="a3165-107">如果未傳遞任何資訊，則會從複製受保護的專案挑選對應的值，避免這些值更新為 null。</span><span class="sxs-lookup"><span data-stu-id="a3165-107">In case any information is not passed, the corresponding values are picked from the replication protected item to avoid these values being updated to null.</span></span>

## <span data-ttu-id="a3165-108">示例</span><span class="sxs-lookup"><span data-stu-id="a3165-108">EXAMPLES</span></span>

### <span data-ttu-id="a3165-109">範例1</span><span class="sxs-lookup"><span data-stu-id="a3165-109">Example 1</span></span>
```powershell
PS C:\> $nicConfig = New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -ReplicationProtectedItem $Rpi -RecoveryVMNetworkId $recoveryNetworkId -RecoveryVMSubnetName $recoverySubnetName -RecoveryNicStaticIPAddress "10.0.0.1" `
    -TfoVMNetworkId $tfoNetworkId -TfoVMSubnetName $tfoSubnetName -TfoNicStaticIPAddress "10.0.1.1"
```

<span data-ttu-id="a3165-110">使用針對 NIC 設定的容錯移轉和測試 faiover 網路設定來建立 ASRVmNicConfig 物件。</span><span class="sxs-lookup"><span data-stu-id="a3165-110">Creates an ASRVmNicConfig object with the failover and test faiover networking settings configured for the NIC.</span></span> <span data-ttu-id="a3165-111">未傳遞的任何屬性都會從已傳送的受保護專案提取。</span><span class="sxs-lookup"><span data-stu-id="a3165-111">Any property that's not passed above is fetched from the protected item passed.</span></span>

### <span data-ttu-id="a3165-112">範例2</span><span class="sxs-lookup"><span data-stu-id="a3165-112">Example 2</span></span>
```powershell
PS C:\> $nicConfig = New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -ReplicationProtectedItem $Rpi -TfoNicName $TfoNicName -TfoNicResourceGroupName $TfoNicRgName -TfoReuseExistingNic
```

<span data-ttu-id="a3165-113">使用針對 NIC 重新命名設定的測試 faiover 網路設定來建立 ASRVmNicConfig 物件。</span><span class="sxs-lookup"><span data-stu-id="a3165-113">Creates an ASRVmNicConfig object with the test faiover networking settings configured for the NIC renaming.</span></span> <span data-ttu-id="a3165-114">未傳遞的任何屬性都會從已傳送的受保護專案提取。</span><span class="sxs-lookup"><span data-stu-id="a3165-114">Any property that's not passed above is fetched from the protected item passed.</span></span>


### <span data-ttu-id="a3165-115">範例3</span><span class="sxs-lookup"><span data-stu-id="a3165-115">Example 3</span></span>

<span data-ttu-id="a3165-116">建立一個 ASR NIC config，其中包含容錯移轉與測試容錯移轉相關的配置詳細資料。</span><span class="sxs-lookup"><span data-stu-id="a3165-116">Creates an ASR NIC config that contains the failover and test failover related configuration details.</span></span> <span data-ttu-id="a3165-117"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="a3165-117">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -RecoveryNetworkSecurityGroupId <String> -RecoveryNicStaticIPAddress '10.0.0.1' -RecoveryVMNetworkId $recoveryNetworkId -RecoveryVMSubnetName $recoverySubnetName -ReplicationProtectedItem $Rpi -TfoNetworkSecurityGroupId <String> -TfoNicStaticIPAddress <String> -TfoVMNetworkId <String> -TfoVMSubnetName <String>
```

## <span data-ttu-id="a3165-118">參數</span><span class="sxs-lookup"><span data-stu-id="a3165-118">PARAMETERS</span></span>

### <span data-ttu-id="a3165-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3165-119">-DefaultProfile</span></span>
<span data-ttu-id="a3165-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a3165-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3165-121">-EnableAcceleratedNetworkingOnRecovery</span><span class="sxs-lookup"><span data-stu-id="a3165-121">-EnableAcceleratedNetworkingOnRecovery</span></span>
<span data-ttu-id="a3165-122">指定是否在恢復 NIC 上啟用加速網路。</span><span class="sxs-lookup"><span data-stu-id="a3165-122">Specifies whether accelerated networking is enabled on recovery NIC.</span></span>

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

### <span data-ttu-id="a3165-123">-EnableAcceleratedNetworkingOnTfo</span><span class="sxs-lookup"><span data-stu-id="a3165-123">-EnableAcceleratedNetworkingOnTfo</span></span>
<span data-ttu-id="a3165-124">指定是否在測試容錯移轉 NIC 上啟用加速網路。</span><span class="sxs-lookup"><span data-stu-id="a3165-124">Specifies whether accelerated networking is enabled on test failover NIC.</span></span>

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

### <span data-ttu-id="a3165-125">-NicId</span><span class="sxs-lookup"><span data-stu-id="a3165-125">-NicId</span></span>
<span data-ttu-id="a3165-126">指定 ASR NIC GUID。</span><span class="sxs-lookup"><span data-stu-id="a3165-126">Specify the ASR NIC GUID.</span></span>

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

### <span data-ttu-id="a3165-127">-RecoveryLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="a3165-127">-RecoveryLBBackendAddressPoolId</span></span>
<span data-ttu-id="a3165-128">為復原 NIC 指定後端位址集區的 Id。</span><span class="sxs-lookup"><span data-stu-id="a3165-128">Specifies the IDs of backend address pools for the recovery NIC.</span></span>

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

### <span data-ttu-id="a3165-129">-RecoveryNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="a3165-129">-RecoveryNetworkSecurityGroupId</span></span>
<span data-ttu-id="a3165-130">指定與恢復 NIC 相關聯之 NSG 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a3165-130">Specifies the ID of the NSG associated with recovery NIC.</span></span>

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

### <span data-ttu-id="a3165-131">-RecoveryNicName</span><span class="sxs-lookup"><span data-stu-id="a3165-131">-RecoveryNicName</span></span>
<span data-ttu-id="a3165-132">指定恢復 NIC 的名稱。</span><span class="sxs-lookup"><span data-stu-id="a3165-132">Specifies the name of the recovery NIC.</span></span>

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

### <span data-ttu-id="a3165-133">-RecoveryNicResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3165-133">-RecoveryNicResourceGroupName</span></span>
<span data-ttu-id="a3165-134">指定復原 NIC 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a3165-134">Specifies the name of the recovery NIC resource group.</span></span>

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

### <span data-ttu-id="a3165-135">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="a3165-135">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="a3165-136">指定恢復 NIC 的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="a3165-136">Specifies the IP address of the recovery NIC.</span></span>

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

### <span data-ttu-id="a3165-137">-RecoveryPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="a3165-137">-RecoveryPublicIPAddressId</span></span>
<span data-ttu-id="a3165-138">指定與恢復 NIC 相關聯之公用 IP 位址的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a3165-138">Specifies the ID of the public IP address associated with recovery NIC.</span></span>

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

### <span data-ttu-id="a3165-139">-RecoveryVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="a3165-139">-RecoveryVMNetworkId</span></span>
<span data-ttu-id="a3165-140">指定復原虛擬網路的 ID。</span><span class="sxs-lookup"><span data-stu-id="a3165-140">Specifies the ID of the recovery virtual network.</span></span>

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

### <span data-ttu-id="a3165-141">-RecoveryVMSubnetName</span><span class="sxs-lookup"><span data-stu-id="a3165-141">-RecoveryVMSubnetName</span></span>
<span data-ttu-id="a3165-142">指定復原子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="a3165-142">Specifies the name of the recovery subnet.</span></span>

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

### <span data-ttu-id="a3165-143">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a3165-143">-ReplicationProtectedItem</span></span>
<span data-ttu-id="a3165-144">指定 ASR 複製受保護的專案。</span><span class="sxs-lookup"><span data-stu-id="a3165-144">Specify the ASR Replication Protected Item.</span></span>

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

### <span data-ttu-id="a3165-145">-ReuseExistingNic</span><span class="sxs-lookup"><span data-stu-id="a3165-145">-ReuseExistingNic</span></span>
<span data-ttu-id="a3165-146">指定在容錯移轉期間，是否可以使用現有的 NIC。</span><span class="sxs-lookup"><span data-stu-id="a3165-146">Specifies whether an existing NIC can be used during failover.</span></span>

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

### <span data-ttu-id="a3165-147">-TfoLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="a3165-147">-TfoLBBackendAddressPoolId</span></span>
<span data-ttu-id="a3165-148">為復原 NIC 指定後端位址集區的 Id。</span><span class="sxs-lookup"><span data-stu-id="a3165-148">Specifies the IDs of backend address pools for the recovery NIC.</span></span>

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

### <span data-ttu-id="a3165-149">-TfoNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="a3165-149">-TfoNetworkSecurityGroupId</span></span>
<span data-ttu-id="a3165-150">指定與測試容錯移轉 NIC 相關聯之 NSG 的 ID。</span><span class="sxs-lookup"><span data-stu-id="a3165-150">Specifies the ID of the NSG associated with test failover NIC.</span></span>

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

### <span data-ttu-id="a3165-151">-TfoNicName</span><span class="sxs-lookup"><span data-stu-id="a3165-151">-TfoNicName</span></span>
<span data-ttu-id="a3165-152">指定測試容錯移轉 NIC 的名稱。</span><span class="sxs-lookup"><span data-stu-id="a3165-152">Specifies the name of the test failover NIC.</span></span>

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

### <span data-ttu-id="a3165-153">-TfoNicResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3165-153">-TfoNicResourceGroupName</span></span>
<span data-ttu-id="a3165-154">指定測試容錯移轉 NIC 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a3165-154">Specifies the name of the test failover NIC resource group.</span></span>

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

### <span data-ttu-id="a3165-155">-TfoNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="a3165-155">-TfoNicStaticIPAddress</span></span>
<span data-ttu-id="a3165-156">指定測試容錯移轉 NIC 的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="a3165-156">Specifies the IP address of the test failover NIC.</span></span>

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

### <span data-ttu-id="a3165-157">-TfoPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="a3165-157">-TfoPublicIPAddressId</span></span>
<span data-ttu-id="a3165-158">指定與測試容錯移轉 NIC 相關聯之公用 IP 位址的 ID。</span><span class="sxs-lookup"><span data-stu-id="a3165-158">Specifies the ID of the public IP address associated with test failover NIC.</span></span>

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

### <span data-ttu-id="a3165-159">-TfoReuseExistingNic</span><span class="sxs-lookup"><span data-stu-id="a3165-159">-TfoReuseExistingNic</span></span>
<span data-ttu-id="a3165-160">指定是否可在測試容錯移轉期間使用現有的 NIC。</span><span class="sxs-lookup"><span data-stu-id="a3165-160">Specifies whether an existing NIC can be used during test failover.</span></span>

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

### <span data-ttu-id="a3165-161">-TfoVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="a3165-161">-TfoVMNetworkId</span></span>
<span data-ttu-id="a3165-162">指定測試容錯移轉虛擬網路的 ID。</span><span class="sxs-lookup"><span data-stu-id="a3165-162">Specifies the ID of the test failover virtual network.</span></span>

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

### <span data-ttu-id="a3165-163">-TfoVMSubnetName</span><span class="sxs-lookup"><span data-stu-id="a3165-163">-TfoVMSubnetName</span></span>
<span data-ttu-id="a3165-164">指定測試容錯移轉子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="a3165-164">Specifies the name of the test failover subnet.</span></span>

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

### <span data-ttu-id="a3165-165">-確認</span><span class="sxs-lookup"><span data-stu-id="a3165-165">-Confirm</span></span>
<span data-ttu-id="a3165-166">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a3165-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3165-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3165-167">-WhatIf</span></span>
<span data-ttu-id="a3165-168">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a3165-168">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a3165-169">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a3165-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3165-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3165-170">CommonParameters</span></span>
<span data-ttu-id="a3165-171">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a3165-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3165-172">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a3165-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3165-173">輸入</span><span class="sxs-lookup"><span data-stu-id="a3165-173">INPUTS</span></span>

### <span data-ttu-id="a3165-174">所有</span><span class="sxs-lookup"><span data-stu-id="a3165-174">None</span></span>

## <span data-ttu-id="a3165-175">輸出</span><span class="sxs-lookup"><span data-stu-id="a3165-175">OUTPUTS</span></span>

### <span data-ttu-id="a3165-176">RecoveryServices. SiteRecovery. ASRVMNicConfig</span><span class="sxs-lookup"><span data-stu-id="a3165-176">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMNicConfig</span></span>

## <span data-ttu-id="a3165-177">筆記</span><span class="sxs-lookup"><span data-stu-id="a3165-177">NOTES</span></span>

## <span data-ttu-id="a3165-178">相關連結</span><span class="sxs-lookup"><span data-stu-id="a3165-178">RELATED LINKS</span></span>