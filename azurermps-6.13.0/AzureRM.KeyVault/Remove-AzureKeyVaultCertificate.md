---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 34985F06-4D8D-463B-B113-972666D18485
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificate.md
ms.openlocfilehash: 8498ea769f8f9a3f7107cb7dd883e79633b9aff7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624052"
---
# <span data-ttu-id="48991-101">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="48991-101">Remove-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="48991-102">摘要</span><span class="sxs-lookup"><span data-stu-id="48991-102">SYNOPSIS</span></span>
<span data-ttu-id="48991-103">移除金鑰保存庫的憑證。</span><span class="sxs-lookup"><span data-stu-id="48991-103">Removes a certificate from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48991-104">句法</span><span class="sxs-lookup"><span data-stu-id="48991-104">SYNTAX</span></span>

### <span data-ttu-id="48991-105">ByVaultNameAndName (預設) </span><span class="sxs-lookup"><span data-stu-id="48991-105">ByVaultNameAndName (Default)</span></span>
```
Remove-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-InRemovedState] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48991-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="48991-106">ByObject</span></span>
```
Remove-AzureKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [-InRemovedState] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48991-107">說明</span><span class="sxs-lookup"><span data-stu-id="48991-107">DESCRIPTION</span></span>
<span data-ttu-id="48991-108">**AzureKeyVaultCertificate** Cmdlet 會從金鑰保存庫中移除憑證。</span><span class="sxs-lookup"><span data-stu-id="48991-108">The **Remove-AzureKeyVaultCertificate** cmdlet removes a certificate from a key vault.</span></span>

## <span data-ttu-id="48991-109">示例</span><span class="sxs-lookup"><span data-stu-id="48991-109">EXAMPLES</span></span>

### <span data-ttu-id="48991-110">範例1：移除憑證</span><span class="sxs-lookup"><span data-stu-id="48991-110">Example 1: Remove a certificate</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "SelfSigned01" -PassThru -Force

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

<span data-ttu-id="48991-111">這個命令會從名為 ContosoKV01 的主要電子倉庫中移除名為 SelfSigned01 的憑證。</span><span class="sxs-lookup"><span data-stu-id="48991-111">This command removes the certificate named SelfSigned01 from the key vault named ContosoKV01.</span></span>
<span data-ttu-id="48991-112">這個命令會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="48991-112">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="48991-113">因此，Cmdlet 不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="48991-113">Therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="48991-114">範例2：從金鑰保存庫永久清除已刪除的憑證</span><span class="sxs-lookup"><span data-stu-id="48991-114">Example 2: Purge the deleted certificate from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="48991-115">這個命令會永久移除名為「Contoso」的金鑰保存庫中名為「MyCert」的憑證。</span><span class="sxs-lookup"><span data-stu-id="48991-115">This command permanently removes the certificate named 'MyCert' from the key vault named 'Contoso'.</span></span>
<span data-ttu-id="48991-116">執行此 Cmdlet 需要「清除」許可權，該許可權必須在此金鑰保存庫上預先授與使用者。</span><span class="sxs-lookup"><span data-stu-id="48991-116">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user on this key vault.</span></span>

## <span data-ttu-id="48991-117">參數</span><span class="sxs-lookup"><span data-stu-id="48991-117">PARAMETERS</span></span>

### <span data-ttu-id="48991-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48991-118">-DefaultProfile</span></span>
<span data-ttu-id="48991-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="48991-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="48991-120">-Force</span><span class="sxs-lookup"><span data-stu-id="48991-120">-Force</span></span>
<span data-ttu-id="48991-121">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="48991-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="48991-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48991-122">-InputObject</span></span>
<span data-ttu-id="48991-123">[憑證] 物件。</span><span class="sxs-lookup"><span data-stu-id="48991-123">Certificate Object.</span></span>

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

### <span data-ttu-id="48991-124">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="48991-124">-InRemovedState</span></span>
<span data-ttu-id="48991-125">如果有，則會永久移除先前刪除的憑證</span><span class="sxs-lookup"><span data-stu-id="48991-125">If present, removes the previously deleted certificate permanently</span></span>

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

### <span data-ttu-id="48991-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="48991-126">-Name</span></span>
<span data-ttu-id="48991-127">指定此 Cmdlet 從金鑰保存庫移除之憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="48991-127">Specifies the name of the certificate that this cmdlet removes from a key vault.</span></span>
<span data-ttu-id="48991-128">這個 Cmdlet 會根據此參數指定的名稱、主要電子倉庫的名稱和您目前的環境，來構造完整的功能變數名稱 (FQDN) 。</span><span class="sxs-lookup"><span data-stu-id="48991-128">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="48991-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="48991-129">-PassThru</span></span>
<span data-ttu-id="48991-130">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="48991-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="48991-131">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="48991-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="48991-132">-VaultName</span><span class="sxs-lookup"><span data-stu-id="48991-132">-VaultName</span></span>
<span data-ttu-id="48991-133">指定此 Cmdlet 移除憑證的主要電子倉庫名稱。</span><span class="sxs-lookup"><span data-stu-id="48991-133">Specifies the name of the key vault from which this cmdlet removes a certificate.</span></span>
<span data-ttu-id="48991-134">這個 Cmdlet 會根據此參數指定的名稱和您目前的環境，來構造金鑰 vault 的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="48991-134">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="48991-135">-確認</span><span class="sxs-lookup"><span data-stu-id="48991-135">-Confirm</span></span>
<span data-ttu-id="48991-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="48991-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48991-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48991-137">-WhatIf</span></span>
<span data-ttu-id="48991-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="48991-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48991-139">未執行 Cmdlet。顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="48991-139">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48991-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="48991-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48991-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48991-141">CommonParameters</span></span>
<span data-ttu-id="48991-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="48991-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48991-143">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="48991-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48991-144">輸入</span><span class="sxs-lookup"><span data-stu-id="48991-144">INPUTS</span></span>

### <span data-ttu-id="48991-145">PSKeyVaultCertificateIdentityItem 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="48991-145">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>
<span data-ttu-id="48991-146">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="48991-146">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="48991-147">輸出</span><span class="sxs-lookup"><span data-stu-id="48991-147">OUTPUTS</span></span>

### <span data-ttu-id="48991-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="48991-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span></span>

## <span data-ttu-id="48991-149">筆記</span><span class="sxs-lookup"><span data-stu-id="48991-149">NOTES</span></span>

## <span data-ttu-id="48991-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="48991-150">RELATED LINKS</span></span>

[<span data-ttu-id="48991-151">附加 AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="48991-151">Add-AzureKeyVaultCertificate</span></span>](./Add-AzureKeyVaultCertificate.md)

[<span data-ttu-id="48991-152">AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="48991-152">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)

[<span data-ttu-id="48991-153">匯入-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="48991-153">Import-AzureKeyVaultCertificate</span></span>](./Import-AzureKeyVaultCertificate.md)

[<span data-ttu-id="48991-154">復原-AzureKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="48991-154">Undo-AzureKeyVaultCertificateRemoval</span></span>](./Undo-AzureKeyVaultCertificateRemoval.md)
