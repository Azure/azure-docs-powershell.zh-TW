---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultCertificate.md
ms.openlocfilehash: 8c4bb4813c2d07577d80743906a4f8155bc81282
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93797669"
---
# <span data-ttu-id="fc5f1-101">Update-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="fc5f1-101">Update-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="fc5f1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fc5f1-102">SYNOPSIS</span></span>
<span data-ttu-id="fc5f1-103">修改憑證的可編輯屬性。</span><span class="sxs-lookup"><span data-stu-id="fc5f1-103">Modifies editable attributes of a certificate.</span></span>

## <span data-ttu-id="fc5f1-104">句法</span><span class="sxs-lookup"><span data-stu-id="fc5f1-104">SYNTAX</span></span>

### <span data-ttu-id="fc5f1-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="fc5f1-105">ByName (Default)</span></span>
```
Update-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fc5f1-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fc5f1-106">ByInputObject</span></span>
```
Update-AzKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [[-Version] <String>]
 [-Enable <Boolean>] [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc5f1-107">說明</span><span class="sxs-lookup"><span data-stu-id="fc5f1-107">DESCRIPTION</span></span>
<span data-ttu-id="fc5f1-108">**AzKeyVaultCertificate** Cmdlet 會修改憑證的可編輯屬性。</span><span class="sxs-lookup"><span data-stu-id="fc5f1-108">The **Update-AzKeyVaultCertificate** cmdlet modifies the editable attributes of a certificate.</span></span>

## <span data-ttu-id="fc5f1-109">示例</span><span class="sxs-lookup"><span data-stu-id="fc5f1-109">EXAMPLES</span></span>

### <span data-ttu-id="fc5f1-110">範例1：修改與憑證相關的標記</span><span class="sxs-lookup"><span data-stu-id="fc5f1-110">Example 1: Modify the tags associated with a certificate</span></span>
```powershell
PS C:\> $Tags = @{ "Team" = "Azure" ; "Role" = "Engg" }
PS C:\> Update-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01" -Tag $Tags -PassThru

Name        : TestCert01
Certificate : [Subject]
                CN=AZURE

              [Issuer]
                CN=AZURE

              [Serial Number]
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

              [Not Before]
                7/27/2016 6:50:01 PM

              [Not After]
                7/27/2018 7:00:01 PM

              [Thumbprint]
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

Id          : https://ContosoKV01.vault.azure.net:443/certificates/TestCert01
KeyId       : https://ContosoKV01.vault.azure.net:443/keys/TestCert01
SecretId    : https://ContosoKV01.vault.azure.net:443/secrets/TestCert01
Thumbprint  : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
Tags        : {[Role, Engg], [Team, Azure]}
Enabled     : True
Created     : 7/28/2016 2:00:01 AM
Updated     : 8/1/2016 5:37:48 PM
```

<span data-ttu-id="fc5f1-111">第一個命令會將一個鍵/值對陣列指派給 $Tags 變數。</span><span class="sxs-lookup"><span data-stu-id="fc5f1-111">The first command assigns an array of key/value pairs to the $Tags variable.</span></span>
<span data-ttu-id="fc5f1-112">第二個命令會將名為 TestCert01 的憑證的 [標記] 值設定為 [$Tags]。</span><span class="sxs-lookup"><span data-stu-id="fc5f1-112">The second command sets the tags value of the certificate named TestCert01 to be $Tags.</span></span>

## <span data-ttu-id="fc5f1-113">參數</span><span class="sxs-lookup"><span data-stu-id="fc5f1-113">PARAMETERS</span></span>

### <span data-ttu-id="fc5f1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc5f1-114">-DefaultProfile</span></span>
<span data-ttu-id="fc5f1-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fc5f1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc5f1-116">-啟用</span><span class="sxs-lookup"><span data-stu-id="fc5f1-116">-Enable</span></span>
<span data-ttu-id="fc5f1-117">如果有的話，請啟用憑證 if 值為 true。</span><span class="sxs-lookup"><span data-stu-id="fc5f1-117">If present, enable a certificate if value is true.</span></span>
<span data-ttu-id="fc5f1-118">如果值為 false，則停用憑證。</span><span class="sxs-lookup"><span data-stu-id="fc5f1-118">Disable a certificate if value is false.</span></span>
<span data-ttu-id="fc5f1-119">如果沒有指定，證書的啟用/停用狀態的現有值會保持不變。</span><span class="sxs-lookup"><span data-stu-id="fc5f1-119">If not specified, the existing value of the certificate's enabled/disabled state remains unchanged.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc5f1-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc5f1-120">-InputObject</span></span>
<span data-ttu-id="fc5f1-121">憑證物件</span><span class="sxs-lookup"><span data-stu-id="fc5f1-121">Certificate object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc5f1-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="fc5f1-122">-Name</span></span>
<span data-ttu-id="fc5f1-123">憑證名。</span><span class="sxs-lookup"><span data-stu-id="fc5f1-123">Certificate name.</span></span>
<span data-ttu-id="fc5f1-124">Cmdlet 會從保存庫名稱、目前已選取的環境和密碼來構造秘密的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="fc5f1-124">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc5f1-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fc5f1-125">-PassThru</span></span>
<span data-ttu-id="fc5f1-126">Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="fc5f1-126">Cmdlet does not return object by default.</span></span>
<span data-ttu-id="fc5f1-127">如果已指定此開關，請傳回 certificate 物件。</span><span class="sxs-lookup"><span data-stu-id="fc5f1-127">If this switch is specified, return certificate object.</span></span>

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

### <span data-ttu-id="fc5f1-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="fc5f1-128">-Tag</span></span>
<span data-ttu-id="fc5f1-129">代表憑證標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="fc5f1-129">A hashtable representing certificate tags.</span></span>
<span data-ttu-id="fc5f1-130">如果未指定，sertificate 的現有標記會保持不變。</span><span class="sxs-lookup"><span data-stu-id="fc5f1-130">If not specified, the existing tags of the sertificate remain unchanged.</span></span>
<span data-ttu-id="fc5f1-131">指定空的 Hashtable 來移除標記。</span><span class="sxs-lookup"><span data-stu-id="fc5f1-131">Remove a tag by specifying an empty Hashtable.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc5f1-132">-VaultName</span><span class="sxs-lookup"><span data-stu-id="fc5f1-132">-VaultName</span></span>
<span data-ttu-id="fc5f1-133">保存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="fc5f1-133">Vault name.</span></span>
<span data-ttu-id="fc5f1-134">Cmdlet 根據名稱和目前所選的環境來構造電子倉庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="fc5f1-134">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc5f1-135">-版本</span><span class="sxs-lookup"><span data-stu-id="fc5f1-135">-Version</span></span>
<span data-ttu-id="fc5f1-136">憑證版本。</span><span class="sxs-lookup"><span data-stu-id="fc5f1-136">Certificate version.</span></span>
<span data-ttu-id="fc5f1-137">Cmdlet 會從保存庫名稱、目前已選取的環境、憑證名稱和憑證版本構造憑證的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="fc5f1-137">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment, certificate name and certificate version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc5f1-138">-確認</span><span class="sxs-lookup"><span data-stu-id="fc5f1-138">-Confirm</span></span>
<span data-ttu-id="fc5f1-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fc5f1-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc5f1-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc5f1-140">-WhatIf</span></span>
<span data-ttu-id="fc5f1-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fc5f1-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc5f1-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fc5f1-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc5f1-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc5f1-143">CommonParameters</span></span>
<span data-ttu-id="fc5f1-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fc5f1-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc5f1-145">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="fc5f1-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc5f1-146">輸入</span><span class="sxs-lookup"><span data-stu-id="fc5f1-146">INPUTS</span></span>

### <span data-ttu-id="fc5f1-147">PSKeyVaultCertificateIdentityItem 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="fc5f1-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="fc5f1-148">輸出</span><span class="sxs-lookup"><span data-stu-id="fc5f1-148">OUTPUTS</span></span>

### <span data-ttu-id="fc5f1-149">PSKeyVaultCertificate 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="fc5f1-149">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="fc5f1-150">筆記</span><span class="sxs-lookup"><span data-stu-id="fc5f1-150">NOTES</span></span>

## <span data-ttu-id="fc5f1-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="fc5f1-151">RELATED LINKS</span></span>
