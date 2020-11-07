---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: CE15E01D-5D86-4960-8E37-7757B35F4464
online version: ''
schema: 2.0.0
ms.openlocfilehash: a87a825249d7d7cda3fc2dc43a93869f8d869705
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93968015"
---
# <span data-ttu-id="da460-101">Get-AzureSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="da460-101">Get-AzureSiteRecoveryVM</span></span>

## <span data-ttu-id="da460-102">摘要</span><span class="sxs-lookup"><span data-stu-id="da460-102">SYNOPSIS</span></span>
<span data-ttu-id="da460-103">取得網站復原管理的虛擬機器的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="da460-103">Gets information about Site Recovery-managed virtual machines.</span></span>

## <span data-ttu-id="da460-104">句法</span><span class="sxs-lookup"><span data-stu-id="da460-104">SYNTAX</span></span>

### <span data-ttu-id="da460-105">ByObject (預設) </span><span class="sxs-lookup"><span data-stu-id="da460-105">ByObject (Default)</span></span>
```
Get-AzureSiteRecoveryVM -ProtectionContainer <ASRProtectionContainer> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="da460-106">ByObjectWithId</span><span class="sxs-lookup"><span data-stu-id="da460-106">ByObjectWithId</span></span>
```
Get-AzureSiteRecoveryVM -Id <String> -ProtectionContainer <ASRProtectionContainer> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="da460-107">ByIDsWithId</span><span class="sxs-lookup"><span data-stu-id="da460-107">ByIDsWithId</span></span>
```
Get-AzureSiteRecoveryVM -Id <String> -ProtectionContainerId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="da460-108">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="da460-108">ByObjectWithName</span></span>
```
Get-AzureSiteRecoveryVM -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="da460-109">ByIDsWithName</span><span class="sxs-lookup"><span data-stu-id="da460-109">ByIDsWithName</span></span>
```
Get-AzureSiteRecoveryVM -Name <String> -ProtectionContainerId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="da460-110">ByIDs</span><span class="sxs-lookup"><span data-stu-id="da460-110">ByIDs</span></span>
```
Get-AzureSiteRecoveryVM -ProtectionContainerId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="da460-111">說明</span><span class="sxs-lookup"><span data-stu-id="da460-111">DESCRIPTION</span></span>
<span data-ttu-id="da460-112">**AzureSiteRecoveryVM** Cmdlet 會取得 Azure Site Recovery 中管理的虛擬機器相關資訊。</span><span class="sxs-lookup"><span data-stu-id="da460-112">The **Get-AzureSiteRecoveryVM** cmdlet gets information about virtual machines managed in Azure Site Recovery.</span></span>

## <span data-ttu-id="da460-113">示例</span><span class="sxs-lookup"><span data-stu-id="da460-113">EXAMPLES</span></span>

### <span data-ttu-id="da460-114">範例1：取得有關虛擬機器的資訊</span><span class="sxs-lookup"><span data-stu-id="da460-114">Example 1: Get information about a virtual machine</span></span>
```
PS C:\> $ProtectionContainer = Get-AzureSiteRecoveryProtectionContainer
PS C:\> Get-AzureSiteRecoveryVM -ProtectionContainer $ProtectionContainer
ID                          : a205fd17-3848-4896-bab6-9dbccc3cd8ed
ServerId                    : 4a94c4a9-c856-4577-afbd-367fe9b3ce9c
ProtectionContainerId       : 4a94c4a9-c856-4577-afbd-367fe9b3ce9c_1c513d45-645d-4ed0-b9ae-e7b869a1f7fc
Name                        : vm1
Type                        : VirtualMachine
FabricObjectId              : 86447b9e-d877-4e9a-8302-adcd6bbf18c0
Protected                   : False
CanCommit                   : False
CanFailover                 : True
CanReverseReplicate         : False
ActiveLocation              : Primary
ProtectionState             : Enabled
ReplicationHealth           : Healthy
TestFailoverState           : None
ReplicationProvider         : HyperVReplica
```

<span data-ttu-id="da460-115">第一個命令使用 **AzureSiteRecoveryProtectionContainer** Cmdlet 來取得受保護的容器，然後將它儲存在 $ProtectionContainer 變數中。</span><span class="sxs-lookup"><span data-stu-id="da460-115">The first command uses the **Get-AzureSiteRecoveryProtectionContainer** cmdlet to get a protected container, and then stores it in the $ProtectionContainer variable.</span></span>

<span data-ttu-id="da460-116">第二個命令會在 $ProtectionContainer 中取得虛擬電腦的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="da460-116">The second command gets information about the virtual machines in $ProtectionContainer.</span></span>

## <span data-ttu-id="da460-117">參數</span><span class="sxs-lookup"><span data-stu-id="da460-117">PARAMETERS</span></span>

### <span data-ttu-id="da460-118">-識別碼</span><span class="sxs-lookup"><span data-stu-id="da460-118">-Id</span></span>
<span data-ttu-id="da460-119">指定要取得資訊的虛擬機器識別碼。</span><span class="sxs-lookup"><span data-stu-id="da460-119">Specifies the ID of the virtual machine about which to get information.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithId, ByIDsWithId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da460-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="da460-120">-Name</span></span>
<span data-ttu-id="da460-121">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="da460-121">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName, ByIDsWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da460-122">-設定檔</span><span class="sxs-lookup"><span data-stu-id="da460-122">-Profile</span></span>
<span data-ttu-id="da460-123">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="da460-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="da460-124">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="da460-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="da460-125">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="da460-125">-ProtectionContainer</span></span>
<span data-ttu-id="da460-126">指定網站復原保護容器物件。</span><span class="sxs-lookup"><span data-stu-id="da460-126">Specifies the Site Recovery protection container object.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: ASRProtectionContainer
Parameter Sets: ByObjectWithId, ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da460-127">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="da460-127">-ProtectionContainerId</span></span>
<span data-ttu-id="da460-128">指定要取得資訊之受保護容器的識別碼。</span><span class="sxs-lookup"><span data-stu-id="da460-128">Specifies the ID of a protected container about which to get information.</span></span>

```yaml
Type: String
Parameter Sets: ByIDsWithId, ByIDsWithName, ByIDs
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da460-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da460-129">CommonParameters</span></span>
<span data-ttu-id="da460-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="da460-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da460-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="da460-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da460-132">輸入</span><span class="sxs-lookup"><span data-stu-id="da460-132">INPUTS</span></span>

## <span data-ttu-id="da460-133">輸出</span><span class="sxs-lookup"><span data-stu-id="da460-133">OUTPUTS</span></span>

## <span data-ttu-id="da460-134">筆記</span><span class="sxs-lookup"><span data-stu-id="da460-134">NOTES</span></span>

## <span data-ttu-id="da460-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="da460-135">RELATED LINKS</span></span>

[<span data-ttu-id="da460-136">Set-AzureSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="da460-136">Set-AzureSiteRecoveryVM</span></span>](./Set-AzureSiteRecoveryVM.md)


