---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 189E3DD8-AA43-4D4C-A873-971E0585E54E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Remove-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Remove-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: 80b03c8ba4bab5968e55dff40633b014a586d450
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450042"
---
# <span data-ttu-id="71e32-101">Remove-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="71e32-101">Remove-AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="71e32-102">摘要</span><span class="sxs-lookup"><span data-stu-id="71e32-102">SYNOPSIS</span></span>
<span data-ttu-id="71e32-103">從備份保存庫刪除原則。</span><span class="sxs-lookup"><span data-stu-id="71e32-103">Deletes a policy from a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71e32-104">句法</span><span class="sxs-lookup"><span data-stu-id="71e32-104">SYNTAX</span></span>

```
Remove-AzureRmBackupProtectionPolicy [-Force] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71e32-105">說明</span><span class="sxs-lookup"><span data-stu-id="71e32-105">DESCRIPTION</span></span>
<span data-ttu-id="71e32-106">**AzureRmBackupProtectionPolicy** Cmdlet 會從 Azure 備份電子倉庫中刪除原則。</span><span class="sxs-lookup"><span data-stu-id="71e32-106">The **Remove-AzureRmBackupProtectionPolicy** cmdlet deletes a policy from an Azure Backup vault.</span></span>

<span data-ttu-id="71e32-107">在您可以刪除備份保護原則之前，原則不能有任何相關聯的備份專案。</span><span class="sxs-lookup"><span data-stu-id="71e32-107">Before you can delete a backup protection policy, the policy must not have any associated Backup items.</span></span>
<span data-ttu-id="71e32-108">在您刪除原則之前，請確認每個相關專案都與其他原則相關聯。</span><span class="sxs-lookup"><span data-stu-id="71e32-108">Before you delete the policy, make sure that each associated item is associated with some other policy.</span></span>
<span data-ttu-id="71e32-109">若要將另一個原則與備份專案建立關聯，請使用 Enable-AzureRmBackupProtection Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="71e32-109">To associate another policy with a backup item, use the Enable-AzureRmBackupProtection cmdlet.</span></span>

## <span data-ttu-id="71e32-110">示例</span><span class="sxs-lookup"><span data-stu-id="71e32-110">EXAMPLES</span></span>

### <span data-ttu-id="71e32-111">範例1：移除備份保護原則</span><span class="sxs-lookup"><span data-stu-id="71e32-111">Example 1: Remove a backup protection policy</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupProtectionPolicy -Vault $Vault -Name "DailyBackup" | Remove-AzureRmBackupProtectionPolicy
```

<span data-ttu-id="71e32-112">第一個命令會使用 Get-AzureRmBackupVault Cmdlet 來取得名為 Vault03 的保存庫。</span><span class="sxs-lookup"><span data-stu-id="71e32-112">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="71e32-113">該命令會將該物件儲存在 $Vault 變數中。</span><span class="sxs-lookup"><span data-stu-id="71e32-113">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="71e32-114">第二個命令會建立一個保留原則，每日保留30天，然後將它儲存在 $Daily 變數中。</span><span class="sxs-lookup"><span data-stu-id="71e32-114">The second command creates a retention policy for 30 days of daily retention, and then stores it in the $Daily variable.</span></span>

<span data-ttu-id="71e32-115">第二個命令會使用 **AzureRmBackupProtectionPolicy** Cmdlet，在 $Vault 中的保存庫中，取得名為 DailyBackup 的保護原則。</span><span class="sxs-lookup"><span data-stu-id="71e32-115">The second command gets the protection policy named DailyBackup in the vault in $Vault by using the **Get-AzureRmBackupProtectionPolicy** cmdlet.</span></span>
<span data-ttu-id="71e32-116">該命令會將原則傳遞給目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="71e32-116">The command passes the policy to the current cmdlet.</span></span>
<span data-ttu-id="71e32-117">該 Cmdlet 會移除原則。</span><span class="sxs-lookup"><span data-stu-id="71e32-117">That cmdlet removes the policy.</span></span>

## <span data-ttu-id="71e32-118">參數</span><span class="sxs-lookup"><span data-stu-id="71e32-118">PARAMETERS</span></span>

### <span data-ttu-id="71e32-119">-Force</span><span class="sxs-lookup"><span data-stu-id="71e32-119">-Force</span></span>
<span data-ttu-id="71e32-120">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="71e32-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="71e32-121">-ProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="71e32-121">-ProtectionPolicy</span></span>
<span data-ttu-id="71e32-122">指定此 Cmdlet 移除的保護原則。</span><span class="sxs-lookup"><span data-stu-id="71e32-122">Specifies protection policy that this cmdlet removes.</span></span>
<span data-ttu-id="71e32-123">若要取得 **AzureRmBackupProtectionPolicy** ，請使用 Get-AzureRmBackupProtectionPolicy Cmdlet</span><span class="sxs-lookup"><span data-stu-id="71e32-123">To obtain an **AzureRmBackupProtectionPolicy** , use the Get-AzureRmBackupProtectionPolicy cmdlet</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupProtectionPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71e32-124">-確認</span><span class="sxs-lookup"><span data-stu-id="71e32-124">-Confirm</span></span>
<span data-ttu-id="71e32-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="71e32-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71e32-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71e32-126">-WhatIf</span></span>
<span data-ttu-id="71e32-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="71e32-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71e32-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="71e32-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71e32-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71e32-129">-DefaultProfile</span></span>
<span data-ttu-id="71e32-130">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="71e32-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71e32-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71e32-131">CommonParameters</span></span>
<span data-ttu-id="71e32-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="71e32-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71e32-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="71e32-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71e32-134">輸入</span><span class="sxs-lookup"><span data-stu-id="71e32-134">INPUTS</span></span>

### <span data-ttu-id="71e32-135">AzureRMBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="71e32-135">AzureRMBackupProtectionPolicy</span></span>

## <span data-ttu-id="71e32-136">輸出</span><span class="sxs-lookup"><span data-stu-id="71e32-136">OUTPUTS</span></span>

### <span data-ttu-id="71e32-137">所有</span><span class="sxs-lookup"><span data-stu-id="71e32-137">None</span></span>

## <span data-ttu-id="71e32-138">筆記</span><span class="sxs-lookup"><span data-stu-id="71e32-138">NOTES</span></span>

## <span data-ttu-id="71e32-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="71e32-139">RELATED LINKS</span></span>

[<span data-ttu-id="71e32-140">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="71e32-140">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="71e32-141">AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="71e32-141">Get-AzureRmBackupProtectionPolicy</span></span>](./Get-AzureRmBackupProtectionPolicy.md)

[<span data-ttu-id="71e32-142">新-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="71e32-142">New-AzureRmBackupProtectionPolicy</span></span>](./New-AzureRmBackupProtectionPolicy.md)


