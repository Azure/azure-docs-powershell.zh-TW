---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/restore-azurekeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 12e1844be497baa24a3b9b4aa9c4e5690564f4ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446985"
---
# <span data-ttu-id="e061c-101">Restore-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e061c-101">Restore-AzureKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="e061c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e061c-102">SYNOPSIS</span></span>
<span data-ttu-id="e061c-103">從備份檔案還原金鑰保存庫中受管理的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="e061c-103">Restores a managed storage account in a key vault from a backup file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e061c-104">句法</span><span class="sxs-lookup"><span data-stu-id="e061c-104">SYNTAX</span></span>

### <span data-ttu-id="e061c-105">ByVaultName (預設) </span><span class="sxs-lookup"><span data-stu-id="e061c-105">ByVaultName (Default)</span></span>
```
Restore-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e061c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e061c-106">ByInputObject</span></span>
```
Restore-AzureKeyVaultManagedStorageAccount [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e061c-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e061c-107">ByResourceId</span></span>
```
Restore-AzureKeyVaultManagedStorageAccount [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e061c-108">說明</span><span class="sxs-lookup"><span data-stu-id="e061c-108">DESCRIPTION</span></span>
<span data-ttu-id="e061c-109">**AzureKeyVaultManagedStorageAccount** Cmdlet 會從備份檔案在指定的金鑰保存庫中建立受管理的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="e061c-109">The **Restore-AzureKeyVaultManagedStorageAccount** cmdlet creates a managed storage account in the specified key vault from a backup file.</span></span>
<span data-ttu-id="e061c-110">這個受管理的儲存空間帳戶是輸入檔案中已備份之受管理儲存空間帳戶的複本，且與原始名稱相同。</span><span class="sxs-lookup"><span data-stu-id="e061c-110">This managed storage account is a replica of the backed-up managed storage account in the input file and has the same name as the original.</span></span>
<span data-ttu-id="e061c-111">如果 [主要電子倉庫] 已經有相同名稱的受管理儲存空間帳戶，這個 Cmdlet 會失敗，而不會覆寫原始的。</span><span class="sxs-lookup"><span data-stu-id="e061c-111">If the key vault already contains a managed storage account by the same name, this cmdlet fails instead of overwriting the original.</span></span>
<span data-ttu-id="e061c-112">您還原受管理的儲存帳戶的主要電子倉庫，可能會與您在其中備份受管理的儲存空間帳戶的主要電子倉庫不同。</span><span class="sxs-lookup"><span data-stu-id="e061c-112">The key vault that you restore the managed storage account into can be different from the key vault that you backed up the managed storage account from.</span></span>
<span data-ttu-id="e061c-113">不過，主要電子倉庫必須使用相同的訂閱，且位於同一個地理位置的 Azure 區域中 (例如北美) 。</span><span class="sxs-lookup"><span data-stu-id="e061c-113">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="e061c-114">請參閱 Microsoft Azure 信任中心 (https://azure.microsoft.com/support/trust-center/) ，瞭解如何將 Azure 區域對應至地理區域。</span><span class="sxs-lookup"><span data-stu-id="e061c-114">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="e061c-115">示例</span><span class="sxs-lookup"><span data-stu-id="e061c-115">EXAMPLES</span></span>

### <span data-ttu-id="e061c-116">範例1：還原已備份的受管理儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="e061c-116">Example 1: Restore a backed-up managed storage account</span></span>
```powershell
PS C:\> Restore-AzureKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"

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

<span data-ttu-id="e061c-117">這個命令會將受管理的儲存空間帳戶（包括其所有版本）從名為 MyKeyVault 的備份檔案中還原到名為的金鑰保存庫。</span><span class="sxs-lookup"><span data-stu-id="e061c-117">This command restores a managed storage account, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="e061c-118">參數</span><span class="sxs-lookup"><span data-stu-id="e061c-118">PARAMETERS</span></span>

### <span data-ttu-id="e061c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e061c-119">-DefaultProfile</span></span>
<span data-ttu-id="e061c-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e061c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e061c-121">-InputFile</span><span class="sxs-lookup"><span data-stu-id="e061c-121">-InputFile</span></span>
<span data-ttu-id="e061c-122">輸入檔。</span><span class="sxs-lookup"><span data-stu-id="e061c-122">Input file.</span></span>
<span data-ttu-id="e061c-123">包含已備份 blob 的輸入檔</span><span class="sxs-lookup"><span data-stu-id="e061c-123">The input file containing the backed-up blob</span></span>

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

### <span data-ttu-id="e061c-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e061c-124">-InputObject</span></span>
<span data-ttu-id="e061c-125">KeyVault 物件</span><span class="sxs-lookup"><span data-stu-id="e061c-125">KeyVault object</span></span>

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

### <span data-ttu-id="e061c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e061c-126">-ResourceId</span></span>
<span data-ttu-id="e061c-127">KeyVault 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="e061c-127">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="e061c-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="e061c-128">-VaultName</span></span>
<span data-ttu-id="e061c-129">保存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="e061c-129">Vault name.</span></span>
<span data-ttu-id="e061c-130">Cmdlet 根據名稱和目前所選的環境來構造電子倉庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="e061c-130">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="e061c-131">-確認</span><span class="sxs-lookup"><span data-stu-id="e061c-131">-Confirm</span></span>
<span data-ttu-id="e061c-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e061c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e061c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e061c-133">-WhatIf</span></span>
<span data-ttu-id="e061c-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e061c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e061c-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e061c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e061c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e061c-136">CommonParameters</span></span>
<span data-ttu-id="e061c-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e061c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e061c-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e061c-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e061c-139">輸入</span><span class="sxs-lookup"><span data-stu-id="e061c-139">INPUTS</span></span>

### <span data-ttu-id="e061c-140">PSKeyVault 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="e061c-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="e061c-141">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="e061c-141">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="e061c-142">System.object</span><span class="sxs-lookup"><span data-stu-id="e061c-142">System.String</span></span>

## <span data-ttu-id="e061c-143">輸出</span><span class="sxs-lookup"><span data-stu-id="e061c-143">OUTPUTS</span></span>

### <span data-ttu-id="e061c-144">PSKeyVaultManagedStorageAccount 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="e061c-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="e061c-145">筆記</span><span class="sxs-lookup"><span data-stu-id="e061c-145">NOTES</span></span>

## <span data-ttu-id="e061c-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="e061c-146">RELATED LINKS</span></span>
