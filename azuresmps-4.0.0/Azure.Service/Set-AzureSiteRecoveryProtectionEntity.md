---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 1415BBA3-3F55-46A9-B20B-DFA72342BDF4
online version: ''
schema: 2.0.0
ms.openlocfilehash: ec7883b996e5da367884fd7d051a5299c6d62a9e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967869"
---
# <span data-ttu-id="145db-101">Set-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="145db-101">Set-AzureSiteRecoveryProtectionEntity</span></span>

## <span data-ttu-id="145db-102">摘要</span><span class="sxs-lookup"><span data-stu-id="145db-102">SYNOPSIS</span></span>
<span data-ttu-id="145db-103">設定網站恢復保護實體的狀態。</span><span class="sxs-lookup"><span data-stu-id="145db-103">Sets the state for a Site Recovery protection entity.</span></span>

## <span data-ttu-id="145db-104">句法</span><span class="sxs-lookup"><span data-stu-id="145db-104">SYNTAX</span></span>

### <span data-ttu-id="145db-105">ByPEObject (預設) </span><span class="sxs-lookup"><span data-stu-id="145db-105">ByPEObject (Default)</span></span>
```
Set-AzureSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity>
 [-ProtectionProfile <ASRProtectionProfile>] -Protection <String> [-OSDiskName <String>] [-OS <String>]
 [-WaitForCompletion] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="145db-106">ByIDs</span><span class="sxs-lookup"><span data-stu-id="145db-106">ByIDs</span></span>
```
Set-AzureSiteRecoveryProtectionEntity -Id <String> -ProtectionContainerId <String>
 [-ProtectionProfile <ASRProtectionProfile>] -Protection <String> [-OSDiskName <String>] [-OS <String>]
 [-WaitForCompletion] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="145db-107">說明</span><span class="sxs-lookup"><span data-stu-id="145db-107">DESCRIPTION</span></span>
<span data-ttu-id="145db-108">**AzureSiteRecoveryProtectionEntity** Cmdlet 可啟用或停用 Azure Site Recovery 保護實體的保護。</span><span class="sxs-lookup"><span data-stu-id="145db-108">The **Set-AzureSiteRecoveryProtectionEntity** cmdlet enables or disables protection on an Azure Site Recovery protection entity.</span></span>

## <span data-ttu-id="145db-109">示例</span><span class="sxs-lookup"><span data-stu-id="145db-109">EXAMPLES</span></span>

### <span data-ttu-id="145db-110">範例1：針對容器中的物件啟用保護</span><span class="sxs-lookup"><span data-stu-id="145db-110">Example 1: Enable protection for objects in a container</span></span>
```
PS C:\> $ProtectionContainer = Get-AzureSiteRecoveryProtectionContainer -Name "Cloud17"
PS C:\> $ProtectionEntity = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $ProtectionContainer -Name "VM01"
PS C:\> Set-AzureSiteRecoveryProtectionEntity -ProtectionEntity $ ProtectionEntity -Protection Enable -ProtectionProfile $ProtectionContainer.AvailableProtectionProfiles[0] -OS Windows
```

<span data-ttu-id="145db-111">第一個命令會使用 **AzureSiteRecoveryProtectionContainer** Cmdlet 取得目前 Azure 網站電子倉庫的容器，然後將它儲存在 $ProtectionContainer 變數中。</span><span class="sxs-lookup"><span data-stu-id="145db-111">The first command gets containers for the current Azure Site vault by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores it in the $ProtectionContainer variable.</span></span>

<span data-ttu-id="145db-112">第二個命令會使用 **AzureSiteRecoveryProtectionEntity** Cmdlet，來取得屬於儲存在 $ProtectionContainer 中之容器的受保護虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="145db-112">The second command gets the protected virtual machines that belong to the container stored in $ProtectionContainer by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>
<span data-ttu-id="145db-113">該命令會將結果儲存在 $ProtectionEntity 變數中。</span><span class="sxs-lookup"><span data-stu-id="145db-113">The command stores the results in the $ProtectionEntity variable.</span></span>

<span data-ttu-id="145db-114">最後一個命令會針對儲存在 $ProtectionEntity 中的實體啟用保護功能。</span><span class="sxs-lookup"><span data-stu-id="145db-114">The final command enables protection for the entities stored in $ProtectionEntity.</span></span>

## <span data-ttu-id="145db-115">參數</span><span class="sxs-lookup"><span data-stu-id="145db-115">PARAMETERS</span></span>

### <span data-ttu-id="145db-116">-Force</span><span class="sxs-lookup"><span data-stu-id="145db-116">-Force</span></span>
<span data-ttu-id="145db-117">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="145db-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="145db-118">-識別碼</span><span class="sxs-lookup"><span data-stu-id="145db-118">-Id</span></span>
<span data-ttu-id="145db-119">指定要啟用或停用保護的受保護虛擬機器的識別碼。</span><span class="sxs-lookup"><span data-stu-id="145db-119">Specifies the ID of a protected virtual machine for which to enable or disable protection.</span></span>

```yaml
Type: String
Parameter Sets: ByIDs
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="145db-120">-OS</span><span class="sxs-lookup"><span data-stu-id="145db-120">-OS</span></span>
<span data-ttu-id="145db-121">指定作業系統類型。</span><span class="sxs-lookup"><span data-stu-id="145db-121">Specifies the operating system type.</span></span>
<span data-ttu-id="145db-122">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="145db-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="145db-123">時間</span><span class="sxs-lookup"><span data-stu-id="145db-123">Windows</span></span>
- <span data-ttu-id="145db-124">Linux</span><span class="sxs-lookup"><span data-stu-id="145db-124">Linux</span></span>

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

### <span data-ttu-id="145db-125">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="145db-125">-OSDiskName</span></span>
<span data-ttu-id="145db-126">指定包含作業系統的磁片名稱。</span><span class="sxs-lookup"><span data-stu-id="145db-126">Specifies the name of the disk that contains the operating system.</span></span>

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

### <span data-ttu-id="145db-127">-設定檔</span><span class="sxs-lookup"><span data-stu-id="145db-127">-Profile</span></span>
<span data-ttu-id="145db-128">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="145db-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="145db-129">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="145db-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="145db-130">-保護</span><span class="sxs-lookup"><span data-stu-id="145db-130">-Protection</span></span>
<span data-ttu-id="145db-131">指定是否應啟用或停用保護。</span><span class="sxs-lookup"><span data-stu-id="145db-131">Specifies whether protection should be enabled or disabled.</span></span>
<span data-ttu-id="145db-132">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="145db-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="145db-133">啟用</span><span class="sxs-lookup"><span data-stu-id="145db-133">Enable</span></span>
- <span data-ttu-id="145db-134">禁止</span><span class="sxs-lookup"><span data-stu-id="145db-134">Disable</span></span>

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

### <span data-ttu-id="145db-135">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="145db-135">-ProtectionContainerId</span></span>
<span data-ttu-id="145db-136">指定受保護容器的識別碼。</span><span class="sxs-lookup"><span data-stu-id="145db-136">Specifies the ID of a protected container.</span></span>
<span data-ttu-id="145db-137">這個 Cmdlet 可為屬於此參數指定之容器的虛擬機器啟用或停用保護。</span><span class="sxs-lookup"><span data-stu-id="145db-137">This cmdlet enables or disables protection for a virtual machine that belongs to the container that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByIDs
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="145db-138">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="145db-138">-ProtectionEntity</span></span>
<span data-ttu-id="145db-139">指定保護實體物件。</span><span class="sxs-lookup"><span data-stu-id="145db-139">Specifies the protection entity object.</span></span>

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

### <span data-ttu-id="145db-140">-ProtectionProfile</span><span class="sxs-lookup"><span data-stu-id="145db-140">-ProtectionProfile</span></span>
<span data-ttu-id="145db-141">指定要啟用保護的保護設定檔。</span><span class="sxs-lookup"><span data-stu-id="145db-141">Specifies a protection profile to enable protection.</span></span>
<span data-ttu-id="145db-142">指定 **ASRProtectionProfile** 物件，該物件是關聯保護容器中其中一個可用的保護設定檔。</span><span class="sxs-lookup"><span data-stu-id="145db-142">Specify an **ASRProtectionProfile** object that is one of the available protection profiles in the associated protection container.</span></span>

```yaml
Type: ASRProtectionProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="145db-143">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="145db-143">-WaitForCompletion</span></span>
<span data-ttu-id="145db-144">表示 Cmdlet 在將控制權傳回給 Windows PowerShell 主控台之前，先等待該作業完成。</span><span class="sxs-lookup"><span data-stu-id="145db-144">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="145db-145">-確認</span><span class="sxs-lookup"><span data-stu-id="145db-145">-Confirm</span></span>
<span data-ttu-id="145db-146">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="145db-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="145db-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="145db-147">-WhatIf</span></span>
<span data-ttu-id="145db-148">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="145db-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="145db-149">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="145db-149">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="145db-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="145db-150">CommonParameters</span></span>
<span data-ttu-id="145db-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="145db-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="145db-152">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="145db-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="145db-153">輸入</span><span class="sxs-lookup"><span data-stu-id="145db-153">INPUTS</span></span>

## <span data-ttu-id="145db-154">輸出</span><span class="sxs-lookup"><span data-stu-id="145db-154">OUTPUTS</span></span>

## <span data-ttu-id="145db-155">筆記</span><span class="sxs-lookup"><span data-stu-id="145db-155">NOTES</span></span>

## <span data-ttu-id="145db-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="145db-156">RELATED LINKS</span></span>

[<span data-ttu-id="145db-157">AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="145db-157">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="145db-158">AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="145db-158">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="145db-159">更新-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="145db-159">Update-AzureSiteRecoveryProtectionEntity</span></span>](./Update-AzureSiteRecoveryProtectionEntity.md)


