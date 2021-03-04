---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstorageencryptionscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageEncryptionScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageEncryptionScope.md
ms.openlocfilehash: 02d91338063a1c06654fa30cbbf584a6f62ea34a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909302"
---
# <span data-ttu-id="a8e89-101">Get-AzStorageEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="a8e89-101">Get-AzStorageEncryptionScope</span></span>

## <span data-ttu-id="a8e89-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a8e89-102">SYNOPSIS</span></span>
<span data-ttu-id="a8e89-103">從儲存空間帳戶取得或列出加密範圍。</span><span class="sxs-lookup"><span data-stu-id="a8e89-103">Get or list encryption scopes from a Storage account.</span></span>

## <span data-ttu-id="a8e89-104">語法</span><span class="sxs-lookup"><span data-stu-id="a8e89-104">SYNTAX</span></span>

### <span data-ttu-id="a8e89-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="a8e89-105">AccountName (Default)</span></span>
```
Get-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-EncryptionScopeName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8e89-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="a8e89-106">AccountObject</span></span>
```
Get-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> [-EncryptionScopeName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8e89-107">描述</span><span class="sxs-lookup"><span data-stu-id="a8e89-107">DESCRIPTION</span></span>
<span data-ttu-id="a8e89-108">**Get-AzStorageEncryptionScope** Cmdlet 會從儲存空間帳戶取得或列出加密範圍。</span><span class="sxs-lookup"><span data-stu-id="a8e89-108">The **Get-AzStorageEncryptionScope** cmdlet gets or lists encryption scopes from a Storage account.</span></span>

## <span data-ttu-id="a8e89-109">例子</span><span class="sxs-lookup"><span data-stu-id="a8e89-109">EXAMPLES</span></span>

### <span data-ttu-id="a8e89-110">範例 1：取得單一加密範圍</span><span class="sxs-lookup"><span data-stu-id="a8e89-110">Example 1: Get a single encryption scope</span></span>
```
PS C:\> Get-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EncryptionScopeName $scopename


   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source             KeyVaultKeyUri                                         
----      -----    ------             --------------                                         
testscope Disabled Microsoft.Keyvault https://keyvalutname.vault.azure.net:443/keys/keyname
```

<span data-ttu-id="a8e89-111">此命令會獲得單一加密範圍。</span><span class="sxs-lookup"><span data-stu-id="a8e89-111">This command gets a single encryption scope.</span></span>

### <span data-ttu-id="a8e89-112">範例 2：列出儲存空間帳戶的所有加密範圍</span><span class="sxs-lookup"><span data-stu-id="a8e89-112">Example 2: List all encryption scopes of a Storage account</span></span>
```
PS C:\> Get-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" 


   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source             KeyVaultKeyUri                                         
----      -----    ------             --------------                                         
testscope Disabled Microsoft.Keyvault https://keyvalutname.vault.azure.net:443/keys/keyname
scope2    Enabled  Microsoft.Storage
```

<span data-ttu-id="a8e89-113">此命令會列出儲存空間帳戶的所有加密範圍。</span><span class="sxs-lookup"><span data-stu-id="a8e89-113">This command lists all encryption scopes of a Storage account.</span></span>

## <span data-ttu-id="a8e89-114">參數</span><span class="sxs-lookup"><span data-stu-id="a8e89-114">PARAMETERS</span></span>

### <span data-ttu-id="a8e89-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8e89-115">-DefaultProfile</span></span>
<span data-ttu-id="a8e89-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a8e89-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8e89-117">-EncryptionScopeName</span><span class="sxs-lookup"><span data-stu-id="a8e89-117">-EncryptionScopeName</span></span>
<span data-ttu-id="a8e89-118">Azure 儲存體 EncryptionScope 名稱</span><span class="sxs-lookup"><span data-stu-id="a8e89-118">Azure Storage EncryptionScope name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8e89-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8e89-119">-ResourceGroupName</span></span>
<span data-ttu-id="a8e89-120">資源組名。</span><span class="sxs-lookup"><span data-stu-id="a8e89-120">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8e89-121">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="a8e89-121">-StorageAccount</span></span>
<span data-ttu-id="a8e89-122">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="a8e89-122">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a8e89-123">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a8e89-123">-StorageAccountName</span></span>
<span data-ttu-id="a8e89-124">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="a8e89-124">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8e89-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8e89-125">CommonParameters</span></span>
<span data-ttu-id="a8e89-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a8e89-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8e89-127">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="a8e89-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8e89-128">輸入</span><span class="sxs-lookup"><span data-stu-id="a8e89-128">INPUTS</span></span>

### <span data-ttu-id="a8e89-129">Microsoft.Azure.Commands.management.storage.models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a8e89-129">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="a8e89-130">輸出</span><span class="sxs-lookup"><span data-stu-id="a8e89-130">OUTPUTS</span></span>

### <span data-ttu-id="a8e89-131">Microsoft.Azure.Commands.management.storage.models.PSEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="a8e89-131">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span></span>

## <span data-ttu-id="a8e89-132">筆記</span><span class="sxs-lookup"><span data-stu-id="a8e89-132">NOTES</span></span>

## <span data-ttu-id="a8e89-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="a8e89-133">RELATED LINKS</span></span>
