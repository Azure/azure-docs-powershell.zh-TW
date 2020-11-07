---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: CB1A36E9-75BE-43CF-9092-9713DFEB96F8
online version: ''
schema: 2.0.0
ms.openlocfilehash: d5329d50f87b92254136c222f406bb49586d6d7a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967034"
---
# <span data-ttu-id="f4b37-101">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="f4b37-101">Get-AzureSiteRecoveryProtectionEntity</span></span>

## <span data-ttu-id="f4b37-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f4b37-102">SYNOPSIS</span></span>
<span data-ttu-id="f4b37-103">在 Site Recovery 保存庫中取得可保護或受保護的實體。</span><span class="sxs-lookup"><span data-stu-id="f4b37-103">Gets protectable or protected entities in a Site Recovery vault.</span></span>

## <span data-ttu-id="f4b37-104">句法</span><span class="sxs-lookup"><span data-stu-id="f4b37-104">SYNTAX</span></span>

### <span data-ttu-id="f4b37-105">ByObject (預設) </span><span class="sxs-lookup"><span data-stu-id="f4b37-105">ByObject (Default)</span></span>
```
Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer <ASRProtectionContainer> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="f4b37-106">ByObjectWithId</span><span class="sxs-lookup"><span data-stu-id="f4b37-106">ByObjectWithId</span></span>
```
Get-AzureSiteRecoveryProtectionEntity -Id <String> -ProtectionContainer <ASRProtectionContainer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="f4b37-107">ByIDsWithId</span><span class="sxs-lookup"><span data-stu-id="f4b37-107">ByIDsWithId</span></span>
```
Get-AzureSiteRecoveryProtectionEntity -Id <String> -ProtectionContainerId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="f4b37-108">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="f4b37-108">ByObjectWithName</span></span>
```
Get-AzureSiteRecoveryProtectionEntity -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="f4b37-109">ByIDsWithName</span><span class="sxs-lookup"><span data-stu-id="f4b37-109">ByIDsWithName</span></span>
```
Get-AzureSiteRecoveryProtectionEntity -Name <String> -ProtectionContainerId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="f4b37-110">ByIDs</span><span class="sxs-lookup"><span data-stu-id="f4b37-110">ByIDs</span></span>
```
Get-AzureSiteRecoveryProtectionEntity -ProtectionContainerId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="f4b37-111">說明</span><span class="sxs-lookup"><span data-stu-id="f4b37-111">DESCRIPTION</span></span>
<span data-ttu-id="f4b37-112">**AzureSiteRecoveryProtectionEntity** Cmdlet 會在目前的 Azure Site Recovery 保存庫中取得可存取或受保護的實體（例如虛擬機器）。</span><span class="sxs-lookup"><span data-stu-id="f4b37-112">The **Get-AzureSiteRecoveryProtectionEntity** cmdlet gets the protectable or protected entities, such as virtual machines, in the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="f4b37-113">示例</span><span class="sxs-lookup"><span data-stu-id="f4b37-113">EXAMPLES</span></span>

### <span data-ttu-id="f4b37-114">範例1：在容器中顯示受保護的虛擬機器</span><span class="sxs-lookup"><span data-stu-id="f4b37-114">Example 1: Display a protected virtual machine in a container</span></span>
```
PS C:\> $Container = Get-AzureSiteRecoveryProtectionContainer
PS C:\> Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $Container 
ID                           : 43aaab46-1cb0-4c39-8077-9a091c3b05ce
ServerId                     : 4a94c4a9-c856-4577-afbd-367fe9b3ce9c
ProtectionContainerId        : 4a94c4a9-c856-4577-afbd-367fe9b3ce9c_1c513d45-645d-4ed0-b9ae-e7b869a1f7fc
Name                         : testvm
Type                         : VirtualMachine
FabricObjectId               : 506B3CAC-5758-49E2-98C4-E5B0512E4D8E
Protected                    : False
CanCommit                    : False
CanFailover                  : False
CanReverseReplicate          : False
ActiveLocation               : Primary
ProtectionStateDescription   : Enabling protection
ReplicationHealth            : 
TestFailoverStateDescription : Nonev
ReplicationProvider          : HyperVReplica
```

<span data-ttu-id="f4b37-115">第一個命令會使用 **AzureSiteRecoveryProtectionContainer** Cmdlet 取得受保護的容器，然後將該物件儲存在 $Container 變數中。</span><span class="sxs-lookup"><span data-stu-id="f4b37-115">The first command gets a protected container by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores that object in the $Container variable.</span></span>

<span data-ttu-id="f4b37-116">第二個命令會在 $Container 中的容器中取得受保護的虛擬機器，然後將其顯示。</span><span class="sxs-lookup"><span data-stu-id="f4b37-116">The second command gets the protected virtual machine that belongs to the container in $Container, and then displays it.</span></span>

## <span data-ttu-id="f4b37-117">參數</span><span class="sxs-lookup"><span data-stu-id="f4b37-117">PARAMETERS</span></span>

### <span data-ttu-id="f4b37-118">-識別碼</span><span class="sxs-lookup"><span data-stu-id="f4b37-118">-Id</span></span>
<span data-ttu-id="f4b37-119">指定要取得的保護實體 ID。</span><span class="sxs-lookup"><span data-stu-id="f4b37-119">Specifies the ID of a protection entity to get.</span></span>

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

### <span data-ttu-id="f4b37-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="f4b37-120">-Name</span></span>
<span data-ttu-id="f4b37-121">指定要取得的保護實體的名稱。</span><span class="sxs-lookup"><span data-stu-id="f4b37-121">Specifies the name of a protection entity to get.</span></span>

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

### <span data-ttu-id="f4b37-122">-設定檔</span><span class="sxs-lookup"><span data-stu-id="f4b37-122">-Profile</span></span>
<span data-ttu-id="f4b37-123">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="f4b37-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f4b37-124">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="f4b37-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f4b37-125">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="f4b37-125">-ProtectionContainer</span></span>
<span data-ttu-id="f4b37-126">指定保護容器。</span><span class="sxs-lookup"><span data-stu-id="f4b37-126">Specifies a protection container.</span></span>

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

### <span data-ttu-id="f4b37-127">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="f4b37-127">-ProtectionContainerId</span></span>
<span data-ttu-id="f4b37-128">指定受保護容器的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f4b37-128">Specifies the ID of a protected container.</span></span>

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

### <span data-ttu-id="f4b37-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4b37-129">CommonParameters</span></span>
<span data-ttu-id="f4b37-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f4b37-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4b37-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f4b37-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4b37-132">輸入</span><span class="sxs-lookup"><span data-stu-id="f4b37-132">INPUTS</span></span>

## <span data-ttu-id="f4b37-133">輸出</span><span class="sxs-lookup"><span data-stu-id="f4b37-133">OUTPUTS</span></span>

## <span data-ttu-id="f4b37-134">筆記</span><span class="sxs-lookup"><span data-stu-id="f4b37-134">NOTES</span></span>

## <span data-ttu-id="f4b37-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="f4b37-135">RELATED LINKS</span></span>

[<span data-ttu-id="f4b37-136">AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="f4b37-136">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="f4b37-137">Set-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="f4b37-137">Set-AzureSiteRecoveryProtectionEntity</span></span>](./Set-AzureSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="f4b37-138">更新-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="f4b37-138">Update-AzureSiteRecoveryProtectionEntity</span></span>](./Update-AzureSiteRecoveryProtectionEntity.md)


