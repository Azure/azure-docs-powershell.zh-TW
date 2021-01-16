---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 4750561aed6643c17fed6e42d13551be76635d72
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98274820"
---
# <span data-ttu-id="b5e82-101">Restore-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b5e82-101">Restore-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="b5e82-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b5e82-102">SYNOPSIS</span></span>
<span data-ttu-id="b5e82-103">從備份檔案還原金鑰保存庫中受管理的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="b5e82-103">Restores a managed storage account in a key vault from a backup file.</span></span>

## <span data-ttu-id="b5e82-104">句法</span><span class="sxs-lookup"><span data-stu-id="b5e82-104">SYNTAX</span></span>

### <span data-ttu-id="b5e82-105">ByVaultName (預設) </span><span class="sxs-lookup"><span data-stu-id="b5e82-105">ByVaultName (Default)</span></span>
```
Restore-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5e82-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b5e82-106">ByInputObject</span></span>
```
Restore-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5e82-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b5e82-107">ByResourceId</span></span>
```
Restore-AzKeyVaultManagedStorageAccount [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5e82-108">說明</span><span class="sxs-lookup"><span data-stu-id="b5e82-108">DESCRIPTION</span></span>
<span data-ttu-id="b5e82-109">**AzKeyVaultManagedStorageAccount** Cmdlet 會從備份檔案在指定的金鑰保存庫中建立受管理的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="b5e82-109">The **Restore-AzKeyVaultManagedStorageAccount** cmdlet creates a managed storage account in the specified key vault from a backup file.</span></span>
<span data-ttu-id="b5e82-110">這個受管理的儲存空間帳戶是輸入檔案中已備份之受管理儲存空間帳戶的複本，且與原始名稱相同。</span><span class="sxs-lookup"><span data-stu-id="b5e82-110">This managed storage account is a replica of the backed-up managed storage account in the input file and has the same name as the original.</span></span>
<span data-ttu-id="b5e82-111">如果 [主要電子倉庫] 已經有相同名稱的受管理儲存空間帳戶，這個 Cmdlet 會失敗，而不會覆寫原始的。</span><span class="sxs-lookup"><span data-stu-id="b5e82-111">If the key vault already contains a managed storage account by the same name, this cmdlet fails instead of overwriting the original.</span></span>
<span data-ttu-id="b5e82-112">您還原受管理的儲存帳戶的主要電子倉庫，可能會與您在其中備份受管理的儲存空間帳戶的主要電子倉庫不同。</span><span class="sxs-lookup"><span data-stu-id="b5e82-112">The key vault that you restore the managed storage account into can be different from the key vault that you backed up the managed storage account from.</span></span>
<span data-ttu-id="b5e82-113">不過，主要電子倉庫必須使用相同的訂閱，且位於同一個地理位置的 Azure 區域中 (例如北美) 。</span><span class="sxs-lookup"><span data-stu-id="b5e82-113">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="b5e82-114">請參閱 Microsoft Azure 信任中心 (https://azure.microsoft.com/support/trust-center/) ，瞭解如何將 Azure 區域對應至地理區域。</span><span class="sxs-lookup"><span data-stu-id="b5e82-114">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="b5e82-115">示例</span><span class="sxs-lookup"><span data-stu-id="b5e82-115">EXAMPLES</span></span>

### <span data-ttu-id="b5e82-116">範例1：還原已備份的受管理儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="b5e82-116">Example 1: Restore a backed-up managed storage account</span></span>
```powershell
PS C:\> Restore-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"

Id                  : https://mykeyvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : MyKeyVault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Active Key Name     : key1
Auto Regenerate Key : True
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 5/21/2018 11:55:58 PM
Updated             : 5/21/2018 11:55:58 PM
Tags                :
```

<span data-ttu-id="b5e82-117">這個命令會將受管理的儲存空間帳戶（包括其所有版本）從名為 MyKeyVault 的備份檔案中還原到名為的金鑰保存庫。</span><span class="sxs-lookup"><span data-stu-id="b5e82-117">This command restores a managed storage account, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="b5e82-118">參數</span><span class="sxs-lookup"><span data-stu-id="b5e82-118">PARAMETERS</span></span>

### <span data-ttu-id="b5e82-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5e82-119">-DefaultProfile</span></span>
<span data-ttu-id="b5e82-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b5e82-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5e82-121">-InputFile</span><span class="sxs-lookup"><span data-stu-id="b5e82-121">-InputFile</span></span>
<span data-ttu-id="b5e82-122">輸入檔。</span><span class="sxs-lookup"><span data-stu-id="b5e82-122">Input file.</span></span>
<span data-ttu-id="b5e82-123">包含已備份 blob 的輸入檔</span><span class="sxs-lookup"><span data-stu-id="b5e82-123">The input file containing the backed-up blob</span></span>

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

### <span data-ttu-id="b5e82-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5e82-124">-InputObject</span></span>
<span data-ttu-id="b5e82-125">KeyVault 物件</span><span class="sxs-lookup"><span data-stu-id="b5e82-125">KeyVault object</span></span>

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

### <span data-ttu-id="b5e82-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b5e82-126">-ResourceId</span></span>
<span data-ttu-id="b5e82-127">KeyVault 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="b5e82-127">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="b5e82-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="b5e82-128">-VaultName</span></span>
<span data-ttu-id="b5e82-129">保存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="b5e82-129">Vault name.</span></span>
<span data-ttu-id="b5e82-130">Cmdlet 根據名稱和目前所選的環境來構造電子倉庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="b5e82-130">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="b5e82-131">-確認</span><span class="sxs-lookup"><span data-stu-id="b5e82-131">-Confirm</span></span>
<span data-ttu-id="b5e82-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b5e82-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5e82-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5e82-133">-WhatIf</span></span>
<span data-ttu-id="b5e82-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b5e82-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5e82-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b5e82-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5e82-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5e82-136">CommonParameters</span></span>
<span data-ttu-id="b5e82-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b5e82-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5e82-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b5e82-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5e82-139">輸入</span><span class="sxs-lookup"><span data-stu-id="b5e82-139">INPUTS</span></span>

### <span data-ttu-id="b5e82-140">PSKeyVault 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="b5e82-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="b5e82-141">System.object</span><span class="sxs-lookup"><span data-stu-id="b5e82-141">System.String</span></span>

## <span data-ttu-id="b5e82-142">輸出</span><span class="sxs-lookup"><span data-stu-id="b5e82-142">OUTPUTS</span></span>

### <span data-ttu-id="b5e82-143">PSKeyVaultManagedStorageAccount 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="b5e82-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="b5e82-144">筆記</span><span class="sxs-lookup"><span data-stu-id="b5e82-144">NOTES</span></span>

## <span data-ttu-id="b5e82-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="b5e82-145">RELATED LINKS</span></span>
