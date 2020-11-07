---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 70ee1aaf9fb082819c626c43ba5c08ad01f0f1d6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795548"
---
# <span data-ttu-id="87075-101">Get-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="87075-101">Get-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="87075-102">摘要</span><span class="sxs-lookup"><span data-stu-id="87075-102">SYNOPSIS</span></span>
<span data-ttu-id="87075-103">取得主要電子倉庫管理的 Azure 儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="87075-103">Gets Key Vault managed Azure Storage Accounts.</span></span>

## <span data-ttu-id="87075-104">句法</span><span class="sxs-lookup"><span data-stu-id="87075-104">SYNTAX</span></span>

### <span data-ttu-id="87075-105">ByVaultName (預設) </span><span class="sxs-lookup"><span data-stu-id="87075-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="87075-106">ByAccountName</span><span class="sxs-lookup"><span data-stu-id="87075-106">ByAccountName</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87075-107">說明</span><span class="sxs-lookup"><span data-stu-id="87075-107">DESCRIPTION</span></span>
<span data-ttu-id="87075-108">如果指定的是帳戶名稱，且帳戶金鑰是由指定的電子倉庫管理，則會取得主要 Vault 管理的 Azure 儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="87075-108">Gets a Key Vault managed Azure Storage Account if the name of the account is specified and the account keys are managed by the specified vault.</span></span> <span data-ttu-id="87075-109">如果未指定帳戶名稱，則會列出其金鑰是由指定的保存庫所管理的所有帳戶。</span><span class="sxs-lookup"><span data-stu-id="87075-109">If the account name is not specified, then all the accounts whose keys are managed by specified vault are listed.</span></span>

## <span data-ttu-id="87075-110">示例</span><span class="sxs-lookup"><span data-stu-id="87075-110">EXAMPLES</span></span>

### <span data-ttu-id="87075-111">範例1：列出所有主要 Vault 管理的儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="87075-111">Example 1: List all Key Vault managed Storage Accounts</span></span>
```
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault'
```

<span data-ttu-id="87075-112">列出由電子倉庫 [myvault] 管理之金鑰的所有帳戶</span><span class="sxs-lookup"><span data-stu-id="87075-112">Lists all the accounts whose keys are managed by vault 'myvault'</span></span>

### <span data-ttu-id="87075-113">範例2：取得重要的 Vault 管理儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="87075-113">Example 2: Get a Key Vault managed Storage Account</span></span>
```
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -Name 'mystorageaccount'
```

<span data-ttu-id="87075-114">取得 "mystorageaccount" 的主要儲存管理儲存空間帳戶的詳細資料（如果其金鑰是由電子倉庫 "myvault" 管理）</span><span class="sxs-lookup"><span data-stu-id="87075-114">Gets the details of Key Vault managed Storage Account of 'mystorageaccount' if its keys are managed by vault 'myvault'</span></span>

## <span data-ttu-id="87075-115">參數</span><span class="sxs-lookup"><span data-stu-id="87075-115">PARAMETERS</span></span>

### <span data-ttu-id="87075-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="87075-116">-AccountName</span></span>
<span data-ttu-id="87075-117">主要保存庫管理的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="87075-117">Key Vault managed storage account name.</span></span> <span data-ttu-id="87075-118">Cmdlet 會從保存庫名稱、目前已選取的環境及 manged 儲存空間帳戶名稱構造受管理儲存空間帳戶名稱的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="87075-118">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: String
Parameter Sets: ByAccountName
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87075-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87075-119">-DefaultProfile</span></span>
<span data-ttu-id="87075-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="87075-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87075-121">-VaultName</span><span class="sxs-lookup"><span data-stu-id="87075-121">-VaultName</span></span>
<span data-ttu-id="87075-122">保存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="87075-122">Vault name.</span></span>
<span data-ttu-id="87075-123">Cmdlet 根據名稱和目前所選的環境來構造電子倉庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="87075-123">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87075-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87075-124">CommonParameters</span></span>
<span data-ttu-id="87075-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="87075-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87075-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="87075-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87075-127">輸入</span><span class="sxs-lookup"><span data-stu-id="87075-127">INPUTS</span></span>

### <span data-ttu-id="87075-128">System.object</span><span class="sxs-lookup"><span data-stu-id="87075-128">System.String</span></span>

## <span data-ttu-id="87075-129">輸出</span><span class="sxs-lookup"><span data-stu-id="87075-129">OUTPUTS</span></span>

### <span data-ttu-id="87075-130">[System.object]。清單 ' 1 [KeyVault. ManagedStorageAccount，KeyVault，版本 = 2.5.0.0，Culture = 中性，PublicKeyToken = null]]。）））</span><span class="sxs-lookup"><span data-stu-id="87075-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount, Microsoft.Azure.Commands.KeyVault, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="87075-131">ManagedStorageAccount 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="87075-131">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="87075-132">筆記</span><span class="sxs-lookup"><span data-stu-id="87075-132">NOTES</span></span>

## <span data-ttu-id="87075-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="87075-133">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

