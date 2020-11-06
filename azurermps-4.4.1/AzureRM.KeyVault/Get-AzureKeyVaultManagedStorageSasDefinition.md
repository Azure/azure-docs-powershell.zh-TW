---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: 63187859a4296f37e5af28880f42a487c018288f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446801"
---
# <span data-ttu-id="f42cf-101">Get-AzureKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="f42cf-101">Get-AzureKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="f42cf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f42cf-102">SYNOPSIS</span></span>
<span data-ttu-id="f42cf-103">取得主要電子倉庫管理的儲存 SAS 定義。</span><span class="sxs-lookup"><span data-stu-id="f42cf-103">Gets Key Vault managed Storage SAS Definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f42cf-104">句法</span><span class="sxs-lookup"><span data-stu-id="f42cf-104">SYNTAX</span></span>

### <span data-ttu-id="f42cf-105">ByAccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="f42cf-105">ByAccountName (Default)</span></span>
```
Get-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f42cf-106">ByDefinitionName</span><span class="sxs-lookup"><span data-stu-id="f42cf-106">ByDefinitionName</span></span>
```
Get-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f42cf-107">說明</span><span class="sxs-lookup"><span data-stu-id="f42cf-107">DESCRIPTION</span></span>
<span data-ttu-id="f42cf-108">如果已指定定義的名稱，則會取得主要 Vault 管理的儲存 SAS 定義。</span><span class="sxs-lookup"><span data-stu-id="f42cf-108">Gets a Key Vault managed Storage SAS Definition if the name of the definition is specified.</span></span> <span data-ttu-id="f42cf-109">如果未指定定義名稱，則會列出與保存庫中指定的主要儲存庫管理儲存空間帳戶相關聯的所有 SAS 定義。</span><span class="sxs-lookup"><span data-stu-id="f42cf-109">If the definition name is not specified, then all the SAS definitions associated with the specified Key Vault managed Storage Account in the vault are listed.</span></span>

## <span data-ttu-id="f42cf-110">示例</span><span class="sxs-lookup"><span data-stu-id="f42cf-110">EXAMPLES</span></span>

### <span data-ttu-id="f42cf-111">範例1：列出所有主要 Vault 管理的儲存 SAS 定義</span><span class="sxs-lookup"><span data-stu-id="f42cf-111">Example 1: List all Key Vault managed Storage SAS Definitions</span></span>
```
PS C:\> Get-AzureKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount'
```

<span data-ttu-id="f42cf-112">列出所有與主要 Vault 管理的儲存帳戶 ' mystorageaccount」（由保存庫 ' myvault」所管理）關聯的所有 SAS 定義</span><span class="sxs-lookup"><span data-stu-id="f42cf-112">Lists all the SAS definitions associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'</span></span>

### <span data-ttu-id="f42cf-113">範例2：取得重要的 Vault 管理儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="f42cf-113">Example 2: Get a Key Vault managed Storage Account</span></span>
```
PS C:\> Get-AzureKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasDef'
```

<span data-ttu-id="f42cf-114">取得與主要電子倉庫管理儲存空間帳戶 "mystorageaccount" （由保存庫 ' myvault」所管理）相關聯的 SAS 定義 ' mysasDef」的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="f42cf-114">Gets the details of SAS Definition 'mysasDef' associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'.</span></span>

## <span data-ttu-id="f42cf-115">參數</span><span class="sxs-lookup"><span data-stu-id="f42cf-115">PARAMETERS</span></span>

### <span data-ttu-id="f42cf-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f42cf-116">-AccountName</span></span>
<span data-ttu-id="f42cf-117">保存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="f42cf-117">Vault name.</span></span>
<span data-ttu-id="f42cf-118">Cmdlet 根據名稱和目前所選的環境來構造電子倉庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="f42cf-118">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f42cf-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="f42cf-119">-Name</span></span>
<span data-ttu-id="f42cf-120">儲存區 sas 定義名稱。</span><span class="sxs-lookup"><span data-stu-id="f42cf-120">Storage sas definition name.</span></span>
<span data-ttu-id="f42cf-121">Cmdlet 會從保存庫名稱、目前所選的環境、儲存空間帳戶名稱和 sas 定義名稱來構造儲存 sas 定義的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="f42cf-121">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f42cf-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="f42cf-122">-VaultName</span></span>
<span data-ttu-id="f42cf-123">保存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="f42cf-123">Vault name.</span></span>
<span data-ttu-id="f42cf-124">Cmdlet 根據名稱和目前所選的環境來構造電子倉庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="f42cf-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f42cf-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f42cf-125">-DefaultProfile</span></span>
<span data-ttu-id="f42cf-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f42cf-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f42cf-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f42cf-127">CommonParameters</span></span>
<span data-ttu-id="f42cf-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f42cf-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f42cf-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f42cf-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f42cf-130">輸入</span><span class="sxs-lookup"><span data-stu-id="f42cf-130">INPUTS</span></span>

### <span data-ttu-id="f42cf-131">System.object</span><span class="sxs-lookup"><span data-stu-id="f42cf-131">System.String</span></span>

## <span data-ttu-id="f42cf-132">輸出</span><span class="sxs-lookup"><span data-stu-id="f42cf-132">OUTPUTS</span></span>

### <span data-ttu-id="f42cf-133">[System.object]。清單 ' 1 [KeyVault. ManagedStorageSasDefinitionListItem，KeyVault，版本 = 2.5.0.0，Culture = 中性，PublicKeyToken = null]]。）））</span><span class="sxs-lookup"><span data-stu-id="f42cf-133">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageSasDefinitionListItem, Microsoft.Azure.Commands.KeyVault, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="f42cf-134">ManagedStorageSasDefinition 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="f42cf-134">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageSasDefinition</span></span>

## <span data-ttu-id="f42cf-135">筆記</span><span class="sxs-lookup"><span data-stu-id="f42cf-135">NOTES</span></span>

## <span data-ttu-id="f42cf-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="f42cf-136">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

