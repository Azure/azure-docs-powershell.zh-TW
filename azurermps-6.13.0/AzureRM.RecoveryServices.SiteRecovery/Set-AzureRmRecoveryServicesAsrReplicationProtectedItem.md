---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/set-azurermrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: d387774ebf5f269474df959de981568141f90fbe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447275"
---
# <span data-ttu-id="48b97-101">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="48b97-101">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="48b97-102">摘要</span><span class="sxs-lookup"><span data-stu-id="48b97-102">SYNOPSIS</span></span>
<span data-ttu-id="48b97-103">針對指定的複製受保護專案設定恢復屬性，例如目標網路和虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="48b97-103">Sets recovery properties such as target network and virtual machine size for the specified replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48b97-104">句法</span><span class="sxs-lookup"><span data-stu-id="48b97-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem>
 [-Name <String>] [-Size <String>] [-PrimaryNic <String>] [-RecoveryNetworkId <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryNicSubnetName <String>] [-RecoveryNicStaticIPAddress <String>]
 [-NicSelectionType <String>] [-RecoveryResourceGroupId <String>] [-LicenseType <String>]
 [-RecoveryAvailabilitySet <String>] [-RecoveryBootDiagStorageAccountId <String>]
 [-AzureToAzureUpdateReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]>]
 [-UseManagedDisk <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="48b97-105">說明</span><span class="sxs-lookup"><span data-stu-id="48b97-105">DESCRIPTION</span></span>
<span data-ttu-id="48b97-106">**AzureRmRecoveryServicesAsrReplicationProtectedItem** Cmdlet 會為複製受保護的專案設定復原屬性。</span><span class="sxs-lookup"><span data-stu-id="48b97-106">The **Set-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet sets the recovery properties for a Replication Protected Item.</span></span>

## <span data-ttu-id="48b97-107">示例</span><span class="sxs-lookup"><span data-stu-id="48b97-107">EXAMPLES</span></span>

### <span data-ttu-id="48b97-108">範例1</span><span class="sxs-lookup"><span data-stu-id="48b97-108">Example 1</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $RPI -PrimaryNic $NicId -RecoveryNetworkId $AzureNetworkID -RecoveryNicSubnetName $subnetName
```

<span data-ttu-id="48b97-109">啟動使用指定參數來更新禁止複製專案設定的作業，並傳回用於追蹤作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="48b97-109">Starts the operation of updating the replication protect item settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="48b97-110">參數</span><span class="sxs-lookup"><span data-stu-id="48b97-110">PARAMETERS</span></span>

### <span data-ttu-id="48b97-111">-AzureToAzureUpdateReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="48b97-111">-AzureToAzureUpdateReplicationConfiguration</span></span>
<span data-ttu-id="48b97-112">指定 [更新 relication] 的 [更新]。</span><span class="sxs-lookup"><span data-stu-id="48b97-112">Specifies the update relication configration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48b97-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48b97-113">-DefaultProfile</span></span>
<span data-ttu-id="48b97-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="48b97-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48b97-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48b97-115">-InputObject</span></span>
<span data-ttu-id="48b97-116">Cmdlet 的輸入物件：與要更新之受複製受保護的專案對應的 ASR 複製受保護專案物件。</span><span class="sxs-lookup"><span data-stu-id="48b97-116">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="48b97-117">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="48b97-117">-LicenseType</span></span>
<span data-ttu-id="48b97-118">指定要用於 Windows Server 虛擬機器的授權類型選取專案。</span><span class="sxs-lookup"><span data-stu-id="48b97-118">Specifiy the license type selection to be used for Windows Server virtual machines.</span></span> <span data-ttu-id="48b97-119">如果您有資格使用 Azure 混合式使用優惠 (中樞) 進行遷移，且想要指定在容錯移轉此受保護的專案時使用中樞設定，請將 [授權類型] 設定為 [WindowsServer]。</span><span class="sxs-lookup"><span data-stu-id="48b97-119">If you are entitled to use the Azure Hybrid Use Benefit (HUB) for migrations and would like to specify that the HUB setting be used while failing over this protected item set the license type to be WindowsServer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NoLicenseType, WindowsServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48b97-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="48b97-120">-Name</span></span>
<span data-ttu-id="48b97-121">指定將在容錯移轉時建立的恢復虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="48b97-121">Specifies the name of the recovery virtual machine that will be created on failover.</span></span>

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

### <span data-ttu-id="48b97-122">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="48b97-122">-NicSelectionType</span></span>
<span data-ttu-id="48b97-123">指定 (NIC 的網路介面卡，) 由使用者設定的屬性或依預設設定的內容。</span><span class="sxs-lookup"><span data-stu-id="48b97-123">Specifies the network interface card (NIC) properties set by user or set by default.</span></span>
<span data-ttu-id="48b97-124">您可以指定 NotSelected，以回到預設值。</span><span class="sxs-lookup"><span data-stu-id="48b97-124">You can specify NotSelected to go back to the default values.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NotSelected, SelectedByUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48b97-125">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="48b97-125">-PrimaryNic</span></span>
<span data-ttu-id="48b97-126">指定此 Cmdlet 設定 [復原網路] 屬性的虛擬機器 NIC。</span><span class="sxs-lookup"><span data-stu-id="48b97-126">Specifies the NIC of the virtual machine for which this cmdlet sets the recovery network property.</span></span>

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

### <span data-ttu-id="48b97-127">-RecoveryAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="48b97-127">-RecoveryAvailabilitySet</span></span>
<span data-ttu-id="48b97-128">容錯移轉之後，已針對複製受保護的專案進行可用性設定。</span><span class="sxs-lookup"><span data-stu-id="48b97-128">Availability set for replication protected item after failover.</span></span>

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

### <span data-ttu-id="48b97-129">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="48b97-129">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="48b97-130">指定用於恢復 azure VM 的啟動診斷的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="48b97-130">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="48b97-131">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="48b97-131">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="48b97-132">要將此虛擬機器容錯移轉至其中的復原雲端服務的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="48b97-132">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="48b97-133">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="48b97-133">-RecoveryNetworkId</span></span>
<span data-ttu-id="48b97-134">指定受保護專案應針對其進行容錯移轉之 Azure 虛擬網路的識別碼。</span><span class="sxs-lookup"><span data-stu-id="48b97-134">Specifies the ID of the Azure virtual network to which the protected item should be failed over.</span></span>

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

### <span data-ttu-id="48b97-135">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="48b97-135">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="48b97-136">指定在恢復時應該指派給主要 NIC 的靜態 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="48b97-136">Specifies the static IP address that should be assigned to primary NIC on recovery.</span></span>

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

### <span data-ttu-id="48b97-137">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="48b97-137">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="48b97-138">指定要在容錯移轉時，將受保護之專案的這個 NIC 連線至之 [復原] Azure 虛擬網路上的子網名稱。</span><span class="sxs-lookup"><span data-stu-id="48b97-138">Specifies the name of the subnet on the recovery Azure virtual network to which this NIC of the protected item should be connected to on failover.</span></span>

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

### <span data-ttu-id="48b97-139">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="48b97-139">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="48b97-140">修復區域中的 Azure 資源群組的識別碼，受保護的專案將會在容錯移轉時復原。</span><span class="sxs-lookup"><span data-stu-id="48b97-140">The ID of the Azure resource group in the recovery region in which the protected item will be recovered on failover.</span></span>

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

### <span data-ttu-id="48b97-141">-大小</span><span class="sxs-lookup"><span data-stu-id="48b97-141">-Size</span></span>
<span data-ttu-id="48b97-142">指定復原虛擬電腦大小。</span><span class="sxs-lookup"><span data-stu-id="48b97-142">Specifies the recovery virtual machine size.</span></span>
<span data-ttu-id="48b97-143">此值應該是由 Azure 虛擬機器支援的大小集合所組成。</span><span class="sxs-lookup"><span data-stu-id="48b97-143">The value should be from the set of sizes supported by Azure virtual machines.</span></span>

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

### <span data-ttu-id="48b97-144">-UseManagedDisk</span><span class="sxs-lookup"><span data-stu-id="48b97-144">-UseManagedDisk</span></span>
<span data-ttu-id="48b97-145">指定在容錯移轉中建立的 Azure 虛擬機器是否應使用受管理的磁片。</span><span class="sxs-lookup"><span data-stu-id="48b97-145">Specifies if the Azure virtual machine that is created on failover should use managed disks.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: True, False

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48b97-146">-確認</span><span class="sxs-lookup"><span data-stu-id="48b97-146">-Confirm</span></span>
<span data-ttu-id="48b97-147">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="48b97-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48b97-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48b97-148">-WhatIf</span></span>
<span data-ttu-id="48b97-149">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="48b97-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="48b97-150">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="48b97-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48b97-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48b97-151">CommonParameters</span></span>
<span data-ttu-id="48b97-152">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="48b97-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48b97-153">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="48b97-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48b97-154">輸入</span><span class="sxs-lookup"><span data-stu-id="48b97-154">INPUTS</span></span>

### <span data-ttu-id="48b97-155">RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="48b97-155">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="48b97-156">輸出</span><span class="sxs-lookup"><span data-stu-id="48b97-156">OUTPUTS</span></span>

### <span data-ttu-id="48b97-157">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="48b97-157">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="48b97-158">筆記</span><span class="sxs-lookup"><span data-stu-id="48b97-158">NOTES</span></span>

## <span data-ttu-id="48b97-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="48b97-159">RELATED LINKS</span></span>

[<span data-ttu-id="48b97-160">AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="48b97-160">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="48b97-161">新-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="48b97-161">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="48b97-162">移除-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="48b97-162">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
