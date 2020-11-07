---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultsecret
schema: 2.0.0
ms.openlocfilehash: 56cc6b11c517379f1d13ebe2dbf2cee00f18211b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93799862"
---
# <span data-ttu-id="973c8-101">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="973c8-101">Remove-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="973c8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="973c8-102">SYNOPSIS</span></span>
<span data-ttu-id="973c8-103">刪除金鑰保存庫中的密碼。</span><span class="sxs-lookup"><span data-stu-id="973c8-103">Deletes a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="973c8-104">句法</span><span class="sxs-lookup"><span data-stu-id="973c8-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="973c8-105">說明</span><span class="sxs-lookup"><span data-stu-id="973c8-105">DESCRIPTION</span></span>
<span data-ttu-id="973c8-106">Remove-AzureKeyVaultSecret Cmdlet 會刪除金鑰保存庫中的密碼。</span><span class="sxs-lookup"><span data-stu-id="973c8-106">The Remove-AzureKeyVaultSecret cmdlet deletes a secret in a key vault.</span></span>
<span data-ttu-id="973c8-107">如果不小心刪除了機密，您可以使用具有特殊「復原」許可權的使用者 Undo-AzureKeyVaultSecretRemoval 來復原機密。</span><span class="sxs-lookup"><span data-stu-id="973c8-107">If the secret was accidentally deleted the secret can be recovered using Undo-AzureKeyVaultSecretRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="973c8-108">這個 Cmdlet 的值為 high，用於 **ConfirmImpact** 屬性。</span><span class="sxs-lookup"><span data-stu-id="973c8-108">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="973c8-109">示例</span><span class="sxs-lookup"><span data-stu-id="973c8-109">EXAMPLES</span></span>

### <span data-ttu-id="973c8-110">範例1：移除金鑰保存庫的密碼</span><span class="sxs-lookup"><span data-stu-id="973c8-110">Example 1: Remove a secret from a key vault</span></span>
```
PS C:\>Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret'
```

<span data-ttu-id="973c8-111">這個命令會從名為 Contoso 的主要電子倉庫中移除名為 FinanceSecret 的密碼。</span><span class="sxs-lookup"><span data-stu-id="973c8-111">This command removes the secret named FinanceSecret from the key vault named Contoso.'</span></span>

### <span data-ttu-id="973c8-112">範例2：移除金鑰保存庫中不含使用者確認的密碼</span><span class="sxs-lookup"><span data-stu-id="973c8-112">Example 2: Remove a secret from a key vault without user confirmation</span></span>
```
PS C:\>Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -Force -Confirm:$False
```

<span data-ttu-id="973c8-113">這個命令會從名為 Contoso 的主要電子倉庫中移除名為 FinanceSecret 的密碼。</span><span class="sxs-lookup"><span data-stu-id="973c8-113">This command removes the secret named FinanceSecret from the key vault named Contoso.</span></span>
<span data-ttu-id="973c8-114">命令會指定 *Force* 和 *Confirm* 參數，因此 Cmdlet 不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="973c8-114">The command specifies the *Force* and *Confirm* parameters, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="973c8-115">範例3：從金鑰保存庫永久清除已刪除的機密</span><span class="sxs-lookup"><span data-stu-id="973c8-115">Example 3: Purge deleted secret from the key vault permanently</span></span>
```
PS C:\>Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -InRemovedState
```

<span data-ttu-id="973c8-116">這個命令會從名為 Contoso 的主要保存庫永久 premoves 名為 FinanceSecret 的密碼。</span><span class="sxs-lookup"><span data-stu-id="973c8-116">This command premoves the secret named FinanceSecret from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="973c8-117">執行這個指令需要「清除」許可權，該許可權必須是先前已明確授與使用者的此金鑰保存庫。</span><span class="sxs-lookup"><span data-stu-id="973c8-117">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

## <span data-ttu-id="973c8-118">參數</span><span class="sxs-lookup"><span data-stu-id="973c8-118">PARAMETERS</span></span>

### <span data-ttu-id="973c8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="973c8-119">-DefaultProfile</span></span>
<span data-ttu-id="973c8-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="973c8-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="973c8-121">-Force</span><span class="sxs-lookup"><span data-stu-id="973c8-121">-Force</span></span>
<span data-ttu-id="973c8-122">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="973c8-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="973c8-123">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="973c8-123">-InRemovedState</span></span>
<span data-ttu-id="973c8-124">如果有，則會永久移除先前刪除的機密。</span><span class="sxs-lookup"><span data-stu-id="973c8-124">If present, removes the previously deleted secret permanently.</span></span>

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

### <span data-ttu-id="973c8-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="973c8-125">-Name</span></span>
<span data-ttu-id="973c8-126">指定秘密的名稱。</span><span class="sxs-lookup"><span data-stu-id="973c8-126">Specifies the name of a secret.</span></span>
<span data-ttu-id="973c8-127">這個 Cmdlet 會根據此參數指定的名稱、主要電子倉庫的名稱和您目前的環境，來構造密碼的完整功能變數名稱 (FQDN) 。</span><span class="sxs-lookup"><span data-stu-id="973c8-127">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="973c8-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="973c8-128">-PassThru</span></span>
<span data-ttu-id="973c8-129">表示此 Cmdlet 會傳回 **KeyVault** 物件的 [.]</span><span class="sxs-lookup"><span data-stu-id="973c8-129">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.Secret** object.</span></span>
<span data-ttu-id="973c8-130">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="973c8-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="973c8-131">-VaultName</span><span class="sxs-lookup"><span data-stu-id="973c8-131">-VaultName</span></span>
<span data-ttu-id="973c8-132">指定機密所屬之金鑰保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="973c8-132">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="973c8-133">這個 Cmdlet 會根據此參數指定的名稱和您目前的環境，來構造金鑰 vault 的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="973c8-133">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="973c8-134">-確認</span><span class="sxs-lookup"><span data-stu-id="973c8-134">-Confirm</span></span>
<span data-ttu-id="973c8-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="973c8-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="973c8-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="973c8-136">-WhatIf</span></span>
<span data-ttu-id="973c8-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="973c8-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="973c8-138">未執行 Cmdlet。顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="973c8-138">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="973c8-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="973c8-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="973c8-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="973c8-140">CommonParameters</span></span>
<span data-ttu-id="973c8-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="973c8-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="973c8-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="973c8-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="973c8-143">輸入</span><span class="sxs-lookup"><span data-stu-id="973c8-143">INPUTS</span></span>

### <span data-ttu-id="973c8-144">字串</span><span class="sxs-lookup"><span data-stu-id="973c8-144">String</span></span>

## <span data-ttu-id="973c8-145">輸出</span><span class="sxs-lookup"><span data-stu-id="973c8-145">OUTPUTS</span></span>

### <span data-ttu-id="973c8-146">DeletedSecret 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="973c8-146">Microsoft.Azure.Commands.KeyVault.Models.DeletedSecret</span></span>
<span data-ttu-id="973c8-147">這個 Cmdlet 只有在您指定 *PassThru* 參數時才會傳回值。</span><span class="sxs-lookup"><span data-stu-id="973c8-147">This cmdlet returns a value only if you specify the *PassThru* parameter.</span></span>

## <span data-ttu-id="973c8-148">筆記</span><span class="sxs-lookup"><span data-stu-id="973c8-148">NOTES</span></span>

## <span data-ttu-id="973c8-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="973c8-149">RELATED LINKS</span></span>

[<span data-ttu-id="973c8-150">AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="973c8-150">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="973c8-151">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="973c8-151">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

[<span data-ttu-id="973c8-152">復原-AzureKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="973c8-152">Undo-AzureKeyVaultSecretRemoval</span></span>](./Undo-AzureKeyVaultSecretRemoval.md)

