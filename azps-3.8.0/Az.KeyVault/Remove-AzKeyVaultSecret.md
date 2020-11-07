---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultSecret.md
ms.openlocfilehash: 71a0dcebdc889eb8116089eb3c5a5b8379c72b20
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957575"
---
# <span data-ttu-id="6c188-101">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="6c188-101">Remove-AzKeyVaultSecret</span></span>

## <span data-ttu-id="6c188-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6c188-102">SYNOPSIS</span></span>
<span data-ttu-id="6c188-103">刪除金鑰保存庫中的密碼。</span><span class="sxs-lookup"><span data-stu-id="6c188-103">Deletes a secret in a key vault.</span></span>

## <span data-ttu-id="6c188-104">句法</span><span class="sxs-lookup"><span data-stu-id="6c188-104">SYNTAX</span></span>

### <span data-ttu-id="6c188-105">ByVaultName (預設) </span><span class="sxs-lookup"><span data-stu-id="6c188-105">ByVaultName (Default)</span></span>
```
Remove-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c188-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="6c188-106">ByInputObject</span></span>
```
Remove-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c188-107">說明</span><span class="sxs-lookup"><span data-stu-id="6c188-107">DESCRIPTION</span></span>
<span data-ttu-id="6c188-108">Remove-AzKeyVaultSecret Cmdlet 會刪除金鑰保存庫中的密碼。</span><span class="sxs-lookup"><span data-stu-id="6c188-108">The Remove-AzKeyVaultSecret cmdlet deletes a secret in a key vault.</span></span>
<span data-ttu-id="6c188-109">如果不小心刪除了機密，您可以使用具有特殊「復原」許可權的使用者 Undo-AzKeyVaultSecretRemoval 來復原機密。</span><span class="sxs-lookup"><span data-stu-id="6c188-109">If the secret was accidentally deleted the secret can be recovered using Undo-AzKeyVaultSecretRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="6c188-110">這個 Cmdlet 的值為 high，用於 **ConfirmImpact** 屬性。</span><span class="sxs-lookup"><span data-stu-id="6c188-110">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="6c188-111">示例</span><span class="sxs-lookup"><span data-stu-id="6c188-111">EXAMPLES</span></span>

### <span data-ttu-id="6c188-112">範例1：移除金鑰保存庫的密碼</span><span class="sxs-lookup"><span data-stu-id="6c188-112">Example 1: Remove a secret from a key vault</span></span>
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

<span data-ttu-id="6c188-113">這個命令會從名為 Contoso 的主要電子倉庫中移除名為 FinanceSecret 的密碼。</span><span class="sxs-lookup"><span data-stu-id="6c188-113">This command removes the secret named FinanceSecret from the key vault named Contoso.'</span></span>

### <span data-ttu-id="6c188-114">範例2：移除金鑰保存庫中不含使用者確認的密碼</span><span class="sxs-lookup"><span data-stu-id="6c188-114">Example 2: Remove a secret from a key vault without user confirmation</span></span>
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

<span data-ttu-id="6c188-115">這個命令會從名為 Contoso 的主要電子倉庫中移除名為 FinanceSecret 的密碼。</span><span class="sxs-lookup"><span data-stu-id="6c188-115">This command removes the secret named FinanceSecret from the key vault named Contoso.</span></span>
<span data-ttu-id="6c188-116">命令會指定 *Force* 和 *Confirm* 參數，因此 Cmdlet 不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="6c188-116">The command specifies the *Force* and *Confirm* parameters, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="6c188-117">範例3：從金鑰保存庫永久清除已刪除的機密</span><span class="sxs-lookup"><span data-stu-id="6c188-117">Example 3: Purge deleted secret from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -InRemovedState
```

<span data-ttu-id="6c188-118">這個命令會從名為 Contoso 的主要保存庫永久 premoves 名為 FinanceSecret 的密碼。</span><span class="sxs-lookup"><span data-stu-id="6c188-118">This command premoves the secret named FinanceSecret from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="6c188-119">執行這個指令需要「清除」許可權，該許可權必須是先前已明確授與使用者的此金鑰保存庫。</span><span class="sxs-lookup"><span data-stu-id="6c188-119">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

## <span data-ttu-id="6c188-120">參數</span><span class="sxs-lookup"><span data-stu-id="6c188-120">PARAMETERS</span></span>

### <span data-ttu-id="6c188-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c188-121">-DefaultProfile</span></span>
<span data-ttu-id="6c188-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="6c188-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6c188-123">-Force</span><span class="sxs-lookup"><span data-stu-id="6c188-123">-Force</span></span>
<span data-ttu-id="6c188-124">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="6c188-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6c188-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6c188-125">-InputObject</span></span>
<span data-ttu-id="6c188-126">主要 Vault 密碼物件</span><span class="sxs-lookup"><span data-stu-id="6c188-126">Key Vault Secret Object</span></span>

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

### <span data-ttu-id="6c188-127">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="6c188-127">-InRemovedState</span></span>
<span data-ttu-id="6c188-128">如果有，則會永久移除先前刪除的機密。</span><span class="sxs-lookup"><span data-stu-id="6c188-128">If present, removes the previously deleted secret permanently.</span></span>

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

### <span data-ttu-id="6c188-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="6c188-129">-Name</span></span>
<span data-ttu-id="6c188-130">指定秘密的名稱。</span><span class="sxs-lookup"><span data-stu-id="6c188-130">Specifies the name of a secret.</span></span>
<span data-ttu-id="6c188-131">這個 Cmdlet 會根據此參數指定的名稱、主要電子倉庫的名稱和您目前的環境，來構造密碼的完整功能變數名稱 (FQDN) 。</span><span class="sxs-lookup"><span data-stu-id="6c188-131">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="6c188-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6c188-132">-PassThru</span></span>
<span data-ttu-id="6c188-133">表示此 Cmdlet 會傳回 **KeyVault** 物件的 [.]</span><span class="sxs-lookup"><span data-stu-id="6c188-133">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.Secret** object.</span></span>
<span data-ttu-id="6c188-134">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="6c188-134">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6c188-135">-VaultName</span><span class="sxs-lookup"><span data-stu-id="6c188-135">-VaultName</span></span>
<span data-ttu-id="6c188-136">指定機密所屬之金鑰保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="6c188-136">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="6c188-137">這個 Cmdlet 會根據此參數指定的名稱和您目前的環境，來構造金鑰 vault 的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="6c188-137">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="6c188-138">-確認</span><span class="sxs-lookup"><span data-stu-id="6c188-138">-Confirm</span></span>
<span data-ttu-id="6c188-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6c188-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c188-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c188-140">-WhatIf</span></span>
<span data-ttu-id="6c188-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6c188-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c188-142">未執行 Cmdlet。顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6c188-142">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c188-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6c188-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c188-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c188-144">CommonParameters</span></span>
<span data-ttu-id="6c188-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6c188-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c188-146">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6c188-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c188-147">輸入</span><span class="sxs-lookup"><span data-stu-id="6c188-147">INPUTS</span></span>

### <span data-ttu-id="6c188-148">PSKeyVaultSecretIdentityItem 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="6c188-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="6c188-149">輸出</span><span class="sxs-lookup"><span data-stu-id="6c188-149">OUTPUTS</span></span>

### <span data-ttu-id="6c188-150">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="6c188-150">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span></span>

## <span data-ttu-id="6c188-151">筆記</span><span class="sxs-lookup"><span data-stu-id="6c188-151">NOTES</span></span>

## <span data-ttu-id="6c188-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="6c188-152">RELATED LINKS</span></span>

[<span data-ttu-id="6c188-153">AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="6c188-153">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="6c188-154">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="6c188-154">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

[<span data-ttu-id="6c188-155">復原-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="6c188-155">Undo-AzKeyVaultSecretRemoval</span></span>](./Undo-AzKeyVaultSecretRemoval.md)

