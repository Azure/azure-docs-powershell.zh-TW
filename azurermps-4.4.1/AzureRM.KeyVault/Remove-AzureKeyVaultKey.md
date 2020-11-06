---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 817BF177-519F-47BA-86CF-4591FB402E2Dl
online version: https://go.microsoft.com/fwlink/?LinkId=690299
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultKey.md
ms.openlocfilehash: b5f2917da71e8c4539660dbb91dd81f3fb5d7959
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454367"
---
# <span data-ttu-id="2e899-101">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="2e899-101">Remove-AzureKeyVaultKey</span></span>

## <span data-ttu-id="2e899-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2e899-102">SYNOPSIS</span></span>
<span data-ttu-id="2e899-103">刪除主要電子倉庫中的金鑰。</span><span class="sxs-lookup"><span data-stu-id="2e899-103">Deletes a key in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e899-104">句法</span><span class="sxs-lookup"><span data-stu-id="2e899-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e899-105">說明</span><span class="sxs-lookup"><span data-stu-id="2e899-105">DESCRIPTION</span></span>
<span data-ttu-id="2e899-106">Remove-AzureKeyVaultKey Cmdlet 會刪除金鑰保存庫中的金鑰。</span><span class="sxs-lookup"><span data-stu-id="2e899-106">The Remove-AzureKeyVaultKey cmdlet deletes a key in a key vault.</span></span>
<span data-ttu-id="2e899-107">如果不小心刪除了金鑰，則可以使用具有特殊「復原」許可權的使用者 Undo-AzureKeyVaultKeyRemoval 來復原金鑰。</span><span class="sxs-lookup"><span data-stu-id="2e899-107">If the key was accidentally deleted the key can be recovered using Undo-AzureKeyVaultKeyRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="2e899-108">這個 Cmdlet 的值為 high，用於 **ConfirmImpact** 屬性。</span><span class="sxs-lookup"><span data-stu-id="2e899-108">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="2e899-109">示例</span><span class="sxs-lookup"><span data-stu-id="2e899-109">EXAMPLES</span></span>

### <span data-ttu-id="2e899-110">範例1：從金鑰保存庫移除金鑰</span><span class="sxs-lookup"><span data-stu-id="2e899-110">Example 1: Remove a key from a key vault</span></span>
```
PS C:\>Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware'
```

<span data-ttu-id="2e899-111">這個命令會從名為 Contoso 的主要電子倉庫中移除名為 ITSoftware 的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="2e899-111">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>

### <span data-ttu-id="2e899-112">範例2：在未確認使用者的情況下移除金鑰</span><span class="sxs-lookup"><span data-stu-id="2e899-112">Example 2: Remove a key without user confirmation</span></span>
```
PS C:\>Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Force -Confirm:$False
```

<span data-ttu-id="2e899-113">這個命令會從名為 Contoso 的主要電子倉庫中移除名為 ITSoftware 的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="2e899-113">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>
<span data-ttu-id="2e899-114">命令會指定 *Force* 和 *Confirm* 參數，因此 Cmdlet 不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2e899-114">The command specifies the *Force* and *Confirm* parameters, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="2e899-115">範例3：從金鑰 vault 永久清除已刪除的金鑰</span><span class="sxs-lookup"><span data-stu-id="2e899-115">Example 3: Purge a deleted key from the key vault permanently</span></span>
```
PS C:\>Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -InRemovedState
```

<span data-ttu-id="2e899-116">這個命令會從名為 Contoso 的主要電子倉庫永久刪除名為 ITSoftware 的金鑰。</span><span class="sxs-lookup"><span data-stu-id="2e899-116">This command removes the key named ITSoftware from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="2e899-117">執行這個指令需要「清除」許可權，該許可權必須是先前已明確授與使用者的此金鑰保存庫。</span><span class="sxs-lookup"><span data-stu-id="2e899-117">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

### <span data-ttu-id="2e899-118">範例4：使用管線運算子移除按鍵</span><span class="sxs-lookup"><span data-stu-id="2e899-118">Example 4: Remove keys by using the pipeline operator</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzureKeyVaultKey
```

<span data-ttu-id="2e899-119">這個命令會取得名為 Contoso 的主要電子倉庫中的所有金鑰，並使用管線運算子將它們傳遞到 **物件** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2e899-119">This command gets all the keys in the key vault named Contoso, and passes them to the **Where-Object** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="2e899-120">這個 Cmdlet 會將已 **啟用** 屬性的值 $False 的金鑰傳遞給目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2e899-120">That cmdlet passes the keys that have a value of $False for the **Enabled** attribute to the current cmdlet.</span></span>
<span data-ttu-id="2e899-121">該 Cmdlet 會移除這些索引鍵。</span><span class="sxs-lookup"><span data-stu-id="2e899-121">That cmdlet removes those keys.</span></span>

## <span data-ttu-id="2e899-122">參數</span><span class="sxs-lookup"><span data-stu-id="2e899-122">PARAMETERS</span></span>

### <span data-ttu-id="2e899-123">-Force</span><span class="sxs-lookup"><span data-stu-id="2e899-123">-Force</span></span>
<span data-ttu-id="2e899-124">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="2e899-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2e899-125">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="2e899-125">-InRemovedState</span></span>
<span data-ttu-id="2e899-126">永久移除先前刪除的金鑰。</span><span class="sxs-lookup"><span data-stu-id="2e899-126">Remove the previously deleted key permanently.</span></span>

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

### <span data-ttu-id="2e899-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="2e899-127">-Name</span></span>
<span data-ttu-id="2e899-128">指定要移除的索引鍵名。</span><span class="sxs-lookup"><span data-stu-id="2e899-128">Specifies the name of the key to remove.</span></span>
<span data-ttu-id="2e899-129">這個 Cmdlet 會根據此參數指定的名稱、主要電子倉庫的名稱和您目前的環境，來構造金鑰的完整功能變數名稱 (FQDN) 。</span><span class="sxs-lookup"><span data-stu-id="2e899-129">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e899-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2e899-130">-PassThru</span></span>
<span data-ttu-id="2e899-131">表示此 Cmdlet 會傳回 **KeyVault KeyBundle** 物件的命令。</span><span class="sxs-lookup"><span data-stu-id="2e899-131">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** object.</span></span>
<span data-ttu-id="2e899-132">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="2e899-132">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2e899-133">-VaultName</span><span class="sxs-lookup"><span data-stu-id="2e899-133">-VaultName</span></span>
<span data-ttu-id="2e899-134">指定要從中移除金鑰的主要電子倉庫名稱。</span><span class="sxs-lookup"><span data-stu-id="2e899-134">Specifies the name of the key vault from which to remove the key.</span></span>
<span data-ttu-id="2e899-135">這個 Cmdlet 會根據此參數指定的名稱和您目前的環境，來構造金鑰 vault 的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="2e899-135">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="2e899-136">-確認</span><span class="sxs-lookup"><span data-stu-id="2e899-136">-Confirm</span></span>
<span data-ttu-id="2e899-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2e899-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e899-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e899-138">-WhatIf</span></span>
<span data-ttu-id="2e899-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2e899-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e899-140">未執行 Cmdlet。顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2e899-140">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e899-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2e899-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e899-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e899-142">-DefaultProfile</span></span>
<span data-ttu-id="2e899-143">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2e899-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e899-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e899-144">CommonParameters</span></span>
<span data-ttu-id="2e899-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2e899-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e899-146">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2e899-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e899-147">輸入</span><span class="sxs-lookup"><span data-stu-id="2e899-147">INPUTS</span></span>

### <span data-ttu-id="2e899-148">字串</span><span class="sxs-lookup"><span data-stu-id="2e899-148">String</span></span>

## <span data-ttu-id="2e899-149">輸出</span><span class="sxs-lookup"><span data-stu-id="2e899-149">OUTPUTS</span></span>

### <span data-ttu-id="2e899-150">DeletedKeyBundle 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="2e899-150">Microsoft.Azure.Commands.KeyVault.Models.DeletedKeyBundle</span></span>
<span data-ttu-id="2e899-151">這個 Cmdlet 只有在您指定 *PassThru* 參數時才會傳回值。</span><span class="sxs-lookup"><span data-stu-id="2e899-151">This cmdlet returns a value only if you specify the *PassThru* parameter.</span></span>

## <span data-ttu-id="2e899-152">筆記</span><span class="sxs-lookup"><span data-stu-id="2e899-152">NOTES</span></span>

## <span data-ttu-id="2e899-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="2e899-153">RELATED LINKS</span></span>

[<span data-ttu-id="2e899-154">附加 AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="2e899-154">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="2e899-155">AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="2e899-155">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="2e899-156">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="2e899-156">Set-AzureKeyVaultKeyAttribute</span></span>](./Set-AzureKeyVaultKeyAttribute.md)

[<span data-ttu-id="2e899-157">復原-AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="2e899-157">Undo-AzureKeyVaultKeyRemoval</span></span>](./Undo-AzureKeyVaultKeyRemoval.md)

