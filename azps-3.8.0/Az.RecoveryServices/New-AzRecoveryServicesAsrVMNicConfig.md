---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrvmnicconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrVMNicConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrVMNicConfig.md
ms.openlocfilehash: f7b6cd7171b6f50ed0f239e733ca98f0ecd5c05a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958628"
---
# <span data-ttu-id="63ffe-101">New-AzRecoveryServicesAsrVMNicConfig</span><span class="sxs-lookup"><span data-stu-id="63ffe-101">New-AzRecoveryServicesAsrVMNicConfig</span></span>

## <span data-ttu-id="63ffe-102">摘要</span><span class="sxs-lookup"><span data-stu-id="63ffe-102">SYNOPSIS</span></span>
<span data-ttu-id="63ffe-103">建立一個 ASR NIC config，其中包含容錯移轉與測試容錯移轉相關的配置詳細資料。</span><span class="sxs-lookup"><span data-stu-id="63ffe-103">Creates an ASR NIC config that contains the failover and test failover related configuration details.</span></span>

## <span data-ttu-id="63ffe-104">句法</span><span class="sxs-lookup"><span data-stu-id="63ffe-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrVMNicConfig -NicId <String> -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-RecoveryVMNetworkId <String>] [-RecoveryVMSubnetName <String>] [-RecoveryNetworkSecurityGroupId <String>]
 [-EnableAcceleratedNetworkingOnRecovery] [-RecoveryNicStaticIPAddress <String>]
 [-RecoveryPublicIPAddressId <String>] [-RecoveryLBBackendAddressPoolId <String[]>] [-TfoVMNetworkId <String>]
 [-TfoVMSubnetName <String>] [-TfoNetworkSecurityGroupId <String>] [-EnableAcceleratedNetworkingOnTfo]
 [-TfoNicStaticIPAddress <String>] [-TfoPublicIPAddressId <String>] [-TfoLBBackendAddressPoolId <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63ffe-105">說明</span><span class="sxs-lookup"><span data-stu-id="63ffe-105">DESCRIPTION</span></span>
<span data-ttu-id="63ffe-106">**新的-AzRecoveryServicesAsrVMNicConfig** Cmdlet 會建立一個 ASR NIC config 物件，其中包含容錯移轉與測試容錯移轉相關詳細資料。</span><span class="sxs-lookup"><span data-stu-id="63ffe-106">The **New-AzRecoveryServicesAsrVMNicConfig** cmdlet creates an ASR NIC config object that contains the failover and test failover related details.</span></span> <span data-ttu-id="63ffe-107">如果未傳遞任何資訊，則會從複製受保護的專案挑選對應的值，避免這些值更新為 null。</span><span class="sxs-lookup"><span data-stu-id="63ffe-107">In case any information is not passed, the corresponding values are picked from the replication protected item to avoid these values being updated to null.</span></span>

## <span data-ttu-id="63ffe-108">示例</span><span class="sxs-lookup"><span data-stu-id="63ffe-108">EXAMPLES</span></span>

### <span data-ttu-id="63ffe-109">範例1</span><span class="sxs-lookup"><span data-stu-id="63ffe-109">Example 1</span></span>
```powershell
PS C:\> $nicConfig = New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -ReplicationProtectedItem $Rpi -RecoveryVMNetworkId $recoveryNetworkId -RecoveryVMSubnetName $recoverySubnetName -RecoveryNicStaticIPAddress "10.0.0.1" `
    -TfoVMNetworkId $tfoNetworkId -TfoVMSubnetName $tfoSubnetName -TfoNicStaticIPAddress "10.0.1.1"
```

<span data-ttu-id="63ffe-110">使用針對 NIC 設定的容錯移轉和測試 faiover 網路設定來建立 ASRVmNicConfig 物件。</span><span class="sxs-lookup"><span data-stu-id="63ffe-110">Creates an ASRVmNicConfig object with the failover and test faiover networking settings configured for the NIC.</span></span> <span data-ttu-id="63ffe-111">未傳遞的任何屬性都會從已傳送的受保護專案提取。</span><span class="sxs-lookup"><span data-stu-id="63ffe-111">Any property that's not passed above is fetched from the protected item passed.</span></span>

## <span data-ttu-id="63ffe-112">參數</span><span class="sxs-lookup"><span data-stu-id="63ffe-112">PARAMETERS</span></span>

### <span data-ttu-id="63ffe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63ffe-113">-DefaultProfile</span></span>
<span data-ttu-id="63ffe-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="63ffe-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63ffe-115">-EnableAcceleratedNetworkingOnRecovery</span><span class="sxs-lookup"><span data-stu-id="63ffe-115">-EnableAcceleratedNetworkingOnRecovery</span></span>
<span data-ttu-id="63ffe-116">指定是否在恢復 NIC 上啟用加速網路。</span><span class="sxs-lookup"><span data-stu-id="63ffe-116">Specifies whether accelerated networking is enabled on recovery NIC.</span></span>

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

### <span data-ttu-id="63ffe-117">-EnableAcceleratedNetworkingOnTfo</span><span class="sxs-lookup"><span data-stu-id="63ffe-117">-EnableAcceleratedNetworkingOnTfo</span></span>
<span data-ttu-id="63ffe-118">指定是否在測試容錯移轉 NIC 上啟用加速網路。</span><span class="sxs-lookup"><span data-stu-id="63ffe-118">Specifies whether accelerated networking is enabled on test failover NIC.</span></span>

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

### <span data-ttu-id="63ffe-119">-NicId</span><span class="sxs-lookup"><span data-stu-id="63ffe-119">-NicId</span></span>
<span data-ttu-id="63ffe-120">指定 ASR NIC GUID。</span><span class="sxs-lookup"><span data-stu-id="63ffe-120">Specify the ASR NIC GUID.</span></span>

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

### <span data-ttu-id="63ffe-121">-RecoveryLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="63ffe-121">-RecoveryLBBackendAddressPoolId</span></span>
<span data-ttu-id="63ffe-122">為復原 NIC 指定後端位址集區的 Id。</span><span class="sxs-lookup"><span data-stu-id="63ffe-122">Specifies the IDs of backend address pools for the recovery NIC.</span></span>

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

### <span data-ttu-id="63ffe-123">-RecoveryNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="63ffe-123">-RecoveryNetworkSecurityGroupId</span></span>
<span data-ttu-id="63ffe-124">指定與恢復 NIC 相關聯之 NSG 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="63ffe-124">Specifies the ID of the NSG associated with recovery NIC.</span></span>

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

### <span data-ttu-id="63ffe-125">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="63ffe-125">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="63ffe-126">指定恢復 NIC 的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="63ffe-126">Specifies the IP address of the recovery NIC.</span></span>

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

### <span data-ttu-id="63ffe-127">-RecoveryPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="63ffe-127">-RecoveryPublicIPAddressId</span></span>
<span data-ttu-id="63ffe-128">指定與恢復 NIC 相關聯之公用 IP 位址的識別碼。</span><span class="sxs-lookup"><span data-stu-id="63ffe-128">Specifies the ID of the public IP address associated with recovery NIC.</span></span>

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

### <span data-ttu-id="63ffe-129">-RecoveryVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="63ffe-129">-RecoveryVMNetworkId</span></span>
<span data-ttu-id="63ffe-130">指定復原虛擬網路的 ID。</span><span class="sxs-lookup"><span data-stu-id="63ffe-130">Specifies the ID of the recovery virtual network.</span></span>

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

### <span data-ttu-id="63ffe-131">-RecoveryVMSubnetName</span><span class="sxs-lookup"><span data-stu-id="63ffe-131">-RecoveryVMSubnetName</span></span>
<span data-ttu-id="63ffe-132">指定復原子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="63ffe-132">Specifies the name of the recovery subnet.</span></span>

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

### <span data-ttu-id="63ffe-133">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="63ffe-133">-ReplicationProtectedItem</span></span>
<span data-ttu-id="63ffe-134">指定 ASR 複製受保護的專案。</span><span class="sxs-lookup"><span data-stu-id="63ffe-134">Specify the ASR Replication Protected Item.</span></span>

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

### <span data-ttu-id="63ffe-135">-TfoLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="63ffe-135">-TfoLBBackendAddressPoolId</span></span>
<span data-ttu-id="63ffe-136">為復原 NIC 指定後端位址集區的 Id。</span><span class="sxs-lookup"><span data-stu-id="63ffe-136">Specifies the IDs of backend address pools for the recovery NIC.</span></span>

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

### <span data-ttu-id="63ffe-137">-TfoNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="63ffe-137">-TfoNetworkSecurityGroupId</span></span>
<span data-ttu-id="63ffe-138">指定與測試容錯移轉 NIC 相關聯之 NSG 的 ID。</span><span class="sxs-lookup"><span data-stu-id="63ffe-138">Specifies the ID of the NSG associated with test failover NIC.</span></span>

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

### <span data-ttu-id="63ffe-139">-TfoNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="63ffe-139">-TfoNicStaticIPAddress</span></span>
<span data-ttu-id="63ffe-140">指定測試容錯移轉 NIC 的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="63ffe-140">Specifies the IP address of the test failover NIC.</span></span>

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

### <span data-ttu-id="63ffe-141">-TfoPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="63ffe-141">-TfoPublicIPAddressId</span></span>
<span data-ttu-id="63ffe-142">指定與測試容錯移轉 NIC 相關聯之公用 IP 位址的 ID。</span><span class="sxs-lookup"><span data-stu-id="63ffe-142">Specifies the ID of the public IP address associated with test failover NIC.</span></span>

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

### <span data-ttu-id="63ffe-143">-TfoVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="63ffe-143">-TfoVMNetworkId</span></span>
<span data-ttu-id="63ffe-144">指定測試容錯移轉虛擬網路的 ID。</span><span class="sxs-lookup"><span data-stu-id="63ffe-144">Specifies the ID of the test failover virtual network.</span></span>

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

### <span data-ttu-id="63ffe-145">-TfoVMSubnetName</span><span class="sxs-lookup"><span data-stu-id="63ffe-145">-TfoVMSubnetName</span></span>
<span data-ttu-id="63ffe-146">指定測試容錯移轉子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="63ffe-146">Specifies the name of the test failover subnet.</span></span>

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

### <span data-ttu-id="63ffe-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63ffe-147">CommonParameters</span></span>
<span data-ttu-id="63ffe-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="63ffe-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63ffe-149">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="63ffe-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63ffe-150">輸入</span><span class="sxs-lookup"><span data-stu-id="63ffe-150">INPUTS</span></span>

### <span data-ttu-id="63ffe-151">所有</span><span class="sxs-lookup"><span data-stu-id="63ffe-151">None</span></span>

## <span data-ttu-id="63ffe-152">輸出</span><span class="sxs-lookup"><span data-stu-id="63ffe-152">OUTPUTS</span></span>

### <span data-ttu-id="63ffe-153">RecoveryServices. SiteRecovery. ASRVMNicConfig</span><span class="sxs-lookup"><span data-stu-id="63ffe-153">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMNicConfig</span></span>

## <span data-ttu-id="63ffe-154">筆記</span><span class="sxs-lookup"><span data-stu-id="63ffe-154">NOTES</span></span>

## <span data-ttu-id="63ffe-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="63ffe-155">RELATED LINKS</span></span>
