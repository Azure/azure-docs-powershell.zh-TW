---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultcertificateremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultCertificateRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultCertificateRemoval.md
ms.openlocfilehash: 7e9af7cd775726fc57b78f3fdead20f36dca13cb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284679"
---
# <span data-ttu-id="b9a15-101">Undo-AzKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="b9a15-101">Undo-AzKeyVaultCertificateRemoval</span></span>

## <span data-ttu-id="b9a15-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b9a15-102">SYNOPSIS</span></span>
<span data-ttu-id="b9a15-103">將 [金鑰 vault] 中已刪除的憑證恢復為 [作用中] 狀態。</span><span class="sxs-lookup"><span data-stu-id="b9a15-103">Recovers a deleted certificate in a key vault into an active state.</span></span>

## <span data-ttu-id="b9a15-104">句法</span><span class="sxs-lookup"><span data-stu-id="b9a15-104">SYNTAX</span></span>

### <span data-ttu-id="b9a15-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="b9a15-105">Default (Default)</span></span>
```
Undo-AzKeyVaultCertificateRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9a15-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="b9a15-106">InputObject</span></span>
```
Undo-AzKeyVaultCertificateRemoval [-InputObject] <PSDeletedKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9a15-107">說明</span><span class="sxs-lookup"><span data-stu-id="b9a15-107">DESCRIPTION</span></span>
<span data-ttu-id="b9a15-108">**Undo AzKeyVaultCertificateRemoval** Cmdlet 會復原先前刪除的憑證。</span><span class="sxs-lookup"><span data-stu-id="b9a15-108">The **Undo-AzKeyVaultCertificateRemoval** cmdlet will recover a previously deleted certificate.</span></span>
<span data-ttu-id="b9a15-109">復原的憑證將是作用中的，可用於所有作業。</span><span class="sxs-lookup"><span data-stu-id="b9a15-109">The recovered certificate will be active and can be used for all operations.</span></span>
<span data-ttu-id="b9a15-110">來電者需要擁有「復原」許可權，才能執行這個作業。</span><span class="sxs-lookup"><span data-stu-id="b9a15-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="b9a15-111">示例</span><span class="sxs-lookup"><span data-stu-id="b9a15-111">EXAMPLES</span></span>

### <span data-ttu-id="b9a15-112">範例1</span><span class="sxs-lookup"><span data-stu-id="b9a15-112">Example 1</span></span>
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

<span data-ttu-id="b9a15-113">這個命令會將先前已刪除的憑證 ' MyCertificate ' 復原為 [作用中] 和 [可用] 的狀態。</span><span class="sxs-lookup"><span data-stu-id="b9a15-113">This command will recover the certificate 'MyCertificate' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="b9a15-114">參數</span><span class="sxs-lookup"><span data-stu-id="b9a15-114">PARAMETERS</span></span>

### <span data-ttu-id="b9a15-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9a15-115">-DefaultProfile</span></span>
<span data-ttu-id="b9a15-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b9a15-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b9a15-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b9a15-117">-InputObject</span></span>
<span data-ttu-id="b9a15-118">已刪除的憑證物件</span><span class="sxs-lookup"><span data-stu-id="b9a15-118">Deleted Certificate object</span></span>

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

### <span data-ttu-id="b9a15-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="b9a15-119">-Name</span></span>
<span data-ttu-id="b9a15-120">憑證名。</span><span class="sxs-lookup"><span data-stu-id="b9a15-120">Certificate name.</span></span>
<span data-ttu-id="b9a15-121">Cmdlet 會從保存庫名稱、目前已選取的 [環境] 和 [憑證名稱] 構造憑證的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="b9a15-121">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment and certificate name.</span></span>

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

### <span data-ttu-id="b9a15-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="b9a15-122">-VaultName</span></span>
<span data-ttu-id="b9a15-123">保存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="b9a15-123">Vault name.</span></span>
<span data-ttu-id="b9a15-124">Cmdlet 根據名稱和目前所選的環境來構造電子倉庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="b9a15-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="b9a15-125">-確認</span><span class="sxs-lookup"><span data-stu-id="b9a15-125">-Confirm</span></span>
<span data-ttu-id="b9a15-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b9a15-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9a15-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9a15-127">-WhatIf</span></span>
<span data-ttu-id="b9a15-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b9a15-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9a15-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b9a15-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9a15-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9a15-130">CommonParameters</span></span>
<span data-ttu-id="b9a15-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b9a15-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9a15-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b9a15-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9a15-133">輸入</span><span class="sxs-lookup"><span data-stu-id="b9a15-133">INPUTS</span></span>

### <span data-ttu-id="b9a15-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="b9a15-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="b9a15-135">輸出</span><span class="sxs-lookup"><span data-stu-id="b9a15-135">OUTPUTS</span></span>

### <span data-ttu-id="b9a15-136">PSKeyVaultCertificate 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="b9a15-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="b9a15-137">筆記</span><span class="sxs-lookup"><span data-stu-id="b9a15-137">NOTES</span></span>

## <span data-ttu-id="b9a15-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="b9a15-138">RELATED LINKS</span></span>

[<span data-ttu-id="b9a15-139">移除-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="b9a15-139">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

[<span data-ttu-id="b9a15-140">AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="b9a15-140">Get-AzKeyVaultCertificate</span></span>](./Get-AzKeyVaultCertificate.md)
