---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: FCE4633A-4F75-4A23-B825-6AC62238658A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryReplicationProtectedItem.md
ms.openlocfilehash: 2070a26a1bfdb41e5135479548f04bdbaced6884
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447949"
---
# <span data-ttu-id="8ac6a-101">Set-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8ac6a-101">Set-AzureRmSiteRecoveryReplicationProtectedItem</span></span>

## <span data-ttu-id="8ac6a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8ac6a-102">SYNOPSIS</span></span>
<span data-ttu-id="8ac6a-103">針對複製受保護的專案設定復原屬性，例如目標網路和虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="8ac6a-103">Sets recovery properties such as target network and virtual machine size for a Replication Protected Item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ac6a-104">句法</span><span class="sxs-lookup"><span data-stu-id="8ac6a-104">SYNTAX</span></span>

```
Set-AzureRmSiteRecoveryReplicationProtectedItem -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-Name <String>] [-Size <String>] [-PrimaryNic <String>] [-RecoveryNetworkId <String>]
 [-RecoveryNicSubnetName <String>] [-RecoveryNicStaticIPAddress <String>] [-NicSelectionType <String>]
 [-LicenseType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ac6a-105">說明</span><span class="sxs-lookup"><span data-stu-id="8ac6a-105">DESCRIPTION</span></span>
<span data-ttu-id="8ac6a-106">**AzureRmSiteRecoveryReplicationProtectedItem** Cmdlet 會為複製受保護的專案設定復原屬性。</span><span class="sxs-lookup"><span data-stu-id="8ac6a-106">The **Set-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet sets the recovery properties for a Replication Protected Item.</span></span>

## <span data-ttu-id="8ac6a-107">示例</span><span class="sxs-lookup"><span data-stu-id="8ac6a-107">EXAMPLES</span></span>

## <span data-ttu-id="8ac6a-108">參數</span><span class="sxs-lookup"><span data-stu-id="8ac6a-108">PARAMETERS</span></span>

### <span data-ttu-id="8ac6a-109">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="8ac6a-109">-LicenseType</span></span>
<span data-ttu-id="8ac6a-110">指定透過混合式使用好處遷移之 Windows Server 虛擬機器的授權類型選取。</span><span class="sxs-lookup"><span data-stu-id="8ac6a-110">Specifies the license type selection for Windows Server virtual machines migrated through Hybrid use benefit.</span></span>

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

### <span data-ttu-id="8ac6a-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="8ac6a-111">-Name</span></span>
<span data-ttu-id="8ac6a-112">指定恢復虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="8ac6a-112">Specifies the name of the recovery virtual machine.</span></span>

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

### <span data-ttu-id="8ac6a-113">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="8ac6a-113">-NicSelectionType</span></span>
<span data-ttu-id="8ac6a-114">指定 (NIC 的網路介面卡，) 由使用者設定的屬性或依預設設定的內容。</span><span class="sxs-lookup"><span data-stu-id="8ac6a-114">Specifies the network interface card (NIC) properties set by user or set by default.</span></span>
<span data-ttu-id="8ac6a-115">您可以指定 NotSelected，以回到預設值。</span><span class="sxs-lookup"><span data-stu-id="8ac6a-115">You can specify NotSelected to go back to the default values.</span></span>

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

### <span data-ttu-id="8ac6a-116">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="8ac6a-116">-PrimaryNic</span></span>
<span data-ttu-id="8ac6a-117">指定此 Cmdlet 設定 [復原網路] 屬性的虛擬機器 NIC。</span><span class="sxs-lookup"><span data-stu-id="8ac6a-117">Specifies the NIC of the virtual machine for which this cmdlet sets the recovery network property.</span></span>

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

### <span data-ttu-id="8ac6a-118">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="8ac6a-118">-RecoveryNetworkId</span></span>
<span data-ttu-id="8ac6a-119">指定此 Cmdlet 可針對其恢復受保護專案的 Azure 虛擬網路識別碼。</span><span class="sxs-lookup"><span data-stu-id="8ac6a-119">Specifies the ID of the Azure virtual network for which this cmdlet recovers the Protected Item.</span></span>

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

### <span data-ttu-id="8ac6a-120">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="8ac6a-120">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="8ac6a-121">指定在恢復時應該指派給主要 NIC 的靜態 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="8ac6a-121">Specifies the static IP address that should be assigned to primary NIC on recovery.</span></span>

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

### <span data-ttu-id="8ac6a-122">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="8ac6a-122">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="8ac6a-123">在恢復 Azure 虛擬網路網路上指定此 Cmdlet 可復原受保護專案的子網名稱。</span><span class="sxs-lookup"><span data-stu-id="8ac6a-123">Specifies the name of the Subnet on the recovery Azure virtual network for which this cmdlet recovers the Protected Item.</span></span>

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

### <span data-ttu-id="8ac6a-124">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8ac6a-124">-ReplicationProtectedItem</span></span>
<span data-ttu-id="8ac6a-125">指定 Azure 網站恢復複製受保護的專案。</span><span class="sxs-lookup"><span data-stu-id="8ac6a-125">Specifies the Azure Site Recovery Replication Protected Item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8ac6a-126">-大小</span><span class="sxs-lookup"><span data-stu-id="8ac6a-126">-Size</span></span>
<span data-ttu-id="8ac6a-127">指定復原虛擬電腦大小。</span><span class="sxs-lookup"><span data-stu-id="8ac6a-127">Specifies the recovery virtual machine size.</span></span>
<span data-ttu-id="8ac6a-128">此值應該是由 Azure 虛擬機器支援的大小集合所組成。</span><span class="sxs-lookup"><span data-stu-id="8ac6a-128">The value should be from the set of sizes supported by Azure virtual machines.</span></span>

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

### <span data-ttu-id="8ac6a-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ac6a-129">-DefaultProfile</span></span>
<span data-ttu-id="8ac6a-130">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8ac6a-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ac6a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ac6a-131">CommonParameters</span></span>
<span data-ttu-id="8ac6a-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8ac6a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ac6a-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8ac6a-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ac6a-134">輸入</span><span class="sxs-lookup"><span data-stu-id="8ac6a-134">INPUTS</span></span>

### <span data-ttu-id="8ac6a-135">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8ac6a-135">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="8ac6a-136">形參 "ReplicationProtectedItem" 接受管線中 "ASRReplicationProtectedItem" 類型的值</span><span class="sxs-lookup"><span data-stu-id="8ac6a-136">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="8ac6a-137">輸出</span><span class="sxs-lookup"><span data-stu-id="8ac6a-137">OUTPUTS</span></span>

### <span data-ttu-id="8ac6a-138">ASRJob 中的 SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="8ac6a-138">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="8ac6a-139">筆記</span><span class="sxs-lookup"><span data-stu-id="8ac6a-139">NOTES</span></span>

## <span data-ttu-id="8ac6a-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="8ac6a-140">RELATED LINKS</span></span>

[<span data-ttu-id="8ac6a-141">AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8ac6a-141">Get-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Get-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="8ac6a-142">新-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8ac6a-142">New-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./New-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="8ac6a-143">移除-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8ac6a-143">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Remove-AzureRmSiteRecoveryReplicationProtectedItem.md)
