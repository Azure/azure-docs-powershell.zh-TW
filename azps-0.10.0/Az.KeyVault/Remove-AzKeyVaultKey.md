---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 817BF177-519F-47BA-86CF-4591FB402E2Dl
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-AzKeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultKey.md
ms.openlocfilehash: 15470f18e457f31deec66554c955890b52e26e83
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794654"
---
# <span data-ttu-id="7a9a9-101">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="7a9a9-101">Remove-AzKeyVaultKey</span></span>

## <span data-ttu-id="7a9a9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7a9a9-102">SYNOPSIS</span></span>
<span data-ttu-id="7a9a9-103">刪除主要電子倉庫中的金鑰。</span><span class="sxs-lookup"><span data-stu-id="7a9a9-103">Deletes a key in a key vault.</span></span>

## <span data-ttu-id="7a9a9-104">句法</span><span class="sxs-lookup"><span data-stu-id="7a9a9-104">SYNTAX</span></span>

```
Remove-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a9a9-105">說明</span><span class="sxs-lookup"><span data-stu-id="7a9a9-105">DESCRIPTION</span></span>
<span data-ttu-id="7a9a9-106">Remove-AzKeyVaultKey Cmdlet 會刪除金鑰保存庫中的金鑰。</span><span class="sxs-lookup"><span data-stu-id="7a9a9-106">The Remove-AzKeyVaultKey cmdlet deletes a key in a key vault.</span></span>
<span data-ttu-id="7a9a9-107">如果不小心刪除了金鑰，則可以使用具有特殊「復原」許可權的使用者 Undo-AzKeyVaultKeyRemoval 來復原金鑰。</span><span class="sxs-lookup"><span data-stu-id="7a9a9-107">If the key was accidentally deleted the key can be recovered using Undo-AzKeyVaultKeyRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="7a9a9-108">這個 Cmdlet 的值為 high，用於 **ConfirmImpact** 屬性。</span><span class="sxs-lookup"><span data-stu-id="7a9a9-108">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="7a9a9-109">示例</span><span class="sxs-lookup"><span data-stu-id="7a9a9-109">EXAMPLES</span></span>

### <span data-ttu-id="7a9a9-110">範例1：從金鑰保存庫移除金鑰</span><span class="sxs-lookup"><span data-stu-id="7a9a9-110">Example 1: Remove a key from a key vault</span></span>
```
PS C:\>Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware'
```

<span data-ttu-id="7a9a9-111">這個命令會從名為 Contoso 的主要電子倉庫中移除名為 ITSoftware 的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="7a9a9-111">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>

### <span data-ttu-id="7a9a9-112">範例2：在未確認使用者的情況下移除金鑰</span><span class="sxs-lookup"><span data-stu-id="7a9a9-112">Example 2: Remove a key without user confirmation</span></span>
```
PS C:\>Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Force -Confirm:$False
```

<span data-ttu-id="7a9a9-113">這個命令會從名為 Contoso 的主要電子倉庫中移除名為 ITSoftware 的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="7a9a9-113">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>
<span data-ttu-id="7a9a9-114">命令會指定 *Force* 和 *Confirm* 參數，因此 Cmdlet 不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="7a9a9-114">The command specifies the *Force* and *Confirm* parameters, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="7a9a9-115">範例3：從金鑰 vault 永久清除已刪除的金鑰</span><span class="sxs-lookup"><span data-stu-id="7a9a9-115">Example 3: Purge a deleted key from the key vault permanently</span></span>
```
PS C:\>Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -InRemovedState
```

<span data-ttu-id="7a9a9-116">這個命令會從名為 Contoso 的主要電子倉庫永久刪除名為 ITSoftware 的金鑰。</span><span class="sxs-lookup"><span data-stu-id="7a9a9-116">This command removes the key named ITSoftware from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="7a9a9-117">執行這個指令需要「清除」許可權，該許可權必須是先前已明確授與使用者的此金鑰保存庫。</span><span class="sxs-lookup"><span data-stu-id="7a9a9-117">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

### <span data-ttu-id="7a9a9-118">範例4：使用管線運算子移除按鍵</span><span class="sxs-lookup"><span data-stu-id="7a9a9-118">Example 4: Remove keys by using the pipeline operator</span></span>
```
PS C:\>Get-AzKeyVaultKey -VaultName 'Contoso' | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzKeyVaultKey
```

<span data-ttu-id="7a9a9-119">這個命令會取得名為 Contoso 的主要電子倉庫中的所有金鑰，並使用管線運算子將它們傳遞到 **物件** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7a9a9-119">This command gets all the keys in the key vault named Contoso, and passes them to the **Where-Object** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7a9a9-120">這個 Cmdlet 會將已 **啟用** 屬性的值 $False 的金鑰傳遞給目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7a9a9-120">That cmdlet passes the keys that have a value of $False for the **Enabled** attribute to the current cmdlet.</span></span>
<span data-ttu-id="7a9a9-121">該 Cmdlet 會移除這些索引鍵。</span><span class="sxs-lookup"><span data-stu-id="7a9a9-121">That cmdlet removes those keys.</span></span>

## <span data-ttu-id="7a9a9-122">參數</span><span class="sxs-lookup"><span data-stu-id="7a9a9-122">PARAMETERS</span></span>

### <span data-ttu-id="7a9a9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a9a9-123">-DefaultProfile</span></span>
<span data-ttu-id="7a9a9-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="7a9a9-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a9a9-125">-Force</span><span class="sxs-lookup"><span data-stu-id="7a9a9-125">-Force</span></span>
<span data-ttu-id="7a9a9-126">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="7a9a9-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7a9a9-127">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="7a9a9-127">-InRemovedState</span></span>
<span data-ttu-id="7a9a9-128">永久移除先前刪除的金鑰。</span><span class="sxs-lookup"><span data-stu-id="7a9a9-128">Remove the previously deleted key permanently.</span></span>

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

### <span data-ttu-id="7a9a9-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="7a9a9-129">-Name</span></span>
<span data-ttu-id="7a9a9-130">指定要移除的索引鍵名。</span><span class="sxs-lookup"><span data-stu-id="7a9a9-130">Specifies the name of the key to remove.</span></span>
<span data-ttu-id="7a9a9-131">這個 Cmdlet 會根據此參數指定的名稱、主要電子倉庫的名稱和您目前的環境，來構造金鑰的完整功能變數名稱 (FQDN) 。</span><span class="sxs-lookup"><span data-stu-id="7a9a9-131">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a9a9-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7a9a9-132">-PassThru</span></span>
<span data-ttu-id="7a9a9-133">表示此 Cmdlet 會傳回 **KeyVault KeyBundle** 物件的命令。</span><span class="sxs-lookup"><span data-stu-id="7a9a9-133">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** object.</span></span>
<span data-ttu-id="7a9a9-134">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="7a9a9-134">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7a9a9-135">-VaultName</span><span class="sxs-lookup"><span data-stu-id="7a9a9-135">-VaultName</span></span>
<span data-ttu-id="7a9a9-136">指定要從中移除金鑰的主要電子倉庫名稱。</span><span class="sxs-lookup"><span data-stu-id="7a9a9-136">Specifies the name of the key vault from which to remove the key.</span></span>
<span data-ttu-id="7a9a9-137">這個 Cmdlet 會根據此參數指定的名稱和您目前的環境，來構造金鑰 vault 的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="7a9a9-137">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="7a9a9-138">-確認</span><span class="sxs-lookup"><span data-stu-id="7a9a9-138">-Confirm</span></span>
<span data-ttu-id="7a9a9-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7a9a9-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a9a9-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a9a9-140">-WhatIf</span></span>
<span data-ttu-id="7a9a9-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7a9a9-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a9a9-142">未執行 Cmdlet。顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7a9a9-142">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a9a9-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7a9a9-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a9a9-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a9a9-144">CommonParameters</span></span>
<span data-ttu-id="7a9a9-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7a9a9-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a9a9-146">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7a9a9-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a9a9-147">輸入</span><span class="sxs-lookup"><span data-stu-id="7a9a9-147">INPUTS</span></span>

### <span data-ttu-id="7a9a9-148">字串</span><span class="sxs-lookup"><span data-stu-id="7a9a9-148">String</span></span>

## <span data-ttu-id="7a9a9-149">輸出</span><span class="sxs-lookup"><span data-stu-id="7a9a9-149">OUTPUTS</span></span>

### <span data-ttu-id="7a9a9-150">DeletedKeyBundle 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="7a9a9-150">Microsoft.Azure.Commands.KeyVault.Models.DeletedKeyBundle</span></span>
<span data-ttu-id="7a9a9-151">這個 Cmdlet 只有在您指定 *PassThru* 參數時才會傳回值。</span><span class="sxs-lookup"><span data-stu-id="7a9a9-151">This cmdlet returns a value only if you specify the *PassThru* parameter.</span></span>

## <span data-ttu-id="7a9a9-152">筆記</span><span class="sxs-lookup"><span data-stu-id="7a9a9-152">NOTES</span></span>

## <span data-ttu-id="7a9a9-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="7a9a9-153">RELATED LINKS</span></span>

[<span data-ttu-id="7a9a9-154">附加 AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="7a9a9-154">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="7a9a9-155">AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="7a9a9-155">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="7a9a9-156">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="7a9a9-156">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)

[<span data-ttu-id="7a9a9-157">復原-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="7a9a9-157">Undo-AzKeyVaultKeyRemoval</span></span>](./Undo-AzKeyVaultKeyRemoval.md)

