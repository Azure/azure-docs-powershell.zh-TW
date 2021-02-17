---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 817BF177-519F-47BA-86CF-4591FB402E2Dl
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultKey.md
ms.openlocfilehash: 3c5435d1a472341d0447ead2f384fa892d6e1202
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100404474"
---
# <span data-ttu-id="078d4-101">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="078d4-101">Remove-AzKeyVaultKey</span></span>

## <span data-ttu-id="078d4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="078d4-102">SYNOPSIS</span></span>
<span data-ttu-id="078d4-103">刪除金鑰庫中的金鑰。</span><span class="sxs-lookup"><span data-stu-id="078d4-103">Deletes a key in a key vault.</span></span>

## <span data-ttu-id="078d4-104">語法</span><span class="sxs-lookup"><span data-stu-id="078d4-104">SYNTAX</span></span>

### <span data-ttu-id="078d4-105">ByVaultName (預設) </span><span class="sxs-lookup"><span data-stu-id="078d4-105">ByVaultName (Default)</span></span>
```
Remove-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="078d4-106">HsmByVaultName</span><span class="sxs-lookup"><span data-stu-id="078d4-106">HsmByVaultName</span></span>
```
Remove-AzKeyVaultKey -HsmName <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="078d4-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="078d4-107">ByInputObject</span></span>
```
Remove-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="078d4-108">描述</span><span class="sxs-lookup"><span data-stu-id="078d4-108">DESCRIPTION</span></span>
<span data-ttu-id="078d4-109">Cmdlet Remove-AzKeyVaultKey刪除金鑰庫中的金鑰。</span><span class="sxs-lookup"><span data-stu-id="078d4-109">The Remove-AzKeyVaultKey cmdlet deletes a key in a key vault.</span></span>
<span data-ttu-id="078d4-110">如果金鑰意外刪除，則具有特殊Undo-AzKeyVaultKeyRemoval金鑰的使用者可以使用該金鑰來復原。</span><span class="sxs-lookup"><span data-stu-id="078d4-110">If the key was accidentally deleted the key can be recovered using Undo-AzKeyVaultKeyRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="078d4-111">此 Cmdlet 的 **ConfirmImpact** 屬性的值為高。</span><span class="sxs-lookup"><span data-stu-id="078d4-111">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="078d4-112">例子</span><span class="sxs-lookup"><span data-stu-id="078d4-112">EXAMPLES</span></span>

### <span data-ttu-id="078d4-113">範例 1：從金鑰庫移除金鑰</span><span class="sxs-lookup"><span data-stu-id="078d4-113">Example 1: Remove a key from a key vault</span></span>
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

<span data-ttu-id="078d4-114">此命令會從名為 Contoso 的金鑰庫移除名為 ITSoftware 的金鑰。</span><span class="sxs-lookup"><span data-stu-id="078d4-114">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>

### <span data-ttu-id="078d4-115">範例 2：移除沒有使用者確認的金鑰</span><span class="sxs-lookup"><span data-stu-id="078d4-115">Example 2: Remove a key without user confirmation</span></span>
```powershell
PS C:\> Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Force
```

<span data-ttu-id="078d4-116">此命令會從名為 Contoso 的金鑰庫移除名為 ITSoftware 的金鑰。</span><span class="sxs-lookup"><span data-stu-id="078d4-116">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>
<span data-ttu-id="078d4-117">命令會指定 *Force* 參數，因此 Cmdlet 不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="078d4-117">The command specifies the *Force* parameter, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="078d4-118">範例 3：永久清除從金鑰保存庫刪除的金鑰</span><span class="sxs-lookup"><span data-stu-id="078d4-118">Example 3: Purge a deleted key from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -InRemovedState
```

<span data-ttu-id="078d4-119">此命令會從名為 Contoso 的金鑰保存庫永久移除名為 ITSoftware 的金鑰。</span><span class="sxs-lookup"><span data-stu-id="078d4-119">This command removes the key named ITSoftware from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="078d4-120">執行此 Cmdlet 需要'清除」許可權，此許可權必須先前已明確授予此金鑰庫的使用者。</span><span class="sxs-lookup"><span data-stu-id="078d4-120">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

### <span data-ttu-id="078d4-121">範例 4：使用管線運算子移除金鑰</span><span class="sxs-lookup"><span data-stu-id="078d4-121">Example 4: Remove keys by using the pipeline operator</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'Contoso' | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzKeyVaultKey
```

<span data-ttu-id="078d4-122">此命令會獲得名稱為 Contoso 的金鑰庫中的所有金鑰，然後使用管線運算子將它們傳遞至 **Where-Object** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="078d4-122">This command gets all the keys in the key vault named Contoso, and passes them to the **Where-Object** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="078d4-123">該 Cmdlet 會將具有值 $False **Enabled** 屬性的按鍵傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="078d4-123">That cmdlet passes the keys that have a value of $False for the **Enabled** attribute to the current cmdlet.</span></span>
<span data-ttu-id="078d4-124">該 Cmdlet 會移除這些按鍵。</span><span class="sxs-lookup"><span data-stu-id="078d4-124">That cmdlet removes those keys.</span></span>

## <span data-ttu-id="078d4-125">參數</span><span class="sxs-lookup"><span data-stu-id="078d4-125">PARAMETERS</span></span>

### <span data-ttu-id="078d4-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="078d4-126">-DefaultProfile</span></span>
<span data-ttu-id="078d4-127">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="078d4-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="078d4-128">-強制</span><span class="sxs-lookup"><span data-stu-id="078d4-128">-Force</span></span>
<span data-ttu-id="078d4-129">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="078d4-129">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="078d4-130">-HsmName</span><span class="sxs-lookup"><span data-stu-id="078d4-130">-HsmName</span></span>
<span data-ttu-id="078d4-131">HSM 名稱。</span><span class="sxs-lookup"><span data-stu-id="078d4-131">HSM name.</span></span> <span data-ttu-id="078d4-132">Cmdlet 會根據名稱和目前選取的環境，建構受管理 HSM 的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="078d4-132">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmByVaultName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="078d4-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="078d4-133">-InputObject</span></span>
<span data-ttu-id="078d4-134">KeyBundle 物件</span><span class="sxs-lookup"><span data-stu-id="078d4-134">KeyBundle Object</span></span>

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

### <span data-ttu-id="078d4-135">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="078d4-135">-InRemovedState</span></span>
<span data-ttu-id="078d4-136">永久移除先前刪除的金鑰。</span><span class="sxs-lookup"><span data-stu-id="078d4-136">Remove the previously deleted key permanently.</span></span>

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

### <span data-ttu-id="078d4-137">-名稱</span><span class="sxs-lookup"><span data-stu-id="078d4-137">-Name</span></span>
<span data-ttu-id="078d4-138">指定要移除的金鑰名稱。</span><span class="sxs-lookup"><span data-stu-id="078d4-138">Specifies the name of the key to remove.</span></span>
<span data-ttu-id="078d4-139">此 Cmdlet 會依據此參數指定的名稱、金鑰庫的名稱，以及您目前的環境，建構金鑰的完全限定功能變數名稱 (FQDN) 。</span><span class="sxs-lookup"><span data-stu-id="078d4-139">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, HsmByVaultName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="078d4-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="078d4-140">-PassThru</span></span>
<span data-ttu-id="078d4-141">表示此 Cmdlet 會返回 **Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultKey** 物件。</span><span class="sxs-lookup"><span data-stu-id="078d4-141">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey** object.</span></span>
<span data-ttu-id="078d4-142">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="078d4-142">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="078d4-143">-VaultName</span><span class="sxs-lookup"><span data-stu-id="078d4-143">-VaultName</span></span>
<span data-ttu-id="078d4-144">指定要移除金鑰的金鑰庫名稱。</span><span class="sxs-lookup"><span data-stu-id="078d4-144">Specifies the name of the key vault from which to remove the key.</span></span>
<span data-ttu-id="078d4-145">此 Cmdlet 會依據此參數指定的名稱和您目前的環境，建構金鑰庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="078d4-145">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="078d4-146">-確認</span><span class="sxs-lookup"><span data-stu-id="078d4-146">-Confirm</span></span>
<span data-ttu-id="078d4-147">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="078d4-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="078d4-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="078d4-148">-WhatIf</span></span>
<span data-ttu-id="078d4-149">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="078d4-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="078d4-150">不會執行 Cmdlet。顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="078d4-150">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="078d4-151">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="078d4-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="078d4-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="078d4-152">CommonParameters</span></span>
<span data-ttu-id="078d4-153">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="078d4-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="078d4-154">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="078d4-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="078d4-155">輸入</span><span class="sxs-lookup"><span data-stu-id="078d4-155">INPUTS</span></span>

### <span data-ttu-id="078d4-156">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="078d4-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="078d4-157">輸出</span><span class="sxs-lookup"><span data-stu-id="078d4-157">OUTPUTS</span></span>

### <span data-ttu-id="078d4-158">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="078d4-158">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="078d4-159">筆記</span><span class="sxs-lookup"><span data-stu-id="078d4-159">NOTES</span></span>

## <span data-ttu-id="078d4-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="078d4-160">RELATED LINKS</span></span>

[<span data-ttu-id="078d4-161">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="078d4-161">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="078d4-162">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="078d4-162">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)


[<span data-ttu-id="078d4-163">Undo-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="078d4-163">Undo-AzKeyVaultKeyRemoval</span></span>](./Undo-AzKeyVaultKeyRemoval.md)

