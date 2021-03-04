---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: a88b137b5735984ce6b5f19389d9035b85b1dfe4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913733"
---
# <span data-ttu-id="84098-101">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="84098-101">Set-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="84098-102">簡介</span><span class="sxs-lookup"><span data-stu-id="84098-102">SYNOPSIS</span></span>
<span data-ttu-id="84098-103">更新儲存庫的屬性。</span><span class="sxs-lookup"><span data-stu-id="84098-103">Updates properties of a Vault.</span></span>

## <span data-ttu-id="84098-104">語法</span><span class="sxs-lookup"><span data-stu-id="84098-104">SYNTAX</span></span>

### <span data-ttu-id="84098-105">AzureRSVaultSoftDelteParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="84098-105">AzureRSVaultSoftDelteParameterSet (Default)</span></span>
```
Set-AzRecoveryServicesVaultProperty -SoftDeleteFeatureState <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84098-106">AzureRSVaultCMKParameterSet</span><span class="sxs-lookup"><span data-stu-id="84098-106">AzureRSVaultCMKParameterSet</span></span>
```
Set-AzRecoveryServicesVaultProperty -EncryptionKeyId <string> -KeyVaultSubscriptionId <string> [-InfrastructureEncryption] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84098-107">描述</span><span class="sxs-lookup"><span data-stu-id="84098-107">DESCRIPTION</span></span>
<span data-ttu-id="84098-108">**Set-AzRecoveryServicesVaultProperty** Cmdlet 會更新復原服務庫的屬性。</span><span class="sxs-lookup"><span data-stu-id="84098-108">The **Set-AzRecoveryServicesVaultProperty** cmdlet updates properties of a Recovery services vault.</span></span> <span data-ttu-id="84098-109">此 Cmdlet 可用來啟用/停用柔刪除，或針對有兩個不同參數集的儲存庫設定 CMK 加密。</span><span class="sxs-lookup"><span data-stu-id="84098-109">This cmdlet can be used to enable/disable soft delete or set CMK encryption for a vault with two different parameter sets.</span></span> 
<span data-ttu-id="84098-110">只有當庫中沒有登錄的容器時，才能停用儲存庫的 **SoftDeleteFeatureState** 屬性。</span><span class="sxs-lookup"><span data-stu-id="84098-110">**SoftDeleteFeatureState** property of a vault can be disabled only if there are no registered containers in the vault.</span></span> <span data-ttu-id="84098-111">只有使用者第一次更新 CMK 保存庫時，才能設定加密。</span><span class="sxs-lookup"><span data-stu-id="84098-111">InfrastructurEncryption can only be set the first time a user updates the CMK vault.</span></span>

## <span data-ttu-id="84098-112">例子</span><span class="sxs-lookup"><span data-stu-id="84098-112">EXAMPLES</span></span>

### <span data-ttu-id="84098-113">範例 1：更新儲存庫的 SoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="84098-113">Example 1: Update SoftDeleteFeatureState of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName" -Name "vaultName"
PS C:\> $props = Set-AzRecoveryServicesVaultProperty -VaultId $vault.Id -SoftDeleteFeatureState Enable
```

<span data-ttu-id="84098-114">第一個命令會獲得保存庫物件，然後將它儲存在$vault變數中。</span><span class="sxs-lookup"><span data-stu-id="84098-114">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="84098-115">第二個命令將儲存庫的 SoftDeleteFeatureState 屬性更新為「啟用」狀態。</span><span class="sxs-lookup"><span data-stu-id="84098-115">The second command Updates the SoftDeleteFeatureState property of the vault to "Enabled" state.</span></span>

### <span data-ttu-id="84098-116">範例 2：更新儲存庫的 CMK 加密</span><span class="sxs-lookup"><span data-stu-id="84098-116">Example 2: Update CMK encryption of a vault</span></span>

```
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName" -Name "vaultName"
PS C:\> $keyVault = Get-AzKeyVault -VaultName "keyVaultName" -ResourceGroupName "RGName" 
PS C:\> $key = Get-AzKeyVaultKey -VaultName "keyVaultName" -Name "keyName" 
PS C:\> Set-AzRecoveryServicesVaultProperty -EncryptionKeyId $key.ID -KeyVaultSubscriptionId "f870818k-5h28-4t48-8961-37458592348r" -InfrastructureEncryption -VaultId $vault.ID
```

<span data-ttu-id="84098-117">第一個 Cmdlet 會獲得 RSVault 來更新加密屬性。</span><span class="sxs-lookup"><span data-stu-id="84098-117">First cmdlet gets the RSVault to update encryption properties.</span></span> <span data-ttu-id="84098-118">第二個 Cmdlet 會獲得 Azure 金鑰庫。</span><span class="sxs-lookup"><span data-stu-id="84098-118">Second cmdlet gets the azure key vault.</span></span> <span data-ttu-id="84098-119">第三個 Cmdlet 會從金鑰庫取得金鑰。</span><span class="sxs-lookup"><span data-stu-id="84098-119">Third cmdlet get the key from the key vault.</span></span>
<span data-ttu-id="84098-120">第四個 Cmdlet 會更新 RSVault 中客戶管理的加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="84098-120">Fourth cmdlet updates the customer managed encryption key within the RSVault.</span></span> <span data-ttu-id="84098-121">使用 -InfrastructureEncryption 參數啟用第一次更新的基礎結構加密。</span><span class="sxs-lookup"><span data-stu-id="84098-121">Use -InfrastructureEncryption param to enable infrastructure encryption for the first time update.</span></span> 

## <span data-ttu-id="84098-122">參數</span><span class="sxs-lookup"><span data-stu-id="84098-122">PARAMETERS</span></span>

### <span data-ttu-id="84098-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84098-123">-DefaultProfile</span></span>
<span data-ttu-id="84098-124">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="84098-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84098-125">-SoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="84098-125">-SoftDeleteFeatureState</span></span>
<span data-ttu-id="84098-126">修復服務庫的 SoftDeleteFeatureState。</span><span class="sxs-lookup"><span data-stu-id="84098-126">SoftDeleteFeatureState of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="84098-127">-EncryptionKeyId</span><span class="sxs-lookup"><span data-stu-id="84098-127">-EncryptionKeyId</span></span>
<span data-ttu-id="84098-128">用於 CMK 之加密金鑰的 KeyId。</span><span class="sxs-lookup"><span data-stu-id="84098-128">KeyId of the encryption key to be used for CMK.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: KeyID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84098-129">-KeyVaultSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="84098-129">-KeyVaultSubscriptionId</span></span>
<span data-ttu-id="84098-130">金鑰庫的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="84098-130">Subscription Id of the Key Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: SubscriptionID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84098-131">-InfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="84098-131">-InfrastructureEncryption</span></span>
<span data-ttu-id="84098-132">啟用此儲存庫上的基礎結構加密。</span><span class="sxs-lookup"><span data-stu-id="84098-132">Enables infrastructure encryption on this vault.</span></span> <span data-ttu-id="84098-133">進行加密時，必須啟用基礎結構加密。</span><span class="sxs-lookup"><span data-stu-id="84098-133">Infrastructure encryption must be enabled when configuring encryption.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84098-134">-VaultId</span><span class="sxs-lookup"><span data-stu-id="84098-134">-VaultId</span></span>
<span data-ttu-id="84098-135">復原服務庫的 ARM 識別碼。</span><span class="sxs-lookup"><span data-stu-id="84098-135">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="84098-136">-確認</span><span class="sxs-lookup"><span data-stu-id="84098-136">-Confirm</span></span>
<span data-ttu-id="84098-137">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="84098-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84098-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84098-138">-WhatIf</span></span>
<span data-ttu-id="84098-139">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="84098-139">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="84098-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84098-140">CommonParameters</span></span>
<span data-ttu-id="84098-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="84098-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84098-142">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="84098-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84098-143">輸入</span><span class="sxs-lookup"><span data-stu-id="84098-143">INPUTS</span></span>

### <span data-ttu-id="84098-144">System.String</span><span class="sxs-lookup"><span data-stu-id="84098-144">System.String</span></span>

### <span data-ttu-id="84098-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.models.VaultSoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="84098-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.VaultSoftDeleteFeatureState</span></span>

## <span data-ttu-id="84098-146">輸出</span><span class="sxs-lookup"><span data-stu-id="84098-146">OUTPUTS</span></span>

### <span data-ttu-id="84098-147">Microsoft.Azure.management.RecoveryServices.Backup.models.BackupResourceVaultConfigResource</span><span class="sxs-lookup"><span data-stu-id="84098-147">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="84098-148">筆記</span><span class="sxs-lookup"><span data-stu-id="84098-148">NOTES</span></span>

## <span data-ttu-id="84098-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="84098-149">RELATED LINKS</span></span>

[<span data-ttu-id="84098-150">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="84098-150">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="84098-151">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="84098-151">Get-AzRecoveryServicesVaultProperty</span></span>](./Get-AzRecoveryServicesVaultProperty.md)
