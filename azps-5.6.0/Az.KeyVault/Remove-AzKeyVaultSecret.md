---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/remove-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultSecret.md
ms.openlocfilehash: 675107a27774cf2fe44ef328cdb0d7a3569e8abb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902045"
---
# <span data-ttu-id="b4b6c-101">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="b4b6c-101">Remove-AzKeyVaultSecret</span></span>

## <span data-ttu-id="b4b6c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b4b6c-102">SYNOPSIS</span></span>
<span data-ttu-id="b4b6c-103">刪除金鑰庫中的機密。</span><span class="sxs-lookup"><span data-stu-id="b4b6c-103">Deletes a secret in a key vault.</span></span>

## <span data-ttu-id="b4b6c-104">語法</span><span class="sxs-lookup"><span data-stu-id="b4b6c-104">SYNTAX</span></span>

### <span data-ttu-id="b4b6c-105">ByVaultName (預設) </span><span class="sxs-lookup"><span data-stu-id="b4b6c-105">ByVaultName (Default)</span></span>
```
Remove-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4b6c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b4b6c-106">ByInputObject</span></span>
```
Remove-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4b6c-107">描述</span><span class="sxs-lookup"><span data-stu-id="b4b6c-107">DESCRIPTION</span></span>
<span data-ttu-id="b4b6c-108">此Remove-AzKeyVaultSecret Cmdlet 會刪除金鑰庫中的一個機密。</span><span class="sxs-lookup"><span data-stu-id="b4b6c-108">The Remove-AzKeyVaultSecret cmdlet deletes a secret in a key vault.</span></span>
<span data-ttu-id="b4b6c-109">如果密碼意外刪除，則具有特殊Undo-AzKeyVaultSecretRemoval使用者可以使用密碼來復原。</span><span class="sxs-lookup"><span data-stu-id="b4b6c-109">If the secret was accidentally deleted the secret can be recovered using Undo-AzKeyVaultSecretRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="b4b6c-110">此 Cmdlet 的 **ConfirmImpact** 屬性的值為高。</span><span class="sxs-lookup"><span data-stu-id="b4b6c-110">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="b4b6c-111">例子</span><span class="sxs-lookup"><span data-stu-id="b4b6c-111">EXAMPLES</span></span>

### <span data-ttu-id="b4b6c-112">範例 1：從金鑰庫移除機密</span><span class="sxs-lookup"><span data-stu-id="b4b6c-112">Example 1: Remove a secret from a key vault</span></span>
```powershell
PS C:\> Remove-AzKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -PassThru

Vault Name           : Contoso
Name                 : FinanceSecret
Version              : f622abc7b1394092812f1eb0f85dc91c
Id                   : https://contoso.vault.azure.net:443/secrets/financesecret/f622abc7b1394092812f1eb0f85dc91c
Deleted Date         : 5/25/2018 4:45:34 PM
Scheduled Purge Date : 8/23/2018 4:45:34 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 4/19/2018 5:56:02 PM
Updated              : 4/26/2018 7:48:40 PM
Content Type         :
Tags                 :
```

<span data-ttu-id="b4b6c-113">此命令會從名為 Contoso 的金鑰庫移除名為 FinanceSecret 的機密。</span><span class="sxs-lookup"><span data-stu-id="b4b6c-113">This command removes the secret named FinanceSecret from the key vault named Contoso.'</span></span>

### <span data-ttu-id="b4b6c-114">範例 2：在未使用者確認的情況下，從金鑰庫移除密碼</span><span class="sxs-lookup"><span data-stu-id="b4b6c-114">Example 2: Remove a secret from a key vault without user confirmation</span></span>
```powershell
PS C:\> Remove-AzKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -PassThru -Force

Vault Name           : Contoso
Name                 : FinanceSecret
Version              : f622abc7b1394092812f1eb0f85dc91c
Id                   : https://contoso.vault.azure.net:443/secrets/financesecret/f622abc7b1394092812f1eb0f85dc91c
Deleted Date         : 5/25/2018 4:45:34 PM
Scheduled Purge Date : 8/23/2018 4:45:34 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 4/19/2018 5:56:02 PM
Updated              : 4/26/2018 7:48:40 PM
Content Type         :
Tags                 :
```

<span data-ttu-id="b4b6c-115">此命令會從名為 Contoso 的金鑰庫移除名為 FinanceSecret 的機密。</span><span class="sxs-lookup"><span data-stu-id="b4b6c-115">This command removes the secret named FinanceSecret from the key vault named Contoso.</span></span>
<span data-ttu-id="b4b6c-116">命令會指定 *強制* 和 *確認* 參數，因此 Cmdlet 不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b4b6c-116">The command specifies the *Force* and *Confirm* parameters, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="b4b6c-117">範例 3：永久清除金鑰保存庫中已刪除的機密</span><span class="sxs-lookup"><span data-stu-id="b4b6c-117">Example 3: Purge deleted secret from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -InRemovedState
```

<span data-ttu-id="b4b6c-118">此命令會從名為 Contoso 的金鑰保存庫永久保存名為 FinanceSecret 的機密。</span><span class="sxs-lookup"><span data-stu-id="b4b6c-118">This command premoves the secret named FinanceSecret from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="b4b6c-119">執行此 Cmdlet 需要'清除」許可權，此許可權必須先前已明確授予此金鑰庫的使用者。</span><span class="sxs-lookup"><span data-stu-id="b4b6c-119">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

## <span data-ttu-id="b4b6c-120">參數</span><span class="sxs-lookup"><span data-stu-id="b4b6c-120">PARAMETERS</span></span>

### <span data-ttu-id="b4b6c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4b6c-121">-DefaultProfile</span></span>
<span data-ttu-id="b4b6c-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="b4b6c-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b4b6c-123">-強制</span><span class="sxs-lookup"><span data-stu-id="b4b6c-123">-Force</span></span>
<span data-ttu-id="b4b6c-124">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="b4b6c-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b4b6c-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4b6c-125">-InputObject</span></span>
<span data-ttu-id="b4b6c-126">Key Vault 機密物件</span><span class="sxs-lookup"><span data-stu-id="b4b6c-126">Key Vault Secret Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4b6c-127">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="b4b6c-127">-InRemovedState</span></span>
<span data-ttu-id="b4b6c-128">如果有，會永久移除先前刪除的機密。</span><span class="sxs-lookup"><span data-stu-id="b4b6c-128">If present, removes the previously deleted secret permanently.</span></span>

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

### <span data-ttu-id="b4b6c-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="b4b6c-129">-Name</span></span>
<span data-ttu-id="b4b6c-130">指定機密的名稱。</span><span class="sxs-lookup"><span data-stu-id="b4b6c-130">Specifies the name of a secret.</span></span>
<span data-ttu-id="b4b6c-131">此 Cmdlet 會根據此參數指定的名稱、金鑰庫的名稱，以及您目前的環境，建構完整功能變數名稱 (FQDN) 的機密。</span><span class="sxs-lookup"><span data-stu-id="b4b6c-131">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4b6c-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b4b6c-132">-PassThru</span></span>
<span data-ttu-id="b4b6c-133">表示此 Cmdlet 會返回 **Microsoft.Azure.Commands.KeyVault.models.Secret** 物件。</span><span class="sxs-lookup"><span data-stu-id="b4b6c-133">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.Secret** object.</span></span>
<span data-ttu-id="b4b6c-134">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="b4b6c-134">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b4b6c-135">-VaultName</span><span class="sxs-lookup"><span data-stu-id="b4b6c-135">-VaultName</span></span>
<span data-ttu-id="b4b6c-136">指定該機密所屬的金鑰庫名稱。</span><span class="sxs-lookup"><span data-stu-id="b4b6c-136">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="b4b6c-137">此 Cmdlet 會依據此參數指定的名稱和您目前的環境，建構金鑰庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="b4b6c-137">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4b6c-138">-確認</span><span class="sxs-lookup"><span data-stu-id="b4b6c-138">-Confirm</span></span>
<span data-ttu-id="b4b6c-139">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b4b6c-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4b6c-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4b6c-140">-WhatIf</span></span>
<span data-ttu-id="b4b6c-141">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b4b6c-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4b6c-142">不會執行 Cmdlet。顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b4b6c-142">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4b6c-143">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b4b6c-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4b6c-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4b6c-144">CommonParameters</span></span>
<span data-ttu-id="b4b6c-145">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b4b6c-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4b6c-146">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b4b6c-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4b6c-147">輸入</span><span class="sxs-lookup"><span data-stu-id="b4b6c-147">INPUTS</span></span>

### <span data-ttu-id="b4b6c-148">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="b4b6c-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="b4b6c-149">輸出</span><span class="sxs-lookup"><span data-stu-id="b4b6c-149">OUTPUTS</span></span>

### <span data-ttu-id="b4b6c-150">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="b4b6c-150">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span></span>

## <span data-ttu-id="b4b6c-151">筆記</span><span class="sxs-lookup"><span data-stu-id="b4b6c-151">NOTES</span></span>

## <span data-ttu-id="b4b6c-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="b4b6c-152">RELATED LINKS</span></span>

[<span data-ttu-id="b4b6c-153">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="b4b6c-153">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="b4b6c-154">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="b4b6c-154">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

[<span data-ttu-id="b4b6c-155">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="b4b6c-155">Undo-AzKeyVaultSecretRemoval</span></span>](./Undo-AzKeyVaultSecretRemoval.md)

