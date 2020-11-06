---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://go.microsoft.com/fwlink/?LinkId=690300
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultSecret.md
ms.openlocfilehash: e5ec1e2377b9a1c04fc10ce976bd800227baabed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454352"
---
# <span data-ttu-id="c8125-101">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="c8125-101">Remove-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="c8125-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c8125-102">SYNOPSIS</span></span>
<span data-ttu-id="c8125-103">刪除金鑰保存庫中的密碼。</span><span class="sxs-lookup"><span data-stu-id="c8125-103">Deletes a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8125-104">句法</span><span class="sxs-lookup"><span data-stu-id="c8125-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8125-105">說明</span><span class="sxs-lookup"><span data-stu-id="c8125-105">DESCRIPTION</span></span>
<span data-ttu-id="c8125-106">Remove-AzureKeyVaultSecret Cmdlet 會刪除金鑰保存庫中的密碼。</span><span class="sxs-lookup"><span data-stu-id="c8125-106">The Remove-AzureKeyVaultSecret cmdlet deletes a secret in a key vault.</span></span>
<span data-ttu-id="c8125-107">如果不小心刪除了機密，您可以使用具有特殊「復原」許可權的使用者 Undo-AzureKeyVaultSecretRemoval 來復原機密。</span><span class="sxs-lookup"><span data-stu-id="c8125-107">If the secret was accidentally deleted the secret can be recovered using Undo-AzureKeyVaultSecretRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="c8125-108">這個 Cmdlet 的值為 high，用於 **ConfirmImpact** 屬性。</span><span class="sxs-lookup"><span data-stu-id="c8125-108">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="c8125-109">示例</span><span class="sxs-lookup"><span data-stu-id="c8125-109">EXAMPLES</span></span>

### <span data-ttu-id="c8125-110">範例1：移除金鑰保存庫的密碼</span><span class="sxs-lookup"><span data-stu-id="c8125-110">Example 1: Remove a secret from a key vault</span></span>
```
PS C:\>Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret'
```

<span data-ttu-id="c8125-111">這個命令會從名為 Contoso 的主要電子倉庫中移除名為 FinanceSecret 的密碼。</span><span class="sxs-lookup"><span data-stu-id="c8125-111">This command removes the secret named FinanceSecret from the key vault named Contoso.'</span></span>

### <span data-ttu-id="c8125-112">範例2：移除金鑰保存庫中不含使用者確認的密碼</span><span class="sxs-lookup"><span data-stu-id="c8125-112">Example 2: Remove a secret from a key vault without user confirmation</span></span>
```
PS C:\>Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -Force -Confirm:$False
```

<span data-ttu-id="c8125-113">這個命令會從名為 Contoso 的主要電子倉庫中移除名為 FinanceSecret 的密碼。</span><span class="sxs-lookup"><span data-stu-id="c8125-113">This command removes the secret named FinanceSecret from the key vault named Contoso.</span></span>
<span data-ttu-id="c8125-114">命令會指定 *Force* 和 *Confirm* 參數，因此 Cmdlet 不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c8125-114">The command specifies the *Force* and *Confirm* parameters, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="c8125-115">範例3：從金鑰保存庫永久清除已刪除的機密</span><span class="sxs-lookup"><span data-stu-id="c8125-115">Example 3: Purge deleted secret from the key vault permanently</span></span>
```
PS C:\>Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -InRemovedState
```

<span data-ttu-id="c8125-116">這個命令會從名為 Contoso 的主要保存庫永久 premoves 名為 FinanceSecret 的密碼。</span><span class="sxs-lookup"><span data-stu-id="c8125-116">This command premoves the secret named FinanceSecret from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="c8125-117">執行這個指令需要「清除」許可權，該許可權必須是先前已明確授與使用者的此金鑰保存庫。</span><span class="sxs-lookup"><span data-stu-id="c8125-117">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

## <span data-ttu-id="c8125-118">參數</span><span class="sxs-lookup"><span data-stu-id="c8125-118">PARAMETERS</span></span>

### <span data-ttu-id="c8125-119">-Force</span><span class="sxs-lookup"><span data-stu-id="c8125-119">-Force</span></span>
<span data-ttu-id="c8125-120">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="c8125-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c8125-121">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="c8125-121">-InRemovedState</span></span>
<span data-ttu-id="c8125-122">如果有，則會永久移除先前刪除的機密。</span><span class="sxs-lookup"><span data-stu-id="c8125-122">If present, removes the previously deleted secret permanently.</span></span>

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

### <span data-ttu-id="c8125-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="c8125-123">-Name</span></span>
<span data-ttu-id="c8125-124">指定秘密的名稱。</span><span class="sxs-lookup"><span data-stu-id="c8125-124">Specifies the name of a secret.</span></span>
<span data-ttu-id="c8125-125">這個 Cmdlet 會根據此參數指定的名稱、主要電子倉庫的名稱和您目前的環境，來構造密碼的完整功能變數名稱 (FQDN) 。</span><span class="sxs-lookup"><span data-stu-id="c8125-125">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SecretName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8125-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c8125-126">-PassThru</span></span>
<span data-ttu-id="c8125-127">表示此 Cmdlet 會傳回 **KeyVault** 物件的 [.]</span><span class="sxs-lookup"><span data-stu-id="c8125-127">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.Secret** object.</span></span>
<span data-ttu-id="c8125-128">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="c8125-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c8125-129">-VaultName</span><span class="sxs-lookup"><span data-stu-id="c8125-129">-VaultName</span></span>
<span data-ttu-id="c8125-130">指定機密所屬之金鑰保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="c8125-130">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="c8125-131">這個 Cmdlet 會根據此參數指定的名稱和您目前的環境，來構造金鑰 vault 的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="c8125-131">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8125-132">-確認</span><span class="sxs-lookup"><span data-stu-id="c8125-132">-Confirm</span></span>
<span data-ttu-id="c8125-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c8125-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8125-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8125-134">-WhatIf</span></span>
<span data-ttu-id="c8125-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c8125-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8125-136">未執行 Cmdlet。顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c8125-136">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8125-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c8125-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8125-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8125-138">-DefaultProfile</span></span>
<span data-ttu-id="c8125-139">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c8125-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8125-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8125-140">CommonParameters</span></span>
<span data-ttu-id="c8125-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c8125-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8125-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c8125-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8125-143">輸入</span><span class="sxs-lookup"><span data-stu-id="c8125-143">INPUTS</span></span>

### <span data-ttu-id="c8125-144">字串</span><span class="sxs-lookup"><span data-stu-id="c8125-144">String</span></span>

## <span data-ttu-id="c8125-145">輸出</span><span class="sxs-lookup"><span data-stu-id="c8125-145">OUTPUTS</span></span>

### <span data-ttu-id="c8125-146">DeletedSecret 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="c8125-146">Microsoft.Azure.Commands.KeyVault.Models.DeletedSecret</span></span>
<span data-ttu-id="c8125-147">這個 Cmdlet 只有在您指定 *PassThru* 參數時才會傳回值。</span><span class="sxs-lookup"><span data-stu-id="c8125-147">This cmdlet returns a value only if you specify the *PassThru* parameter.</span></span>

## <span data-ttu-id="c8125-148">筆記</span><span class="sxs-lookup"><span data-stu-id="c8125-148">NOTES</span></span>

## <span data-ttu-id="c8125-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="c8125-149">RELATED LINKS</span></span>

[<span data-ttu-id="c8125-150">AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="c8125-150">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="c8125-151">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="c8125-151">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

[<span data-ttu-id="c8125-152">復原-AzureKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="c8125-152">Undo-AzureKeyVaultSecretRemoval</span></span>](./Undo-AzureKeyVaultSecretRemoval.md)

