---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 817BF177-519F-47BA-86CF-4591FB402E2Dl
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultKey.md
ms.openlocfilehash: bfdd237ecadadae181d9e9dd3a201580537097f0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141655"
---
# <span data-ttu-id="4ba58-101">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4ba58-101">Remove-AzKeyVaultKey</span></span>

## <span data-ttu-id="4ba58-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4ba58-102">SYNOPSIS</span></span>
<span data-ttu-id="4ba58-103">刪除主要電子倉庫中的金鑰。</span><span class="sxs-lookup"><span data-stu-id="4ba58-103">Deletes a key in a key vault.</span></span>

## <span data-ttu-id="4ba58-104">句法</span><span class="sxs-lookup"><span data-stu-id="4ba58-104">SYNTAX</span></span>

### <span data-ttu-id="4ba58-105">ByVaultName (預設) </span><span class="sxs-lookup"><span data-stu-id="4ba58-105">ByVaultName (Default)</span></span>
```
Remove-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ba58-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4ba58-106">ByInputObject</span></span>
```
Remove-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ba58-107">說明</span><span class="sxs-lookup"><span data-stu-id="4ba58-107">DESCRIPTION</span></span>
<span data-ttu-id="4ba58-108">Remove-AzKeyVaultKey Cmdlet 會刪除金鑰保存庫中的金鑰。</span><span class="sxs-lookup"><span data-stu-id="4ba58-108">The Remove-AzKeyVaultKey cmdlet deletes a key in a key vault.</span></span>
<span data-ttu-id="4ba58-109">如果不小心刪除了金鑰，則可以使用具有特殊「復原」許可權的使用者 Undo-AzKeyVaultKeyRemoval 來復原金鑰。</span><span class="sxs-lookup"><span data-stu-id="4ba58-109">If the key was accidentally deleted the key can be recovered using Undo-AzKeyVaultKeyRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="4ba58-110">這個 Cmdlet 的值為 high，用於 **ConfirmImpact** 屬性。</span><span class="sxs-lookup"><span data-stu-id="4ba58-110">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="4ba58-111">示例</span><span class="sxs-lookup"><span data-stu-id="4ba58-111">EXAMPLES</span></span>

### <span data-ttu-id="4ba58-112">範例1：從金鑰保存庫移除金鑰</span><span class="sxs-lookup"><span data-stu-id="4ba58-112">Example 1: Remove a key from a key vault</span></span>
```powershell
PS C:\> Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -PassThru

Vault Name           : contoso
Name                 : key2
Id                   : https://contoso.vault.azure.net:443/keys/itsoftware/fdad15793ba0437e960497908ef9eb32
Deleted Date         : 5/24/2018 11:28:25 PM
Scheduled Purge Date : 8/22/2018 11:28:25 PM
Enabled              : False
Expires              : 10/11/2018 11:32:49 PM
Not Before           : 4/11/2018 11:22:49 PM
Created              : 4/12/2018 10:16:38 PM
Updated              : 4/12/2018 10:16:38 PM
Purge Disabled       : False
Tags                 :
```

<span data-ttu-id="4ba58-113">這個命令會從名為 Contoso 的主要電子倉庫中移除名為 ITSoftware 的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="4ba58-113">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>

### <span data-ttu-id="4ba58-114">範例2：在未確認使用者的情況下移除金鑰</span><span class="sxs-lookup"><span data-stu-id="4ba58-114">Example 2: Remove a key without user confirmation</span></span>
```powershell
PS C:\> Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Force
```

<span data-ttu-id="4ba58-115">這個命令會從名為 Contoso 的主要電子倉庫中移除名為 ITSoftware 的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="4ba58-115">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>
<span data-ttu-id="4ba58-116">此命令會指定 *Force* 參數，因此 Cmdlet 不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4ba58-116">The command specifies the *Force* parameter, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="4ba58-117">範例3：從金鑰 vault 永久清除已刪除的金鑰</span><span class="sxs-lookup"><span data-stu-id="4ba58-117">Example 3: Purge a deleted key from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -InRemovedState
```

<span data-ttu-id="4ba58-118">這個命令會從名為 Contoso 的主要電子倉庫永久刪除名為 ITSoftware 的金鑰。</span><span class="sxs-lookup"><span data-stu-id="4ba58-118">This command removes the key named ITSoftware from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="4ba58-119">執行這個指令需要「清除」許可權，該許可權必須是先前已明確授與使用者的此金鑰保存庫。</span><span class="sxs-lookup"><span data-stu-id="4ba58-119">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

### <span data-ttu-id="4ba58-120">範例4：使用管線運算子移除按鍵</span><span class="sxs-lookup"><span data-stu-id="4ba58-120">Example 4: Remove keys by using the pipeline operator</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'Contoso' | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzKeyVaultKey
```

<span data-ttu-id="4ba58-121">這個命令會取得名為 Contoso 的主要電子倉庫中的所有金鑰，並使用管線運算子將它們傳遞到 **物件** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4ba58-121">This command gets all the keys in the key vault named Contoso, and passes them to the **Where-Object** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="4ba58-122">這個 Cmdlet 會將已 **啟用** 屬性的值 $False 的金鑰傳遞給目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4ba58-122">That cmdlet passes the keys that have a value of $False for the **Enabled** attribute to the current cmdlet.</span></span>
<span data-ttu-id="4ba58-123">該 Cmdlet 會移除這些索引鍵。</span><span class="sxs-lookup"><span data-stu-id="4ba58-123">That cmdlet removes those keys.</span></span>

## <span data-ttu-id="4ba58-124">參數</span><span class="sxs-lookup"><span data-stu-id="4ba58-124">PARAMETERS</span></span>

### <span data-ttu-id="4ba58-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ba58-125">-DefaultProfile</span></span>
<span data-ttu-id="4ba58-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="4ba58-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4ba58-127">-Force</span><span class="sxs-lookup"><span data-stu-id="4ba58-127">-Force</span></span>
<span data-ttu-id="4ba58-128">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="4ba58-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4ba58-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4ba58-129">-InputObject</span></span>
<span data-ttu-id="4ba58-130">KeyBundle 物件</span><span class="sxs-lookup"><span data-stu-id="4ba58-130">KeyBundle Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ba58-131">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="4ba58-131">-InRemovedState</span></span>
<span data-ttu-id="4ba58-132">永久移除先前刪除的金鑰。</span><span class="sxs-lookup"><span data-stu-id="4ba58-132">Remove the previously deleted key permanently.</span></span>

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

### <span data-ttu-id="4ba58-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="4ba58-133">-Name</span></span>
<span data-ttu-id="4ba58-134">指定要移除的索引鍵名。</span><span class="sxs-lookup"><span data-stu-id="4ba58-134">Specifies the name of the key to remove.</span></span>
<span data-ttu-id="4ba58-135">這個 Cmdlet 會根據此參數指定的名稱、主要電子倉庫的名稱和您目前的環境，來構造金鑰的完整功能變數名稱 (FQDN) 。</span><span class="sxs-lookup"><span data-stu-id="4ba58-135">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ba58-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4ba58-136">-PassThru</span></span>
<span data-ttu-id="4ba58-137">表示此 Cmdlet 會傳回 **KeyVault PSKeyVaultKey** 物件的命令。</span><span class="sxs-lookup"><span data-stu-id="4ba58-137">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey** object.</span></span>
<span data-ttu-id="4ba58-138">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="4ba58-138">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4ba58-139">-VaultName</span><span class="sxs-lookup"><span data-stu-id="4ba58-139">-VaultName</span></span>
<span data-ttu-id="4ba58-140">指定要從中移除金鑰的主要電子倉庫名稱。</span><span class="sxs-lookup"><span data-stu-id="4ba58-140">Specifies the name of the key vault from which to remove the key.</span></span>
<span data-ttu-id="4ba58-141">這個 Cmdlet 會根據此參數指定的名稱和您目前的環境，來構造金鑰 vault 的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="4ba58-141">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="4ba58-142">-確認</span><span class="sxs-lookup"><span data-stu-id="4ba58-142">-Confirm</span></span>
<span data-ttu-id="4ba58-143">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4ba58-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ba58-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ba58-144">-WhatIf</span></span>
<span data-ttu-id="4ba58-145">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4ba58-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ba58-146">未執行 Cmdlet。顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4ba58-146">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ba58-147">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4ba58-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ba58-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ba58-148">CommonParameters</span></span>
<span data-ttu-id="4ba58-149">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4ba58-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ba58-150">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4ba58-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ba58-151">輸入</span><span class="sxs-lookup"><span data-stu-id="4ba58-151">INPUTS</span></span>

### <span data-ttu-id="4ba58-152">PSKeyVaultKeyIdentityItem 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="4ba58-152">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="4ba58-153">輸出</span><span class="sxs-lookup"><span data-stu-id="4ba58-153">OUTPUTS</span></span>

### <span data-ttu-id="4ba58-154">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4ba58-154">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="4ba58-155">筆記</span><span class="sxs-lookup"><span data-stu-id="4ba58-155">NOTES</span></span>

## <span data-ttu-id="4ba58-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="4ba58-156">RELATED LINKS</span></span>

[<span data-ttu-id="4ba58-157">附加 AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4ba58-157">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="4ba58-158">AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4ba58-158">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="4ba58-159">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="4ba58-159">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)

[<span data-ttu-id="4ba58-160">復原-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="4ba58-160">Undo-AzKeyVaultKeyRemoval</span></span>](./Undo-AzKeyVaultKeyRemoval.md)
