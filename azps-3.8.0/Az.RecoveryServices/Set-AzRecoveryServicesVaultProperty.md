---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: a9bd1eead98a7afb06e1f5b480f8a65fc5079bd4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959463"
---
# <span data-ttu-id="4c7eb-101">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="4c7eb-101">Set-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="4c7eb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4c7eb-102">SYNOPSIS</span></span>
<span data-ttu-id="4c7eb-103">更新電子倉庫的屬性。</span><span class="sxs-lookup"><span data-stu-id="4c7eb-103">Updates properties of a Vault.</span></span>

## <span data-ttu-id="4c7eb-104">句法</span><span class="sxs-lookup"><span data-stu-id="4c7eb-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultProperty -SoftDeleteFeatureState <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c7eb-105">說明</span><span class="sxs-lookup"><span data-stu-id="4c7eb-105">DESCRIPTION</span></span>
<span data-ttu-id="4c7eb-106">**AzRecoveryServicesVaultProperty** Cmdlet 會更新恢復服務保存庫的屬性。</span><span class="sxs-lookup"><span data-stu-id="4c7eb-106">The **Set-AzRecoveryServicesVaultProperty** cmdlet updates properties of a Recovery services vault.</span></span>
<span data-ttu-id="4c7eb-107">您可以使用 **AzRecoveryServicesVaultProperty** Cmdlet 來取得保存庫目前的屬性。</span><span class="sxs-lookup"><span data-stu-id="4c7eb-107">You can use **Set-AzRecoveryServicesVaultProperty** cmdlet to get the current properties of a vault.</span></span>
<span data-ttu-id="4c7eb-108">您可以在任何時間點，使用此 Cmdlet **SoftDeleteFeatureState** 屬性來啟用保存庫。</span><span class="sxs-lookup"><span data-stu-id="4c7eb-108">Using this cmdlet **SoftDeleteFeatureState** property of a vault can be enabled at any point of time.</span></span>
<span data-ttu-id="4c7eb-109">只有在保存庫中沒有已註冊的容器，才能停用保存庫的 **SoftDeleteFeatureState** 屬性。</span><span class="sxs-lookup"><span data-stu-id="4c7eb-109">**SoftDeleteFeatureState** property of a vault can be disabled only if there are no registered containers in the vault.</span></span>
<span data-ttu-id="4c7eb-110">使用 Set-AzRecoveryServicesVaultContext Cmdlet 來設定 vault 內容，然後再使用目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4c7eb-110">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="4c7eb-111">示例</span><span class="sxs-lookup"><span data-stu-id="4c7eb-111">EXAMPLES</span></span>

### <span data-ttu-id="4c7eb-112">範例1：更新電子倉庫的 SoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="4c7eb-112">Example 1: Update SoftDeleteFeatureState of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -Name "MyVaultName"
PS C:\> $props = Set-AzRecoveryServicesVaultProperty -VaultId $vault.Id -SoftDeleteFeatureState Enable
```

<span data-ttu-id="4c7eb-113">第一個命令會取得 Vault 物件，然後將它儲存在 $vault 變數中。</span><span class="sxs-lookup"><span data-stu-id="4c7eb-113">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="4c7eb-114">第二個命令會將保存庫的 SoftDeleteFeatureState 屬性更新為「已啟用」狀態。</span><span class="sxs-lookup"><span data-stu-id="4c7eb-114">The second command Updates the SoftDeleteFeatureState property of the vault to "Enabled" state.</span></span>

## <span data-ttu-id="4c7eb-115">參數</span><span class="sxs-lookup"><span data-stu-id="4c7eb-115">PARAMETERS</span></span>

### <span data-ttu-id="4c7eb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c7eb-116">-DefaultProfile</span></span>
<span data-ttu-id="4c7eb-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4c7eb-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c7eb-118">-SoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="4c7eb-118">-SoftDeleteFeatureState</span></span>
<span data-ttu-id="4c7eb-119">[復原服務] 保存庫的 SoftDeleteFeatureState。</span><span class="sxs-lookup"><span data-stu-id="4c7eb-119">SoftDeleteFeatureState of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="4c7eb-120">-VaultId</span><span class="sxs-lookup"><span data-stu-id="4c7eb-120">-VaultId</span></span>
<span data-ttu-id="4c7eb-121">[恢復服務] 保存庫的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="4c7eb-121">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="4c7eb-122">-確認</span><span class="sxs-lookup"><span data-stu-id="4c7eb-122">-Confirm</span></span>
<span data-ttu-id="4c7eb-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4c7eb-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c7eb-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c7eb-124">-WhatIf</span></span>
<span data-ttu-id="4c7eb-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4c7eb-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4c7eb-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4c7eb-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c7eb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c7eb-127">CommonParameters</span></span>
<span data-ttu-id="4c7eb-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4c7eb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c7eb-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4c7eb-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c7eb-130">輸入</span><span class="sxs-lookup"><span data-stu-id="4c7eb-130">INPUTS</span></span>

### <span data-ttu-id="4c7eb-131">System.object</span><span class="sxs-lookup"><span data-stu-id="4c7eb-131">System.String</span></span>

### <span data-ttu-id="4c7eb-132">VaultSoftDeleteFeatureState 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="4c7eb-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.VaultSoftDeleteFeatureState</span></span>

## <span data-ttu-id="4c7eb-133">輸出</span><span class="sxs-lookup"><span data-stu-id="4c7eb-133">OUTPUTS</span></span>

### <span data-ttu-id="4c7eb-134">BackupResourceVaultConfigResource 中的 RecoveryServices 備份。</span><span class="sxs-lookup"><span data-stu-id="4c7eb-134">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="4c7eb-135">筆記</span><span class="sxs-lookup"><span data-stu-id="4c7eb-135">NOTES</span></span>

## <span data-ttu-id="4c7eb-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="4c7eb-136">RELATED LINKS</span></span>

[<span data-ttu-id="4c7eb-137">AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="4c7eb-137">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="4c7eb-138">AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="4c7eb-138">Get-AzRecoveryServicesVaultProperty</span></span>](./Get-AzRecoveryServicesVaultProperty.md)


