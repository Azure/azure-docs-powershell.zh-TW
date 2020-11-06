---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultsecretremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultSecretRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultSecretRemoval.md
ms.openlocfilehash: ecc22deb6be4f8fe85b66454091f6bfbd01d3a80
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449097"
---
# <span data-ttu-id="d77fa-101">Undo-AzureKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="d77fa-101">Undo-AzureKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="d77fa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d77fa-102">SYNOPSIS</span></span>
<span data-ttu-id="d77fa-103">將 [金鑰 vault] 中已刪除的機密恢復為 [作用中] 狀態。</span><span class="sxs-lookup"><span data-stu-id="d77fa-103">Recovers a deleted secret in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d77fa-104">句法</span><span class="sxs-lookup"><span data-stu-id="d77fa-104">SYNTAX</span></span>

### <span data-ttu-id="d77fa-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="d77fa-105">Default (Default)</span></span>
```
Undo-AzureKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d77fa-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="d77fa-106">InputObject</span></span>
```
Undo-AzureKeyVaultSecretRemoval [-InputObject] <PSDeletedKeyVaultSecretIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d77fa-107">說明</span><span class="sxs-lookup"><span data-stu-id="d77fa-107">DESCRIPTION</span></span>
<span data-ttu-id="d77fa-108">**Undo AzureKeyVaultSecretRemoval** Cmdlet 會復原先前刪除的機密。</span><span class="sxs-lookup"><span data-stu-id="d77fa-108">The **Undo-AzureKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="d77fa-109">復原的秘密將是作用中的，而且可用於所有正常的機密作業。</span><span class="sxs-lookup"><span data-stu-id="d77fa-109">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="d77fa-110">來電者需要擁有「復原」許可權，才能執行這個作業。</span><span class="sxs-lookup"><span data-stu-id="d77fa-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="d77fa-111">示例</span><span class="sxs-lookup"><span data-stu-id="d77fa-111">EXAMPLES</span></span>

### <span data-ttu-id="d77fa-112">範例1</span><span class="sxs-lookup"><span data-stu-id="d77fa-112">Example 1</span></span>
```powershell
PS C:\> Undo-AzureKeyVaultSecretRemoval -VaultName 'MyKeyVault' -Name 'MySecret'

Vault Name   : MyKeyVault
Name         : MySecret
Version      : f622abc7b1394092812f1eb0f85dc91c
Id           : https://mykeyvault.vault.azure.net:443/secrets/mysecret/f622abc7b1394092812f1eb0f85dc91c
Enabled      : True
Expires      :
Not Before   :
Created      : 4/19/2018 5:56:02 PM
Updated      : 4/26/2018 7:48:40 PM
Content Type :
Tags         :
```

<span data-ttu-id="d77fa-113">這個命令會將先前刪除的秘密「MySecret」復原成作用中且可用的狀態。</span><span class="sxs-lookup"><span data-stu-id="d77fa-113">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="d77fa-114">參數</span><span class="sxs-lookup"><span data-stu-id="d77fa-114">PARAMETERS</span></span>

### <span data-ttu-id="d77fa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d77fa-115">-DefaultProfile</span></span>
<span data-ttu-id="d77fa-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="d77fa-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d77fa-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d77fa-117">-InputObject</span></span>
<span data-ttu-id="d77fa-118">已刪除的機密物件</span><span class="sxs-lookup"><span data-stu-id="d77fa-118">Deleted secret object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d77fa-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="d77fa-119">-Name</span></span>
<span data-ttu-id="d77fa-120">[秘密名稱]。</span><span class="sxs-lookup"><span data-stu-id="d77fa-120">Secret name.</span></span>
<span data-ttu-id="d77fa-121">Cmdlet 會從保存庫名稱、目前已選取的環境和密碼來構造秘密的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="d77fa-121">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d77fa-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="d77fa-122">-VaultName</span></span>
<span data-ttu-id="d77fa-123">保存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="d77fa-123">Vault name.</span></span>
<span data-ttu-id="d77fa-124">Cmdlet 根據名稱和目前所選的環境來構造電子倉庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="d77fa-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="d77fa-125">-確認</span><span class="sxs-lookup"><span data-stu-id="d77fa-125">-Confirm</span></span>
<span data-ttu-id="d77fa-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d77fa-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d77fa-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d77fa-127">-WhatIf</span></span>
<span data-ttu-id="d77fa-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d77fa-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d77fa-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d77fa-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d77fa-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d77fa-130">CommonParameters</span></span>
<span data-ttu-id="d77fa-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d77fa-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d77fa-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d77fa-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d77fa-133">輸入</span><span class="sxs-lookup"><span data-stu-id="d77fa-133">INPUTS</span></span>

### <span data-ttu-id="d77fa-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="d77fa-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span></span>
<span data-ttu-id="d77fa-135">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="d77fa-135">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="d77fa-136">輸出</span><span class="sxs-lookup"><span data-stu-id="d77fa-136">OUTPUTS</span></span>

### <span data-ttu-id="d77fa-137">PSKeyVaultSecret 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="d77fa-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="d77fa-138">筆記</span><span class="sxs-lookup"><span data-stu-id="d77fa-138">NOTES</span></span>

## <span data-ttu-id="d77fa-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="d77fa-139">RELATED LINKS</span></span>

[<span data-ttu-id="d77fa-140">移除-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="d77fa-140">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

[<span data-ttu-id="d77fa-141">附加 AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="d77fa-141">Add-AzureKeyVaultSecret</span></span>](./Add-AzureKeyVaultSecret.md)

[<span data-ttu-id="d77fa-142">AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="d77fa-142">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)
