---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/undo-azkeyvaultcertificateremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultCertificateRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultCertificateRemoval.md
ms.openlocfilehash: e514ded413eaca5ae5992e452a6b35f78ab6532b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911933"
---
# <span data-ttu-id="65923-101">Undo-AzKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="65923-101">Undo-AzKeyVaultCertificateRemoval</span></span>

## <span data-ttu-id="65923-102">簡介</span><span class="sxs-lookup"><span data-stu-id="65923-102">SYNOPSIS</span></span>
<span data-ttu-id="65923-103">將金鑰庫中已刪除的憑證復原為使用中狀態。</span><span class="sxs-lookup"><span data-stu-id="65923-103">Recovers a deleted certificate in a key vault into an active state.</span></span>

## <span data-ttu-id="65923-104">語法</span><span class="sxs-lookup"><span data-stu-id="65923-104">SYNTAX</span></span>

### <span data-ttu-id="65923-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="65923-105">Default (Default)</span></span>
```
Undo-AzKeyVaultCertificateRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65923-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="65923-106">InputObject</span></span>
```
Undo-AzKeyVaultCertificateRemoval [-InputObject] <PSDeletedKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65923-107">描述</span><span class="sxs-lookup"><span data-stu-id="65923-107">DESCRIPTION</span></span>
<span data-ttu-id="65923-108">**Undo-AzKeyVaultCertificateRemoval** Cmdlet 會復原先前刪除的憑證。</span><span class="sxs-lookup"><span data-stu-id="65923-108">The **Undo-AzKeyVaultCertificateRemoval** cmdlet will recover a previously deleted certificate.</span></span>
<span data-ttu-id="65923-109">復原的憑證將會為使用中，而且可用於所有作業。</span><span class="sxs-lookup"><span data-stu-id="65923-109">The recovered certificate will be active and can be used for all operations.</span></span>
<span data-ttu-id="65923-110">來電者必須擁有復原許可權，才能執行此作業。</span><span class="sxs-lookup"><span data-stu-id="65923-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="65923-111">例子</span><span class="sxs-lookup"><span data-stu-id="65923-111">EXAMPLES</span></span>

### <span data-ttu-id="65923-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="65923-112">Example 1</span></span>
```powershell
PS C:\> Undo-AzKeyVaultCertificateRemoval -VaultName 'MyKeyVault' -Name 'MyCertificate'

Certificate   : [Subject]
                  CN=contoso.com

                [Issuer]
                  CN=contoso.com

                [Serial Number]
                  XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

                [Not Before]
                  5/24/2018 10:58:13 AM

                [Not After]
                  11/24/2018 10:08:13 AM

                [Thumbprint]
                  XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

KeyId         : https://mykeyvault.vault.azure.net:443/keys/mycertificate/7fe415d5518240c1a6fce89986b8d334
SecretId      : https://mykeyvault.vault.azure.net:443/secrets/mycertificate/7fe415d5518240c1a6fce89986b8d334
Thumbprint    : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
RecoveryLevel : Recoverable+Purgeable
Enabled       : True
Expires       : 11/24/2018 6:08:13 PM
NotBefore     : 5/24/2018 5:58:13 PM
Created       : 5/24/2018 6:08:13 PM
Updated       : 5/24/2018 6:08:13 PM
Tags          :
VaultName     : MyKeyVault
Name          : MyCertificate
Version       : 7fe415d5518240c1a6fce89986b8d334
Id            : https://mykeyvault.vault.azure.net:443/certificates/mycertificate/7fe415d5518240c1a6fce89986b8d334
```

<span data-ttu-id="65923-113">此命令將復原先前已刪除的憑證 "MyCertificate"，以進入使用中且可用狀態。</span><span class="sxs-lookup"><span data-stu-id="65923-113">This command will recover the certificate 'MyCertificate' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="65923-114">參數</span><span class="sxs-lookup"><span data-stu-id="65923-114">PARAMETERS</span></span>

### <span data-ttu-id="65923-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65923-115">-DefaultProfile</span></span>
<span data-ttu-id="65923-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="65923-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="65923-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="65923-117">-InputObject</span></span>
<span data-ttu-id="65923-118">已刪除的憑證物件</span><span class="sxs-lookup"><span data-stu-id="65923-118">Deleted Certificate object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65923-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="65923-119">-Name</span></span>
<span data-ttu-id="65923-120">憑證名稱。</span><span class="sxs-lookup"><span data-stu-id="65923-120">Certificate name.</span></span>
<span data-ttu-id="65923-121">Cmdlet 會從庫名稱、目前選取的環境和憑證名稱建構憑證的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="65923-121">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment and certificate name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65923-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="65923-122">-VaultName</span></span>
<span data-ttu-id="65923-123">儲存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="65923-123">Vault name.</span></span>
<span data-ttu-id="65923-124">Cmdlet 會根據名稱和目前選取的環境來建構庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="65923-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65923-125">-確認</span><span class="sxs-lookup"><span data-stu-id="65923-125">-Confirm</span></span>
<span data-ttu-id="65923-126">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="65923-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65923-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65923-127">-WhatIf</span></span>
<span data-ttu-id="65923-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="65923-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65923-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="65923-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65923-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65923-130">CommonParameters</span></span>
<span data-ttu-id="65923-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="65923-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65923-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="65923-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65923-133">輸入</span><span class="sxs-lookup"><span data-stu-id="65923-133">INPUTS</span></span>

### <span data-ttu-id="65923-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="65923-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="65923-135">輸出</span><span class="sxs-lookup"><span data-stu-id="65923-135">OUTPUTS</span></span>

### <span data-ttu-id="65923-136">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="65923-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="65923-137">筆記</span><span class="sxs-lookup"><span data-stu-id="65923-137">NOTES</span></span>

## <span data-ttu-id="65923-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="65923-138">RELATED LINKS</span></span>

[<span data-ttu-id="65923-139">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="65923-139">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

[<span data-ttu-id="65923-140">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="65923-140">Get-AzKeyVaultCertificate</span></span>](./Get-AzKeyVaultCertificate.md)
