---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: BFE741CC-C166-4534-93F4-D21AAFAD9FF6
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 775d3349d0bb9392ad51a260a478c45c13163008
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959484"
---
# <span data-ttu-id="d6704-101">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d6704-101">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="d6704-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d6704-102">SYNOPSIS</span></span>
<span data-ttu-id="d6704-103">從保存庫刪除備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="d6704-103">Deletes a Backup protection policy from a vault.</span></span>

## <span data-ttu-id="d6704-104">句法</span><span class="sxs-lookup"><span data-stu-id="d6704-104">SYNTAX</span></span>

### <span data-ttu-id="d6704-105">PolicyName (預設) </span><span class="sxs-lookup"><span data-stu-id="d6704-105">PolicyName (Default)</span></span>
```
Remove-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-PassThru] [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6704-106">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="d6704-106">PolicyObject</span></span>
```
Remove-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-PassThru] [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6704-107">說明</span><span class="sxs-lookup"><span data-stu-id="d6704-107">DESCRIPTION</span></span>
<span data-ttu-id="d6704-108">**AzRecoveryServicesBackupProtectionPolicy** Cmdlet 會刪除電子倉庫的備份原則。</span><span class="sxs-lookup"><span data-stu-id="d6704-108">The **Remove-AzRecoveryServicesBackupProtectionPolicy** cmdlet deletes backup policies for a vault.</span></span>
<span data-ttu-id="d6704-109">在您可以刪除備份保護原則之前，原則不能有任何相關聯的備份專案。</span><span class="sxs-lookup"><span data-stu-id="d6704-109">Before you can delete a Backup protection policy, the policy must not have any associated Backup items.</span></span>
<span data-ttu-id="d6704-110">在您刪除原則之前，請確認每個相關專案都與其他原則相關聯。</span><span class="sxs-lookup"><span data-stu-id="d6704-110">Before you delete the policy, make sure that each associated item is associated with some other policy.</span></span>
<span data-ttu-id="d6704-111">若要將另一個原則與備份專案建立關聯，請使用 Enable-AzRecoveryServicesBackupProtection Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d6704-111">To associate another policy with a Backup item, use the Enable-AzRecoveryServicesBackupProtection cmdlet.</span></span>
<span data-ttu-id="d6704-112">使用 Set-AzRecoveryServicesVaultContext Cmdlet 來設定 vault 內容，然後再使用目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d6704-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="d6704-113">示例</span><span class="sxs-lookup"><span data-stu-id="d6704-113">EXAMPLES</span></span>

### <span data-ttu-id="d6704-114">範例1：移除原則</span><span class="sxs-lookup"><span data-stu-id="d6704-114">Example 1: Remove a policy</span></span>
```
PS C:\>$Pol= Get-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Remove-AzRecoveryServicesBackupProtectionPolicy -Policy $Pol
```

<span data-ttu-id="d6704-115">第一個命令會取得名為 NewPolicy 的備份保護原則，然後將它儲存在 $Pol 變數中。</span><span class="sxs-lookup"><span data-stu-id="d6704-115">The first command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="d6704-116">第二個命令會移除 $Pol 中的原則物件。</span><span class="sxs-lookup"><span data-stu-id="d6704-116">The second command removes the policy object in $Pol.</span></span>

## <span data-ttu-id="d6704-117">參數</span><span class="sxs-lookup"><span data-stu-id="d6704-117">PARAMETERS</span></span>

### <span data-ttu-id="d6704-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6704-118">-DefaultProfile</span></span>
<span data-ttu-id="d6704-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d6704-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6704-120">-Force</span><span class="sxs-lookup"><span data-stu-id="d6704-120">-Force</span></span>
<span data-ttu-id="d6704-121">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="d6704-121">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6704-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="d6704-122">-Name</span></span>
<span data-ttu-id="d6704-123">指定要移除的備份保護原則名稱。</span><span class="sxs-lookup"><span data-stu-id="d6704-123">Specifies the name of the Backup protection policy to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6704-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d6704-124">-PassThru</span></span>
<span data-ttu-id="d6704-125">傳回要刪除的原則。</span><span class="sxs-lookup"><span data-stu-id="d6704-125">Return the policy to be deleted.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6704-126">-原則</span><span class="sxs-lookup"><span data-stu-id="d6704-126">-Policy</span></span>
<span data-ttu-id="d6704-127">指定要移除的備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="d6704-127">Specifies the Backup protection policy to remove.</span></span>
<span data-ttu-id="d6704-128">若要取得 **BackupPolicy** 物件，請使用 Get-AzRecoveryServicesBackupProtectionPolicy Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d6704-128">To obtain an **BackupPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: PolicyObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6704-129">-VaultId</span><span class="sxs-lookup"><span data-stu-id="d6704-129">-VaultId</span></span>
<span data-ttu-id="d6704-130">[恢復服務] 保存庫的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="d6704-130">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6704-131">-確認</span><span class="sxs-lookup"><span data-stu-id="d6704-131">-Confirm</span></span>
<span data-ttu-id="d6704-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d6704-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6704-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6704-133">-WhatIf</span></span>
<span data-ttu-id="d6704-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d6704-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6704-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d6704-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6704-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6704-136">CommonParameters</span></span>
<span data-ttu-id="d6704-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d6704-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6704-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d6704-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6704-139">輸入</span><span class="sxs-lookup"><span data-stu-id="d6704-139">INPUTS</span></span>

### <span data-ttu-id="d6704-140">PolicyBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="d6704-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="d6704-141">System.object</span><span class="sxs-lookup"><span data-stu-id="d6704-141">System.String</span></span>

## <span data-ttu-id="d6704-142">輸出</span><span class="sxs-lookup"><span data-stu-id="d6704-142">OUTPUTS</span></span>

### <span data-ttu-id="d6704-143">PolicyBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="d6704-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="d6704-144">筆記</span><span class="sxs-lookup"><span data-stu-id="d6704-144">NOTES</span></span>

## <span data-ttu-id="d6704-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="d6704-145">RELATED LINKS</span></span>

[<span data-ttu-id="d6704-146">AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d6704-146">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="d6704-147">新-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d6704-147">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="d6704-148">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d6704-148">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


