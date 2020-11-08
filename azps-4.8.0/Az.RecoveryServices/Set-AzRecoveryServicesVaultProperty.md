---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: 4b34bdf2357b389081297df8f49745127953985b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94135459"
---
# <span data-ttu-id="5ce71-101">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="5ce71-101">Set-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="5ce71-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5ce71-102">SYNOPSIS</span></span>
<span data-ttu-id="5ce71-103">更新電子倉庫的屬性。</span><span class="sxs-lookup"><span data-stu-id="5ce71-103">Updates properties of a Vault.</span></span>

## <span data-ttu-id="5ce71-104">句法</span><span class="sxs-lookup"><span data-stu-id="5ce71-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultProperty -SoftDeleteFeatureState <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ce71-105">說明</span><span class="sxs-lookup"><span data-stu-id="5ce71-105">DESCRIPTION</span></span>
<span data-ttu-id="5ce71-106">**AzRecoveryServicesVaultProperty** Cmdlet 會更新恢復服務保存庫的屬性。</span><span class="sxs-lookup"><span data-stu-id="5ce71-106">The **Set-AzRecoveryServicesVaultProperty** cmdlet updates properties of a Recovery services vault.</span></span>
<span data-ttu-id="5ce71-107">這個 Cmdlet 會在目前的 set 作業之後傳回更新的保存庫屬性。</span><span class="sxs-lookup"><span data-stu-id="5ce71-107">This cmdlet returns the updated vault properties after the current set operation.</span></span>
<span data-ttu-id="5ce71-108">您可以在任何時間點啟用此類 vault （例如虛刪除）的 Cmdlet 屬性。</span><span class="sxs-lookup"><span data-stu-id="5ce71-108">Using this cmdlet properties of vault such as soft-delete can be enabled at any point of time.</span></span>
<span data-ttu-id="5ce71-109">只有在保存庫中沒有已註冊的容器，才能停用保存庫的 **SoftDeleteFeatureState** 屬性。</span><span class="sxs-lookup"><span data-stu-id="5ce71-109">**SoftDeleteFeatureState** property of a vault can be disabled only if there are no registered containers in the vault.</span></span>

## <span data-ttu-id="5ce71-110">示例</span><span class="sxs-lookup"><span data-stu-id="5ce71-110">EXAMPLES</span></span>

### <span data-ttu-id="5ce71-111">範例1：更新電子倉庫的 SoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="5ce71-111">Example 1: Update SoftDeleteFeatureState of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -Name "MyVaultName"
PS C:\> $props = Set-AzRecoveryServicesVaultProperty -VaultId $vault.Id -SoftDeleteFeatureState Enable
```

<span data-ttu-id="5ce71-112">第一個命令會取得 Vault 物件，然後將它儲存在 $vault 變數中。</span><span class="sxs-lookup"><span data-stu-id="5ce71-112">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="5ce71-113">第二個命令會將保存庫的 SoftDeleteFeatureState 屬性更新為「已啟用」狀態。</span><span class="sxs-lookup"><span data-stu-id="5ce71-113">The second command Updates the SoftDeleteFeatureState property of the vault to "Enabled" state.</span></span>

## <span data-ttu-id="5ce71-114">參數</span><span class="sxs-lookup"><span data-stu-id="5ce71-114">PARAMETERS</span></span>

### <span data-ttu-id="5ce71-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ce71-115">-DefaultProfile</span></span>
<span data-ttu-id="5ce71-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5ce71-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ce71-117">-SoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="5ce71-117">-SoftDeleteFeatureState</span></span>
<span data-ttu-id="5ce71-118">[復原服務] 保存庫的 SoftDeleteFeatureState。</span><span class="sxs-lookup"><span data-stu-id="5ce71-118">SoftDeleteFeatureState of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enable, Disable

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ce71-119">-VaultId</span><span class="sxs-lookup"><span data-stu-id="5ce71-119">-VaultId</span></span>
<span data-ttu-id="5ce71-120">[恢復服務] 保存庫的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="5ce71-120">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="5ce71-121">-確認</span><span class="sxs-lookup"><span data-stu-id="5ce71-121">-Confirm</span></span>
<span data-ttu-id="5ce71-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5ce71-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ce71-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ce71-123">-WhatIf</span></span>
<span data-ttu-id="5ce71-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5ce71-124">Shows what would happen if the cmdlet runs.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ce71-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ce71-125">CommonParameters</span></span>
<span data-ttu-id="5ce71-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5ce71-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ce71-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5ce71-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ce71-128">輸入</span><span class="sxs-lookup"><span data-stu-id="5ce71-128">INPUTS</span></span>

### <span data-ttu-id="5ce71-129">System.object</span><span class="sxs-lookup"><span data-stu-id="5ce71-129">System.String</span></span>

### <span data-ttu-id="5ce71-130">VaultSoftDeleteFeatureState 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="5ce71-130">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.VaultSoftDeleteFeatureState</span></span>

## <span data-ttu-id="5ce71-131">輸出</span><span class="sxs-lookup"><span data-stu-id="5ce71-131">OUTPUTS</span></span>

### <span data-ttu-id="5ce71-132">BackupResourceVaultConfigResource 中的 RecoveryServices 備份。</span><span class="sxs-lookup"><span data-stu-id="5ce71-132">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="5ce71-133">筆記</span><span class="sxs-lookup"><span data-stu-id="5ce71-133">NOTES</span></span>

## <span data-ttu-id="5ce71-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="5ce71-134">RELATED LINKS</span></span>

[<span data-ttu-id="5ce71-135">AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="5ce71-135">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="5ce71-136">AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="5ce71-136">Get-AzRecoveryServicesVaultProperty</span></span>](./Get-AzRecoveryServicesVaultProperty.md)


