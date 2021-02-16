---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultsecretremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
ms.openlocfilehash: 9513cba1532ec70acb77cdf97d19de25db36434f
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100397929"
---
# <span data-ttu-id="1ea77-101">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="1ea77-101">Undo-AzKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="1ea77-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1ea77-102">SYNOPSIS</span></span>
<span data-ttu-id="1ea77-103">將金鑰庫中已刪除的機密復原為使用中狀態。</span><span class="sxs-lookup"><span data-stu-id="1ea77-103">Recovers a deleted secret in a key vault into an active state.</span></span>

## <span data-ttu-id="1ea77-104">語法</span><span class="sxs-lookup"><span data-stu-id="1ea77-104">SYNTAX</span></span>

### <span data-ttu-id="1ea77-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="1ea77-105">Default (Default)</span></span>
```
Undo-AzKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ea77-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="1ea77-106">InputObject</span></span>
```
Undo-AzKeyVaultSecretRemoval [-InputObject] <PSDeletedKeyVaultSecretIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ea77-107">描述</span><span class="sxs-lookup"><span data-stu-id="1ea77-107">DESCRIPTION</span></span>
<span data-ttu-id="1ea77-108">**Undo-AzKeyVaultSecretRemoval Cmdlet** 會復原先前刪除的機密。</span><span class="sxs-lookup"><span data-stu-id="1ea77-108">The **Undo-AzKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="1ea77-109">已復原的機密將會為使用中，而且可用於所有一般機密作業。</span><span class="sxs-lookup"><span data-stu-id="1ea77-109">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="1ea77-110">來電者必須擁有復原許可權，才能執行此作業。</span><span class="sxs-lookup"><span data-stu-id="1ea77-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="1ea77-111">例子</span><span class="sxs-lookup"><span data-stu-id="1ea77-111">EXAMPLES</span></span>

### <span data-ttu-id="1ea77-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="1ea77-112">Example 1</span></span>
```powershell
PS C:\> Undo-AzKeyVaultSecretRemoval -VaultName 'MyKeyVault' -Name 'MySecret'

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

<span data-ttu-id="1ea77-113">此命令將會將先前刪除的機密 MySecret 復原為使用中且可使用的狀態。</span><span class="sxs-lookup"><span data-stu-id="1ea77-113">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="1ea77-114">參數</span><span class="sxs-lookup"><span data-stu-id="1ea77-114">PARAMETERS</span></span>

### <span data-ttu-id="1ea77-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ea77-115">-DefaultProfile</span></span>
<span data-ttu-id="1ea77-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="1ea77-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1ea77-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1ea77-117">-InputObject</span></span>
<span data-ttu-id="1ea77-118">已刪除的機密物件</span><span class="sxs-lookup"><span data-stu-id="1ea77-118">Deleted secret object</span></span>

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

### <span data-ttu-id="1ea77-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="1ea77-119">-Name</span></span>
<span data-ttu-id="1ea77-120">機密名稱。</span><span class="sxs-lookup"><span data-stu-id="1ea77-120">Secret name.</span></span>
<span data-ttu-id="1ea77-121">Cmdlet 會從儲存庫名稱、目前選取的環境和機密名稱建構一個機密的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="1ea77-121">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="1ea77-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="1ea77-122">-VaultName</span></span>
<span data-ttu-id="1ea77-123">儲存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="1ea77-123">Vault name.</span></span>
<span data-ttu-id="1ea77-124">Cmdlet 會根據名稱和目前選取的環境來建構庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="1ea77-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="1ea77-125">-確認</span><span class="sxs-lookup"><span data-stu-id="1ea77-125">-Confirm</span></span>
<span data-ttu-id="1ea77-126">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="1ea77-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ea77-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ea77-127">-WhatIf</span></span>
<span data-ttu-id="1ea77-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1ea77-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ea77-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1ea77-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ea77-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ea77-130">CommonParameters</span></span>
<span data-ttu-id="1ea77-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1ea77-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ea77-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1ea77-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ea77-133">輸入</span><span class="sxs-lookup"><span data-stu-id="1ea77-133">INPUTS</span></span>

### <span data-ttu-id="1ea77-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="1ea77-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="1ea77-135">輸出</span><span class="sxs-lookup"><span data-stu-id="1ea77-135">OUTPUTS</span></span>

### <span data-ttu-id="1ea77-136">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="1ea77-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="1ea77-137">筆記</span><span class="sxs-lookup"><span data-stu-id="1ea77-137">NOTES</span></span>

## <span data-ttu-id="1ea77-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="1ea77-138">RELATED LINKS</span></span>

[<span data-ttu-id="1ea77-139">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="1ea77-139">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)


[<span data-ttu-id="1ea77-140">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="1ea77-140">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)
