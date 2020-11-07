---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 185506BC-6155-4517-BCBD-BCDE7450C7A8
online version: ''
schema: 2.0.0
ms.openlocfilehash: f8017c2947a8d046226a63b5ed07b3714c35b22c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967856"
---
# <span data-ttu-id="20342-101">Start-AzureSiteRecoveryProtectionProfileDissociationJob</span><span class="sxs-lookup"><span data-stu-id="20342-101">Start-AzureSiteRecoveryProtectionProfileDissociationJob</span></span>

## <span data-ttu-id="20342-102">摘要</span><span class="sxs-lookup"><span data-stu-id="20342-102">SYNOPSIS</span></span>
<span data-ttu-id="20342-103">在與網站復原保護容器相關聯的複寫原則上啟動 dissociation 作業。</span><span class="sxs-lookup"><span data-stu-id="20342-103">Starts a dissociation job on a replication policy associated with a Site Recovery protection container.</span></span>

## <span data-ttu-id="20342-104">句法</span><span class="sxs-lookup"><span data-stu-id="20342-104">SYNTAX</span></span>

### <span data-ttu-id="20342-105">EnterpriseToAzure (預設) </span><span class="sxs-lookup"><span data-stu-id="20342-105">EnterpriseToAzure (Default)</span></span>
```
Start-AzureSiteRecoveryProtectionProfileDissociationJob -ProtectionProfile <ASRProtectionProfile>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="20342-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="20342-106">EnterpriseToEnterprise</span></span>
```
Start-AzureSiteRecoveryProtectionProfileDissociationJob -ProtectionProfile <ASRProtectionProfile>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="20342-107">說明</span><span class="sxs-lookup"><span data-stu-id="20342-107">DESCRIPTION</span></span>
<span data-ttu-id="20342-108">**AzureSiteRecoveryProtectionProfileDissociationJob** Cmdlet 會在與 Azure Site Recovery 保護容器相關聯的複寫原則上啟動 dissociation 作業。</span><span class="sxs-lookup"><span data-stu-id="20342-108">The **Start-AzureSiteRecoveryProtectionProfileDissociationJob** cmdlet initiates a dissociation job on the replication policy associated with an Azure Site Recovery protection container.</span></span>

## <span data-ttu-id="20342-109">示例</span><span class="sxs-lookup"><span data-stu-id="20342-109">EXAMPLES</span></span>

### <span data-ttu-id="20342-110">範例1：取消保護設定檔的關聯</span><span class="sxs-lookup"><span data-stu-id="20342-110">Example 1: Dissociate a protection profile</span></span>
```
PS C:\> $ProtectionContainer01 = Get-AzureSiteRecoveryProtectionContainer -Id "5ba2ea95-856d-4033-9ca3-91e3e2c080b9"
PS C:\> $ProtectionContainer02 = Get-AzureSiteRecoveryProtectionContainer -Id "cf011f2a-aa19-443c-9f60-357f6b8afb77"
PS C:\> Start-AzureSiteRecoveryProtectionProfileDissociationJob -PrimaryProtectionContainer $ProtectionContainer01 -ProtectionProfile $ProtectionContainer01.AvailableProtectionProfiles[0] -RecoveryProtectionContainer $ProtectionContainer02
Name             : MyProtectionProfile
ID               : 51978b0f-9241-4153-9171-2e19344f0805
ClientRequestId  : bb6f3200-b7c6-4c6f-bcbc-a70bb9946f03-2015-01-30 02:55:55Z-P
State            : NotStarted
StateDescription : NotStarted
StartTime        : 
EndTime          : 
AllowedActions   : 
Tasks            : {}
Errors           : {}
```

<span data-ttu-id="20342-111">第一個命令會使用 **AzureSiteRecoveryProtectionContainer** Cmdlet 取得保護容器，然後將該容器儲存在 $ProtectionContainer 01 變數中。</span><span class="sxs-lookup"><span data-stu-id="20342-111">The first command gets a protection container by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores that container in the $ProtectionContainer01 variable.</span></span>

<span data-ttu-id="20342-112">第二個命令會取得保護容器，然後將它儲存在 $ProtectionContainer 02 變數中。</span><span class="sxs-lookup"><span data-stu-id="20342-112">The second command gets a protection container, and then stores it in the $ProtectionContainer02 variable.</span></span>

<span data-ttu-id="20342-113">最終的命令會從儲存在 $ProtectionContainer 01 中的容器中，將保護設定檔 dissociates 為主要保護容器。</span><span class="sxs-lookup"><span data-stu-id="20342-113">The final command dissociates the protection profile from the container stored in $ProtectionContainer01 as the primary protection container.</span></span>
<span data-ttu-id="20342-114">此命令會 dissociates 儲存在 $ProtectionContainer 02 中作為復原保護容器的容器。</span><span class="sxs-lookup"><span data-stu-id="20342-114">The command dissociates the container stored in $ProtectionContainer02 as the recovery protection container.</span></span>

## <span data-ttu-id="20342-115">參數</span><span class="sxs-lookup"><span data-stu-id="20342-115">PARAMETERS</span></span>

### <span data-ttu-id="20342-116">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="20342-116">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="20342-117">指定主要保護容器。</span><span class="sxs-lookup"><span data-stu-id="20342-117">Specifies a primary protection container.</span></span>

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

### <span data-ttu-id="20342-118">-設定檔</span><span class="sxs-lookup"><span data-stu-id="20342-118">-Profile</span></span>
<span data-ttu-id="20342-119">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="20342-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="20342-120">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="20342-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="20342-121">-ProtectionProfile</span><span class="sxs-lookup"><span data-stu-id="20342-121">-ProtectionProfile</span></span>
<span data-ttu-id="20342-122">指定要解除與保護容器關聯的保護設定檔設定。</span><span class="sxs-lookup"><span data-stu-id="20342-122">Specifies the protection profile settings to disassociate from the protection containers.</span></span>
<span data-ttu-id="20342-123">指定要套用至保護容器的保護設定檔設定。</span><span class="sxs-lookup"><span data-stu-id="20342-123">Specifies the protection profile settings to apply to the protection containers.</span></span>
<span data-ttu-id="20342-124">若要取得 **ASRProtectionProfile** 物件，請使用 New-AzureSiteRecoveryProtectionProfileObject Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="20342-124">To obtain an **ASRProtectionProfile** object, use the New-AzureSiteRecoveryProtectionProfileObject cmdlet.</span></span>

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

### <span data-ttu-id="20342-125">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="20342-125">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="20342-126">指定復原保護容器。</span><span class="sxs-lookup"><span data-stu-id="20342-126">Specifies a recovery protection container.</span></span>

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

### <span data-ttu-id="20342-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20342-127">CommonParameters</span></span>
<span data-ttu-id="20342-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="20342-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20342-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="20342-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20342-130">輸入</span><span class="sxs-lookup"><span data-stu-id="20342-130">INPUTS</span></span>

## <span data-ttu-id="20342-131">輸出</span><span class="sxs-lookup"><span data-stu-id="20342-131">OUTPUTS</span></span>

## <span data-ttu-id="20342-132">筆記</span><span class="sxs-lookup"><span data-stu-id="20342-132">NOTES</span></span>

## <span data-ttu-id="20342-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="20342-133">RELATED LINKS</span></span>

[<span data-ttu-id="20342-134">AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="20342-134">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="20342-135">新-AzureSiteRecoveryProtectionProfileObject</span><span class="sxs-lookup"><span data-stu-id="20342-135">New-AzureSiteRecoveryProtectionProfileObject</span></span>](./New-AzureSiteRecoveryProtectionProfileObject.md)

[<span data-ttu-id="20342-136">開始-AzureSiteRecoveryProtectionProfileAssociationJob</span><span class="sxs-lookup"><span data-stu-id="20342-136">Start-AzureSiteRecoveryProtectionProfileAssociationJob</span></span>](./Start-AzureSiteRecoveryProtectionProfileAssociationJob.md)


