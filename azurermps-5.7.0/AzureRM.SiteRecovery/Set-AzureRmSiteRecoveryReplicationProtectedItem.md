---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: FCE4633A-4F75-4A23-B825-6AC62238658A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/set-azurermsiterecoveryreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryReplicationProtectedItem.md
ms.openlocfilehash: e09cc216b7ba3ef383467ea53478cfe8819e0a4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454007"
---
# <span data-ttu-id="f55f9-101">Set-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f55f9-101">Set-AzureRmSiteRecoveryReplicationProtectedItem</span></span>

## <span data-ttu-id="f55f9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f55f9-102">SYNOPSIS</span></span>
<span data-ttu-id="f55f9-103">針對複製受保護的專案設定復原屬性，例如目標網路和虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="f55f9-103">Sets recovery properties such as target network and virtual machine size for a Replication Protected Item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f55f9-104">句法</span><span class="sxs-lookup"><span data-stu-id="f55f9-104">SYNTAX</span></span>

```
Set-AzureRmSiteRecoveryReplicationProtectedItem -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-Name <String>] [-Size <String>] [-PrimaryNic <String>] [-RecoveryNetworkId <String>]
 [-RecoveryNicSubnetName <String>] [-RecoveryNicStaticIPAddress <String>] [-NicSelectionType <String>]
 [-LicenseType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f55f9-105">說明</span><span class="sxs-lookup"><span data-stu-id="f55f9-105">DESCRIPTION</span></span>
<span data-ttu-id="f55f9-106">**AzureRmSiteRecoveryReplicationProtectedItem** Cmdlet 會為複製受保護的專案設定復原屬性。</span><span class="sxs-lookup"><span data-stu-id="f55f9-106">The **Set-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet sets the recovery properties for a Replication Protected Item.</span></span>

## <span data-ttu-id="f55f9-107">示例</span><span class="sxs-lookup"><span data-stu-id="f55f9-107">EXAMPLES</span></span>

## <span data-ttu-id="f55f9-108">參數</span><span class="sxs-lookup"><span data-stu-id="f55f9-108">PARAMETERS</span></span>

### <span data-ttu-id="f55f9-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f55f9-109">-DefaultProfile</span></span>
<span data-ttu-id="f55f9-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f55f9-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f55f9-111">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="f55f9-111">-LicenseType</span></span>
<span data-ttu-id="f55f9-112">指定透過混合式使用好處遷移之 Windows Server 虛擬機器的授權類型選取。</span><span class="sxs-lookup"><span data-stu-id="f55f9-112">Specifies the license type selection for Windows Server virtual machines migrated through Hybrid use benefit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: NoLicenseType, WindowsServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f55f9-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="f55f9-113">-Name</span></span>
<span data-ttu-id="f55f9-114">指定恢復虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="f55f9-114">Specifies the name of the recovery virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f55f9-115">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="f55f9-115">-NicSelectionType</span></span>
<span data-ttu-id="f55f9-116">指定 (NIC 的網路介面卡，) 由使用者設定的屬性或依預設設定的內容。</span><span class="sxs-lookup"><span data-stu-id="f55f9-116">Specifies the network interface card (NIC) properties set by user or set by default.</span></span>
<span data-ttu-id="f55f9-117">您可以指定 NotSelected，以回到預設值。</span><span class="sxs-lookup"><span data-stu-id="f55f9-117">You can specify NotSelected to go back to the default values.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: NotSelected, SelectedByUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f55f9-118">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="f55f9-118">-PrimaryNic</span></span>
<span data-ttu-id="f55f9-119">指定此 Cmdlet 設定 [復原網路] 屬性的虛擬機器 NIC。</span><span class="sxs-lookup"><span data-stu-id="f55f9-119">Specifies the NIC of the virtual machine for which this cmdlet sets the recovery network property.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f55f9-120">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="f55f9-120">-RecoveryNetworkId</span></span>
<span data-ttu-id="f55f9-121">指定此 Cmdlet 可針對其恢復受保護專案的 Azure 虛擬網路識別碼。</span><span class="sxs-lookup"><span data-stu-id="f55f9-121">Specifies the ID of the Azure virtual network for which this cmdlet recovers the Protected Item.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f55f9-122">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="f55f9-122">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="f55f9-123">指定在恢復時應該指派給主要 NIC 的靜態 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="f55f9-123">Specifies the static IP address that should be assigned to primary NIC on recovery.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f55f9-124">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="f55f9-124">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="f55f9-125">在恢復 Azure 虛擬網路網路上指定此 Cmdlet 可復原受保護專案的子網名稱。</span><span class="sxs-lookup"><span data-stu-id="f55f9-125">Specifies the name of the Subnet on the recovery Azure virtual network for which this cmdlet recovers the Protected Item.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f55f9-126">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f55f9-126">-ReplicationProtectedItem</span></span>
<span data-ttu-id="f55f9-127">指定 Azure 網站恢復複製受保護的專案。</span><span class="sxs-lookup"><span data-stu-id="f55f9-127">Specifies the Azure Site Recovery Replication Protected Item.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f55f9-128">-大小</span><span class="sxs-lookup"><span data-stu-id="f55f9-128">-Size</span></span>
<span data-ttu-id="f55f9-129">指定復原虛擬電腦大小。</span><span class="sxs-lookup"><span data-stu-id="f55f9-129">Specifies the recovery virtual machine size.</span></span>
<span data-ttu-id="f55f9-130">此值應該是由 Azure 虛擬機器支援的大小集合所組成。</span><span class="sxs-lookup"><span data-stu-id="f55f9-130">The value should be from the set of sizes supported by Azure virtual machines.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f55f9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f55f9-131">CommonParameters</span></span>
<span data-ttu-id="f55f9-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f55f9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f55f9-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f55f9-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f55f9-134">輸入</span><span class="sxs-lookup"><span data-stu-id="f55f9-134">INPUTS</span></span>

### <span data-ttu-id="f55f9-135">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f55f9-135">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="f55f9-136">形參 "ReplicationProtectedItem" 接受管線中 "ASRReplicationProtectedItem" 類型的值</span><span class="sxs-lookup"><span data-stu-id="f55f9-136">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="f55f9-137">輸出</span><span class="sxs-lookup"><span data-stu-id="f55f9-137">OUTPUTS</span></span>

### <span data-ttu-id="f55f9-138">ASRJob 中的 SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="f55f9-138">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f55f9-139">筆記</span><span class="sxs-lookup"><span data-stu-id="f55f9-139">NOTES</span></span>

## <span data-ttu-id="f55f9-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="f55f9-140">RELATED LINKS</span></span>

[<span data-ttu-id="f55f9-141">AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f55f9-141">Get-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Get-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="f55f9-142">新-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f55f9-142">New-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./New-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="f55f9-143">移除-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f55f9-143">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Remove-AzureRmSiteRecoveryReplicationProtectedItem.md)
