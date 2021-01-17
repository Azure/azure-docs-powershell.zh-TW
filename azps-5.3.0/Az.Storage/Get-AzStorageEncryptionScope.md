---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageencryptionscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageEncryptionScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageEncryptionScope.md
ms.openlocfilehash: cdc2f8b1742625feb042865a9b75e2c495d7aac2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98436069"
---
# <span data-ttu-id="397c1-101">Get-AzStorageEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="397c1-101">Get-AzStorageEncryptionScope</span></span>

## <span data-ttu-id="397c1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="397c1-102">SYNOPSIS</span></span>
<span data-ttu-id="397c1-103">從儲存空間帳戶取得或列出加密範圍。</span><span class="sxs-lookup"><span data-stu-id="397c1-103">Get or list encryption scopes from a Storage account.</span></span>

## <span data-ttu-id="397c1-104">句法</span><span class="sxs-lookup"><span data-stu-id="397c1-104">SYNTAX</span></span>

### <span data-ttu-id="397c1-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="397c1-105">AccountName (Default)</span></span>
```
Get-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-EncryptionScopeName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="397c1-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="397c1-106">AccountObject</span></span>
```
Get-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> [-EncryptionScopeName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="397c1-107">說明</span><span class="sxs-lookup"><span data-stu-id="397c1-107">DESCRIPTION</span></span>
<span data-ttu-id="397c1-108">**AzStorageEncryptionScope** Cmdlet 會從儲存空間帳戶取得或列出加密範圍。</span><span class="sxs-lookup"><span data-stu-id="397c1-108">The **Get-AzStorageEncryptionScope** cmdlet gets or lists encryption scopes from a Storage account.</span></span>

## <span data-ttu-id="397c1-109">示例</span><span class="sxs-lookup"><span data-stu-id="397c1-109">EXAMPLES</span></span>

### <span data-ttu-id="397c1-110">範例1：取得單一加密範圍</span><span class="sxs-lookup"><span data-stu-id="397c1-110">Example 1: Get a single encryption scope</span></span>
```
PS C:\> Get-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EncryptionScopeName $scopename


   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source             KeyVaultKeyUri                                         
----      -----    ------             --------------                                         
testscope Disabled Microsoft.Keyvault https://keyvalutname.vault.azure.net:443/keys/keyname
```

<span data-ttu-id="397c1-111">這個命令會取得單一加密範圍。</span><span class="sxs-lookup"><span data-stu-id="397c1-111">This command gets a single encryption scope.</span></span>

### <span data-ttu-id="397c1-112">範例2：列出儲存空間帳戶的所有加密範圍</span><span class="sxs-lookup"><span data-stu-id="397c1-112">Example 2: List all encryption scopes of a Storage account</span></span>
```
PS C:\> Get-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" 


   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source             KeyVaultKeyUri                                         
----      -----    ------             --------------                                         
testscope Disabled Microsoft.Keyvault https://keyvalutname.vault.azure.net:443/keys/keyname
scope2    Enabled  Microsoft.Storage
```

<span data-ttu-id="397c1-113">這個命令會列出儲存空間帳戶的所有加密範圍。</span><span class="sxs-lookup"><span data-stu-id="397c1-113">This command lists all encryption scopes of a Storage account.</span></span>

## <span data-ttu-id="397c1-114">參數</span><span class="sxs-lookup"><span data-stu-id="397c1-114">PARAMETERS</span></span>

### <span data-ttu-id="397c1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="397c1-115">-DefaultProfile</span></span>
<span data-ttu-id="397c1-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="397c1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="397c1-117">-EncryptionScopeName</span><span class="sxs-lookup"><span data-stu-id="397c1-117">-EncryptionScopeName</span></span>
<span data-ttu-id="397c1-118">Azure 儲存空間 EncryptionScope 名稱</span><span class="sxs-lookup"><span data-stu-id="397c1-118">Azure Storage EncryptionScope name</span></span>

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

### <span data-ttu-id="397c1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="397c1-119">-ResourceGroupName</span></span>
<span data-ttu-id="397c1-120">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="397c1-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="397c1-121">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="397c1-121">-StorageAccount</span></span>
<span data-ttu-id="397c1-122">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="397c1-122">Storage account object</span></span>

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

### <span data-ttu-id="397c1-123">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="397c1-123">-StorageAccountName</span></span>
<span data-ttu-id="397c1-124">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="397c1-124">Storage Account Name.</span></span>

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

### <span data-ttu-id="397c1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="397c1-125">CommonParameters</span></span>
<span data-ttu-id="397c1-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="397c1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="397c1-127">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="397c1-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="397c1-128">輸入</span><span class="sxs-lookup"><span data-stu-id="397c1-128">INPUTS</span></span>

### <span data-ttu-id="397c1-129">PSStorageAccount 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="397c1-129">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="397c1-130">輸出</span><span class="sxs-lookup"><span data-stu-id="397c1-130">OUTPUTS</span></span>

### <span data-ttu-id="397c1-131">PSEncryptionScope 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="397c1-131">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span></span>

## <span data-ttu-id="397c1-132">筆記</span><span class="sxs-lookup"><span data-stu-id="397c1-132">NOTES</span></span>

## <span data-ttu-id="397c1-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="397c1-133">RELATED LINKS</span></span>
