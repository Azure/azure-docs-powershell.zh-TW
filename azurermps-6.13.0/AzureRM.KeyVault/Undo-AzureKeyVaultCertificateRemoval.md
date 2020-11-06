---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultcertificateremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultCertificateRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultCertificateRemoval.md
ms.openlocfilehash: db2b9066524bd21daa1fa65b87554d9b028754de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456063"
---
# <span data-ttu-id="cf11d-101">Undo-AzureKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="cf11d-101">Undo-AzureKeyVaultCertificateRemoval</span></span>

## <span data-ttu-id="cf11d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cf11d-102">SYNOPSIS</span></span>
<span data-ttu-id="cf11d-103">將 [金鑰 vault] 中已刪除的憑證恢復為 [作用中] 狀態。</span><span class="sxs-lookup"><span data-stu-id="cf11d-103">Recovers a deleted certificate in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf11d-104">句法</span><span class="sxs-lookup"><span data-stu-id="cf11d-104">SYNTAX</span></span>

### <span data-ttu-id="cf11d-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="cf11d-105">Default (Default)</span></span>
```
Undo-AzureKeyVaultCertificateRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf11d-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="cf11d-106">InputObject</span></span>
```
Undo-AzureKeyVaultCertificateRemoval [-InputObject] <PSDeletedKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf11d-107">說明</span><span class="sxs-lookup"><span data-stu-id="cf11d-107">DESCRIPTION</span></span>
<span data-ttu-id="cf11d-108">**Undo AzureKeyVaultCertificateRemoval** Cmdlet 會復原先前刪除的憑證。</span><span class="sxs-lookup"><span data-stu-id="cf11d-108">The **Undo-AzureKeyVaultCertificateRemoval** cmdlet will recover a previously deleted certificate.</span></span>
<span data-ttu-id="cf11d-109">復原的憑證將是作用中的，可用於所有作業。</span><span class="sxs-lookup"><span data-stu-id="cf11d-109">The recovered certificate will be active and can be used for all operations.</span></span>
<span data-ttu-id="cf11d-110">來電者需要擁有「復原」許可權，才能執行這個作業。</span><span class="sxs-lookup"><span data-stu-id="cf11d-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="cf11d-111">示例</span><span class="sxs-lookup"><span data-stu-id="cf11d-111">EXAMPLES</span></span>

### <span data-ttu-id="cf11d-112">範例1</span><span class="sxs-lookup"><span data-stu-id="cf11d-112">Example 1</span></span>
```powershell
PS C:\> Undo-AzureKeyVaultCertificateRemoval -VaultName 'MyKeyVault' -Name 'MyCertificate'

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

<span data-ttu-id="cf11d-113">這個命令會將先前已刪除的憑證 ' MyCertificate ' 復原為 [作用中] 和 [可用] 的狀態。</span><span class="sxs-lookup"><span data-stu-id="cf11d-113">This command will recover the certificate 'MyCertificate' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="cf11d-114">參數</span><span class="sxs-lookup"><span data-stu-id="cf11d-114">PARAMETERS</span></span>

### <span data-ttu-id="cf11d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf11d-115">-DefaultProfile</span></span>
<span data-ttu-id="cf11d-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="cf11d-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cf11d-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf11d-117">-InputObject</span></span>
<span data-ttu-id="cf11d-118">已刪除的憑證物件</span><span class="sxs-lookup"><span data-stu-id="cf11d-118">Deleted Certificate object</span></span>

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

### <span data-ttu-id="cf11d-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="cf11d-119">-Name</span></span>
<span data-ttu-id="cf11d-120">憑證名。</span><span class="sxs-lookup"><span data-stu-id="cf11d-120">Certificate name.</span></span>
<span data-ttu-id="cf11d-121">Cmdlet 會從保存庫名稱、目前已選取的 [環境] 和 [憑證名稱] 構造憑證的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="cf11d-121">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment and certificate name.</span></span>

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

### <span data-ttu-id="cf11d-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="cf11d-122">-VaultName</span></span>
<span data-ttu-id="cf11d-123">保存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="cf11d-123">Vault name.</span></span>
<span data-ttu-id="cf11d-124">Cmdlet 根據名稱和目前所選的環境來構造電子倉庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="cf11d-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="cf11d-125">-確認</span><span class="sxs-lookup"><span data-stu-id="cf11d-125">-Confirm</span></span>
<span data-ttu-id="cf11d-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cf11d-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf11d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf11d-127">-WhatIf</span></span>
<span data-ttu-id="cf11d-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cf11d-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf11d-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cf11d-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf11d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf11d-130">CommonParameters</span></span>
<span data-ttu-id="cf11d-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cf11d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf11d-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cf11d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf11d-133">輸入</span><span class="sxs-lookup"><span data-stu-id="cf11d-133">INPUTS</span></span>

### <span data-ttu-id="cf11d-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="cf11d-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span></span>
<span data-ttu-id="cf11d-135">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="cf11d-135">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="cf11d-136">輸出</span><span class="sxs-lookup"><span data-stu-id="cf11d-136">OUTPUTS</span></span>

### <span data-ttu-id="cf11d-137">PSKeyVaultCertificate 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="cf11d-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="cf11d-138">筆記</span><span class="sxs-lookup"><span data-stu-id="cf11d-138">NOTES</span></span>

## <span data-ttu-id="cf11d-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="cf11d-139">RELATED LINKS</span></span>

[<span data-ttu-id="cf11d-140">移除-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="cf11d-140">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)

[<span data-ttu-id="cf11d-141">AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="cf11d-141">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)
