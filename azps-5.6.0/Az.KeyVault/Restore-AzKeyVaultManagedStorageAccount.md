---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/restore-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 136469819a43dbb918aefebd8134b38ef4a943c7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902041"
---
# <span data-ttu-id="a11db-101">Restore-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a11db-101">Restore-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="a11db-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a11db-102">SYNOPSIS</span></span>
<span data-ttu-id="a11db-103">從備份檔案還原金鑰保存庫中的受管理儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="a11db-103">Restores a managed storage account in a key vault from a backup file.</span></span>

## <span data-ttu-id="a11db-104">語法</span><span class="sxs-lookup"><span data-stu-id="a11db-104">SYNTAX</span></span>

### <span data-ttu-id="a11db-105">ByVaultName (預設) </span><span class="sxs-lookup"><span data-stu-id="a11db-105">ByVaultName (Default)</span></span>
```
Restore-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a11db-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a11db-106">ByInputObject</span></span>
```
Restore-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a11db-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a11db-107">ByResourceId</span></span>
```
Restore-AzKeyVaultManagedStorageAccount [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a11db-108">描述</span><span class="sxs-lookup"><span data-stu-id="a11db-108">DESCRIPTION</span></span>
<span data-ttu-id="a11db-109">**Restore-AzKeyVaultManagedStorageAccount** Cmdlet 會從備份檔案，于指定的金鑰保存庫中建立受管理的儲存帳戶。</span><span class="sxs-lookup"><span data-stu-id="a11db-109">The **Restore-AzKeyVaultManagedStorageAccount** cmdlet creates a managed storage account in the specified key vault from a backup file.</span></span>
<span data-ttu-id="a11db-110">此受管理的儲存帳戶是輸入檔案中備份受管理儲存帳戶的複本，其名稱與原始帳戶相同。</span><span class="sxs-lookup"><span data-stu-id="a11db-110">This managed storage account is a replica of the backed-up managed storage account in the input file and has the same name as the original.</span></span>
<span data-ttu-id="a11db-111">如果金鑰保存庫已經包含相同名稱的受管理儲存空間帳戶，此 Cmdlet 會失敗，而不會覆寫原始帳戶。</span><span class="sxs-lookup"><span data-stu-id="a11db-111">If the key vault already contains a managed storage account by the same name, this cmdlet fails instead of overwriting the original.</span></span>
<span data-ttu-id="a11db-112">還原受管理儲存帳戶的金鑰保存庫，可能會與備份受管理儲存帳戶的金鑰保存庫不同。</span><span class="sxs-lookup"><span data-stu-id="a11db-112">The key vault that you restore the managed storage account into can be different from the key vault that you backed up the managed storage account from.</span></span>
<span data-ttu-id="a11db-113">不過，金鑰庫必須使用相同的訂閱，而且位於位於相同地理位置的 Azure (例如北美地區) 。</span><span class="sxs-lookup"><span data-stu-id="a11db-113">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="a11db-114">請參閱 Microsoft Azure 信任中心 (https://azure.microsoft.com/support/trust-center/) Azure 區域與地理位置的相互比對。</span><span class="sxs-lookup"><span data-stu-id="a11db-114">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="a11db-115">例子</span><span class="sxs-lookup"><span data-stu-id="a11db-115">EXAMPLES</span></span>

### <span data-ttu-id="a11db-116">範例 1：還原備份受管理的儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="a11db-116">Example 1: Restore a backed-up managed storage account</span></span>
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

<span data-ttu-id="a11db-117">此命令會從名為 Backup.blob 的備份檔案還原受管理的儲存空間帳戶，包括所有版本，並還原到名為 MyKeyVault 的金鑰保存庫。</span><span class="sxs-lookup"><span data-stu-id="a11db-117">This command restores a managed storage account, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="a11db-118">參數</span><span class="sxs-lookup"><span data-stu-id="a11db-118">PARAMETERS</span></span>

### <span data-ttu-id="a11db-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a11db-119">-DefaultProfile</span></span>
<span data-ttu-id="a11db-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a11db-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a11db-121">-InputFile</span><span class="sxs-lookup"><span data-stu-id="a11db-121">-InputFile</span></span>
<span data-ttu-id="a11db-122">輸入檔案。</span><span class="sxs-lookup"><span data-stu-id="a11db-122">Input file.</span></span>
<span data-ttu-id="a11db-123">包含備份 Blob 的輸入檔案</span><span class="sxs-lookup"><span data-stu-id="a11db-123">The input file containing the backed-up blob</span></span>

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

### <span data-ttu-id="a11db-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a11db-124">-InputObject</span></span>
<span data-ttu-id="a11db-125">KeyVault 物件</span><span class="sxs-lookup"><span data-stu-id="a11db-125">KeyVault object</span></span>

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

### <span data-ttu-id="a11db-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a11db-126">-ResourceId</span></span>
<span data-ttu-id="a11db-127">KeyVault 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="a11db-127">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="a11db-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="a11db-128">-VaultName</span></span>
<span data-ttu-id="a11db-129">儲存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="a11db-129">Vault name.</span></span>
<span data-ttu-id="a11db-130">Cmdlet 會根據名稱和目前選取的環境來建構庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="a11db-130">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="a11db-131">-確認</span><span class="sxs-lookup"><span data-stu-id="a11db-131">-Confirm</span></span>
<span data-ttu-id="a11db-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a11db-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a11db-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a11db-133">-WhatIf</span></span>
<span data-ttu-id="a11db-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a11db-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a11db-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a11db-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a11db-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a11db-136">CommonParameters</span></span>
<span data-ttu-id="a11db-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a11db-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a11db-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a11db-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a11db-139">輸入</span><span class="sxs-lookup"><span data-stu-id="a11db-139">INPUTS</span></span>

### <span data-ttu-id="a11db-140">Microsoft.Azure.Commands.KeyVault.models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="a11db-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="a11db-141">System.String</span><span class="sxs-lookup"><span data-stu-id="a11db-141">System.String</span></span>

## <span data-ttu-id="a11db-142">輸出</span><span class="sxs-lookup"><span data-stu-id="a11db-142">OUTPUTS</span></span>

### <span data-ttu-id="a11db-143">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a11db-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="a11db-144">筆記</span><span class="sxs-lookup"><span data-stu-id="a11db-144">NOTES</span></span>

## <span data-ttu-id="a11db-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="a11db-145">RELATED LINKS</span></span>
