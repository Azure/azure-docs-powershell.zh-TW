---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragefileserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileServiceProperty.md
ms.openlocfilehash: 9503f62667405c8e7a652bffc150a747eadb40f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909294"
---
# <span data-ttu-id="310fa-101">Get-AzStorageFileServiceProperty</span><span class="sxs-lookup"><span data-stu-id="310fa-101">Get-AzStorageFileServiceProperty</span></span>

## <span data-ttu-id="310fa-102">簡介</span><span class="sxs-lookup"><span data-stu-id="310fa-102">SYNOPSIS</span></span>
<span data-ttu-id="310fa-103">為 Azure 儲存檔案服務獲取服務屬性。</span><span class="sxs-lookup"><span data-stu-id="310fa-103">Gets service properties for Azure Storage File services.</span></span>

## <span data-ttu-id="310fa-104">語法</span><span class="sxs-lookup"><span data-stu-id="310fa-104">SYNTAX</span></span>

### <span data-ttu-id="310fa-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="310fa-105">AccountName (Default)</span></span>
```
Get-AzStorageFileServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="310fa-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="310fa-106">AccountObject</span></span>
```
Get-AzStorageFileServiceProperty -StorageAccount <PSStorageAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="310fa-107">FileServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="310fa-107">FileServicePropertiesResourceId</span></span>
```
Get-AzStorageFileServiceProperty [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="310fa-108">描述</span><span class="sxs-lookup"><span data-stu-id="310fa-108">DESCRIPTION</span></span>
<span data-ttu-id="310fa-109">**Get-AzStorageFileServiceProperty** Cmdlet 會取得 Azure 儲存體檔服務的服務屬性。</span><span class="sxs-lookup"><span data-stu-id="310fa-109">The **Get-AzStorageFileServiceProperty** cmdlet gets the service properties for Azure Storage File services.</span></span>

## <span data-ttu-id="310fa-110">例子</span><span class="sxs-lookup"><span data-stu-id="310fa-110">EXAMPLES</span></span>

### <span data-ttu-id="310fa-111">範例 1：取得指定儲存帳戶的 Azure 儲存體檔案服務屬性</span><span class="sxs-lookup"><span data-stu-id="310fa-111">Example 1: Get  Azure Storage File services property of a specified Storage Account</span></span>
```powershell
PS C:\> Get-AzStorageFileServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"

StorageAccountName                            : mystorageaccount
ResourceGroupName                             : myresourcegroup
ShareDeleteRetentionPolicy.Enabled            : True
ShareDeleteRetentionPolicy.Days               : 3
```

<span data-ttu-id="310fa-112">此命令會獲得指定儲存帳戶的 File services 屬性。</span><span class="sxs-lookup"><span data-stu-id="310fa-112">This command gets the File services property of a specified Storage Account.</span></span>

## <span data-ttu-id="310fa-113">參數</span><span class="sxs-lookup"><span data-stu-id="310fa-113">PARAMETERS</span></span>

### <span data-ttu-id="310fa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="310fa-114">-DefaultProfile</span></span>
<span data-ttu-id="310fa-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="310fa-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="310fa-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="310fa-116">-ResourceGroupName</span></span>
<span data-ttu-id="310fa-117">資源組名。</span><span class="sxs-lookup"><span data-stu-id="310fa-117">Resource Group Name.</span></span>

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

### <span data-ttu-id="310fa-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="310fa-118">-ResourceId</span></span>
<span data-ttu-id="310fa-119">輸入儲存帳戶資源識別碼或檔案服務屬性資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="310fa-119">Input a Storage account Resource Id, or a File service properties Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: FileServicePropertiesResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="310fa-120">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="310fa-120">-StorageAccount</span></span>
<span data-ttu-id="310fa-121">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="310fa-121">Storage account object</span></span>

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

### <span data-ttu-id="310fa-122">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="310fa-122">-StorageAccountName</span></span>
<span data-ttu-id="310fa-123">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="310fa-123">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="310fa-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="310fa-124">CommonParameters</span></span>
<span data-ttu-id="310fa-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="310fa-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="310fa-126">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="310fa-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="310fa-127">輸入</span><span class="sxs-lookup"><span data-stu-id="310fa-127">INPUTS</span></span>

### <span data-ttu-id="310fa-128">Microsoft.Azure.Commands.management.storage.models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="310fa-128">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="310fa-129">System.String</span><span class="sxs-lookup"><span data-stu-id="310fa-129">System.String</span></span>

## <span data-ttu-id="310fa-130">輸出</span><span class="sxs-lookup"><span data-stu-id="310fa-130">OUTPUTS</span></span>

### <span data-ttu-id="310fa-131">Microsoft.Azure.Commands.management.storage.models.PSFileServiceProperties</span><span class="sxs-lookup"><span data-stu-id="310fa-131">Microsoft.Azure.Commands.Management.Storage.Models.PSFileServiceProperties</span></span>

## <span data-ttu-id="310fa-132">筆記</span><span class="sxs-lookup"><span data-stu-id="310fa-132">NOTES</span></span>

## <span data-ttu-id="310fa-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="310fa-133">RELATED LINKS</span></span>
