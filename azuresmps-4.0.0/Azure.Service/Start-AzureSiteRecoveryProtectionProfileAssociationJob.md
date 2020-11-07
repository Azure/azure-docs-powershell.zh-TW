---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: CB5E1419-C4C7-4524-ACCC-13C9D9CCA621
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4955bfa121d6742903dd2ca99721186c7c860004
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967294"
---
# <span data-ttu-id="baa82-101">Start-AzureSiteRecoveryProtectionProfileAssociationJob</span><span class="sxs-lookup"><span data-stu-id="baa82-101">Start-AzureSiteRecoveryProtectionProfileAssociationJob</span></span>

## <span data-ttu-id="baa82-102">摘要</span><span class="sxs-lookup"><span data-stu-id="baa82-102">SYNOPSIS</span></span>
<span data-ttu-id="baa82-103">啟動網站恢復複製原則關聯作業。</span><span class="sxs-lookup"><span data-stu-id="baa82-103">Starts a Site Recovery replication policy association job.</span></span>

## <span data-ttu-id="baa82-104">句法</span><span class="sxs-lookup"><span data-stu-id="baa82-104">SYNTAX</span></span>

### <span data-ttu-id="baa82-105">EnterpriseToAzure (預設) </span><span class="sxs-lookup"><span data-stu-id="baa82-105">EnterpriseToAzure (Default)</span></span>
```
Start-AzureSiteRecoveryProtectionProfileAssociationJob -ProtectionProfile <ASRProtectionProfile>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="baa82-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="baa82-106">EnterpriseToEnterprise</span></span>
```
Start-AzureSiteRecoveryProtectionProfileAssociationJob -ProtectionProfile <ASRProtectionProfile>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="baa82-107">說明</span><span class="sxs-lookup"><span data-stu-id="baa82-107">DESCRIPTION</span></span>
<span data-ttu-id="baa82-108">**AzureSiteRecoveryProtectionProfileAssociationJob** Cmdlet 會啟動關聯作業，以將複製原則與 Azure Site Recovery 保護容器產生關聯。</span><span class="sxs-lookup"><span data-stu-id="baa82-108">The **Start-AzureSiteRecoveryProtectionProfileAssociationJob** cmdlet initiates an association job to associate a replication policy with an Azure Site Recovery protection container.</span></span>

## <span data-ttu-id="baa82-109">示例</span><span class="sxs-lookup"><span data-stu-id="baa82-109">EXAMPLES</span></span>

### <span data-ttu-id="baa82-110">範例1：關聯保護設定檔</span><span class="sxs-lookup"><span data-stu-id="baa82-110">Example 1: Associate a protection profile</span></span>
```
PS C:\> $ProtectionContainer01 = Get-AzureSiteRecoveryProtectionContainer -Id "5ba2ea95-856d-4033-9ca3-91e3e2c080b9"
PS C:\> $ProtectionProfile = New-AzureSiteRecoveryProtectionProfileObject -ReplicationProvider "HyperVReplica" -AllowReplicaDeletion -ApplicationConsistentSnapshotFrequencyInHours 1 -CompressionEnabled -RecoveryPoints 2 -ReplicationFrequencyInSeconds 30 -ReplicationMethod "Online" -ReplicationPort 8085 -ReplicationStartTime 1
PS C:\> $ProtectionContainer02 = Get-AzureSiteRecoveryProtectionContainer -Id "cf011f2a-aa19-443c-9f60-357f6b8afb77"
PS C:\> Start-AzureSiteRecoveryProtectionProfileAssociationJob -PrimaryProtectionContainer $ProtectionContainer01 -ProtectionProfile $ProtectionProfile -RecoveryProtectionContainer $ProtectionContainer02
Name             : MyProtectionProfile
ID               : 51978b0f-9241-4153-9171-2e19344f0805
ClientRequestId  : bb6f3200-b7c6-4c6f-bcbc-a70bb9946f03-2015-01-27 22:55:55Z-P
State            : InProgress
StateDescription : InProgress
StartTime        : 1/27/2015 10:56:01 PM
EndTime          : 
AllowedActions   : 
Tasks            : {Adding the protection group, Configuring Windows Server 2012 R2 Hyper-V hosts for Azure}
Errors           : {}
```

<span data-ttu-id="baa82-111">第一個命令會使用 **AzureSiteRecoveryProtectionContainer** Cmdlet 取得保護容器，然後將該容器儲存在 $ProtectionContainer 01 變數中。</span><span class="sxs-lookup"><span data-stu-id="baa82-111">The first command gets a protection container by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores that container in the $ProtectionContainer01 variable.</span></span>

<span data-ttu-id="baa82-112">第二個命令會使用 **新的 AzureSiteRecoveryProtectionProfileObject** Cmdlet 來建立保護設定檔，並將該保護設定檔儲存在 $ProtectionProfile 變數中。</span><span class="sxs-lookup"><span data-stu-id="baa82-112">The second command creates a protection profile by using the **New-AzureSiteRecoveryProtectionProfileObject** cmdlet, and stores that protection profile in the $ProtectionProfile variable.</span></span>

<span data-ttu-id="baa82-113">第三個命令會取得保護容器，然後將它儲存在 $ProtectionContainer 02 變數中。</span><span class="sxs-lookup"><span data-stu-id="baa82-113">The third command gets a protection container, and then stores it in the $ProtectionContainer02 variable.</span></span>

<span data-ttu-id="baa82-114">最後一個命令會將儲存在 $ProtectionProfile 中的保護設定檔與 $ProtectionContainer 01 中儲存為主要保護容器的容器相關聯。</span><span class="sxs-lookup"><span data-stu-id="baa82-114">The final command associates the protection profile stored in $ProtectionProfile to the container stored in $ProtectionContainer01 as the primary protection container.</span></span>
<span data-ttu-id="baa82-115">該命令會將儲存在 $ProtectionContainer 02 中的容器與復原保護容器進行關聯。</span><span class="sxs-lookup"><span data-stu-id="baa82-115">The command associates the container stored in $ProtectionContainer02 as the recovery protection container.</span></span>

## <span data-ttu-id="baa82-116">參數</span><span class="sxs-lookup"><span data-stu-id="baa82-116">PARAMETERS</span></span>

### <span data-ttu-id="baa82-117">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="baa82-117">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="baa82-118">指定要套用保護設定檔設定的主要保護容器。</span><span class="sxs-lookup"><span data-stu-id="baa82-118">Specifies the primary protection container on which to apply the protection profile settings.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baa82-119">-設定檔</span><span class="sxs-lookup"><span data-stu-id="baa82-119">-Profile</span></span>
<span data-ttu-id="baa82-120">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="baa82-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="baa82-121">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="baa82-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baa82-122">-ProtectionProfile</span><span class="sxs-lookup"><span data-stu-id="baa82-122">-ProtectionProfile</span></span>
<span data-ttu-id="baa82-123">指定要套用至保護容器的保護設定檔設定。</span><span class="sxs-lookup"><span data-stu-id="baa82-123">Specifies the protection profile settings to apply to the protection containers.</span></span>
<span data-ttu-id="baa82-124">若要取得 **ASRProtectionProfile** 物件，請使用 New-AzureSiteRecoveryProtectionProfileObject Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="baa82-124">To obtain an **ASRProtectionProfile** object, use the New-AzureSiteRecoveryProtectionProfileObject cmdlet.</span></span>

```yaml
Type: ASRProtectionProfile
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="baa82-125">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="baa82-125">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="baa82-126">指定要套用保護設定檔設定的復原保護容器。</span><span class="sxs-lookup"><span data-stu-id="baa82-126">Specifies the recovery protection container on which to apply the protection profile settings.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baa82-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baa82-127">CommonParameters</span></span>
<span data-ttu-id="baa82-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="baa82-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baa82-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="baa82-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baa82-130">輸入</span><span class="sxs-lookup"><span data-stu-id="baa82-130">INPUTS</span></span>

## <span data-ttu-id="baa82-131">輸出</span><span class="sxs-lookup"><span data-stu-id="baa82-131">OUTPUTS</span></span>

## <span data-ttu-id="baa82-132">筆記</span><span class="sxs-lookup"><span data-stu-id="baa82-132">NOTES</span></span>

## <span data-ttu-id="baa82-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="baa82-133">RELATED LINKS</span></span>

[<span data-ttu-id="baa82-134">AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="baa82-134">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="baa82-135">新-AzureSiteRecoveryProtectionProfileObject</span><span class="sxs-lookup"><span data-stu-id="baa82-135">New-AzureSiteRecoveryProtectionProfileObject</span></span>](./New-AzureSiteRecoveryProtectionProfileObject.md)

[<span data-ttu-id="baa82-136">開始-AzureSiteRecoveryProtectionProfileDissociationJob</span><span class="sxs-lookup"><span data-stu-id="baa82-136">Start-AzureSiteRecoveryProtectionProfileDissociationJob</span></span>](./Start-AzureSiteRecoveryProtectionProfileDissociationJob.md)


