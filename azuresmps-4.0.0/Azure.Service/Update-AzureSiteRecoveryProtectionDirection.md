---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 870EE77E-57D9-4B52-9F80-CB24D642E6E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4f94d95b40fb89f0c1df89ad0c8a9b78eb283184
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967846"
---
# <span data-ttu-id="d4f9b-101">Update-AzureSiteRecoveryProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="d4f9b-101">Update-AzureSiteRecoveryProtectionDirection</span></span>

## <span data-ttu-id="d4f9b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d4f9b-102">SYNOPSIS</span></span>
<span data-ttu-id="d4f9b-103">更新來源和目標伺服器，以保護網站恢復物件。</span><span class="sxs-lookup"><span data-stu-id="d4f9b-103">Updates the source and target server for the protection of a Site Recovery object.</span></span>

## <span data-ttu-id="d4f9b-104">句法</span><span class="sxs-lookup"><span data-stu-id="d4f9b-104">SYNTAX</span></span>

### <span data-ttu-id="d4f9b-105">ByRPObject (預設) </span><span class="sxs-lookup"><span data-stu-id="d4f9b-105">ByRPObject (Default)</span></span>
```
Update-AzureSiteRecoveryProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d4f9b-106">ByRPId</span><span class="sxs-lookup"><span data-stu-id="d4f9b-106">ByRPId</span></span>
```
Update-AzureSiteRecoveryProtectionDirection -RPId <String> -Direction <String> [-WaitForCompletion]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d4f9b-107">ByPEId</span><span class="sxs-lookup"><span data-stu-id="d4f9b-107">ByPEId</span></span>
```
Update-AzureSiteRecoveryProtectionDirection -ProtectionEntityId <String> -ProtectionContainerId <String>
 -Direction <String> [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d4f9b-108">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="d4f9b-108">ByPEObject</span></span>
```
Update-AzureSiteRecoveryProtectionDirection -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d4f9b-109">說明</span><span class="sxs-lookup"><span data-stu-id="d4f9b-109">DESCRIPTION</span></span>
<span data-ttu-id="d4f9b-110">在 commit 容錯移轉作業完成之後， **更新-AzureSiteRecoveryProtectionDirection** Cmdlet 會更新來源和目標伺服器，以保護 Azure Site Recovery 物件。</span><span class="sxs-lookup"><span data-stu-id="d4f9b-110">The **Update-AzureSiteRecoveryProtectionDirection** cmdlet updates the source and target server for the protection of an Azure Site Recovery object after a commit failover operation finishes.</span></span>

## <span data-ttu-id="d4f9b-111">示例</span><span class="sxs-lookup"><span data-stu-id="d4f9b-111">EXAMPLES</span></span>

### <span data-ttu-id="d4f9b-112">範例1：修改容器中受保護物件的方向</span><span class="sxs-lookup"><span data-stu-id="d4f9b-112">Example 1: Modify the direction for a protected object in a container</span></span>
```
PS C:\> $Container = Get-AzureSiteRecoveryProtectionContainer 
PS C:\> $Protected = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $Container  
PS C:\> Update-AzureSiteRecoveryProtectionDirection -Direction RecoveryToPrimary -ProtectionEntity $Protected 
ID               : c38eecdc-731c-405b-a61c-08db99aae2fe
ClientRequestId  : 32ace403-0916-4967-83a1-529176bd6e88-2014-49-06 15:49:24Z-P
State            : NotStarted
StateDescription : NotStarted
StartTime        : 
EndTime          : 
AllowedActions   : {}
Name             : 
Tasks            : {}
Errors           : {}
```

<span data-ttu-id="d4f9b-113">第一個命令會使用 **AzureSiteRecoveryProtectionContainer** Cmdlet 來取得目前 Azure Site Recovery 保存庫中受保護的容器，然後將其儲存在 $Container 變數中。</span><span class="sxs-lookup"><span data-stu-id="d4f9b-113">The first command gets the protected containers in the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores it in the $Container variable.</span></span>

<span data-ttu-id="d4f9b-114">第二個命令會使用 **AzureSiteRecoveryProtectionEntity** Cmdlet，來取得屬於儲存在 $Container 中之容器的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="d4f9b-114">The second command gets the virtual machines that belong to the container stored in $Container by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>
<span data-ttu-id="d4f9b-115">該命令會將結果儲存在 $Protected 變數中。</span><span class="sxs-lookup"><span data-stu-id="d4f9b-115">The command stores the results in the $Protected variable.</span></span>

<span data-ttu-id="d4f9b-116">最終命令會針對 $Protected 中儲存的物件設定 RecoverToPrimary 方向。</span><span class="sxs-lookup"><span data-stu-id="d4f9b-116">The final command sets the direction to RecoverToPrimary for the objects stored in $Protected.</span></span>

## <span data-ttu-id="d4f9b-117">參數</span><span class="sxs-lookup"><span data-stu-id="d4f9b-117">PARAMETERS</span></span>

### <span data-ttu-id="d4f9b-118">方向</span><span class="sxs-lookup"><span data-stu-id="d4f9b-118">-Direction</span></span>
<span data-ttu-id="d4f9b-119">指定認可的方向。</span><span class="sxs-lookup"><span data-stu-id="d4f9b-119">Specifies the direction of the commit.</span></span>
<span data-ttu-id="d4f9b-120">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="d4f9b-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d4f9b-121">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="d4f9b-121">PrimaryToRecovery</span></span>
- <span data-ttu-id="d4f9b-122">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="d4f9b-122">RecoveryToPrimary</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4f9b-123">-設定檔</span><span class="sxs-lookup"><span data-stu-id="d4f9b-123">-Profile</span></span>
<span data-ttu-id="d4f9b-124">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="d4f9b-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d4f9b-125">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="d4f9b-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d4f9b-126">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="d4f9b-126">-ProtectionContainerId</span></span>
<span data-ttu-id="d4f9b-127">指定受保護容器的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d4f9b-127">Specifies the ID of a protected container.</span></span>
<span data-ttu-id="d4f9b-128">這個 Cmdlet 會修改受保護的虛擬機器的方向，該電腦屬於此參數指定的容器。</span><span class="sxs-lookup"><span data-stu-id="d4f9b-128">This cmdlet modifies the direction for a protected virtual machine that belongs to the container that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByPEId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4f9b-129">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="d4f9b-129">-ProtectionEntity</span></span>
<span data-ttu-id="d4f9b-130">指定保護實體物件。</span><span class="sxs-lookup"><span data-stu-id="d4f9b-130">Specifies the protection entity object.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d4f9b-131">-ProtectionEntityId</span><span class="sxs-lookup"><span data-stu-id="d4f9b-131">-ProtectionEntityId</span></span>
<span data-ttu-id="d4f9b-132">指定受保護的虛擬機器的 ID。</span><span class="sxs-lookup"><span data-stu-id="d4f9b-132">Specifies the ID of a protected virtual machine.</span></span>
<span data-ttu-id="d4f9b-133">這個 Cmdlet 會修改此參數指定的受保護虛擬機器的方向。</span><span class="sxs-lookup"><span data-stu-id="d4f9b-133">This cmdlet modifies the direction for the protected virtual machine that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByPEId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4f9b-134">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d4f9b-134">-RecoveryPlan</span></span>
<span data-ttu-id="d4f9b-135">指定復原方案物件。</span><span class="sxs-lookup"><span data-stu-id="d4f9b-135">Specifies a recovery plan object.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d4f9b-136">-RPId</span><span class="sxs-lookup"><span data-stu-id="d4f9b-136">-RPId</span></span>
<span data-ttu-id="d4f9b-137">指定復原方案的 ID。</span><span class="sxs-lookup"><span data-stu-id="d4f9b-137">Specifies the ID of a recovery plan.</span></span>
<span data-ttu-id="d4f9b-138">這個 Cmdlet 會修改此參數指定的復原方案的方向。</span><span class="sxs-lookup"><span data-stu-id="d4f9b-138">This cmdlet modifies the direction for the recovery plan that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByRPId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4f9b-139">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="d4f9b-139">-WaitForCompletion</span></span>
<span data-ttu-id="d4f9b-140">表示 Cmdlet 在將控制權傳回給 Windows PowerShell 主控台之前，先等待該作業完成。</span><span class="sxs-lookup"><span data-stu-id="d4f9b-140">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4f9b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4f9b-141">CommonParameters</span></span>
<span data-ttu-id="d4f9b-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d4f9b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4f9b-143">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d4f9b-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4f9b-144">輸入</span><span class="sxs-lookup"><span data-stu-id="d4f9b-144">INPUTS</span></span>

## <span data-ttu-id="d4f9b-145">輸出</span><span class="sxs-lookup"><span data-stu-id="d4f9b-145">OUTPUTS</span></span>

## <span data-ttu-id="d4f9b-146">筆記</span><span class="sxs-lookup"><span data-stu-id="d4f9b-146">NOTES</span></span>

## <span data-ttu-id="d4f9b-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="d4f9b-147">RELATED LINKS</span></span>

[<span data-ttu-id="d4f9b-148">AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d4f9b-148">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="d4f9b-149">AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="d4f9b-149">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)


