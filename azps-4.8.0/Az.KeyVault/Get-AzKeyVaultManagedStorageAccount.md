---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 6e7cbaf9ed6e9f0d9751e8e16004891a7fcbb056
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127832"
---
# <span data-ttu-id="36223-101">Get-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="36223-101">Get-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="36223-102">摘要</span><span class="sxs-lookup"><span data-stu-id="36223-102">SYNOPSIS</span></span>
<span data-ttu-id="36223-103">取得主要電子倉庫管理的 Azure 儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="36223-103">Gets Key Vault managed Azure Storage Accounts.</span></span>

## <span data-ttu-id="36223-104">句法</span><span class="sxs-lookup"><span data-stu-id="36223-104">SYNTAX</span></span>

### <span data-ttu-id="36223-105">ByAccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="36223-105">ByAccountName (Default)</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-VaultName] <String> [[-AccountName] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36223-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="36223-106">ByInputObject</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVault> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36223-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="36223-107">ByResourceId</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-ResourceId] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36223-108">說明</span><span class="sxs-lookup"><span data-stu-id="36223-108">DESCRIPTION</span></span>
<span data-ttu-id="36223-109">如果指定的是帳戶名稱，且帳戶金鑰是由指定的電子倉庫管理，則會取得主要 Vault 管理的 Azure 儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="36223-109">Gets a Key Vault managed Azure Storage Account if the name of the account is specified and the account keys are managed by the specified vault.</span></span> <span data-ttu-id="36223-110">如果未指定帳戶名稱，則會列出其金鑰是由指定的保存庫所管理的所有帳戶。</span><span class="sxs-lookup"><span data-stu-id="36223-110">If the account name is not specified, then all the accounts whose keys are managed by specified vault are listed.</span></span>

## <span data-ttu-id="36223-111">示例</span><span class="sxs-lookup"><span data-stu-id="36223-111">EXAMPLES</span></span>

### <span data-ttu-id="36223-112">範例1：列出所有主要 Vault 管理的儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="36223-112">Example 1: List all Key Vault managed Storage Accounts</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault'

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

<span data-ttu-id="36223-113">列出由電子倉庫 [myvault] 管理之金鑰的所有帳戶</span><span class="sxs-lookup"><span data-stu-id="36223-113">Lists all the accounts whose keys are managed by vault 'myvault'</span></span>

### <span data-ttu-id="36223-114">範例2：取得重要的 Vault 管理儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="36223-114">Example 2: Get a Key Vault managed Storage Account</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -Name 'mystorageaccount'

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/maddie1/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Active Key Name     : key2
Auto Regenerate Key : False
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

<span data-ttu-id="36223-115">取得 "mystorageaccount" 的主要儲存管理儲存空間帳戶的詳細資料（如果其金鑰是由電子倉庫 "myvault" 管理）</span><span class="sxs-lookup"><span data-stu-id="36223-115">Gets the details of Key Vault managed Storage Account of 'mystorageaccount' if its keys are managed by vault 'myvault'</span></span>

### <span data-ttu-id="36223-116">範例3：使用篩選列出所有主要儲存空間管理的儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="36223-116">Example 3: List all Key Vault managed Storage Accounts using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -Name "test*"

Id                  : https://myvault.vault.azure.net:443/storage/test1
Vault Name          : myvault
AccountName         : test1
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/test1
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :

Id                  : https://myvault.vault.azure.net:443/storage/test2
Vault Name          : myvault
AccountName         : test2
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/test2
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

<span data-ttu-id="36223-117">列出其金鑰是由以「test」開頭的保存庫 ' myvault ' 管理的所有帳戶。</span><span class="sxs-lookup"><span data-stu-id="36223-117">Lists all the accounts whose keys are managed by vault 'myvault' that start with "test"</span></span>

## <span data-ttu-id="36223-118">參數</span><span class="sxs-lookup"><span data-stu-id="36223-118">PARAMETERS</span></span>

### <span data-ttu-id="36223-119">-AccountName</span><span class="sxs-lookup"><span data-stu-id="36223-119">-AccountName</span></span>
<span data-ttu-id="36223-120">主要保存庫管理的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="36223-120">Key Vault managed storage account name.</span></span> <span data-ttu-id="36223-121">Cmdlet 會從保存庫名稱、目前已選取的環境及 manged 儲存空間帳戶名稱構造受管理儲存空間帳戶名稱的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="36223-121">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAccountName
Aliases: StorageAccountName, Name

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36223-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36223-122">-DefaultProfile</span></span>
<span data-ttu-id="36223-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="36223-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="36223-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36223-124">-InputObject</span></span>
<span data-ttu-id="36223-125">Vault 物件。</span><span class="sxs-lookup"><span data-stu-id="36223-125">Vault object.</span></span>

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

### <span data-ttu-id="36223-126">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="36223-126">-InRemovedState</span></span>
<span data-ttu-id="36223-127">指定是否要在輸出中顯示先前刪除的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="36223-127">Specifies whether to show the previously deleted storage accounts in the output.</span></span>

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

### <span data-ttu-id="36223-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="36223-128">-ResourceId</span></span>
<span data-ttu-id="36223-129">保存庫資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="36223-129">Vault resource id.</span></span>

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

### <span data-ttu-id="36223-130">-VaultName</span><span class="sxs-lookup"><span data-stu-id="36223-130">-VaultName</span></span>
<span data-ttu-id="36223-131">保存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="36223-131">Vault name.</span></span>
<span data-ttu-id="36223-132">Cmdlet 根據名稱和目前所選的環境來構造電子倉庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="36223-132">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36223-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36223-133">CommonParameters</span></span>
<span data-ttu-id="36223-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="36223-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36223-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="36223-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36223-136">輸入</span><span class="sxs-lookup"><span data-stu-id="36223-136">INPUTS</span></span>

### <span data-ttu-id="36223-137">PSKeyVault 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="36223-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="36223-138">System.object</span><span class="sxs-lookup"><span data-stu-id="36223-138">System.String</span></span>

## <span data-ttu-id="36223-139">輸出</span><span class="sxs-lookup"><span data-stu-id="36223-139">OUTPUTS</span></span>

### <span data-ttu-id="36223-140">PSKeyVaultManagedStorageAccountIdentityItem 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="36223-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

### <span data-ttu-id="36223-141">PSKeyVaultManagedStorageAccount 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="36223-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

### <span data-ttu-id="36223-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="36223-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span></span>

### <span data-ttu-id="36223-143">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="36223-143">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="36223-144">筆記</span><span class="sxs-lookup"><span data-stu-id="36223-144">NOTES</span></span>

## <span data-ttu-id="36223-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="36223-145">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

