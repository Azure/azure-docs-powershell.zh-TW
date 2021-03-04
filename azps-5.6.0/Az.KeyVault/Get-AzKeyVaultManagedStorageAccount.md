---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/get-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 552a696a31b8c5fb26a1c6a17434ef53380d0491
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914825"
---
# <span data-ttu-id="b555f-101">Get-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b555f-101">Get-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="b555f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b555f-102">SYNOPSIS</span></span>
<span data-ttu-id="b555f-103">獲得金鑰保存庫管理的 Azure 儲存帳戶。</span><span class="sxs-lookup"><span data-stu-id="b555f-103">Gets Key Vault managed Azure Storage Accounts.</span></span>

## <span data-ttu-id="b555f-104">語法</span><span class="sxs-lookup"><span data-stu-id="b555f-104">SYNTAX</span></span>

### <span data-ttu-id="b555f-105">ByAccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="b555f-105">ByAccountName (Default)</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-VaultName] <String> [[-AccountName] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b555f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b555f-106">ByInputObject</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVault> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b555f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b555f-107">ByResourceId</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-ResourceId] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b555f-108">描述</span><span class="sxs-lookup"><span data-stu-id="b555f-108">DESCRIPTION</span></span>
<span data-ttu-id="b555f-109">如果指定帳戶名稱，且帳戶金鑰是由指定的保存庫管理，則獲得金鑰保存庫管理的 Azure 儲存帳戶。</span><span class="sxs-lookup"><span data-stu-id="b555f-109">Gets a Key Vault managed Azure Storage Account if the name of the account is specified and the account keys are managed by the specified vault.</span></span> <span data-ttu-id="b555f-110">如果未指定帳戶名稱，會列出所有由指定儲存庫管理之金鑰的帳戶。</span><span class="sxs-lookup"><span data-stu-id="b555f-110">If the account name is not specified, then all the accounts whose keys are managed by specified vault are listed.</span></span>

## <span data-ttu-id="b555f-111">例子</span><span class="sxs-lookup"><span data-stu-id="b555f-111">EXAMPLES</span></span>

### <span data-ttu-id="b555f-112">範例 1：列出所有金鑰保存庫受管理的儲存帳戶</span><span class="sxs-lookup"><span data-stu-id="b555f-112">Example 1: List all Key Vault managed Storage Accounts</span></span>
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

<span data-ttu-id="b555f-113">列出由 "myvault" 庫管理之金鑰的所有帳戶</span><span class="sxs-lookup"><span data-stu-id="b555f-113">Lists all the accounts whose keys are managed by vault 'myvault'</span></span>

### <span data-ttu-id="b555f-114">範例 2：取得金鑰保存庫管理的儲存帳戶</span><span class="sxs-lookup"><span data-stu-id="b555f-114">Example 2: Get a Key Vault managed Storage Account</span></span>
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

<span data-ttu-id="b555f-115">如果金鑰是由保存庫 'myvault' 管理，則獲得金鑰保存庫管理儲存帳戶的'mystorageaccount'詳細資料</span><span class="sxs-lookup"><span data-stu-id="b555f-115">Gets the details of Key Vault managed Storage Account of 'mystorageaccount' if its keys are managed by vault 'myvault'</span></span>

### <span data-ttu-id="b555f-116">範例 3：使用篩選列出所有金鑰保存庫受管理的儲存帳戶</span><span class="sxs-lookup"><span data-stu-id="b555f-116">Example 3: List all Key Vault managed Storage Accounts using filtering</span></span>
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

<span data-ttu-id="b555f-117">列出所有以「測試」為開始由「測試」開始由「myvault」管理之儲存庫「myvault」的帳戶</span><span class="sxs-lookup"><span data-stu-id="b555f-117">Lists all the accounts whose keys are managed by vault 'myvault' that start with "test"</span></span>

## <span data-ttu-id="b555f-118">參數</span><span class="sxs-lookup"><span data-stu-id="b555f-118">PARAMETERS</span></span>

### <span data-ttu-id="b555f-119">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b555f-119">-AccountName</span></span>
<span data-ttu-id="b555f-120">金鑰保存庫受管理的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="b555f-120">Key Vault managed storage account name.</span></span> <span data-ttu-id="b555f-121">Cmdlet 會從保存庫名稱、目前選取的環境和偽造的儲存帳戶名稱建構受管理儲存帳戶名稱的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="b555f-121">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAccountName
Aliases: StorageAccountName, Name

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="b555f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b555f-122">-DefaultProfile</span></span>
<span data-ttu-id="b555f-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="b555f-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b555f-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b555f-124">-InputObject</span></span>
<span data-ttu-id="b555f-125">Vault 物件。</span><span class="sxs-lookup"><span data-stu-id="b555f-125">Vault object.</span></span>

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

### <span data-ttu-id="b555f-126">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="b555f-126">-InRemovedState</span></span>
<span data-ttu-id="b555f-127">指定是否要在輸出中顯示先前刪除的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="b555f-127">Specifies whether to show the previously deleted storage accounts in the output.</span></span>

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

### <span data-ttu-id="b555f-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b555f-128">-ResourceId</span></span>
<span data-ttu-id="b555f-129">Vault 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="b555f-129">Vault resource id.</span></span>

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

### <span data-ttu-id="b555f-130">-VaultName</span><span class="sxs-lookup"><span data-stu-id="b555f-130">-VaultName</span></span>
<span data-ttu-id="b555f-131">儲存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="b555f-131">Vault name.</span></span>
<span data-ttu-id="b555f-132">Cmdlet 會根據名稱和目前選取的環境來建構庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="b555f-132">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="b555f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b555f-133">CommonParameters</span></span>
<span data-ttu-id="b555f-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b555f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b555f-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b555f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b555f-136">輸入</span><span class="sxs-lookup"><span data-stu-id="b555f-136">INPUTS</span></span>

### <span data-ttu-id="b555f-137">Microsoft.Azure.Commands.KeyVault.models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="b555f-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="b555f-138">System.String</span><span class="sxs-lookup"><span data-stu-id="b555f-138">System.String</span></span>

## <span data-ttu-id="b555f-139">輸出</span><span class="sxs-lookup"><span data-stu-id="b555f-139">OUTPUTS</span></span>

### <span data-ttu-id="b555f-140">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="b555f-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

### <span data-ttu-id="b555f-141">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b555f-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

### <span data-ttu-id="b555f-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="b555f-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span></span>

### <span data-ttu-id="b555f-143">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b555f-143">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="b555f-144">筆記</span><span class="sxs-lookup"><span data-stu-id="b555f-144">NOTES</span></span>

## <span data-ttu-id="b555f-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="b555f-145">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

