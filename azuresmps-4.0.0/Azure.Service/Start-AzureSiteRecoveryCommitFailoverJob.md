---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 44A22B6C-5FD4-43B0-9726-71E28AE53E9D
online version: ''
schema: 2.0.0
ms.openlocfilehash: de1b7a24c1af362297319d0297ce356b00ef9d49
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967224"
---
# <span data-ttu-id="54bce-101">Start-AzureSiteRecoveryCommitFailoverJob</span><span class="sxs-lookup"><span data-stu-id="54bce-101">Start-AzureSiteRecoveryCommitFailoverJob</span></span>

## <span data-ttu-id="54bce-102">摘要</span><span class="sxs-lookup"><span data-stu-id="54bce-102">SYNOPSIS</span></span>
<span data-ttu-id="54bce-103">啟動針對網站復原物件的 [確認容錯移轉] 動作。</span><span class="sxs-lookup"><span data-stu-id="54bce-103">Starts the commit failover action for a Site Recovery object.</span></span>

## <span data-ttu-id="54bce-104">句法</span><span class="sxs-lookup"><span data-stu-id="54bce-104">SYNTAX</span></span>

### <span data-ttu-id="54bce-105">ByRPId (預設) </span><span class="sxs-lookup"><span data-stu-id="54bce-105">ByRPId (Default)</span></span>
```
Start-AzureSiteRecoveryCommitFailoverJob -RPId <String> [-Direction <String>] [-WaitForCompletion]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="54bce-106">ByPEId</span><span class="sxs-lookup"><span data-stu-id="54bce-106">ByPEId</span></span>
```
Start-AzureSiteRecoveryCommitFailoverJob -ProtectionEntityId <String> -ProtectionContainerId <String>
 [-Direction <String>] [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="54bce-107">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="54bce-107">ByRPObject</span></span>
```
Start-AzureSiteRecoveryCommitFailoverJob -RecoveryPlan <ASRRecoveryPlan> [-Direction <String>]
 [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="54bce-108">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="54bce-108">ByPEObject</span></span>
```
Start-AzureSiteRecoveryCommitFailoverJob -ProtectionEntity <ASRProtectionEntity> [-Direction <String>]
 [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="54bce-109">說明</span><span class="sxs-lookup"><span data-stu-id="54bce-109">DESCRIPTION</span></span>
<span data-ttu-id="54bce-110">在容錯移轉作業之後， **Start AzureSiteRecoveryCommitFailoverJob** Cmdlet 會啟動 Azure Site Recovery 物件的 commit 容錯移轉進程。</span><span class="sxs-lookup"><span data-stu-id="54bce-110">The **Start-AzureSiteRecoveryCommitFailoverJob** cmdlet starts the commit failover process for an Azure Site Recovery object after a failover operation.</span></span>

## <span data-ttu-id="54bce-111">示例</span><span class="sxs-lookup"><span data-stu-id="54bce-111">EXAMPLES</span></span>

### <span data-ttu-id="54bce-112">範例1：啟動認可容錯移轉作業</span><span class="sxs-lookup"><span data-stu-id="54bce-112">Example 1: Start a commit failover job</span></span>
```
PS C:\> $Container = Get-AzureSiteRecoveryProtectionContainer 
PS C:\> $Protected = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $Container 
PS C:\> Start-AzureSiteRecoveryCommitFailoverJob -ProtectionEntity $Protected
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

<span data-ttu-id="54bce-113">第一個命令會使用 **AzureSiteRecoveryProtectionContainer** Cmdlet 來取得目前 Azure Site Recovery 保存庫的所有受保護容器，然後將結果儲存在 $Container 變數中。</span><span class="sxs-lookup"><span data-stu-id="54bce-113">The first command gets all protected containers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores the results in the $Container variable.</span></span>

<span data-ttu-id="54bce-114">第二個命令會使用 **AzureSiteRecoveryProtectionEntity** Cmdlet，來取得屬於儲存在 $Container 中之容器的受保護虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="54bce-114">The second command gets the protected virtual machines that belong to the container stored in $Container by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>
<span data-ttu-id="54bce-115">該命令會將結果儲存在 $Protected 變數中。</span><span class="sxs-lookup"><span data-stu-id="54bce-115">The command stores the results in the $Protected variable.</span></span>

<span data-ttu-id="54bce-116">最終命令會針對儲存在 $Protected 中的受保護物件啟動容錯移轉作業。</span><span class="sxs-lookup"><span data-stu-id="54bce-116">The final command starts the failover job for the protected objects stored in $Protected.</span></span>

## <span data-ttu-id="54bce-117">參數</span><span class="sxs-lookup"><span data-stu-id="54bce-117">PARAMETERS</span></span>

### <span data-ttu-id="54bce-118">方向</span><span class="sxs-lookup"><span data-stu-id="54bce-118">-Direction</span></span>
<span data-ttu-id="54bce-119">指定容錯移轉的方向。</span><span class="sxs-lookup"><span data-stu-id="54bce-119">Specifies the direction of the failover.</span></span>
<span data-ttu-id="54bce-120">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="54bce-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="54bce-121">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="54bce-121">PrimaryToRecovery</span></span>
- <span data-ttu-id="54bce-122">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="54bce-122">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="54bce-123">-設定檔</span><span class="sxs-lookup"><span data-stu-id="54bce-123">-Profile</span></span>
<span data-ttu-id="54bce-124">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="54bce-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="54bce-125">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="54bce-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="54bce-126">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="54bce-126">-ProtectionContainerId</span></span>
<span data-ttu-id="54bce-127">指定受保護容器的識別碼。</span><span class="sxs-lookup"><span data-stu-id="54bce-127">Specifies the ID of a protected container.</span></span>
<span data-ttu-id="54bce-128">這個 Cmdlet 會針對屬於這個 Cmdlet 所指定容器的受保護虛擬機器啟動作業。</span><span class="sxs-lookup"><span data-stu-id="54bce-128">This cmdlet starts the job for a protected virtual machine that belongs to the container that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="54bce-129">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="54bce-129">-ProtectionEntity</span></span>
<span data-ttu-id="54bce-130">指定要開始作業的 **ASRProtectionEntity** 物件。</span><span class="sxs-lookup"><span data-stu-id="54bce-130">Specifies an **ASRProtectionEntity** object for which to start the job.</span></span>
<span data-ttu-id="54bce-131">若要取得 **ASRProtectionEntity** 物件，請使用 **AzureSiteRecoveryProtectionEntity** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="54bce-131">To obtain an **ASRProtectionEntity** object, use the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>

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

### <span data-ttu-id="54bce-132">-ProtectionEntityId</span><span class="sxs-lookup"><span data-stu-id="54bce-132">-ProtectionEntityId</span></span>
<span data-ttu-id="54bce-133">指定要啟動作業之受保護虛擬機器的識別碼。</span><span class="sxs-lookup"><span data-stu-id="54bce-133">Specifies the ID of a protected virtual machine for which to start the job.</span></span>

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

### <span data-ttu-id="54bce-134">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="54bce-134">-RecoveryPlan</span></span>
<span data-ttu-id="54bce-135">指定要啟動作業的復原方案物件。</span><span class="sxs-lookup"><span data-stu-id="54bce-135">Specifies a recovery plan object for which to start the job.</span></span>
<span data-ttu-id="54bce-136">若要取得 **ASRRecoveryPlan** 物件，請使用 **AzureSiteRecoveryRecoveryPlan** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="54bce-136">To obtain an **ASRRecoveryPlan** object, use the **Get-AzureSiteRecoveryRecoveryPlan** cmdlet.</span></span>

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

### <span data-ttu-id="54bce-137">-RPId</span><span class="sxs-lookup"><span data-stu-id="54bce-137">-RPId</span></span>
<span data-ttu-id="54bce-138">指定要開始作業的復原方案識別碼。</span><span class="sxs-lookup"><span data-stu-id="54bce-138">Specifies the ID of a recovery plan for which to start the job.</span></span>

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

### <span data-ttu-id="54bce-139">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="54bce-139">-WaitForCompletion</span></span>
<span data-ttu-id="54bce-140">表示 Cmdlet 在將控制權傳回給 Windows PowerShell 主控台之前，先等待該作業完成。</span><span class="sxs-lookup"><span data-stu-id="54bce-140">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="54bce-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54bce-141">CommonParameters</span></span>
<span data-ttu-id="54bce-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="54bce-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54bce-143">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="54bce-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54bce-144">輸入</span><span class="sxs-lookup"><span data-stu-id="54bce-144">INPUTS</span></span>

## <span data-ttu-id="54bce-145">輸出</span><span class="sxs-lookup"><span data-stu-id="54bce-145">OUTPUTS</span></span>

## <span data-ttu-id="54bce-146">筆記</span><span class="sxs-lookup"><span data-stu-id="54bce-146">NOTES</span></span>

## <span data-ttu-id="54bce-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="54bce-147">RELATED LINKS</span></span>

[<span data-ttu-id="54bce-148">AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="54bce-148">Get-AzureSiteRecoveryRecoveryPlan</span></span>](./Get-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="54bce-149">AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="54bce-149">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="54bce-150">AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="54bce-150">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)


