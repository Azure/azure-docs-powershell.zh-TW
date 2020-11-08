---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azmanagedhsmkeyremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzManagedHsmKeyRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzManagedHsmKeyRemoval.md
ms.openlocfilehash: be1713584a1d0ce897c1c728f6aa7ae8b6ca3255
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94136726"
---
# <span data-ttu-id="a4f79-101">Undo-AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="a4f79-101">Undo-AzManagedHsmKeyRemoval</span></span>

## <span data-ttu-id="a4f79-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a4f79-102">SYNOPSIS</span></span>
<span data-ttu-id="a4f79-103">將受管理 HSM 中的已刪除金鑰復原成作用中狀態。</span><span class="sxs-lookup"><span data-stu-id="a4f79-103">Recovers a deleted key in a managed HSM into an active state.</span></span>

## <span data-ttu-id="a4f79-104">句法</span><span class="sxs-lookup"><span data-stu-id="a4f79-104">SYNTAX</span></span>

### <span data-ttu-id="a4f79-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="a4f79-105">Default (Default)</span></span>
```
Undo-AzManagedHsmKeyRemoval [-HsmName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4f79-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="a4f79-106">InputObject</span></span>
```
Undo-AzManagedHsmKeyRemoval [-InputObject] <PSDeletedKeyVaultKeyIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4f79-107">說明</span><span class="sxs-lookup"><span data-stu-id="a4f79-107">DESCRIPTION</span></span>
<span data-ttu-id="a4f79-108">**Undo AzManagedHsmKeyRemoval** Cmdlet 會復原先前刪除的金鑰。</span><span class="sxs-lookup"><span data-stu-id="a4f79-108">The **Undo-AzManagedHsmKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="a4f79-109">復原的金鑰將是作用中的，而且可用於所有正常按鍵作業。</span><span class="sxs-lookup"><span data-stu-id="a4f79-109">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="a4f79-110">來電者需要擁有「復原」許可權，才能執行這個作業。</span><span class="sxs-lookup"><span data-stu-id="a4f79-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="a4f79-111">示例</span><span class="sxs-lookup"><span data-stu-id="a4f79-111">EXAMPLES</span></span>

### <span data-ttu-id="a4f79-112">範例1</span><span class="sxs-lookup"><span data-stu-id="a4f79-112">Example 1</span></span>
```powershell
PS C:\> Undo-AzManagedHsmKeyRemoval -HsmName testmhsm -Name testkey001

Vault/HSM Name : testmhsm
Name           : testkey001
Version        : 7cff8510da04433b98144a3e33ad2bae
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey001/7cff8510da04433b98144a3e33ad2bae
Enabled        : True
Expires        :
Not Before     :
Created        : 10/14/2020 10:13:03 AM
Updated        : 10/14/2020 10:13:03 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="a4f79-113">這個命令會將先前刪除的金鑰 ' testkey001 ' 復原為 [作用中] 和 [可用] 的狀態。</span><span class="sxs-lookup"><span data-stu-id="a4f79-113">This command will recover the key 'testkey001' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="a4f79-114">參數</span><span class="sxs-lookup"><span data-stu-id="a4f79-114">PARAMETERS</span></span>

### <span data-ttu-id="a4f79-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4f79-115">-DefaultProfile</span></span>
<span data-ttu-id="a4f79-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a4f79-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4f79-117">-HsmName</span><span class="sxs-lookup"><span data-stu-id="a4f79-117">-HsmName</span></span>
<span data-ttu-id="a4f79-118">HSM 名稱。</span><span class="sxs-lookup"><span data-stu-id="a4f79-118">HSM name.</span></span> <span data-ttu-id="a4f79-119">Cmdlet 根據名稱和目前所選的環境來構造受管理的 HSM 的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="a4f79-119">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="a4f79-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4f79-120">-InputObject</span></span>
<span data-ttu-id="a4f79-121">已刪除的主要物件</span><span class="sxs-lookup"><span data-stu-id="a4f79-121">Deleted key object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4f79-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="a4f79-122">-Name</span></span>
<span data-ttu-id="a4f79-123">索引鍵名稱。</span><span class="sxs-lookup"><span data-stu-id="a4f79-123">Key name.</span></span>
<span data-ttu-id="a4f79-124">Cmdlet 會從 managed HSM 名稱、目前已選取的環境和金鑰名稱來構造金鑰的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="a4f79-124">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4f79-125">-確認</span><span class="sxs-lookup"><span data-stu-id="a4f79-125">-Confirm</span></span>
<span data-ttu-id="a4f79-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a4f79-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4f79-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4f79-127">-WhatIf</span></span>
<span data-ttu-id="a4f79-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a4f79-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4f79-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a4f79-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4f79-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4f79-130">CommonParameters</span></span>
<span data-ttu-id="a4f79-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a4f79-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4f79-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a4f79-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4f79-133">輸入</span><span class="sxs-lookup"><span data-stu-id="a4f79-133">INPUTS</span></span>

### <span data-ttu-id="a4f79-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="a4f79-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="a4f79-135">輸出</span><span class="sxs-lookup"><span data-stu-id="a4f79-135">OUTPUTS</span></span>

### <span data-ttu-id="a4f79-136">PSKeyVaultKey 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="a4f79-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="a4f79-137">筆記</span><span class="sxs-lookup"><span data-stu-id="a4f79-137">NOTES</span></span>

## <span data-ttu-id="a4f79-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="a4f79-138">RELATED LINKS</span></span>

[<span data-ttu-id="a4f79-139">附加 AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="a4f79-139">Add-AzManagedHsmKey</span></span>](./Add-AzManagedHsmKey.md)

[<span data-ttu-id="a4f79-140">備份-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="a4f79-140">Backup-AzManagedHsmKey</span></span>](./Backup-AzManagedHsmKey.md)

[<span data-ttu-id="a4f79-141">移除-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="a4f79-141">Remove-AzManagedHsmKey</span></span>](./Remove-AzManagedHsmKey.md)

[<span data-ttu-id="a4f79-142">Restore-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="a4f79-142">Restore-AzManagedHsmKey</span></span>](./Restore-AzManagedHsmKey.md)

[<span data-ttu-id="a4f79-143">AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="a4f79-143">Get-AzManagedHsmKey</span></span>](./Get-AzManagedHsmKey.md)

[<span data-ttu-id="a4f79-144">更新-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="a4f79-144">Update-AzManagedHsmKey</span></span>](./Update-AzManagedHsmKey.md)