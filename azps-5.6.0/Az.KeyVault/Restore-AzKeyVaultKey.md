---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: C4E7ACDF-22FB-4D49-93B3-69E787B7E0CD
online version: https://docs.microsoft.com/powershell/module/az.keyvault/restore-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultKey.md
ms.openlocfilehash: 00ab59f65e20c21760371db06a672df4b40fd193
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917717"
---
# <span data-ttu-id="c61e6-101">Restore-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="c61e6-101">Restore-AzKeyVaultKey</span></span>

## <span data-ttu-id="c61e6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c61e6-102">SYNOPSIS</span></span>
<span data-ttu-id="c61e6-103">從備份金鑰在金鑰庫中建立金鑰。</span><span class="sxs-lookup"><span data-stu-id="c61e6-103">Creates a key in a key vault from a backed-up key.</span></span>

## <span data-ttu-id="c61e6-104">語法</span><span class="sxs-lookup"><span data-stu-id="c61e6-104">SYNTAX</span></span>

### <span data-ttu-id="c61e6-105">ByVaultName (預設) </span><span class="sxs-lookup"><span data-stu-id="c61e6-105">ByVaultName (Default)</span></span>
```
Restore-AzKeyVaultKey [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c61e6-106">HsmByVaultName</span><span class="sxs-lookup"><span data-stu-id="c61e6-106">HsmByVaultName</span></span>
```
Restore-AzKeyVaultKey -HsmName <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c61e6-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c61e6-107">ByInputObject</span></span>
```
Restore-AzKeyVaultKey [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c61e6-108">HsmByInputObject</span><span class="sxs-lookup"><span data-stu-id="c61e6-108">HsmByInputObject</span></span>
```
Restore-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c61e6-109">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c61e6-109">ByResourceId</span></span>
```
Restore-AzKeyVaultKey [-ResourceId] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c61e6-110">HsmByResourceId</span><span class="sxs-lookup"><span data-stu-id="c61e6-110">HsmByResourceId</span></span>
```
Restore-AzKeyVaultKey -HsmResourceId <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c61e6-111">描述</span><span class="sxs-lookup"><span data-stu-id="c61e6-111">DESCRIPTION</span></span>
<span data-ttu-id="c61e6-112">**Restore-AzKeyVaultKey** Cmdlet 會建立指定金鑰庫中的金鑰。</span><span class="sxs-lookup"><span data-stu-id="c61e6-112">The **Restore-AzKeyVaultKey** cmdlet creates a key in the specified key vault.</span></span>
<span data-ttu-id="c61e6-113">此金鑰是輸入檔案中備份金鑰的複本，其名稱與原始金鑰相同。</span><span class="sxs-lookup"><span data-stu-id="c61e6-113">This key is a replica of the backed-up key in the input file and has the same name as the original key.</span></span>
<span data-ttu-id="c61e6-114">如果金鑰庫已經有相同名稱的金鑰，此 Cmdlet 會失敗，而不會覆寫原始金鑰。</span><span class="sxs-lookup"><span data-stu-id="c61e6-114">If the key vault already has a key by the same name, this cmdlet fails instead of overwriting the original key.</span></span>
<span data-ttu-id="c61e6-115">如果備份包含多個版本的金鑰，所有版本會還原。</span><span class="sxs-lookup"><span data-stu-id="c61e6-115">If the backup contains multiple versions of a key, all versions are restored.</span></span>
<span data-ttu-id="c61e6-116">還原金鑰的金鑰庫可能會與備份金鑰的金鑰庫不同。</span><span class="sxs-lookup"><span data-stu-id="c61e6-116">The key vault that you restore the key into can be different from the key vault that you backed up the key from.</span></span>
<span data-ttu-id="c61e6-117">不過，金鑰庫必須使用相同的訂閱，而且位於位於相同地理位置的 Azure (例如北美地區) 。</span><span class="sxs-lookup"><span data-stu-id="c61e6-117">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="c61e6-118">請參閱 Microsoft Azure 信任中心 (https://azure.microsoft.com/support/trust-center/) Azure 區域與地理位置的相互比對。</span><span class="sxs-lookup"><span data-stu-id="c61e6-118">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="c61e6-119">例子</span><span class="sxs-lookup"><span data-stu-id="c61e6-119">EXAMPLES</span></span>

### <span data-ttu-id="c61e6-120">範例 1：還原備份金鑰</span><span class="sxs-lookup"><span data-stu-id="c61e6-120">Example 1: Restore a backed-up key</span></span>
```powershell
PS C:\> Restore-AzKeyVaultKey -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"

Vault Name     : MyKeyVault
Name           : key1
Version        : 394f9379a47a4e2086585468de6c7ae5
Id             : https://mykeyvault.vault.azure.net:443/keys/key1/394f9379a47a4e2086585468de6c7ae5
Enabled        : True
Expires        :
Not Before     :
Created        : 4/6/2018 11:31:36 PM
Updated        : 4/6/2018 11:35:04 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="c61e6-121">此命令會從名為 Backup.blob 的備份檔案將金鑰 ，包括所有版本還原到名為 MyKeyVault 的金鑰保存庫。</span><span class="sxs-lookup"><span data-stu-id="c61e6-121">This command restores a key, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="c61e6-122">參數</span><span class="sxs-lookup"><span data-stu-id="c61e6-122">PARAMETERS</span></span>

### <span data-ttu-id="c61e6-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c61e6-123">-DefaultProfile</span></span>
<span data-ttu-id="c61e6-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="c61e6-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c61e6-125">-HsmName</span><span class="sxs-lookup"><span data-stu-id="c61e6-125">-HsmName</span></span>
<span data-ttu-id="c61e6-126">HSM 名稱。</span><span class="sxs-lookup"><span data-stu-id="c61e6-126">HSM name.</span></span> <span data-ttu-id="c61e6-127">Cmdlet 會根據名稱和目前選取的環境，建構受管理 HSM 的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="c61e6-127">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmByVaultName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c61e6-128">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="c61e6-128">-HsmObject</span></span>
<span data-ttu-id="c61e6-129">HSM 物件</span><span class="sxs-lookup"><span data-stu-id="c61e6-129">HSM object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: HsmByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c61e6-130">-HsmResourceId</span><span class="sxs-lookup"><span data-stu-id="c61e6-130">-HsmResourceId</span></span>
<span data-ttu-id="c61e6-131">Hsm 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="c61e6-131">Hsm Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: HsmByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c61e6-132">-InputFile</span><span class="sxs-lookup"><span data-stu-id="c61e6-132">-InputFile</span></span>
<span data-ttu-id="c61e6-133">指定包含要還原之金鑰備份的輸入檔案。</span><span class="sxs-lookup"><span data-stu-id="c61e6-133">Specifies the input file that contains the backup of the key to restore.</span></span>

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

### <span data-ttu-id="c61e6-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c61e6-134">-InputObject</span></span>
<span data-ttu-id="c61e6-135">KeyVault 物件</span><span class="sxs-lookup"><span data-stu-id="c61e6-135">KeyVault object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c61e6-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c61e6-136">-ResourceId</span></span>
<span data-ttu-id="c61e6-137">KeyVault 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="c61e6-137">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="c61e6-138">-VaultName</span><span class="sxs-lookup"><span data-stu-id="c61e6-138">-VaultName</span></span>
<span data-ttu-id="c61e6-139">指定要還原金鑰的金鑰庫名稱。</span><span class="sxs-lookup"><span data-stu-id="c61e6-139">Specifies the name of the key vault into which to restore the key.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c61e6-140">-確認</span><span class="sxs-lookup"><span data-stu-id="c61e6-140">-Confirm</span></span>
<span data-ttu-id="c61e6-141">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c61e6-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c61e6-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c61e6-142">-WhatIf</span></span>
<span data-ttu-id="c61e6-143">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c61e6-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c61e6-144">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c61e6-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c61e6-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c61e6-145">CommonParameters</span></span>
<span data-ttu-id="c61e6-146">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c61e6-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c61e6-147">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c61e6-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c61e6-148">輸入</span><span class="sxs-lookup"><span data-stu-id="c61e6-148">INPUTS</span></span>

### <span data-ttu-id="c61e6-149">Microsoft.Azure.Commands.KeyVault.models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="c61e6-149">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="c61e6-150">System.String</span><span class="sxs-lookup"><span data-stu-id="c61e6-150">System.String</span></span>

## <span data-ttu-id="c61e6-151">輸出</span><span class="sxs-lookup"><span data-stu-id="c61e6-151">OUTPUTS</span></span>

### <span data-ttu-id="c61e6-152">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="c61e6-152">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="c61e6-153">筆記</span><span class="sxs-lookup"><span data-stu-id="c61e6-153">NOTES</span></span>

## <span data-ttu-id="c61e6-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="c61e6-154">RELATED LINKS</span></span>

[<span data-ttu-id="c61e6-155">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="c61e6-155">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="c61e6-156">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="c61e6-156">Backup-AzKeyVaultKey</span></span>](./Backup-AzKeyVaultKey.md)

[<span data-ttu-id="c61e6-157">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="c61e6-157">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="c61e6-158">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="c61e6-158">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

