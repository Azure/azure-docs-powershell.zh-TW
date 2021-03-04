---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 34985F06-4D8D-463B-B113-972666D18485
online version: https://docs.microsoft.com/powershell/module/az.keyvault/remove-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificate.md
ms.openlocfilehash: f1491fcf42ace90efa012778cfb5fec7faeaee07
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908538"
---
# <span data-ttu-id="b5ba2-101">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="b5ba2-101">Remove-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="b5ba2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b5ba2-102">SYNOPSIS</span></span>
<span data-ttu-id="b5ba2-103">從金鑰庫移除憑證。</span><span class="sxs-lookup"><span data-stu-id="b5ba2-103">Removes a certificate from a key vault.</span></span>

## <span data-ttu-id="b5ba2-104">語法</span><span class="sxs-lookup"><span data-stu-id="b5ba2-104">SYNTAX</span></span>

### <span data-ttu-id="b5ba2-105">ByVaultNameAndName (預設) </span><span class="sxs-lookup"><span data-stu-id="b5ba2-105">ByVaultNameAndName (Default)</span></span>
```
Remove-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-InRemovedState] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5ba2-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="b5ba2-106">ByObject</span></span>
```
Remove-AzKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [-InRemovedState] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5ba2-107">描述</span><span class="sxs-lookup"><span data-stu-id="b5ba2-107">DESCRIPTION</span></span>
<span data-ttu-id="b5ba2-108">**Remove-AzKeyVaultCertificate** Cmdlet 會從金鑰庫移除憑證。</span><span class="sxs-lookup"><span data-stu-id="b5ba2-108">The **Remove-AzKeyVaultCertificate** cmdlet removes a certificate from a key vault.</span></span>

## <span data-ttu-id="b5ba2-109">例子</span><span class="sxs-lookup"><span data-stu-id="b5ba2-109">EXAMPLES</span></span>

### <span data-ttu-id="b5ba2-110">範例 1：移除憑證</span><span class="sxs-lookup"><span data-stu-id="b5ba2-110">Example 1: Remove a certificate</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "SelfSigned01" -PassThru -Force

Certificate        : [Subject]
                       CN=contoso.com

                     [Issuer]
                       CN=contoso.com

                     [Serial Number]
                       XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

                     [Not Before]
                       4/11/2018 4:28:39 PM

                     [Not After]
                       10/11/2018 4:38:39 PM

                     [Thumbprint]
                       XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

KeyId              : https://contosokv01.vault.azure.net:443/keys/selfsigned01/968c3920884a435abf8faea11f565456
SecretId           : https://contosokv01.vault.azure.net:443/secrets/selfsigned01/968c3920884a435abf8faea11f565456
Thumbprint         : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
RecoveryLevel      : Purgeable
ScheduledPurgeDate :
DeletedDate        :
Enabled            : True
Expires            : 10/11/2018 11:38:39 PM
NotBefore          : 4/11/2018 11:28:39 PM
Created            : 4/11/2018 11:38:39 PM
Updated            : 4/11/2018 11:38:39 PM
Tags               :
VaultName          : ContosoKV01
Name               : SelfSigned01
Version            : 968c3920884a435abf8faea11f565456
Id                 : https://contosokv01.vault.azure.net:443/certificates/selfsigned01/968c3920884a435abf8faea11f565456
```

<span data-ttu-id="b5ba2-111">此命令會從名為 ContosoKV01 的金鑰庫移除名為 SelfSigned01 的憑證。</span><span class="sxs-lookup"><span data-stu-id="b5ba2-111">This command removes the certificate named SelfSigned01 from the key vault named ContosoKV01.</span></span>
<span data-ttu-id="b5ba2-112">此命令會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="b5ba2-112">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="b5ba2-113">因此，Cmdlet 不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b5ba2-113">Therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="b5ba2-114">範例 2：永久清除從金鑰保存庫刪除的憑證</span><span class="sxs-lookup"><span data-stu-id="b5ba2-114">Example 2: Purge the deleted certificate from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="b5ba2-115">此命令會從名為 Contoso 的金鑰保存庫永久移除名為 "MyCert" 的憑證。</span><span class="sxs-lookup"><span data-stu-id="b5ba2-115">This command permanently removes the certificate named 'MyCert' from the key vault named 'Contoso'.</span></span>
<span data-ttu-id="b5ba2-116">執行此 Cmdlet 需要'清除'許可權，此許可權必須先前已明確授予此金鑰庫的使用者。</span><span class="sxs-lookup"><span data-stu-id="b5ba2-116">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user on this key vault.</span></span>

## <span data-ttu-id="b5ba2-117">參數</span><span class="sxs-lookup"><span data-stu-id="b5ba2-117">PARAMETERS</span></span>

### <span data-ttu-id="b5ba2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5ba2-118">-DefaultProfile</span></span>
<span data-ttu-id="b5ba2-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="b5ba2-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b5ba2-120">-強制</span><span class="sxs-lookup"><span data-stu-id="b5ba2-120">-Force</span></span>
<span data-ttu-id="b5ba2-121">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="b5ba2-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b5ba2-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5ba2-122">-InputObject</span></span>
<span data-ttu-id="b5ba2-123">憑證物件。</span><span class="sxs-lookup"><span data-stu-id="b5ba2-123">Certificate Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5ba2-124">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="b5ba2-124">-InRemovedState</span></span>
<span data-ttu-id="b5ba2-125">如果有，會永久移除先前刪除的憑證</span><span class="sxs-lookup"><span data-stu-id="b5ba2-125">If present, removes the previously deleted certificate permanently</span></span>

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

### <span data-ttu-id="b5ba2-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="b5ba2-126">-Name</span></span>
<span data-ttu-id="b5ba2-127">指定此 Cmdlet 從金鑰庫移除的憑證名稱。</span><span class="sxs-lookup"><span data-stu-id="b5ba2-127">Specifies the name of the certificate that this cmdlet removes from a key vault.</span></span>
<span data-ttu-id="b5ba2-128">此 Cmdlet 會根據此參數指定的名稱、金鑰庫的名稱，以及您目前的環境，建構憑證的完全限定功能變數名稱 (FQDN) 。</span><span class="sxs-lookup"><span data-stu-id="b5ba2-128">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultNameAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5ba2-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b5ba2-129">-PassThru</span></span>
<span data-ttu-id="b5ba2-130">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="b5ba2-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b5ba2-131">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="b5ba2-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b5ba2-132">-VaultName</span><span class="sxs-lookup"><span data-stu-id="b5ba2-132">-VaultName</span></span>
<span data-ttu-id="b5ba2-133">指定此 Cmdlet 移除憑證的金鑰庫名稱。</span><span class="sxs-lookup"><span data-stu-id="b5ba2-133">Specifies the name of the key vault from which this cmdlet removes a certificate.</span></span>
<span data-ttu-id="b5ba2-134">此 Cmdlet 會依據此參數指定的名稱和您目前的環境，建構金鑰庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="b5ba2-134">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultNameAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5ba2-135">-確認</span><span class="sxs-lookup"><span data-stu-id="b5ba2-135">-Confirm</span></span>
<span data-ttu-id="b5ba2-136">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b5ba2-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5ba2-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5ba2-137">-WhatIf</span></span>
<span data-ttu-id="b5ba2-138">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b5ba2-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5ba2-139">不會執行 Cmdlet。顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b5ba2-139">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5ba2-140">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b5ba2-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5ba2-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5ba2-141">CommonParameters</span></span>
<span data-ttu-id="b5ba2-142">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b5ba2-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5ba2-143">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b5ba2-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5ba2-144">輸入</span><span class="sxs-lookup"><span data-stu-id="b5ba2-144">INPUTS</span></span>

### <span data-ttu-id="b5ba2-145">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="b5ba2-145">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="b5ba2-146">輸出</span><span class="sxs-lookup"><span data-stu-id="b5ba2-146">OUTPUTS</span></span>

### <span data-ttu-id="b5ba2-147">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="b5ba2-147">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span></span>

## <span data-ttu-id="b5ba2-148">筆記</span><span class="sxs-lookup"><span data-stu-id="b5ba2-148">NOTES</span></span>

## <span data-ttu-id="b5ba2-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="b5ba2-149">RELATED LINKS</span></span>

[<span data-ttu-id="b5ba2-150">Add-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="b5ba2-150">Add-AzKeyVaultCertificate</span></span>](./Add-AzKeyVaultCertificate.md)

[<span data-ttu-id="b5ba2-151">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="b5ba2-151">Get-AzKeyVaultCertificate</span></span>](./Get-AzKeyVaultCertificate.md)

[<span data-ttu-id="b5ba2-152">Import-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="b5ba2-152">Import-AzKeyVaultCertificate</span></span>](./Import-AzKeyVaultCertificate.md)

[<span data-ttu-id="b5ba2-153">Undo-AzKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="b5ba2-153">Undo-AzKeyVaultCertificateRemoval</span></span>](./Undo-AzKeyVaultCertificateRemoval.md)
