---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzManagedHsmKey.md
ms.openlocfilehash: 38e0dbf124643a7d669c1787314790166e88f6a9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141647"
---
# <span data-ttu-id="02ae1-101">Restore-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="02ae1-101">Restore-AzManagedHsmKey</span></span>

## <span data-ttu-id="02ae1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="02ae1-102">SYNOPSIS</span></span>
<span data-ttu-id="02ae1-103">從備份金鑰在 managed HSM 中建立金鑰。</span><span class="sxs-lookup"><span data-stu-id="02ae1-103">Creates a key in a managed HSM from a backed-up key.</span></span>

## <span data-ttu-id="02ae1-104">句法</span><span class="sxs-lookup"><span data-stu-id="02ae1-104">SYNTAX</span></span>

### <span data-ttu-id="02ae1-105">ByHsmName (預設) </span><span class="sxs-lookup"><span data-stu-id="02ae1-105">ByHsmName (Default)</span></span>
```
Restore-AzManagedHsmKey [-HsmName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02ae1-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="02ae1-106">ByInputObject</span></span>
```
Restore-AzManagedHsmKey [-InputObject] <PSManagedHsm> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02ae1-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="02ae1-107">ByResourceId</span></span>
```
Restore-AzManagedHsmKey [-ResourceId] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02ae1-108">說明</span><span class="sxs-lookup"><span data-stu-id="02ae1-108">DESCRIPTION</span></span>
<span data-ttu-id="02ae1-109">**Restore-AzManagedHsmKey** Cmdlet 會在指定的受管理 HSM 中建立金鑰。</span><span class="sxs-lookup"><span data-stu-id="02ae1-109">The **Restore-AzManagedHsmKey** cmdlet creates a key in the specified managed HSM.</span></span>
<span data-ttu-id="02ae1-110">此金鑰是輸入檔案中備份金鑰的複本，且與原始金鑰的名稱相同。</span><span class="sxs-lookup"><span data-stu-id="02ae1-110">This key is a replica of the backed-up key in the input file and has the same name as the original key.</span></span>
<span data-ttu-id="02ae1-111">如果受管理的 HSM 已有相同名稱的金鑰，這個 Cmdlet 會失敗，而不會覆寫原始金鑰。</span><span class="sxs-lookup"><span data-stu-id="02ae1-111">If the managed HSM already has a key by the same name, this cmdlet fails instead of overwriting the original key.</span></span>
<span data-ttu-id="02ae1-112">如果備份包含多個版本的金鑰，則會還原所有版本。</span><span class="sxs-lookup"><span data-stu-id="02ae1-112">If the backup contains multiple versions of a key, all versions are restored.</span></span>
<span data-ttu-id="02ae1-113">您還原金鑰的受管理 HSM 可能與您備份金鑰的受管理 HSM 不同。</span><span class="sxs-lookup"><span data-stu-id="02ae1-113">The managed HSM that you restore the key into can be different from the managed HSM that you backed up the key from.</span></span>
<span data-ttu-id="02ae1-114">不過，受管理的 HSM 必須使用相同的訂閱，且位於同一個地理位置的 Azure 區域中 (例如北美) 。</span><span class="sxs-lookup"><span data-stu-id="02ae1-114">However, the managed HSM must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="02ae1-115">請參閱 Microsoft Azure 信任中心 (https://azure.microsoft.com/support/trust-center/) ，瞭解如何將 Azure 區域對應至地理區域。</span><span class="sxs-lookup"><span data-stu-id="02ae1-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="02ae1-116">示例</span><span class="sxs-lookup"><span data-stu-id="02ae1-116">EXAMPLES</span></span>

### <span data-ttu-id="02ae1-117">範例1</span><span class="sxs-lookup"><span data-stu-id="02ae1-117">Example 1</span></span>
```powershell
PS C:\> Restore-AzManagedHsmKey -HsmName testmhsm -InputFile "C:\Backup.blob"

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

<span data-ttu-id="02ae1-118">這個命令會從名為 testmhsm 的受管理 HSM 中，將包含其所有版本之備份檔案的金鑰（包括其所有版本）還原。</span><span class="sxs-lookup"><span data-stu-id="02ae1-118">This command restores a key, including all of its versions, from the backup file named Backup.blob into the managed HSM named testmhsm.</span></span>

## <span data-ttu-id="02ae1-119">參數</span><span class="sxs-lookup"><span data-stu-id="02ae1-119">PARAMETERS</span></span>

### <span data-ttu-id="02ae1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02ae1-120">-DefaultProfile</span></span>
<span data-ttu-id="02ae1-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="02ae1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02ae1-122">-HsmName</span><span class="sxs-lookup"><span data-stu-id="02ae1-122">-HsmName</span></span>
<span data-ttu-id="02ae1-123">HSM 名稱。</span><span class="sxs-lookup"><span data-stu-id="02ae1-123">HSM name.</span></span> <span data-ttu-id="02ae1-124">Cmdlet 根據名稱和目前所選的環境來構造受管理的 HSM 的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="02ae1-124">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHsmName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02ae1-125">-InputFile</span><span class="sxs-lookup"><span data-stu-id="02ae1-125">-InputFile</span></span>
<span data-ttu-id="02ae1-126">輸入檔。</span><span class="sxs-lookup"><span data-stu-id="02ae1-126">Input file.</span></span>
<span data-ttu-id="02ae1-127">包含已備份 blob 的輸入檔</span><span class="sxs-lookup"><span data-stu-id="02ae1-127">The input file containing the backed-up blob</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02ae1-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02ae1-128">-InputObject</span></span>
<span data-ttu-id="02ae1-129">HSM 物件</span><span class="sxs-lookup"><span data-stu-id="02ae1-129">HSM object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02ae1-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="02ae1-130">-ResourceId</span></span>
<span data-ttu-id="02ae1-131">HSM 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="02ae1-131">HSM Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02ae1-132">-確認</span><span class="sxs-lookup"><span data-stu-id="02ae1-132">-Confirm</span></span>
<span data-ttu-id="02ae1-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="02ae1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02ae1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02ae1-134">-WhatIf</span></span>
<span data-ttu-id="02ae1-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="02ae1-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02ae1-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="02ae1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02ae1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02ae1-137">CommonParameters</span></span>
<span data-ttu-id="02ae1-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="02ae1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02ae1-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="02ae1-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02ae1-140">輸入</span><span class="sxs-lookup"><span data-stu-id="02ae1-140">INPUTS</span></span>

### <span data-ttu-id="02ae1-141">PSKeyVaultKeyIdentityItem 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="02ae1-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="02ae1-142">System.object</span><span class="sxs-lookup"><span data-stu-id="02ae1-142">System.String</span></span>

## <span data-ttu-id="02ae1-143">輸出</span><span class="sxs-lookup"><span data-stu-id="02ae1-143">OUTPUTS</span></span>

### <span data-ttu-id="02ae1-144">PSKeyVaultKey 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="02ae1-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="02ae1-145">筆記</span><span class="sxs-lookup"><span data-stu-id="02ae1-145">NOTES</span></span>

## <span data-ttu-id="02ae1-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="02ae1-146">RELATED LINKS</span></span>

[<span data-ttu-id="02ae1-147">附加 AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="02ae1-147">Add-AzManagedHsmKey</span></span>](./Add-AzManagedHsmKey.md)

[<span data-ttu-id="02ae1-148">備份-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="02ae1-148">Backup-AzManagedHsmKey</span></span>](./Backup-AzManagedHsmKey.md)

[<span data-ttu-id="02ae1-149">移除-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="02ae1-149">Remove-AzManagedHsmKey</span></span>](./Remove-AzManagedHsmKey.md)

[<span data-ttu-id="02ae1-150">復原-AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="02ae1-150">Undo-AzManagedHsmKeyRemoval</span></span>](./Undo-AzManagedHsmKeyRemoval.md)

[<span data-ttu-id="02ae1-151">AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="02ae1-151">Get-AzManagedHsmKey</span></span>](./Get-AzManagedHsmKey.md)

[<span data-ttu-id="02ae1-152">更新-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="02ae1-152">Update-AzManagedHsmKey</span></span>](./Update-AzManagedHsmKey.md)