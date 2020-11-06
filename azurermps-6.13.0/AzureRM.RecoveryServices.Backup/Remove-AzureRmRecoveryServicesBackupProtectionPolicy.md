---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: BFE741CC-C166-4534-93F4-D21AAFAD9FF6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/remove-azurermrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 805deece859eb4baa05d8c3d34dfcc8a9d571354
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455940"
---
# <span data-ttu-id="5d44c-101">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="5d44c-101">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="5d44c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5d44c-102">SYNOPSIS</span></span>
<span data-ttu-id="5d44c-103">從保存庫刪除備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="5d44c-103">Deletes a Backup protection policy from a vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d44c-104">句法</span><span class="sxs-lookup"><span data-stu-id="5d44c-104">SYNTAX</span></span>

### <span data-ttu-id="5d44c-105">PolicyName (預設) </span><span class="sxs-lookup"><span data-stu-id="5d44c-105">PolicyName (Default)</span></span>
```
Remove-AzureRmRecoveryServicesBackupProtectionPolicy [-Name] <String> [-PassThru] [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d44c-106">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="5d44c-106">PolicyObject</span></span>
```
Remove-AzureRmRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-PassThru] [-Force]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d44c-107">說明</span><span class="sxs-lookup"><span data-stu-id="5d44c-107">DESCRIPTION</span></span>
<span data-ttu-id="5d44c-108">**AzureRmRecoveryServicesBackupProtectionPolicy** Cmdlet 會刪除電子倉庫的備份原則。</span><span class="sxs-lookup"><span data-stu-id="5d44c-108">The **Remove-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet deletes backup policies for a vault.</span></span>
<span data-ttu-id="5d44c-109">在您可以刪除備份保護原則之前，原則不能有任何相關聯的備份專案。</span><span class="sxs-lookup"><span data-stu-id="5d44c-109">Before you can delete a Backup protection policy, the policy must not have any associated Backup items.</span></span>
<span data-ttu-id="5d44c-110">在您刪除原則之前，請確認每個相關專案都與其他原則相關聯。</span><span class="sxs-lookup"><span data-stu-id="5d44c-110">Before you delete the policy, make sure that each associated item is associated with some other policy.</span></span>
<span data-ttu-id="5d44c-111">若要將另一個原則與備份專案建立關聯，請使用 Enable-AzureRmRecoveryServicesBackupProtection Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5d44c-111">To associate another policy with a Backup item, use the Enable-AzureRmRecoveryServicesBackupProtection cmdlet.</span></span>
<span data-ttu-id="5d44c-112">使用 Set-AzureRmRecoveryServicesVaultContext Cmdlet 來設定 vault 內容，然後再使用目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5d44c-112">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="5d44c-113">示例</span><span class="sxs-lookup"><span data-stu-id="5d44c-113">EXAMPLES</span></span>

### <span data-ttu-id="5d44c-114">範例1：移除原則</span><span class="sxs-lookup"><span data-stu-id="5d44c-114">Example 1: Remove a policy</span></span>
```
PS C:\>$Pol= Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Remove-AzureRmRecoveryServicesBackupProtectionPolicy -Policy $Pol
```

<span data-ttu-id="5d44c-115">第一個命令會取得名為 NewPolicy 的備份保護原則，然後將它儲存在 $Pol 變數中。</span><span class="sxs-lookup"><span data-stu-id="5d44c-115">The first command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="5d44c-116">第二個命令會移除 $Pol 中的原則物件。</span><span class="sxs-lookup"><span data-stu-id="5d44c-116">The second command removes the policy object in $Pol.</span></span>

## <span data-ttu-id="5d44c-117">參數</span><span class="sxs-lookup"><span data-stu-id="5d44c-117">PARAMETERS</span></span>

### <span data-ttu-id="5d44c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d44c-118">-DefaultProfile</span></span>
<span data-ttu-id="5d44c-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5d44c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d44c-120">-Force</span><span class="sxs-lookup"><span data-stu-id="5d44c-120">-Force</span></span>
<span data-ttu-id="5d44c-121">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="5d44c-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5d44c-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="5d44c-122">-Name</span></span>
<span data-ttu-id="5d44c-123">指定要移除的備份保護原則名稱。</span><span class="sxs-lookup"><span data-stu-id="5d44c-123">Specifies the name of the Backup protection policy to remove.</span></span>

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

### <span data-ttu-id="5d44c-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5d44c-124">-PassThru</span></span>
<span data-ttu-id="5d44c-125">傳回要刪除的原則。</span><span class="sxs-lookup"><span data-stu-id="5d44c-125">Return the policy to be deleted.</span></span>

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

### <span data-ttu-id="5d44c-126">-原則</span><span class="sxs-lookup"><span data-stu-id="5d44c-126">-Policy</span></span>
<span data-ttu-id="5d44c-127">指定要移除的備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="5d44c-127">Specifies the Backup protection policy to remove.</span></span>
<span data-ttu-id="5d44c-128">若要取得 **BackupPolicy** 物件，請使用 Get-AzureRmRecoveryServicesBackupProtectionPolicy Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5d44c-128">To obtain an **BackupPolicy** object, use the Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="5d44c-129">-VaultId</span><span class="sxs-lookup"><span data-stu-id="5d44c-129">-VaultId</span></span>
<span data-ttu-id="5d44c-130">[恢復服務] 保存庫的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="5d44c-130">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="5d44c-131">-確認</span><span class="sxs-lookup"><span data-stu-id="5d44c-131">-Confirm</span></span>
<span data-ttu-id="5d44c-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5d44c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d44c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d44c-133">-WhatIf</span></span>
<span data-ttu-id="5d44c-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5d44c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d44c-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5d44c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d44c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d44c-136">CommonParameters</span></span>
<span data-ttu-id="5d44c-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5d44c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d44c-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5d44c-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d44c-139">輸入</span><span class="sxs-lookup"><span data-stu-id="5d44c-139">INPUTS</span></span>

### <span data-ttu-id="5d44c-140">PolicyBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="5d44c-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>
<span data-ttu-id="5d44c-141">參數：原則 (ByValue) </span><span class="sxs-lookup"><span data-stu-id="5d44c-141">Parameters: Policy (ByValue)</span></span>

### <span data-ttu-id="5d44c-142">System.object</span><span class="sxs-lookup"><span data-stu-id="5d44c-142">System.String</span></span>
<span data-ttu-id="5d44c-143">參數： VaultId (ByValue) </span><span class="sxs-lookup"><span data-stu-id="5d44c-143">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="5d44c-144">輸出</span><span class="sxs-lookup"><span data-stu-id="5d44c-144">OUTPUTS</span></span>

### <span data-ttu-id="5d44c-145">PolicyBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="5d44c-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="5d44c-146">筆記</span><span class="sxs-lookup"><span data-stu-id="5d44c-146">NOTES</span></span>

## <span data-ttu-id="5d44c-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="5d44c-147">RELATED LINKS</span></span>

[<span data-ttu-id="5d44c-148">AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="5d44c-148">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="5d44c-149">新-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="5d44c-149">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="5d44c-150">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="5d44c-150">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)


